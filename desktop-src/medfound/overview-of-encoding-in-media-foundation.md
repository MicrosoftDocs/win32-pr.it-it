---
description: Questo argomento è una panoramica delle API di codifica dei file disponibili in Microsoft Media Foundation.
ms.assetid: 69dbef63-e272-4ad2-8d04-ae9366f79b33
title: Cenni preliminari sulla codifica in Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81882bd6da43f4040614347b662d988844c7b7a6
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104563668"
---
# <a name="overview-of-encoding-in-media-foundation"></a><span data-ttu-id="2b4ca-103">Cenni preliminari sulla codifica in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2b4ca-103">Overview of Encoding in Media Foundation</span></span>

<span data-ttu-id="2b4ca-104">Questo argomento è una panoramica delle API di codifica dei file disponibili in Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="2b4ca-104">This topic is an overview of the file encoding APIs provided in Microsoft Media Foundation.</span></span>

## <a name="terminology"></a><span data-ttu-id="2b4ca-105">Terminologia</span><span class="sxs-lookup"><span data-stu-id="2b4ca-105">Terminology</span></span>

<span data-ttu-id="2b4ca-106">La *codifica* è un termine generale che copre diversi processi distinti:</span><span class="sxs-lookup"><span data-stu-id="2b4ca-106">*Encoding* is a general term that covers several distinct processes:</span></span>

1.  <span data-ttu-id="2b4ca-107">Codifica di un flusso audio o video in formati compressi.</span><span class="sxs-lookup"><span data-stu-id="2b4ca-107">Encoding an audio or video stream into a compressed formats.</span></span> <span data-ttu-id="2b4ca-108">Ad esempio, la codifica di un flusso video nel video H. 264.</span><span class="sxs-lookup"><span data-stu-id="2b4ca-108">For example, encoding a video stream to H.264 video.</span></span>
2.  <span data-ttu-id="2b4ca-109">Multiplexing ("muxing") di uno o più flussi in un flusso a byte singolo.</span><span class="sxs-lookup"><span data-stu-id="2b4ca-109">Multiplexing ("muxing") one or more streams into a single byte stream.</span></span> <span data-ttu-id="2b4ca-110">In genere, i flussi in ingresso vengono codificati per primi.</span><span class="sxs-lookup"><span data-stu-id="2b4ca-110">Typically, the incoming streams are encoded first.</span></span> <span data-ttu-id="2b4ca-111">Questo passaggio può comportare il packetizing dei flussi codificati.</span><span class="sxs-lookup"><span data-stu-id="2b4ca-111">This step might involve packetizing the encoded streams.</span></span>
3.  <span data-ttu-id="2b4ca-112">Scrittura di un flusso di byte multiplex in un file, ad esempio un file MP4 o Advanced Systems Format (ASF).</span><span class="sxs-lookup"><span data-stu-id="2b4ca-112">Writing a multiplexed byte stream to a file, such as an MP4 or Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="2b4ca-113">In alternativa, il flusso multiplex può essere inviato in rete.</span><span class="sxs-lookup"><span data-stu-id="2b4ca-113">Alternatively, the multiplexed stream can be sent over the network.</span></span>

<span data-ttu-id="2b4ca-114">Il diagramma seguente illustra questi tre processi:</span><span class="sxs-lookup"><span data-stu-id="2b4ca-114">The following diagram shows these three processes:</span></span>

![diagramma che illustra i processi di codifica e multiplex](images/encoding03.png)

<span data-ttu-id="2b4ca-116">Le varianti di questo processo includono la transcodifica e remuxing:</span><span class="sxs-lookup"><span data-stu-id="2b4ca-116">Variations of this process include transcoding and remuxing:</span></span>

