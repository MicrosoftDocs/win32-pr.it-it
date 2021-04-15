---
description: L'elaborazione video di DXVA incapsula le funzioni dell'hardware grafico dedicato all'elaborazione di immagini video non compresse. I servizi di elaborazione video includono la deinterlacciamento e la combinazione di video.
ms.assetid: bd688f81-4b7c-4016-b0bd-e40782131f8e
title: Elaborazione video DXVA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcf5058d93ddd7c506a501eb6ca07c4661755fc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524545"
---
# <a name="dxva-video-processing"></a><span data-ttu-id="d1026-104">Elaborazione video DXVA</span><span class="sxs-lookup"><span data-stu-id="d1026-104">DXVA Video Processing</span></span>

<span data-ttu-id="d1026-105">L'elaborazione video di DXVA incapsula le funzioni dell'hardware grafico dedicato all'elaborazione di immagini video non compresse.</span><span class="sxs-lookup"><span data-stu-id="d1026-105">DXVA video processing encapsulates the functions of the graphics hardware that are devoted to processing uncompressed video images.</span></span> <span data-ttu-id="d1026-106">I servizi di elaborazione video includono la deinterlacciamento e la combinazione di video.</span><span class="sxs-lookup"><span data-stu-id="d1026-106">Video processing services include deinterlacing and video mixing.</span></span>

