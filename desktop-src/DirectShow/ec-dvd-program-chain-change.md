---
description: Inviato quando viene modificato il PGC (Current Program Chain).
ms.assetid: 80fcd059-6ab4-4116-ac3a-012c451237b3
title: EC_DVD_PROGRAM_CHAIN_CHANGE (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_PROGRAM_CHAIN_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: eefd45ac1d147a0409417f215e56a4db490dfdbe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326641"
---
# <a name="ec_dvd_program_chain_change"></a><span data-ttu-id="a631c-103">\_ \_ \_ modifica catena programma DVD \_ EC</span><span class="sxs-lookup"><span data-stu-id="a631c-103">EC\_DVD\_PROGRAM\_CHAIN\_CHANGE</span></span>

<span data-ttu-id="a631c-104">Inviato quando viene modificato il PGC (Current Program Chain).</span><span class="sxs-lookup"><span data-stu-id="a631c-104">Sent when current program chain (PGC) changes.</span></span>

## <a name="parameters"></a><span data-ttu-id="a631c-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="a631c-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a631c-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="a631c-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="a631c-107">Il nuovo numero della catena di programmi (PGCN).</span><span class="sxs-lookup"><span data-stu-id="a631c-107">The new program chain number (PGCN).</span></span>

</dd> <dt>

<span data-ttu-id="a631c-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="a631c-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="a631c-109">Identificatore delle impostazioni locali (LCID) della lingua audio.</span><span class="sxs-lookup"><span data-stu-id="a631c-109">The locale identifier (LCID) of the audio language.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a631c-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="a631c-110">Remarks</span></span>

<span data-ttu-id="a631c-111">Questo evento è disabilitato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="a631c-111">This event is disabled by default.</span></span> <span data-ttu-id="a631c-112">Per abilitare questo evento, chiamare [**IDVDControl2:: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) e impostare l'opzione **DVD \_ NotifyPositionChange** su **true**.</span><span class="sxs-lookup"><span data-stu-id="a631c-112">To enable this event, call [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) and set the **DVD\_NotifyPositionChange** option to **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a631c-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a631c-113">Requirements</span></span>



| <span data-ttu-id="a631c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a631c-114">Requirement</span></span> | <span data-ttu-id="a631c-115">Valore</span><span class="sxs-lookup"><span data-stu-id="a631c-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a631c-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a631c-116">Header</span></span><br/> | <dl> <span data-ttu-id="a631c-117"><dt>Dvdevcode. h (include dshow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a631c-117"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a631c-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a631c-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a631c-119">Applicazioni DVD</span><span class="sxs-lookup"><span data-stu-id="a631c-119">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="a631c-120">Codici di notifica degli eventi DVD</span><span class="sxs-lookup"><span data-stu-id="a631c-120">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="a631c-121">Notifica degli eventi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="a631c-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




