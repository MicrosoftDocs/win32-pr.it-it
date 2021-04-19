---
description: In questo argomento viene descritto come creare una topologia per la riproduzione audio o video.
ms.assetid: 9c536c4e-fbf8-4c16-932f-e5863b7652fe
title: Creazione di topologie di riproduzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f6d34e9237278766ccb1ee174ba6c09bf953933
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305464"
---
# <a name="creating-playback-topologies"></a><span data-ttu-id="7a523-103">Creazione di topologie di riproduzione</span><span class="sxs-lookup"><span data-stu-id="7a523-103">Creating Playback Topologies</span></span>

<span data-ttu-id="7a523-104">In questo argomento viene descritto come creare una topologia per la riproduzione audio o video.</span><span class="sxs-lookup"><span data-stu-id="7a523-104">This topic describes how to create a topology for audio or video playback.</span></span> <span data-ttu-id="7a523-105">Per la riproduzione di base, è possibile creare una topologia parziale, in cui i nodi di origine sono connessi direttamente ai nodi di output.</span><span class="sxs-lookup"><span data-stu-id="7a523-105">For basic playback, you can create a partial topology, in which the source nodes are connected directly to the output nodes.</span></span> <span data-ttu-id="7a523-106">Non è necessario inserire nodi per le trasformazioni intermedie, ad esempio decodificatori o convertitori di colori.</span><span class="sxs-lookup"><span data-stu-id="7a523-106">You do not need to insert any nodes for the intermediate transforms, such as decoders or color converters.</span></span> <span data-ttu-id="7a523-107">La sessione multimediale utilizzerà il caricatore della topologia per risolvere la topologia e il caricatore della topologia inserirà le trasformazioni necessarie.</span><span class="sxs-lookup"><span data-stu-id="7a523-107">The Media Session will use the topology loader to resolve the topology, and the topology loader will insert the transforms that are required.</span></span>

