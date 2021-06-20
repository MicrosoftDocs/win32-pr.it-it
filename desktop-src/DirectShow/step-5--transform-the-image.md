---
description: Usare questo esempio per comprendere in che modo il codificatore RLE può implementare il metodo come parte della scrittura di un filtro di trasformazione.
ms.assetid: b7d878ab-523f-4b52-b98d-c9d4fa18ce8a
title: Passaggio 5. Trasformare l'immagine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ac9d32e48ba438f8bde2d8d4d9aca3b827ebc0c
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406784"
---
# <a name="step-5-transform-the-image"></a><span data-ttu-id="bbcf9-104">Passaggio 5.</span><span class="sxs-lookup"><span data-stu-id="bbcf9-104">Step 5.</span></span> <span data-ttu-id="bbcf9-105">Trasformare l'immagine</span><span class="sxs-lookup"><span data-stu-id="bbcf9-105">Transform the Image</span></span>

<span data-ttu-id="bbcf9-106">Questo è il passaggio 5 dell'esercitazione [Scrittura di filtri di trasformazione.](writing-transform-filters.md)</span><span class="sxs-lookup"><span data-stu-id="bbcf9-106">This is step 5 of the tutorial [Writing Transform Filters](writing-transform-filters.md).</span></span>

<span data-ttu-id="bbcf9-107">Il filtro upstream fornisce esempi di contenuti multimediali al filtro di trasformazione chiamando il metodo [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) sul pin di input del filtro di trasformazione.</span><span class="sxs-lookup"><span data-stu-id="bbcf9-107">The upstream filter delivers media samples to the transform filter by calling the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method on the transform filter's input pin.</span></span> <span data-ttu-id="bbcf9-108">Per elaborare i dati, il filtro di trasformazione chiama **il metodo Transform,** che è virtuale puro.</span><span class="sxs-lookup"><span data-stu-id="bbcf9-108">To process the data, the transform filter calls the **Transform** method, which is pure virtual.</span></span> <span data-ttu-id="bbcf9-109">Le **classi CTransformFilter** **e CTransInPlaceFilter** usano due versioni diverse di questo metodo:</span><span class="sxs-lookup"><span data-stu-id="bbcf9-109">The **CTransformFilter** and **CTransInPlaceFilter** classes use two different versions of this method:</span></span>

-   <span data-ttu-id="bbcf9-110">[**CTransformFilter::Transform**](ctransformfilter-transform.md) accetta un puntatore all'esempio di input e un puntatore all'esempio di output.</span><span class="sxs-lookup"><span data-stu-id="bbcf9-110">[**CTransformFilter::Transform**](ctransformfilter-transform.md) takes a pointer to the input sample and a pointer to the output sample.</span></span> <span data-ttu-id="bbcf9-111">Prima che il filtro chiami il metodo , copia le proprietà di esempio dall'esempio di input all'esempio di output, inclusi i timestamp.</span><span class="sxs-lookup"><span data-stu-id="bbcf9-111">Before the filter calls the method, it copies the sample properties from the input sample to the output sample, including the time stamps.</span></span>
-   <span data-ttu-id="bbcf9-112">[**CTransInPlaceFilter::Transform**](ctransinplacefilter-transform.md) accetta un puntatore all'esempio di input.</span><span class="sxs-lookup"><span data-stu-id="bbcf9-112">[**CTransInPlaceFilter::Transform**](ctransinplacefilter-transform.md) takes a pointer to the input sample.</span></span> <span data-ttu-id="bbcf9-113">Il filtro modifica i dati sul posto.</span><span class="sxs-lookup"><span data-stu-id="bbcf9-113">The filter modifies the data in place.</span></span>

<span data-ttu-id="bbcf9-114">Se il **metodo Transform** restituisce S \_ OK, il filtro recapita il campione a valle.</span><span class="sxs-lookup"><span data-stu-id="bbcf9-114">If the **Transform** method returns S\_OK, the filter delivers the sample downstream.</span></span> <span data-ttu-id="bbcf9-115">Per ignorare un frame, restituire S \_ FALSE.</span><span class="sxs-lookup"><span data-stu-id="bbcf9-115">To skip a frame, return S\_FALSE.</span></span> <span data-ttu-id="bbcf9-116">Se si verifica un errore di flusso, restituire un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="bbcf9-116">If there is a streaming error, return a failure code.</span></span>

<span data-ttu-id="bbcf9-117">L'esempio seguente illustra come il codificatore RLE potrebbe implementare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="bbcf9-117">The following example shows how the RLE encoder might implement this method.</span></span> <span data-ttu-id="bbcf9-118">L'implementazione potrebbe variare notevolmente, a seconda del filtro.</span><span class="sxs-lookup"><span data-stu-id="bbcf9-118">Your own implementation might differ considerably, depending on what your filter does.</span></span>


