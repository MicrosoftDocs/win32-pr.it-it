---
description: Specifica se un campione video contiene un solo campo o due campi con interfoliazione. Questo attributo si applica agli esempi di supporti.
ms.assetid: 550619be-2042-4a2c-9ad2-728474835255
title: Attributo MFSampleExtension_SingleField (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 217d7c43a9777982485ba350d259a59a518e26c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527925"
---
# <a name="mfsampleextension_singlefield-attribute"></a><span data-ttu-id="ceb3b-104">\_Attributo SingleField di MFSampleExtension</span><span class="sxs-lookup"><span data-stu-id="ceb3b-104">MFSampleExtension\_SingleField attribute</span></span>

<span data-ttu-id="ceb3b-105">Specifica se un campione video contiene un solo campo o due campi con interfoliazione.</span><span class="sxs-lookup"><span data-stu-id="ceb3b-105">Specifies whether a video sample contains a single field or two interleaved fields.</span></span> <span data-ttu-id="ceb3b-106">Questo attributo si applica agli esempi di supporti.</span><span class="sxs-lookup"><span data-stu-id="ceb3b-106">This attribute applies to media samples.</span></span>

## <a name="data-type"></a><span data-ttu-id="ceb3b-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="ceb3b-107">Data type</span></span>

<span data-ttu-id="ceb3b-108">**Bool** archiviato come **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ceb3b-108">**BOOL** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="ceb3b-109">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="ceb3b-109">Get/set</span></span>

<span data-ttu-id="ceb3b-110">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="ceb3b-110">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="ceb3b-111">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="ceb3b-111">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="ceb3b-112">Si applica a</span><span class="sxs-lookup"><span data-stu-id="ceb3b-112">Applies to</span></span>

[<span data-ttu-id="ceb3b-113">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="ceb3b-113">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="ceb3b-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="ceb3b-114">Remarks</span></span>

<span data-ttu-id="ceb3b-115">Se il valore è **true**, l'esempio contiene un campo.</span><span class="sxs-lookup"><span data-stu-id="ceb3b-115">If the value is **TRUE**, the sample contains one field.</span></span> <span data-ttu-id="ceb3b-116">Se il valore è **false** o l'attributo non è impostato, l'esempio contiene un frame completo.</span><span class="sxs-lookup"><span data-stu-id="ceb3b-116">If the value is **FALSE** or the attribute is not set, the sample contains a complete frame.</span></span> <span data-ttu-id="ceb3b-117">(Due campi se interlacciato o un frame progressivo).</span><span class="sxs-lookup"><span data-stu-id="ceb3b-117">(Two fields if interlaced, or a progressive frame.)</span></span>

<span data-ttu-id="ceb3b-118">Se il tipo di supporto è frame progressivi o campi con interfoliazione, questo attributo deve essere impostato su **false** o Left.</span><span class="sxs-lookup"><span data-stu-id="ceb3b-118">If the media type is progressive frames or interleaved fields, this attribute must be **FALSE** or left unset.</span></span>

<span data-ttu-id="ceb3b-119">Se il tipo di supporto è Single Field, questo attributo deve essere **true**.</span><span class="sxs-lookup"><span data-stu-id="ceb3b-119">If the media type is single field, this attribute must be **TRUE**.</span></span> <span data-ttu-id="ceb3b-120">Impostare l'attributo [**MFSampleExtension \_ BottomFieldFirst**](mfsampleextension-bottomfieldfirst-attribute.md) nell'esempio per indicare se si tratta del campo superiore o inferiore.</span><span class="sxs-lookup"><span data-stu-id="ceb3b-120">Set the [**MFSampleExtension\_BottomFieldFirst**](mfsampleextension-bottomfieldfirst-attribute.md) attribute on the sample to indicate whether it is the upper field or the lower field.</span></span>

<span data-ttu-id="ceb3b-121">Attualmente il renderer video migliorato (EVR) non supporta il contenuto che passa tra i frame interlacciati e i singoli campi.</span><span class="sxs-lookup"><span data-stu-id="ceb3b-121">Currently the enhanced video renderer (EVR) does not support content that switches between interlaced frames and single fields.</span></span>

<span data-ttu-id="ceb3b-122">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="ceb3b-122">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="ceb3b-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ceb3b-123">Requirements</span></span>



| <span data-ttu-id="ceb3b-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="ceb3b-124">Requirement</span></span> | <span data-ttu-id="ceb3b-125">Valore</span><span class="sxs-lookup"><span data-stu-id="ceb3b-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ceb3b-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ceb3b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ceb3b-127">App desktop di Windows Vista app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="ceb3b-127">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="ceb3b-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ceb3b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ceb3b-129">App UWP per \[ app desktop di Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="ceb3b-129">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="ceb3b-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ceb3b-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="ceb3b-131"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="ceb3b-131"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ceb3b-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ceb3b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ceb3b-133">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ceb3b-133">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ceb3b-134">Attributi di esempio</span><span class="sxs-lookup"><span data-stu-id="ceb3b-134">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="ceb3b-135">Esempi di supporti</span><span class="sxs-lookup"><span data-stu-id="ceb3b-135">Media Samples</span></span>](media-samples.md)
</dt> <dt>

[<span data-ttu-id="ceb3b-136">Interlacciamento video</span><span class="sxs-lookup"><span data-stu-id="ceb3b-136">Video Interlacing</span></span>](video-interlacing.md)
</dt> </dl>

 

 