-   <span data-ttu-id="2b4ca-117">La *transcodifica* significa la decodifica di un file esistente, la ricodifica dei flussi e il nuovo multiplexing dei flussi codificati.</span><span class="sxs-lookup"><span data-stu-id="2b4ca-117">*Transcoding* means decoding an existing file, re-encoding the streams, and re-multiplexing the encoded streams.</span></span> <span data-ttu-id="2b4ca-118">La transcodifica può essere eseguita per convertire un file da un tipo di codifica a un altro; ad esempio, per convertire il video H. 264 in Windows Media Video (WMV).</span><span class="sxs-lookup"><span data-stu-id="2b4ca-118">Transcoding might be done to convert a file from one encoding type to another; for example, to convert H.264 video to Windows Media Video (WMV).</span></span> <span data-ttu-id="2b4ca-119">Questa operazione può essere eseguita anche per modificare la velocità in bit codificata; dimensioni del fotogramma video; frequenza dei fotogrammi; o altri parametri di formato.</span><span class="sxs-lookup"><span data-stu-id="2b4ca-119">It can also be done to change the encoded bit rate; the video frame size; the frame rate; or other format parameters.</span></span>
-   <span data-ttu-id="2b4ca-120">Il *rimultiplexing* o *remuxing* indica il demultiplexing di un file e il nuovo multiplexing dei flussi, senza passaggio di decodifica/codifica.</span><span class="sxs-lookup"><span data-stu-id="2b4ca-120">*Remultiplexing* or *remuxing* means demultiplexing a file and re-multiplexing the streams, with no decode/encode step.</span></span> <span data-ttu-id="2b4ca-121">Questa operazione può essere eseguita per modificare il modo in cui i pacchetti audio/video vengono multiplexati, per rimuovere un flusso o per combinare flussi da due file di origine diversi.</span><span class="sxs-lookup"><span data-stu-id="2b4ca-121">This might be done to change how the audio/video packets are multiplexed, to remove a stream, or to combine streams from two different source files.</span></span>
-   <span data-ttu-id="2b4ca-122">*Transrating* è un caso speciale di transcodifica, in cui la velocità in bit viene modificata senza modificare il tipo di compressione.</span><span class="sxs-lookup"><span data-stu-id="2b4ca-122">*Transrating* is a special case of transcoding, where the bit-rate is changed without changing the compression type.</span></span> <span data-ttu-id="2b4ca-123">Ad esempio, è possibile convertire un file a velocità elevata a una velocità in bit inferiore.</span><span class="sxs-lookup"><span data-stu-id="2b4ca-123">For example, you might convert a high-bit-rate file to a lower bit-rate.</span></span> <span data-ttu-id="2b4ca-124">Uno scenario tipico in cui è possibile usare la transclassificazione è quando si sincronizza il contenuto multimediale da un PC a un dispositivo portatile.</span><span class="sxs-lookup"><span data-stu-id="2b4ca-124">A typical scenario in which transrating might be used is when synchronizing media content from a PC to a portable device.</span></span> <span data-ttu-id="2b4ca-125">Se il dispositivo portatile non supporta una velocità in bit elevata, è possibile che il file venga rivalutato prima di essere copiato nel dispositivo portatile.</span><span class="sxs-lookup"><span data-stu-id="2b4ca-125">If the portable device does not support a high bit rate, the file might be transrated before it is copied to the portable device.</span></span>

<span data-ttu-id="2b4ca-126">Il diagramma di blocco seguente illustra il processo di transcodifica.</span><span class="sxs-lookup"><span data-stu-id="2b4ca-126">The following block diagram shows the transcoding process.</span></span>

![diagramma che illustra il processo di transcodifica](images/encoding05.png)

<span data-ttu-id="2b4ca-128">Il diagramma di blocco seguente illustra il processo remuxing.</span><span class="sxs-lookup"><span data-stu-id="2b4ca-128">The following block diagram shows the remuxing process.</span></span>

![diagramma che mostra il processo remuxing](images/encoding06.png)

<span data-ttu-id="2b4ca-130">Questa documentazione usa talvolta la *codifica* dei termini per includere sia la transcodifica che remuxing.</span><span class="sxs-lookup"><span data-stu-id="2b4ca-130">This documentation sometimes uses the term *encoding* to include both transcoding and remuxing.</span></span> <span data-ttu-id="2b4ca-131">Quando è importante distinguere tra di essi, la documentazione nota la differenza.</span><span class="sxs-lookup"><span data-stu-id="2b4ca-131">When it is important to distinguish between them, the documentation will note the difference.</span></span>

