---
description: Questo esempio compila un grafico di anteprima video usando il metodo ICaptureGraphBuilder2::RenderStream in DirectShow.
ms.assetid: 9b401de1-910a-41f7-bf80-dda73ee4a204
title: Anteprima di video (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 482fed2e164bbe867d848b05d417c89d0790256f
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406894"
---
# <a name="previewing-video-directshow"></a><span data-ttu-id="83700-103">Anteprima di video (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="83700-103">Previewing Video (DirectShow)</span></span>

<span data-ttu-id="83700-104">Per compilare un grafico di anteprima video, chiamare il [**metodo ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) come segue:</span><span class="sxs-lookup"><span data-stu-id="83700-104">To build a video preview graph, call the [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method as follows:</span></span>


```C++
ICaptureGraphBuilder2 *pBuild; // Capture Graph Builder
// Initialize pBuild (not shown).

IBaseFilter *pCap; // Video capture filter.

/* Initialize pCap and add it to the filter graph (not shown). */

hr = pBuild->RenderStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, 
    pCap, NULL, NULL);
```



<span data-ttu-id="83700-105">Questo esempio presuppone quanto segue:</span><span class="sxs-lookup"><span data-stu-id="83700-105">This example assumes the following:</span></span>

-   <span data-ttu-id="83700-106">*pBuild* è stato inizializzato, come descritto in [Informazioni su Capture Graph Builder](about-the-capture-graph-builder.md).</span><span class="sxs-lookup"><span data-stu-id="83700-106">*pBuild* was initialized, as described in [About the Capture Graph Builder](about-the-capture-graph-builder.md).</span></span>
-   <span data-ttu-id="83700-107">*pCap* è stato inizializzato creando un'istanza del filtro di acquisizione e aggiungendola al grafico dei filtri, come descritto in [Selezione di un dispositivo di acquisizione](selecting-a-capture-device.md).</span><span class="sxs-lookup"><span data-stu-id="83700-107">*pCap* was initialized, by creating an instance of the capture filter and adding it to the filter graph, as described in [Selecting a Capture Device](selecting-a-capture-device.md).</span></span>

<span data-ttu-id="83700-108">Il primo parametro del [**metodo ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) specifica una categoria di pin. per un grafico di anteprima, usare **PIN \_ CATEGORY \_ PREVIEW**.</span><span class="sxs-lookup"><span data-stu-id="83700-108">The first parameter to the [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method specifies a pin category; for a preview graph, use **PIN\_CATEGORY\_PREVIEW**.</span></span> <span data-ttu-id="83700-109">Il secondo parametro specifica un tipo di supporto, come GUID di tipo principale.</span><span class="sxs-lookup"><span data-stu-id="83700-109">The second parameter specifies a media type, as a major type GUID.</span></span> <span data-ttu-id="83700-110">Per il video, usare **MEDIATYPE \_ Video**.</span><span class="sxs-lookup"><span data-stu-id="83700-110">For video, use **MEDIATYPE\_Video**.</span></span> <span data-ttu-id="83700-111">I dispositivi DV offrono audio e video interleaved, per i quali il tipo di supporto **è MEDIATYPE \_ Interleaved.**</span><span class="sxs-lookup"><span data-stu-id="83700-111">DV devices deliver interleaved audio and video, for which the media type is **MEDIATYPE\_Interleaved**.</span></span> <span data-ttu-id="83700-112">Per altre informazioni sull'acquisizione DV, vedere [Video digitale in DirectShow.](digital-video-in-directshow.md)</span><span class="sxs-lookup"><span data-stu-id="83700-112">(For more information about DV capture, see [Digital Video in DirectShow](digital-video-in-directshow.md).)</span></span>

<span data-ttu-id="83700-113">Il terzo parametro è un puntatore all'interfaccia [**IBaseFilter del**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) filtro di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="83700-113">The third parameter is a pointer to the capture filter's [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface.</span></span> <span data-ttu-id="83700-114">I due parametri successivi non sono necessari in questo esempio.</span><span class="sxs-lookup"><span data-stu-id="83700-114">The next two parameters are not needed in this example.</span></span> <span data-ttu-id="83700-115">Vengono usati per specificare filtri aggiuntivi che potrebbero essere necessari per eseguire il rendering del flusso.</span><span class="sxs-lookup"><span data-stu-id="83700-115">They are used to specify additional filters that might be needed to render the stream.</span></span> <span data-ttu-id="83700-116">Impostando l'ultimo parametro **su NULL,** Capture Graph Builder seleziona un renderer predefinito per il flusso, in base al tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="83700-116">Setting the last parameter to **NULL** causes the Capture Graph Builder to select a default renderer for the stream, based on the media type.</span></span> <span data-ttu-id="83700-117">Per i video, Capture Graph Builder usa sempre il filtro [Renderer video](video-renderer-filter.md) come renderer predefinito.</span><span class="sxs-lookup"><span data-stu-id="83700-117">For video, the Capture Graph Builder always uses the [Video Renderer](video-renderer-filter.md) filter as the default renderer.</span></span>

> [!Note]  
> <span data-ttu-id="83700-118">In Windows XP e versioni successive, sebbene video mixing renderer (VMR) sia il renderer video predefinito per i metodi [**IGraphBuilder,**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) non è il renderer predefinito per il [**metodo RenderStream.**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream)</span><span class="sxs-lookup"><span data-stu-id="83700-118">In Windows XP and later, although the Video Mixing Renderer (VMR) is the default video renderer for [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) methods, it is not the default renderer for the [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method.</span></span> <span data-ttu-id="83700-119">In qualsiasi piattaforma, Capture Graph Builder usa sempre il filtro renderer video precedente, a meno che non venga specificato diversamente.</span><span class="sxs-lookup"><span data-stu-id="83700-119">On any platform, the Capture Graph Builder always uses the old Video Renderer filter unless you specify otherwise.</span></span>

 

<span data-ttu-id="83700-120">Anche se la categoria pin viene specificata come **PIN \_ CATEGORY \_ PREVIEW,** non è importante se il filtro dispone effettivamente di un pin di anteprima; potrebbe avere un pin della porta video o solo un pin di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="83700-120">Although the pin category is given as **PIN\_CATEGORY\_PREVIEW**, it does not matter whether the filter actually has a preview pin; it could have a video port pin or just a capture pin.</span></span> <span data-ttu-id="83700-121">In entrambi i casi, Capture Graph Builder compila automaticamente il grafico corretto.</span><span class="sxs-lookup"><span data-stu-id="83700-121">In either case, the Capture Graph Builder automatically builds the correct graph.</span></span>

<span data-ttu-id="83700-122">Il diagramma seguente illustra il grafico più semplice possibile per l'anteprima del video.</span><span class="sxs-lookup"><span data-stu-id="83700-122">The following diagram shows the simplest possible graph for previewing video.</span></span>

![Grafico di anteprima video](images/vidcap01.png)

<span data-ttu-id="83700-124">In questo diagramma il filtro di acquisizione ha un segnaposto di anteprima che si connette direttamente al renderer video.</span><span class="sxs-lookup"><span data-stu-id="83700-124">In this diagram, the capture filter has a preview pin, which connects directly to the video renderer.</span></span>

<span data-ttu-id="83700-125">Se il filtro di acquisizione ha solo un pin di acquisizione, Capture Graph Builder inserisce un filtro [Smart Tee,](smart-tee-filter.md) che suddivide il flusso in un flusso di acquisizione e in un flusso di anteprima.</span><span class="sxs-lookup"><span data-stu-id="83700-125">If the capture filter has only a capture pin, the Capture Graph Builder inserts a [Smart Tee](smart-tee-filter.md) filter, which splits the stream into a capture stream and a preview stream.</span></span> <span data-ttu-id="83700-126">Questa operazione è descritta in modo più dettagliato in [Combinazione di acquisizione video e anteprima.](combining-video-capture-and-preview.md)</span><span class="sxs-lookup"><span data-stu-id="83700-126">This is described in more detail in [Combining Video Capture and Preview](combining-video-capture-and-preview.md).</span></span>

<span data-ttu-id="83700-127">In alcuni casi, il flusso video deve passare attraverso il filtro Overlay Mixer.</span><span class="sxs-lookup"><span data-stu-id="83700-127">In some cases, the video stream must go through the Overlay Mixer filter.</span></span> <span data-ttu-id="83700-128">In tal caso, [**il metodo RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) lo aggiunge automaticamente al grafico.</span><span class="sxs-lookup"><span data-stu-id="83700-128">If so, the [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method adds it to the graph automatically.</span></span>

## <a name="related-topics"></a><span data-ttu-id="83700-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="83700-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83700-130">Combinazione di acquisizione video e anteprima</span><span class="sxs-lookup"><span data-stu-id="83700-130">Combining Video Capture and Preview</span></span>](combining-video-capture-and-preview.md)
</dt> <dt>

[<span data-ttu-id="83700-131">Acquisizione video</span><span class="sxs-lookup"><span data-stu-id="83700-131">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 



