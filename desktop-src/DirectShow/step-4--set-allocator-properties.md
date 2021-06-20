---
description: Impostare le proprietà dell'allocatore come parte della scrittura di un filtro di trasformazione. Il pin di output del filtro di trasformazione seleziona l'allocatore downstream.
ms.assetid: c2fd6d8b-b239-45e4-9c02-41edafa58762
title: Passaggio 4. Impostare le proprietà dell'allocatore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9ee7d9ecdc85b63ec6bd774a3a47e0e9399dcf3
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406824"
---
# <a name="step-4-set-allocator-properties"></a><span data-ttu-id="825c6-105">Passaggio 4.</span><span class="sxs-lookup"><span data-stu-id="825c6-105">Step 4.</span></span> <span data-ttu-id="825c6-106">Impostare le proprietà dell'allocatore</span><span class="sxs-lookup"><span data-stu-id="825c6-106">Set Allocator Properties</span></span>

<span data-ttu-id="825c6-107">Questo è il passaggio 4 dell'esercitazione [Scrittura di filtri di trasformazione.](writing-transform-filters.md)</span><span class="sxs-lookup"><span data-stu-id="825c6-107">This is step 4 of the tutorial [Writing Transform Filters](writing-transform-filters.md).</span></span>

> [!Note]  
> <span data-ttu-id="825c6-108">Questo passaggio non è necessario per i filtri che derivano da **CTransInPlaceFilter.**</span><span class="sxs-lookup"><span data-stu-id="825c6-108">This step is not required for filters that derive from **CTransInPlaceFilter**.</span></span>

 

<span data-ttu-id="825c6-109">Quando due pin concordano su un tipo di supporto, selezionano un allocatore per la connessione e negoziano le proprietà dell'allocatore, ad esempio le dimensioni del buffer e il numero di buffer.</span><span class="sxs-lookup"><span data-stu-id="825c6-109">After two pins agree on a media type, they select an allocator for the connection and negotiate allocator properties, such as the buffer size and the number of buffers.</span></span>

<span data-ttu-id="825c6-110">Nella classe **CTransformFilter** sono presenti due allocatori, uno per la connessione pin upstream e uno per la connessione pin downstream.</span><span class="sxs-lookup"><span data-stu-id="825c6-110">In the **CTransformFilter** class, there are two allocators, one for the upstream pin connection and one for the downstream pin connection.</span></span> <span data-ttu-id="825c6-111">Il filtro upstream seleziona l'allocatore upstream e sceglie anche le proprietà dell'allocatore.</span><span class="sxs-lookup"><span data-stu-id="825c6-111">The upstream filter selects the upstream allocator and also chooses the allocator properties.</span></span> <span data-ttu-id="825c6-112">Il pin di input accetta qualsiasi decisione del filtro upstream.</span><span class="sxs-lookup"><span data-stu-id="825c6-112">The input pin accepts whatever the upstream filter decides.</span></span> <span data-ttu-id="825c6-113">Se è necessario modificare questo comportamento, eseguire l'override del [**metodo CBaseInputPin::NotifyAllocator.**](cbaseinputpin-notifyallocator.md)</span><span class="sxs-lookup"><span data-stu-id="825c6-113">If you need to modify this behavior, override the [**CBaseInputPin::NotifyAllocator**](cbaseinputpin-notifyallocator.md) method.</span></span>

<span data-ttu-id="825c6-114">Il pin di output del filtro di trasformazione seleziona l'allocatore downstream.</span><span class="sxs-lookup"><span data-stu-id="825c6-114">The transform filter's output pin selects the downstream allocator.</span></span> <span data-ttu-id="825c6-115">Esegue i passaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="825c6-115">It performs the following steps:</span></span>

1.  <span data-ttu-id="825c6-116">Se il filtro downstream può fornire un allocatore, il pin di output usa tale allocatore.</span><span class="sxs-lookup"><span data-stu-id="825c6-116">If the downstream filter can provide an allocator, the output pin uses that one.</span></span> <span data-ttu-id="825c6-117">In caso contrario, il pin di output crea un nuovo allocatore.</span><span class="sxs-lookup"><span data-stu-id="825c6-117">Otherwise, the output pin creates a new allocator.</span></span>
2.  <span data-ttu-id="825c6-118">Il pin di output ottiene i requisiti dell'allocatore del filtro downstream (se presenti) chiamando [**IMemInputPin::GetAllocatorRequirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements).</span><span class="sxs-lookup"><span data-stu-id="825c6-118">The output pin gets the downstream filter's allocator requirements (if any) by calling [**IMemInputPin::GetAllocatorRequirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements).</span></span>
3.  <span data-ttu-id="825c6-119">Il pin di output chiama il metodo [**CTransformFilter::D ecideBufferSize**](ctransformfilter-decidebuffersize.md) del filtro di trasformazione, che è virtuale puro.</span><span class="sxs-lookup"><span data-stu-id="825c6-119">The output pin calls the transform filter's [**CTransformFilter::DecideBufferSize**](ctransformfilter-decidebuffersize.md) method, which is pure virtual.</span></span> <span data-ttu-id="825c6-120">I parametri di questo metodo sono un puntatore all'allocatore e una struttura [**ALLOCATOR \_ PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) con i requisiti del filtro downstream.</span><span class="sxs-lookup"><span data-stu-id="825c6-120">The parameters to this method are a pointer to the allocator and an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure with the downstream filter's requirements.</span></span> <span data-ttu-id="825c6-121">Se il filtro downstream non ha requisiti di allocatore, la struttura viene azzerato.</span><span class="sxs-lookup"><span data-stu-id="825c6-121">If the downstream filter has no allocator requirements, the structure is zeroed out.</span></span>
4.  <span data-ttu-id="825c6-122">Nel metodo **DecideBufferSize** la classe derivata imposta le proprietà dell'allocatore chiamando [**IMemAllocator::SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties).</span><span class="sxs-lookup"><span data-stu-id="825c6-122">In the **DecideBufferSize** method, the derived class sets the allocator properties by calling [**IMemAllocator::SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties).</span></span>