-   [<span data-ttu-id="7a523-108">Creazione della topologia</span><span class="sxs-lookup"><span data-stu-id="7a523-108">Creating the Topology</span></span>](#creating-the-topology)
-   [<span data-ttu-id="7a523-109">Connessione di flussi a sink multimediali</span><span class="sxs-lookup"><span data-stu-id="7a523-109">Connecting Streams to Media Sinks</span></span>](#connecting-streams-to-media-sinks)
-   [<span data-ttu-id="7a523-110">Creazione del sink multimediale</span><span class="sxs-lookup"><span data-stu-id="7a523-110">Creating the Media Sink</span></span>](#creating-the-media-sink)
-   [<span data-ttu-id="7a523-111">Passaggi successivi</span><span class="sxs-lookup"><span data-stu-id="7a523-111">Next Steps</span></span>](#next-steps)
-   [<span data-ttu-id="7a523-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7a523-112">Related topics</span></span>](#related-topics)

## <a name="creating-the-topology"></a><span data-ttu-id="7a523-113">Creazione della topologia</span><span class="sxs-lookup"><span data-stu-id="7a523-113">Creating the Topology</span></span>

<span data-ttu-id="7a523-114">Ecco i passaggi generali per la creazione di una topologia di riproduzione parziale da un'origine multimediale:</span><span class="sxs-lookup"><span data-stu-id="7a523-114">Here are the overall steps for creating a partial playback topology from a media source:</span></span>

1.  <span data-ttu-id="7a523-115">Creare l'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="7a523-115">Create the media source.</span></span> <span data-ttu-id="7a523-116">Nella maggior parte dei casi, si userà il resolver di origine per creare l'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="7a523-116">In most cases, you will use the source resolver to create the media source.</span></span> <span data-ttu-id="7a523-117">Per ulteriori informazioni, vedere [resolver di origine](source-resolver.md).</span><span class="sxs-lookup"><span data-stu-id="7a523-117">For more information, see [Source Resolver](source-resolver.md).</span></span>
2.  <span data-ttu-id="7a523-118">Ottenere il descrittore di presentazione dell'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="7a523-118">Get the media source's presentation descriptor.</span></span>
3.  <span data-ttu-id="7a523-119">Creare una topologia vuota.</span><span class="sxs-lookup"><span data-stu-id="7a523-119">Create an empty topology.</span></span>
4.  <span data-ttu-id="7a523-120">Usare il descrittore della presentazione per enumerare i descrittori del flusso.</span><span class="sxs-lookup"><span data-stu-id="7a523-120">Use the presentation descriptor to enumerate the stream descriptors.</span></span> <span data-ttu-id="7a523-121">Per ogni descrittore di flusso:</span><span class="sxs-lookup"><span data-stu-id="7a523-121">For each stream descriptor:</span></span>
    1.  <span data-ttu-id="7a523-122">Ottenere il tipo di supporto principale del flusso, ad esempio audio o video.</span><span class="sxs-lookup"><span data-stu-id="7a523-122">Get the stream's major media type, such as audio or video.</span></span>
    2.  <span data-ttu-id="7a523-123">Controllare se il flusso è attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="7a523-123">Check if the stream is currently selected.</span></span> <span data-ttu-id="7a523-124">Facoltativamente, è possibile selezionare o deselezionare un flusso, in base al tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="7a523-124">(Optionally, you can select or deselect a stream, based on the media type.)</span></span>
    3.  <span data-ttu-id="7a523-125">Se il flusso è selezionato, creare un oggetto attivazione per il sink multimediale, in base al tipo di supporto del flusso.</span><span class="sxs-lookup"><span data-stu-id="7a523-125">If the stream is selected, create an activation object for the media sink, based on the stream's media type.</span></span>
    4.  <span data-ttu-id="7a523-126">Aggiungere un nodo di origine per il flusso e un nodo di output per il sink multimediale.</span><span class="sxs-lookup"><span data-stu-id="7a523-126">Add a source node for the stream and an output node for the media sink.</span></span>
    5.  <span data-ttu-id="7a523-127">Connettere il nodo di origine al nodo di output.</span><span class="sxs-lookup"><span data-stu-id="7a523-127">Connect the source node to the output node.</span></span>

<span data-ttu-id="7a523-128">Per semplificare il processo, il codice di esempio in questo argomento è organizzato in diverse funzioni.</span><span class="sxs-lookup"><span data-stu-id="7a523-128">To make this process easier to follow, the example code in this topic is organized into several functions.</span></span> <span data-ttu-id="7a523-129">La funzione di primo livello è denominata `CreatePlaybackTopology` .</span><span class="sxs-lookup"><span data-stu-id="7a523-129">The top-level function is named `CreatePlaybackTopology`.</span></span> <span data-ttu-id="7a523-130">Sono necessari tre parametri:</span><span class="sxs-lookup"><span data-stu-id="7a523-130">It takes three parameters:</span></span>

-   <span data-ttu-id="7a523-131">Puntatore a un'interfaccia [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) dell'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="7a523-131">A pointer to a [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) interface of the media source.</span></span>
-   <span data-ttu-id="7a523-132">Puntatore all'interfaccia [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) del descrittore di presentazione.</span><span class="sxs-lookup"><span data-stu-id="7a523-132">A pointer to the [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) interface of the presentation descriptor.</span></span> <span data-ttu-id="7a523-133">Ottenere questo puntatore chiamando [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span><span class="sxs-lookup"><span data-stu-id="7a523-133">Get this pointer by calling [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span></span> <span data-ttu-id="7a523-134">Per le origini con più presentazioni, i descrittori di presentazione per le presentazioni successive vengono recapitati nell'evento [MENewPresentation](menewpresentation.md) .</span><span class="sxs-lookup"><span data-stu-id="7a523-134">For sources with multiple presentations, the presentation descriptors for subsequent presentations are delivered in the [MENewPresentation](menewpresentation.md) event.</span></span>
-   <span data-ttu-id="7a523-135">Handle per una finestra dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7a523-135">A handle to an application window.</span></span> <span data-ttu-id="7a523-136">Se l'origine ha un flusso video, il video verrà visualizzato in questa finestra.</span><span class="sxs-lookup"><span data-stu-id="7a523-136">If the source has a video stream, the video will be displayed in this window.</span></span>

<span data-ttu-id="7a523-137">La funzione restituisce un puntatore a una topologia di riproduzione parziale nel parametro *ppTopology* .</span><span class="sxs-lookup"><span data-stu-id="7a523-137">The function returns a pointer to a partial playback topology in the *ppTopology* parameter.</span></span>


```C++
//  Create a playback topology from a media source.
HRESULT CreatePlaybackTopology(
    IMFMediaSource *pSource,          // Media source.
    IMFPresentationDescriptor *pPD,   // Presentation descriptor.
    HWND hVideoWnd,                   // Video window.
    IMFTopology **ppTopology)         // Receives a pointer to the topology.
{
    IMFTopology *pTopology = NULL;
    DWORD cSourceStreams = 0;

    // Create a new topology.
    HRESULT hr = MFCreateTopology(&pTopology);
    if (FAILED(hr))
    {
        goto done;
    }




    // Get the number of streams in the media source.
    hr = pPD->GetStreamDescriptorCount(&cSourceStreams);
    if (FAILED(hr))
    {
        goto done;
    }

    // For each stream, create the topology nodes and add them to the topology.
    for (DWORD i = 0; i < cSourceStreams; i++)
    {
        hr = AddBranchToPartialTopology(pTopology, pSource, pPD, i, hVideoWnd);
        if (FAILED(hr))
        {
            goto done;
        }
    }

    // Return the IMFTopology pointer to the caller.
    *ppTopology = pTopology;
    (*ppTopology)->AddRef();

done:
    SafeRelease(&pTopology);
    return hr;
}
```



<span data-ttu-id="7a523-138">Questa funzione esegue questa procedura:</span><span class="sxs-lookup"><span data-stu-id="7a523-138">This function performs the following steps:</span></span>

1.  <span data-ttu-id="7a523-139">Chiamare [**MFCreateTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology) per creare la topologia.</span><span class="sxs-lookup"><span data-stu-id="7a523-139">Call [**MFCreateTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology) to create the topology.</span></span> <span data-ttu-id="7a523-140">Inizialmente, la topologia non contiene alcun nodo.</span><span class="sxs-lookup"><span data-stu-id="7a523-140">Initially, the topology does not contain any nodes.</span></span>
2.  <span data-ttu-id="7a523-141">Chiamare [**IMFPresentationDescriptor:: GetStreamDescriptorCount**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorcount) per ottenere il numero di flussi nella presentazione.</span><span class="sxs-lookup"><span data-stu-id="7a523-141">Call [**IMFPresentationDescriptor::GetStreamDescriptorCount**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorcount) to get the number of streams in the presentation.</span></span>
3.  <span data-ttu-id="7a523-142">Per ogni flusso, chiamare la funzione definita dall'applicazione `AddBranchToPartialTopology` a un ramo nella topologia.</span><span class="sxs-lookup"><span data-stu-id="7a523-142">For each stream, call the application-defined `AddBranchToPartialTopology` function to a branch in the topology.</span></span> <span data-ttu-id="7a523-143">Questa funzione è illustrata nella sezione successiva.</span><span class="sxs-lookup"><span data-stu-id="7a523-143">This function is shown in the next section.</span></span>

## <a name="connecting-streams-to-media-sinks"></a><span data-ttu-id="7a523-144">Connessione di flussi a sink multimediali</span><span class="sxs-lookup"><span data-stu-id="7a523-144">Connecting Streams to Media Sinks</span></span>

<span data-ttu-id="7a523-145">Per ogni flusso selezionato, aggiungere un nodo di origine e un nodo di output, quindi connettere i due nodi.</span><span class="sxs-lookup"><span data-stu-id="7a523-145">For each selected stream, add a source node and an output node, then connect the two nodes.</span></span> <span data-ttu-id="7a523-146">Il nodo di origine rappresenta il flusso.</span><span class="sxs-lookup"><span data-stu-id="7a523-146">The source node represents the stream.</span></span> <span data-ttu-id="7a523-147">Il nodo di output rappresenta il [renderer video migliorato](enhanced-video-renderer.md) (EVR) o il [renderer di streaming audio](streaming-audio-renderer.md) (SAR).</span><span class="sxs-lookup"><span data-stu-id="7a523-147">The output node represents either the [Enhanced Video Renderer](enhanced-video-renderer.md) (EVR) or the [Streaming Audio Renderer](streaming-audio-renderer.md) (SAR).</span></span>

<span data-ttu-id="7a523-148">La `AddBranchToPartialTopology` funzione, mostrata nell'esempio successivo, accetta i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="7a523-148">The `AddBranchToPartialTopology` function, shown in the next example, takes the following parameters:</span></span>

-   <span data-ttu-id="7a523-149">Puntatore all'interfaccia [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) della topologia.</span><span class="sxs-lookup"><span data-stu-id="7a523-149">A pointer to the [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) interface of the topology.</span></span>
-   <span data-ttu-id="7a523-150">Puntatore all'interfaccia [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) dell'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="7a523-150">A pointer to the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) interface of the media source.</span></span>
-   <span data-ttu-id="7a523-151">Puntatore all'interfaccia [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) del descrittore di presentazione.</span><span class="sxs-lookup"><span data-stu-id="7a523-151">A pointer to the [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) interface of the presentation descriptor.</span></span>
-   <span data-ttu-id="7a523-152">Indice in base zero del flusso.</span><span class="sxs-lookup"><span data-stu-id="7a523-152">The zero-based index of the stream.</span></span>
-   <span data-ttu-id="7a523-153">Handle per la finestra del video.</span><span class="sxs-lookup"><span data-stu-id="7a523-153">A handle to the video window.</span></span> <span data-ttu-id="7a523-154">Questo handle viene usato solo per il flusso video.</span><span class="sxs-lookup"><span data-stu-id="7a523-154">This handle is used only for the video stream.</span></span>


```C++
//  Add a topology branch for one stream.
//
//  For each stream, this function does the following:
//
//    1. Creates a source node associated with the stream. 
//    2. Creates an output node for the renderer. 
//    3. Connects the two nodes.
//
//  The media session will add any decoders that are needed.

HRESULT AddBranchToPartialTopology(
    IMFTopology *pTopology,         // Topology.
    IMFMediaSource *pSource,        // Media source.
    IMFPresentationDescriptor *pPD, // Presentation descriptor.
    DWORD iStream,                  // Stream index.
    HWND hVideoWnd)                 // Window for video playback.
{
    IMFStreamDescriptor *pSD = NULL;
    IMFActivate         *pSinkActivate = NULL;
    IMFTopologyNode     *pSourceNode = NULL;
    IMFTopologyNode     *pOutputNode = NULL;

    BOOL fSelected = FALSE;

    HRESULT hr = pPD->GetStreamDescriptorByIndex(iStream, &fSelected, &pSD);
    if (FAILED(hr))
    {
        goto done;
    }

    if (fSelected)
    {
        // Create the media sink activation object.
        hr = CreateMediaSinkActivate(pSD, hVideoWnd, &pSinkActivate);
        if (FAILED(hr))
        {
            goto done;
        }

        // Add a source node for this stream.
        hr = AddSourceNode(pTopology, pSource, pPD, pSD, &pSourceNode);
        if (FAILED(hr))
        {
            goto done;
        }

        // Create the output node for the renderer.
        hr = AddOutputNode(pTopology, pSinkActivate, 0, &pOutputNode);
        if (FAILED(hr))
        {
            goto done;
        }

        // Connect the source node to the output node.
        hr = pSourceNode->ConnectOutput(0, pOutputNode, 0);
    }
    // else: If not selected, don't add the branch. 

done:
    SafeRelease(&pSD);
    SafeRelease(&pSinkActivate);
    SafeRelease(&pSourceNode);
    SafeRelease(&pOutputNode);
    return hr;
}
```



<span data-ttu-id="7a523-155">La funzione esegue le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="7a523-155">The function does the following:</span></span>

1.  <span data-ttu-id="7a523-156">Chiama [**IMFPresentationDescriptor:: GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) e passa l'indice del flusso.</span><span class="sxs-lookup"><span data-stu-id="7a523-156">Calls [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) and passes in the stream index.</span></span> <span data-ttu-id="7a523-157">Questo metodo restituisce un puntatore al descrittore del flusso per il flusso, insieme a un valore booleano che indica se il flusso è selezionato.</span><span class="sxs-lookup"><span data-stu-id="7a523-157">This method returns a pointer to the stream descriptor for that stream, along with a Boolean value indicating whether the stream is selected.</span></span>
2.  <span data-ttu-id="7a523-158">Se il flusso non è selezionato, la funzione viene chiusa e restituisce S \_ OK, perché non è necessario che l'applicazione crei un ramo della topologia per un flusso a meno che non sia selezionato.</span><span class="sxs-lookup"><span data-stu-id="7a523-158">If the stream is not selected, the function exits and returns S\_OK, because the application does not need to create a topology branch for a stream unless it is selected.</span></span>
3.  <span data-ttu-id="7a523-159">Se il flusso è selezionato, la funzione completa il ramo della topologia come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="7a523-159">If the stream is selected, the function completes the topology branch as follows:</span></span>
    1.  <span data-ttu-id="7a523-160">Crea un oggetto attivazione per il sink, chiamando la funzione CreateMediaSinkActivate definita dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7a523-160">Creates an activation object for the sink, by calling the application-defined CreateMediaSinkActivate function.</span></span> <span data-ttu-id="7a523-161">Questa funzione è illustrata nella sezione successiva.</span><span class="sxs-lookup"><span data-stu-id="7a523-161">This function is shown in the next section.</span></span>
    2.  <span data-ttu-id="7a523-162">Aggiunge un nodo di origine alla topologia.</span><span class="sxs-lookup"><span data-stu-id="7a523-162">Adds a source node to the topology.</span></span> <span data-ttu-id="7a523-163">Il codice per questo passaggio è illustrato nell'argomento [creazione di nodi di origine](creating-source-nodes.md).</span><span class="sxs-lookup"><span data-stu-id="7a523-163">Code for this step is shown in the topic [Creating Source Nodes](creating-source-nodes.md).</span></span>
    3.  <span data-ttu-id="7a523-164">Aggiunge un nodo di output alla topologia.</span><span class="sxs-lookup"><span data-stu-id="7a523-164">Adds an output node to the topology.</span></span> <span data-ttu-id="7a523-165">Il codice per questo passaggio è illustrato nell'argomento [creazione di nodi di output](creating-output-nodes.md).</span><span class="sxs-lookup"><span data-stu-id="7a523-165">Code for this step is shown in the topic [Creating Output Nodes](creating-output-nodes.md).</span></span>
    4.  <span data-ttu-id="7a523-166">Connette i due nodi chiamando [**IMFTopologyNode:: ConnectOutput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-connectoutput) nel nodo di origine.</span><span class="sxs-lookup"><span data-stu-id="7a523-166">Connects the two nodes by calling [**IMFTopologyNode::ConnectOutput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-connectoutput) on the source node.</span></span> <span data-ttu-id="7a523-167">Connettendo i nodi, l'applicazione indica che il nodo upstream deve recapitare i dati al nodo downstream.</span><span class="sxs-lookup"><span data-stu-id="7a523-167">By connecting the nodes, the application indicates that the upstream node should deliver data to the downstream node.</span></span> <span data-ttu-id="7a523-168">Un nodo di origine ha un output e un nodo di output ha un input, quindi entrambi gli indici del flusso sono pari A zero.</span><span class="sxs-lookup"><span data-stu-id="7a523-168">A source node has one output, and an output node has one input, so both stream indexes are zero.</span></span>

<span data-ttu-id="7a523-169">Le applicazioni più avanzate possono selezionare o deselezionare i flussi, anziché usare la configurazione predefinita dell'origine.</span><span class="sxs-lookup"><span data-stu-id="7a523-169">More advanced applications can select or deselect streams, instead of using the source's default configuration.</span></span> <span data-ttu-id="7a523-170">Un'origine potrebbe avere più flussi ed è possibile che sia selezionata per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="7a523-170">A source could have multiple streams, and any of them might be selected by default.</span></span> <span data-ttu-id="7a523-171">Il descrittore di presentazione dell'origine multimediale dispone di un set predefinito di selezioni di flusso.</span><span class="sxs-lookup"><span data-stu-id="7a523-171">The media source's presentation descriptor has a default set of stream selections.</span></span> <span data-ttu-id="7a523-172">In un semplice file video con un solo flusso audio e un flusso video, l'origine multimediale in genere seleziona entrambi i flussi per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="7a523-172">In a simple video file with a single audio stream and video stream, the media source will usually select both streams by default.</span></span> <span data-ttu-id="7a523-173">Tuttavia, un file potrebbe avere più flussi audio per lingue diverse o più flussi video codificati a velocità in bit diverse.</span><span class="sxs-lookup"><span data-stu-id="7a523-173">However, a file might have multiple audio streams for different languages, or multiple video streams encoded at different bit rates.</span></span> <span data-ttu-id="7a523-174">In tal caso, alcuni flussi verranno deselezionati per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="7a523-174">In that case, some of the streams will be unselected by default.</span></span> <span data-ttu-id="7a523-175">L'applicazione può modificare la selezione chiamando [**IMFPresentationDescriptor:: SelectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) e [**IMFPresentationDescriptor::D eselectstream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream) sul descrittore della presentazione.</span><span class="sxs-lookup"><span data-stu-id="7a523-175">The application can change the selection by calling [**IMFPresentationDescriptor::SelectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) and [**IMFPresentationDescriptor::DeselectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream) on the presentation descriptor.</span></span>

## <a name="creating-the-media-sink"></a><span data-ttu-id="7a523-176">Creazione del sink multimediale</span><span class="sxs-lookup"><span data-stu-id="7a523-176">Creating the Media Sink</span></span>

<span data-ttu-id="7a523-177">La funzione Next crea un oggetto Activation per il sink del supporto EVR o SAR.</span><span class="sxs-lookup"><span data-stu-id="7a523-177">The next function creates an activation object for the EVR or SAR media sink.</span></span>


```C++
//  Create an activation object for a renderer, based on the stream media type.

HRESULT CreateMediaSinkActivate(
    IMFStreamDescriptor *pSourceSD,     // Pointer to the stream descriptor.
    HWND hVideoWindow,                  // Handle to the video clipping window.
    IMFActivate **ppActivate
)
{
    IMFMediaTypeHandler *pHandler = NULL;
    IMFActivate *pActivate = NULL;

    // Get the media type handler for the stream.
    HRESULT hr = pSourceSD->GetMediaTypeHandler(&pHandler);
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the major media type.
    GUID guidMajorType;
    hr = pHandler->GetMajorType(&guidMajorType);
    if (FAILED(hr))
    {
        goto done;
    }
 
    // Create an IMFActivate object for the renderer, based on the media type.
    if (MFMediaType_Audio == guidMajorType)
    {
        // Create the audio renderer.
        hr = MFCreateAudioRendererActivate(&pActivate);
    }
    else if (MFMediaType_Video == guidMajorType)
    {
        // Create the video renderer.
        hr = MFCreateVideoRendererActivate(hVideoWindow, &pActivate);
    }
    else
    {
        // Unknown stream type. 
        hr = E_FAIL;
        // Optionally, you could deselect this stream instead of failing.
    }
    if (FAILED(hr))
    {
        goto done;
    }
 
    // Return IMFActivate pointer to caller.
    *ppActivate = pActivate;
    (*ppActivate)->AddRef();

done:
    SafeRelease(&pHandler);
    SafeRelease(&pActivate);
    return hr;
}
```



<span data-ttu-id="7a523-178">Questa funzione esegue questa procedura:</span><span class="sxs-lookup"><span data-stu-id="7a523-178">This function performs the following steps:</span></span>

1.  <span data-ttu-id="7a523-179">Chiama [**IMFStreamDescriptor:: GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) sul descrittore del flusso.</span><span class="sxs-lookup"><span data-stu-id="7a523-179">Calls [**IMFStreamDescriptor::GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) on the stream descriptor.</span></span> <span data-ttu-id="7a523-180">Questo metodo restituisce un puntatore all'interfaccia [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) .</span><span class="sxs-lookup"><span data-stu-id="7a523-180">This method returns an [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) interface pointer.</span></span>

2.  <span data-ttu-id="7a523-181">Chiama [**IMFMediaTypeHandler:: GetMajorType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmajortype).</span><span class="sxs-lookup"><span data-stu-id="7a523-181">Calls [**IMFMediaTypeHandler::GetMajorType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmajortype).</span></span> <span data-ttu-id="7a523-182">Questo metodo restituisce il GUID del tipo principale per il flusso.</span><span class="sxs-lookup"><span data-stu-id="7a523-182">This method returns the major type GUID for the stream.</span></span>

3.  <span data-ttu-id="7a523-183">Se il tipo di flusso è audio, la funzione chiama [**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate) per creare l'oggetto attivazione renderer audio.</span><span class="sxs-lookup"><span data-stu-id="7a523-183">If the stream type is audio, the function calls [**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate) to create the audio renderer activation object.</span></span> <span data-ttu-id="7a523-184">Se il tipo di flusso è video, la funzione chiama [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) per creare l'oggetto attivazione del renderer video.</span><span class="sxs-lookup"><span data-stu-id="7a523-184">If the stream type is video, the function calls [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) to create the video renderer activation object.</span></span> <span data-ttu-id="7a523-185">Entrambe queste funzioni restituiscono un puntatore all'interfaccia [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .</span><span class="sxs-lookup"><span data-stu-id="7a523-185">Both of these functions return a pointer to the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface.</span></span> <span data-ttu-id="7a523-186">Questo puntatore viene usato per inizializzare il nodo di output per il sink, come illustrato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="7a523-186">This pointer is used to initialize the output node for the sink, as shown previously.</span></span>

<span data-ttu-id="7a523-187">Per qualsiasi altro tipo di flusso, in questo esempio viene restituito un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="7a523-187">For any other stream type, this example returns an error code.</span></span> <span data-ttu-id="7a523-188">In alternativa, è possibile deselezionare semplicemente il flusso.</span><span class="sxs-lookup"><span data-stu-id="7a523-188">Alternatively, you could simply deselect the stream.</span></span>

## <a name="next-steps"></a><span data-ttu-id="7a523-189">Passaggi successivi</span><span class="sxs-lookup"><span data-stu-id="7a523-189">Next Steps</span></span>

<span data-ttu-id="7a523-190">Per riprodurre un file multimediale alla volta, accodare la topologia nella sessione multimediale chiamando [**IMFMediaSession:: Setopologia**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span><span class="sxs-lookup"><span data-stu-id="7a523-190">To play one media file at a time, queue the topology on the Media Session by calling [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span></span> <span data-ttu-id="7a523-191">La sessione multimediale utilizzerà il caricatore della topologia per risolvere la topologia.</span><span class="sxs-lookup"><span data-stu-id="7a523-191">The Media Session will use the topology loader to resolve the topology.</span></span> <span data-ttu-id="7a523-192">Per un esempio completo, vedere [come riprodurre file multimediali con Media Foundation](how-to-play-unprotected-media-files.md).</span><span class="sxs-lookup"><span data-stu-id="7a523-192">For a complete example, see [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7a523-193">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7a523-193">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a523-194">Come riprodurre file multimediali non protetti</span><span class="sxs-lookup"><span data-stu-id="7a523-194">How to Play Unprotected Media Files</span></span>](how-to-play-unprotected-media-files.md)
</dt> <dt>

[<span data-ttu-id="7a523-195">Sessione multimediale</span><span class="sxs-lookup"><span data-stu-id="7a523-195">Media Session</span></span>](media-session.md)
</dt> <dt>

[<span data-ttu-id="7a523-196">Topologie</span><span class="sxs-lookup"><span data-stu-id="7a523-196">Topologies</span></span>](topologies.md)
</dt> </dl>

 

 



