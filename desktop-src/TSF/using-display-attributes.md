---
title: Uso degli attributi di visualizzazione
description: Snello come usare gli attributi di visualizzazione. Framework servizi di testo (TSF) consente a un servizio di testo di fornire attributi di visualizzazione per il testo.
ms.assetid: b0f6e8e8-586a-4b51-a498-fb22bd36161f
keywords:
- Framework servizi di testo (TSF), visualizzare gli attributi
- TSF (Framework servizi di testo), visualizzare gli attributi
- applicazioni abilitate per TSF,visualizzazione di attributi
- attributi di visualizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3c576064ab22571b5a7822f5e6ff143add55d03
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406134"
---
# <a name="using-display-attributes"></a>Uso degli attributi di visualizzazione

Framework servizi di testo (TSF) consente a un servizio di testo di fornire attributi di visualizzazione per il testo. In questo modo un'applicazione può visualizzare commenti e suggerimenti visivi aggiuntivi. Ad esempio, un servizio di testo per il controllo ortografico può evidenziare una parola con errori di ortografia con una sottolineatura rossa. Gli attributi di visualizzazione che è possibile specificare sono definiti dalla struttura [TF \_ DISPLAYATTRIBUTE](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute) e includono il colore del testo, il colore di sfondo del testo, lo stile di sottolineatura, il colore della sottolineatura e lo spessore della sottolineatura.

Quando si esegue il rendering del testo, un'applicazione deve ottenere gli attributi di visualizzazione per il testo disegnato e usare gli attributi per modificare il modo in cui viene disegnato il testo. Completare la procedura seguente per ottenere gli attributi di visualizzazione.

1.  Ottenere un oggetto proprietà per GUID \_ PROP \_ ATTRIBUTE chiamando [ITfContext::GetProperty](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty).
2.  Ottenere il valore dell'ATTRIBUTO \_ GUID PROP \_ per l'intervallo specificato chiamando [ITfReadOnlyProperty::GetValue](/windows/desktop/api/Msctf/nf-msctf-itfreadonlyproperty-getvalue). Viene fornito un [valore TfGuidAtom.](tfguidatom.md)
3.  Convertire il [valore TfGuidAtom](tfguidatom.md) in un GUID chiamando [ITfCategoryMgr::GetGUID](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid).
4.  Creare un [oggetto ITfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo) per l'attributo di visualizzazione chiamando [ITfDisplayAttributeMgr::GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo).
5.  Ottenere le informazioni sull'attributo di visualizzazione chiamando [ITfDisplayAttributeInfo::GetAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo).

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

[TF \_ DISPLAYATTRIBUTE](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute)
</dt> <dt>

[ITfContext::GetProperty](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty)
</dt> <dt>

[ITfReadOnlyProperty::GetValue](/windows/desktop/api/Msctf/nf-msctf-itfreadonlyproperty-getvalue)
</dt> <dt>

[TfGuidAtom](tfguidatom.md)
</dt> <dt>

[ITfCategoryMgr::GetGUID](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid)
</dt> <dt>

[ITfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo)
</dt> <dt>

[ITfDisplayAttributeMgr::GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo)
</dt> <dt>

 ITfDisplayAttributeInfo::GetAttributeInfo 
</dt> </dl>

 

 




