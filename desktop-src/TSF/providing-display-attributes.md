---
title: Specifica degli attributi di visualizzazione
description: Informazioni su come specificare gli attributi di visualizzazione. Framework servizi di testo (TSF) consente a un servizio di testo di fornire attributi di visualizzazione per il testo.
ms.assetid: 5809f5b8-0396-4abd-b5fe-61ecc8cd0914
keywords:
- Framework servizi di testo (TSF), visualizzare gli attributi
- TSF (Framework servizi di testo),visualizzare attributi
- servizi di testo, visualizzare attributi
- attributi di visualizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 780cc191e39d5b1d0c3329bab87af5267e4a6c73
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406114"
---
# <a name="providing-display-attributes"></a>Specifica degli attributi di visualizzazione

Framework servizi di testo (TSF) consente a un servizio di testo di fornire attributi di visualizzazione per il testo. In questo modo è possibile fornire all'utente feedback visivo aggiuntivo. Ad esempio, un servizio di testo per il correttore ortografico può evidenziare una parola con errori di ortografia con una sottolineatura rossa. Gli attributi di visualizzazione forniti sono definiti dalla struttura [ \_ DISPLAYATTRIBUTE di TF](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute) e includono il colore del testo, il colore di sfondo del testo, lo stile di sottolineatura, il colore della sottolineatura e lo spessore della sottolineatura.

I client che usano queste informazioni sugli attributi di visualizzazione sono in genere applicazioni, ma possono includere anche servizi di testo. Gestione TSF media tra il provider di attributi di visualizzazione e il client e tiene traccia del provider di attributi di visualizzazione degli attributi di visualizzazione specifici.

Per fornire gli attributi di visualizzazione, un servizio di testo deve eseguire le operazioni seguenti.

1.  Registrare il servizio di testo come provider di attributi di visualizzazione chiamando [ITfCategoryMgr::RegisterCategory](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registercategory) con l'identificatore di classe del servizio di testo per il primo parametro, GUID \_ TFCAT DISPLAYATTRIBUTEPROVIDER per il secondo parametro e l'identificatore di classe del servizio di testo nuovamente per \_ il terzo parametro.
2.  Implementare [ITfDisplayAttributeProvider](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeprovider) e renderlo disponibile dal class factory.
3.  Implementare [IEnumTfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-ienumtfdisplayattributeinfo) e renderlo disponibile da [ITfDisplayAttributeProvider::EnumDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-enumdisplayattributeinfo).
4.  Implementare [un oggetto ITfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo) per ogni tipo di attributo di visualizzazione fornito dal servizio di testo.

## <a name="applying-the-display-attributes"></a>Applicazione degli attributi di visualizzazione

Il servizio di testo deve applicare l'attributo di visualizzazione a un intervallo di testo. Un servizio di testo può modificare il valore della proprietà solo durante una sessione di modifica di lettura/scrittura.

Supponendo che si presenti all'interno di una sessione di modifica di lettura/scrittura, un attributo di visualizzazione viene applicato nel modo seguente.

1.  Ottenere un [oggetto ITfRange](/windows/desktop/api/Msctf/nn-msctf-itfrange) che copre il testo a cui verrà applicato l'attributo di visualizzazione.
2.  Ottenere un [oggetto ITfProperty](/windows/desktop/api/Msctf/nn-msctf-itfproperty) per gli attributi di testo chiamando [ITfContext::GetProperty](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty) con GUID \_ PROP \_ ATTRIBUTE.
3.  Creare un [TfGuidAtom dal](tfguidatom.md) **GUID** dell'identificatore dell'attributo di visualizzazione definito dal servizio di testo chiamando [ITfCategoryMgr::RegisterGUID](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registerguid).
4.  Inizializzare una variabile VARIANT su VT I4 e impostare il membro \_ **lVal** sul **TfGuidAtom** creato nel passaggio precedente.
5.  Applicare l'attributo display all'intervallo chiamando [ITfProperty::SetValue](/windows/desktop/api/Msctf/nf-msctf-itfproperty-setvalue) con il cookie di modifica di lettura/scrittura, l'intervallo e VARIANT inizializzati nel passaggio precedente.


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



## <a name="supplying-the-display-attribute-information-object"></a>Specifica dell'oggetto informazioni sull'attributo di visualizzazione

Un client ottiene un **oggetto ITfDisplayAttributeInfo** in uno dei due modi seguenti.

1.  Il client chiama [ITfDisplayAttributeMgr::GetDisplayAttributeInfo con](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo) l'identificatore **GUID** dell'attributo di visualizzazione. La prima volta che il client chiama **ITfDisplayAttributeMgr::GetDisplayAttributeInfo,** il gestore TSF crea un'istanza del provider di attributi di visualizzazione chiamando CoCreateInstance con l'identificatore di classe passato come primo parametro a **ITfCategoryMgr::RegisterCategory**. Le chiamate successive a **ITfDisplayAttributeMgr::GetDisplayAttributeInfo** riutilizzeranno l'oggetto provider dell'attributo di visualizzazione.

    Il gestore TSF chiama quindi [ITfDisplayAttributeProvider::GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-getdisplayattributeinfo) con il **GUID** dell'attributo di visualizzazione per ottenere **l'oggetto ITfDisplayAttributeInfo.**

    Il gestore TSF passa quindi **l'oggetto ITfDisplayAttributeInfo** al client.

2.  Il client chiama [ITfDisplayAttributeMgr::EnumDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-enumdisplayattributeinfo) per ottenere un **oggetto IEnumTfDisplayAttributeInfo** che contiene tutti gli attributi di visualizzazione forniti da tutti i provider di attributi di visualizzazione. Il gestore TSF enumera ogni provider di attributi di visualizzazione e crea un'istanza di ogni provider chiamando CoCreateInstance con l'identificatore di classe passato come terzo parametro a **ITfCategoryMgr::RegisterCategory**.

    Il gestore TSF chiama quindi **ITfDisplayAttributeProvider::EnumDisplayAttributeInfo** di ogni provider per ottenere un oggetto **IEnumTfDisplayAttributeInfo** che contiene tutti gli attributi di visualizzazione forniti dal provider.

    Il gestore TSF chiama quindi il metodo [IEnumTfDisplayAttributeInfo::Next](/windows/desktop/api/Msctf/nf-msctf-ienumtfdisplayattributeinfo-next) del provider, aggiungendo ogni oggetto **ITfDisplayAttributeInfo** ottenuto all'enumeratore del manager, fino a quando non viene raggiunta la fine dell'enumerazione del provider.

    Quando tutti gli oggetti **ITfDisplayAttributeInfo** per tutti i provider di attributi di visualizzazione vengono aggiunti all'enumeratore del gestore TSF, il gestore restituisce il relativo enumeratore al client. Il client chiama quindi **IEnumTfDisplayAttributeInfo::Next** una o più volte per ottenere **gli oggetti ITfDisplayAttributeInfo.**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[TF \_ DISPLAYATTRIBUTE](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute)
</dt> <dt>

[ITfCategoryMgr::RegisterCategory](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registercategory)
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

[ITfContext::GetProperty](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty)
</dt> <dt>

[TfGuidAtom](tfguidatom.md)
</dt> <dt>

[ITfCategoryMgr::RegisterGUID](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registerguid)
</dt> <dt>

[ITfProperty::SetValue](/windows/desktop/api/Msctf/nf-msctf-itfproperty-setvalue)
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

[IEnumTfDisplayAttributeInfo::Next](/windows/desktop/api/Msctf/nf-msctf-ienumtfdisplayattributeinfo-next)
</dt> </dl>

 

 




