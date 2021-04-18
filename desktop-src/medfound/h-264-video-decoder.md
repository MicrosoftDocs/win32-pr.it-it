---
description: Il decodificatore Media Foundation H. 264 video è una trasformazione Media Foundation che supporta la decodifica dei profili Baseline, Main e High, fino al livello 5,1.
ms.assetid: 783a3618-981a-4573-9e9e-ebf5eeb75d06
title: Decoder video H. 264
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75c4713b1a4e36d1ba085b2239c24ca0f6e4fae0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484053"
---
# <a name="h264-video-decoder"></a><span data-ttu-id="6136e-103">Decoder video H. 264</span><span class="sxs-lookup"><span data-stu-id="6136e-103">H.264 Video Decoder</span></span>

<span data-ttu-id="6136e-104">Il decodificatore Media Foundation H. 264 video è una [trasformazione Media Foundation](media-foundation-transforms.md) che supporta la decodifica dei profili Baseline, Main e High, fino al livello 5,1.</span><span class="sxs-lookup"><span data-stu-id="6136e-104">The Media Foundation H.264 video decoder is a [Media Foundation Transform](media-foundation-transforms.md) that supports decoding of Baseline, Main, and High profiles, up to level 5.1.</span></span>

<span data-ttu-id="6136e-105">Il decodificatore video H. 264 espone le interfacce seguenti.</span><span class="sxs-lookup"><span data-stu-id="6136e-105">The H.264 video decoder exposes the following interfaces.</span></span>

