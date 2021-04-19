---
description: Indica che la riproduzione DVD è stata arrestata. Questo evento viene inviato quando un titolo o un capitolo viene completato e il navigatore DVD non trova altre istruzioni di branching per la riproduzione successiva. L'evento non viene inviato quando l'applicazione interrompe la riproduzione.
ms.assetid: c8617307-d70e-48af-8e85-69105595aa10
title: EC_DVD_PLAYBACK_STOPPED (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_PLAYBACK_STOPPED
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 2304d83aea532b764777b683c57c3bdd4d5df79a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326643"
---
# <a name="ec_dvd_playback_stopped"></a><span data-ttu-id="50c50-105">\_riproduzione DVD \_ EC \_ arrestata</span><span class="sxs-lookup"><span data-stu-id="50c50-105">EC\_DVD\_PLAYBACK\_STOPPED</span></span>

<span data-ttu-id="50c50-106">Indica che la riproduzione DVD è stata arrestata.</span><span class="sxs-lookup"><span data-stu-id="50c50-106">Indicates that DVD playback has been stopped.</span></span> <span data-ttu-id="50c50-107">Questo evento viene inviato quando un titolo o un capitolo viene completato e il [navigatore DVD](dvd-navigator-filter.md) non trova altre istruzioni di branching per la riproduzione successiva.</span><span class="sxs-lookup"><span data-stu-id="50c50-107">This event is sent when a title or chapter completes and the [DVD Navigator](dvd-navigator-filter.md) does not find any other branching instruction for subsequent playback.</span></span> <span data-ttu-id="50c50-108">L'evento non viene inviato quando l'applicazione interrompe la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="50c50-108">The event is not sent when the application stops playback.</span></span>

## <a name="parameters"></a><span data-ttu-id="50c50-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="50c50-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50c50-110"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="50c50-110"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="50c50-111">Membro dell'enumerazione del [**DVD \_ PB \_ arrestato**](/previous-versions/windows/desktop/api/dvdevcod/ne-dvdevcod-dvd_pb_stopped) , che indica perché la riproduzione è stata arrestata.</span><span class="sxs-lookup"><span data-stu-id="50c50-111">A member of the [**DVD\_PB\_STOPPED**](/previous-versions/windows/desktop/api/dvdevcod/ne-dvdevcod-dvd_pb_stopped) enumeration, indicating why playback stopped.</span></span>

</dd> <dt>

<span data-ttu-id="50c50-112"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="50c50-112"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="50c50-113">Zero.</span><span class="sxs-lookup"><span data-stu-id="50c50-113">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="50c50-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="50c50-114">Remarks</span></span>

<span data-ttu-id="50c50-115">Questo evento viene generato in tutti i domini.</span><span class="sxs-lookup"><span data-stu-id="50c50-115">This event is raised in all domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="50c50-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="50c50-116">Requirements</span></span>



| <span data-ttu-id="50c50-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="50c50-117">Requirement</span></span> | <span data-ttu-id="50c50-118">Valore</span><span class="sxs-lookup"><span data-stu-id="50c50-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50c50-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="50c50-119">Header</span></span><br/> | <dl> <span data-ttu-id="50c50-120"><dt>Dvdevcode. h (include dshow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="50c50-120"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50c50-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="50c50-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50c50-122">Applicazioni DVD</span><span class="sxs-lookup"><span data-stu-id="50c50-122">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="50c50-123">Codici di notifica degli eventi DVD</span><span class="sxs-lookup"><span data-stu-id="50c50-123">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="50c50-124">Notifica degli eventi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="50c50-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




