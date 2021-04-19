---
description: Inviato quando cambia il set di titoli video corrente (VTS).
ms.assetid: 7b8849c8-c71e-44d6-b33a-8e80247bdb22
title: EC_DVD_TITLE_SET_CHANGE (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_TITLE_SET_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: c5685cfb909a7fa24c39dff969076269845a663e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326631"
---
# <a name="ec_dvd_title_set_change"></a><span data-ttu-id="7082b-103">\_modifica del \_ set di titoli del DVD EC \_ \_</span><span class="sxs-lookup"><span data-stu-id="7082b-103">EC\_DVD\_TITLE\_SET\_CHANGE</span></span>

<span data-ttu-id="7082b-104">Inviato quando cambia il set di titoli video corrente (VTS).</span><span class="sxs-lookup"><span data-stu-id="7082b-104">Sent when current Video Title Set (VTS) changes.</span></span>

## <a name="parameters"></a><span data-ttu-id="7082b-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="7082b-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7082b-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="7082b-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="7082b-107">Il nuovo numero di set del titolo video (VTSN).</span><span class="sxs-lookup"><span data-stu-id="7082b-107">The new Video Title Set Number (VTSN).</span></span>

</dd> <dt>

<span data-ttu-id="7082b-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="7082b-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="7082b-109">Zero.</span><span class="sxs-lookup"><span data-stu-id="7082b-109">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7082b-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="7082b-110">Remarks</span></span>

<span data-ttu-id="7082b-111">Questo evento è disabilitato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="7082b-111">This event is disabled by default.</span></span> <span data-ttu-id="7082b-112">Per abilitare questo evento, chiamare [**IDVDControl2:: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) e impostare l'opzione **DVD \_ NotifyPositionChange** su **true**.</span><span class="sxs-lookup"><span data-stu-id="7082b-112">To enable this event, call [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) and set the **DVD\_NotifyPositionChange** option to **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="7082b-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7082b-113">Requirements</span></span>



| <span data-ttu-id="7082b-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="7082b-114">Requirement</span></span> | <span data-ttu-id="7082b-115">Valore</span><span class="sxs-lookup"><span data-stu-id="7082b-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7082b-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7082b-116">Header</span></span><br/> | <dl> <span data-ttu-id="7082b-117"><dt>Dvdevcode. h (include dshow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7082b-117"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7082b-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7082b-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7082b-119">Applicazioni DVD</span><span class="sxs-lookup"><span data-stu-id="7082b-119">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="7082b-120">Codici di notifica degli eventi DVD</span><span class="sxs-lookup"><span data-stu-id="7082b-120">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="7082b-121">Notifica degli eventi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="7082b-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




