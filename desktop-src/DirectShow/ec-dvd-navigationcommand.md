---
description: Inviato quando il navigatore DVD elabora un comando di spostamento DVD.
ms.assetid: 95e502b6-330f-4bc7-8adc-851913987370
title: EC_DVD_NavigationCommand (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_NavigationCommand
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: e81dbf108868cbaec4c44a436f2c8271bb5f282a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326653"
---
# <a name="ec_dvd_navigationcommand"></a><span data-ttu-id="16bd5-103">\_NavigationCommand DVD \_ EC</span><span class="sxs-lookup"><span data-stu-id="16bd5-103">EC\_DVD\_NavigationCommand</span></span>

<span data-ttu-id="16bd5-104">Inviato quando il [navigatore DVD](dvd-navigator-filter.md) elabora un comando di spostamento DVD.</span><span class="sxs-lookup"><span data-stu-id="16bd5-104">Sent when the [DVD Navigator](dvd-navigator-filter.md) processes a DVD navigation command.</span></span>

## <a name="parameters"></a><span data-ttu-id="16bd5-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="16bd5-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16bd5-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="16bd5-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="16bd5-107">Bit 32 inferiori del comando di navigazione non elaborato.</span><span class="sxs-lookup"><span data-stu-id="16bd5-107">The lower 32 bits of the raw navigation command.</span></span>

</dd> <dt>

<span data-ttu-id="16bd5-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="16bd5-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="16bd5-109">Bit 32 superiori del comando di navigazione non elaborato.</span><span class="sxs-lookup"><span data-stu-id="16bd5-109">The upper 32 bits of the raw navigation command.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="16bd5-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="16bd5-110">Remarks</span></span>

<span data-ttu-id="16bd5-111">Questo evento è disabilitato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="16bd5-111">This event is disabled by default.</span></span> <span data-ttu-id="16bd5-112">Per abilitare questo evento, chiamare [**IDVDControl2:: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) e impostare l'opzione **DVD \_ EnableLoggingEvents** su **true**.</span><span class="sxs-lookup"><span data-stu-id="16bd5-112">To enable this event, call [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) and set the **DVD\_EnableLoggingEvents** option to **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="16bd5-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="16bd5-113">Requirements</span></span>



| <span data-ttu-id="16bd5-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="16bd5-114">Requirement</span></span> | <span data-ttu-id="16bd5-115">Valore</span><span class="sxs-lookup"><span data-stu-id="16bd5-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16bd5-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="16bd5-116">Header</span></span><br/> | <dl> <span data-ttu-id="16bd5-117"><dt>Dvdevcode. h (include dshow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="16bd5-117"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16bd5-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="16bd5-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16bd5-119">Applicazioni DVD</span><span class="sxs-lookup"><span data-stu-id="16bd5-119">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="16bd5-120">Codici di notifica degli eventi DVD</span><span class="sxs-lookup"><span data-stu-id="16bd5-120">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="16bd5-121">Notifica degli eventi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="16bd5-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




