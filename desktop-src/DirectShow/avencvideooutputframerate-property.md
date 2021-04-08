---
description: Specifica la frequenza dei fotogrammi nel flusso di output del codificatore, in frame al secondo.
ms.assetid: 72e16c7d-977e-4269-9576-afc789e31826
title: Proprietà AVEncVideoOutputFrameRate (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad4cb675c266d146936a3402934e51486ded5b02
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746231"
---
# <a name="avencvideooutputframerate-property"></a><span data-ttu-id="16294-103">Proprietà AVEncVideoOutputFrameRate</span><span class="sxs-lookup"><span data-stu-id="16294-103">AVEncVideoOutputFrameRate property</span></span>

<span data-ttu-id="16294-104">Specifica la frequenza dei fotogrammi nel flusso di output del codificatore, in frame al secondo.</span><span class="sxs-lookup"><span data-stu-id="16294-104">Specifies the frame rate on the encoder's output stream, in frames per second.</span></span>

<span data-ttu-id="16294-105">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="16294-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="16294-106">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="16294-106">Data type</span></span>

<span data-ttu-id="16294-107">**UInt64** (**VT \_ UI8**)</span><span class="sxs-lookup"><span data-stu-id="16294-107">**UINT64** (**VT\_UI8**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="16294-108">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="16294-108">Property GUID</span></span>

<span data-ttu-id="16294-109">**Codecapis \_ AVEncVideoOutputFrameRate**</span><span class="sxs-lookup"><span data-stu-id="16294-109">**CODECAPI\_AVEncVideoOutputFrameRate**</span></span>

## <a name="property-value"></a><span data-ttu-id="16294-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="16294-110">Property value</span></span>

<span data-ttu-id="16294-111">Il valore di questa proprietà è un rapporto che definisce la frequenza dei fotogrammi.</span><span class="sxs-lookup"><span data-stu-id="16294-111">The value of this property is a ratio that defines the frame rate.</span></span> <span data-ttu-id="16294-112">I 32 bit superiori contengono il numeratore e i 32 bit inferiori contengono il denominatore.</span><span class="sxs-lookup"><span data-stu-id="16294-112">The upper 32 bits contain the numerator, and the lower 32 bits contain the denominator.</span></span> <span data-ttu-id="16294-113">La tabella seguente mostra le frequenze dei fotogrammi comuni, in frame al secondo.</span><span class="sxs-lookup"><span data-stu-id="16294-113">The following table shows common frame rates, in frames per second.</span></span>



| <span data-ttu-id="16294-114">Frequenza dei fotogrammi</span><span class="sxs-lookup"><span data-stu-id="16294-114">Frame rate</span></span> | <span data-ttu-id="16294-115">Proporzioni</span><span class="sxs-lookup"><span data-stu-id="16294-115">Ratio</span></span>      |
|------------|------------|
| <span data-ttu-id="16294-116">23,97</span><span class="sxs-lookup"><span data-stu-id="16294-116">23.97</span></span>      | <span data-ttu-id="16294-117">24000/1001</span><span class="sxs-lookup"><span data-stu-id="16294-117">24000/1001</span></span> |
| <span data-ttu-id="16294-118">24</span><span class="sxs-lookup"><span data-stu-id="16294-118">24</span></span>         | <span data-ttu-id="16294-119">24/1</span><span class="sxs-lookup"><span data-stu-id="16294-119">24/1</span></span>       |
| <span data-ttu-id="16294-120">25</span><span class="sxs-lookup"><span data-stu-id="16294-120">25</span></span>         | <span data-ttu-id="16294-121">25/1</span><span class="sxs-lookup"><span data-stu-id="16294-121">25/1</span></span>       |
| <span data-ttu-id="16294-122">29,97</span><span class="sxs-lookup"><span data-stu-id="16294-122">29.97</span></span>      | <span data-ttu-id="16294-123">30000/1001</span><span class="sxs-lookup"><span data-stu-id="16294-123">30000/1001</span></span> |
| <span data-ttu-id="16294-124">30</span><span class="sxs-lookup"><span data-stu-id="16294-124">30</span></span>         | <span data-ttu-id="16294-125">30/1</span><span class="sxs-lookup"><span data-stu-id="16294-125">30/1</span></span>       |
| <span data-ttu-id="16294-126">50</span><span class="sxs-lookup"><span data-stu-id="16294-126">50</span></span>         | <span data-ttu-id="16294-127">50/1</span><span class="sxs-lookup"><span data-stu-id="16294-127">50/1</span></span>       |
| <span data-ttu-id="16294-128">59,94</span><span class="sxs-lookup"><span data-stu-id="16294-128">59.94</span></span>      | <span data-ttu-id="16294-129">60000/1001</span><span class="sxs-lookup"><span data-stu-id="16294-129">60000/1001</span></span> |
| <span data-ttu-id="16294-130">60</span><span class="sxs-lookup"><span data-stu-id="16294-130">60</span></span>         | <span data-ttu-id="16294-131">60/1</span><span class="sxs-lookup"><span data-stu-id="16294-131">60/1</span></span>       |



 

## <a name="remarks"></a><span data-ttu-id="16294-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="16294-132">Remarks</span></span>

<span data-ttu-id="16294-133">Le applicazioni possono impostare questa proprietà per specificare la frequenza dei fotogrammi di output.</span><span class="sxs-lookup"><span data-stu-id="16294-133">Applications can set this property to specify the output frame rate.</span></span> <span data-ttu-id="16294-134">I codificatori possono inoltre restituire questa proprietà come funzionalità.</span><span class="sxs-lookup"><span data-stu-id="16294-134">Encoders can also return this property as a capability.</span></span> <span data-ttu-id="16294-135">A seconda del codificatore, il valore potrebbe essere limitato alla frequenza dei fotogrammi di input.</span><span class="sxs-lookup"><span data-stu-id="16294-135">Depending on the encoder, the value might be restricted to the input frame rate.</span></span> <span data-ttu-id="16294-136">In caso contrario, il codificatore è in grado di convertire internamente la frequenza dei fotogrammi.</span><span class="sxs-lookup"><span data-stu-id="16294-136">If not, the encoder is able to convert the frame rate internally.</span></span> <span data-ttu-id="16294-137">Vedere [**Proprietà AVEncVideoOutputFrameRateConversion**](avencvideooutputframerateconversion-property.md).</span><span class="sxs-lookup"><span data-stu-id="16294-137">See [**AVEncVideoOutputFrameRateConversion Property**](avencvideooutputframerateconversion-property.md).</span></span>

<span data-ttu-id="16294-138">Questa proprietà viene usata anche con [codificatori della fotocamera H. 264 UVC 1,5](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5).</span><span class="sxs-lookup"><span data-stu-id="16294-138">This property is also used with [H.264 UVC 1.5 camera encoders](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5).</span></span>

## <a name="requirements"></a><span data-ttu-id="16294-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="16294-139">Requirements</span></span>



| <span data-ttu-id="16294-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="16294-140">Requirement</span></span> | <span data-ttu-id="16294-141">Valore</span><span class="sxs-lookup"><span data-stu-id="16294-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="16294-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="16294-142">Minimum supported client</span></span><br/> | <span data-ttu-id="16294-143">App UWP di Windows 2000 Professional \[ desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="16294-143">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="16294-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="16294-144">Minimum supported server</span></span><br/> | <span data-ttu-id="16294-145">App desktop di Windows 2000 Server \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="16294-145">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="16294-146">Intestazione</span><span class="sxs-lookup"><span data-stu-id="16294-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="16294-147"><dt>Codecapis. h</dt></span><span class="sxs-lookup"><span data-stu-id="16294-147"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16294-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="16294-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16294-149">Proprietà dell'API codec</span><span class="sxs-lookup"><span data-stu-id="16294-149">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="16294-150">**Interfaccia ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="16294-150">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

