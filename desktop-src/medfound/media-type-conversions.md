---
description: Conversioni di tipi di supporto
ms.assetid: 6aee18b8-79b1-47fb-816f-d1c2c77b3a03
title: Conversioni di tipi di supporto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee3a72e74439251f9661e0ff27166c504e47c238
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "103761465"
---
# <a name="media-type-conversions"></a><span data-ttu-id="0191e-103">Conversioni di tipi di supporto</span><span class="sxs-lookup"><span data-stu-id="0191e-103">Media Type Conversions</span></span>

<span data-ttu-id="0191e-104">In alcuni casi è necessario eseguire la conversione tra Media Foundation tipi di supporto e le strutture di tipo multimediale precedenti da DirectShow o Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="0191e-104">Occasionally it is necessary to convert between Media Foundation media types and the older media type structures from DirectShow or the Windows Media Format SDK.</span></span>

### <a name="from-a-format-structure-to-a-media-foundation-type"></a><span data-ttu-id="0191e-105">Da una struttura di formato a un tipo di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0191e-105">From a Format Structure to a Media Foundation Type</span></span>

<span data-ttu-id="0191e-106">Le funzioni seguenti inizializzano un Media Foundation tipo di supporto da una struttura di formato.</span><span class="sxs-lookup"><span data-stu-id="0191e-106">The following functions initialize a Media Foundation media type from a format structure.</span></span> <span data-ttu-id="0191e-107">Queste funzioni sono utili anche se un flusso di dati o un'intestazione di file contiene una struttura di formato.</span><span class="sxs-lookup"><span data-stu-id="0191e-107">These functions are also useful if a data stream or a file header contains a format structure.</span></span> <span data-ttu-id="0191e-108">L'intestazione di file per i file audio WAVE, ad esempio, contiene una struttura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="0191e-108">For example, the file header for WAVE audio files contains a [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0191e-109">Struttura da convertire</span><span class="sxs-lookup"><span data-stu-id="0191e-109">Structure to Convert</span></span></th>
<th><span data-ttu-id="0191e-110">Funzione</span><span class="sxs-lookup"><span data-stu-id="0191e-110">Function</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0191e-111"><a href="/windows/win32/api/strmif/ns-strmif-am_media_type"><strong>AM_MEDIA_TYPE</strong></a> (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="0191e-111"><a href="/windows/win32/api/strmif/ns-strmif-am_media_type"><strong>AM_MEDIA_TYPE</strong></a> (DirectShow)</span></span><br/> <span data-ttu-id="0191e-112"><a href="/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type"><strong>DMO_MEDIA_TYPE</strong></a> (oggetti multimediali DirectX)</span><span class="sxs-lookup"><span data-stu-id="0191e-112"><a href="/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type"><strong>DMO_MEDIA_TYPE</strong></a> (DirectX Media Objects)</span></span> <br/> <span data-ttu-id="0191e-113"><a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type"><strong>WM_MEDIA_TYPE</strong></a> (Windows Media Format SDK)</span><span class="sxs-lookup"><span data-stu-id="0191e-113"><a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type"><strong>WM_MEDIA_TYPE</strong></a> (Windows Media Format SDK)</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="0191e-114">Queste strutture sono equivalenti.</span><span class="sxs-lookup"><span data-stu-id="0191e-114">These structures are equivalent.</span></span>
</blockquote>
<br/> <br/></td>
<td><span data-ttu-id="0191e-115"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromammediatype"><strong>MFInitMediaTypeFromAMMediaType</strong></a></span><span class="sxs-lookup"><span data-stu-id="0191e-115"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromammediatype"><strong>MFInitMediaTypeFromAMMediaType</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0191e-116"><a href="/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader"><strong>BITMAPINFOHEADER</strong></a></span><span class="sxs-lookup"><span data-stu-id="0191e-116"><a href="/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader"><strong>BITMAPINFOHEADER</strong></a></span></span></td>
<td><span data-ttu-id="0191e-117"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreatevideomediatypefrombitmapinfoheaderex"><strong>MFCreateVideoMediaTypeFromBitMapInfoHeaderEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="0191e-117"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreatevideomediatypefrombitmapinfoheaderex"><strong>MFCreateVideoMediaTypeFromBitMapInfoHeaderEx</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0191e-118"><a href="/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat"><strong>MFVIDEOFORMAT</strong></a></span><span class="sxs-lookup"><span data-stu-id="0191e-118"><a href="/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat"><strong>MFVIDEOFORMAT</strong></a></span></span></td>
<td><span data-ttu-id="0191e-119"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefrommfvideoformat"><strong>MFInitMediaTypeFromMFVideoFormat</strong></a></span><span class="sxs-lookup"><span data-stu-id="0191e-119"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefrommfvideoformat"><strong>MFInitMediaTypeFromMFVideoFormat</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0191e-120"><a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo"><strong>MPEG1VIDEOINFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="0191e-120"><a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo"><strong>MPEG1VIDEOINFO</strong></a></span></span></td>
<td><span data-ttu-id="0191e-121"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefrommpeg1videoinfo"><strong>MFInitMediaTypeFromMPEG1VideoInfo</strong></a></span><span class="sxs-lookup"><span data-stu-id="0191e-121"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefrommpeg1videoinfo"><strong>MFInitMediaTypeFromMPEG1VideoInfo</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0191e-122"><a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo"><strong>MPEG2VIDEOINFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="0191e-122"><a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo"><strong>MPEG2VIDEOINFO</strong></a></span></span></td>
<td><span data-ttu-id="0191e-123"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefrommpeg2videoinfo"><strong>MFInitMediaTypeFromMPEG2VideoInfo</strong></a></span><span class="sxs-lookup"><span data-stu-id="0191e-123"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefrommpeg2videoinfo"><strong>MFInitMediaTypeFromMPEG2VideoInfo</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0191e-124"><a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2"><strong>VIDEOINFOHEADER2</strong></a></span><span class="sxs-lookup"><span data-stu-id="0191e-124"><a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2"><strong>VIDEOINFOHEADER2</strong></a></span></span></td>
<td><span data-ttu-id="0191e-125"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromvideoinfoheader2"><strong>MFInitMediaTypeFromVideoInfoHeader2</strong></a></span><span class="sxs-lookup"><span data-stu-id="0191e-125"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromvideoinfoheader2"><strong>MFInitMediaTypeFromVideoInfoHeader2</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0191e-126"><a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader"><strong>VIDEOINFOHEADER</strong></a></span><span class="sxs-lookup"><span data-stu-id="0191e-126"><a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader"><strong>VIDEOINFOHEADER</strong></a></span></span></td>
<td><span data-ttu-id="0191e-127"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromvideoinfoheader"><strong>MFInitMediaTypeFromVideoInfoHeader</strong></a></span><span class="sxs-lookup"><span data-stu-id="0191e-127"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromvideoinfoheader"><strong>MFInitMediaTypeFromVideoInfoHeader</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0191e-128"><a href="/previous-versions/dd757713(v=vs.85)"><strong>WAVEFORMATEX</strong></a> o <a href="/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)"> <strong>WAVEFORMATEXTENSIBLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="0191e-128"><a href="/previous-versions/dd757713(v=vs.85)"><strong>WAVEFORMATEX</strong></a> or <a href="/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)"><strong>WAVEFORMATEXTENSIBLE</strong></a></span></span></td>
<td><span data-ttu-id="0191e-129"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex"><strong>MFInitMediaTypeFromWaveFormatEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="0191e-129"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex"><strong>MFInitMediaTypeFromWaveFormatEx</strong></a></span></span></td>
</tr>
</tbody>
</table>



 

