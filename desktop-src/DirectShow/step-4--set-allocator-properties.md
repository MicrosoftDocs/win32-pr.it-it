---
description: Passaggio 4.
ms.assetid: c2fd6d8b-b239-45e4-9c02-41edafa58762
title: Passaggio 4. Imposta proprietà allocatore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a32d5e3affba32b96dc93cb97e1886322bc6f2c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316326"
---
# <a name="step-4-set-allocator-properties"></a><span data-ttu-id="b97f3-104">Passaggio 4.</span><span class="sxs-lookup"><span data-stu-id="b97f3-104">Step 4.</span></span> <span data-ttu-id="b97f3-105">Imposta proprietà allocatore</span><span class="sxs-lookup"><span data-stu-id="b97f3-105">Set Allocator Properties</span></span>

<span data-ttu-id="b97f3-106">Questo è il passaggio 4 dell'esercitazione [scrittura dei filtri di trasformazione](writing-transform-filters.md).</span><span class="sxs-lookup"><span data-stu-id="b97f3-106">This is step 4 of the tutorial [Writing Transform Filters](writing-transform-filters.md).</span></span>

> [!Note]  
> <span data-ttu-id="b97f3-107">Questo passaggio non è necessario per i filtri che derivano da **CTransInPlaceFilter**.</span><span class="sxs-lookup"><span data-stu-id="b97f3-107">This step is not required for filters that derive from **CTransInPlaceFilter**.</span></span>

 

<span data-ttu-id="b97f3-108">Dopo aver accettato due pin per un tipo di supporto, selezionare un allocatore per la connessione e negoziare le proprietà dell'allocatore, ad esempio la dimensione del buffer e il numero di buffer.</span><span class="sxs-lookup"><span data-stu-id="b97f3-108">After two pins agree on a media type, they select an allocator for the connection and negotiate allocator properties, such as the buffer size and the number of buffers.</span></span>

<span data-ttu-id="b97f3-109">Nella classe **CTransformFilter** sono disponibili due allocatori, uno per la connessione pin upstream e uno per la connessione pin downstream.</span><span class="sxs-lookup"><span data-stu-id="b97f3-109">In the **CTransformFilter** class, there are two allocators, one for the upstream pin connection and one for the downstream pin connection.</span></span> <span data-ttu-id="b97f3-110">Il filtro upstream seleziona l'allocatore upstream e sceglie anche le proprietà dell'allocatore.</span><span class="sxs-lookup"><span data-stu-id="b97f3-110">The upstream filter selects the upstream allocator and also chooses the allocator properties.</span></span> <span data-ttu-id="b97f3-111">Il pin di input accetta qualsiasi cosa venga deciso dal filtro upstream.</span><span class="sxs-lookup"><span data-stu-id="b97f3-111">The input pin accepts whatever the upstream filter decides.</span></span> <span data-ttu-id="b97f3-112">Se è necessario modificare questo comportamento, eseguire l'override del metodo [**CBaseInputPin:: NotifyAllocator**](cbaseinputpin-notifyallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="b97f3-112">If you need to modify this behavior, override the [**CBaseInputPin::NotifyAllocator**](cbaseinputpin-notifyallocator.md) method.</span></span>

<span data-ttu-id="b97f3-113">Il pin di output del filtro di trasformazione seleziona l'allocatore downstream.</span><span class="sxs-lookup"><span data-stu-id="b97f3-113">The transform filter's output pin selects the downstream allocator.</span></span> <span data-ttu-id="b97f3-114">Esegue i passaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="b97f3-114">It performs the following steps:</span></span>

