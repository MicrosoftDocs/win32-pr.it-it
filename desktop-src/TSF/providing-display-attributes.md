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
# <a name="providing-display-attributes"></a><span data-ttu-id="cd0f5-108">Specifica degli attributi di visualizzazione</span><span class="sxs-lookup"><span data-stu-id="cd0f5-108">Providing Display Attributes</span></span>

<span data-ttu-id="cd0f5-109">Framework servizi di testo (TSF) consente a un servizio di testo di fornire attributi di visualizzazione per il testo.</span><span class="sxs-lookup"><span data-stu-id="cd0f5-109">Text Services Framework (TSF) enables a text service to provide display attributes for text.</span></span> <span data-ttu-id="cd0f5-110">In questo modo è possibile fornire all'utente feedback visivo aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="cd0f5-110">This enables additional visual feedback to be supplied to the user.</span></span> <span data-ttu-id="cd0f5-111">Ad esempio, un servizio di testo per il correttore ortografico può evidenziare una parola con errori di ortografia con una sottolineatura rossa.</span><span class="sxs-lookup"><span data-stu-id="cd0f5-111">For example, a spelling checker text service can highlight a misspelled word with a red underline.</span></span> <span data-ttu-id="cd0f5-112">Gli attributi di visualizzazione forniti sono definiti dalla struttura [ \_ DISPLAYATTRIBUTE di TF](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute) e includono il colore del testo, il colore di sfondo del testo, lo stile di sottolineatura, il colore della sottolineatura e lo spessore della sottolineatura.</span><span class="sxs-lookup"><span data-stu-id="cd0f5-112">The display attributes provided are defined by the [TF\_DISPLAYATTRIBUTE](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute) structure and include text color, text background color, underline style, underline color, and underline weight.</span></span>

<span data-ttu-id="cd0f5-113">I client che usano queste informazioni sugli attributi di visualizzazione sono in genere applicazioni, ma possono includere anche servizi di testo.</span><span class="sxs-lookup"><span data-stu-id="cd0f5-113">Clients that use this display attribute information will most often be applications, but can also include text services.</span></span> <span data-ttu-id="cd0f5-114">Gestione TSF media tra il provider di attributi di visualizzazione e il client e tiene traccia del provider di attributi di visualizzazione degli attributi di visualizzazione specifici.</span><span class="sxs-lookup"><span data-stu-id="cd0f5-114">The TSF manager mediates between the display attribute provider and the client and tracks the display attribute provider of the specific display attributes.</span></span>

<span data-ttu-id="cd0f5-115">Per fornire gli attributi di visualizzazione, un servizio di testo deve eseguire le operazioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="cd0f5-115">To provide display attributes, a text service must do the following.</span></span>

1.  <span data-ttu-id="cd0f5-116">Registrare il servizio di testo come provider di attributi di visualizzazione chiamando [ITfCategoryMgr::RegisterCategory](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registercategory) con l'identificatore di classe del servizio di testo per il primo parametro, GUID \_ TFCAT DISPLAYATTRIBUTEPROVIDER per il secondo parametro e l'identificatore di classe del servizio di testo nuovamente per \_ il terzo parametro.</span><span class="sxs-lookup"><span data-stu-id="cd0f5-116">Register the text service as a display attribute provider by calling [ITfCategoryMgr::RegisterCategory](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registercategory) with the class identifier of the text service for the first parameter, GUID\_TFCAT\_DISPLAYATTRIBUTEPROVIDER for the second parameter and the class identifier of the text service again for the third parameter.</span></span>
2.  <span data-ttu-id="cd0f5-117">Implementare [ITfDisplayAttributeProvider](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeprovider) e renderlo disponibile dal class factory.</span><span class="sxs-lookup"><span data-stu-id="cd0f5-117">Implement [ITfDisplayAttributeProvider](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeprovider) and make it available from the class factory.</span></span>
3.  <span data-ttu-id="cd0f5-118">Implementare [IEnumTfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-ienumtfdisplayattributeinfo) e renderlo disponibile da [ITfDisplayAttributeProvider::EnumDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-enumdisplayattributeinfo).</span><span class="sxs-lookup"><span data-stu-id="cd0f5-118">Implement [IEnumTfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-ienumtfdisplayattributeinfo) and make it available from [ITfDisplayAttributeProvider::EnumDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-enumdisplayattributeinfo).</span></span>
4.  <span data-ttu-id="cd0f5-119">Implementare [un oggetto ITfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo) per ogni tipo di attributo di visualizzazione fornito dal servizio di testo.</span><span class="sxs-lookup"><span data-stu-id="cd0f5-119">Implement an [ITfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo) object for each type of display attribute that the text service provides.</span></span>

