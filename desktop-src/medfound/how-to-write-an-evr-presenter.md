---
description: Questo articolo descrive come scrivere un presentatore personalizzato per il renderer video avanzato (EVR).
ms.assetid: 1135b309-b158-4b70-9f76-5c93d0ad3250
title: Come scrivere un presentatore EVR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 505ba7ec225ac5f1316ad4343a4e1058ff0b6cb8
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118776"
---
# <a name="how-to-write-an-evr-presenter"></a><span data-ttu-id="f833a-103">Come scrivere un presentatore EVR</span><span class="sxs-lookup"><span data-stu-id="f833a-103">How to Write an EVR Presenter</span></span>

<span data-ttu-id="f833a-104">Questo articolo descrive come scrivere un presentatore personalizzato per il renderer video avanzato (EVR).</span><span class="sxs-lookup"><span data-stu-id="f833a-104">This article describes how to write a custom presenter for the enhanced video renderer (EVR).</span></span> <span data-ttu-id="f833a-105">Un presentatore personalizzato può essere usato con DirectShow e Media Foundation; Le interfacce e il modello a oggetti sono gli stessi per entrambe le tecnologie, anche se la sequenza esatta delle operazioni può variare.</span><span class="sxs-lookup"><span data-stu-id="f833a-105">A custom presenter can be used with both DirectShow and Media Foundation; the interfaces and object model are the same for both technologies, although the exact sequence of operations might vary.</span></span>