<span data-ttu-id="d1026-107">In questo argomento sono incluse le sezioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="d1026-107">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="d1026-108">Overview</span><span class="sxs-lookup"><span data-stu-id="d1026-108">Overview</span></span>](#overview)
-   [<span data-ttu-id="d1026-109">Creazione di un dispositivo di elaborazione video</span><span class="sxs-lookup"><span data-stu-id="d1026-109">Creating a Video Processing Device</span></span>](#creating-a-video-processing-device)
    -   [<span data-ttu-id="d1026-110">Ottenere il puntatore IDirectXVideoProcessorService</span><span class="sxs-lookup"><span data-stu-id="d1026-110">Get the IDirectXVideoProcessorService Pointer</span></span>](#get-the-idirectxvideoprocessorservice-pointer)
    -   [<span data-ttu-id="d1026-111">Enumerare i dispositivi di elaborazione video</span><span class="sxs-lookup"><span data-stu-id="d1026-111">Enumerate the Video Processing Devices</span></span>](#enumerate-the-video-processing-devices)
    -   [<span data-ttu-id="d1026-112">Enumerare i formati di Render-Target</span><span class="sxs-lookup"><span data-stu-id="d1026-112">Enumerate Render-Target Formats</span></span>](#enumerate-render-target-formats)
    -   [<span data-ttu-id="d1026-113">Eseguire query sulle funzionalità del dispositivo</span><span class="sxs-lookup"><span data-stu-id="d1026-113">Query the Device Capabilities</span></span>](#query-the-device-capabilities)
    -   [<span data-ttu-id="d1026-114">Creare il dispositivo</span><span class="sxs-lookup"><span data-stu-id="d1026-114">Create the Device</span></span>](#create-the-device)
-   [<span data-ttu-id="d1026-115">Blit processo video</span><span class="sxs-lookup"><span data-stu-id="d1026-115">Video Process Blit</span></span>](#video-process-blit)
    -   [<span data-ttu-id="d1026-116">Parametri blit</span><span class="sxs-lookup"><span data-stu-id="d1026-116">Blit Parameters</span></span>](#blit-parameters)
    -   [<span data-ttu-id="d1026-117">Esempi di input</span><span class="sxs-lookup"><span data-stu-id="d1026-117">Input Samples</span></span>](#input-samples)
-   [<span data-ttu-id="d1026-118">Composizione immagine</span><span class="sxs-lookup"><span data-stu-id="d1026-118">Image Composition</span></span>](#image-composition)
    -   [<span data-ttu-id="d1026-119">Esempio 1: Letterbox</span><span class="sxs-lookup"><span data-stu-id="d1026-119">Example 1: Letterboxing</span></span>](#example-1-letterboxing)
    -   [<span data-ttu-id="d1026-120">Esempio 2: estensione delle immagini del sottoflusso</span><span class="sxs-lookup"><span data-stu-id="d1026-120">Example 2: Stretching Substream Images</span></span>](#example-2-stretching-substream-images)
    -   [<span data-ttu-id="d1026-121">Esempio 3: mancata corrispondenza tra le altezze di flusso</span><span class="sxs-lookup"><span data-stu-id="d1026-121">Example 3: Mismatched Stream Heights</span></span>](#example-3-mismatched-stream-heights)
    -   [<span data-ttu-id="d1026-122">Esempio 4: rettangolo di destinazione più piccolo della superficie di destinazione</span><span class="sxs-lookup"><span data-stu-id="d1026-122">Example 4: Target Rectangle Smaller Than Destination Surface</span></span>](#example-4-target-rectangle-smaller-than-destination-surface)
    -   [<span data-ttu-id="d1026-123">Esempio 5: rettangoli di origine</span><span class="sxs-lookup"><span data-stu-id="d1026-123">Example 5: Source Rectangles</span></span>](#example-5-source-rectangles)
    -   [<span data-ttu-id="d1026-124">Esempio 6: intersezione di rettangoli di destinazione</span><span class="sxs-lookup"><span data-stu-id="d1026-124">Example 6: Intersecting Destination Rectangles</span></span>](#example-6-intersecting-destination-rectangles)
    -   [<span data-ttu-id="d1026-125">Esempio 7: allungamento e ritaglio di video</span><span class="sxs-lookup"><span data-stu-id="d1026-125">Example 7: Stretching and Cropping Video</span></span>](#example-7-stretching-and-cropping-video)
-   [<span data-ttu-id="d1026-126">Ordine di esempio di input</span><span class="sxs-lookup"><span data-stu-id="d1026-126">Input Sample Order</span></span>](#input-sample-order)
    -   [<span data-ttu-id="d1026-127">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d1026-127">Example 1</span></span>](#example-1-letterboxing)
    -   [<span data-ttu-id="d1026-128">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="d1026-128">Example 2</span></span>](#example-2-stretching-substream-images)
    -   [<span data-ttu-id="d1026-129">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="d1026-129">Example 3</span></span>](#example-3-mismatched-stream-heights)
    -   [<span data-ttu-id="d1026-130">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="d1026-130">Example 4</span></span>](#example-4-target-rectangle-smaller-than-destination-surface)
-   [<span data-ttu-id="d1026-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d1026-131">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="d1026-132">Panoramica</span><span class="sxs-lookup"><span data-stu-id="d1026-132">Overview</span></span>

<span data-ttu-id="d1026-133">L'hardware grafico può utilizzare l'unità di elaborazione grafica (GPU) per elaborare immagini video non compresse.</span><span class="sxs-lookup"><span data-stu-id="d1026-133">Graphics hardware can use the graphics processing unit (GPU) to process uncompressed video images.</span></span> <span data-ttu-id="d1026-134">Un dispositivo di *elaborazione video* è un componente software che incapsula queste funzioni.</span><span class="sxs-lookup"><span data-stu-id="d1026-134">A *video processing* device is a software component that encapsulates these functions.</span></span> <span data-ttu-id="d1026-135">Le applicazioni possono utilizzare un dispositivo di elaborazione video per eseguire funzioni quali:</span><span class="sxs-lookup"><span data-stu-id="d1026-135">Applications can use a video processing device to perform functions such as:</span></span>

-   <span data-ttu-id="d1026-136">Deinterlacciamento e telecine inverso</span><span class="sxs-lookup"><span data-stu-id="d1026-136">Deinterlacing and inverse telecine</span></span>
-   <span data-ttu-id="d1026-137">Combinazione di sottoflussi video nell'immagine video principale</span><span class="sxs-lookup"><span data-stu-id="d1026-137">Mixing video substreams onto the main video image</span></span>
-   <span data-ttu-id="d1026-138">Regolazione del colore (ProcAmp) e filtro delle immagini</span><span class="sxs-lookup"><span data-stu-id="d1026-138">Color adjustment (ProcAmp) and image filtering</span></span>
-   <span data-ttu-id="d1026-139">Ridimensionamento delle immagini</span><span class="sxs-lookup"><span data-stu-id="d1026-139">Image scaling</span></span>
-   <span data-ttu-id="d1026-140">Conversione dello spazio colore</span><span class="sxs-lookup"><span data-stu-id="d1026-140">Color-space conversion</span></span>
-   <span data-ttu-id="d1026-141">Fusione alfa</span><span class="sxs-lookup"><span data-stu-id="d1026-141">Alpha blending</span></span>

<span data-ttu-id="d1026-142">Il diagramma seguente illustra le fasi della pipeline di elaborazione video.</span><span class="sxs-lookup"><span data-stu-id="d1026-142">The following diagram shows the stages in the video processing pipeline.</span></span> <span data-ttu-id="d1026-143">Il diagramma non ha lo scopo di mostrare un'implementazione effettiva.</span><span class="sxs-lookup"><span data-stu-id="d1026-143">The diagram is not meant to show an actual implementation.</span></span> <span data-ttu-id="d1026-144">Ad esempio, il driver di grafica potrebbe combinare varie fasi in un'unica operazione.</span><span class="sxs-lookup"><span data-stu-id="d1026-144">For example, the graphics driver might combine several stages into a single operation.</span></span> <span data-ttu-id="d1026-145">Tutte queste operazioni possono essere eseguite in una singola chiamata al dispositivo di elaborazione video.</span><span class="sxs-lookup"><span data-stu-id="d1026-145">All of these operations can be performed in a single call to the video processing device.</span></span> <span data-ttu-id="d1026-146">Alcune fasi illustrate di seguito, ad esempio il filtro rumore e i dettagli, potrebbero non essere supportate dal driver.</span><span class="sxs-lookup"><span data-stu-id="d1026-146">Some stages shown here, such as noise and detail filtering, might not be supported by the driver.</span></span>

![diagramma che mostra le fasi dell'elaborazione video di DXVA.](images/8581554e-a1bc-4cab-9ae1-99a6537e2a84.gif)

<span data-ttu-id="d1026-148">L'input per la pipeline di elaborazione video include sempre un flusso video *primario* , che contiene i dati dell'immagine principale.</span><span class="sxs-lookup"><span data-stu-id="d1026-148">The input to the video processing pipeline always includes a *primary* video stream, which contains the main image data.</span></span> <span data-ttu-id="d1026-149">Il flusso video primario determina la frequenza dei fotogrammi per il video di output.</span><span class="sxs-lookup"><span data-stu-id="d1026-149">The primary video stream determines the frame rate for the output video.</span></span> <span data-ttu-id="d1026-150">Ogni frame del video di output viene calcolato in relazione ai dati di input dal flusso video primario.</span><span class="sxs-lookup"><span data-stu-id="d1026-150">Each frame of the output video is calculated relative to the input data from the primary video stream.</span></span> <span data-ttu-id="d1026-151">I pixel nel flusso primario sono sempre opachi, senza dati alfa per pixel.</span><span class="sxs-lookup"><span data-stu-id="d1026-151">Pixels in the primary stream are always opaque, with no per-pixel alpha data.</span></span> <span data-ttu-id="d1026-152">Il flusso video primario può essere progressivo o interlacciato.</span><span class="sxs-lookup"><span data-stu-id="d1026-152">The primary video stream can be progressive or interlaced.</span></span>

<span data-ttu-id="d1026-153">Facoltativamente, la pipeline di elaborazione video può ricevere fino a 15 sottoflussi video.</span><span class="sxs-lookup"><span data-stu-id="d1026-153">Optionally, the video processing pipeline can receive up to 15 video substreams.</span></span> <span data-ttu-id="d1026-154">Un sottoflusso contiene dati di immagine ausiliari, ad esempio didascalie chiuse o immagini secondarie di DVD.</span><span class="sxs-lookup"><span data-stu-id="d1026-154">A substream contains auxiliary image data, such as closed captions or DVD subpictures.</span></span> <span data-ttu-id="d1026-155">Queste immagini vengono visualizzate sul flusso video primario e in genere non sono destinate a essere visualizzate da soli.</span><span class="sxs-lookup"><span data-stu-id="d1026-155">These images are displayed over the primary video stream, and are generally not meant to be shown by themselves.</span></span> <span data-ttu-id="d1026-156">Le immagini di flussi secondari possono contenere dati alfa per pixel e sono sempre frame progressivi.</span><span class="sxs-lookup"><span data-stu-id="d1026-156">Substream pictures can contain per-pixel alpha data, and are always progressive frames.</span></span> <span data-ttu-id="d1026-157">Il dispositivo di elaborazione video Alpha-combina le immagini del sottoflusso con il frame deinterlacciato corrente dal flusso video primario.</span><span class="sxs-lookup"><span data-stu-id="d1026-157">The video processing device alpha-blends the substream images with the current deinterlaced frame from the primary video stream.</span></span>

<span data-ttu-id="d1026-158">Nella parte restante di questo argomento, il termine *immagine* viene usato per i dati di input in un dispositivo di elaborazione video.</span><span class="sxs-lookup"><span data-stu-id="d1026-158">In the remainder of this topic, the term *picture* is used for the input data to a video processing device.</span></span> <span data-ttu-id="d1026-159">Un'immagine può essere costituita da un frame progressivo, da un singolo campo o da due campi con interfoliazione.</span><span class="sxs-lookup"><span data-stu-id="d1026-159">A picture might consist of a progressive frame, a single field, or two interleaved fields.</span></span> <span data-ttu-id="d1026-160">L'output è sempre un frame deinterlacciato.</span><span class="sxs-lookup"><span data-stu-id="d1026-160">The output is always a deinterlaced frame.</span></span>

<span data-ttu-id="d1026-161">Un driver video può implementare più di un dispositivo di elaborazione video per fornire diversi set di funzionalità di elaborazione video.</span><span class="sxs-lookup"><span data-stu-id="d1026-161">A video driver can implement more than one video processing device, to provide different sets of video processing capabilities.</span></span> <span data-ttu-id="d1026-162">I dispositivi sono identificati dal GUID.</span><span class="sxs-lookup"><span data-stu-id="d1026-162">Devices are identified by GUID.</span></span> <span data-ttu-id="d1026-163">I GUID seguenti sono predefiniti:</span><span class="sxs-lookup"><span data-stu-id="d1026-163">The following GUIDs are predefined:</span></span>

-   <span data-ttu-id="d1026-164">**DXVA2 \_ VideoProcBobDevice**.</span><span class="sxs-lookup"><span data-stu-id="d1026-164">**DXVA2\_VideoProcBobDevice**.</span></span> <span data-ttu-id="d1026-165">Questo dispositivo esegue il deinterlacciamento Bob.</span><span class="sxs-lookup"><span data-stu-id="d1026-165">This device performs bob deinterlacing.</span></span>
-   <span data-ttu-id="d1026-166">**DXVA2 \_ VideoProcProgressiveDevice**.</span><span class="sxs-lookup"><span data-stu-id="d1026-166">**DXVA2\_VideoProcProgressiveDevice**.</span></span> <span data-ttu-id="d1026-167">Questo dispositivo viene usato se il video contiene solo frame progressivi, senza frame interlacciati.</span><span class="sxs-lookup"><span data-stu-id="d1026-167">This device is used if the video contains only progressive frames, with no interlaced frames.</span></span> <span data-ttu-id="d1026-168">(Alcuni contenuti video contengono una combinazione di frame progressivi e interlacciati.</span><span class="sxs-lookup"><span data-stu-id="d1026-168">(Some video content contains a mix of progressive and interlaced frames.</span></span> <span data-ttu-id="d1026-169">Il dispositivo progressivo non può essere usato per questo tipo di contenuto video misto, perché è necessario un passaggio di deinterlacciamento per i frame interlacciati.</span><span class="sxs-lookup"><span data-stu-id="d1026-169">The progressive device cannot be used for this kind of "mixed" video content, because a deinterlacing step is required for the interlaced frames.)</span></span>

<span data-ttu-id="d1026-170">Ogni driver di grafica che supporta l'elaborazione video DXVA deve implementare almeno questi due dispositivi.</span><span class="sxs-lookup"><span data-stu-id="d1026-170">Every graphics driver that supports DXVA video processing must implement at least these two devices.</span></span> <span data-ttu-id="d1026-171">Il driver di grafica può anche fornire altri dispositivi, che sono identificati da GUID specifici del driver.</span><span class="sxs-lookup"><span data-stu-id="d1026-171">The graphics driver may also provide other devices, which are identified by driver-specific GUIDs.</span></span> <span data-ttu-id="d1026-172">Un driver, ad esempio, potrebbe implementare un algoritmo di deinterlacciamento proprietario che produce un output di qualità superiore rispetto a quello di Bob deinterlacciamento.</span><span class="sxs-lookup"><span data-stu-id="d1026-172">For example, a driver might implement a proprietary deinterlacing algorithm that produces better quality output than bob deinterlacing.</span></span> <span data-ttu-id="d1026-173">Alcuni algoritmi di deinterlacciamento possono richiedere immagini di riferimento in avanti o indietro dal flusso primario.</span><span class="sxs-lookup"><span data-stu-id="d1026-173">Some deinterlacing algorithms may require forward or backward reference pictures from the primary stream.</span></span> <span data-ttu-id="d1026-174">In tal caso, il chiamante deve fornire queste immagini al driver nella sequenza corretta, come descritto più avanti in questa sezione.</span><span class="sxs-lookup"><span data-stu-id="d1026-174">If so, the caller must provide these pictures to the driver in the correct sequence, as described later in this section.</span></span>

<span data-ttu-id="d1026-175">Viene inoltre fornito un dispositivo software di riferimento.</span><span class="sxs-lookup"><span data-stu-id="d1026-175">A reference software device is also provided.</span></span> <span data-ttu-id="d1026-176">Il dispositivo software è ottimizzato per la qualità anziché per la velocità e potrebbe non essere adatto per l'elaborazione video in tempo reale.</span><span class="sxs-lookup"><span data-stu-id="d1026-176">The software device is optimized for quality rather than speed, and may not be adequate for real-time video processing.</span></span> <span data-ttu-id="d1026-177">Il dispositivo software di riferimento usa il valore GUID DXVA2 \_ VideoProcSoftwareDevice.</span><span class="sxs-lookup"><span data-stu-id="d1026-177">The reference software device uses the GUID value DXVA2\_VideoProcSoftwareDevice.</span></span>

## <a name="creating-a-video-processing-device"></a><span data-ttu-id="d1026-178">Creazione di un dispositivo di elaborazione video</span><span class="sxs-lookup"><span data-stu-id="d1026-178">Creating a Video Processing Device</span></span>

<span data-ttu-id="d1026-179">Prima di usare l'elaborazione video DXVA, l'applicazione deve creare un dispositivo di elaborazione video.</span><span class="sxs-lookup"><span data-stu-id="d1026-179">Before using DXVA video processing, the application must create a video processing device.</span></span> <span data-ttu-id="d1026-180">Ecco una breve descrizione dei passaggi, illustrati più dettagliatamente nella parte restante di questa sezione:</span><span class="sxs-lookup"><span data-stu-id="d1026-180">Here is a brief outline of the steps, which are explained in greater detail in the remainder of this section:</span></span>

1.  <span data-ttu-id="d1026-181">Ottenere un puntatore all'interfaccia [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice) .</span><span class="sxs-lookup"><span data-stu-id="d1026-181">Get a pointer to the [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice) interface.</span></span>
2.  <span data-ttu-id="d1026-182">Creare una descrizione del formato video per il flusso video primario.</span><span class="sxs-lookup"><span data-stu-id="d1026-182">Create a description of the video format for the primary video stream.</span></span> <span data-ttu-id="d1026-183">Usare questa descrizione per ottenere un elenco dei dispositivi di elaborazione video che supportano il formato video.</span><span class="sxs-lookup"><span data-stu-id="d1026-183">Use this description to get a list of the video processing devices that support the video format.</span></span> <span data-ttu-id="d1026-184">I dispositivi sono identificati dal GUID.</span><span class="sxs-lookup"><span data-stu-id="d1026-184">Devices are identified by GUID.</span></span>
3.  <span data-ttu-id="d1026-185">Per un dispositivo specifico, ottenere un elenco di formati di destinazione di rendering supportati dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d1026-185">For a particular device, get a list of render-target formats supported by the device.</span></span> <span data-ttu-id="d1026-186">I formati vengono restituiti come un elenco di valori **D3DFORMAT** .</span><span class="sxs-lookup"><span data-stu-id="d1026-186">The formats are returned as a list of **D3DFORMAT** values.</span></span> <span data-ttu-id="d1026-187">Se si prevede di combinare sottoflussi, ottenere anche un elenco dei formati sottoflussi supportati.</span><span class="sxs-lookup"><span data-stu-id="d1026-187">If you plan to mix substreams, get a list of the supported substream formats as well.</span></span>
4.  <span data-ttu-id="d1026-188">Eseguire una query sulle funzionalità di ogni dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d1026-188">Query the capabilities of each device.</span></span>
5.  <span data-ttu-id="d1026-189">Creare il dispositivo di elaborazione video.</span><span class="sxs-lookup"><span data-stu-id="d1026-189">Create the video processing device.</span></span>

<span data-ttu-id="d1026-190">In alcuni casi è possibile omettere alcuni di questi passaggi.</span><span class="sxs-lookup"><span data-stu-id="d1026-190">Sometimes you can omit some of these steps.</span></span> <span data-ttu-id="d1026-191">Ad esempio, anziché ottenere l'elenco dei formati di destinazione di rendering, è possibile provare semplicemente a creare il dispositivo di elaborazione video con il formato preferito e verificare se l'operazione ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="d1026-191">For example, instead of getting the list of render-target formats, you could simply try creating the video processing device with your preferred format, and see if it succeeds.</span></span> <span data-ttu-id="d1026-192">Un formato comune, ad esempio D3DFMT \_ X8R8G8B8, è probabile che abbia esito positivo.</span><span class="sxs-lookup"><span data-stu-id="d1026-192">A common format such as D3DFMT\_X8R8G8B8 is likely to succeed.</span></span>

<span data-ttu-id="d1026-193">Nella parte restante di questa sezione vengono descritti in dettaglio questi passaggi.</span><span class="sxs-lookup"><span data-stu-id="d1026-193">The remainder of this section describes these steps in detail.</span></span>

### <a name="get-the-idirectxvideoprocessorservice-pointer"></a><span data-ttu-id="d1026-194">Ottenere il puntatore IDirectXVideoProcessorService</span><span class="sxs-lookup"><span data-stu-id="d1026-194">Get the IDirectXVideoProcessorService Pointer</span></span>

<span data-ttu-id="d1026-195">L'interfaccia [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice) è ottenuta dal dispositivo Direct3D.</span><span class="sxs-lookup"><span data-stu-id="d1026-195">The [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice) interface is obtained from the Direct3D device.</span></span> <span data-ttu-id="d1026-196">Esistono due modi per ottenere un puntatore a questa interfaccia:</span><span class="sxs-lookup"><span data-stu-id="d1026-196">There are two ways to get a pointer to this interface:</span></span>

-   <span data-ttu-id="d1026-197">Da un dispositivo Direct3D.</span><span class="sxs-lookup"><span data-stu-id="d1026-197">From a Direct3D device.</span></span>
-   <span data-ttu-id="d1026-198">Dal [Gestione dispositivi Direct3D](direct3d-device-manager.md).</span><span class="sxs-lookup"><span data-stu-id="d1026-198">From the [Direct3D Device Manager](direct3d-device-manager.md).</span></span>

<span data-ttu-id="d1026-199">Se è presente un puntatore a un dispositivo Direct3D, è possibile ottenere un puntatore [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice) chiamando la funzione [**DXVA2CreateVideoService**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createvideoservice) .</span><span class="sxs-lookup"><span data-stu-id="d1026-199">If you have a pointer to a Direct3D device, you can get an [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice) pointer by calling the [**DXVA2CreateVideoService**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createvideoservice) function.</span></span> <span data-ttu-id="d1026-200">Passare un puntatore all'interfaccia **IDirect3DDevice9** del dispositivo e specificare **IID \_ IDirectXVideoProcessorService** per il parametro *riid* , come illustrato nel codice seguente:</span><span class="sxs-lookup"><span data-stu-id="d1026-200">Pass in a pointer to the device's **IDirect3DDevice9** interface, and specify **IID\_IDirectXVideoProcessorService** for the *riid* parameter, as shown in the following code:</span></span>


```C++
    // Create the DXVA-2 Video Processor service.
    hr = DXVA2CreateVideoService(g_pD3DD9, IID_PPV_ARGS(&g_pDXVAVPS));
```



<span data-ttu-id="d1026-201">n alcuni casi, un oggetto crea il dispositivo Direct3D e lo condivide con altri oggetti tramite il [Gestione dispositivi Direct3D](direct3d-device-manager.md).</span><span class="sxs-lookup"><span data-stu-id="d1026-201">n some cases, one object creates the Direct3D device and then shares it with other objects through the [Direct3D Device Manager](direct3d-device-manager.md).</span></span> <span data-ttu-id="d1026-202">In questa situazione, è possibile chiamare [**IDirect3DDeviceManager9:: GetVideoService**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-getvideoservice) in gestione dispositivi per ottenere il puntatore [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice) , come illustrato nel codice seguente:</span><span class="sxs-lookup"><span data-stu-id="d1026-202">In this situation, you can call [**IDirect3DDeviceManager9::GetVideoService**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-getvideoservice) on the device manager to get the [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice) pointer, as shown in the following code:</span></span>


```C++
HRESULT GetVideoProcessorService(
    IDirect3DDeviceManager9 *pDeviceManager,
    IDirectXVideoProcessorService **ppVPService
    )
{
    *ppVPService = NULL;

    HANDLE hDevice;

    HRESULT hr = pDeviceManager->OpenDeviceHandle(&hDevice);
    if (SUCCEEDED(hr))
    {
        // Get the video processor service 
        HRESULT hr2 = pDeviceManager->GetVideoService(
            hDevice, 
            IID_PPV_ARGS(ppVPService)
            );

        // Close the device handle.
        hr = pDeviceManager->CloseDeviceHandle(hDevice);

        if (FAILED(hr2))
        {
            hr = hr2;
        }
    }

    if (FAILED(hr))
    {
        SafeRelease(ppVPService);
    }

    return hr;
}
```



### <a name="enumerate-the-video-processing-devices"></a><span data-ttu-id="d1026-203">Enumerare i dispositivi di elaborazione video</span><span class="sxs-lookup"><span data-stu-id="d1026-203">Enumerate the Video Processing Devices</span></span>

<span data-ttu-id="d1026-204">Per ottenere un elenco di dispositivi di elaborazione video, compilare una struttura [**DXVA2 \_ VideoDesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) con il formato del flusso video primario e passare la struttura al metodo [**IDirectXVideoProcessorService:: GetVideoProcessorDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids) .</span><span class="sxs-lookup"><span data-stu-id="d1026-204">To get a list of video processing devices, fill in a [**DXVA2\_VideoDesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) structure with the format of the primary video stream, and pass this structure to the [**IDirectXVideoProcessorService::GetVideoProcessorDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids) method.</span></span> <span data-ttu-id="d1026-205">Il metodo restituisce una matrice di GUID, uno per ogni dispositivo di elaborazione video che può essere usato con questo formato video.</span><span class="sxs-lookup"><span data-stu-id="d1026-205">The method returns an array of GUIDs, one for each video processing device that can be used with this video format.</span></span>

<span data-ttu-id="d1026-206">Si consideri un'applicazione che esegue il rendering di un flusso video in formato YUY2 usando la definizione BT. 709 del colore YUV, con una frequenza dei fotogrammi di 29,97 fotogrammi al secondo.</span><span class="sxs-lookup"><span data-stu-id="d1026-206">Consider an application that renders a video stream in YUY2 format, using the BT.709 definition of YUV color, with a frame rate of 29.97 frames per second.</span></span> <span data-ttu-id="d1026-207">Si supponga che il contenuto video sia costituito interamente da frame progressivi.</span><span class="sxs-lookup"><span data-stu-id="d1026-207">Assume that the video content consists entirely of progressive frames.</span></span> <span data-ttu-id="d1026-208">Il frammento di codice seguente mostra come compilare la descrizione del formato e ottenere i GUID del dispositivo:</span><span class="sxs-lookup"><span data-stu-id="d1026-208">The following code fragment shows how to fill in the format description and get the device GUIDs:</span></span>


```C++
    // Initialize the video descriptor.

    g_VideoDesc.SampleWidth                         = VIDEO_MAIN_WIDTH;
    g_VideoDesc.SampleHeight                        = VIDEO_MAIN_HEIGHT;
    g_VideoDesc.SampleFormat.VideoChromaSubsampling = DXVA2_VideoChromaSubsampling_MPEG2;
    g_VideoDesc.SampleFormat.NominalRange           = DXVA2_NominalRange_16_235;
    g_VideoDesc.SampleFormat.VideoTransferMatrix    = EX_COLOR_INFO[g_ExColorInfo][0];
    g_VideoDesc.SampleFormat.VideoLighting          = DXVA2_VideoLighting_dim;
    g_VideoDesc.SampleFormat.VideoPrimaries         = DXVA2_VideoPrimaries_BT709;
    g_VideoDesc.SampleFormat.VideoTransferFunction  = DXVA2_VideoTransFunc_709;
    g_VideoDesc.SampleFormat.SampleFormat           = DXVA2_SampleProgressiveFrame;
    g_VideoDesc.Format                              = VIDEO_MAIN_FORMAT;
    g_VideoDesc.InputSampleFreq.Numerator           = VIDEO_FPS;
    g_VideoDesc.InputSampleFreq.Denominator         = 1;
    g_VideoDesc.OutputFrameFreq.Numerator           = VIDEO_FPS;
    g_VideoDesc.OutputFrameFreq.Denominator         = 1;

    // Query the video processor GUID.

    UINT count;
    GUID* guids = NULL;

    hr = g_pDXVAVPS->GetVideoProcessorDeviceGuids(&g_VideoDesc, &count, &guids);
```



<span data-ttu-id="d1026-209">Il codice per questo esempio è tratto dall'esempio [DXVA2 \_ VideoProc](dxva2-videoproc-sample.md) SDK.</span><span class="sxs-lookup"><span data-stu-id="d1026-209">The code for this example is taken from the [DXVA2\_VideoProc](dxva2-videoproc-sample.md) SDK sample.</span></span>

<span data-ttu-id="d1026-210">La matrice *pGuids* in questo esempio viene allocata dal metodo [**GetVideoProcessorDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids) , quindi l'applicazione deve liberare la matrice chiamando [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="d1026-210">The *pGuids* array in this example is allocated by the [**GetVideoProcessorDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids) method, so the application must free the array by calling [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span> <span data-ttu-id="d1026-211">I passaggi rimanenti possono essere eseguiti usando uno dei GUID del dispositivo restituiti da questo metodo.</span><span class="sxs-lookup"><span data-stu-id="d1026-211">The remaining steps can be performed using any of the device GUIDs returned by this method.</span></span>

### <a name="enumerate-render-target-formats"></a><span data-ttu-id="d1026-212">Enumerare i formati di Render-Target</span><span class="sxs-lookup"><span data-stu-id="d1026-212">Enumerate Render-Target Formats</span></span>

<span data-ttu-id="d1026-213">Per ottenere l'elenco dei formati di destinazione di rendering supportati dal dispositivo, passare il GUID del dispositivo e la struttura [**DXVA2 \_ VideoDesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) al metodo [**IDirectXVideoProcessorService:: GetVideoProcessorRenderTargets**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorrendertargets) , come illustrato nel codice seguente:</span><span class="sxs-lookup"><span data-stu-id="d1026-213">To get the list of render-target formats supported by the device, pass the device GUID and the [**DXVA2\_VideoDesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) structure to the [**IDirectXVideoProcessorService::GetVideoProcessorRenderTargets**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorrendertargets) method, as shown in the following code:</span></span>


```C++
    // Query the supported render-target formats.

    UINT i, count;
    D3DFORMAT* formats = NULL;

    HRESULT hr = g_pDXVAVPS->GetVideoProcessorRenderTargets(
        guid, &g_VideoDesc, &count, &formats);

    if (FAILED(hr))
    {
        DBGMSG((L"GetVideoProcessorRenderTargets failed: 0x%x.\n", hr));
        return FALSE;
    }

    for (i = 0; i < count; i++)
    {
        if (formats[i] == VIDEO_RENDER_TARGET_FORMAT)
        {
            break;
        }
    }

    CoTaskMemFree(formats);

    if (i >= count)
    {
        DBGMSG((L"The device does not support the render-target format.\n"));
        return FALSE;
    }
```



<span data-ttu-id="d1026-214">Il metodo restituisce una matrice di valori **D3DFORMAT** .</span><span class="sxs-lookup"><span data-stu-id="d1026-214">The method returns an array of **D3DFORMAT** values.</span></span> <span data-ttu-id="d1026-215">In questo esempio, in cui il tipo di input è YUY2, un tipico elenco di formati potrebbe essere D3DFMT \_ X8R8G8B8 (RGB a 32 bit) e D3DMFT \_ YUY2 (il formato di input).</span><span class="sxs-lookup"><span data-stu-id="d1026-215">In this example, where the input type is YUY2, a typical list of formats might be D3DFMT\_X8R8G8B8 (32-bit RGB) and D3DMFT\_YUY2 (the input format).</span></span> <span data-ttu-id="d1026-216">Tuttavia, l'elenco esatto dipenderà dal driver.</span><span class="sxs-lookup"><span data-stu-id="d1026-216">However, the exact list will depend on the driver.</span></span>

<span data-ttu-id="d1026-217">L'elenco dei formati disponibili per i flussi sottoflussi può variare a seconda del formato di destinazione di rendering e del formato di input.</span><span class="sxs-lookup"><span data-stu-id="d1026-217">The list of available formats for the substreams can vary depending on the render-target format and the input format.</span></span> <span data-ttu-id="d1026-218">Per ottenere l'elenco dei formati di sottoflusso, passare il GUID del dispositivo, la struttura del formato e il formato di destinazione di rendering al metodo [**IDirectXVideoProcessorService:: GetVideoProcessorSubStreamFormats**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorsubstreamformats) , come illustrato nel codice seguente:</span><span class="sxs-lookup"><span data-stu-id="d1026-218">To get the list of substream formats, pass the device GUID, the format structure, and the render-target format to the [**IDirectXVideoProcessorService::GetVideoProcessorSubStreamFormats**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorsubstreamformats) method, as shown in the following code:</span></span>


```C++
    // Query the supported substream formats.

    formats = NULL;

    hr = g_pDXVAVPS->GetVideoProcessorSubStreamFormats(
        guid, &g_VideoDesc, VIDEO_RENDER_TARGET_FORMAT, &count, &formats);

    if (FAILED(hr))
    {
        DBGMSG((L"GetVideoProcessorSubStreamFormats failed: 0x%x.\n", hr));
        return FALSE;
    }

    for (i = 0; i < count; i++)
    {
        if (formats[i] == VIDEO_SUB_FORMAT)
        {
            break;
        }
    }

    CoTaskMemFree(formats);

    if (i >= count)
    {
        DBGMSG((L"The device does not support the substream format.\n"));
        return FALSE;
    }
```



<span data-ttu-id="d1026-219">Questo metodo restituisce un'altra matrice di valori **D3DFORMAT** .</span><span class="sxs-lookup"><span data-stu-id="d1026-219">This method returns another array of **D3DFORMAT** values.</span></span> <span data-ttu-id="d1026-220">I formati di sottoflusso tipici sono AYUV e AI44.</span><span class="sxs-lookup"><span data-stu-id="d1026-220">Typical substream formats are AYUV and AI44.</span></span>

### <a name="query-the-device-capabilities"></a><span data-ttu-id="d1026-221">Eseguire query sulle funzionalità del dispositivo</span><span class="sxs-lookup"><span data-stu-id="d1026-221">Query the Device Capabilities</span></span>

<span data-ttu-id="d1026-222">Per ottenere le funzionalità di un particolare dispositivo, passare il GUID del dispositivo, la struttura del formato e un formato di destinazione di rendering al metodo [**IDirectXVideoProcessorService:: GetVideoProcessorCaps**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorcaps) .</span><span class="sxs-lookup"><span data-stu-id="d1026-222">To get the capabilities of a particular device, pass the device GUID, the format structure, and a render-target format to the [**IDirectXVideoProcessorService::GetVideoProcessorCaps**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorcaps) method.</span></span> <span data-ttu-id="d1026-223">Il metodo compila una struttura della struttura [**DXVA2 \_ VideoProcessorCaps**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessorcaps) con le funzionalità del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d1026-223">The method fills in a [**DXVA2\_VideoProcessorCaps**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessorcaps) structure structure with the device capabilities.</span></span>


```C++
    // Query video processor capabilities.

    hr = g_pDXVAVPS->GetVideoProcessorCaps(
        guid, &g_VideoDesc, VIDEO_RENDER_TARGET_FORMAT, &g_VPCaps);

    if (FAILED(hr))
    {
        DBGMSG((L"GetVideoProcessorCaps failed: 0x%x.\n", hr));
        return FALSE;
    }
```



### <a name="create-the-device"></a><span data-ttu-id="d1026-224">Creare il dispositivo</span><span class="sxs-lookup"><span data-stu-id="d1026-224">Create the Device</span></span>

<span data-ttu-id="d1026-225">Per creare il dispositivo di elaborazione video, chiamare [**IDirectXVideoProcessorService:: CreateVideoProcessor**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-createvideoprocessor).</span><span class="sxs-lookup"><span data-stu-id="d1026-225">To create the video processing device, call [**IDirectXVideoProcessorService::CreateVideoProcessor**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-createvideoprocessor).</span></span> <span data-ttu-id="d1026-226">L'input per questo metodo è il GUID del dispositivo, la descrizione del formato, il formato della destinazione di rendering e il numero massimo di flussi sottoflussi che si prevede di combinare.</span><span class="sxs-lookup"><span data-stu-id="d1026-226">The input to this method is the device GUID, the format description, the render-target format, and the maximum number of substreams that you plan to mix.</span></span> <span data-ttu-id="d1026-227">Il metodo restituisce un puntatore all'interfaccia [**IDirectXVideoProcessor**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessor) , che rappresenta il dispositivo di elaborazione video.</span><span class="sxs-lookup"><span data-stu-id="d1026-227">The method returns a pointer to the [**IDirectXVideoProcessor**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessor) interface, which represents the video processing device.</span></span>


```C++
    // Finally create a video processor device.

    hr = g_pDXVAVPS->CreateVideoProcessor(
        guid,
        &g_VideoDesc,
        VIDEO_RENDER_TARGET_FORMAT,
        SUB_STREAM_COUNT,
        &g_pDXVAVPD
        );
```



## <a name="video-process-blit"></a><span data-ttu-id="d1026-228">Blit processo video</span><span class="sxs-lookup"><span data-stu-id="d1026-228">Video Process Blit</span></span>

<span data-ttu-id="d1026-229">L'operazione di elaborazione video principale è l' *elaborazione video blit*.</span><span class="sxs-lookup"><span data-stu-id="d1026-229">The main video processing operation is the *video processing blit*.</span></span> <span data-ttu-id="d1026-230">Un *blit* è qualsiasi operazione che combina due o più bitmap in una singola bitmap.</span><span class="sxs-lookup"><span data-stu-id="d1026-230">(A *blit* is any operation that combines two or more bitmaps into a single bitmap.</span></span> <span data-ttu-id="d1026-231">Un blit di elaborazione video combina le immagini di input per creare un frame di output. Per eseguire un blit di elaborazione video, chiamare [**IDirectXVideoProcessor:: VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt).</span><span class="sxs-lookup"><span data-stu-id="d1026-231">A video processing blit combines input pictures to create an output frame.) To perform a video processing blit, call [**IDirectXVideoProcessor::VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt).</span></span> <span data-ttu-id="d1026-232">Questo metodo passa un set di esempi video al dispositivo di elaborazione video.</span><span class="sxs-lookup"><span data-stu-id="d1026-232">This method passes a set of video samples to the video processing device.</span></span> <span data-ttu-id="d1026-233">In risposta, il dispositivo di elaborazione video elabora le immagini di input e genera un frame di output.</span><span class="sxs-lookup"><span data-stu-id="d1026-233">In response, the video processing device processes the input pictures and generates one output frame.</span></span> <span data-ttu-id="d1026-234">L'elaborazione può includere la deinterlacciamento, la conversione dello spazio colore e la combinazione di sottoflussi.</span><span class="sxs-lookup"><span data-stu-id="d1026-234">Processing can include deinterlacing, color-space conversion, and substream mixing.</span></span> <span data-ttu-id="d1026-235">L'output viene scritto in una superficie di destinazione fornita dal chiamante.</span><span class="sxs-lookup"><span data-stu-id="d1026-235">The output is written to a destination surface provided by the caller.</span></span>

<span data-ttu-id="d1026-236">Il metodo [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) accetta i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="d1026-236">The [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) method takes the following parameters:</span></span>

-   <span data-ttu-id="d1026-237">*pRT* punta a una superficie di destinazione di rendering **IDirect3DSurface9** che riceverà il frame video elaborato.</span><span class="sxs-lookup"><span data-stu-id="d1026-237">*pRT* points to an **IDirect3DSurface9** render target surface that will receive the processed video frame.</span></span>
-   <span data-ttu-id="d1026-238">*pBltParams* punta a una struttura [**DXVA2 \_ VideoProcessBltParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) che specifica i parametri per blit.</span><span class="sxs-lookup"><span data-stu-id="d1026-238">*pBltParams* points to a [**DXVA2\_VideoProcessBltParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) structure that specifies the parameters for the blit.</span></span>
-   <span data-ttu-id="d1026-239">*pSamples* è l'indirizzo di una matrice di strutture [**DXVA2 \_ VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) .</span><span class="sxs-lookup"><span data-stu-id="d1026-239">*pSamples* is the address of an array of [**DXVA2\_VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) structures.</span></span> <span data-ttu-id="d1026-240">Queste strutture contengono gli esempi di input per blit.</span><span class="sxs-lookup"><span data-stu-id="d1026-240">These structures contain the input samples for the blit.</span></span>
-   <span data-ttu-id="d1026-241">*NumSamples valore* fornisce la dimensione della matrice *pSamples* .</span><span class="sxs-lookup"><span data-stu-id="d1026-241">*NumSamples* gives the size of the *pSamples* array.</span></span>
-   <span data-ttu-id="d1026-242">Il parametro *riservato* è riservato e deve essere impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="d1026-242">The *Reserved* parameter is reserved and should be set to **NULL**.</span></span>

<span data-ttu-id="d1026-243">Nella matrice *pSamples* il chiamante deve fornire gli esempi di input seguenti:</span><span class="sxs-lookup"><span data-stu-id="d1026-243">In the *pSamples* array, the caller must provide the following input samples:</span></span>

-   <span data-ttu-id="d1026-244">Immagine corrente dal flusso video primario.</span><span class="sxs-lookup"><span data-stu-id="d1026-244">The current picture from the primary video stream.</span></span>
-   <span data-ttu-id="d1026-245">Immagini di riferimento avanti e indietro, se richieste dall'algoritmo di deinterlacciamento.</span><span class="sxs-lookup"><span data-stu-id="d1026-245">Forward and backward reference pictures, if required by the deinterlacing algorithm.</span></span>
-   <span data-ttu-id="d1026-246">Zero o più immagini di flussi secondari, fino a un massimo di 15 flussi secondari.</span><span class="sxs-lookup"><span data-stu-id="d1026-246">Zero or more substream pictures, up to a maximum of 15 substreams.</span></span>

<span data-ttu-id="d1026-247">Il driver prevede che la matrice sia in un ordine specifico, come descritto nell' [ordine di esempio di input](#input-sample-order).</span><span class="sxs-lookup"><span data-stu-id="d1026-247">The driver expects this array to be in a particular order, as described in [Input Sample Order](#input-sample-order).</span></span>

### <a name="blit-parameters"></a><span data-ttu-id="d1026-248">Parametri blit</span><span class="sxs-lookup"><span data-stu-id="d1026-248">Blit Parameters</span></span>

<span data-ttu-id="d1026-249">La struttura [**DXVA2 \_ VideoProcessBltParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) contiene parametri generali per blit.</span><span class="sxs-lookup"><span data-stu-id="d1026-249">The [**DXVA2\_VideoProcessBltParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) structure contains general parameters for the blit.</span></span> <span data-ttu-id="d1026-250">I parametri più importanti vengono archiviati nei seguenti membri della struttura:</span><span class="sxs-lookup"><span data-stu-id="d1026-250">The most important parameters are stored in the following members of the structure:</span></span>

-   <span data-ttu-id="d1026-251">**TargetFrame** è l'ora di presentazione del frame di output.</span><span class="sxs-lookup"><span data-stu-id="d1026-251">**TargetFrame** is the presentation time of the output frame.</span></span> <span data-ttu-id="d1026-252">Per contenuti progressivi, questo tempo deve essere uguale all'ora di inizio per il frame corrente dal flusso video primario.</span><span class="sxs-lookup"><span data-stu-id="d1026-252">For progressive content, this time must equal the start time for the current frame from the primary video stream.</span></span> <span data-ttu-id="d1026-253">Questa volta viene specificato nel membro **iniziale** della struttura [**\_ VideoSample di DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) per tale esempio di input.</span><span class="sxs-lookup"><span data-stu-id="d1026-253">This time is specified in the **Start** member of the [**DXVA2\_VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) structure for that input sample.</span></span>

    <span data-ttu-id="d1026-254">Per il contenuto interlacciato, un frame con due campi con interfoliazione produce due fotogrammi di output deinterlacciati.</span><span class="sxs-lookup"><span data-stu-id="d1026-254">For interlaced content, a frame with two interleaved fields produces two deinterlaced output frames.</span></span> <span data-ttu-id="d1026-255">Nel primo frame di output, l'ora di presentazione deve corrispondere all'ora di inizio dell'immagine corrente nel flusso video principale, proprio come il contenuto progressivo.</span><span class="sxs-lookup"><span data-stu-id="d1026-255">On the first output frame, the presentation time must equal the start time of the current picture in the primary video stream, just like progressive content.</span></span> <span data-ttu-id="d1026-256">Sul secondo frame di output, l'ora di inizio deve essere uguale al punto medio tra l'ora di inizio dell'immagine corrente nel flusso video primario e l'ora di inizio dell'immagine successiva nel flusso.</span><span class="sxs-lookup"><span data-stu-id="d1026-256">On the second output frame, the start time must equal the midpoint between the start time of the current picture in the primary video stream and the start time of the next picture in the stream.</span></span> <span data-ttu-id="d1026-257">Se, ad esempio, il video di input è 25 fotogrammi al secondo (50 campi al secondo), i frame di output avranno i timestamp indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="d1026-257">For example, if the input video is 25 frames per second (50 fields per second), the output frames will have the time stamps shown in the following table.</span></span> <span data-ttu-id="d1026-258">I timestamp vengono visualizzati in unità di 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="d1026-258">Time stamps are shown in units of 100 nanoseconds.</span></span>

    

    | <span data-ttu-id="d1026-259">Immagine input</span><span class="sxs-lookup"><span data-stu-id="d1026-259">Input picture</span></span> | <span data-ttu-id="d1026-260">**TargetFrame** (1)</span><span class="sxs-lookup"><span data-stu-id="d1026-260">**TargetFrame** (1)</span></span> | <span data-ttu-id="d1026-261">**TargetFrame** (2)</span><span class="sxs-lookup"><span data-stu-id="d1026-261">**TargetFrame** (2)</span></span> |
    |---------------|---------------------|---------------------|
    | <span data-ttu-id="d1026-262">0</span><span class="sxs-lookup"><span data-stu-id="d1026-262">0</span></span>             | <span data-ttu-id="d1026-263">0</span><span class="sxs-lookup"><span data-stu-id="d1026-263">0</span></span>                   | <span data-ttu-id="d1026-264">200000</span><span class="sxs-lookup"><span data-stu-id="d1026-264">200000</span></span>              |
    | <span data-ttu-id="d1026-265">400000</span><span class="sxs-lookup"><span data-stu-id="d1026-265">400000</span></span>        | <span data-ttu-id="d1026-266">0</span><span class="sxs-lookup"><span data-stu-id="d1026-266">0</span></span>                   | <span data-ttu-id="d1026-267">600000</span><span class="sxs-lookup"><span data-stu-id="d1026-267">600000</span></span>              |
    | <span data-ttu-id="d1026-268">800000</span><span class="sxs-lookup"><span data-stu-id="d1026-268">800000</span></span>        | <span data-ttu-id="d1026-269">800000</span><span class="sxs-lookup"><span data-stu-id="d1026-269">800000</span></span>              | <span data-ttu-id="d1026-270">1000000</span><span class="sxs-lookup"><span data-stu-id="d1026-270">1000000</span></span>             |
    | <span data-ttu-id="d1026-271">1,2 milioni</span><span class="sxs-lookup"><span data-stu-id="d1026-271">1200000</span></span>       | <span data-ttu-id="d1026-272">1,2 milioni</span><span class="sxs-lookup"><span data-stu-id="d1026-272">1200000</span></span>             | <span data-ttu-id="d1026-273">1,4 milioni</span><span class="sxs-lookup"><span data-stu-id="d1026-273">1400000</span></span>             |

    

     

    <span data-ttu-id="d1026-274">Se il contenuto interlacciato è costituito da campi singoli anziché da campi con interfoliazione, i tempi di output corrispondono sempre ai tempi di input, come per il contenuto progressivo.</span><span class="sxs-lookup"><span data-stu-id="d1026-274">If interlaced content consists of single fields rather than interleaved fields, the output times always match the input times, as with progressive content.</span></span>

-   <span data-ttu-id="d1026-275">**TargetRect** definisce un'area rettangolare all'interno dell'area di destinazione.</span><span class="sxs-lookup"><span data-stu-id="d1026-275">**TargetRect** defines a rectangular region within the destination surface.</span></span> <span data-ttu-id="d1026-276">Blit scriverà l'output in questa area.</span><span class="sxs-lookup"><span data-stu-id="d1026-276">The blit will write the output to this region.</span></span> <span data-ttu-id="d1026-277">In particolare, ogni pixel all'interno di **targetRect** verrà modificato e nessun pixel al di fuori di **targetRect** verrà modificato.</span><span class="sxs-lookup"><span data-stu-id="d1026-277">Specifically, every pixel inside **TargetRect** will be modified, and no pixels outside of **TargetRect** will be modified.</span></span> <span data-ttu-id="d1026-278">Il rettangolo di destinazione definisce il rettangolo di delimitazione per tutti i flussi video di input.</span><span class="sxs-lookup"><span data-stu-id="d1026-278">The target rectangle defines the bounding rectangle for all of the input video streams.</span></span> <span data-ttu-id="d1026-279">La posizione dei singoli flussi all'interno di tale rettangolo viene controllata tramite il parametro *pSamples* di [**IDirectXVideoProcessor:: VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt).</span><span class="sxs-lookup"><span data-stu-id="d1026-279">Placement of individual streams within that rectangle is controlled through the *pSamples* parameter of [**IDirectXVideoProcessor::VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt).</span></span>
-   <span data-ttu-id="d1026-280">**BackgroundColor** restituisce il colore dello sfondo quando non viene visualizzata alcuna immagine video.</span><span class="sxs-lookup"><span data-stu-id="d1026-280">**BackgroundColor** gives the color of the background wherever no video image appears.</span></span> <span data-ttu-id="d1026-281">Quando, ad esempio, viene visualizzata un'immagine video di 16 x 9 in un'area di 4 x 3 (letterbox), le aree letterbox vengono visualizzate con il colore di sfondo.</span><span class="sxs-lookup"><span data-stu-id="d1026-281">For example, when a 16 x 9 video image is displayed within a 4 x 3 area (letterboxing), the letterboxed regions are displayed with the background color.</span></span> <span data-ttu-id="d1026-282">Il colore di sfondo si applica solo all'interno del rettangolo di destinazione (**targetRect**).</span><span class="sxs-lookup"><span data-stu-id="d1026-282">The background color applies only within the target rectangle (**TargetRect**).</span></span> <span data-ttu-id="d1026-283">Qualsiasi pixel al di fuori di **targetRect** non viene modificato.</span><span class="sxs-lookup"><span data-stu-id="d1026-283">Any pixels outside of **TargetRect** are not modified.</span></span>
-   <span data-ttu-id="d1026-284">**DestFormat** descrive lo spazio di colore per il video di output, ad esempio se viene usato il colore ITU-R BT. 709 o BT. 601.</span><span class="sxs-lookup"><span data-stu-id="d1026-284">**DestFormat** describes the color space for the output video—for example, whether ITU-R BT.709 or BT.601 color is used.</span></span> <span data-ttu-id="d1026-285">Queste informazioni possono influire sul modo in cui viene visualizzata l'immagine.</span><span class="sxs-lookup"><span data-stu-id="d1026-285">This information can affect how the image is displayed.</span></span> <span data-ttu-id="d1026-286">Per ulteriori informazioni, vedere [informazioni sui colori estese](extended-color-information.md).</span><span class="sxs-lookup"><span data-stu-id="d1026-286">For more information, see [Extended Color Information](extended-color-information.md).</span></span>

<span data-ttu-id="d1026-287">Altri parametri sono descritti nella pagina di riferimento per la [**struttura \_ VideoProcessBltParams di DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) .</span><span class="sxs-lookup"><span data-stu-id="d1026-287">Other parameters are described on the reference page for the [**DXVA2\_VideoProcessBltParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) structure.</span></span>

### <a name="input-samples"></a><span data-ttu-id="d1026-288">Esempi di input</span><span class="sxs-lookup"><span data-stu-id="d1026-288">Input Samples</span></span>

<span data-ttu-id="d1026-289">Il parametro *pSamples* di [**IDirectXVideoProcessor:: VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) punta a una matrice di strutture [**DXVA2 \_ VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) .</span><span class="sxs-lookup"><span data-stu-id="d1026-289">The *pSamples* parameter of [**IDirectXVideoProcessor::VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) points to an array of [**DXVA2\_VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) structures.</span></span> <span data-ttu-id="d1026-290">Ognuna di queste strutture contiene informazioni su un esempio di input e un puntatore alla superficie Direct3D che contiene l'esempio.</span><span class="sxs-lookup"><span data-stu-id="d1026-290">Each of these structures contains information about one input sample and a pointer to the Direct3D surface that contains the sample.</span></span> <span data-ttu-id="d1026-291">Ogni esempio è uno dei seguenti:</span><span class="sxs-lookup"><span data-stu-id="d1026-291">Each sample is one of the following:</span></span>

-   <span data-ttu-id="d1026-292">Immagine corrente dal flusso primario.</span><span class="sxs-lookup"><span data-stu-id="d1026-292">The current picture from the primary stream.</span></span>
-   <span data-ttu-id="d1026-293">Immagine di riferimento avanti o indietro dal flusso primario, usata per la deinterlacciamento.</span><span class="sxs-lookup"><span data-stu-id="d1026-293">A forward or backward reference picture from the primary stream, used for deinterlacing.</span></span>
-   <span data-ttu-id="d1026-294">Immagine del flusso di flussi.</span><span class="sxs-lookup"><span data-stu-id="d1026-294">A substream picture.</span></span>

<span data-ttu-id="d1026-295">L'ordine esatto in cui gli esempi devono essere visualizzati nella matrice è descritto più avanti nella sezione [ordine di esempio di input](#input-sample-order).</span><span class="sxs-lookup"><span data-stu-id="d1026-295">The exact order in which the samples must appear in the array is described later, in the section [Input Sample Order](#input-sample-order).</span></span>

<span data-ttu-id="d1026-296">È possibile fornire fino a 15 immagini di flussi secondari, sebbene la maggior parte delle applicazioni video necessiti di un solo sottoflusso, al massimo.</span><span class="sxs-lookup"><span data-stu-id="d1026-296">Up to 15 substream pictures can be provided, although most video applications need only one substream, at the most.</span></span> <span data-ttu-id="d1026-297">Il numero di flussi substream può variare con ogni chiamata a [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt).</span><span class="sxs-lookup"><span data-stu-id="d1026-297">The number of substreams can change with each call to [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt).</span></span> <span data-ttu-id="d1026-298">Le immagini di flussi secondari sono indicate impostando il membro **SampleFormat. SampleFormat** della struttura [**DXVA2 \_ VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) uguale a DXVA2 \_ SampleSubStream.</span><span class="sxs-lookup"><span data-stu-id="d1026-298">Substream pictures are indicated by setting the **SampleFormat.SampleFormat** member of the [**DXVA2\_VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) structure equal to DXVA2\_SampleSubStream.</span></span> <span data-ttu-id="d1026-299">Per il flusso video primario, questo membro descrive l'interlacciamento del video di input.</span><span class="sxs-lookup"><span data-stu-id="d1026-299">For the primary video stream, this member describes the interlacing of the input video.</span></span> <span data-ttu-id="d1026-300">Per ulteriori informazioni, vedere [**DXVA2 \_ SampleFormat**](/windows/desktop/api/dxva2api/ne-dxva2api-dxva2_sampleformat) Enumeration.</span><span class="sxs-lookup"><span data-stu-id="d1026-300">For more information, see [**DXVA2\_SampleFormat**](/windows/desktop/api/dxva2api/ne-dxva2api-dxva2_sampleformat) enumeration.</span></span>

<span data-ttu-id="d1026-301">Per il flusso video primario, i membri **iniziale** e **finale** della struttura [**DXVA2 \_ VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) forniscono le ore di inizio e di fine dell'esempio di input.</span><span class="sxs-lookup"><span data-stu-id="d1026-301">For the primary video stream, the **Start** and **End** members of the [**DXVA2\_VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) structure give the start and end times of the input sample.</span></span> <span data-ttu-id="d1026-302">Per le immagini di flussi secondari, impostare questi valori su zero, perché l'ora di presentazione viene sempre calcolata dal flusso primario.</span><span class="sxs-lookup"><span data-stu-id="d1026-302">For substream pictures, set these values to zero, because the presentation time is always calculated from the primary stream.</span></span> <span data-ttu-id="d1026-303">L'applicazione è responsabile del rilevamento del momento in cui ogni immagine di flusso substream deve essere presentata e inviata a [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) al momento giusto.</span><span class="sxs-lookup"><span data-stu-id="d1026-303">The application is responsible for tracking when each substream picture should be presented and submitting it to [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) at the proper time.</span></span>

<span data-ttu-id="d1026-304">Due rettangoli definiscono la modalità di posizionamento del video di origine per ogni flusso:</span><span class="sxs-lookup"><span data-stu-id="d1026-304">Two rectangles define how the source video is positioned for each stream:</span></span>

-   <span data-ttu-id="d1026-305">Il membro **SrcRect** della struttura [**DXVA2 \_ VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) specifica il *rettangolo di origine*, un'area rettangolare dell'immagine di origine che verrà visualizzata nel frame di output composito.</span><span class="sxs-lookup"><span data-stu-id="d1026-305">The **SrcRect** member of the [**DXVA2\_VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) structure specifies the *source rectangle*, a rectangular region of the source picture that will appear in the composited output frame.</span></span> <span data-ttu-id="d1026-306">Per ritagliare l'immagine, impostarla su un valore inferiore alle dimensioni del frame.</span><span class="sxs-lookup"><span data-stu-id="d1026-306">To crop the picture, set this to a value smaller than the frame size.</span></span> <span data-ttu-id="d1026-307">In caso contrario, impostarlo uguale alle dimensioni del frame.</span><span class="sxs-lookup"><span data-stu-id="d1026-307">Otherwise, set it equal to the frame size.</span></span>
-   <span data-ttu-id="d1026-308">Il membro **DstRect** della stessa struttura specifica il *rettangolo di destinazione*, un'area rettangolare della superficie di destinazione in cui verrà visualizzato il frame del video.</span><span class="sxs-lookup"><span data-stu-id="d1026-308">The **DstRect** member of the same structure specifies the *destination rectangle*, a rectangular region of the destination surface where the video frame will appear.</span></span>

<span data-ttu-id="d1026-309">Il driver Blits i pixel dal rettangolo di origine al rettangolo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="d1026-309">The driver blits pixels from the source rectangle into the destination rectangle.</span></span> <span data-ttu-id="d1026-310">I due rettangoli possono avere dimensioni o proporzioni diverse; il driver scalerà l'immagine in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="d1026-310">The two rectangles can have different sizes or aspect ratios; the driver will scale the image as needed.</span></span> <span data-ttu-id="d1026-311">Ogni flusso di input può inoltre utilizzare un fattore di scala diverso.</span><span class="sxs-lookup"><span data-stu-id="d1026-311">Moreover, each input stream can use a different scaling factor.</span></span> <span data-ttu-id="d1026-312">Di fatto, la scalabilità potrebbe essere necessaria per produrre le proporzioni corrette nel frame di output.</span><span class="sxs-lookup"><span data-stu-id="d1026-312">In fact, scaling might be necessary to produce the correct aspect ratio in the output frame.</span></span> <span data-ttu-id="d1026-313">Il driver non prende in considerazione le proporzioni dei pixel dell'origine, pertanto se l'immagine di origine utilizza pixel non quadrati, spetta all'applicazione calcolare il rettangolo di destinazione corretto.</span><span class="sxs-lookup"><span data-stu-id="d1026-313">The driver does not take the source's pixel aspect ratio into account, so if the source image uses non-square pixels, it is up to the application to calculate the correct destination rectangle.</span></span>

<span data-ttu-id="d1026-314">I formati dei sottoflussi preferiti sono AYUV e AI44.</span><span class="sxs-lookup"><span data-stu-id="d1026-314">The preferred substream formats are AYUV and AI44.</span></span> <span data-ttu-id="d1026-315">Quest'ultimo è un formato pallet con 16 colori.</span><span class="sxs-lookup"><span data-stu-id="d1026-315">The latter is a palletized format with 16 colors.</span></span> <span data-ttu-id="d1026-316">Le voci della tavolozza sono specificate nel membro **PAL** della struttura [**\_ VideoSample di DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) .</span><span class="sxs-lookup"><span data-stu-id="d1026-316">Palette entries are specified in the **Pal** member of the [**DXVA2\_VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) structure.</span></span> <span data-ttu-id="d1026-317">Se il formato del video di origine è espresso originariamente come tipo di supporto Media Foundation, le voci della tavolozza vengono archiviate nell'attributo della [**\_ \_ tavolozza MF mt**](mf-mt-palette-attribute.md) . Per i formati non pallet, deselezionare la matrice su zero.</span><span class="sxs-lookup"><span data-stu-id="d1026-317">(If your source video format is originally expressed as a Media Foundation media type, the palette entries are stored in the [**MF\_MT\_PALETTE**](mf-mt-palette-attribute.md) attribute.) For non-palletized formats, clear this array to zero.</span></span>

## <a name="image-composition"></a><span data-ttu-id="d1026-318">Composizione immagine</span><span class="sxs-lookup"><span data-stu-id="d1026-318">Image Composition</span></span>

<span data-ttu-id="d1026-319">Ogni operazione blit è definita dai tre rettangoli seguenti:</span><span class="sxs-lookup"><span data-stu-id="d1026-319">Every blit operation is defined by the following three rectangles:</span></span>

-   <span data-ttu-id="d1026-320">Il rettangolo di *destinazione* (**targetRect**) definisce l'area all'interno della superficie di destinazione in cui verrà visualizzato l'output.</span><span class="sxs-lookup"><span data-stu-id="d1026-320">The *target* rectangle (**TargetRect**) defines the region within the destination surface where the output will appear.</span></span> <span data-ttu-id="d1026-321">L'immagine di output viene ritagliata in questo rettangolo.</span><span class="sxs-lookup"><span data-stu-id="d1026-321">The output image is clipped to this rectangle.</span></span>
-   <span data-ttu-id="d1026-322">Il rettangolo di *destinazione* per ogni flusso (**DstRect**) definisce dove viene visualizzato il flusso di input nell'immagine composita.</span><span class="sxs-lookup"><span data-stu-id="d1026-322">The *destination* rectangle for each stream (**DstRect**) defines where the input stream appears in the composited image.</span></span>
-   <span data-ttu-id="d1026-323">Il rettangolo di *origine* per ogni flusso (**SrcRect**) definisce quale parte dell'immagine di origine viene visualizzata.</span><span class="sxs-lookup"><span data-stu-id="d1026-323">The *source* rectangle for each stream (**SrcRect**) defines which part of the source image appears.</span></span>

<span data-ttu-id="d1026-324">I rettangoli di destinazione e di destinazione vengono specificati in relazione alla superficie di destinazione.</span><span class="sxs-lookup"><span data-stu-id="d1026-324">The target and destination rectangles are specified relative to the destination surface.</span></span> <span data-ttu-id="d1026-325">Il rettangolo di origine viene specificato in relazione all'immagine di origine.</span><span class="sxs-lookup"><span data-stu-id="d1026-325">The source rectangle is specified relative to the source image.</span></span> <span data-ttu-id="d1026-326">Tutti i rettangoli sono specificati in pixel.</span><span class="sxs-lookup"><span data-stu-id="d1026-326">All rectangles are specified in pixels.</span></span>

![diagramma che mostra i rettangoli di origine, di destinazione e di destinazione](images/dxva-vp-rects.gif)

<span data-ttu-id="d1026-328">Il dispositivo di elaborazione video Alpha fonde le immagini di input, usando una delle seguenti origini di dati Alpha:</span><span class="sxs-lookup"><span data-stu-id="d1026-328">The video processing device alpha blends the input pictures, using any of the following sources of alpha data:</span></span>

-   <span data-ttu-id="d1026-329">Dati alfa per pixel da sottoflussi.</span><span class="sxs-lookup"><span data-stu-id="d1026-329">Per-pixel alpha data from substreams.</span></span>
-   <span data-ttu-id="d1026-330">Valore alfa planare per ogni flusso video, specificato nel membro **PlanarAlpha** della struttura [**\_ VideoSample di DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) .</span><span class="sxs-lookup"><span data-stu-id="d1026-330">A planar alpha value for each video stream, specified in the **PlanarAlpha** member of the [**DXVA2\_VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) structure.</span></span>
-   <span data-ttu-id="d1026-331">Valore alfa planare dell'immagine composita, specificata nel membro **Alpha** della struttura VideoProcessBltParams di [**DXVA2 \_**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) .</span><span class="sxs-lookup"><span data-stu-id="d1026-331">The planar alpha value of the composited image, specified in the **Alpha** member of the [**DXVA2\_VideoProcessBltParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) structure.</span></span> <span data-ttu-id="d1026-332">Questo valore viene usato per fondere l'intera immagine composita con il colore di sfondo.</span><span class="sxs-lookup"><span data-stu-id="d1026-332">This value is used to blend the entire composited image with the background color.</span></span>

<span data-ttu-id="d1026-333">Questa sezione fornisce una serie di esempi che illustrano il modo in cui il dispositivo di elaborazione video crea l'immagine di output.</span><span class="sxs-lookup"><span data-stu-id="d1026-333">This section gives a series of examples that show how the video processing device creates the output image.</span></span>

### <a name="example-1-letterboxing"></a><span data-ttu-id="d1026-334">Esempio 1: Letterbox</span><span class="sxs-lookup"><span data-stu-id="d1026-334">Example 1: Letterboxing</span></span>

<span data-ttu-id="d1026-335">Questo esempio illustra come creare una letterbox per l'immagine di origine, impostando il rettangolo di destinazione su un valore inferiore al rettangolo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="d1026-335">This example shows how to letterbox the source image, by setting the destination rectangle to be smaller than the target rectangle.</span></span> <span data-ttu-id="d1026-336">Il flusso video primario in questo esempio è un'immagine 720 × 480 ed è destinato a essere visualizzato in corrispondenza di un 16:9 proporzioni.</span><span class="sxs-lookup"><span data-stu-id="d1026-336">The primary video stream in this example is a 720 × 480 image, and is meant to be displayed at a 16:9 aspect ratio.</span></span> <span data-ttu-id="d1026-337">La superficie di destinazione è 640 × 480 pixel (4:3 proporzioni).</span><span class="sxs-lookup"><span data-stu-id="d1026-337">The destination surface is 640 × 480 pixels (4:3 aspect ratio).</span></span> <span data-ttu-id="d1026-338">Per ottenere le proporzioni corrette, il rettangolo di destinazione deve essere 640 × 360.</span><span class="sxs-lookup"><span data-stu-id="d1026-338">To achieve the correct aspect ratio, the destination rectangle must be 640 × 360.</span></span> <span data-ttu-id="d1026-339">Per semplicità, in questo esempio non è incluso un sottoflusso.</span><span class="sxs-lookup"><span data-stu-id="d1026-339">For simplicity, this example does not include a substream.</span></span> <span data-ttu-id="d1026-340">Nel diagramma seguente vengono illustrati i rettangoli di origine e di destinazione.</span><span class="sxs-lookup"><span data-stu-id="d1026-340">The following diagram shows the source and destination rectangles.</span></span>

![diagramma che mostra le letterbox.](images/428105fa-a26b-48a6-991d-44d24ab786b1.gif)

<span data-ttu-id="d1026-342">Il diagramma precedente Mostra i rettangoli seguenti:</span><span class="sxs-lookup"><span data-stu-id="d1026-342">The preceding diagram shows the following rectangles:</span></span>

-   <span data-ttu-id="d1026-343">Rettangolo di destinazione: {0, 0, 640, 480}</span><span class="sxs-lookup"><span data-stu-id="d1026-343">Target rectangle: { 0, 0, 640, 480 }</span></span>
-   <span data-ttu-id="d1026-344">Video principale:</span><span class="sxs-lookup"><span data-stu-id="d1026-344">Primary video:</span></span>

    -   <span data-ttu-id="d1026-345">Rettangolo di origine: {0, 0, 720, 480}</span><span class="sxs-lookup"><span data-stu-id="d1026-345">Source rectangle: { 0, 0, 720, 480 }</span></span>
    -   <span data-ttu-id="d1026-346">Rettangolo di destinazione: {0, 60, 640, 420}</span><span class="sxs-lookup"><span data-stu-id="d1026-346">Destination rectangle: { 0, 60, 640, 420 }</span></span>

<span data-ttu-id="d1026-347">Il driver Deinterlaccia il video, compatta il frame deinterlacciato a 640 × 360 e blit il frame nel rettangolo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="d1026-347">The driver will deinterlace the video, shrink the deinterlaced frame to 640 × 360, and blit the frame into the destination rectangle.</span></span> <span data-ttu-id="d1026-348">Il rettangolo di destinazione è più grande del rettangolo di destinazione, pertanto il driver utilizzerà il colore di sfondo per riempire le barre orizzontali sopra e sotto il frame.</span><span class="sxs-lookup"><span data-stu-id="d1026-348">The target rectangle is larger than the destination rectangle, so the driver will use the background color to fill the horizontal bars above and below the frame.</span></span> <span data-ttu-id="d1026-349">Il colore di sfondo viene specificato nella [**struttura \_ VideoProcessBltParams di DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) .</span><span class="sxs-lookup"><span data-stu-id="d1026-349">The background color is specified in the [**DXVA2\_VideoProcessBltParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) structure.</span></span>

### <a name="example-2-stretching-substream-images"></a><span data-ttu-id="d1026-350">Esempio 2: estensione delle immagini del sottoflusso</span><span class="sxs-lookup"><span data-stu-id="d1026-350">Example 2: Stretching Substream Images</span></span>

<span data-ttu-id="d1026-351">Le immagini di flussi secondari possono estendersi oltre l'immagine principale del video.</span><span class="sxs-lookup"><span data-stu-id="d1026-351">Substream pictures can extend beyond the primary video picture.</span></span> <span data-ttu-id="d1026-352">Nel video DVD, ad esempio, il flusso video primario può avere una proporzioni 4:3 mentre il sottoflusso è 16:9.</span><span class="sxs-lookup"><span data-stu-id="d1026-352">In DVD video, for example, the primary video stream can have a 4:3 aspect ratio while the substream is 16:9.</span></span> <span data-ttu-id="d1026-353">In questo esempio, entrambi i flussi video hanno le stesse dimensioni di origine (720 × 480), ma il sottoflusso deve essere visualizzato in base a un rapporto 16:9.</span><span class="sxs-lookup"><span data-stu-id="d1026-353">In this example, both video streams have the same source dimensions (720 × 480), but the substream is intended to be shown at a 16:9 aspect ratio.</span></span> <span data-ttu-id="d1026-354">Per ottenere queste proporzioni, l'immagine del sottoflusso viene allungata orizzontalmente.</span><span class="sxs-lookup"><span data-stu-id="d1026-354">To achieve this aspect ratio, the substream image is stretched horizontally.</span></span> <span data-ttu-id="d1026-355">I rettangoli di origine e di destinazione sono illustrati nel diagramma seguente.</span><span class="sxs-lookup"><span data-stu-id="d1026-355">The source and destination rectangles are shown in the following diagram.</span></span>

![diagramma che mostra l'estensione dell'immagine del flusso secondari.](images/7ab31c65-06b9-4843-90b8-2f9fb6f6b20e.gif)

<span data-ttu-id="d1026-357">Il diagramma precedente Mostra i rettangoli seguenti:</span><span class="sxs-lookup"><span data-stu-id="d1026-357">The preceding diagram shows the following rectangles:</span></span>

-   <span data-ttu-id="d1026-358">Rettangolo di destinazione: {0, 0, 854, 480}</span><span class="sxs-lookup"><span data-stu-id="d1026-358">Target rectangle: { 0, 0, 854, 480 }</span></span>
-   <span data-ttu-id="d1026-359">Video principale:</span><span class="sxs-lookup"><span data-stu-id="d1026-359">Primary video:</span></span>

    -   <span data-ttu-id="d1026-360">Rettangolo di origine: {0, 0, 720, 480}</span><span class="sxs-lookup"><span data-stu-id="d1026-360">Source rectangle: { 0, 0, 720, 480 }</span></span>
    -   <span data-ttu-id="d1026-361">Rettangolo di destinazione: {0, 107, 474, 480}</span><span class="sxs-lookup"><span data-stu-id="d1026-361">Destination rectangle: { 0, 107, 474, 480 }</span></span>

-   <span data-ttu-id="d1026-362">Substream</span><span class="sxs-lookup"><span data-stu-id="d1026-362">Substream:</span></span>
    -   <span data-ttu-id="d1026-363">Rettangolo di origine: {0, 0, 720, 480}</span><span class="sxs-lookup"><span data-stu-id="d1026-363">Source rectangle: { 0, 0, 720, 480 }</span></span>
    -   <span data-ttu-id="d1026-364">Rettangolo di destinazione: {0, 0, 854, 480}</span><span class="sxs-lookup"><span data-stu-id="d1026-364">Destination rectangle: { 0, 0, 854, 480 }</span></span>

<span data-ttu-id="d1026-365">Questi valori conservano l'altezza dell'immagine e scalano entrambe le immagini orizzontalmente.</span><span class="sxs-lookup"><span data-stu-id="d1026-365">These values preserve the image height and scale both images horizontally.</span></span> <span data-ttu-id="d1026-366">Nelle aree in cui sono visualizzate entrambe le immagini, sono con Blend alfa.</span><span class="sxs-lookup"><span data-stu-id="d1026-366">In the regions where both images appear, they are alpha blended.</span></span> <span data-ttu-id="d1026-367">Se l'immagine del sottoflusso exends oltre il video prima, il sottoflusso è alfa blended con il colore di sfondo.</span><span class="sxs-lookup"><span data-stu-id="d1026-367">Where the substream picture exends beyond the primay video, the substream is alpha blended with the background color.</span></span> <span data-ttu-id="d1026-368">Questo account di fusione alfa per i colori modificati sul lato destro del diagramma.</span><span class="sxs-lookup"><span data-stu-id="d1026-368">This alpha blending accounts for the altered colors in the right-hand side of the diagram.</span></span>

### <a name="example-3-mismatched-stream-heights"></a><span data-ttu-id="d1026-369">Esempio 3: mancata corrispondenza tra le altezze di flusso</span><span class="sxs-lookup"><span data-stu-id="d1026-369">Example 3: Mismatched Stream Heights</span></span>

<span data-ttu-id="d1026-370">Nell'esempio precedente, il sottoflusso e il flusso primario sono della stessa altezza.</span><span class="sxs-lookup"><span data-stu-id="d1026-370">In the previous example, the substream and the primary stream are the same height.</span></span> <span data-ttu-id="d1026-371">I flussi possono anche avere altezze non corrispondenti, come illustrato in questo esempio.</span><span class="sxs-lookup"><span data-stu-id="d1026-371">Streams can also have mismatched heights, as shown in this example.</span></span> <span data-ttu-id="d1026-372">Le aree all'interno del rettangolo di destinazione in cui non viene visualizzato alcun video vengono disegnate utilizzando il colore di sfondo, in questo esempio il nero.</span><span class="sxs-lookup"><span data-stu-id="d1026-372">Areas within the target rectangle where no video appears are drawn using the background color—black in this example.</span></span> <span data-ttu-id="d1026-373">I rettangoli di origine e di destinazione sono illustrati nel diagramma seguente.</span><span class="sxs-lookup"><span data-stu-id="d1026-373">The source and destination rectangles are shown in the following diagram.</span></span>

![diagramma che mostra le altezze di flusso non corrispondenti,](images/0190a15a-d971-450f-90ed-ce5633e1069c.gif)

<span data-ttu-id="d1026-375">Il diagramma precedente Mostra i rettangoli seguenti:</span><span class="sxs-lookup"><span data-stu-id="d1026-375">The preceding diagram shows the following rectangles:</span></span>

-   <span data-ttu-id="d1026-376">Rettangolo di destinazione: {0, 0, 150, 85}</span><span class="sxs-lookup"><span data-stu-id="d1026-376">Target rectangle: { 0, 0, 150, 85 }</span></span>
-   <span data-ttu-id="d1026-377">Video principale:</span><span class="sxs-lookup"><span data-stu-id="d1026-377">Primary video:</span></span>
    -   <span data-ttu-id="d1026-378">Rettangolo di origine: {0, 0, 150, 50}</span><span class="sxs-lookup"><span data-stu-id="d1026-378">Source rectangle: { 0, 0, 150, 50 }</span></span>
    -   <span data-ttu-id="d1026-379">Rettangolo di destinazione: {0, 17, 150, 67}</span><span class="sxs-lookup"><span data-stu-id="d1026-379">Destination rectangle: { 0, 17, 150, 67 }</span></span>
-   <span data-ttu-id="d1026-380">Substream</span><span class="sxs-lookup"><span data-stu-id="d1026-380">Substream:</span></span>
    -   <span data-ttu-id="d1026-381">Rettangolo di origine: {0, 0, 100, 85}</span><span class="sxs-lookup"><span data-stu-id="d1026-381">Source rectangle: { 0, 0, 100, 85 }</span></span>
    -   <span data-ttu-id="d1026-382">Rettangolo di destinazione: {25, 0, 125, 85}</span><span class="sxs-lookup"><span data-stu-id="d1026-382">Destination rectangle: { 25, 0, 125, 85 }</span></span>

### <a name="example-4-target-rectangle-smaller-than-destination-surface"></a><span data-ttu-id="d1026-383">Esempio 4: rettangolo di destinazione più piccolo della superficie di destinazione</span><span class="sxs-lookup"><span data-stu-id="d1026-383">Example 4: Target Rectangle Smaller Than Destination Surface</span></span>

<span data-ttu-id="d1026-384">In questo esempio viene illustrato un caso in cui il rettangolo di destinazione è più piccolo della superficie di destinazione.</span><span class="sxs-lookup"><span data-stu-id="d1026-384">This example shows a case where the target rectangle is smaller than the destination surface.</span></span>

![diagramma che mostra un blit a un rettangolo di destinazione.](images/360a85a3-333c-4b32-b8f7-1beb1e805921.gif)

<span data-ttu-id="d1026-386">Il diagramma precedente Mostra i rettangoli seguenti:</span><span class="sxs-lookup"><span data-stu-id="d1026-386">The preceding diagram shows the following rectangles:</span></span>

-   <span data-ttu-id="d1026-387">Superficie di destinazione: {0, 0, 300, 200}</span><span class="sxs-lookup"><span data-stu-id="d1026-387">Destination surface: { 0, 0, 300, 200 }</span></span>
-   <span data-ttu-id="d1026-388">Rettangolo di destinazione: {0, 0, 150, 85}</span><span class="sxs-lookup"><span data-stu-id="d1026-388">Target rectangle: { 0, 0, 150, 85 }</span></span>
-   <span data-ttu-id="d1026-389">Video principale:</span><span class="sxs-lookup"><span data-stu-id="d1026-389">Primary video:</span></span>
    -   <span data-ttu-id="d1026-390">Rettangolo di origine: {0, 0, 150, 50}</span><span class="sxs-lookup"><span data-stu-id="d1026-390">Source rectangle: { 0, 0, 150, 50 }</span></span>
    -   <span data-ttu-id="d1026-391">Rettangolo di destinazione: {0, 17, 150, 67}</span><span class="sxs-lookup"><span data-stu-id="d1026-391">Destination rectangle: { 0, 17, 150, 67 }</span></span>
-   <span data-ttu-id="d1026-392">Substream</span><span class="sxs-lookup"><span data-stu-id="d1026-392">Substream:</span></span>
    -   <span data-ttu-id="d1026-393">Rettangolo di origine: {0, 0, 100, 85}</span><span class="sxs-lookup"><span data-stu-id="d1026-393">Source rectangle: { 0, 0, 100, 85 }</span></span>
    -   <span data-ttu-id="d1026-394">Rettangolo di destinazione: {25, 0, 125, 85}</span><span class="sxs-lookup"><span data-stu-id="d1026-394">Destination rectangle: { 25, 0, 125, 85 }</span></span>

<span data-ttu-id="d1026-395">I pixel all'esterno del rettangolo di destinazione non vengono modificati, pertanto il colore di sfondo viene visualizzato solo all'interno del rettangolo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="d1026-395">Pixels outside of the target rectangle are not modified, so the background color appears only within the target rectangle.</span></span> <span data-ttu-id="d1026-396">L'area tratteggiata indica parti della superficie di destinazione che non sono interessate dal blit.</span><span class="sxs-lookup"><span data-stu-id="d1026-396">The dotted area indicates portions of the destination surface that are not affected by the blit.</span></span>

### <a name="example-5-source-rectangles"></a><span data-ttu-id="d1026-397">Esempio 5: rettangoli di origine</span><span class="sxs-lookup"><span data-stu-id="d1026-397">Example 5: Source Rectangles</span></span>

<span data-ttu-id="d1026-398">Se si specifica un rettangolo di origine inferiore a quello dell'immagine di origine, il driver blit solo quella parte dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="d1026-398">If you specify a source rectangle that is smaller than the source picture, the driver will blit just that portion of the picture.</span></span> <span data-ttu-id="d1026-399">In questo esempio, i rettangoli di origine specificano il quadrante inferiore destro del flusso video primario e il quadrante inferiore sinistro del sottoflusso, indicato dai contrassegni hash nel diagramma.</span><span class="sxs-lookup"><span data-stu-id="d1026-399">In this example, the source rectangles specify the lower-right quadrant of the primary video stream and the lower-left quadrant of the substream (indicated by hash marks in the diagram).</span></span> <span data-ttu-id="d1026-400">I rettangoli di destinazione hanno le stesse dimensioni dei rettangoli di origine, quindi il video non viene allungato.</span><span class="sxs-lookup"><span data-stu-id="d1026-400">The destination rectangles are the same sizes as the source rectangles, so the video is not stretched.</span></span> <span data-ttu-id="d1026-401">I rettangoli di origine e di destinazione sono illustrati nel diagramma seguente.</span><span class="sxs-lookup"><span data-stu-id="d1026-401">The source and destination rectangles are shown in the following diagram.</span></span>

![diagramma che mostra un blit da due rettangoli di origine.](images/b1de4cc3-0155-40be-acac-b486e2af8c0d.gif)

<span data-ttu-id="d1026-403">Il diagramma precedente Mostra i rettangoli seguenti:</span><span class="sxs-lookup"><span data-stu-id="d1026-403">The preceding diagram shows the following rectangles:</span></span>

-   <span data-ttu-id="d1026-404">Rettangolo di destinazione: {0, 0, 720, 576}</span><span class="sxs-lookup"><span data-stu-id="d1026-404">Target rectangle: { 0, 0, 720, 576 }</span></span>
-   <span data-ttu-id="d1026-405">Video principale:</span><span class="sxs-lookup"><span data-stu-id="d1026-405">Primary video:</span></span>
    -   <span data-ttu-id="d1026-406">Dimensioni superficie di origine: {0, 0, 720, 480}</span><span class="sxs-lookup"><span data-stu-id="d1026-406">Source surface size: { 0, 0, 720, 480 }</span></span>
    -   <span data-ttu-id="d1026-407">Rettangolo di origine: {360, 240, 720, 480}</span><span class="sxs-lookup"><span data-stu-id="d1026-407">Source rectangle: { 360, 240, 720, 480 }</span></span>
    -   <span data-ttu-id="d1026-408">Rettangolo di destinazione: {0, 0, 360, 240}</span><span class="sxs-lookup"><span data-stu-id="d1026-408">Destination rectangle: { 0, 0, 360, 240 }</span></span>
-   <span data-ttu-id="d1026-409">Substream</span><span class="sxs-lookup"><span data-stu-id="d1026-409">Substream:</span></span>
    -   <span data-ttu-id="d1026-410">Dimensioni superficie di origine: {0, 0, 640, 576}</span><span class="sxs-lookup"><span data-stu-id="d1026-410">Source surface size: { 0, 0, 640, 576 }</span></span>
    -   <span data-ttu-id="d1026-411">Rettangolo di origine: {0, 288, 320, 576}</span><span class="sxs-lookup"><span data-stu-id="d1026-411">Source rectangle: { 0, 288, 320, 576 }</span></span>
    -   <span data-ttu-id="d1026-412">Rettangolo di destinazione: {400, 0, 720, 288}</span><span class="sxs-lookup"><span data-stu-id="d1026-412">Destination rectangle: { 400, 0, 720, 288 }</span></span>

### <a name="example-6-intersecting-destination-rectangles"></a><span data-ttu-id="d1026-413">Esempio 6: intersezione di rettangoli di destinazione</span><span class="sxs-lookup"><span data-stu-id="d1026-413">Example 6: Intersecting Destination Rectangles</span></span>

<span data-ttu-id="d1026-414">Questo esempio è simile a quello precedente, ma i rettangoli di destinazione si intersecano.</span><span class="sxs-lookup"><span data-stu-id="d1026-414">This example is similar to previous one, but the destination rectangles intersect.</span></span> <span data-ttu-id="d1026-415">Le dimensioni della superficie sono identiche a quelle dell'esempio precedente, ma i rettangoli di origine e di destinazione non lo sono.</span><span class="sxs-lookup"><span data-stu-id="d1026-415">The surface dimensions are the same as in the previous example, but the source and destination rectangles are not.</span></span> <span data-ttu-id="d1026-416">Anche in questo caso, il video viene ritagliato ma non allungato.</span><span class="sxs-lookup"><span data-stu-id="d1026-416">Again, the video is cropped but not stretched.</span></span> <span data-ttu-id="d1026-417">I rettangoli di origine e di destinazione sono illustrati nel diagramma seguente.</span><span class="sxs-lookup"><span data-stu-id="d1026-417">The source and destination rectangles are shown in the following diagram.</span></span>

![diagramma che mostra i rettangoli di destinazione intersecanti.](images/fbe450cb-c84d-4110-9515-00f27601528e.gif)

<span data-ttu-id="d1026-419">Il diagramma precedente Mostra i rettangoli seguenti:</span><span class="sxs-lookup"><span data-stu-id="d1026-419">The preceding diagram shows the following rectangles:</span></span>

-   <span data-ttu-id="d1026-420">Rettangolo di destinazione: {0, 0, 720, 576}</span><span class="sxs-lookup"><span data-stu-id="d1026-420">Target rectangle: { 0, 0, 720, 576 }</span></span>
-   <span data-ttu-id="d1026-421">Video principale:</span><span class="sxs-lookup"><span data-stu-id="d1026-421">Primary video:</span></span>
    -   <span data-ttu-id="d1026-422">Dimensioni superficie di origine: {0, 0, 720, 480}</span><span class="sxs-lookup"><span data-stu-id="d1026-422">Source surface size: { 0, 0, 720, 480 }</span></span>
    -   <span data-ttu-id="d1026-423">Rettangolo di origine: {260, 92, 720, 480}</span><span class="sxs-lookup"><span data-stu-id="d1026-423">Source rectangle: { 260, 92, 720, 480 }</span></span>
    -   <span data-ttu-id="d1026-424">Rettangolo di destinazione: {0, 0, 460, 388}</span><span class="sxs-lookup"><span data-stu-id="d1026-424">Destination rectangle: { 0, 0, 460, 388 }</span></span>
-   <span data-ttu-id="d1026-425">Substream</span><span class="sxs-lookup"><span data-stu-id="d1026-425">Substream:</span></span>
    -   <span data-ttu-id="d1026-426">Dimensioni superficie di origine: {0, 0, 640, 576}</span><span class="sxs-lookup"><span data-stu-id="d1026-426">Source surface size: { 0, 0, 640, 576 }</span></span>
    -   <span data-ttu-id="d1026-427">Rettangolo di origine: {0, 0, 460, 388}</span><span class="sxs-lookup"><span data-stu-id="d1026-427">Source rectangle: { 0, 0, 460, 388 }</span></span>
    -   <span data-ttu-id="d1026-428">Rettangolo di destinazione: {260, 188, 720, 576}</span><span class="sxs-lookup"><span data-stu-id="d1026-428">Destination rectangle: { 260, 188, 720, 576 }</span></span>

### <a name="example-7-stretching-and-cropping-video"></a><span data-ttu-id="d1026-429">Esempio 7: allungamento e ritaglio di video</span><span class="sxs-lookup"><span data-stu-id="d1026-429">Example 7: Stretching and Cropping Video</span></span>

<span data-ttu-id="d1026-430">In questo esempio il video è allungato e ritagliato.</span><span class="sxs-lookup"><span data-stu-id="d1026-430">In this example, the video is stretched as well as cropped.</span></span> <span data-ttu-id="d1026-431">Un'area 180 × 120 da ogni flusso viene estesa per coprire un'area 360 × 240 nel rettangolo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="d1026-431">A 180 × 120 region from each stream is stretched to cover a 360 × 240 area in the destination rectangle.</span></span>

![diagramma che mostra l'estensione e il ritaglio.](images/ce83529c-8545-492c-9d3e-ef221c30e326.gif)

<span data-ttu-id="d1026-433">Il diagramma precedente Mostra i rettangoli seguenti:</span><span class="sxs-lookup"><span data-stu-id="d1026-433">The preceding diagram shows the following rectangles:</span></span>

-   <span data-ttu-id="d1026-434">Rettangolo di destinazione: {0, 0, 720, 480}</span><span class="sxs-lookup"><span data-stu-id="d1026-434">Target rectangle: { 0, 0, 720, 480 }</span></span>
-   <span data-ttu-id="d1026-435">Video principale:</span><span class="sxs-lookup"><span data-stu-id="d1026-435">Primary video:</span></span>
    -   <span data-ttu-id="d1026-436">Dimensioni superficie di origine: {0, 0, 360, 240}</span><span class="sxs-lookup"><span data-stu-id="d1026-436">Source surface size: { 0, 0, 360, 240 }</span></span>
    -   <span data-ttu-id="d1026-437">Rettangolo di origine: {180, 120, 360, 240}</span><span class="sxs-lookup"><span data-stu-id="d1026-437">Source rectangle: { 180, 120, 360, 240 }</span></span>
    -   <span data-ttu-id="d1026-438">Rettangolo di destinazione: {0, 0, 360, 240}</span><span class="sxs-lookup"><span data-stu-id="d1026-438">Destination rectangle: { 0, 0, 360, 240 }</span></span>
-   <span data-ttu-id="d1026-439">Substream</span><span class="sxs-lookup"><span data-stu-id="d1026-439">Substream:</span></span>
    -   <span data-ttu-id="d1026-440">Dimensioni superficie di origine: {0, 0, 360, 240}</span><span class="sxs-lookup"><span data-stu-id="d1026-440">Source surface size: { 0, 0, 360, 240 }</span></span>
    -   <span data-ttu-id="d1026-441">Rettangolo di origine: {0, 0, 180, 120}</span><span class="sxs-lookup"><span data-stu-id="d1026-441">Source rectangle: { 0, 0, 180, 120 }</span></span>
    -   <span data-ttu-id="d1026-442">Rettangolo di destinazione: {360, 240, 720, 480}</span><span class="sxs-lookup"><span data-stu-id="d1026-442">Destination rectangle: { 360, 240, 720, 480 }</span></span>

## <a name="input-sample-order"></a><span data-ttu-id="d1026-443">Ordine di esempio di input</span><span class="sxs-lookup"><span data-stu-id="d1026-443">Input Sample Order</span></span>

<span data-ttu-id="d1026-444">Il parametro *pSamples* del metodo [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) è un puntatore a una matrice di esempi di input.</span><span class="sxs-lookup"><span data-stu-id="d1026-444">The *pSamples* parameter of the [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) method is a pointer to an array of input samples.</span></span> <span data-ttu-id="d1026-445">Gli esempi dal flusso video primario vengono visualizzati per primi, seguiti da immagini substream nell'ordine Z.</span><span class="sxs-lookup"><span data-stu-id="d1026-445">Samples from the primary video stream appear first, followed by substream pictures in Z-order.</span></span> <span data-ttu-id="d1026-446">Gli esempi devono essere inseriti nella matrice nell'ordine seguente:</span><span class="sxs-lookup"><span data-stu-id="d1026-446">Samples must be placed into the array in the following order:</span></span>

-   <span data-ttu-id="d1026-447">Gli esempi per il flusso video primario vengono visualizzati per primi nella matrice, in ordine temporale.</span><span class="sxs-lookup"><span data-stu-id="d1026-447">Samples for the primary video stream appear first in the array, in temporal order.</span></span> <span data-ttu-id="d1026-448">A seconda della modalità di deinterlacciamento, il driver potrebbe richiedere uno o più esempi di riferimento dal flusso video primario.</span><span class="sxs-lookup"><span data-stu-id="d1026-448">Depending on the deinterlace mode, the driver may require one or more reference samples from the primary video stream.</span></span> <span data-ttu-id="d1026-449">I membri **NumForwardRefSamples** e **NumBackwardRefSamples** della struttura [**DXVA2 \_ VideoProcessorCaps**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessorcaps) specificano il numero di campioni di riferimento avanti e indietro necessari.</span><span class="sxs-lookup"><span data-stu-id="d1026-449">The **NumForwardRefSamples** and **NumBackwardRefSamples** members of the [**DXVA2\_VideoProcessorCaps**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessorcaps) structure specify how many forward and backward reference samples are needed.</span></span> <span data-ttu-id="d1026-450">Il chiamante deve fornire questi esempi di riferimento anche se il contenuto video è progressivo e non richiede la deinterlacciamento.</span><span class="sxs-lookup"><span data-stu-id="d1026-450">The caller must provide these reference samples even if the video content is progressive and does not require deinterlacing.</span></span> <span data-ttu-id="d1026-451">Questa situazione può verificarsi quando si assegnano frame progressivi a un dispositivo di deinterlacciamento, ad esempio quando l'origine contiene una combinazione di frame sia interlacciati che progressivi.</span><span class="sxs-lookup"><span data-stu-id="d1026-451">(This can occur when progressive frames are given to a deinterlacing device, for example when the source contains a mix of both interlaced and progressive frames.)</span></span>
-   <span data-ttu-id="d1026-452">Dopo gli esempi per il flusso video primario, la matrice può contenere fino a 15 campioni di sottoflusso, disposti in ordine Z, dal basso verso l'alto.</span><span class="sxs-lookup"><span data-stu-id="d1026-452">After the samples for the primary video stream, the array can contain up to 15 substream samples, arranged in Z-order, from bottom to top.</span></span> <span data-ttu-id="d1026-453">I flussi secondari sono sempre progressivi e non richiedono immagini di riferimento.</span><span class="sxs-lookup"><span data-stu-id="d1026-453">Substreams are always progressive and do not require reference pictures.</span></span>

<span data-ttu-id="d1026-454">In qualsiasi momento, il flusso video primario può passare da contenuto interlacciato a quello progressivo e il numero di flussi subesistenti può cambiare.</span><span class="sxs-lookup"><span data-stu-id="d1026-454">At any time, the primary video stream can switch between interlaced and progressive content, and the number of substreams can change.</span></span>

<span data-ttu-id="d1026-455">Il membro **SampleFormat. SampleFormat** della struttura [**DXVA2 \_ VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) indica il tipo di immagine.</span><span class="sxs-lookup"><span data-stu-id="d1026-455">The **SampleFormat.SampleFormat** member of the [**DXVA2\_VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) structure indicates the type of picture.</span></span> <span data-ttu-id="d1026-456">Per le immagini di flussi secondari, impostare questo valore su DXVA2 \_ SampleSubStream.</span><span class="sxs-lookup"><span data-stu-id="d1026-456">For substream pictures, set this value to DXVA2\_SampleSubStream.</span></span> <span data-ttu-id="d1026-457">Per le immagini progressive, il valore è DXVA2 \_ SampleProgressiveFrame.</span><span class="sxs-lookup"><span data-stu-id="d1026-457">For progressive pictures, the value is DXVA2\_SampleProgressiveFrame.</span></span> <span data-ttu-id="d1026-458">Per le immagini interlacciate, il valore dipende dal layout del campo.</span><span class="sxs-lookup"><span data-stu-id="d1026-458">For interlaced pictures, the value depends on the field layout.</span></span>

<span data-ttu-id="d1026-459">Se il driver richiede esempi di riferimento avanti e indietro, il numero completo di campioni potrebbe non essere disponibile all'inizio della sequenza video.</span><span class="sxs-lookup"><span data-stu-id="d1026-459">If the driver requires forward and backward reference samples, the full number of samples might not be available at the start of the video sequence.</span></span> <span data-ttu-id="d1026-460">In tal caso, includere le relative voci nella matrice *pSamples* , ma contrassegnare i campioni mancanti con il tipo DXVA2 \_ SampleUnknown.</span><span class="sxs-lookup"><span data-stu-id="d1026-460">In that case, include entries for them in the *pSamples* array, but mark the missing samples as having type DXVA2\_SampleUnknown.</span></span>

<span data-ttu-id="d1026-461">I membri **iniziale** e **finale** della struttura [**DXVA2 \_ VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) forniscono la posizione temporale di ogni campione.</span><span class="sxs-lookup"><span data-stu-id="d1026-461">The **Start** and **End** members of the [**DXVA2\_VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) structure give the temporal location of each sample.</span></span> <span data-ttu-id="d1026-462">Questi valori vengono usati solo per gli esempi dal flusso video primario.</span><span class="sxs-lookup"><span data-stu-id="d1026-462">These values are used only for samples from the primary video stream.</span></span> <span data-ttu-id="d1026-463">Per le immagini di flussi secondari, impostare entrambi i membri su zero.</span><span class="sxs-lookup"><span data-stu-id="d1026-463">For substream pictures, set both members to zero.</span></span>

<span data-ttu-id="d1026-464">Gli esempi seguenti possono essere utili per chiarire tali requisiti.</span><span class="sxs-lookup"><span data-stu-id="d1026-464">The following examples may help to clarify these requirements.</span></span>

### <a name="example-1"></a><span data-ttu-id="d1026-465">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d1026-465">Example 1</span></span>

<span data-ttu-id="d1026-466">Il caso più semplice si verifica quando non sono presenti sottoflussi e l'algoritmo di deinterlacciamento non richiede esempi di riferimento (**NumForwardRefSamples** e **NumBackwardRefSamples** sono entrambi zero).</span><span class="sxs-lookup"><span data-stu-id="d1026-466">The simplest case occurs when there are no substreams and the deinterlacing algorithm does not require reference samples (**NumForwardRefSamples** and **NumBackwardRefSamples** are both zero).</span></span> <span data-ttu-id="d1026-467">Il deinterlacciamento Bob è un esempio di tale algoritmo.</span><span class="sxs-lookup"><span data-stu-id="d1026-467">Bob deinterlacing is an example of such an algorithm.</span></span> <span data-ttu-id="d1026-468">In questo caso, la matrice *pSamples* deve contenere una singola superficie di input, come illustrato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="d1026-468">In this case, the *pSamples* array should contain a single input surface, as shown in the following table.</span></span>



| <span data-ttu-id="d1026-469">Indice</span><span class="sxs-lookup"><span data-stu-id="d1026-469">Index</span></span>           | <span data-ttu-id="d1026-470">Tipo di superficie</span><span class="sxs-lookup"><span data-stu-id="d1026-470">Surface type</span></span>        | <span data-ttu-id="d1026-471">Posizione temporale</span><span class="sxs-lookup"><span data-stu-id="d1026-471">Temporal location</span></span> |
|-----------------|---------------------|-------------------|
| <span data-ttu-id="d1026-472">*pSamples* \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="d1026-472">*pSamples*\[0\]</span></span> | <span data-ttu-id="d1026-473">Immagine interlacciata.</span><span class="sxs-lookup"><span data-stu-id="d1026-473">Interlaced picture.</span></span> | <span data-ttu-id="d1026-474">*T*</span><span class="sxs-lookup"><span data-stu-id="d1026-474">*T*</span></span>               |



 

<span data-ttu-id="d1026-475">Si presuppone che il valore time *T* sia l'ora di inizio del fotogramma video corrente.</span><span class="sxs-lookup"><span data-stu-id="d1026-475">The time value *T* is assumed to be the start time of the current video frame.</span></span>

### <a name="example-2"></a><span data-ttu-id="d1026-476">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="d1026-476">Example 2</span></span>

<span data-ttu-id="d1026-477">In questo esempio, l'applicazione combina due sottoflussi con il flusso primario.</span><span class="sxs-lookup"><span data-stu-id="d1026-477">In this example, the application mixes two substreams with the primary stream.</span></span> <span data-ttu-id="d1026-478">L'algoritmo di deinterlacciamento non richiede esempi di riferimento.</span><span class="sxs-lookup"><span data-stu-id="d1026-478">The deinterlacing algorithm does not require reference samples.</span></span> <span data-ttu-id="d1026-479">Nella tabella seguente viene illustrato il modo in cui questi esempi vengono disposti nella matrice *pSamples* .</span><span class="sxs-lookup"><span data-stu-id="d1026-479">The following table shows how these samples are arranged in the *pSamples* array.</span></span>



| <span data-ttu-id="d1026-480">Indice</span><span class="sxs-lookup"><span data-stu-id="d1026-480">Index</span></span>           | <span data-ttu-id="d1026-481">Tipo di superficie</span><span class="sxs-lookup"><span data-stu-id="d1026-481">Surface type</span></span>       | <span data-ttu-id="d1026-482">Posizione temporale</span><span class="sxs-lookup"><span data-stu-id="d1026-482">Temporal location</span></span> | <span data-ttu-id="d1026-483">Ordine Z</span><span class="sxs-lookup"><span data-stu-id="d1026-483">Z-order</span></span> |
|-----------------|--------------------|-------------------|---------|
| <span data-ttu-id="d1026-484">*pSamples* \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="d1026-484">*pSamples*\[0\]</span></span> | <span data-ttu-id="d1026-485">Immagine interlacciata</span><span class="sxs-lookup"><span data-stu-id="d1026-485">Interlaced picture</span></span> | <span data-ttu-id="d1026-486">*T*</span><span class="sxs-lookup"><span data-stu-id="d1026-486">*T*</span></span>               | <span data-ttu-id="d1026-487">0</span><span class="sxs-lookup"><span data-stu-id="d1026-487">0</span></span>       |
| <span data-ttu-id="d1026-488">*pSamples* \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="d1026-488">*pSamples*\[1\]</span></span> | <span data-ttu-id="d1026-489">Substream</span><span class="sxs-lookup"><span data-stu-id="d1026-489">Substream</span></span>          | <span data-ttu-id="d1026-490">0</span><span class="sxs-lookup"><span data-stu-id="d1026-490">0</span></span>                 | <span data-ttu-id="d1026-491">1</span><span class="sxs-lookup"><span data-stu-id="d1026-491">1</span></span>       |
| <span data-ttu-id="d1026-492">*pSamples* \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="d1026-492">*pSamples*\[2\]</span></span> | <span data-ttu-id="d1026-493">Substream</span><span class="sxs-lookup"><span data-stu-id="d1026-493">Substream</span></span>          | <span data-ttu-id="d1026-494">0</span><span class="sxs-lookup"><span data-stu-id="d1026-494">0</span></span>                 | <span data-ttu-id="d1026-495">2</span><span class="sxs-lookup"><span data-stu-id="d1026-495">2</span></span>       |



 

### <a name="example-3"></a><span data-ttu-id="d1026-496">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="d1026-496">Example 3</span></span>

<span data-ttu-id="d1026-497">Si supponga ora che l'algoritmo di deinterlacciamento richieda un esempio di riferimento all'indietro e un esempio di riferimento in avanti.</span><span class="sxs-lookup"><span data-stu-id="d1026-497">Now suppose that the deinterlacing algorithm requires one backward reference sample and one forward reference sample.</span></span> <span data-ttu-id="d1026-498">Vengono inoltre fornite due immagini di flussi secondari, per un totale di cinque superfici.</span><span class="sxs-lookup"><span data-stu-id="d1026-498">In addition, two substream pictures are provided, for a total of five surfaces.</span></span> <span data-ttu-id="d1026-499">L'ordinamento corretto è illustrato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="d1026-499">The correct ordering is shown in the following table.</span></span>



| <span data-ttu-id="d1026-500">Indice</span><span class="sxs-lookup"><span data-stu-id="d1026-500">Index</span></span>           | <span data-ttu-id="d1026-501">Tipo di superficie</span><span class="sxs-lookup"><span data-stu-id="d1026-501">Surface type</span></span>                   | <span data-ttu-id="d1026-502">Posizione temporale</span><span class="sxs-lookup"><span data-stu-id="d1026-502">Temporal location</span></span> | <span data-ttu-id="d1026-503">Ordine Z</span><span class="sxs-lookup"><span data-stu-id="d1026-503">Z-order</span></span>        |
|-----------------|--------------------------------|-------------------|----------------|
| <span data-ttu-id="d1026-504">*pSamples* \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="d1026-504">*pSamples*\[0\]</span></span> | <span data-ttu-id="d1026-505">Immagine interlacciata (riferimento)</span><span class="sxs-lookup"><span data-stu-id="d1026-505">Interlaced picture (reference)</span></span> | <span data-ttu-id="d1026-506">*T* − 1</span><span class="sxs-lookup"><span data-stu-id="d1026-506">*T* −1</span></span>            | <span data-ttu-id="d1026-507">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="d1026-507">Not applicable</span></span> |
| <span data-ttu-id="d1026-508">*pSamples* \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="d1026-508">*pSamples*\[1\]</span></span> | <span data-ttu-id="d1026-509">Immagine interlacciata</span><span class="sxs-lookup"><span data-stu-id="d1026-509">Interlaced picture</span></span>             | <span data-ttu-id="d1026-510">*T*</span><span class="sxs-lookup"><span data-stu-id="d1026-510">*T*</span></span>               | <span data-ttu-id="d1026-511">0</span><span class="sxs-lookup"><span data-stu-id="d1026-511">0</span></span>              |
| <span data-ttu-id="d1026-512">*pSamples* \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="d1026-512">*pSamples*\[2\]</span></span> | <span data-ttu-id="d1026-513">Immagine interlacciata (riferimento)</span><span class="sxs-lookup"><span data-stu-id="d1026-513">Interlaced picture (reference)</span></span> | <span data-ttu-id="d1026-514">*T* + 1</span><span class="sxs-lookup"><span data-stu-id="d1026-514">*T* +1</span></span>            | <span data-ttu-id="d1026-515">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="d1026-515">Not applicable</span></span> |
| <span data-ttu-id="d1026-516">*pSamples* \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="d1026-516">*pSamples*\[3\]</span></span> | <span data-ttu-id="d1026-517">Substream</span><span class="sxs-lookup"><span data-stu-id="d1026-517">Substream</span></span>                      | <span data-ttu-id="d1026-518">0</span><span class="sxs-lookup"><span data-stu-id="d1026-518">0</span></span>                 | <span data-ttu-id="d1026-519">1</span><span class="sxs-lookup"><span data-stu-id="d1026-519">1</span></span>              |
| <span data-ttu-id="d1026-520">*pSamples* \[ 4\]</span><span class="sxs-lookup"><span data-stu-id="d1026-520">*pSamples*\[4\]</span></span> | <span data-ttu-id="d1026-521">Substream</span><span class="sxs-lookup"><span data-stu-id="d1026-521">Substream</span></span>                      | <span data-ttu-id="d1026-522">0</span><span class="sxs-lookup"><span data-stu-id="d1026-522">0</span></span>                 | <span data-ttu-id="d1026-523">2</span><span class="sxs-lookup"><span data-stu-id="d1026-523">2</span></span>              |



 

<span data-ttu-id="d1026-524">L'ora *t* − 1 è l'ora di inizio del frame prima del frame corrente e *T* + 1 è l'ora di inizio del frame seguente.</span><span class="sxs-lookup"><span data-stu-id="d1026-524">The time *T* −1 is the start time of the frame before the current frame, and *T* +1 is the start time of the following frame.</span></span>

<span data-ttu-id="d1026-525">Se il flusso video passa al contenuto progressivo, usando la stessa modalità di deinterlacciamento, l'applicazione deve fornire lo stesso numero di campioni, come illustrato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="d1026-525">If the video stream switches to progressive content, using the same deinterlacing mode, the application must provide the same number of samples, as shown in the following table.</span></span>



| <span data-ttu-id="d1026-526">Indice</span><span class="sxs-lookup"><span data-stu-id="d1026-526">Index</span></span>           | <span data-ttu-id="d1026-527">Tipo di superficie</span><span class="sxs-lookup"><span data-stu-id="d1026-527">Surface type</span></span>                    | <span data-ttu-id="d1026-528">Posizione temporale</span><span class="sxs-lookup"><span data-stu-id="d1026-528">Temporal location</span></span> | <span data-ttu-id="d1026-529">Ordine Z</span><span class="sxs-lookup"><span data-stu-id="d1026-529">Z-order</span></span>        |
|-----------------|---------------------------------|-------------------|----------------|
| <span data-ttu-id="d1026-530">*pSamples* \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="d1026-530">*pSamples*\[0\]</span></span> | <span data-ttu-id="d1026-531">Immagine progressiva (riferimento)</span><span class="sxs-lookup"><span data-stu-id="d1026-531">Progressive picture (reference)</span></span> | <span data-ttu-id="d1026-532">*T* − 1</span><span class="sxs-lookup"><span data-stu-id="d1026-532">*T* −1</span></span>            | <span data-ttu-id="d1026-533">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="d1026-533">Not applicable</span></span> |
| <span data-ttu-id="d1026-534">*pSamples* \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="d1026-534">*pSamples*\[1\]</span></span> | <span data-ttu-id="d1026-535">Immagine progressiva</span><span class="sxs-lookup"><span data-stu-id="d1026-535">Progressive picture</span></span>             | <span data-ttu-id="d1026-536">*T*</span><span class="sxs-lookup"><span data-stu-id="d1026-536">*T*</span></span>               | <span data-ttu-id="d1026-537">0</span><span class="sxs-lookup"><span data-stu-id="d1026-537">0</span></span>              |
| <span data-ttu-id="d1026-538">*pSamples* \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="d1026-538">*pSamples*\[2\]</span></span> | <span data-ttu-id="d1026-539">Immagine progressiva (riferimento)</span><span class="sxs-lookup"><span data-stu-id="d1026-539">Progressive picture (reference)</span></span> | <span data-ttu-id="d1026-540">*T* + 1</span><span class="sxs-lookup"><span data-stu-id="d1026-540">*T* +1</span></span>            | <span data-ttu-id="d1026-541">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="d1026-541">Not applicable</span></span> |
| <span data-ttu-id="d1026-542">*pSamples* \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="d1026-542">*pSamples*\[3\]</span></span> | <span data-ttu-id="d1026-543">Substream</span><span class="sxs-lookup"><span data-stu-id="d1026-543">Substream</span></span>                       | <span data-ttu-id="d1026-544">0</span><span class="sxs-lookup"><span data-stu-id="d1026-544">0</span></span>                 | <span data-ttu-id="d1026-545">1</span><span class="sxs-lookup"><span data-stu-id="d1026-545">1</span></span>              |
| <span data-ttu-id="d1026-546">*pSamples* \[ 4\]</span><span class="sxs-lookup"><span data-stu-id="d1026-546">*pSamples*\[4\]</span></span> | <span data-ttu-id="d1026-547">Substream</span><span class="sxs-lookup"><span data-stu-id="d1026-547">Substream</span></span>                       | <span data-ttu-id="d1026-548">0</span><span class="sxs-lookup"><span data-stu-id="d1026-548">0</span></span>                 | <span data-ttu-id="d1026-549">2</span><span class="sxs-lookup"><span data-stu-id="d1026-549">2</span></span>              |



 

### <a name="example-4"></a><span data-ttu-id="d1026-550">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="d1026-550">Example 4</span></span>

<span data-ttu-id="d1026-551">All'inizio di una sequenza video, gli esempi di riferimento avanti e indietro potrebbero non essere disponibili.</span><span class="sxs-lookup"><span data-stu-id="d1026-551">At the start of a video sequence, forward and backward reference samples might not be available.</span></span> <span data-ttu-id="d1026-552">Quando si verifica questa situazione, le voci degli esempi mancanti sono incluse nella matrice *pSamples* , con il tipo di esempio DXVA2 \_ SampleUnknown.</span><span class="sxs-lookup"><span data-stu-id="d1026-552">When this happens, entries for the missing samples are included in the *pSamples* array, with sample type DXVA2\_SampleUnknown.</span></span>

<span data-ttu-id="d1026-553">Supponendo che la modalità di deinterlacciamento necessiti di un esempio di riferimento a ritroso e in avanti, le prime tre chiamate a [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) avrebbero le sequenze di input visualizzate nelle tre tabelle seguenti.</span><span class="sxs-lookup"><span data-stu-id="d1026-553">Assuming that the deinterlacing mode needs one forward and one backward reference sample, the first three calls to [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) would have the sequences of inputs shown in the following three tables.</span></span>



| <span data-ttu-id="d1026-554">Indice</span><span class="sxs-lookup"><span data-stu-id="d1026-554">Index</span></span>           | <span data-ttu-id="d1026-555">Tipo di superficie</span><span class="sxs-lookup"><span data-stu-id="d1026-555">Surface type</span></span>                   | <span data-ttu-id="d1026-556">Posizione temporale</span><span class="sxs-lookup"><span data-stu-id="d1026-556">Temporal location</span></span> |
|-----------------|--------------------------------|-------------------|
| <span data-ttu-id="d1026-557">*pSamples* \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="d1026-557">*pSamples*\[0\]</span></span> | <span data-ttu-id="d1026-558">Sconosciuto</span><span class="sxs-lookup"><span data-stu-id="d1026-558">Unknown</span></span>                        | <span data-ttu-id="d1026-559">0</span><span class="sxs-lookup"><span data-stu-id="d1026-559">0</span></span>                 |
| <span data-ttu-id="d1026-560">*pSamples* \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="d1026-560">*pSamples*\[1\]</span></span> | <span data-ttu-id="d1026-561">Sconosciuto</span><span class="sxs-lookup"><span data-stu-id="d1026-561">Unknown</span></span>                        | <span data-ttu-id="d1026-562">0</span><span class="sxs-lookup"><span data-stu-id="d1026-562">0</span></span>                 |
| <span data-ttu-id="d1026-563">*pSamples* \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="d1026-563">*pSamples*\[2\]</span></span> | <span data-ttu-id="d1026-564">Immagine interlacciata (riferimento)</span><span class="sxs-lookup"><span data-stu-id="d1026-564">Interlaced picture (reference)</span></span> | <span data-ttu-id="d1026-565">*T* + 1</span><span class="sxs-lookup"><span data-stu-id="d1026-565">*T* +1</span></span>            |



 



| <span data-ttu-id="d1026-566">Indice</span><span class="sxs-lookup"><span data-stu-id="d1026-566">Index</span></span>           | <span data-ttu-id="d1026-567">Tipo di superficie</span><span class="sxs-lookup"><span data-stu-id="d1026-567">Surface type</span></span>                   | <span data-ttu-id="d1026-568">Posizione temporale</span><span class="sxs-lookup"><span data-stu-id="d1026-568">Temporal location</span></span> |
|-----------------|--------------------------------|-------------------|
| <span data-ttu-id="d1026-569">*pSamples* \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="d1026-569">*pSamples*\[0\]</span></span> | <span data-ttu-id="d1026-570">Sconosciuto</span><span class="sxs-lookup"><span data-stu-id="d1026-570">Unknown</span></span>                        | <span data-ttu-id="d1026-571">0</span><span class="sxs-lookup"><span data-stu-id="d1026-571">0</span></span>                 |
| <span data-ttu-id="d1026-572">*pSamples* \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="d1026-572">*pSamples*\[1\]</span></span> | <span data-ttu-id="d1026-573">Immagine interlacciata</span><span class="sxs-lookup"><span data-stu-id="d1026-573">Interlaced picture</span></span>             | <span data-ttu-id="d1026-574">*T*</span><span class="sxs-lookup"><span data-stu-id="d1026-574">*T*</span></span>               |
| <span data-ttu-id="d1026-575">*pSamples* \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="d1026-575">*pSamples*\[2\]</span></span> | <span data-ttu-id="d1026-576">Immagine interlacciata (riferimento)</span><span class="sxs-lookup"><span data-stu-id="d1026-576">Interlaced picture (reference)</span></span> | <span data-ttu-id="d1026-577">*T* + 1</span><span class="sxs-lookup"><span data-stu-id="d1026-577">*T* +1</span></span>            |



 



| <span data-ttu-id="d1026-578">Indice</span><span class="sxs-lookup"><span data-stu-id="d1026-578">Index</span></span>           | <span data-ttu-id="d1026-579">Tipo di superficie</span><span class="sxs-lookup"><span data-stu-id="d1026-579">Surface type</span></span>                   | <span data-ttu-id="d1026-580">Posizione temporale</span><span class="sxs-lookup"><span data-stu-id="d1026-580">Temporal location</span></span> |
|-----------------|--------------------------------|-------------------|
| <span data-ttu-id="d1026-581">*pSamples* \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="d1026-581">*pSamples*\[0\]</span></span> | <span data-ttu-id="d1026-582">Immagine interlacciata</span><span class="sxs-lookup"><span data-stu-id="d1026-582">Interlaced picture</span></span>             | <span data-ttu-id="d1026-583">*T* − 1</span><span class="sxs-lookup"><span data-stu-id="d1026-583">*T* −1</span></span>            |
| <span data-ttu-id="d1026-584">*pSamples* \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="d1026-584">*pSamples*\[1\]</span></span> | <span data-ttu-id="d1026-585">Immagine interlacciata</span><span class="sxs-lookup"><span data-stu-id="d1026-585">Interlaced picture</span></span>             | <span data-ttu-id="d1026-586">*T*</span><span class="sxs-lookup"><span data-stu-id="d1026-586">*T*</span></span>               |
| <span data-ttu-id="d1026-587">*pSamples* \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="d1026-587">*pSamples*\[2\]</span></span> | <span data-ttu-id="d1026-588">Immagine interlacciata (riferimento)</span><span class="sxs-lookup"><span data-stu-id="d1026-588">Interlaced picture (reference)</span></span> | <span data-ttu-id="d1026-589">*T* + 1</span><span class="sxs-lookup"><span data-stu-id="d1026-589">*T* +1</span></span>            |



 

## <a name="related-topics"></a><span data-ttu-id="d1026-590">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d1026-590">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1026-591">Accelerazione video DirectX 2,0</span><span class="sxs-lookup"><span data-stu-id="d1026-591">DirectX Video Acceleration 2.0</span></span>](directx-video-acceleration-2-0.md)
</dt> <dt>

[<span data-ttu-id="d1026-592">\_Esempio DXVA2 VideoProc</span><span class="sxs-lookup"><span data-stu-id="d1026-592">DXVA2\_VideoProc Sample</span></span>](dxva2-videoproc-sample.md)
</dt> </dl>

 

 
