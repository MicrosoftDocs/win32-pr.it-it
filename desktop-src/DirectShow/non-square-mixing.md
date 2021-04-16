---
description: Combinazione non quadrata
ms.assetid: 8d27a921-5638-43ac-807d-e3bd7b9b2de8
title: Combinazione non quadrata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79d23f423f0dbe19f1ff0ba35c44f8fd2f8732bc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522050"
---
# <a name="non-square-mixing"></a><span data-ttu-id="57e0a-103">Combinazione non quadrata</span><span class="sxs-lookup"><span data-stu-id="57e0a-103">Non-Square Mixing</span></span>

<span data-ttu-id="57e0a-104">Questo argomento si applica a Windows XP Service Pack 2 o versioni successive.</span><span class="sxs-lookup"><span data-stu-id="57e0a-104">This topic applies to Windows XP Service Pack 2 or later.</span></span>

<span data-ttu-id="57e0a-105">Quando VMR-9 combina due o più flussi, è possibile che si verifichi il ridimensionamento in due punti: quando il mixer composi i flussi di input e quando Allocator-Presenter esegue il rendering dell'immagine composita.</span><span class="sxs-lookup"><span data-stu-id="57e0a-105">When the VMR-9 mixes two or more streams, there are two points where scaling can occur: When the mixer composites the input streams, and when the allocator-presenter renders the composited image.</span></span>

![operazioni di combinazione VMR](images/vmr-nonsquare-mixing.png)

<span data-ttu-id="57e0a-107">Le versioni precedenti di VMR-9 compostano sempre i flussi di input usando una percentuale quadrata (1:1) di proporzioni in pixel, anche in presenza di un unico flusso video.</span><span class="sxs-lookup"><span data-stu-id="57e0a-107">Previous versions of the VMR-9 always composited the input streams using a square (1:1) pixel aspect ratio (PAR), even when there was only a single video stream.</span></span> <span data-ttu-id="57e0a-108">Se il flusso di input presenta pixel non quadrati, questo ha causato un'operazione di ridimensionamento non necessaria.</span><span class="sxs-lookup"><span data-stu-id="57e0a-108">If the input stream had non-square pixels, this caused an unnecessary scaling operation.</span></span> <span data-ttu-id="57e0a-109">Il ridimensionamento deve essere evitato quanto più possibile, ovviamente perché peggiora la qualità dell'immagine finale.</span><span class="sxs-lookup"><span data-stu-id="57e0a-109">Scaling should be avoided as much as possible, of course, because it degrades the final image quality.</span></span>

<span data-ttu-id="57e0a-110">A partire da Windows XP Service Pack 2, VMR-9 supporta due modi diversi per evitare il problema del doppio ridimensionamento:</span><span class="sxs-lookup"><span data-stu-id="57e0a-110">Starting in Windows XP Service Pack 2, the VMR-9 supports two different ways to avoid the problem of double scaling:</span></span>

-   <span data-ttu-id="57e0a-111">Implementare un allocatore-Presenter personalizzato e supportare l'interfaccia [**IVMRSurfaceAllocatorEx9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatorex9) .</span><span class="sxs-lookup"><span data-stu-id="57e0a-111">Implement a custom allocator-presenter and support the [**IVMRSurfaceAllocatorEx9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatorex9) interface.</span></span>
-   <span data-ttu-id="57e0a-112">Usare la modalità di combinazione non quadrata.</span><span class="sxs-lookup"><span data-stu-id="57e0a-112">Use non-square mixing mode.</span></span>

<span data-ttu-id="57e0a-113">In questa sezione viene descritta la modalità di combinazione non quadrata.</span><span class="sxs-lookup"><span data-stu-id="57e0a-113">This section describes non-square mixing mode.</span></span> <span data-ttu-id="57e0a-114">Le applicazioni possono combinare entrambe le tecniche.</span><span class="sxs-lookup"><span data-stu-id="57e0a-114">Applications can combine both techniques.</span></span>

<span data-ttu-id="57e0a-115">**Funzionamento della combinazione non quadrata**</span><span class="sxs-lookup"><span data-stu-id="57e0a-115">**How Non-Square Mixing Works**</span></span>

<span data-ttu-id="57e0a-116">In modalità di combinazione non quadrata, VMR-9 Seleziona un flusso di input come dimensione di destinazione e PAR.</span><span class="sxs-lookup"><span data-stu-id="57e0a-116">In non-square mixing mode, the VMR-9 selects one input stream to be the target size and PAR.</span></span> <span data-ttu-id="57e0a-117">Il mixer di VMR non ridimensiona il video da tale flusso o da altri flussi con le stesse dimensioni dell'immagine e PAR.</span><span class="sxs-lookup"><span data-stu-id="57e0a-117">The VMR's mixer does not scale the video from that stream or from any other streams with the same image size and PAR.</span></span> <span data-ttu-id="57e0a-118">I flussi con dimensioni o proporzioni diverse vengono ridimensionati in modo da corrispondere alla parità di destinazione e alla cassettatura per adattarsi alle dimensioni dell'immagine di output finale.</span><span class="sxs-lookup"><span data-stu-id="57e0a-118">Streams with a different size or aspect ratio are scaled to match the target PAR and letterboxed to fit the final output image size.</span></span>

