---
description: 'Il codificatore Microsoft Media Foundation H. 264 video è una trasformazione Media Foundation che supporta i profili H. 264 seguenti:'
ms.assetid: 4d4c768f-b76a-40ca-8736-2f592a4f4cc4
title: Codificatore video H. 264
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5631239e9db0ddf078848bc3c4a04282e7e79990
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308773"
---
# <a name="h264-video-encoder"></a><span data-ttu-id="318e5-103">Codificatore video H. 264</span><span class="sxs-lookup"><span data-stu-id="318e5-103">H.264 Video Encoder</span></span>

<span data-ttu-id="318e5-104">Il codificatore Microsoft Media Foundation H. 264 video è una [trasformazione Media Foundation](media-foundation-transforms.md) che supporta i profili h. 264 seguenti:</span><span class="sxs-lookup"><span data-stu-id="318e5-104">The Microsoft Media Foundation H.264 video encoder is a [Media Foundation transform](media-foundation-transforms.md) that supports the following H.264 profiles:</span></span>

-   <span data-ttu-id="318e5-105">Profilo di base</span><span class="sxs-lookup"><span data-stu-id="318e5-105">Baseline Profile</span></span>
-   <span data-ttu-id="318e5-106">Main Profile</span><span class="sxs-lookup"><span data-stu-id="318e5-106">Main Profile</span></span>
-   <span data-ttu-id="318e5-107">Profilo elevato (richiede Windows 8)</span><span class="sxs-lookup"><span data-stu-id="318e5-107">High profile (requires Windows 8)</span></span>

<span data-ttu-id="318e5-108">Il codificatore video H. 264 espone le interfacce seguenti:</span><span class="sxs-lookup"><span data-stu-id="318e5-108">The H.264 video encoder exposes the following interfaces:</span></span>

