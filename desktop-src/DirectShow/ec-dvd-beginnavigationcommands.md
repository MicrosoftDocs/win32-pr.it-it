---
description: Inviato quando viene avviato un set di comandi di spostamento su DVD.
ms.assetid: 9cdcb211-a9e3-4a15-81bd-7ada2b9d823a
title: EC_DVD_BeginNavigationCommands (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_BeginNavigationCommands
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: cda904c4fcc0b1acdd16c8fc4596eef332140ec4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331286"
---
# <a name="ec_dvd_beginnavigationcommands"></a><span data-ttu-id="b20b8-103">\_BeginNavigationCommands DVD \_ EC</span><span class="sxs-lookup"><span data-stu-id="b20b8-103">EC\_DVD\_BeginNavigationCommands</span></span>

<span data-ttu-id="b20b8-104">Inviato quando viene avviato un set di comandi di spostamento su DVD.</span><span class="sxs-lookup"><span data-stu-id="b20b8-104">Sent when a set of DVD navigation commands are starting.</span></span>

## <a name="parameters"></a><span data-ttu-id="b20b8-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="b20b8-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b20b8-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="b20b8-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="b20b8-107">Valore dell'enumerazione [**\_ NavCmdType DVD**](/windows/win32/api/strmif/ne-strmif-dvd_navcmdtype) .</span><span class="sxs-lookup"><span data-stu-id="b20b8-107">A value from the [**DVD\_NavCmdType**](/windows/win32/api/strmif/ne-strmif-dvd_navcmdtype) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="b20b8-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="b20b8-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="b20b8-109">Zero.</span><span class="sxs-lookup"><span data-stu-id="b20b8-109">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b20b8-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="b20b8-110">Remarks</span></span>

<span data-ttu-id="b20b8-111">Questo evento è disabilitato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="b20b8-111">This event is disabled by default.</span></span> <span data-ttu-id="b20b8-112">Per abilitare questo evento, chiamare [**IDVDControl2:: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) e impostare l'opzione **DVD \_ EnableLoggingEvents** su **true**.</span><span class="sxs-lookup"><span data-stu-id="b20b8-112">To enable this event, call [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) and set the **DVD\_EnableLoggingEvents** option to **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="b20b8-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b20b8-113">Requirements</span></span>



| <span data-ttu-id="b20b8-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="b20b8-114">Requirement</span></span> | <span data-ttu-id="b20b8-115">Valore</span><span class="sxs-lookup"><span data-stu-id="b20b8-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b20b8-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b20b8-116">Header</span></span><br/> | <dl> <span data-ttu-id="b20b8-117"><dt>Dvdevcode. h (include dshow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b20b8-117"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b20b8-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b20b8-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b20b8-119">Applicazioni DVD</span><span class="sxs-lookup"><span data-stu-id="b20b8-119">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="b20b8-120">Codici di notifica degli eventi DVD</span><span class="sxs-lookup"><span data-stu-id="b20b8-120">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="b20b8-121">Notifica degli eventi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="b20b8-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




