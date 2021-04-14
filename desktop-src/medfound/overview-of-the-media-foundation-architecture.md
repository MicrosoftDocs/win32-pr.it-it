---
description: In questo argomento viene descritta la progettazione generale di Microsoft Media Foundation. Per informazioni sull'utilizzo di Media Foundation per attività di programmazione specifiche, vedere Guida alla programmazione di Media Foundation.
ms.assetid: DEA2B19A-CF15-4BF4-84C3-9A6417C942E2
title: Panoramica dell'architettura Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0944eae1a74c1a5ba3dda8d94b69088128237f1
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104551941"
---
# <a name="overview-of-the-media-foundation-architecture"></a><span data-ttu-id="33773-104">Panoramica dell'architettura Media Foundation</span><span class="sxs-lookup"><span data-stu-id="33773-104">Overview of the Media Foundation Architecture</span></span>

<span data-ttu-id="33773-105">In questo argomento viene descritta la progettazione generale di Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="33773-105">This topic describes the general design of Microsoft Media Foundation.</span></span> <span data-ttu-id="33773-106">Per informazioni sull'utilizzo di Media Foundation per attività di programmazione specifiche, vedere [Guida alla programmazione di Media Foundation](media-foundation-programming-guide.md).</span><span class="sxs-lookup"><span data-stu-id="33773-106">For information about using Media Foundation for specific programming tasks, see [Media Foundation Programming Guide](media-foundation-programming-guide.md).</span></span>

<span data-ttu-id="33773-107">Nel diagramma seguente viene illustrata una visualizzazione di alto livello dell'architettura Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="33773-107">The following diagram shows a high-level view of the Media Foundation architecture.</span></span>

