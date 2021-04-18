---
title: Fornire attributi di visualizzazione
description: Il Framework di servizi di testo (TSF) consente a un servizio di testo di fornire attributi di visualizzazione per il testo.
ms.assetid: 5809f5b8-0396-4abd-b5fe-61ecc8cd0914
keywords:
- Framework servizi di testo (TSF), attributi di visualizzazione
- TSF (Text Services Framework), attributi di visualizzazione
- Servizi di testo, attributi di visualizzazione
- attributi di visualizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c08f59bb64ef4f06df020a40189d273c703768d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298173"
---
# <a name="providing-display-attributes"></a>Fornire attributi di visualizzazione

Il Framework di servizi di testo (TSF) consente a un servizio di testo di fornire attributi di visualizzazione per il testo. In questo modo è possibile fornire all'utente ulteriori commenti e suggerimenti visivi. Ad esempio, un servizio di testo del correttore ortografico può evidenziare una parola errata con una sottolineatura rossa. Gli attributi di visualizzazione specificati sono definiti dalla struttura [tf \_ DISPLAYATTRIBUTE](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute) e includono il colore del testo, il colore di sfondo del testo, lo stile di sottolineatura, il colore di sottolineatura e il peso della

I client che utilizzano queste informazioni sugli attributi di visualizzazione saranno spesso applicazioni, ma possono includere anche servizi di testo. Il gestore TSF intermedia tra il provider di attributi di visualizzazione e il client e tiene traccia del provider di attributi di visualizzazione degli attributi di visualizzazione specifici.

Per fornire attributi di visualizzazione, un servizio di testo deve eseguire le operazioni seguenti.

1.  Registrare il servizio di testo come provider di attributi di visualizzazione chiamando [ITfCategoryMgr:: RegisterCategory](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registercategory) con l'identificatore di classe del servizio di testo per il primo parametro, GUID \_ TFCAT \_ DISPLAYATTRIBUTEPROVIDER per il secondo parametro e l'identificatore di classe del servizio di testo per il terzo parametro.
2.  Implementare [ITfDisplayAttributeProvider](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeprovider) e renderlo disponibile dal class factory.
3.  Implementare [IEnumTfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-ienumtfdisplayattributeinfo) e renderlo disponibile da [ITfDisplayAttributeProvider:: EnumDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-enumdisplayattributeinfo).
4.  Implementare un oggetto [ITfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo) per ogni tipo di attributo di visualizzazione fornito dal servizio di testo.

## <a name="applying-the-display-attributes"></a>Applicazione degli attributi di visualizzazione

Il servizio di testo deve applicare l'attributo di visualizzazione a un intervallo di testo. Un servizio di testo può modificare il valore della proprietà solo durante una sessione di modifica di lettura/scrittura.

Supponendo che si trovi all'interno di una sessione di modifica di lettura/scrittura, viene applicato un attributo di visualizzazione nel modo seguente.

1.  Ottenere un oggetto [ITfRange](/windows/desktop/api/Msctf/nn-msctf-itfrange) che copra il testo a cui verrà applicato l'attributo di visualizzazione.
2.  Ottenere un oggetto [ITfProperty](/windows/desktop/api/Msctf/nn-msctf-itfproperty) per gli attributi di testo chiamando [ITfContext:: GetProperty](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty) con l' \_ attributo GUID Prop \_ .
3.  Creare un [TfGuidAtom](tfguidatom.md) dal **GUID** identificatore dell'attributo di visualizzazione definito dal servizio di testo chiamando [ITfCategoryMgr:: RegisterGUID](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registerguid).
4.  Inizializzare una variabile VARIANT su VT \_ I4 e impostare il membro **LVal** su **TfGuidAtom** creato nel passaggio precedente.
5.  Applicare l'attributo di visualizzazione all'intervallo chiamando [ITfProperty:: SetValue](/windows/desktop/api/Msctf/nf-msctf-itfproperty-setvalue) con il cookie di modifica di lettura/scrittura, l'intervallo e la variante inizializzata nel passaggio precedente.


```C++
STDAPI CEditSession::DoEditSession(TfEditCookie ec)
{
    HRESULT hr;
    ITfCategoryMgr *pCategoryMgr;
    TfGuidAtom  gaDisplayAttribute = TF_INVALID_GUIDATOM;

    //Create a TfGuidAtom for the display attribute identifier. 
    hr = CoCreateInstance(CLSID_TF_CategoryMgr,
                         NULL, 
                         CLSCTX_INPROC_SERVER, 
                         IID_ITfCategoryMgr, 
                         (void**)&pCategoryMgr);
    
    if(SUCCEEDED(hr))
    {
        hr = pCategoryMgr->RegisterGUID(guidDisplayAttribute, &gaDisplayAttribute);

        pCategoryMgr->Release();
    }
    
    //Apply the display attribute to the selected text. 
    if(TF_INVALID_GUIDATOM != gaDisplayAttribute)
    {
        TF_SELECTION tfSel;
        ULONG cFetched;

        //Get the selection. 
        hr = m_pContext->GetSelection(ec, TF_DEFAULT_SELECTION, 1, &tfSel, &cFetched);
        if(SUCCEEDED(hr) && cFetched)
        {
            ITfProperty *pDisplayAttributeProperty;

            //Get the display attribute property. 
            hr = m_pContext->GetProperty(GUID_PROP_ATTRIBUTE, &pDisplayAttributeProperty);
            if(SUCCEEDED(hr))
            {
                VARIANT var;

                VariantInit(&var);

                //All display attributes are TfGuidAtoms and TfGuidAtoms are VT_I4. 
                var.vt = VT_I4; 
                var.lVal = gaDisplayAttribute;

                //Set the display attribute value over the range. 
                hr = pDisplayAttributeProperty->SetValue(ec, tfSel.range, &var);

                pDisplayAttributeProperty->Release();
            }

            tfSel.range->Release();
        }
    }

    return S_OK;
}
```