<span data-ttu-id="825c6-123">In genere, la classe derivata selezionerà le proprietà dell'allocatore in base al formato di output, ai requisiti del filtro downstream e ai requisiti specifici del filtro.</span><span class="sxs-lookup"><span data-stu-id="825c6-123">Generally, the derived class will select allocator properties based on the output format, the downstream filter's requirements, and the filter's own requirements.</span></span> <span data-ttu-id="825c6-124">Provare a selezionare le proprietà compatibili con la richiesta del filtro downstream.</span><span class="sxs-lookup"><span data-stu-id="825c6-124">Try to select properties that are compatible with the downstream filter's request.</span></span> <span data-ttu-id="825c6-125">In caso contrario, il filtro downstream potrebbe rifiutare la connessione.</span><span class="sxs-lookup"><span data-stu-id="825c6-125">Otherwise, the downstream filter might reject the connection.</span></span>

<span data-ttu-id="825c6-126">Nell'esempio seguente il codificatore RLE imposta i valori minimi per le dimensioni del buffer, l'allineamento del buffer e il numero di buffer.</span><span class="sxs-lookup"><span data-stu-id="825c6-126">In the following example, the RLE encoder sets minimum values for the buffer size, buffer alignment, and buffer count.</span></span> <span data-ttu-id="825c6-127">Per il prefisso, usa qualsiasi valore richiesto dal filtro downstream.</span><span class="sxs-lookup"><span data-stu-id="825c6-127">For the prefix, it uses whatever value the downstream filter requested.</span></span> <span data-ttu-id="825c6-128">Il prefisso è in genere zero byte, ma alcuni filtri lo richiedono.</span><span class="sxs-lookup"><span data-stu-id="825c6-128">The prefix is typically zero bytes, but some filters require it.</span></span> <span data-ttu-id="825c6-129">Ad esempio, il [filtro Mux AVI](avi-mux-filter.md) usa il prefisso per scrivere le intestazioni RIFF.</span><span class="sxs-lookup"><span data-stu-id="825c6-129">For example, the [AVI Mux](avi-mux-filter.md) filter uses the prefix to write RIFF headers.</span></span>


```C++
HRESULT CRleFilter::DecideBufferSize(
    IMemAllocator *pAlloc, ALLOCATOR_PROPERTIES *pProp)
{
    AM_MEDIA_TYPE mt;
    HRESULT hr = m_pOutput->ConnectionMediaType(&mt);
    if (FAILED(hr))
    {
        return hr;
    }

    ASSERT(mt.formattype == FORMAT_VideoInfo);
    BITMAPINFOHEADER *pbmi = HEADER(mt.pbFormat);
    pProp->cbBuffer = DIBSIZE(*pbmi) * 2; 
    if (pProp->cbAlign == 0)
    {
        pProp->cbAlign = 1;
    }
    if (pProp->cBuffers == 0)
    {
        pProp->cBuffers = 1;
    }
    // Release the format block.
    FreeMediaType(mt);

    // Set allocator properties.
    ALLOCATOR_PROPERTIES Actual;
    hr = pAlloc->SetProperties(pProp, &Actual);
    if (FAILED(hr)) 
    {
        return hr;
    }
    // Even when it succeeds, check the actual result.
    if (pProp->cbBuffer > Actual.cbBuffer) 
    {
        return E_FAIL;
    }
    return S_OK;
}
```



