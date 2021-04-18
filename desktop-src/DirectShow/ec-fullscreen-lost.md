---
description: Il renderer video sta per uscire dalla modalità schermo intero.
ms.assetid: f720a9b6-930a-4ed7-9798-1c72fa7a11ff
title: EC_FULLSCREEN_LOST (dshow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf36b5652ea5f7cde26950a18de086af0862dac7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328626"
---
# <a name="ec_fullscreen_lost"></a><span data-ttu-id="82374-103">EC \_ FullScreen \_ perso</span><span class="sxs-lookup"><span data-stu-id="82374-103">EC\_FULLSCREEN\_LOST</span></span>

<span data-ttu-id="82374-104">Il renderer video sta per uscire dalla modalità schermo intero.</span><span class="sxs-lookup"><span data-stu-id="82374-104">The video renderer is switching out of full-screen mode.</span></span>

## <a name="parameters"></a><span data-ttu-id="82374-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="82374-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82374-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="82374-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="82374-107">Zero.</span><span class="sxs-lookup"><span data-stu-id="82374-107">Zero.</span></span>

</dd> <dt>

<span data-ttu-id="82374-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="82374-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="82374-109">(**IUnknown** \* ) Puntatore all'interfaccia [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) del renderer video o **null**.</span><span class="sxs-lookup"><span data-stu-id="82374-109">(**IUnknown**\*) Pointer to the video renderer's [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface, or **NULL**.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="82374-110">Azione predefinita</span><span class="sxs-lookup"><span data-stu-id="82374-110">Default Action</span></span>

<span data-ttu-id="82374-111">No.</span><span class="sxs-lookup"><span data-stu-id="82374-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="82374-112">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="82374-112">Remarks</span></span>

<span data-ttu-id="82374-113">Quando il [renderer a schermo intero](full-screen-renderer-filter.md) perde l'attivazione, invia questo evento.</span><span class="sxs-lookup"><span data-stu-id="82374-113">When the [Full Screen Renderer](full-screen-renderer-filter.md) loses activation, it sends this event.</span></span> <span data-ttu-id="82374-114">Quando un altro renderer video disattiva la modalità schermo intero, il gestore del grafico del filtro Invia questo evento in risposta a un evento di [**\_ attivazione EC**](ec-activate.md) dal renderer.</span><span class="sxs-lookup"><span data-stu-id="82374-114">When another video renderer switches out of full-screen mode, the filter graph manager sends this event, in response to an [**EC\_ACTIVATE**](ec-activate.md) event from the renderer.</span></span>

## <a name="requirements"></a><span data-ttu-id="82374-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="82374-115">Requirements</span></span>



| <span data-ttu-id="82374-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="82374-116">Requirement</span></span> | <span data-ttu-id="82374-117">Valore</span><span class="sxs-lookup"><span data-stu-id="82374-117">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="82374-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="82374-118">Header</span></span><br/> | <dl> <span data-ttu-id="82374-119"><dt>Dshow. h</dt></span><span class="sxs-lookup"><span data-stu-id="82374-119"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82374-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="82374-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82374-121">Codici di notifica degli eventi</span><span class="sxs-lookup"><span data-stu-id="82374-121">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="82374-122">Notifica degli eventi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="82374-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




