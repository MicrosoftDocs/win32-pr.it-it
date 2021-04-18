---
description: Indica quando cambia il numero del titolo DVD corrente.
ms.assetid: 9888f2ec-fc2d-4d6d-a03d-b381373337eb
title: EC_DVD_TITLE_CHANGE (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_TITLE_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 9539d29704797b1c7b001d426250762d2ed27b3e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325651"
---
# <a name="ec_dvd_title_change"></a><span data-ttu-id="101e5-103">\_modifica del \_ titolo del DVD EC \_</span><span class="sxs-lookup"><span data-stu-id="101e5-103">EC\_DVD\_TITLE\_CHANGE</span></span>

<span data-ttu-id="101e5-104">Indica quando cambia il numero del titolo DVD corrente.</span><span class="sxs-lookup"><span data-stu-id="101e5-104">Indicates when the current DVD title number changes.</span></span>

## <a name="parameters"></a><span data-ttu-id="101e5-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="101e5-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="101e5-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="101e5-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="101e5-107">Valore **DWORD** che indica il nuovo numero di titolo.</span><span class="sxs-lookup"><span data-stu-id="101e5-107">**DWORD** value indicating the new title number.</span></span>

</dd> <dt>

<span data-ttu-id="101e5-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="101e5-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="101e5-109">Zero.</span><span class="sxs-lookup"><span data-stu-id="101e5-109">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="101e5-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="101e5-110">Remarks</span></span>

<span data-ttu-id="101e5-111">I numeri di titolo sono compresi tra 1 e 99.</span><span class="sxs-lookup"><span data-stu-id="101e5-111">Title numbers range from 1 to 99.</span></span> <span data-ttu-id="101e5-112">Questo numero indica il numero di TTN, ovvero il numero del titolo rispetto all'intero disco, non il TTN VTS, \_ ovvero il numero di titolo rispetto a un VTS corrente.</span><span class="sxs-lookup"><span data-stu-id="101e5-112">This number indicates the TTN, which is the title number with respect to the whole disc, not the VTS\_TTN which is the title number with respect to just a current VTS.</span></span>

<span data-ttu-id="101e5-113">Questo evento viene generato nel dominio del titolo.</span><span class="sxs-lookup"><span data-stu-id="101e5-113">This event is raised in the title domain.</span></span>

## <a name="requirements"></a><span data-ttu-id="101e5-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="101e5-114">Requirements</span></span>



| <span data-ttu-id="101e5-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="101e5-115">Requirement</span></span> | <span data-ttu-id="101e5-116">Valore</span><span class="sxs-lookup"><span data-stu-id="101e5-116">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="101e5-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="101e5-117">Header</span></span><br/> | <dl> <span data-ttu-id="101e5-118"><dt>Dvdevcode. h (include dshow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="101e5-118"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="101e5-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="101e5-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="101e5-120">Applicazioni DVD</span><span class="sxs-lookup"><span data-stu-id="101e5-120">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="101e5-121">Codici di notifica degli eventi DVD</span><span class="sxs-lookup"><span data-stu-id="101e5-121">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="101e5-122">Notifica degli eventi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="101e5-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