<span data-ttu-id="825c6-130">L'allocatore potrebbe non essere in grado di corrispondere esattamente alla richiesta.</span><span class="sxs-lookup"><span data-stu-id="825c6-130">The allocator may not be able to match your request exactly.</span></span> <span data-ttu-id="825c6-131">Di conseguenza, **il metodo SetProperties** restituisce il risultato effettivo in una struttura **ALLOCATOR \_ PROPERTIES** separata *(il parametro Actual* nell'esempio precedente).</span><span class="sxs-lookup"><span data-stu-id="825c6-131">Therefore, the **SetProperties** method returns the actual result in a separate **ALLOCATOR\_PROPERTIES** structure (the *Actual* parameter, in the previous example).</span></span> <span data-ttu-id="825c6-132">Anche quando **SetProperties** ha esito positivo, è necessario controllare il risultato per assicurarsi che soddisfino i requisiti minimi del filtro.</span><span class="sxs-lookup"><span data-stu-id="825c6-132">Even when **SetProperties** succeeds, you should check the result to make sure they meet your filter's minimum requirements.</span></span>

<span data-ttu-id="825c6-133">**Allocatori personalizzati**</span><span class="sxs-lookup"><span data-stu-id="825c6-133">**Custom Allocators**</span></span>

<span data-ttu-id="825c6-134">Per impostazione predefinita, tutte le classi di filtro usano la [**classe CMemAllocator**](cmemallocator.md) per i relativi allocatori.</span><span class="sxs-lookup"><span data-stu-id="825c6-134">By default, all of the filter classes use the [**CMemAllocator**](cmemallocator.md) class for their allocators.</span></span> <span data-ttu-id="825c6-135">Questa classe alloca memoria dallo spazio degli indirizzi virtuali del processo client (usando **VirtualAlloc).**</span><span class="sxs-lookup"><span data-stu-id="825c6-135">This class allocates memory from the virtual address space of the client process (using **VirtualAlloc**).</span></span> <span data-ttu-id="825c6-136">Se il filtro deve usare un altro tipo di memoria, ad esempio le superfici DirectDraw, è possibile implementare un allocatore personalizzato.</span><span class="sxs-lookup"><span data-stu-id="825c6-136">If your filter needs to use some other kind of memory, such as DirectDraw surfaces, you can implement a custom allocator.</span></span> <span data-ttu-id="825c6-137">È possibile usare la [**classe CBaseAllocator**](cbaseallocator.md) o scrivere una classe allocatore completamente nuova.</span><span class="sxs-lookup"><span data-stu-id="825c6-137">You can use the [**CBaseAllocator**](cbaseallocator.md) class or write an entirely new allocator class.</span></span> <span data-ttu-id="825c6-138">Se il filtro ha un allocatore personalizzato, eseguire l'override dei metodi seguenti, a seconda del pin che usa l'allocatore:</span><span class="sxs-lookup"><span data-stu-id="825c6-138">If your filter has a custom allocator, override the following methods, depending on which pin uses the allocator:</span></span>

-   <span data-ttu-id="825c6-139">Pin di input: [**CBaseInputPin::GetAllocator**](cbaseinputpin-getallocator.md) e [**CBaseInputPin::NotifyAllocator**](cbaseinputpin-notifyallocator.md).</span><span class="sxs-lookup"><span data-stu-id="825c6-139">Input pin: [**CBaseInputPin::GetAllocator**](cbaseinputpin-getallocator.md) and [**CBaseInputPin::NotifyAllocator**](cbaseinputpin-notifyallocator.md).</span></span>
-   <span data-ttu-id="825c6-140">Pin di output: [**CBaseOutputPin::D ecideAllocator**](cbaseoutputpin-decideallocator.md).</span><span class="sxs-lookup"><span data-stu-id="825c6-140">Output pin: [**CBaseOutputPin::DecideAllocator**](cbaseoutputpin-decideallocator.md).</span></span>

<span data-ttu-id="825c6-141">Se l'altro filtro rifiuta di connettersi usando l'allocatore personalizzato, il filtro può non riuscire o connettersi all'allocatore dell'altro filtro.</span><span class="sxs-lookup"><span data-stu-id="825c6-141">If the other filter refuses to connect using your custom allocator, your filter can either fail the connection, or else connect with the other filter's allocator.</span></span> <span data-ttu-id="825c6-142">Nel secondo caso, potrebbe essere necessario impostare un flag interno che indica il tipo di allocatore.</span><span class="sxs-lookup"><span data-stu-id="825c6-142">In the latter case, you might need to set an internal flag indicating the type of allocator.</span></span> <span data-ttu-id="825c6-143">Per un esempio di questo approccio, vedere [**Classe CDrawImage**](cdrawimage.md).</span><span class="sxs-lookup"><span data-stu-id="825c6-143">For an example of this approach, see [**CDrawImage Class**](cdrawimage.md).</span></span>

<span data-ttu-id="825c6-144">Passaggio [5. Trasformare l'immagine](step-5--transform-the-image.md).</span><span class="sxs-lookup"><span data-stu-id="825c6-144">Next: [Step 5. Transform the Image](step-5--transform-the-image.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="825c6-145">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="825c6-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="825c6-146">Scrittura di filtri DirectMostra filtri</span><span class="sxs-lookup"><span data-stu-id="825c6-146">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



