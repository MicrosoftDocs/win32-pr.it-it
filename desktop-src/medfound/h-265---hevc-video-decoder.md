---
description: Il decodificatore Media Foundation H. 265 video è una trasformazione Media Foundation che supporta la decodifica del contenuto H. 265/HEVC nel formato allegato B e può essere usato per la riproduzione di file MP4 e M2TS.
ms.assetid: BBE754E4-2AAD-4CFD-B53F-2B66693502EE
title: Decodificatore video H. 265/HEVC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0c20a83f82e106bd749deb8bf2350cc9e5a347a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527697"
---
# <a name="h265--hevc-video-decoder"></a><span data-ttu-id="e0d28-103">Decodificatore video H. 265/HEVC</span><span class="sxs-lookup"><span data-stu-id="e0d28-103">H.265 / HEVC Video Decoder</span></span>

<span data-ttu-id="e0d28-104">Il decodificatore Media Foundation H. 265 video è una [trasformazione Media Foundation](media-foundation-transforms.md) che supporta la decodifica del contenuto H. 265/HEVC nel formato allegato B e può essere usato per la riproduzione di file MP4 e M2TS.</span><span class="sxs-lookup"><span data-stu-id="e0d28-104">The Media Foundation H.265 video decoder is a [Media Foundation Transform](media-foundation-transforms.md) that supports decoding H.265/HEVC content in Annex B format and can be used in playback of mp4 and m2ts files.</span></span>

<span data-ttu-id="e0d28-105">Il decodificatore H. 265 video espone le interfacce seguenti.</span><span class="sxs-lookup"><span data-stu-id="e0d28-105">The H.265 video decoder exposes the following interfaces.</span></span>

