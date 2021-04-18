---
description: Il decodificatore MPEG-2 video è una trasformazione Media Foundation che decodifica il video MPEG-1 e MPEG-2.
ms.assetid: 3E7FAE14-932D-44A3-997B-567C0D2EAE7B
title: Decoder video MPEG-2
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ca4384154faff777280fd0a03cf4fd289603e7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527901"
---
# <a name="mpeg-2-video-decoder"></a><span data-ttu-id="dfd39-103">Decoder video MPEG-2</span><span class="sxs-lookup"><span data-stu-id="dfd39-103">MPEG-2 Video Decoder</span></span>

<span data-ttu-id="dfd39-104">Il decodificatore MPEG-2 video è una [trasformazione Media Foundation](media-foundation-transforms.md) che decodifica il video MPEG-1 e MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="dfd39-104">The MPEG-2 Video Decoder is a [Media Foundation transform](media-foundation-transforms.md) that decodes MPEG-1 and MPEG-2 video.</span></span> <span data-ttu-id="dfd39-105">Il decodificatore supporta i video MPEG-2 Simple e Main Profile (H. 262, ISO/IEC 13818-2) e MPEG-1 video (ISO/IEC 11172-2).</span><span class="sxs-lookup"><span data-stu-id="dfd39-105">The decoder supports MPEG-2 Simple and Main profile video (H.262, ISO/IEC 13818-2) and MPEG-1 video (ISO/IEC 11172-2).</span></span>

## <a name="input-types"></a><span data-ttu-id="dfd39-106">Tipi di input</span><span class="sxs-lookup"><span data-stu-id="dfd39-106">Input Types</span></span>

<span data-ttu-id="dfd39-107">Il decodificatore supporta i tipi di supporti di input seguenti.</span><span class="sxs-lookup"><span data-stu-id="dfd39-107">The decoder supports the following input media types.</span></span>

| <span data-ttu-id="dfd39-108">Attributo</span><span class="sxs-lookup"><span data-stu-id="dfd39-108">Attribute</span></span>                                                 | <span data-ttu-id="dfd39-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dfd39-109">Description</span></span>                                                             |
|-----------------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="dfd39-110">**\_ \_ tipo principale MF \_ mt**</span><span class="sxs-lookup"><span data-stu-id="dfd39-110">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md) | <span data-ttu-id="dfd39-111">**Video di MFMediaType \_**</span><span class="sxs-lookup"><span data-stu-id="dfd39-111">**MFMediaType\_Video**</span></span>                                                  |
| [<span data-ttu-id="dfd39-112">**sottotipo MF \_ mt \_**</span><span class="sxs-lookup"><span data-stu-id="dfd39-112">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)        | <span data-ttu-id="dfd39-113">**MFVideoFormat \_ MPEG1**</span><span class="sxs-lookup"><span data-stu-id="dfd39-113">**MFVideoFormat\_MPEG1**</span></span><br/> <span data-ttu-id="dfd39-114">**MFVideoFormat \_ MPEG2**</span><span class="sxs-lookup"><span data-stu-id="dfd39-114">**MFVideoFormat\_MPEG2**</span></span><br/> |



 

## <a name="output-types"></a><span data-ttu-id="dfd39-115">Tipi di output</span><span class="sxs-lookup"><span data-stu-id="dfd39-115">Output Types</span></span>

<span data-ttu-id="dfd39-116">Il decodificatore supporta i tipi di output seguenti.</span><span class="sxs-lookup"><span data-stu-id="dfd39-116">The decoder supports the following output types.</span></span>