-   [<span data-ttu-id="318e5-109">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="318e5-109">**ICodecAPI**</span></span>](/windows/win32/api/strmif/nn-strmif-icodecapi)
-   [<span data-ttu-id="318e5-110">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="318e5-110">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="input-types"></a><span data-ttu-id="318e5-111">Tipi di input</span><span class="sxs-lookup"><span data-stu-id="318e5-111">Input Types</span></span>

<span data-ttu-id="318e5-112">Il tipo di supporto di input deve avere uno dei seguenti sottotipi:</span><span class="sxs-lookup"><span data-stu-id="318e5-112">The input media type must have one of the following subtypes:</span></span>

-   <span data-ttu-id="318e5-113">**MFVideoFormat_I420**</span><span class="sxs-lookup"><span data-stu-id="318e5-113">**MFVideoFormat_I420**</span></span>
-   <span data-ttu-id="318e5-114">**MFVideoFormat_IYUV**</span><span class="sxs-lookup"><span data-stu-id="318e5-114">**MFVideoFormat_IYUV**</span></span>
-   <span data-ttu-id="318e5-115">**MFVideoFormat_NV12**</span><span class="sxs-lookup"><span data-stu-id="318e5-115">**MFVideoFormat_NV12**</span></span>
-   <span data-ttu-id="318e5-116">**MFVideoFormat_YUY2**</span><span class="sxs-lookup"><span data-stu-id="318e5-116">**MFVideoFormat_YUY2**</span></span>
-   <span data-ttu-id="318e5-117">**MFVideoFormat_YV12**</span><span class="sxs-lookup"><span data-stu-id="318e5-117">**MFVideoFormat_YV12**</span></span>

<span data-ttu-id="318e5-118">Per altre informazioni su questi sottotipi, vedere [GUID del sottotipo video](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="318e5-118">For more information about these subtypes, see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>

<span data-ttu-id="318e5-119">Il tipo di output deve essere impostato prima del tipo di input.</span><span class="sxs-lookup"><span data-stu-id="318e5-119">The output type must be set before the input type.</span></span> <span data-ttu-id="318e5-120">Fino a quando non viene impostato il tipo di output, il metodo [**IMFTransform:: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) del codificatore restituisce **MF_E_TRANSFORM_TYPE_NOT_SET**.</span><span class="sxs-lookup"><span data-stu-id="318e5-120">Until the output type is set, the encoder's [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) method returns **MF_E_TRANSFORM_TYPE_NOT_SET**.</span></span>

## <a name="output-types"></a><span data-ttu-id="318e5-121">Tipi di output</span><span class="sxs-lookup"><span data-stu-id="318e5-121">Output Types</span></span>

<span data-ttu-id="318e5-122">Il codificatore supporta un solo sottotipo di output:</span><span class="sxs-lookup"><span data-stu-id="318e5-122">The encoder supports a single output subtype:</span></span>

-   <span data-ttu-id="318e5-123">**MFVideoFormat_H264**</span><span class="sxs-lookup"><span data-stu-id="318e5-123">**MFVideoFormat_H264**</span></span>

<span data-ttu-id="318e5-124">Impostare gli attributi seguenti sul tipo di supporto di output.</span><span class="sxs-lookup"><span data-stu-id="318e5-124">Set the following attributes on the output media type.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="318e5-125">Attributo</span><span class="sxs-lookup"><span data-stu-id="318e5-125">Attribute</span></span></th>
<th><span data-ttu-id="318e5-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="318e5-126">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="318e5-127"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="318e5-127"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span></span></td>
<td><span data-ttu-id="318e5-128">Tipo principale.</span><span class="sxs-lookup"><span data-stu-id="318e5-128">Major type.</span></span> <span data-ttu-id="318e5-129">Deve essere <strong>MFMediaType_Video</strong>.</span><span class="sxs-lookup"><span data-stu-id="318e5-129">Must be <strong>MFMediaType_Video</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="318e5-130"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="318e5-130"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span></span></td>
<td><span data-ttu-id="318e5-131">Sottotipo video.</span><span class="sxs-lookup"><span data-stu-id="318e5-131">Video subtype.</span></span> <span data-ttu-id="318e5-132">Deve essere <strong>MFVideoFormat_H264</strong>.</span><span class="sxs-lookup"><span data-stu-id="318e5-132">Must be <strong>MFVideoFormat_H264</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="318e5-133"><a href="mf-mt-avg-bitrate-attribute.md"><strong>MF_MT_AVG_BITRATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="318e5-133"><a href="mf-mt-avg-bitrate-attribute.md"><strong>MF_MT_AVG_BITRATE</strong></a></span></span></td>
<td><span data-ttu-id="318e5-134">Velocità in bit codificata media, in bit al secondo.</span><span class="sxs-lookup"><span data-stu-id="318e5-134">Average encoded bit rate, in bits per second.</span></span> <span data-ttu-id="318e5-135">Deve essere maggiore di zero.</span><span class="sxs-lookup"><span data-stu-id="318e5-135">Must be greater than zero.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="318e5-136"><a href="mf-mt-frame-rate-attribute.md"><strong>MF_MT_FRAME_RATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="318e5-136"><a href="mf-mt-frame-rate-attribute.md"><strong>MF_MT_FRAME_RATE</strong></a></span></span></td>
<td><span data-ttu-id="318e5-137">Frequenza di fotogrammi.</span><span class="sxs-lookup"><span data-stu-id="318e5-137">Frame rate.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="318e5-138"><a href="mf-mt-frame-size-attribute.md"><strong>MF_MT_FRAME_SIZE</strong></a></span><span class="sxs-lookup"><span data-stu-id="318e5-138"><a href="mf-mt-frame-size-attribute.md"><strong>MF_MT_FRAME_SIZE</strong></a></span></span></td>
<td><span data-ttu-id="318e5-139">Dimensioni del frame.</span><span class="sxs-lookup"><span data-stu-id="318e5-139">Frame size.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="318e5-140"><a href="mf-mt-interlace-mode-attribute.md"><strong>MF_MT_INTERLACE_MODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="318e5-140"><a href="mf-mt-interlace-mode-attribute.md"><strong>MF_MT_INTERLACE_MODE</strong></a></span></span></td>
<td><span data-ttu-id="318e5-141">Modalità interlacciamento.</span><span class="sxs-lookup"><span data-stu-id="318e5-141">Interlace mode.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="318e5-142"><a href="mf-mt-mpeg2-profile-attribute.md"><strong>MF_MT_MPEG2_PROFILE</strong></a></span><span class="sxs-lookup"><span data-stu-id="318e5-142"><a href="mf-mt-mpeg2-profile-attribute.md"><strong>MF_MT_MPEG2_PROFILE</strong></a></span></span></td>
<td><span data-ttu-id="318e5-143">Profilo di codifica H. 264.</span><span class="sxs-lookup"><span data-stu-id="318e5-143">H.264 encoding profile.</span></span><br/> <span data-ttu-id="318e5-144">I valori supportati sono:</span><span class="sxs-lookup"><span data-stu-id="318e5-144">The supported values are:</span></span><br/>
<ul>
<li><span data-ttu-id="318e5-145"><strong>eAVEncH264VProfile_Base</strong> (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="318e5-145"><strong>eAVEncH264VProfile_Base</strong> (default)</span></span></li>
<li><span data-ttu-id="318e5-146"><strong>eAVEncH264VProfile_Main</strong></span><span class="sxs-lookup"><span data-stu-id="318e5-146"><strong>eAVEncH264VProfile_Main</strong></span></span></li>
<li><span data-ttu-id="318e5-147"><strong>eAVEncH264VProfile_High</strong> (richiede Windows 8)</span><span class="sxs-lookup"><span data-stu-id="318e5-147"><strong>eAVEncH264VProfile_High</strong> (requires Windows 8)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="318e5-148"><a href="mf-mt-mpeg2-level-attribute.md"><strong>MF_MT_MPEG2_LEVEL</strong></a></span><span class="sxs-lookup"><span data-stu-id="318e5-148"><a href="mf-mt-mpeg2-level-attribute.md"><strong>MF_MT_MPEG2_LEVEL</strong></a></span></span></td>
<td><span data-ttu-id="318e5-149">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="318e5-149">Optional.</span></span> <span data-ttu-id="318e5-150">Specifica il livello di codifica H. 264.</span><span class="sxs-lookup"><span data-stu-id="318e5-150">Specifies the H.264 encoding level.</span></span><br/> <span data-ttu-id="318e5-151">Il valore predefinito è-1, che indica che il codificatore selezionerà il livello di codifica.</span><span class="sxs-lookup"><span data-stu-id="318e5-151">The default value is –1, indicating that the encoder will select the encoding level.</span></span><br/> <span data-ttu-id="318e5-152">È consigliabile non impostare il livello nel tipo di supporto e consentire al codificatore di selezionare il livello.</span><span class="sxs-lookup"><span data-stu-id="318e5-152">It is recommended not to set the level in the media type, and allow the encoder to select the level.</span></span> <span data-ttu-id="318e5-153">Il codificatore può derivare il livello appropriato per un determinato flusso video, prendendo in considerazione i vincoli di formato e le caratteristiche del video.</span><span class="sxs-lookup"><span data-stu-id="318e5-153">The encoder can derive the proper level for a given video stream, taking into account the format constraints and the characteristics of the video.</span></span> <span data-ttu-id="318e5-154">Per ulteriori informazioni sui vincoli di profilo e di livello, vedere l'allegato A di ITU-T H. 264.</span><span class="sxs-lookup"><span data-stu-id="318e5-154">For more information about profile and level constraints, refer to Annex A of ITU-T H.264.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="318e5-155"><a href="mf-mt-pixel-aspect-ratio-attribute.md"><strong>MF_MT_PIXEL_ASPECT_RATIO</strong></a></span><span class="sxs-lookup"><span data-stu-id="318e5-155"><a href="mf-mt-pixel-aspect-ratio-attribute.md"><strong>MF_MT_PIXEL_ASPECT_RATIO</strong></a></span></span></td>
<td><span data-ttu-id="318e5-156">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="318e5-156">Optional.</span></span> <span data-ttu-id="318e5-157">Specifica le proporzioni in pixel.</span><span class="sxs-lookup"><span data-stu-id="318e5-157">Specifies the pixel aspect ratio.</span></span> <span data-ttu-id="318e5-158">Il valore predefinito è 1:1.</span><span class="sxs-lookup"><span data-stu-id="318e5-158">The default value is 1:1.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="318e5-159">Dopo aver impostato il tipo di output, il codificatore video aggiorna il tipo aggiungendo l'attributo [**MF_MT_MPEG_SEQUENCE_HEADER**](mf-mt-mpeg-sequence-header-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="318e5-159">After the output type is set, the video encoder updates the type by adding the [**MF_MT_MPEG_SEQUENCE_HEADER**](mf-mt-mpeg-sequence-header-attribute.md) attribute.</span></span> <span data-ttu-id="318e5-160">Questo attributo contiene l'intestazione della sequenza.</span><span class="sxs-lookup"><span data-stu-id="318e5-160">This attribute contains the sequence header.</span></span>

## <a name="codec-properties"></a><span data-ttu-id="318e5-161">Proprietà codec</span><span class="sxs-lookup"><span data-stu-id="318e5-161">Codec Properties</span></span>

<span data-ttu-id="318e5-162">Il codificatore H. 264 implementa l'interfaccia [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) per l'impostazione dei parametri di codifica.</span><span class="sxs-lookup"><span data-stu-id="318e5-162">The H.264 encoder implements the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface for setting encoding parameters.</span></span> <span data-ttu-id="318e5-163">Supporta le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="318e5-163">It supports the following properties.</span></span>

<span data-ttu-id="318e5-164">Per i requisiti di codec per la certificazione del codificatore HCK, vedere la sezione relativa al **codificatore hardware certificato** di seguito.</span><span class="sxs-lookup"><span data-stu-id="318e5-164">For the codec requirements for HCK encoder certification, see the **Certified Hardware Encoder** section below.</span></span>

<span data-ttu-id="318e5-165">Le proprietà seguenti sono supportate in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="318e5-165">The following properties are supported in Windows 7.</span></span>



| <span data-ttu-id="318e5-166">Proprietà</span><span class="sxs-lookup"><span data-stu-id="318e5-166">Property</span></span>                                                                              | <span data-ttu-id="318e5-167">Descrizione</span><span class="sxs-lookup"><span data-stu-id="318e5-167">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="318e5-168">**CODECAPI_AVEncCommonRateControlMode**</span><span class="sxs-lookup"><span data-stu-id="318e5-168">**CODECAPI_AVEncCommonRateControlMode**</span></span>](../directshow/avenccommonratecontrolmode-property.md) | <span data-ttu-id="318e5-169">Imposta la modalità di controllo della frequenza.</span><span class="sxs-lookup"><span data-stu-id="318e5-169">Sets the rate control mode.</span></span> <span data-ttu-id="318e5-170">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="318e5-170">See Remarks.</span></span> <span data-ttu-id="318e5-171">La modalità predefinita è la velocità in bit variabile (VBR) non vincolata.</span><span class="sxs-lookup"><span data-stu-id="318e5-171">The default mode is unconstrained variable bit rate (VBR).</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="318e5-172">**CODECAPI_AVEncCommonQuality**</span><span class="sxs-lookup"><span data-stu-id="318e5-172">**CODECAPI_AVEncCommonQuality**</span></span>](../directshow/avenccommonquality-property.md)                 | <span data-ttu-id="318e5-173">Imposta il livello di qualità.</span><span class="sxs-lookup"><span data-stu-id="318e5-173">Sets the quality level.</span></span> <span data-ttu-id="318e5-174">Questa proprietà si applica quando la modalità di controllo della velocità è VBR basata sulla qualità (**eAVEncCommonRateControlMode_Quality**).</span><span class="sxs-lookup"><span data-stu-id="318e5-174">This property applies when the rate control mode is quality-based VBR (**eAVEncCommonRateControlMode_Quality**).</span></span> <span data-ttu-id="318e5-175">L'intervallo valido è compreso tra 1 e 100.</span><span class="sxs-lookup"><span data-stu-id="318e5-175">The valid range is 1–100.</span></span> <span data-ttu-id="318e5-176">Il valore predefinito è 70.</span><span class="sxs-lookup"><span data-stu-id="318e5-176">The default value is 70.</span></span> <br/> <span data-ttu-id="318e5-177">Per impostare questo parametro, impostare la proprietà prima di chiamare [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span><span class="sxs-lookup"><span data-stu-id="318e5-177">To set this parameter, set the property before calling [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span></span> <br/> <span data-ttu-id="318e5-178">Per impostare questo parametro in Windows 7, impostare la proprietà prima di chiamare [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span><span class="sxs-lookup"><span data-stu-id="318e5-178">To set this parameter in Windows 7, set the property before calling [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span></span> <span data-ttu-id="318e5-179">Il codificatore ignora le modifiche dopo l'impostazione del tipo di output.</span><span class="sxs-lookup"><span data-stu-id="318e5-179">The encoder ignores changes after the output type is set.</span></span> <br/> <span data-ttu-id="318e5-180">In Windows 8, questa proprietà può essere impostata in qualsiasi momento durante la codifica.</span><span class="sxs-lookup"><span data-stu-id="318e5-180">In Windows 8, this property can be set at any time during encoding.</span></span> <span data-ttu-id="318e5-181">Le modifiche vengono applicate a partire dal frame di input successivo.</span><span class="sxs-lookup"><span data-stu-id="318e5-181">Changes are applied starting at the next input frame.</span></span> <br/> <span data-ttu-id="318e5-182">Internamente, il codificatore converte questa proprietà in un valore [AVEncVideoEncodeQP](codecapi-avencvideoencodeqp.md) .</span><span class="sxs-lookup"><span data-stu-id="318e5-182">Internally, the encoder converts this property to an [AVEncVideoEncodeQP](codecapi-avencvideoencodeqp.md) value.</span></span> <br/> |



 

<span data-ttu-id="318e5-183">Per le seguenti proprietà è necessario Windows 8.</span><span class="sxs-lookup"><span data-stu-id="318e5-183">The following properties require Windows 8.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="318e5-184">Proprietà</span><span class="sxs-lookup"><span data-stu-id="318e5-184">Property</span></span></th>
<th><span data-ttu-id="318e5-185">Descrizione</span><span class="sxs-lookup"><span data-stu-id="318e5-185">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="318e5-186"><a href="codecapi-avencadaptivemode.md">CODECAPI_AVEncAdaptiveMode</a></span><span class="sxs-lookup"><span data-stu-id="318e5-186"><a href="codecapi-avencadaptivemode.md">CODECAPI_AVEncAdaptiveMode</a></span></span></td>
<td><span data-ttu-id="318e5-187">Imposta la modalità di codifica adattiva.</span><span class="sxs-lookup"><span data-stu-id="318e5-187">Sets the adaptive encoding mode.</span></span> <span data-ttu-id="318e5-188">Il codificatore H. 264 supporta le modalità seguenti in Windows 8:</span><span class="sxs-lookup"><span data-stu-id="318e5-188">The H.264 encoder supports the following modes in Windows 8:</span></span>
<ul>
<li><span data-ttu-id="318e5-189"><strong>eAVEncAdaptiveMode_None</strong>.</span><span class="sxs-lookup"><span data-stu-id="318e5-189"><strong>eAVEncAdaptiveMode_None</strong>.</span></span> <span data-ttu-id="318e5-190">Nessuna codifica adattiva.</span><span class="sxs-lookup"><span data-stu-id="318e5-190">No adaptive encoding.</span></span> <span data-ttu-id="318e5-191">(impostazione predefinita).</span><span class="sxs-lookup"><span data-stu-id="318e5-191">(Default.)</span></span></li>
<li><span data-ttu-id="318e5-192"><strong>eAVEncAdaptiveMode_FrameRate</strong>.</span><span class="sxs-lookup"><span data-stu-id="318e5-192"><strong>eAVEncAdaptiveMode_FrameRate</strong>.</span></span> <span data-ttu-id="318e5-193">In modo adattivo modificare la frequenza dei fotogrammi.</span><span class="sxs-lookup"><span data-stu-id="318e5-193">Adaptively change the frame rate.</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="318e5-194"><a href="/windows/desktop/DirectShow/avenccommonbuffersize-property">CODECAPI_AVEncCommonBufferSize</a></span><span class="sxs-lookup"><span data-stu-id="318e5-194"><a href="/windows/desktop/DirectShow/avenccommonbuffersize-property">CODECAPI_AVEncCommonBufferSize</a></span></span></td>
<td><span data-ttu-id="318e5-195">Imposta la dimensione del buffer, in byte, per la codifica di velocità in bit costante (CBR).</span><span class="sxs-lookup"><span data-stu-id="318e5-195">Sets the buffer size, in bytes, for constant bit rate (CBR) encoding.</span></span><br/> <span data-ttu-id="318e5-196">L'intervallo valido è [1... 2 ³ ² – 1].</span><span class="sxs-lookup"><span data-stu-id="318e5-196">The valid range is [1 ... 2³²–1].</span></span> <br/> <span data-ttu-id="318e5-197">Richiede Windows 8.</span><span class="sxs-lookup"><span data-stu-id="318e5-197">Requires Windows 8.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="318e5-198"><a href="/windows/desktop/DirectShow/avenccommonmaxbitrate-property">CODECAPI_AVEncCommonMaxBitRate</a></span><span class="sxs-lookup"><span data-stu-id="318e5-198"><a href="/windows/desktop/DirectShow/avenccommonmaxbitrate-property">CODECAPI_AVEncCommonMaxBitRate</a></span></span></td>
<td><span data-ttu-id="318e5-199">Per la codifica VBR vincolata, specifica la frequenza con cui &quot; &quot; viene svuotato il bucket di perdita, in bit al secondo.</span><span class="sxs-lookup"><span data-stu-id="318e5-199">For constrained VBR encoding, specifies the rate at which the &quot;leaky bucket&quot; is drained, in bits per second.</span></span> <span data-ttu-id="318e5-200">Questa proprietà si applica quando la modalità di controllo della velocità è <strong>eAVEncCommonRateControlMode_PeakConstrainedVBR</strong>.</span><span class="sxs-lookup"><span data-stu-id="318e5-200">This property applies when the rate control mode is <strong>eAVEncCommonRateControlMode_PeakConstrainedVBR</strong>.</span></span> <br/> <span data-ttu-id="318e5-201">L'intervallo valido è [1... 2 ³ ² – 1].</span><span class="sxs-lookup"><span data-stu-id="318e5-201">The valid range is [1 ... 2³²–1].</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="318e5-202"><a href="/windows/desktop/DirectShow/avenccommonmeanbitrate-property">CODECAPI_AVEncCommonMeanBitRate</a></span><span class="sxs-lookup"><span data-stu-id="318e5-202"><a href="/windows/desktop/DirectShow/avenccommonmeanbitrate-property">CODECAPI_AVEncCommonMeanBitRate</a></span></span></td>
<td><span data-ttu-id="318e5-203">Imposta la velocità in bit media per il flusso di bit codificato, in bit al secondo.</span><span class="sxs-lookup"><span data-stu-id="318e5-203">Sets the average bit rate for the encoded bit stream, in bits per second.</span></span> <span data-ttu-id="318e5-204">Questa proprietà viene ignorata se la modalità di controllo della velocità è <strong>eAVEncCommonRateControlMode_Quality</strong>.</span><span class="sxs-lookup"><span data-stu-id="318e5-204">This property is ignored if the rate control mode is <strong>eAVEncCommonRateControlMode_Quality</strong>.</span></span> <br/> <span data-ttu-id="318e5-205">L'intervallo valido è [1... 2 ³ ² – 1].</span><span class="sxs-lookup"><span data-stu-id="318e5-205">The valid range is [1 ... 2³²–1].</span></span> <br/> <span data-ttu-id="318e5-206">Nelle modalità CBR e VBR non vincolate la velocità in bit media determina la dimensione finale del file.</span><span class="sxs-lookup"><span data-stu-id="318e5-206">In CBR and unconstrained VBR modes, the average bit rate determines the final size of the file.</span></span> <span data-ttu-id="318e5-207">In modalità CBR la velocità in bit media è anche la velocità con cui i bit compressi vengono svuotati dal &quot; bucket di perdita. &quot; per ulteriori informazioni, vedere <a href="the-leaky-bucket-buffer-model.md">il modello di buffer di bucket a perdita</a>.</span><span class="sxs-lookup"><span data-stu-id="318e5-207">In CBR mode, the average bit rate is also the rate at which compressed bits are drained from the &quot;leaky bucket.&quot; (For more information, see <a href="the-leaky-bucket-buffer-model.md">The Leaky Bucket Buffer Model</a>.)</span></span> <br/> <span data-ttu-id="318e5-208">In Windows 7, la velocità in bit media viene specificata dall'attributo <a href="mf-mt-avg-bitrate-attribute.md">MF_MT_AVG_BITRATE</a> nel tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="318e5-208">In Windows 7, the average bit rate is specified by the <a href="mf-mt-avg-bitrate-attribute.md">MF_MT_AVG_BITRATE</a> attribute on the media type.</span></span> <br/> <span data-ttu-id="318e5-209">In Windows 8 è possibile impostare la velocità in bit media usando l'attributo <a href="mf-mt-avg-bitrate-attribute.md">MF_MT_AVG_BITRATE</a> o la proprietà <a href="/windows/desktop/DirectShow/avenccommonmeanbitrate-property">CODECAPI_AVEncCommonMeanBitRate</a> .</span><span class="sxs-lookup"><span data-stu-id="318e5-209">In Windows 8, you can set the average bit rate using either the <a href="mf-mt-avg-bitrate-attribute.md">MF_MT_AVG_BITRATE</a> attribute or the <a href="/windows/desktop/DirectShow/avenccommonmeanbitrate-property">CODECAPI_AVEncCommonMeanBitRate</a> property.</span></span> <span data-ttu-id="318e5-210">Se entrambe le impostazioni sono impostate, CODECAPI_AVEncCommonMeanBitRate esegue l'override di.</span><span class="sxs-lookup"><span data-stu-id="318e5-210">If both are set, CODECAPI_AVEncCommonMeanBitRate overrides.</span></span> <span data-ttu-id="318e5-211">In Windows 8 è possibile impostare la velocità in bit media durante la codifica.</span><span class="sxs-lookup"><span data-stu-id="318e5-211">In Windows 8, you can set the average bit rate during encoding.</span></span> <span data-ttu-id="318e5-212">Se la velocità in bit viene modificata, il codificatore utilizza la codifica adattiva.</span><span class="sxs-lookup"><span data-stu-id="318e5-212">If the bit rate changes, the encoder uses adaptive encoding.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="318e5-213"><a href="/windows/desktop/DirectShow/avenccommonqualityvsspeed-property">CODECAPI_AVEncCommonQualityVsSpeed</a></span><span class="sxs-lookup"><span data-stu-id="318e5-213"><a href="/windows/desktop/DirectShow/avenccommonqualityvsspeed-property">CODECAPI_AVEncCommonQualityVsSpeed</a></span></span></td>
<td><span data-ttu-id="318e5-214">Imposta il compromesso di qualità/velocità.</span><span class="sxs-lookup"><span data-stu-id="318e5-214">Sets the quality/speed tradeoff.</span></span> <span data-ttu-id="318e5-215">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="318e5-215">Valid range:</span></span>
<ul>
<li><span data-ttu-id="318e5-216">0 – 33: complessità bassa</span><span class="sxs-lookup"><span data-stu-id="318e5-216">0–33: Low complexity</span></span></li>
<li><span data-ttu-id="318e5-217">34 – 66: complessità media (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="318e5-217">34–66: Medium complexity (default)</span></span></li>
<li><span data-ttu-id="318e5-218">67 – 100: complessità elevata</span><span class="sxs-lookup"><span data-stu-id="318e5-218">67–100: High complexity</span></span></li>
</ul>
<br/> <span data-ttu-id="318e5-219">Questo valore influiscono sul modo in cui il codificatore esegue diverse operazioni di codifica, ad esempio la compensazione del movimento.</span><span class="sxs-lookup"><span data-stu-id="318e5-219">This value affects how the encoder performs various encoding operations, such as motion compensation.</span></span> <span data-ttu-id="318e5-220">A livelli di complessità più elevati, il codificatore viene eseguito più lentamente, ma produce una qualità migliore con la stessa velocità in bit.</span><span class="sxs-lookup"><span data-stu-id="318e5-220">At higher complexity levels, the encoder runs more slowly but produces better quality at the same bit rate.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="318e5-221"><a href="codecapi-avench264cabacenable.md">CODECAPI_AVEncH264CABACEnable</a></span><span class="sxs-lookup"><span data-stu-id="318e5-221"><a href="codecapi-avench264cabacenable.md">CODECAPI_AVEncH264CABACEnable</a></span></span></td>
<td><span data-ttu-id="318e5-222">Abilita o Disabilita CABAC (codice aritmetico binario adattivo per il contesto) per la codifica dell'entropia H. 264.</span><span class="sxs-lookup"><span data-stu-id="318e5-222">Enables or disables CABAC (context-adaptive binary arithmetic coding) for H.264 entropy coding.</span></span> <span data-ttu-id="318e5-223">Il valore predefinito è <strong>VARIANT_FALSE</strong>.</span><span class="sxs-lookup"><span data-stu-id="318e5-223">The default value is <strong>VARIANT_FALSE</strong>.</span></span> <br/> <span data-ttu-id="318e5-224">CABAC non viene usato per il profilo di base.</span><span class="sxs-lookup"><span data-stu-id="318e5-224">CABAC is not used for Baseline profile.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="318e5-225"><a href="codecapi-avench264spsid.md">CODECAPI_AVEncH264SPSID</a></span><span class="sxs-lookup"><span data-stu-id="318e5-225"><a href="codecapi-avench264spsid.md">CODECAPI_AVEncH264SPSID</a></span></span></td>
<td><span data-ttu-id="318e5-226">Imposta il valore di <strong>seq_parameter_set_id</strong> nell'unità SPS nal del Bitstream H. 264.</span><span class="sxs-lookup"><span data-stu-id="318e5-226">Sets the value of <strong>seq_parameter_set_id</strong> in the SPS NAL unit of the H.264 bitstream.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="318e5-227"><a href="/windows/desktop/DirectShow/avencmpvdefaultbpicturecount-property">CODECAPI_AVEncMPVDefaultBPictureCount</a></span><span class="sxs-lookup"><span data-stu-id="318e5-227"><a href="/windows/desktop/DirectShow/avencmpvdefaultbpicturecount-property">CODECAPI_AVEncMPVDefaultBPictureCount</a></span></span></td>
<td><span data-ttu-id="318e5-228">Imposta il numero massimo di fotogrammi B consecutivi nel bitstream di output.</span><span class="sxs-lookup"><span data-stu-id="318e5-228">Sets the maximum number of consecutive B frames in the output bitstream.</span></span> <span data-ttu-id="318e5-229">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="318e5-229">Valid values are:</span></span>
<ul>
<li><span data-ttu-id="318e5-230">0: non usare i frame B (impostazione predefinita).</span><span class="sxs-lookup"><span data-stu-id="318e5-230">0: Do not use B frames (default).</span></span></li>
<li><span data-ttu-id="318e5-231">1: usare un frame B.</span><span class="sxs-lookup"><span data-stu-id="318e5-231">1: Use one B frame.</span></span></li>
<li><span data-ttu-id="318e5-232">2: usare due fotogrammi B.</span><span class="sxs-lookup"><span data-stu-id="318e5-232">2: Use two B frames.</span></span></li>
</ul>
<span data-ttu-id="318e5-233">Per impostare questo parametro, impostare la proprietà prima di chiamare <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype"><strong>IMFTransform:: SetOutputType</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="318e5-233">To set this parameter, set the property before calling <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype"><strong>IMFTransform::SetOutputType</strong></a>.</span></span> <br/> <span data-ttu-id="318e5-234">Per il profilo di base, il numero di fotogrammi B è sempre zero.</span><span class="sxs-lookup"><span data-stu-id="318e5-234">For Baseline profile, the number of B frames is always zero.</span></span> <span data-ttu-id="318e5-235">Il codificatore eseguirà l'override dei valori diversi da zero.</span><span class="sxs-lookup"><span data-stu-id="318e5-235">The encoder will override nonzero values.</span></span><br/> <span data-ttu-id="318e5-236">Per gli altri profili H. 264, se questa proprietà è diversa da zero, il modello di codifica è IBBPBBP, in cui il numero massimo di fotogrammi B consecutivi è uguale a <a href="/windows/desktop/DirectShow/avencmpvdefaultbpicturecount-property">CODECAPI_AVEncMPVDefaultBPictureCount</a>.</span><span class="sxs-lookup"><span data-stu-id="318e5-236">For other H.264 profiles, if this property is nonzero, the encoding pattern is IBBPBBP, where the maximum number of consecutive B frames is equal to <a href="/windows/desktop/DirectShow/avencmpvdefaultbpicturecount-property">CODECAPI_AVEncMPVDefaultBPictureCount</a>.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="318e5-237"><a href="/windows/desktop/DirectShow/avencmpvgopsize-property">CODECAPI_AVEncMPVGOPSize</a></span><span class="sxs-lookup"><span data-stu-id="318e5-237"><a href="/windows/desktop/DirectShow/avencmpvgopsize-property">CODECAPI_AVEncMPVGOPSize</a></span></span></td>
<td><span data-ttu-id="318e5-238">Imposta il numero di immagini da un'intestazione GOP alla successiva, incluso l'ancoraggio principale ma non quello seguente.</span><span class="sxs-lookup"><span data-stu-id="318e5-238">Sets the number of pictures from one GOP header to the next, including the leading anchor but not the following one.</span></span> <br/> <span data-ttu-id="318e5-239">L'intervallo valido è [0... 2 ³ ² – 1].</span><span class="sxs-lookup"><span data-stu-id="318e5-239">The valid range is [0 ... 2³²–1].</span></span> <span data-ttu-id="318e5-240">Se il valore è zero, il codificatore seleziona la dimensione GOP.</span><span class="sxs-lookup"><span data-stu-id="318e5-240">If zero, the encoder selects the GOP size.</span></span> <span data-ttu-id="318e5-241">Il valore predefinito è zero.</span><span class="sxs-lookup"><span data-stu-id="318e5-241">The default value is zero.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="318e5-242"><a href="codecapi-avencnumworkerthreads.md">CODECAPI_AVEncNumWorkerThreads</a></span><span class="sxs-lookup"><span data-stu-id="318e5-242"><a href="codecapi-avencnumworkerthreads.md">CODECAPI_AVEncNumWorkerThreads</a></span></span></td>
<td><span data-ttu-id="318e5-243">Imposta il numero di thread di lavoro utilizzati da un codificatore.</span><span class="sxs-lookup"><span data-stu-id="318e5-243">Sets the number of worker threads used by a encoder.</span></span><br/> <span data-ttu-id="318e5-244">L'intervallo valido è compreso tra 0 e 16.</span><span class="sxs-lookup"><span data-stu-id="318e5-244">The valid range is 0–16.</span></span> <span data-ttu-id="318e5-245">Se è zero, il codificatore seleziona il numero di thread.</span><span class="sxs-lookup"><span data-stu-id="318e5-245">If zero, the encoder selects the number of threads.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="318e5-246"><a href="codecapi-avencvideocontenttype.md">CODECAPI_AVEncVideoContentType</a></span><span class="sxs-lookup"><span data-stu-id="318e5-246"><a href="codecapi-avencvideocontenttype.md">CODECAPI_AVEncVideoContentType</a></span></span></td>
<td><span data-ttu-id="318e5-247">Indica il tipo di contenuto video.</span><span class="sxs-lookup"><span data-stu-id="318e5-247">Indicates the type of video content.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="318e5-248"><a href="codecapi-avencvideoencodeqp.md">CODECAPI_AVEncVideoEncodeQP</a></span><span class="sxs-lookup"><span data-stu-id="318e5-248"><a href="codecapi-avencvideoencodeqp.md">CODECAPI_AVEncVideoEncodeQP</a></span></span></td>
<td><span data-ttu-id="318e5-249">Intervallo valido: 16-51.</span><span class="sxs-lookup"><span data-stu-id="318e5-249">Valid range: 16–51.</span></span> <span data-ttu-id="318e5-250">Il valore predefinito è 24.</span><span class="sxs-lookup"><span data-stu-id="318e5-250">The default value is 24.</span></span> <br/> <span data-ttu-id="318e5-251">Questa proprietà si applica quando la modalità di controllo della velocità è <strong>eAVEncCommonRateControlMode_Quality</strong>.</span><span class="sxs-lookup"><span data-stu-id="318e5-251">This property applies when the rate control mode is <strong>eAVEncCommonRateControlMode_Quality</strong>.</span></span> <br/> <span data-ttu-id="318e5-252">Questa proprietà configura la stessa impostazione di codifica di <a href="/windows/desktop/DirectShow/avenccommonquality-property"><strong>AVEncCommonQuality</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="318e5-252">This property configures the same encoding setting as <a href="/windows/desktop/DirectShow/avenccommonquality-property"><strong>AVEncCommonQuality</strong></a>.</span></span> <span data-ttu-id="318e5-253">Tuttavia, <a href="codecapi-avencvideoencodeqp.md">AVEncVideoEncodeQP</a> consente all'applicazione di specificare direttamente il valore di QP.</span><span class="sxs-lookup"><span data-stu-id="318e5-253">However, <a href="codecapi-avencvideoencodeqp.md">AVEncVideoEncodeQP</a> enables the application to specify the value of QP directly.</span></span> <span data-ttu-id="318e5-254">Se entrambe le proprietà sono impostate, AVEncVideoEncodeQP esegue l'override di.</span><span class="sxs-lookup"><span data-stu-id="318e5-254">If both properties are set, AVEncVideoEncodeQP overrides.</span></span> <br/> <span data-ttu-id="318e5-255">Il valore predefinito di 24 corrisponde al valore predefinito 70 per l'impostazione <a href="/windows/desktop/DirectShow/avenccommonquality-property"><strong>AVEncCommonQuality</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="318e5-255">The default value of 24 corresponds to the default value of 70 for the <a href="/windows/desktop/DirectShow/avenccommonquality-property"><strong>AVEncCommonQuality</strong></a> setting.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="318e5-256"><a href="codecapi-avencvideoforcekeyframe.md">CODECAPI_AVEncVideoForceKeyFrame</a></span><span class="sxs-lookup"><span data-stu-id="318e5-256"><a href="codecapi-avencvideoforcekeyframe.md">CODECAPI_AVEncVideoForceKeyFrame</a></span></span></td>
<td><span data-ttu-id="318e5-257">Impone al codificatore di codificare il fotogramma successivo come fotogramma chiave.</span><span class="sxs-lookup"><span data-stu-id="318e5-257">Forces the encoder to code the next frame as a key frame.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="318e5-258"><a href="codecapi-avencvideominqp.md">CODECAPI_AVEncVideoMinQP</a></span><span class="sxs-lookup"><span data-stu-id="318e5-258"><a href="codecapi-avencvideominqp.md">CODECAPI_AVEncVideoMinQP</a></span></span></td>
<td><span data-ttu-id="318e5-259">Intervallo valido: 0 – 51.</span><span class="sxs-lookup"><span data-stu-id="318e5-259">Valid range: 0–51.</span></span> <span data-ttu-id="318e5-260">Il valore predefinito è 0.</span><span class="sxs-lookup"><span data-stu-id="318e5-260">The default value is 0.</span></span> <br/> <span data-ttu-id="318e5-261">Questa proprietà si applica a tutte le modalità di controllo della frequenza.</span><span class="sxs-lookup"><span data-stu-id="318e5-261">This property applies to all rate control modes.</span></span> <span data-ttu-id="318e5-262">Il codificatore non deve produrre un valore QP inferiore a quello specificato dalla proprietà <a href="codecapi-avencvideominqp.md">CODECAPI_AVEncVideoMinQP</a> .</span><span class="sxs-lookup"><span data-stu-id="318e5-262">The encoder should not produce a QP value lower than what is specified by the <a href="codecapi-avencvideominqp.md">CODECAPI_AVEncVideoMinQP</a> property.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="318e5-263"><a href="codecapi-avlowlatencymode.md">CODECAPI_AVLowLatencyMode</a></span><span class="sxs-lookup"><span data-stu-id="318e5-263"><a href="codecapi-avlowlatencymode.md">CODECAPI_AVLowLatencyMode</a></span></span></td>
<td><span data-ttu-id="318e5-264">Abilita o Disabilita la modalità a bassa latenza.</span><span class="sxs-lookup"><span data-stu-id="318e5-264">Enables or disables low-latency mode.</span></span> <span data-ttu-id="318e5-265">Vedere &quot; multithreading &quot; nella sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="318e5-265">See &quot;Multithreading&quot; in the Remarks section.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="318e5-266">Commenti</span><span class="sxs-lookup"><span data-stu-id="318e5-266">Remarks</span></span>

<span data-ttu-id="318e5-267">Il codificatore supporta le modalità di controllo della frequenza seguenti.</span><span class="sxs-lookup"><span data-stu-id="318e5-267">The encoder supports the following rate control modes.</span></span>



| <span data-ttu-id="318e5-268">Modalità</span><span class="sxs-lookup"><span data-stu-id="318e5-268">Mode</span></span>                                  | <span data-ttu-id="318e5-269">Costante</span><span class="sxs-lookup"><span data-stu-id="318e5-269">Constant</span></span>                                            | <span data-ttu-id="318e5-270">Descrizione</span><span class="sxs-lookup"><span data-stu-id="318e5-270">Description</span></span>                                                                                                                                                                                                                                         |
|---------------------------------------|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="318e5-271">Velocità in bit costante (CBR)</span><span class="sxs-lookup"><span data-stu-id="318e5-271">Constant bit rate (CBR)</span></span>               | <span data-ttu-id="318e5-272">**eAVEncCommonRateControlMode_CBR**</span><span class="sxs-lookup"><span data-stu-id="318e5-272">**eAVEncCommonRateControlMode_CBR**</span></span>                | <span data-ttu-id="318e5-273">Il codificatore tenta di ottenere una velocità in bit costante, usando un modello "bucket Leak".</span><span class="sxs-lookup"><span data-stu-id="318e5-273">The encoder tries to achieve a constant bit rate, using a "leaky bucket" model.</span></span> <span data-ttu-id="318e5-274">La velocità in bit di destinazione viene fornita dalla proprietà [CODECAPI_AVEncCommonMeanBitRate](../directshow/avenccommonmeanbitrate-property.md) .</span><span class="sxs-lookup"><span data-stu-id="318e5-274">The target bit rate is given by the [CODECAPI_AVEncCommonMeanBitRate](../directshow/avenccommonmeanbitrate-property.md) property.</span></span> <br/> <span data-ttu-id="318e5-275">Richiede Windows 8.</span><span class="sxs-lookup"><span data-stu-id="318e5-275">Requires Windows 8.</span></span> <br/> |
| <span data-ttu-id="318e5-276">Velocità in bit variabile vincolata (VBR)</span><span class="sxs-lookup"><span data-stu-id="318e5-276">Constrained variable bit rate (VBR)</span></span>   | <span data-ttu-id="318e5-277">**eAVEncCommonRateControlMode_PeakConstrainedVBR**</span><span class="sxs-lookup"><span data-stu-id="318e5-277">**eAVEncCommonRateControlMode_PeakConstrainedVBR**</span></span> | <span data-ttu-id="318e5-278">Il codificatore usa un modello di "bucket a perdita" con una velocità in bit massima.</span><span class="sxs-lookup"><span data-stu-id="318e5-278">The encoder uses a "leaky bucket" model with a peak bit rate.</span></span> <span data-ttu-id="318e5-279">La velocità di svuotamento per il bucket perso è determinata dalla proprietà [CODECAPI_AVEncCommonMaxBitRate](../directshow/avenccommonmaxbitrate-property.md) .</span><span class="sxs-lookup"><span data-stu-id="318e5-279">The drain rate for the leaky bucket is given by the [CODECAPI_AVEncCommonMaxBitRate](../directshow/avenccommonmaxbitrate-property.md) property.</span></span> <br/> <span data-ttu-id="318e5-280">Richiede Windows 8.</span><span class="sxs-lookup"><span data-stu-id="318e5-280">Requires Windows 8.</span></span> <br/>     |
| <span data-ttu-id="318e5-281">Velocità in bit della variabile basata sulla qualità (VBR)</span><span class="sxs-lookup"><span data-stu-id="318e5-281">Quality-based variable bit rate (VBR)</span></span> | <span data-ttu-id="318e5-282">**eAVEncCommonRateControlMode_Quality**</span><span class="sxs-lookup"><span data-stu-id="318e5-282">**eAVEncCommonRateControlMode_Quality**</span></span>            | <span data-ttu-id="318e5-283">Il codificatore tenta di ottenere un livello di qualità costante, fornito dalla proprietà [**AVEncCommonQuality**](../directshow/avenccommonquality-property.md) .</span><span class="sxs-lookup"><span data-stu-id="318e5-283">The encoder tries to achieve a constant quality level, given by the [**AVEncCommonQuality**](../directshow/avenccommonquality-property.md) property.</span></span>                                                                                                           |
| <span data-ttu-id="318e5-284">VBR non vincolato</span><span class="sxs-lookup"><span data-stu-id="318e5-284">Unconstrained VBR</span></span>                     | <span data-ttu-id="318e5-285">**eAVEncCommonRateControlMode_UnconstrainedVBR**</span><span class="sxs-lookup"><span data-stu-id="318e5-285">**eAVEncCommonRateControlMode_UnconstrainedVBR**</span></span>   | <span data-ttu-id="318e5-286">Il codificatore tenta di ottenere la velocità in bit di destinazione fornita dall'attributo [**MF_MT_AVG_BITRATE**](mf-mt-avg-bitrate-attribute.md) nel tipo di supporto di output.</span><span class="sxs-lookup"><span data-stu-id="318e5-286">The encoder tries to achieve the target bitrate given by the [**MF_MT_AVG_BITRATE**](mf-mt-avg-bitrate-attribute.md) attribute in the output media type.</span></span> <span data-ttu-id="318e5-287">Si tratta della modalità predefinita.</span><span class="sxs-lookup"><span data-stu-id="318e5-287">This is the default mode.</span></span>                                                              |



 

<span data-ttu-id="318e5-288">Le modalità CBR e VBR vincolate richiedono Windows 8.</span><span class="sxs-lookup"><span data-stu-id="318e5-288">CBR and constrained VBR modes require Windows 8.</span></span>

<span data-ttu-id="318e5-289">In Windows 8, il codificatore imposta gli attributi seguenti sugli esempi di output:</span><span class="sxs-lookup"><span data-stu-id="318e5-289">In Windows 8, the encoder sets the following attributes on the output samples:</span></span>

-   [<span data-ttu-id="318e5-290">MFSampleExtension_DecodeTimestamp</span><span class="sxs-lookup"><span data-stu-id="318e5-290">MFSampleExtension_DecodeTimestamp</span></span>](mfsampleextension-decodetimestamp.md)
-   [<span data-ttu-id="318e5-291">MFSampleExtension_VideoEncodePictureType</span><span class="sxs-lookup"><span data-stu-id="318e5-291">MFSampleExtension_VideoEncodePictureType</span></span>](mfsampleextension-videoencodepicturetype.md)
-   [<span data-ttu-id="318e5-292">MFSampleExtension_VideoEncodeQP</span><span class="sxs-lookup"><span data-stu-id="318e5-292">MFSampleExtension_VideoEncodeQP</span></span>](mfsampleextension-videoencodeqp.md)

> [!Note]  
> <span data-ttu-id="318e5-293">Una versione precedente della documentazione ha erroneamente indicato che il codificatore è supportato in Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="318e5-293">A previous version of the documentation incorrectly stated that the encoder is supported on Windows Server 2008 R2.</span></span>

 

### <a name="multithreading"></a><span data-ttu-id="318e5-294">Multithreading</span><span class="sxs-lookup"><span data-stu-id="318e5-294">Multithreading</span></span>

<span data-ttu-id="318e5-295">In Windows 8 il codificatore supporta due modalità di codifica:</span><span class="sxs-lookup"><span data-stu-id="318e5-295">In Windows 8, the encoder supports two encoding modes:</span></span>

-   <span data-ttu-id="318e5-296">**Codifica Slice.**</span><span class="sxs-lookup"><span data-stu-id="318e5-296">**Slice encoding.**</span></span> <span data-ttu-id="318e5-297">In questa modalità, le sezioni vengono codificate in parallelo.</span><span class="sxs-lookup"><span data-stu-id="318e5-297">In this mode, slices are encoded in parallel.</span></span> <span data-ttu-id="318e5-298">Ogni sezione è codificata in un thread diverso.</span><span class="sxs-lookup"><span data-stu-id="318e5-298">Each slice is encoded on a different thread.</span></span> <span data-ttu-id="318e5-299">Questa modalità presenta una bassa latenza, perché una singola immagine è codificata in parallelo.</span><span class="sxs-lookup"><span data-stu-id="318e5-299">This mode has low latency, because a single picture is encoded in parallel.</span></span> <span data-ttu-id="318e5-300">Questo approccio, tuttavia, non viene ridimensionato con l'aumentare del numero di core, perché il numero di sezioni è limitato dal numero di righe di macroblocco nell'immagine di input.</span><span class="sxs-lookup"><span data-stu-id="318e5-300">However, this approach does not scale as the number of cores increases, because the number of slices is bounded by the number of macroblock rows in the input picture.</span></span>
-   <span data-ttu-id="318e5-301">**Codifica multiframe.**</span><span class="sxs-lookup"><span data-stu-id="318e5-301">**Multi-frame encoding.**</span></span> <span data-ttu-id="318e5-302">In questa modalità, il codificatore accetta più frame di input e li codifica in parallelo.</span><span class="sxs-lookup"><span data-stu-id="318e5-302">In this mode, the encoder accepts multiple frames of input and encodes them in parallel.</span></span> <span data-ttu-id="318e5-303">Questa modalità offre una migliore scalabilità in un ambiente multicore, ma introduce più latenza.</span><span class="sxs-lookup"><span data-stu-id="318e5-303">This mode scales better in a multicore environment, but introduces more latency.</span></span>

<span data-ttu-id="318e5-304">Per ridurre al minimo la latenza, l'impostazione predefinita del codificatore è la codifica Slice.</span><span class="sxs-lookup"><span data-stu-id="318e5-304">The encoder defaults to slice encoding, to minimize latency.</span></span> <span data-ttu-id="318e5-305">Per abilitare la codifica multiframe, impostare la proprietà [CODECAPI_AVLowLatencyMode](codecapi-avlowlatencymode.md) su **VARIANT_FALSE**.</span><span class="sxs-lookup"><span data-stu-id="318e5-305">To enable multi-frame encoding, set the [CODECAPI_AVLowLatencyMode](codecapi-avlowlatencymode.md) property to **VARIANT_FALSE**.</span></span>

<span data-ttu-id="318e5-306">Per impostare il numero di thread di lavoro utilizzati dal codificatore, impostare la proprietà [CODECAPI_AVEncNumWorkerThreads](codecapi-avencnumworkerthreads.md) .</span><span class="sxs-lookup"><span data-stu-id="318e5-306">To set the number of worker threads used by the encoder, set the [CODECAPI_AVEncNumWorkerThreads](codecapi-avencnumworkerthreads.md) property.</span></span>

<span data-ttu-id="318e5-307">In Windows 7, il codificatore usa sempre la codifica Slice.</span><span class="sxs-lookup"><span data-stu-id="318e5-307">In Windows 7, the encoder always uses slice encoding.</span></span>

### <a name="certified-hardware-encoder"></a><span data-ttu-id="318e5-308">Codificatore hardware certificato</span><span class="sxs-lookup"><span data-stu-id="318e5-308">Certified Hardware Encoder</span></span>

<span data-ttu-id="318e5-309">Se è presente un codificatore hardware certificato, in genere verrà usato al posto del codificatore di sistema della posta in arrivo per Media Foundation scenari correlati.</span><span class="sxs-lookup"><span data-stu-id="318e5-309">If a certified hardware encoder is present, it will generally be used instead of the inbox system encoder for Media Foundation related scenarios.</span></span> <span data-ttu-id="318e5-310">I codificatori certificati sono necessari per supportare un determinato set di proprietà **ICodecAPI** e possono facoltativamente supportare un altro set di proprietà.</span><span class="sxs-lookup"><span data-stu-id="318e5-310">Certified encoders are required to support a certain set of **ICodecAPI** properties and can optionally support another set of properties.</span></span> <span data-ttu-id="318e5-311">Il processo di certificazione deve garantire che le proprietà obbligatorie siano supportate correttamente e, se è supportata una proprietà facoltativa, anche se è supportata correttamente.</span><span class="sxs-lookup"><span data-stu-id="318e5-311">The certification process should guarantee that the required properties are properly supported and, if an optional property is supported, that it is also properly supported.</span></span>

<span data-ttu-id="318e5-312">Di seguito è riportato il set di proprietà **ICodecAPI** obbligatorie e facoltative per i codificatori per passare la certificazione del codificatore HCK.</span><span class="sxs-lookup"><span data-stu-id="318e5-312">The following is the set of required and optional **ICodecAPI** properties for encoders to pass the HCK encoder certification.</span></span>

<span data-ttu-id="318e5-313">Sono necessarie le seguenti proprietà di Windows 8 e Windows 8.1 **ICodecAPI** :</span><span class="sxs-lookup"><span data-stu-id="318e5-313">The following Windows 8 and Windows 8.1 **ICodecAPI** properties are required:</span></span>

-   [<span data-ttu-id="318e5-314">CODECAPI_AVEncCommonRateControlMode</span><span class="sxs-lookup"><span data-stu-id="318e5-314">CODECAPI_AVEncCommonRateControlMode</span></span>](../directshow/avenccommonratecontrolmode-property.md)
-   [<span data-ttu-id="318e5-315">CODECAPI_AVEncCommonQuality</span><span class="sxs-lookup"><span data-stu-id="318e5-315">CODECAPI_AVEncCommonQuality</span></span>](../directshow/avenccommonquality-property.md)
-   [<span data-ttu-id="318e5-316">CODECAPI_AVEncCommonQualityVsSpeed</span><span class="sxs-lookup"><span data-stu-id="318e5-316">CODECAPI_AVEncCommonQualityVsSpeed</span></span>](../directshow/avenccommonqualityvsspeed-property.md)
-   [<span data-ttu-id="318e5-317">CODECAPI_AVEncCommonMeanBitRate</span><span class="sxs-lookup"><span data-stu-id="318e5-317">CODECAPI_AVEncCommonMeanBitRate</span></span>](../directshow/avenccommonmeanbitrate-property.md)
-   [<span data-ttu-id="318e5-318">CODECAPI_AVEncCommonMaxBitRate</span><span class="sxs-lookup"><span data-stu-id="318e5-318">CODECAPI_AVEncCommonMaxBitRate</span></span>](../directshow/avenccommonmaxbitrate-property.md)
-   [<span data-ttu-id="318e5-319">CODECAPI_AVEncCommonBufferSize</span><span class="sxs-lookup"><span data-stu-id="318e5-319">CODECAPI_AVEncCommonBufferSize</span></span>](../directshow/avenccommonbuffersize-property.md)
-   [<span data-ttu-id="318e5-320">CODECAPI_AVEncMPVGOPSize</span><span class="sxs-lookup"><span data-stu-id="318e5-320">CODECAPI_AVEncMPVGOPSize</span></span>](../directshow/avencmpvgopsize-property.md)
-   [<span data-ttu-id="318e5-321">CODECAPI_AVEncVideoEncodeQP</span><span class="sxs-lookup"><span data-stu-id="318e5-321">CODECAPI_AVEncVideoEncodeQP</span></span>](codecapi-avencvideoencodeqp.md)
-   [<span data-ttu-id="318e5-322">CODECAPI_AVEncVideoForceKeyFrame</span><span class="sxs-lookup"><span data-stu-id="318e5-322">CODECAPI_AVEncVideoForceKeyFrame</span></span>](codecapi-avencvideoforcekeyframe.md)

<span data-ttu-id="318e5-323">Le seguenti Windows 8.1 proprietà **ICodecAPI** sono facoltative, ma sono testate in HCK se supportate.</span><span class="sxs-lookup"><span data-stu-id="318e5-323">The following Windows 8.1 **ICodecAPI** properties are optional, but are tested in HCK if supported.</span></span>

-   [<span data-ttu-id="318e5-324">CODECAPI_AVEncVideoMinQP</span><span class="sxs-lookup"><span data-stu-id="318e5-324">CODECAPI_AVEncVideoMinQP</span></span>](codecapi-avencvideominqp.md)
-   [<span data-ttu-id="318e5-325">CODECAPI_AVEncVideoLTRBufferControl</span><span class="sxs-lookup"><span data-stu-id="318e5-325">CODECAPI_AVEncVideoLTRBufferControl</span></span>](codecapi-avencvideoltrbuffercontrol.md)
-   [<span data-ttu-id="318e5-326">CODECAPI_AVEncVideoMarkLTRFrame</span><span class="sxs-lookup"><span data-stu-id="318e5-326">CODECAPI_AVEncVideoMarkLTRFrame</span></span>](codecapi-avencvideomarkltrframe.md)
-   [<span data-ttu-id="318e5-327">CODECAPI_AVEncVideoUseLTRFrame</span><span class="sxs-lookup"><span data-stu-id="318e5-327">CODECAPI_AVEncVideoUseLTRFrame</span></span>](codecapi-avencvideouseltrframe.md)
-   [<span data-ttu-id="318e5-328">CODECAPI_AVEncVideoEncodeFrameTypeQP</span><span class="sxs-lookup"><span data-stu-id="318e5-328">CODECAPI_AVEncVideoEncodeFrameTypeQP</span></span>](codecapi-avencvideoencodeframetypeqp.md)
-   [<span data-ttu-id="318e5-329">CODECAPI_AVEncSliceControlMode</span><span class="sxs-lookup"><span data-stu-id="318e5-329">CODECAPI_AVEncSliceControlMode</span></span>](codecapi-avencslicecontrolmode.md)
-   [<span data-ttu-id="318e5-330">CODECAPI_AVEncSliceControlSize</span><span class="sxs-lookup"><span data-stu-id="318e5-330">CODECAPI_AVEncSliceControlSize</span></span>](codecapi-avencslicecontrolsize.md)
-   [<span data-ttu-id="318e5-331">CODECAPI_AVEncVideoMaxNumRefFrame</span><span class="sxs-lookup"><span data-stu-id="318e5-331">CODECAPI_AVEncVideoMaxNumRefFrame</span></span>](codecapi-avencvideomaxnumrefframe.md)
-   [<span data-ttu-id="318e5-332">CODECAPI_AVEncVideoMeanAbsoluteDifference</span><span class="sxs-lookup"><span data-stu-id="318e5-332">CODECAPI_AVEncVideoMeanAbsoluteDifference</span></span>](codecapi-avencvideomeanabsolutedifference.md)
-   [<span data-ttu-id="318e5-333">CODECAPI_AVEncVideoMaxQP</span><span class="sxs-lookup"><span data-stu-id="318e5-333">CODECAPI_AVEncVideoMaxQP</span></span>](codecapi-avencvideomaxqp.md)
-   [<span data-ttu-id="318e5-334">CODECAPI_AVEncVideoROIEnabled</span><span class="sxs-lookup"><span data-stu-id="318e5-334">CODECAPI_AVEncVideoROIEnabled</span></span>](codecapi-avencvideoroienabled.md)
-   <span data-ttu-id="318e5-335">[CODECAPI_AVEncVideoTemporalLayerCount](codecapi-avencvideotemporallayercount.md) (dinamico)</span><span class="sxs-lookup"><span data-stu-id="318e5-335">[CODECAPI_AVEncVideoTemporalLayerCount](codecapi-avencvideotemporallayercount.md) (Dynamic)</span></span>
-   [<span data-ttu-id="318e5-336">CODECAPI_AVEncH264CABACEnable</span><span class="sxs-lookup"><span data-stu-id="318e5-336">CODECAPI_AVEncH264CABACEnable</span></span>](codecapi-avench264cabacenable.md)

<span data-ttu-id="318e5-337">Le seguenti proprietà di Windows 8 e Windows 8.1 **ICodecAPI** sono facoltative, ma sono testate in HCK se supportate.</span><span class="sxs-lookup"><span data-stu-id="318e5-337">The following Windows 8 and Windows 8.1 **ICodecAPI** properties are optional, but are tested in HCK if supported.</span></span>

-   <span data-ttu-id="318e5-338">[CODECAPI_AVEncVideoTemporalLayerCount](codecapi-avencvideotemporallayercount.md) (statico)</span><span class="sxs-lookup"><span data-stu-id="318e5-338">[CODECAPI_AVEncVideoTemporalLayerCount](codecapi-avencvideotemporallayercount.md) (Static)</span></span>
-   [<span data-ttu-id="318e5-339">CODECAPI_AVLowLatencyMode</span><span class="sxs-lookup"><span data-stu-id="318e5-339">CODECAPI_AVLowLatencyMode</span></span>](codecapi-avlowlatencymode.md)

<span data-ttu-id="318e5-340">Le proprietà **ICodecAPI** seguenti sono facoltative.</span><span class="sxs-lookup"><span data-stu-id="318e5-340">The following **ICodecAPI** properties are optional.</span></span> <span data-ttu-id="318e5-341">Non vengono testati in HCK.</span><span class="sxs-lookup"><span data-stu-id="318e5-341">They are not tested in HCK.</span></span>

-   [<span data-ttu-id="318e5-342">CODECAPI_AVEncMPVDefaultBPictureCount</span><span class="sxs-lookup"><span data-stu-id="318e5-342">CODECAPI_AVEncMPVDefaultBPictureCount</span></span>](../directshow/avencmpvdefaultbpicturecount-property.md)

## <a name="requirements"></a><span data-ttu-id="318e5-343">Requisiti</span><span class="sxs-lookup"><span data-stu-id="318e5-343">Requirements</span></span>



| <span data-ttu-id="318e5-344">Requisito</span><span class="sxs-lookup"><span data-stu-id="318e5-344">Requirement</span></span> | <span data-ttu-id="318e5-345">Valore</span><span class="sxs-lookup"><span data-stu-id="318e5-345">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="318e5-346">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="318e5-346">Minimum supported client</span></span><br/> | <span data-ttu-id="318e5-347">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="318e5-347">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="318e5-348">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="318e5-348">Minimum supported server</span></span><br/> | <span data-ttu-id="318e5-349">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="318e5-349">None supported</span></span><br/>                                                                |
| <span data-ttu-id="318e5-350">DLL</span><span class="sxs-lookup"><span data-stu-id="318e5-350">DLL</span></span><br/>                      | <dl> <span data-ttu-id="318e5-351"><dt>Mfh264enc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="318e5-351"><dt>Mfh264enc.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="318e5-352">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="318e5-352">See also</span></span>

<dl> <dt>

[<span data-ttu-id="318e5-353">Oggetti codec</span><span class="sxs-lookup"><span data-stu-id="318e5-353">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="318e5-354">Supporto MPEG-4 in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="318e5-354">MPEG-4 Support in Media Foundation</span></span>](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="318e5-355">Formati multimediali supportati in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="318e5-355">Supported Media Formats in Media Foundation</span></span>](supported-media-formats-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="318e5-356">Tipi di supporti video</span><span class="sxs-lookup"><span data-stu-id="318e5-356">Video Media Types</span></span>](video-media-types.md)
</dt> </dl>

 

 
