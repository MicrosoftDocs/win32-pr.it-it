---
title: Tipi di estensioni di esempio
description: Tipi di estensioni di esempio
ms.assetid: 8de2e003-cb21-4be9-bcde-7f5909b6260a
keywords:
- Windows Media Format SDK, estensioni di esempio
- ASF (Advanced Systems Format), estensioni di esempio
- ASF (formato avanzato dei sistemi), estensioni di esempio
- Windows Media Format SDK, estensioni di unità dati
- ASF (Advanced Systems Format), estensioni di unità dati
- ASF (formato di sistemi avanzati), estensioni di unità dati
- Windows Media Format SDK, proprietà del buffer
- ASF (Advanced Systems Format), proprietà del buffer
- ASF (formato avanzato dei sistemi), proprietà del buffer
- estensioni di esempio, tipi
- estensioni unità dati, tipi
- Proprietà buffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 972e3da1ecaad277158bb270cc358436f53db9e2
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/11/2020
ms.locfileid: "106299537"
---
# <a name="sample-extension-types"></a><span data-ttu-id="3b8a2-115">Tipi di estensioni di esempio</span><span class="sxs-lookup"><span data-stu-id="3b8a2-115">Sample Extension Types</span></span>

<span data-ttu-id="3b8a2-116">Le estensioni di esempio, denominate anche estensioni di unità dati (quote) o proprietà del buffer, sono elementi di dati allegati agli esempi di supporti nella sezione dati del file ASF.</span><span class="sxs-lookup"><span data-stu-id="3b8a2-116">Sample extensions, also called data unit extensions (DUEs) or buffer properties, are items of data that are attached to the media samples in the data section of the ASF file.</span></span> <span data-ttu-id="3b8a2-117">In Windows Media Format SDK sono definiti diversi tipi di estensioni di esempio.</span><span class="sxs-lookup"><span data-stu-id="3b8a2-117">Several types of sample extensions are defined in the Windows Media Format SDK.</span></span> <span data-ttu-id="3b8a2-118">È anche possibile creare i propri tipi di estensione.</span><span class="sxs-lookup"><span data-stu-id="3b8a2-118">You can also create your own extension types.</span></span>

<span data-ttu-id="3b8a2-119">Per usare le estensioni di esempio, è necessario identificare il tipo di estensione nei dati di configurazione del flusso del profilo.</span><span class="sxs-lookup"><span data-stu-id="3b8a2-119">To use sample extensions, you must identify the extension type in the stream configuration data of the profile.</span></span> <span data-ttu-id="3b8a2-120">Chiamare il metodo [**IWMStreamConfig2:: AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) per configurare un flusso in modo che accetti esempi con dati estesi.</span><span class="sxs-lookup"><span data-stu-id="3b8a2-120">Call the [**IWMStreamConfig2::AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) method to configure a stream to accept samples with extended data.</span></span>

<span data-ttu-id="3b8a2-121">È necessario aggiungere singole estensioni di esempio agli esempi di input chiamando il metodo [**INSSBuffer3:: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) .</span><span class="sxs-lookup"><span data-stu-id="3b8a2-121">Individual sample extensions must be added to the input samples by calling the [**INSSBuffer3::SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) method.</span></span> <span data-ttu-id="3b8a2-122">Quando si leggono gli esempi, è possibile chiamare il metodo [**INSSBuffer3:: GetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-getproperty) per recuperare i dati dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="3b8a2-122">When reading samples, you can call the [**INSSBuffer3::GetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-getproperty) method to retrieve the extension data.</span></span> <span data-ttu-id="3b8a2-123">È inoltre possibile utilizzare i metodi dell'interfaccia [**INSSBuffer4**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer4) per enumerare le estensioni dell'unità dati associate a un esempio.</span><span class="sxs-lookup"><span data-stu-id="3b8a2-123">You can also use the methods of the [**INSSBuffer4**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer4) interface to enumerate the data unit extensions attached to a sample.</span></span>