```C++
HRESULT CRleFilter::Transform(IMediaSample *pSource, IMediaSample *pDest)
{
    // Get pointers to the underlying buffers.
    BYTE *pBufferIn, *pBufferOut;
    hr = pSource->GetPointer(&pBufferIn);
    if (FAILED(hr))
    {
        return hr;
    }
    hr = pDest->GetPointer(&pBufferOut);
    if (FAILED(hr))
    {
        return hr;
    }
    // Process the data.
    DWORD cbDest = EncodeFrame(pBufferIn, pBufferOut);
    KASSERT((long)cbDest <= pDest->GetSize());

    pDest->SetActualDataLength(cbDest);
    pDest->SetSyncPoint(TRUE);
    return S_OK;
}
```



<span data-ttu-id="bbcf9-119">Questo esempio presuppone che EncodeFrame sia un metodo privato che implementa la codifica RLE.</span><span class="sxs-lookup"><span data-stu-id="bbcf9-119">This example assumes that EncodeFrame is a private method that implements the RLE encoding.</span></span> <span data-ttu-id="bbcf9-120">L'algoritmo di codifica stesso non è descritto qui. Per informazioni dettagliate, vedere l'argomento "Compressione bitmap" nella documentazione di Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="bbcf9-120">The encoding algorithm itself is not described here; for details, see the topic "Bitmap Compression" in the Platform SDK documentation.</span></span>

