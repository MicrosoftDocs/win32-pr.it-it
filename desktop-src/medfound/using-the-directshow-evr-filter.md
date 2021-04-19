---
description: Uso del filtro EVR DirectShow
ms.assetid: 4d85aed0-4b11-4c5f-bfc0-cad0a7d2f490
title: Uso del filtro EVR DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02568a5ea9cbaa0310409a5a0966a2bea1bbfffe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310173"
---
# <a name="using-the-directshow-evr-filter"></a><span data-ttu-id="332ba-103">Uso del filtro EVR DirectShow</span><span class="sxs-lookup"><span data-stu-id="332ba-103">Using the DirectShow EVR Filter</span></span>

<span data-ttu-id="332ba-104">Per creare il filtro EVR (Enhanced video renderer), chiamare **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="332ba-104">To create the enhanced video renderer (EVR) filter, call **CoCreateInstance**.</span></span> <span data-ttu-id="332ba-105">Il CLSID è CLSID \_ EnhancedVideoRenderer, definito in UUIDs. h.</span><span class="sxs-lookup"><span data-stu-id="332ba-105">The CLSID is CLSID\_EnhancedVideoRenderer, defined in uuids.h.</span></span> <span data-ttu-id="332ba-106">Non è necessario chiamare [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) o [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) per usare il filtro EVR.</span><span class="sxs-lookup"><span data-stu-id="332ba-106">You do not have to call [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) or [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) to use the EVR filter.</span></span>

