---
description: Inviato quando VMR ha selezionato il meccanismo di rendering.
ms.assetid: 815d1254-c6e3-4a6c-ba4a-bf3da7d35d1f
title: EC_VMR_RENDERDEVICE_SET (dshow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9855b23e25a2c3b955c1499b9505efffcc5637e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329482"
---
# <a name="ec_vmr_renderdevice_set"></a><span data-ttu-id="7ac5e-103">\_set di \_ RENDERDEVICE \_ VMR EC</span><span class="sxs-lookup"><span data-stu-id="7ac5e-103">EC\_VMR\_RENDERDEVICE\_SET</span></span>

<span data-ttu-id="7ac5e-104">Inviato quando VMR ha selezionato il meccanismo di rendering.</span><span class="sxs-lookup"><span data-stu-id="7ac5e-104">Sent when the VMR has selected its rendering mechanism.</span></span>

## <a name="parameters"></a><span data-ttu-id="7ac5e-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="7ac5e-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ac5e-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="7ac5e-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="7ac5e-107">Può essere uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="7ac5e-107">May be one of the following values:</span></span>



| <span data-ttu-id="7ac5e-108">Valore</span><span class="sxs-lookup"><span data-stu-id="7ac5e-108">Value</span></span>                        | <span data-ttu-id="7ac5e-109">Significato</span><span class="sxs-lookup"><span data-stu-id="7ac5e-109">Meaning</span></span>                                                  |
|------------------------------|----------------------------------------------------------|
| <span data-ttu-id="7ac5e-110">\_ \_ sovrimpressione del dispositivo di rendering VMR \_</span><span class="sxs-lookup"><span data-stu-id="7ac5e-110">VMR\_RENDER\_DEVICE\_OVERLAY</span></span> | <span data-ttu-id="7ac5e-111">VMR eseguirà il rendering nella superficie della sovrimpressione (solo VMR-7).</span><span class="sxs-lookup"><span data-stu-id="7ac5e-111">The VMR will render to the overlay surface (VMR-7 only).</span></span> |
| <span data-ttu-id="7ac5e-112">\_VIDMEM del \_ dispositivo di rendering VMR \_</span><span class="sxs-lookup"><span data-stu-id="7ac5e-112">VMR\_RENDER\_DEVICE\_VIDMEM</span></span>  | <span data-ttu-id="7ac5e-113">Il VMR eseguirà il rendering nella memoria video.</span><span class="sxs-lookup"><span data-stu-id="7ac5e-113">The VMR will render to video memory.</span></span>                     |
| <span data-ttu-id="7ac5e-114">\_SYSMEM del \_ dispositivo di rendering VMR \_</span><span class="sxs-lookup"><span data-stu-id="7ac5e-114">VMR\_RENDER\_DEVICE\_SYSMEM</span></span>  | <span data-ttu-id="7ac5e-115">Il VMR eseguirà il rendering nella memoria di sistema (solo VMR-7).</span><span class="sxs-lookup"><span data-stu-id="7ac5e-115">The VMR will render to system memory (VMR-7 only).</span></span>       |



 

</dd> <dt>

<span data-ttu-id="7ac5e-116"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="7ac5e-116"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="7ac5e-117">Non usato.</span><span class="sxs-lookup"><span data-stu-id="7ac5e-117">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7ac5e-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="7ac5e-118">Remarks</span></span>

<span data-ttu-id="7ac5e-119">Questo evento viene inviato sia da VMR-7 che da VMR-9 e viene inoltrato alle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="7ac5e-119">This event is sent by both the VMR-7 and the VMR-9 and it is forwarded to applications.</span></span> <span data-ttu-id="7ac5e-120">Si noti che VMR-9 supporta solo le destinazioni di rendering della memoria video.</span><span class="sxs-lookup"><span data-stu-id="7ac5e-120">Note that the VMR-9 only supports video memory render targets.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ac5e-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7ac5e-121">Requirements</span></span>



| <span data-ttu-id="7ac5e-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ac5e-122">Requirement</span></span> | <span data-ttu-id="7ac5e-123">Valore</span><span class="sxs-lookup"><span data-stu-id="7ac5e-123">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7ac5e-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7ac5e-124">Header</span></span><br/> | <dl> <span data-ttu-id="7ac5e-125"><dt>Dshow. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ac5e-125"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ac5e-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7ac5e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ac5e-127">Codici di notifica degli eventi</span><span class="sxs-lookup"><span data-stu-id="7ac5e-127">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="7ac5e-128">Notifica degli eventi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="7ac5e-128">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