<span data-ttu-id="3b8a2-124">Nella tabella seguente sono elencati gli identificatori di estensione di unità dati predefiniti e vengono descritti i dati allegati agli esempi per ciascuno di essi.</span><span class="sxs-lookup"><span data-stu-id="3b8a2-124">The following table lists the predefined data unit extension identifiers, and describes the data that is attached to samples for each.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3b8a2-125">GUID dell'estensione di esempio</span><span class="sxs-lookup"><span data-stu-id="3b8a2-125">Sample extension GUID</span></span></th>
<th><span data-ttu-id="3b8a2-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3b8a2-126">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3b8a2-127">WM_SampleExtensionGUID_OutputCleanPoint</span><span class="sxs-lookup"><span data-stu-id="3b8a2-127">WM_SampleExtensionGUID_OutputCleanPoint</span></span></td>
<td><span data-ttu-id="3b8a2-128">I dati indicano se l'esempio è un <a href="wmformat-glossary.md"><em>cleanpoint</em></a>.</span><span class="sxs-lookup"><span data-stu-id="3b8a2-128">The data indicates whether the sample is a <a href="wmformat-glossary.md"><em>cleanpoint</em></a>.</span></span> <span data-ttu-id="3b8a2-129">Un valore pari a zero indica che l'esempio non è un cleanpoint.</span><span class="sxs-lookup"><span data-stu-id="3b8a2-129">A value of zero indicates that the sample is not a cleanpoint.</span></span> <span data-ttu-id="3b8a2-130">Un valore diverso da zero indica che si tratta di un cleanpoint.</span><span class="sxs-lookup"><span data-stu-id="3b8a2-130">A non-zero value indicates that it is a cleanpoint.</span></span> <span data-ttu-id="3b8a2-131">Questo tipo di estensione di unità dati di esempio viene usato per tenere traccia di cleanpoints durante la scrittura di flussi multimediali precompressi che sono stati codificati con codec di terze parti.</span><span class="sxs-lookup"><span data-stu-id="3b8a2-131">This sample data unit extension (DUE) type is used to keep track of cleanpoints when writing precompressed media streams that were encoded with third-party codecs.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3b8a2-132">WM_SampleExtensionGUID_Timecode</span><span class="sxs-lookup"><span data-stu-id="3b8a2-132">WM_SampleExtensionGUID_Timecode</span></span></td>
<td><span data-ttu-id="3b8a2-133">I dati sono una struttura di <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data"><strong>WMT_TIMECODE_EXTENSION_DATA</strong></a> contenente i dati del codice Time SMPTE associati all'esempio. Le dimensioni di questa operazione sono sempre WM_SampleExtension_Timecode_Size, ovvero 14 byte.</span><span class="sxs-lookup"><span data-stu-id="3b8a2-133">The data is a <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data"><strong>WMT_TIMECODE_EXTENSION_DATA</strong></a> structure containing SMPTE time code data associated with the sample.The size for this DUE is always WM_SampleExtension_Timecode_Size, which is 14 bytes.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3b8a2-134">WM_SampleExtensionGUID_FileName</span><span class="sxs-lookup"><span data-stu-id="3b8a2-134">WM_SampleExtensionGUID_FileName</span></span></td>
<td><span data-ttu-id="3b8a2-135">Questo tipo di estensione di esempio viene usato per i flussi di file.</span><span class="sxs-lookup"><span data-stu-id="3b8a2-135">This type of sample extension is used for file streams.</span></span> <span data-ttu-id="3b8a2-136">I dati in un esempio di flusso di file sono una parte di un file di dati.</span><span class="sxs-lookup"><span data-stu-id="3b8a2-136">The data in a file stream sample is a piece of a data file.</span></span> <span data-ttu-id="3b8a2-137">I dati nell'estensione di esempio specificano il nome del file da cui è stato utilizzato il contenuto del campione. Il nome del file è una stringa di caratteri wide contenente il nome del file in formato nome. estensione senza informazioni sul percorso.</span><span class="sxs-lookup"><span data-stu-id="3b8a2-137">The data in the sample extension specifies the name of the file from which the content in the sample was taken.The file name is a wide-character string containing the file name in name.extension format without any path information.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3b8a2-138">WM_SampleExtensionGUID_ContentType</span><span class="sxs-lookup"><span data-stu-id="3b8a2-138">WM_SampleExtensionGUID_ContentType</span></span></td>
<td><span data-ttu-id="3b8a2-139">I dati identificano il tipo di contenuto contenuto nell'esempio.</span><span class="sxs-lookup"><span data-stu-id="3b8a2-139">The data identifies the type of content that the sample contains.</span></span> <span data-ttu-id="3b8a2-140">Questo tipo di estensione di esempio viene usato con i flussi video interlacciati. Tutto il contenuto interlacciato usa il flag di WM_CT_INTERLACED combinato da <strong>un operatore OR</strong> bit per bit con WM_CT_BOTTOM_FIELD_FIRST, WM_CT_TOP_FIELD_FIRST o WM_CT_REPEAT_FIRST_FIELD.</span><span class="sxs-lookup"><span data-stu-id="3b8a2-140">This type of sample extension is used with interlaced video streams.All interlaced content uses the WM_CT_INTERLACED flag combined by a bitwise <strong>OR</strong> with either WM_CT_BOTTOM_FIELD_FIRST, WM_CT_TOP_FIELD_FIRST, or WM_CT_REPEAT_FIRST_FIELD.</span></span><br/> <span data-ttu-id="3b8a2-141">L'ordine dei campi non viene utilizzato nel processo di codifica, ma viene mantenuto con gli esempi compressi, in modo che possa essere passato all'hardware di rendering.</span><span class="sxs-lookup"><span data-stu-id="3b8a2-141">The field order is not used in the encoding process, but is maintained with the compressed samples so that it can be passed to the rendering hardware.</span></span> <span data-ttu-id="3b8a2-142">La riproduzione di contenuto interlacciato con l'ordine dei campi errato introduce elementi come l'instabilità del movimento nel video.</span><span class="sxs-lookup"><span data-stu-id="3b8a2-142">Playing interlaced content with the incorrect field order introduces artifacts such as motion jitter in the video.</span></span><br/> <span data-ttu-id="3b8a2-143">Le dimensioni di questa operazione sono sempre WM_SampleExtension_ContentType_Size.</span><span class="sxs-lookup"><span data-stu-id="3b8a2-143">The size for this DUE is always WM_SampleExtension_ContentType_Size.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3b8a2-144">WM_SampleExtensionGUID_PixelAspectRatio</span><span class="sxs-lookup"><span data-stu-id="3b8a2-144">WM_SampleExtensionGUID_PixelAspectRatio</span></span></td>
<td><span data-ttu-id="3b8a2-145">I dati indicano le proporzioni in pixel del contenuto nell'esempio.</span><span class="sxs-lookup"><span data-stu-id="3b8a2-145">The data indicates the pixel aspect ratio of the content in the sample.</span></span> <span data-ttu-id="3b8a2-146">Questo vale solo per i video. Questo tipo di estensione viene utilizzato per identificare le proporzioni dei pixel non quadrati.</span><span class="sxs-lookup"><span data-stu-id="3b8a2-146">This applies only to video.This extension type is used to identify the aspect ratio of non-square pixels.</span></span> <span data-ttu-id="3b8a2-147">Per altre informazioni, vedere <a href="to-read-and-write-video-streams-with-non-square-pixels.md">per leggere e scrivere flussi video con pixel non quadrati</a>.</span><span class="sxs-lookup"><span data-stu-id="3b8a2-147">For more information, see <a href="to-read-and-write-video-streams-with-non-square-pixels.md">To Read and Write Video Streams with Non-Square Pixels</a>.</span></span><br/> <span data-ttu-id="3b8a2-148">I valori delle proporzioni vengono archiviati come una parola il cui byte minimo è l'aspetto X e il cui byte elevato è l'aspetto Y.</span><span class="sxs-lookup"><span data-stu-id="3b8a2-148">Aspect ratio values are stored as a word whose low byte is the X aspect and whose high byte is the Y aspect.</span></span> <span data-ttu-id="3b8a2-149">Ad esempio, 16:9 viene archiviato come 0x0910.</span><span class="sxs-lookup"><span data-stu-id="3b8a2-149">For example, 16:9 is stored as 0x0910.</span></span><br/> <span data-ttu-id="3b8a2-150">Le dimensioni di questa operazione sono sempre WM_SampleExtension_PixelAspectRatio_Size, ovvero 2 byte.</span><span class="sxs-lookup"><span data-stu-id="3b8a2-150">The size for this DUE is always WM_SampleExtension_PixelAspectRatio_Size, which is 2 bytes.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3b8a2-151">WM_SampleExtensionGUID_SampleDuration</span><span class="sxs-lookup"><span data-stu-id="3b8a2-151">WM_SampleExtensionGUID_SampleDuration</span></span></td>
<td><span data-ttu-id="3b8a2-152">I dati indicano la durata, in millisecondi, dell'esempio contenuto nell'oggetto buffer.</span><span class="sxs-lookup"><span data-stu-id="3b8a2-152">The data indicates the duration, in milliseconds, of the sample contained in the buffer object.</span></span> <span data-ttu-id="3b8a2-153">In caso di riproduzione, se il valore è impostato, l'oggetto Reader lo userà per sovrascrivere il valore di durata campione esistente. Questa causa viene impostata automaticamente dai componenti di Runtime SDK sui flussi video con velocità in bit di 100 kbps o superiore, in cui il sovraccarico delle informazioni non è significativo.</span><span class="sxs-lookup"><span data-stu-id="3b8a2-153">On playback, if this DUE is set the reader object will use it to overwrite the existing sample duration value.This DUE is set automatically by the SDK run-time components on video streams with bit rates of 100 kbps or greater, where the overhead of the DUE information is not significant.</span></span> <span data-ttu-id="3b8a2-154">Non è impostato per i flussi con velocità in bit inferiore a 100 kbps.</span><span class="sxs-lookup"><span data-stu-id="3b8a2-154">It is not set for streams with bit rates under 100 kbps.</span></span> <span data-ttu-id="3b8a2-155">Poiché il writer (nei flussi a velocità elevata) sovrascriverà il valore con i propri dati, le applicazioni non devono impostare questa funzione.</span><span class="sxs-lookup"><span data-stu-id="3b8a2-155">Applications should not set this DUE manually because the writer (on high-bit-rate streams) will overwrite the value with its own data.</span></span><br/> <span data-ttu-id="3b8a2-156">Le dimensioni di questa operazione sono sempre WM_SampleExtension_SampleDuration_Size, ovvero 2 byte.</span><span class="sxs-lookup"><span data-stu-id="3b8a2-156">The size for this DUE is always WM_SampleExtension_SampleDuration_Size, which is 2 bytes.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3b8a2-157">WM_SampleExtensionGUID_ChromaLocation</span><span class="sxs-lookup"><span data-stu-id="3b8a2-157">WM_SampleExtensionGUID_ChromaLocation</span></span></td>
<td><span data-ttu-id="3b8a2-158">I dati indicano il tipo di sottocampionamento Chroma usato nel formato video I420. Il valore di questa estensione è impostato su uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="3b8a2-158">The data indicates the type of chroma subsampling used in the I420 video format.The value of this extension is set to one of the follow values:</span></span><br/>
<ul>
<li><span data-ttu-id="3b8a2-159">WM_CL_INTERLACED420</span><span class="sxs-lookup"><span data-stu-id="3b8a2-159">WM_CL_INTERLACED420</span></span></li>
<li><span data-ttu-id="3b8a2-160">WM_CL_PROGRESSIVE420</span><span class="sxs-lookup"><span data-stu-id="3b8a2-160">WM_CL_PROGRESSIVE420</span></span></li>
</ul>
<span data-ttu-id="3b8a2-161">Questa estensione di unità dati non è configurata nel profilo.</span><span class="sxs-lookup"><span data-stu-id="3b8a2-161">This data unit extension is not configured in the profile.</span></span> <span data-ttu-id="3b8a2-162">È incluso nell'output degli esempi dal decodificatore.</span><span class="sxs-lookup"><span data-stu-id="3b8a2-162">It is included in samples output from the decoder.</span></span><br/> <span data-ttu-id="3b8a2-163">La dimensione di questa operazione è sempre WM_SampleExtension_ChromaLocation_Size, ovvero 1 byte.</span><span class="sxs-lookup"><span data-stu-id="3b8a2-163">The size of this DUE is always WM_SampleExtension_ChromaLocation_Size, which is 1 byte.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3b8a2-164">WM_SampleExtensionGUID_ColorSpaceInfo</span><span class="sxs-lookup"><span data-stu-id="3b8a2-164">WM_SampleExtensionGUID_ColorSpaceInfo</span></span></td>
<td><span data-ttu-id="3b8a2-165">I dati forniscono informazioni sullo spazio di colore usato per il frame video corrente. Il valore di questa estensione è una struttura <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_colorspaceinfo_extension_data"><strong>WMT_COLORSPACEINFO_EXTENSION_DATA</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="3b8a2-165">The data provides information about the color space used for the current video frame.The value of this extension is a <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_colorspaceinfo_extension_data"><strong>WMT_COLORSPACEINFO_EXTENSION_DATA</strong></a> structure.</span></span><br/> <span data-ttu-id="3b8a2-166">Questa estensione di unità dati non è configurata nel profilo.</span><span class="sxs-lookup"><span data-stu-id="3b8a2-166">This data unit extension is not configured in the profile.</span></span> <span data-ttu-id="3b8a2-167">È incluso nell'output degli esempi dal decodificatore.</span><span class="sxs-lookup"><span data-stu-id="3b8a2-167">It is included in samples output from the decoder.</span></span><br/> <span data-ttu-id="3b8a2-168">La dimensione di questa operazione è sempre WM_SampleExtension_ColorSpaceInfo_Size, ovvero 3 byte.</span><span class="sxs-lookup"><span data-stu-id="3b8a2-168">The size of this DUE is always WM_SampleExtension_ColorSpaceInfo_Size, which is 3 bytes.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3b8a2-169">WM_SampleExtensionGUID_UserDataInfo</span><span class="sxs-lookup"><span data-stu-id="3b8a2-169">WM_SampleExtensionGUID_UserDataInfo</span></span></td>
<td><span data-ttu-id="3b8a2-170">I dati sono dati utente personalizzati. I primi quattro byte dei dati contengono la dimensione dei dati personalizzati.</span><span class="sxs-lookup"><span data-stu-id="3b8a2-170">The data is custom user data.The first four bytes of the data contain the size of the custom data.</span></span><br/> <span data-ttu-id="3b8a2-171">Il byte successivo contiene il tipo di dati utente specificati nell'estensione di esempio.</span><span class="sxs-lookup"><span data-stu-id="3b8a2-171">The next byte contains the type of user data provided in the sample extension.</span></span> <span data-ttu-id="3b8a2-172">Sono supportati i tipi seguenti:</span><span class="sxs-lookup"><span data-stu-id="3b8a2-172">The following types are supported:</span></span><br/>
<ul>
<li><span data-ttu-id="3b8a2-173">0x1F-dati utente a livello di sequenza</span><span class="sxs-lookup"><span data-stu-id="3b8a2-173">0x1F - Sequence level user data</span></span></li>
<li><span data-ttu-id="3b8a2-174">0x1E-dati utente a livello di punto di ingresso</span><span class="sxs-lookup"><span data-stu-id="3b8a2-174">0x1E - Entry-point level user data</span></span></li>
<li><span data-ttu-id="3b8a2-175">0x1D-dati utente a livello di frame</span><span class="sxs-lookup"><span data-stu-id="3b8a2-175">0x1D - Frame level user data</span></span></li>
<li><span data-ttu-id="3b8a2-176">0x1C-dati utente a livello di campo</span><span class="sxs-lookup"><span data-stu-id="3b8a2-176">0x1C - Field level user data</span></span></li>
<li><span data-ttu-id="3b8a2-177">0x1B-dati utente a livello di sezione</span><span class="sxs-lookup"><span data-stu-id="3b8a2-177">0x1B - Slice level user data</span></span></li>
</ul>
<span data-ttu-id="3b8a2-178">Il sesto e i byte successivi contengono i dati dell'utente.</span><span class="sxs-lookup"><span data-stu-id="3b8a2-178">The sixth and subsequent bytes contain the user data.</span></span> <span data-ttu-id="3b8a2-179">Sono presenti molti byte di dati utente specificati dal numero nei primi quattro byte.</span><span class="sxs-lookup"><span data-stu-id="3b8a2-179">There are as many bytes of user data as specified by the number in the first four bytes.</span></span><br/> <span data-ttu-id="3b8a2-180">Questa estensione di unità dati non è configurata nel profilo.</span><span class="sxs-lookup"><span data-stu-id="3b8a2-180">This data unit extension is not configured in the profile.</span></span> <span data-ttu-id="3b8a2-181">È incluso negli esempi di output del decodificatore.</span><span class="sxs-lookup"><span data-stu-id="3b8a2-181">It is included in samples that are output from the decoder.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3b8a2-182">WM_SampleExtensionGUID_SampleProtectionSalt</span><span class="sxs-lookup"><span data-stu-id="3b8a2-182">WM_SampleExtensionGUID_SampleProtectionSalt</span></span></td>
<td><span data-ttu-id="3b8a2-183">I dati vengono crittografati in base all'esempio.</span><span class="sxs-lookup"><span data-stu-id="3b8a2-183">The data is encrypted by sample.</span></span> <span data-ttu-id="3b8a2-184">Questo tipo di estensione di esempio viene utilizzato per il contenuto importato da un formato di file non ASF e uno schema di protezione dei diritti diverso da Windows Media DRM. Quando si importa contenuto protetto, ogni esempio deve includere un valore salt univoco.</span><span class="sxs-lookup"><span data-stu-id="3b8a2-184">This sample extension type is used for content that is imported from a non-ASF file format and a rights protection scheme other than Windows Media DRM.When importing protected content, each sample must include a unique salt.</span></span> <span data-ttu-id="3b8a2-185">In genere, questo valore è un contatore a incremento progressivo costante.</span><span class="sxs-lookup"><span data-stu-id="3b8a2-185">Typically, this value is a monotonically increasing counter.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="3b8a2-186">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3b8a2-186">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b8a2-187">**Guida di riferimento alla programmazione**</span><span class="sxs-lookup"><span data-stu-id="3b8a2-187">**Programming Reference**</span></span>](programming-reference.md)
</dt> </dl>

 

 





