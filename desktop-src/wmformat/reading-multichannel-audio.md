---
title: Lettura dell'audio multicanale
description: Lettura dell'audio multicanale
ms.assetid: 9d577c5c-7275-493e-8a77-318c264b59b3
keywords:
- Windows Media Format SDK, lettura di audio multicanale
- ASF (Advanced Systems Format), lettura di audio multicanale
- ASF (Advanced Systems Format), lettura di audio multicanale
- ASF (Advanced Systems Format), audio multicanale
- ASF (formato avanzato dei sistemi), audio multicanale
- codec, lettura di audio multicanale
- audio multicanale, lettura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59da950eb4218ad87995ed80e22de4de302f8e42
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729455"
---
# <a name="reading-multichannel-audio"></a><span data-ttu-id="e0743-110">Lettura dell'audio multicanale</span><span class="sxs-lookup"><span data-stu-id="e0743-110">Reading Multichannel Audio</span></span>

<span data-ttu-id="e0743-111">Il codec Windows Media Audio 9 Professional può codificare l'audio multicanale (più di due canali).</span><span class="sxs-lookup"><span data-stu-id="e0743-111">The Windows Media Audio 9 Professional codec can encode multichannel audio (more than two channels).</span></span> <span data-ttu-id="e0743-112">Quando si legge un file con audio multicanale, è necessario configurare correttamente l'output o l'audio verrà recapitato a una qualità inferiore e in stereo.</span><span class="sxs-lookup"><span data-stu-id="e0743-112">When reading a file with multichannel audio, you must configure the output properly or the audio will be delivered at a lower quality and in stereo.</span></span> <span data-ttu-id="e0743-113">Per impostare un output per il recapito audio multicanale, è necessario impostare due impostazioni di output: g \_ wszEnableDiscreteOutput e g \_ wszSpeakerConfig.</span><span class="sxs-lookup"><span data-stu-id="e0743-113">To set an output for multichannel audio delivery, you must set two output settings: g\_wszEnableDiscreteOutput and g\_wszSpeakerConfig.</span></span>

<span data-ttu-id="e0743-114">Impostando g \_ wszEnableDiscreteOutput su **true** , il codec viene impostato in modo da fornire un output audio ad alta definizione.</span><span class="sxs-lookup"><span data-stu-id="e0743-114">Setting g\_wszEnableDiscreteOutput to **TRUE** sets the codec to deliver high-definition audio output.</span></span> <span data-ttu-id="e0743-115">L'audio ad alta definizione è codificato dal codec Windows Media Audio 9 con esempi a 24 bit in stereo o più canali.</span><span class="sxs-lookup"><span data-stu-id="e0743-115">High-definition audio is encoded by the Windows Media Audio 9 codec with 24-bit samples in stereo or multiple channels.</span></span> <span data-ttu-id="e0743-116">Se questa impostazione è **false**, verrà recapitato solo l'output stereo a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="e0743-116">If this setting is **FALSE**, only 16-bit stereo output will be delivered.</span></span>

<span data-ttu-id="e0743-117">Il numero di altoparlanti nel computer di riproduzione è impostato con g \_ wszSpeakerConfig.</span><span class="sxs-lookup"><span data-stu-id="e0743-117">The number of speakers on the playing computer is set with g\_wszSpeakerConfig.</span></span> <span data-ttu-id="e0743-118">Questa impostazione è un valore **DWORD** impostato su una delle costanti del relatore DirectSound elencate nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="e0743-118">This setting is a **DWORD** value set to one of the DirectSound speaker constants listed in the following table.</span></span> <span data-ttu-id="e0743-119">Per risolvere questi nomi costanti per il compilatore, è necessario includere DSOUND. h.</span><span class="sxs-lookup"><span data-stu-id="e0743-119">To resolve these constant names for your compiler, you must include dsound.h.</span></span>