1.  <span data-ttu-id="b97f3-115">Se il filtro downstream può fornire un allocatore, il pin di output lo utilizzerà.</span><span class="sxs-lookup"><span data-stu-id="b97f3-115">If the downstream filter can provide an allocator, the output pin uses that one.</span></span> <span data-ttu-id="b97f3-116">In caso contrario, il pin di output crea un nuovo allocatore.</span><span class="sxs-lookup"><span data-stu-id="b97f3-116">Otherwise, the output pin creates a new allocator.</span></span>
2.  <span data-ttu-id="b97f3-117">Il pin di output ottiene i requisiti dell'allocatore del filtro downstream chiamando [**IMemInputPin:: GetAllocatorRequirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements).</span><span class="sxs-lookup"><span data-stu-id="b97f3-117">The output pin gets the downstream filter's allocator requirements (if any) by calling [**IMemInputPin::GetAllocatorRequirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements).</span></span>
3.  <span data-ttu-id="b97f3-118">Il pin di output chiama il metodo [**CTransformFilter::D ecidebuffersize**](ctransformfilter-decidebuffersize.md) del filtro di trasformazione, che è virtuale puro.</span><span class="sxs-lookup"><span data-stu-id="b97f3-118">The output pin calls the transform filter's [**CTransformFilter::DecideBufferSize**](ctransformfilter-decidebuffersize.md) method, which is pure virtual.</span></span> <span data-ttu-id="b97f3-119">I parametri di questo metodo sono un puntatore all'allocatore e una struttura delle [**\_ proprietà dell'allocatore**](/windows/win32/api/strmif/ns-strmif-allocator_properties) con i requisiti del filtro downstream.</span><span class="sxs-lookup"><span data-stu-id="b97f3-119">The parameters to this method are a pointer to the allocator and an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure with the downstream filter's requirements.</span></span> <span data-ttu-id="b97f3-120">Se il filtro downstream non presenta requisiti per l'allocatore, la struttura viene azzerata.</span><span class="sxs-lookup"><span data-stu-id="b97f3-120">If the downstream filter has no allocator requirements, the structure is zeroed out.</span></span>
4.  <span data-ttu-id="b97f3-121">Nel metodo **DecideBufferSize** la classe derivata imposta le proprietà dell'allocatore chiamando [**IMemAllocator::**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties)SetValue.</span><span class="sxs-lookup"><span data-stu-id="b97f3-121">In the **DecideBufferSize** method, the derived class sets the allocator properties by calling [**IMemAllocator::SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties).</span></span>

<span data-ttu-id="b97f3-122">In genere, la classe derivata selezionerà le proprietà dell'allocatore in base al formato di output, i requisiti del filtro downstream e i requisiti del filtro.</span><span class="sxs-lookup"><span data-stu-id="b97f3-122">Generally, the derived class will select allocator properties based on the output format, the downstream filter's requirements, and the filter's own requirements.</span></span> <span data-ttu-id="b97f3-123">Provare a selezionare le proprietà compatibili con la richiesta del filtro downstream.</span><span class="sxs-lookup"><span data-stu-id="b97f3-123">Try to select properties that are compatible with the downstream filter's request.</span></span> <span data-ttu-id="b97f3-124">In caso contrario, il filtro downstream potrebbe rifiutare la connessione.</span><span class="sxs-lookup"><span data-stu-id="b97f3-124">Otherwise, the downstream filter might reject the connection.</span></span>

<span data-ttu-id="b97f3-125">Nell'esempio seguente il codificatore RLE imposta i valori minimi per le dimensioni del buffer, l'allineamento del buffer e il numero di buffer.</span><span class="sxs-lookup"><span data-stu-id="b97f3-125">In the following example, the RLE encoder sets minimum values for the buffer size, buffer alignment, and buffer count.</span></span> <span data-ttu-id="b97f3-126">Per il prefisso, USA qualsiasi valore richiesto dal filtro downstream.</span><span class="sxs-lookup"><span data-stu-id="b97f3-126">For the prefix, it uses whatever value the downstream filter requested.</span></span> <span data-ttu-id="b97f3-127">Il prefisso è in genere pari a zero byte, ma alcuni filtri lo richiedono.</span><span class="sxs-lookup"><span data-stu-id="b97f3-127">The prefix is typically zero bytes, but some filters require it.</span></span> <span data-ttu-id="b97f3-128">Ad esempio, il filtro [Mux AVI](avi-mux-filter.md) usa il prefisso per scrivere le intestazioni riff.</span><span class="sxs-lookup"><span data-stu-id="b97f3-128">For example, the [AVI Mux](avi-mux-filter.md) filter uses the prefix to write RIFF headers.</span></span>


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



<span data-ttu-id="b97f3-129">L'allocatore potrebbe non essere in grado di soddisfare esattamente la richiesta.</span><span class="sxs-lookup"><span data-stu-id="b97f3-129">The allocator may not be able to match your request exactly.</span></span> <span data-ttu-id="b97f3-130">Pertanto, il metodo **seproperties** restituisce il risultato effettivo in una struttura **di \_ Proprietà allocatore** separata (il parametro *effettivo* nell'esempio precedente).</span><span class="sxs-lookup"><span data-stu-id="b97f3-130">Therefore, the **SetProperties** method returns the actual result in a separate **ALLOCATOR\_PROPERTIES** structure (the *Actual* parameter, in the previous example).</span></span> <span data-ttu-id="b97f3-131">Anche in caso di esito positivo delle **Proprietà** , è necessario controllare il risultato per assicurarsi che soddisfino i requisiti minimi del filtro.</span><span class="sxs-lookup"><span data-stu-id="b97f3-131">Even when **SetProperties** succeeds, you should check the result to make sure they meet your filter's minimum requirements.</span></span>

