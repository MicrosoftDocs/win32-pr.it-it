---
description: Inviato quando il navigatore DVD analizza un pacchetto PCI.
ms.assetid: e2e65007-7c34-4be4-86b9-9491061891e5
title: EC_DVD_VOBU_Offset (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_VOBU_Offset
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 531207d4d8b0debb29dd5d02e01e400218e4a2bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325647"
---
# <a name="ec_dvd_vobu_offset"></a><span data-ttu-id="2a713-103">\_ \_ Offset VOBU DVD \_ EC</span><span class="sxs-lookup"><span data-stu-id="2a713-103">EC\_DVD\_VOBU\_Offset</span></span>

<span data-ttu-id="2a713-104">Inviato quando il [navigatore DVD](dvd-navigator-filter.md) analizza un pacchetto PCI.</span><span class="sxs-lookup"><span data-stu-id="2a713-104">Sent when the [DVD Navigator](dvd-navigator-filter.md) parses a PCI packet.</span></span>

## <a name="parameters"></a><span data-ttu-id="2a713-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="2a713-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a713-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="2a713-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="2a713-107">Offset di blocco della VOBU (video Object Unit) più recente.</span><span class="sxs-lookup"><span data-stu-id="2a713-107">The block offset of the most recent video object unit (VOBU).</span></span>

</dd> <dt>

<span data-ttu-id="2a713-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="2a713-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="2a713-109">Il numero di set del titolo del video corrente (VTSN).</span><span class="sxs-lookup"><span data-stu-id="2a713-109">The current video title set number (VTSN).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2a713-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="2a713-110">Remarks</span></span>

<span data-ttu-id="2a713-111">Questo evento è disabilitato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="2a713-111">This event is disabled by default.</span></span> <span data-ttu-id="2a713-112">Per abilitare questo evento, chiamare [**IDVDControl2:: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) e impostare l'opzione **DVD \_ EnableLoggingEvents** su **true**.</span><span class="sxs-lookup"><span data-stu-id="2a713-112">To enable this event, call [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) and set the **DVD\_EnableLoggingEvents** option to **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a713-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2a713-113">Requirements</span></span>



| <span data-ttu-id="2a713-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a713-114">Requirement</span></span> | <span data-ttu-id="2a713-115">Valore</span><span class="sxs-lookup"><span data-stu-id="2a713-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a713-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2a713-116">Header</span></span><br/> | <dl> <span data-ttu-id="2a713-117"><dt>Dvdevcode. h (include dshow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2a713-117"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a713-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2a713-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a713-119">Applicazioni DVD</span><span class="sxs-lookup"><span data-stu-id="2a713-119">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="2a713-120">Codici di notifica degli eventi DVD</span><span class="sxs-lookup"><span data-stu-id="2a713-120">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="2a713-121">Notifica degli eventi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="2a713-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