## <a name="supplying-the-display-attribute-information-object"></a>Specifica dell'oggetto informazioni sugli attributi di visualizzazione

Un client ottiene un oggetto **ITfDisplayAttributeInfo** in uno dei due modi.

1.  Il client chiama [ITfDisplayAttributeMgr:: GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo) con l'identificatore **GUID** dell'attributo di visualizzazione. La prima volta che il client chiama **ITfDisplayAttributeMgr:: GetDisplayAttributeInfo**, gestione TSF creerà un'istanza del provider di attributi di visualizzazione chiamando CoCreateInstance con l'identificatore di classe passato come primo parametro a **ITfCategoryMgr:: RegisterCategory**. Le chiamate successive a **ITfDisplayAttributeMgr:: GetDisplayAttributeInfo** riutilizzeranno l'oggetto provider di attributi di visualizzazione.

    Gestione TSF chiama quindi [ITfDisplayAttributeProvider:: GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-getdisplayattributeinfo) con il **GUID** dell'attributo di visualizzazione per ottenere l'oggetto **ITfDisplayAttributeInfo** .

    Il gestore di TSF passa quindi l'oggetto **ITfDisplayAttributeInfo** di nuovo al client.

2.  Il client chiama [ITfDisplayAttributeMgr:: EnumDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-enumdisplayattributeinfo) per ottenere un oggetto **IEnumTfDisplayAttributeInfo** che contiene tutti gli attributi di visualizzazione forniti da tutti i provider di attributi di visualizzazione. Gestione TSF enumera ogni provider di attributi di visualizzazione e crea un'istanza di ogni provider chiamando CoCreateInstance con l'identificatore di classe passato come terzo parametro a **ITfCategoryMgr:: RegisterCategory**.

    Il gestore TSF chiama quindi ogni provider **ITfDisplayAttributeProvider:: EnumDisplayAttributeInfo** per ottenere un oggetto **IEnumTfDisplayAttributeInfo** che contiene tutti gli attributi di visualizzazione forniti dal provider.

    Il gestore TSF chiama quindi il metodo [IEnumTfDisplayAttributeInfo:: Next](/windows/desktop/api/Msctf/nf-msctf-ienumtfdisplayattributeinfo-next) del provider, aggiungendo ogni oggetto **ITfDisplayAttributeInfo** ottenuto all'enumeratore own del Manager, fino a quando non viene raggiunta la fine dell'enumerazione del provider.

    Quando tutti gli oggetti **ITfDisplayAttributeInfo** per tutti i provider di attributi di visualizzazione vengono aggiunti all'enumeratore del gestore TSF, il gestore restituisce il relativo enumeratore al client. Il client chiama quindi **IEnumTfDisplayAttributeInfo:: Next** una o più volte per ottenere gli oggetti **ITfDisplayAttributeInfo** .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[\_DISPLAYATTRIBUTE TF](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute)
</dt> <dt>

[ITfCategoryMgr:: RegisterCategory](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registercategory)
</dt> <dt>

[ITfDisplayAttributeProvider](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeprovider)
</dt> <dt>

[IEnumTfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-ienumtfdisplayattributeinfo)
</dt> <dt>

[ITfDisplayAttributeProvider::EnumDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-enumdisplayattributeinfo)
</dt> <dt>

[ITfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo)
</dt> <dt>

[ITfRange](/windows/desktop/api/Msctf/nn-msctf-itfrange)
</dt> <dt>

[ITfProperty](/windows/desktop/api/Msctf/nn-msctf-itfproperty)
</dt> <dt>

[ITfContext:: GetProperty](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty)
</dt> <dt>

[TfGuidAtom](tfguidatom.md)
</dt> <dt>

[ITfCategoryMgr::RegisterGUID](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registerguid)
</dt> <dt>

[ITfProperty:: SetValue](/windows/desktop/api/Msctf/nf-msctf-itfproperty-setvalue)
</dt> <dt>

[ITfDisplayAttributeMgr::GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo)
</dt> <dt>

[ITfDisplayAttributeProvider::GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-getdisplayattributeinfo)
</dt> <dt>

[ITfDisplayAttributeMgr::EnumDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-enumdisplayattributeinfo)
</dt> <dt>

 IEnumTfDisplayAttributeInfo 
</dt> <dt>

 ITfDisplayAttributeProvider::EnumDisplayAttributeInfo 
</dt> <dt>

[IEnumTfDisplayAttributeInfo:: Next](/windows/desktop/api/Msctf/nf-msctf-ienumtfdisplayattributeinfo-next)
</dt> </dl>

 

 




