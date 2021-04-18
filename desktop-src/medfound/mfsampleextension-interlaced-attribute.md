---
description: Indica se un frame video è interlacciato o progressivo.
ms.assetid: 3cb80e75-e803-493b-a22d-e485e77b5177
title: Attributo MFSampleExtension_Interlaced (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43a273b548192ac52da8604eb36fde5ec0e9fcf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309091"
---
# <a name="mfsampleextension_interlaced-attribute"></a><span data-ttu-id="15cf7-103">MFSampleExtension- \_ attributo interlacciato</span><span class="sxs-lookup"><span data-stu-id="15cf7-103">MFSampleExtension\_Interlaced attribute</span></span>

<span data-ttu-id="15cf7-104">Indica se un frame video è interlacciato o progressivo.</span><span class="sxs-lookup"><span data-stu-id="15cf7-104">Indicates whether a video frame is interlaced or progressive.</span></span> <span data-ttu-id="15cf7-105">Se **true**, il frame è interlacciato.</span><span class="sxs-lookup"><span data-stu-id="15cf7-105">If **TRUE**, the frame is interlaced.</span></span> <span data-ttu-id="15cf7-106">Se **false**, il frame è progressivo.</span><span class="sxs-lookup"><span data-stu-id="15cf7-106">If **FALSE**, the frame is progressive.</span></span> <span data-ttu-id="15cf7-107">Se non impostato, il tipo di supporto descrive il interlacciamento.</span><span class="sxs-lookup"><span data-stu-id="15cf7-107">If not set, the media type describes the interlacing.</span></span> <span data-ttu-id="15cf7-108">Questo attributo si applica agli esempi di supporti.</span><span class="sxs-lookup"><span data-stu-id="15cf7-108">This attribute applies to media samples.</span></span>

## <a name="data-type"></a><span data-ttu-id="15cf7-109">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="15cf7-109">Data type</span></span>

<span data-ttu-id="15cf7-110">**Bool** archiviato come **UInt32**</span><span class="sxs-lookup"><span data-stu-id="15cf7-110">**BOOL** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="15cf7-111">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="15cf7-111">Get/set</span></span>

<span data-ttu-id="15cf7-112">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="15cf7-112">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="15cf7-113">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="15cf7-113">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="15cf7-114">Si applica a</span><span class="sxs-lookup"><span data-stu-id="15cf7-114">Applies to</span></span>

[<span data-ttu-id="15cf7-115">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="15cf7-115">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="15cf7-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="15cf7-116">Remarks</span></span>

<span data-ttu-id="15cf7-117">Per contenuti video contenenti frame misti progressivi e interlacciati, impostare il tipo di supporto su interlacciato e utilizzare questo attributo in ogni frame per indicare se il frame è progressivo o interlacciato.</span><span class="sxs-lookup"><span data-stu-id="15cf7-117">For video content that contains mixed progressive and interlaced frames, set the media type to interlaced and use this attribute on each frame to indicate whether the frame is progressive or interlaced.</span></span>

<span data-ttu-id="15cf7-118">Per contenuto video completamente interlacciato, impostare il tipo di supporto su interlacciato e omettere questo attributo o impostarlo su **true** in ogni campione.</span><span class="sxs-lookup"><span data-stu-id="15cf7-118">For video content that is entirely interlaced, set the media type to interlaced and omit this attribute, or set it to **TRUE** on every sample.</span></span>

<span data-ttu-id="15cf7-119">Per contenuti video completamente progressivi, impostare il tipo di supporto su progressive e omettere questo attributo o impostarlo su **false** in ogni esempio.</span><span class="sxs-lookup"><span data-stu-id="15cf7-119">For video content that is entirely progressive, set the media type to progressive and omit this attribute, or set it to **FALSE** on every sample.</span></span>

<span data-ttu-id="15cf7-120">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="15cf7-120">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="15cf7-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="15cf7-121">Requirements</span></span>



| <span data-ttu-id="15cf7-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="15cf7-122">Requirement</span></span> | <span data-ttu-id="15cf7-123">Valore</span><span class="sxs-lookup"><span data-stu-id="15cf7-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="15cf7-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="15cf7-124">Minimum supported client</span></span><br/> | <span data-ttu-id="15cf7-125">App desktop di Windows Vista app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="15cf7-125">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="15cf7-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="15cf7-126">Minimum supported server</span></span><br/> | <span data-ttu-id="15cf7-127">App UWP per \[ app desktop di Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="15cf7-127">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="15cf7-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="15cf7-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="15cf7-129"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="15cf7-129"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15cf7-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="15cf7-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15cf7-131">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="15cf7-131">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="15cf7-132">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="15cf7-132">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="15cf7-133">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="15cf7-133">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="15cf7-134">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="15cf7-134">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> <dt>

[<span data-ttu-id="15cf7-135">Attributi di esempio</span><span class="sxs-lookup"><span data-stu-id="15cf7-135">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="15cf7-136">Esempi di supporti</span><span class="sxs-lookup"><span data-stu-id="15cf7-136">Media Samples</span></span>](media-samples.md)
</dt> <dt>

[<span data-ttu-id="15cf7-137">Interlacciamento video</span><span class="sxs-lookup"><span data-stu-id="15cf7-137">Video Interlacing</span></span>](video-interlacing.md)
</dt> </dl>

 

 




