---
description: Segnala l'inizio di ogni unità VOBU (video Object Unit), un segmento video di lunghezza compresa tra 0,4 e 1,0 secondi.
ms.assetid: 1f2def2f-3a6b-458b-b564-09b6cf74543c
title: EC_DVD_CURRENT_TIME (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_CURRENT_TIME
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 0f1bb2f5f31efa881917ac71ea381cc0a82e8744
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327440"
---
# <a name="ec_dvd_current_time"></a><span data-ttu-id="7354a-103">\_ \_ ora corrente DVD \_ EC</span><span class="sxs-lookup"><span data-stu-id="7354a-103">EC\_DVD\_CURRENT\_TIME</span></span>

<span data-ttu-id="7354a-104">Segnala l'inizio di ogni unità VOBU (video Object Unit), un segmento video di lunghezza compresa tra 0,4 e 1,0 secondi.</span><span class="sxs-lookup"><span data-stu-id="7354a-104">Signals the beginning of every video object unit (VOBU), a video segment which is 0.4 to 1.0 seconds in length.</span></span>

## <a name="parameters"></a><span data-ttu-id="7354a-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="7354a-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7354a-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="7354a-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="7354a-107">Valore **DWORD** che indica il codice temporale di riproduzione corrente in un formato binario codificato (BCD) di ore, minuti, secondi, frame (HH: mm: SS: FF).</span><span class="sxs-lookup"><span data-stu-id="7354a-107">**DWORD** value indicating the current playback timecode in a binary coded decimal (BCD) hours, minutes, seconds, frames (HH:MM:SS:FF) format.</span></span> <span data-ttu-id="7354a-108">Membro della struttura [**del \_ timecode del DVD**](/windows/win32/api/strmif/ns-strmif-dvd_timecode) .</span><span class="sxs-lookup"><span data-stu-id="7354a-108">Member of the [**DVD\_TIMECODE**](/windows/win32/api/strmif/ns-strmif-dvd_timecode) structure.</span></span>

</dd> <dt>

<span data-ttu-id="7354a-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="7354a-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="7354a-110">Valore booleano (**bool**) che indica il timecode.</span><span class="sxs-lookup"><span data-stu-id="7354a-110">Boolean (**BOOL**) value indicating the timecode.</span></span> <span data-ttu-id="7354a-111">Zero (0) indica 25 fotogrammi al secondo, mentre 1 indica 30 fotogrammi al secondo (non eliminati).</span><span class="sxs-lookup"><span data-stu-id="7354a-111">Zero (0) indicates 25 frames per second while 1 indicates 30 frames per second (nondropped).</span></span> <span data-ttu-id="7354a-112">Il valore 2 indica che non è possibile determinare il tempo di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="7354a-112">A value of 2 indicates the playback time cannot be determined.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7354a-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="7354a-113">Remarks</span></span>

<span data-ttu-id="7354a-114">Solo i film lineari semplici segnalano questo evento.</span><span class="sxs-lookup"><span data-stu-id="7354a-114">Only simple linear movies signal this event.</span></span>

<span data-ttu-id="7354a-115">Questo evento viene generato nel dominio del titolo.</span><span class="sxs-lookup"><span data-stu-id="7354a-115">This event is raised in the title domain.</span></span>

## <a name="requirements"></a><span data-ttu-id="7354a-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7354a-116">Requirements</span></span>



| <span data-ttu-id="7354a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="7354a-117">Requirement</span></span> | <span data-ttu-id="7354a-118">Valore</span><span class="sxs-lookup"><span data-stu-id="7354a-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7354a-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7354a-119">Header</span></span><br/> | <dl> <span data-ttu-id="7354a-120"><dt>Dvdevcode. h (include dshow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7354a-120"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7354a-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7354a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7354a-122">Applicazioni DVD</span><span class="sxs-lookup"><span data-stu-id="7354a-122">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="7354a-123">Codici di notifica degli eventi DVD</span><span class="sxs-lookup"><span data-stu-id="7354a-123">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="7354a-124">Notifica degli eventi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="7354a-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




