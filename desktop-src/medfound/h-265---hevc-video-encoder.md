---
description: Il codificatore Media Foundation H. 265 video è una trasformazione Media Foundation che supporta la codifica del contenuto nel formato H. 265/HEVC.
ms.assetid: 790CFB39-6FC0-432D-A434-5262C30EABF4
title: Codificatore video H. 265/HEVC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 015295792a72f3250c47389192586dbc00566858
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966945"
---
# <a name="h265--hevc-video-encoder"></a><span data-ttu-id="77d82-103">Codificatore video H. 265/HEVC</span><span class="sxs-lookup"><span data-stu-id="77d82-103">H.265 / HEVC Video Encoder</span></span>

<span data-ttu-id="77d82-104">Il codificatore Media Foundation H. 265 video è una [trasformazione Media Foundation](media-foundation-transforms.md) che supporta la codifica del contenuto nel formato H. 265/HEVC.</span><span class="sxs-lookup"><span data-stu-id="77d82-104">The Media Foundation H.265 video encoder is a [Media Foundation Transform](media-foundation-transforms.md) that supports encoding content into the H.265/HEVC format.</span></span> <span data-ttu-id="77d82-105">Il codificatore supporta i profili seguenti:</span><span class="sxs-lookup"><span data-stu-id="77d82-105">The encoder supports the following profiles:</span></span>

-   <span data-ttu-id="77d82-106">Main Profile</span><span class="sxs-lookup"><span data-stu-id="77d82-106">Main Profile</span></span>

<span data-ttu-id="77d82-107">Il codificatore video H. 265 espone le interfacce seguenti:</span><span class="sxs-lookup"><span data-stu-id="77d82-107">The H.265 video encoder exposes the following interfaces:</span></span>