![diagramma che mostra una visualizzazione di alto livello dell'architettura di Media Foundation.](images/mfarch01.png)

<span data-ttu-id="33773-109">Media Foundation fornisce due modelli di programmazione distinti.</span><span class="sxs-lookup"><span data-stu-id="33773-109">Media Foundation provides two distinct programming models.</span></span> <span data-ttu-id="33773-110">Il primo modello, visualizzato sul lato sinistro del diagramma, usa una pipeline end-to-end per i dati multimediali.</span><span class="sxs-lookup"><span data-stu-id="33773-110">The first model, shown on the left side of the diagram, uses an end-to-end pipeline for media data.</span></span> <span data-ttu-id="33773-111">L'applicazione Inizializza la pipeline, ad esempio specificando l'URL di un file da riprodurre, quindi chiama i metodi per controllare il flusso.</span><span class="sxs-lookup"><span data-stu-id="33773-111">The application initializes the pipeline—for example, by providing the URL of a file to play—and then calls methods to control streaming.</span></span> <span data-ttu-id="33773-112">Nel secondo modello, visualizzato sul lato destro del diagramma, l'applicazione estrae i dati da un'origine o li inserisce in una destinazione (o entrambi).</span><span class="sxs-lookup"><span data-stu-id="33773-112">In the second model, shown on the right side of the diagram, the application either pulls data from a source, or pushes it to a destination (or both).</span></span> <span data-ttu-id="33773-113">Questo modello è particolarmente utile se è necessario elaborare i dati, perché l'applicazione ha accesso diretto al flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="33773-113">This model is particularly useful if you need to process the data, because the application has direct access to the data stream.</span></span>

### <a name="primitives-and-platform"></a><span data-ttu-id="33773-114">Primitive e piattaforma</span><span class="sxs-lookup"><span data-stu-id="33773-114">Primitives and Platform</span></span>

<span data-ttu-id="33773-115">A partire dalla fine del diagramma, le *primitive* sono oggetti helper usati nell'API Media Foundation:</span><span class="sxs-lookup"><span data-stu-id="33773-115">Starting from the bottom of the diagram, the *primitives* are helper objects used throughout the Media Foundation API:</span></span>

-   <span data-ttu-id="33773-116">[Gli attributi](attributes-and-properties.md) sono un modo generico per archiviare le informazioni all'interno di un oggetto, come un elenco di coppie chiave/valore.</span><span class="sxs-lookup"><span data-stu-id="33773-116">[Attributes](attributes-and-properties.md) are a generic way to store information inside an object, as a list of key/value pairs.</span></span>
-   <span data-ttu-id="33773-117">I [tipi di supporto](media-types.md) descrivono il formato di un flusso di dati multimediali.</span><span class="sxs-lookup"><span data-stu-id="33773-117">[Media Types](media-types.md) describe the format of a media data stream.</span></span>
-   <span data-ttu-id="33773-118">I [buffer multimediali](media-buffers.md) contengono blocchi di dati multimediali, ad esempio fotogrammi video ed esempi audio, e vengono usati per il trasporto di dati tra oggetti.</span><span class="sxs-lookup"><span data-stu-id="33773-118">[Media Buffers](media-buffers.md) hold chunks of media data, such as video frames and audio samples, and are used to transport data between objects.</span></span>
-   <span data-ttu-id="33773-119">Gli [esempi di supporti](media-samples.md) sono contenitori per i buffer multimediali.</span><span class="sxs-lookup"><span data-stu-id="33773-119">[Media Samples](media-samples.md) are containers for media buffers.</span></span> <span data-ttu-id="33773-120">Contengono anche i metadati relativi ai buffer, ad esempio i timestamp.</span><span class="sxs-lookup"><span data-stu-id="33773-120">They also contain metadata about the buffers, such as time stamps.</span></span>

<span data-ttu-id="33773-121">Le [API della piattaforma Media Foundation](media-foundation-platform-apis.md) forniscono alcune funzionalità di base usate dalla pipeline Media Foundation, ad esempio callback asincroni e code di lavoro.</span><span class="sxs-lookup"><span data-stu-id="33773-121">The [Media Foundation Platform APIs](media-foundation-platform-apis.md) provide some core functionality that is used by the Media Foundation pipeline, such as asynchronous callbacks and work queues.</span></span> <span data-ttu-id="33773-122">Alcune applicazioni potrebbero dover chiamare direttamente queste API; Inoltre, sarà necessario se si implementa un'origine, una trasformazione o un sink personalizzato per Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="33773-122">Certain applications might need to call these APIs directly; also, you will need them if you implement a custom source, transform, or sink for Media Foundation.</span></span>

### <a name="media-pipeline"></a><span data-ttu-id="33773-123">Pipeline multimediale</span><span class="sxs-lookup"><span data-stu-id="33773-123">Media Pipeline</span></span>

<span data-ttu-id="33773-124">La pipeline multimediale contiene tre tipi di oggetto che generano o elaborano i dati multimediali:</span><span class="sxs-lookup"><span data-stu-id="33773-124">The media pipeline contains three types of object that generate or process media data:</span></span>

-   <span data-ttu-id="33773-125">Le [origini supporti](media-sources.md) introducono dati nella pipeline.</span><span class="sxs-lookup"><span data-stu-id="33773-125">[Media Sources](media-sources.md) introduce data into the pipeline.</span></span> <span data-ttu-id="33773-126">Un'origine multimediale può ottenere dati da un file locale, ad esempio un file video; da un flusso di rete; o da un dispositivo di acquisizione hardware.</span><span class="sxs-lookup"><span data-stu-id="33773-126">A media source might get data from a local file, such as a video file; from a network stream; or from a hardware capture device.</span></span>
-   <span data-ttu-id="33773-127">[Media Foundation Transforms](media-foundation-transforms.md) (MFTS) elabora i dati da un flusso.</span><span class="sxs-lookup"><span data-stu-id="33773-127">[Media Foundation Transforms](media-foundation-transforms.md) (MFTs) process data from a stream.</span></span> <span data-ttu-id="33773-128">Codificatori e decodificatori vengono implementati come MFTs.</span><span class="sxs-lookup"><span data-stu-id="33773-128">Encoders and decoders are implemented as MFTs.</span></span>
-   <span data-ttu-id="33773-129">I [sink dei supporti](media-sinks.md) utilizzano i dati; ad esempio, visualizzando il video sullo schermo, riproducendo audio o scrivendo i dati in un file multimediale.</span><span class="sxs-lookup"><span data-stu-id="33773-129">[Media Sinks](media-sinks.md) consume the data; for example, by showing video on the display, playing audio, or writing the data to a media file.</span></span>

<span data-ttu-id="33773-130">Le terze parti possono implementare origini, sink e MFTs personalizzati; ad esempio, per supportare nuovi formati di file multimediali.</span><span class="sxs-lookup"><span data-stu-id="33773-130">Third parties can implement their own custom sources, sinks, and MFTs; for example, to support new media file formats.</span></span>

<span data-ttu-id="33773-131">La [sessione multimediale](media-session.md) controlla il flusso di dati attraverso la pipeline e gestisce attività quali il controllo della qualità, la sincronizzazione audio/video e la risposta alle modifiche del formato.</span><span class="sxs-lookup"><span data-stu-id="33773-131">The [Media Session](media-session.md) controls the flow of data through the pipeline, and handles tasks such as quality control, audio/video synchronization, and responding to format changes.</span></span>

### <a name="source-reader-and-sink-writer"></a><span data-ttu-id="33773-132">Reader di origine e writer di sink</span><span class="sxs-lookup"><span data-stu-id="33773-132">Source Reader and Sink Writer</span></span>

<span data-ttu-id="33773-133">Il [lettore di origine](source-reader.md) e il [writer di sink](sink-writer.md) forniscono una modalità alternativa per usare i componenti di base Media Foundation (origini supporti, trasformazioni e sink multimediali).</span><span class="sxs-lookup"><span data-stu-id="33773-133">The [Source Reader](source-reader.md) and [Sink Writer](sink-writer.md) provide an alternative way to use the basic Media Foundation components (media sources, transforms, and media sinks).</span></span> <span data-ttu-id="33773-134">Il lettore di origine ospita un'origine multimediale e zero o più decodificatori, mentre il writer del sink ospita un sink multimediale e zero o più codificatori.</span><span class="sxs-lookup"><span data-stu-id="33773-134">The source reader hosts a media source and zero or more decoders, while the sink writer hosts a media sink and zero or more encoders.</span></span> <span data-ttu-id="33773-135">È possibile usare il lettore di origine per ottenere dati compressi o non compressi da un'origine multimediale e usare il writer di sink per codificare i dati e inviare i dati a un sink multimediale.</span><span class="sxs-lookup"><span data-stu-id="33773-135">You can use the source reader to get compressed or uncompressed data from a media source, and use the sink writer to encode data and send the data to a media sink.</span></span>

> [!Note]  
> <span data-ttu-id="33773-136">Il lettore di origine e il writer di sink sono disponibili in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="33773-136">The source reader and sink writer are available in Windows 7.</span></span>

 

<span data-ttu-id="33773-137">Questo modello di programmazione fornisce all'applicazione un maggiore controllo sul flusso di dati e fornisce anche l'accesso diretto all'applicazione ai dati dall'origine.</span><span class="sxs-lookup"><span data-stu-id="33773-137">This programming model gives the application more control over the flow of data, and also gives the application direct access to the data from the source.</span></span>

## <a name="related-topics"></a><span data-ttu-id="33773-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="33773-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33773-139">Media Foundation: concetti essenziali</span><span class="sxs-lookup"><span data-stu-id="33773-139">Media Foundation: Essential Concepts</span></span>](media-foundation-programming--essential-concepts.md)
</dt> <dt>

[<span data-ttu-id="33773-140">Architettura di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="33773-140">Media Foundation Architecture</span></span>](media-foundation-architecture.md)
</dt> </dl>

 

 