<span data-ttu-id="b97f3-132">**Allocatori personalizzati**</span><span class="sxs-lookup"><span data-stu-id="b97f3-132">**Custom Allocators**</span></span>

<span data-ttu-id="b97f3-133">Per impostazione predefinita, tutte le classi di filtro utilizzano la classe [**CMemAllocator**](cmemallocator.md) per gli allocatori.</span><span class="sxs-lookup"><span data-stu-id="b97f3-133">By default, all of the filter classes use the [**CMemAllocator**](cmemallocator.md) class for their allocators.</span></span> <span data-ttu-id="b97f3-134">Questa classe alloca memoria dallo spazio degli indirizzi virtuali del processo client (tramite **VirtualAlloc**).</span><span class="sxs-lookup"><span data-stu-id="b97f3-134">This class allocates memory from the virtual address space of the client process (using **VirtualAlloc**).</span></span> <span data-ttu-id="b97f3-135">Se il filtro deve usare un altro tipo di memoria, ad esempio le superfici DirectDraw, è possibile implementare un allocatore personalizzato.</span><span class="sxs-lookup"><span data-stu-id="b97f3-135">If your filter needs to use some other kind of memory, such as DirectDraw surfaces, you can implement a custom allocator.</span></span> <span data-ttu-id="b97f3-136">È possibile usare la classe [**CBaseAllocator**](cbaseallocator.md) o scrivere una classe allocator completamente nuova.</span><span class="sxs-lookup"><span data-stu-id="b97f3-136">You can use the [**CBaseAllocator**](cbaseallocator.md) class or write an entirely new allocator class.</span></span> <span data-ttu-id="b97f3-137">Se il filtro ha un allocatore personalizzato, eseguire l'override dei metodi seguenti, a seconda del PIN che usa l'allocatore:</span><span class="sxs-lookup"><span data-stu-id="b97f3-137">If your filter has a custom allocator, override the following methods, depending on which pin uses the allocator:</span></span>

-   <span data-ttu-id="b97f3-138">Pin di input: [**CBaseInputPin:: Getallocator**](cbaseinputpin-getallocator.md) e [**CBaseInputPin:: NotifyAllocator**](cbaseinputpin-notifyallocator.md).</span><span class="sxs-lookup"><span data-stu-id="b97f3-138">Input pin: [**CBaseInputPin::GetAllocator**](cbaseinputpin-getallocator.md) and [**CBaseInputPin::NotifyAllocator**](cbaseinputpin-notifyallocator.md).</span></span>
-   <span data-ttu-id="b97f3-139">Pin di output: [**CBaseOutputPin::D ecideallocator**](cbaseoutputpin-decideallocator.md).</span><span class="sxs-lookup"><span data-stu-id="b97f3-139">Output pin: [**CBaseOutputPin::DecideAllocator**](cbaseoutputpin-decideallocator.md).</span></span>

<span data-ttu-id="b97f3-140">Se l'altro filtro si rifiuta di connettersi usando l'allocatore personalizzato, il filtro può interrompere la connessione oppure connettersi con l'allocatore dell'altro filtro.</span><span class="sxs-lookup"><span data-stu-id="b97f3-140">If the other filter refuses to connect using your custom allocator, your filter can either fail the connection, or else connect with the other filter's allocator.</span></span> <span data-ttu-id="b97f3-141">Nel secondo caso, potrebbe essere necessario impostare un flag interno che indichi il tipo di allocatore.</span><span class="sxs-lookup"><span data-stu-id="b97f3-141">In the latter case, you might need to set an internal flag indicating the type of allocator.</span></span> <span data-ttu-id="b97f3-142">Per un esempio di questo approccio, vedere [**classe CDrawImage**](cdrawimage.md).</span><span class="sxs-lookup"><span data-stu-id="b97f3-142">For an example of this approach, see [**CDrawImage Class**](cdrawimage.md).</span></span>

<span data-ttu-id="b97f3-143">Successivo: [passaggio 5. Trasformare l'immagine](step-5--transform-the-image.md).</span><span class="sxs-lookup"><span data-stu-id="b97f3-143">Next: [Step 5. Transform the Image](step-5--transform-the-image.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b97f3-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b97f3-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b97f3-145">Scrittura di filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="b97f3-145">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