### <a name="from-a-media-foundation-type-to-a-format-structure"></a><span data-ttu-id="0191e-130">Da un tipo di Media Foundation a una struttura di formato</span><span class="sxs-lookup"><span data-stu-id="0191e-130">From a Media Foundation Type to a Format Structure</span></span>

<span data-ttu-id="0191e-131">Le funzioni seguenti creano o inizializzano una struttura di formato da un tipo di supporto Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="0191e-131">The following functions create or initialize a format structure from a Media Foundation media type.</span></span>



| <span data-ttu-id="0191e-132">Funzione</span><span class="sxs-lookup"><span data-stu-id="0191e-132">Function</span></span>                                                                             | <span data-ttu-id="0191e-133">Struttura di destinazione</span><span class="sxs-lookup"><span data-stu-id="0191e-133">Target Structure</span></span>                                                                                                                                                                    |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0191e-134">**IMFMediaType:: getrappresentation**</span><span class="sxs-lookup"><span data-stu-id="0191e-134">**IMFMediaType::GetRepresentation**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getrepresentation)            | <span data-ttu-id="0191e-135">[**Am \_ MEDIA \_ Type**](/windows/win32/api/strmif/ns-strmif-am_media_type), [**MFVIDEOFORMAT**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat), [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)o [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2)</span><span class="sxs-lookup"><span data-stu-id="0191e-135">[**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type), [**MFVIDEOFORMAT**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat), [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader), or [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2)</span></span> |
| [<span data-ttu-id="0191e-136">**MFCreateAMMediaTypeFromMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="0191e-136">**MFCreateAMMediaTypeFromMFMediaType**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfcreateammediatypefrommfmediatype)     | [<span data-ttu-id="0191e-137">**\_tipo di supporto am \_**</span><span class="sxs-lookup"><span data-stu-id="0191e-137">**AM\_MEDIA\_TYPE**</span></span>](/windows/win32/api/strmif/ns-strmif-am_media_type)                                                                                                                                          |
| [<span data-ttu-id="0191e-138">**MFCreateMFVideoFormatFromMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="0191e-138">**MFCreateMFVideoFormatFromMFMediaType**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemfvideoformatfrommfmediatype) | [<span data-ttu-id="0191e-139">**MFVIDEOFORMAT**</span><span class="sxs-lookup"><span data-stu-id="0191e-139">**MFVIDEOFORMAT**</span></span>](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat)                                                                                                                                              |
| [<span data-ttu-id="0191e-140">**MFCreateWaveFormatExFromMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="0191e-140">**MFCreateWaveFormatExFromMFMediaType**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfcreatewaveformatexfrommfmediatype)   | <span data-ttu-id="0191e-141">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) o [ **WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0191e-141">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) or [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85))</span></span>                                                                                    |
| [<span data-ttu-id="0191e-142">**MFInitAMMediaTypeFromMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="0191e-142">**MFInitAMMediaTypeFromMFMediaType**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfinitammediatypefrommfmediatype)         | [<span data-ttu-id="0191e-143">**\_tipo di supporto am \_**</span><span class="sxs-lookup"><span data-stu-id="0191e-143">**AM\_MEDIA\_TYPE**</span></span>](/windows/win32/api/strmif/ns-strmif-am_media_type)                                                                                                                                          |



 

## <a name="format-mappings"></a><span data-ttu-id="0191e-144">Mapping del formato</span><span class="sxs-lookup"><span data-stu-id="0191e-144">Format Mappings</span></span>

<span data-ttu-id="0191e-145">Nelle tabelle seguenti sono elencati gli attributi Media Foundation che corrispondono a diverse strutture di formato.</span><span class="sxs-lookup"><span data-stu-id="0191e-145">The following tables list the Media Foundation attributes that correspond to various format structures.</span></span> <span data-ttu-id="0191e-146">Non tutti questi attributi possono essere tradotti direttamente.</span><span class="sxs-lookup"><span data-stu-id="0191e-146">Not all of these attributes can be translated directly.</span></span> <span data-ttu-id="0191e-147">Per eseguire le conversioni, è necessario usare le funzioni elencate nella sezione precedente. Queste tabelle vengono fornite principalmente per riferimento.</span><span class="sxs-lookup"><span data-stu-id="0191e-147">To perform conversions, you should use the functions listed in the previous section; these tables are provided mainly for reference.</span></span>

### <a name="am_media_type"></a><span data-ttu-id="0191e-148">\_tipo di supporto am \_</span><span class="sxs-lookup"><span data-stu-id="0191e-148">AM\_MEDIA\_TYPE</span></span>



| <span data-ttu-id="0191e-149">Membro</span><span class="sxs-lookup"><span data-stu-id="0191e-149">Member</span></span>                   | <span data-ttu-id="0191e-150">Attributo</span><span class="sxs-lookup"><span data-stu-id="0191e-150">Attribute</span></span>                                                                            |
|--------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0191e-151">**bTemporalCompression**</span><span class="sxs-lookup"><span data-stu-id="0191e-151">**bTemporalCompression**</span></span> | [<span data-ttu-id="0191e-152">**\_ \_ tutti gli esempi MF mt \_ \_ Independent**</span><span class="sxs-lookup"><span data-stu-id="0191e-152">**MF\_MT\_ALL\_SAMPLES\_INDEPENDENT**</span></span>](mf-mt-all-samples-independent-attribute.md) |
| <span data-ttu-id="0191e-153">**bFixedSizeSamples**</span><span class="sxs-lookup"><span data-stu-id="0191e-153">**bFixedSizeSamples**</span></span>    | [<span data-ttu-id="0191e-154">**\_esempi di \_ \_ dimensioni fisse MF mt \_**</span><span class="sxs-lookup"><span data-stu-id="0191e-154">**MF\_MT\_FIXED\_SIZE\_SAMPLES**</span></span>](mf-mt-fixed-size-samples-attribute.md)           |
| <span data-ttu-id="0191e-155">**lSampleSize**</span><span class="sxs-lookup"><span data-stu-id="0191e-155">**lSampleSize**</span></span>          | [<span data-ttu-id="0191e-156">**\_ \_ dimensioni campione MF \_ mt**</span><span class="sxs-lookup"><span data-stu-id="0191e-156">**MF\_MT\_SAMPLE\_SIZE**</span></span>](mf-mt-sample-size-attribute.md)                          |



 

### <a name="waveformatex-waveformatextensible"></a><span data-ttu-id="0191e-157">WAVEFORMATEX, WAVEFORMATEXTENSIBLE</span><span class="sxs-lookup"><span data-stu-id="0191e-157">WAVEFORMATEX, WAVEFORMATEXTENSIBLE</span></span>



| <span data-ttu-id="0191e-158">Membro</span><span class="sxs-lookup"><span data-stu-id="0191e-158">Member</span></span>                  | <span data-ttu-id="0191e-159">Attributo</span><span class="sxs-lookup"><span data-stu-id="0191e-159">Attribute</span></span>                                                                                                                                                                 |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0191e-160">**wFormatTag**</span><span class="sxs-lookup"><span data-stu-id="0191e-160">**wFormatTag**</span></span>          | [<span data-ttu-id="0191e-161">**sottotipo MF \_ mt \_**</span><span class="sxs-lookup"><span data-stu-id="0191e-161">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)<br/> <span data-ttu-id="0191e-162">Se **wFormatTag** è \_ Extensible Format WAVE \_ , il sottotipo viene trovato nel membro **subformat** .</span><span class="sxs-lookup"><span data-stu-id="0191e-162">If **wFormatTag** is WAVE\_FORMAT\_EXTENSIBLE, the subtype is found in the **SubFormat** member.</span></span><br/> |
| <span data-ttu-id="0191e-163">**nChannels**</span><span class="sxs-lookup"><span data-stu-id="0191e-163">**nChannels**</span></span>           | [<span data-ttu-id="0191e-164">**numero \_ di \_ \_ canali audio MF mt \_**</span><span class="sxs-lookup"><span data-stu-id="0191e-164">**MF\_MT\_AUDIO\_NUM\_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)                                                                                                |
| <span data-ttu-id="0191e-165">**nSamplesPerSec**</span><span class="sxs-lookup"><span data-stu-id="0191e-165">**nSamplesPerSec**</span></span>      | [<span data-ttu-id="0191e-166">**\_ \_ campioni audio MF \_ mt \_ al \_ secondo**</span><span class="sxs-lookup"><span data-stu-id="0191e-166">**MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md)                                                                                   |
| <span data-ttu-id="0191e-167">**nAvgBytesPerSec**</span><span class="sxs-lookup"><span data-stu-id="0191e-167">**nAvgBytesPerSec**</span></span>     | [<span data-ttu-id="0191e-168">**\_ \_ Media byte audio MF mt \_ \_ \_ al \_ secondo**</span><span class="sxs-lookup"><span data-stu-id="0191e-168">**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md)                                                                              |
| <span data-ttu-id="0191e-169">**nBlockAlign**</span><span class="sxs-lookup"><span data-stu-id="0191e-169">**nBlockAlign**</span></span>         | [<span data-ttu-id="0191e-170">**\_ \_ \_ allineamento blocchi audio MF \_ mt**</span><span class="sxs-lookup"><span data-stu-id="0191e-170">**MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT**</span></span>](mf-mt-audio-block-alignment-attribute.md)                                                                                          |
| <span data-ttu-id="0191e-171">**wBitsPerSample**</span><span class="sxs-lookup"><span data-stu-id="0191e-171">**wBitsPerSample**</span></span>      | [<span data-ttu-id="0191e-172">**\_ \_ bit audio MF \_ mt \_ per \_ campione**</span><span class="sxs-lookup"><span data-stu-id="0191e-172">**MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE**</span></span>](mf-mt-audio-bits-per-sample-attribute.md)                                                                                         |
| <span data-ttu-id="0191e-173">**wValidBitsPerSample**</span><span class="sxs-lookup"><span data-stu-id="0191e-173">**wValidBitsPerSample**</span></span> | [<span data-ttu-id="0191e-174">**\_ \_ bit validi per l'audio MF mt \_ \_ \_ per \_ campione**</span><span class="sxs-lookup"><span data-stu-id="0191e-174">**MF\_MT\_AUDIO\_VALID\_BITS\_PER\_SAMPLE**</span></span>](mf-mt-audio-valid-bits-per-sample-attribute.md)                                                                            |
| <span data-ttu-id="0191e-175">**wSamplesPerBlock**</span><span class="sxs-lookup"><span data-stu-id="0191e-175">**wSamplesPerBlock**</span></span>    | [<span data-ttu-id="0191e-176">**\_ \_ campioni audio MF \_ mt \_ per \_ blocco**</span><span class="sxs-lookup"><span data-stu-id="0191e-176">**MF\_MT\_AUDIO\_SAMPLES\_PER\_BLOCK**</span></span>](mf-mt-audio-samples-per-block-attribute.md)                                                                                     |
| <span data-ttu-id="0191e-177">**dwChannelMask**</span><span class="sxs-lookup"><span data-stu-id="0191e-177">**dwChannelMask**</span></span>       | [<span data-ttu-id="0191e-178">**\_ \_ \_ maschera canale audio MF \_ mt**</span><span class="sxs-lookup"><span data-stu-id="0191e-178">**MF\_MT\_AUDIO\_CHANNEL\_MASK**</span></span>](mf-mt-audio-channel-mask-attribute.md)                                                                                                |
| <span data-ttu-id="0191e-179">**Sottoformati**</span><span class="sxs-lookup"><span data-stu-id="0191e-179">**SubFormat**</span></span>           | [<span data-ttu-id="0191e-180">**sottotipo MF \_ mt \_**</span><span class="sxs-lookup"><span data-stu-id="0191e-180">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                                                                                                        |
| <span data-ttu-id="0191e-181">Dati aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="0191e-181">Extra data</span></span>              | [<span data-ttu-id="0191e-182">**\_ \_ dati utente MF \_ mt**</span><span class="sxs-lookup"><span data-stu-id="0191e-182">**MF\_MT\_USER\_DATA**</span></span>](mf-mt-user-data-attribute.md)                                                                                                                   |



 

### <a name="videoinfoheader-videoinfoheader2"></a><span data-ttu-id="0191e-183">VIDEOINFOHEADER, VIDEOINFOHEADER2</span><span class="sxs-lookup"><span data-stu-id="0191e-183">VIDEOINFOHEADER, VIDEOINFOHEADER2</span></span>



| <span data-ttu-id="0191e-184">Membro</span><span class="sxs-lookup"><span data-stu-id="0191e-184">Member</span></span>                                         | <span data-ttu-id="0191e-185">Attributo</span><span class="sxs-lookup"><span data-stu-id="0191e-185">Attribute</span></span>                                                                                                                                                                                                                                        |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0191e-186">**dwBitRate**</span><span class="sxs-lookup"><span data-stu-id="0191e-186">**dwBitRate**</span></span>                                  | [<span data-ttu-id="0191e-187">**\_velocità in \_ bit media MF mt \_**</span><span class="sxs-lookup"><span data-stu-id="0191e-187">**MF\_MT\_AVG\_BITRATE**</span></span>](mf-mt-avg-bitrate-attribute.md)                                                                                                                                                                                      |
| <span data-ttu-id="0191e-188">**dwBitErrorRate**</span><span class="sxs-lookup"><span data-stu-id="0191e-188">**dwBitErrorRate**</span></span>                             | [<span data-ttu-id="0191e-189">**\_frequenza di \_ \_ errori bit \_ medio \_ MF mt**</span><span class="sxs-lookup"><span data-stu-id="0191e-189">**MF\_MT\_AVG\_BIT\_ERROR\_RATE**</span></span>](mf-mt-avg-bit-error-rate-attribute.md)                                                                                                                                                                      |
| <span data-ttu-id="0191e-190">**AvgTimePerFrame**</span><span class="sxs-lookup"><span data-stu-id="0191e-190">**AvgTimePerFrame**</span></span>                            | <span data-ttu-id="0191e-191">[**MF \_ \_ \_ Frequenza fotogrammi mt**](mf-mt-frame-rate-attribute.md); usare [**MFAverageTimePerFrameToFrameRate**](/windows/desktop/api/mfapi/nf-mfapi-mfaveragetimeperframetoframerate) per calcolare questo valore.</span><span class="sxs-lookup"><span data-stu-id="0191e-191">[**MF\_MT\_FRAME\_RATE**](mf-mt-frame-rate-attribute.md); use [**MFAverageTimePerFrameToFrameRate**](/windows/desktop/api/mfapi/nf-mfapi-mfaveragetimeperframetoframerate) to calculate this value.</span></span>                                                                             |
| <span data-ttu-id="0191e-192">**dwInterlaceFlags**</span><span class="sxs-lookup"><span data-stu-id="0191e-192">**dwInterlaceFlags**</span></span>                           | [<span data-ttu-id="0191e-193">**\_modalità di \_ intreccio MF mt \_**</span><span class="sxs-lookup"><span data-stu-id="0191e-193">**MF\_MT\_INTERLACE\_MODE**</span></span>](mf-mt-interlace-mode-attribute.md)                                                                                                                                                                                |
| <span data-ttu-id="0191e-194">**dwCopyProtectFlags**</span><span class="sxs-lookup"><span data-stu-id="0191e-194">**dwCopyProtectFlags**</span></span>                         | <span data-ttu-id="0191e-195">Nessun equivalente definito</span><span class="sxs-lookup"><span data-stu-id="0191e-195">No defined equivalent</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="0191e-196">**dwPictAspectRatioX**, **dwPictAspectRatioY**</span><span class="sxs-lookup"><span data-stu-id="0191e-196">**dwPictAspectRatioX**, **dwPictAspectRatioY**</span></span> | <span data-ttu-id="0191e-197">[**MF \_ Proporzioni MT \_ pixel \_ \_**](mf-mt-pixel-aspect-ratio-attribute.md); è necessario convertire le proporzioni dell'immagine in proporzioni dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="0191e-197">[**MF\_MT\_PIXEL\_ASPECT\_RATIO**](mf-mt-pixel-aspect-ratio-attribute.md); must convert from picture aspect ratio to picture aspect ratio.</span></span>                                                                                                      |
| <span data-ttu-id="0191e-198">**dwControlFlags**</span><span class="sxs-lookup"><span data-stu-id="0191e-198">**dwControlFlags**</span></span>                             | <span data-ttu-id="0191e-199">[**MF \_ \_flag di \_ controllo \_ del pad mt**](mf-mt-pad-control-flags-attribute.md).</span><span class="sxs-lookup"><span data-stu-id="0191e-199">[**MF\_MT\_PAD\_CONTROL\_FLAGS**](mf-mt-pad-control-flags-attribute.md).</span></span> <span data-ttu-id="0191e-200">Se è presente il flag **AMCONTROL \_ COLORINFO \_ present** , impostare gli attributi di colore esteso descritti in [informazioni estese sui colori](extended-color-information.md).</span><span class="sxs-lookup"><span data-stu-id="0191e-200">If the **AMCONTROL\_COLORINFO\_PRESENT** flag is present, set the extended color attributes described in [Extended Color Information](extended-color-information.md).</span></span> |
| <span data-ttu-id="0191e-201">**bmiHeader. biWidth**, **BmiHeader. biHeight**</span><span class="sxs-lookup"><span data-stu-id="0191e-201">**bmiHeader.biWidth**, **bmiHeader.biHeight**</span></span>  | [<span data-ttu-id="0191e-202">**\_dimensioni del \_ frame MF mt \_**</span><span class="sxs-lookup"><span data-stu-id="0191e-202">**MF\_MT\_FRAME\_SIZE**</span></span>](mf-mt-frame-size-attribute.md)                                                                                                                                                                                        |
| <span data-ttu-id="0191e-203">**bmiHeader.biBitCount**</span><span class="sxs-lookup"><span data-stu-id="0191e-203">**bmiHeader.biBitCount**</span></span>                       | <span data-ttu-id="0191e-204">Implicito nel sottotipo ([**\_ \_ sottotipo MF mt**](mf-mt-subtype-attribute.md)).</span><span class="sxs-lookup"><span data-stu-id="0191e-204">Implicit in the subtype ([**MF\_MT\_SUBTYPE**](mf-mt-subtype-attribute.md)).</span></span>                                                                                                                                                                    |
| <span data-ttu-id="0191e-205">**bmiHeader. biCompression**</span><span class="sxs-lookup"><span data-stu-id="0191e-205">**bmiHeader.biCompression**</span></span>                    | <span data-ttu-id="0191e-206">Implicito nel sottotipo.</span><span class="sxs-lookup"><span data-stu-id="0191e-206">Implicit in the subtype.</span></span>                                                                                                                                                                                                                         |
| <span data-ttu-id="0191e-207">**bmiHeader.biSizeImage**</span><span class="sxs-lookup"><span data-stu-id="0191e-207">**bmiHeader.biSizeImage**</span></span>                      | [<span data-ttu-id="0191e-208">**\_ \_ dimensioni campione MF \_ mt**</span><span class="sxs-lookup"><span data-stu-id="0191e-208">**MF\_MT\_SAMPLE\_SIZE**</span></span>](mf-mt-sample-size-attribute.md)                                                                                                                                                                                      |
| <span data-ttu-id="0191e-209">Informazioni tavolozza</span><span class="sxs-lookup"><span data-stu-id="0191e-209">Palette information</span></span>                            | [<span data-ttu-id="0191e-210">**\_ \_ tavolozza MF mt**</span><span class="sxs-lookup"><span data-stu-id="0191e-210">**MF\_MT\_PALETTE**</span></span>](mf-mt-palette-attribute.md)                                                                                                                                                                                               |



 

<span data-ttu-id="0191e-211">Gli attributi seguenti possono essere dedotti dalla struttura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) o [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) , ma richiedono anche una certa conoscenza dei dettagli del formato.</span><span class="sxs-lookup"><span data-stu-id="0191e-211">The following attributes can be inferred from the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) or [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) structure but also require some knowledge of the format details.</span></span> <span data-ttu-id="0191e-212">Ad esempio, diversi formati YUV hanno requisiti di stride diversi.</span><span class="sxs-lookup"><span data-stu-id="0191e-212">For example, different YUV formats have different stride requirements.</span></span>

-   [<span data-ttu-id="0191e-213">**\_ \_ stride predefinito MF \_ mt**</span><span class="sxs-lookup"><span data-stu-id="0191e-213">**MF\_MT\_DEFAULT\_STRIDE**</span></span>](mf-mt-default-stride-attribute.md)
-   [<span data-ttu-id="0191e-214">**\_ \_ \_ apertura minima schermo \_ MF mt**</span><span class="sxs-lookup"><span data-stu-id="0191e-214">**MF\_MT\_MINIMUM\_DISPLAY\_APERTURE**</span></span>](mf-mt-minimum-display-aperture-attribute.md)
-   [<span data-ttu-id="0191e-215">**\_apertura dell' \_ analisi della panoramica MF mt \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0191e-215">**MF\_MT\_PAN\_SCAN\_APERTURE**</span></span>](mf-mt-pan-scan-aperture-attribute.md)

### <a name="mpeg1videoinfo"></a><span data-ttu-id="0191e-216">MPEG1VIDEOINFO</span><span class="sxs-lookup"><span data-stu-id="0191e-216">MPEG1VIDEOINFO</span></span>



| <span data-ttu-id="0191e-217">Membro</span><span class="sxs-lookup"><span data-stu-id="0191e-217">Member</span></span>                                   | <span data-ttu-id="0191e-218">Attributo</span><span class="sxs-lookup"><span data-stu-id="0191e-218">Attribute</span></span>                                                                       |
|------------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="0191e-219">**dwStartTimeCode**</span><span class="sxs-lookup"><span data-stu-id="0191e-219">**dwStartTimeCode**</span></span>                      | [<span data-ttu-id="0191e-220">**\_ \_ \_ codice ora di inizio \_ MF mt MPEG \_**</span><span class="sxs-lookup"><span data-stu-id="0191e-220">**MF\_MT\_MPEG\_START\_TIME\_CODE**</span></span>](mf-mt-mpeg-start-time-code-attribute.md) |
| <span data-ttu-id="0191e-221">**bSequenceHeader**</span><span class="sxs-lookup"><span data-stu-id="0191e-221">**bSequenceHeader**</span></span>                      | [<span data-ttu-id="0191e-222">**\_intestazione della sequenza MF mt \_ MPEG \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0191e-222">**MF\_MT\_MPEG\_SEQUENCE\_HEADER**</span></span>](mf-mt-mpeg-sequence-header-attribute.md)  |
| <span data-ttu-id="0191e-223">**biXPelsPerMeter**, **biYPelsPerMeter**</span><span class="sxs-lookup"><span data-stu-id="0191e-223">**biXPelsPerMeter**, **biYPelsPerMeter**</span></span> | [<span data-ttu-id="0191e-224">**proporzioni MF \_ mt \_ pixel \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0191e-224">**MF\_MT\_PIXEL\_ASPECT\_RATIO**</span></span>](mf-mt-pixel-aspect-ratio-attribute.md)      |



 

### <a name="mpeg2videoinfo"></a><span data-ttu-id="0191e-225">MPEG2VIDEOINFO</span><span class="sxs-lookup"><span data-stu-id="0191e-225">MPEG2VIDEOINFO</span></span>



| <span data-ttu-id="0191e-226">Membro</span><span class="sxs-lookup"><span data-stu-id="0191e-226">Member</span></span>               | <span data-ttu-id="0191e-227">Attributo</span><span class="sxs-lookup"><span data-stu-id="0191e-227">Attribute</span></span>                                                                       |
|----------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="0191e-228">**dwStartTimeCode**</span><span class="sxs-lookup"><span data-stu-id="0191e-228">**dwStartTimeCode**</span></span>  | [<span data-ttu-id="0191e-229">**\_ \_ \_ codice ora di inizio \_ MF mt MPEG \_**</span><span class="sxs-lookup"><span data-stu-id="0191e-229">**MF\_MT\_MPEG\_START\_TIME\_CODE**</span></span>](mf-mt-mpeg-start-time-code-attribute.md) |
| <span data-ttu-id="0191e-230">**dwSequenceHeader**</span><span class="sxs-lookup"><span data-stu-id="0191e-230">**dwSequenceHeader**</span></span> | [<span data-ttu-id="0191e-231">**\_intestazione della sequenza MF mt \_ MPEG \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0191e-231">**MF\_MT\_MPEG\_SEQUENCE\_HEADER**</span></span>](mf-mt-mpeg-sequence-header-attribute.md)  |
| <span data-ttu-id="0191e-232">**dwProfile**</span><span class="sxs-lookup"><span data-stu-id="0191e-232">**dwProfile**</span></span>        | [<span data-ttu-id="0191e-233">**\_ \_ Profilo MPEG2 MF \_ mt**</span><span class="sxs-lookup"><span data-stu-id="0191e-233">**MF\_MT\_MPEG2\_PROFILE**</span></span>](mf-mt-mpeg2-profile-attribute.md)                 |
| <span data-ttu-id="0191e-234">**dwLevel**</span><span class="sxs-lookup"><span data-stu-id="0191e-234">**dwLevel**</span></span>          | [<span data-ttu-id="0191e-235">**\_ \_ Livello MPEG2 MF \_ mt**</span><span class="sxs-lookup"><span data-stu-id="0191e-235">**MF\_MT\_MPEG2\_LEVEL**</span></span>](mf-mt-mpeg2-level-attribute.md)                     |
| <span data-ttu-id="0191e-236">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="0191e-236">**dwFlags**</span></span>          | [<span data-ttu-id="0191e-237">**\_ \_ Flag MPEG2 MF \_ mt**</span><span class="sxs-lookup"><span data-stu-id="0191e-237">**MF\_MT\_MPEG2\_FLAGS**</span></span>](mf-mt-mpeg2-flags-attribute.md)                     |



 

## <a name="examples"></a><span data-ttu-id="0191e-238">Esempio</span><span class="sxs-lookup"><span data-stu-id="0191e-238">Examples</span></span>

<span data-ttu-id="0191e-239">Il codice seguente compila una struttura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) da un tipo di supporto video.</span><span class="sxs-lookup"><span data-stu-id="0191e-239">The following code fills in a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure from a video media type.</span></span> <span data-ttu-id="0191e-240">Si noti che questa conversione perde alcune informazioni sul formato (interlacciamento, frequenza dei fotogrammi, dati di colore estesi).</span><span class="sxs-lookup"><span data-stu-id="0191e-240">Note that this conversions loses some of the format information (interlacing, frame rate, extended color data).</span></span> <span data-ttu-id="0191e-241">Tuttavia, potrebbe essere utile quando si salva una bitmap da un frame video, ad esempio.</span><span class="sxs-lookup"><span data-stu-id="0191e-241">However, it might be useful when saving a bitmap from a video frame, for example.</span></span>


```C++
#include <dshow.h>
#include <dvdmedia.h>

// Converts a video type to a BITMAPINFO structure.
// The caller must free the structure by calling CoTaskMemFree.

// Note that this conversion loses some format information, including 
// interlacing, and frame rate.

HRESULT GetBitmapInfoHeaderFromMFMediaType(
    IMFMediaType *pType,            // Pointer to the media type.
    BITMAPINFOHEADER **ppBmih,      // Receives a pointer to the structure. 
    DWORD *pcbSize)                 // Receives the size of the structure.
{
    *ppBmih = NULL;
    *pcbSize = 0;

    GUID majorType = GUID_NULL;
    AM_MEDIA_TYPE *pmt = NULL;
    DWORD cbSize = 0;
    DWORD cbOffset = 0;
    BITMAPINFOHEADER *pBMIH = NULL;

    // Verify that this is a video type.
    HRESULT hr = pType->GetMajorType(&majorType);
    if (FAILED(hr))
    {
        goto done;
    }

    if (majorType != MFMediaType_Video)
    {
        hr = MF_E_INVALIDMEDIATYPE;
        goto done;
    }

    hr = pType->GetRepresentation(AM_MEDIA_TYPE_REPRESENTATION, (void**)&pmt);
    if (FAILED(hr))
    {
        goto done;
    }

    if (pmt->formattype == FORMAT_VideoInfo)
    {
        cbOffset = (FIELD_OFFSET(VIDEOINFOHEADER,bmiHeader));
    }
    else if (pmt->formattype == FORMAT_VideoInfo2)
    {
        cbOffset = (FIELD_OFFSET(VIDEOINFOHEADER2,bmiHeader));
    }
    else
    {
        hr = MF_E_INVALIDMEDIATYPE; // Unsupported format type.
        goto done;
    }

    if (pmt->cbFormat - cbOffset < sizeof(BITMAPINFOHEADER))
    {
        hr = E_UNEXPECTED; // Bad format size. 
        goto done;
    }

    cbSize = pmt->cbFormat - cbOffset;

    pBMIH = (BITMAPINFOHEADER*)CoTaskMemAlloc(cbSize);
    if (pBMIH == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }
    
    CopyMemory(pBMIH, pmt->pbFormat + cbOffset, cbSize);
    
    *ppBmih = pBMIH;
    *pcbSize = cbSize;

done:
    if (pmt)
    {
        pType->FreeRepresentation(AM_MEDIA_TYPE_REPRESENTATION, pmt);
    }
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="0191e-242">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0191e-242">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0191e-243">Tipi di supporto</span><span class="sxs-lookup"><span data-stu-id="0191e-243">Media Types</span></span>](media-types.md)
</dt> </dl>

 

 
