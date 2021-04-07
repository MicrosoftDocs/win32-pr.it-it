---
description: Il filtro Microsoft MPEG-2 Encoder codifica audio e video MPEG-2 e multiplex i flussi per generare un flusso di programma MPEG-2 o un flusso di trasporto.
ms.assetid: 61e8918b-7f5a-4720-bb3b-df9ac7614894
title: Microsoft MPEG-2 encoder (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef5fad3b316db9ac4e47efcb9de761227cdd3279
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745967"
---
# <a name="microsoft-mpeg-2-encoder"></a><span data-ttu-id="f682f-103">Codificatore Microsoft MPEG-2</span><span class="sxs-lookup"><span data-stu-id="f682f-103">Microsoft MPEG-2 Encoder</span></span>

<span data-ttu-id="f682f-104">Il filtro Microsoft MPEG-2 Encoder codifica audio e video MPEG-2 e multiplex i flussi per generare un flusso di programma MPEG-2 o un flusso di trasporto.</span><span class="sxs-lookup"><span data-stu-id="f682f-104">The Microsoft MPEG-2 Encoder filter encodes MPEG-2 audio and video and multiplexes the streams to generate an MPEG-2 program stream or transport stream.</span></span>

> [!Note]  
> <span data-ttu-id="f682f-105">Questo filtro non è supportato nelle piattaforme basate su IA-64.</span><span class="sxs-lookup"><span data-stu-id="f682f-105">This filter is not supported on IA-64-based platforms.</span></span>

 



<span data-ttu-id="f682f-106">Informazioni sul filtro</span><span class="sxs-lookup"><span data-stu-id="f682f-106">Filter Information</span></span>

<span data-ttu-id="f682f-107">Interfacce di filtro</span><span class="sxs-lookup"><span data-stu-id="f682f-107">Filter Interfaces</span></span>

[<span data-ttu-id="f682f-108">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="f682f-108">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/> [<span data-ttu-id="f682f-109">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="f682f-109">**ICodecAPI**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/> <span data-ttu-id="f682f-110">**IEncoderAPI**</span><span class="sxs-lookup"><span data-stu-id="f682f-110">**IEncoderAPI**</span></span><br/> [<span data-ttu-id="f682f-111">**IMediaSeeking**</span><span class="sxs-lookup"><span data-stu-id="f682f-111">**IMediaSeeking**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [<span data-ttu-id="f682f-112">**IVideoEncoder**</span><span class="sxs-lookup"><span data-stu-id="f682f-112">**IVideoEncoder**</span></span>](/windows/win32/api/strmif/nn-strmif-ivideoencoder)<br/>

<span data-ttu-id="f682f-113">Tipi di supporti pin di input</span><span class="sxs-lookup"><span data-stu-id="f682f-113">Input Pin Media Types</span></span>

<span data-ttu-id="f682f-114">Vedere la sezione Osservazioni</span><span class="sxs-lookup"><span data-stu-id="f682f-114">See Remarks</span></span>

<span data-ttu-id="f682f-115">Interfacce pin di input</span><span class="sxs-lookup"><span data-stu-id="f682f-115">Input Pin Interfaces</span></span>

[<span data-ttu-id="f682f-116">**IMemInputPin**</span><span class="sxs-lookup"><span data-stu-id="f682f-116">**IMemInputPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [<span data-ttu-id="f682f-117">**IPin**</span><span class="sxs-lookup"><span data-stu-id="f682f-117">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [<span data-ttu-id="f682f-118">**IQualityControl**</span><span class="sxs-lookup"><span data-stu-id="f682f-118">**IQualityControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

<span data-ttu-id="f682f-119">Tipi di supporti pin di output</span><span class="sxs-lookup"><span data-stu-id="f682f-119">Output Pin Media Types</span></span>

<span data-ttu-id="f682f-120">Vedere la sezione Osservazioni</span><span class="sxs-lookup"><span data-stu-id="f682f-120">See Remarks</span></span>

<span data-ttu-id="f682f-121">Interfacce del PIN di output</span><span class="sxs-lookup"><span data-stu-id="f682f-121">Output Pin Interfaces</span></span>

[<span data-ttu-id="f682f-122">**IMediaSeeking**</span><span class="sxs-lookup"><span data-stu-id="f682f-122">**IMediaSeeking**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [<span data-ttu-id="f682f-123">**IPin**</span><span class="sxs-lookup"><span data-stu-id="f682f-123">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [<span data-ttu-id="f682f-124">**IQualityControl**</span><span class="sxs-lookup"><span data-stu-id="f682f-124">**IQualityControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

<span data-ttu-id="f682f-125">CLSID filtro</span><span class="sxs-lookup"><span data-stu-id="f682f-125">Filter CLSID</span></span>

<span data-ttu-id="f682f-126">**CLSID \_ CMPEG2EncoderDS** (dichiarata in wmcodecdsp. h)</span><span class="sxs-lookup"><span data-stu-id="f682f-126">**CLSID\_CMPEG2EncoderDS** (declared in wmcodecdsp.h)</span></span>

<span data-ttu-id="f682f-127">File eseguibile</span><span class="sxs-lookup"><span data-stu-id="f682f-127">Executable</span></span>

<span data-ttu-id="f682f-128">msmpeg2enc.dll</span><span class="sxs-lookup"><span data-stu-id="f682f-128">msmpeg2enc.dll</span></span>

[<span data-ttu-id="f682f-129">Merito</span><span class="sxs-lookup"><span data-stu-id="f682f-129">Merit</span></span>](merit.md)

<span data-ttu-id="f682f-130">**il merito non viene \_ \_ \_ utilizzato**</span><span class="sxs-lookup"><span data-stu-id="f682f-130">**MERIT\_DO\_NOT\_USE**</span></span>

[<span data-ttu-id="f682f-131">Categoria filtro</span><span class="sxs-lookup"><span data-stu-id="f682f-131">Filter Category</span></span>](filter-categories.md)

<span data-ttu-id="f682f-132">**\_LEGACYAMFILTERCATEGORY CLSID**</span><span class="sxs-lookup"><span data-stu-id="f682f-132">**CLSID\_LegacyAmFilterCategory**</span></span>



 

## <a name="remarks"></a><span data-ttu-id="f682f-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="f682f-133">Remarks</span></span>

<span data-ttu-id="f682f-134">Questo filtro combina la funzionalità di codifica di altri due filtri:</span><span class="sxs-lookup"><span data-stu-id="f682f-134">This filter combines the encoding functionality of two other filters:</span></span>

-   [<span data-ttu-id="f682f-135">**Codificatore audio Microsoft MPEG-2**</span><span class="sxs-lookup"><span data-stu-id="f682f-135">**Microsoft MPEG-2 Audio Encoder**</span></span>](microsoft-mpeg-2-audio-encoder.md)
-   [<span data-ttu-id="f682f-136">**Codificatore video Microsoft MPEG-2**</span><span class="sxs-lookup"><span data-stu-id="f682f-136">**Microsoft MPEG-2 Video Encoder**</span></span>](microsoft-mpeg-2-video-encoder.md)

<span data-ttu-id="f682f-137">Ad eccezione di quanto indicato, questo filtro supporta le stesse funzionalità di codifica di questi due codificatori.</span><span class="sxs-lookup"><span data-stu-id="f682f-137">Except as noted, this filter supports the same encoding features as those two encoders.</span></span>

<span data-ttu-id="f682f-138">Inizialmente il filtro ha un pin di input, che può accettare l'input audio o video.</span><span class="sxs-lookup"><span data-stu-id="f682f-138">Initially the filter has one input pin, which can accept audio or video input.</span></span> <span data-ttu-id="f682f-139">Quando tale PIN è connesso, il filtro crea un secondo pin di input.</span><span class="sxs-lookup"><span data-stu-id="f682f-139">When that pin is connected, the filter creates a second input pin.</span></span> <span data-ttu-id="f682f-140">Se il primo pin di input riceve audio, il secondo pin di input accetta solo video e viceversa.</span><span class="sxs-lookup"><span data-stu-id="f682f-140">If the first input pin receives audio, the second input pin accepts only video, and vice versa.</span></span> <span data-ttu-id="f682f-141">Ogni pin di input supporta gli stessi tipi di supporti del filtro del codificatore corrispondente.</span><span class="sxs-lookup"><span data-stu-id="f682f-141">Each input pin supports the same media types as the corresponding encoder filter.</span></span>

<span data-ttu-id="f682f-142">Se è connesso un solo pin di input, il filtro supporta gli stessi tipi di output del codificatore audio o video corrispondente.</span><span class="sxs-lookup"><span data-stu-id="f682f-142">If only one input pin is connected, the filter supports the same output types as the corresponding audio or video encoder.</span></span> <span data-ttu-id="f682f-143">Se entrambi i pin sono connessi, il filtro supporta i tipi di output seguenti:</span><span class="sxs-lookup"><span data-stu-id="f682f-143">If both pins are connected, the filter supports the following kinds of output:</span></span>

-   <span data-ttu-id="f682f-144">Audio-oggetto visivo in un flusso di programma MPEG-2</span><span class="sxs-lookup"><span data-stu-id="f682f-144">Audio-visual in an MPEG-2 program stream</span></span>
-   <span data-ttu-id="f682f-145">Audio-oggetto visivo in un flusso di trasporto MPEG-2</span><span class="sxs-lookup"><span data-stu-id="f682f-145">Audio-visual in an MPEG-2 transport stream</span></span>

<span data-ttu-id="f682f-146">Questi corrispondono ai tipi di output seguenti:</span><span class="sxs-lookup"><span data-stu-id="f682f-146">These correspond to the following output types:</span></span>

-   <span data-ttu-id="f682f-147">**MEDIATYPE \_ Flusso**, **\_ \_ programma MEDIASUBTYPE MPEG2**</span><span class="sxs-lookup"><span data-stu-id="f682f-147">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_MPEG2\_PROGRAM**</span></span>
-   <span data-ttu-id="f682f-148">**MEDIATYPE \_ Flusso**, **\_ \_ trasporto MPEG2 MEDIASUBTYPE**</span><span class="sxs-lookup"><span data-stu-id="f682f-148">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_MPEG2\_TRANSPORT**</span></span>

<span data-ttu-id="f682f-149">Questo filtro non può eseguire il multiplexing di flussi codificati in precedenza.</span><span class="sxs-lookup"><span data-stu-id="f682f-149">This filter cannot multiplex streams that were previously encoded.</span></span> <span data-ttu-id="f682f-150">I flussi di input devono essere file audio/video non compressi, che vengono codificati dal filtro prima del multiplexing.</span><span class="sxs-lookup"><span data-stu-id="f682f-150">The input streams must be uncompressed audio/video, which the filter encodes before multiplexing.</span></span> <span data-ttu-id="f682f-151">Il flusso multiplexato è limitato a un solo programma, contenente un massimo di un audio e un flusso video.</span><span class="sxs-lookup"><span data-stu-id="f682f-151">The multiplexed stream is limited to one program, containing up to one audio and one video stream.</span></span>

### <a name="codec-properties"></a><span data-ttu-id="f682f-152">Proprietà codec</span><span class="sxs-lookup"><span data-stu-id="f682f-152">Codec Properties</span></span>

<span data-ttu-id="f682f-153">Il filtro supporta le proprietà combinate dei filtri [**MPEG-2 audio encoder**](microsoft-mpeg-2-audio-encoder.md) e [**MPEG-2 video encoder**](microsoft-mpeg-2-video-encoder.md) , con la differenza seguente:</span><span class="sxs-lookup"><span data-stu-id="f682f-153">The filter supports the combined properties of the [**MPEG-2 Audio Encoder**](microsoft-mpeg-2-audio-encoder.md) and [**MPEG-2 Video Encoder**](microsoft-mpeg-2-video-encoder.md) filters, with the following difference:</span></span>

-   <span data-ttu-id="f682f-154">La proprietà [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md) imposta la velocità in bit media per il flusso video.</span><span class="sxs-lookup"><span data-stu-id="f682f-154">The [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md) property sets the average bit rate for the video stream.</span></span>
-   <span data-ttu-id="f682f-155">La proprietà [**AVEncAudioMeanBitRate**](avencaudiomeanbitrate.md) imposta la velocità in bit media per il flusso audio.</span><span class="sxs-lookup"><span data-stu-id="f682f-155">The [**AVEncAudioMeanBitRate**](avencaudiomeanbitrate.md) property sets the average bit rate for the audio stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="f682f-156">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f682f-156">Requirements</span></span>



| <span data-ttu-id="f682f-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="f682f-157">Requirement</span></span> | <span data-ttu-id="f682f-158">Valore</span><span class="sxs-lookup"><span data-stu-id="f682f-158">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f682f-159">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f682f-159">Minimum supported client</span></span><br/> | <span data-ttu-id="f682f-160">Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 Home Premium, Windows 7 Professional, Windows 7 Enterprise, Windows 7 Ultimate \[ desktop apps\]</span><span class="sxs-lookup"><span data-stu-id="f682f-160">Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 Home Premium, Windows 7 Professional, Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="f682f-161">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f682f-161">Minimum supported server</span></span><br/> | <span data-ttu-id="f682f-162">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="f682f-162">None supported</span></span><br/>                                                                                                                                                     |
| <span data-ttu-id="f682f-163">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f682f-163">Header</span></span><br/>                   | <dl> <span data-ttu-id="f682f-164"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f682f-164"><dt>Wmcodecdsp.h</dt></span></span> </dl>                                                                                       |



## <a name="see-also"></a><span data-ttu-id="f682f-165">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f682f-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f682f-166">Filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="f682f-166">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 
