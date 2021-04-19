---
description: Indica che il navigatore DVD ha iniziato a riprodurre i dati del karaoke o ha terminato la riproduzione.
ms.assetid: 910bf809-a56a-4d02-9c7e-429769a4ec2b
title: EC_DVD_KARAOKE_MODE (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_KARAOKE_MODE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: fb83bc1de9c2933b53935c056b192eca74c4245c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326656"
---
# <a name="ec_dvd_karaoke_mode"></a><span data-ttu-id="36ab6-103">\_ \_ modalità Karaoke DVD \_ EC</span><span class="sxs-lookup"><span data-stu-id="36ab6-103">EC\_DVD\_KARAOKE\_MODE</span></span>

<span data-ttu-id="36ab6-104">Indica che il [navigatore DVD](data-flow-in-the-dvd-navigator.md) ha iniziato a riprodurre i dati del karaoke o ha terminato la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="36ab6-104">Indicates that the [DVD Navigator](data-flow-in-the-dvd-navigator.md) has either begun playing or finished playing karaoke data.</span></span>

## <a name="parameters"></a><span data-ttu-id="36ab6-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="36ab6-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36ab6-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="36ab6-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="36ab6-107">.</span><span class="sxs-lookup"><span data-stu-id="36ab6-107">Boolean value.</span></span> <span data-ttu-id="36ab6-108">Se **true**, viene riprodotta una traccia del karaoke.</span><span class="sxs-lookup"><span data-stu-id="36ab6-108">If **TRUE**, a karaoke track is being played.</span></span> <span data-ttu-id="36ab6-109">In caso contrario, non viene eseguita alcuna traccia del karaoke.</span><span class="sxs-lookup"><span data-stu-id="36ab6-109">Otherwise, no karaoke track is being played.</span></span>

</dd> <dt>

<span data-ttu-id="36ab6-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="36ab6-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="36ab6-111">Riservato.</span><span class="sxs-lookup"><span data-stu-id="36ab6-111">Reserved.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="36ab6-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="36ab6-112">Remarks</span></span>

<span data-ttu-id="36ab6-113">Il lettore DVD segnala questo evento ogni volta che cambia dominio.</span><span class="sxs-lookup"><span data-stu-id="36ab6-113">The DVD player signals this event whenever it changes domains.</span></span>

<span data-ttu-id="36ab6-114">Questo evento viene generato in tutti i domini DVD.</span><span class="sxs-lookup"><span data-stu-id="36ab6-114">This event is raised in all DVD domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="36ab6-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="36ab6-115">Requirements</span></span>



| <span data-ttu-id="36ab6-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="36ab6-116">Requirement</span></span> | <span data-ttu-id="36ab6-117">Valore</span><span class="sxs-lookup"><span data-stu-id="36ab6-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36ab6-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="36ab6-118">Header</span></span><br/> | <dl> <span data-ttu-id="36ab6-119"><dt>Dvdevcode. h (include dshow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="36ab6-119"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36ab6-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="36ab6-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36ab6-121">Applicazioni DVD</span><span class="sxs-lookup"><span data-stu-id="36ab6-121">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="36ab6-122">Codici di notifica degli eventi DVD</span><span class="sxs-lookup"><span data-stu-id="36ab6-122">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="36ab6-123">Notifica degli eventi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="36ab6-123">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