<span data-ttu-id="57e0a-119">La scelta dei flussi dipende dalla modalità di combinazione corrente:</span><span class="sxs-lookup"><span data-stu-id="57e0a-119">The choice of streams depends on the current mixing mode:</span></span>

-   <span data-ttu-id="57e0a-120">La modalità di combinazione YUV è limitata a un flusso video sul pin 0.</span><span class="sxs-lookup"><span data-stu-id="57e0a-120">YUV mixing mode is restricted to one video stream on pin 0.</span></span> <span data-ttu-id="57e0a-121">(Gli altri pin possono avere flussi di didascalie o sottotitoli). Pertanto, VMR-9 seleziona sempre il pin 0 per la dimensione dell'immagine di destinazione e la PAR.</span><span class="sxs-lookup"><span data-stu-id="57e0a-121">(The other pins may have subpicture or closed caption streams.) Therefore, the VMR-9 always selects pin 0 for the target image size and PAR.</span></span>
-   <span data-ttu-id="57e0a-122">In modalità di combinazione RGB, VMR seleziona il flusso con le dimensioni massime dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="57e0a-122">In RGB mixing mode, the VMR selects the stream with the largest image size.</span></span> <span data-ttu-id="57e0a-123">Se è presente più di un oggetto, viene selezionato quello con l'ordine z più elevato; Se è ancora presente una cravatta, viene selezionato il flusso con il numero di pin più basso.</span><span class="sxs-lookup"><span data-stu-id="57e0a-123">If there is more than one, it selects the one with the highest z-order; and if there is still a tie, it selects the stream with the lowest pin number.</span></span>

<span data-ttu-id="57e0a-124">**Esempi di operazione**</span><span class="sxs-lookup"><span data-stu-id="57e0a-124">**Examples of Operation**</span></span>

<span data-ttu-id="57e0a-125">**Esempio 1.**</span><span class="sxs-lookup"><span data-stu-id="57e0a-125">**Example 1.**</span></span> <span data-ttu-id="57e0a-126">Il flusso 0 è 720 x 480 pixel con proporzioni dell'immagine 16:9.</span><span class="sxs-lookup"><span data-stu-id="57e0a-126">Stream 0 is 720 x 480 pixels with a picture aspect ratio of 16:9.</span></span> <span data-ttu-id="57e0a-127">Il flusso 1 è un 640 x 480 pixel con proporzioni dell'immagine 4:3.</span><span class="sxs-lookup"><span data-stu-id="57e0a-127">Stream 1 is a 640 x 480 pixels with a picture aspect ratio of 4:3.</span></span>

<span data-ttu-id="57e0a-128">In questo esempio, il flusso 0 ha le dimensioni massime dell'immagine, quindi VMR sceglie questo flusso, indipendentemente dalla modalità di combinazione RGB o dalla modalità di combinazione YUB.</span><span class="sxs-lookup"><span data-stu-id="57e0a-128">In this example, stream 0 has the largest image size, so the VMR chooses this stream, regardless of RGB mixing mode or YUB mixing mode.</span></span> <span data-ttu-id="57e0a-129">Il valore PAR è 32:27 (16:9/720:480), che indica che l'immagine deve essere allungata orizzontalmente in base a questo rapporto per produrre le proporzioni dell'immagine 16:9 corrette.</span><span class="sxs-lookup"><span data-stu-id="57e0a-129">The PAR is 32:27 (16:9 / 720:480), meaning the image must be stretched horizontally by this ratio to produce the correct 16:9 picture aspect ratio.</span></span>

<span data-ttu-id="57e0a-130">Per corrispondere alla parità di destinazione, il mixer VMR ridimensiona il flusso 1 in base al rapporto inverso (27:32), ottenendo un'immagine 540 x 480.</span><span class="sxs-lookup"><span data-stu-id="57e0a-130">To match the target PAR, the VMR mixer scales stream 1 by the inverse ratio (27:32), resulting in a 540 x 480 image.</span></span> <span data-ttu-id="57e0a-131">I due flussi vengono quindi composti in una superficie.</span><span class="sxs-lookup"><span data-stu-id="57e0a-131">The two streams are then composited onto one surface.</span></span> <span data-ttu-id="57e0a-132">Per visualizzare correttamente l'immagine risultante, il relatore allocatore deve allungare l'immagine orizzontalmente per adattarsi alle proporzioni dell'immagine 16:9.</span><span class="sxs-lookup"><span data-stu-id="57e0a-132">To display the resulting image correctly, the allocator presenter must stretch the image horizontally to fit the 16:9 picture aspect ratio.</span></span>