## <a name="applying-the-display-attributes"></a><span data-ttu-id="cd0f5-120">Applicazione degli attributi di visualizzazione</span><span class="sxs-lookup"><span data-stu-id="cd0f5-120">Applying the Display Attributes</span></span>

<span data-ttu-id="cd0f5-121">Il servizio di testo deve applicare l'attributo di visualizzazione a un intervallo di testo.</span><span class="sxs-lookup"><span data-stu-id="cd0f5-121">The text service must apply the display attribute to a range of text.</span></span> <span data-ttu-id="cd0f5-122">Un servizio di testo può modificare il valore della proprietà solo durante una sessione di modifica di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="cd0f5-122">A text service can only modify the property value during a read/write edit session.</span></span>

<span data-ttu-id="cd0f5-123">Supponendo che si presenti all'interno di una sessione di modifica di lettura/scrittura, un attributo di visualizzazione viene applicato nel modo seguente.</span><span class="sxs-lookup"><span data-stu-id="cd0f5-123">Assuming this is within a read/write edit session, a display attribute is applied in the following manner.</span></span>

1.  <span data-ttu-id="cd0f5-124">Ottenere un [oggetto ITfRange](/windows/desktop/api/Msctf/nn-msctf-itfrange) che copre il testo a cui verrà applicato l'attributo di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="cd0f5-124">Obtain an [ITfRange](/windows/desktop/api/Msctf/nn-msctf-itfrange) object that covers the text that the display attribute will be applied to.</span></span>
2.  <span data-ttu-id="cd0f5-125">Ottenere un [oggetto ITfProperty](/windows/desktop/api/Msctf/nn-msctf-itfproperty) per gli attributi di testo chiamando [ITfContext::GetProperty](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty) con GUID \_ PROP \_ ATTRIBUTE.</span><span class="sxs-lookup"><span data-stu-id="cd0f5-125">Obtain an [ITfProperty](/windows/desktop/api/Msctf/nn-msctf-itfproperty) object for the text attributes by calling [ITfContext::GetProperty](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty) with GUID\_PROP\_ATTRIBUTE.</span></span>
3.  <span data-ttu-id="cd0f5-126">Creare un [TfGuidAtom dal](tfguidatom.md) **GUID** dell'identificatore dell'attributo di visualizzazione definito dal servizio di testo chiamando [ITfCategoryMgr::RegisterGUID](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registerguid).</span><span class="sxs-lookup"><span data-stu-id="cd0f5-126">Create a [TfGuidAtom](tfguidatom.md) from the text service-defined display attribute identifier **GUID** by calling [ITfCategoryMgr::RegisterGUID](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registerguid).</span></span>
4.  <span data-ttu-id="cd0f5-127">Inizializzare una variabile VARIANT su VT I4 e impostare il membro \_ **lVal** sul **TfGuidAtom** creato nel passaggio precedente.</span><span class="sxs-lookup"><span data-stu-id="cd0f5-127">Initialize a VARIANT variable to VT\_I4 and set the **lVal** member to the **TfGuidAtom** created in the previous step.</span></span>
5.  <span data-ttu-id="cd0f5-128">Applicare l'attributo display all'intervallo chiamando [ITfProperty::SetValue](/windows/desktop/api/Msctf/nf-msctf-itfproperty-setvalue) con il cookie di modifica di lettura/scrittura, l'intervallo e VARIANT inizializzati nel passaggio precedente.</span><span class="sxs-lookup"><span data-stu-id="cd0f5-128">Apply the display attribute to the range by calling [ITfProperty::SetValue](/windows/desktop/api/Msctf/nf-msctf-itfproperty-setvalue) with the read/write edit cookie, the range and the VARIANT initialized in the previous step.</span></span>


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



## <a name="supplying-the-display-attribute-information-object"></a><span data-ttu-id="cd0f5-129">Specifica dell'oggetto informazioni sull'attributo di visualizzazione</span><span class="sxs-lookup"><span data-stu-id="cd0f5-129">Supplying the Display Attribute Information Object</span></span>

<span data-ttu-id="cd0f5-130">Un client ottiene un **oggetto ITfDisplayAttributeInfo** in uno dei due modi seguenti.</span><span class="sxs-lookup"><span data-stu-id="cd0f5-130">A client obtains an **ITfDisplayAttributeInfo** object in one of two ways.</span></span>