<span data-ttu-id="2b4ca-132">Vedere anche: [Media Foundation: concetti essenziali](media-foundation-programming--essential-concepts.md).</span><span class="sxs-lookup"><span data-stu-id="2b4ca-132">See also: [Media Foundation: Essential Concepts](media-foundation-programming--essential-concepts.md).</span></span>

## <a name="media-foundation-encoding-architecture"></a><span data-ttu-id="2b4ca-133">Architettura di codifica Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2b4ca-133">Media Foundation Encoding Architecture</span></span>

<span data-ttu-id="2b4ca-134">Al livello più basso dell'architettura Media Foundation, per la codifica vengono usati i tipi di componenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="2b4ca-134">At the lowest layer of the Media Foundation architecture, the following types of component are used for encoding:</span></span>

-   <span data-ttu-id="2b4ca-135">Per la transcodifica, le [origini multimediali](media-sources.md) vengono usate per demultiplexare il file di origine.</span><span class="sxs-lookup"><span data-stu-id="2b4ca-135">For transcoding, [Media Sources](media-sources.md) are used to demultiplex the source file.</span></span>
-   <span data-ttu-id="2b4ca-136">Per il processo di codifica, [Media Foundation le trasformazioni](media-foundation-transforms.md) vengono usate per decodificare e codificare i flussi.</span><span class="sxs-lookup"><span data-stu-id="2b4ca-136">For the encoding process, [Media Foundation Transforms](media-foundation-transforms.md) are used to decode and encode streams.</span></span>
-   <span data-ttu-id="2b4ca-137">Per il processo di multiplexing, i [sink di supporto](media-sinks.md) vengono usati per eseguire il multiplexing dei flussi e scrivere il flusso multiplexato in un file o in una rete.</span><span class="sxs-lookup"><span data-stu-id="2b4ca-137">For the multiplexing process, [Media Sinks](media-sinks.md) are used to multiplex the streams and write the multiplexed stream to a file or network.</span></span>

<span data-ttu-id="2b4ca-138">Il diagramma seguente illustra il flusso di dati tra questi componenti in uno scenario di transcodifica:</span><span class="sxs-lookup"><span data-stu-id="2b4ca-138">The following diagram shows the data flow between these components in a transcoding scenario:</span></span>

![diagramma che illustra i componenti utilizzati per la transcodifica](images/encoding04.png)

<span data-ttu-id="2b4ca-140">La maggior parte delle applicazioni non utilizzerà direttamente questi componenti.</span><span class="sxs-lookup"><span data-stu-id="2b4ca-140">Most applications will not use these components directly.</span></span> <span data-ttu-id="2b4ca-141">Al contrario, un'applicazione userà API di livello superiore che gestiscono questi componenti di livello inferiore.</span><span class="sxs-lookup"><span data-stu-id="2b4ca-141">Instead, an application will use higher-level APIs that manage these lower-level components.</span></span> <span data-ttu-id="2b4ca-142">Media Foundation fornisce due API di livello superiore per la codifica:</span><span class="sxs-lookup"><span data-stu-id="2b4ca-142">Media Foundation provides two higher-level APIs for encoding:</span></span>

<dl> <dt>

<span data-ttu-id="2b4ca-143"><span id="Media_Session"></span><span id="media_session"></span><span id="MEDIA_SESSION"></span>[Sessione multimediale](media-session.md)</span><span class="sxs-lookup"><span data-stu-id="2b4ca-143"><span id="Media_Session"></span><span id="media_session"></span><span id="MEDIA_SESSION"></span>[Media Session](media-session.md)</span></span>
</dt> <dd>

