---
description: Indica il nuovo dominio del lettore DVD.
ms.assetid: 4faa46d6-2ba2-44a3-b237-acac3b32f8b1
title: EC_DVD_DOMAIN_CHANGE (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_DOMAIN_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 815b6b2dd318d0b7716f4cf640ef3f83dacd0d60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326658"
---
# <a name="ec_dvd_domain_change"></a><span data-ttu-id="c2d1a-103">\_ \_ Modifica dominio DVD \_ EC</span><span class="sxs-lookup"><span data-stu-id="c2d1a-103">EC\_DVD\_DOMAIN\_CHANGE</span></span>

<span data-ttu-id="c2d1a-104">Indica il nuovo dominio del lettore DVD.</span><span class="sxs-lookup"><span data-stu-id="c2d1a-104">Indicates the DVD player's new domain.</span></span>

## <a name="parameters"></a><span data-ttu-id="c2d1a-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="c2d1a-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2d1a-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="c2d1a-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="c2d1a-107">Valore **DWORD** che indica il nuovo dominio.</span><span class="sxs-lookup"><span data-stu-id="c2d1a-107">**DWORD** value indicating the new domain.</span></span> <span data-ttu-id="c2d1a-108">Membro del tipo di dati enumerato del [**\_ dominio DVD**](/windows/win32/api/strmif/ne-strmif-dvd_domain) .</span><span class="sxs-lookup"><span data-stu-id="c2d1a-108">Member of the [**DVD\_DOMAIN**](/windows/win32/api/strmif/ne-strmif-dvd_domain) enumerated data type.</span></span>

</dd> <dt>

<span data-ttu-id="c2d1a-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="c2d1a-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="c2d1a-110">Zero.</span><span class="sxs-lookup"><span data-stu-id="c2d1a-110">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c2d1a-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="c2d1a-111">Remarks</span></span>

<span data-ttu-id="c2d1a-112">Il lettore DVD segnala questo evento ogni volta che cambia dominio.</span><span class="sxs-lookup"><span data-stu-id="c2d1a-112">The DVD player signals this event whenever it changes domains.</span></span>

<span data-ttu-id="c2d1a-113">Questo evento viene generato in tutti i domini DVD.</span><span class="sxs-lookup"><span data-stu-id="c2d1a-113">This event is raised in all DVD domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2d1a-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c2d1a-114">Requirements</span></span>



| <span data-ttu-id="c2d1a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2d1a-115">Requirement</span></span> | <span data-ttu-id="c2d1a-116">Valore</span><span class="sxs-lookup"><span data-stu-id="c2d1a-116">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2d1a-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c2d1a-117">Header</span></span><br/> | <dl> <span data-ttu-id="c2d1a-118"><dt>Dvdevcode. h (include dshow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c2d1a-118"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2d1a-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c2d1a-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2d1a-120">Applicazioni DVD</span><span class="sxs-lookup"><span data-stu-id="c2d1a-120">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="c2d1a-121">Codici di notifica degli eventi DVD</span><span class="sxs-lookup"><span data-stu-id="c2d1a-121">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="c2d1a-122">Notifica degli eventi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="c2d1a-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