1.  <span data-ttu-id="cd0f5-131">Il client chiama [ITfDisplayAttributeMgr::GetDisplayAttributeInfo con](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo) l'identificatore **GUID** dell'attributo di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="cd0f5-131">The client calls [ITfDisplayAttributeMgr::GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo) with the **GUID** identifier of the display attribute.</span></span> <span data-ttu-id="cd0f5-132">La prima volta che il client chiama **ITfDisplayAttributeMgr::GetDisplayAttributeInfo,** il gestore TSF crea un'istanza del provider di attributi di visualizzazione chiamando CoCreateInstance con l'identificatore di classe passato come primo parametro a **ITfCategoryMgr::RegisterCategory**.</span><span class="sxs-lookup"><span data-stu-id="cd0f5-132">The first time the client calls **ITfDisplayAttributeMgr::GetDisplayAttributeInfo**, the TSF manager will create an instance of the display attribute provider by calling CoCreateInstance with the class identifier passed as the first parameter to **ITfCategoryMgr::RegisterCategory**.</span></span> <span data-ttu-id="cd0f5-133">Le chiamate successive a **ITfDisplayAttributeMgr::GetDisplayAttributeInfo** riutilizzeranno l'oggetto provider dell'attributo di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="cd0f5-133">Subsequent calls to **ITfDisplayAttributeMgr::GetDisplayAttributeInfo** will reuse the display attribute provider object.</span></span>

    <span data-ttu-id="cd0f5-134">Il gestore TSF chiama quindi [ITfDisplayAttributeProvider::GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-getdisplayattributeinfo) con il **GUID** dell'attributo di visualizzazione per ottenere **l'oggetto ITfDisplayAttributeInfo.**</span><span class="sxs-lookup"><span data-stu-id="cd0f5-134">The TSF manager then calls [ITfDisplayAttributeProvider::GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-getdisplayattributeinfo) with the display attribute **GUID** to obtain the **ITfDisplayAttributeInfo** object.</span></span>

    <span data-ttu-id="cd0f5-135">Il gestore TSF passa quindi **l'oggetto ITfDisplayAttributeInfo** al client.</span><span class="sxs-lookup"><span data-stu-id="cd0f5-135">The TSF manager then passes the **ITfDisplayAttributeInfo** object back to the client.</span></span>

2.  <span data-ttu-id="cd0f5-136">Il client chiama [ITfDisplayAttributeMgr::EnumDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-enumdisplayattributeinfo) per ottenere un **oggetto IEnumTfDisplayAttributeInfo** che contiene tutti gli attributi di visualizzazione forniti da tutti i provider di attributi di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="cd0f5-136">The client calls [ITfDisplayAttributeMgr::EnumDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-enumdisplayattributeinfo) to obtain an **IEnumTfDisplayAttributeInfo** object that contains all of the display attributes provided by all of the display attribute providers.</span></span> <span data-ttu-id="cd0f5-137">Il gestore TSF enumera ogni provider di attributi di visualizzazione e crea un'istanza di ogni provider chiamando CoCreateInstance con l'identificatore di classe passato come terzo parametro a **ITfCategoryMgr::RegisterCategory**.</span><span class="sxs-lookup"><span data-stu-id="cd0f5-137">The TSF manager enumerates each display attribute provider and creates an instance of each provider by calling CoCreateInstance with the class identifier passed as the third parameter to **ITfCategoryMgr::RegisterCategory**.</span></span>

    <span data-ttu-id="cd0f5-138">Il gestore TSF chiama quindi **ITfDisplayAttributeProvider::EnumDisplayAttributeInfo** di ogni provider per ottenere un oggetto **IEnumTfDisplayAttributeInfo** che contiene tutti gli attributi di visualizzazione forniti dal provider.</span><span class="sxs-lookup"><span data-stu-id="cd0f5-138">The TSF manager then calls each provider's **ITfDisplayAttributeProvider::EnumDisplayAttributeInfo** to obtain an **IEnumTfDisplayAttributeInfo** object that contains all of the display attributes provided by the provider.</span></span>

    <span data-ttu-id="cd0f5-139">Il gestore TSF chiama quindi il metodo [IEnumTfDisplayAttributeInfo::Next](/windows/desktop/api/Msctf/nf-msctf-ienumtfdisplayattributeinfo-next) del provider, aggiungendo ogni oggetto **ITfDisplayAttributeInfo** ottenuto all'enumeratore del manager, fino a quando non viene raggiunta la fine dell'enumerazione del provider.</span><span class="sxs-lookup"><span data-stu-id="cd0f5-139">The TSF manager then calls the provider's [IEnumTfDisplayAttributeInfo::Next](/windows/desktop/api/Msctf/nf-msctf-ienumtfdisplayattributeinfo-next) method, adding each **ITfDisplayAttributeInfo** object obtained to the manager's own enumerator, until the end of the provider's enumeration is reached.</span></span>

    <span data-ttu-id="cd0f5-140">Quando tutti gli oggetti **ITfDisplayAttributeInfo** per tutti i provider di attributi di visualizzazione vengono aggiunti all'enumeratore del gestore TSF, il gestore restituisce il relativo enumeratore al client.</span><span class="sxs-lookup"><span data-stu-id="cd0f5-140">When all of the **ITfDisplayAttributeInfo** objects for all of the display attribute providers are added to the TSF manager's enumerator, the manager returns its enumerator to the client.</span></span> <span data-ttu-id="cd0f5-141">Il client chiama quindi **IEnumTfDisplayAttributeInfo::Next** una o più volte per ottenere **gli oggetti ITfDisplayAttributeInfo.**</span><span class="sxs-lookup"><span data-stu-id="cd0f5-141">The client then calls **IEnumTfDisplayAttributeInfo::Next** one or more times to obtain the **ITfDisplayAttributeInfo** objects.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cd0f5-142">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cd0f5-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cd0f5-143">TF \_ DISPLAYATTRIBUTE</span><span class="sxs-lookup"><span data-stu-id="cd0f5-143">TF\_DISPLAYATTRIBUTE</span></span>](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute)
