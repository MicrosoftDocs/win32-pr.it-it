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
# <a name="providing-display-attributes"></a><span data-ttu-id="e47ab-107">Fornire attributi di visualizzazione</span><span class="sxs-lookup"><span data-stu-id="e47ab-107">Providing Display Attributes</span></span>

<span data-ttu-id="e47ab-108">Il Framework di servizi di testo (TSF) consente a un servizio di testo di fornire attributi di visualizzazione per il testo.</span><span class="sxs-lookup"><span data-stu-id="e47ab-108">Text Services Framework (TSF) enables a text service to provide display attributes for text.</span></span> <span data-ttu-id="e47ab-109">In questo modo è possibile fornire all'utente ulteriori commenti e suggerimenti visivi.</span><span class="sxs-lookup"><span data-stu-id="e47ab-109">This enables additional visual feedback to be supplied to the user.</span></span> <span data-ttu-id="e47ab-110">Ad esempio, un servizio di testo del correttore ortografico può evidenziare una parola errata con una sottolineatura rossa.</span><span class="sxs-lookup"><span data-stu-id="e47ab-110">For example, a spelling checker text service can highlight a misspelled word with a red underline.</span></span> <span data-ttu-id="e47ab-111">Gli attributi di visualizzazione specificati sono definiti dalla struttura [tf \_ DISPLAYATTRIBUTE](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute) e includono il colore del testo, il colore di sfondo del testo, lo stile di sottolineatura, il colore di sottolineatura e il peso della</span><span class="sxs-lookup"><span data-stu-id="e47ab-111">The display attributes provided are defined by the [TF\_DISPLAYATTRIBUTE](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute) structure and include text color, text background color, underline style, underline color, and underline weight.</span></span>

<span data-ttu-id="e47ab-112">I client che utilizzano queste informazioni sugli attributi di visualizzazione saranno spesso applicazioni, ma possono includere anche servizi di testo.</span><span class="sxs-lookup"><span data-stu-id="e47ab-112">Clients that use this display attribute information will most often be applications, but can also include text services.</span></span> <span data-ttu-id="e47ab-113">Il gestore TSF intermedia tra il provider di attributi di visualizzazione e il client e tiene traccia del provider di attributi di visualizzazione degli attributi di visualizzazione specifici.</span><span class="sxs-lookup"><span data-stu-id="e47ab-113">The TSF manager mediates between the display attribute provider and the client and tracks the display attribute provider of the specific display attributes.</span></span>

<span data-ttu-id="e47ab-114">Per fornire attributi di visualizzazione, un servizio di testo deve eseguire le operazioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="e47ab-114">To provide display attributes, a text service must do the following.</span></span>

1.  <span data-ttu-id="e47ab-115">Registrare il servizio di testo come provider di attributi di visualizzazione chiamando [ITfCategoryMgr:: RegisterCategory](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registercategory) con l'identificatore di classe del servizio di testo per il primo parametro, GUID \_ TFCAT \_ DISPLAYATTRIBUTEPROVIDER per il secondo parametro e l'identificatore di classe del servizio di testo per il terzo parametro.</span><span class="sxs-lookup"><span data-stu-id="e47ab-115">Register the text service as a display attribute provider by calling [ITfCategoryMgr::RegisterCategory](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registercategory) with the class identifier of the text service for the first parameter, GUID\_TFCAT\_DISPLAYATTRIBUTEPROVIDER for the second parameter and the class identifier of the text service again for the third parameter.</span></span>
2.  <span data-ttu-id="e47ab-116">Implementare [ITfDisplayAttributeProvider](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeprovider) e renderlo disponibile dal class factory.</span><span class="sxs-lookup"><span data-stu-id="e47ab-116">Implement [ITfDisplayAttributeProvider](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeprovider) and make it available from the class factory.</span></span>
3.  <span data-ttu-id="e47ab-117">Implementare [IEnumTfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-ienumtfdisplayattributeinfo) e renderlo disponibile da [ITfDisplayAttributeProvider:: EnumDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-enumdisplayattributeinfo).</span><span class="sxs-lookup"><span data-stu-id="e47ab-117">Implement [IEnumTfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-ienumtfdisplayattributeinfo) and make it available from [ITfDisplayAttributeProvider::EnumDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-enumdisplayattributeinfo).</span></span>
4.  <span data-ttu-id="e47ab-118">Implementare un oggetto [ITfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo) per ogni tipo di attributo di visualizzazione fornito dal servizio di testo.</span><span class="sxs-lookup"><span data-stu-id="e47ab-118">Implement an [ITfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo) object for each type of display attribute that the text service provides.</span></span>