| <span data-ttu-id="dfd39-117">Attributo</span><span class="sxs-lookup"><span data-stu-id="dfd39-117">Attribute</span></span>                                                 | <span data-ttu-id="dfd39-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dfd39-118">Description</span></span>                                                                                                                                                                    |
|-----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dfd39-119">**\_ \_ tipo principale MF \_ mt**</span><span class="sxs-lookup"><span data-stu-id="dfd39-119">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md) | <span data-ttu-id="dfd39-120">**Video di MFMediaType \_**</span><span class="sxs-lookup"><span data-stu-id="dfd39-120">**MFMediaType\_Video**</span></span>                                                                                                                                                         |
| [<span data-ttu-id="dfd39-121">**sottotipo MF \_ mt \_**</span><span class="sxs-lookup"><span data-stu-id="dfd39-121">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)        | <span data-ttu-id="dfd39-122">**\_I420 MFVideoFormat**</span><span class="sxs-lookup"><span data-stu-id="dfd39-122">**MFVideoFormat\_I420**</span></span><br/> <span data-ttu-id="dfd39-123">**\_IYUV MFVideoFormat**</span><span class="sxs-lookup"><span data-stu-id="dfd39-123">**MFVideoFormat\_IYUV**</span></span><br/> <span data-ttu-id="dfd39-124">**\_NV12 MFVideoFormat**</span><span class="sxs-lookup"><span data-stu-id="dfd39-124">**MFVideoFormat\_NV12**</span></span><br/> <span data-ttu-id="dfd39-125">**\_YUY2 MFVideoFormat**</span><span class="sxs-lookup"><span data-stu-id="dfd39-125">**MFVideoFormat\_YUY2**</span></span><br/> <span data-ttu-id="dfd39-126">**\_YV12 MFVideoFormat**</span><span class="sxs-lookup"><span data-stu-id="dfd39-126">**MFVideoFormat\_YV12**</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="dfd39-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="dfd39-127">Remarks</span></span>

<span data-ttu-id="dfd39-128">Il decodificatore MPEG-2 video espone le interfacce seguenti:</span><span class="sxs-lookup"><span data-stu-id="dfd39-128">The MPEG-2 video decoder exposes the following interfaces:</span></span>