-   <span data-ttu-id="6136e-106">[**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) (supportato in Windows 8)</span><span class="sxs-lookup"><span data-stu-id="6136e-106">[**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) (supported in Windows 8)</span></span>
-   [<span data-ttu-id="6136e-107">**IMFGetService**</span><span class="sxs-lookup"><span data-stu-id="6136e-107">**IMFGetService**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [<span data-ttu-id="6136e-108">**IMFQualityAdvise**</span><span class="sxs-lookup"><span data-stu-id="6136e-108">**IMFQualityAdvise**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)
-   [<span data-ttu-id="6136e-109">**IMFQualityAdvise2**</span><span class="sxs-lookup"><span data-stu-id="6136e-109">**IMFQualityAdvise2**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2)
-   [<span data-ttu-id="6136e-110">**IMFRateControl**</span><span class="sxs-lookup"><span data-stu-id="6136e-110">**IMFRateControl**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)
-   [<span data-ttu-id="6136e-111">**IMFRateSupport**</span><span class="sxs-lookup"><span data-stu-id="6136e-111">**IMFRateSupport**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)
-   [<span data-ttu-id="6136e-112">**IMFRealTimeClient**</span><span class="sxs-lookup"><span data-stu-id="6136e-112">**IMFRealTimeClient**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient)
-   [<span data-ttu-id="6136e-113">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="6136e-113">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

<span data-ttu-id="6136e-114">Per creare un'istanza del decodificatore, eseguire una delle operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="6136e-114">To create an instance of the decoder, do one of the following:</span></span>

-   <span data-ttu-id="6136e-115">Chiamare la funzione [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) o [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .</span><span class="sxs-lookup"><span data-stu-id="6136e-115">Call the [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) or [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function.</span></span>
-   <span data-ttu-id="6136e-116">Chiamare [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="6136e-116">Call [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span> <span data-ttu-id="6136e-117">Il CLSID per il decodificatore è **CLSID \_ CMSH264DecoderMFT**, dichiarato in wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="6136e-117">The CLSID for the decoder is **CLSID\_CMSH264DecoderMFT**, declared in wmcodecdsp.h.</span></span>

## <a name="input-types"></a><span data-ttu-id="6136e-118">Tipi di input</span><span class="sxs-lookup"><span data-stu-id="6136e-118">Input Types</span></span>

<span data-ttu-id="6136e-119">Il tipo di input deve contenere almeno i due attributi seguenti:</span><span class="sxs-lookup"><span data-stu-id="6136e-119">The input type must contain at least the following two attributes:</span></span>



| <span data-ttu-id="6136e-120">Attributo</span><span class="sxs-lookup"><span data-stu-id="6136e-120">Attribute</span></span>                                                 | <span data-ttu-id="6136e-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6136e-121">Description</span></span>                                                                                   |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6136e-122">**\_ \_ tipo principale MF \_ mt**</span><span class="sxs-lookup"><span data-stu-id="6136e-122">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md) | <span data-ttu-id="6136e-123">**Video di MFMediaType \_**</span><span class="sxs-lookup"><span data-stu-id="6136e-123">**MFMediaType\_Video**</span></span>                                                                        |
| [<span data-ttu-id="6136e-124">**sottotipo MF \_ mt \_**</span><span class="sxs-lookup"><span data-stu-id="6136e-124">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)        | <span data-ttu-id="6136e-125">[MFVideoFormat \_ H264](video-subtype-guids.md) o MFVideoFormat \_ H264 \_ es</span><span class="sxs-lookup"><span data-stu-id="6136e-125">[MFVideoFormat\_H264](video-subtype-guids.md) or MFVideoFormat\_H264\_ES</span></span> |



 

<span data-ttu-id="6136e-126">Se il tipo di input contiene solo questi due attributi, il decodificatore offrirà un tipo di output predefinito, che funge da segnaposto.</span><span class="sxs-lookup"><span data-stu-id="6136e-126">If the input type contains only these two attributes, the decoder will offer a default output type, which acts as a placeholder.</span></span> <span data-ttu-id="6136e-127">Quando il decodificatore riceve un numero di campioni di input sufficiente per produrre un frame di output, segnala una modifica di formato restituendo **MF \_ E \_ Transform \_ Stream \_ Change** da [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).</span><span class="sxs-lookup"><span data-stu-id="6136e-127">When the decoder receives enough input samples to produce an output frame, it signals a format change by returning **MF\_E\_TRANSFORM\_STREAM\_CHANGE** from [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).</span></span> <span data-ttu-id="6136e-128">Vedere la documentazione di **ProcessOutput** per informazioni dettagliate sulla gestione delle modifiche del formato.</span><span class="sxs-lookup"><span data-stu-id="6136e-128">See the **ProcessOutput** documentation for details about handling format changes.</span></span>

<span data-ttu-id="6136e-129">Per evitare una modifica del formato iniziale, fornire quante più informazioni possibile nel tipo di input, tra cui:</span><span class="sxs-lookup"><span data-stu-id="6136e-129">To avoid an initial format change, provide as much information in the input type as possible, including:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6136e-130">Attributo</span><span class="sxs-lookup"><span data-stu-id="6136e-130">Attribute</span></span></th>
<th><span data-ttu-id="6136e-131">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6136e-131">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6136e-132"><a href="mf-mt-frame-rate-attribute.md"><strong>MF_MT_FRAME_RATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="6136e-132"><a href="mf-mt-frame-rate-attribute.md"><strong>MF_MT_FRAME_RATE</strong></a></span></span></td>
<td><span data-ttu-id="6136e-133">Frequenza di fotogrammi.</span><span class="sxs-lookup"><span data-stu-id="6136e-133">Frame rate.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6136e-134"><a href="mf-mt-frame-size-attribute.md"><strong>MF_MT_FRAME_SIZE</strong></a></span><span class="sxs-lookup"><span data-stu-id="6136e-134"><a href="mf-mt-frame-size-attribute.md"><strong>MF_MT_FRAME_SIZE</strong></a></span></span></td>
<td><span data-ttu-id="6136e-135">Dimensioni del frame.</span><span class="sxs-lookup"><span data-stu-id="6136e-135">Frame dimensions.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6136e-136"><a href="mf-mt-interlace-mode-attribute.md"><strong>MF_MT_INTERLACE_MODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="6136e-136"><a href="mf-mt-interlace-mode-attribute.md"><strong>MF_MT_INTERLACE_MODE</strong></a></span></span></td>
<td><span data-ttu-id="6136e-137">Modalità interlacciamento.</span><span class="sxs-lookup"><span data-stu-id="6136e-137">Interlace mode.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="6136e-138">Nel video H. 264 la struttura interlacciata può variare in modo dinamico, quindi il valore consigliato di questo attributo viene <strong>MFVideoInterlace_MixedInterlaceOrProgressive</strong>.</span><span class="sxs-lookup"><span data-stu-id="6136e-138">In H.264 video, the interlace structure can change dynamically, so the recommended value of this attribute is <strong>MFVideoInterlace_MixedInterlaceOrProgressive</strong>.</span></span> <span data-ttu-id="6136e-139">Le informazioni interlacciate nel flusso elementare video hanno la precedenza sul tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="6136e-139">Interlace information in the video elementary stream takes precedence over the media type.</span></span> <span data-ttu-id="6136e-140">Per altre informazioni, vedere <a href="video-interlacing.md">interlacciamento video</a>.</span><span class="sxs-lookup"><span data-stu-id="6136e-140">For more information, see <a href="video-interlacing.md">Video Interlacing</a>.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6136e-141"><a href="mf-mt-pixel-aspect-ratio-attribute.md"><strong>MF_MT_PIXEL_ASPECT_RATIO</strong></a></span><span class="sxs-lookup"><span data-stu-id="6136e-141"><a href="mf-mt-pixel-aspect-ratio-attribute.md"><strong>MF_MT_PIXEL_ASPECT_RATIO</strong></a></span></span></td>
<td><span data-ttu-id="6136e-142">Proporzioni pixel.</span><span class="sxs-lookup"><span data-stu-id="6136e-142">Pixel aspect ratio.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="6136e-143">Il tipo di input deve essere impostato prima del tipo di output.</span><span class="sxs-lookup"><span data-stu-id="6136e-143">The input type must be set before the output type.</span></span> <span data-ttu-id="6136e-144">Fino a quando non viene impostato il tipo di input, il metodo [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) del codificatore restituisce il **tipo di \_ trasformazione MF E \_ \_ \_ non \_ impostato**.</span><span class="sxs-lookup"><span data-stu-id="6136e-144">Until the input type is set, the encoder's [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) method returns **MF\_E\_TRANSFORM\_TYPE\_NOT\_SET**.</span></span>

## <a name="output-types"></a><span data-ttu-id="6136e-145">Tipi di output</span><span class="sxs-lookup"><span data-stu-id="6136e-145">Output Types</span></span>

<span data-ttu-id="6136e-146">Il decodificatore supporta i sottotipi di output seguenti:</span><span class="sxs-lookup"><span data-stu-id="6136e-146">The decoder supports the following output subtypes:</span></span>

-   <span data-ttu-id="6136e-147">**\_I420 MFVideoFormat**</span><span class="sxs-lookup"><span data-stu-id="6136e-147">**MFVideoFormat\_I420**</span></span>
-   <span data-ttu-id="6136e-148">**\_IYUV MFVideoFormat**</span><span class="sxs-lookup"><span data-stu-id="6136e-148">**MFVideoFormat\_IYUV**</span></span>
-   <span data-ttu-id="6136e-149">**\_NV12 MFVideoFormat**</span><span class="sxs-lookup"><span data-stu-id="6136e-149">**MFVideoFormat\_NV12**</span></span>
-   <span data-ttu-id="6136e-150">**\_YUY2 MFVideoFormat**</span><span class="sxs-lookup"><span data-stu-id="6136e-150">**MFVideoFormat\_YUY2**</span></span>
-   <span data-ttu-id="6136e-151">**\_YV12 MFVideoFormat**</span><span class="sxs-lookup"><span data-stu-id="6136e-151">**MFVideoFormat\_YV12**</span></span>

<span data-ttu-id="6136e-152">Per altre informazioni su questi sottotipi, vedere [GUID del sottotipo video](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="6136e-152">For more information about these subtypes, see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>

## <a name="transform-attributes"></a><span data-ttu-id="6136e-153">Attributi di trasformazione</span><span class="sxs-lookup"><span data-stu-id="6136e-153">Transform Attributes</span></span>

<span data-ttu-id="6136e-154">Il decodificatore H. 264 implementa il metodo [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) .</span><span class="sxs-lookup"><span data-stu-id="6136e-154">The H.264 decoder implements the [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) method.</span></span> <span data-ttu-id="6136e-155">Le applicazioni possono utilizzare questo metodo per ottenere o impostare gli attributi seguenti.</span><span class="sxs-lookup"><span data-stu-id="6136e-155">Applications can use this method to get or set the following attributes.</span></span>



| <span data-ttu-id="6136e-156">Attributo</span><span class="sxs-lookup"><span data-stu-id="6136e-156">Attribute</span></span>                                                                                       | <span data-ttu-id="6136e-157">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6136e-157">Description</span></span>                                                                                |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6136e-158">Codecapis \_ AVDecVideoAcceleration \_ H264</span><span class="sxs-lookup"><span data-stu-id="6136e-158">CODECAPI\_AVDecVideoAcceleration\_H264</span></span>](../directshow/avdecvideoacceleration-h264-property.md)            | <span data-ttu-id="6136e-159">Abilita o Disabilita l'accelerazione hardware.</span><span class="sxs-lookup"><span data-stu-id="6136e-159">Enables or disables hardware acceleration.</span></span>                                                 |
| [<span data-ttu-id="6136e-160">Codecapis \_ AVDecVideoThumbnailGenerationMode</span><span class="sxs-lookup"><span data-stu-id="6136e-160">CODECAPI\_AVDecVideoThumbnailGenerationMode</span></span>](../directshow/avdecvideothumbnailgenerationmode-property.md) | <span data-ttu-id="6136e-161">Abilita o Disabilita la modalità di generazione delle anteprime.</span><span class="sxs-lookup"><span data-stu-id="6136e-161">Enables or disables thumbnail generation mode.</span></span>                                             |
| [<span data-ttu-id="6136e-162">\_Compatibile con \_ D3D \_</span><span class="sxs-lookup"><span data-stu-id="6136e-162">MF\_SA\_D3D\_AWARE</span></span>](mf-sa-d3d-aware-attribute.md)                                             | <span data-ttu-id="6136e-163">Indica che il decodificatore supporta l'accelerazione video DirectX (DXVA).</span><span class="sxs-lookup"><span data-stu-id="6136e-163">Indicates that the decoder supports DirectX Video Acceleration (DXVA).</span></span> <span data-ttu-id="6136e-164">Considera come di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="6136e-164">Treat as read-only.</span></span> |



 

<span data-ttu-id="6136e-165">In Windows 8, il decodificatore H. 264 supporta anche gli attributi seguenti.</span><span class="sxs-lookup"><span data-stu-id="6136e-165">In Windows 8, the H.264 decoder also supports the following attributes.</span></span>



| <span data-ttu-id="6136e-166">Attributo</span><span class="sxs-lookup"><span data-stu-id="6136e-166">Attribute</span></span>                                                                                                     | <span data-ttu-id="6136e-167">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6136e-167">Description</span></span>                                                                                                 |
|---------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6136e-168">Codecapis \_ AVLowLatencyMode</span><span class="sxs-lookup"><span data-stu-id="6136e-168">CODECAPI\_AVLowLatencyMode</span></span>](codecapi-avlowlatencymode.md)                                                   | <span data-ttu-id="6136e-169">Abilita o Disabilita la modalità di decodifica a bassa latenza.</span><span class="sxs-lookup"><span data-stu-id="6136e-169">Enables or disables low-latency decoding mode.</span></span>                                                              |
| [<span data-ttu-id="6136e-170">Codecapis \_ AVDecNumWorkerThreads</span><span class="sxs-lookup"><span data-stu-id="6136e-170">CODECAPI\_AVDecNumWorkerThreads</span></span>](codecapi-avdecnumworkerthreads.md)                                         | <span data-ttu-id="6136e-171">Imposta il numero di thread di lavoro utilizzati dal decodificatore.</span><span class="sxs-lookup"><span data-stu-id="6136e-171">Sets the number of worker threads used by the decoder.</span></span>                                                      |
| [<span data-ttu-id="6136e-172">Codecapis \_ AVDecVideoMaxCodedWidth</span><span class="sxs-lookup"><span data-stu-id="6136e-172">CODECAPI\_AVDecVideoMaxCodedWidth</span></span>](codecapi-avdecvideomaxcodedwidth.md)                                     | <span data-ttu-id="6136e-173">Imposta la larghezza massima dell'immagine che il decodificatore accetterà come tipo di input.</span><span class="sxs-lookup"><span data-stu-id="6136e-173">Sets the maximum picture width that the decoder will accept as an input type.</span></span>                               |
| [<span data-ttu-id="6136e-174">Codecapis \_ AVDecVideoMaxCodedHeight</span><span class="sxs-lookup"><span data-stu-id="6136e-174">CODECAPI\_AVDecVideoMaxCodedHeight</span></span>](codecapi-avdecvideomaxcodedheight.md)                                   | <span data-ttu-id="6136e-175">Imposta l'altezza massima dell'immagine che il decodificatore accetterà come tipo di input.</span><span class="sxs-lookup"><span data-stu-id="6136e-175">Sets the maximum picture height that the decoder will accept as an input type.</span></span>                              |
| [<span data-ttu-id="6136e-176">\_ \_ numero minimo di \_ campioni di output MF \_ sa \_</span><span class="sxs-lookup"><span data-stu-id="6136e-176">MF\_SA\_MINIMUM\_OUTPUT\_SAMPLE\_COUNT</span></span>](mf-sa-minimum-output-sample-count.md)                               | <span data-ttu-id="6136e-177">Specifica il numero massimo di campioni di output.</span><span class="sxs-lookup"><span data-stu-id="6136e-177">Specifies the maximum number of output samples.</span></span>                                                             |
| [<span data-ttu-id="6136e-178">il \_ decodificatore MFT \_ espone i \_ \_ tipi \_ di output in \_ \_ ordine nativo</span><span class="sxs-lookup"><span data-stu-id="6136e-178">MFT\_DECODER\_EXPOSE\_OUTPUT\_TYPES\_IN\_NATIVE\_ORDER</span></span>](mft-decoder-expose-output-types-in-native-order.md) | <span data-ttu-id="6136e-179">Specifica se un decodificatore espone i tipi di output IYUV/I420 (adatti per la transcodifica) prima di altri formati.</span><span class="sxs-lookup"><span data-stu-id="6136e-179">Specifies whether a decoder exposes IYUV/I420 output types (suitable for transcoding) before other formats.</span></span> |



 

<span data-ttu-id="6136e-180">In Windows 8, il decodificatore H. 264 supporta l'interfaccia [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) .</span><span class="sxs-lookup"><span data-stu-id="6136e-180">In Windows 8, the H.264 decoder supports the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface.</span></span> <span data-ttu-id="6136e-181">Questa interfaccia fornisce un'API alternativate per l'impostazione delle proprietà dei codec seguenti.</span><span class="sxs-lookup"><span data-stu-id="6136e-181">This interface provides an alternativate API for setting the following codec properties.</span></span>

-   [<span data-ttu-id="6136e-182">Codecapis \_ AVDecVideoMaxCodedWidth</span><span class="sxs-lookup"><span data-stu-id="6136e-182">CODECAPI\_AVDecVideoMaxCodedWidth</span></span>](codecapi-avdecvideomaxcodedwidth.md)
-   [<span data-ttu-id="6136e-183">Codecapis \_ AVDecVideoAcceleration \_ H264</span><span class="sxs-lookup"><span data-stu-id="6136e-183">CODECAPI\_AVDecVideoAcceleration\_H264</span></span>](../directshow/avdecvideoacceleration-h264-property.md)
-   [<span data-ttu-id="6136e-184">Codecapis \_ AVDecVideoMaxCodedHeight</span><span class="sxs-lookup"><span data-stu-id="6136e-184">CODECAPI\_AVDecVideoMaxCodedHeight</span></span>](codecapi-avdecvideomaxcodedheight.md)
-   [<span data-ttu-id="6136e-185">Codecapis \_ AVDecVideoMaxCodedWidth</span><span class="sxs-lookup"><span data-stu-id="6136e-185">CODECAPI\_AVDecVideoMaxCodedWidth</span></span>](codecapi-avdecvideomaxcodedwidth.md)
-   [<span data-ttu-id="6136e-186">Codecapis \_ AVDecVideoThumbnailGenerationMode</span><span class="sxs-lookup"><span data-stu-id="6136e-186">CODECAPI\_AVDecVideoThumbnailGenerationMode</span></span>](../directshow/avdecvideothumbnailgenerationmode-property.md)

## <a name="format-constraints"></a><span data-ttu-id="6136e-187">Vincoli di formato</span><span class="sxs-lookup"><span data-stu-id="6136e-187">Format Constraints</span></span>

<span data-ttu-id="6136e-188">Il decodificatore supporta i formati seguenti:</span><span class="sxs-lookup"><span data-stu-id="6136e-188">The decoder supports the following formats:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6136e-189">Profili/livelli</span><span class="sxs-lookup"><span data-stu-id="6136e-189">Profiles/Levels</span></span></td>
<td><span data-ttu-id="6136e-190">Profili Baseline, Main e High, fino al livello 5,1.</span><span class="sxs-lookup"><span data-stu-id="6136e-190">Baseline, Main, and High profiles, up to level 5.1.</span></span> <span data-ttu-id="6136e-191">Per informazioni dettagliate, vedere la specifica ITU-T H. 264.</span><span class="sxs-lookup"><span data-stu-id="6136e-191">(See ITU-T H.264 specification for details.)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6136e-192">Formati Chroma</span><span class="sxs-lookup"><span data-stu-id="6136e-192">Chroma Formats</span></span></td>
<td><span data-ttu-id="6136e-193">4:2:0 Chroma o monocromatico</span><span class="sxs-lookup"><span data-stu-id="6136e-193">4:2:0 chroma or monochrome</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6136e-194">Risoluzione minima</span><span class="sxs-lookup"><span data-stu-id="6136e-194">Minimum Resolution</span></span></td>
<td><span data-ttu-id="6136e-195">48 × 48 pixel</span><span class="sxs-lookup"><span data-stu-id="6136e-195">48 × 48 pixels</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6136e-196">Risoluzione massima</span><span class="sxs-lookup"><span data-stu-id="6136e-196">Maximum Resolution</span></span></td>
<td><span data-ttu-id="6136e-197">4096 × 2304 pixel</span><span class="sxs-lookup"><span data-stu-id="6136e-197">4096 × 2304 pixels</span></span><br/> <span data-ttu-id="6136e-198">La risoluzione massima garantita per l'accelerazione DXVA è 1920 × 1088 pixel; con risoluzioni più elevate, la decodifica viene eseguita con DXVA, se supportata dall'hardware sottostante. in caso contrario, la decodifica viene eseguita con il software.</span><span class="sxs-lookup"><span data-stu-id="6136e-198">The maximum guaranteed resolution for DXVA acceleration is 1920 × 1088 pixels; at higher resolutions, decoding is done with DXVA, if it is supported by the underlying hardware, otherwise, decoding is done with software.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="6136e-199">In Windows 7 la risoluzione massima supportata è 1920 × 1088 pixel per la decodifica sia del software che del DXVA.</span><span class="sxs-lookup"><span data-stu-id="6136e-199">In Windows 7, the maximum supported resolution is 1920 × 1088 pixels for both software and DXVA decoding.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6136e-200">DXVA</span><span class="sxs-lookup"><span data-stu-id="6136e-200">DXVA</span></span></td>
<td><span data-ttu-id="6136e-201">Il decodificatore supporta DXVA versione 2, ma non DXVA versione 1.</span><span class="sxs-lookup"><span data-stu-id="6136e-201">The decoder supports DXVA version 2, but not DXVA version 1.</span></span> <span data-ttu-id="6136e-202">La decodifica DXVA è supportata solo per i Bitstream della linea di base, principale e del profilo superiore compatibili con la principale.</span><span class="sxs-lookup"><span data-stu-id="6136e-202">DXVA decoding is supported only for Main-compatible Baseline, Main, and High profile bitstreams.</span></span> <span data-ttu-id="6136e-203">I Bitstream di base compatibili con la principale sono definiti come <strong>profile_idc</strong>= 66 e <strong>constrained_set1_flag</strong>= 1.</span><span class="sxs-lookup"><span data-stu-id="6136e-203">(Main-compatible Baseline bitstreams are defined as <strong>profile_idc</strong>=66 and <strong>constrained_set1_flag</strong>=1.)</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="6136e-204">I dati di input devono essere conformi all'allegato B di ISO/IEC 14496-10.</span><span class="sxs-lookup"><span data-stu-id="6136e-204">Input data must conform to Annex B of ISO/IEC 14496-10.</span></span> <span data-ttu-id="6136e-205">I dati devono includere i codici iniziali.</span><span class="sxs-lookup"><span data-stu-id="6136e-205">The data must include the start codes.</span></span> <span data-ttu-id="6136e-206">Il decodificatore ignora i byte finché non trova un set di parametri di sequenza (SPS) e un set di parametri immagine (PPS) validi nel flusso di byte.</span><span class="sxs-lookup"><span data-stu-id="6136e-206">The decoder skips bytes until it finds a valid sequence parameter set (SPS) and picture parameter set (PPS) in the byte stream.</span></span>

<span data-ttu-id="6136e-207">Il decodificatore non supporta la tecnologia granulare dei film.</span><span class="sxs-lookup"><span data-stu-id="6136e-207">The decoder does not support Film Grain Technology.</span></span>

> [!Note]  
> <span data-ttu-id="6136e-208">Una versione precedente della documentazione ha erroneamente indicato che il decodificatore è supportato in Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="6136e-208">A previous version of the documentation incorrectly stated that the decoder is supported on Windows Server 2008 R2.</span></span>

 

<span data-ttu-id="6136e-209">Se è installato il supplemento di aggiornamento della piattaforma per Windows Vista, il decodificatore video H. 264 è disponibile in Windows Vista, ma è accessibile solo in Windows Vista tramite il [lettore di origine](source-reader.md).</span><span class="sxs-lookup"><span data-stu-id="6136e-209">If Platform Update Supplement for Windows Vista is installed, the H.264 video decoder is available on Windows Vista, but is accessible on Windows Vista only by using the [Source Reader](source-reader.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6136e-210">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6136e-210">Requirements</span></span>



| <span data-ttu-id="6136e-211">Requisito</span><span class="sxs-lookup"><span data-stu-id="6136e-211">Requirement</span></span> | <span data-ttu-id="6136e-212">Valore</span><span class="sxs-lookup"><span data-stu-id="6136e-212">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="6136e-213">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6136e-213">Minimum supported client</span></span><br/> | <span data-ttu-id="6136e-214">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="6136e-214">Windows 7 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="6136e-215">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6136e-215">Minimum supported server</span></span><br/> | <span data-ttu-id="6136e-216">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="6136e-216">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="6136e-217">DLL</span><span class="sxs-lookup"><span data-stu-id="6136e-217">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6136e-218"><dt>Msmpeg2vdec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6136e-218"><dt>Msmpeg2vdec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6136e-219">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6136e-219">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6136e-220">Oggetti codec</span><span class="sxs-lookup"><span data-stu-id="6136e-220">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="6136e-221">Supporto MPEG-4 in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6136e-221">MPEG-4 Support in Media Foundation</span></span>](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="6136e-222">Formati multimediali supportati in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6136e-222">Supported Media Formats in Media Foundation</span></span>](supported-media-formats-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="6136e-223">Tipi di supporti video</span><span class="sxs-lookup"><span data-stu-id="6136e-223">Video Media Types</span></span>](video-media-types.md)
</dt> </dl>

 

 
