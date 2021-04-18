---
description: Ora approssimativa in cui la sessione multimediale ha generato un evento.
ms.assetid: 58083bc8-59cc-4503-8fae-36fcd864921a
title: Attributo MF_SESSION_APPROX_EVENT_OCCURRENCE_TIME (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a31b1970c2c9d86384c12c50777a8cee55e3ffd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315013"
---
# <a name="mf_session_approx_event_occurrence_time-attribute"></a><span data-ttu-id="5914c-103">\_ \_ \_ \_ Attributo tempo di occorrenza \_ evento MF Session approx</span><span class="sxs-lookup"><span data-stu-id="5914c-103">MF\_SESSION\_APPROX\_EVENT\_OCCURRENCE\_TIME attribute</span></span>

<span data-ttu-id="5914c-104">Ora approssimativa in cui la sessione multimediale ha generato un evento.</span><span class="sxs-lookup"><span data-stu-id="5914c-104">The approximate time when the Media Session raised an event.</span></span>

## <a name="data-type"></a><span data-ttu-id="5914c-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="5914c-105">Data type</span></span>

<span data-ttu-id="5914c-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="5914c-106">**UINT64**</span></span>

<span data-ttu-id="5914c-107">Considera come valore **LONGLONG** .</span><span class="sxs-lookup"><span data-stu-id="5914c-107">Treat as a **LONGLONG** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5914c-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="5914c-108">Remarks</span></span>

<span data-ttu-id="5914c-109">Per alcuni eventi della sessione multimediale è presente questo attributo.</span><span class="sxs-lookup"><span data-stu-id="5914c-109">Some events from the Media Session have this attribute.</span></span> <span data-ttu-id="5914c-110">Il valore indica l'ora di presentazione approssimativa in cui è stato generato l'evento.</span><span class="sxs-lookup"><span data-stu-id="5914c-110">The value gives the approximate presentation time when the event was raised.</span></span>

<span data-ttu-id="5914c-111">Questo attributo è un valore con segno, sebbene venga archiviato come **UInt64**.</span><span class="sxs-lookup"><span data-stu-id="5914c-111">This attribute is a signed value, although it is stored as a **UINT64**.</span></span>

<span data-ttu-id="5914c-112">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="5914c-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="5914c-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5914c-113">Requirements</span></span>



| <span data-ttu-id="5914c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="5914c-114">Requirement</span></span> | <span data-ttu-id="5914c-115">Valore</span><span class="sxs-lookup"><span data-stu-id="5914c-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5914c-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5914c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5914c-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5914c-117">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="5914c-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5914c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5914c-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5914c-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5914c-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5914c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="5914c-121"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="5914c-121"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5914c-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5914c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5914c-123">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5914c-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="5914c-124">Attributi dell'evento</span><span class="sxs-lookup"><span data-stu-id="5914c-124">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="5914c-125">**IMFAttributes:: GetUInt64**</span><span class="sxs-lookup"><span data-stu-id="5914c-125">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="5914c-126">**IMFAttributes:: UINT64**</span><span class="sxs-lookup"><span data-stu-id="5914c-126">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 