-   [<span data-ttu-id="dfd39-129">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="dfd39-129">**ICodecAPI**</span></span>](/windows/win32/api/strmif/nn-strmif-icodecapi)
-   [<span data-ttu-id="dfd39-130">**IMFGetService**</span><span class="sxs-lookup"><span data-stu-id="dfd39-130">**IMFGetService**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [<span data-ttu-id="dfd39-131">**IMFQualityAdvise**</span><span class="sxs-lookup"><span data-stu-id="dfd39-131">**IMFQualityAdvise**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)
-   [<span data-ttu-id="dfd39-132">**IMFQualityAdvise2**</span><span class="sxs-lookup"><span data-stu-id="dfd39-132">**IMFQualityAdvise2**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2)
-   [<span data-ttu-id="dfd39-133">**IMFRateControl**</span><span class="sxs-lookup"><span data-stu-id="dfd39-133">**IMFRateControl**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)
-   [<span data-ttu-id="dfd39-134">**IMFRateSupport**</span><span class="sxs-lookup"><span data-stu-id="dfd39-134">**IMFRateSupport**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)
-   [<span data-ttu-id="dfd39-135">**IMFRealTimeClient**</span><span class="sxs-lookup"><span data-stu-id="dfd39-135">**IMFRealTimeClient**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient)
-   [<span data-ttu-id="dfd39-136">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="dfd39-136">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

<span data-ttu-id="dfd39-137">L'input per il decodificatore deve essere un flusso elementare.</span><span class="sxs-lookup"><span data-stu-id="dfd39-137">The input to the decoder must be an elementary stream.</span></span> <span data-ttu-id="dfd39-138">La risoluzione massima supportata è 1920 × 1088 pixel.</span><span class="sxs-lookup"><span data-stu-id="dfd39-138">The maximum supported resolution is 1920 × 1088 pixels.</span></span>

<span data-ttu-id="dfd39-139">Il decodificatore supporta l'accelerazione video DirectX (DXVA) con Microsoft Direct3D 9 o Microsoft Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="dfd39-139">The decoder supports DirectX Video Acceleration (DXVA) using either Microsoft Direct3D 9 or Microsoft Direct3D 11.</span></span>

### <a name="special-decoding-modes"></a><span data-ttu-id="dfd39-140">Modalità di decodifica speciali</span><span class="sxs-lookup"><span data-stu-id="dfd39-140">Special Decoding Modes</span></span>

-   <span data-ttu-id="dfd39-141">**Modalità a bassa latenza.**</span><span class="sxs-lookup"><span data-stu-id="dfd39-141">**Low latency mode.**</span></span> <span data-ttu-id="dfd39-142">Questa modalità è appropriata per scenari come le comunicazioni in tempo reale.</span><span class="sxs-lookup"><span data-stu-id="dfd39-142">This mode is appropriate for scenarios such as real-time communications.</span></span> <span data-ttu-id="dfd39-143">Riduce la latenza di avvio, quindi il decodificatore produce prima di tutto il primo esempio di output.</span><span class="sxs-lookup"><span data-stu-id="dfd39-143">It reduces start-up latency, so the decoder produces the first output sample sooner.</span></span> <span data-ttu-id="dfd39-144">Tuttavia, il decodificatore memorizza un minor numero di campioni in questa modalità, che potenzialmente possono causare problemi, perché il decodificatore non decodifica il numero di frame in anticipo.</span><span class="sxs-lookup"><span data-stu-id="dfd39-144">However, the decoder buffers fewer samples in this mode, which can potentially lead to glitches, because the decoder does not decode as many frames in advance.</span></span> <span data-ttu-id="dfd39-145">Per abilitare la modalità a bassa latenza, impostare l'attributo [CODEcapis \_ AVLowLatencyMode](codecapi-avlowlatencymode.md) .</span><span class="sxs-lookup"><span data-stu-id="dfd39-145">To enable low latency mode, set the [CODECAPI\_AVLowLatencyMode](codecapi-avlowlatencymode.md) attribute.</span></span>
-   <span data-ttu-id="dfd39-146">**La ricerca.**</span><span class="sxs-lookup"><span data-stu-id="dfd39-146">**Seeking.**</span></span> <span data-ttu-id="dfd39-147">Per una ricerca precisa, chiamare il metodo [**IMFTransform:: SetOutputBounds**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputbounds) .</span><span class="sxs-lookup"><span data-stu-id="dfd39-147">For precise seeking, call the [**IMFTransform::SetOutputBounds**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputbounds) method.</span></span> <span data-ttu-id="dfd39-148">Quando viene chiamato questo metodo, il decodificatore restituisce solo i frame che rientrano nell'intervallo di timestamp specificato dal chiamante.</span><span class="sxs-lookup"><span data-stu-id="dfd39-148">When this method is called, the decoder outputs only frames that fall within the range of time stamps specified by the caller.</span></span>
-   <span data-ttu-id="dfd39-149">**Modalità di generazione delle anteprime**.</span><span class="sxs-lookup"><span data-stu-id="dfd39-149">**Thumbnail generation mode**.</span></span> <span data-ttu-id="dfd39-150">Questa modalità è progettata per la generazione rapida di immagini di anteprima.</span><span class="sxs-lookup"><span data-stu-id="dfd39-150">This mode is intended for quick generation of thumbnail images.</span></span> <span data-ttu-id="dfd39-151">In questa modalità, il decodificatore decodifica inizialmente solo I frame I.</span><span class="sxs-lookup"><span data-stu-id="dfd39-151">In this mode, the decoder initially decodes only I frames.</span></span> <span data-ttu-id="dfd39-152">Se in un certo numero di frame non viene trovato un frame I, il decodificatore inizia a Decodificare P frame e restituisce frame non-I a intervalli fissi (uno per *N* immagini) finché non viene raggiunto un frame di i.</span><span class="sxs-lookup"><span data-stu-id="dfd39-152">If no I frame is found within a certain number of frames, the decoder starts decoding P frames and outputs non–I frames at a fixed interval (one per *N* pictures) until an I frame is reached.</span></span> <span data-ttu-id="dfd39-153">Per abilitare la modalità di generazione delle anteprime, impostare la proprietà [CODEcapis \_ AVDecVideoThumbnailGenerationMode](../directshow/avdecvideothumbnailgenerationmode-property.md) .</span><span class="sxs-lookup"><span data-stu-id="dfd39-153">To enable thumbnail generation mode, set the [CODECAPI\_AVDecVideoThumbnailGenerationMode](../directshow/avdecvideothumbnailgenerationmode-property.md) property.</span></span>
-   <span data-ttu-id="dfd39-154">**Riproduzione di trick.**</span><span class="sxs-lookup"><span data-stu-id="dfd39-154">**Trick play.**</span></span> <span data-ttu-id="dfd39-155">Il decodificatore può decodificare le tariffe più velocemente rispetto al tempo reale.</span><span class="sxs-lookup"><span data-stu-id="dfd39-155">The decoder can decode at rates faster than real time.</span></span> <span data-ttu-id="dfd39-156">A una velocità di riproduzione superiore, il decodificatore passa alla decodifica solo I frame I.</span><span class="sxs-lookup"><span data-stu-id="dfd39-156">At higher playback rates, the decoder will switch to decoding only I frames.</span></span> <span data-ttu-id="dfd39-157">Per la riproduzione inversa vengono decodificati solo I frame I.</span><span class="sxs-lookup"><span data-stu-id="dfd39-157">For reverse playback, only I frames are decoded.</span></span>

### <a name="codec-properties"></a><span data-ttu-id="dfd39-158">Proprietà codec</span><span class="sxs-lookup"><span data-stu-id="dfd39-158">Codec Properties</span></span>

<span data-ttu-id="dfd39-159">Il decodificatore supporta le proprietà seguenti tramite il metodo [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) .</span><span class="sxs-lookup"><span data-stu-id="dfd39-159">The decoder supports the following properties through the [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) method.</span></span>



| <span data-ttu-id="dfd39-160">Proprietà</span><span class="sxs-lookup"><span data-stu-id="dfd39-160">Property</span></span>                                                                                                      | <span data-ttu-id="dfd39-161">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dfd39-161">Description</span></span>                                                                                                |
|---------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dfd39-162">Codecapis \_ AVDecVideoThumbnailGenerationMode</span><span class="sxs-lookup"><span data-stu-id="dfd39-162">CODECAPI\_AVDecVideoThumbnailGenerationMode</span></span>](../directshow/avdecvideothumbnailgenerationmode-property.md)               | <span data-ttu-id="dfd39-163">Abilita o Disabilita la modalità di generazione delle anteprime.</span><span class="sxs-lookup"><span data-stu-id="dfd39-163">Enables or disables thumbnail generation mode.</span></span>                                                             |
| [<span data-ttu-id="dfd39-164">Codecapis \_ AVDecVideoAcceleration \_ MPEG2</span><span class="sxs-lookup"><span data-stu-id="dfd39-164">CODECAPI\_AVDecVideoAcceleration\_MPEG2</span></span>](../directshow/avdecvideoacceleration-mpeg2-property.md)                        | <span data-ttu-id="dfd39-165">Abilita o Disabilita la decodifica con accelerazione hardware.</span><span class="sxs-lookup"><span data-stu-id="dfd39-165">Enables or disables hardware accelerated decoding.</span></span>                                                         |
| [<span data-ttu-id="dfd39-166">Codecapis \_ AVLowLatencyMode</span><span class="sxs-lookup"><span data-stu-id="dfd39-166">CODECAPI\_AVLowLatencyMode</span></span>](codecapi-avlowlatencymode.md)                                                   | <span data-ttu-id="dfd39-167">Abilita o Disabilita la modalità a bassa latenza.</span><span class="sxs-lookup"><span data-stu-id="dfd39-167">Enables or disables low-latency mode.</span></span>                                                                      |
| [<span data-ttu-id="dfd39-168">il \_ decodificatore MFT \_ espone i \_ \_ tipi \_ di output in \_ \_ ordine nativo</span><span class="sxs-lookup"><span data-stu-id="dfd39-168">MFT\_DECODER\_EXPOSE\_OUTPUT\_TYPES\_IN\_NATIVE\_ORDER</span></span>](mft-decoder-expose-output-types-in-native-order.md) | <span data-ttu-id="dfd39-169">Specifica se il decodificatore espone i tipi di output idonei per la transcodifica prima di altri formati.</span><span class="sxs-lookup"><span data-stu-id="dfd39-169">Specifies whether the decoder exposes output types that are suitable for transcoding before other formats.</span></span> |



 

<span data-ttu-id="dfd39-170">Di queste proprietà, è possibile impostare anche i seguenti elementi tramite l'interfaccia [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) :</span><span class="sxs-lookup"><span data-stu-id="dfd39-170">Of these properties, the following can also be set through the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface:</span></span>

-   [<span data-ttu-id="dfd39-171">Codecapis \_ AVDecVideoThumbnailGenerationMode</span><span class="sxs-lookup"><span data-stu-id="dfd39-171">CODECAPI\_AVDecVideoThumbnailGenerationMode</span></span>](../directshow/avdecvideothumbnailgenerationmode-property.md)
-   [<span data-ttu-id="dfd39-172">Codecapis \_ AVDecVideoAcceleration \_ MPEG2</span><span class="sxs-lookup"><span data-stu-id="dfd39-172">CODECAPI\_AVDecVideoAcceleration\_MPEG2</span></span>](../directshow/avdecvideoacceleration-mpeg2-property.md)
-   [<span data-ttu-id="dfd39-173">Codecapis \_ AVLowLatencyMode</span><span class="sxs-lookup"><span data-stu-id="dfd39-173">CODECAPI\_AVLowLatencyMode</span></span>](codecapi-avlowlatencymode.md)

### <a name="limitations"></a><span data-ttu-id="dfd39-174">Limitazioni</span><span class="sxs-lookup"><span data-stu-id="dfd39-174">Limitations</span></span>

-   <span data-ttu-id="dfd39-175">Il decodificatore non è supportato nelle piattaforme basate su IA-64.</span><span class="sxs-lookup"><span data-stu-id="dfd39-175">The decoder is not supported on IA-64–based platforms.</span></span>
-   <span data-ttu-id="dfd39-176">Il decodificatore non supporta la decrittografia CSS o la riproduzione di DVD crittografati.</span><span class="sxs-lookup"><span data-stu-id="dfd39-176">The decoder does not support CSS decryption or playback of encrypted DVDs.</span></span>

## <a name="requirements"></a><span data-ttu-id="dfd39-177">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dfd39-177">Requirements</span></span>



| <span data-ttu-id="dfd39-178">Requisito</span><span class="sxs-lookup"><span data-stu-id="dfd39-178">Requirement</span></span> | <span data-ttu-id="dfd39-179">Valore</span><span class="sxs-lookup"><span data-stu-id="dfd39-179">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfd39-180">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dfd39-180">Minimum supported client</span></span><br/> | <span data-ttu-id="dfd39-181">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="dfd39-181">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="dfd39-182">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dfd39-182">Minimum supported server</span></span><br/> | <span data-ttu-id="dfd39-183">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="dfd39-183">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="dfd39-184">DLL</span><span class="sxs-lookup"><span data-stu-id="dfd39-184">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dfd39-185"><dt>Msmpeg2vdec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dfd39-185"><dt>Msmpeg2vdec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dfd39-186">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dfd39-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfd39-187">Oggetti codec</span><span class="sxs-lookup"><span data-stu-id="dfd39-187">Codec Objects</span></span>](codecobjects.md)
</dt> </dl>

 

 
