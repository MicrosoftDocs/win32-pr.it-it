---
description: Il provider Clock è stato disconnesso.
ms.assetid: 0a885b7a-840d-4112-85f7-ff6f2d87bb75
title: EC_CLOCK_UNSET (dshow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85ead35d89eee94bbffb38a96f658ccb2bb6e6e4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328466"
---
# <a name="ec_clock_unset"></a><span data-ttu-id="47b4c-103">orologio EC non \_ \_ impostato</span><span class="sxs-lookup"><span data-stu-id="47b4c-103">EC\_CLOCK\_UNSET</span></span>

<span data-ttu-id="47b4c-104">Il provider Clock è stato disconnesso.</span><span class="sxs-lookup"><span data-stu-id="47b4c-104">The clock provider was disconnected.</span></span>

## <a name="parameters"></a><span data-ttu-id="47b4c-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="47b4c-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47b4c-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="47b4c-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="47b4c-107">Zero.</span><span class="sxs-lookup"><span data-stu-id="47b4c-107">Zero.</span></span>

</dd> <dt>

<span data-ttu-id="47b4c-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="47b4c-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="47b4c-109">Zero.</span><span class="sxs-lookup"><span data-stu-id="47b4c-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="47b4c-110">Azione predefinita</span><span class="sxs-lookup"><span data-stu-id="47b4c-110">Default Action</span></span>

<span data-ttu-id="47b4c-111">Il gestore del grafico del filtro sceglie un nuovo Clock di riferimento al successivo comando Sospendi o Esegui.</span><span class="sxs-lookup"><span data-stu-id="47b4c-111">The Filter Graph Manager chooses a new reference clock on the next pause or run command.</span></span> <span data-ttu-id="47b4c-112">Inoltre, l'evento viene inviato all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="47b4c-112">It also forwards the event to the application.</span></span>

## <a name="remarks"></a><span data-ttu-id="47b4c-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="47b4c-113">Remarks</span></span>

<span data-ttu-id="47b4c-114">KSProxy segnala questo evento quando il pin di un filtro che fornisce un clock è disconnesso.</span><span class="sxs-lookup"><span data-stu-id="47b4c-114">KSProxy signals this event when the pin of a clock-providing filter is disconnected.</span></span>

## <a name="requirements"></a><span data-ttu-id="47b4c-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="47b4c-115">Requirements</span></span>



| <span data-ttu-id="47b4c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="47b4c-116">Requirement</span></span> | <span data-ttu-id="47b4c-117">Valore</span><span class="sxs-lookup"><span data-stu-id="47b4c-117">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="47b4c-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="47b4c-118">Header</span></span><br/> | <dl> <span data-ttu-id="47b4c-119"><dt>Dshow. h</dt></span><span class="sxs-lookup"><span data-stu-id="47b4c-119"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47b4c-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="47b4c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47b4c-121">Codici di notifica degli eventi</span><span class="sxs-lookup"><span data-stu-id="47b4c-121">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="47b4c-122">Notifica degli eventi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="47b4c-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




