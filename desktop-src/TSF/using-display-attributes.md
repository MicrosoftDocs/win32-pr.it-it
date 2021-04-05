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
# <a name="using-display-attributes"></a><span data-ttu-id="f87fa-107">Utilizzo degli attributi di visualizzazione</span><span class="sxs-lookup"><span data-stu-id="f87fa-107">Using Display Attributes</span></span>

<span data-ttu-id="f87fa-108">Il Framework di servizi di testo (TSF) consente a un servizio di testo di fornire attributi di visualizzazione per il testo.</span><span class="sxs-lookup"><span data-stu-id="f87fa-108">Text Services Framework (TSF) enables a text service to provide display attributes for text.</span></span> <span data-ttu-id="f87fa-109">Questo consente a un'applicazione di visualizzare ulteriori commenti e suggerimenti visivi.</span><span class="sxs-lookup"><span data-stu-id="f87fa-109">This enables an application to display additional visual feedback.</span></span> <span data-ttu-id="f87fa-110">Ad esempio, un servizio di testo del correttore ortografico può evidenziare una parola errata con una sottolineatura rossa.</span><span class="sxs-lookup"><span data-stu-id="f87fa-110">For example, a spelling checker text service can highlight a misspelled word with a red underline.</span></span> <span data-ttu-id="f87fa-111">Gli attributi di visualizzazione che è possibile fornire sono definiti dalla struttura [tf \_ DISPLAYATTRIBUTE](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute) e includono il colore del testo, il colore di sfondo del testo, lo stile di sottolineatura, il colore di sottolineatura e il peso della</span><span class="sxs-lookup"><span data-stu-id="f87fa-111">The display attributes that can be provided are defined by the [TF\_DISPLAYATTRIBUTE](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute) structure and include text color, text background color, underline style, underline color, and underline weight.</span></span>

<span data-ttu-id="f87fa-112">Quando si esegue il rendering del testo, un'applicazione deve ottenere gli attributi di visualizzazione per il testo disegnato e utilizzare gli attributi per modificare la modalità di disegno del testo.</span><span class="sxs-lookup"><span data-stu-id="f87fa-112">When rendering text, an application should obtain the display attributes for the text drawn and use the attributes to modify how the text is drawn.</span></span> <span data-ttu-id="f87fa-113">Completare i passaggi seguenti per ottenere gli attributi di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="f87fa-113">Complete the following steps to obtain display attributes.</span></span>

1.  <span data-ttu-id="f87fa-114">Ottenere un oggetto Property per l' \_ attributo GUID prop chiamando \_ [ITfContext:: GetProperty](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty).</span><span class="sxs-lookup"><span data-stu-id="f87fa-114">Obtain a property object for GUID\_PROP\_ATTRIBUTE by calling [ITfContext::GetProperty](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty).</span></span>
2.  <span data-ttu-id="f87fa-115">Ottenere il valore dell'attributo GUID \_ prop \_ per l'intervallo specificato chiamando [ITfReadOnlyProperty:: GetValue](/windows/desktop/api/Msctf/nf-msctf-itfreadonlyproperty-getvalue).</span><span class="sxs-lookup"><span data-stu-id="f87fa-115">Obtain the value of the GUID\_PROP\_ATTRIBUTE for the specified range by calling [ITfReadOnlyProperty::GetValue](/windows/desktop/api/Msctf/nf-msctf-itfreadonlyproperty-getvalue).</span></span> <span data-ttu-id="f87fa-116">Questa operazione fornisce un valore [TfGuidAtom](tfguidatom.md) .</span><span class="sxs-lookup"><span data-stu-id="f87fa-116">This supplies a [TfGuidAtom](tfguidatom.md) value.</span></span>
3.  <span data-ttu-id="f87fa-117">Convertire il valore [TfGuidAtom](tfguidatom.md) in un GUID chiamando [ITfCategoryMgr:: GetGuid](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid).</span><span class="sxs-lookup"><span data-stu-id="f87fa-117">Convert the [TfGuidAtom](tfguidatom.md) value into a GUID by calling [ITfCategoryMgr::GetGUID](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid).</span></span>
4.  <span data-ttu-id="f87fa-118">Creare un oggetto [ITfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo) per l'attributo di visualizzazione chiamando [ITfDisplayAttributeMgr:: GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo).</span><span class="sxs-lookup"><span data-stu-id="f87fa-118">Create an [ITfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo) object for the display attribute by calling [ITfDisplayAttributeMgr::GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo).</span></span>
5.  <span data-ttu-id="f87fa-119">Ottenere le informazioni sugli attributi di visualizzazione chiamando [ITfDisplayAttributeInfo:: GetAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo).</span><span class="sxs-lookup"><span data-stu-id="f87fa-119">Obtain the display attribute information by calling [ITfDisplayAttributeInfo::GetAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo).</span></span>

<span data-ttu-id="f87fa-120">Nell'esempio di codice seguente viene illustrata una funzione che ottiene gli attributi di visualizzazione da un contesto, un intervallo e un cookie di modifica forniti.</span><span class="sxs-lookup"><span data-stu-id="f87fa-120">The following code example demonstrates a function that obtains the display attributes from a supplied context, range, and edit cookie.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="f87fa-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f87fa-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f87fa-122">\_DISPLAYATTRIBUTE TF</span><span class="sxs-lookup"><span data-stu-id="f87fa-122">TF\_DISPLAYATTRIBUTE</span></span>](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute)
</dt> <dt>

[<span data-ttu-id="f87fa-123">ITfContext:: GetProperty</span><span class="sxs-lookup"><span data-stu-id="f87fa-123">ITfContext::GetProperty</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty)
</dt> <dt>

[<span data-ttu-id="f87fa-124">ITfReadOnlyProperty:: GetValue</span><span class="sxs-lookup"><span data-stu-id="f87fa-124">ITfReadOnlyProperty::GetValue</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfreadonlyproperty-getvalue)
</dt> <dt>

[<span data-ttu-id="f87fa-125">TfGuidAtom</span><span class="sxs-lookup"><span data-stu-id="f87fa-125">TfGuidAtom</span></span>](tfguidatom.md)
</dt> <dt>

[<span data-ttu-id="f87fa-126">ITfCategoryMgr:: GetGuid</span><span class="sxs-lookup"><span data-stu-id="f87fa-126">ITfCategoryMgr::GetGUID</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid)
</dt> <dt>

[<span data-ttu-id="f87fa-127">ITfDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="f87fa-127">ITfDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo)
</dt> <dt>

[<span data-ttu-id="f87fa-128">ITfDisplayAttributeMgr::GetDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="f87fa-128">ITfDisplayAttributeMgr::GetDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo)
</dt> <dt>

 <span data-ttu-id="f87fa-129">ITfDisplayAttributeInfo::GetAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="f87fa-129">ITfDisplayAttributeInfo::GetAttributeInfo</span></span> 
</dt> </dl>

 

 




