---
description: Il filtro Microsoft MPEG-2 Audio Encoder codifica i livelli audio MPEG-1 I e II, incluso il supporto per le estensioni MPEG-2 Low Sampling Frequency (LSF).
ms.assetid: a36e838b-8b11-4851-9dd2-efd9fe070770
title: Codificatore audio Microsoft MPEG-2 (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43d055acd379d9e966f43eac284e38a10c05a86c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303991"
---
# <a name="microsoft-mpeg-2-audio-encoder"></a><span data-ttu-id="63b1d-103">Codificatore audio Microsoft MPEG-2</span><span class="sxs-lookup"><span data-stu-id="63b1d-103">Microsoft MPEG-2 Audio Encoder</span></span>

<span data-ttu-id="63b1d-104">Il filtro Microsoft MPEG-2 Audio Encoder codifica i livelli audio MPEG-1 I e II, incluso il supporto per le estensioni MPEG-2 Low Sampling Frequency (LSF).</span><span class="sxs-lookup"><span data-stu-id="63b1d-104">The Microsoft MPEG-2 Audio Encoder filter encodes MPEG-1 audio layers I and II, including support for the MPEG-2 Low Sampling Frequency (LSF) extensions.</span></span>

<span data-ttu-id="63b1d-105">Per codificare i flussi audio/video multiplex, usare il filtro [**Microsoft MPEG-2 Encoder**](microsoft-mpeg-2-encoder.md) , che incapsula le funzioni di questo filtro e del filtro [**codificatore video Microsoft MPEG-2**](microsoft-mpeg-2-video-encoder.md) .</span><span class="sxs-lookup"><span data-stu-id="63b1d-105">To encode and multiplex audio/video streams, use the [**Microsoft MPEG-2 Encoder**](microsoft-mpeg-2-encoder.md) filter, which encapsulates the functions of both this filter and the [**Microsoft MPEG-2 Video Encoder**](microsoft-mpeg-2-video-encoder.md) filter.</span></span>

> [!Note]  
> <span data-ttu-id="63b1d-106">Questo filtro non è supportato nelle piattaforme basate su IA-64.</span><span class="sxs-lookup"><span data-stu-id="63b1d-106">This filter is not supported on IA-64-based platforms.</span></span>

 



<span data-ttu-id="63b1d-107">Informazioni sul filtro</span><span class="sxs-lookup"><span data-stu-id="63b1d-107">Filter Information</span></span>

<span data-ttu-id="63b1d-108">Interfacce di filtro</span><span class="sxs-lookup"><span data-stu-id="63b1d-108">Filter Interfaces</span></span>

[<span data-ttu-id="63b1d-109">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="63b1d-109">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/> [<span data-ttu-id="63b1d-110">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="63b1d-110">**ICodecAPI**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/> <span data-ttu-id="63b1d-111">**IEncoderAPI**</span><span class="sxs-lookup"><span data-stu-id="63b1d-111">**IEncoderAPI**</span></span><br/> [<span data-ttu-id="63b1d-112">**IMediaSeeking**</span><span class="sxs-lookup"><span data-stu-id="63b1d-112">**IMediaSeeking**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [<span data-ttu-id="63b1d-113">**IVideoEncoder**</span><span class="sxs-lookup"><span data-stu-id="63b1d-113">**IVideoEncoder**</span></span>](/windows/win32/api/strmif/nn-strmif-ivideoencoder)<br/>

<span data-ttu-id="63b1d-114">Tipi di supporti pin di input</span><span class="sxs-lookup"><span data-stu-id="63b1d-114">Input Pin Media Types</span></span>

<span data-ttu-id="63b1d-115">**MEDIATYPE \_ Audio**, **\_ PCM MEDIASUBTYPE**</span><span class="sxs-lookup"><span data-stu-id="63b1d-115">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_PCM**</span></span>

<span data-ttu-id="63b1d-116">Interfacce pin di input</span><span class="sxs-lookup"><span data-stu-id="63b1d-116">Input Pin Interfaces</span></span>

[<span data-ttu-id="63b1d-117">**IMemInputPin**</span><span class="sxs-lookup"><span data-stu-id="63b1d-117">**IMemInputPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [<span data-ttu-id="63b1d-118">**IPin**</span><span class="sxs-lookup"><span data-stu-id="63b1d-118">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [<span data-ttu-id="63b1d-119">**IQualityControl**</span><span class="sxs-lookup"><span data-stu-id="63b1d-119">**IQualityControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

<span data-ttu-id="63b1d-120">Tipi di supporti pin di output</span><span class="sxs-lookup"><span data-stu-id="63b1d-120">Output Pin Media Types</span></span>

<span data-ttu-id="63b1d-121">**MEDIATYPE \_ Audio**, **\_ \_ audio MPEG2 MEDIASUBTYPE**</span><span class="sxs-lookup"><span data-stu-id="63b1d-121">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_MPEG2\_AUDIO**</span></span><br/> <span data-ttu-id="63b1d-122">**MEDIATYPE \_ Flusso**, **MEDIASUBTYPE \_ \_ audio MPEG2**</span><span class="sxs-lookup"><span data-stu-id="63b1d-122">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_MPEG2\_AUDIO**</span></span><br/> <span data-ttu-id="63b1d-123">**MEDIATYPE \_ Flusso**, **\_ \_ programma MEDIASUBTYPE MPEG2**</span><span class="sxs-lookup"><span data-stu-id="63b1d-123">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_MPEG2\_PROGRAM**</span></span><br/> <span data-ttu-id="63b1d-124">**MEDIATYPE \_ Flusso**, **\_ \_ trasporto MPEG2 MEDIASUBTYPE**</span><span class="sxs-lookup"><span data-stu-id="63b1d-124">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_MPEG2\_TRANSPORT**</span></span><br/>

<span data-ttu-id="63b1d-125">Interfacce del PIN di output</span><span class="sxs-lookup"><span data-stu-id="63b1d-125">Output Pin Interfaces</span></span>

[<span data-ttu-id="63b1d-126">**IMediaSeeking**</span><span class="sxs-lookup"><span data-stu-id="63b1d-126">**IMediaSeeking**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [<span data-ttu-id="63b1d-127">**IPin**</span><span class="sxs-lookup"><span data-stu-id="63b1d-127">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [<span data-ttu-id="63b1d-128">**IQualityControl**</span><span class="sxs-lookup"><span data-stu-id="63b1d-128">**IQualityControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

<span data-ttu-id="63b1d-129">CLSID filtro</span><span class="sxs-lookup"><span data-stu-id="63b1d-129">Filter CLSID</span></span>

<span data-ttu-id="63b1d-130">**CLSID \_ CMPEG2EncoderAudioDS** (dichiarata in wmcodecdsp. h)</span><span class="sxs-lookup"><span data-stu-id="63b1d-130">**CLSID\_CMPEG2EncoderAudioDS** (declared in wmcodecdsp.h)</span></span>

<span data-ttu-id="63b1d-131">File eseguibile</span><span class="sxs-lookup"><span data-stu-id="63b1d-131">Executable</span></span>

<span data-ttu-id="63b1d-132">msmpeg2enc.dll</span><span class="sxs-lookup"><span data-stu-id="63b1d-132">msmpeg2enc.dll</span></span>

[<span data-ttu-id="63b1d-133">Merito</span><span class="sxs-lookup"><span data-stu-id="63b1d-133">Merit</span></span>](merit.md)

<span data-ttu-id="63b1d-134">**il merito non viene \_ \_ \_ utilizzato**</span><span class="sxs-lookup"><span data-stu-id="63b1d-134">**MERIT\_DO\_NOT\_USE**</span></span>

[<span data-ttu-id="63b1d-135">Categoria filtro</span><span class="sxs-lookup"><span data-stu-id="63b1d-135">Filter Category</span></span>](filter-categories.md)

<span data-ttu-id="63b1d-136">**\_LEGACYAMFILTERCATEGORY CLSID**</span><span class="sxs-lookup"><span data-stu-id="63b1d-136">**CLSID\_LegacyAmFilterCategory**</span></span>



 

## <a name="remarks"></a><span data-ttu-id="63b1d-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="63b1d-137">Remarks</span></span>

<span data-ttu-id="63b1d-138">Il codificatore audio MPEG-2 può produrre i tipi di output seguenti:</span><span class="sxs-lookup"><span data-stu-id="63b1d-138">The MPEG-2 Audio Encoder can produce the following kinds of output:</span></span>

-   <span data-ttu-id="63b1d-139">Flusso audio elementare</span><span class="sxs-lookup"><span data-stu-id="63b1d-139">Audio elementary stream</span></span>
-   <span data-ttu-id="63b1d-140">Audio in un flusso di programma MPEG-2</span><span class="sxs-lookup"><span data-stu-id="63b1d-140">Audio in an MPEG-2 program stream</span></span>
-   <span data-ttu-id="63b1d-141">Audio in un flusso di trasporto MPEG-2</span><span class="sxs-lookup"><span data-stu-id="63b1d-141">Audio in an MPEG-2 transport stream</span></span>

<span data-ttu-id="63b1d-142">Supporta le estensioni MPEG-1 Layer I e II e MPEG-2 Low Sampling Frequency (LSF)</span><span class="sxs-lookup"><span data-stu-id="63b1d-142">It supports MPEG-1 layers I and II and MPEG-2 low sampling frequency (LSF) extensions</span></span>

<span data-ttu-id="63b1d-143">Gli esempi di input devono essere a 16 bit per campione, con una frequenza di campionamento audio di 48, 44,1, 32, 22,05 o 16 KHz.</span><span class="sxs-lookup"><span data-stu-id="63b1d-143">Input samples must 16 bits per sample, with an audio sampling rate of 48, 44.1, 32, 22.05, or 16 KHz.</span></span> <span data-ttu-id="63b1d-144">Il codificatore non può ricampionare il flusso audio; l'audio codificato ha la stessa frequenza di campionamento dell'input.</span><span class="sxs-lookup"><span data-stu-id="63b1d-144">The encoder cannot resample the audio stream; the encoded audio has the same sample rate as the input.</span></span>

<span data-ttu-id="63b1d-145">Gli esempi di input devono essere mono o stereo.</span><span class="sxs-lookup"><span data-stu-id="63b1d-145">Input samples must be mono or stereo.</span></span> <span data-ttu-id="63b1d-146">L'audio codificato ha il numero di canali come input.</span><span class="sxs-lookup"><span data-stu-id="63b1d-146">The encoded audio has the number of channels as the input.</span></span>

### <a name="limitations"></a><span data-ttu-id="63b1d-147">Limitazioni</span><span class="sxs-lookup"><span data-stu-id="63b1d-147">Limitations</span></span>

<span data-ttu-id="63b1d-148">Il codificatore non supporta quanto segue:</span><span class="sxs-lookup"><span data-stu-id="63b1d-148">The encoder does not support the following:</span></span>

-   <span data-ttu-id="63b1d-149">Bitstream audio MPEG Layer III.</span><span class="sxs-lookup"><span data-stu-id="63b1d-149">MPEG layer III audio bitstreams.</span></span>
-   <span data-ttu-id="63b1d-150">Bitstream di estensione multicanale MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="63b1d-150">MPEG-2 multi-channel extension bitstreams.</span></span>
-   <span data-ttu-id="63b1d-151">Bitstream MPEG-4 AAC.</span><span class="sxs-lookup"><span data-stu-id="63b1d-151">MPEG-4 AAC bitstreams.</span></span>
-   <span data-ttu-id="63b1d-152">Bitstream MPEG-2 non compatibili con le versioni precedenti (NBC).</span><span class="sxs-lookup"><span data-stu-id="63b1d-152">MPEG-2 non-backward compatible (NBC) bitstreams.</span></span>
-   <span data-ttu-id="63b1d-153">Generazione di pacchetti di flusso elementare (PES) in pacchetto.</span><span class="sxs-lookup"><span data-stu-id="63b1d-153">Generation of packetized elementary stream (PES) packets.</span></span>
-   <span data-ttu-id="63b1d-154">Codifica Dolby Digital.</span><span class="sxs-lookup"><span data-stu-id="63b1d-154">Dolby Digital encoding.</span></span>

### <a name="codec-properties"></a><span data-ttu-id="63b1d-155">Proprietà codec</span><span class="sxs-lookup"><span data-stu-id="63b1d-155">Codec Properties</span></span>

<span data-ttu-id="63b1d-156">Il filtro supporta le seguenti proprietà tramite [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):</span><span class="sxs-lookup"><span data-stu-id="63b1d-156">The filter supports the following properties through [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):</span></span>

-   [<span data-ttu-id="63b1d-157">**AVAudioChannelCount**</span><span class="sxs-lookup"><span data-stu-id="63b1d-157">**AVAudioChannelCount**</span></span>](avaudiochannelcount-property.md)
-   [<span data-ttu-id="63b1d-158">**AVAudioSampleRate**</span><span class="sxs-lookup"><span data-stu-id="63b1d-158">**AVAudioSampleRate**</span></span>](avaudiosamplerate-property.md)
-   [<span data-ttu-id="63b1d-159">**AVEncAudioIntervalToEncode**</span><span class="sxs-lookup"><span data-stu-id="63b1d-159">**AVEncAudioIntervalToEncode**</span></span>](avencaudiointervaltoencode-property.md)
-   [<span data-ttu-id="63b1d-160">**AVEncCommonFormatConstraint**</span><span class="sxs-lookup"><span data-stu-id="63b1d-160">**AVEncCommonFormatConstraint**</span></span>](avenccommonformatconstraint-property.md)
-   [<span data-ttu-id="63b1d-161">**AVEncCommonMeanBitRate**</span><span class="sxs-lookup"><span data-stu-id="63b1d-161">**AVEncCommonMeanBitRate**</span></span>](avenccommonmeanbitrate-property.md)
-   [<span data-ttu-id="63b1d-162">**AVEncMPACodingMode**</span><span class="sxs-lookup"><span data-stu-id="63b1d-162">**AVEncMPACodingMode**</span></span>](avencmpacodingmode-property.md)
-   [<span data-ttu-id="63b1d-163">**AVEncMPACopyright**</span><span class="sxs-lookup"><span data-stu-id="63b1d-163">**AVEncMPACopyright**</span></span>](avencmpacopyright-property.md)
-   [<span data-ttu-id="63b1d-164">**AVEncMPAEmphasisType**</span><span class="sxs-lookup"><span data-stu-id="63b1d-164">**AVEncMPAEmphasisType**</span></span>](avencmpaemphasistype-property.md)
-   [<span data-ttu-id="63b1d-165">**AVEncMPAEnableRedundancyProtection**</span><span class="sxs-lookup"><span data-stu-id="63b1d-165">**AVEncMPAEnableRedundancyProtection**</span></span>](avencmpaenableredundancyprotection-property.md)
-   [<span data-ttu-id="63b1d-166">**AVEncMPALayer**</span><span class="sxs-lookup"><span data-stu-id="63b1d-166">**AVEncMPALayer**</span></span>](avencmpalayer-property.md)
-   [<span data-ttu-id="63b1d-167">**AVEncMPAOriginalBitstream**</span><span class="sxs-lookup"><span data-stu-id="63b1d-167">**AVEncMPAOriginalBitstream**</span></span>](avencmpaoriginalbitstream-property.md)
-   [<span data-ttu-id="63b1d-168">**AVEncMPAPrivateUserBit**</span><span class="sxs-lookup"><span data-stu-id="63b1d-168">**AVEncMPAPrivateUserBit**</span></span>](avencmpaprivateuserbit-property.md)

> [!Note]  
> <span data-ttu-id="63b1d-169">Una versione precedente della documentazione elenca erroneamente alcune proprietà aggiuntive che non sono supportate.</span><span class="sxs-lookup"><span data-stu-id="63b1d-169">An earlier version of the documentation incorrectly listed some additional properties that are not supported.</span></span>

 

<span data-ttu-id="63b1d-170">Per compatibilità con le versioni precedenti, il filtro supporta la seguente proprietà tramite l'interfaccia **IEncoderAPI** :</span><span class="sxs-lookup"><span data-stu-id="63b1d-170">For backward compatibility, the filter supports the following property through the **IEncoderAPI** interface:</span></span>



| <span data-ttu-id="63b1d-171">Proprietà</span><span class="sxs-lookup"><span data-stu-id="63b1d-171">Property</span></span>                 | <span data-ttu-id="63b1d-172">Descrizione</span><span class="sxs-lookup"><span data-stu-id="63b1d-172">Description</span></span>                                                                      |
|--------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="63b1d-173">**\_velocità in bit ENCAPIPARAM**</span><span class="sxs-lookup"><span data-stu-id="63b1d-173">**ENCAPIPARAM\_BITRATE**</span></span> | <span data-ttu-id="63b1d-174">Equivalente a [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md).</span><span class="sxs-lookup"><span data-stu-id="63b1d-174">Equivalent to [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md).</span></span> |



 

<span data-ttu-id="63b1d-175">È consigliabile impostare le proprietà nell'ordine seguente:</span><span class="sxs-lookup"><span data-stu-id="63b1d-175">It is recommended to set properties in the following order:</span></span>

1.  [<span data-ttu-id="63b1d-176">**AVEncCommonFormatConstraint**</span><span class="sxs-lookup"><span data-stu-id="63b1d-176">**AVEncCommonFormatConstraint**</span></span>](avenccommonformatconstraint-property.md)
2.  [<span data-ttu-id="63b1d-177">**AVEncMPALayer**</span><span class="sxs-lookup"><span data-stu-id="63b1d-177">**AVEncMPALayer**</span></span>](avencmpalayer-property.md)
3.  [<span data-ttu-id="63b1d-178">**AVEncCommonMeanBitRate**</span><span class="sxs-lookup"><span data-stu-id="63b1d-178">**AVEncCommonMeanBitRate**</span></span>](avenccommonmeanbitrate-property.md)
4.  [<span data-ttu-id="63b1d-179">**AVEncMPACodingMode**</span><span class="sxs-lookup"><span data-stu-id="63b1d-179">**AVEncMPACodingMode**</span></span>](avencmpacodingmode-property.md)

<span data-ttu-id="63b1d-180">Impostare le proprietà rimanenti in qualsiasi ordine.</span><span class="sxs-lookup"><span data-stu-id="63b1d-180">Set the remaining properties in any order.</span></span>

## <a name="requirements"></a><span data-ttu-id="63b1d-181">Requisiti</span><span class="sxs-lookup"><span data-stu-id="63b1d-181">Requirements</span></span>



| <span data-ttu-id="63b1d-182">Requisito</span><span class="sxs-lookup"><span data-stu-id="63b1d-182">Requirement</span></span> | <span data-ttu-id="63b1d-183">Valore</span><span class="sxs-lookup"><span data-stu-id="63b1d-183">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63b1d-184">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="63b1d-184">Minimum supported client</span></span><br/> | <span data-ttu-id="63b1d-185">Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 Home Premium, Windows 7 Professional, Windows 7 Enterprise, Windows 7 Ultimate \[ desktop apps\]</span><span class="sxs-lookup"><span data-stu-id="63b1d-185">Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 Home Premium, Windows 7 Professional, Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="63b1d-186">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="63b1d-186">Minimum supported server</span></span><br/> | <span data-ttu-id="63b1d-187">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="63b1d-187">None supported</span></span><br/>                                                                                                                                                     |
| <span data-ttu-id="63b1d-188">Intestazione</span><span class="sxs-lookup"><span data-stu-id="63b1d-188">Header</span></span><br/>                   | <dl> <span data-ttu-id="63b1d-189"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="63b1d-189"><dt>Wmcodecdsp.h</dt></span></span> </dl>                                                                                       |



## <a name="see-also"></a><span data-ttu-id="63b1d-190">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="63b1d-190">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63b1d-191">Filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="63b1d-191">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="63b1d-192">**Tipi di supporti di Demultiplexer MPEG-2**</span><span class="sxs-lookup"><span data-stu-id="63b1d-192">**MPEG-2 Demultiplexer Media Types**</span></span>](mpeg-2-demultiplexer-media-types.md)
</dt> </dl>

 

 
