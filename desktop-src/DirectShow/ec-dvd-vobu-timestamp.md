---
description: Inviato quando il navigatore DVD analizza un pacchetto PCI.
ms.assetid: 25548c23-22f0-47cb-9062-273ad39d3007
title: EC_DVD_VOBU_Timestamp (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_VOBU_Timestamp
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 762a900a83154ce38ee00fcf4173ebc32b41cf30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325646"
---
# <a name="ec_dvd_vobu_timestamp"></a><span data-ttu-id="9f602-103">\_ \_ Timestamp VOBU DVD \_ EC</span><span class="sxs-lookup"><span data-stu-id="9f602-103">EC\_DVD\_VOBU\_Timestamp</span></span>

<span data-ttu-id="9f602-104">Inviato quando il [navigatore DVD](dvd-navigator-filter.md) analizza un pacchetto PCI.</span><span class="sxs-lookup"><span data-stu-id="9f602-104">Sent when the [DVD Navigator](dvd-navigator-filter.md) parses a PCI packet.</span></span>

<span data-ttu-id="9f602-105">I dati dell'evento corrispondono al timestamp della VOBU (video Object Unit) più recente.</span><span class="sxs-lookup"><span data-stu-id="9f602-105">The event data is the time stamp of the most recent video object unit (VOBU).</span></span>

## <a name="parameters"></a><span data-ttu-id="9f602-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9f602-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f602-107"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="9f602-107"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="9f602-108">Contiene il **valore DWORD** di ordine inferiore del timestamp.</span><span class="sxs-lookup"><span data-stu-id="9f602-108">Contains the low-order **DWORD** of the time stamp.</span></span>

</dd> <dt>

<span data-ttu-id="9f602-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="9f602-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="9f602-110">Contiene il **valore DWORD** di ordine superiore del timestamp.</span><span class="sxs-lookup"><span data-stu-id="9f602-110">Contains the high-order **DWORD** of the time stamp.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9f602-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="9f602-111">Remarks</span></span>

<span data-ttu-id="9f602-112">Questo evento è disabilitato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="9f602-112">This event is disabled by default.</span></span> <span data-ttu-id="9f602-113">Per abilitare questo evento, chiamare [**IDVDControl2:: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) e impostare l'opzione **DVD \_ EnableLoggingEvents** su **true**.</span><span class="sxs-lookup"><span data-stu-id="9f602-113">To enable this event, call [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) and set the **DVD\_EnableLoggingEvents** option to **TRUE**.</span></span>

<span data-ttu-id="9f602-114">Ricostruire l'indicatore di data e ora come segue:</span><span class="sxs-lookup"><span data-stu-id="9f602-114">Reconstruct the time stamp as follows:</span></span>


```C++
LARGE_INTEGER li;
li.LowPart = DWORD( lParam1 );
li.HighPart = DWORD( lParam2 );
```



## <a name="requirements"></a><span data-ttu-id="9f602-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9f602-115">Requirements</span></span>



| <span data-ttu-id="9f602-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f602-116">Requirement</span></span> | <span data-ttu-id="9f602-117">Valore</span><span class="sxs-lookup"><span data-stu-id="9f602-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f602-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9f602-118">Header</span></span><br/> | <dl> <span data-ttu-id="9f602-119"><dt>Dvdevcode. h (include dshow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9f602-119"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f602-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9f602-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f602-121">Applicazioni DVD</span><span class="sxs-lookup"><span data-stu-id="9f602-121">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="9f602-122">Codici di notifica degli eventi DVD</span><span class="sxs-lookup"><span data-stu-id="9f602-122">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="9f602-123">Notifica degli eventi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="9f602-123">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