| <span data-ttu-id="e0743-120">Costante</span><span class="sxs-lookup"><span data-stu-id="e0743-120">Constant</span></span>             | <span data-ttu-id="e0743-121">Valore</span><span class="sxs-lookup"><span data-stu-id="e0743-121">Value</span></span>      | <span data-ttu-id="e0743-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e0743-122">Description</span></span>                                                                  |
|----------------------|------------|------------------------------------------------------------------------------|
| <span data-ttu-id="e0743-123">DSSPEAKER \_ diretto</span><span class="sxs-lookup"><span data-stu-id="e0743-123">DSSPEAKER\_DIRECTOUT</span></span> | <span data-ttu-id="e0743-124">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e0743-124">0x00000000</span></span> | <span data-ttu-id="e0743-125">L'audio viene passato direttamente, senza essere configurato per gli speaker.</span><span class="sxs-lookup"><span data-stu-id="e0743-125">The audio is passed through directly, without being configured for speakers.</span></span> |
| <span data-ttu-id="e0743-126">\_cuffia DSSPEAKER</span><span class="sxs-lookup"><span data-stu-id="e0743-126">DSSPEAKER\_HEADPHONE</span></span> | <span data-ttu-id="e0743-127">0x00000001</span><span class="sxs-lookup"><span data-stu-id="e0743-127">0x00000001</span></span> | <span data-ttu-id="e0743-128">Il computer client è dotato di cuffie.</span><span class="sxs-lookup"><span data-stu-id="e0743-128">The client computer is equipped with headphones.</span></span>                             |
| <span data-ttu-id="e0743-129">\_mono DSSPEAKER</span><span class="sxs-lookup"><span data-stu-id="e0743-129">DSSPEAKER\_MONO</span></span>      | <span data-ttu-id="e0743-130">0x00000002</span><span class="sxs-lookup"><span data-stu-id="e0743-130">0x00000002</span></span> | <span data-ttu-id="e0743-131">Il computer client è dotato di un altoparlante mono.</span><span class="sxs-lookup"><span data-stu-id="e0743-131">The client computer is equipped with a monaural speaker.</span></span>                     |
| <span data-ttu-id="e0743-132">DSSPEAKER \_ quad</span><span class="sxs-lookup"><span data-stu-id="e0743-132">DSSPEAKER\_QUAD</span></span>      | <span data-ttu-id="e0743-133">0x00000003</span><span class="sxs-lookup"><span data-stu-id="e0743-133">0x00000003</span></span> | <span data-ttu-id="e0743-134">Il computer client è dotato di altoparlanti quadrifonica.</span><span class="sxs-lookup"><span data-stu-id="e0743-134">The client computer is equipped with quadraphonic speakers.</span></span>                  |
| <span data-ttu-id="e0743-135">DSSPEAKER \_ stereo</span><span class="sxs-lookup"><span data-stu-id="e0743-135">DSSPEAKER\_STEREO</span></span>    | <span data-ttu-id="e0743-136">0x00000004</span><span class="sxs-lookup"><span data-stu-id="e0743-136">0x00000004</span></span> | <span data-ttu-id="e0743-137">Il computer client è dotato di altoparlanti stereo.</span><span class="sxs-lookup"><span data-stu-id="e0743-137">The client computer is equipped with stereo speakers.</span></span>                        |
| <span data-ttu-id="e0743-138">DSSPEAKER \_ surround</span><span class="sxs-lookup"><span data-stu-id="e0743-138">DSSPEAKER\_SURROUND</span></span>  | <span data-ttu-id="e0743-139">0x00000005</span><span class="sxs-lookup"><span data-stu-id="e0743-139">0x00000005</span></span> | <span data-ttu-id="e0743-140">Il computer client è dotato di altoparlanti con audio surround a quattro canali.</span><span class="sxs-lookup"><span data-stu-id="e0743-140">The client computer is equipped with four-channel surround-sound speakers.</span></span>   |
| <span data-ttu-id="e0743-141">\_5POINT1 DSSPEAKER</span><span class="sxs-lookup"><span data-stu-id="e0743-141">DSSPEAKER\_5POINT1</span></span>   | <span data-ttu-id="e0743-142">0x00000006</span><span class="sxs-lookup"><span data-stu-id="e0743-142">0x00000006</span></span> | <span data-ttu-id="e0743-143">Il computer client è dotato di cinque altoparlanti e un subwoofer.</span><span class="sxs-lookup"><span data-stu-id="e0743-143">The client computer is equipped with five speakers and a subwoofer.</span></span>          |
| <span data-ttu-id="e0743-144">\_7POINT1 DSSPEAKER</span><span class="sxs-lookup"><span data-stu-id="e0743-144">DSSPEAKER\_7POINT1</span></span>   | <span data-ttu-id="e0743-145">0x00000007</span><span class="sxs-lookup"><span data-stu-id="e0743-145">0x00000007</span></span> | <span data-ttu-id="e0743-146">Il computer client è dotato di sette altoparlanti e un subwoofer.</span><span class="sxs-lookup"><span data-stu-id="e0743-146">The client computer is equipped with seven speakers and a subwoofer.</span></span>         |



 

