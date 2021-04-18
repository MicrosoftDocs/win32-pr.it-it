---
description: Specifica la velocità massima di elaborazione macroblocco per un flusso video H. 264.
ms.assetid: 882F54D1-A963-4016-BEC7-F9C1AC5885FD
title: Attributo MF_MT_H264_MAX_MB_PER_SEC (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b53bdbabd9a633464ed388f2309627b69413c27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309541"
---
# <a name="mf_mt_h264_max_mb_per_sec-attribute"></a><span data-ttu-id="c8cf1-103">\_Attributo MF mt \_ H264 \_ Max \_ MB \_ / \_ sec</span><span class="sxs-lookup"><span data-stu-id="c8cf1-103">MF\_MT\_H264\_MAX\_MB\_PER\_SEC attribute</span></span>

<span data-ttu-id="c8cf1-104">Specifica la velocità massima di elaborazione macroblocco per un flusso video H. 264.</span><span class="sxs-lookup"><span data-stu-id="c8cf1-104">Specifies the maximum macroblock processing rate for an H.264 video stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="c8cf1-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="c8cf1-105">Data type</span></span>

<span data-ttu-id="c8cf1-106">**\[ UInt32 \]** Archiviato come **Uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="c8cf1-106">**UINT32\[\]** stored as **UINT8\[\]**</span></span>

## <a name="applies-to"></a><span data-ttu-id="c8cf1-107">Si applica a</span><span class="sxs-lookup"><span data-stu-id="c8cf1-107">Applies to</span></span>

[<span data-ttu-id="c8cf1-108">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="c8cf1-108">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="c8cf1-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="c8cf1-109">Remarks</span></span>

<span data-ttu-id="c8cf1-110">Questo attributo si applica ai tipi di supporto per i flussi H. 264 trasmessi tramite USB.</span><span class="sxs-lookup"><span data-stu-id="c8cf1-110">This attribute applies to media types for H.264 streams transmitted over USB.</span></span> <span data-ttu-id="c8cf1-111">Il valore dell'attributo è una matrice di valori UINT32, che corrispondono ai campi seguenti nel descrittore di formato video UVC 1,5 H. 264.</span><span class="sxs-lookup"><span data-stu-id="c8cf1-111">The value of the attribute is an array of UINT32 values, which correspond to the following fields in the UVC 1.5 H.264 video format descriptor.</span></span>

| <span data-ttu-id="c8cf1-112">Elemento Array</span><span class="sxs-lookup"><span data-stu-id="c8cf1-112">Array Element</span></span> | <span data-ttu-id="c8cf1-113">Campo descrittore</span><span class="sxs-lookup"><span data-stu-id="c8cf1-113">Descriptor Field</span></span>                                           |
|---------------|------------------------------------------------------------|
| <span data-ttu-id="c8cf1-114">0</span><span class="sxs-lookup"><span data-stu-id="c8cf1-114">0</span></span>             | <span data-ttu-id="c8cf1-115">**dwMaxMBperSecOneResolutionNoScalability**</span><span class="sxs-lookup"><span data-stu-id="c8cf1-115">**dwMaxMBperSecOneResolutionNoScalability**</span></span>                |
| <span data-ttu-id="c8cf1-116">1</span><span class="sxs-lookup"><span data-stu-id="c8cf1-116">1</span></span>             | <span data-ttu-id="c8cf1-117">**dwMaxMBperSecTwoResolutionsNoScalability**</span><span class="sxs-lookup"><span data-stu-id="c8cf1-117">**dwMaxMBperSecTwoResolutionsNoScalability**</span></span>               |
| <span data-ttu-id="c8cf1-118">2</span><span class="sxs-lookup"><span data-stu-id="c8cf1-118">2</span></span>             | <span data-ttu-id="c8cf1-119">**dwMaxMBperSecThreeResolutionsNoScalability**</span><span class="sxs-lookup"><span data-stu-id="c8cf1-119">**dwMaxMBperSecThreeResolutionsNoScalability**</span></span>             |
| <span data-ttu-id="c8cf1-120">3</span><span class="sxs-lookup"><span data-stu-id="c8cf1-120">3</span></span>             | <span data-ttu-id="c8cf1-121">**dwMaxMBperSecFourResolutionsNoScalability**</span><span class="sxs-lookup"><span data-stu-id="c8cf1-121">**dwMaxMBperSecFourResolutionsNoScalability**</span></span>              |
| <span data-ttu-id="c8cf1-122">4</span><span class="sxs-lookup"><span data-stu-id="c8cf1-122">4</span></span>             | <span data-ttu-id="c8cf1-123">**dwMaxMBperSecOneResolutionTemporalScalability**</span><span class="sxs-lookup"><span data-stu-id="c8cf1-123">**dwMaxMBperSecOneResolutionTemporalScalability**</span></span>          |
| <span data-ttu-id="c8cf1-124">5</span><span class="sxs-lookup"><span data-stu-id="c8cf1-124">5</span></span>             | <span data-ttu-id="c8cf1-125">**dwMaxMBperSecTwoResolutionsTemporalScalablility**</span><span class="sxs-lookup"><span data-stu-id="c8cf1-125">**dwMaxMBperSecTwoResolutionsTemporalScalablility**</span></span>        |
| <span data-ttu-id="c8cf1-126">6</span><span class="sxs-lookup"><span data-stu-id="c8cf1-126">6</span></span>             | <span data-ttu-id="c8cf1-127">**dwMaxMBperSecThreeResolutionsTemporalScalability**</span><span class="sxs-lookup"><span data-stu-id="c8cf1-127">**dwMaxMBperSecThreeResolutionsTemporalScalability**</span></span>       |
| <span data-ttu-id="c8cf1-128">7</span><span class="sxs-lookup"><span data-stu-id="c8cf1-128">7</span></span>             | <span data-ttu-id="c8cf1-129">**dwMaxMBperSecFourResolutionsTemporalScalability**</span><span class="sxs-lookup"><span data-stu-id="c8cf1-129">**dwMaxMBperSecFourResolutionsTemporalScalability**</span></span>        |
| <span data-ttu-id="c8cf1-130">8</span><span class="sxs-lookup"><span data-stu-id="c8cf1-130">8</span></span>             | <span data-ttu-id="c8cf1-131">**dwMaxMBperSecOneResolutionTemporalQualityScalability**</span><span class="sxs-lookup"><span data-stu-id="c8cf1-131">**dwMaxMBperSecOneResolutionTemporalQualityScalability**</span></span>   |
| <span data-ttu-id="c8cf1-132">9</span><span class="sxs-lookup"><span data-stu-id="c8cf1-132">9</span></span>             | <span data-ttu-id="c8cf1-133">**dwMaxMBperSecTwoResolutionsTemporalQualityScalability**</span><span class="sxs-lookup"><span data-stu-id="c8cf1-133">**dwMaxMBperSecTwoResolutionsTemporalQualityScalability**</span></span>  |
| <span data-ttu-id="c8cf1-134">10</span><span class="sxs-lookup"><span data-stu-id="c8cf1-134">10</span></span>            | <span data-ttu-id="c8cf1-135">**dwMaxMBperSecThreeResolutionsTemporalQualityScalablity**</span><span class="sxs-lookup"><span data-stu-id="c8cf1-135">**dwMaxMBperSecThreeResolutionsTemporalQualityScalablity**</span></span> |
| <span data-ttu-id="c8cf1-136">11</span><span class="sxs-lookup"><span data-stu-id="c8cf1-136">11</span></span>            | <span data-ttu-id="c8cf1-137">**dwMaxMBperSecFourResolutionsTemporalQualityScalability**</span><span class="sxs-lookup"><span data-stu-id="c8cf1-137">**dwMaxMBperSecFourResolutionsTemporalQualityScalability**</span></span> |
| <span data-ttu-id="c8cf1-138">12</span><span class="sxs-lookup"><span data-stu-id="c8cf1-138">12</span></span>            | <span data-ttu-id="c8cf1-139">**dwMaxMBperSecOneResolutionFullScalability**</span><span class="sxs-lookup"><span data-stu-id="c8cf1-139">**dwMaxMBperSecOneResolutionFullScalability**</span></span>              |
| <span data-ttu-id="c8cf1-140">13</span><span class="sxs-lookup"><span data-stu-id="c8cf1-140">13</span></span>            | <span data-ttu-id="c8cf1-141">**dwMaxMBperSecTwoResolutionsFullScalability**</span><span class="sxs-lookup"><span data-stu-id="c8cf1-141">**dwMaxMBperSecTwoResolutionsFullScalability**</span></span>             |
| <span data-ttu-id="c8cf1-142">14</span><span class="sxs-lookup"><span data-stu-id="c8cf1-142">14</span></span>            | <span data-ttu-id="c8cf1-143">**dwMaxMBperSecThreeResolutionsFullScalability**</span><span class="sxs-lookup"><span data-stu-id="c8cf1-143">**dwMaxMBperSecThreeResolutionsFullScalability**</span></span>           |
| <span data-ttu-id="c8cf1-144">15</span><span class="sxs-lookup"><span data-stu-id="c8cf1-144">15</span></span>            | <span data-ttu-id="c8cf1-145">**dwMaxMBperSecFourResolutionsFullScalability**</span><span class="sxs-lookup"><span data-stu-id="c8cf1-145">**dwMaxMBperSecFourResolutionsFullScalability**</span></span>            |



 

<span data-ttu-id="c8cf1-146">Questo attributo viene usato anche con [codificatori della fotocamera H. 264 UVC 1,5](camera-encoder-h264-uvc-1-5.md).</span><span class="sxs-lookup"><span data-stu-id="c8cf1-146">This attribute is also used with [H.264 UVC 1.5 camera encoders](camera-encoder-h264-uvc-1-5.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c8cf1-147">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c8cf1-147">Requirements</span></span>



| <span data-ttu-id="c8cf1-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8cf1-148">Requirement</span></span> | <span data-ttu-id="c8cf1-149">Valore</span><span class="sxs-lookup"><span data-stu-id="c8cf1-149">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c8cf1-150">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c8cf1-150">Minimum supported client</span></span><br/> | <span data-ttu-id="c8cf1-151">App desktop di Windows 8 app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="c8cf1-151">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="c8cf1-152">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c8cf1-152">Minimum supported server</span></span><br/> | <span data-ttu-id="c8cf1-153">App UWP per \[ app desktop di Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="c8cf1-153">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="c8cf1-154">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c8cf1-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8cf1-155"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8cf1-155"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8cf1-156">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c8cf1-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8cf1-157">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c8cf1-157">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c8cf1-158">Attributi del tipo di supporto</span><span class="sxs-lookup"><span data-stu-id="c8cf1-158">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