<span data-ttu-id="332ba-107">Per altre informazioni sull'uso del filtro EVR in un'applicazione DirectShow, vedere [riproduzione audio/video in DirectShow](../directshow/audio-video-playback-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="332ba-107">For more information about using the EVR filter in a DirectShow application, see [Audio/Video Playback in DirectShow](../directshow/audio-video-playback-in-directshow.md).</span></span>

<span data-ttu-id="332ba-108">Il filtro EVR inizia con un pin di input, che corrisponde al flusso di riferimento.</span><span class="sxs-lookup"><span data-stu-id="332ba-108">The EVR filter starts with one input pin, which corresponds to the reference stream.</span></span> <span data-ttu-id="332ba-109">Per aggiungere PIN per i sottoflussi, eseguire una query sul filtro per l'interfaccia [**IEVRFilterConfig**](/windows/desktop/api/evr/nn-evr-ievrfilterconfig) e chiamare [**IEVRFilterConfig:: SetNumberOfStreams**](/windows/desktop/api/evr/nf-evr-ievrfilterconfig-setnumberofstreams).</span><span class="sxs-lookup"><span data-stu-id="332ba-109">To add pins for substreams, query the filter for the [**IEVRFilterConfig**](/windows/desktop/api/evr/nn-evr-ievrfilterconfig) interface and call [**IEVRFilterConfig::SetNumberOfStreams**](/windows/desktop/api/evr/nf-evr-ievrfilterconfig-setnumberofstreams).</span></span> <span data-ttu-id="332ba-110">Chiamare questo metodo prima di connettere i pin di input.</span><span class="sxs-lookup"><span data-stu-id="332ba-110">Call this method before connecting any input pins.</span></span> <span data-ttu-id="332ba-111">Il pin 0 è sempre il flusso di riferimento.</span><span class="sxs-lookup"><span data-stu-id="332ba-111">Pin 0 is always the reference stream.</span></span> <span data-ttu-id="332ba-112">Connettere questo pin prima di qualsiasi altro pin, perché il formato del flusso di riferimento potrebbe limitare i formati dei sottoflussi disponibili.</span><span class="sxs-lookup"><span data-stu-id="332ba-112">Connect this pin before any other pins, because the format of the reference stream might limit which substream formats are available.</span></span>

<span data-ttu-id="332ba-113">Prima di avviare il grafo, impostare la finestra ritaglio video e il rettangolo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="332ba-113">Before starting the graph, set the video clipping window and the destination rectangle.</span></span> <span data-ttu-id="332ba-114">Per altre informazioni, vedere [uso dei controlli video display](using-the-video-display-controls.md).</span><span class="sxs-lookup"><span data-stu-id="332ba-114">For more information, see [Using the Video Display Controls](using-the-video-display-controls.md).</span></span>

<span data-ttu-id="332ba-115">A differenza del renderer video mixing (VMR), EVR non dispone di modalità operative (finestra, senza finestra e così via).</span><span class="sxs-lookup"><span data-stu-id="332ba-115">Unlike the Video Mixing Renderer (VMR), the EVR does not have operational modes (windowed, windowless, and so forth).</span></span> <span data-ttu-id="332ba-116">In particolare:</span><span class="sxs-lookup"><span data-stu-id="332ba-116">In particular:</span></span>

-   <span data-ttu-id="332ba-117">EVR non supporta la modalità finestra.</span><span class="sxs-lookup"><span data-stu-id="332ba-117">The EVR does not support windowed mode.</span></span> <span data-ttu-id="332ba-118">L'applicazione deve fornire la finestra di ridimensionamento.</span><span class="sxs-lookup"><span data-stu-id="332ba-118">The application must provide the clipping window.</span></span>
-   <span data-ttu-id="332ba-119">Il EVR non dispone di una modalità di rendering.</span><span class="sxs-lookup"><span data-stu-id="332ba-119">The EVR does not have a renderless mode.</span></span> <span data-ttu-id="332ba-120">Per sostituire il Presenter predefinito, chiamare [**IMFVideoRenderer:: InitializeRenderer**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer).</span><span class="sxs-lookup"><span data-stu-id="332ba-120">To replace the default presenter, call [**IMFVideoRenderer::InitializeRenderer**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer).</span></span>
-   <span data-ttu-id="332ba-121">Il EVR non dispone di una modalità di combinazione.</span><span class="sxs-lookup"><span data-stu-id="332ba-121">The EVR does not have a mixing mode.</span></span> <span data-ttu-id="332ba-122">Il EVR crea sempre il mixer.</span><span class="sxs-lookup"><span data-stu-id="332ba-122">The EVR always creates the mixer.</span></span> <span data-ttu-id="332ba-123">Se si dispone di un flusso di input, non è necessario chiamare [**SetNumberOfStreams**](/windows/desktop/api/evr/nf-evr-ievrfilterconfig-setnumberofstreams) per forzare il EVR a usare il mixer.</span><span class="sxs-lookup"><span data-stu-id="332ba-123">If you have one input stream, it is not necessary to call [**SetNumberOfStreams**](/windows/desktop/api/evr/nf-evr-ievrfilterconfig-setnumberofstreams) to force the EVR to use the mixer.</span></span>

## <a name="filter-interfaces"></a><span data-ttu-id="332ba-124">Interfacce di filtro</span><span class="sxs-lookup"><span data-stu-id="332ba-124">Filter Interfaces</span></span>

<span data-ttu-id="332ba-125">Il filtro EVR espone le interfacce seguenti.</span><span class="sxs-lookup"><span data-stu-id="332ba-125">The EVR filter exposes the following interfaces.</span></span> <span data-ttu-id="332ba-126">Alcune di queste interfacce sono documentate in DirectShow SDK.</span><span class="sxs-lookup"><span data-stu-id="332ba-126">Some of these interfaces are documented in the DirectShow SDK.</span></span> <span data-ttu-id="332ba-127">Usare **QueryInterface** per recuperare i puntatori a queste interfacce:</span><span class="sxs-lookup"><span data-stu-id="332ba-127">Use **QueryInterface** to retrieve pointers to these interfaces:</span></span>

-   <span data-ttu-id="332ba-128">[**IAMCertifiedOutputProtection**](/windows/win32/api/strmif/nn-strmif-iamcertifiedoutputprotection) (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="332ba-128">[**IAMCertifiedOutputProtection**](/windows/win32/api/strmif/nn-strmif-iamcertifiedoutputprotection) (DirectShow)</span></span>
-   <span data-ttu-id="332ba-129">[**IAMFilterMiscFlags**](/windows/win32/api/strmif/nn-strmif-iamfiltermiscflags) (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="332ba-129">[**IAMFilterMiscFlags**](/windows/win32/api/strmif/nn-strmif-iamfiltermiscflags) (DirectShow)</span></span>
-   <span data-ttu-id="332ba-130">[**IBaseFilter**](/windows/win32/api/strmif/nn-strmif-ibasefilter) (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="332ba-130">[**IBaseFilter**](/windows/win32/api/strmif/nn-strmif-ibasefilter) (DirectShow)</span></span>
-   [<span data-ttu-id="332ba-131">**IEVRFilterConfig**</span><span class="sxs-lookup"><span data-stu-id="332ba-131">**IEVRFilterConfig**</span></span>](/windows/desktop/api/evr/nn-evr-ievrfilterconfig)
-   <span data-ttu-id="332ba-132">[**IKsPropertySet**](../directshow/ikspropertyset.md) (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="332ba-132">[**IKsPropertySet**](../directshow/ikspropertyset.md) (DirectShow)</span></span>
-   <span data-ttu-id="332ba-133">[**IMediaEventSink**](/windows/win32/api/strmif/nn-strmif-imediaeventsink) (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="332ba-133">[**IMediaEventSink**](/windows/win32/api/strmif/nn-strmif-imediaeventsink) (DirectShow)</span></span>
-   [<span data-ttu-id="332ba-134">**IMFGetService**</span><span class="sxs-lookup"><span data-stu-id="332ba-134">**IMFGetService**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [<span data-ttu-id="332ba-135">**IMFVideoPositionMapper**</span><span class="sxs-lookup"><span data-stu-id="332ba-135">**IMFVideoPositionMapper**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper)
-   [<span data-ttu-id="332ba-136">**IMFVideoRenderer**</span><span class="sxs-lookup"><span data-stu-id="332ba-136">**IMFVideoRenderer**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideorenderer)
-   <span data-ttu-id="332ba-137">**IPersistStream**</span><span class="sxs-lookup"><span data-stu-id="332ba-137">**IPersistStream**</span></span>
-   <span data-ttu-id="332ba-138">[**IQualityControl**](/windows/win32/api/strmif/nn-strmif-iqualitycontrol) (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="332ba-138">[**IQualityControl**](/windows/win32/api/strmif/nn-strmif-iqualitycontrol) (DirectShow)</span></span>
-   <span data-ttu-id="332ba-139">[**IQualProp**](/previous-versions/windows/desktop/api/amvideo/nn-amvideo-iqualprop) (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="332ba-139">[**IQualProp**](/previous-versions/windows/desktop/api/amvideo/nn-amvideo-iqualprop) (DirectShow)</span></span>
-   <span data-ttu-id="332ba-140">**ISpecifyPropertyPages**</span><span class="sxs-lookup"><span data-stu-id="332ba-140">**ISpecifyPropertyPages**</span></span>

## <a name="input-pin-interfaces"></a><span data-ttu-id="332ba-141">Interfacce pin di input</span><span class="sxs-lookup"><span data-stu-id="332ba-141">Input Pin Interfaces</span></span>

<span data-ttu-id="332ba-142">I pin di input nel filtro EVR espongono le interfacce seguenti.</span><span class="sxs-lookup"><span data-stu-id="332ba-142">The input pins on the EVR filter expose the following interfaces.</span></span> <span data-ttu-id="332ba-143">Usare **QueryInterface** per recuperare i puntatori a queste interfacce:</span><span class="sxs-lookup"><span data-stu-id="332ba-143">Use **QueryInterface** to retrieve pointers to these interfaces:</span></span>

-   [<span data-ttu-id="332ba-144">**IEVRVideoStreamControl**</span><span class="sxs-lookup"><span data-stu-id="332ba-144">**IEVRVideoStreamControl**</span></span>](/windows/desktop/api/evr9/nn-evr9-ievrvideostreamcontrol)
-   <span data-ttu-id="332ba-145">[**IMemInputPin**](/windows/win32/api/strmif/nn-strmif-imeminputpin) (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="332ba-145">[**IMemInputPin**](/windows/win32/api/strmif/nn-strmif-imeminputpin) (DirectShow)</span></span>
-   [<span data-ttu-id="332ba-146">**IMFGetService**</span><span class="sxs-lookup"><span data-stu-id="332ba-146">**IMFGetService**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   <span data-ttu-id="332ba-147">[**Ipin**](/windows/win32/api/strmif/nn-strmif-ipin) (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="332ba-147">[**IPin**](/windows/win32/api/strmif/nn-strmif-ipin) (DirectShow)</span></span>
-   <span data-ttu-id="332ba-148">[**IQualityControl**](/windows/win32/api/strmif/nn-strmif-iqualitycontrol) (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="332ba-148">[**IQualityControl**](/windows/win32/api/strmif/nn-strmif-iqualitycontrol) (DirectShow)</span></span>

<span data-ttu-id="332ba-149">Inoltre, è possibile utilizzare l'interfaccia [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) per recuperare l'interfaccia seguente:</span><span class="sxs-lookup"><span data-stu-id="332ba-149">In addition, you can use the [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) interface to retrieve the following interface:</span></span>

-   [<span data-ttu-id="332ba-150">**IDirectXVideoMemoryConfiguration**</span><span class="sxs-lookup"><span data-stu-id="332ba-150">**IDirectXVideoMemoryConfiguration**</span></span>](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration)

## <a name="related-topics"></a><span data-ttu-id="332ba-151">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="332ba-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="332ba-152">Riproduzione audio/video in DirectShow</span><span class="sxs-lookup"><span data-stu-id="332ba-152">Audio/Video Playback in DirectShow</span></span>](../directshow/audio-video-playback-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="332ba-153">Renderer video migliorato</span><span class="sxs-lookup"><span data-stu-id="332ba-153">Enhanced Video Renderer</span></span>](enhanced-video-renderer.md)
</dt> </dl>

 

 
