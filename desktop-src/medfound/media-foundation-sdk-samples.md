---
description: Questa sezione descrive le applicazioni di esempio che illustrano come usare Media Foundation. Encoding SamplesPlayback SamplesPlug-InsSource Reader SamplesVideo CaptureMiscellaneous SamplesDeprecated o argomenti obsoleti SamplesRelated
ms.assetid: 9d460107-ec12-4df5-a7a9-d19943685599
title: Esempi di Media Foundation SDK
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f335b5ba744b098efdb7570aa861ad36fc9216cf
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "103761417"
---
# <a name="media-foundation-sdk-samples"></a><span data-ttu-id="ea581-103">Esempi di Media Foundation SDK</span><span class="sxs-lookup"><span data-stu-id="ea581-103">Media Foundation SDK Samples</span></span>

<span data-ttu-id="ea581-104">In questa sezione vengono descritte le applicazioni di esempio che illustrano come utilizzare Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="ea581-104">This section describes sample applications that demonstrate how to use Media Foundation.</span></span>

-   [<span data-ttu-id="ea581-105">Esempi di codifica</span><span class="sxs-lookup"><span data-stu-id="ea581-105">Encoding Samples</span></span>](#encoding-samples)
-   [<span data-ttu-id="ea581-106">Esempi di riproduzione</span><span class="sxs-lookup"><span data-stu-id="ea581-106">Playback Samples</span></span>](#playback-samples)
-   [<span data-ttu-id="ea581-107">Plug-in</span><span class="sxs-lookup"><span data-stu-id="ea581-107">Plug-Ins</span></span>](#plug-ins)
-   [<span data-ttu-id="ea581-108">Esempi di Reader di origine</span><span class="sxs-lookup"><span data-stu-id="ea581-108">Source Reader Samples</span></span>](#source-reader-samples)
-   [<span data-ttu-id="ea581-109">Acquisizione video</span><span class="sxs-lookup"><span data-stu-id="ea581-109">Video Capture</span></span>](#video-capture)
-   [<span data-ttu-id="ea581-110">Esempi vari</span><span class="sxs-lookup"><span data-stu-id="ea581-110">Miscellaneous Samples</span></span>](#miscellaneous-samples)
-   [<span data-ttu-id="ea581-111">Esempi deprecati o obsoleti</span><span class="sxs-lookup"><span data-stu-id="ea581-111">Deprecated or Obsolete Samples</span></span>](#deprecated-or-obsolete-samples)
-   [<span data-ttu-id="ea581-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ea581-112">Related topics</span></span>](#related-topics)

## <a name="encoding-samples"></a><span data-ttu-id="ea581-113">Esempi di codifica</span><span class="sxs-lookup"><span data-stu-id="ea581-113">Encoding Samples</span></span>



| <span data-ttu-id="ea581-114">Esempio</span><span class="sxs-lookup"><span data-stu-id="ea581-114">Sample</span></span>                            | <span data-ttu-id="ea581-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ea581-115">Description</span></span>                                                 |
|-----------------------------------|-------------------------------------------------------------|
| [<span data-ttu-id="ea581-116">Transcodifica</span><span class="sxs-lookup"><span data-stu-id="ea581-116">Transcode</span></span>](transcode-sample.md) | <span data-ttu-id="ea581-117">Viene illustrato come ricodificare un file multimediale in un formato Windows Media.</span><span class="sxs-lookup"><span data-stu-id="ea581-117">Shows how to reencode a media file to Windows Media format.</span></span> |



 

## <a name="playback-samples"></a><span data-ttu-id="ea581-118">Esempi di riproduzione</span><span class="sxs-lookup"><span data-stu-id="ea581-118">Playback Samples</span></span>



| <span data-ttu-id="ea581-119">Esempio</span><span class="sxs-lookup"><span data-stu-id="ea581-119">Sample</span></span>                                            | <span data-ttu-id="ea581-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ea581-120">Description</span></span>                                                                                                                                                                                                     |
|---------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea581-121">[BasicPlayback](/previous-versions//bb970475(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ea581-121">[BasicPlayback](/previous-versions//bb970475(v=vs.85))</span></span>          | <span data-ttu-id="ea581-122">Riproduce file audio e video usando la [sessione multimediale](media-session.md).</span><span class="sxs-lookup"><span data-stu-id="ea581-122">Plays audio and video files by using the [Media Session](media-session.md).</span></span> <span data-ttu-id="ea581-123">In questo esempio viene illustrato come creare topologie di riproduzione, controllare la sessione multimediale e ricevere eventi della sessione durante la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="ea581-123">This sample demonstrates how to create playback topologies, control the Media Session, and receive session events during playback.</span></span> |
| <span data-ttu-id="ea581-124">[MFPlayer](/previous-versions//bb970516(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ea581-124">[MFPlayer](/previous-versions//bb970516(v=vs.85))</span></span>                    | <span data-ttu-id="ea581-125">Illustra alcune funzioni di riproduzione che non sono incluse nell'esempio [BasicPlayback](/previous-versions//bb970475(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="ea581-125">Demonstrates some playback functions that are not included in the [BasicPlayback](/previous-versions//bb970475(v=vs.85)) sample.</span></span>                                                                                              |
| [<span data-ttu-id="ea581-126">ProtectedPlayback</span><span class="sxs-lookup"><span data-stu-id="ea581-126">ProtectedPlayback</span></span>](protectedplayback-sample.md) | <span data-ttu-id="ea581-127">Riproduce file audio e video protetti.</span><span class="sxs-lookup"><span data-stu-id="ea581-127">Plays protected audio and video files.</span></span> <span data-ttu-id="ea581-128">Questo esempio illustra come usare la sessione del percorso multimediale protetto (PMP) e come usare gli oggetti di attivazione del contenuto.</span><span class="sxs-lookup"><span data-stu-id="ea581-128">This sample shows how to use the protected media path (PMP) session and how to use content enabler objects.</span></span>                                                              |



 

## <a name="plug-ins"></a><span data-ttu-id="ea581-129">Plug-Ins</span><span class="sxs-lookup"><span data-stu-id="ea581-129">Plug-Ins</span></span>



| <span data-ttu-id="ea581-130">Esempio</span><span class="sxs-lookup"><span data-stu-id="ea581-130">Sample</span></span>                                       | <span data-ttu-id="ea581-131">Sub-Area</span><span class="sxs-lookup"><span data-stu-id="ea581-131">Sub-Area</span></span>                         | <span data-ttu-id="ea581-132">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ea581-132">Description</span></span>                                                                                            |
|----------------------------------------------|----------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ea581-133">Decodificatore</span><span class="sxs-lookup"><span data-stu-id="ea581-133">Decoder</span></span>](decoder-sample.md)                | <span data-ttu-id="ea581-134">Trasformazione Media Foundation (MFT)</span><span class="sxs-lookup"><span data-stu-id="ea581-134">Media Foundation transform (MFT)</span></span> | <span data-ttu-id="ea581-135">Decodificatore video.</span><span class="sxs-lookup"><span data-stu-id="ea581-135">Video decoder.</span></span>                                                                                         |
| [<span data-ttu-id="ea581-136">EVRPresenter</span><span class="sxs-lookup"><span data-stu-id="ea581-136">EVRPresenter</span></span>](evrpresenter-sample.md)      | <span data-ttu-id="ea581-137">Varie</span><span class="sxs-lookup"><span data-stu-id="ea581-137">Miscellaneous</span></span>                    | <span data-ttu-id="ea581-138">Presenter personalizzato per il [renderer video avanzato](enhanced-video-renderer.md) (EVR).</span><span class="sxs-lookup"><span data-stu-id="ea581-138">Custom presenter for the [Enhanced Video Renderer](enhanced-video-renderer.md) (EVR).</span></span>                 |
| [<span data-ttu-id="ea581-139">\_AUDIODELAY MFT</span><span class="sxs-lookup"><span data-stu-id="ea581-139">MFT\_AudioDelay</span></span>](mft-audiodelay-sample.md) | <span data-ttu-id="ea581-140">MFT</span><span class="sxs-lookup"><span data-stu-id="ea581-140">MFT</span></span>                              | <span data-ttu-id="ea581-141">Trasformazione effetto audio.</span><span class="sxs-lookup"><span data-stu-id="ea581-141">Audio effect transform.</span></span> <span data-ttu-id="ea581-142">Viene illustrato come scrivere un MFT di base per l'elaborazione audio.</span><span class="sxs-lookup"><span data-stu-id="ea581-142">Shows how to write a basic MFT for audio processing.</span></span>                           |
| [<span data-ttu-id="ea581-143">\_Scala di grigi MFT</span><span class="sxs-lookup"><span data-stu-id="ea581-143">MFT\_Grayscale</span></span>](mft-grayscale-sample.md)   | <span data-ttu-id="ea581-144">MFT</span><span class="sxs-lookup"><span data-stu-id="ea581-144">MFT</span></span>                              | <span data-ttu-id="ea581-145">Effetto video in scala di grigi.</span><span class="sxs-lookup"><span data-stu-id="ea581-145">Grayscale video effect.</span></span> <span data-ttu-id="ea581-146">Viene illustrato come scrivere un MFT di base per l'elaborazione video.</span><span class="sxs-lookup"><span data-stu-id="ea581-146">Shows how to write a basic MFT for video processing.</span></span>                           |
| [<span data-ttu-id="ea581-147">MPEG1Source</span><span class="sxs-lookup"><span data-stu-id="ea581-147">MPEG1Source</span></span>](mpeg1source-sample.md)        | <span data-ttu-id="ea581-148">Origine supporto</span><span class="sxs-lookup"><span data-stu-id="ea581-148">Media source</span></span>                     | <span data-ttu-id="ea581-149">Analizza i flussi a livello di sistema MPEG-1.</span><span class="sxs-lookup"><span data-stu-id="ea581-149">Parses MPEG-1 systems-layer streams.</span></span> <span data-ttu-id="ea581-150">Viene illustrato come scrivere un'origine multimediale personalizzata e un gestore del flusso di byte.</span><span class="sxs-lookup"><span data-stu-id="ea581-150">Shows how to write a custom media source and byte-stream handler.</span></span> |
| [<span data-ttu-id="ea581-151">WavSink</span><span class="sxs-lookup"><span data-stu-id="ea581-151">WavSink</span></span>](wavsink-sample.md)                | <span data-ttu-id="ea581-152">Sink multimediale</span><span class="sxs-lookup"><span data-stu-id="ea581-152">Media sink</span></span>                       | <span data-ttu-id="ea581-153">Sink di archivio che scrive i file WAV.</span><span class="sxs-lookup"><span data-stu-id="ea581-153">An archive sink that writes .wav files.</span></span> <span data-ttu-id="ea581-154">Viene illustrato come scrivere un sink multimediale personalizzato.</span><span class="sxs-lookup"><span data-stu-id="ea581-154">Shows how to write a custom media sink.</span></span>                        |
| [<span data-ttu-id="ea581-155">WavSource</span><span class="sxs-lookup"><span data-stu-id="ea581-155">WavSource</span></span>](wavsource-sample.md)            | <span data-ttu-id="ea581-156">Origine supporto</span><span class="sxs-lookup"><span data-stu-id="ea581-156">Media source</span></span>                     | <span data-ttu-id="ea581-157">Analizza i file WAV.</span><span class="sxs-lookup"><span data-stu-id="ea581-157">Parses .wav files.</span></span> <span data-ttu-id="ea581-158">Viene illustrato come scrivere un'origine multimediale personalizzata e un gestore del flusso di byte.</span><span class="sxs-lookup"><span data-stu-id="ea581-158">Shows how to write a custom media source and byte-stream handler.</span></span>                   |



 

## <a name="source-reader-samples"></a><span data-ttu-id="ea581-159">Esempi di Reader di origine</span><span class="sxs-lookup"><span data-stu-id="ea581-159">Source Reader Samples</span></span>



| <span data-ttu-id="ea581-160">Esempio</span><span class="sxs-lookup"><span data-stu-id="ea581-160">Sample</span></span>                                      | <span data-ttu-id="ea581-161">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ea581-161">Description</span></span>                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="ea581-162">Clip audio</span><span class="sxs-lookup"><span data-stu-id="ea581-162">Audio Clip</span></span>](audio-clip-sample.md)         | <span data-ttu-id="ea581-163">Usa il [lettore di origine](source-reader.md) per decodificare l'audio da un file multimediale.</span><span class="sxs-lookup"><span data-stu-id="ea581-163">Uses the [Source Reader](source-reader.md) to decode audio from a media file.</span></span>      |
| [<span data-ttu-id="ea581-164">VideoThumbnail</span><span class="sxs-lookup"><span data-stu-id="ea581-164">VideoThumbnail</span></span>](videothumbnail-sample.md) | <span data-ttu-id="ea581-165">Usa il [lettore di origine](source-reader.md) per ottenere singoli frame da un file video.</span><span class="sxs-lookup"><span data-stu-id="ea581-165">Uses the [Source Reader](source-reader.md) to get single frames from a video file.</span></span> |



 

## <a name="video-capture"></a><span data-ttu-id="ea581-166">Acquisizione video</span><span class="sxs-lookup"><span data-stu-id="ea581-166">Video Capture</span></span>



| <span data-ttu-id="ea581-167">Esempio</span><span class="sxs-lookup"><span data-stu-id="ea581-167">Sample</span></span>                                        | <span data-ttu-id="ea581-168">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ea581-168">Description</span></span>                                                                                 |
|-----------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ea581-169">MFCaptureD3D</span><span class="sxs-lookup"><span data-stu-id="ea581-169">MFCaptureD3D</span></span>](mfcaptured3d-sample.md)       | <span data-ttu-id="ea581-170">Mostra come visualizzare in anteprima i video da un dispositivo di acquisizione video, usando Direct3D per eseguire il rendering del video.</span><span class="sxs-lookup"><span data-stu-id="ea581-170">Shows how to preview video from a video capture device, using Direct3D to render the video.</span></span> |
| [<span data-ttu-id="ea581-171">MFCaptureToFile</span><span class="sxs-lookup"><span data-stu-id="ea581-171">MFCaptureToFile</span></span>](mfcapturetofile-sample.md) | <span data-ttu-id="ea581-172">Mostra come acquisire video da una videocamera a un file.</span><span class="sxs-lookup"><span data-stu-id="ea581-172">Shows how to capture video from a video camera to a file.</span></span>                                   |



 

## <a name="miscellaneous-samples"></a><span data-ttu-id="ea581-173">Esempi vari</span><span class="sxs-lookup"><span data-stu-id="ea581-173">Miscellaneous Samples</span></span>



| <span data-ttu-id="ea581-174">Esempio</span><span class="sxs-lookup"><span data-stu-id="ea581-174">Sample</span></span>                                         | <span data-ttu-id="ea581-175">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ea581-175">Description</span></span>                                                                                                                                           |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ea581-176">ASFParser</span><span class="sxs-lookup"><span data-stu-id="ea581-176">ASFParser</span></span>](asfparser-sample.md)              | <span data-ttu-id="ea581-177">Viene illustrato come analizzare i dati da un file Advanced Systems Format (ASF).</span><span class="sxs-lookup"><span data-stu-id="ea581-177">Shows how to parse data from an Advanced Systems Format (ASF) file.</span></span>                                                                                   |
| [<span data-ttu-id="ea581-178">DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="ea581-178">DXVA-HD</span></span>](dxva-hd-sample.md)                  | <span data-ttu-id="ea581-179">Mostra come usare Microsoft DirectX Video Acceleration High Definition (DXVA-HD).</span><span class="sxs-lookup"><span data-stu-id="ea581-179">Shows how to use Microsoft DirectX Video Acceleration High Definition (DXVA-HD).</span></span>                                                                      |
| [<span data-ttu-id="ea581-180">\_VIDEOPROC DXVA2</span><span class="sxs-lookup"><span data-stu-id="ea581-180">DXVA2\_VideoProc</span></span>](dxva2-videoproc-sample.md) | <span data-ttu-id="ea581-181">Usa l'accelerazione video DirectX (DXVA) 2,0 per creare un flusso di video YUV 4:2:2.</span><span class="sxs-lookup"><span data-stu-id="ea581-181">Uses DirectX Video Acceleration (DXVA) 2.0 to create a stream of 4:2:2 YUV video.</span></span> <span data-ttu-id="ea581-182">Questo esempio illustra come usare le funzionalità di elaborazione video di DXVA.</span><span class="sxs-lookup"><span data-stu-id="ea581-182">This sample shows how to use the video processing features of DXVA.</span></span> |



 

## <a name="deprecated-or-obsolete-samples"></a><span data-ttu-id="ea581-183">Esempi deprecati o obsoleti</span><span class="sxs-lookup"><span data-stu-id="ea581-183">Deprecated or Obsolete Samples</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ea581-184">Esempio</span><span class="sxs-lookup"><span data-stu-id="ea581-184">Sample</span></span></th>
<th><span data-ttu-id="ea581-185">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ea581-185">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ea581-186"><a href="mfplayer2-sample.md">MFPlayer2</a></span><span class="sxs-lookup"><span data-stu-id="ea581-186"><a href="mfplayer2-sample.md">MFPlayer2</a></span></span></td>
<td><span data-ttu-id="ea581-187">Illustra alcune funzionalità di riproduzione avanzate dell'API <a href="using-mfplay-for-audio-video-playback.md">MFPlay</a> .</span><span class="sxs-lookup"><span data-stu-id="ea581-187">Demonstrates some advanced playback features of the <a href="using-mfplay-for-audio-video-playback.md">MFPlay</a> API.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ea581-188"><a href="/previous-versions//bb970336(v=vs.85)">PlaybackFX</a></span><span class="sxs-lookup"><span data-stu-id="ea581-188"><a href="/previous-versions//bb970336(v=vs.85)">PlaybackFX</a></span></span></td>
<td><span data-ttu-id="ea581-189">Applica un effetto scala di grigi al video.</span><span class="sxs-lookup"><span data-stu-id="ea581-189">Applies a grayscale effect to video.</span></span> <span data-ttu-id="ea581-190">Viene illustrato come inserire MFTs in una topologia di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="ea581-190">Shows how to insert MFTs into a playback topology.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="ea581-191">Questo esempio non è più incluso nell'SDK.</span><span class="sxs-lookup"><span data-stu-id="ea581-191">This sample is no longer included in the SDK.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ea581-192"><a href="playlist-sample.md">Playlist</a></span><span class="sxs-lookup"><span data-stu-id="ea581-192"><a href="playlist-sample.md">Playlist</a></span></span></td>
<td><span data-ttu-id="ea581-193">Riproduce una sequenza di file audio usando l'origine del sequencer.</span><span class="sxs-lookup"><span data-stu-id="ea581-193">Plays a sequence of audio files using the sequencer source.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="ea581-194">Questo esempio non è più incluso nell'SDK.</span><span class="sxs-lookup"><span data-stu-id="ea581-194">This sample is no longer included in the SDK.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ea581-195"><a href="simplecapture-sample.md">SimpleCapture</a></span><span class="sxs-lookup"><span data-stu-id="ea581-195"><a href="simplecapture-sample.md">SimpleCapture</a></span></span></td>
<td><span data-ttu-id="ea581-196">Mostra come visualizzare in anteprima i video da un dispositivo di acquisizione video, usando l'API MFPlay.</span><span class="sxs-lookup"><span data-stu-id="ea581-196">Shows how to preview video from a video capture device, using the MFPlay API.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ea581-197"><a href="simpleplay-sample.md">SimplePlay</a></span><span class="sxs-lookup"><span data-stu-id="ea581-197"><a href="simpleplay-sample.md">SimplePlay</a></span></span></td>
<td><span data-ttu-id="ea581-198">Viene illustrato come riprodurre un file multimediale tramite l'API MFPlay.</span><span class="sxs-lookup"><span data-stu-id="ea581-198">Shows how to play a media file using the MFPlay API.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="ea581-199">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ea581-199">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea581-200">Microsoft Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ea581-200">Microsoft Media Foundation</span></span>](microsoft-media-foundation-sdk.md)
</dt> <dt>

[<span data-ttu-id="ea581-201">Informazioni su Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ea581-201">About Media Foundation</span></span>](about-the-media-foundation-sdk.md)
</dt> </dl>

 

 
