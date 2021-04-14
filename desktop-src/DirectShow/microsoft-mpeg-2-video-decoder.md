---
description: Questo filtro decodifica il video MPEG-1, MPEG-2, H. 264.
ms.assetid: d8195c3a-97ac-4ad1-a097-18878c8fda6f
title: Decodificatore video Microsoft MPEG-2 (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8460b5b554fffc8f0dd8679810e5ef3f42bcb004
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401113"
---
# <a name="microsoft-mpeg-2-video-decoder"></a><span data-ttu-id="a91d7-103">Decoder video Microsoft MPEG-2</span><span class="sxs-lookup"><span data-stu-id="a91d7-103">Microsoft MPEG-2 Video Decoder</span></span>

<span data-ttu-id="a91d7-104">Questo filtro decodifica il video MPEG-1, MPEG-2, H. 264.</span><span class="sxs-lookup"><span data-stu-id="a91d7-104">This filter decodes MPEG-1, MPEG-2, H.264 video.</span></span>

> [!Note]  
> <span data-ttu-id="a91d7-105">La decodifica del video H. 264 richiede Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a91d7-105">Decoding of H.264 video requires Windows 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="a91d7-106">Questo filtro non è supportato nelle piattaforme basate su IA-64.</span><span class="sxs-lookup"><span data-stu-id="a91d7-106">This filter is not supported on IA-64-based platforms.</span></span>

 

<span data-ttu-id="a91d7-107">Nel registro di sistema il nome descrittivo di questo filtro è "Microsoft DTV-DVD video decoder".</span><span class="sxs-lookup"><span data-stu-id="a91d7-107">In the registry, the friendly name of this filter is "Microsoft DTV-DVD Video Decoder".</span></span>



<span data-ttu-id="a91d7-108">Informazioni sul filtro</span><span class="sxs-lookup"><span data-stu-id="a91d7-108">Filter Information</span></span>

<span data-ttu-id="a91d7-109">Interfacce di filtro</span><span class="sxs-lookup"><span data-stu-id="a91d7-109">Filter Interfaces</span></span>

[<span data-ttu-id="a91d7-110">**IAMDecoderCaps**</span><span class="sxs-lookup"><span data-stu-id="a91d7-110">**IAMDecoderCaps**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamdecodercaps)<br/> [<span data-ttu-id="a91d7-111">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="a91d7-111">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/> [<span data-ttu-id="a91d7-112">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="a91d7-112">**ICodecAPI**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/>

<span data-ttu-id="a91d7-113">Tipi di supporti pin di input</span><span class="sxs-lookup"><span data-stu-id="a91d7-113">Input Pin Media Types</span></span>

<span data-ttu-id="a91d7-114">Pin di input video:</span><span class="sxs-lookup"><span data-stu-id="a91d7-114">Video input pin:</span></span>

-   <span data-ttu-id="a91d7-115">MEDIATYPE \_ DVD \_ Encrypted \_ Pack, \_ video MEDIASUBTYPE MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="a91d7-115">MEDIATYPE\_DVD\_ENCRYPTED\_PACK, MEDIASUBTYPE\_MPEG2\_VIDEO</span></span>
-   <span data-ttu-id="a91d7-116">MEDIATYPE \_ MPEG2 \_ PE, \_ video MEDIASUBTYPE MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="a91d7-116">MEDIATYPE\_MPEG2\_PES, MEDIASUBTYPE\_MPEG2\_VIDEO</span></span>
-   <span data-ttu-id="a91d7-117">\_Video di MEDIATYPE, MEDIASUBTYPE \_ MPEG1Packet</span><span class="sxs-lookup"><span data-stu-id="a91d7-117">MEDIATYPE\_Video, MEDIASUBTYPE\_MPEG1Packet</span></span>
-   <span data-ttu-id="a91d7-118">\_Video di MEDIATYPE, MEDIASUBTYPE \_ MPEG1Payload</span><span class="sxs-lookup"><span data-stu-id="a91d7-118">MEDIATYPE\_Video, MEDIASUBTYPE\_MPEG1Payload</span></span>
-   <span data-ttu-id="a91d7-119">Video \_ di MEDIATYPE, \_ video di MEDIASUBTYPE MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="a91d7-119">MEDIATYPE\_Video, MEDIASUBTYPE\_MPEG2\_VIDEO</span></span>

<span data-ttu-id="a91d7-120">Pin di input della sottoimmagine:</span><span class="sxs-lookup"><span data-stu-id="a91d7-120">Subpicture input pin:</span></span><br/>

-   <span data-ttu-id="a91d7-121">MEDIATYPE \_ DVD \_ Encrypted \_ Pack, \_ \_ sottoimmagine DVD MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="a91d7-121">MEDIATYPE\_DVD\_ENCRYPTED\_PACK, MEDIASUBTYPE\_DVD\_SUBPICTURE</span></span>

<span data-ttu-id="a91d7-122">A partire da Windows 7, il pin di input video supporta anche i tipi di input seguenti:</span><span class="sxs-lookup"><span data-stu-id="a91d7-122">Starting in Windows 7, the video input pin also supports the following input types:</span></span><br/>

-   <span data-ttu-id="a91d7-123">**MEDIATYPE \_ Video**, **MEDIASUBTYPE \_ AVC1**</span><span class="sxs-lookup"><span data-stu-id="a91d7-123">**MEDIATYPE\_Video**, **MEDIASUBTYPE\_AVC1**</span></span>
-   <span data-ttu-id="a91d7-124">**MEDIATYPE \_ Video**, **MEDIASUBTYPE \_ H264**</span><span class="sxs-lookup"><span data-stu-id="a91d7-124">**MEDIATYPE\_Video**, **MEDIASUBTYPE\_H264**</span></span>
-   <span data-ttu-id="a91d7-125">**MEDIATYPE \_ Video**, **MEDIASUBTYPE \_ H264**</span><span class="sxs-lookup"><span data-stu-id="a91d7-125">**MEDIATYPE\_Video**, **MEDIASUBTYPE\_h264**</span></span>
-   <span data-ttu-id="a91d7-126">**MEDIATYPE \_ Video**, **MEDIASUBTYPE \_ x264**</span><span class="sxs-lookup"><span data-stu-id="a91d7-126">**MEDIATYPE\_Video**, **MEDIASUBTYPE\_X264**</span></span>
-   <span data-ttu-id="a91d7-127">**MEDIATYPE \_ Video**, **MEDIASUBTYPE \_ x264**</span><span class="sxs-lookup"><span data-stu-id="a91d7-127">**MEDIATYPE\_Video**, **MEDIASUBTYPE\_x264**</span></span>

<span data-ttu-id="a91d7-128">Per ulteriori informazioni, vedere i [tipi di video H. 264](h-264-video-types.md) .</span><span class="sxs-lookup"><span data-stu-id="a91d7-128">See [H.264 Video Types](h-264-video-types.md) for more information.</span></span> <span data-ttu-id="a91d7-129">Il tipo di supporto di input può variare in modo dinamico tra i tipi MPEG2 e H. 264.</span><span class="sxs-lookup"><span data-stu-id="a91d7-129">The input media type can change dynamically between MPEG2 and H.264 types.</span></span><br/>

<span data-ttu-id="a91d7-130">Interfacce pin di input</span><span class="sxs-lookup"><span data-stu-id="a91d7-130">Input Pin Interfaces</span></span>

[<span data-ttu-id="a91d7-131">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="a91d7-131">**ICodecAPI**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/> [<span data-ttu-id="a91d7-132">**IKsPropertySet**</span><span class="sxs-lookup"><span data-stu-id="a91d7-132">**IKsPropertySet**</span></span>](ikspropertyset.md)<br/> [<span data-ttu-id="a91d7-133">**IMemInputPin**</span><span class="sxs-lookup"><span data-stu-id="a91d7-133">**IMemInputPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [<span data-ttu-id="a91d7-134">**IMFSampleProtection**</span><span class="sxs-lookup"><span data-stu-id="a91d7-134">**IMFSampleProtection**</span></span>](/windows/win32/api/mfidl/nn-mfidl-imfsampleprotection)<br/> [<span data-ttu-id="a91d7-135">**IPin**</span><span class="sxs-lookup"><span data-stu-id="a91d7-135">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [<span data-ttu-id="a91d7-136">**IQualityControl**</span><span class="sxs-lookup"><span data-stu-id="a91d7-136">**IQualityControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

<span data-ttu-id="a91d7-137">Tipi di supporti pin di output</span><span class="sxs-lookup"><span data-stu-id="a91d7-137">Output Pin Media Types</span></span>

<span data-ttu-id="a91d7-138">Pin di output del video:</span><span class="sxs-lookup"><span data-stu-id="a91d7-138">Video output pin:</span></span>

-   <span data-ttu-id="a91d7-139">MEDIATYPE \_ video, DXVA \_ ModeMPEG2 \_ A (DXVA 1,0)</span><span class="sxs-lookup"><span data-stu-id="a91d7-139">MEDIATYPE\_Video, DXVA\_ModeMPEG2\_A (DXVA 1.0)</span></span>
-   <span data-ttu-id="a91d7-140">MEDIATYPE \_ video, DXVA \_ ModeMPEG2 \_ C (DXVA 1,0)</span><span class="sxs-lookup"><span data-stu-id="a91d7-140">MEDIATYPE\_Video, DXVA\_ModeMPEG2\_C (DXVA 1.0)</span></span>
-   <span data-ttu-id="a91d7-141">\_Video di MEDIATYPE, MEDIASUBTYPE \_ I420 (decodifica software o DXVA 2.0)</span><span class="sxs-lookup"><span data-stu-id="a91d7-141">MEDIATYPE\_Video, MEDIASUBTYPE\_I420 (Software decode or DXVA2.0)</span></span>
-   <span data-ttu-id="a91d7-142">\_Video di MEDIATYPE, MEDIASUBTYPE \_ NV12 (decodifica software o DXVA 2.0)</span><span class="sxs-lookup"><span data-stu-id="a91d7-142">MEDIATYPE\_Video, MEDIASUBTYPE\_NV12 (Software decode or DXVA2.0)</span></span>
-   <span data-ttu-id="a91d7-143">\_Video di MEDIATYPE, MEDIASUBTYPE \_ YUY2 (decodifica software o DXVA 2.0)</span><span class="sxs-lookup"><span data-stu-id="a91d7-143">MEDIATYPE\_Video, MEDIASUBTYPE\_YUY2 (Software decode or DXVA2.0)</span></span>
-   <span data-ttu-id="a91d7-144">MEDIATYPE \_ video, MEDIASUBTYPE \_ IMC3 (solo DXVA 2.0)</span><span class="sxs-lookup"><span data-stu-id="a91d7-144">MEDIATYPE\_Video, MEDIASUBTYPE\_IMC3 (DXVA2.0 only)</span></span>
-   <span data-ttu-id="a91d7-145">MEDIATYPE \_ video, MEDIASUBTYPE \_ IMC4 (solo DXVA 2.0)</span><span class="sxs-lookup"><span data-stu-id="a91d7-145">MEDIATYPE\_Video, MEDIASUBTYPE\_IMC4 (DXVA2.0 only)</span></span>
-   <span data-ttu-id="a91d7-146">MEDIATYPE \_ video, MEDIASUBTYPE \_ S340 (solo DXVA 2.0)</span><span class="sxs-lookup"><span data-stu-id="a91d7-146">MEDIATYPE\_Video, MEDIASUBTYPE\_S340 (DXVA2.0 only)</span></span>
-   <span data-ttu-id="a91d7-147">MEDIATYPE \_ video, MEDIASUBTYPE \_ YV12 (solo DXVA 2.0)</span><span class="sxs-lookup"><span data-stu-id="a91d7-147">MEDIATYPE\_Video, MEDIASUBTYPE\_YV12 (DXVA2.0 only)</span></span>

<span data-ttu-id="a91d7-148">Pin di output riga 21:</span><span class="sxs-lookup"><span data-stu-id="a91d7-148">Line-21 output pin:</span></span><br/>

-   <span data-ttu-id="a91d7-149">MEDIATYPE \_ AUXLine21Data, MEDIASUBTYPE \_ Line21 \_ GOPPacket</span><span class="sxs-lookup"><span data-stu-id="a91d7-149">MEDIATYPE\_AUXLine21Data, MEDIASUBTYPE\_Line21\_GOPPacket</span></span>

<span data-ttu-id="a91d7-150">Pin di output della sottoimmagine:</span><span class="sxs-lookup"><span data-stu-id="a91d7-150">Subpicture output pin:</span></span><br/>

-   <span data-ttu-id="a91d7-151">\_Video di MEDIATYPE, MEDIASUBTYPE \_ AI44</span><span class="sxs-lookup"><span data-stu-id="a91d7-151">MEDIATYPE\_Video, MEDIASUBTYPE\_AI44</span></span>
-   <span data-ttu-id="a91d7-152">\_Video di MEDIATYPE, MEDIASUBTYPE \_ ARGB32</span><span class="sxs-lookup"><span data-stu-id="a91d7-152">MEDIATYPE\_Video, MEDIASUBTYPE\_ARGB32</span></span>
-   <span data-ttu-id="a91d7-153">\_Video di MEDIATYPE, MEDIASUBTYPE \_ ARGB4444</span><span class="sxs-lookup"><span data-stu-id="a91d7-153">MEDIATYPE\_Video, MEDIASUBTYPE\_ARGB4444</span></span>
-   <span data-ttu-id="a91d7-154">\_Video di MEDIATYPE, MEDIASUBTYPE \_ AYUV</span><span class="sxs-lookup"><span data-stu-id="a91d7-154">MEDIATYPE\_Video, MEDIASUBTYPE\_AYUV</span></span>

<span data-ttu-id="a91d7-155">Interfacce del PIN di output</span><span class="sxs-lookup"><span data-stu-id="a91d7-155">Output Pin Interfaces</span></span>

<span data-ttu-id="a91d7-156">[**IAMVideoAcceleratorNotify**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoacceleratornotify) (solo pin di output video)</span><span class="sxs-lookup"><span data-stu-id="a91d7-156">[**IAMVideoAcceleratorNotify**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoacceleratornotify) (video output pin only)</span></span><br/> [<span data-ttu-id="a91d7-157">**IKsPropertySet**</span><span class="sxs-lookup"><span data-stu-id="a91d7-157">**IKsPropertySet**</span></span>](ikspropertyset.md)<br/> [<span data-ttu-id="a91d7-158">**IMediaSeeking**</span><span class="sxs-lookup"><span data-stu-id="a91d7-158">**IMediaSeeking**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [<span data-ttu-id="a91d7-159">**IPin**</span><span class="sxs-lookup"><span data-stu-id="a91d7-159">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [<span data-ttu-id="a91d7-160">**IQualityControl**</span><span class="sxs-lookup"><span data-stu-id="a91d7-160">**IQualityControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/> [<span data-ttu-id="a91d7-161">**IVPConfig**</span><span class="sxs-lookup"><span data-stu-id="a91d7-161">**IVPConfig**</span></span>](/previous-versions/windows/desktop/api/Vpconfig/nn-vpconfig-ivpconfig)<br/>

<span data-ttu-id="a91d7-162">CLSID filtro</span><span class="sxs-lookup"><span data-stu-id="a91d7-162">Filter CLSID</span></span>

<span data-ttu-id="a91d7-163">**CLSID \_ CMPEG2VidDecoderDS** (definito in wmcodecdsp. h)</span><span class="sxs-lookup"><span data-stu-id="a91d7-163">**CLSID\_CMPEG2VidDecoderDS** (defined in wmcodecdsp.h)</span></span>

<span data-ttu-id="a91d7-164">File eseguibile</span><span class="sxs-lookup"><span data-stu-id="a91d7-164">Executable</span></span>

<span data-ttu-id="a91d7-165">msmpeg2vdec.dll</span><span class="sxs-lookup"><span data-stu-id="a91d7-165">msmpeg2vdec.dll</span></span>

[<span data-ttu-id="a91d7-166">Merito</span><span class="sxs-lookup"><span data-stu-id="a91d7-166">Merit</span></span>](merit.md)

<span data-ttu-id="a91d7-167">Il **merito \_ NORMALE** -1</span><span class="sxs-lookup"><span data-stu-id="a91d7-167">**MERIT\_NORMAL** - 1</span></span>

[<span data-ttu-id="a91d7-168">Categoria filtro</span><span class="sxs-lookup"><span data-stu-id="a91d7-168">Filter Category</span></span>](filter-categories.md)

<span data-ttu-id="a91d7-169">**\_LEGACYAMFILTERCATEGORY CLSID**</span><span class="sxs-lookup"><span data-stu-id="a91d7-169">**CLSID\_LegacyAmFilterCategory**</span></span>



 

## <a name="remarks"></a><span data-ttu-id="a91d7-170">Commenti</span><span class="sxs-lookup"><span data-stu-id="a91d7-170">Remarks</span></span>

<span data-ttu-id="a91d7-171">Questo filtro ha due pin di input e tre pin di output.</span><span class="sxs-lookup"><span data-stu-id="a91d7-171">This filter has two input pins and three output pins.</span></span>

<span data-ttu-id="a91d7-172">Pin di input:</span><span class="sxs-lookup"><span data-stu-id="a91d7-172">Input pins:</span></span>

-   <span data-ttu-id="a91d7-173">Input video</span><span class="sxs-lookup"><span data-stu-id="a91d7-173">Video input</span></span>
-   <span data-ttu-id="a91d7-174">Input della sottoimmagine</span><span class="sxs-lookup"><span data-stu-id="a91d7-174">Subpicture input</span></span>

<span data-ttu-id="a91d7-175">Pin di output:</span><span class="sxs-lookup"><span data-stu-id="a91d7-175">Output pins:</span></span>

-   <span data-ttu-id="a91d7-176">Output video</span><span class="sxs-lookup"><span data-stu-id="a91d7-176">Video output</span></span>
-   <span data-ttu-id="a91d7-177">Output riga 21</span><span class="sxs-lookup"><span data-stu-id="a91d7-177">Line-21 output</span></span>
-   <span data-ttu-id="a91d7-178">Output della sottoimmagine</span><span class="sxs-lookup"><span data-stu-id="a91d7-178">Subpicture output</span></span>

<span data-ttu-id="a91d7-179">Il filtro non crea il pin di output della sottoimmagine, a meno che il pin di input del video non sia connesso con un tipo di supporto del **\_ \_ \_ pacchetto DVD crittografato MEDIATYPE** .</span><span class="sxs-lookup"><span data-stu-id="a91d7-179">The filter does not create the subpicture output pin unless the video input pin is connected with a **MEDIATYPE\_DVD\_ENCRYPTED\_PACK** media type.</span></span>

### <a name="mpeg-12-support"></a><span data-ttu-id="a91d7-180">Supporto MPEG-1/2</span><span class="sxs-lookup"><span data-stu-id="a91d7-180">MPEG-1/2 Support</span></span>

<span data-ttu-id="a91d7-181">Per MPEG-1 e MPEG-2, il decodificatore supporta i formati seguenti:</span><span class="sxs-lookup"><span data-stu-id="a91d7-181">For MPEG-1 and MPEG-2, the decoder supports the following formats:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a91d7-182">Profili/livelli</span><span class="sxs-lookup"><span data-stu-id="a91d7-182">Profiles/Levels</span></span></td>
<td><span data-ttu-id="a91d7-183">Qualsiasi combinazione dei seguenti profili e livelli:</span><span class="sxs-lookup"><span data-stu-id="a91d7-183">Any combination of the following profiles and levels:</span></span><br/>
<ul>
<li><span data-ttu-id="a91d7-184">Profili: semplice, principale</span><span class="sxs-lookup"><span data-stu-id="a91d7-184">Profiles: Simple, Main</span></span></li>
<li><span data-ttu-id="a91d7-185">Livelli: Low, Main, High, High 1440</span><span class="sxs-lookup"><span data-stu-id="a91d7-185">Levels: Low, Main, High, High 1440</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a91d7-186">Formati Chroma</span><span class="sxs-lookup"><span data-stu-id="a91d7-186">Chroma Formats</span></span></td>
<td><span data-ttu-id="a91d7-187">Chroma 4:2:0</span><span class="sxs-lookup"><span data-stu-id="a91d7-187">4:2:0 chroma</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a91d7-188">Risoluzione massima</span><span class="sxs-lookup"><span data-stu-id="a91d7-188">Maximum Resolution</span></span></td>
<td><span data-ttu-id="a91d7-189">1920 × 1088 pixel</span><span class="sxs-lookup"><span data-stu-id="a91d7-189">1920 × 1088 pixels</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a91d7-190">DXVA</span><span class="sxs-lookup"><span data-stu-id="a91d7-190">DXVA</span></span></td>
<td><span data-ttu-id="a91d7-191">Il decodificatore supporta la versione 1 e la versione 2 di DirectX Video Acceleration (DXVA).</span><span class="sxs-lookup"><span data-stu-id="a91d7-191">The decoder supports DirectX Video Acceleration (DXVA) version 1 and version 2.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="a91d7-192">Il decodificatore non supporta i Bitstream scalabili.</span><span class="sxs-lookup"><span data-stu-id="a91d7-192">The decoder does not support scalable bitstreams.</span></span> <span data-ttu-id="a91d7-193">L'input deve essere un flusso video elementare.</span><span class="sxs-lookup"><span data-stu-id="a91d7-193">The input must be an elementary video stream.</span></span>

<span data-ttu-id="a91d7-194">Il decodificatore non supporta i formati Chroma 4:2:2.</span><span class="sxs-lookup"><span data-stu-id="a91d7-194">The decoder does not support 4:2:2 chroma formats.</span></span>

### <a name="h264-support"></a><span data-ttu-id="a91d7-195">Supporto di H. 264</span><span class="sxs-lookup"><span data-stu-id="a91d7-195">H.264 Support</span></span>

<span data-ttu-id="a91d7-196">Per H. 264, il decodificatore supporta i formati seguenti:</span><span class="sxs-lookup"><span data-stu-id="a91d7-196">For H.264, the decoder supports the following formats:</span></span>



| <span data-ttu-id="a91d7-197">Requisito</span><span class="sxs-lookup"><span data-stu-id="a91d7-197">Requirement</span></span> | <span data-ttu-id="a91d7-198">Valore</span><span class="sxs-lookup"><span data-stu-id="a91d7-198">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a91d7-199">Profili/livelli</span><span class="sxs-lookup"><span data-stu-id="a91d7-199">Profiles/Levels</span></span>    | <span data-ttu-id="a91d7-200">Profili Baseline, Main e High, fino al livello 5,1.</span><span class="sxs-lookup"><span data-stu-id="a91d7-200">Baseline, Main, and High profiles, up to level 5.1.</span></span> <span data-ttu-id="a91d7-201">Per informazioni dettagliate, vedere la specifica ITU-T H. 264.</span><span class="sxs-lookup"><span data-stu-id="a91d7-201">(See ITU-T H.264 specification for details.)</span></span>                                                                                                                                                                          |
| <span data-ttu-id="a91d7-202">Formati Chroma</span><span class="sxs-lookup"><span data-stu-id="a91d7-202">Chroma Formats</span></span>     | <span data-ttu-id="a91d7-203">4:2:0 Chroma o monocromatico</span><span class="sxs-lookup"><span data-stu-id="a91d7-203">4:2:0 chroma or monochrome</span></span>                                                                                                                                                                                                                                                |
| <span data-ttu-id="a91d7-204">Risoluzione minima</span><span class="sxs-lookup"><span data-stu-id="a91d7-204">Minimum Resolution</span></span> | <span data-ttu-id="a91d7-205">48 × 48 pixel</span><span class="sxs-lookup"><span data-stu-id="a91d7-205">48 × 48 pixels</span></span>                                                                                                                                                                                                                                                            |
| <span data-ttu-id="a91d7-206">Risoluzione massima</span><span class="sxs-lookup"><span data-stu-id="a91d7-206">Maximum Resolution</span></span> | <span data-ttu-id="a91d7-207">1920 × 1088 pixel</span><span class="sxs-lookup"><span data-stu-id="a91d7-207">1920 × 1088 pixels</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="a91d7-208">DXVA</span><span class="sxs-lookup"><span data-stu-id="a91d7-208">DXVA</span></span>               | <span data-ttu-id="a91d7-209">Il decodificatore supporta DXVA versione 2, ma non DXVA versione 1.</span><span class="sxs-lookup"><span data-stu-id="a91d7-209">The decoder supports DXVA version 2, but not DXVA version 1.</span></span> <span data-ttu-id="a91d7-210">La decodifica DXVA è supportata solo per i Bitstream della linea di base, principale e del profilo superiore compatibili con la principale.</span><span class="sxs-lookup"><span data-stu-id="a91d7-210">DXVA decoding is supported only for Main-compatible Baseline, Main, and High profile bitstreams.</span></span> <span data-ttu-id="a91d7-211">I Bitstream di base compatibili con la principale sono definiti come **profilo \_ idc**= 66 e **\_ \_ flag set1 vincolato**= 1.</span><span class="sxs-lookup"><span data-stu-id="a91d7-211">(Main-compatible Baseline bitstreams are defined as **profile\_idc**=66 and **constrained\_set1\_flag**=1.)</span></span> |



 

<span data-ttu-id="a91d7-212">Il decodificatore non supporta la tecnologia granulare dei film.</span><span class="sxs-lookup"><span data-stu-id="a91d7-212">The decoder does not support Film Grain Technology.</span></span>

<span data-ttu-id="a91d7-213">Per informazioni sui tipi di supporto H. 264, vedere [tipi di video h. 264](h-264-video-types.md).</span><span class="sxs-lookup"><span data-stu-id="a91d7-213">For information about the H.264 media types, see [H.264 Video Types](h-264-video-types.md).</span></span>

### <a name="codec-properties"></a><span data-ttu-id="a91d7-214">Proprietà codec</span><span class="sxs-lookup"><span data-stu-id="a91d7-214">Codec Properties</span></span>

<span data-ttu-id="a91d7-215">I pin di input supportano i set di proprietà seguenti tramite [**IKsPropertySet**](ikspropertyset.md):</span><span class="sxs-lookup"><span data-stu-id="a91d7-215">The input pins support the following property sets through [**IKsPropertySet**](ikspropertyset.md):</span></span>

-   [<span data-ttu-id="a91d7-216">**Set di proprietà di protezione copia DVD**</span><span class="sxs-lookup"><span data-stu-id="a91d7-216">**DVD Copy Protection Property Set**</span></span>](dvd-copy-protection-property-set.md)
-   <span data-ttu-id="a91d7-217">[**Set di proprietà della sottoimmagine DVD**](dvd-subpicture-property-set.md) (solo pin dell'immagine)</span><span class="sxs-lookup"><span data-stu-id="a91d7-217">[**DVD Subpicture Property Set**](dvd-subpicture-property-set.md) (subpicture pin only)</span></span>

<span data-ttu-id="a91d7-218">I pin di input supportano le proprietà seguenti tramite [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):</span><span class="sxs-lookup"><span data-stu-id="a91d7-218">The input pins support the following properties through [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):</span></span>



| <span data-ttu-id="a91d7-219">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a91d7-219">Property</span></span>                                                                  | <span data-ttu-id="a91d7-220">Richiede</span><span class="sxs-lookup"><span data-stu-id="a91d7-220">Requires</span></span>      |
|---------------------------------------------------------------------------|---------------|
| [<span data-ttu-id="a91d7-221">**AVDecCommonInputFormat**</span><span class="sxs-lookup"><span data-stu-id="a91d7-221">**AVDecCommonInputFormat**</span></span>](avdeccommoninputformat-property.md)         | <span data-ttu-id="a91d7-222">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a91d7-222">Windows Vista</span></span> |
| [<span data-ttu-id="a91d7-223">**AVDecVideoInputScanType**</span><span class="sxs-lookup"><span data-stu-id="a91d7-223">**AVDecVideoInputScanType**</span></span>](avdecvideoinputscantype-property.md)       | <span data-ttu-id="a91d7-224">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a91d7-224">Windows Vista</span></span> |
| [<span data-ttu-id="a91d7-225">**AVDecVideoPixelAspectRatio**</span><span class="sxs-lookup"><span data-stu-id="a91d7-225">**AVDecVideoPixelAspectRatio**</span></span>](avdecvideopixelaspectratio-property.md) | <span data-ttu-id="a91d7-226">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a91d7-226">Windows Vista</span></span> |



 

<span data-ttu-id="a91d7-227">Il filtro supporta le seguenti proprietà tramite [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):</span><span class="sxs-lookup"><span data-stu-id="a91d7-227">The filter supports the following properties through [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):</span></span>



| <span data-ttu-id="a91d7-228">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a91d7-228">Property</span></span>                                                                                | <span data-ttu-id="a91d7-229">Richiede</span><span class="sxs-lookup"><span data-stu-id="a91d7-229">Requires</span></span>      |
|-----------------------------------------------------------------------------------------|---------------|
| [<span data-ttu-id="a91d7-230">**AVDecMmcssClass**</span><span class="sxs-lookup"><span data-stu-id="a91d7-230">**AVDecMmcssClass**</span></span>](avdecmmcss-property.md)                                          | <span data-ttu-id="a91d7-231">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a91d7-231">Windows Vista</span></span> |
| [<span data-ttu-id="a91d7-232">**AVDecVideoAcceleration \_ H264**</span><span class="sxs-lookup"><span data-stu-id="a91d7-232">**AVDecVideoAcceleration\_H264**</span></span>](avdecvideoacceleration-h264-property.md)            | <span data-ttu-id="a91d7-233">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a91d7-233">Windows 7</span></span>     |
| [<span data-ttu-id="a91d7-234">**AVDecVideoAcceleration \_ MPEG2**</span><span class="sxs-lookup"><span data-stu-id="a91d7-234">**AVDecVideoAcceleration\_MPEG2**</span></span>](avdecvideoacceleration-mpeg2-property.md)          | <span data-ttu-id="a91d7-235">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a91d7-235">Windows 7</span></span>     |
| [<span data-ttu-id="a91d7-236">**AVDecVideoDropPicWithMissingRef**</span><span class="sxs-lookup"><span data-stu-id="a91d7-236">**AVDecVideoDropPicWithMissingRef**</span></span>](avdecvideodroppicwithmissingref-property.md)     | <span data-ttu-id="a91d7-237">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a91d7-237">Windows 7</span></span>     |
| [<span data-ttu-id="a91d7-238">**AVDecVideoFastDecodeMode**</span><span class="sxs-lookup"><span data-stu-id="a91d7-238">**AVDecVideoFastDecodeMode**</span></span>](avdecvideofastdecodemode.md)                            | <span data-ttu-id="a91d7-239">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a91d7-239">Windows 7</span></span>     |
| [<span data-ttu-id="a91d7-240">**AVDecVideoImageSize**</span><span class="sxs-lookup"><span data-stu-id="a91d7-240">**AVDecVideoImageSize**</span></span>](avdecvideoimagesize.md)                                      | <span data-ttu-id="a91d7-241">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a91d7-241">Windows 7</span></span>     |
| [<span data-ttu-id="a91d7-242">**AVDecVideoSoftwareDeinterlaceMode**</span><span class="sxs-lookup"><span data-stu-id="a91d7-242">**AVDecVideoSoftwareDeinterlaceMode**</span></span>](avdecvideosoftwaredeinterlacemode-property.md) | <span data-ttu-id="a91d7-243">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a91d7-243">Windows 7</span></span>     |
| [<span data-ttu-id="a91d7-244">**AVDecVideoThumbnailGenerationMode**</span><span class="sxs-lookup"><span data-stu-id="a91d7-244">**AVDecVideoThumbnailGenerationMode**</span></span>](avdecvideothumbnailgenerationmode-property.md) | <span data-ttu-id="a91d7-245">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a91d7-245">Windows 7</span></span>     |



 

## <a name="requirements"></a><span data-ttu-id="a91d7-246">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a91d7-246">Requirements</span></span>



| <span data-ttu-id="a91d7-247">Requisito</span><span class="sxs-lookup"><span data-stu-id="a91d7-247">Requirement</span></span> | <span data-ttu-id="a91d7-248">Valore</span><span class="sxs-lookup"><span data-stu-id="a91d7-248">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a91d7-249">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a91d7-249">Minimum supported client</span></span><br/> | <span data-ttu-id="a91d7-250">Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 Home Premium, Windows 7 Professional, Windows 7 Enterprise, Windows 7 Ultimate \[ desktop apps\]</span><span class="sxs-lookup"><span data-stu-id="a91d7-250">Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 Home Premium, Windows 7 Professional, Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a91d7-251">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a91d7-251">Minimum supported server</span></span><br/> | <span data-ttu-id="a91d7-252">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="a91d7-252">None supported</span></span><br/>                                                                                                                                                     |
| <span data-ttu-id="a91d7-253">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a91d7-253">Header</span></span><br/>                   | <dl> <span data-ttu-id="a91d7-254"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a91d7-254"><dt>Wmcodecdsp.h</dt></span></span> </dl>                                                                                       |



## <a name="see-also"></a><span data-ttu-id="a91d7-255">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a91d7-255">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a91d7-256">Filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="a91d7-256">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="a91d7-257">**Tipi di supporti DVD**</span><span class="sxs-lookup"><span data-stu-id="a91d7-257">**DVD Media Types**</span></span>](dvd-media-types.md)
</dt> <dt>

[<span data-ttu-id="a91d7-258">Tipi di video H. 264</span><span class="sxs-lookup"><span data-stu-id="a91d7-258">H.264 Video Types</span></span>](h-264-video-types.md)
</dt> </dl>

 

 
