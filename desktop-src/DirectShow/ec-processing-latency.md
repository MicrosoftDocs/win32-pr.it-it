---
description: Indica la quantità di tempo che un componente sta prendendo per elaborare ogni campione.
ms.assetid: 84f81ee1-76d8-46fb-86ef-2500f8f4ef36
title: EC_PROCESSING_LATENCY (dshow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d97514b4d2851f619f89f42e644766d50b7d25f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324162"
---
# <a name="ec_processing_latency"></a><span data-ttu-id="c9a8d-103">\_latenza di elaborazione EC \_</span><span class="sxs-lookup"><span data-stu-id="c9a8d-103">EC\_PROCESSING\_LATENCY</span></span>

<span data-ttu-id="c9a8d-104">Indica la quantità di tempo che un componente sta prendendo per elaborare ogni campione.</span><span class="sxs-lookup"><span data-stu-id="c9a8d-104">Indicates the amount of time that a component is taking to process each sample.</span></span>

## <a name="parameters"></a><span data-ttu-id="c9a8d-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="c9a8d-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9a8d-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="c9a8d-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="c9a8d-107">(**const reference \_ Time** \* ) la quantità di tempo per l'elaborazione di ogni campione, in unità di 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="c9a8d-107">(**const REFERENCE\_TIME**\*) The amount of time to process each sample, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="c9a8d-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="c9a8d-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="c9a8d-109">Zero.</span><span class="sxs-lookup"><span data-stu-id="c9a8d-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="c9a8d-110">Azione predefinita</span><span class="sxs-lookup"><span data-stu-id="c9a8d-110">Default Action</span></span>

<span data-ttu-id="c9a8d-111">No.</span><span class="sxs-lookup"><span data-stu-id="c9a8d-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9a8d-112">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="c9a8d-112">Remarks</span></span>

<span data-ttu-id="c9a8d-113">Un presentatore per il filtro EVR ( [**Enhanced video renderer**](enhanced-video-renderer-filter.md) ) può inviare questo messaggio al EVR per inviare una notifica a EVR sulla latenza di elaborazione del relatore.</span><span class="sxs-lookup"><span data-stu-id="c9a8d-113">A presenter for the [**Enhanced Video Renderer**](enhanced-video-renderer-filter.md) (EVR) filter can send this message to the EVR to notify the EVR about the presenter's processing latency.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9a8d-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c9a8d-114">Requirements</span></span>



| <span data-ttu-id="c9a8d-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9a8d-115">Requirement</span></span> | <span data-ttu-id="c9a8d-116">Valore</span><span class="sxs-lookup"><span data-stu-id="c9a8d-116">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c9a8d-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c9a8d-117">Header</span></span><br/> | <dl> <span data-ttu-id="c9a8d-118"><dt>Dshow. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9a8d-118"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9a8d-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c9a8d-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9a8d-120">Codici di notifica degli eventi</span><span class="sxs-lookup"><span data-stu-id="c9a8d-120">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="c9a8d-121">Notifica degli eventi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="c9a8d-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




