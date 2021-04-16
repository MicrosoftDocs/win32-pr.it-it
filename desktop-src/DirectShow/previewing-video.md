---
description: Anteprima del video
ms.assetid: 9b401de1-910a-41f7-bf80-dda73ee4a204
title: Anteprima video (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae0a8f0d0a422794c4e887693e80391a99bd8d70
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104559856"
---
# <a name="previewing-video-directshow"></a><span data-ttu-id="d0e0f-103">Anteprima video (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="d0e0f-103">Previewing Video (DirectShow)</span></span>

<span data-ttu-id="d0e0f-104">Per creare un grafico di anteprima video, chiamare il metodo [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="d0e0f-104">To build a video preview graph, call the [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method as follows:</span></span>


```C++
ICaptureGraphBuilder2 *pBuild; // Capture Graph Builder
// Initialize pBuild (not shown).

IBaseFilter *pCap; // Video capture filter.

/* Initialize pCap and add it to the filter graph (not shown). */

hr = pBuild->RenderStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, 
    pCap, NULL, NULL);
```



<span data-ttu-id="d0e0f-105">In questo esempio si presuppone quanto segue:</span><span class="sxs-lookup"><span data-stu-id="d0e0f-105">This example assumes the following:</span></span>

-   <span data-ttu-id="d0e0f-106">*pBuild* è stato inizializzato, come descritto in [informazioni sul generatore di grafici di acquisizione](about-the-capture-graph-builder.md).</span><span class="sxs-lookup"><span data-stu-id="d0e0f-106">*pBuild* was initialized, as described in [About the Capture Graph Builder](about-the-capture-graph-builder.md).</span></span>
-   <span data-ttu-id="d0e0f-107">*pCap* è stato inizializzato creando un'istanza del filtro di acquisizione e aggiungendola al grafico di filtro, come descritto in [selezione di un dispositivo di acquisizione](selecting-a-capture-device.md).</span><span class="sxs-lookup"><span data-stu-id="d0e0f-107">*pCap* was initialized, by creating an instance of the capture filter and adding it to the filter graph, as described in [Selecting a Capture Device](selecting-a-capture-device.md).</span></span>

<span data-ttu-id="d0e0f-108">Il primo parametro del metodo [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) specifica una categoria pin. per un grafico di anteprima, usare l' **\_ \_ anteprima della categoria pin**.</span><span class="sxs-lookup"><span data-stu-id="d0e0f-108">The first parameter to the [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method specifies a pin category; for a preview graph, use **PIN\_CATEGORY\_PREVIEW**.</span></span> <span data-ttu-id="d0e0f-109">Il secondo parametro specifica un tipo di supporto, come un GUID di tipo principale.</span><span class="sxs-lookup"><span data-stu-id="d0e0f-109">The second parameter specifies a media type, as a major type GUID.</span></span> <span data-ttu-id="d0e0f-110">Per video, usare **il \_ video di MEDIATYPE**.</span><span class="sxs-lookup"><span data-stu-id="d0e0f-110">For video, use **MEDIATYPE\_Video**.</span></span> <span data-ttu-id="d0e0f-111">I dispositivi DV forniscono audio e video con interfoliazione, per i quali il tipo di supporto è **\_ Interleaved MEDIATYPE**.</span><span class="sxs-lookup"><span data-stu-id="d0e0f-111">DV devices deliver interleaved audio and video, for which the media type is **MEDIATYPE\_Interleaved**.</span></span> <span data-ttu-id="d0e0f-112">Per ulteriori informazioni sull'acquisizione DV, vedere la pagina relativa ai [video digitali in DirectShow](digital-video-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="d0e0f-112">(For more information about DV capture, see [Digital Video in DirectShow](digital-video-in-directshow.md).)</span></span>

<span data-ttu-id="d0e0f-113">Il terzo parametro è un puntatore all'interfaccia [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) del filtro di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="d0e0f-113">The third parameter is a pointer to the capture filter's [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface.</span></span> <span data-ttu-id="d0e0f-114">In questo esempio i due parametri successivi non sono necessari.</span><span class="sxs-lookup"><span data-stu-id="d0e0f-114">The next two parameters are not needed in this example.</span></span> <span data-ttu-id="d0e0f-115">Vengono usati per specificare filtri aggiuntivi che potrebbero essere necessari per eseguire il rendering del flusso.</span><span class="sxs-lookup"><span data-stu-id="d0e0f-115">They are used to specify additional filters that might be needed to render the stream.</span></span> <span data-ttu-id="d0e0f-116">Impostando l'ultimo parametro su **null** , il generatore del grafico di acquisizione seleziona un renderer predefinito per il flusso, in base al tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="d0e0f-116">Setting the last parameter to **NULL** causes the Capture Graph Builder to select a default renderer for the stream, based on the media type.</span></span> <span data-ttu-id="d0e0f-117">Per i video, il generatore di grafici di acquisizione usa sempre il filtro [renderer video](video-renderer-filter.md) come renderer predefinito.</span><span class="sxs-lookup"><span data-stu-id="d0e0f-117">For video, the Capture Graph Builder always uses the [Video Renderer](video-renderer-filter.md) filter as the default renderer.</span></span>

> [!Note]  
> <span data-ttu-id="d0e0f-118">In Windows XP e versioni successive, anche se il renderer video mixing (VMR) è il renderer video predefinito per i metodi [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) , non è il renderer predefinito per il metodo [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) .</span><span class="sxs-lookup"><span data-stu-id="d0e0f-118">In Windows XP and later, although the Video Mixing Renderer (VMR) is the default video renderer for [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) methods, it is not the default renderer for the [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method.</span></span> <span data-ttu-id="d0e0f-119">In qualsiasi piattaforma, il generatore di grafici di acquisizione usa sempre il vecchio filtro renderer video, a meno che non venga specificato diversamente.</span><span class="sxs-lookup"><span data-stu-id="d0e0f-119">On any platform, the Capture Graph Builder always uses the old Video Renderer filter unless you specify otherwise.</span></span>

 

<span data-ttu-id="d0e0f-120">Sebbene la categoria PIN venga fornita come **\_ \_ anteprima della categoria pin**, non è importante se il filtro ha effettivamente un pin di anteprima, ma potrebbe avere un PIN della porta video o semplicemente un pin di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="d0e0f-120">Although the pin category is given as **PIN\_CATEGORY\_PREVIEW**, it does not matter whether the filter actually has a preview pin; it could have a video port pin or just a capture pin.</span></span> <span data-ttu-id="d0e0f-121">In entrambi i casi, il generatore di grafici di acquisizione compila automaticamente il grafo corretto.</span><span class="sxs-lookup"><span data-stu-id="d0e0f-121">In either case, the Capture Graph Builder automatically builds the correct graph.</span></span>

<span data-ttu-id="d0e0f-122">Il diagramma seguente mostra il grafico più semplice possibile per la visualizzazione in anteprima dei video.</span><span class="sxs-lookup"><span data-stu-id="d0e0f-122">The following diagram shows the simplest possible graph for previewing video.</span></span>

![grafico di anteprima video](images/vidcap01.png)

<span data-ttu-id="d0e0f-124">In questo diagramma, il filtro di acquisizione include un pin di anteprima, che si connette direttamente al renderer video.</span><span class="sxs-lookup"><span data-stu-id="d0e0f-124">In this diagram, the capture filter has a preview pin, which connects directly to the video renderer.</span></span>

<span data-ttu-id="d0e0f-125">Se il filtro di acquisizione include solo un pin di acquisizione, il generatore del grafico di acquisizione inserisce un filtro di [Smart Tee](smart-tee-filter.md) , che suddivide il flusso in un flusso di acquisizione e in un flusso di anteprima.</span><span class="sxs-lookup"><span data-stu-id="d0e0f-125">If the capture filter has only a capture pin, the Capture Graph Builder inserts a [Smart Tee](smart-tee-filter.md) filter, which splits the stream into a capture stream and a preview stream.</span></span> <span data-ttu-id="d0e0f-126">Questa operazione viene descritta in modo più dettagliato nella [combinazione di acquisizione video e anteprima](combining-video-capture-and-preview.md).</span><span class="sxs-lookup"><span data-stu-id="d0e0f-126">This is described in more detail in [Combining Video Capture and Preview](combining-video-capture-and-preview.md).</span></span>

<span data-ttu-id="d0e0f-127">In alcuni casi, il flusso video deve passare attraverso il filtro del mixer sovrapposto.</span><span class="sxs-lookup"><span data-stu-id="d0e0f-127">In some cases, the video stream must go through the Overlay Mixer filter.</span></span> <span data-ttu-id="d0e0f-128">In tal caso, il metodo [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) lo aggiunge automaticamente al grafico.</span><span class="sxs-lookup"><span data-stu-id="d0e0f-128">If so, the [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method adds it to the graph automatically.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d0e0f-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d0e0f-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d0e0f-130">Combinazione di acquisizione video e anteprima</span><span class="sxs-lookup"><span data-stu-id="d0e0f-130">Combining Video Capture and Preview</span></span>](combining-video-capture-and-preview.md)
</dt> <dt>

[<span data-ttu-id="d0e0f-131">Acquisizione video</span><span class="sxs-lookup"><span data-stu-id="d0e0f-131">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 