## <a name="applying-the-display-attributes"></a><span data-ttu-id="e47ab-119">Applicazione degli attributi di visualizzazione</span><span class="sxs-lookup"><span data-stu-id="e47ab-119">Applying the Display Attributes</span></span>

<span data-ttu-id="e47ab-120">Il servizio di testo deve applicare l'attributo di visualizzazione a un intervallo di testo.</span><span class="sxs-lookup"><span data-stu-id="e47ab-120">The text service must apply the display attribute to a range of text.</span></span> <span data-ttu-id="e47ab-121">Un servizio di testo può modificare il valore della proprietà solo durante una sessione di modifica di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="e47ab-121">A text service can only modify the property value during a read/write edit session.</span></span>

<span data-ttu-id="e47ab-122">Supponendo che si trovi all'interno di una sessione di modifica di lettura/scrittura, viene applicato un attributo di visualizzazione nel modo seguente.</span><span class="sxs-lookup"><span data-stu-id="e47ab-122">Assuming this is within a read/write edit session, a display attribute is applied in the following manner.</span></span>

1.  <span data-ttu-id="e47ab-123">Ottenere un oggetto [ITfRange](/windows/desktop/api/Msctf/nn-msctf-itfrange) che copra il testo a cui verrà applicato l'attributo di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="e47ab-123">Obtain an [ITfRange](/windows/desktop/api/Msctf/nn-msctf-itfrange) object that covers the text that the display attribute will be applied to.</span></span>
2.  <span data-ttu-id="e47ab-124">Ottenere un oggetto [ITfProperty](/windows/desktop/api/Msctf/nn-msctf-itfproperty) per gli attributi di testo chiamando [ITfContext:: GetProperty](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty) con l' \_ attributo GUID Prop \_ .</span><span class="sxs-lookup"><span data-stu-id="e47ab-124">Obtain an [ITfProperty](/windows/desktop/api/Msctf/nn-msctf-itfproperty) object for the text attributes by calling [ITfContext::GetProperty](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty) with GUID\_PROP\_ATTRIBUTE.</span></span>
3.  <span data-ttu-id="e47ab-125">Creare un [TfGuidAtom](tfguidatom.md) dal **GUID** identificatore dell'attributo di visualizzazione definito dal servizio di testo chiamando [ITfCategoryMgr:: RegisterGUID](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registerguid).</span><span class="sxs-lookup"><span data-stu-id="e47ab-125">Create a [TfGuidAtom](tfguidatom.md) from the text service-defined display attribute identifier **GUID** by calling [ITfCategoryMgr::RegisterGUID](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registerguid).</span></span>
4.  <span data-ttu-id="e47ab-126">Inizializzare una variabile VARIANT su VT \_ I4 e impostare il membro **LVal** su **TfGuidAtom** creato nel passaggio precedente.</span><span class="sxs-lookup"><span data-stu-id="e47ab-126">Initialize a VARIANT variable to VT\_I4 and set the **lVal** member to the **TfGuidAtom** created in the previous step.</span></span>
5.  <span data-ttu-id="e47ab-127">Applicare l'attributo di visualizzazione all'intervallo chiamando [ITfProperty:: SetValue](/windows/desktop/api/Msctf/nf-msctf-itfproperty-setvalue) con il cookie di modifica di lettura/scrittura, l'intervallo e la variante inizializzata nel passaggio precedente.</span><span class="sxs-lookup"><span data-stu-id="e47ab-127">Apply the display attribute to the range by calling [ITfProperty::SetValue](/windows/desktop/api/Msctf/nf-msctf-itfproperty-setvalue) with the read/write edit cookie, the range and the VARIANT initialized in the previous step.</span></span>


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



## <a name="supplying-the-display-attribute-information-object"></a><span data-ttu-id="e47ab-128">Specifica dell'oggetto informazioni sugli attributi di visualizzazione</span><span class="sxs-lookup"><span data-stu-id="e47ab-128">Supplying the Display Attribute Information Object</span></span>

<span data-ttu-id="e47ab-129">Un client ottiene un oggetto **ITfDisplayAttributeInfo** in uno dei due modi.</span><span class="sxs-lookup"><span data-stu-id="e47ab-129">A client obtains an **ITfDisplayAttributeInfo** object in one of two ways.</span></span>