<span data-ttu-id="f833a-106">Il codice di esempio in questo argomento è adattato [dall'esempio EVRPresenter](evrpresenter-sample.md), fornito nel Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="f833a-106">The example code in this topic is adapted from the [EVRPresenter Sample](evrpresenter-sample.md), which is provided in the Windows SDK.</span></span>

<span data-ttu-id="f833a-107">In questo argomento sono incluse le sezioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="f833a-107">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="f833a-108">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="f833a-108">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="f833a-109">Modello a oggetti del presentatore</span><span class="sxs-lookup"><span data-stu-id="f833a-109">Presenter Object Model</span></span>](#presenter-object-model)
    -   [<span data-ttu-id="f833a-110">Flusso di dati inside the EVR</span><span class="sxs-lookup"><span data-stu-id="f833a-110">Data Flow Inside the EVR</span></span>](#data-flow-inside-the-evr)
    -   [<span data-ttu-id="f833a-111">Stati del presentatore</span><span class="sxs-lookup"><span data-stu-id="f833a-111">Presenter States</span></span>](#presenter-states)
    -   [<span data-ttu-id="f833a-112">Interfacce del presentatore</span><span class="sxs-lookup"><span data-stu-id="f833a-112">Presenter Interfaces</span></span>](#presenter-interfaces)
    -   [<span data-ttu-id="f833a-113">Implementazione di IMFVideoDeviceID</span><span class="sxs-lookup"><span data-stu-id="f833a-113">Implementing IMFVideoDeviceID</span></span>](#implementing-imfvideodeviceid)
    -   [<span data-ttu-id="f833a-114">Implementazione di IMFTopologyServiceLookupClient</span><span class="sxs-lookup"><span data-stu-id="f833a-114">Implementing IMFTopologyServiceLookupClient</span></span>](#implementing-imftopologyservicelookupclient)
    -   [<span data-ttu-id="f833a-115">Implementazione di IMFVideoPresenter</span><span class="sxs-lookup"><span data-stu-id="f833a-115">Implementing IMFVideoPresenter</span></span>](#implementing-imfvideopresenter)
    -   [<span data-ttu-id="f833a-116">Implementazione di IMFClockStateSink</span><span class="sxs-lookup"><span data-stu-id="f833a-116">Implementing IMFClockStateSink</span></span>](#implementing-imfclockstatesink)
    -   [<span data-ttu-id="f833a-117">Implementazione di IMFRateSupport</span><span class="sxs-lookup"><span data-stu-id="f833a-117">Implementing IMFRateSupport</span></span>](#implementing-imfratesupport)
    -   [<span data-ttu-id="f833a-118">Invio di eventi all'EVR</span><span class="sxs-lookup"><span data-stu-id="f833a-118">Sending Events to the EVR</span></span>](#sending-events-to-the-evr)
-   [<span data-ttu-id="f833a-119">Formati di negoziazione</span><span class="sxs-lookup"><span data-stu-id="f833a-119">Negotiating Formats</span></span>](#negotiating-formats)
-   [<span data-ttu-id="f833a-120">Gestione del dispositivo Direct3D</span><span class="sxs-lookup"><span data-stu-id="f833a-120">Managing the Direct3D Device</span></span>](#managing-the-direct3d-device)
    -   [<span data-ttu-id="f833a-121">Allocazione di superfici Direct3D</span><span class="sxs-lookup"><span data-stu-id="f833a-121">Allocating Direct3D Surfaces</span></span>](#allocating-direct3d-surfaces)
    -   [<span data-ttu-id="f833a-122">Esempi di rilevamento</span><span class="sxs-lookup"><span data-stu-id="f833a-122">Tracking Samples</span></span>](#tracking-samples)
-   [<span data-ttu-id="f833a-123">Elaborazione dell'output</span><span class="sxs-lookup"><span data-stu-id="f833a-123">Processing Output</span></span>](#processing-output)
    -   [<span data-ttu-id="f833a-124">Ridisegno di frame</span><span class="sxs-lookup"><span data-stu-id="f833a-124">Repainting Frames</span></span>](#repainting-frames)
    -   [<span data-ttu-id="f833a-125">Esempi di pianificazione</span><span class="sxs-lookup"><span data-stu-id="f833a-125">Scheduling Samples</span></span>](#scheduling-samples)
    -   [<span data-ttu-id="f833a-126">Presentazione di esempi</span><span class="sxs-lookup"><span data-stu-id="f833a-126">Presenting Samples</span></span>](#presenting-samples)
    -   [<span data-ttu-id="f833a-127">Rettangoli di origine e destinazione</span><span class="sxs-lookup"><span data-stu-id="f833a-127">Source and Destination Rectangles</span></span>](#source-and-destination-rectangles)
    -   [<span data-ttu-id="f833a-128">Fine del flusso</span><span class="sxs-lookup"><span data-stu-id="f833a-128">End of Stream</span></span>](#end-of-stream)
-   [<span data-ttu-id="f833a-129">Esecuzione istruzione/istruzione dei frame</span><span class="sxs-lookup"><span data-stu-id="f833a-129">Frame Stepping</span></span>](#frame-stepping)
    -   [<span data-ttu-id="f833a-130">Implementazione dell'esecuzione di istruzioni dei frame</span><span class="sxs-lookup"><span data-stu-id="f833a-130">Implementing Frame Stepping</span></span>](#implementing-frame-stepping)
-   [<span data-ttu-id="f833a-131">Impostazione del presentatore nell'EVR</span><span class="sxs-lookup"><span data-stu-id="f833a-131">Setting the Presenter on the EVR</span></span>](#setting-the-presenter-on-the-evr)
    -   [<span data-ttu-id="f833a-132">Impostazione del presentatore in DirectShow</span><span class="sxs-lookup"><span data-stu-id="f833a-132">Setting the Presenter in DirectShow</span></span>](#setting-the-presenter-in-directshow)
    -   [<span data-ttu-id="f833a-133">Impostazione del presenter in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f833a-133">Setting the Presenter in Media Foundation</span></span>](#setting-the-presenter-in-media-foundation)
-   [<span data-ttu-id="f833a-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f833a-134">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="f833a-135">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="f833a-135">Prerequisites</span></span>

<span data-ttu-id="f833a-136">Prima di scrivere un presentatore personalizzato, è necessario avere familiarità con le tecnologie seguenti:</span><span class="sxs-lookup"><span data-stu-id="f833a-136">Before writing a custom presenter, you should be familiar with the following technologies:</span></span>

-   <span data-ttu-id="f833a-137">Renderer video avanzato.</span><span class="sxs-lookup"><span data-stu-id="f833a-137">The enhanced video renderer.</span></span> <span data-ttu-id="f833a-138">Vedere [Renderer video avanzato.](enhanced-video-renderer.md)</span><span class="sxs-lookup"><span data-stu-id="f833a-138">See [Enhanced Video Renderer](enhanced-video-renderer.md).</span></span>
-   <span data-ttu-id="f833a-139">Grafica Direct3D.</span><span class="sxs-lookup"><span data-stu-id="f833a-139">Direct3D graphics.</span></span> <span data-ttu-id="f833a-140">Non è necessario comprendere la grafica 3D per scrivere un presentatore, ma è necessario sapere come creare un dispositivo Direct3D e gestire le superfici Direct3D.</span><span class="sxs-lookup"><span data-stu-id="f833a-140">You don't need to understand 3-D graphics to write a presenter, but you must know how to create a Direct3D device and manage Direct3D surfaces.</span></span> <span data-ttu-id="f833a-141">Se non si ha familiarità con Direct3D, leggere le sezioni "Dispositivi Direct3D" e "Risorse Direct3D" nella documentazione di DirectX Graphics SDK.</span><span class="sxs-lookup"><span data-stu-id="f833a-141">If you aren't familiar with Direct3D, read the sections "Direct3D Devices" and "Direct3D Resources" in the DirectX Graphics SDK documentation.</span></span>
-   <span data-ttu-id="f833a-142">DirectShow filter graphs or the Media Foundation pipeline,depending on which technology your application will use to render video.</span><span class="sxs-lookup"><span data-stu-id="f833a-142">DirectShow filter graphs or the Media Foundation pipeline, depending on which technology your application will use to render video.</span></span>
-   <span data-ttu-id="f833a-143">[Media Foundation trasforma](media-foundation-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="f833a-143">[Media Foundation Transforms](media-foundation-transforms.md).</span></span> <span data-ttu-id="f833a-144">Il mixer EVR è una Media Foundation e il presentatore chiama i metodi direttamente sul mixer.</span><span class="sxs-lookup"><span data-stu-id="f833a-144">The EVR mixer is a Media Foundation transform, and the presenter calls methods directly on the mixer.</span></span>
-   <span data-ttu-id="f833a-145">Implementazione di oggetti COM.</span><span class="sxs-lookup"><span data-stu-id="f833a-145">Implementing COM objects.</span></span> <span data-ttu-id="f833a-146">Il presentatore è un oggetto COM in-process a thread libero.</span><span class="sxs-lookup"><span data-stu-id="f833a-146">The presenter is an in-process, free-threaded COM object.</span></span>

## <a name="presenter-object-model"></a><span data-ttu-id="f833a-147">Modello a oggetti del presentatore</span><span class="sxs-lookup"><span data-stu-id="f833a-147">Presenter Object Model</span></span>

<span data-ttu-id="f833a-148">Questa sezione contiene una panoramica del modello a oggetti del presentatore e delle interfacce.</span><span class="sxs-lookup"><span data-stu-id="f833a-148">This section contains an overview the presenter object model and interfaces.</span></span>

### <a name="data-flow-inside-the-evr"></a><span data-ttu-id="f833a-149">Flusso di dati inside the EVR</span><span class="sxs-lookup"><span data-stu-id="f833a-149">Data Flow Inside the EVR</span></span>

<span data-ttu-id="f833a-150">EVR usa due componenti plug-in per eseguire il rendering del video: il *mixer* e il *presentatore*.</span><span class="sxs-lookup"><span data-stu-id="f833a-150">The EVR uses two plug-in components to render video: the *mixer* and the *presenter*.</span></span> <span data-ttu-id="f833a-151">Il mixer unisce i flussi video e, se necessario, ne deinterlaccia il video.</span><span class="sxs-lookup"><span data-stu-id="f833a-151">The mixer blends the video streams and deinterlaces the video if needed.</span></span> <span data-ttu-id="f833a-152">Il presentatore disegna (o *presenta)* il video sullo schermo e pianifica quando viene disegnato ogni fotogramma.</span><span class="sxs-lookup"><span data-stu-id="f833a-152">The presenter draws (or *presents*) the video onto the display and schedules when each frame is drawn.</span></span> <span data-ttu-id="f833a-153">Le applicazioni possono sostituire uno di questi oggetti con un'implementazione personalizzata.</span><span class="sxs-lookup"><span data-stu-id="f833a-153">Applications can replace either of these objects with a custom implementation.</span></span>

<span data-ttu-id="f833a-154">L'EVR ha uno o più flussi di input e il mixer ha un numero corrispondente di flussi di input.</span><span class="sxs-lookup"><span data-stu-id="f833a-154">The EVR has one or more input streams, and the mixer has a corresponding number of input streams.</span></span> <span data-ttu-id="f833a-155">Il flusso 0 è sempre il *flusso di riferimento*.</span><span class="sxs-lookup"><span data-stu-id="f833a-155">Stream 0 is always the *reference stream*.</span></span> <span data-ttu-id="f833a-156">Gli altri flussi sono *flussi secondari,* che il mixer si combina con alfa nel flusso di riferimento.</span><span class="sxs-lookup"><span data-stu-id="f833a-156">The other streams are *substreams*, which the mixer alpha-blends onto the reference stream.</span></span> <span data-ttu-id="f833a-157">Il flusso di riferimento determina la frequenza dei fotogrammi master per il video composito.</span><span class="sxs-lookup"><span data-stu-id="f833a-157">The reference stream determines the master frame-rate for the composited video.</span></span> <span data-ttu-id="f833a-158">Per ogni fotogramma di riferimento, il mixer accetta il frame più recente da ogni flusso secondario, li combina con alfa nel frame di riferimento e restituisce un singolo frame composito.</span><span class="sxs-lookup"><span data-stu-id="f833a-158">For each reference frame, the mixer takes the most recent frame from each substream, alpha-blends them onto the reference frame, and outputs a single composited frame.</span></span> <span data-ttu-id="f833a-159">Il mixer esegue anche la deinterlacing e la conversione dei colori da YUV a RGB, se necessario.</span><span class="sxs-lookup"><span data-stu-id="f833a-159">The mixer also performs deinterlacing and color conversion from YUV to RGB if needed.</span></span> <span data-ttu-id="f833a-160">L'EVR inserisce sempre il mixer nella pipeline video, indipendentemente dal numero di flussi di input o dal formato video.</span><span class="sxs-lookup"><span data-stu-id="f833a-160">The EVR always inserts the mixer into the video pipeline, regardless of the number of input streams or the video format.</span></span> <span data-ttu-id="f833a-161">L'immagine seguente illustra questo processo.</span><span class="sxs-lookup"><span data-stu-id="f833a-161">The following image illustrates this process.</span></span>

![diagramma che mostra il flusso di riferimento e il flusso secondario che puntano al mixer, che punta al presentatore, che punta alla visualizzazione](images/459338c4-cff8-4d20-bffd-ff1cbbe6f332.gif)

<span data-ttu-id="f833a-163">Il presentatore esegue le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="f833a-163">The presenter performs the following tasks:</span></span>

-   <span data-ttu-id="f833a-164">Imposta il formato di output sul mixer.</span><span class="sxs-lookup"><span data-stu-id="f833a-164">Sets the output format on the mixer.</span></span> <span data-ttu-id="f833a-165">Prima dell'inizio dello streaming, il presentatore imposta un tipo di contenuto multimediale nel flusso di output del mixer.</span><span class="sxs-lookup"><span data-stu-id="f833a-165">Before streaming begins, the presenter sets a media type on the mixer's output stream.</span></span> <span data-ttu-id="f833a-166">Questo tipo di supporto definisce il formato dell'immagine composita.</span><span class="sxs-lookup"><span data-stu-id="f833a-166">This media type defines the format of the composited image.</span></span>
-   <span data-ttu-id="f833a-167">Crea il dispositivo Direct3D.</span><span class="sxs-lookup"><span data-stu-id="f833a-167">Creates the Direct3D device.</span></span>
-   <span data-ttu-id="f833a-168">Alloca le superfici Direct3D.</span><span class="sxs-lookup"><span data-stu-id="f833a-168">Allocates Direct3D surfaces.</span></span> <span data-ttu-id="f833a-169">Il mixer blitta i fotogrammi compositi su queste superfici.</span><span class="sxs-lookup"><span data-stu-id="f833a-169">The mixer blits the composited frames onto these surfaces.</span></span>
-   <span data-ttu-id="f833a-170">Ottiene l'output dal mixer.</span><span class="sxs-lookup"><span data-stu-id="f833a-170">Gets the output from the mixer.</span></span>
-   <span data-ttu-id="f833a-171">Pianifica la presentazione dei fotogrammi.</span><span class="sxs-lookup"><span data-stu-id="f833a-171">Schedules when the frames are presented.</span></span> <span data-ttu-id="f833a-172">L'EVR fornisce l'orologio di presentazione e il presentatore pianifica i fotogrammi in base a questo orologio.</span><span class="sxs-lookup"><span data-stu-id="f833a-172">The EVR provides the presentation clock, and the presenter schedules frames according to this clock.</span></span>
-   <span data-ttu-id="f833a-173">Presenta ogni frame usando Direct3D.</span><span class="sxs-lookup"><span data-stu-id="f833a-173">Presents each frame using Direct3D.</span></span>
-   <span data-ttu-id="f833a-174">Esegue l'esecuzione e lo scrubbing dei fotogrammi.</span><span class="sxs-lookup"><span data-stu-id="f833a-174">Performs frame stepping and scrubbing.</span></span>

### <a name="presenter-states"></a><span data-ttu-id="f833a-175">Stati del presentatore</span><span class="sxs-lookup"><span data-stu-id="f833a-175">Presenter States</span></span>

<span data-ttu-id="f833a-176">In qualsiasi momento, il presentatore si trova in uno degli stati seguenti:</span><span class="sxs-lookup"><span data-stu-id="f833a-176">At any time, the presenter is in one of following states:</span></span>

-   <span data-ttu-id="f833a-177">*Avviato*.</span><span class="sxs-lookup"><span data-stu-id="f833a-177">*Started*.</span></span> <span data-ttu-id="f833a-178">L'orologio di presentazione dell'EVR è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="f833a-178">The EVR's presentation clock is running.</span></span> <span data-ttu-id="f833a-179">Il presentatore pianifica i fotogrammi video per la presentazione non appena arrivano.</span><span class="sxs-lookup"><span data-stu-id="f833a-179">The presenter schedules video frames for presentation as they arrive.</span></span>
-   <span data-ttu-id="f833a-180">*In pausa.*</span><span class="sxs-lookup"><span data-stu-id="f833a-180">*Paused*.</span></span> <span data-ttu-id="f833a-181">L'orologio di presentazione è sospeso.</span><span class="sxs-lookup"><span data-stu-id="f833a-181">The presentation clock is suspended.</span></span> <span data-ttu-id="f833a-182">Il presentatore non presenta nuovi esempi, ma mantiene la coda degli esempi pianificati.</span><span class="sxs-lookup"><span data-stu-id="f833a-182">The presenter does not present any new samples but maintains its queue of scheduled samples.</span></span> <span data-ttu-id="f833a-183">Se vengono ricevuti nuovi esempi, il presentatore li aggiunge alla coda.</span><span class="sxs-lookup"><span data-stu-id="f833a-183">If new samples are received, the presenter adds them to the queue.</span></span>
-   <span data-ttu-id="f833a-184">*Arrestato.*</span><span class="sxs-lookup"><span data-stu-id="f833a-184">*Stopped*.</span></span> <span data-ttu-id="f833a-185">L'orologio di presentazione viene arrestato.</span><span class="sxs-lookup"><span data-stu-id="f833a-185">The presentation clock is stopped.</span></span> <span data-ttu-id="f833a-186">Il presentatore rimuove tutti gli esempi pianificati.</span><span class="sxs-lookup"><span data-stu-id="f833a-186">The presenter discards any samples that were scheduled.</span></span>
-   <span data-ttu-id="f833a-187">*Arrestare*.</span><span class="sxs-lookup"><span data-stu-id="f833a-187">*Shut down*.</span></span> <span data-ttu-id="f833a-188">Il presentatore rilascia tutte le risorse correlate allo streaming, ad esempio le superfici Direct3D.</span><span class="sxs-lookup"><span data-stu-id="f833a-188">The presenter releases any resources related to streaming, such as Direct3D surfaces.</span></span> <span data-ttu-id="f833a-189">Si tratta dello stato iniziale del presentatore e dello stato finale prima dell'eliminazione definitiva del presentatore.</span><span class="sxs-lookup"><span data-stu-id="f833a-189">This is the presenter's initial state, and the final state before the presenter is destroyed.</span></span>

<span data-ttu-id="f833a-190">Nel codice di esempio in questo argomento lo stato del presentatore è rappresentato da un'enumerazione :</span><span class="sxs-lookup"><span data-stu-id="f833a-190">In the example code in this topic, the presenter state is represented by an enumeration:</span></span>


```C++
enum RENDER_STATE
{
    RENDER_STATE_STARTED = 1,
    RENDER_STATE_STOPPED,
    RENDER_STATE_PAUSED,
    RENDER_STATE_SHUTDOWN,  // Initial state.
};
```



<span data-ttu-id="f833a-191">Alcune operazioni non sono valide mentre il presentatore si trova nello stato di arresto.</span><span class="sxs-lookup"><span data-stu-id="f833a-191">Some operations are not valid while the presenter is in the shutdown state.</span></span> <span data-ttu-id="f833a-192">Il codice di esempio verifica questo stato chiamando un metodo helper:</span><span class="sxs-lookup"><span data-stu-id="f833a-192">The example code checks for this state by calling a helper method:</span></span>


```C++
    HRESULT CheckShutdown() const
    {
        if (m_RenderState == RENDER_STATE_SHUTDOWN)
        {
            return MF_E_SHUTDOWN;
        }
        else
        {
            return S_OK;
        }
    }
```



### <a name="presenter-interfaces"></a><span data-ttu-id="f833a-193">Interfacce del presentatore</span><span class="sxs-lookup"><span data-stu-id="f833a-193">Presenter Interfaces</span></span>

<span data-ttu-id="f833a-194">È necessario un presentatore per implementare le interfacce seguenti:</span><span class="sxs-lookup"><span data-stu-id="f833a-194">A presenter is required to implement the following interfaces:</span></span>



| <span data-ttu-id="f833a-195">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="f833a-195">Interface</span></span>                                                                | <span data-ttu-id="f833a-196">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f833a-196">Description</span></span>                                                                                                                                                         |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f833a-197">**IMFClockStateSink**</span><span class="sxs-lookup"><span data-stu-id="f833a-197">**IMFClockStateSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)                           | <span data-ttu-id="f833a-198">Notifica al presentatore quando l'orologio dell'EVR cambia stato.</span><span class="sxs-lookup"><span data-stu-id="f833a-198">Notifies the presenter when the EVR's clock changes state.</span></span> <span data-ttu-id="f833a-199">Vedere [Implementazione di IMFClockStateSink.](#implementing-imfclockstatesink)</span><span class="sxs-lookup"><span data-stu-id="f833a-199">See [Implementing IMFClockStateSink](#implementing-imfclockstatesink).</span></span>                                   |
| [<span data-ttu-id="f833a-200">**IMFGetService**</span><span class="sxs-lookup"><span data-stu-id="f833a-200">**IMFGetService**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)                                   | <span data-ttu-id="f833a-201">Consente all'applicazione e ad altri componenti nella pipeline di ottenere le interfacce dal presentatore.</span><span class="sxs-lookup"><span data-stu-id="f833a-201">Provides a way for the application and other components in the pipeline to get interfaces from the presenter.</span></span>                                                       |
| [<span data-ttu-id="f833a-202">**IMFTopologyServiceLookupClient**</span><span class="sxs-lookup"><span data-stu-id="f833a-202">**IMFTopologyServiceLookupClient**</span></span>](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient) | <span data-ttu-id="f833a-203">Consente al presentatore di ottenere le interfacce dall'EVR o dal mixer.</span><span class="sxs-lookup"><span data-stu-id="f833a-203">Enables the presenter to get interfaces from the EVR or the mixer.</span></span> <span data-ttu-id="f833a-204">Vedere [Implementazione di IMFTopologyServiceLookupClient.](#implementing-imftopologyservicelookupclient)</span><span class="sxs-lookup"><span data-stu-id="f833a-204">See [Implementing IMFTopologyServiceLookupClient](#implementing-imftopologyservicelookupclient).</span></span> |
| [<span data-ttu-id="f833a-205">**IMFVideoDeviceID**</span><span class="sxs-lookup"><span data-stu-id="f833a-205">**IMFVideoDeviceID**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)                             | <span data-ttu-id="f833a-206">Assicura che il presentatore e il mixer usino tecnologie compatibili.</span><span class="sxs-lookup"><span data-stu-id="f833a-206">Ensures that the presenter and the mixer use compatible technologies.</span></span> <span data-ttu-id="f833a-207">Vedere [Implementazione di IMFVideoDeviceID.](#implementing-imfvideodeviceid)</span><span class="sxs-lookup"><span data-stu-id="f833a-207">See [Implementing IMFVideoDeviceID](#implementing-imfvideodeviceid).</span></span>                          |
| [<span data-ttu-id="f833a-208">**IMFVideoPresenter**</span><span class="sxs-lookup"><span data-stu-id="f833a-208">**IMFVideoPresenter**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideopresenter)                           | <span data-ttu-id="f833a-209">Elabora i messaggi provenienti da EVR.</span><span class="sxs-lookup"><span data-stu-id="f833a-209">Processes messages from the EVR.</span></span> <span data-ttu-id="f833a-210">Vedere [Implementazione di IMFVideoPresenter.](#implementing-imfvideopresenter)</span><span class="sxs-lookup"><span data-stu-id="f833a-210">See [Implementing IMFVideoPresenter](#implementing-imfvideopresenter).</span></span>                                                             |



 

<span data-ttu-id="f833a-211">Le interfacce seguenti sono facoltative:</span><span class="sxs-lookup"><span data-stu-id="f833a-211">The following interfaces are optional:</span></span>



| <span data-ttu-id="f833a-212">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="f833a-212">Interface</span></span>                                                | <span data-ttu-id="f833a-213">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f833a-213">Description</span></span>                                                                                                                                                               |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f833a-214">**IEVRTrustedVideoPlugin**</span><span class="sxs-lookup"><span data-stu-id="f833a-214">**IEVRTrustedVideoPlugin**</span></span>](/windows/desktop/api/evr/nn-evr-ievrtrustedvideoplugin) | <span data-ttu-id="f833a-215">Consente al presentatore di usare supporti protetti.</span><span class="sxs-lookup"><span data-stu-id="f833a-215">Enables the presenter to work with protected media.</span></span> <span data-ttu-id="f833a-216">Implementare questa interfaccia se il presentatore è un componente attendibile progettato per funzionare nel percorso del supporto protetto (PMP).</span><span class="sxs-lookup"><span data-stu-id="f833a-216">Implement this interface if your presenter is a trusted component designed to work in the protected media path (PMP).</span></span> |
| [<span data-ttu-id="f833a-217">**IMFRateSupport**</span><span class="sxs-lookup"><span data-stu-id="f833a-217">**IMFRateSupport**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)                 | <span data-ttu-id="f833a-218">Segnala l'intervallo di velocità di riproduzione supportate dal presentatore.</span><span class="sxs-lookup"><span data-stu-id="f833a-218">Reports the range of playback rates that the presenter supports.</span></span> <span data-ttu-id="f833a-219">Vedere [Implementazione di IMFRateSupport.](#implementing-imfratesupport)</span><span class="sxs-lookup"><span data-stu-id="f833a-219">See [Implementing IMFRateSupport](#implementing-imfratesupport).</span></span>                                         |
| [<span data-ttu-id="f833a-220">**IMFVideoPositionMapper**</span><span class="sxs-lookup"><span data-stu-id="f833a-220">**IMFVideoPositionMapper**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper) | <span data-ttu-id="f833a-221">Esegue il mapping delle coordinate del fotogramma video di output alle coordinate sul fotogramma video di input.</span><span class="sxs-lookup"><span data-stu-id="f833a-221">Maps coordinates on the output video frame to coordinates on the input video frame.</span></span>                                                                                       |
| [<span data-ttu-id="f833a-222">**IQualProp**</span><span class="sxs-lookup"><span data-stu-id="f833a-222">**IQualProp**</span></span>](/previous-versions/windows/desktop/api/amvideo/nn-amvideo-iqualprop)                         | <span data-ttu-id="f833a-223">Segnala informazioni sulle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="f833a-223">Reports performance information.</span></span> <span data-ttu-id="f833a-224">L'EVR usa queste informazioni per la gestione del controllo di qualità.</span><span class="sxs-lookup"><span data-stu-id="f833a-224">The EVR uses this information for quality-control management.</span></span> <span data-ttu-id="f833a-225">Questa interfaccia è documentata in DirectShow SDK.</span><span class="sxs-lookup"><span data-stu-id="f833a-225">This interface is documented in the DirectShow SDK.</span></span>                        |



 

<span data-ttu-id="f833a-226">È anche possibile fornire interfacce per consentire all'applicazione di comunicare con il presentatore.</span><span class="sxs-lookup"><span data-stu-id="f833a-226">You can also provide interfaces for the application to communicate with the presenter.</span></span> <span data-ttu-id="f833a-227">A questo scopo, il presentatore standard implementa l'interfaccia [**IMFVideoDisplayControl.**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol)</span><span class="sxs-lookup"><span data-stu-id="f833a-227">The standard presenter implements the [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) interface for this purpose.</span></span> <span data-ttu-id="f833a-228">È possibile implementare questa interfaccia o definirne una personalizzata.</span><span class="sxs-lookup"><span data-stu-id="f833a-228">You can implement this interface or define your own.</span></span> <span data-ttu-id="f833a-229">L'applicazione ottiene le interfacce dal presentatore chiamando [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) su EVR.</span><span class="sxs-lookup"><span data-stu-id="f833a-229">The application obtains interfaces from the presenter by calling [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) on the EVR.</span></span> <span data-ttu-id="f833a-230">Quando il GUID del **servizio MR_VIDEO_RENDER_SERVICE**, EVR passa la **richiesta GetService** al presentatore.</span><span class="sxs-lookup"><span data-stu-id="f833a-230">When the service GUID is **MR_VIDEO_RENDER_SERVICE**, the EVR passes the **GetService** request to the presenter.</span></span>

### <a name="implementing-imfvideodeviceid"></a><span data-ttu-id="f833a-231">Implementazione di IMFVideoDeviceID</span><span class="sxs-lookup"><span data-stu-id="f833a-231">Implementing IMFVideoDeviceID</span></span>

<span data-ttu-id="f833a-232">[**L'interfaccia IMFVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid) contiene un metodo, [**GetDeviceID,**](/windows/desktop/api/evr/nf-evr-imfvideodeviceid-getdeviceid)che restituisce un GUID del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f833a-232">The [**IMFVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid) interface contains one method, [**GetDeviceID**](/windows/desktop/api/evr/nf-evr-imfvideodeviceid-getdeviceid), which returns a device GUID.</span></span> <span data-ttu-id="f833a-233">Il GUID del dispositivo garantisce che il presentatore e il mixer usino tecnologie compatibili.</span><span class="sxs-lookup"><span data-stu-id="f833a-233">The device GUID ensures that the presenter and the mixer use compatible technologies.</span></span> <span data-ttu-id="f833a-234">Se i GUID del dispositivo non corrispondono, l'inizializzazione di EVR non riesce.</span><span class="sxs-lookup"><span data-stu-id="f833a-234">If the device GUIDs do not match, the EVR fails to initialize.</span></span>

<span data-ttu-id="f833a-235">Il mixer e il presentatore standard usano entrambi Direct3D 9, con il GUID del dispositivo uguale **IID_IDirect3DDevice9**.</span><span class="sxs-lookup"><span data-stu-id="f833a-235">The standard mixer and presenter both use Direct3D 9, with the device GUID equal to **IID_IDirect3DDevice9**.</span></span> <span data-ttu-id="f833a-236">Se si intende usare il presentatore personalizzato con il mixer standard, il GUID del dispositivo del presentatore deve essere **IID_IDirect3DDevice9**.</span><span class="sxs-lookup"><span data-stu-id="f833a-236">If you intend to use your custom presenter with the standard mixer, the presenter's device GUID must be **IID_IDirect3DDevice9**.</span></span> <span data-ttu-id="f833a-237">Se si sostituiscono entrambi i componenti, è possibile definire un nuovo GUID del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f833a-237">If you replace both components, you could define a new device GUID.</span></span> <span data-ttu-id="f833a-238">Nella parte restante di questo articolo si presuppone che il presentatore usi Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="f833a-238">For the remainder of this article, it is assumed that the presenter uses Direct3D 9.</span></span> <span data-ttu-id="f833a-239">Ecco l'implementazione standard di [**GetDeviceID:**](/windows/desktop/api/evr/nf-evr-imfvideodeviceid-getdeviceid)</span><span class="sxs-lookup"><span data-stu-id="f833a-239">Here is the standard implementation of [**GetDeviceID**](/windows/desktop/api/evr/nf-evr-imfvideodeviceid-getdeviceid):</span></span>


```C++
HRESULT EVRCustomPresenter::GetDeviceID(IID* pDeviceID)
{
    if (pDeviceID == NULL)
    {
        return E_POINTER;
    }

    *pDeviceID = __uuidof(IDirect3DDevice9);
    return S_OK;
}
```



<span data-ttu-id="f833a-240">Il metodo deve avere esito positivo anche quando il presentatore viene arrestato.</span><span class="sxs-lookup"><span data-stu-id="f833a-240">The method should succeed even when the presenter is shut down.</span></span>

### <a name="implementing-imftopologyservicelookupclient"></a><span data-ttu-id="f833a-241">Implementazione di IMFTopologyServiceLookupClient</span><span class="sxs-lookup"><span data-stu-id="f833a-241">Implementing IMFTopologyServiceLookupClient</span></span>

<span data-ttu-id="f833a-242">[**L'interfaccia IMFTopologyServiceLookupClient**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient) consente al presentatore di ottenere i puntatori di interfaccia da EVR e dal mixer come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="f833a-242">The [**IMFTopologyServiceLookupClient**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient) interface enables the presenter to get interface pointers from the EVR and from the mixer as follows:</span></span>

1.  <span data-ttu-id="f833a-243">Quando EVR inizializza il presentatore, chiama il metodo [**IMFTopologyServiceLookupClient::InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) del presentatore.</span><span class="sxs-lookup"><span data-stu-id="f833a-243">When the EVR initializes the presenter, it calls the presenter's [**IMFTopologyServiceLookupClient::InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) method.</span></span> <span data-ttu-id="f833a-244">L'argomento è un puntatore [**all'interfaccia IMFTopologyServiceLookup di EVR.**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookup)</span><span class="sxs-lookup"><span data-stu-id="f833a-244">The argument is a pointer to the EVR's [**IMFTopologyServiceLookup**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookup) interface.</span></span>
2.  <span data-ttu-id="f833a-245">Il presentatore chiama [**IMFTopologyServiceLookup::LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice) per ottenere i puntatori a interfaccia dall'EVR o dal mixer.</span><span class="sxs-lookup"><span data-stu-id="f833a-245">The presenter calls [**IMFTopologyServiceLookup::LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice) to get interface pointers from either the EVR or the mixer.</span></span>

<span data-ttu-id="f833a-246">Il [**metodo LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice) è simile al [**metodo IMFGetService::GetService.**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice)</span><span class="sxs-lookup"><span data-stu-id="f833a-246">The [**LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice) method is similar to the [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) method.</span></span> <span data-ttu-id="f833a-247">Entrambi i metodi accettano un GUID del servizio e un identificatore di interfaccia (IID) come input, ma **LookupService** restituisce una matrice di puntatori a interfaccia, mentre **GetService** restituisce un singolo puntatore.</span><span class="sxs-lookup"><span data-stu-id="f833a-247">Both methods take a service GUID and an interface identifier (IID) as input, but **LookupService** returns an array of interface pointers, while **GetService** returns a single pointer.</span></span> <span data-ttu-id="f833a-248">In pratica, tuttavia, è sempre possibile impostare le dimensioni della matrice su 1.</span><span class="sxs-lookup"><span data-stu-id="f833a-248">In practice, however, you can always set the array size to 1.</span></span> <span data-ttu-id="f833a-249">L'oggetto sottoposto a query dipende dal GUID del servizio:</span><span class="sxs-lookup"><span data-stu-id="f833a-249">The object queried depends on the service GUID:</span></span>

-   <span data-ttu-id="f833a-250">Se il GUID del servizio **MR_VIDEO_RENDER_SERVICE**, viene eseguita una query su EVR.</span><span class="sxs-lookup"><span data-stu-id="f833a-250">If the service GUID is **MR_VIDEO_RENDER_SERVICE**, the EVR is queried.</span></span>
-   <span data-ttu-id="f833a-251">Se il GUID del servizio **MR_VIDEO_MIXER_SERVICE**, viene eseguita una query sul mixer.</span><span class="sxs-lookup"><span data-stu-id="f833a-251">If the service GUID is **MR_VIDEO_MIXER_SERVICE**, the mixer is queried.</span></span>

<span data-ttu-id="f833a-252">Nell'implementazione [**di InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers)ottenere le interfacce seguenti da EVR:</span><span class="sxs-lookup"><span data-stu-id="f833a-252">In your implementation of [**InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers), get the following interfaces from the EVR:</span></span>



| <span data-ttu-id="f833a-253">Interfaccia EVR</span><span class="sxs-lookup"><span data-stu-id="f833a-253">EVR Interface</span></span>                                | <span data-ttu-id="f833a-254">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f833a-254">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f833a-255">**IMediaEventSink**</span><span class="sxs-lookup"><span data-stu-id="f833a-255">**IMediaEventSink**</span></span>](/windows/win32/api/strmif/nn-strmif-imediaeventsink) | <span data-ttu-id="f833a-256">Consente al presentatore di inviare messaggi all'EVR.</span><span class="sxs-lookup"><span data-stu-id="f833a-256">Provides a way for the presenter to send messages to the EVR.</span></span> <span data-ttu-id="f833a-257">Questa interfaccia è definita in DirectShow SDK, quindi i messaggi seguono il modello per gli eventi DirectShow, non per Media Foundation eventi.</span><span class="sxs-lookup"><span data-stu-id="f833a-257">This interface is defined in the DirectShow SDK, so the messages follow the pattern for DirectShow events, not Media Foundation events.</span></span><br/>                                                                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="f833a-258">**IMFClock**</span><span class="sxs-lookup"><span data-stu-id="f833a-258">**IMFClock**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfclock)                 | <span data-ttu-id="f833a-259">Rappresenta l'orologio dell'EVR.</span><span class="sxs-lookup"><span data-stu-id="f833a-259">Represents the EVR's clock.</span></span> <span data-ttu-id="f833a-260">Il presentatore usa questa interfaccia per pianificare gli esempi per la presentazione.</span><span class="sxs-lookup"><span data-stu-id="f833a-260">The presenter uses this interface to schedule samples for presentation.</span></span> <span data-ttu-id="f833a-261">L'EVR può essere eseguito senza clock, pertanto questa interfaccia potrebbe non essere disponibile.</span><span class="sxs-lookup"><span data-stu-id="f833a-261">The EVR can run without a clock, so this interface might not be available.</span></span> <span data-ttu-id="f833a-262">In caso contrario, ignorare il codice di errore [**da LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice).</span><span class="sxs-lookup"><span data-stu-id="f833a-262">If not, ignore the error code from [**LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice).</span></span><br/> <span data-ttu-id="f833a-263">L'orologio implementa anche [**l'interfaccia IMFTimer.**](/windows/desktop/api/mfidl/nn-mfidl-imftimer)</span><span class="sxs-lookup"><span data-stu-id="f833a-263">The clock also implements the [**IMFTimer**](/windows/desktop/api/mfidl/nn-mfidl-imftimer) interface.</span></span> <span data-ttu-id="f833a-264">Nella pipeline Media Foundation l'orologio implementa [**l'interfaccia IMFPresentationClock.**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock)</span><span class="sxs-lookup"><span data-stu-id="f833a-264">In the Media Foundation pipeline, the clock implements the [**IMFPresentationClock**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock) interface.</span></span> <span data-ttu-id="f833a-265">Non implementa questa interfaccia in DirectShow.</span><span class="sxs-lookup"><span data-stu-id="f833a-265">It does not implement this interface in DirectShow.</span></span><br/> |



 

<span data-ttu-id="f833a-266">Ottenere le interfacce seguenti dal mixer:</span><span class="sxs-lookup"><span data-stu-id="f833a-266">Get the following interfaces from the mixer:</span></span>



| <span data-ttu-id="f833a-267">Interfaccia mixer</span><span class="sxs-lookup"><span data-stu-id="f833a-267">Mixer Interface</span></span>                              | <span data-ttu-id="f833a-268">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f833a-268">Description</span></span>                                                |
|----------------------------------------------|------------------------------------------------------------|
| [<span data-ttu-id="f833a-269">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="f833a-269">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)         | <span data-ttu-id="f833a-270">Consente al presentatore di comunicare con il mixer.</span><span class="sxs-lookup"><span data-stu-id="f833a-270">Enables the presenter to communicate with the mixer.</span></span>       |
| [<span data-ttu-id="f833a-271">**IMFVideoDeviceID**</span><span class="sxs-lookup"><span data-stu-id="f833a-271">**IMFVideoDeviceID**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideodeviceid) | <span data-ttu-id="f833a-272">Consente al presentatore di convalidare il GUID del dispositivo del mixer.</span><span class="sxs-lookup"><span data-stu-id="f833a-272">Enables the presenter to validate the mixer's device GUID.</span></span> |



 

<span data-ttu-id="f833a-273">Il codice seguente implementa il [**metodo InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) :</span><span class="sxs-lookup"><span data-stu-id="f833a-273">The following code implements the [**InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) method :</span></span>


```C++
HRESULT EVRCustomPresenter::InitServicePointers(
    IMFTopologyServiceLookup *pLookup
    )
{
    if (pLookup == NULL)
    {
        return E_POINTER;
    }

    HRESULT             hr = S_OK;
    DWORD               dwObjectCount = 0;

    EnterCriticalSection(&m_ObjectLock);

    // Do not allow initializing when playing or paused.
    if (IsActive())
    {
        hr = MF_E_INVALIDREQUEST;
        goto done;
    }

    SafeRelease(&m_pClock);
    SafeRelease(&m_pMixer);
    SafeRelease(&m_pMediaEventSink);

    // Ask for the clock. Optional, because the EVR might not have a clock.
    dwObjectCount = 1;

    (void)pLookup->LookupService(
        MF_SERVICE_LOOKUP_GLOBAL,   // Not used.
        0,                          // Reserved.
        MR_VIDEO_RENDER_SERVICE,    // Service to look up.
        IID_PPV_ARGS(&m_pClock),    // Interface to retrieve.
        &dwObjectCount              // Number of elements retrieved.
        );

    // Ask for the mixer. (Required.)
    dwObjectCount = 1;

    hr = pLookup->LookupService(
        MF_SERVICE_LOOKUP_GLOBAL, 0,
        MR_VIDEO_MIXER_SERVICE, IID_PPV_ARGS(&m_pMixer), &dwObjectCount
        );

    if (FAILED(hr))
    {
        goto done;
    }

    // Make sure that we can work with this mixer.
    hr = ConfigureMixer(m_pMixer);
    if (FAILED(hr))
    {
        goto done;
    }

    // Ask for the EVR's event-sink interface. (Required.)
    dwObjectCount = 1;

    hr = pLookup->LookupService(
        MF_SERVICE_LOOKUP_GLOBAL, 0,
        MR_VIDEO_RENDER_SERVICE, IID_PPV_ARGS(&m_pMediaEventSink),
        &dwObjectCount
        );

    if (FAILED(hr))
    {
        goto done;
    }

    // Successfully initialized. Set the state to "stopped."
    m_RenderState = RENDER_STATE_STOPPED;

done:
    LeaveCriticalSection(&m_ObjectLock);
    return hr;
}
```



<span data-ttu-id="f833a-274">Quando i puntatori a interfaccia ottenuti da [**LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice) non sono più validi, L'EVR chiama [**IMFTopologyServiceLookupClient::ReleaseServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers).</span><span class="sxs-lookup"><span data-stu-id="f833a-274">When the interface pointers obtained from [**LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice) are no longer valid, the EVR calls [**IMFTopologyServiceLookupClient::ReleaseServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers).</span></span> <span data-ttu-id="f833a-275">All'interno di questo metodo rilasciare tutti i puntatori a interfaccia e impostare lo stato del presentatore per l'arresto:</span><span class="sxs-lookup"><span data-stu-id="f833a-275">Inside this method, release all interface pointers and set the presenter state to shut down:</span></span>


```C++
HRESULT EVRCustomPresenter::ReleaseServicePointers()
{
    // Enter the shut-down state.
    EnterCriticalSection(&m_ObjectLock);

    m_RenderState = RENDER_STATE_SHUTDOWN;

    LeaveCriticalSection(&m_ObjectLock);

    // Flush any samples that were scheduled.
    Flush();

    // Clear the media type and release related resources.
    SetMediaType(NULL);

    // Release all services that were acquired from InitServicePointers.
    SafeRelease(&m_pClock);
    SafeRelease(&m_pMixer);
    SafeRelease(&m_pMediaEventSink);

    return S_OK;
}
```



<span data-ttu-id="f833a-276">L'EVR chiama [**ReleaseServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers) per vari motivi, tra cui:</span><span class="sxs-lookup"><span data-stu-id="f833a-276">The EVR calls [**ReleaseServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers) for various reasons, including:</span></span>

-   <span data-ttu-id="f833a-277">Disconnessione o riconnessione dei pin (DirectShow) o aggiunta o rimozione di sink di flusso (Media Foundation).</span><span class="sxs-lookup"><span data-stu-id="f833a-277">Disconnecting or reconnecting pins (DirectShow), or adding or removing stream sinks (Media Foundation).</span></span>
-   <span data-ttu-id="f833a-278">Modifica del formato.</span><span class="sxs-lookup"><span data-stu-id="f833a-278">Changing format.</span></span>
-   <span data-ttu-id="f833a-279">Impostazione di un nuovo orologio.</span><span class="sxs-lookup"><span data-stu-id="f833a-279">Setting a new clock.</span></span>
-   <span data-ttu-id="f833a-280">Arresto finale di EVR.</span><span class="sxs-lookup"><span data-stu-id="f833a-280">Final shutdown of the EVR.</span></span>

<span data-ttu-id="f833a-281">Durante la durata del presentatore, EVR potrebbe chiamare [**InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) e [**ReleaseServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers) più volte.</span><span class="sxs-lookup"><span data-stu-id="f833a-281">During the lifetime of the presenter, the EVR might call [**InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) and [**ReleaseServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers) several times.</span></span>

### <a name="implementing-imfvideopresenter"></a><span data-ttu-id="f833a-282">Implementazione di IMFVideoPresenter</span><span class="sxs-lookup"><span data-stu-id="f833a-282">Implementing IMFVideoPresenter</span></span>

<span data-ttu-id="f833a-283">[**L'interfaccia IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter) eredita [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink) e aggiunge due metodi:</span><span class="sxs-lookup"><span data-stu-id="f833a-283">The [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter) interface inherits [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink) and adds two methods:</span></span>



| <span data-ttu-id="f833a-284">Metodo</span><span class="sxs-lookup"><span data-stu-id="f833a-284">Method</span></span>                                                               | <span data-ttu-id="f833a-285">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f833a-285">Description</span></span>                                            |
|----------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="f833a-286">**GetCurrentMediaType**</span><span class="sxs-lookup"><span data-stu-id="f833a-286">**GetCurrentMediaType**</span></span>](/windows/desktop/api/evr/nf-evr-imfvideopresenter-getcurrentmediatype) | <span data-ttu-id="f833a-287">Restituisce il tipo di contenuto multimediale dei fotogrammi video compositi.</span><span class="sxs-lookup"><span data-stu-id="f833a-287">Returns the media type of the composited video frames.</span></span> |
| [<span data-ttu-id="f833a-288">**ProcessMessage**</span><span class="sxs-lookup"><span data-stu-id="f833a-288">**ProcessMessage**</span></span>](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage)           | <span data-ttu-id="f833a-289">Segnala al presentatore di eseguire varie azioni.</span><span class="sxs-lookup"><span data-stu-id="f833a-289">Signals the presenter to perform various actions.</span></span>      |



 

<span data-ttu-id="f833a-290">Il [**metodo GetCurrentMediaType**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-getcurrentmediatype) restituisce il tipo di supporto del presentatore.</span><span class="sxs-lookup"><span data-stu-id="f833a-290">The [**GetCurrentMediaType**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-getcurrentmediatype) method returns the presenter's media type.</span></span> <span data-ttu-id="f833a-291">Per informazioni dettagliate sull'impostazione del tipo di supporto, vedere [Formati di negoziazione.](#negotiating-formats) Il tipo di supporto viene restituito come [**puntatore a interfaccia IMFVideoMediaType.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfvideomediatype)</span><span class="sxs-lookup"><span data-stu-id="f833a-291">(For details about setting the media type, see [Negotiating Formats](#negotiating-formats).) The media type is returned as an [**IMFVideoMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfvideomediatype) interface pointer.</span></span> <span data-ttu-id="f833a-292">Nell'esempio seguente si presuppone che il presentatore archivi il tipo di supporto come [**puntatore IMFMediaType.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)</span><span class="sxs-lookup"><span data-stu-id="f833a-292">The following example assumes that the presenter stores the media type as an [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) pointer.</span></span> <span data-ttu-id="f833a-293">Per ottenere **l'interfaccia IMFVideoMediaType** dal tipo di supporto, chiamare **QueryInterface:**</span><span class="sxs-lookup"><span data-stu-id="f833a-293">To get the **IMFVideoMediaType** interface from the media type, call **QueryInterface**:</span></span>


```C++
HRESULT EVRCustomPresenter::GetCurrentMediaType(
    IMFVideoMediaType** ppMediaType
    )
{
    HRESULT hr = S_OK;

    if (ppMediaType == NULL)
    {
        return E_POINTER;
    }

    *ppMediaType = NULL;

    EnterCriticalSection(&m_ObjectLock);

    hr = CheckShutdown();
    if (FAILED(hr))
    {
        goto done;
    }

    if (m_pMediaType == NULL)
    {
        hr = MF_E_NOT_INITIALIZED;
        goto done;
    }

    hr = m_pMediaType->QueryInterface(IID_PPV_ARGS(ppMediaType));

done:
    LeaveCriticalSection(&m_ObjectLock);
    return hr;
}
```



<span data-ttu-id="f833a-294">Il [**metodo ProcessMessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) è il meccanismo principale per la comunicazione tra EVR e il presentatore.</span><span class="sxs-lookup"><span data-stu-id="f833a-294">The [**ProcessMessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) method is the primary mechanism for the EVR to communicate with the presenter.</span></span> <span data-ttu-id="f833a-295">Vengono definiti i messaggi seguenti.</span><span class="sxs-lookup"><span data-stu-id="f833a-295">The following messages are defined.</span></span> <span data-ttu-id="f833a-296">I dettagli dell'implementazione di ogni messaggio sono disponibili nella parte restante di questo argomento.</span><span class="sxs-lookup"><span data-stu-id="f833a-296">The details of implementing each message are given in the remainder of this topic.</span></span>



| <span data-ttu-id="f833a-297">Message</span><span class="sxs-lookup"><span data-stu-id="f833a-297">Message</span></span>                                | <span data-ttu-id="f833a-298">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f833a-298">Description</span></span>                                                                                                                                                                                                                                        |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f833a-299">**MFVP_MESSAGE_INVALIDATEMEDIATYPE**</span><span class="sxs-lookup"><span data-stu-id="f833a-299">**MFVP_MESSAGE_INVALIDATEMEDIATYPE**</span></span> | <span data-ttu-id="f833a-300">Il tipo di supporto di output del mixer non è valido.</span><span class="sxs-lookup"><span data-stu-id="f833a-300">The mixer's output media type is invalid.</span></span> <span data-ttu-id="f833a-301">Il presentatore deve negoziare un nuovo tipo di supporto con il mixer.</span><span class="sxs-lookup"><span data-stu-id="f833a-301">The presenter should negotiate a new media type with the mixer.</span></span> <span data-ttu-id="f833a-302">Vedere [Formati di negoziazione](#negotiating-formats).</span><span class="sxs-lookup"><span data-stu-id="f833a-302">See [Negotiating Formats](#negotiating-formats).</span></span>                                                                                         |
| <span data-ttu-id="f833a-303">**MFVP_MESSAGE_BEGINSTREAMING**</span><span class="sxs-lookup"><span data-stu-id="f833a-303">**MFVP_MESSAGE_BEGINSTREAMING**</span></span>      | <span data-ttu-id="f833a-304">Lo streaming è stato avviato.</span><span class="sxs-lookup"><span data-stu-id="f833a-304">Streaming has started.</span></span> <span data-ttu-id="f833a-305">Questo messaggio non richiede alcuna azione specifica, ma è possibile usarlo per allocare risorse.</span><span class="sxs-lookup"><span data-stu-id="f833a-305">No particular action is required by this message, but you can use it to allocate resources.</span></span>                                                                                                                                 |
| <span data-ttu-id="f833a-306">**MFVP_MESSAGE_ENDSTREAMING**</span><span class="sxs-lookup"><span data-stu-id="f833a-306">**MFVP_MESSAGE_ENDSTREAMING**</span></span>        | <span data-ttu-id="f833a-307">Lo streaming è terminato.</span><span class="sxs-lookup"><span data-stu-id="f833a-307">Streaming has ended.</span></span> <span data-ttu-id="f833a-308">Rilasciare tutte le risorse allocate in risposta al **MFVP_MESSAGE_BEGINSTREAMING** messaggio.</span><span class="sxs-lookup"><span data-stu-id="f833a-308">Release any resources that you allocated in response to the **MFVP_MESSAGE_BEGINSTREAMING** message.</span></span>                                                                                                                        |
| <span data-ttu-id="f833a-309">**MFVP_MESSAGE_PROCESSINPUTNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="f833a-309">**MFVP_MESSAGE_PROCESSINPUTNOTIFY**</span></span>  | <span data-ttu-id="f833a-310">Il mixer ha ricevuto un nuovo esempio di input e potrebbe essere in grado di generare un nuovo frame di output.</span><span class="sxs-lookup"><span data-stu-id="f833a-310">The mixer has received a new input sample and might be able to generate a new output frame.</span></span> <span data-ttu-id="f833a-311">Il presentatore deve chiamare [**IMFTransform::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) nel mixer.</span><span class="sxs-lookup"><span data-stu-id="f833a-311">The presenter should call [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) on the mixer.</span></span> <span data-ttu-id="f833a-312">Vedere [Output di elaborazione](#processing-output).</span><span class="sxs-lookup"><span data-stu-id="f833a-312">See [Processing Output](#processing-output).</span></span> |
| <span data-ttu-id="f833a-313">**MFVP_MESSAGE_ENDOFSTREAM**</span><span class="sxs-lookup"><span data-stu-id="f833a-313">**MFVP_MESSAGE_ENDOFSTREAM**</span></span>         | <span data-ttu-id="f833a-314">La presentazione è terminata.</span><span class="sxs-lookup"><span data-stu-id="f833a-314">The presentation has ended.</span></span> <span data-ttu-id="f833a-315">Vedere [Fine del flusso](#end-of-stream).</span><span class="sxs-lookup"><span data-stu-id="f833a-315">See [End of Stream](#end-of-stream).</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="f833a-316">**MFVP_MESSAGE_FLUSH**</span><span class="sxs-lookup"><span data-stu-id="f833a-316">**MFVP_MESSAGE_FLUSH**</span></span>               | <span data-ttu-id="f833a-317">L'EVR sta scaricando i dati nella pipeline di rendering.</span><span class="sxs-lookup"><span data-stu-id="f833a-317">The EVR is flushing the data in its rendering pipeline.</span></span> <span data-ttu-id="f833a-318">Il presentatore deve eliminare tutti i fotogrammi video pianificati per la presentazione.</span><span class="sxs-lookup"><span data-stu-id="f833a-318">The presenter should discard any video frames that are scheduled for presentation.</span></span>                                                                                                         |
| <span data-ttu-id="f833a-319">**MFVP_MESSAGE_STEP**</span><span class="sxs-lookup"><span data-stu-id="f833a-319">**MFVP_MESSAGE_STEP**</span></span>                | <span data-ttu-id="f833a-320">Richiede al presentatore di eseguire un passaggio avanti di N fotogrammi.</span><span class="sxs-lookup"><span data-stu-id="f833a-320">Requests the presenter to step forward N frames.</span></span> <span data-ttu-id="f833a-321">Il presentatore deve rimuovere i fotogrammi N-1 successivi e visualizzare l'N° frame.</span><span class="sxs-lookup"><span data-stu-id="f833a-321">The presenter should discard the next N-1 frames and display the Nth frame.</span></span> <span data-ttu-id="f833a-322">Vedere [Esecuzione di istruzioni per i frame](#frame-stepping).</span><span class="sxs-lookup"><span data-stu-id="f833a-322">See [Frame Stepping](#frame-stepping).</span></span>                                                                                |
| <span data-ttu-id="f833a-323">**MFVP_MESSAGE_CANCELSTEP**</span><span class="sxs-lookup"><span data-stu-id="f833a-323">**MFVP_MESSAGE_CANCELSTEP**</span></span>          | <span data-ttu-id="f833a-324">Annulla l'esecuzione di istruzioni per i frame.</span><span class="sxs-lookup"><span data-stu-id="f833a-324">Cancels frame stepping.</span></span>                                                                                                                                                                                                                            |



 

### <a name="implementing-imfclockstatesink"></a><span data-ttu-id="f833a-325">Implementazione di IMFClockStateSink</span><span class="sxs-lookup"><span data-stu-id="f833a-325">Implementing IMFClockStateSink</span></span>

<span data-ttu-id="f833a-326">Il presentatore deve implementare [**l'interfaccia IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink) come parte dell'implementazione di [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter), che eredita **IMFClockStateSink.**</span><span class="sxs-lookup"><span data-stu-id="f833a-326">The presenter must implement the [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink) interface as part of its implementation of [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter), which inherits **IMFClockStateSink**.</span></span> <span data-ttu-id="f833a-327">L'EVR usa questa interfaccia per inviare una notifica al presentatore ogni volta che lo stato dell'orologio dell'EVR cambia.</span><span class="sxs-lookup"><span data-stu-id="f833a-327">The EVR uses this interface to notify the presenter whenever the EVR's clock changes state.</span></span> <span data-ttu-id="f833a-328">Per altre informazioni sugli stati dell'orologio, vedere [Presentation Clock](presentation-clock.md).</span><span class="sxs-lookup"><span data-stu-id="f833a-328">For more information about the clock states, see [Presentation Clock](presentation-clock.md).</span></span>

<span data-ttu-id="f833a-329">Ecco alcune linee guida per l'implementazione dei metodi in questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="f833a-329">Here are some guidelines for implementing the methods in this interface.</span></span> <span data-ttu-id="f833a-330">Tutti i metodi dovrebbero avere esito negativo se il presentatore viene arrestato.</span><span class="sxs-lookup"><span data-stu-id="f833a-330">All of the methods should fail if the presenter is shut down.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f833a-331"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart"><strong>OnClockStart</strong></a></span><span class="sxs-lookup"><span data-stu-id="f833a-331"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart"><strong>OnClockStart</strong></a></span></span></td>
<td><ol>
<li><span data-ttu-id="f833a-332">Impostare lo stato del presentatore su started.</span><span class="sxs-lookup"><span data-stu-id="f833a-332">Set the presenter state to started.</span></span></li>
<li><span data-ttu-id="f833a-333">Se <em>llClockStartOffset</em> non <strong>è</strong>PRESENTATION_CURRENT_POSITION , scaricare la coda di esempi del presentatore.</span><span class="sxs-lookup"><span data-stu-id="f833a-333">If the <em>llClockStartOffset</em> is not <strong>PRESENTATION_CURRENT_POSITION</strong>, flush the presenter's queue of samples.</span></span> <span data-ttu-id="f833a-334">Equivale a ricevere un messaggio <strong>MFVP_MESSAGE_FLUSH</strong> messaggio.</span><span class="sxs-lookup"><span data-stu-id="f833a-334">(This is equivalent to receiving an <strong>MFVP_MESSAGE_FLUSH</strong> message.)</span></span></li>
<li><span data-ttu-id="f833a-335">Se una richiesta del passaggio del frame precedente è ancora in sospeso, elaborare la richiesta (vedere <a href="#frame-stepping">Frame Stepping</a>).</span><span class="sxs-lookup"><span data-stu-id="f833a-335">If a previous frame-step request is still pending, process the request (see <a href="#frame-stepping">Frame Stepping</a>).</span></span> <span data-ttu-id="f833a-336">In caso contrario, provare a elaborare l'output dal mixer (vedere <a href="#processing-output">Output di elaborazione</a>).</span><span class="sxs-lookup"><span data-stu-id="f833a-336">Otherwise, try to process output from the mixer (see <a href="#processing-output">Processing Output</a>.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f833a-337"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstop"><strong>OnClockStop</strong></a></span><span class="sxs-lookup"><span data-stu-id="f833a-337"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstop"><strong>OnClockStop</strong></a></span></span></td>
<td><ol>
<li><span data-ttu-id="f833a-338">Impostare lo stato del presentatore su arrestato.</span><span class="sxs-lookup"><span data-stu-id="f833a-338">Set the presenter state to stopped.</span></span></li>
<li><span data-ttu-id="f833a-339">Scaricare la coda di esempi del presentatore.</span><span class="sxs-lookup"><span data-stu-id="f833a-339">Flush the presenter's queue of samples.</span></span></li>
<li><span data-ttu-id="f833a-340">Annullare qualsiasi operazione in sospeso del passaggio del frame.</span><span class="sxs-lookup"><span data-stu-id="f833a-340">Cancel any pending frame-step operation.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f833a-341"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockpause"><strong>OnClockPause</strong></a></span><span class="sxs-lookup"><span data-stu-id="f833a-341"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockpause"><strong>OnClockPause</strong></a></span></span></td>
<td><span data-ttu-id="f833a-342">Impostare lo stato del presentatore su Sospeso.</span><span class="sxs-lookup"><span data-stu-id="f833a-342">Set the presenter state to paused.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f833a-343"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart"><strong>OnClockRestart</strong></a></span><span class="sxs-lookup"><span data-stu-id="f833a-343"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart"><strong>OnClockRestart</strong></a></span></span></td>
<td><span data-ttu-id="f833a-344">Trattare come <a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart"><strong>OnClockStart,</strong></a> ma non scaricare la coda di esempi.</span><span class="sxs-lookup"><span data-stu-id="f833a-344">Treat the same as <a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart"><strong>OnClockStart</strong></a> but do not flush the queue of samples.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f833a-345"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate"><strong>OnClockSetRate</strong></a></span><span class="sxs-lookup"><span data-stu-id="f833a-345"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate"><strong>OnClockSetRate</strong></a></span></span></td>
<td><ol>
<li><span data-ttu-id="f833a-346">Se la frequenza cambia da zero a diversa da zero, annullare l'esecuzione del frame.</span><span class="sxs-lookup"><span data-stu-id="f833a-346">If the rate is changing from zero to nonzero, cancel frame stepping.</span></span></li>
<li><span data-ttu-id="f833a-347">Archiviare la nuova frequenza di clock.</span><span class="sxs-lookup"><span data-stu-id="f833a-347">Store the new clock rate.</span></span> <span data-ttu-id="f833a-348">La frequenza di clock influisce sulla presentazione dei campioni.</span><span class="sxs-lookup"><span data-stu-id="f833a-348">The clock rate affects when samples are presented.</span></span> <span data-ttu-id="f833a-349">Per altre informazioni, vedere <a href="#scheduling-samples">Esempi di pianificazione</a>.</span><span class="sxs-lookup"><span data-stu-id="f833a-349">For more information, see <a href="#scheduling-samples">Scheduling Samples</a>.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="implementing-imfratesupport"></a><span data-ttu-id="f833a-350">Implementazione di IMFRateSupport</span><span class="sxs-lookup"><span data-stu-id="f833a-350">Implementing IMFRateSupport</span></span>

<span data-ttu-id="f833a-351">Per supportare velocità di riproduzione diverse da 1×, il presentatore deve implementare [**l'interfaccia IMFRateSupport.**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)</span><span class="sxs-lookup"><span data-stu-id="f833a-351">To support playback rates other than 1× speed, the presenter must implement the [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) interface.</span></span> <span data-ttu-id="f833a-352">Ecco alcune linee guida per l'implementazione dei metodi in questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="f833a-352">Here are some guidelines for implementing the methods in this interface.</span></span> <span data-ttu-id="f833a-353">Tutti i metodi devono avere esito negativo dopo l'arresto del presentatore.</span><span class="sxs-lookup"><span data-stu-id="f833a-353">All of the methods should fail after the presenter is shut down.</span></span> <span data-ttu-id="f833a-354">Per altre informazioni su questa interfaccia, vedere [Controllo della frequenza.](rate-control.md)</span><span class="sxs-lookup"><span data-stu-id="f833a-354">For more information about this interface, see [Rate Control](rate-control.md).</span></span>



| <span data-ttu-id="f833a-355">Valore</span><span class="sxs-lookup"><span data-stu-id="f833a-355">Value</span></span>                                                          | <span data-ttu-id="f833a-356">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f833a-356">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f833a-357">**GetSlowestRate**</span><span class="sxs-lookup"><span data-stu-id="f833a-357">**GetSlowestRate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getslowestrate)   | <span data-ttu-id="f833a-358">Restituisce zero per indicare nessuna velocità di riproduzione minima.</span><span class="sxs-lookup"><span data-stu-id="f833a-358">Return zero to indicate no minimum playback rate.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="f833a-359">**GetFastestRate**</span><span class="sxs-lookup"><span data-stu-id="f833a-359">**GetFastestRate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getfastestrate)   | <span data-ttu-id="f833a-360">Per la riproduzione non thinned, la frequenza di riproduzione non deve superare la frequenza di aggiornamento del *monitoraggio:* frequenza massima di aggiornamento della frequenza  =   (Hz) /frequenza *fotogrammi video* (fps).</span><span class="sxs-lookup"><span data-stu-id="f833a-360">For non-thinned playback, the playback rate should not exceed the refresh rate of the monitor: *maximum rate* = *refresh rate* (Hz) / *video frame rate* (fps).</span></span> <span data-ttu-id="f833a-361">La frequenza dei fotogrammi video è specificata nel tipo di supporto del presentatore.</span><span class="sxs-lookup"><span data-stu-id="f833a-361">The video frame rate is specified in the presenter's media type.</span></span> <br/> <span data-ttu-id="f833a-362">Per la riproduzione thinned, la velocità di riproduzione è illimitata; restituisce il valore **FLT_MAX**.</span><span class="sxs-lookup"><span data-stu-id="f833a-362">For thinned playback, the playback rate is unbounded; return the value **FLT_MAX**.</span></span> <span data-ttu-id="f833a-363">In pratica, l'origine e il decodificatore saranno i fattori limitanti durante la riproduzione con thinning.</span><span class="sxs-lookup"><span data-stu-id="f833a-363">In practice, the source and the decoder will be the limiting factors during thinned playback.</span></span> <br/> <span data-ttu-id="f833a-364">Per la riproduzione inversa, restituire il negativo della velocità massima.</span><span class="sxs-lookup"><span data-stu-id="f833a-364">For reverse playback, return the negative of the maximum rate.</span></span><br/> |
| [<span data-ttu-id="f833a-365">**IsRateSupported**</span><span class="sxs-lookup"><span data-stu-id="f833a-365">**IsRateSupported**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported) | <span data-ttu-id="f833a-366">Restituisce **MF_E_UNSUPPORTED_RATE** se il valore assoluto di *flRate* supera la velocità di riproduzione massima del presentatore.</span><span class="sxs-lookup"><span data-stu-id="f833a-366">Return **MF_E_UNSUPPORTED_RATE** if the absolute value of *flRate* exceeds the presenter's maximum playback rate.</span></span> <span data-ttu-id="f833a-367">Calcolare la velocità di riproduzione massima come descritto per [**GetFastestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getfastestrate).</span><span class="sxs-lookup"><span data-stu-id="f833a-367">Calculate the maximum playback rate as described for [**GetFastestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getfastestrate).</span></span>                                                                                                                                                                                                                                                                                    |



 

<span data-ttu-id="f833a-368">L'esempio seguente illustra come implementare il [**metodo GetFastestRate:**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getfastestrate)</span><span class="sxs-lookup"><span data-stu-id="f833a-368">The following example shows how to implement the [**GetFastestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getfastestrate) method:</span></span>


```C++
float EVRCustomPresenter::GetMaxRate(BOOL bThin)
{
    // Non-thinned:
    // If we have a valid frame rate and a monitor refresh rate, the maximum
    // playback rate is equal to the refresh rate. Otherwise, the maximum rate
    // is unbounded (FLT_MAX).

    // Thinned: The maximum rate is unbounded.

    float   fMaxRate = FLT_MAX;
    MFRatio fps = { 0, 0 };
    UINT    MonitorRateHz = 0;

    if (!bThin && (m_pMediaType != NULL))
    {
        GetFrameRate(m_pMediaType, &fps);
        MonitorRateHz = m_pD3DPresentEngine->RefreshRate();

        if (fps.Denominator && fps.Numerator && MonitorRateHz)
        {
            // Max Rate = Refresh Rate / Frame Rate
            fMaxRate = (float)MulDiv(
                MonitorRateHz, fps.Denominator, fps.Numerator);
        }
    }

    return fMaxRate;
}
```



<span data-ttu-id="f833a-369">L'esempio precedente chiama un metodo helper, GetMaxRate, per calcolare la velocità di riproduzione in avanti massima:</span><span class="sxs-lookup"><span data-stu-id="f833a-369">The previous example calls a helper method, GetMaxRate, to calculate the maximum forward playback rate:</span></span>

<span data-ttu-id="f833a-370">L'esempio seguente illustra come implementare il [**metodo IsRateSupported:**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported)</span><span class="sxs-lookup"><span data-stu-id="f833a-370">The following example shows how to implement the [**IsRateSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported) method:</span></span>


```C++
HRESULT EVRCustomPresenter::IsRateSupported(
    BOOL bThin,
    float fRate,
    float *pfNearestSupportedRate
    )
{
    EnterCriticalSection(&m_ObjectLock);

    float   fMaxRate = 0.0f;
    float   fNearestRate = fRate;  // If we support fRate, that is the nearest.

    HRESULT hr = CheckShutdown();
    if (FAILED(hr))
    {
        goto done;
    }

    // Find the maximum forward rate.
    // Note: We have no minimum rate (that is, we support anything down to 0).
    fMaxRate = GetMaxRate(bThin);

    if (fabsf(fRate) > fMaxRate)
    {
        // The (absolute) requested rate exceeds the maximum rate.
        hr = MF_E_UNSUPPORTED_RATE;

        // The nearest supported rate is fMaxRate.
        fNearestRate = fMaxRate;
        if (fRate < 0)
        {
            // Negative for reverse playback.
            fNearestRate = -fNearestRate;
        }
    }

    // Return the nearest supported rate.
    if (pfNearestSupportedRate != NULL)
    {
        *pfNearestSupportedRate = fNearestRate;
    }

done:
    LeaveCriticalSection(&m_ObjectLock);
    return hr;
}
```



### <a name="sending-events-to-the-evr"></a><span data-ttu-id="f833a-371">Invio di eventi all'EVR</span><span class="sxs-lookup"><span data-stu-id="f833a-371">Sending Events to the EVR</span></span>

<span data-ttu-id="f833a-372">Il presentatore deve inviare una notifica all'EVR di vari eventi.</span><span class="sxs-lookup"><span data-stu-id="f833a-372">The presenter must notify the EVR of various events.</span></span> <span data-ttu-id="f833a-373">A tale scopo, usa l'interfaccia [**IMediaEventSink**](/windows/win32/api/strmif/nn-strmif-imediaeventsink) dell'EVR, ottenuta quando l'EVR chiama il metodo [**IMFTopologyServiceLookupClient::InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) del presentatore.</span><span class="sxs-lookup"><span data-stu-id="f833a-373">To do so, it uses the EVR's [**IMediaEventSink**](/windows/win32/api/strmif/nn-strmif-imediaeventsink) interface, obtained when the EVR calls the presenter's [**IMFTopologyServiceLookupClient::InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) method.</span></span> <span data-ttu-id="f833a-374">**L'interfaccia IMediaEventSink** è in origine un'interfaccia DirectShow, ma viene usata sia in DirectShow EVR che nella Media Foundation. Il codice seguente illustra come inviare un evento all'EVR:</span><span class="sxs-lookup"><span data-stu-id="f833a-374">(The **IMediaEventSink** interface is originally a DirectShow interface, but is used in both the DirectShow EVR and the Media Foundation.) The following code shows how to send an event to the EVR:</span></span>


```C++
    // NotifyEvent: Send an event to the EVR through its IMediaEventSink interface.
    void NotifyEvent(long EventCode, LONG_PTR Param1, LONG_PTR Param2)
    {
        if (m_pMediaEventSink)
        {
            m_pMediaEventSink->Notify(EventCode, Param1, Param2);
        }
    }
```



<span data-ttu-id="f833a-375">Nella tabella seguente sono elencati gli eventi inviati dal presentatore, insieme ai parametri dell'evento.</span><span class="sxs-lookup"><span data-stu-id="f833a-375">The following table lists the events that the presenter sends, along with the event parameters.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f833a-376">Event</span><span class="sxs-lookup"><span data-stu-id="f833a-376">Event</span></span></th>
<th><span data-ttu-id="f833a-377">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f833a-377">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f833a-378"><a href="/windows/desktop/DirectShow/ec-complete"><strong>EC_COMPLETE</strong></a></span><span class="sxs-lookup"><span data-stu-id="f833a-378"><a href="/windows/desktop/DirectShow/ec-complete"><strong>EC_COMPLETE</strong></a></span></span></td>
<td><span data-ttu-id="f833a-379">Il presentatore ha completato il rendering di tutti i fotogrammi dopo MFVP_MESSAGE_ENDOFSTREAM messaggio.</span><span class="sxs-lookup"><span data-stu-id="f833a-379">The presenter has finished rendering all frames after the MFVP_MESSAGE_ENDOFSTREAM message.</span></span><br/>
<ul>
<li><span data-ttu-id="f833a-380"><em>Param1:</em>HRESULT che indica lo stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="f833a-380"><em>Param1</em>: HRESULT indicating the status of the operation.</span></span></li>
<li><span data-ttu-id="f833a-381"><em>Param2:</em>non usato.</span><span class="sxs-lookup"><span data-stu-id="f833a-381"><em>Param2</em>: Not used.</span></span></li>
</ul>
<span data-ttu-id="f833a-382">Per altre informazioni, vedere <a href="#end-of-stream">Fine del flusso</a>.</span><span class="sxs-lookup"><span data-stu-id="f833a-382">For more information, see <a href="#end-of-stream">End of Stream</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f833a-383"><a href="/windows/desktop/DirectShow/ec-display-changed"><strong>EC_DISPLAY_CHANGED</strong></a></span><span class="sxs-lookup"><span data-stu-id="f833a-383"><a href="/windows/desktop/DirectShow/ec-display-changed"><strong>EC_DISPLAY_CHANGED</strong></a></span></span></td>
<td><span data-ttu-id="f833a-384">Il dispositivo Direct3D è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="f833a-384">The Direct3D device has changed.</span></span><br/>
<ul>
<li><span data-ttu-id="f833a-385"><em>Param1:</em>non usato.</span><span class="sxs-lookup"><span data-stu-id="f833a-385"><em>Param1</em>: Not used.</span></span></li>
<li><span data-ttu-id="f833a-386"><em>Param2:</em>non usato.</span><span class="sxs-lookup"><span data-stu-id="f833a-386"><em>Param2</em>: Not used.</span></span></li>
</ul>
<span data-ttu-id="f833a-387">Per altre informazioni, vedere <a href="#managing-the-direct3d-device">Gestione del dispositivo Direct3D</a>.</span><span class="sxs-lookup"><span data-stu-id="f833a-387">For more information, see <a href="#managing-the-direct3d-device">Managing the Direct3D Device</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f833a-388"><a href="/windows/desktop/DirectShow/ec-errorabort"><strong>EC_ERRORABORT</strong></a></span><span class="sxs-lookup"><span data-stu-id="f833a-388"><a href="/windows/desktop/DirectShow/ec-errorabort"><strong>EC_ERRORABORT</strong></a></span></span></td>
<td><span data-ttu-id="f833a-389">Si è verificato un errore che richiede l'arresto del flusso.</span><span class="sxs-lookup"><span data-stu-id="f833a-389">An error has occurred that requires streaming to stop.</span></span><br/>
<ul>
<li><span data-ttu-id="f833a-390"><em>Param1:</em> <strong>HRESULT</strong> che indica l'errore che si è verificato.</span><span class="sxs-lookup"><span data-stu-id="f833a-390"><em>Param1</em>: <strong>HRESULT</strong> indicating the error that occurred.</span></span></li>
<li><span data-ttu-id="f833a-391"><em>Param2:</em>non usato.</span><span class="sxs-lookup"><span data-stu-id="f833a-391"><em>Param2</em>: Not used.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f833a-392"><a href="/windows/desktop/DirectShow/ec-processing-latency"><strong>EC_PROCESSING_LATENCY</strong></a></span><span class="sxs-lookup"><span data-stu-id="f833a-392"><a href="/windows/desktop/DirectShow/ec-processing-latency"><strong>EC_PROCESSING_LATENCY</strong></a></span></span></td>
<td><span data-ttu-id="f833a-393">Specifica la quantità di tempo che il presentatore sta prendendo per eseguire il rendering di ogni frame.</span><span class="sxs-lookup"><span data-stu-id="f833a-393">Specifies the amount of time that the presenter is taking to render each frame.</span></span> <span data-ttu-id="f833a-394">Facoltativo.</span><span class="sxs-lookup"><span data-stu-id="f833a-394">(Optional.)</span></span><br/>
<ul>
<li><span data-ttu-id="f833a-395"><em>Param1:</em>puntatore a un valore <strong>LONGLONG</strong> costante che contiene la quantità di tempo per elaborare il frame, in unità da 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="f833a-395"><em>Param1</em>: Pointer to a constant <strong>LONGLONG</strong> value that contains the amount of time to process the frame, in 100-nanosecond units.</span></span></li>
<li><span data-ttu-id="f833a-396"><em>Param2:</em>non usato.</span><span class="sxs-lookup"><span data-stu-id="f833a-396"><em>Param2</em>: Not used.</span></span></li>
</ul>
<span data-ttu-id="f833a-397">Per altre informazioni, vedere <a href="#processing-output">Elaborazione dell'output</a>.</span><span class="sxs-lookup"><span data-stu-id="f833a-397">For more information, see <a href="#processing-output">Processing Output</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f833a-398"><a href="/windows/desktop/DirectShow/ec-sample-latency"><strong>EC_SAMPLE_LATENCY</strong></a></span><span class="sxs-lookup"><span data-stu-id="f833a-398"><a href="/windows/desktop/DirectShow/ec-sample-latency"><strong>EC_SAMPLE_LATENCY</strong></a></span></span></td>
<td><span data-ttu-id="f833a-399">Specifica il tempo di ritardo corrente negli esempi di rendering.</span><span class="sxs-lookup"><span data-stu-id="f833a-399">Specifies the current lag time in rendering samples.</span></span> <span data-ttu-id="f833a-400">Se il valore è positivo, gli esempi sono in ritardo rispetto alla pianificazione.</span><span class="sxs-lookup"><span data-stu-id="f833a-400">If the value is positive, samples are behind schedule.</span></span> <span data-ttu-id="f833a-401">Se il valore è negativo, i campioni sono in anticipo rispetto alla pianificazione.</span><span class="sxs-lookup"><span data-stu-id="f833a-401">If the value is negative, samples are ahead of schedule.</span></span> <span data-ttu-id="f833a-402">Facoltativo.</span><span class="sxs-lookup"><span data-stu-id="f833a-402">(Optional.)</span></span><br/>
<ul>
<li><span data-ttu-id="f833a-403"><em>Param1:</em>puntatore a un <strong>valore LONGLONG</strong> costante che contiene il tempo di ritardo, in unità di 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="f833a-403"><em>Param1</em>: Pointer to a constant <strong>LONGLONG</strong> value that contains the lag time, in 100-nanosecond units.</span></span></li>
<li><span data-ttu-id="f833a-404"><em>Param2:</em>non usato.</span><span class="sxs-lookup"><span data-stu-id="f833a-404"><em>Param2</em>: Not used.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f833a-405"><a href="/windows/desktop/DirectShow/ec-scrub-time"><strong>EC_SCRUB_TIME</strong></a></span><span class="sxs-lookup"><span data-stu-id="f833a-405"><a href="/windows/desktop/DirectShow/ec-scrub-time"><strong>EC_SCRUB_TIME</strong></a></span></span></td>
<td><span data-ttu-id="f833a-406">Inviato immediatamente dopo <strong>EC_STEP_COMPLETE</strong> se la velocità di riproduzione è pari a zero.</span><span class="sxs-lookup"><span data-stu-id="f833a-406">Sent immediately after <strong>EC_STEP_COMPLETE</strong> if the playback rate is zero.</span></span> <span data-ttu-id="f833a-407">Questo evento contiene il timestamp del frame visualizzato.</span><span class="sxs-lookup"><span data-stu-id="f833a-407">This event contains the time stamp of the frame that was displayed.</span></span><br/>
<ul>
<li><span data-ttu-id="f833a-408"><em>Param1:</em>32 bit inferiori del timestamp.</span><span class="sxs-lookup"><span data-stu-id="f833a-408"><em>Param1</em>: Lower 32 bits of the time stamp.</span></span></li>
<li><span data-ttu-id="f833a-409"><em>Param2:</em>32 bit superiori del timestamp.</span><span class="sxs-lookup"><span data-stu-id="f833a-409"><em>Param2</em>: Upper 32 bits of the time stamp.</span></span></li>
</ul>
<span data-ttu-id="f833a-410">Per altre informazioni, vedere Esecuzione di <a href="#frame-stepping">istruzioni nei frame.</a></span><span class="sxs-lookup"><span data-stu-id="f833a-410">For more information, see <a href="#frame-stepping">Frame Stepping</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f833a-411"><a href="/windows/desktop/DirectShow/ec-step-complete"><strong>EC_STEP_COMPLETE</strong></a></span><span class="sxs-lookup"><span data-stu-id="f833a-411"><a href="/windows/desktop/DirectShow/ec-step-complete"><strong>EC_STEP_COMPLETE</strong></a></span></span></td>
<td><span data-ttu-id="f833a-412">Il presentatore ha completato o annullato un passaggio del frame.</span><span class="sxs-lookup"><span data-stu-id="f833a-412">The presenter has completed or canceled a frame step.</span></span><br/>
<ul>
<li><span data-ttu-id="f833a-413"><em>Param1:</em>non usato.</span><span class="sxs-lookup"><span data-stu-id="f833a-413"><em>Param1</em>: Not used.</span></span></li>
<li><span data-ttu-id="f833a-414"><em>Param2:</em>non usato.</span><span class="sxs-lookup"><span data-stu-id="f833a-414"><em>Param2</em>: Not used.</span></span></li>
</ul>
<span data-ttu-id="f833a-415">Per altre informazioni, vedere Esecuzione di <a href="#frame-stepping">istruzioni nei frame.</a></span><span class="sxs-lookup"><span data-stu-id="f833a-415">For more information, see <a href="#frame-stepping">Frame Stepping</a>.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="f833a-416">Una versione precedente della documentazione descriveva <em>Param1 in modo non</em> corretto.</span><span class="sxs-lookup"><span data-stu-id="f833a-416">A previous version of the documentation described <em>Param1</em> incorrectly.</span></span> <span data-ttu-id="f833a-417">Questo parametro non viene usato per questo evento.</span><span class="sxs-lookup"><span data-stu-id="f833a-417">This parameter is not used for this event.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="negotiating-formats"></a><span data-ttu-id="f833a-418">Formati di negoziazione</span><span class="sxs-lookup"><span data-stu-id="f833a-418">Negotiating Formats</span></span>

<span data-ttu-id="f833a-419">Ogni volta che il presentatore riceve **un messaggio MFVP_MESSAGE_INVALIDATEMEDIATYPE** da EVR, deve impostare il formato di output nel mixer, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="f833a-419">Whenever the presenter receives an **MFVP_MESSAGE_INVALIDATEMEDIATYPE** message from the EVR, it must set the output format on the mixer, as follows:</span></span>

1.  <span data-ttu-id="f833a-420">Chiamare [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) sul mixer per ottenere un possibile tipo di output.</span><span class="sxs-lookup"><span data-stu-id="f833a-420">Call [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) on the mixer to get a possible output type.</span></span> <span data-ttu-id="f833a-421">Questo tipo descrive un formato che il mixer può produrre in base ai flussi di input e alle funzionalità di elaborazione video del dispositivo grafico.</span><span class="sxs-lookup"><span data-stu-id="f833a-421">This type describes a format that the mixer can produce given the input streams and the video processing capabilities of the graphics device.</span></span>
2.  <span data-ttu-id="f833a-422">Controllare se il presentatore può usare questo tipo di supporto come formato di rendering.</span><span class="sxs-lookup"><span data-stu-id="f833a-422">Check whether the presenter can use this media type as its rendering format.</span></span> <span data-ttu-id="f833a-423">Ecco alcuni aspetti da controllare, anche se l'implementazione potrebbe avere requisiti specifici:</span><span class="sxs-lookup"><span data-stu-id="f833a-423">Here are some things to check, although your implementation might have its own requirements:</span></span>

    -   <span data-ttu-id="f833a-424">Il video deve essere non compresso.</span><span class="sxs-lookup"><span data-stu-id="f833a-424">The video must be uncompressed.</span></span>
    -   <span data-ttu-id="f833a-425">Il video deve avere solo fotogrammi progressivi.</span><span class="sxs-lookup"><span data-stu-id="f833a-425">The video must have progressive frames only.</span></span> <span data-ttu-id="f833a-426">Verificare che [**l'attributo MF_MT_INTERLACE_MODE**](mf-mt-interlace-mode-attribute.md) sia **uguale MFVideoInterlace_Progressive**.</span><span class="sxs-lookup"><span data-stu-id="f833a-426">Check that the [**MF_MT_INTERLACE_MODE**](mf-mt-interlace-mode-attribute.md) attribute equals **MFVideoInterlace_Progressive**.</span></span>
    -   <span data-ttu-id="f833a-427">Il formato deve essere compatibile con il dispositivo Direct3D.</span><span class="sxs-lookup"><span data-stu-id="f833a-427">The format must be compatible with the Direct3D device.</span></span>

    <span data-ttu-id="f833a-428">Se il tipo non è accettabile, tornare al passaggio 1 e ottenere il tipo proposto successivo del mixer.</span><span class="sxs-lookup"><span data-stu-id="f833a-428">If the type is not acceptable, return to step 1 and get the mixer's next proposed type.</span></span>

3.  <span data-ttu-id="f833a-429">Creare un nuovo tipo di supporto che sia un clone del tipo originale e quindi modificare gli attributi seguenti:</span><span class="sxs-lookup"><span data-stu-id="f833a-429">Create a new media type that is a clone of the original type and then change the following attributes:</span></span>

    -   <span data-ttu-id="f833a-430">Impostare [](mf-mt-frame-size-attribute.md) l MF_MT_FRAME_SIZE attribuita uguale alla larghezza e all'altezza desiderate per le superfici Direct3D da allocare.</span><span class="sxs-lookup"><span data-stu-id="f833a-430">Set the [**MF_MT_FRAME_SIZE**](mf-mt-frame-size-attribute.md) attribute equal to the width and height that you want for the Direct3D surfaces you will allocate.</span></span>
    -   <span data-ttu-id="f833a-431">Impostare [**l'MF_MT_PAN_SCAN_ENABLED**](mf-mt-pan-scan-enabled-attribute.md) su **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="f833a-431">Set the [**MF_MT_PAN_SCAN_ENABLED**](mf-mt-pan-scan-enabled-attribute.md) attribute to **FALSE**.</span></span>
    -   <span data-ttu-id="f833a-432">Impostare [](mf-mt-pixel-aspect-ratio-attribute.md) l MF_MT_PIXEL_ASPECT_RATIO attribuita del valore pari al valore PAR della visualizzazione (in genere 1:1).</span><span class="sxs-lookup"><span data-stu-id="f833a-432">Set the [**MF_MT_PIXEL_ASPECT_RATIO**](mf-mt-pixel-aspect-ratio-attribute.md) attribute equal to the PAR of the display (typically 1:1).</span></span>
    -   <span data-ttu-id="f833a-433">Impostare l'apertura geometrica [**(MF_MT_GEOMETRIC_APERTURE**](mf-mt-geometric-aperture-attribute.md) attributo ) su un rettangolo all'interno della superficie Direct3D.</span><span class="sxs-lookup"><span data-stu-id="f833a-433">Set the geometric aperture ([**MF_MT_GEOMETRIC_APERTURE**](mf-mt-geometric-aperture-attribute.md) attribute) equal to a rectangle within the Direct3D surface.</span></span> <span data-ttu-id="f833a-434">Quando il mixer genera un frame di output, esegue il blittang dell'immagine di origine in questo rettangolo.</span><span class="sxs-lookup"><span data-stu-id="f833a-434">When the mixer generates an output frame, it blits the source image onto this rectangle.</span></span> <span data-ttu-id="f833a-435">L'apertura geometrica può essere grande quanto la superficie o può essere un subrectangle all'interno della superficie.</span><span class="sxs-lookup"><span data-stu-id="f833a-435">The geometric aperture can be as large as the surface, or it can be a subrectangle within the surface.</span></span> <span data-ttu-id="f833a-436">Per altre informazioni, vedere [Rettangoli di origine e destinazione.](#source-and-destination-rectangles)</span><span class="sxs-lookup"><span data-stu-id="f833a-436">For more information, see [Source and Destination Rectangles](#source-and-destination-rectangles).</span></span>

4.  <span data-ttu-id="f833a-437">Per verificare se il mixer accetterà il tipo di output modificato, chiamare [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) con il flag **MFT_SET_TYPE_TEST_ONLY.**</span><span class="sxs-lookup"><span data-stu-id="f833a-437">To test whether the mixer will accept the modified output type, call [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) with the **MFT_SET_TYPE_TEST_ONLY** flag.</span></span> <span data-ttu-id="f833a-438">Se il mixer rifiuta il tipo, tornare al passaggio 1 e ottenere il tipo successivo.</span><span class="sxs-lookup"><span data-stu-id="f833a-438">If the mixer rejects the type, go back to step 1 and get the next type.</span></span>
5.  <span data-ttu-id="f833a-439">Allocare un pool di superfici Direct3D, come descritto in [Allocazione di superfici Direct3D.](#allocating-direct3d-surfaces)</span><span class="sxs-lookup"><span data-stu-id="f833a-439">Allocate a pool of Direct3D surfaces, as described in [Allocating Direct3D Surfaces](#allocating-direct3d-surfaces).</span></span> <span data-ttu-id="f833a-440">Il mixer userà queste superfici quando disegna i fotogrammi video compositi.</span><span class="sxs-lookup"><span data-stu-id="f833a-440">The mixer will use these surfaces when it draws the composited video frames.</span></span>
6.  <span data-ttu-id="f833a-441">Impostare il tipo di output nel mixer chiamando [**SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) senza flag.</span><span class="sxs-lookup"><span data-stu-id="f833a-441">Set the output type on the mixer by calling [**SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) with no flags.</span></span> <span data-ttu-id="f833a-442">Se la prima chiamata a **SetOutputType** ha avuto esito positivo nel passaggio 4, il metodo dovrebbe riuscire di nuovo.</span><span class="sxs-lookup"><span data-stu-id="f833a-442">If the first call to **SetOutputType** succeeded in step 4, the method should succeed again.</span></span>

<span data-ttu-id="f833a-443">Se il mixer esaure i tipi, il [**metodo GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) **restituisce MF_E_NO_MORE_TYPES**.</span><span class="sxs-lookup"><span data-stu-id="f833a-443">If the mixer runs out of types, the [**GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) method returns **MF_E_NO_MORE_TYPES**.</span></span> <span data-ttu-id="f833a-444">Se il presentatore non riesce a trovare un tipo di output appropriato per il mixer, non è possibile eseguire il rendering del flusso.</span><span class="sxs-lookup"><span data-stu-id="f833a-444">If the presenter cannot find a suitable output type for the mixer, the stream cannot be rendered.</span></span> <span data-ttu-id="f833a-445">In tal caso, DirectShow o Media Foundation provare un altro formato di flusso.</span><span class="sxs-lookup"><span data-stu-id="f833a-445">In that case, DirectShow or Media Foundation might try another stream format.</span></span> <span data-ttu-id="f833a-446">Pertanto, il presentatore potrebbe ricevere MFVP_MESSAGE_INVALIDATEMEDIATYPE **messaggi** in una riga fino a quando non viene trovato un tipo valido.</span><span class="sxs-lookup"><span data-stu-id="f833a-446">Therefore, the presenter might receive several **MFVP_MESSAGE_INVALIDATEMEDIATYPE** messages in a row until a valid type is found.</span></span>

<span data-ttu-id="f833a-447">Il mixer crea automaticamente una letterbox del video, prendendo in considerazione le proporzioni pixel (PAR) dell'origine e della destinazione.</span><span class="sxs-lookup"><span data-stu-id="f833a-447">The mixer automatically letterboxes the video, taking into account the pixel aspect ratio (PAR) of the source and destination.</span></span> <span data-ttu-id="f833a-448">Per ottenere risultati ottimali, la larghezza e l'altezza della superficie e l'apertura geometrica devono essere uguali alle dimensioni effettive in cui si vuole che il video venga visualizzato sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="f833a-448">For best results, the surface width and height and the geometric aperture should be equal to the actual size that you want the video to appear on the display.</span></span> <span data-ttu-id="f833a-449">L'immagine seguente illustra questo processo.</span><span class="sxs-lookup"><span data-stu-id="f833a-449">The following image illustrates this process.</span></span>

![diagramma che mostra un fram composito che porta a una superficie direct3d, che porta a una finestra](images/b746edca-8830-4c88-aa59-0067b020d4af.gif)

<span data-ttu-id="f833a-451">Il codice seguente illustra la struttura del processo.</span><span class="sxs-lookup"><span data-stu-id="f833a-451">The following code shows the outline of the process.</span></span> <span data-ttu-id="f833a-452">Alcuni dei passaggi vengono inseriti nelle funzioni helper, i cui dettagli esatti dipendono dai requisiti del presentatore.</span><span class="sxs-lookup"><span data-stu-id="f833a-452">Some of the steps are placed in helper functions, the exact details of which will depend on the requirements of your presenter.</span></span>


```C++
HRESULT EVRCustomPresenter::RenegotiateMediaType()
{
    HRESULT hr = S_OK;
    BOOL bFoundMediaType = FALSE;

    IMFMediaType *pMixerType = NULL;
    IMFMediaType *pOptimalType = NULL;
    IMFVideoMediaType *pVideoType = NULL;

    if (!m_pMixer)
    {
        return MF_E_INVALIDREQUEST;
    }

    // Loop through all of the mixer's proposed output types.
    DWORD iTypeIndex = 0;
    while (!bFoundMediaType && (hr != MF_E_NO_MORE_TYPES))
    {
        SafeRelease(&pMixerType);
        SafeRelease(&pOptimalType);

        // Step 1. Get the next media type supported by mixer.
        hr = m_pMixer->GetOutputAvailableType(0, iTypeIndex++, &pMixerType);
        if (FAILED(hr))
        {
            break;
        }

        // From now on, if anything in this loop fails, try the next type,
        // until we succeed or the mixer runs out of types.

        // Step 2. Check if we support this media type.
        if (SUCCEEDED(hr))
        {
            // Note: None of the modifications that we make later in CreateOptimalVideoType
            // will affect the suitability of the type, at least for us. (Possibly for the mixer.)
            hr = IsMediaTypeSupported(pMixerType);
        }

        // Step 3. Adjust the mixer's type to match our requirements.
        if (SUCCEEDED(hr))
        {
            hr = CreateOptimalVideoType(pMixerType, &pOptimalType);
        }

        // Step 4. Check if the mixer will accept this media type.
        if (SUCCEEDED(hr))
        {
            hr = m_pMixer->SetOutputType(0, pOptimalType, MFT_SET_TYPE_TEST_ONLY);
        }

        // Step 5. Try to set the media type on ourselves.
        if (SUCCEEDED(hr))
        {
            hr = SetMediaType(pOptimalType);
        }

        // Step 6. Set output media type on mixer.
        if (SUCCEEDED(hr))
        {
            hr = m_pMixer->SetOutputType(0, pOptimalType, 0);

            assert(SUCCEEDED(hr)); // This should succeed unless the MFT lied in the previous call.

            // If something went wrong, clear the media type.
            if (FAILED(hr))
            {
                SetMediaType(NULL);
            }
        }

        if (SUCCEEDED(hr))
        {
            bFoundMediaType = TRUE;
        }
    }

    SafeRelease(&pMixerType);
    SafeRelease(&pOptimalType);
    SafeRelease(&pVideoType);

    return hr;
}
```



<span data-ttu-id="f833a-453">Per altre informazioni sui tipi di file multimediali video, vedere [Tipi di file multimediali video.](video-media-types.md)</span><span class="sxs-lookup"><span data-stu-id="f833a-453">For more information about video media types, see [Video Media Types](video-media-types.md).</span></span>

## <a name="managing-the-direct3d-device"></a><span data-ttu-id="f833a-454">Gestione del dispositivo Direct3D</span><span class="sxs-lookup"><span data-stu-id="f833a-454">Managing the Direct3D Device</span></span>

<span data-ttu-id="f833a-455">Il presentatore crea il dispositivo Direct3D e gestisce eventuali perdite di dispositivi durante lo streaming.</span><span class="sxs-lookup"><span data-stu-id="f833a-455">The presenter creates the Direct3D device and handles any device loss during streaming.</span></span> <span data-ttu-id="f833a-456">Il presentatore ospita anche gestione dispositivi Direct3D, che consente ad altri componenti di usare lo stesso dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f833a-456">The presenter also hosts the Direct3D device manager, which provides a way for other components to use the same device.</span></span> <span data-ttu-id="f833a-457">Ad esempio, il mixer usa il dispositivo Direct3D per combinare substream, delnterlace ed eseguire regolazioni del colore.</span><span class="sxs-lookup"><span data-stu-id="f833a-457">For example, the mixer uses the Direct3D device to mix substreams, deinterlace, and perform color adjustments.</span></span> <span data-ttu-id="f833a-458">I decodificatori possono usare il dispositivo Direct3D per la decodifica con accelerazione video.</span><span class="sxs-lookup"><span data-stu-id="f833a-458">Decoders can use the Direct3D device for video-accelerated decoding.</span></span> <span data-ttu-id="f833a-459">Per altre informazioni sull'accelerazione video, vedere [Accelerazione video DirectX 2.0.](directx-video-acceleration-2-0.md)</span><span class="sxs-lookup"><span data-stu-id="f833a-459">(For more information about video acceleration, see [DirectX Video Acceleration 2.0](directx-video-acceleration-2-0.md).)</span></span>

<span data-ttu-id="f833a-460">Per configurare il dispositivo Direct3D, seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="f833a-460">To set up the Direct3D device, perform the following steps:</span></span>

1.  <span data-ttu-id="f833a-461">Creare l'oggetto Direct3D chiamando **Direct3DCreate9** **o Direct3DCreate9Ex.**</span><span class="sxs-lookup"><span data-stu-id="f833a-461">Create the Direct3D object by calling **Direct3DCreate9** or **Direct3DCreate9Ex**.</span></span>
2.  <span data-ttu-id="f833a-462">Creare il dispositivo chiamando **IDirect3D9::CreateDevice** o **IDirect3D9Ex::CreateDevice**.</span><span class="sxs-lookup"><span data-stu-id="f833a-462">Create the device by calling **IDirect3D9::CreateDevice** or **IDirect3D9Ex::CreateDevice**.</span></span>
3.  <span data-ttu-id="f833a-463">Creare gestione dispositivi chiamando [**DXVA2CreateDirect3DDeviceManager9.**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createdirect3ddevicemanager9)</span><span class="sxs-lookup"><span data-stu-id="f833a-463">Create the device manager by calling [**DXVA2CreateDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createdirect3ddevicemanager9).</span></span>
4.  <span data-ttu-id="f833a-464">Impostare il dispositivo in Gestione dispositivi chiamando [**IDirect3DDeviceManager9::ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice).</span><span class="sxs-lookup"><span data-stu-id="f833a-464">Set the device on the device manager by calling [**IDirect3DDeviceManager9::ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice).</span></span>

<span data-ttu-id="f833a-465">Se un altro componente della pipeline richiede gestione dispositivi, chiama [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) in EVR, specificando MR_VIDEO_ACCELERATION_SERVICE **per** il GUID del servizio.</span><span class="sxs-lookup"><span data-stu-id="f833a-465">If another pipeline component needs the device manager, it calls [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) on the EVR, specifying **MR_VIDEO_ACCELERATION_SERVICE** for the service GUID.</span></span> <span data-ttu-id="f833a-466">EVR passa la richiesta al presentatore.</span><span class="sxs-lookup"><span data-stu-id="f833a-466">The EVR passes the request to the presenter.</span></span> <span data-ttu-id="f833a-467">Dopo che l'oggetto ottiene il puntatore [**IDirect3DDeviceManager9,**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) può ottenere un handle per il dispositivo chiamando [**IDirect3DDeviceManager9::OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle).</span><span class="sxs-lookup"><span data-stu-id="f833a-467">After the object gets the [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) pointer, it can get a handle to the device by calling [**IDirect3DDeviceManager9::OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle).</span></span> <span data-ttu-id="f833a-468">Quando l'oggetto deve usare il dispositivo, passa l'handle del dispositivo al metodo [**IDirect3DDeviceManager9::LockDevice,**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) che restituisce un **puntatore IDirect3DDevice9.**</span><span class="sxs-lookup"><span data-stu-id="f833a-468">When the object needs to use the device, it passes the device handle to the [**IDirect3DDeviceManager9::LockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) method, which returns an **IDirect3DDevice9** pointer.</span></span>

<span data-ttu-id="f833a-469">Dopo aver creato il dispositivo, se il presentatore elimina il dispositivo e ne crea uno nuovo, il presentatore deve chiamare [**nuovamente ResetDevice.**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice)</span><span class="sxs-lookup"><span data-stu-id="f833a-469">After the device is created, if the presenter destroys the device and creates a new one, the presenter must call [**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) again.</span></span> <span data-ttu-id="f833a-470">Il **metodo ResetDevice** invalida tutti gli handle di dispositivo esistenti, causando la restituzione di [**LockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) **DXVA2_E_NEW_VIDEO_DEVICE**.</span><span class="sxs-lookup"><span data-stu-id="f833a-470">The **ResetDevice** method invalidates any existing device handles, which causes [**LockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) to return **DXVA2_E_NEW_VIDEO_DEVICE**.</span></span> <span data-ttu-id="f833a-471">Questo codice di errore segnala ad altri oggetti che usano il dispositivo di aprire un nuovo handle di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f833a-471">This error code signals to other objects using the device that they should open a new device handle.</span></span> <span data-ttu-id="f833a-472">Per altre informazioni sull'uso di Gestione dispositivi, vedere [Gestione dispositivi Direct3D.](direct3d-device-manager.md)</span><span class="sxs-lookup"><span data-stu-id="f833a-472">For more information about using the device manager, see [Direct3D Device Manager](direct3d-device-manager.md).</span></span>

<span data-ttu-id="f833a-473">Il presentatore può creare il dispositivo in modalità finestra o in modalità esclusiva a schermo intero.</span><span class="sxs-lookup"><span data-stu-id="f833a-473">The presenter can create the device in windowed mode or full-screen exclusive mode.</span></span> <span data-ttu-id="f833a-474">Per la modalità finestra, è necessario fornire all'applicazione un modo per specificare la finestra video.</span><span class="sxs-lookup"><span data-stu-id="f833a-474">For windowed mode, you should provide a way for the application to specify the video window.</span></span> <span data-ttu-id="f833a-475">Il presentatore standard implementa il [**metodo IMFVideoDisplayControl::SetVideoWindow**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow) a questo scopo.</span><span class="sxs-lookup"><span data-stu-id="f833a-475">The standard presenter implements the [**IMFVideoDisplayControl::SetVideoWindow**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow) method for this purpose.</span></span> <span data-ttu-id="f833a-476">È necessario creare il dispositivo quando il presentatore viene creato per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="f833a-476">You must create the device when the presenter is first created.</span></span> <span data-ttu-id="f833a-477">In genere, al momento non si conoscono tutti i parametri del dispositivo, ad esempio la finestra o il formato del buffer nascosto.</span><span class="sxs-lookup"><span data-stu-id="f833a-477">Typically, you won't know all of the device parameters at this time, such as the window or the back buffer format.</span></span> <span data-ttu-id="f833a-478">È possibile creare un dispositivo temporaneo e sostituirlo in \#&; ricordarsi di chiamare [**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) in Gestione dispositivi.</span><span class="sxs-lookup"><span data-stu-id="f833a-478">You can create a temporary device and replace it later&\#;just remember to call [**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) on the device manager.</span></span>

<span data-ttu-id="f833a-479">Se si crea un nuovo dispositivo o si chiama **IDirect3DDevice9::Reset** o **IDirect3DDevice9Ex::ResetEx** in un dispositivo esistente, inviare un evento [**EC_DISPLAY_CHANGED**](../directshow/ec-display-changed.md) all'EVR.</span><span class="sxs-lookup"><span data-stu-id="f833a-479">If you create a new device, or if you call **IDirect3DDevice9::Reset** or **IDirect3DDevice9Ex::ResetEx** on an existing device, send an [**EC_DISPLAY_CHANGED**](../directshow/ec-display-changed.md) event to the EVR.</span></span> <span data-ttu-id="f833a-480">Questo evento notifica all'EVR di rinegoziare il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="f833a-480">This event notifies the EVR to renegotiate the media type.</span></span> <span data-ttu-id="f833a-481">L'EVR ignora i parametri dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="f833a-481">The EVR ignores the event parameters for this event.</span></span>

### <a name="allocating-direct3d-surfaces"></a><span data-ttu-id="f833a-482">Allocazione di superfici Direct3D</span><span class="sxs-lookup"><span data-stu-id="f833a-482">Allocating Direct3D Surfaces</span></span>

<span data-ttu-id="f833a-483">Dopo che il presentatore ha impostato il tipo di supporto, può allocare le superfici Direct3D, che verranno usate dal mixer per scrivere i fotogrammi video.</span><span class="sxs-lookup"><span data-stu-id="f833a-483">After the presenter sets the media type, it can allocate the Direct3D surfaces, which the mixer will use to write the video frames.</span></span> <span data-ttu-id="f833a-484">La superficie deve corrispondere al tipo di supporto del presentatore:</span><span class="sxs-lookup"><span data-stu-id="f833a-484">The surface must match the presenter's media type:</span></span>

-   <span data-ttu-id="f833a-485">Il formato della superficie deve corrispondere al sottotipo multimediale.</span><span class="sxs-lookup"><span data-stu-id="f833a-485">The surface format must match the media subtype.</span></span> <span data-ttu-id="f833a-486">Ad esempio, se il sottotipo **è MFVideoFormat_RGB24**, il formato della superficie deve **essere D3DFMT_X8R8G8B8**.</span><span class="sxs-lookup"><span data-stu-id="f833a-486">For example, if the subtype is **MFVideoFormat_RGB24**, the surface format must be **D3DFMT_X8R8G8B8**.</span></span> <span data-ttu-id="f833a-487">Per altre informazioni sui sottotipi e sui formati Direct3D, vedere [GUID di sottotipo video.](video-subtype-guids.md)</span><span class="sxs-lookup"><span data-stu-id="f833a-487">For more information about subtypes and Direct3D formats, see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>
-   <span data-ttu-id="f833a-488">La larghezza e l'altezza della superficie devono corrispondere alle dimensioni specificate [**nell'attributo MF_MT_FRAME_SIZE**](mf-mt-frame-size-attribute.md) del tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="f833a-488">The surface width and height must match the dimensions given in the [**MF_MT_FRAME_SIZE**](mf-mt-frame-size-attribute.md) attribute of the media type.</span></span>

<span data-ttu-id="f833a-489">Il modo consigliato per allocare le superfici dipende dal fatto che il presentatore venga eseguito in modalità finestra o a schermo intero.</span><span class="sxs-lookup"><span data-stu-id="f833a-489">The recommended way to allocate surfaces depends on whether the presenter runs windowed or full-screen.</span></span>

<span data-ttu-id="f833a-490">Se il dispositivo Direct3D è in finestra, è possibile creare diverse catene di scambio, ognuna con un singolo buffer nascosto.</span><span class="sxs-lookup"><span data-stu-id="f833a-490">If the Direct3D device is windowed, you can create several swap chains, each with a single back buffer.</span></span> <span data-ttu-id="f833a-491">Con questo approccio, è possibile presentare ogni superficie in modo indipendente, perché la presentazione di una catena di scambio non interferisce con le altre catene di scambio.</span><span class="sxs-lookup"><span data-stu-id="f833a-491">Using this approach, you can present each surface independently, because presenting one swap chain will not interfere with the other swap chains.</span></span> <span data-ttu-id="f833a-492">Il mixer può scrivere dati su una superficie mentre un'altra superficie è pianificata per la presentazione.</span><span class="sxs-lookup"><span data-stu-id="f833a-492">The mixer can write data to a surface while another surface is scheduled for presentation.</span></span>

<span data-ttu-id="f833a-493">Prima di tutto, decidere il numero di catene di scambio da creare.</span><span class="sxs-lookup"><span data-stu-id="f833a-493">First, decide how many swap chains to create.</span></span> <span data-ttu-id="f833a-494">È consigliabile almeno tre.</span><span class="sxs-lookup"><span data-stu-id="f833a-494">A minimum of three is recommended.</span></span> <span data-ttu-id="f833a-495">Per ogni catena di scambio, eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="f833a-495">For each swap chain, do the following:</span></span>

1.  <span data-ttu-id="f833a-496">Chiamare **IDirect3DDevice9::CreateAdditionalSwapChain** per creare la catena di scambio.</span><span class="sxs-lookup"><span data-stu-id="f833a-496">Call **IDirect3DDevice9::CreateAdditionalSwapChain** to create the swap chain.</span></span>
2.  <span data-ttu-id="f833a-497">Chiamare **IDirect3DSwapChain9::GetBackBuffer** per ottenere un puntatore alla superficie del buffer nascosto della catena di scambio.</span><span class="sxs-lookup"><span data-stu-id="f833a-497">Call **IDirect3DSwapChain9::GetBackBuffer** to get a pointer to the swap chain's back buffer surface.</span></span>
3.  <span data-ttu-id="f833a-498">Chiamare [**MFCreateVideoSampleFromSurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) e passare un puntatore alla superficie.</span><span class="sxs-lookup"><span data-stu-id="f833a-498">Call [**MFCreateVideoSampleFromSurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) and pass in a pointer to the surface.</span></span> <span data-ttu-id="f833a-499">Questa funzione restituisce un puntatore a un oggetto video di esempio.</span><span class="sxs-lookup"><span data-stu-id="f833a-499">This function returns a pointer to a video sample object.</span></span> <span data-ttu-id="f833a-500">L'oggetto video di esempio implementa l'interfaccia [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) e il presentatore usa questa interfaccia per distribuire la superficie al mixer quando il presentatore chiama il metodo [**IMFTransform::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) del mixer.</span><span class="sxs-lookup"><span data-stu-id="f833a-500">The video sample object implements the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface, and the presenter uses this interface to deliver the surface to the mixer when the presenter calls the mixer's [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) method.</span></span> <span data-ttu-id="f833a-501">Per altre informazioni sull'oggetto di esempio video, vedere [Esempi video](video-samples.md).</span><span class="sxs-lookup"><span data-stu-id="f833a-501">For more information about the video sample object, see [Video Samples](video-samples.md).</span></span>
4.  <span data-ttu-id="f833a-502">Archiviare il [**puntatore IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) in una coda.</span><span class="sxs-lookup"><span data-stu-id="f833a-502">Store the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) pointer in a queue.</span></span> <span data-ttu-id="f833a-503">Il presentatore estrarrà gli esempi da questa coda durante l'elaborazione, come descritto in [Output di elaborazione](#processing-output).</span><span class="sxs-lookup"><span data-stu-id="f833a-503">The presenter will pull samples from this queue during processing as described in [Processing Output](#processing-output).</span></span>
5.  <span data-ttu-id="f833a-504">Mantenere un riferimento al **puntatore IDirect3DSwapChain9** in modo che la catena di scambio non sia rilasciata.</span><span class="sxs-lookup"><span data-stu-id="f833a-504">Keep a reference to the **IDirect3DSwapChain9** pointer so the swap chain is not released.</span></span>

<span data-ttu-id="f833a-505">In modalità esclusiva a schermo intero, il dispositivo non può avere più di una catena di scambio.</span><span class="sxs-lookup"><span data-stu-id="f833a-505">In full-screen exclusive mode, the device cannot have more than one swap chain.</span></span> <span data-ttu-id="f833a-506">Questa catena di scambio viene creata in modo implicito quando si crea il dispositivo a schermo intero.</span><span class="sxs-lookup"><span data-stu-id="f833a-506">This swap chain is created implicitly when you create the full-screen device.</span></span> <span data-ttu-id="f833a-507">La catena di scambio può avere più buffer nascosto.</span><span class="sxs-lookup"><span data-stu-id="f833a-507">The swap chain can have more than one back buffer.</span></span> <span data-ttu-id="f833a-508">Sfortunatamente, tuttavia, se si presenta un buffer nascosto mentre si scrive in un altro buffer nascosto nella stessa catena di scambio, non esiste un modo semplice per coordinare le due operazioni.</span><span class="sxs-lookup"><span data-stu-id="f833a-508">Unfortunately, however, if you present one back buffer while you write to another back buffer in the same swap chain, there is no easy way to coordinate the two operations.</span></span> <span data-ttu-id="f833a-509">Ciò è dovuto al modo in cui Direct3D implementa il capovolgimento della superficie.</span><span class="sxs-lookup"><span data-stu-id="f833a-509">This is because of the way Direct3D implements surface flipping.</span></span> <span data-ttu-id="f833a-510">Quando si chiama Present, il driver di grafica aggiorna i puntatori di superficie nella memoria grafica.</span><span class="sxs-lookup"><span data-stu-id="f833a-510">When you call Present, the graphics driver updates the surface pointers in graphics memory.</span></span> <span data-ttu-id="f833a-511">Se si tengono puntatori **IDirect3DSurface9** quando si chiama **Present**, questi  puntino a buffer diversi dopo la chiamata Present.</span><span class="sxs-lookup"><span data-stu-id="f833a-511">If you are holding any **IDirect3DSurface9** pointers when you call **Present**, they will point to different buffers after the **Present** call returns.</span></span>

<span data-ttu-id="f833a-512">L'opzione più semplice è creare un esempio video per la catena di scambio.</span><span class="sxs-lookup"><span data-stu-id="f833a-512">The simplest option is to create one video sample for the swap chain.</span></span> <span data-ttu-id="f833a-513">Se si sceglie questa opzione, seguire gli stessi passaggi indicati per la modalità a finestre.</span><span class="sxs-lookup"><span data-stu-id="f833a-513">If you choose this option, follow the same steps given for windowed mode.</span></span> <span data-ttu-id="f833a-514">L'unica differenza è che la coda di esempio contiene un singolo esempio video.</span><span class="sxs-lookup"><span data-stu-id="f833a-514">The only difference is that the sample queue contains a single video sample.</span></span> <span data-ttu-id="f833a-515">Un'altra opzione è creare superfici fuori schermo e quindi eseguire il blit nel buffer nascosto.</span><span class="sxs-lookup"><span data-stu-id="f833a-515">Another option is to create offscreen surfaces and then blit them to the back buffer.</span></span> <span data-ttu-id="f833a-516">Le superfici create devono supportare il metodo [**IDirectXVideoProcessor::VideoProcessBlt,**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) che il mixer usa per combinare i fotogrammi di output.</span><span class="sxs-lookup"><span data-stu-id="f833a-516">The surfaces that you create must support the [**IDirectXVideoProcessor::VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) method, which the mixer uses to composite the output frames.</span></span>

### <a name="tracking-samples"></a><span data-ttu-id="f833a-517">Esempi di rilevamento</span><span class="sxs-lookup"><span data-stu-id="f833a-517">Tracking Samples</span></span>

<span data-ttu-id="f833a-518">Quando il presentatore alloca per la prima volta gli esempi video, li inserisce in una coda.</span><span class="sxs-lookup"><span data-stu-id="f833a-518">When the presenter first allocates the video samples, it places them in a queue.</span></span> <span data-ttu-id="f833a-519">Il presentatore attinge da questa coda ogni volta che deve ottenere un nuovo frame dal mixer.</span><span class="sxs-lookup"><span data-stu-id="f833a-519">The presenter draws from this queue whenever it needs to get a new frame from the mixer.</span></span> <span data-ttu-id="f833a-520">Dopo che il mixer ha restituito il frame, il presentatore sposta l'esempio in una seconda coda.</span><span class="sxs-lookup"><span data-stu-id="f833a-520">After the mixer outputs the frame, the presenter moves the sample into a second queue.</span></span> <span data-ttu-id="f833a-521">La seconda coda è per gli esempi in attesa degli orari di presentazione pianificati.</span><span class="sxs-lookup"><span data-stu-id="f833a-521">The second queue is for samples that are waiting for their scheduled presentation times.</span></span>

<span data-ttu-id="f833a-522">Per tenere traccia più facilmente dello stato di ogni esempio, l'oggetto di esempio video implementa [**l'interfaccia IMFTrackedSample.**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample)</span><span class="sxs-lookup"><span data-stu-id="f833a-522">To make it easier to track the status of each sample, the video sample object implements the [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) interface.</span></span> <span data-ttu-id="f833a-523">È possibile usare questa interfaccia come segue:</span><span class="sxs-lookup"><span data-stu-id="f833a-523">You can use this interface as follows:</span></span>

1.  <span data-ttu-id="f833a-524">Implementare [**l'interfaccia IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) nel presentatore.</span><span class="sxs-lookup"><span data-stu-id="f833a-524">Implement the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface in your presenter.</span></span>
2.  <span data-ttu-id="f833a-525">Prima di inserire un esempio nella coda pianificata, eseguire una query sull'oggetto di esempio video per [**l'interfaccia IMFTrackedSample.**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample)</span><span class="sxs-lookup"><span data-stu-id="f833a-525">Before you place a sample in the scheduled queue, query the video sample object for the [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) interface.</span></span>

3.  <span data-ttu-id="f833a-526">Chiamare [**IMFTrackedSample::SetAllocator**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) con un puntatore all'interfaccia di callback.</span><span class="sxs-lookup"><span data-stu-id="f833a-526">Call [**IMFTrackedSample::SetAllocator**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) with a pointer to your callback interface.</span></span>
4.  <span data-ttu-id="f833a-527">Quando l'esempio è pronto per la presentazione, rimuoverlo dalla coda pianificata, presentarlo e rilasciare tutti i riferimenti all'esempio.</span><span class="sxs-lookup"><span data-stu-id="f833a-527">When the sample is ready for presentation, remove it from the scheduled queue, present it, and release all references to the sample.</span></span>
5.  <span data-ttu-id="f833a-528">L'esempio richiama il callback.</span><span class="sxs-lookup"><span data-stu-id="f833a-528">The sample invokes the callback.</span></span> <span data-ttu-id="f833a-529">L'oggetto di esempio non viene eliminato in questo caso perché contiene un conteggio dei riferimenti su se stesso fino a quando non viene richiamato il callback.</span><span class="sxs-lookup"><span data-stu-id="f833a-529">(The sample object is not deleted in this case because it holds a reference count on itself until the callback is invoked.)</span></span>
6.  <span data-ttu-id="f833a-530">All'interno del callback, restituire l'esempio alla coda disponibile.</span><span class="sxs-lookup"><span data-stu-id="f833a-530">Inside the callback, return the sample to the available queue.</span></span>

<span data-ttu-id="f833a-531">Non è necessario un presentatore per usare [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) per tenere traccia degli esempi. è possibile implementare qualsiasi tecnica più adatta alla progettazione.</span><span class="sxs-lookup"><span data-stu-id="f833a-531">A presenter is not required to use [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) to track samples; you can implement any technique that works best for your design.</span></span> <span data-ttu-id="f833a-532">Uno dei vantaggi di **IMFTrackedSample** è che è possibile spostare le funzioni di pianificazione e rendering del presentatore in oggetti helper e questi oggetti non necessitano di alcun meccanismo speciale per la chiamata al presentatore quando rilasciano esempi video perché l'oggetto di esempio fornisce tale meccanismo.</span><span class="sxs-lookup"><span data-stu-id="f833a-532">One advantage of **IMFTrackedSample** is that you can move the presenter's scheduling and rendering functions into helper objects, and these objects do not need any special mechanism for calling back to the presenter when they release video samples because the sample object provides that mechanism.</span></span>

<span data-ttu-id="f833a-533">Il codice seguente illustra come impostare il callback:</span><span class="sxs-lookup"><span data-stu-id="f833a-533">The following code shows how to set the callback:</span></span>


```C++
HRESULT EVRCustomPresenter::TrackSample(IMFSample *pSample)
{
    IMFTrackedSample *pTracked = NULL;

    HRESULT hr = pSample->QueryInterface(IID_PPV_ARGS(&pTracked));

    if (SUCCEEDED(hr))
    {
        hr = pTracked->SetAllocator(&m_SampleFreeCB, NULL);
    }

    SafeRelease(&pTracked);
    return hr;
}
```



<span data-ttu-id="f833a-534">Nel callback chiamare [**IMFAsyncResult::GetObject sull'oggetto**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getobject) risultato asincrono per recuperare un puntatore all'esempio:</span><span class="sxs-lookup"><span data-stu-id="f833a-534">In the callback, call [**IMFAsyncResult::GetObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getobject) on the asynchronous result object to retrieve a pointer to the sample:</span></span>


```C++
HRESULT EVRCustomPresenter::OnSampleFree(IMFAsyncResult *pResult)
{
    IUnknown *pObject = NULL;
    IMFSample *pSample = NULL;
    IUnknown *pUnk = NULL;

    // Get the sample from the async result object.
    HRESULT hr = pResult->GetObject(&pObject);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pObject->QueryInterface(IID_PPV_ARGS(&pSample));
    if (FAILED(hr))
    {
        goto done;
    }

    // If this sample was submitted for a frame-step, the frame step operation
    // is complete.

    if (m_FrameStep.state == FRAMESTEP_SCHEDULED)
    {
        // Query the sample for IUnknown and compare it to our cached value.
        hr = pSample->QueryInterface(IID_PPV_ARGS(&pUnk));
        if (FAILED(hr))
        {
            goto done;
        }

        if (m_FrameStep.pSampleNoRef == (DWORD_PTR)pUnk)
        {
            // Notify the EVR.
            hr = CompleteFrameStep(pSample);
            if (FAILED(hr))
            {
                goto done;
            }
        }

        // Note: Although pObject is also an IUnknown pointer, it is not
        // guaranteed to be the exact pointer value returned through
        // QueryInterface. Therefore, the second QueryInterface call is
        // required.
    }

    /*** Begin lock ***/

    EnterCriticalSection(&m_ObjectLock);

    UINT32 token = MFGetAttributeUINT32(
        pSample, MFSamplePresenter_SampleCounter, (UINT32)-1);

    if (token == m_TokenCounter)
    {
        // Return the sample to the sample pool.
        hr = m_SamplePool.ReturnSample(pSample);
        if (SUCCEEDED(hr))
        {
            // A free sample is available. Process more data if possible.
            (void)ProcessOutputLoop();
        }
    }

    LeaveCriticalSection(&m_ObjectLock);

    /*** End lock ***/

done:
    if (FAILED(hr))
    {
        NotifyEvent(EC_ERRORABORT, hr, 0);
    }
    SafeRelease(&pObject);
    SafeRelease(&pSample);
    SafeRelease(&pUnk);
    return hr;
}
```



## <a name="processing-output"></a><span data-ttu-id="f833a-535">Elaborazione dell'output</span><span class="sxs-lookup"><span data-stu-id="f833a-535">Processing Output</span></span>

<span data-ttu-id="f833a-536">Ogni volta che il mixer riceve un nuovo esempio di input, l'EVR invia **un** messaggio MFVP_MESSAGE_PROCESSINPUTNOTIFY al presentatore.</span><span class="sxs-lookup"><span data-stu-id="f833a-536">Whenever the mixer receives a new input sample, the EVR sends an **MFVP_MESSAGE_PROCESSINPUTNOTIFY** message to the presenter.</span></span> <span data-ttu-id="f833a-537">Questo messaggio indica che il mixer potrebbe avere un nuovo fotogramma video da recapitare.</span><span class="sxs-lookup"><span data-stu-id="f833a-537">This message indicates that the mixer might have a new video frame to deliver.</span></span> <span data-ttu-id="f833a-538">In risposta, il presentatore chiama [**IMFTransform::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) nel mixer.</span><span class="sxs-lookup"><span data-stu-id="f833a-538">In response, the presenter calls [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) on the mixer.</span></span> <span data-ttu-id="f833a-539">Se il metodo ha esito positivo, il presentatore pianifica l'esempio per la presentazione.</span><span class="sxs-lookup"><span data-stu-id="f833a-539">If the method succeeds, the presenter schedules the sample for presentation.</span></span>

<span data-ttu-id="f833a-540">Per ottenere l'output dal mixer, seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="f833a-540">To get output from the mixer, perform the following steps:</span></span>

1.  <span data-ttu-id="f833a-541">Controllare lo stato dell'orologio.</span><span class="sxs-lookup"><span data-stu-id="f833a-541">Check the clock state.</span></span> <span data-ttu-id="f833a-542">Se l'orologio è sospeso, ignorare il messaggio **MFVP_MESSAGE_PROCESSINPUTNOTIFY** a meno che non si tratta del primo fotogramma video.</span><span class="sxs-lookup"><span data-stu-id="f833a-542">If the clock is paused, ignore the **MFVP_MESSAGE_PROCESSINPUTNOTIFY** message unless this is the first video frame.</span></span> <span data-ttu-id="f833a-543">Se l'orologio è in esecuzione o se si tratta del primo fotogramma video, continuare.</span><span class="sxs-lookup"><span data-stu-id="f833a-543">If the clock is running, or if this is the first video frame, continue.</span></span>
2.  <span data-ttu-id="f833a-544">Ottenere un esempio dalla coda di esempi disponibili.</span><span class="sxs-lookup"><span data-stu-id="f833a-544">Get a sample from the queue of available samples.</span></span> <span data-ttu-id="f833a-545">Se la coda è vuota, significa che tutti i campioni allocati sono attualmente pianificati per la presentazione.</span><span class="sxs-lookup"><span data-stu-id="f833a-545">If the queue is empty, it means that all allocated samples are currently scheduled for presenting.</span></span> <span data-ttu-id="f833a-546">In questo caso, ignorare il **MFVP_MESSAGE_PROCESSINPUTNOTIFY** al momento.</span><span class="sxs-lookup"><span data-stu-id="f833a-546">In that case, ignore the **MFVP_MESSAGE_PROCESSINPUTNOTIFY** message at this time.</span></span> <span data-ttu-id="f833a-547">Quando l'esempio successivo diventa disponibile, ripetere i passaggi elencati qui.</span><span class="sxs-lookup"><span data-stu-id="f833a-547">When the next sample becomes available, repeat the steps listed here.</span></span>
3.  <span data-ttu-id="f833a-548">(Facoltativo). Se l'orologio è disponibile, ottenere l'ora corrente (*T1*) chiamando [**IMFClock::GetCorrelatedTime**](/windows/desktop/api/mfidl/nf-mfidl-imfclock-getcorrelatedtime).</span><span class="sxs-lookup"><span data-stu-id="f833a-548">(Optional.) If the clock is available, get the current clock time (*T1*) by calling [**IMFClock::GetCorrelatedTime**](/windows/desktop/api/mfidl/nf-mfidl-imfclock-getcorrelatedtime).</span></span>
4.  <span data-ttu-id="f833a-549">Chiamare [**IMFTransform::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) nel mixer.</span><span class="sxs-lookup"><span data-stu-id="f833a-549">Call [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) on the mixer.</span></span> <span data-ttu-id="f833a-550">Se **ProcessOutput ha** esito positivo, l'esempio contiene un fotogramma video.</span><span class="sxs-lookup"><span data-stu-id="f833a-550">If **ProcessOutput** succeeds, the sample contains a video frame.</span></span> <span data-ttu-id="f833a-551">Se il metodo ha esito negativo, controllare il codice restituito.</span><span class="sxs-lookup"><span data-stu-id="f833a-551">If the method fails, check the return code.</span></span> <span data-ttu-id="f833a-552">I codici di errore seguenti **di ProcessOutput** non sono errori critici:</span><span class="sxs-lookup"><span data-stu-id="f833a-552">The following error codes from **ProcessOutput** are not critical failures:</span></span>

    

    | <span data-ttu-id="f833a-553">Codice di errore</span><span class="sxs-lookup"><span data-stu-id="f833a-553">Error code</span></span>                              | <span data-ttu-id="f833a-554">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f833a-554">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                    |
    |-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="f833a-555">**MF_E_TRANSFORM_NEED_MORE_INPUT**</span><span class="sxs-lookup"><span data-stu-id="f833a-555">**MF_E_TRANSFORM_NEED_MORE_INPUT**</span></span> | <span data-ttu-id="f833a-556">Il mixer richiede più input prima di poter produrre un nuovo frame di output.</span><span class="sxs-lookup"><span data-stu-id="f833a-556">The mixer needs more input before it can produce a new output frame.</span></span><br/> <span data-ttu-id="f833a-557">Se si ottiene questo codice di errore, verificare se l'EVR ha raggiunto la fine del flusso e rispondere di conseguenza, come descritto in [Fine del flusso](#end-of-stream).</span><span class="sxs-lookup"><span data-stu-id="f833a-557">If you get this error code, check whether the EVR has reached the end of the stream and respond accordingly, as described in [End of Stream](#end-of-stream).</span></span> <span data-ttu-id="f833a-558">In caso contrario, ignorare **questo MF_E_TRANSFORM_NEED_MORE_INPUT** messaggio.</span><span class="sxs-lookup"><span data-stu-id="f833a-558">Otherwise, ignore this **MF_E_TRANSFORM_NEED_MORE_INPUT** message.</span></span> <span data-ttu-id="f833a-559">L'EVR ne invierà un altro quando il mixer ottiene più input.</span><span class="sxs-lookup"><span data-stu-id="f833a-559">The EVR will send another one when the mixer gets more input.</span></span><br/> |
    | <span data-ttu-id="f833a-560">**MF_E_TRANSFORM_STREAM_CHANGE**</span><span class="sxs-lookup"><span data-stu-id="f833a-560">**MF_E_TRANSFORM_STREAM_CHANGE**</span></span>    | <span data-ttu-id="f833a-561">Il tipo di output del mixer non è più valido, probabilmente a causa di una modifica del formato a monte.</span><span class="sxs-lookup"><span data-stu-id="f833a-561">The mixer's output type has become invalid, possibly due to a format change upstream.</span></span><br/> <span data-ttu-id="f833a-562">Se si ottiene questo codice di errore, impostare il tipo di supporto del presentatore su **NULL.**</span><span class="sxs-lookup"><span data-stu-id="f833a-562">If you get this error code, set the presenter's media type to **NULL**.</span></span> <span data-ttu-id="f833a-563">L'EVR richiederà un nuovo formato.</span><span class="sxs-lookup"><span data-stu-id="f833a-563">The EVR will request a new format.</span></span><br/>                                                                                                                                                                         |
    | <span data-ttu-id="f833a-564">**MF_E_TRANSFORM_TYPE_NOT_SET**</span><span class="sxs-lookup"><span data-stu-id="f833a-564">**MF_E_TRANSFORM_TYPE_NOT_SET**</span></span>    | <span data-ttu-id="f833a-565">Il mixer richiede un nuovo tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="f833a-565">The mixer requires a new media type.</span></span><br/> <span data-ttu-id="f833a-566">Se si ottiene questo codice di errore, rinegoziare il tipo di output del mixer come descritto in [Formati negoziali](#negotiating-formats).</span><span class="sxs-lookup"><span data-stu-id="f833a-566">If you get this error code, renegotiate the mixer's output type as described in [Negotiating Formats](#negotiating-formats).</span></span><br/>                                                                                                                                                                                                        |

    

     

    <span data-ttu-id="f833a-567">Se [**ProcessOutput ha**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) esito positivo, continuare.</span><span class="sxs-lookup"><span data-stu-id="f833a-567">If [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) succeeds, continue.</span></span>

5.  <span data-ttu-id="f833a-568">(Facoltativo). Se l'orologio è disponibile, ottenere l'ora corrente (*T2*).</span><span class="sxs-lookup"><span data-stu-id="f833a-568">(Optional.) If the clock is available, get the current clock time (*T2*).</span></span> <span data-ttu-id="f833a-569">La latenza introdotta dal mixer è (*T2*  -  *T1*).</span><span class="sxs-lookup"><span data-stu-id="f833a-569">The amount of latency introduced by the mixer is (*T2* - *T1*).</span></span> <span data-ttu-id="f833a-570">Inviare **un EC_PROCESSING_LATENCY** evento con questo valore all'EVR.</span><span class="sxs-lookup"><span data-stu-id="f833a-570">Send an **EC_PROCESSING_LATENCY** event with this value to the EVR.</span></span> <span data-ttu-id="f833a-571">L'EVR usa questo valore per il controllo qualità.</span><span class="sxs-lookup"><span data-stu-id="f833a-571">The EVR uses this value for quality control.</span></span> <span data-ttu-id="f833a-572">Se non è disponibile alcun orologio, non vi è alcun motivo per inviare **l'EC_PROCESSING_LATENCY** evento.</span><span class="sxs-lookup"><span data-stu-id="f833a-572">If no clock is available, there is no reason to send the **EC_PROCESSING_LATENCY** event.</span></span>
6.  <span data-ttu-id="f833a-573">(Facoltativo). Eseguire una query [**sull'esempio per IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) e chiamare [**IMFTrackedSample::SetAllocator**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) come descritto in [Esempi di rilevamento](#tracking-samples).</span><span class="sxs-lookup"><span data-stu-id="f833a-573">(Optional.) Query the sample for [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) and call [**IMFTrackedSample::SetAllocator**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) as described in [Tracking Samples](#tracking-samples).</span></span>
7.  <span data-ttu-id="f833a-574">Pianificare l'esempio per la presentazione.</span><span class="sxs-lookup"><span data-stu-id="f833a-574">Schedule the sample for presentation.</span></span>

<span data-ttu-id="f833a-575">Questa sequenza di passaggi può terminare prima che il presentatore osceni l'output dal mixer.</span><span class="sxs-lookup"><span data-stu-id="f833a-575">This sequence of steps can terminate before the presenter gets any output from the mixer.</span></span> <span data-ttu-id="f833a-576">Per assicurarsi che nessuna richiesta sia eliminata, è necessario ripetere gli stessi passaggi quando si verificano le condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="f833a-576">To ensure that no requests are dropped, you should repeat the same steps when the following occur:</span></span>

-   <span data-ttu-id="f833a-577">Viene chiamato il metodo [**IMFClockStateSink::OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) o **IMFClockStateSink::OnClockStart** del presentatore.</span><span class="sxs-lookup"><span data-stu-id="f833a-577">The presenter's [**IMFClockStateSink::OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) or **IMFClockStateSink::OnClockStart** method is called.</span></span> <span data-ttu-id="f833a-578">In questo modo viene gestito il caso in cui il mixer ignora l'input perché l'orologio è sospeso (passaggio 1).</span><span class="sxs-lookup"><span data-stu-id="f833a-578">This handles the case where the mixer ignores input because the clock is paused (step 1).</span></span>
-   <span data-ttu-id="f833a-579">Viene richiamato il callback [**IMFTrackedSample.**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample)</span><span class="sxs-lookup"><span data-stu-id="f833a-579">The [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) callback is invoked.</span></span> <span data-ttu-id="f833a-580">Questo gestisce il caso in cui il mixer riceve input, ma tutti gli esempi video del presentatore sono in uso (passaggio 2).</span><span class="sxs-lookup"><span data-stu-id="f833a-580">This handles the case where the mixer receives input but all of the presenter's video samples are in use (step 2).</span></span>

<span data-ttu-id="f833a-581">I seguenti esempi di codice illustrano questi passaggi in modo più dettagliato.</span><span class="sxs-lookup"><span data-stu-id="f833a-581">The next several code examples show these steps in more detail.</span></span> <span data-ttu-id="f833a-582">Il presentatore chiama il `ProcessInputNotify` metodo (illustrato nell'esempio seguente) quando ottiene il **MFVP_MESSAGE_PROCESSINPUTNOTIFY** messaggio.</span><span class="sxs-lookup"><span data-stu-id="f833a-582">The presenter calls the `ProcessInputNotify` method (shown in the following example) when it gets the **MFVP_MESSAGE_PROCESSINPUTNOTIFY** message.</span></span>


```C++
//-----------------------------------------------------------------------------
// ProcessInputNotify
//
// Attempts to get a new output sample from the mixer.
//
// This method is called when the EVR sends an MFVP_MESSAGE_PROCESSINPUTNOTIFY
// message, which indicates that the mixer has a new input sample.
//
// Note: If there are multiple input streams, the mixer might not deliver an
// output sample for every input sample.
//-----------------------------------------------------------------------------

HRESULT EVRCustomPresenter::ProcessInputNotify()
{
    HRESULT hr = S_OK;

    // Set the flag that says the mixer has a new sample.
    m_bSampleNotify = TRUE;

    if (m_pMediaType == NULL)
    {
        // We don't have a valid media type yet.
        hr = MF_E_TRANSFORM_TYPE_NOT_SET;
    }
    else
    {
        // Try to process an output sample.
        ProcessOutputLoop();
    }
    return hr;
}
```



<span data-ttu-id="f833a-583">Questo `ProcessInputNotify` metodo imposta un flag booleano per registrare il fatto che il mixer ha un nuovo input.</span><span class="sxs-lookup"><span data-stu-id="f833a-583">This `ProcessInputNotify` method sets a Boolean flag to record the fact that the mixer has new input.</span></span> <span data-ttu-id="f833a-584">Chiama quindi il `ProcessOutputLoop` metodo , illustrato nell'esempio successivo.</span><span class="sxs-lookup"><span data-stu-id="f833a-584">Then it calls the `ProcessOutputLoop` method, shown in the next example.</span></span> <span data-ttu-id="f833a-585">Questo metodo tenta di eseguire il pull del maggior numero possibile di esempi dal mixer:</span><span class="sxs-lookup"><span data-stu-id="f833a-585">This method attempts to pull as many samples as possible from the mixer:</span></span>


```C++
void EVRCustomPresenter::ProcessOutputLoop()
{
    HRESULT hr = S_OK;

    // Process as many samples as possible.
    while (hr == S_OK)
    {
        // If the mixer doesn't have a new input sample, break from the loop.
        if (!m_bSampleNotify)
        {
            hr = MF_E_TRANSFORM_NEED_MORE_INPUT;
            break;
        }

        // Try to process a sample.
        hr = ProcessOutput();

        // NOTE: ProcessOutput can return S_FALSE to indicate it did not
        // process a sample. If so, break out of the loop.
    }

    if (hr == MF_E_TRANSFORM_NEED_MORE_INPUT)
    {
        // The mixer has run out of input data. Check for end-of-stream.
        CheckEndOfStream();
    }
}
```



<span data-ttu-id="f833a-586">Il `ProcessOutput` metodo , illustrato nell'esempio successivo, tenta di ottenere un singolo fotogramma video dal mixer.</span><span class="sxs-lookup"><span data-stu-id="f833a-586">The `ProcessOutput` method, shown in the next example, attempts to get a single video frame from the mixer.</span></span> <span data-ttu-id="f833a-587">Se non è disponibile alcun fotogramma video, restituisce S_FALSE o un codice di errore, che interrompe `ProcessSample` il ciclo in `ProcessOutputLoop` .</span><span class="sxs-lookup"><span data-stu-id="f833a-587">If no video frame is available, `ProcessSample` returns S_FALSE or an error code, either of which interrupts the loop in `ProcessOutputLoop`.</span></span> <span data-ttu-id="f833a-588">La maggior parte del lavoro viene eseguita all'interno del `ProcessOutput` metodo :</span><span class="sxs-lookup"><span data-stu-id="f833a-588">Most of the work is done inside the `ProcessOutput` method:</span></span>


```C++
//-----------------------------------------------------------------------------
// ProcessOutput
//
// Attempts to get a new output sample from the mixer.
//
// Called in two situations:
// (1) ProcessOutputLoop, if the mixer has a new input sample.
// (2) Repainting the last frame.
//-----------------------------------------------------------------------------

HRESULT EVRCustomPresenter::ProcessOutput()
{
    assert(m_bSampleNotify || m_bRepaint);  // See note above.

    HRESULT     hr = S_OK;
    DWORD       dwStatus = 0;
    LONGLONG    mixerStartTime = 0, mixerEndTime = 0;
    MFTIME      systemTime = 0;
    BOOL        bRepaint = m_bRepaint; // Temporarily store this state flag.

    MFT_OUTPUT_DATA_BUFFER dataBuffer;
    ZeroMemory(&dataBuffer, sizeof(dataBuffer));

    IMFSample *pSample = NULL;

    // If the clock is not running, we present the first sample,
    // and then don't present any more until the clock starts.

    if ((m_RenderState != RENDER_STATE_STARTED) &&  // Not running.
         !m_bRepaint &&             // Not a repaint request.
         m_bPrerolled               // At least one sample has been presented.
         )
    {
        return S_FALSE;
    }

    // Make sure we have a pointer to the mixer.
    if (m_pMixer == NULL)
    {
        return MF_E_INVALIDREQUEST;
    }

    // Try to get a free sample from the video sample pool.
    hr = m_SamplePool.GetSample(&pSample);
    if (hr == MF_E_SAMPLEALLOCATOR_EMPTY)
    {
        // No free samples. Try again when a sample is released.
        return S_FALSE;
    }
    else if (FAILED(hr))
    {
        return hr;
    }

    // From now on, we have a valid video sample pointer, where the mixer will
    // write the video data.
    assert(pSample != NULL);

    // (If the following assertion fires, it means we are not managing the sample pool correctly.)
    assert(MFGetAttributeUINT32(pSample, MFSamplePresenter_SampleCounter, (UINT32)-1) == m_TokenCounter);

    if (m_bRepaint)
    {
        // Repaint request. Ask the mixer for the most recent sample.
        SetDesiredSampleTime(
            pSample,
            m_scheduler.LastSampleTime(),
            m_scheduler.FrameDuration()
            );

        m_bRepaint = FALSE; // OK to clear this flag now.
    }
    else
    {
        // Not a repaint request. Clear the desired sample time; the mixer will
        // give us the next frame in the stream.
        ClearDesiredSampleTime(pSample);

        if (m_pClock)
        {
            // Latency: Record the starting time for ProcessOutput.
            (void)m_pClock->GetCorrelatedTime(0, &mixerStartTime, &systemTime);
        }
    }

    // Now we are ready to get an output sample from the mixer.
    dataBuffer.dwStreamID = 0;
    dataBuffer.pSample = pSample;
    dataBuffer.dwStatus = 0;

    hr = m_pMixer->ProcessOutput(0, 1, &dataBuffer, &dwStatus);

    if (FAILED(hr))
    {
        // Return the sample to the pool.
        HRESULT hr2 = m_SamplePool.ReturnSample(pSample);
        if (FAILED(hr2))
        {
            hr = hr2;
            goto done;
        }
        // Handle some known error codes from ProcessOutput.
        if (hr == MF_E_TRANSFORM_TYPE_NOT_SET)
        {
            // The mixer's format is not set. Negotiate a new format.
            hr = RenegotiateMediaType();
        }
        else if (hr == MF_E_TRANSFORM_STREAM_CHANGE)
        {
            // There was a dynamic media type change. Clear our media type.
            SetMediaType(NULL);
        }
        else if (hr == MF_E_TRANSFORM_NEED_MORE_INPUT)
        {
            // The mixer needs more input.
            // We have to wait for the mixer to get more input.
            m_bSampleNotify = FALSE;
        }
    }
    else
    {
        // We got an output sample from the mixer.

        if (m_pClock && !bRepaint)
        {
            // Latency: Record the ending time for the ProcessOutput operation,
            // and notify the EVR of the latency.

            (void)m_pClock->GetCorrelatedTime(0, &mixerEndTime, &systemTime);

            LONGLONG latencyTime = mixerEndTime - mixerStartTime;
            NotifyEvent(EC_PROCESSING_LATENCY, (LONG_PTR)&latencyTime, 0);
        }

        // Set up notification for when the sample is released.
        hr = TrackSample(pSample);
        if (FAILED(hr))
        {
            goto done;
        }

        // Schedule the sample.
        if ((m_FrameStep.state == FRAMESTEP_NONE) || bRepaint)
        {
            hr = DeliverSample(pSample, bRepaint);
            if (FAILED(hr))
            {
                goto done;
            }
        }
        else
        {
            // We are frame-stepping (and this is not a repaint request).
            hr = DeliverFrameStepSample(pSample);
            if (FAILED(hr))
            {
                goto done;
            }
        }

        m_bPrerolled = TRUE; // We have presented at least one sample now.
    }

done:
    SafeRelease(&pSample);

    // Important: Release any events returned from the ProcessOutput method.
    SafeRelease(&dataBuffer.pEvents);
    return hr;
}
```



<span data-ttu-id="f833a-589">Alcune osservazioni su questo esempio:</span><span class="sxs-lookup"><span data-stu-id="f833a-589">Some remarks about this example:</span></span>

-   <span data-ttu-id="f833a-590">Si *presuppone m_SamplePool* variabile sia un oggetto raccolta che contiene la coda di esempi video disponibili.</span><span class="sxs-lookup"><span data-stu-id="f833a-590">The *m_SamplePool* variable is assumed to be a collection object that holds the queue of available video samples.</span></span> <span data-ttu-id="f833a-591">Il metodo `GetSample` dell'oggetto restituisce **MF_E_SAMPLEALLOCATOR_EMPTY** se la coda è vuota.</span><span class="sxs-lookup"><span data-stu-id="f833a-591">The object's `GetSample` method returns **MF_E_SAMPLEALLOCATOR_EMPTY** if the queue is empty.</span></span>
-   <span data-ttu-id="f833a-592">Se il metodo [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) del mixer restituisce MF_E_TRANSFORM_NEED_MORE_INPUT, significa che il mixer non può produrre altro output, quindi il presentatore cancella il *flag* m_fSampleNotify.</span><span class="sxs-lookup"><span data-stu-id="f833a-592">If the mixer's [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) method returns MF_E_TRANSFORM_NEED_MORE_INPUT, it means the mixer cannot produce any more output, so the presenter clears the *m_fSampleNotify* flag.</span></span>
-   <span data-ttu-id="f833a-593">Il `TrackSample` metodo , che imposta il callback [**IMFTrackedSample,**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) è illustrato nella sezione [Esempi di rilevamento](#tracking-samples).</span><span class="sxs-lookup"><span data-stu-id="f833a-593">The `TrackSample` method, which sets the [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) callback, is shown in the section [Tracking Samples](#tracking-samples).</span></span>

### <a name="repainting-frames"></a><span data-ttu-id="f833a-594">Ridipingere i frame</span><span class="sxs-lookup"><span data-stu-id="f833a-594">Repainting Frames</span></span>

<span data-ttu-id="f833a-595">A volte il presentatore potrebbe dover ridisegnare il fotogramma video più recente.</span><span class="sxs-lookup"><span data-stu-id="f833a-595">Occasionally the presenter might need to repaint the most recent video frame.</span></span> <span data-ttu-id="f833a-596">Ad esempio, il presentatore standard ridisegna il frame nelle situazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="f833a-596">For example, the standard presenter repaints the frame in the following situations:</span></span>

-   <span data-ttu-id="f833a-597">In modalità finestra, in risposta ai **WM_PAINT** ricevuti dalla finestra dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f833a-597">In windowed mode, in response to **WM_PAINT** messages received by the application's window.</span></span> <span data-ttu-id="f833a-598">Vedere [**IMFVideoDisplayControl::RepaintVideo**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo).</span><span class="sxs-lookup"><span data-stu-id="f833a-598">See [**IMFVideoDisplayControl::RepaintVideo**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo).</span></span>
-   <span data-ttu-id="f833a-599">Se il rettangolo di destinazione cambia quando l'applicazione chiama [**IMFVideoDisplayControl::SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition).</span><span class="sxs-lookup"><span data-stu-id="f833a-599">If the destination rectangle changes when the application calls [**IMFVideoDisplayControl::SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition).</span></span>

<span data-ttu-id="f833a-600">Seguire questa procedura per richiedere al mixer di creare di nuovo il frame più recente:</span><span class="sxs-lookup"><span data-stu-id="f833a-600">Use the following steps to request the mixer to re-create the most recent frame:</span></span>

1.  <span data-ttu-id="f833a-601">Ottenere un video di esempio dalla coda.</span><span class="sxs-lookup"><span data-stu-id="f833a-601">Get a video sample from the queue.</span></span>
2.  <span data-ttu-id="f833a-602">Eseguire una query sull'esempio per [**l'interfaccia IMFDesiredSample.**](/windows/desktop/api/evr/nn-evr-imfdesiredsample)</span><span class="sxs-lookup"><span data-stu-id="f833a-602">Query the sample for the [**IMFDesiredSample**](/windows/desktop/api/evr/nn-evr-imfdesiredsample) interface.</span></span>
3.  <span data-ttu-id="f833a-603">Chiamare [**IMFDesiredSample::SetDesiredSampleTimeAndDuration**](/windows/desktop/api/evr/nf-evr-imfdesiredsample-setdesiredsampletimeandduration).</span><span class="sxs-lookup"><span data-stu-id="f833a-603">Call [**IMFDesiredSample::SetDesiredSampleTimeAndDuration**](/windows/desktop/api/evr/nf-evr-imfdesiredsample-setdesiredsampletimeandduration).</span></span> <span data-ttu-id="f833a-604">Specificare il timestamp del fotogramma video più recente.</span><span class="sxs-lookup"><span data-stu-id="f833a-604">Specify the time stamp of the most recent video frame.</span></span> <span data-ttu-id="f833a-605">È necessario memorizzare nella cache questo valore e aggiornarlo per ogni frame.</span><span class="sxs-lookup"><span data-stu-id="f833a-605">(You will need to cache this value and update it for each frame.)</span></span>
4.  <span data-ttu-id="f833a-606">Chiamare [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) sul mixer.</span><span class="sxs-lookup"><span data-stu-id="f833a-606">Call [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) on the mixer.</span></span>

<span data-ttu-id="f833a-607">Quando si ridisegna un frame, è possibile ignorare l'orologio della presentazione e presentare immediatamente il frame.</span><span class="sxs-lookup"><span data-stu-id="f833a-607">When repainting a frame, you can ignore the presentation clock and present the frame immediately.</span></span>

### <a name="scheduling-samples"></a><span data-ttu-id="f833a-608">Esempi di pianificazione</span><span class="sxs-lookup"><span data-stu-id="f833a-608">Scheduling Samples</span></span>

<span data-ttu-id="f833a-609">I fotogrammi video possono raggiungere l'EVR in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="f833a-609">Video frames can reach the EVR at any time.</span></span> <span data-ttu-id="f833a-610">Il presentatore è responsabile della presentazione di ogni fotogramma all'ora corretta, in base al timestamp dell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="f833a-610">The presenter is responsible for presenting each frame at the correct time, based on the time stamp of the frame.</span></span> <span data-ttu-id="f833a-611">Quando il presentatore ottiene un nuovo esempio dal mixer, lo inserisce nella coda pianificata.</span><span class="sxs-lookup"><span data-stu-id="f833a-611">When the presenter gets a new sample from the mixer, it puts the sample on the scheduled queue.</span></span> <span data-ttu-id="f833a-612">In un thread separato, il presentatore ottiene continuamente il primo esempio dall'inizio della coda e determina se:</span><span class="sxs-lookup"><span data-stu-id="f833a-612">On a separate thread, the presenter continually gets the first sample from the head of the queue and determines whether to:</span></span>

-   <span data-ttu-id="f833a-613">Presentare l'esempio.</span><span class="sxs-lookup"><span data-stu-id="f833a-613">Present the sample.</span></span>
-   <span data-ttu-id="f833a-614">Mantenere l'esempio nella coda perché è in anticipo.</span><span class="sxs-lookup"><span data-stu-id="f833a-614">Keep the sample on the queue because it is early.</span></span>
-   <span data-ttu-id="f833a-615">Eliminare l'esempio perché è in ritardo.</span><span class="sxs-lookup"><span data-stu-id="f833a-615">Discard the sample because it is late.</span></span> <span data-ttu-id="f833a-616">Anche se è consigliabile evitare di eliminare i frame, se possibile, potrebbe essere necessario se il presentatore continua a essere in ritardo.</span><span class="sxs-lookup"><span data-stu-id="f833a-616">Although you should avoid dropping frames if possible, you might need to if the presenter is continually falling behind.</span></span>

<span data-ttu-id="f833a-617">Per ottenere il timestamp per un fotogramma video, chiamare [**IMFSample::GetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampletime) nell'esempio video.</span><span class="sxs-lookup"><span data-stu-id="f833a-617">To get the time stamp for a video frame, call [**IMFSample::GetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampletime) on the video sample.</span></span> <span data-ttu-id="f833a-618">Il timestamp è relativo all'orologio di presentazione dell'EVR.</span><span class="sxs-lookup"><span data-stu-id="f833a-618">The time stamp is relative to the EVR's presentation clock.</span></span> <span data-ttu-id="f833a-619">Per ottenere l'ora corrente, chiamare [**IMFClock::GetCorrelatedTime**](/windows/desktop/api/mfidl/nf-mfidl-imfclock-getcorrelatedtime).</span><span class="sxs-lookup"><span data-stu-id="f833a-619">To get the current clock time, call [**IMFClock::GetCorrelatedTime**](/windows/desktop/api/mfidl/nf-mfidl-imfclock-getcorrelatedtime).</span></span> <span data-ttu-id="f833a-620">Se l'EVR non ha un orologio di presentazione o se un campione non ha un timestamp, è possibile presentare l'esempio immediatamente dopo averlo creato.</span><span class="sxs-lookup"><span data-stu-id="f833a-620">If the EVR does not have a presentation clock, or if a sample does not have a time stamp, you can present the sample immediately after you get it.</span></span>

<span data-ttu-id="f833a-621">Per ottenere la durata di ogni esempio, chiamare [**IMFSample::GetSampleDuration**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampleduration).</span><span class="sxs-lookup"><span data-stu-id="f833a-621">To get the duration of each sample, call [**IMFSample::GetSampleDuration**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampleduration).</span></span> <span data-ttu-id="f833a-622">Se l'esempio non ha una durata, è possibile usare la funzione [**MFFrameRateToAverageTimePerFrame**](/windows/desktop/api/mfapi/nf-mfapi-mfframeratetoaveragetimeperframe) per calcolare la durata dalla frequenza dei fotogrammi.</span><span class="sxs-lookup"><span data-stu-id="f833a-622">If the sample does not have a duration, you can use the [**MFFrameRateToAverageTimePerFrame**](/windows/desktop/api/mfapi/nf-mfapi-mfframeratetoaveragetimeperframe) function to calculate the duration from the frame rate.</span></span>

<span data-ttu-id="f833a-623">Quando si pianificano esempi, tenere presente quanto segue:</span><span class="sxs-lookup"><span data-stu-id="f833a-623">When you schedule samples, keep in mind the following:</span></span>

-   <span data-ttu-id="f833a-624">Se la velocità di riproduzione è più veloce o più lenta della velocità normale, l'orologio viene eseguito a una velocità più veloce o più lenta.</span><span class="sxs-lookup"><span data-stu-id="f833a-624">If the playback rate is faster or slower than normal speed, the clock runs at a faster or slower rate.</span></span> <span data-ttu-id="f833a-625">Ciò significa che il timestamp di un campione fornisce sempre l'ora di destinazione corretta rispetto all'orologio di presentazione.</span><span class="sxs-lookup"><span data-stu-id="f833a-625">That means the time stamp on a sample always gives the correct target time relative to the presentation clock.</span></span> <span data-ttu-id="f833a-626">Tuttavia, se si converte l'ora di presentazione in un'altra ora di clock (ad esempio, il contatore delle prestazioni ad alta risoluzione), è necessario ridimensionare gli orari in base alla velocità di clock.</span><span class="sxs-lookup"><span data-stu-id="f833a-626">However, if you translate presentation times into some other clock time (for example, the high-resolution performace counter), then you must scale the times based on the clock speed.</span></span> <span data-ttu-id="f833a-627">Se la velocità del clock cambia, EVR chiama il metodo [**IMFClockStateSink::OnClockSetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) del presentatore.</span><span class="sxs-lookup"><span data-stu-id="f833a-627">If the clock speed changes, the EVR calls the presenter's [**IMFClockStateSink::OnClockSetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) method.</span></span>
-   <span data-ttu-id="f833a-628">La velocità di riproduzione può essere negativa per la riproduzione inversa.</span><span class="sxs-lookup"><span data-stu-id="f833a-628">The playback rate can be negative for reverse playback.</span></span> <span data-ttu-id="f833a-629">Quando la velocità di riproduzione è negativa, l'orologio della presentazione viene eseguito all'indietro.</span><span class="sxs-lookup"><span data-stu-id="f833a-629">When the playback rate is negative, the presentation clock runs backward.</span></span> <span data-ttu-id="f833a-630">In altre parole, *l'ora N* + 1 si verifica prima dell'ora *N*.</span><span class="sxs-lookup"><span data-stu-id="f833a-630">In other words, time *N* + 1 occurs before time *N*.</span></span>

<span data-ttu-id="f833a-631">L'esempio seguente calcola la velocità di un campione in anticipo o in ritardo rispetto all'orologio di presentazione:</span><span class="sxs-lookup"><span data-stu-id="f833a-631">The following example calculates how early or late a sample is, relative to the presentation clock:</span></span>


```C++
    LONGLONG hnsPresentationTime = 0;
    LONGLONG hnsTimeNow = 0;
    MFTIME   hnsSystemTime = 0;

    BOOL bPresentNow = TRUE;
    LONG lNextSleep = 0;

    if (m_pClock)
    {
        // Get the sample's time stamp. It is valid for a sample to
        // have no time stamp.
        hr = pSample->GetSampleTime(&hnsPresentationTime);

        // Get the clock time. (But if the sample does not have a time stamp,
        // we don't need the clock time.)
        if (SUCCEEDED(hr))
        {
            hr = m_pClock->GetCorrelatedTime(0, &hnsTimeNow, &hnsSystemTime);
        }

        // Calculate the time until the sample's presentation time.
        // A negative value means the sample is late.
        LONGLONG hnsDelta = hnsPresentationTime - hnsTimeNow;
        if (m_fRate < 0)
        {
            // For reverse playback, the clock runs backward. Therefore, the
            // delta is reversed.
            hnsDelta = - hnsDelta;
        }
```



<span data-ttu-id="f833a-632">L'orologio di presentazione è in genere basato sull'orologio di sistema o sul renderer audio.</span><span class="sxs-lookup"><span data-stu-id="f833a-632">The presentation clock is usually driven by the system clock or the audio renderer.</span></span> <span data-ttu-id="f833a-633">Il renderer audio deriva il tempo dalla velocità con cui la scheda audio utilizza l'audio. In generale, l'orologio di presentazione non è sincronizzato con la frequenza di aggiornamento del monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="f833a-633">(The audio renderer derives the time from the rate at which the sound card consumes audio.) In general, the presentation clock is not synchronized with the refresh rate of the monitor.</span></span>

<span data-ttu-id="f833a-634">Se i parametri di  presentazione Direct3D specificano D3DPRESENT_INTERVAL_DEFAULT o **D3DPRESENT_INTERVAL_ONE**  per l'intervallo di presentazione, l'operazione Present attende la retrace verticale del monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="f833a-634">If your Direct3D presentation parameters specify **D3DPRESENT_INTERVAL_DEFAULT** or **D3DPRESENT_INTERVAL_ONE** for the presentation interval, the **Present** operation waits for the monitor's vertical retrace.</span></span> <span data-ttu-id="f833a-635">Si tratta di un modo semplice per impedire la rimozione, ma riduce l'accuratezza dell'algoritmo di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="f833a-635">This is an easy way to prevent tearing, but reduces the accuracy of your scheduling algorithm.</span></span> <span data-ttu-id="f833a-636">Viceversa, se l'intervallo di presentazione è D3DPRESENT_INTERVAL_IMMEDIATE , il metodo **Present** viene eseguito immediatamente, causando  la rimozione a meno che l'algoritmo di pianificazione non sia sufficientemente accurato da chiamare Present solo **durante** il periodo di retrace verticale.</span><span class="sxs-lookup"><span data-stu-id="f833a-636">Conversely, if the presentation interval is **D3DPRESENT_INTERVAL_IMMEDIATE**, the **Present** method executes immediately, which causes tearing unless your scheduling algorithm is accurate enough that you call **Present** only during the vertical retrace period.</span></span>

<span data-ttu-id="f833a-637">Le funzioni seguenti consentono di ottenere informazioni di intervallo accurate:</span><span class="sxs-lookup"><span data-stu-id="f833a-637">The following functions can help you get accurate timing information:</span></span>

-   <span data-ttu-id="f833a-638">**IDirect3DDevice9::GetRasterStatus** restituisce informazioni sul raster, inclusa la linea di analisi corrente e se il raster si trova nel punto vuoto verticale.</span><span class="sxs-lookup"><span data-stu-id="f833a-638">**IDirect3DDevice9::GetRasterStatus** returns information about the raster, including the current scan line and whether the raster is in the vertical blank period.</span></span>
-   <span data-ttu-id="f833a-639">**DwmGetCompositionTimingInfo restituisce informazioni sull'intervallo** per gestione finestre desktop.</span><span class="sxs-lookup"><span data-stu-id="f833a-639">**DwmGetCompositionTimingInfo** returns timing information for the desktop window manager.</span></span> <span data-ttu-id="f833a-640">Queste informazioni sono utili se la composizione desktop è abilitata.</span><span class="sxs-lookup"><span data-stu-id="f833a-640">This information is useful if desktop composition is enabled.</span></span>

### <a name="presenting-samples"></a><span data-ttu-id="f833a-641">Presentazione di esempi</span><span class="sxs-lookup"><span data-stu-id="f833a-641">Presenting Samples</span></span>

<span data-ttu-id="f833a-642">In questa sezione si presuppone che sia stata creata una catena di scambio separata per ogni superficie, come descritto in [Allocazione di superfici Direct3D.](#allocating-direct3d-surfaces)</span><span class="sxs-lookup"><span data-stu-id="f833a-642">This section assumes that you created a separate swap chain for each surface as described in [Allocating Direct3D Surfaces](#allocating-direct3d-surfaces).</span></span> <span data-ttu-id="f833a-643">Per presentare un esempio, ottenere la catena di scambio dall'esempio video come segue:</span><span class="sxs-lookup"><span data-stu-id="f833a-643">To present a sample, get the swap chain from the video sample as follows:</span></span>

1.  <span data-ttu-id="f833a-644">Chiamare [**IMFSample::GetBufferByIndex**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbufferbyindex) nell'esempio video per ottenere il buffer.</span><span class="sxs-lookup"><span data-stu-id="f833a-644">Call [**IMFSample::GetBufferByIndex**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbufferbyindex) on the video sample to get the buffer.</span></span>
2.  <span data-ttu-id="f833a-645">Eseguire una query sul buffer per [**l'interfaccia IMFGetService.**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)</span><span class="sxs-lookup"><span data-stu-id="f833a-645">Query the buffer for the [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) interface.</span></span>
3.  <span data-ttu-id="f833a-646">Chiamare [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) per ottenere **l'interfaccia IDirect3DSurface9** della superficie Direct3D.</span><span class="sxs-lookup"><span data-stu-id="f833a-646">Call [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) to get the **IDirect3DSurface9** interface of the Direct3D surface.</span></span> <span data-ttu-id="f833a-647">È possibile combinare questo passaggio e il passaggio precedente in uno chiamando [**MFGetService.**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice)</span><span class="sxs-lookup"><span data-stu-id="f833a-647">(You can combine this step and the previous step into one by calling [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice).)</span></span>
4.  <span data-ttu-id="f833a-648">Chiamare **IDirect3DSurface9::GetContainer** sulla superficie per ottenere un puntatore alla catena di scambio.</span><span class="sxs-lookup"><span data-stu-id="f833a-648">Call **IDirect3DSurface9::GetContainer** on the surface to get a pointer to the swap chain.</span></span>
5.  <span data-ttu-id="f833a-649">Chiamare **IDirect3DSwapChain9::P resent** sulla catena di scambio.</span><span class="sxs-lookup"><span data-stu-id="f833a-649">Call **IDirect3DSwapChain9::Present** on the swap chain.</span></span>

<span data-ttu-id="f833a-650">Il codice seguente illustra questi passaggi:</span><span class="sxs-lookup"><span data-stu-id="f833a-650">The following code shows these steps:</span></span>


```C++
HRESULT D3DPresentEngine::PresentSample(IMFSample* pSample, LONGLONG llTarget)
{
    HRESULT hr = S_OK;

    IMFMediaBuffer* pBuffer = NULL;
    IDirect3DSurface9* pSurface = NULL;
    IDirect3DSwapChain9* pSwapChain = NULL;

    if (pSample)
    {
        // Get the buffer from the sample.
        hr = pSample->GetBufferByIndex(0, &pBuffer);
        if (FAILED(hr))
        {
            goto done;
        }

        // Get the surface from the buffer.
        hr = MFGetService(pBuffer, MR_BUFFER_SERVICE, IID_PPV_ARGS(&pSurface));
        if (FAILED(hr))
        {
            goto done;
        }
    }
    else if (m_pSurfaceRepaint)
    {
        // Redraw from the last surface.
        pSurface = m_pSurfaceRepaint;
        pSurface->AddRef();
    }

    if (pSurface)
    {
        // Get the swap chain from the surface.
        hr = pSurface->GetContainer(IID_PPV_ARGS(&pSwapChain));
        if (FAILED(hr))
        {
            goto done;
        }

        // Present the swap chain.
        hr = PresentSwapChain(pSwapChain, pSurface);
        if (FAILED(hr))
        {
            goto done;
        }

        // Store this pointer in case we need to repaint the surface.
        CopyComPointer(m_pSurfaceRepaint, pSurface);
    }
    else
    {
        // No surface. All we can do is paint a black rectangle.
        PaintFrameWithGDI();
    }

done:
    SafeRelease(&pSwapChain);
    SafeRelease(&pSurface);
    SafeRelease(&pBuffer);

    if (FAILED(hr))
    {
        if (hr == D3DERR_DEVICELOST || hr == D3DERR_DEVICENOTRESET || hr == D3DERR_DEVICEHUNG)
        {
            // We failed because the device was lost. Fill the destination rectangle.
            PaintFrameWithGDI();

            // Ignore. We need to reset or re-create the device, but this method
            // is probably being called from the scheduler thread, which is not the
            // same thread that created the device. The Reset(Ex) method must be
            // called from the thread that created the device.

            // The presenter will detect the state when it calls CheckDeviceState()
            // on the next sample.
            hr = S_OK;
        }
    }
    return hr;
}
```



### <a name="source-and-destination-rectangles"></a><span data-ttu-id="f833a-651">Rettangoli di origine e destinazione</span><span class="sxs-lookup"><span data-stu-id="f833a-651">Source and Destination Rectangles</span></span>

<span data-ttu-id="f833a-652">Il *rettangolo di* origine è la parte del fotogramma video da visualizzare.</span><span class="sxs-lookup"><span data-stu-id="f833a-652">The *source rectangle* is the portion of the video frame to display.</span></span> <span data-ttu-id="f833a-653">È definito in relazione a un sistema di coordinate normalizzato, in cui l'intero fotogramma video occupa un rettangolo con le coordinate {0, 0, 1, 1}.</span><span class="sxs-lookup"><span data-stu-id="f833a-653">It is defined relative to a normalized coordinate system, in which the entire video frame occupies a rectangle with coordinates {0, 0, 1, 1}.</span></span> <span data-ttu-id="f833a-654">Il *rettangolo di destinazione* è l'area all'interno della superficie di destinazione in cui viene disegnato il fotogramma video.</span><span class="sxs-lookup"><span data-stu-id="f833a-654">The *destination rectangle* is the area within the destination surface where the video frame is drawn.</span></span> <span data-ttu-id="f833a-655">Il presentatore standard consente a un'applicazione di impostare questi rettangoli chiamando [**IMFVideoDisplayControl::SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition).</span><span class="sxs-lookup"><span data-stu-id="f833a-655">The standard presenter enables an application to set these rectangles by calling [**IMFVideoDisplayControl::SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition).</span></span>

<span data-ttu-id="f833a-656">Sono disponibili diverse opzioni per l'applicazione dei rettangoli di origine e di destinazione.</span><span class="sxs-lookup"><span data-stu-id="f833a-656">There are several options for applying source and destination rectangles.</span></span> <span data-ttu-id="f833a-657">La prima opzione è consentire al mixer di applicarli:</span><span class="sxs-lookup"><span data-stu-id="f833a-657">The first option is to let the mixer apply them:</span></span>

-   <span data-ttu-id="f833a-658">Impostare il rettangolo [](video-zoom-rect-attribute.md) di origine usando l VIDEO_ZOOM_RECT attribuito .</span><span class="sxs-lookup"><span data-stu-id="f833a-658">Set the source rectangle using the [**VIDEO_ZOOM_RECT**](video-zoom-rect-attribute.md) attribute.</span></span> <span data-ttu-id="f833a-659">Il mixer applicherà il rettangolo di origine quando blitterà il video sulla superficie di destinazione.</span><span class="sxs-lookup"><span data-stu-id="f833a-659">The mixer will apply the source rectangle when it blits the video to the destination surface.</span></span> <span data-ttu-id="f833a-660">Il rettangolo di origine predefinito del mixer è l'intero frame.</span><span class="sxs-lookup"><span data-stu-id="f833a-660">The mixer's default source rectangle is the entire frame.</span></span>
-   <span data-ttu-id="f833a-661">Impostare il rettangolo di destinazione come apertura geometrica nel tipo di output del mixer.</span><span class="sxs-lookup"><span data-stu-id="f833a-661">Set the destination rectangle as the geometric aperture in the mixer's output type.</span></span> <span data-ttu-id="f833a-662">Per altre informazioni, vedere [Formati di negoziazione.](#negotiating-formats)</span><span class="sxs-lookup"><span data-stu-id="f833a-662">For more information, see [Negotiating Formats](#negotiating-formats).</span></span>

<span data-ttu-id="f833a-663">La seconda opzione è applicare i rettangoli quando **si imposta IDirect3DSwapChain9::P resent** specificando i parametri *pSourceRect* e *pDestRect* nel **metodo Present.**</span><span class="sxs-lookup"><span data-stu-id="f833a-663">The second option is to apply the rectangles when you **IDirect3DSwapChain9::Present** by specifying the *pSourceRect* and *pDestRect* parameters in the **Present** method.</span></span> <span data-ttu-id="f833a-664">È possibile combinare queste opzioni.</span><span class="sxs-lookup"><span data-stu-id="f833a-664">You can combine these options.</span></span> <span data-ttu-id="f833a-665">Ad esempio, è possibile impostare il rettangolo di origine sul mixer, ma applicare il rettangolo di destinazione nel **metodo** Present.</span><span class="sxs-lookup"><span data-stu-id="f833a-665">For example, you could set the source rectangle on the mixer but apply the destination rectangle in the **Present** method.</span></span>

<span data-ttu-id="f833a-666">Se l'applicazione modifica il rettangolo di destinazione o ridimensiona la finestra, potrebbe essere necessario allocare nuove superfici.</span><span class="sxs-lookup"><span data-stu-id="f833a-666">If the application changes the destination rectangle or resizes the window, you might need to allocate new surfaces.</span></span> <span data-ttu-id="f833a-667">In tal caso, è necessario prestare attenzione a sincronizzare questa operazione con il thread di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="f833a-667">If so, you must be careful to synchronize this operation with your scheduling thread.</span></span> <span data-ttu-id="f833a-668">Scaricare la coda di pianificazione ed eliminare i campioni precedenti prima di allocare nuove superfici.</span><span class="sxs-lookup"><span data-stu-id="f833a-668">Flush the scheduling queue and discard the old samples before allocating new surfaces.</span></span>

### <a name="end-of-stream"></a><span data-ttu-id="f833a-669">Fine del flusso</span><span class="sxs-lookup"><span data-stu-id="f833a-669">End of Stream</span></span>

<span data-ttu-id="f833a-670">Al termine di ogni flusso di input in EVR, L'EVR invia un **messaggio MFVP_MESSAGE_ENDOFSTREAM** al presentatore.</span><span class="sxs-lookup"><span data-stu-id="f833a-670">When every input stream on the EVR has ended, the EVR sends an **MFVP_MESSAGE_ENDOFSTREAM** message to the presenter.</span></span> <span data-ttu-id="f833a-671">Al momento della ricezione del messaggio, tuttavia, potrebbero rimanere alcuni fotogrammi video da elaborare.</span><span class="sxs-lookup"><span data-stu-id="f833a-671">At the point when you receive the message, however, there might be a few video frames remaining to be processed.</span></span> <span data-ttu-id="f833a-672">Prima di rispondere al messaggio di fine flusso, è necessario svuotare tutto l'output dal mixer e presentare tutti i fotogrammi rimanenti.</span><span class="sxs-lookup"><span data-stu-id="f833a-672">Before you respond to the end-of-stream message, you must drain all of the output from the mixer and present all of the remaining frames.</span></span> <span data-ttu-id="f833a-673">Dopo aver presentato l'ultimo frame, inviare **un evento EC_COMPLETE** all'EVR.</span><span class="sxs-lookup"><span data-stu-id="f833a-673">After the last frame is presented, send an **EC_COMPLETE** event to the EVR.</span></span>

<span data-ttu-id="f833a-674">Nell'esempio seguente viene illustrato un metodo che invia **l'EC_COMPLETE** evento se vengono soddisfatte diverse condizioni.</span><span class="sxs-lookup"><span data-stu-id="f833a-674">The next example shows a method that sends the **EC_COMPLETE** event if various conditions are met.</span></span> <span data-ttu-id="f833a-675">In caso contrario, restituisce S_OK senza inviare l'evento:</span><span class="sxs-lookup"><span data-stu-id="f833a-675">Otherwise, it returns S_OK without sending the event:</span></span>


```C++
HRESULT EVRCustomPresenter::CheckEndOfStream()
{
    if (!m_bEndStreaming)
    {
        // The EVR did not send the MFVP_MESSAGE_ENDOFSTREAM message.
        return S_OK;
    }

    if (m_bSampleNotify)
    {
        // The mixer still has input.
        return S_OK;
    }

    if (m_SamplePool.AreSamplesPending())
    {
        // Samples are still scheduled for rendering.
        return S_OK;
    }

    // Everything is complete. Now we can tell the EVR that we are done.
    NotifyEvent(EC_COMPLETE, (LONG_PTR)S_OK, 0);
    m_bEndStreaming = FALSE;
    return S_OK;
}
```



<span data-ttu-id="f833a-676">Questo metodo controlla gli stati seguenti:</span><span class="sxs-lookup"><span data-stu-id="f833a-676">This method checks the following states:</span></span>

-   <span data-ttu-id="f833a-677">Se la *m_fSampleNotify* è **TRUE,** significa che il mixer ha uno o più fotogrammi che non sono ancora stati elaborati.</span><span class="sxs-lookup"><span data-stu-id="f833a-677">If the *m_fSampleNotify* variable is **TRUE**, it means the mixer has one or more frames that have not been processed yet.</span></span> <span data-ttu-id="f833a-678">Per informazioni dettagliate, vedere [Elaborazione dell'output.](#processing-output)</span><span class="sxs-lookup"><span data-stu-id="f833a-678">(For details, see [Processing Output](#processing-output).)</span></span>
-   <span data-ttu-id="f833a-679">La *m_fEndStreaming* è un flag booleano il cui valore iniziale **è FALSE.**</span><span class="sxs-lookup"><span data-stu-id="f833a-679">The *m_fEndStreaming* variable is a Boolean flag whose initial value **FALSE**.</span></span> <span data-ttu-id="f833a-680">Il presentatore imposta il flag su **TRUE** quando EVR invia il **MFVP_MESSAGE_ENDOFSTREAM** messaggio.</span><span class="sxs-lookup"><span data-stu-id="f833a-680">The presenter sets the flag to **TRUE** when the EVR sends the **MFVP_MESSAGE_ENDOFSTREAM** message.</span></span>
-   <span data-ttu-id="f833a-681">Si `AreSamplesPending` presuppone che il metodo restituirà **TRUE** finché uno o più frame sono in attesa nella coda pianificata.</span><span class="sxs-lookup"><span data-stu-id="f833a-681">The `AreSamplesPending` method is assumed to return **TRUE** as long as one or more frames are waiting in the scheduled queue.</span></span>

<span data-ttu-id="f833a-682">Nel metodo [**IMFVideoPresenter::P rocessMessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) impostare *m_fEndStreaming* su **TRUE** e chiamare quando EVR invia il messaggio `CheckEndOfStream` **MFVP_MESSAGE_ENDOFSTREAM** seguente:</span><span class="sxs-lookup"><span data-stu-id="f833a-682">In the [**IMFVideoPresenter::ProcessMessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) method, set *m_fEndStreaming* to **TRUE** and call `CheckEndOfStream` when the EVR sends the **MFVP_MESSAGE_ENDOFSTREAM** message:</span></span>


```C++
HRESULT EVRCustomPresenter::ProcessMessage(
    MFVP_MESSAGE_TYPE eMessage,
    ULONG_PTR ulParam
    )
{
    HRESULT hr = S_OK;

    EnterCriticalSection(&m_ObjectLock);

    hr = CheckShutdown();
    if (FAILED(hr))
    {
        goto done;
    }

    switch (eMessage)
    {
    // Flush all pending samples.
    case MFVP_MESSAGE_FLUSH:
        hr = Flush();
        break;

    // Renegotiate the media type with the mixer.
    case MFVP_MESSAGE_INVALIDATEMEDIATYPE:
        hr = RenegotiateMediaType();
        break;

    // The mixer received a new input sample.
    case MFVP_MESSAGE_PROCESSINPUTNOTIFY:
        hr = ProcessInputNotify();
        break;

    // Streaming is about to start.
    case MFVP_MESSAGE_BEGINSTREAMING:
        hr = BeginStreaming();
        break;

    // Streaming has ended. (The EVR has stopped.)
    case MFVP_MESSAGE_ENDSTREAMING:
        hr = EndStreaming();
        break;

    // All input streams have ended.
    case MFVP_MESSAGE_ENDOFSTREAM:
        // Set the EOS flag.
        m_bEndStreaming = TRUE;
        // Check if it's time to send the EC_COMPLETE event to the EVR.
        hr = CheckEndOfStream();
        break;

    // Frame-stepping is starting.
    case MFVP_MESSAGE_STEP:
        hr = PrepareFrameStep(LODWORD(ulParam));
        break;

    // Cancels frame-stepping.
    case MFVP_MESSAGE_CANCELSTEP:
        hr = CancelFrameStep();
        break;

    default:
        hr = E_INVALIDARG; // Unknown message. This case should never occur.
        break;
    }

done:
    LeaveCriticalSection(&m_ObjectLock);
    return hr;
}
```



<span data-ttu-id="f833a-683">Chiamare anche se il metodo `CheckEndOfStream` [**IMFTransform::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) del mixer **restituisce MF_E_TRANSFORM_NEED_MORE_INPUT**.</span><span class="sxs-lookup"><span data-stu-id="f833a-683">In addition, call `CheckEndOfStream` if the mixer's [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) method returns **MF_E_TRANSFORM_NEED_MORE_INPUT**.</span></span> <span data-ttu-id="f833a-684">Questo codice di errore indica che il mixer non ha altri esempi di input (vedere [Output di elaborazione).](#processing-output)</span><span class="sxs-lookup"><span data-stu-id="f833a-684">This error code indicates that the mixer has no more input samples (see [Processing Output](#processing-output)).</span></span>

## <a name="frame-stepping"></a><span data-ttu-id="f833a-685">Esecuzione istruzione/istruzione dei frame</span><span class="sxs-lookup"><span data-stu-id="f833a-685">Frame Stepping</span></span>

<span data-ttu-id="f833a-686">EVR è progettato per supportare l'esecuzione di istruzioni dei frame in DirectShow e lo scrubbing in Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="f833a-686">The EVR is designed to support frame stepping in DirectShow and scrubbing in Media Foundation.</span></span> <span data-ttu-id="f833a-687">L'esecuzione di istruzioni e lo scrubbing dei frame sono concettualmente simili.</span><span class="sxs-lookup"><span data-stu-id="f833a-687">Frame stepping and scrubbing are conceptually similar.</span></span> <span data-ttu-id="f833a-688">In entrambi i casi, l'applicazione richiede un fotogramma video alla volta.</span><span class="sxs-lookup"><span data-stu-id="f833a-688">In both cases, the application requests one video frame at a time.</span></span> <span data-ttu-id="f833a-689">Internamente, il presentatore usa lo stesso meccanismo per implementare entrambe le funzionalità.</span><span class="sxs-lookup"><span data-stu-id="f833a-689">Internally, the presenter uses the same mechanism to implement both features.</span></span>

<span data-ttu-id="f833a-690">L'esecuzione di istruzioni dei frame in DirectShow funziona come segue:</span><span class="sxs-lookup"><span data-stu-id="f833a-690">Frame stepping in DirectShow works as follows:</span></span>

-   <span data-ttu-id="f833a-691">L'applicazione [**chiama IVideoFrameStep::Step**](/windows/win32/api/strmif/nf-strmif-ivideoframestep-step).</span><span class="sxs-lookup"><span data-stu-id="f833a-691">The application calls [**IVideoFrameStep::Step**](/windows/win32/api/strmif/nf-strmif-ivideoframestep-step).</span></span> <span data-ttu-id="f833a-692">Il numero di passaggi è specificato nel *parametro dwSteps.*</span><span class="sxs-lookup"><span data-stu-id="f833a-692">The number of steps is given in the *dwSteps* parameter.</span></span> <span data-ttu-id="f833a-693">EVR invia un **messaggio MFVP_MESSAGE_STEP** al presentatore, dove il parametro del messaggio (*ulParam*) è il numero di passaggi.</span><span class="sxs-lookup"><span data-stu-id="f833a-693">The EVR sends an **MFVP_MESSAGE_STEP** message to the presenter, where the message parameter (*ulParam*) is the number of steps.</span></span>
-   <span data-ttu-id="f833a-694">Se l'applicazione chiama [**IVideoFrameStep::CancelStep**](/windows/win32/api/strmif/nf-strmif-ivideoframestep-cancelstep) o modifica lo stato del grafo (in esecuzione, sospeso **o** arrestato), EVR invia MFVP_MESSAGE_CANCELSTEP messaggio.</span><span class="sxs-lookup"><span data-stu-id="f833a-694">If the application calls [**IVideoFrameStep::CancelStep**](/windows/win32/api/strmif/nf-strmif-ivideoframestep-cancelstep) or changes the graph state (running, paused, or stopped), the EVR sends an **MFVP_MESSAGE_CANCELSTEP** message.</span></span>

<span data-ttu-id="f833a-695">Lo scrubbing in Media Foundation funziona come segue:</span><span class="sxs-lookup"><span data-stu-id="f833a-695">Scrubbing in Media Foundation works as follows:</span></span>

-   <span data-ttu-id="f833a-696">L'applicazione imposta la velocità di riproduzione su zero chiamando [**IMFRateControl::SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate).</span><span class="sxs-lookup"><span data-stu-id="f833a-696">The application sets the playback rate to zero by calling [**IMFRateControl::SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate).</span></span>
-   <span data-ttu-id="f833a-697">Per eseguire il rendering di un nuovo frame, l'applicazione chiama [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) con la posizione desiderata.</span><span class="sxs-lookup"><span data-stu-id="f833a-697">To render a new frame, the application calls [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) with the desired position.</span></span> <span data-ttu-id="f833a-698">EVR invia un messaggio **MFVP_MESSAGE_STEP** con *ulParam* uguale a 1.</span><span class="sxs-lookup"><span data-stu-id="f833a-698">The EVR sends an **MFVP_MESSAGE_STEP** message with *ulParam* equal to 1.</span></span>
-   <span data-ttu-id="f833a-699">Per arrestare lo scrubbing, l'applicazione imposta la velocità di riproduzione su un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="f833a-699">To stop scrubbing, the application sets the playback rate to a nonzero value.</span></span> <span data-ttu-id="f833a-700">L'EVR invia il **MFVP_MESSAGE_CANCELSTEP** messaggio.</span><span class="sxs-lookup"><span data-stu-id="f833a-700">The EVR sends the **MFVP_MESSAGE_CANCELSTEP** message.</span></span>

<span data-ttu-id="f833a-701">Dopo aver ricevuto **il MFVP_MESSAGE_STEP,** il presentatore attende l'arrivo del frame di destinazione.</span><span class="sxs-lookup"><span data-stu-id="f833a-701">After receiving the **MFVP_MESSAGE_STEP** message, the presenter waits for the target frame to arrive.</span></span> <span data-ttu-id="f833a-702">Se il numero di passaggi è *N,* il presentatore rimuove i campioni successivi *(N* - 1) e presenta *il campione N.*</span><span class="sxs-lookup"><span data-stu-id="f833a-702">If the number of steps is *N*, the presenter discards the next (*N* - 1) samples and presents the *N* th sample.</span></span> <span data-ttu-id="f833a-703">Quando il presentatore completa il passaggio del frame, invia un evento [**EC_STEP_COMPLETE**](../directshow/ec-step-complete.md) all'EVR con *lParam1* impostato su **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="f833a-703">When the presenter completes the frame step, it sends an [**EC_STEP_COMPLETE**](../directshow/ec-step-complete.md) event to the EVR with *lParam1* set to **FALSE**.</span></span> <span data-ttu-id="f833a-704">Inoltre, se la velocità di riproduzione è zero, il presentatore invia un [**evento EC_SCRUB_TIME**](../directshow/ec-scrub-time.md) registrazione.</span><span class="sxs-lookup"><span data-stu-id="f833a-704">In addition, if the playback rate is zero, the presenter sends an [**EC_SCRUB_TIME**](../directshow/ec-scrub-time.md) event.</span></span> <span data-ttu-id="f833a-705">Se EVR annulla l'esecuzione istruzione/routine dei frame mentre un'operazione del passaggio del frame è ancora in sospeso, il presentatore invia un evento **EC_STEP_COMPLETE** con *lParam1* impostato su **TRUE.**</span><span class="sxs-lookup"><span data-stu-id="f833a-705">If the EVR cancels frame stepping while a frame-step operation is still pending, the presenter sends an **EC_STEP_COMPLETE** event with *lParam1* set to **TRUE**.</span></span>

<span data-ttu-id="f833a-706">L'applicazione può incorniciare il passaggio o  lo scrubbing più volte, in modo che il presentatore possa ricevere più messaggi MFVP_MESSAGE_STEP prima di ricevere un **MFVP_MESSAGE_CANCELSTEP** messaggio.</span><span class="sxs-lookup"><span data-stu-id="f833a-706">The application can frame step or scrub multiple times, so the presenter might receive multiple **MFVP_MESSAGE_STEP** messages before it gets an **MFVP_MESSAGE_CANCELSTEP** message.</span></span> <span data-ttu-id="f833a-707">Inoltre, il presentatore può ricevere il **messaggio MFVP_MESSAGE_STEP** prima dell'avvio dell'orologio o mentre l'orologio è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="f833a-707">Also, the presenter can receive the **MFVP_MESSAGE_STEP** message before the clock starts or while the clock is running.</span></span>

### <a name="implementing-frame-stepping"></a><span data-ttu-id="f833a-708">Implementazione dell'esecuzione di istruzioni dei frame</span><span class="sxs-lookup"><span data-stu-id="f833a-708">Implementing Frame Stepping</span></span>

<span data-ttu-id="f833a-709">In questa sezione viene descritto un algoritmo per implementare l'esecuzione di istruzioni dei frame.</span><span class="sxs-lookup"><span data-stu-id="f833a-709">This section describes an algorithm to implement frame stepping.</span></span> <span data-ttu-id="f833a-710">L'algoritmo di esecuzione delle istruzioni dei frame usa le variabili seguenti:</span><span class="sxs-lookup"><span data-stu-id="f833a-710">The frame stepping algorithm uses the following variables:</span></span>

-   <span data-ttu-id="f833a-711">*step_count*.</span><span class="sxs-lookup"><span data-stu-id="f833a-711">*step_count*.</span></span> <span data-ttu-id="f833a-712">Intero senza segno che specifica il numero di passaggi nell'operazione di esecuzione delle istruzioni del frame corrente.</span><span class="sxs-lookup"><span data-stu-id="f833a-712">An unsigned integer that specifies the number of steps in the current frame stepping operation.</span></span>
-   <span data-ttu-id="f833a-713">*step_queue*.</span><span class="sxs-lookup"><span data-stu-id="f833a-713">*step_queue*.</span></span> <span data-ttu-id="f833a-714">Coda di [**puntatori IMFSample.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)</span><span class="sxs-lookup"><span data-stu-id="f833a-714">A queue of [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) pointers.</span></span>
-   <span data-ttu-id="f833a-715">*step_state*.</span><span class="sxs-lookup"><span data-stu-id="f833a-715">*step_state*.</span></span> <span data-ttu-id="f833a-716">In qualsiasi momento, il presentatore può essere in uno degli stati seguenti per quanto riguarda l'esecuzione di istruzioni nei frame:</span><span class="sxs-lookup"><span data-stu-id="f833a-716">At any time, the presenter can be in one of the following states with respect to frame stepping:</span></span> 

    | <span data-ttu-id="f833a-717">State</span><span class="sxs-lookup"><span data-stu-id="f833a-717">State</span></span>         | <span data-ttu-id="f833a-718">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f833a-718">Description</span></span>                                                                                                                                                                                                     |
    |---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="f833a-719">NOT_STEPPING</span><span class="sxs-lookup"><span data-stu-id="f833a-719">NOT_STEPPING</span></span> | <span data-ttu-id="f833a-720">Non l'esecuzione di istruzioni nei frame.</span><span class="sxs-lookup"><span data-stu-id="f833a-720">Not frame stepping.</span></span>                                                                                                                                                                                             |
    | <span data-ttu-id="f833a-721">WAITING</span><span class="sxs-lookup"><span data-stu-id="f833a-721">WAITING</span></span>       | <span data-ttu-id="f833a-722">Il presentatore ha ricevuto il **messaggio MFVP_MESSAGE_STEP,** ma l'orologio non è stato avviato.</span><span class="sxs-lookup"><span data-stu-id="f833a-722">The presenter has received the **MFVP_MESSAGE_STEP** message, but the clock has not started.</span></span>                                                                                                                  |
    | <span data-ttu-id="f833a-723">PENDING</span><span class="sxs-lookup"><span data-stu-id="f833a-723">PENDING</span></span>       | <span data-ttu-id="f833a-724">Il presentatore ha ricevuto il **messaggio MFVP_MESSAGE_STEP** e l'orologio è stato avviato, ma il presentatore è in attesa di ricevere il frame di destinazione.</span><span class="sxs-lookup"><span data-stu-id="f833a-724">The presenter has received the **MFVP_MESSAGE_STEP** message and the clock has started, but the presenter is waiting to receive the target frame.</span></span>                                                             |
    | <span data-ttu-id="f833a-725">Programmato</span><span class="sxs-lookup"><span data-stu-id="f833a-725">SCHEDULED</span></span>     | <span data-ttu-id="f833a-726">Il presentatore ha ricevuto il frame di destinazione e lo ha pianificato per la presentazione, ma il frame non è stato presentato.</span><span class="sxs-lookup"><span data-stu-id="f833a-726">The presenter has received the target frame and has scheduled it for presentation, but the frame has not been presented.</span></span>                                                                                        |
    | <span data-ttu-id="f833a-727">Completo</span><span class="sxs-lookup"><span data-stu-id="f833a-727">COMPLETE</span></span>      | <span data-ttu-id="f833a-728">Il presentatore ha presentato il frame di destinazione e inviato [**l'evento EC_STEP_COMPLETE**](../directshow/ec-step-complete.md) ed è in attesa del messaggio MFVP_MESSAGE_STEP **o** **MFVP_MESSAGE_CANCELSTEP** successivo.</span><span class="sxs-lookup"><span data-stu-id="f833a-728">The presenter has presented the target frame and sent the [**EC_STEP_COMPLETE**](../directshow/ec-step-complete.md) event, and is waiting for the next **MFVP_MESSAGE_STEP** or **MFVP_MESSAGE_CANCELSTEP** message.</span></span> |

    

     

    <span data-ttu-id="f833a-729">Questi stati sono indipendenti dagli stati del presentatore elencati nella sezione [Stati del presentatore](#presenter-states).</span><span class="sxs-lookup"><span data-stu-id="f833a-729">These states are independent of the presenter states listed in the section [Presenter States](#presenter-states).</span></span>

<span data-ttu-id="f833a-730">Per l'algoritmo frame-stepping vengono definite le procedure seguenti:</span><span class="sxs-lookup"><span data-stu-id="f833a-730">The following procedures are defined for the frame-stepping algorithm:</span></span>

<span data-ttu-id="f833a-731">Procedura PrepareFrameStep</span><span class="sxs-lookup"><span data-stu-id="f833a-731">PrepareFrameStep Procedure</span></span>

1.  <span data-ttu-id="f833a-732">Incrementare *step_count*.</span><span class="sxs-lookup"><span data-stu-id="f833a-732">Increment *step_count*.</span></span>
2.  <span data-ttu-id="f833a-733">Impostare *step_state* su WAITING.</span><span class="sxs-lookup"><span data-stu-id="f833a-733">Set *step_state* to WAITING.</span></span>
3.  <span data-ttu-id="f833a-734">Se l'orologio è in esecuzione, chiamare StartFrameStep.</span><span class="sxs-lookup"><span data-stu-id="f833a-734">If the clock is running, call StartFrameStep.</span></span>

<span data-ttu-id="f833a-735">Procedura StartFrameStep</span><span class="sxs-lookup"><span data-stu-id="f833a-735">StartFrameStep Procedure</span></span>

1.  <span data-ttu-id="f833a-736">Se *step_state* è uguale a WAITING, impostare *step_state* su PENDING.</span><span class="sxs-lookup"><span data-stu-id="f833a-736">If *step_state* equals WAITING, set *step_state* to PENDING.</span></span> <span data-ttu-id="f833a-737">Per ogni esempio in *step_queue*, chiamare DeliverFrameStepSample.</span><span class="sxs-lookup"><span data-stu-id="f833a-737">For each sample in *step_queue*, call DeliverFrameStepSample.</span></span>
2.  <span data-ttu-id="f833a-738">Se *step_state* è uguale NOT_STEPPING, rimuovere tutti gli esempi *step_queue* e pianificarli per la presentazione.</span><span class="sxs-lookup"><span data-stu-id="f833a-738">If *step_state* equals NOT_STEPPING, remove any samples from *step_queue* and schedule them for presentation.</span></span>

<span data-ttu-id="f833a-739">Procedura CompleteFrameStep</span><span class="sxs-lookup"><span data-stu-id="f833a-739">CompleteFrameStep Procedure</span></span>

1.  <span data-ttu-id="f833a-740">Impostare *step_state* su COMPLETE.</span><span class="sxs-lookup"><span data-stu-id="f833a-740">Set *step_state* to COMPLETE.</span></span>
2.  <span data-ttu-id="f833a-741">Inviare l EC_STEP_COMPLETE eventi con *lParam1*  =  **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="f833a-741">Send the EC_STEP_COMPLETE event with *lParam1* = **FALSE**.</span></span>
3.  <span data-ttu-id="f833a-742">Se la frequenza di clock è zero, inviare **l'evento EC_SCRUB_TIME** con l'ora di esempio.</span><span class="sxs-lookup"><span data-stu-id="f833a-742">If the clock rate is zero, send the **EC_SCRUB_TIME** event with the sample time.</span></span>

<span data-ttu-id="f833a-743">Procedura DeliverFrameStepSample</span><span class="sxs-lookup"><span data-stu-id="f833a-743">DeliverFrameStepSample Procedure</span></span>

1.  <span data-ttu-id="f833a-744">Se la frequenza di clock è pari a zero e *la durata* del campione del campione  +    <  *di esempio è ,* rimuovere il campione.</span><span class="sxs-lookup"><span data-stu-id="f833a-744">If the clock rate is zero and *sample time* + *sample duration* < *clock time*, discard the sample.</span></span> <span data-ttu-id="f833a-745">Exit.</span><span class="sxs-lookup"><span data-stu-id="f833a-745">Exit.</span></span>
2.  <span data-ttu-id="f833a-746">Se *step_state* è uguale a SCHEDULED o COMPLETE, aggiungere l'esempio *a step_queue*.</span><span class="sxs-lookup"><span data-stu-id="f833a-746">If *step_state* equals SCHEDULED or COMPLETE, add the sample to *step_queue*.</span></span> <span data-ttu-id="f833a-747">Exit.</span><span class="sxs-lookup"><span data-stu-id="f833a-747">Exit.</span></span>
3.  <span data-ttu-id="f833a-748">Decremento *step_count*.</span><span class="sxs-lookup"><span data-stu-id="f833a-748">Decrement *step_count*.</span></span>
4.  <span data-ttu-id="f833a-749">Se *step_count* > 0, eliminare l'esempio.</span><span class="sxs-lookup"><span data-stu-id="f833a-749">If *step_count* > 0, discard the sample.</span></span> <span data-ttu-id="f833a-750">Exit.</span><span class="sxs-lookup"><span data-stu-id="f833a-750">Exit.</span></span>
5.  <span data-ttu-id="f833a-751">Se *step_state* è uguale a WAITING, aggiungere l'esempio *a step_queue*.</span><span class="sxs-lookup"><span data-stu-id="f833a-751">If *step_state* equals WAITING, add the sample to *step_queue*.</span></span> <span data-ttu-id="f833a-752">Exit.</span><span class="sxs-lookup"><span data-stu-id="f833a-752">Exit.</span></span>
6.  <span data-ttu-id="f833a-753">Pianificare l'esempio per la presentazione.</span><span class="sxs-lookup"><span data-stu-id="f833a-753">Schedule the sample for presentation.</span></span>
7.  <span data-ttu-id="f833a-754">Impostare *step_state* su SCHEDULED.</span><span class="sxs-lookup"><span data-stu-id="f833a-754">Set *step_state* to SCHEDULED.</span></span>

<span data-ttu-id="f833a-755">Procedura CancelFrameStep</span><span class="sxs-lookup"><span data-stu-id="f833a-755">CancelFrameStep Procedure</span></span>

1.  <span data-ttu-id="f833a-756">Impostare *step_state* su NOT_STEPPING</span><span class="sxs-lookup"><span data-stu-id="f833a-756">Set *step_state* to NOT_STEPPING</span></span>
2.  <span data-ttu-id="f833a-757">Reimpostare *step_count* su zero.</span><span class="sxs-lookup"><span data-stu-id="f833a-757">Reset *step_count* to zero.</span></span>
3.  <span data-ttu-id="f833a-758">Se il valore precedente di *step_state* è WAITING, PENDING o SCHEDULED, inviare EC_STEP_COMPLETE *con lParam1*  =  **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="f833a-758">If the previous value of *step_state* was WAITING, PENDING, or SCHEDULED, send EC_STEP_COMPLETE with *lParam1* = **TRUE**.</span></span>

<span data-ttu-id="f833a-759">Chiamare queste procedure nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="f833a-759">Call these procedures as follows:</span></span>



| <span data-ttu-id="f833a-760">Metodo o messaggio del presentatore</span><span class="sxs-lookup"><span data-stu-id="f833a-760">Presenter message or method</span></span>                                                   | <span data-ttu-id="f833a-761">Procedura</span><span class="sxs-lookup"><span data-stu-id="f833a-761">Procedure</span></span>           |
|-------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="f833a-762">**MFVP_MESSAGE_STEP** messaggio</span><span class="sxs-lookup"><span data-stu-id="f833a-762">**MFVP_MESSAGE_STEP** message</span></span>                                               | `PrepareFrameStep`  |
| <span data-ttu-id="f833a-763">**MFVP_MESSAGE_STEP** messaggio</span><span class="sxs-lookup"><span data-stu-id="f833a-763">**MFVP_MESSAGE_STEP** message</span></span>                                               | `CancelStep`        |
| [<span data-ttu-id="f833a-764">**IMFClockStateSink::OnClockStart**</span><span class="sxs-lookup"><span data-stu-id="f833a-764">**IMFClockStateSink::OnClockStart**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart)     | `StartFrameStep`    |
| [<span data-ttu-id="f833a-765">**IMFClockStateSink::OnClockRestart**</span><span class="sxs-lookup"><span data-stu-id="f833a-765">**IMFClockStateSink::OnClockRestart**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart) | `StartFrameStep`    |
| <span data-ttu-id="f833a-766">Callback [**di IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample)</span><span class="sxs-lookup"><span data-stu-id="f833a-766">[**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) callback</span></span>                         | `CompleteFrameStep` |
| [<span data-ttu-id="f833a-767">**IMFClockStateSink::OnClockStop**</span><span class="sxs-lookup"><span data-stu-id="f833a-767">**IMFClockStateSink::OnClockStop**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstop)       | `CancelFrameStep`   |
| [<span data-ttu-id="f833a-768">**IMFClockStateSink::OnClockSetRate**</span><span class="sxs-lookup"><span data-stu-id="f833a-768">**IMFClockStateSink::OnClockSetRate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) | `CancelFrameStep`   |



 

<span data-ttu-id="f833a-769">Il diagramma di flusso seguente illustra le procedure di creazione di istruzioni per i frame.</span><span class="sxs-lookup"><span data-stu-id="f833a-769">The following flow chart shows the frame-stepping procedures.</span></span>

![Diagramma di flusso che mostra i percorsi che iniziano con mfvp \- message \- step e mfvp \- message \- processinputnotify e terminano con "state = complete"](images/d9baaa67-a9b1-4e27-9a32-08a45b0677d3.gif)

## <a name="setting-the-presenter-on-the-evr"></a><span data-ttu-id="f833a-771">Impostazione del presentatore nell'EVR</span><span class="sxs-lookup"><span data-stu-id="f833a-771">Setting the Presenter on the EVR</span></span>

<span data-ttu-id="f833a-772">Dopo aver implementato il presentatore, il passaggio successivo consiste nel configurare EVR per usarlo.</span><span class="sxs-lookup"><span data-stu-id="f833a-772">After implementing the presenter, the next step is to configure the EVR to use it.</span></span>

### <a name="setting-the-presenter-in-directshow"></a><span data-ttu-id="f833a-773">Impostazione del presentatore in DirectShow</span><span class="sxs-lookup"><span data-stu-id="f833a-773">Setting the Presenter in DirectShow</span></span>

<span data-ttu-id="f833a-774">In un'applicazione DirectShow impostare il presentatore in EVR come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="f833a-774">In a DirectShow application, set the presenter on the EVR as follows:</span></span>

1.  <span data-ttu-id="f833a-775">Creare il filtro EVR chiamando **CoCreateInstance.**</span><span class="sxs-lookup"><span data-stu-id="f833a-775">Create the EVR filter by calling **CoCreateInstance**.</span></span> <span data-ttu-id="f833a-776">Il CLSID è **CLSID_EnhancedVideoRenderer**.</span><span class="sxs-lookup"><span data-stu-id="f833a-776">The CLSID is **CLSID_EnhancedVideoRenderer**.</span></span>
2.  <span data-ttu-id="f833a-777">Aggiungere l'EVR al grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="f833a-777">Add the EVR to the filter graph.</span></span>
3.  <span data-ttu-id="f833a-778">Creare un'istanza del presentatore.</span><span class="sxs-lookup"><span data-stu-id="f833a-778">Create an instance of your presenter.</span></span> <span data-ttu-id="f833a-779">Il presentatore può supportare la creazione di oggetti COM standard **tramite IClassFactory,** ma questo non è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="f833a-779">Your presenter can support standard COM object creation through **IClassFactory**, but this is not mandatory.</span></span>
4.  <span data-ttu-id="f833a-780">Eseguire una query sul filtro EVR per [**l'interfaccia IMFVideoRenderer.**](/windows/desktop/api/evr/nn-evr-imfvideorenderer)</span><span class="sxs-lookup"><span data-stu-id="f833a-780">Query the EVR filter for the [**IMFVideoRenderer**](/windows/desktop/api/evr/nn-evr-imfvideorenderer) interface.</span></span>
5.  <span data-ttu-id="f833a-781">Chiamare [**IMFVideoRenderer::InitializeRenderer**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer).</span><span class="sxs-lookup"><span data-stu-id="f833a-781">Call [**IMFVideoRenderer::InitializeRenderer**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer).</span></span>

### <a name="setting-the-presenter-in-media-foundation"></a><span data-ttu-id="f833a-782">Impostazione del presenter in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f833a-782">Setting the Presenter in Media Foundation</span></span>

<span data-ttu-id="f833a-783">In Media Foundation sono disponibili diverse opzioni, a seconda che si crei il sink del supporto EVR o l'oggetto di attivazione EVR.</span><span class="sxs-lookup"><span data-stu-id="f833a-783">In Media Foundation, you have several options, depending on whether you create the EVR media sink or the EVR activation object.</span></span> <span data-ttu-id="f833a-784">Per altre informazioni sugli oggetti attivazione, vedere [Oggetti di attivazione.](activation-objects.md)</span><span class="sxs-lookup"><span data-stu-id="f833a-784">For more information about activation objects, see [Activation Objects](activation-objects.md).</span></span>

<span data-ttu-id="f833a-785">Per il sink del supporto EVR, eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="f833a-785">For the EVR media sink, do the following:</span></span>

1.  <span data-ttu-id="f833a-786">Chiamare [**MFCreateVideoRenderer**](/windows/desktop/api/evr/nc-evr-mfcreatevideorenderer) per creare il sink multimediale.</span><span class="sxs-lookup"><span data-stu-id="f833a-786">Call [**MFCreateVideoRenderer**](/windows/desktop/api/evr/nc-evr-mfcreatevideorenderer) to create the media sink.</span></span>
2.  <span data-ttu-id="f833a-787">Creare un'istanza del presentatore.</span><span class="sxs-lookup"><span data-stu-id="f833a-787">Create an instance of your presenter.</span></span>
3.  <span data-ttu-id="f833a-788">Eseguire una query sul sink dei supporti EVR per [**l'interfaccia IMFVideoRenderer.**](/windows/desktop/api/evr/nn-evr-imfvideorenderer)</span><span class="sxs-lookup"><span data-stu-id="f833a-788">Query the EVR media sink for the [**IMFVideoRenderer**](/windows/desktop/api/evr/nn-evr-imfvideorenderer) interface.</span></span>
4.  <span data-ttu-id="f833a-789">Chiamare [**IMFVideoRenderer::InitializeRenderer**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer).</span><span class="sxs-lookup"><span data-stu-id="f833a-789">Call [**IMFVideoRenderer::InitializeRenderer**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer).</span></span>

<span data-ttu-id="f833a-790">Per l'oggetto attivazione EVR, eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="f833a-790">For the EVR activation object, do the following:</span></span>

1.  <span data-ttu-id="f833a-791">Chiamare [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) per creare l'oggetto attivazione.</span><span class="sxs-lookup"><span data-stu-id="f833a-791">Call [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) to create the activation object.</span></span>
2.  <span data-ttu-id="f833a-792">Impostare uno degli attributi seguenti nell'oggetto attivazione:</span><span class="sxs-lookup"><span data-stu-id="f833a-792">Set one of the following attributes on the activation object:</span></span> 

    | <span data-ttu-id="f833a-793">Attributo</span><span class="sxs-lookup"><span data-stu-id="f833a-793">Attribute</span></span>                                                                                                         | <span data-ttu-id="f833a-794">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f833a-794">Description</span></span>                                                                                                                                                                                                                               |
    |-------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | [<span data-ttu-id="f833a-795">**MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_ACTIVATE**</span><span class="sxs-lookup"><span data-stu-id="f833a-795">**MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_ACTIVATE**</span></span>](mf-activate-custom-video-presenter-activate-attribute.md) | <span data-ttu-id="f833a-796">Puntatore a un oggetto attivazione per il presentatore.</span><span class="sxs-lookup"><span data-stu-id="f833a-796">Pointer to an activation object for the presenter.</span></span><br/> <span data-ttu-id="f833a-797">Con questo flag, è necessario fornire un oggetto attivazione per il presentatore.</span><span class="sxs-lookup"><span data-stu-id="f833a-797">With this flag, you must provide an activation object for your presenter.</span></span> <span data-ttu-id="f833a-798">L'oggetto attivazione deve implementare [**l'interfaccia IMFActivate.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)</span><span class="sxs-lookup"><span data-stu-id="f833a-798">The activation object must implement the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface.</span></span><br/> |
    | [<span data-ttu-id="f833a-799">**MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_CLSID**</span><span class="sxs-lookup"><span data-stu-id="f833a-799">**MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_CLSID**</span></span>](mf-activate-custom-video-presenter-clsid-attribute.md)       | <span data-ttu-id="f833a-800">CLSID del presentatore.</span><span class="sxs-lookup"><span data-stu-id="f833a-800">CLSID of the presenter.</span></span><br/> <span data-ttu-id="f833a-801">Con questo flag, il presentatore deve supportare la creazione di oggetti COM standard tramite **IClassFactory**.</span><span class="sxs-lookup"><span data-stu-id="f833a-801">With this flag, your presenter must support standard COM object creation through **IClassFactory**.</span></span><br/>                                                                                         |

    

     

3.  <span data-ttu-id="f833a-802">Facoltativamente, impostare [**l'attributo MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_FLAGS**](mf-activate-custom-video-presenter-flags-attribute.md) nell'oggetto di attivazione.</span><span class="sxs-lookup"><span data-stu-id="f833a-802">Optionally, set the [**MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_FLAGS**](mf-activate-custom-video-presenter-flags-attribute.md) attribute on the activation object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f833a-803">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f833a-803">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f833a-804">Renderer video avanzato</span><span class="sxs-lookup"><span data-stu-id="f833a-804">Enhanced Video Renderer</span></span>](enhanced-video-renderer.md)
</dt> <dt>

[<span data-ttu-id="f833a-805">Esempio di EVRPresenter</span><span class="sxs-lookup"><span data-stu-id="f833a-805">EVRPresenter Sample</span></span>](evrpresenter-sample.md)
</dt> </dl>

 

 