-   [<span data-ttu-id="77d82-108">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="77d82-108">**ICodecAPI**</span></span>](/windows/win32/api/strmif/nn-strmif-icodecapi)
-   [<span data-ttu-id="77d82-109">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="77d82-109">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="input-types"></a><span data-ttu-id="77d82-110">Tipi di input</span><span class="sxs-lookup"><span data-stu-id="77d82-110">Input Types</span></span>

<span data-ttu-id="77d82-111">Il tipo di supporto di input deve avere uno dei seguenti sottotipi:</span><span class="sxs-lookup"><span data-stu-id="77d82-111">The input media type must have one of the following subtypes:</span></span>

-   <span data-ttu-id="77d82-112">**\_IYUV MFVideoFormat**</span><span class="sxs-lookup"><span data-stu-id="77d82-112">**MFVideoFormat\_IYUV**</span></span>
-   <span data-ttu-id="77d82-113">**\_NV12 MFVideoFormat**</span><span class="sxs-lookup"><span data-stu-id="77d82-113">**MFVideoFormat\_NV12**</span></span>
-   <span data-ttu-id="77d82-114">**\_YUY2 MFVideoFormat**</span><span class="sxs-lookup"><span data-stu-id="77d82-114">**MFVideoFormat\_YUY2**</span></span>
-   <span data-ttu-id="77d82-115">**\_YV12 MFVideoFormat**</span><span class="sxs-lookup"><span data-stu-id="77d82-115">**MFVideoFormat\_YV12**</span></span>

<span data-ttu-id="77d82-116">Per altre informazioni su questi sottotipi, vedere [GUID del sottotipo video](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="77d82-116">For more information about these subtypes, see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>

<span data-ttu-id="77d82-117">Il tipo di output deve essere impostato prima del tipo di input.</span><span class="sxs-lookup"><span data-stu-id="77d82-117">The output type must be set before the input type.</span></span> <span data-ttu-id="77d82-118">Fino a quando non viene impostato il tipo di output, il metodo [**IMFTransform:: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) del codificatore restituisce il **tipo di \_ trasformazione MF E \_ \_ \_ non \_ impostato**.</span><span class="sxs-lookup"><span data-stu-id="77d82-118">Until the output type is set, the encoder's [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) method returns **MF\_E\_TRANSFORM\_TYPE\_NOT\_SET**.</span></span>

## <a name="output-types"></a><span data-ttu-id="77d82-119">Tipi di output</span><span class="sxs-lookup"><span data-stu-id="77d82-119">Output Types</span></span>

<span data-ttu-id="77d82-120">Il codificatore supporta un solo sottotipo di output:</span><span class="sxs-lookup"><span data-stu-id="77d82-120">The encoder supports a single output subtype:</span></span>

-   <span data-ttu-id="77d82-121">**\_H265 MFVideoFormat**</span><span class="sxs-lookup"><span data-stu-id="77d82-121">**MFVideoFormat\_H265**</span></span>

<span data-ttu-id="77d82-122">Impostare gli attributi seguenti sul tipo di supporto di output.</span><span class="sxs-lookup"><span data-stu-id="77d82-122">Set the following attributes on the output media type.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="77d82-123">Attributo</span><span class="sxs-lookup"><span data-stu-id="77d82-123">Attribute</span></span></th>
<th><span data-ttu-id="77d82-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="77d82-124">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="77d82-125"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="77d82-125"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span></span></td>
<td><span data-ttu-id="77d82-126">Tipo principale.</span><span class="sxs-lookup"><span data-stu-id="77d82-126">Major type.</span></span> <span data-ttu-id="77d82-127">Deve essere <strong>MFMediaType_Video</strong>.</span><span class="sxs-lookup"><span data-stu-id="77d82-127">Must be <strong>MFMediaType_Video</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="77d82-128"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="77d82-128"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span></span></td>
<td><span data-ttu-id="77d82-129">Sottotipo video.</span><span class="sxs-lookup"><span data-stu-id="77d82-129">Video subtype.</span></span> <span data-ttu-id="77d82-130">Deve essere <strong>MFVideoFormat_HEVC</strong>.</span><span class="sxs-lookup"><span data-stu-id="77d82-130">Must be <strong>MFVideoFormat_HEVC</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="77d82-131"><a href="mf-mt-avg-bitrate-attribute.md"><strong>MF_MT_AVG_BITRATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="77d82-131"><a href="mf-mt-avg-bitrate-attribute.md"><strong>MF_MT_AVG_BITRATE</strong></a></span></span></td>
<td><span data-ttu-id="77d82-132">Velocità in bit codificata media, in bit al secondo.</span><span class="sxs-lookup"><span data-stu-id="77d82-132">Average encoded bit rate, in bits per second.</span></span> <span data-ttu-id="77d82-133">Deve essere maggiore di zero.</span><span class="sxs-lookup"><span data-stu-id="77d82-133">Must be greater than zero.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="77d82-134"><a href="mf-mt-frame-rate-attribute.md"><strong>MF_MT_FRAME_RATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="77d82-134"><a href="mf-mt-frame-rate-attribute.md"><strong>MF_MT_FRAME_RATE</strong></a></span></span></td>
<td><span data-ttu-id="77d82-135">Frequenza di fotogrammi.</span><span class="sxs-lookup"><span data-stu-id="77d82-135">Frame rate.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="77d82-136"><a href="mf-mt-frame-size-attribute.md"><strong>MF_MT_FRAME_SIZE</strong></a></span><span class="sxs-lookup"><span data-stu-id="77d82-136"><a href="mf-mt-frame-size-attribute.md"><strong>MF_MT_FRAME_SIZE</strong></a></span></span></td>
<td><span data-ttu-id="77d82-137">Dimensioni del frame.</span><span class="sxs-lookup"><span data-stu-id="77d82-137">Frame size.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="77d82-138"><a href="mf-mt-interlace-mode-attribute.md"><strong>MF_MT_INTERLACE_MODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="77d82-138"><a href="mf-mt-interlace-mode-attribute.md"><strong>MF_MT_INTERLACE_MODE</strong></a></span></span></td>
<td><span data-ttu-id="77d82-139">Modalità interlacciamento.</span><span class="sxs-lookup"><span data-stu-id="77d82-139">Interlace mode.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="77d82-140"><a href="mf-mt-video-profile.md">MF_MT_VIDEO_PROFILE</a></span><span class="sxs-lookup"><span data-stu-id="77d82-140"><a href="mf-mt-video-profile.md">MF_MT_VIDEO_PROFILE</a></span></span></td>
<td><span data-ttu-id="77d82-141">Profilo di codifica H. 265.</span><span class="sxs-lookup"><span data-stu-id="77d82-141">H.265 encoding profile.</span></span><br/> <span data-ttu-id="77d82-142">I valori supportati sono:</span><span class="sxs-lookup"><span data-stu-id="77d82-142">The supported values are:</span></span> <br/>
<ul>
<li><span data-ttu-id="77d82-143"><strong>eAVEncH265VProfile_Main_420_8</strong></span><span class="sxs-lookup"><span data-stu-id="77d82-143"><strong>eAVEncH265VProfile_Main_420_8</strong></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="77d82-144"><a href="mf-mt-mpeg2-level-attribute.md"><strong>MF_MT_MPEG2_LEVEL</strong></a></span><span class="sxs-lookup"><span data-stu-id="77d82-144"><a href="mf-mt-mpeg2-level-attribute.md"><strong>MF_MT_MPEG2_LEVEL</strong></a></span></span></td>
<td><span data-ttu-id="77d82-145">Specifica il livello del video codificato.</span><span class="sxs-lookup"><span data-stu-id="77d82-145">Specifies the level of the coded video.</span></span> <span data-ttu-id="77d82-146">Per ulteriori informazioni sui vincoli di profilo e di livello, vedere l'allegato A di ITU-T H. 265.</span><span class="sxs-lookup"><span data-stu-id="77d82-146">For more information about profile and level constraints, refer to Annex A of ITU-T H.265.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="77d82-147"><a href="mf-mt-pixel-aspect-ratio-attribute.md"><strong>MF_MT_PIXEL_ASPECT_RATIO</strong></a></span><span class="sxs-lookup"><span data-stu-id="77d82-147"><a href="mf-mt-pixel-aspect-ratio-attribute.md"><strong>MF_MT_PIXEL_ASPECT_RATIO</strong></a></span></span></td>
<td><span data-ttu-id="77d82-148">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="77d82-148">Optional.</span></span> <span data-ttu-id="77d82-149">Specifica le proporzioni in pixel.</span><span class="sxs-lookup"><span data-stu-id="77d82-149">Specifies the pixel aspect ratio.</span></span> <span data-ttu-id="77d82-150">Il valore predefinito è 1:1.</span><span class="sxs-lookup"><span data-stu-id="77d82-150">The default value is 1:1.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="77d82-151">Dopo aver impostato il tipo di output, il codificatore video aggiorna il tipo aggiungendo l'attributo dell' [**\_ \_ \_ \_ intestazione della sequenza MPEG di MF mt**](mf-mt-mpeg-sequence-header-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="77d82-151">After the output type is set, the video encoder updates the type by adding the [**MF\_MT\_MPEG\_SEQUENCE\_HEADER**](mf-mt-mpeg-sequence-header-attribute.md) attribute.</span></span> <span data-ttu-id="77d82-152">Questo attributo contiene l'intestazione della sequenza.</span><span class="sxs-lookup"><span data-stu-id="77d82-152">This attribute contains the sequence header.</span></span>

## <a name="supported-imftransform-methods"></a><span data-ttu-id="77d82-153">Metodi IMFTransform supportati</span><span class="sxs-lookup"><span data-stu-id="77d82-153">Supported IMFTransform methods</span></span>

<span data-ttu-id="77d82-154">Per il codificatore H. 265/HEVC sono supportati i seguenti metodi dell'interfaccia [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) :</span><span class="sxs-lookup"><span data-stu-id="77d82-154">The following methods of the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface are supported for the H.265/HEVC encoder:</span></span>

-   [<span data-ttu-id="77d82-155">**GetAttributes**</span><span class="sxs-lookup"><span data-stu-id="77d82-155">**GetAttributes**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes)
-   [<span data-ttu-id="77d82-156">**GetInputAvailableType**</span><span class="sxs-lookup"><span data-stu-id="77d82-156">**GetInputAvailableType**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype)
-   [<span data-ttu-id="77d82-157">**GetInputCurrentType**</span><span class="sxs-lookup"><span data-stu-id="77d82-157">**GetInputCurrentType**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputcurrenttype)
-   [<span data-ttu-id="77d82-158">**GetInputStatus**</span><span class="sxs-lookup"><span data-stu-id="77d82-158">**GetInputStatus**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstatus)
-   [<span data-ttu-id="77d82-159">**GetInputStreamInfo**</span><span class="sxs-lookup"><span data-stu-id="77d82-159">**GetInputStreamInfo**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreaminfo)
-   [<span data-ttu-id="77d82-160">**GetOutputAvailableType**</span><span class="sxs-lookup"><span data-stu-id="77d82-160">**GetOutputAvailableType**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype)
-   [<span data-ttu-id="77d82-161">**GetOutputCurrentType**</span><span class="sxs-lookup"><span data-stu-id="77d82-161">**GetOutputCurrentType**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputcurrenttype)
-   [<span data-ttu-id="77d82-162">**GetOutputStatus**</span><span class="sxs-lookup"><span data-stu-id="77d82-162">**GetOutputStatus**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstatus)
-   [<span data-ttu-id="77d82-163">**GetOutputStreamInfo**</span><span class="sxs-lookup"><span data-stu-id="77d82-163">**GetOutputStreamInfo**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo)
-   [<span data-ttu-id="77d82-164">**GetStreamCount**</span><span class="sxs-lookup"><span data-stu-id="77d82-164">**GetStreamCount**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamcount)
-   [<span data-ttu-id="77d82-165">**GetStreamLimits**</span><span class="sxs-lookup"><span data-stu-id="77d82-165">**GetStreamLimits**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamlimits)
-   [<span data-ttu-id="77d82-166">**ProcessEvent**</span><span class="sxs-lookup"><span data-stu-id="77d82-166">**ProcessEvent**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent)
-   [<span data-ttu-id="77d82-167">**ProcessMessage**</span><span class="sxs-lookup"><span data-stu-id="77d82-167">**ProcessMessage**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage)
-   [<span data-ttu-id="77d82-168">**ProcessInput**</span><span class="sxs-lookup"><span data-stu-id="77d82-168">**ProcessInput**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput)
-   [<span data-ttu-id="77d82-169">**ProcessOutput**</span><span class="sxs-lookup"><span data-stu-id="77d82-169">**ProcessOutput**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)
-   [<span data-ttu-id="77d82-170">**SetInputType**</span><span class="sxs-lookup"><span data-stu-id="77d82-170">**SetInputType**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype)
-   [<span data-ttu-id="77d82-171">**SetOutputType**</span><span class="sxs-lookup"><span data-stu-id="77d82-171">**SetOutputType**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype)
-   [<span data-ttu-id="77d82-172">**SetOutputBounds**</span><span class="sxs-lookup"><span data-stu-id="77d82-172">**SetOutputBounds**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputbounds)

<span data-ttu-id="77d82-173">Tutti gli altri metodi di [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) restituiranno l'errore E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="77d82-173">All other [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) methods will return the error E\_NOTIMPL.</span></span>

## <a name="supported-icodecapi-methods"></a><span data-ttu-id="77d82-174">Metodi ICodecAPI supportati</span><span class="sxs-lookup"><span data-stu-id="77d82-174">Supported ICodecAPI methods</span></span>

<span data-ttu-id="77d82-175">Per il codificatore H. 265/HEVC sono supportati i seguenti metodi dell'interfaccia [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) :</span><span class="sxs-lookup"><span data-stu-id="77d82-175">The following methods of the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface are supported for the H.265/HEVC encoder:</span></span>

-   [<span data-ttu-id="77d82-176">**IsSupported**</span><span class="sxs-lookup"><span data-stu-id="77d82-176">**IsSupported**</span></span>](/windows/win32/api/strmif/nf-strmif-icodecapi-issupported)
-   [<span data-ttu-id="77d82-177">**SetValue**</span><span class="sxs-lookup"><span data-stu-id="77d82-177">**SetValue**</span></span>](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue)
-   [<span data-ttu-id="77d82-178">**GetValue**</span><span class="sxs-lookup"><span data-stu-id="77d82-178">**GetValue**</span></span>](/windows/win32/api/strmif/nf-strmif-icodecapi-getvalue)
-   [<span data-ttu-id="77d82-179">**GetParameterRange**</span><span class="sxs-lookup"><span data-stu-id="77d82-179">**GetParameterRange**</span></span>](/windows/win32/api/strmif/nf-strmif-icodecapi-getparameterrange)
-   [<span data-ttu-id="77d82-180">**GetParameterValues**</span><span class="sxs-lookup"><span data-stu-id="77d82-180">**GetParameterValues**</span></span>](/windows/win32/api/strmif/nf-strmif-icodecapi-getparametervalues)

<span data-ttu-id="77d82-181">Tutti gli altri metodi di [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) restituiranno l'errore E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="77d82-181">All other [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) methods will return the error E\_NOTIMPL.</span></span>

## <a name="codec-properties"></a><span data-ttu-id="77d82-182">Proprietà codec</span><span class="sxs-lookup"><span data-stu-id="77d82-182">Codec Properties</span></span>

<span data-ttu-id="77d82-183">Il codificatore H. 265 implementa l'interfaccia [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) per l'impostazione dei parametri di codifica.</span><span class="sxs-lookup"><span data-stu-id="77d82-183">The H.265 encoder implements the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface for setting encoding parameters.</span></span> <span data-ttu-id="77d82-184">Supporta le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="77d82-184">It supports the following properties.</span></span>

<span data-ttu-id="77d82-185">Per i requisiti di codec per la certificazione del codificatore HCK, vedere la sezione relativa al **codificatore hardware certificato** di seguito.</span><span class="sxs-lookup"><span data-stu-id="77d82-185">For the codec requirements for HCK encoder certification, see the **Certified Hardware Encoder** section below.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="77d82-186">Proprietà</span><span class="sxs-lookup"><span data-stu-id="77d82-186">Property</span></span></th>
<th><span data-ttu-id="77d82-187">Descrizione</span><span class="sxs-lookup"><span data-stu-id="77d82-187">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="77d82-188"><a href="/windows/desktop/DirectShow/avenccommonratecontrolmode-property"><strong>CODECAPI_AVEncCommonRateControlMode</strong></a></span><span class="sxs-lookup"><span data-stu-id="77d82-188"><a href="/windows/desktop/DirectShow/avenccommonratecontrolmode-property"><strong>CODECAPI_AVEncCommonRateControlMode</strong></a></span></span></td>
<td><span data-ttu-id="77d82-189">Imposta la modalità di controllo della frequenza.</span><span class="sxs-lookup"><span data-stu-id="77d82-189">Sets the rate control mode.</span></span> <span data-ttu-id="77d82-190">Le modalità supportate sono:</span><span class="sxs-lookup"><span data-stu-id="77d82-190">The supported modes are:</span></span><br/>
<ul>
<li><span data-ttu-id="77d82-191"><strong>eAVEncCommonRateControlMode_CBR</strong></span><span class="sxs-lookup"><span data-stu-id="77d82-191"><strong>eAVEncCommonRateControlMode_CBR</strong></span></span></li>
<li><span data-ttu-id="77d82-192"><strong>eAVEncCommonRateControlMode_Quality</strong></span><span class="sxs-lookup"><span data-stu-id="77d82-192"><strong>eAVEncCommonRateControlMode_Quality</strong></span></span></li>
</ul>
<span data-ttu-id="77d82-193">Se vengono specificate altre modalità, verrà usato il controllo della velocità <strong>eAVEncCommonRateControlMode_CBR</strong> .</span><span class="sxs-lookup"><span data-stu-id="77d82-193">If other modes are specified, the <strong>eAVEncCommonRateControlMode_CBR</strong> rate control will be used.</span></span><br/> <span data-ttu-id="77d82-194">Si tratta di un valore VT_UI4.</span><span class="sxs-lookup"><span data-stu-id="77d82-194">This is a VT_UI4 value.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="77d82-195"><a href="/windows/desktop/DirectShow/avenccommonmeanbitrate-property">CODECAPI_AVEncCommonMeanBitRate</a></span><span class="sxs-lookup"><span data-stu-id="77d82-195"><a href="/windows/desktop/DirectShow/avenccommonmeanbitrate-property">CODECAPI_AVEncCommonMeanBitRate</a></span></span></td>
<td><span data-ttu-id="77d82-196">Imposta la velocità in bit media per il flusso di bit codificato, in bit al secondo.</span><span class="sxs-lookup"><span data-stu-id="77d82-196">Sets the average bit rate for the encoded bit stream, in bits per second.</span></span> <br/> <span data-ttu-id="77d82-197">L'intervallo valido è [1... 2 ³ ² – 1].</span><span class="sxs-lookup"><span data-stu-id="77d82-197">The valid range is [1 ... 2³²–1].</span></span> <br/> <span data-ttu-id="77d82-198">Si tratta di un valore VT_UI4.</span><span class="sxs-lookup"><span data-stu-id="77d82-198">This is a VT_UI4 value.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="77d82-199"><a href="/windows/desktop/DirectShow/avenccommonbuffersize-property">CODECAPI_AVEncCommonBufferSize</a></span><span class="sxs-lookup"><span data-stu-id="77d82-199"><a href="/windows/desktop/DirectShow/avenccommonbuffersize-property">CODECAPI_AVEncCommonBufferSize</a></span></span></td>
<td><span data-ttu-id="77d82-200">Imposta la dimensione del buffer, in byte, per la codifica di velocità in bit costante (CBR).</span><span class="sxs-lookup"><span data-stu-id="77d82-200">Sets the buffer size, in bytes, for constant bit rate (CBR) encoding.</span></span><br/> <span data-ttu-id="77d82-201">L'intervallo valido è [1... 2 ³ ² – 1].</span><span class="sxs-lookup"><span data-stu-id="77d82-201">The valid range is [1 ... 2³²–1].</span></span> <br/> <span data-ttu-id="77d82-202">Si tratta di un valore VT_UI4.</span><span class="sxs-lookup"><span data-stu-id="77d82-202">This is a VT_UI4 value.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="77d82-203"><a href="/windows/desktop/DirectShow/avenccommonmaxbitrate-property">CODECAPI_AVEncCommonMaxBitRate</a></span><span class="sxs-lookup"><span data-stu-id="77d82-203"><a href="/windows/desktop/DirectShow/avenccommonmaxbitrate-property">CODECAPI_AVEncCommonMaxBitRate</a></span></span></td>
<td><span data-ttu-id="77d82-204">Imposta la velocità in bit massima per le modalità di controllo della frequenza che consentono una velocità in bit di picco.</span><span class="sxs-lookup"><span data-stu-id="77d82-204">Sets the maximum bitrate for rate control modes that allow a peak bitrate.</span></span> <br/> <span data-ttu-id="77d82-205">L'intervallo valido è [1... 2 ³ ² – 1].</span><span class="sxs-lookup"><span data-stu-id="77d82-205">The valid range is [1 ... 2³²–1].</span></span> <br/> <span data-ttu-id="77d82-206">Si tratta di un valore VT_UI4.</span><span class="sxs-lookup"><span data-stu-id="77d82-206">This is a VT_UI4 value.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="77d82-207"><a href="/windows/desktop/DirectShow/avencmpvgopsize-property">CODECAPI_AVEncMPVGOPSize</a></span><span class="sxs-lookup"><span data-stu-id="77d82-207"><a href="/windows/desktop/DirectShow/avencmpvgopsize-property">CODECAPI_AVEncMPVGOPSize</a></span></span></td>
<td><span data-ttu-id="77d82-208">Imposta il numero di immagini da un'intestazione GOP alla successiva, incluso l'ancoraggio principale ma non quello seguente.</span><span class="sxs-lookup"><span data-stu-id="77d82-208">Sets the number of pictures from one GOP header to the next, including the leading anchor but not the following one.</span></span> <br/> <span data-ttu-id="77d82-209">L'intervallo valido è [0... 2 ³ ² – 1].</span><span class="sxs-lookup"><span data-stu-id="77d82-209">The valid range is [0 ... 2³²–1].</span></span> <span data-ttu-id="77d82-210">Se il valore è zero, il codificatore seleziona la dimensione GOP.</span><span class="sxs-lookup"><span data-stu-id="77d82-210">If zero, the encoder selects the GOP size.</span></span> <span data-ttu-id="77d82-211">Il valore predefinito è zero.</span><span class="sxs-lookup"><span data-stu-id="77d82-211">The default value is zero.</span></span> <br/> <span data-ttu-id="77d82-212">Si tratta di un valore VT_UI4.</span><span class="sxs-lookup"><span data-stu-id="77d82-212">This is a VT_UI4 value.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="77d82-213"><a href="codecapi-avlowlatencymode.md">CODECAPI_AVLowLatencyMode</a></span><span class="sxs-lookup"><span data-stu-id="77d82-213"><a href="codecapi-avlowlatencymode.md">CODECAPI_AVLowLatencyMode</a></span></span></td>
<td><span data-ttu-id="77d82-214">Abilita o Disabilita la modalità a bassa latenza.</span><span class="sxs-lookup"><span data-stu-id="77d82-214">Enables or disables low-latency mode.</span></span> <br/> <span data-ttu-id="77d82-215">Si tratta di un valore VT_BOOL.</span><span class="sxs-lookup"><span data-stu-id="77d82-215">This is a VT_BOOL value.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="77d82-216"><a href="/windows/desktop/DirectShow/avenccommonqualityvsspeed-property">CODECAPI_AVEncCommonQualityVsSpeed</a></span><span class="sxs-lookup"><span data-stu-id="77d82-216"><a href="/windows/desktop/DirectShow/avenccommonqualityvsspeed-property">CODECAPI_AVEncCommonQualityVsSpeed</a></span></span></td>
<td><span data-ttu-id="77d82-217">Imposta il compromesso di qualità/velocità.</span><span class="sxs-lookup"><span data-stu-id="77d82-217">Sets the quality/speed tradeoff.</span></span> <span data-ttu-id="77d82-218">Questo valore influiscono sul modo in cui il codificatore esegue diverse operazioni di codifica, ad esempio la compensazione del movimento.</span><span class="sxs-lookup"><span data-stu-id="77d82-218">This value affects how the encoder performs various encoding operations, such as motion compensation.</span></span> <span data-ttu-id="77d82-219">A livelli di complessità più elevati, il codificatore viene eseguito più lentamente, ma produce una qualità migliore con la stessa velocità in bit.</span><span class="sxs-lookup"><span data-stu-id="77d82-219">At higher complexity levels, the encoder runs more slowly but produces better quality at the same bit rate.</span></span> <br/> <span data-ttu-id="77d82-220">L'intervallo valido è 0 – 100.</span><span class="sxs-lookup"><span data-stu-id="77d82-220">The valid range is 0 – 100.</span></span> <span data-ttu-id="77d82-221">Internamente, questo valore viene mappato a un set più piccolo di livelli di qualità/velocità supportato dal codificatore.</span><span class="sxs-lookup"><span data-stu-id="77d82-221">Internally, this value is mapped to a smaller set of quality/speed levels supported by the encoder.</span></span><br/> <span data-ttu-id="77d82-222">Si tratta di un valore VT_UI4.</span><span class="sxs-lookup"><span data-stu-id="77d82-222">This is a VT_UI4 value.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="77d82-223"><a href="codecapi-avencvideoforcekeyframe.md">CODECAPI_AVEncVideoForceKeyFrame</a></span><span class="sxs-lookup"><span data-stu-id="77d82-223"><a href="codecapi-avencvideoforcekeyframe.md">CODECAPI_AVEncVideoForceKeyFrame</a></span></span></td>
<td><span data-ttu-id="77d82-224">Impone al codificatore di codificare il fotogramma successivo come fotogramma chiave.</span><span class="sxs-lookup"><span data-stu-id="77d82-224">Forces the encoder to code the next frame as a key frame.</span></span><br/> <span data-ttu-id="77d82-225">Si tratta di un valore VT_UI4.</span><span class="sxs-lookup"><span data-stu-id="77d82-225">This is a VT_UI4 value.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="77d82-226"><a href="codecapi-avencvideoencodeqp.md">CODECAPI_AVEncVideoEncodeQP</a></span><span class="sxs-lookup"><span data-stu-id="77d82-226"><a href="codecapi-avencvideoencodeqp.md">CODECAPI_AVEncVideoEncodeQP</a></span></span></td>
<td><span data-ttu-id="77d82-227">Quando questa proprietà è impostata, il codificatore userà il QP specificato per codificare il frame successivo e tutti i frame successivi fino a quando non viene specificato un nuovo QP.</span><span class="sxs-lookup"><span data-stu-id="77d82-227">When this property is set it will cause the encoder to use the specified QP to encode the next frame and all subsequent frames until a new QP is specified.</span></span> <br/> <span data-ttu-id="77d82-228">Intervallo valido: 0-51, inclusivo</span><span class="sxs-lookup"><span data-stu-id="77d82-228">Valid range: 0–51, inclusive</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="77d82-229"><a href="codecapi-avencvideominqp.md">CODECAPI_AVEncVideoMinQP</a></span><span class="sxs-lookup"><span data-stu-id="77d82-229"><a href="codecapi-avencvideominqp.md">CODECAPI_AVEncVideoMinQP</a></span></span></td>
<td><span data-ttu-id="77d82-230">Questa proprietà consente di impostare un limite per il numero minimo di QP che il codificatore può usare durante controllo della frequenza CBR.</span><span class="sxs-lookup"><span data-stu-id="77d82-230">This property will set a limit on the minimum QP that the encoder can use during CBR ratecontrol.</span></span><br/> <span data-ttu-id="77d82-231">Si tratta di un valore VT_UI4.</span><span class="sxs-lookup"><span data-stu-id="77d82-231">This is a VT_UI4 value.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="77d82-232"><a href="codecapi-avencvideomaxqp.md">CODECAPI_AVEncVideoMaxQP</a></span><span class="sxs-lookup"><span data-stu-id="77d82-232"><a href="codecapi-avencvideomaxqp.md">CODECAPI_AVEncVideoMaxQP</a></span></span></td>
<td><span data-ttu-id="77d82-233">Questa proprietà consente di impostare un limite per il numero massimo di QP che il codificatore può usare durante controllo della frequenza CBR.</span><span class="sxs-lookup"><span data-stu-id="77d82-233">This property will set a limit on the maximum QP that the encoder can use during CBR ratecontrol.</span></span><br/> <span data-ttu-id="77d82-234">Si tratta di un valore VT_UI4.</span><span class="sxs-lookup"><span data-stu-id="77d82-234">This is a VT_UI4 value.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="77d82-235"><a href="codecapi-videoencoderdisplaycontenttype.md">CODECAPI_VideoEncoderDisplayContentType</a></span><span class="sxs-lookup"><span data-stu-id="77d82-235"><a href="codecapi-videoencoderdisplaycontenttype.md">CODECAPI_VideoEncoderDisplayContentType</a></span></span></td>
<td><span data-ttu-id="77d82-236">Imposta un valore che indica se il contenuto è video a schermo intero, anziché il contenuto dello schermo che potrebbe contenere una finestra di video più piccola o senza video.</span><span class="sxs-lookup"><span data-stu-id="77d82-236">Sets whether the content is full-screen video, as opposed to screen content that might have a smaller window of video or have no video at all.</span></span><br/> <span data-ttu-id="77d82-237">Si tratta di un valore VT_UI4.</span><span class="sxs-lookup"><span data-stu-id="77d82-237">This is a VT_UI4 value.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="77d82-238"><a href="codecapi-avencnumworkerthreads.md">CODECAPI_AVEncNumWorkerThreads</a></span><span class="sxs-lookup"><span data-stu-id="77d82-238"><a href="codecapi-avencnumworkerthreads.md">CODECAPI_AVEncNumWorkerThreads</a></span></span></td>
<td><span data-ttu-id="77d82-239">Imposta il numero di thread utilizzati per eseguire l'operazione di compressione.</span><span class="sxs-lookup"><span data-stu-id="77d82-239">Sets the number of threads used to perform the compression operation.</span></span> <span data-ttu-id="77d82-240">Il codificatore suddividerà il frame in riquadri in modo che il numero di thread sia uguale al numero di riquadri.</span><span class="sxs-lookup"><span data-stu-id="77d82-240">The encoder will divide the frame into tiles such that the number of threads equals the number of tiles.</span></span><br/>
<ul>
<li><span data-ttu-id="77d82-241">Numero di processori logici.</span><span class="sxs-lookup"><span data-stu-id="77d82-241">The number of logical processors.</span></span> <span data-ttu-id="77d82-242">Il numero di thread deve essere minore o uguale al numero di processori logici.</span><span class="sxs-lookup"><span data-stu-id="77d82-242">The number of threads must be less than or equal to the number of logical processors.</span></span></li>
<li><span data-ttu-id="77d82-243">Dimensioni del frame.</span><span class="sxs-lookup"><span data-stu-id="77d82-243">The size of the frame.</span></span> <span data-ttu-id="77d82-244">Le dimensioni di un riquadro devono essere maggiori o uguali a 265x64 pixel.</span><span class="sxs-lookup"><span data-stu-id="77d82-244">The size of a tile must bigger than or equal to 265x64 pixels.</span></span></li>
<li><span data-ttu-id="77d82-245">Parità.</span><span class="sxs-lookup"><span data-stu-id="77d82-245">Parity.</span></span> <span data-ttu-id="77d82-246">Il numero di thread deve essere un valore pari.</span><span class="sxs-lookup"><span data-stu-id="77d82-246">The number of threads must be an even value.</span></span> <span data-ttu-id="77d82-247">Se il valore specificato è dispari, verrà usato il successivo valore di pari livello inferiore.</span><span class="sxs-lookup"><span data-stu-id="77d82-247">If the specified value is odd then the next lower even value will be used.</span></span></li>
</ul>
<span data-ttu-id="77d82-248">Si tratta di un valore VT_UI4.</span><span class="sxs-lookup"><span data-stu-id="77d82-248">This is a VT_UI4 value.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="certified-hardware-encoder"></a><span data-ttu-id="77d82-249">Codificatore hardware certificato</span><span class="sxs-lookup"><span data-stu-id="77d82-249">Certified Hardware Encoder</span></span>

<span data-ttu-id="77d82-250">Se è presente un codificatore hardware certificato, in genere verrà usato al posto del codificatore di sistema della posta in arrivo per Media Foundation scenari correlati.</span><span class="sxs-lookup"><span data-stu-id="77d82-250">If a certified hardware encoder is present, it will generally be used instead of the inbox system encoder for Media Foundation related scenarios.</span></span> <span data-ttu-id="77d82-251">I codificatori certificati sono necessari per supportare un determinato set di proprietà **ICodecAPI** e possono facoltativamente supportare un altro set di proprietà.</span><span class="sxs-lookup"><span data-stu-id="77d82-251">Certified encoders are required to support a certain set of **ICodecAPI** properties and can optionally support another set of properties.</span></span> <span data-ttu-id="77d82-252">Il processo di certificazione deve garantire che le proprietà obbligatorie siano supportate correttamente e, se è supportata una proprietà facoltativa, anche se è supportata correttamente.</span><span class="sxs-lookup"><span data-stu-id="77d82-252">The certification process should guarantee that the required properties are properly supported and, if an optional property is supported, that it is also properly supported.</span></span>

<span data-ttu-id="77d82-253">Di seguito è riportato il set di proprietà **ICodecAPI** obbligatorie e facoltative per i codificatori per passare la certificazione del codificatore HCK.</span><span class="sxs-lookup"><span data-stu-id="77d82-253">The following is the set of required and optional **ICodecAPI** properties for encoders to pass the HCK encoder certification.</span></span>

-   [<span data-ttu-id="77d82-254">Codecapis \_ AVEncCommonRateControlMode</span><span class="sxs-lookup"><span data-stu-id="77d82-254">CODECAPI\_AVEncCommonRateControlMode</span></span>](../directshow/avenccommonratecontrolmode-property.md)
-   [<span data-ttu-id="77d82-255">Codecapis \_ AVEncCommonQuality</span><span class="sxs-lookup"><span data-stu-id="77d82-255">CODECAPI\_AVEncCommonQuality</span></span>](../directshow/avenccommonquality-property.md)
-   [<span data-ttu-id="77d82-256">Codecapis \_ AVEncCommonMeanBitRate</span><span class="sxs-lookup"><span data-stu-id="77d82-256">CODECAPI\_AVEncCommonMeanBitRate</span></span>](../directshow/avenccommonmeanbitrate-property.md)
-   [<span data-ttu-id="77d82-257">Codecapis \_ AVEncCommonBufferSize</span><span class="sxs-lookup"><span data-stu-id="77d82-257">CODECAPI\_AVEncCommonBufferSize</span></span>](../directshow/avenccommonbuffersize-property.md)
-   [<span data-ttu-id="77d82-258">Codecapis \_ AVEncMPVGOPSize</span><span class="sxs-lookup"><span data-stu-id="77d82-258">CODECAPI\_AVEncMPVGOPSize</span></span>](../directshow/avencmpvgopsize-property.md)
-   [<span data-ttu-id="77d82-259">Codecapis \_ AVEncVideoEncodeQP</span><span class="sxs-lookup"><span data-stu-id="77d82-259">CODECAPI\_AVEncVideoEncodeQP</span></span>](codecapi-avencvideoencodeqp.md)
-   [<span data-ttu-id="77d82-260">Codecapis \_ AVEncVideoForceKeyFrame</span><span class="sxs-lookup"><span data-stu-id="77d82-260">CODECAPI\_AVEncVideoForceKeyFrame</span></span>](codecapi-avencvideoforcekeyframe.md)

## <a name="requirements"></a><span data-ttu-id="77d82-261">Requisiti</span><span class="sxs-lookup"><span data-stu-id="77d82-261">Requirements</span></span>



| <span data-ttu-id="77d82-262">Requisito</span><span class="sxs-lookup"><span data-stu-id="77d82-262">Requirement</span></span> | <span data-ttu-id="77d82-263">Valore</span><span class="sxs-lookup"><span data-stu-id="77d82-263">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="77d82-264">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="77d82-264">Minimum supported client</span></span><br/> | <span data-ttu-id="77d82-265">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="77d82-265">Windows 10 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="77d82-266">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="77d82-266">Minimum supported server</span></span><br/> | <span data-ttu-id="77d82-267">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="77d82-267">None supported</span></span><br/>                                                                |
| <span data-ttu-id="77d82-268">DLL</span><span class="sxs-lookup"><span data-stu-id="77d82-268">DLL</span></span><br/>                      | <dl> <span data-ttu-id="77d82-269"><dt>Mfh265enc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="77d82-269"><dt>Mfh265enc.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77d82-270">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="77d82-270">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77d82-271">Oggetti codec</span><span class="sxs-lookup"><span data-stu-id="77d82-271">Codec Objects</span></span>](codecobjects.md)
</dt> </dl>

 

 
