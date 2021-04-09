---
description: Tempo di presentazione per un esempio di cui è stato eseguito il rendering durante lo scrubbing.
ms.assetid: 6ce52cf5-014b-49a2-abf7-2c9cc5340a42
title: Attributo MF_EVENT_SCRUBSAMPLE_TIME (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de7c4fb1a8015367fa3d48edb066cdb135983926
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967044"
---
# <a name="mf_event_scrubsample_time-attribute"></a><span data-ttu-id="e07f3-103">\_ \_ Attributo tempo SCRUBSAMPLE evento MF \_</span><span class="sxs-lookup"><span data-stu-id="e07f3-103">MF\_EVENT\_SCRUBSAMPLE\_TIME attribute</span></span>

<span data-ttu-id="e07f3-104">Tempo di presentazione per un esempio di cui è stato eseguito il rendering durante lo scrubbing.</span><span class="sxs-lookup"><span data-stu-id="e07f3-104">Presentation time for a sample that was rendered while scrubbing.</span></span>

## <a name="data-type"></a><span data-ttu-id="e07f3-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="e07f3-105">Data type</span></span>

<span data-ttu-id="e07f3-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="e07f3-106">**UINT64**</span></span>

<span data-ttu-id="e07f3-107">Considera come valore **LONGLONG** .</span><span class="sxs-lookup"><span data-stu-id="e07f3-107">Treat as a **LONGLONG** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e07f3-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="e07f3-108">Remarks</span></span>

<span data-ttu-id="e07f3-109">Questo attributo viene utilizzato con l'evento [MEStreamSinkScrubSampleComplete](mestreamsinkscrubsamplecomplete.md) .</span><span class="sxs-lookup"><span data-stu-id="e07f3-109">This attribute is used with the [MEStreamSinkScrubSampleComplete](mestreamsinkscrubsamplecomplete.md) event.</span></span>

<span data-ttu-id="e07f3-110">Questo attributo è un valore con segno, sebbene venga archiviato come **UInt64**.</span><span class="sxs-lookup"><span data-stu-id="e07f3-110">This attribute is a signed value, although it is stored as a **UINT64**.</span></span>

<span data-ttu-id="e07f3-111">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="e07f3-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="e07f3-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e07f3-112">Requirements</span></span>



| <span data-ttu-id="e07f3-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="e07f3-113">Requirement</span></span> | <span data-ttu-id="e07f3-114">Valore</span><span class="sxs-lookup"><span data-stu-id="e07f3-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e07f3-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e07f3-115">Minimum supported client</span></span><br/> | <span data-ttu-id="e07f3-116">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e07f3-116">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e07f3-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e07f3-117">Minimum supported server</span></span><br/> | <span data-ttu-id="e07f3-118">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e07f3-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e07f3-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e07f3-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="e07f3-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="e07f3-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e07f3-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e07f3-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e07f3-122">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e07f3-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e07f3-123">Attributi dell'evento</span><span class="sxs-lookup"><span data-stu-id="e07f3-123">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="e07f3-124">**IMFAttributes:: GetUInt64**</span><span class="sxs-lookup"><span data-stu-id="e07f3-124">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="e07f3-125">**IMFAttributes:: UINT64**</span><span class="sxs-lookup"><span data-stu-id="e07f3-125">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 




