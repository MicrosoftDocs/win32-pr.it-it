---
description: 'Questo filtro decodifica i formati audio seguenti:'
ms.assetid: 2fd14296-9eed-4e25-b140-6281c707fdb7
title: Decoder audio Microsoft MPEG-1/gg/AAC (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a685fa2be32dd963cdc7de08ec716117e6a7016e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303992"
---
# <a name="microsoft-mpeg-1ddaac-audio-decoder"></a><span data-ttu-id="0c389-103">Decoder audio Microsoft MPEG-1/gg/AAC</span><span class="sxs-lookup"><span data-stu-id="0c389-103">Microsoft MPEG-1/DD/AAC Audio Decoder</span></span>

<span data-ttu-id="0c389-104">Questo filtro decodifica i formati audio seguenti:</span><span class="sxs-lookup"><span data-stu-id="0c389-104">This filter decodes the following audio formats:</span></span>

-   <span data-ttu-id="0c389-105">MPEG-1 Audio Layer I e II.</span><span class="sxs-lookup"><span data-stu-id="0c389-105">MPEG-1 audio layers I and II.</span></span>
-   <span data-ttu-id="0c389-106">Audio MPEG-2 compatibile con le versioni precedenti, livelli I e II (ISO/IEC 13818-3), mono e stereo.</span><span class="sxs-lookup"><span data-stu-id="0c389-106">Backward-compatible MPEG-2 audio, layers I and II (ISO/IEC 13818-3), mono and stereo only.</span></span>
-   <span data-ttu-id="0c389-107">Profilo di alta complessità (LC, Advanced Audio Coding).</span><span class="sxs-lookup"><span data-stu-id="0c389-107">Advanced Audio Coding (AAC) Low Complexity (LC) profile.</span></span>
-   <span data-ttu-id="0c389-108">High-Efficiency AAC (HE-AAC) versione 1 e versione 2.</span><span class="sxs-lookup"><span data-stu-id="0c389-108">High-Efficiency AAC (HE-AAC) version 1 and version 2.</span></span>
-   <span data-ttu-id="0c389-109">Digital Theater Systems (DTS) pass-through per l'output digitale.</span><span class="sxs-lookup"><span data-stu-id="0c389-109">Pass-through Digital Theater Systems (DTS) for digital output.</span></span>
-   <span data-ttu-id="0c389-110">Solo LPCM, mono e stereo, con o senza intestazioni PE.</span><span class="sxs-lookup"><span data-stu-id="0c389-110">LPCM, mono and stereo only, with or without PES headers.</span></span>
-   <span data-ttu-id="0c389-111">Dolby Digital.</span><span class="sxs-lookup"><span data-stu-id="0c389-111">Dolby Digital.</span></span>
-   <span data-ttu-id="0c389-112">Dolby Digital Plus, inclusa la conversione da Dolby Digital Plus a Dolby Digital for Digital output.</span><span class="sxs-lookup"><span data-stu-id="0c389-112">Dolby Digital Plus, including conversion from Dolby Digital Plus to Dolby Digital for digital output.</span></span>

> [!Note]  
> <span data-ttu-id="0c389-113">L'implementazione Microsoft della tecnologia Dolby Digital è limitata ai sensi del programma di licenza Dolby Digital per l'uso da parte delle applicazioni Microsoft.</span><span class="sxs-lookup"><span data-stu-id="0c389-113">The Microsoft implementation of the Dolby Digital technology is restricted under terms of the Dolby Digital licensing program to use by Microsoft applications.</span></span>

 

> [!Note]  
> <span data-ttu-id="0c389-114">Questo filtro non è supportato nelle piattaforme basate su IA-64.</span><span class="sxs-lookup"><span data-stu-id="0c389-114">This filter is not supported on IA-64-based platforms.</span></span>

 

<span data-ttu-id="0c389-115">La decodifica dei formati Dolby Digital Plus, AAC e HE-AAC richiede Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0c389-115">Decoding of Dolby Digital Plus, AAC, and HE-AAC formats requires Windows 7.</span></span> <span data-ttu-id="0c389-116">La decodifica di Dolby Digital o Dolby Digital Plus non è supportata in Windows 7 Home Basic o Windows 7 Starter.</span><span class="sxs-lookup"><span data-stu-id="0c389-116">Decoding of Dolby Digital or Dolby Digital Plus is not supported on Windows 7 Home Basic or Windows 7 Starter.</span></span>

<span data-ttu-id="0c389-117">Nel registro di sistema il nome descrittivo di questo filtro è "Microsoft DTV-DVD audio decoder".</span><span class="sxs-lookup"><span data-stu-id="0c389-117">In the registry, the friendly name of this filter is "Microsoft DTV-DVD Audio Decoder".</span></span>



<span data-ttu-id="0c389-118">Informazioni sul filtro</span><span class="sxs-lookup"><span data-stu-id="0c389-118">Filter Information</span></span>

<span data-ttu-id="0c389-119">Interfacce di filtro</span><span class="sxs-lookup"><span data-stu-id="0c389-119">Filter Interfaces</span></span>

[<span data-ttu-id="0c389-120">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="0c389-120">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/> [<span data-ttu-id="0c389-121">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="0c389-121">**ICodecAPI**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/>

<span data-ttu-id="0c389-122">Tipi di supporti pin di input</span><span class="sxs-lookup"><span data-stu-id="0c389-122">Input Pin Media Types</span></span>

<span data-ttu-id="0c389-123">In Windows Vista e versioni successive, il filtro supporta i tipi di input seguenti:</span><span class="sxs-lookup"><span data-stu-id="0c389-123">In Windows Vista and later, the filter supports the following input types:</span></span><br/>

-   <span data-ttu-id="0c389-124">**MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ Dolby \_ AC3** (vedere la nota 1).</span><span class="sxs-lookup"><span data-stu-id="0c389-124">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_DOLBY\_AC3** (See Note 1.)</span></span>
-   <span data-ttu-id="0c389-125">**MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ MPEG1Audio**</span><span class="sxs-lookup"><span data-stu-id="0c389-125">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_MPEG1Audio**</span></span>
-   <span data-ttu-id="0c389-126">**MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ MPEG1Payload**</span><span class="sxs-lookup"><span data-stu-id="0c389-126">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_MPEG1Payload**</span></span>
-   <span data-ttu-id="0c389-127">**MEDIATYPE \_ Audio**, **\_ \_ audio MPEG2 MEDIASUBTYPE**</span><span class="sxs-lookup"><span data-stu-id="0c389-127">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_MPEG2\_AUDIO**</span></span>
-   <span data-ttu-id="0c389-128">**MEDIATYPE \_ DVD \_ Encrypted \_ Pack**, **MEDIASUBTYPE \_ Dolby \_ AC3** (vedere la nota 1).</span><span class="sxs-lookup"><span data-stu-id="0c389-128">**MEDIATYPE\_DVD\_ENCRYPTED\_PACK**, **MEDIASUBTYPE\_DOLBY\_AC3** (See Note 1.)</span></span>
-   <span data-ttu-id="0c389-129">**MEDIATYPE \_ DVD \_ Encrypted \_ Pack**, **MEDIASUBTYPE \_ DTS** (vedere la nota 2).</span><span class="sxs-lookup"><span data-stu-id="0c389-129">**MEDIATYPE\_DVD\_ENCRYPTED\_PACK**, **MEDIASUBTYPE\_DTS** (See Note 2.)</span></span>
-   <span data-ttu-id="0c389-130">**MEDIATYPE \_ DVD \_ Encrypted \_ Pack**, **MEDIASUBTYPE \_ DVD \_ LPCM \_ audio**</span><span class="sxs-lookup"><span data-stu-id="0c389-130">**MEDIATYPE\_DVD\_ENCRYPTED\_PACK**, **MEDIASUBTYPE\_DVD\_LPCM\_AUDIO**</span></span>
-   <span data-ttu-id="0c389-131">**MEDIATYPE \_ DVD \_ Encrypted \_ Pack**, **MEDIASUBTYPE \_ MPEG2 \_ audio**</span><span class="sxs-lookup"><span data-stu-id="0c389-131">**MEDIATYPE\_DVD\_ENCRYPTED\_PACK**, **MEDIASUBTYPE\_MPEG2\_AUDIO**</span></span>
-   <span data-ttu-id="0c389-132">**MEDIATYPE \_ MPEG2 \_ PE**, **MEDIASUBTYPE \_ Dolby \_ AC3** (vedere la nota 1).</span><span class="sxs-lookup"><span data-stu-id="0c389-132">**MEDIATYPE\_MPEG2\_PES**, **MEDIASUBTYPE\_DOLBY\_AC3** (See Note 1.)</span></span>
-   <span data-ttu-id="0c389-133">**MEDIATYPE \_ MPEG2 \_ PE**, **MEDIASUBTYPE \_ DTS** (vedere la nota 2).</span><span class="sxs-lookup"><span data-stu-id="0c389-133">**MEDIATYPE\_MPEG2\_PES**, **MEDIASUBTYPE\_DTS** (See Note 2.)</span></span>
-   <span data-ttu-id="0c389-134">**MEDIATYPE \_ MPEG2 \_ PE**, **MEDIASUBTYPE \_ DVD \_ LPCM \_ audio**</span><span class="sxs-lookup"><span data-stu-id="0c389-134">**MEDIATYPE\_MPEG2\_PES**, **MEDIASUBTYPE\_DVD\_LPCM\_AUDIO**</span></span>
-   <span data-ttu-id="0c389-135">**MEDIATYPE \_ MPEG2 \_ PE**, **\_ \_ audio MPEG2 MEDIASUBTYPE**</span><span class="sxs-lookup"><span data-stu-id="0c389-135">**MEDIATYPE\_MPEG2\_PES**, **MEDIASUBTYPE\_MPEG2\_AUDIO**</span></span>
-   <span data-ttu-id="0c389-136">**MEDIATYPE \_ Stream**, **MEDIASUBTYPE \_ Dolby \_ AC3** (vedere la nota 1).</span><span class="sxs-lookup"><span data-stu-id="0c389-136">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_DOLBY\_AC3** (See Note 1.)</span></span>
-   <span data-ttu-id="0c389-137">**MEDIATYPE \_ Flusso**, **MEDIASUBTYPE \_ MPEG1Audio**</span><span class="sxs-lookup"><span data-stu-id="0c389-137">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_MPEG1Audio**</span></span>
-   <span data-ttu-id="0c389-138">**MEDIATYPE \_ Flusso**, **MEDIASUBTYPE \_ \_ audio MPEG2**</span><span class="sxs-lookup"><span data-stu-id="0c389-138">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_MPEG2\_AUDIO**</span></span>

<span data-ttu-id="0c389-139">A partire da Windows 7, il filtro supporta anche i tipi di input seguenti:</span><span class="sxs-lookup"><span data-stu-id="0c389-139">Starting in Windows 7, the filter also supports the following input types:</span></span><br/>

-   <span data-ttu-id="0c389-140">**MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ Dolby \_ DDPLUS** (vedere la nota 1).</span><span class="sxs-lookup"><span data-stu-id="0c389-140">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_DOLBY\_DDPLUS** (See Note 1.)</span></span>
-   <span data-ttu-id="0c389-141">**MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ DTS2** (vedere la nota 2).</span><span class="sxs-lookup"><span data-stu-id="0c389-141">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_DTS2** (See Note 2.)</span></span>
-   <span data-ttu-id="0c389-142">**MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ DVD \_ LPCM \_ audio**</span><span class="sxs-lookup"><span data-stu-id="0c389-142">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_DVD\_LPCM\_AUDIO**</span></span>
-   <span data-ttu-id="0c389-143">**MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ DVM** (vedere la nota 1).</span><span class="sxs-lookup"><span data-stu-id="0c389-143">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_DVM** (See Note 1.)</span></span>
-   <span data-ttu-id="0c389-144">**MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ MPEG \_ ADTS \_ AAC**</span><span class="sxs-lookup"><span data-stu-id="0c389-144">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_MPEG\_ADTS\_AAC**</span></span>
-   <span data-ttu-id="0c389-145">**MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ MPEG \_ LOAS**</span><span class="sxs-lookup"><span data-stu-id="0c389-145">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_MPEG\_LOAS**</span></span>
-   <span data-ttu-id="0c389-146">**MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ MPEG1AudioPayload**</span><span class="sxs-lookup"><span data-stu-id="0c389-146">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_MPEG1AudioPayload**</span></span>
-   <span data-ttu-id="0c389-147">**MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ RAW \_ AAC1**</span><span class="sxs-lookup"><span data-stu-id="0c389-147">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_RAW\_AAC1**</span></span>
-   <span data-ttu-id="0c389-148">**MEDIATYPE \_ Stream**, **MEDIASUBTYPE \_ Dolby \_ DDPLUS** (vedere la nota 1).</span><span class="sxs-lookup"><span data-stu-id="0c389-148">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_DOLBY\_DDPLUS** (See Note 1.)</span></span>
-   <span data-ttu-id="0c389-149">**MEDIATYPE \_ Stream**, **MEDIASUBTYPE \_ MPEG \_ ADTS \_ AAC**</span><span class="sxs-lookup"><span data-stu-id="0c389-149">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_MPEG\_ADTS\_AAC**</span></span>
-   <span data-ttu-id="0c389-150">**MEDIATYPE \_ Stream**, **MEDIASUBTYPE \_ MPEG \_ LOAS**</span><span class="sxs-lookup"><span data-stu-id="0c389-150">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_MPEG\_LOAS**</span></span>

<span data-ttu-id="0c389-151">Il tipo di input può variare in modo dinamico durante il flusso.</span><span class="sxs-lookup"><span data-stu-id="0c389-151">The input type can change dynamically during streaming.</span></span><br/> <span data-ttu-id="0c389-152">Per ulteriori informazioni su questi tipi di supporti, vedere [**sottotipi audio**](audio-subtypes.md).</span><span class="sxs-lookup"><span data-stu-id="0c389-152">For more information about these media types, see [**Audio Subtypes**](audio-subtypes.md).</span></span><br/>

> [!Note]  
> 1. <span data-ttu-id="0c389-153">L'implementazione Microsoft della tecnologia Dolby Digital è limitata ai sensi del programma di licenza Dolby Digital per l'uso da parte delle applicazioni Microsoft.</span><span class="sxs-lookup"><span data-stu-id="0c389-153">The Microsoft implementation of the Dolby Digital technology is restricted under terms of the Dolby Digital licensing program to use by Microsoft applications.</span></span>

<br/>

> [!Note]  
> 2. <span data-ttu-id="0c389-154">Per l'input DTS (Digital Theater Systems), è supportato solo l'output S/PDIF (DTS su S/PDIF).</span><span class="sxs-lookup"><span data-stu-id="0c389-154">For Digital Theater Systems (DTS) input, only S/PDIF output is supported (DTS over S/PDIF).</span></span> <span data-ttu-id="0c389-155">La decodifica audio non è supportata.</span><span class="sxs-lookup"><span data-stu-id="0c389-155">Audio decoding is not supported.</span></span>

<br/>

<span data-ttu-id="0c389-156">Interfacce pin di input</span><span class="sxs-lookup"><span data-stu-id="0c389-156">Input Pin Interfaces</span></span>

[<span data-ttu-id="0c389-157">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="0c389-157">**ICodecAPI**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/> [<span data-ttu-id="0c389-158">**IKsPropertySet**</span><span class="sxs-lookup"><span data-stu-id="0c389-158">**IKsPropertySet**</span></span>](ikspropertyset.md)<br/> [<span data-ttu-id="0c389-159">**IMemInputPin**</span><span class="sxs-lookup"><span data-stu-id="0c389-159">**IMemInputPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [<span data-ttu-id="0c389-160">**IPin**</span><span class="sxs-lookup"><span data-stu-id="0c389-160">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [<span data-ttu-id="0c389-161">**IQualityControl**</span><span class="sxs-lookup"><span data-stu-id="0c389-161">**IQualityControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

<span data-ttu-id="0c389-162">Tipi di supporti pin di output</span><span class="sxs-lookup"><span data-stu-id="0c389-162">Output Pin Media Types</span></span>

<span data-ttu-id="0c389-163">In Windows Vista e versioni successive, il filtro supporta i tipi di output seguenti:</span><span class="sxs-lookup"><span data-stu-id="0c389-163">In Windows Vista and later, the filter supports the following output types:</span></span><br/>

-   <span data-ttu-id="0c389-164">**MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ Dolby \_ AC3 \_ SPDIF** (uguale al **\_ sottotipo KSDATAFORMAT \_ IEC61937 \_ Dolby \_ Digital**)</span><span class="sxs-lookup"><span data-stu-id="0c389-164">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_DOLBY\_AC3\_SPDIF** (same as **KSDATAFORMAT\_SUBTYPE\_IEC61937\_DOLBY\_DIGITAL**)</span></span>
-   <span data-ttu-id="0c389-165">**MEDIATYPE \_ Audio**, **\_ PCM MEDIASUBTYPE**</span><span class="sxs-lookup"><span data-stu-id="0c389-165">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_PCM**</span></span>

<span data-ttu-id="0c389-166">A partire da Windows 7, il filtro supporta anche i tipi di output seguenti:</span><span class="sxs-lookup"><span data-stu-id="0c389-166">Starting in Windows 7, the filter also supports the following output types:</span></span><br/>

-   <span data-ttu-id="0c389-167">**MEDIATYPE \_ Audio**, **\_ sottotipo KSDATAFORMAT \_ IEC61937 \_ DTS**</span><span class="sxs-lookup"><span data-stu-id="0c389-167">**MEDIATYPE\_Audio**, **KSDATAFORMAT\_SUBTYPE\_IEC61937\_DTS**</span></span>
-   <span data-ttu-id="0c389-168">**MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ IEEE \_ float**</span><span class="sxs-lookup"><span data-stu-id="0c389-168">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_IEEE\_FLOAT**</span></span>

<span data-ttu-id="0c389-169">Interfacce del PIN di output</span><span class="sxs-lookup"><span data-stu-id="0c389-169">Output Pin Interfaces</span></span>

[<span data-ttu-id="0c389-170">**IMediaSeeking**</span><span class="sxs-lookup"><span data-stu-id="0c389-170">**IMediaSeeking**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [<span data-ttu-id="0c389-171">**IPin**</span><span class="sxs-lookup"><span data-stu-id="0c389-171">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [<span data-ttu-id="0c389-172">**IQualityControl**</span><span class="sxs-lookup"><span data-stu-id="0c389-172">**IQualityControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

<span data-ttu-id="0c389-173">CLSID filtro</span><span class="sxs-lookup"><span data-stu-id="0c389-173">Filter CLSID</span></span>

<span data-ttu-id="0c389-174">**CLSID \_ CMPEG2AudDecoderDS** (dichiarata in wmcodecdsp. h)</span><span class="sxs-lookup"><span data-stu-id="0c389-174">**CLSID\_CMPEG2AudDecoderDS** (declared in wmcodecdsp.h)</span></span>

<span data-ttu-id="0c389-175">File eseguibile</span><span class="sxs-lookup"><span data-stu-id="0c389-175">Executable</span></span>

<span data-ttu-id="0c389-176">msmpeg2adec.dll</span><span class="sxs-lookup"><span data-stu-id="0c389-176">msmpeg2adec.dll</span></span>

[<span data-ttu-id="0c389-177">Merito</span><span class="sxs-lookup"><span data-stu-id="0c389-177">Merit</span></span>](merit.md)

<span data-ttu-id="0c389-178">Il **merito \_ NORMALE** -1</span><span class="sxs-lookup"><span data-stu-id="0c389-178">**MERIT\_NORMAL** - 1</span></span>

[<span data-ttu-id="0c389-179">Categoria filtro</span><span class="sxs-lookup"><span data-stu-id="0c389-179">Filter Category</span></span>](filter-categories.md)

<span data-ttu-id="0c389-180">**\_LEGACYAMFILTERCATEGORY CLSID**</span><span class="sxs-lookup"><span data-stu-id="0c389-180">**CLSID\_LegacyAmFilterCategory**</span></span>



 

> [!Note]  
> <span data-ttu-id="0c389-181">Una versione precedente della documentazione ha dichiarato che questo filtro può decodificare "MPEG-2 audio".</span><span class="sxs-lookup"><span data-stu-id="0c389-181">An earlier version of the documentation stated that this filter can decode "MPEG-2 audio."</span></span> <span data-ttu-id="0c389-182">Il filtro decodifica solo l'audio MPEG-2 compatibile con le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="0c389-182">The filter decodes only backward-compatible MPEG-2 audio.</span></span>

 

## <a name="remarks"></a><span data-ttu-id="0c389-183">Commenti</span><span class="sxs-lookup"><span data-stu-id="0c389-183">Remarks</span></span>

<span data-ttu-id="0c389-184">I flussi mono sono sempre decodificati in stereo.</span><span class="sxs-lookup"><span data-stu-id="0c389-184">Mono streams are always decoded to stereo.</span></span>

<span data-ttu-id="0c389-185">Per i flussi con una configurazione di canale di due o più altoparlanti, il decodificatore esegue una delle operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="0c389-185">For streams with a channel configuration of two or more speakers, the decoder does one of the following:</span></span>

-   <span data-ttu-id="0c389-186">Si mescola a sei canali, usando la configurazione comune del altoparlante 5,1.</span><span class="sxs-lookup"><span data-stu-id="0c389-186">Up-mixes to six channels, using the common 5.1 speaker configuration.</span></span>
-   <span data-ttu-id="0c389-187">Da downmixes a stereo.</span><span class="sxs-lookup"><span data-stu-id="0c389-187">Downmixes to stereo.</span></span>

<span data-ttu-id="0c389-188">Per selezionare una delle due opzioni, usare l'interfaccia [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) per impostare la proprietà [**AVDecCommonOutputFormat**](avdeccommonoutputformat-property.md) , prima di connettere i pin.</span><span class="sxs-lookup"><span data-stu-id="0c389-188">To select between these two options, use the [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) interface to set the [**AVDecCommonOutputFormat**](avdeccommonoutputformat-property.md) property, before connecting the pins.</span></span> <span data-ttu-id="0c389-189">In alternativa, quando l'applicazione compila il grafico del filtro, può impostare il tipo di supporto desiderato sul pin di output.</span><span class="sxs-lookup"><span data-stu-id="0c389-189">Alternatively, when the application builds the filter graph, it can set the desired media type on the output pin.</span></span>

### <a name="aac-decoding"></a><span data-ttu-id="0c389-190">Decodifica AAC</span><span class="sxs-lookup"><span data-stu-id="0c389-190">AAC Decoding</span></span>

<span data-ttu-id="0c389-191">Per AAC, il decodificatore presenta determinati vincoli di formato nell'input AAC compresso.</span><span class="sxs-lookup"><span data-stu-id="0c389-191">For AAC, the decoder has certain format constraints on the compressed AAC input.</span></span> <span data-ttu-id="0c389-192">Questi vincoli di formato sono identici a quelli del [**Decodificatore Media Foundation AAC**](../medfound/aac-decoder.md)e sono documentati nella sezione "[**vincoli di formato**](../medfound/aac-decoder.md)".</span><span class="sxs-lookup"><span data-stu-id="0c389-192">These format constraints are the same as the Media Foundation [**AAC Decoder**](../medfound/aac-decoder.md), and are documented in the section "[**Format Constraints**](../medfound/aac-decoder.md)".</span></span>

<span data-ttu-id="0c389-193">Il decodificatore DirectShow accetta anche tipi di input diversi rispetto al decodificatore Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="0c389-193">The DirectShow decoder also accepts different input types than the Media Foundation decoder.</span></span> <span data-ttu-id="0c389-194">Il decodificatore DirectShow supporta i tipi di input AAC seguenti:</span><span class="sxs-lookup"><span data-stu-id="0c389-194">The DirectShow decoder supports the following AAC input types:</span></span>

-   <span data-ttu-id="0c389-195">**MEDIASUBTYPE \_ \_AAC1 RAW**: AAC non elaborato, in genere disponibile in AVI o Matroska (. File MKV).</span><span class="sxs-lookup"><span data-stu-id="0c389-195">**MEDIASUBTYPE\_RAW\_AAC1**: Raw AAC, typically found in AVI or Matroska (.MKV) files.</span></span>
-   <span data-ttu-id="0c389-196">**MEDIASUBTYPE \_ MPEG \_ ADTS \_ AAC**: AAC in un flusso di trasporto dati audio (ADTS) per lo streaming.</span><span class="sxs-lookup"><span data-stu-id="0c389-196">**MEDIASUBTYPE\_MPEG\_ADTS\_AAC**: AAC in an Audio Data Transport Stream (ADTS) for streaming.</span></span>
-   <span data-ttu-id="0c389-197">**MEDIASUBTYPE \_ MPEG \_ LOAS**: flusso di trasporto con un livello di sincronizzazione (LOAS) e un livello multiplex (latm).</span><span class="sxs-lookup"><span data-stu-id="0c389-197">**MEDIASUBTYPE\_MPEG\_LOAS**: Transport stream with a synchronization layer (LOAS) and a multiplex layer (LATM).</span></span>

<span data-ttu-id="0c389-198">Il decodificatore Media Foundation supporta i tipi di input AAC seguenti:</span><span class="sxs-lookup"><span data-stu-id="0c389-198">The Media Foundation decoder supports the following AAC input types:</span></span>

-   <span data-ttu-id="0c389-199">MFAudioFormat \_ AAC (uguale a **MEDIASUBTYPE \_ MPEG \_ HEAAC**) per la riproduzione di file MP4.</span><span class="sxs-lookup"><span data-stu-id="0c389-199">MFAudioFormat\_AAC (same as **MEDIASUBTYPE\_MPEG\_HEAAC**) for MP4 file playback.</span></span>
-   <span data-ttu-id="0c389-200">**MEDIASUBTYPE \_ \_AAC1 non elaborati**.</span><span class="sxs-lookup"><span data-stu-id="0c389-200">**MEDIASUBTYPE\_RAW\_AAC1**.</span></span>

### <a name="property-sets"></a><span data-ttu-id="0c389-201">Set di proprietà</span><span class="sxs-lookup"><span data-stu-id="0c389-201">Property Sets</span></span>

<span data-ttu-id="0c389-202">Il pin di input del decodificatore supporta i set di proprietà seguenti tramite [**IKsPropertySet**](ikspropertyset.md):</span><span class="sxs-lookup"><span data-stu-id="0c389-202">The decoder's input pin supports the following property sets through [**IKsPropertySet**](ikspropertyset.md):</span></span>

-   [<span data-ttu-id="0c389-203">**Set di proprietà di protezione copia DVD**</span><span class="sxs-lookup"><span data-stu-id="0c389-203">**DVD Copy Protection Property Set**</span></span>](dvd-copy-protection-property-set.md)
-   <span data-ttu-id="0c389-204">[**Set di proprietà di modifica della frequenza**](rate-change-property-set.md).</span><span class="sxs-lookup"><span data-stu-id="0c389-204">[**Rate-Change Property Set**](rate-change-property-set.md).</span></span>

> [!Note]  
> <span data-ttu-id="0c389-205">A partire da Windows 7, il decodificatore supporta la modalità Trick tramite il set di proprietà rate-Change.</span><span class="sxs-lookup"><span data-stu-id="0c389-205">Starting in Windows 7, the decoder supports trick mode through the rate-change property set.</span></span> <span data-ttu-id="0c389-206">Supporta le frequenze di riproduzione nell'intervallo \[ 0,501 – 2,0 \] , dove 1,0 è la frequenza di riproduzione normale e 2,0 è il doppio della normale frequenza.</span><span class="sxs-lookup"><span data-stu-id="0c389-206">It supports playback rates in the range \[0.501 – 2.0\], where 1.0 is normal playback rate, and 2.0 is twice the normal rate.</span></span>

 

### <a name="codec-properties"></a><span data-ttu-id="0c389-207">Proprietà codec</span><span class="sxs-lookup"><span data-stu-id="0c389-207">Codec Properties</span></span>

<span data-ttu-id="0c389-208">Il pin di input del decodificatore supporta le seguenti proprietà tramite [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):</span><span class="sxs-lookup"><span data-stu-id="0c389-208">The decoder's input pin supports the following properties through [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):</span></span>



| <span data-ttu-id="0c389-209">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0c389-209">Property</span></span>                                                          | <span data-ttu-id="0c389-210">Richiede</span><span class="sxs-lookup"><span data-stu-id="0c389-210">Requires</span></span>                                                 |
|-------------------------------------------------------------------|----------------------------------------------------------|
| [<span data-ttu-id="0c389-211">**AVAudioChannelConfig**</span><span class="sxs-lookup"><span data-stu-id="0c389-211">**AVAudioChannelConfig**</span></span>](avaudiochannelconfig-property.md)     | <span data-ttu-id="0c389-212">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0c389-212">Windows Vista</span></span>                                            |
| [<span data-ttu-id="0c389-213">**AVAudioChannelCount**</span><span class="sxs-lookup"><span data-stu-id="0c389-213">**AVAudioChannelCount**</span></span>](avaudiochannelcount-property.md)       | <span data-ttu-id="0c389-214">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0c389-214">Windows Vista</span></span>                                            |
| [<span data-ttu-id="0c389-215">**AVAudioSampleRate**</span><span class="sxs-lookup"><span data-stu-id="0c389-215">**AVAudioSampleRate**</span></span>](avaudiosamplerate-property.md)           | <span data-ttu-id="0c389-216">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0c389-216">Windows Vista</span></span>                                            |
| [<span data-ttu-id="0c389-217">**AVDDSurroundMode**</span><span class="sxs-lookup"><span data-stu-id="0c389-217">**AVDDSurroundMode**</span></span>](avddsurroundmode-property.md)             | <span data-ttu-id="0c389-218">Solo Windows Vista; non supportato in Windows 7 o versioni successive.</span><span class="sxs-lookup"><span data-stu-id="0c389-218">Windows Vista only; not supported in Windows 7 or later.</span></span> |
| [<span data-ttu-id="0c389-219">**AVDecAudioDualMono**</span><span class="sxs-lookup"><span data-stu-id="0c389-219">**AVDecAudioDualMono**</span></span>](avdecaudiodualmono-property.md)         | <span data-ttu-id="0c389-220">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0c389-220">Windows Vista</span></span>                                            |
| [<span data-ttu-id="0c389-221">**AVDecCommonInputFormat**</span><span class="sxs-lookup"><span data-stu-id="0c389-221">**AVDecCommonInputFormat**</span></span>](avdeccommoninputformat-property.md) | <span data-ttu-id="0c389-222">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0c389-222">Windows Vista</span></span>                                            |
| [<span data-ttu-id="0c389-223">**AVDecCommonMeanBitRate**</span><span class="sxs-lookup"><span data-stu-id="0c389-223">**AVDecCommonMeanBitRate**</span></span>](avdeccommonmeanbitrate.md)          | <span data-ttu-id="0c389-224">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0c389-224">Windows 7</span></span>                                                |



 

<span data-ttu-id="0c389-225">Il filtro supporta le seguenti proprietà tramite [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):</span><span class="sxs-lookup"><span data-stu-id="0c389-225">The filter supports the following properties through [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):</span></span>



| <span data-ttu-id="0c389-226">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0c389-226">Property</span></span>                                                                          | <span data-ttu-id="0c389-227">Richiede</span><span class="sxs-lookup"><span data-stu-id="0c389-227">Requires</span></span>      |
|-----------------------------------------------------------------------------------|---------------|
| [<span data-ttu-id="0c389-228">**AVDecAACDownmixMode**</span><span class="sxs-lookup"><span data-stu-id="0c389-228">**AVDecAACDownmixMode**</span></span>](avdecaacdownmixmode-property.md)                       | <span data-ttu-id="0c389-229">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0c389-229">Windows 7</span></span>     |
| [<span data-ttu-id="0c389-230">**AVDecAudioDualMonoReproMode**</span><span class="sxs-lookup"><span data-stu-id="0c389-230">**AVDecAudioDualMonoReproMode**</span></span>](avdecaudiodualmonorepromode-property.md)       | <span data-ttu-id="0c389-231">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0c389-231">Windows Vista</span></span> |
| <span data-ttu-id="0c389-232">[**AVDecCommonOutputFormat**](avdeccommonoutputformat-property.md) (vedere la nota 3).</span><span class="sxs-lookup"><span data-stu-id="0c389-232">[**AVDecCommonOutputFormat**](avdeccommonoutputformat-property.md) (See Note 3.)</span></span> | <span data-ttu-id="0c389-233">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0c389-233">Windows Vista</span></span> |
| [<span data-ttu-id="0c389-234">**AVDecDDDynamicRangeScaleHigh**</span><span class="sxs-lookup"><span data-stu-id="0c389-234">**AVDecDDDynamicRangeScaleHigh**</span></span>](avdecdddynamicrangescalehigh-property.md)     | <span data-ttu-id="0c389-235">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0c389-235">Windows Vista</span></span> |
| [<span data-ttu-id="0c389-236">**AVDecDDDynamicRangeScaleLow**</span><span class="sxs-lookup"><span data-stu-id="0c389-236">**AVDecDDDynamicRangeScaleLow**</span></span>](avdecdddynamicrangescalelow-property.md)       | <span data-ttu-id="0c389-237">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0c389-237">Windows Vista</span></span> |
| [<span data-ttu-id="0c389-238">**AVDecDDOperationalMode**</span><span class="sxs-lookup"><span data-stu-id="0c389-238">**AVDecDDOperationalMode**</span></span>](avdecddoperationalmode-property.md)                 | <span data-ttu-id="0c389-239">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0c389-239">Windows Vista</span></span> |
| [<span data-ttu-id="0c389-240">**AVDecMmcssClass**</span><span class="sxs-lookup"><span data-stu-id="0c389-240">**AVDecMmcssClass**</span></span>](avdecmmcss-property.md)                                    | <span data-ttu-id="0c389-241">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0c389-241">Windows Vista</span></span> |
| [<span data-ttu-id="0c389-242">**AVDSPLoudnessEqualization**</span><span class="sxs-lookup"><span data-stu-id="0c389-242">**AVDSPLoudnessEqualization**</span></span>](avdsploudnessequalization-property.md)           | <span data-ttu-id="0c389-243">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0c389-243">Windows 7</span></span>     |
| [<span data-ttu-id="0c389-244">**AVDSPSpeakerFill**</span><span class="sxs-lookup"><span data-stu-id="0c389-244">**AVDSPSpeakerFill**</span></span>](avdspspeakerfill-property.md)                             | <span data-ttu-id="0c389-245">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0c389-245">Windows 7</span></span>     |



 

> [!Note]  
> 3. <span data-ttu-id="0c389-246">Prima di connettere il pin di output del decodificatore, è necessario impostare la proprietà [**AVDecCommonOutputFormat**](avdeccommonoutputformat-property.md) .</span><span class="sxs-lookup"><span data-stu-id="0c389-246">The [**AVDecCommonOutputFormat**](avdeccommonoutputformat-property.md) property must be set before the decoder's output pin is connected.</span></span> <span data-ttu-id="0c389-247">In caso contrario, la modifica non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="0c389-247">Otherwise, the change has no effect.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0c389-248">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0c389-248">Requirements</span></span>



| <span data-ttu-id="0c389-249">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c389-249">Requirement</span></span> | <span data-ttu-id="0c389-250">Valore</span><span class="sxs-lookup"><span data-stu-id="0c389-250">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c389-251">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0c389-251">Minimum supported client</span></span><br/> | <span data-ttu-id="0c389-252">Windows Vista Home Premium, Windows Vista Ultimate, \[ solo app desktop Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="0c389-252">Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="0c389-253">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0c389-253">Minimum supported server</span></span><br/> | <span data-ttu-id="0c389-254">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="0c389-254">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="0c389-255">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0c389-255">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c389-256"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c389-256"><dt>Wmcodecdsp.h</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="0c389-257">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0c389-257">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c389-258">**Sottotipi audio**</span><span class="sxs-lookup"><span data-stu-id="0c389-258">**Audio Subtypes**</span></span>](audio-subtypes.md)
</dt> <dt>

[<span data-ttu-id="0c389-259">Filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="0c389-259">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="0c389-260">**Tipi di supporti DVD**</span><span class="sxs-lookup"><span data-stu-id="0c389-260">**DVD Media Types**</span></span>](dvd-media-types.md)
</dt> </dl>

 

 