<span data-ttu-id="e0743-147">Per impostare queste impostazioni, utilizzare [**IWMReaderAdvanced2:: SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting).</span><span class="sxs-lookup"><span data-stu-id="e0743-147">To set these settings, use [**IWMReaderAdvanced2::SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting).</span></span>

<span data-ttu-id="e0743-148">Infine, affinché i canali vengano restituiti in modo discreto, senza riduzioni fino a stereo, è necessario impostare il tipo di supporto corretto nell'output attenendosi alla procedura seguente:</span><span class="sxs-lookup"><span data-stu-id="e0743-148">Finally, for the channels to be output discretely, with no fold-down to stereo, you must set the correct media type on the output by following these steps:</span></span>

1.  <span data-ttu-id="e0743-149">Chiamare [**IWMReader:: GetOutputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformatcount) per ottenere il numero di formati supportati per l'output audio pertinente.</span><span class="sxs-lookup"><span data-stu-id="e0743-149">Call [**IWMReader::GetOutputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformatcount) to get the number of supported formats for the relevant audio output.</span></span> <span data-ttu-id="e0743-150">Gli indici del formato di output sono in base zero.</span><span class="sxs-lookup"><span data-stu-id="e0743-150">Output format indexes are zero-based.</span></span>
2.  <span data-ttu-id="e0743-151">Per ogni formato supportato, chiamare [**IWMReader:: GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat) per recuperare l'interfaccia [**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) nell'oggetto proprietà del supporto di output.</span><span class="sxs-lookup"><span data-stu-id="e0743-151">For each supported format, call [**IWMReader::GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat) to retrieve the [**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) interface on the output media properties object.</span></span>
3.  <span data-ttu-id="e0743-152">Chiamare [**IWMMediaProps:: GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype) per recuperare il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="e0743-152">Call [**IWMMediaProps::GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype) to retrieve the media type.</span></span>
4.  <span data-ttu-id="e0743-153">Se il tipo di supporto recuperato è il tipo multicanale desiderato, impostarlo chiamando [**IWMReader:: SetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-setoutputprops).</span><span class="sxs-lookup"><span data-stu-id="e0743-153">If the retrieved media type is the desired multichannel type, then set it by calling [**IWMReader::SetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-setoutputprops).</span></span>

<span data-ttu-id="e0743-154">Dopo aver impostato l'output discreto e la configurazione dell'altoparlante, i formati di output enumerati dal lettore devono includere formati multicanale che usano la struttura [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd757721(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="e0743-154">After you have set discrete output and the speaker configuration, the output formats enumerated by the reader should include multichannel formats that use the [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd757721(v=vs.85)) structure.</span></span> <span data-ttu-id="e0743-155">Se si enumerano i formati di output prima di impostare le proprietà, verranno inclusi solo i formati con 1 o 2 canali e un massimo di 16 bit per canale.</span><span class="sxs-lookup"><span data-stu-id="e0743-155">If you enumerate the output formats before setting the properties, only formats with 1 or 2 channels and a maximum of 16 bits per channel will be included.</span></span> <span data-ttu-id="e0743-156">Come per gli altri formati audio, è consigliabile usare solo i formati enumerati dal lettore; non configurare il proprio.</span><span class="sxs-lookup"><span data-stu-id="e0743-156">As with other audio formats, you should use only the formats enumerated by the reader; do not configure your own.</span></span>

> [!Note]  
> <span data-ttu-id="e0743-157">È possibile generare l'audio multicanale solo se l'applicazione è in esecuzione in Microsoft Windows XP o in una versione successiva di Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="e0743-157">You can output multichannel audio only if your application is running on Microsoft Windows XP or a later version of Microsoft Windows.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="e0743-158">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e0743-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0743-159">**Input, flussi e output**</span><span class="sxs-lookup"><span data-stu-id="e0743-159">**Inputs, Streams and Outputs**</span></span>](inputs-streams-and-outputs.md)
</dt> <dt>

[<span data-ttu-id="e0743-160">**Lettura di file ASF**</span><span class="sxs-lookup"><span data-stu-id="e0743-160">**Reading ASF Files**</span></span>](reading-asf-files.md)
</dt> <dt>

[<span data-ttu-id="e0743-161">**Impostazioni di output**</span><span class="sxs-lookup"><span data-stu-id="e0743-161">**Output Settings**</span></span>](output-settings.md)
</dt> <dt>

[<span data-ttu-id="e0743-162">**Uso di High-Resolution audio PCM**</span><span class="sxs-lookup"><span data-stu-id="e0743-162">**Working with High-Resolution PCM Audio**</span></span>](working-with-high-resolution-pcm-audio.md)
</dt> </dl>

 

 