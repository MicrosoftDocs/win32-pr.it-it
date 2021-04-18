---
description: Un nuovo segmento è stato avviato.
ms.assetid: 9742436a-e233-4641-a0d5-aa240cde5f28
title: EC_SEGMENT_STARTED (dshow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7e7df85bddb78fe2687a017b481e6db62ba37c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325042"
---
# <a name="ec_segment_started"></a><span data-ttu-id="0ba2b-103">\_segmento EC \_ avviato</span><span class="sxs-lookup"><span data-stu-id="0ba2b-103">EC\_SEGMENT\_STARTED</span></span>

<span data-ttu-id="0ba2b-104">Un nuovo segmento è stato avviato.</span><span class="sxs-lookup"><span data-stu-id="0ba2b-104">A new segment has started.</span></span>

## <a name="parameters"></a><span data-ttu-id="0ba2b-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="0ba2b-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ba2b-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="0ba2b-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="0ba2b-107">(**const** **Reference \_ Time** \* ) puntatore a un valore di **\_ ora di riferimento** che specifica il tempo di flusso accumulato dopo l'avvio del segmento, in unità 100-nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="0ba2b-107">(**const** **REFERENCE\_TIME**\*) Pointer to a **REFERENCE\_TIME** value that specifies the accumulated stream time since the start of the segment, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="0ba2b-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="0ba2b-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="0ba2b-109">(**DWORD**) Numero di segmento (in base zero).</span><span class="sxs-lookup"><span data-stu-id="0ba2b-109">(**DWORD**) Segment number (zero-based).</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="0ba2b-110">Azione predefinita</span><span class="sxs-lookup"><span data-stu-id="0ba2b-110">Default Action</span></span>

<span data-ttu-id="0ba2b-111">Questo evento non viene inviato all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0ba2b-111">This event is not sent to the application.</span></span> <span data-ttu-id="0ba2b-112">Le applicazioni non possono eseguire l'override dell'azione predefinita per questo evento.</span><span class="sxs-lookup"><span data-stu-id="0ba2b-112">Applications cannot override the default action for this event.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ba2b-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="0ba2b-113">Remarks</span></span>

<span data-ttu-id="0ba2b-114">Se un filtro invierà una [**\_ fine \_ del \_ segmento EC**](ec-end-of-segment.md) alla fine di un segmento, invierà questo evento all'inizio del segmento.</span><span class="sxs-lookup"><span data-stu-id="0ba2b-114">If a filter will send an [**EC\_END\_OF\_SEGMENT**](ec-end-of-segment.md) at the end of a segment, it sends this event at the start of the segment.</span></span> <span data-ttu-id="0ba2b-115">Filter Graph Manager usa questa notifica degli eventi per calcolare \_ \_ il numero di notifiche della fine del \_ segmento EC che dovrebbe aspettarsi alla fine del segmento.</span><span class="sxs-lookup"><span data-stu-id="0ba2b-115">The filter graph manager uses this event notification to compute how many EC\_END\_OF\_SEGMENT notifications it should expect at the end of the segment.</span></span>

<span data-ttu-id="0ba2b-116">Per impostazione predefinita, i filtri non inviano eventi [**\_ \_ di fine \_ segmento EC**](ec-end-of-segment.md) alla fine dei segmenti e pertanto non devono inviare questo evento.</span><span class="sxs-lookup"><span data-stu-id="0ba2b-116">By default, filters do not send [**EC\_END\_OF\_SEGMENT**](ec-end-of-segment.md) events at the end of segments, and therefore should not send this event.</span></span> <span data-ttu-id="0ba2b-117">Per altre informazioni, vedere [**IMediaSeeking:: Sepositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions).</span><span class="sxs-lookup"><span data-stu-id="0ba2b-117">For more information, see [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions).</span></span>

## <a name="requirements"></a><span data-ttu-id="0ba2b-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0ba2b-118">Requirements</span></span>



| <span data-ttu-id="0ba2b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ba2b-119">Requirement</span></span> | <span data-ttu-id="0ba2b-120">Valore</span><span class="sxs-lookup"><span data-stu-id="0ba2b-120">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0ba2b-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0ba2b-121">Header</span></span><br/> | <dl> <span data-ttu-id="0ba2b-122"><dt>Dshow. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ba2b-122"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ba2b-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0ba2b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ba2b-124">Codici di notifica degli eventi</span><span class="sxs-lookup"><span data-stu-id="0ba2b-124">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="0ba2b-125">Notifica degli eventi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="0ba2b-125">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