</dt> <dt>

[<span data-ttu-id="cd0f5-144">ITfCategoryMgr::RegisterCategory</span><span class="sxs-lookup"><span data-stu-id="cd0f5-144">ITfCategoryMgr::RegisterCategory</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registercategory)
</dt> <dt>

[<span data-ttu-id="cd0f5-145">ITfDisplayAttributeProvider</span><span class="sxs-lookup"><span data-stu-id="cd0f5-145">ITfDisplayAttributeProvider</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeprovider)
</dt> <dt>

[<span data-ttu-id="cd0f5-146">IEnumTfDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="cd0f5-146">IEnumTfDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nn-msctf-ienumtfdisplayattributeinfo)
</dt> <dt>

[<span data-ttu-id="cd0f5-147">ITfDisplayAttributeProvider::EnumDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="cd0f5-147">ITfDisplayAttributeProvider::EnumDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-enumdisplayattributeinfo)
</dt> <dt>

[<span data-ttu-id="cd0f5-148">ITfDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="cd0f5-148">ITfDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo)
</dt> <dt>

[<span data-ttu-id="cd0f5-149">ITfRange</span><span class="sxs-lookup"><span data-stu-id="cd0f5-149">ITfRange</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfrange)
</dt> <dt>

[<span data-ttu-id="cd0f5-150">ITfProperty</span><span class="sxs-lookup"><span data-stu-id="cd0f5-150">ITfProperty</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfproperty)
</dt> <dt>

[<span data-ttu-id="cd0f5-151">ITfContext::GetProperty</span><span class="sxs-lookup"><span data-stu-id="cd0f5-151">ITfContext::GetProperty</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty)
</dt> <dt>

[<span data-ttu-id="cd0f5-152">TfGuidAtom</span><span class="sxs-lookup"><span data-stu-id="cd0f5-152">TfGuidAtom</span></span>](tfguidatom.md)
</dt> <dt>

[<span data-ttu-id="cd0f5-153">ITfCategoryMgr::RegisterGUID</span><span class="sxs-lookup"><span data-stu-id="cd0f5-153">ITfCategoryMgr::RegisterGUID</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registerguid)
</dt> <dt>

[<span data-ttu-id="cd0f5-154">ITfProperty::SetValue</span><span class="sxs-lookup"><span data-stu-id="cd0f5-154">ITfProperty::SetValue</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfproperty-setvalue)
</dt> <dt>

[<span data-ttu-id="cd0f5-155">ITfDisplayAttributeMgr::GetDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="cd0f5-155">ITfDisplayAttributeMgr::GetDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo)
</dt> <dt>

[<span data-ttu-id="cd0f5-156">ITfDisplayAttributeProvider::GetDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="cd0f5-156">ITfDisplayAttributeProvider::GetDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-getdisplayattributeinfo)
</dt> <dt>

[<span data-ttu-id="cd0f5-157">ITfDisplayAttributeMgr::EnumDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="cd0f5-157">ITfDisplayAttributeMgr::EnumDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-enumdisplayattributeinfo)
</dt> <dt>

 <span data-ttu-id="cd0f5-158">IEnumTfDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="cd0f5-158">IEnumTfDisplayAttributeInfo</span></span> 
</dt> <dt>

 <span data-ttu-id="cd0f5-159">ITfDisplayAttributeProvider::EnumDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="cd0f5-159">ITfDisplayAttributeProvider::EnumDisplayAttributeInfo</span></span> 
</dt> <dt>

[<span data-ttu-id="cd0f5-160">IEnumTfDisplayAttributeInfo::Next</span><span class="sxs-lookup"><span data-stu-id="cd0f5-160">IEnumTfDisplayAttributeInfo::Next</span></span>](/windows/desktop/api/Msctf/nf-msctf-ienumtfdisplayattributeinfo-next)
</dt> </dl>

 

 




