---
description: Inviato quando il numero del programma DVD o il numero di cella cambia.
ms.assetid: a500e86d-cd42-4716-9c57-828a72c4e1df
title: EC_DVD_PROGRAM_CELL_CHANGE (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_PROGRAM_CELL_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: d41f691016c3e41cfc3e14ed1ce6fff276dcc70e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325656"
---
# <a name="ec_dvd_program_cell_change"></a><span data-ttu-id="1e540-103">\_ \_ \_ modifica cella programma DVD \_ EC</span><span class="sxs-lookup"><span data-stu-id="1e540-103">EC\_DVD\_PROGRAM\_CELL\_CHANGE</span></span>

<span data-ttu-id="1e540-104">Inviato quando il numero del programma DVD o il numero di cella cambia.</span><span class="sxs-lookup"><span data-stu-id="1e540-104">Sent when the DVD program number or cell number changes.</span></span>

## <a name="parameters"></a><span data-ttu-id="1e540-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="1e540-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e540-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="1e540-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="1e540-107">Nuovo numero di programma.</span><span class="sxs-lookup"><span data-stu-id="1e540-107">The new program number.</span></span>

</dd> <dt>

<span data-ttu-id="1e540-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="1e540-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="1e540-109">Nuovo numero di cella.</span><span class="sxs-lookup"><span data-stu-id="1e540-109">The new cell number.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1e540-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="1e540-110">Remarks</span></span>

<span data-ttu-id="1e540-111">Questo evento è disabilitato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="1e540-111">This event is disabled by default.</span></span> <span data-ttu-id="1e540-112">Per abilitare questo evento, chiamare [**IDVDControl2:: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) e impostare l'opzione **DVD \_ NotifyPositionChange** su **true**.</span><span class="sxs-lookup"><span data-stu-id="1e540-112">To enable this event, call [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) and set the **DVD\_NotifyPositionChange** option to **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e540-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1e540-113">Requirements</span></span>



| <span data-ttu-id="1e540-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e540-114">Requirement</span></span> | <span data-ttu-id="1e540-115">Valore</span><span class="sxs-lookup"><span data-stu-id="1e540-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e540-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1e540-116">Header</span></span><br/> | <dl> <span data-ttu-id="1e540-117"><dt>Dvdevcode. h (include dshow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1e540-117"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e540-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1e540-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e540-119">Applicazioni DVD</span><span class="sxs-lookup"><span data-stu-id="1e540-119">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="1e540-120">Codici di notifica degli eventi DVD</span><span class="sxs-lookup"><span data-stu-id="1e540-120">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="1e540-121">Notifica degli eventi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="1e540-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