1.  <span data-ttu-id="e47ab-130">Il client chiama [ITfDisplayAttributeMgr:: GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo) con l'identificatore **GUID** dell'attributo di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="e47ab-130">The client calls [ITfDisplayAttributeMgr::GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo) with the **GUID** identifier of the display attribute.</span></span> <span data-ttu-id="e47ab-131">La prima volta che il client chiama **ITfDisplayAttributeMgr:: GetDisplayAttributeInfo**, gestione TSF creerà un'istanza del provider di attributi di visualizzazione chiamando CoCreateInstance con l'identificatore di classe passato come primo parametro a **ITfCategoryMgr:: RegisterCategory**.</span><span class="sxs-lookup"><span data-stu-id="e47ab-131">The first time the client calls **ITfDisplayAttributeMgr::GetDisplayAttributeInfo**, the TSF manager will create an instance of the display attribute provider by calling CoCreateInstance with the class identifier passed as the first parameter to **ITfCategoryMgr::RegisterCategory**.</span></span> <span data-ttu-id="e47ab-132">Le chiamate successive a **ITfDisplayAttributeMgr:: GetDisplayAttributeInfo** riutilizzeranno l'oggetto provider di attributi di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="e47ab-132">Subsequent calls to **ITfDisplayAttributeMgr::GetDisplayAttributeInfo** will reuse the display attribute provider object.</span></span>

    <span data-ttu-id="e47ab-133">Gestione TSF chiama quindi [ITfDisplayAttributeProvider:: GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-getdisplayattributeinfo) con il **GUID** dell'attributo di visualizzazione per ottenere l'oggetto **ITfDisplayAttributeInfo** .</span><span class="sxs-lookup"><span data-stu-id="e47ab-133">The TSF manager then calls [ITfDisplayAttributeProvider::GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-getdisplayattributeinfo) with the display attribute **GUID** to obtain the **ITfDisplayAttributeInfo** object.</span></span>

    <span data-ttu-id="e47ab-134">Il gestore di TSF passa quindi l'oggetto **ITfDisplayAttributeInfo** di nuovo al client.</span><span class="sxs-lookup"><span data-stu-id="e47ab-134">The TSF manager then passes the **ITfDisplayAttributeInfo** object back to the client.</span></span>

2.  <span data-ttu-id="e47ab-135">Il client chiama [ITfDisplayAttributeMgr:: EnumDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-enumdisplayattributeinfo) per ottenere un oggetto **IEnumTfDisplayAttributeInfo** che contiene tutti gli attributi di visualizzazione forniti da tutti i provider di attributi di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="e47ab-135">The client calls [ITfDisplayAttributeMgr::EnumDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-enumdisplayattributeinfo) to obtain an **IEnumTfDisplayAttributeInfo** object that contains all of the display attributes provided by all of the display attribute providers.</span></span> <span data-ttu-id="e47ab-136">Gestione TSF enumera ogni provider di attributi di visualizzazione e crea un'istanza di ogni provider chiamando CoCreateInstance con l'identificatore di classe passato come terzo parametro a **ITfCategoryMgr:: RegisterCategory**.</span><span class="sxs-lookup"><span data-stu-id="e47ab-136">The TSF manager enumerates each display attribute provider and creates an instance of each provider by calling CoCreateInstance with the class identifier passed as the third parameter to **ITfCategoryMgr::RegisterCategory**.</span></span>

    <span data-ttu-id="e47ab-137">Il gestore TSF chiama quindi ogni provider **ITfDisplayAttributeProvider:: EnumDisplayAttributeInfo** per ottenere un oggetto **IEnumTfDisplayAttributeInfo** che contiene tutti gli attributi di visualizzazione forniti dal provider.</span><span class="sxs-lookup"><span data-stu-id="e47ab-137">The TSF manager then calls each provider's **ITfDisplayAttributeProvider::EnumDisplayAttributeInfo** to obtain an **IEnumTfDisplayAttributeInfo** object that contains all of the display attributes provided by the provider.</span></span>

    <span data-ttu-id="e47ab-138">Il gestore TSF chiama quindi il metodo [IEnumTfDisplayAttributeInfo:: Next](/windows/desktop/api/Msctf/nf-msctf-ienumtfdisplayattributeinfo-next) del provider, aggiungendo ogni oggetto **ITfDisplayAttributeInfo** ottenuto all'enumeratore own del Manager, fino a quando non viene raggiunta la fine dell'enumerazione del provider.</span><span class="sxs-lookup"><span data-stu-id="e47ab-138">The TSF manager then calls the provider's [IEnumTfDisplayAttributeInfo::Next](/windows/desktop/api/Msctf/nf-msctf-ienumtfdisplayattributeinfo-next) method, adding each **ITfDisplayAttributeInfo** object obtained to the manager's own enumerator, until the end of the provider's enumeration is reached.</span></span>

    <span data-ttu-id="e47ab-139">Quando tutti gli oggetti **ITfDisplayAttributeInfo** per tutti i provider di attributi di visualizzazione vengono aggiunti all'enumeratore del gestore TSF, il gestore restituisce il relativo enumeratore al client.</span><span class="sxs-lookup"><span data-stu-id="e47ab-139">When all of the **ITfDisplayAttributeInfo** objects for all of the display attribute providers are added to the TSF manager's enumerator, the manager returns its enumerator to the client.</span></span> <span data-ttu-id="e47ab-140">Il client chiama quindi **IEnumTfDisplayAttributeInfo:: Next** una o più volte per ottenere gli oggetti **ITfDisplayAttributeInfo** .</span><span class="sxs-lookup"><span data-stu-id="e47ab-140">The client then calls **IEnumTfDisplayAttributeInfo::Next** one or more times to obtain the **ITfDisplayAttributeInfo** objects.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e47ab-141">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e47ab-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e47ab-142">\_DISPLAYATTRIBUTE TF</span><span class="sxs-lookup"><span data-stu-id="e47ab-142">TF\_DISPLAYATTRIBUTE</span></span>](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute)
