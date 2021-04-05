---
title: Utilizzo degli attributi di visualizzazione
description: Il Framework di servizi di testo (TSF) consente a un servizio di testo di fornire attributi di visualizzazione per il testo.
ms.assetid: b0f6e8e8-586a-4b51-a498-fb22bd36161f
keywords:
- Framework servizi di testo (TSF), attributi di visualizzazione
- TSF (Text Services Framework), attributi di visualizzazione
- Applicazioni abilitate per TSF, attributi di visualizzazione
- attributi di visualizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbc725f67fab904db23f6232ac5efb5d63c62c26
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708344"
---
# <a name="using-display-attributes"></a>Utilizzo degli attributi di visualizzazione

Il Framework di servizi di testo (TSF) consente a un servizio di testo di fornire attributi di visualizzazione per il testo. Questo consente a un'applicazione di visualizzare ulteriori commenti e suggerimenti visivi. Ad esempio, un servizio di testo del correttore ortografico può evidenziare una parola errata con una sottolineatura rossa. Gli attributi di visualizzazione che è possibile fornire sono definiti dalla struttura [tf \_ DISPLAYATTRIBUTE](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute) e includono il colore del testo, il colore di sfondo del testo, lo stile di sottolineatura, il colore di sottolineatura e il peso della

Quando si esegue il rendering del testo, un'applicazione deve ottenere gli attributi di visualizzazione per il testo disegnato e utilizzare gli attributi per modificare la modalità di disegno del testo. Completare i passaggi seguenti per ottenere gli attributi di visualizzazione.

1.  Ottenere un oggetto Property per l' \_ attributo GUID prop chiamando \_ [ITfContext:: GetProperty](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty).
2.  Ottenere il valore dell'attributo GUID \_ prop \_ per l'intervallo specificato chiamando [ITfReadOnlyProperty:: GetValue](/windows/desktop/api/Msctf/nf-msctf-itfreadonlyproperty-getvalue). Questa operazione fornisce un valore [TfGuidAtom](tfguidatom.md) .
3.  Convertire il valore [TfGuidAtom](tfguidatom.md) in un GUID chiamando [ITfCategoryMgr:: GetGuid](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid).
4.  Creare un oggetto [ITfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo) per l'attributo di visualizzazione chiamando [ITfDisplayAttributeMgr:: GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo).
5.  Ottenere le informazioni sugli attributi di visualizzazione chiamando [ITfDisplayAttributeInfo:: GetAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo).

Nell'esempio di codice seguente viene illustrata una funzione che ottiene gli attributi di visualizzazione da un contesto, un intervallo e un cookie di modifica forniti.


```C++
HRESULT GetDispAttrFromRange(   ITfContext *pContext, 
                                ITfRange *pRange, 
                                TfEditCookie ec, 
                                TF_DISPLAYATTRIBUTE *pDispAttr)
{
    HRESULT     hr;
    
    //Create the category manager. 
    ITfCategoryMgr  *pCategoryMgr;
    hr = CoCreateInstance(  CLSID_TF_CategoryMgr,
                            NULL, 
                            CLSCTX_INPROC_SERVER, 
                            IID_ITfCategoryMgr, 
                            (LPVOID*)&pCategoryMgr);
    if(FAILED(hr))
    {
        return hr;
    }

    //Create the display attribute manager. 
    ITfDisplayAttributeMgr  *pDispMgr;
    hr = CoCreateInstance(  CLSID_TF_DisplayAttributeMgr,
                            NULL, 
                            CLSCTX_INPROC_SERVER, 
                            IID_ITfDisplayAttributeMgr, 
                            (LPVOID*)&pDispMgr);
    if(FAILED(hr))
    {
        pCategoryMgr->Release();
        return hr;
    }
    
    //Get the display attribute property. 
    ITfProperty *pProp;
    hr = pContext->GetProperty(GUID_PROP_ATTRIBUTE, &pProp);
    if(SUCCEEDED(hr))
    {
        VARIANT var;

        VariantInit(&var);
        hr = pProp->GetValue(ec, pRange, &var);
        if(S_OK == hr)  //Returns S_FALSE if the range is not completely covered by the property.  
        {
            if(VT_I4 == var.vt)
            {
                //The property is a guidatom. 
                GUID    guid;

                //Convert the guidatom into a GUID. 
                hr = pCategoryMgr->GetGUID((TfGuidAtom)var.lVal, &guid);
                if(SUCCEEDED(hr))
                {
                    ITfDisplayAttributeInfo *pDispInfo;

                    //Get the display attribute info object for this attribute. 
                    hr = pDispMgr->GetDisplayAttributeInfo(guid, &pDispInfo, NULL);
                    if(SUCCEEDED(hr))
                    {
                        //Get the display attribute info. 
                        hr = pDispInfo->GetAttributeInfo(pDispAttr);

                        pDispInfo->Release();
                    }
                }
            }
            else
            {
                //An error occurred; GUID_PROP_ATTRIBUTE must always be VT_I4. 
                hr = E_FAIL;
            }
            VariantClear(&var);
        }
    pProp->Release();
    }

    pCategoryMgr->Release();
    pDispMgr->Release();

    return hr;
}

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[\_DISPLAYATTRIBUTE TF](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute)
</dt> <dt>

[ITfContext:: GetProperty](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty)
</dt> <dt>

[ITfReadOnlyProperty:: GetValue](/windows/desktop/api/Msctf/nf-msctf-itfreadonlyproperty-getvalue)
</dt> <dt>

[TfGuidAtom](tfguidatom.md)
</dt> <dt>

[ITfCategoryMgr:: GetGuid](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid)
</dt> <dt>

[ITfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo)
</dt> <dt>

[ITfDisplayAttributeMgr::GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo)
</dt> <dt>

 ITfDisplayAttributeInfo::GetAttributeInfo 
</dt> </dl>

 

 