<span data-ttu-id="bbcf9-121">In primo luogo, [**l'esempio chiama IMediaSample::GetPointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) per recuperare gli indirizzi dei buffer sottostanti.</span><span class="sxs-lookup"><span data-stu-id="bbcf9-121">First, the example calls [**IMediaSample::GetPointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) to retrieve the addresses of the underlying buffers.</span></span> <span data-ttu-id="bbcf9-122">Li passa al metodo EncoderFrame privato.</span><span class="sxs-lookup"><span data-stu-id="bbcf9-122">It passes these to the private EncoderFrame method.</span></span> <span data-ttu-id="bbcf9-123">Chiama quindi [**IMediaSample::SetActualDataLength**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setactualdatalength) per specificare la lunghezza dei dati codificati.</span><span class="sxs-lookup"><span data-stu-id="bbcf9-123">Then it calls [**IMediaSample::SetActualDataLength**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setactualdatalength) to specify the length of the encoded data.</span></span> <span data-ttu-id="bbcf9-124">Il filtro downstream necessita di queste informazioni per poter gestire correttamente il buffer.</span><span class="sxs-lookup"><span data-stu-id="bbcf9-124">The downstream filter needs this information so that it can manage the buffer properly.</span></span> <span data-ttu-id="bbcf9-125">Infine, il metodo chiama [**IMediaSample::SetSyncPoint**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setsyncpoint) per impostare il flag del fotogramma chiave su **TRUE.**</span><span class="sxs-lookup"><span data-stu-id="bbcf9-125">Finally, the method calls [**IMediaSample::SetSyncPoint**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setsyncpoint) to set the key frame flag to **TRUE**.</span></span> <span data-ttu-id="bbcf9-126">La codifica della lunghezza di esecuzione non usa fotogrammi differenziali, quindi ogni fotogramma è un fotogramma chiave.</span><span class="sxs-lookup"><span data-stu-id="bbcf9-126">Run-length encoding does not use any delta frames, so every frame is a key frame.</span></span> <span data-ttu-id="bbcf9-127">Per i frame differenziali, impostare il valore su **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="bbcf9-127">For delta frames, set the value to **FALSE**.</span></span>

<span data-ttu-id="bbcf9-128">Altri problemi che è necessario considerare includono:</span><span class="sxs-lookup"><span data-stu-id="bbcf9-128">Other issues that you must consider include:</span></span>

-   <span data-ttu-id="bbcf9-129">Timestamp.</span><span class="sxs-lookup"><span data-stu-id="bbcf9-129">Time stamps.</span></span> <span data-ttu-id="bbcf9-130">La **classe CTransformFilter** indica il timestamp dell'esempio di output prima di chiamare il **metodo Transform.**</span><span class="sxs-lookup"><span data-stu-id="bbcf9-130">The **CTransformFilter** class timestamps the output sample before calling the **Transform** method.</span></span> <span data-ttu-id="bbcf9-131">Copia i valori del timestamp dall'esempio di input, senza modificarli.</span><span class="sxs-lookup"><span data-stu-id="bbcf9-131">It copies the time stamp values from the input sample, without modifying them.</span></span> <span data-ttu-id="bbcf9-132">Se il filtro deve modificare i timestamp, chiamare [**IMediaSample::SetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) nell'esempio di output.</span><span class="sxs-lookup"><span data-stu-id="bbcf9-132">If your filter needs to change the time stamps, call [**IMediaSample::SetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) on the output sample.</span></span>
-   <span data-ttu-id="bbcf9-133">Modifiche al formato.</span><span class="sxs-lookup"><span data-stu-id="bbcf9-133">Format changes.</span></span> <span data-ttu-id="bbcf9-134">Il filtro upstream può modificare i formati durante il flusso collegando un tipo di supporto all'esempio.</span><span class="sxs-lookup"><span data-stu-id="bbcf9-134">The upstream filter can change formats mid-stream by attaching a media type to the sample.</span></span> <span data-ttu-id="bbcf9-135">Prima di procedere, chiama [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) sul pin di input del filtro.</span><span class="sxs-lookup"><span data-stu-id="bbcf9-135">Before doing so, it calls [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) on your filter's input pin.</span></span> <span data-ttu-id="bbcf9-136">Nella classe **CTransformFilter** viene generata una chiamata a **CheckInputType** seguita da **CheckTransform.**</span><span class="sxs-lookup"><span data-stu-id="bbcf9-136">In the **CTransformFilter** class, this results in a call to **CheckInputType** followed by **CheckTransform**.</span></span> <span data-ttu-id="bbcf9-137">Il filtro downstream può anche modificare i tipi di supporti, usando lo stesso meccanismo.</span><span class="sxs-lookup"><span data-stu-id="bbcf9-137">The downstream filter can also change media types, using the same mechanism.</span></span> <span data-ttu-id="bbcf9-138">Nel filtro personalizzato è necessario controllare due elementi:</span><span class="sxs-lookup"><span data-stu-id="bbcf9-138">In your own filter, there are two things to watch for:</span></span>

    -   <span data-ttu-id="bbcf9-139">Assicurarsi che **QueryAccept** non restituirà false accettazioni.</span><span class="sxs-lookup"><span data-stu-id="bbcf9-139">Make sure that **QueryAccept** does not return false acceptances.</span></span>
    -   <span data-ttu-id="bbcf9-140">Se il filtro accetta modifiche al formato, verificarle all'interno del **metodo Transform** chiamando [**IMediaSample::GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype).</span><span class="sxs-lookup"><span data-stu-id="bbcf9-140">If your filter does accept format changes, check for them inside the **Transform** method by calling [**IMediaSample::GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype).</span></span> <span data-ttu-id="bbcf9-141">Se il metodo restituisce S \_ OK, il filtro deve rispondere alla modifica del formato.</span><span class="sxs-lookup"><span data-stu-id="bbcf9-141">If that method returns S\_OK, your filter must respond to the format change.</span></span>

    <span data-ttu-id="bbcf9-142">Per altre informazioni, vedere [Modifiche al formato dinamico.](dynamic-format-changes.md)</span><span class="sxs-lookup"><span data-stu-id="bbcf9-142">For more information, see [Dynamic Format Changes](dynamic-format-changes.md).</span></span>

-   <span data-ttu-id="bbcf9-143">Discussioni.</span><span class="sxs-lookup"><span data-stu-id="bbcf9-143">Threads.</span></span> <span data-ttu-id="bbcf9-144">Sia in **CTransformFilter** che **in CTransInPlaceFilter** il filtro di trasformazione fornisce esempi di output in modo sincrono all'interno **del metodo Receive.**</span><span class="sxs-lookup"><span data-stu-id="bbcf9-144">In both **CTransformFilter** and **CTransInPlaceFilter**, the transform filter delivers output samples synchronously inside the **Receive** method.</span></span> <span data-ttu-id="bbcf9-145">Il filtro non crea thread di lavoro per elaborare i dati.</span><span class="sxs-lookup"><span data-stu-id="bbcf9-145">The filter does not create any worker threads to process the data.</span></span> <span data-ttu-id="bbcf9-146">In genere, non esiste alcun motivo per cui un filtro di trasformazione crei thread di lavoro.</span><span class="sxs-lookup"><span data-stu-id="bbcf9-146">Typically, there is no reason for a transform filter to create worker threads.</span></span>

<span data-ttu-id="bbcf9-147">Passaggio [successivo: Passaggio 6. Aggiunta del supporto per COM.](step-6--add-support-for-com.md)</span><span class="sxs-lookup"><span data-stu-id="bbcf9-147">Next: [Step 6. Add Support for COM](step-6--add-support-for-com.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bbcf9-148">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bbcf9-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bbcf9-149">Scrittura di filtri DirectMostra filtri</span><span class="sxs-lookup"><span data-stu-id="bbcf9-149">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



