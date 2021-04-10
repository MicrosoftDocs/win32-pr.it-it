---
description: Specifica se ripetere il primo campo in un frame interlacciato. Questo attributo si applica agli esempi di supporti.
ms.assetid: c469f418-fa23-443f-8012-0d548ee98c17
title: Attributo MFSampleExtension_RepeatFirstField (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0af10157c280a3e48ed8f415529534fc97fd5cc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130519"
---
# <a name="mfsampleextension_repeatfirstfield-attribute"></a><span data-ttu-id="c1e6e-104">\_Attributo RepeatFirstField di MFSampleExtension</span><span class="sxs-lookup"><span data-stu-id="c1e6e-104">MFSampleExtension\_RepeatFirstField attribute</span></span>

<span data-ttu-id="c1e6e-105">Specifica se ripetere il primo campo in un frame interlacciato.</span><span class="sxs-lookup"><span data-stu-id="c1e6e-105">Specifies whether to repeat the first field in an interlaced frame.</span></span> <span data-ttu-id="c1e6e-106">Questo attributo si applica agli esempi di supporti.</span><span class="sxs-lookup"><span data-stu-id="c1e6e-106">This attribute applies to media samples.</span></span>

## <a name="data-type"></a><span data-ttu-id="c1e6e-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="c1e6e-107">Data type</span></span>

<span data-ttu-id="c1e6e-108">**Bool** archiviato come **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c1e6e-108">**BOOL** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="c1e6e-109">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="c1e6e-109">Get/set</span></span>

<span data-ttu-id="c1e6e-110">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="c1e6e-110">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="c1e6e-111">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="c1e6e-111">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="c1e6e-112">Si applica a</span><span class="sxs-lookup"><span data-stu-id="c1e6e-112">Applies to</span></span>

[<span data-ttu-id="c1e6e-113">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="c1e6e-113">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="c1e6e-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="c1e6e-114">Remarks</span></span>

<span data-ttu-id="c1e6e-115">Se il valore è **false** o l'attributo non è impostato, il primo campo non viene ripetuto.</span><span class="sxs-lookup"><span data-stu-id="c1e6e-115">If the value is **FALSE** or the attribute is not set, the first field is not repeated.</span></span> <span data-ttu-id="c1e6e-116">Se il valore è **true**, il primo campo viene ripetuto.</span><span class="sxs-lookup"><span data-stu-id="c1e6e-116">If the value is **TRUE**, the first field is repeated.</span></span> <span data-ttu-id="c1e6e-117">Il valore **true** è valido solo quando sono soddisfatte le condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="c1e6e-117">The value **TRUE** is valid only when the following conditions are true:</span></span>

-   <span data-ttu-id="c1e6e-118">Il tipo di supporto è misto interlacciato e progressivo.</span><span class="sxs-lookup"><span data-stu-id="c1e6e-118">The media type is mixed interlaced and progressive.</span></span> <span data-ttu-id="c1e6e-119">L'attributo dell'attributo della [**\_ \_ \_ modalità di interpolazione MF mt**](mf-mt-interlace-mode-attribute.md) sul tipo di supporto è **MFVideoInterlace \_ MixedInterlaceOrProgressive**.</span><span class="sxs-lookup"><span data-stu-id="c1e6e-119">(The [**MF\_MT\_INTERLACE\_MODE**](mf-mt-interlace-mode-attribute.md) attribute attribute on the media type is **MFVideoInterlace\_MixedInterlaceOrProgressive**.)</span></span>
-   <span data-ttu-id="c1e6e-120">Il frame è progressivo e l'attributo [**\_ interlacciato MFSampleExtension**](mfsampleextension-interlaced-attribute.md) nell'esempio è **true**.</span><span class="sxs-lookup"><span data-stu-id="c1e6e-120">The frame is progressive and the [**MFSampleExtension\_Interlaced**](mfsampleextension-interlaced-attribute.md) attribute on the sample is **TRUE**.</span></span>
-   <span data-ttu-id="c1e6e-121">L' [**attributo \_ BottomFieldFirst di MFSampleExtension**](mfsampleextension-bottomfieldfirst-attribute.md) è impostato nell'esempio.</span><span class="sxs-lookup"><span data-stu-id="c1e6e-121">The [**MFSampleExtension\_BottomFieldFirst**](mfsampleextension-bottomfieldfirst-attribute.md) attribute is set on the sample.</span></span> <span data-ttu-id="c1e6e-122">Il valore può essere **true** o **false**.</span><span class="sxs-lookup"><span data-stu-id="c1e6e-122">The value can be **TRUE** or **FALSE**.</span></span> <span data-ttu-id="c1e6e-123">L'ordinamento dei campi è determinato da questo attributo.</span><span class="sxs-lookup"><span data-stu-id="c1e6e-123">The ordering of the fields is determined by this attribute.</span></span>

<span data-ttu-id="c1e6e-124">Questo attributo viene usato per la discesa 3:2.</span><span class="sxs-lookup"><span data-stu-id="c1e6e-124">This attribute is used for 3:2 pulldown.</span></span> <span data-ttu-id="c1e6e-125">La tabella seguente mostra l'ordine in cui vengono visualizzati i campi.</span><span class="sxs-lookup"><span data-stu-id="c1e6e-125">The following table shows the order in which fields are displayed.</span></span>



| <span data-ttu-id="c1e6e-126">\_RepeatFirstField MFSampleExtension</span><span class="sxs-lookup"><span data-stu-id="c1e6e-126">MFSampleExtension\_RepeatFirstField</span></span> | <span data-ttu-id="c1e6e-127">\_BottomFieldFirst MFSampleExtension</span><span class="sxs-lookup"><span data-stu-id="c1e6e-127">MFSampleExtension\_BottomFieldFirst</span></span> | <span data-ttu-id="c1e6e-128">Ordine campi</span><span class="sxs-lookup"><span data-stu-id="c1e6e-128">Field order</span></span>         |
|-------------------------------------|-------------------------------------|---------------------|
| <span data-ttu-id="c1e6e-129">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="c1e6e-129">**TRUE**</span></span>                            | <span data-ttu-id="c1e6e-130">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="c1e6e-130">**TRUE**</span></span>                            | <span data-ttu-id="c1e6e-131">Inferiore, superiore, inferiore</span><span class="sxs-lookup"><span data-stu-id="c1e6e-131">Lower, upper, lower</span></span> |
| <span data-ttu-id="c1e6e-132">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="c1e6e-132">**TRUE**</span></span>                            | <span data-ttu-id="c1e6e-133">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="c1e6e-133">**FALSE**</span></span>                           | <span data-ttu-id="c1e6e-134">Superiore, inferiore, superiore</span><span class="sxs-lookup"><span data-stu-id="c1e6e-134">Upper, lower, upper</span></span> |
| <span data-ttu-id="c1e6e-135">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="c1e6e-135">**FALSE**</span></span>                           | <span data-ttu-id="c1e6e-136">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="c1e6e-136">**TRUE**</span></span>                            | <span data-ttu-id="c1e6e-137">Inferiore, superiore</span><span class="sxs-lookup"><span data-stu-id="c1e6e-137">Lower, upper</span></span>        |
| <span data-ttu-id="c1e6e-138">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="c1e6e-138">**FALSE**</span></span>                           | <span data-ttu-id="c1e6e-139">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="c1e6e-139">**FALSE**</span></span>                           | <span data-ttu-id="c1e6e-140">Superiore, inferiore</span><span class="sxs-lookup"><span data-stu-id="c1e6e-140">Upper, lower</span></span>        |



 

<span data-ttu-id="c1e6e-141">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="c1e6e-141">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1e6e-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c1e6e-142">Requirements</span></span>



| <span data-ttu-id="c1e6e-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1e6e-143">Requirement</span></span> | <span data-ttu-id="c1e6e-144">Valore</span><span class="sxs-lookup"><span data-stu-id="c1e6e-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c1e6e-145">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c1e6e-145">Minimum supported client</span></span><br/> | <span data-ttu-id="c1e6e-146">App desktop di Windows Vista app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="c1e6e-146">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="c1e6e-147">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c1e6e-147">Minimum supported server</span></span><br/> | <span data-ttu-id="c1e6e-148">App UWP per \[ app desktop di Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="c1e6e-148">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="c1e6e-149">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c1e6e-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1e6e-150"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1e6e-150"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1e6e-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c1e6e-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1e6e-152">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c1e6e-152">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c1e6e-153">Attributi di esempio</span><span class="sxs-lookup"><span data-stu-id="c1e6e-153">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="c1e6e-154">Esempi di supporti</span><span class="sxs-lookup"><span data-stu-id="c1e6e-154">Media Samples</span></span>](media-samples.md)
</dt> <dt>

[<span data-ttu-id="c1e6e-155">Interlacciamento video</span><span class="sxs-lookup"><span data-stu-id="c1e6e-155">Video Interlacing</span></span>](video-interlacing.md)
</dt> </dl>

 

 