-   <span data-ttu-id="e0d28-106">[**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) (supportato in Windows 8)</span><span class="sxs-lookup"><span data-stu-id="e0d28-106">[**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) (supported in Windows 8)</span></span>
-   [<span data-ttu-id="e0d28-107">**IMFAttributes**</span><span class="sxs-lookup"><span data-stu-id="e0d28-107">**IMFAttributes**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)
-   [<span data-ttu-id="e0d28-108">**IMFGetService**</span><span class="sxs-lookup"><span data-stu-id="e0d28-108">**IMFGetService**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [<span data-ttu-id="e0d28-109">**IMFQualityAdvise**</span><span class="sxs-lookup"><span data-stu-id="e0d28-109">**IMFQualityAdvise**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)
-   [<span data-ttu-id="e0d28-110">**IMFQualityAdvise2**</span><span class="sxs-lookup"><span data-stu-id="e0d28-110">**IMFQualityAdvise2**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2)
-   [<span data-ttu-id="e0d28-111">**IMFRateControl**</span><span class="sxs-lookup"><span data-stu-id="e0d28-111">**IMFRateControl**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)
-   [<span data-ttu-id="e0d28-112">**IMFRateSupport**</span><span class="sxs-lookup"><span data-stu-id="e0d28-112">**IMFRateSupport**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)
-   [<span data-ttu-id="e0d28-113">**IMFRealTimeClient**</span><span class="sxs-lookup"><span data-stu-id="e0d28-113">**IMFRealTimeClient**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient)
-   [<span data-ttu-id="e0d28-114">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="e0d28-114">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

<span data-ttu-id="e0d28-115">Per creare un'istanza del decodificatore, chiamare la funzione [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) o [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .</span><span class="sxs-lookup"><span data-stu-id="e0d28-115">To create an instance of the decoder call the [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) or [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function.</span></span>

## <a name="input-types"></a><span data-ttu-id="e0d28-116">Tipi di input</span><span class="sxs-lookup"><span data-stu-id="e0d28-116">Input Types</span></span>

<span data-ttu-id="e0d28-117">Il tipo di input deve contenere almeno i due attributi seguenti:</span><span class="sxs-lookup"><span data-stu-id="e0d28-117">The input type must contain at least the following two attributes:</span></span>



| <span data-ttu-id="e0d28-118">Attributo</span><span class="sxs-lookup"><span data-stu-id="e0d28-118">Attribute</span></span>                                                 | <span data-ttu-id="e0d28-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e0d28-119">Description</span></span>                                                                                   |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e0d28-120">**\_ \_ tipo principale MF \_ mt**</span><span class="sxs-lookup"><span data-stu-id="e0d28-120">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md) | <span data-ttu-id="e0d28-121">**Video di MFMediaType \_**</span><span class="sxs-lookup"><span data-stu-id="e0d28-121">**MFMediaType\_Video**</span></span>                                                                        |
| [<span data-ttu-id="e0d28-122">**sottotipo MF \_ mt \_**</span><span class="sxs-lookup"><span data-stu-id="e0d28-122">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)        | <span data-ttu-id="e0d28-123">[MFVideoFormat \_ HEVC](video-subtype-guids.md) o MFVideoFormat \_ HEVC \_ es</span><span class="sxs-lookup"><span data-stu-id="e0d28-123">[MFVideoFormat\_HEVC](video-subtype-guids.md) or MFVideoFormat\_HEVC\_ES</span></span> |



 

<span data-ttu-id="e0d28-124">Il primo sottotipo di supporto, MFVideoFormat \_ HEVC, indica che gli esempi di supporti contengono il Bitstream H. 265 con i codici iniziali e che il flusso ha Interleaved SPS/PPS.</span><span class="sxs-lookup"><span data-stu-id="e0d28-124">The first media subtype, MFVideoFormat\_HEVC, indicates that the media samples carry H.265 bitstream with start codes, and the stream has interleaved SPS/PPS.</span></span> <span data-ttu-id="e0d28-125">Si presuppone un frame per campione.</span><span class="sxs-lookup"><span data-stu-id="e0d28-125">It assumes one frame per sample.</span></span>

<span data-ttu-id="e0d28-126">Il sottotipo di supporto MFVideoFormat \_ HEVC \_ es indica che gli esempi di supporti contengono un bitstream elementare H. 265, in cui ogni esempio può contenere un'immagine parziale, più immagini, alcune immagini e un'immagine parziale.</span><span class="sxs-lookup"><span data-stu-id="e0d28-126">The media subtype MFVideoFormat\_ HEVC\_ES is to indicate the media samples carry elementary H.265 bitstream, where each sample may contain a partial picture, multiple pictures, some pictures plus a partial picture.</span></span>

<span data-ttu-id="e0d28-127">I tipi di supporti di input non possono essere modificati dinamicamente tra due tipi.</span><span class="sxs-lookup"><span data-stu-id="e0d28-127">The input media types cannot change dynamically between two types.</span></span> <span data-ttu-id="e0d28-128">Il decodificatore può rilevare le modifiche al formato di output in fase di elaborazione in base alla sintassi del flusso elementare (proporzioni, dimensioni, flag interlacciati, informazioni colorimetria) e attivare le modifiche del tipo di supporto di output corrispondente.</span><span class="sxs-lookup"><span data-stu-id="e0d28-128">The decoder can detect in-flight output format changes based on the elementary stream syntax (aspect ratio, dimension, interlace flags, colorimetry information) and trigger corresponding output media type changes.</span></span>

<span data-ttu-id="e0d28-129">Per il tipo di supporto di input, il decodificatore prevede che l'origine imposti il profilo corretto.</span><span class="sxs-lookup"><span data-stu-id="e0d28-129">For input media type, the decoder expects the source to set the correct Profile.</span></span> <span data-ttu-id="e0d28-130">Ad esempio, se il contenuto è 10 bit, il tipo di supporto di input deve specificare il profilo come main10.</span><span class="sxs-lookup"><span data-stu-id="e0d28-130">For example if the content is going to be 10bit, input media type should specify the profile as Main10.</span></span>

## <a name="output-types"></a><span data-ttu-id="e0d28-131">Tipi di output</span><span class="sxs-lookup"><span data-stu-id="e0d28-131">Output Types</span></span>

<span data-ttu-id="e0d28-132">Il decodificatore supporta i sottotipi di output seguenti:</span><span class="sxs-lookup"><span data-stu-id="e0d28-132">The decoder supports the following output subtypes:</span></span>

-   <span data-ttu-id="e0d28-133">**\_NV12 MFVideoFormat**</span><span class="sxs-lookup"><span data-stu-id="e0d28-133">**MFVideoFormat\_NV12**</span></span>
-   <span data-ttu-id="e0d28-134">**\_P010 MFVideoFormat**</span><span class="sxs-lookup"><span data-stu-id="e0d28-134">**MFVideoFormat\_P010**</span></span>

<span data-ttu-id="e0d28-135">Per altre informazioni su questi sottotipi, vedere [GUID del sottotipo video](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="e0d28-135">For more information about these subtypes, see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>

## <a name="transform-attributes"></a><span data-ttu-id="e0d28-136">Attributi di trasformazione</span><span class="sxs-lookup"><span data-stu-id="e0d28-136">Transform Attributes</span></span>

<span data-ttu-id="e0d28-137">Il decodificatore H. 265 implementa il metodo [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) .</span><span class="sxs-lookup"><span data-stu-id="e0d28-137">The H.265 decoder implements the [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) method.</span></span> <span data-ttu-id="e0d28-138">Le applicazioni possono utilizzare questo metodo per ottenere o impostare gli attributi seguenti.</span><span class="sxs-lookup"><span data-stu-id="e0d28-138">Applications can use this method to get or set the following attributes.</span></span>



| <span data-ttu-id="e0d28-139">Attributo</span><span class="sxs-lookup"><span data-stu-id="e0d28-139">Attribute</span></span>                                                                                       | <span data-ttu-id="e0d28-140">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e0d28-140">Description</span></span>                                                                                                                   |
|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e0d28-141">Codecapis \_ AVLowLatencyMode</span><span class="sxs-lookup"><span data-stu-id="e0d28-141">CODECAPI\_AVLowLatencyMode</span></span>](codecapi-avlowlatencymode.md)                                     | <span data-ttu-id="e0d28-142">Abilita o Disabilita la modalità di decodifica a bassa latenza.</span><span class="sxs-lookup"><span data-stu-id="e0d28-142">Enables or disables low-latency decoding mode.</span></span>                                                                                |
| [<span data-ttu-id="e0d28-143">Codecapis \_ AVDecNumWorkerThreads</span><span class="sxs-lookup"><span data-stu-id="e0d28-143">CODECAPI\_AVDecNumWorkerThreads</span></span>](codecapi-avdecnumworkerthreads.md)                           | <span data-ttu-id="e0d28-144">Imposta il numero di thread di lavoro utilizzati dal decodificatore.</span><span class="sxs-lookup"><span data-stu-id="e0d28-144">Sets the number of worker threads used by the decoder.</span></span>                                                                        |
| [<span data-ttu-id="e0d28-145">Codecapis \_ AVDecVideoThumbnailGenerationMode</span><span class="sxs-lookup"><span data-stu-id="e0d28-145">CODECAPI\_AVDecVideoThumbnailGenerationMode</span></span>](../directshow/avdecvideothumbnailgenerationmode-property.md) | <span data-ttu-id="e0d28-146">Abilita o Disabilita la modalità di generazione delle anteprime.</span><span class="sxs-lookup"><span data-stu-id="e0d28-146">Enables or disables thumbnail generation mode.</span></span>                                                                                |
| [<span data-ttu-id="e0d28-147">\_set di \_ lunghezza MF Nalu \_</span><span class="sxs-lookup"><span data-stu-id="e0d28-147">MF\_NALU\_LENGTH\_SET</span></span>](mf-nalu-length-set.md)                                                 | <span data-ttu-id="e0d28-148">Indica che le informazioni sulla lunghezza di NALU verranno inviate come BLOB con ogni esempio H. 265 compresso.</span><span class="sxs-lookup"><span data-stu-id="e0d28-148">Indicates that NALU length information will be sent as a BLOB with each compressed H.265 sample.</span></span>                              |
| [<span data-ttu-id="e0d28-149">\_ \_ informazioni sulla lunghezza di MF Nalu \_</span><span class="sxs-lookup"><span data-stu-id="e0d28-149">MF\_NALU\_LENGTH\_INFORMATION</span></span>](mf-nalu-length-information.md)                                 | <span data-ttu-id="e0d28-150">Indica le lunghezze di NALUs nell'esempio.</span><span class="sxs-lookup"><span data-stu-id="e0d28-150">Indicates the lengths of NALUs in the sample.</span></span> <span data-ttu-id="e0d28-151">Si tratta di un BLOB MF impostato su esempi di input compressi per il decodificatore H. 265.</span><span class="sxs-lookup"><span data-stu-id="e0d28-151">This is a MF BLOB that is set on compressed input samples to the H.265 decoder.</span></span> |
| [<span data-ttu-id="e0d28-152">\_ \_ numero minimo di \_ campioni di output MF \_ sa \_</span><span class="sxs-lookup"><span data-stu-id="e0d28-152">MF\_SA\_MINIMUM\_OUTPUT\_SAMPLE\_COUNT</span></span>](mf-sa-minimum-output-sample-count.md)                 | <span data-ttu-id="e0d28-153">Specifica il numero massimo di campioni di output.</span><span class="sxs-lookup"><span data-stu-id="e0d28-153">Specifies the maximum number of output samples.</span></span>                                                                               |



 

<span data-ttu-id="e0d28-154">Il decodificatore H. 265 supporta l'interfaccia [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) .</span><span class="sxs-lookup"><span data-stu-id="e0d28-154">The H.265 decoder supports the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface.</span></span> <span data-ttu-id="e0d28-155">Questa interfaccia fornisce un'API alternativate per l'impostazione delle proprietà dei codec seguenti.</span><span class="sxs-lookup"><span data-stu-id="e0d28-155">This interface provides an alternativate API for setting the following codec properties.</span></span>

-   [<span data-ttu-id="e0d28-156">Codecapis \_ AVDecNumWorkerThreads</span><span class="sxs-lookup"><span data-stu-id="e0d28-156">CODECAPI\_AVDecNumWorkerThreads</span></span>](codecapi-avdecnumworkerthreads.md)
-   [<span data-ttu-id="e0d28-157">Codecapis \_ AVDecVideoThumbnailGenerationMode</span><span class="sxs-lookup"><span data-stu-id="e0d28-157">CODECAPI\_AVDecVideoThumbnailGenerationMode</span></span>](../directshow/avdecvideothumbnailgenerationmode-property.md)
-   [<span data-ttu-id="e0d28-158">Codecapis \_ AVLowLatencyMode</span><span class="sxs-lookup"><span data-stu-id="e0d28-158">CODECAPI\_AVLowLatencyMode</span></span>](codecapi-avlowlatencymode.md)

## <a name="format-constraints"></a><span data-ttu-id="e0d28-159">Vincoli di formato</span><span class="sxs-lookup"><span data-stu-id="e0d28-159">Format Constraints</span></span>

<span data-ttu-id="e0d28-160">Il decodificatore supporta i formati seguenti:</span><span class="sxs-lookup"><span data-stu-id="e0d28-160">The decoder supports the following formats:</span></span>



| <span data-ttu-id="e0d28-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0d28-161">Requirement</span></span> | <span data-ttu-id="e0d28-162">Valore</span><span class="sxs-lookup"><span data-stu-id="e0d28-162">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0d28-163">Profili/livelli</span><span class="sxs-lookup"><span data-stu-id="e0d28-163">Profiles/Levels</span></span>    | <span data-ttu-id="e0d28-164">Profili principale, Main Still Picture e main10</span><span class="sxs-lookup"><span data-stu-id="e0d28-164">Main, Main Still Picture, and Main10 profiles</span></span>                                                                                                                                                                                                                        |
| <span data-ttu-id="e0d28-165">Formati Chroma</span><span class="sxs-lookup"><span data-stu-id="e0d28-165">Chroma Formats</span></span>     | <span data-ttu-id="e0d28-166">Chroma 4:2:0</span><span class="sxs-lookup"><span data-stu-id="e0d28-166">4:2:0 chroma</span></span>                                                                                                                                                                                                                                                         |
| <span data-ttu-id="e0d28-167">Risoluzione minima</span><span class="sxs-lookup"><span data-stu-id="e0d28-167">Minimum Resolution</span></span> | <span data-ttu-id="e0d28-168">48 × 48 pixel</span><span class="sxs-lookup"><span data-stu-id="e0d28-168">48 × 48 pixels</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="e0d28-169">Risoluzione massima</span><span class="sxs-lookup"><span data-stu-id="e0d28-169">Maximum Resolution</span></span> | <span data-ttu-id="e0d28-170">4096 × 2304 pixel</span><span class="sxs-lookup"><span data-stu-id="e0d28-170">4096 × 2304 pixels</span></span><br/> <span data-ttu-id="e0d28-171">La risoluzione massima garantita per l'accelerazione DXVA è 1920 × 1088 pixel; con risoluzioni più elevate, la decodifica viene eseguita con DXVA, se supportata dall'hardware sottostante. in caso contrario, la decodifica viene eseguita con il software.</span><span class="sxs-lookup"><span data-stu-id="e0d28-171">The maximum guaranteed resolution for DXVA acceleration is 1920 × 1088 pixels; at higher resolutions, decoding is done with DXVA, if it is supported by the underlying hardware, otherwise, decoding is done with software.</span></span><br/> |
| <span data-ttu-id="e0d28-172">DXVA</span><span class="sxs-lookup"><span data-stu-id="e0d28-172">DXVA</span></span>               | <span data-ttu-id="e0d28-173">Il decodificatore supporta DX11 e DX12 DXVA, ma non DXVA versione 2 o DXVA versione 1.</span><span class="sxs-lookup"><span data-stu-id="e0d28-173">The decoder supports DX11 and DX12 DXVA, but not DXVA version 2 or DXVA version 1.</span></span>                                                                                                                                                                                                         |



 

<span data-ttu-id="e0d28-174">I dati di input devono essere conformi all'allegato B di ITU-T H. 265 \| ISO/IEC 23008-2.</span><span class="sxs-lookup"><span data-stu-id="e0d28-174">Input data must conform to Annex B of ITU-T H.265 \| ISO/IEC 23008-2.</span></span> <span data-ttu-id="e0d28-175">I dati devono includere i codici iniziali.</span><span class="sxs-lookup"><span data-stu-id="e0d28-175">The data must include the start codes.</span></span> <span data-ttu-id="e0d28-176">Il decodificatore ignora i byte finché non trova un set di parametri di sequenza (SPS) e un set di parametri immagine (PPS) validi nel flusso di byte.</span><span class="sxs-lookup"><span data-stu-id="e0d28-176">The decoder skips bytes until it finds a valid sequence parameter set (SPS) and picture parameter set (PPS) in the byte stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0d28-177">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e0d28-177">Requirements</span></span>



| <span data-ttu-id="e0d28-178">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0d28-178">Requirement</span></span> | <span data-ttu-id="e0d28-179">Valore</span><span class="sxs-lookup"><span data-stu-id="e0d28-179">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0d28-180">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e0d28-180">Minimum supported client</span></span><br/> | <span data-ttu-id="e0d28-181">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="e0d28-181">Windows 10 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="e0d28-182">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e0d28-182">Minimum supported server</span></span><br/> | <span data-ttu-id="e0d28-183">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="e0d28-183">None supported</span></span><br/>                                                                |
| <span data-ttu-id="e0d28-184">DLL</span><span class="sxs-lookup"><span data-stu-id="e0d28-184">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e0d28-185"><dt>hevcdecoder.dll</dt> <dt>hevcdecoder_store.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0d28-185"><dt>hevcdecoder.dll</dt> <dt>hevcdecoder_store.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0d28-186">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e0d28-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0d28-187">Oggetti codec</span><span class="sxs-lookup"><span data-stu-id="e0d28-187">Codec Objects</span></span>](codecobjects.md)
</dt> </dl>

 

 