![esempio 1.](images/vmr-nonsquare-mixing2.png)

<span data-ttu-id="57e0a-134">**Esempio 2.**</span><span class="sxs-lookup"><span data-stu-id="57e0a-134">**Example 2.**</span></span> <span data-ttu-id="57e0a-135">Il flusso 0 è 720 x 480 pixel con proporzioni dell'immagine 16:9.</span><span class="sxs-lookup"><span data-stu-id="57e0a-135">Stream 0 is 720 x 480 pixels with a picture aspect ratio of 16:9.</span></span> <span data-ttu-id="57e0a-136">Il flusso 1 è un 1024 x 768 pixel con proporzioni dell'immagine 4:3.</span><span class="sxs-lookup"><span data-stu-id="57e0a-136">Stream 1 is a 1024 x 768 pixels with a picture aspect ratio of 4:3.</span></span>

<span data-ttu-id="57e0a-137">Se VMR-9 USA la modalità di combinazione YUV, seleziona sempre il flusso 0.</span><span class="sxs-lookup"><span data-stu-id="57e0a-137">If the VMR-9 is using YUV mixing mode, it always selects stream 0.</span></span> <span data-ttu-id="57e0a-138">Estende quindi il flusso da 1 a 540 x 480 pixel, in modo da corrispondere alla PAR del flusso 0.</span><span class="sxs-lookup"><span data-stu-id="57e0a-138">Therefore, it stretches stream 1 to 540 x 480 pixels, to match the PAR of stream 0.</span></span>

<span data-ttu-id="57e0a-139">Se VMR-9 USA la modalità di combinazione RGB, seleziona il flusso 1 come destinazione, perché tale flusso ha le dimensioni massime dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="57e0a-139">If the VMR-9 is using RGB mixing mode, it selects stream 1 as the target, because that stream has the largest image size.</span></span> <span data-ttu-id="57e0a-140">Estende il flusso 0 alla dimensione di un'immagine di 1024 x 576 pixel.</span><span class="sxs-lookup"><span data-stu-id="57e0a-140">It stretches stream 0 to an image size of 1024 x 576 pixels.</span></span> <span data-ttu-id="57e0a-141">Si noti che in questo caso l'immagine composita ha un valore pari a 1:1, pertanto non è necessario che l'allocatore-Presenter venga corretto per i pixel non quadrati.</span><span class="sxs-lookup"><span data-stu-id="57e0a-141">Note that in this case, the composited image has a PAR of 1:1, so the allocator-presenter does not have to correct for non-square pixels.</span></span> <span data-ttu-id="57e0a-142">Potrebbe comunque essere necessario estendere il video per tenere conto del rettangolo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="57e0a-142">(It might still need to stretch the video to account for the destination rectangle.)</span></span>

<span data-ttu-id="57e0a-143">**Uso della modalità di combinazione non quadrata**</span><span class="sxs-lookup"><span data-stu-id="57e0a-143">**Using Non-Square Mixing Mode**</span></span>

<span data-ttu-id="57e0a-144">La modalità di combinazione non quadrata è consigliata se si verifica una delle condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="57e0a-144">Non-square mixing mode is recommended if either of the following conditions are true:</span></span>

-   <span data-ttu-id="57e0a-145">L'applicazione non invia mai più di un flusso video a VMR-9.</span><span class="sxs-lookup"><span data-stu-id="57e0a-145">Your application never sends more than one video stream to the VMR-9.</span></span>
-   <span data-ttu-id="57e0a-146">L'applicazione esegue il rendering dei file DVD, TV o MS-DVR.</span><span class="sxs-lookup"><span data-stu-id="57e0a-146">Your application renders DVD, television, or ms-dvr files.</span></span> <span data-ttu-id="57e0a-147">In questo caso, è consigliabile usare anche la modalità di combinazione YUV se l'hardware grafico lo supporta.</span><span class="sxs-lookup"><span data-stu-id="57e0a-147">You should also use YUV mixing mode in this case, if the graphics hardware supports it.</span></span>

<span data-ttu-id="57e0a-148">Se l'applicazione combina più flussi video che possono avere dimensioni diverse per le immagini o proporzioni di pixel, è consigliabile usare la modalità di combinazione quadrata predefinita.</span><span class="sxs-lookup"><span data-stu-id="57e0a-148">If your application mixes multiple video streams that may have varying image sizes or pixel aspect ratios, the default square mixing mode is recommended.</span></span>

