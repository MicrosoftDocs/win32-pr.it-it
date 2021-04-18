---
description: Inviato quando il relatore dell'allocatore VMR-7 ha chiamato il metodo di capovolgimento DirectDraw sulla superficie visualizzata. In questo modo, VMR mantiene la tabella DirectXVA delle superfici sincronizzate con la catena di capovolgimento di DirectDraw.
ms.assetid: e298857b-0579-48b4-add0-72320bc52d63
title: EC_VMR_SURFACE_FLIPPED (dshow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1feafaa58f0cacdafde04591d494dbb9a9eb258e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329480"
---
# <a name="ec_vmr_surface_flipped"></a><span data-ttu-id="06833-104">\_superficie VMR \_ EC \_ capovolta</span><span class="sxs-lookup"><span data-stu-id="06833-104">EC\_VMR\_SURFACE\_FLIPPED</span></span>

<span data-ttu-id="06833-105">Inviato quando il relatore dell'allocatore VMR-7 ha chiamato il metodo di capovolgimento DirectDraw sulla superficie visualizzata.</span><span class="sxs-lookup"><span data-stu-id="06833-105">Sent when the VMR-7's allocator presenter has called the DirectDraw Flip method on the surface being presented.</span></span> <span data-ttu-id="06833-106">In questo modo, VMR mantiene la tabella DirectXVA delle superfici sincronizzate con la catena di capovolgimento di DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="06833-106">This allows the VMR to keep its DirectXVA table of surfaces synchronized with DirectDraw's flipping chain.</span></span>

## <a name="parameters"></a><span data-ttu-id="06833-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="06833-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06833-108"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="06833-108"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="06833-109">(**HRESULT**) Codice di stato restituito dal metodo di capovolgimento DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="06833-109">(**HRESULT**) Status code returned from the DirectDraw Flip method.</span></span>

</dd> <dt>

<span data-ttu-id="06833-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="06833-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="06833-111">Non usato.</span><span class="sxs-lookup"><span data-stu-id="06833-111">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="06833-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="06833-112">Remarks</span></span>

<span data-ttu-id="06833-113">Allocator-Presenter personalizzato per VMR-7 deve inviare questo evento.</span><span class="sxs-lookup"><span data-stu-id="06833-113">Custom allocator-presenters for the VMR-7 should send this event.</span></span> <span data-ttu-id="06833-114">Questo evento non viene inviato alle applicazioni e non viene usato con Allocator-Presenter per VMR-9.</span><span class="sxs-lookup"><span data-stu-id="06833-114">This event is not forwarded to applications and it is not used with allocator-presenters for the VMR-9.</span></span>

## <a name="requirements"></a><span data-ttu-id="06833-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="06833-115">Requirements</span></span>



| <span data-ttu-id="06833-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="06833-116">Requirement</span></span> | <span data-ttu-id="06833-117">Valore</span><span class="sxs-lookup"><span data-stu-id="06833-117">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="06833-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="06833-118">Header</span></span><br/> | <dl> <span data-ttu-id="06833-119"><dt>Dshow. h</dt></span><span class="sxs-lookup"><span data-stu-id="06833-119"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06833-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="06833-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06833-121">Codici di notifica degli eventi</span><span class="sxs-lookup"><span data-stu-id="06833-121">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="06833-122">Notifica degli eventi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="06833-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