</dt> <dt>

[<span data-ttu-id="e47ab-143">ITfCategoryMgr:: RegisterCategory</span><span class="sxs-lookup"><span data-stu-id="e47ab-143">ITfCategoryMgr::RegisterCategory</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registercategory)
</dt> <dt>

[<span data-ttu-id="e47ab-144">ITfDisplayAttributeProvider</span><span class="sxs-lookup"><span data-stu-id="e47ab-144">ITfDisplayAttributeProvider</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeprovider)
</dt> <dt>

[<span data-ttu-id="e47ab-145">IEnumTfDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="e47ab-145">IEnumTfDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nn-msctf-ienumtfdisplayattributeinfo)
</dt> <dt>

[<span data-ttu-id="e47ab-146">ITfDisplayAttributeProvider::EnumDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="e47ab-146">ITfDisplayAttributeProvider::EnumDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-enumdisplayattributeinfo)
</dt> <dt>

[<span data-ttu-id="e47ab-147">ITfDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="e47ab-147">ITfDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo)
</dt> <dt>

[<span data-ttu-id="e47ab-148">ITfRange</span><span class="sxs-lookup"><span data-stu-id="e47ab-148">ITfRange</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfrange)
</dt> <dt>

[<span data-ttu-id="e47ab-149">ITfProperty</span><span class="sxs-lookup"><span data-stu-id="e47ab-149">ITfProperty</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfproperty)
</dt> <dt>

[<span data-ttu-id="e47ab-150">ITfContext:: GetProperty</span><span class="sxs-lookup"><span data-stu-id="e47ab-150">ITfContext::GetProperty</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty)
</dt> <dt>

[<span data-ttu-id="e47ab-151">TfGuidAtom</span><span class="sxs-lookup"><span data-stu-id="e47ab-151">TfGuidAtom</span></span>](tfguidatom.md)
</dt> <dt>

[<span data-ttu-id="e47ab-152">ITfCategoryMgr::RegisterGUID</span><span class="sxs-lookup"><span data-stu-id="e47ab-152">ITfCategoryMgr::RegisterGUID</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registerguid)
</dt> <dt>

[<span data-ttu-id="e47ab-153">ITfProperty:: SetValue</span><span class="sxs-lookup"><span data-stu-id="e47ab-153">ITfProperty::SetValue</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfproperty-setvalue)
</dt> <dt>

[<span data-ttu-id="e47ab-154">ITfDisplayAttributeMgr::GetDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="e47ab-154">ITfDisplayAttributeMgr::GetDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo)
</dt> <dt>

[<span data-ttu-id="e47ab-155">ITfDisplayAttributeProvider::GetDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="e47ab-155">ITfDisplayAttributeProvider::GetDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-getdisplayattributeinfo)
</dt> <dt>

[<span data-ttu-id="e47ab-156">ITfDisplayAttributeMgr::EnumDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="e47ab-156">ITfDisplayAttributeMgr::EnumDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-enumdisplayattributeinfo)
</dt> <dt>

 <span data-ttu-id="e47ab-157">IEnumTfDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="e47ab-157">IEnumTfDisplayAttributeInfo</span></span> 
</dt> <dt>

 <span data-ttu-id="e47ab-158">ITfDisplayAttributeProvider::EnumDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="e47ab-158">ITfDisplayAttributeProvider::EnumDisplayAttributeInfo</span></span> 
</dt> <dt>

[<span data-ttu-id="e47ab-159">IEnumTfDisplayAttributeInfo:: Next</span><span class="sxs-lookup"><span data-stu-id="e47ab-159">IEnumTfDisplayAttributeInfo::Next</span></span>](/windows/desktop/api/Msctf/nf-msctf-ienumtfdisplayattributeinfo-next)
</dt> </dl>

 

 