<span data-ttu-id="57e0a-149">Per configurare la modalità di combinazione non quadrata, è necessario arrestare il grafico del filtro e tutti i pin di input disconnessi in VMR-9.</span><span class="sxs-lookup"><span data-stu-id="57e0a-149">To configure non-square mixing mode, the filter graph must be stopped and all input pins disconnected on the VMR-9.</span></span> <span data-ttu-id="57e0a-150">Chiamare quindi [**IVMRMixerControl9:: SetMixingPrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs) con il \_ flag NonSquareMixing di MixerPref9:</span><span class="sxs-lookup"><span data-stu-id="57e0a-150">Then call [**IVMRMixerControl9::SetMixingPrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs) with the MixerPref9\_NonSquareMixing flag:</span></span>


```C++
DWORD dwPrefs;
pMixControl->GetMixingPrefs(&dwPrefs);  
dwPrefs |= MixerPref9_NonSquareMixing;
pMixControl->SetMixingPrefs(dwPrefs);
```



> [!Note]  
> <span data-ttu-id="57e0a-151">Se si combina il \_ flag MixerPref9 NonSquareMixing con il \_ flag MixerPref9 ARADJUSTXORY, VMR-9 ignora il flag MixerPref9 ARAdjustXorY \_ .</span><span class="sxs-lookup"><span data-stu-id="57e0a-151">If you combine the MixerPref9\_NonSquareMixing flag with the MixerPref9\_ARAdjustXorY flag, the VMR-9 ignores the MixerPref9\_ARAdjustXorY flag.</span></span>

 

<span data-ttu-id="57e0a-152">Se l'applicazione usa un presentatore-Presenter personalizzato con modalità di combinazione non quadrata, tenere presente che l'immagine composita potrebbe avere una PAR non quadrata.</span><span class="sxs-lookup"><span data-stu-id="57e0a-152">If your application uses a custom allocator-presenter with non-square mixing mode, be aware that the composited image may have a non-square PAR.</span></span> <span data-ttu-id="57e0a-153">Allocator-Presenter deve ridimensionare l'immagine in una PAR quadrata (1:1).</span><span class="sxs-lookup"><span data-stu-id="57e0a-153">The allocator-presenter must scale the image to a square (1:1) PAR.</span></span>

<span data-ttu-id="57e0a-154">**Bitmap statiche**</span><span class="sxs-lookup"><span data-stu-id="57e0a-154">**Static Bitmaps**</span></span>

<span data-ttu-id="57e0a-155">Se si usa l'interfaccia [**IVMRMixerBitmap9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9) per combinare una bitmap statica nel video, è consigliabile considerare la bitmap come un secondo flusso video per la modalità di combinazione VMR.</span><span class="sxs-lookup"><span data-stu-id="57e0a-155">If you use the [**IVMRMixerBitmap9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9) interface to blend a static bitmap onto the video, you should consider the bitmap to be a second video stream for purposes of the VMR mixing mode.</span></span>

<span data-ttu-id="57e0a-156">Il VMR considera la bitmap come avente la stessa parità della destinazione.</span><span class="sxs-lookup"><span data-stu-id="57e0a-156">The VMR treats the bitmap as having the same PAR as the target.</span></span> <span data-ttu-id="57e0a-157">Non ridimensiona la bitmap per adattarla alle proporzioni in pixel della destinazione.</span><span class="sxs-lookup"><span data-stu-id="57e0a-157">It does not scale the bitmap to adjust for the target's pixel aspect ratio.</span></span> <span data-ttu-id="57e0a-158">Nella configurazione predefinita di VMR, la destinazione ha una PAR 1:1, che corrisponde alla maggior parte delle bitmap.</span><span class="sxs-lookup"><span data-stu-id="57e0a-158">In the VMR's default configuration, the target has a 1:1 PAR, which matches most bitmaps.</span></span> <span data-ttu-id="57e0a-159">In modalità di combinazione non quadrata, la destinazione potrebbe avere pixel non quadrati.</span><span class="sxs-lookup"><span data-stu-id="57e0a-159">In non-square mixing mode, the target might have non-square pixels.</span></span> <span data-ttu-id="57e0a-160">Per assicurarsi che la bitmap venga visualizzata correttamente, l'applicazione deve fornire un'immagine il cui PAR corrisponda alla parità di destinazione.</span><span class="sxs-lookup"><span data-stu-id="57e0a-160">To ensure that the bitmap is displayed correctly, the application should supply an image whose PAR matches the target PAR.</span></span>

## <a name="related-topics"></a><span data-ttu-id="57e0a-161">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="57e0a-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="57e0a-162">Uso della modalità di combinazione VMR</span><span class="sxs-lookup"><span data-stu-id="57e0a-162">Using VMR Mixing Mode</span></span>](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



