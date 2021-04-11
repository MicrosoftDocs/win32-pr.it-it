---
description: Questo argomento descrive come usare l'API transcode per codificare un file multimediale.
ms.assetid: 52b27359-b319-41a0-88e8-d23567420e92
title: Uso dell'API transcode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bb97dd61ef75e71a82b522b65b682f861022bcf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127887"
---
# <a name="using-the-transcode-api"></a><span data-ttu-id="02a09-103">Uso dell'API transcode</span><span class="sxs-lookup"><span data-stu-id="02a09-103">Using the Transcode API</span></span>

<span data-ttu-id="02a09-104">Questo argomento descrive come usare l'API transcode per codificare un file multimediale.</span><span class="sxs-lookup"><span data-stu-id="02a09-104">This topic described how to use the transcode API to encode a media file.</span></span>

-   [<span data-ttu-id="02a09-105">Overview</span><span class="sxs-lookup"><span data-stu-id="02a09-105">Overview</span></span>](#overview)
-   [<span data-ttu-id="02a09-106">Creazione di un'origine multimediale</span><span class="sxs-lookup"><span data-stu-id="02a09-106">Creating a Media Source</span></span>](#creating-a-media-source)
-   [<span data-ttu-id="02a09-107">Creazione di un profilo di transcodifica</span><span class="sxs-lookup"><span data-stu-id="02a09-107">Creating a Transcode Profile</span></span>](#creating-a-transcode-profile)
    -   [<span data-ttu-id="02a09-108">Attributi audio</span><span class="sxs-lookup"><span data-stu-id="02a09-108">Audio Attributes</span></span>](#audio-attributes)
    -   [<span data-ttu-id="02a09-109">Attributi video</span><span class="sxs-lookup"><span data-stu-id="02a09-109">Video Attributes</span></span>](#video-attributes)
    -   [<span data-ttu-id="02a09-110">Attributi del contenitore</span><span class="sxs-lookup"><span data-stu-id="02a09-110">Container Attributes</span></span>](#container-attributes)
-   [<span data-ttu-id="02a09-111">Creazione di una topologia transcodifica</span><span class="sxs-lookup"><span data-stu-id="02a09-111">Creating a Transcode Topology</span></span>](#creating-a-transcode-topology)
-   [<span data-ttu-id="02a09-112">Esecuzione della sessione di codifica</span><span class="sxs-lookup"><span data-stu-id="02a09-112">Running the Encoding Session</span></span>](#running-the-encoding-session)
-   [<span data-ttu-id="02a09-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="02a09-113">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="02a09-114">Panoramica</span><span class="sxs-lookup"><span data-stu-id="02a09-114">Overview</span></span>

<span data-ttu-id="02a09-115">Prima di utilizzare l'API transcode, l'applicazione deve disporre delle seguenti informazioni:</span><span class="sxs-lookup"><span data-stu-id="02a09-115">Before using the transcode API, the application must have the following pieces of information:</span></span>

-   <span data-ttu-id="02a09-116">Il percorso o l'URL di un file multimediale esistente che verrà codificato nuovamente.</span><span class="sxs-lookup"><span data-stu-id="02a09-116">The path or URL to an existing media file that will be re-encoded.</span></span>
-   <span data-ttu-id="02a09-117">Nome del file di output.</span><span class="sxs-lookup"><span data-stu-id="02a09-117">The name of the output file.</span></span>
-   <span data-ttu-id="02a09-118">Tipo di contenitore per il file di output, ad esempio MP4 o Advanced Streaming Format (ASF).</span><span class="sxs-lookup"><span data-stu-id="02a09-118">The container type for the output file, such as MP4 or Advanced Streaming Format (ASF).</span></span>
-   <span data-ttu-id="02a09-119">Formato di codifica.</span><span class="sxs-lookup"><span data-stu-id="02a09-119">The encoding format.</span></span> <span data-ttu-id="02a09-120">Queste informazioni includono i tipi di supporto che descrivono i flussi audio e video codificati.</span><span class="sxs-lookup"><span data-stu-id="02a09-120">This information includes the media types that describe the encoded audio and video streams.</span></span>

<span data-ttu-id="02a09-121">Per usare l'API transcode, un'applicazione esegue i passaggi seguenti.</span><span class="sxs-lookup"><span data-stu-id="02a09-121">To use the transcode API, an application performs the following steps.</span></span>

1.  <span data-ttu-id="02a09-122">Creare un'origine multimediale per leggere il file di origine.</span><span class="sxs-lookup"><span data-stu-id="02a09-122">Create a media source to read the source file.</span></span>
2.  <span data-ttu-id="02a09-123">Creare un profilo transcodifica.</span><span class="sxs-lookup"><span data-stu-id="02a09-123">Create a transcode profile.</span></span> <span data-ttu-id="02a09-124">Aggiungere gli attributi che descrivono il flusso audio, il flusso video e il contenitore di file.</span><span class="sxs-lookup"><span data-stu-id="02a09-124">Add attributes that describe the audio stream, video stream, and file container.</span></span>
3.  <span data-ttu-id="02a09-125">Utilizzare il profilo transcodifica per creare una topologia di codifica.</span><span class="sxs-lookup"><span data-stu-id="02a09-125">Use the transcode profile to create an encoding topology.</span></span> <span data-ttu-id="02a09-126">Per ulteriori informazioni sulle topologie, vedere [informazioni sulle topologie](about-topologies.md).</span><span class="sxs-lookup"><span data-stu-id="02a09-126">(For more information about topologies, see [About Topologies](about-topologies.md).)</span></span>
4.  <span data-ttu-id="02a09-127">Impostare la topologia nella [sessione multimediale](media-session.md).</span><span class="sxs-lookup"><span data-stu-id="02a09-127">Set the topology on the [Media Session](media-session.md).</span></span>
5.  <span data-ttu-id="02a09-128">Avviare la sessione multimediale e attendere l'evento [MESessionEnded](mesessionended.md) .</span><span class="sxs-lookup"><span data-stu-id="02a09-128">Start the Media Session and wait for the [MESessionEnded](mesessionended.md) event.</span></span>

<span data-ttu-id="02a09-129">Nella parte restante di questo argomento vengono descritti in modo più dettagliato questi passaggi.</span><span class="sxs-lookup"><span data-stu-id="02a09-129">The remainder of this topic describes these steps in more detail.</span></span>

## <a name="creating-a-media-source"></a><span data-ttu-id="02a09-130">Creazione di un'origine multimediale</span><span class="sxs-lookup"><span data-stu-id="02a09-130">Creating a Media Source</span></span>

<span data-ttu-id="02a09-131">Un'origine multimediale è un oggetto che legge e analizza il file di origine.</span><span class="sxs-lookup"><span data-stu-id="02a09-131">A media source is an object that reads and parses the source file.</span></span> <span data-ttu-id="02a09-132">Per creare un'origine multimediale, usare il [resolver di origine](source-resolver.md).</span><span class="sxs-lookup"><span data-stu-id="02a09-132">To create a media source, use the [Source Resolver](source-resolver.md).</span></span> <span data-ttu-id="02a09-133">È possibile trovare il codice di esempio nell'argomento [usando il resolver di origine](using-the-source-resolver.md).</span><span class="sxs-lookup"><span data-stu-id="02a09-133">You can find example code in the topic [Using the Source Resolver](using-the-source-resolver.md).</span></span>

## <a name="creating-a-transcode-profile"></a><span data-ttu-id="02a09-134">Creazione di un profilo di transcodifica</span><span class="sxs-lookup"><span data-stu-id="02a09-134">Creating a Transcode Profile</span></span>

<span data-ttu-id="02a09-135">Un *profilo di transcodifica* descrive il formato e le impostazioni utilizzati per codificare il file di output.</span><span class="sxs-lookup"><span data-stu-id="02a09-135">A *transcode profile* describes the format and settings that are used to encode the output file.</span></span> <span data-ttu-id="02a09-136">Il profilo transcode contiene tre set di attributi:</span><span class="sxs-lookup"><span data-stu-id="02a09-136">The transcode profile contains three sets of attributes:</span></span>

-   <span data-ttu-id="02a09-137">Attributi audio: descrivere il formato audio di destinazione e le impostazioni del codificatore audio.</span><span class="sxs-lookup"><span data-stu-id="02a09-137">Audio attributes: Describe the target audio format and audio encoder settings.</span></span>
-   <span data-ttu-id="02a09-138">Attributi video: descrivere il formato video di destinazione e le impostazioni del codificatore video.</span><span class="sxs-lookup"><span data-stu-id="02a09-138">Video attributes: Describe the target video format and video encoder settings.</span></span>
-   <span data-ttu-id="02a09-139">Attributi del contenitore: definire il tipo di contenitore di file, nonché alcune impostazioni di codifica globali.</span><span class="sxs-lookup"><span data-stu-id="02a09-139">Container attributes: Define the type of file container, as well as some global encoding settings.</span></span>

<span data-ttu-id="02a09-140">Per creare un profilo transcodifica, chiamare la funzione [**MFCreateTranscodeProfile**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodeprofile) .</span><span class="sxs-lookup"><span data-stu-id="02a09-140">To create a transcode profile, call the [**MFCreateTranscodeProfile**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodeprofile) function.</span></span> <span data-ttu-id="02a09-141">Questa funzione restituisce un puntatore all'interfaccia [**IMFTranscodeProfile**](/windows/desktop/api/mfidl/nn-mfidl-imftranscodeprofile) .</span><span class="sxs-lookup"><span data-stu-id="02a09-141">This function returns a pointer to the [**IMFTranscodeProfile**](/windows/desktop/api/mfidl/nn-mfidl-imftranscodeprofile) interface.</span></span> <span data-ttu-id="02a09-142">L'oggetto profilo iniziale è vuoto; non contiene attributi.</span><span class="sxs-lookup"><span data-stu-id="02a09-142">The initial profile object is empty; it contains no attributes.</span></span> <span data-ttu-id="02a09-143">Il passaggio successivo consiste nell'aggiungere gli attributi che definiscono il profilo.</span><span class="sxs-lookup"><span data-stu-id="02a09-143">The next step is to add the attributes that define the profile.</span></span>

### <a name="audio-attributes"></a><span data-ttu-id="02a09-144">Attributi audio</span><span class="sxs-lookup"><span data-stu-id="02a09-144">Audio Attributes</span></span>

<span data-ttu-id="02a09-145">Per aggiungere attributi per il flusso audio, chiamare [**IMFTranscodeProfile:: SetAudioAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes).</span><span class="sxs-lookup"><span data-stu-id="02a09-145">To add attributes for the audio stream, call [**IMFTranscodeProfile::SetAudioAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes).</span></span> <span data-ttu-id="02a09-146">Questi attributi specificano come codificare il flusso audio.</span><span class="sxs-lookup"><span data-stu-id="02a09-146">These attributes specify how the audio stream is encoded.</span></span> <span data-ttu-id="02a09-147">Se il file di output non conterrà un flusso audio, omettere questi attributi.</span><span class="sxs-lookup"><span data-stu-id="02a09-147">If the output file will not contain an audio stream, omit these attributes.</span></span>

<span data-ttu-id="02a09-148">Gli attributi audio rientrano in due categorie:</span><span class="sxs-lookup"><span data-stu-id="02a09-148">Audio attributes fall into two categories:</span></span>

-   <span data-ttu-id="02a09-149">Attributi che specificano il formato del flusso codificato</span><span class="sxs-lookup"><span data-stu-id="02a09-149">Attributes that specify the format of the encoded stream</span></span>
-   <span data-ttu-id="02a09-150">Attributi che specificano altri parametri di codifica.</span><span class="sxs-lookup"><span data-stu-id="02a09-150">Attributes that specify other encoding parameters.</span></span>

<span data-ttu-id="02a09-151">Gli attributi di formato sono semplicemente attributi di tipo media, come descritto nella sezione [tipi di supporti audio](audio-media-types.md).</span><span class="sxs-lookup"><span data-stu-id="02a09-151">Format attributes are simply media-type attributes, as described in the section [Audio Media Types](audio-media-types.md).</span></span> <span data-ttu-id="02a09-152">Il set esatto di attributi di formato dipende dal codificatore.</span><span class="sxs-lookup"><span data-stu-id="02a09-152">The exact set of format attributes depends on the encoder.</span></span> <span data-ttu-id="02a09-153">(Vedere [formati multimediali supportati in Media Foundation](supported-media-formats-in-media-foundation.md)). Di seguito è riportato un elenco di attributi di formato audio tipici:</span><span class="sxs-lookup"><span data-stu-id="02a09-153">(See [Supported Media Formats in Media Foundation](supported-media-formats-in-media-foundation.md).) Here is a list of typical audio format attributes:</span></span>



| <span data-ttu-id="02a09-154">Format (attributo)</span><span class="sxs-lookup"><span data-stu-id="02a09-154">Format Attribute</span></span>                                                                         | <span data-ttu-id="02a09-155">Descrizione</span><span class="sxs-lookup"><span data-stu-id="02a09-155">Description</span></span>                                                      |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="02a09-156">sottotipo MF \_ mt \_</span><span class="sxs-lookup"><span data-stu-id="02a09-156">MF\_MT\_SUBTYPE</span></span>](mf-mt-subtype-attribute.md)                                           | <span data-ttu-id="02a09-157">Sottotipo.</span><span class="sxs-lookup"><span data-stu-id="02a09-157">The subtype.</span></span> <span data-ttu-id="02a09-158">Vedere [GUID del sottotipo audio](audio-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="02a09-158">See [Audio Subtype GUIDs](audio-subtype-guids.md).</span></span> |
| [<span data-ttu-id="02a09-159">numero \_ di \_ \_ canali audio MF mt \_</span><span class="sxs-lookup"><span data-stu-id="02a09-159">MF\_MT\_AUDIO\_NUM\_CHANNELS</span></span>](mf-mt-audio-num-channels-attribute.md)                   | <span data-ttu-id="02a09-160">Numero di canali audio.</span><span class="sxs-lookup"><span data-stu-id="02a09-160">The number of audio channels.</span></span>                                    |
| [<span data-ttu-id="02a09-161">\_ \_ campioni audio MF \_ mt \_ al \_ secondo</span><span class="sxs-lookup"><span data-stu-id="02a09-161">MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND</span></span>](mf-mt-audio-samples-per-second-attribute.md)      | <span data-ttu-id="02a09-162">Numero di campioni audio al secondo.</span><span class="sxs-lookup"><span data-stu-id="02a09-162">The number of audio samples per second.</span></span>                          |
| [<span data-ttu-id="02a09-163">\_ \_ \_ allineamento blocchi audio MF \_ mt</span><span class="sxs-lookup"><span data-stu-id="02a09-163">MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT</span></span>](mf-mt-audio-block-alignment-attribute.md)             | <span data-ttu-id="02a09-164">Allineamento del blocco.</span><span class="sxs-lookup"><span data-stu-id="02a09-164">The block alignment.</span></span>                                             |
| [<span data-ttu-id="02a09-165">\_ \_ Media byte audio MF mt \_ \_ \_ al \_ secondo</span><span class="sxs-lookup"><span data-stu-id="02a09-165">MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md) | <span data-ttu-id="02a09-166">Numero medio di byte al secondo (velocità in bit codificata).</span><span class="sxs-lookup"><span data-stu-id="02a09-166">The average number of bytes per second (the encoded bit rate).</span></span>   |



 

<span data-ttu-id="02a09-167">Sono definiti i seguenti parametri di codifica.</span><span class="sxs-lookup"><span data-stu-id="02a09-167">The following encoding parameters are defined.</span></span>



| <span data-ttu-id="02a09-168">Parametro di codifica</span><span class="sxs-lookup"><span data-stu-id="02a09-168">Encoding Parameter</span></span>                                                             | <span data-ttu-id="02a09-169">Descrizione</span><span class="sxs-lookup"><span data-stu-id="02a09-169">Description</span></span>                                                                |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="02a09-170">\_ \_ \_ codificatore INserimenti MF transcode \_</span><span class="sxs-lookup"><span data-stu-id="02a09-170">MF\_TRANSCODE\_DONOT\_INSERT\_ENCODER</span></span>](mf-transcode-donot-insert-encoder.md) | <span data-ttu-id="02a09-171">Impedisce all'API transcodifica di inserire un codificatore per il flusso audio.</span><span class="sxs-lookup"><span data-stu-id="02a09-171">Prevents the transcode API from inserting an encoder for the audio stream.</span></span> |
| [<span data-ttu-id="02a09-172">MF \_ transcode \_ ENCODINGPROFILE</span><span class="sxs-lookup"><span data-stu-id="02a09-172">MF\_TRANSCODE\_ENCODINGPROFILE</span></span>](mf-transcode-encodingprofile.md)             | <span data-ttu-id="02a09-173">Specifica il modello di conformità del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="02a09-173">Specifies the device conformance template.</span></span> <span data-ttu-id="02a09-174">(Si applica solo ai file ASF).</span><span class="sxs-lookup"><span data-stu-id="02a09-174">(Applies only to ASF files.)</span></span>    |
| [<span data-ttu-id="02a09-175">MF \_ transcode \_ QUALITYVSSPEED</span><span class="sxs-lookup"><span data-stu-id="02a09-175">MF\_TRANSCODE\_QUALITYVSSPEED</span></span>](mf-transcode-qualityvsspeed.md)               | <span data-ttu-id="02a09-176">Specifica il compromesso tra la qualità e la velocità di codifica.</span><span class="sxs-lookup"><span data-stu-id="02a09-176">Specifies the trade-off between encoding quality and speed.</span></span>                |



 

<span data-ttu-id="02a09-177">È necessario impostare gli attributi di formato.</span><span class="sxs-lookup"><span data-stu-id="02a09-177">You must set the format attributes.</span></span> <span data-ttu-id="02a09-178">I parametri di codifica sono facoltativi.</span><span class="sxs-lookup"><span data-stu-id="02a09-178">The encoding parameters are optional.</span></span>

<span data-ttu-id="02a09-179">Un modo per trovare un formato compatibile con il codificatore consiste nel chiamare la funzione [**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) .</span><span class="sxs-lookup"><span data-stu-id="02a09-179">One way to find a format that is compatible with the encoder is to call the [**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) function.</span></span> <span data-ttu-id="02a09-180">Il codificatore desiderato è specificato dal sottotipo.</span><span class="sxs-lookup"><span data-stu-id="02a09-180">The desired encoder is specified by subtype.</span></span> <span data-ttu-id="02a09-181">La funzione restituisce una raccolta di tipi di supporto per il codificatore.</span><span class="sxs-lookup"><span data-stu-id="02a09-181">The function returns a collection of media types for that encoder.</span></span> <span data-ttu-id="02a09-182">È possibile selezionare un tipo dall'elenco e copiare gli attributi nel profilo.</span><span class="sxs-lookup"><span data-stu-id="02a09-182">You can select a type from the list and copy the attributes to the profile.</span></span> <span data-ttu-id="02a09-183">Per un codice di esempio che usa questo approccio, vedere [esercitazione: codifica di un file WMA](tutorial--converting-an-mp3-file-to-a-wma-file.md).</span><span class="sxs-lookup"><span data-stu-id="02a09-183">For example code that uses this approach, see [Tutorial: Encoding a WMA File](tutorial--converting-an-mp3-file-to-a-wma-file.md).</span></span>

### <a name="video-attributes"></a><span data-ttu-id="02a09-184">Attributi video</span><span class="sxs-lookup"><span data-stu-id="02a09-184">Video Attributes</span></span>

<span data-ttu-id="02a09-185">Per aggiungere attributi per il flusso video, chiamare [**IMFTranscodeProfile:: SetVideoAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes).</span><span class="sxs-lookup"><span data-stu-id="02a09-185">To add attributes for the video stream, call [**IMFTranscodeProfile::SetVideoAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes).</span></span> <span data-ttu-id="02a09-186">Questi attributi specificano il modo in cui il flusso video è codificato.</span><span class="sxs-lookup"><span data-stu-id="02a09-186">These attributes specify how the video stream is encoded.</span></span> <span data-ttu-id="02a09-187">Se il file di output non conterrà un flusso video, omettere questi attributi.</span><span class="sxs-lookup"><span data-stu-id="02a09-187">If the output file will not contain a video stream, omit these attributes.</span></span>

<span data-ttu-id="02a09-188">Come per gli attributi audio, gli attributi video rientrano in due categorie:</span><span class="sxs-lookup"><span data-stu-id="02a09-188">As with audio attributes, the video attributes fall into two categories:</span></span>

-   <span data-ttu-id="02a09-189">Attributi che specificano il formato del flusso codificato</span><span class="sxs-lookup"><span data-stu-id="02a09-189">Attributes that specify the format of the encoded stream</span></span>
-   <span data-ttu-id="02a09-190">Attributi che specificano altri parametri di codifica.</span><span class="sxs-lookup"><span data-stu-id="02a09-190">Attributes that specify other encoding parameters.</span></span>

<span data-ttu-id="02a09-191">Gli attributi di formato sono attributi del tipo di supporto, come descritto nella sezione [tipi di supporti video](video-media-types.md).</span><span class="sxs-lookup"><span data-stu-id="02a09-191">Format attributes are media-type attributes, as described in the section [Video Media Types](video-media-types.md).</span></span> <span data-ttu-id="02a09-192">Di seguito è riportato un elenco di attributi di formato video tipici:</span><span class="sxs-lookup"><span data-stu-id="02a09-192">Here is a list of typical video format attributes:</span></span>



| <span data-ttu-id="02a09-193">Format (attributo)</span><span class="sxs-lookup"><span data-stu-id="02a09-193">Format Attribute</span></span>                                                       | <span data-ttu-id="02a09-194">Descrizione</span><span class="sxs-lookup"><span data-stu-id="02a09-194">Description</span></span>                                                      |
|------------------------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="02a09-195">sottotipo MF \_ mt \_</span><span class="sxs-lookup"><span data-stu-id="02a09-195">MF\_MT\_SUBTYPE</span></span>](mf-mt-subtype-attribute.md)                         | <span data-ttu-id="02a09-196">Sottotipo.</span><span class="sxs-lookup"><span data-stu-id="02a09-196">The subtype.</span></span> <span data-ttu-id="02a09-197">Vedere [GUID del sottotipo video](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="02a09-197">See [Video Subtype GUIDs](video-subtype-guids.md).</span></span> |
| [<span data-ttu-id="02a09-198">\_ \_ frequenza fotogrammi MF mt \_</span><span class="sxs-lookup"><span data-stu-id="02a09-198">MF\_MT\_FRAME\_RATE</span></span>](mf-mt-frame-rate-attribute.md)                  | <span data-ttu-id="02a09-199">Frequenza dei fotogrammi.</span><span class="sxs-lookup"><span data-stu-id="02a09-199">The frame rate.</span></span>                                                  |
| [<span data-ttu-id="02a09-200">\_dimensioni del \_ frame MF mt \_</span><span class="sxs-lookup"><span data-stu-id="02a09-200">MF\_MT\_FRAME\_SIZE</span></span>](mf-mt-frame-size-attribute.md)                  | <span data-ttu-id="02a09-201">Dimensioni del frame.</span><span class="sxs-lookup"><span data-stu-id="02a09-201">The frame size.</span></span>                                                  |
| [<span data-ttu-id="02a09-202">**\_velocità in \_ bit media MF mt \_**</span><span class="sxs-lookup"><span data-stu-id="02a09-202">**MF\_MT\_AVG\_BITRATE**</span></span>](mf-mt-avg-bitrate-attribute.md)            | <span data-ttu-id="02a09-203">Velocità in bit media.</span><span class="sxs-lookup"><span data-stu-id="02a09-203">The average bit rate.</span></span>                                            |
| [<span data-ttu-id="02a09-204">proporzioni MF \_ mt \_ pixel \_ \_</span><span class="sxs-lookup"><span data-stu-id="02a09-204">MF\_MT\_PIXEL\_ASPECT\_RATIO</span></span>](mf-mt-pixel-aspect-ratio-attribute.md) | <span data-ttu-id="02a09-205">Proporzioni dei pixel.</span><span class="sxs-lookup"><span data-stu-id="02a09-205">The pixel aspect ratio.</span></span>                                          |



 

<span data-ttu-id="02a09-206">Sono definiti i seguenti parametri di codifica.</span><span class="sxs-lookup"><span data-stu-id="02a09-206">The following encoding parameters are defined.</span></span>



| <span data-ttu-id="02a09-207">Parametro di codifica</span><span class="sxs-lookup"><span data-stu-id="02a09-207">Encoding Parameter</span></span>                                                             | <span data-ttu-id="02a09-208">Descrizione</span><span class="sxs-lookup"><span data-stu-id="02a09-208">Description</span></span>                                                                |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="02a09-209">\_ \_ \_ codificatore INserimenti MF transcode \_</span><span class="sxs-lookup"><span data-stu-id="02a09-209">MF\_TRANSCODE\_DONOT\_INSERT\_ENCODER</span></span>](mf-transcode-donot-insert-encoder.md) | <span data-ttu-id="02a09-210">Impedisce all'API transcodifica di inserire un codificatore per il flusso video.</span><span class="sxs-lookup"><span data-stu-id="02a09-210">Prevents the transcode API from inserting an encoder for the video stream.</span></span> |
| [<span data-ttu-id="02a09-211">MF \_ transcode \_ ENCODINGPROFILE</span><span class="sxs-lookup"><span data-stu-id="02a09-211">MF\_TRANSCODE\_ENCODINGPROFILE</span></span>](mf-transcode-encodingprofile.md)             | <span data-ttu-id="02a09-212">Specifica il modello di conformità del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="02a09-212">Specifies the device conformance template.</span></span> <span data-ttu-id="02a09-213">(Si applica solo ai file ASF).</span><span class="sxs-lookup"><span data-stu-id="02a09-213">(Applies only to ASF files.)</span></span>    |
| [<span data-ttu-id="02a09-214">MF \_ transcode \_ QUALITYVSSPEED</span><span class="sxs-lookup"><span data-stu-id="02a09-214">MF\_TRANSCODE\_QUALITYVSSPEED</span></span>](mf-transcode-qualityvsspeed.md)               | <span data-ttu-id="02a09-215">Specifica il compromesso tra la qualità e la velocità di codifica.</span><span class="sxs-lookup"><span data-stu-id="02a09-215">Specifies the trade-off between encoding quality and speed.</span></span>                |



 

<span data-ttu-id="02a09-216">È necessario impostare gli attributi di formato.</span><span class="sxs-lookup"><span data-stu-id="02a09-216">You must set the format attributes.</span></span> <span data-ttu-id="02a09-217">I parametri di codifica sono facoltativi.</span><span class="sxs-lookup"><span data-stu-id="02a09-217">The encoding parameters are optional.</span></span>

### <a name="container-attributes"></a><span data-ttu-id="02a09-218">Attributi del contenitore</span><span class="sxs-lookup"><span data-stu-id="02a09-218">Container Attributes</span></span>

<span data-ttu-id="02a09-219">Gli attributi del contenitore definiscono le caratteristiche a livello di file del file di output.</span><span class="sxs-lookup"><span data-stu-id="02a09-219">Container attributes define file-level characteristics of the output file.</span></span> <span data-ttu-id="02a09-220">Per impostare gli attributi del contenitore, chiamare [**IMFTranscodeProfile:: SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes).</span><span class="sxs-lookup"><span data-stu-id="02a09-220">To set container attributes, call [**IMFTranscodeProfile::SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes).</span></span> <span data-ttu-id="02a09-221">Vengono definiti gli attributi seguenti.</span><span class="sxs-lookup"><span data-stu-id="02a09-221">The following attributes are defined.</span></span>



| <span data-ttu-id="02a09-222">Attributo</span><span class="sxs-lookup"><span data-stu-id="02a09-222">Attribute</span></span>                                                                          | <span data-ttu-id="02a09-223">Descrizione</span><span class="sxs-lookup"><span data-stu-id="02a09-223">Description</span></span>                                                                                                                                            |
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="02a09-224">MF \_ transcode \_ Adjust \_ profile</span><span class="sxs-lookup"><span data-stu-id="02a09-224">MF\_TRANSCODE\_ADJUST\_PROFILE</span></span>](mf-transcode-adjust-profile.md)                  | <span data-ttu-id="02a09-225">Definisce le impostazioni del flusso da utilizzare per la topologia transcodifica.</span><span class="sxs-lookup"><span data-stu-id="02a09-225">Defines the stream settings to use for the transcode topology.</span></span> <span data-ttu-id="02a09-226">È possibile impostare i flag per utilizzare le impostazioni di origine di input o utilizzare attributi di flusso personalizzati.</span><span class="sxs-lookup"><span data-stu-id="02a09-226">You can set the flags to use the input source settings or use custom stream attributes.</span></span> |
| [<span data-ttu-id="02a09-227">MF \_ transcode \_ CONTAINERTYPE</span><span class="sxs-lookup"><span data-stu-id="02a09-227">MF\_TRANSCODE\_CONTAINERTYPE</span></span>](mf-transcode-containertype.md)                     | <span data-ttu-id="02a09-228">Specifica il formato del file di output, ad esempio MP4 o ASF.</span><span class="sxs-lookup"><span data-stu-id="02a09-228">Specifies the file format of the output file, such as MP4 or ASF.</span></span> <span data-ttu-id="02a09-229">In base a questo valore, il sink multimediale appropriato viene aggiunto alla topologia.</span><span class="sxs-lookup"><span data-stu-id="02a09-229">Based on this value, the appropriate media sink is added to the topology.</span></span>            |
| [<span data-ttu-id="02a09-230">MF \_ transcode \_ Ignora \_ \_ trasferimento metadati</span><span class="sxs-lookup"><span data-stu-id="02a09-230">MF\_TRANSCODE\_SKIP\_METADATA\_TRANSFER</span></span>](mf-transcode-skip-metadata-transfer.md) | <span data-ttu-id="02a09-231">Specifica se i metadati dell'origine vengono copiati nel file di output.</span><span class="sxs-lookup"><span data-stu-id="02a09-231">Specifies whether metadata from the source is copied to the output file.</span></span>                                                                               |
| [<span data-ttu-id="02a09-232">MF \_ transcode \_ TOPOLOGYMODE</span><span class="sxs-lookup"><span data-stu-id="02a09-232">MF\_TRANSCODE\_TOPOLOGYMODE</span></span>](mf-transcode-topologymode.md)                       | <span data-ttu-id="02a09-233">Specifica se i codec basati su hardware possono essere utilizzati durante la transcodifica.</span><span class="sxs-lookup"><span data-stu-id="02a09-233">Specifies whether hardware-based codecs may be used during transcoding.</span></span>                                                                                |
| [<span data-ttu-id="02a09-234">\_Attributo di \_ sblocco \_ FIELDOFUSE MFT</span><span class="sxs-lookup"><span data-stu-id="02a09-234">MFT\_FIELDOFUSE\_UNLOCK\_Attribute</span></span>](mft-fieldofuse-unlock-attribute.md)          | <span data-ttu-id="02a09-235">Sblocca un codec con restrizioni di campo di utilizzo.</span><span class="sxs-lookup"><span data-stu-id="02a09-235">Unlocks a codec that has field-of-use restrictions.</span></span> <span data-ttu-id="02a09-236">Per ulteriori informazioni, vedere [restrizioni relative all'utilizzo dei campi](field-of-use-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="02a09-236">For more information, see [Field of Use Restrictions](field-of-use-restrictions.md).</span></span>              |



 

<span data-ttu-id="02a09-237">L'attributo [MF \_ transcode \_ CONTAINERTYPE](mf-transcode-containertype.md) è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="02a09-237">The [MF\_TRANSCODE\_CONTAINERTYPE](mf-transcode-containertype.md) attribute is required.</span></span> <span data-ttu-id="02a09-238">Gli altri attributi del contenitore sono facoltativi.</span><span class="sxs-lookup"><span data-stu-id="02a09-238">The other container attributes are optional.</span></span>

## <a name="creating-a-transcode-topology"></a><span data-ttu-id="02a09-239">Creazione di una topologia transcodifica</span><span class="sxs-lookup"><span data-stu-id="02a09-239">Creating a Transcode Topology</span></span>

<span data-ttu-id="02a09-240">La topologia transcodifica è una topologia parziale che contiene l'origine multimediale, i codec appropriati e il sink multimediale.</span><span class="sxs-lookup"><span data-stu-id="02a09-240">The transcode topology is a partial topology that contains the media source, the appropriate codecs, and the media sink.</span></span> <span data-ttu-id="02a09-241">Per creare la topologia transcode, chiamare la funzione [**MFCreateTranscodeTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) .</span><span class="sxs-lookup"><span data-stu-id="02a09-241">To create the transcode topology, call to the [**MFCreateTranscodeTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) function.</span></span> <span data-ttu-id="02a09-242">Questa funzione accetta come input i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="02a09-242">This function takes the following parameters as input:</span></span>

-   <span data-ttu-id="02a09-243">Puntatore all'interfaccia [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) dell'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="02a09-243">A pointer to the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) interface of the media source.</span></span>
-   <span data-ttu-id="02a09-244">Nome del file di output.</span><span class="sxs-lookup"><span data-stu-id="02a09-244">The name of the output file.</span></span>
-   <span data-ttu-id="02a09-245">Puntatore all'interfaccia [**IMFTranscodeProfile**](/windows/desktop/api/mfidl/nn-mfidl-imftranscodeprofile) del profilo transcodifica.</span><span class="sxs-lookup"><span data-stu-id="02a09-245">A pointer to the [**IMFTranscodeProfile**](/windows/desktop/api/mfidl/nn-mfidl-imftranscodeprofile) interface of the transcode profile.</span></span>

<span data-ttu-id="02a09-246">La funzione restituisce un puntatore all'interfaccia [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) .</span><span class="sxs-lookup"><span data-stu-id="02a09-246">The function returns a pointer to the [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) interface.</span></span>

## <a name="running-the-encoding-session"></a><span data-ttu-id="02a09-247">Esecuzione della sessione di codifica</span><span class="sxs-lookup"><span data-stu-id="02a09-247">Running the Encoding Session</span></span>

<span data-ttu-id="02a09-248">Dopo aver creato la topologia, si è pronti per codificare il file.</span><span class="sxs-lookup"><span data-stu-id="02a09-248">After you create the topology, you are ready to encode the file.</span></span> <span data-ttu-id="02a09-249">A questo punto è possibile rimuovere il profilo.</span><span class="sxs-lookup"><span data-stu-id="02a09-249">You can discard the profile at this point.</span></span>

1.  <span data-ttu-id="02a09-250">Chiamare [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) per creare la sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="02a09-250">Call [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) to create the Media Session.</span></span>
2.  <span data-ttu-id="02a09-251">Chiamare [**IMFMediaSession:: Setopologia**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) per impostare la topologia nella sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="02a09-251">Call [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) to set the topology on the Media Session.</span></span>
3.  <span data-ttu-id="02a09-252">Chiamare [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) per avviare la sessione di codifica.</span><span class="sxs-lookup"><span data-stu-id="02a09-252">Call [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) to start the encoding session.</span></span>
4.  <span data-ttu-id="02a09-253">Attendere l'evento [MESessionEnded](mesessionended.md) .</span><span class="sxs-lookup"><span data-stu-id="02a09-253">Wait for the [MESessionEnded](mesessionended.md) event.</span></span>
5.  <span data-ttu-id="02a09-254">Chiamare [**IMFMediaSession:: Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) per chiudere la sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="02a09-254">Call [**IMFMediaSession::Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) to close the Media Session.</span></span>
6.  <span data-ttu-id="02a09-255">Attendere l'evento [MESessionClosed](mesessionclosed.md) .</span><span class="sxs-lookup"><span data-stu-id="02a09-255">Wait for the [MESessionClosed](mesessionclosed.md) event.</span></span>
7.  <span data-ttu-id="02a09-256">Chiamare [**IMFMediaSource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown).</span><span class="sxs-lookup"><span data-stu-id="02a09-256">Call [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown).</span></span>
8.  <span data-ttu-id="02a09-257">Chiamare [**IMFMediaSession:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown).</span><span class="sxs-lookup"><span data-stu-id="02a09-257">Call [**IMFMediaSession::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown).</span></span>

<span data-ttu-id="02a09-258">La maggior parte del tempo impiegato per la codifica viene eseguita tra i passaggi 3 e 4.</span><span class="sxs-lookup"><span data-stu-id="02a09-258">Most of the time spent encoding occurs between steps 3 and 4.</span></span>

## <a name="related-topics"></a><span data-ttu-id="02a09-259">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="02a09-259">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02a09-260">API transcodifica</span><span class="sxs-lookup"><span data-stu-id="02a09-260">Transcode API</span></span>](transcode-api.md)
</dt> <dt>

[<span data-ttu-id="02a09-261">Informazioni sulla sessione multimediale</span><span class="sxs-lookup"><span data-stu-id="02a09-261">About the Media Session</span></span>](about-the-media-session.md)
</dt> </dl>

 

 