<span data-ttu-id="2b4ca-144">La sessione multimediale fornisce una pipeline end-to-end che sposta i dati dall'origine multimediale, tramite i codec e infine al sink multimediale.</span><span class="sxs-lookup"><span data-stu-id="2b4ca-144">The Media Session provides an end-to-end pipeline that moves data from the media source, through the codecs, and finally to the media sink.</span></span> <span data-ttu-id="2b4ca-145">L'applicazione controlla la sessione multimediale e riceve gli eventi di stato dalla sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="2b4ca-145">The application controls the Media Session and receives status events from the Media Session.</span></span>

</dd> <dt>

<span data-ttu-id="2b4ca-146"><span id="Source_Reader_plus_Sink_Writer"></span><span id="source_reader_plus_sink_writer"></span><span id="SOURCE_READER_PLUS_SINK_WRITER"></span>[Reader di origine](source-reader.md) e [writer di sink](sink-writer.md)</span><span class="sxs-lookup"><span data-stu-id="2b4ca-146"><span id="Source_Reader_plus_Sink_Writer"></span><span id="source_reader_plus_sink_writer"></span><span id="SOURCE_READER_PLUS_SINK_WRITER"></span>[Source Reader](source-reader.md) plus [Sink Writer](sink-writer.md)</span></span>
</dt> <dd>

<span data-ttu-id="2b4ca-147">Il lettore di origine esegue il wrapping dell'origine multimediale e, facoltativamente, dei decodificatori.</span><span class="sxs-lookup"><span data-stu-id="2b4ca-147">The Source Reader wraps the media source and optionally the decoders.</span></span> <span data-ttu-id="2b4ca-148">Fornisce esempi codificati o decodificati nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2b4ca-148">It delivers either encoded or decoded samples the application.</span></span> <span data-ttu-id="2b4ca-149">Il writer di sink esegue il wrapping del sink multimediale e, facoltativamente, dei codificatori.</span><span class="sxs-lookup"><span data-stu-id="2b4ca-149">The Sink Writer wraps the media sink and optionally the encoders.</span></span> <span data-ttu-id="2b4ca-150">L'applicazione passa gli esempi al writer del sink.</span><span class="sxs-lookup"><span data-stu-id="2b4ca-150">The application passes samples to the Sink Writer.</span></span>

</dd> </dl>

<span data-ttu-id="2b4ca-151">Il diagramma seguente illustra la sessione multimediale:</span><span class="sxs-lookup"><span data-stu-id="2b4ca-151">The following diagram shows the Media Session:</span></span>

![diagramma che illustra il modo in cui la sessione multimediale esegue la transcodifica](images/encoding01.png)

<span data-ttu-id="2b4ca-153">L' [API transcode](transcode-api.md) (la casella ombreggiata blu) è un set di API introdotte in Windows 7, che semplificano la configurazione della sessione multimediale per la codifica.</span><span class="sxs-lookup"><span data-stu-id="2b4ca-153">The [Transcode API](transcode-api.md) (the blue shaded box) is a set of APIs introduced in Windows 7, which make it easier to configure the Media Session for encoding.</span></span>

<span data-ttu-id="2b4ca-154">Il diagramma seguente mostra l'Reader di origine e il writer del sink:</span><span class="sxs-lookup"><span data-stu-id="2b4ca-154">The next diagram shows the Source Reader and Sink Writer:</span></span>

![diagramma che mostra la transcodifica con l'Reader di origine e il writer di sink](images/encoding02.png)

## <a name="related-topics"></a><span data-ttu-id="2b4ca-156">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2b4ca-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b4ca-157">Codifica e creazione di file</span><span class="sxs-lookup"><span data-stu-id="2b4ca-157">Encoding and File Authoring</span></span>](encoding-and-file-authoring.md)
</dt> <dt>

[<span data-ttu-id="2b4ca-158">Programmazione Media Foundation: concetti essenziali</span><span class="sxs-lookup"><span data-stu-id="2b4ca-158">Media Foundation Programming: Essential Concepts</span></span>](media-foundation-programming--essential-concepts.md)
</dt> </dl>

 

 



