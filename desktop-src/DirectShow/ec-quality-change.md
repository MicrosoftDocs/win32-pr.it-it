---
description: Il grafico sta eliminando gli esempi per il controllo qualità.
ms.assetid: a21fe766-58a5-4851-a282-883374287e18
title: EC_QUALITY_CHANGE (dshow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5752db30c8ad6ed85655948cf2adb9ef7ac8078
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324161"
---
# <a name="ec_quality_change"></a><span data-ttu-id="f1e50-103">\_modifica della qualità EC \_</span><span class="sxs-lookup"><span data-stu-id="f1e50-103">EC\_QUALITY\_CHANGE</span></span>

<span data-ttu-id="f1e50-104">Il grafico sta eliminando gli esempi per il controllo qualità.</span><span class="sxs-lookup"><span data-stu-id="f1e50-104">The graph is dropping samples, for quality control.</span></span>

## <a name="parameters"></a><span data-ttu-id="f1e50-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="f1e50-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1e50-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="f1e50-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="f1e50-107">Zero.</span><span class="sxs-lookup"><span data-stu-id="f1e50-107">Zero.</span></span>

</dd> <dt>

<span data-ttu-id="f1e50-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="f1e50-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="f1e50-109">Zero.</span><span class="sxs-lookup"><span data-stu-id="f1e50-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="f1e50-110">Azione predefinita</span><span class="sxs-lookup"><span data-stu-id="f1e50-110">Default Action</span></span>

<span data-ttu-id="f1e50-111">No.</span><span class="sxs-lookup"><span data-stu-id="f1e50-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1e50-112">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="f1e50-112">Remarks</span></span>

<span data-ttu-id="f1e50-113">Un filtro Invia questo evento se rilascia esempi in risposta a un messaggio di controllo di qualità.</span><span class="sxs-lookup"><span data-stu-id="f1e50-113">A filter sends this event if it drops samples in response to a quality control message.</span></span> <span data-ttu-id="f1e50-114">Invia l'evento solo quando regola il livello di qualità, non per ogni campione che rilascia.</span><span class="sxs-lookup"><span data-stu-id="f1e50-114">It sends the event only when it adjusts the quality level, not for each sample that it drops.</span></span> <span data-ttu-id="f1e50-115">Per altre informazioni, vedere [gestione del controllo di qualità](quality-control-management.md).</span><span class="sxs-lookup"><span data-stu-id="f1e50-115">For more information, see [Quality-Control Management](quality-control-management.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f1e50-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f1e50-116">Requirements</span></span>



| <span data-ttu-id="f1e50-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1e50-117">Requirement</span></span> | <span data-ttu-id="f1e50-118">Valore</span><span class="sxs-lookup"><span data-stu-id="f1e50-118">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f1e50-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f1e50-119">Header</span></span><br/> | <dl> <span data-ttu-id="f1e50-120"><dt>Dshow. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1e50-120"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1e50-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f1e50-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1e50-122">Codici di notifica degli eventi</span><span class="sxs-lookup"><span data-stu-id="f1e50-122">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="f1e50-123">Notifica degli eventi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="f1e50-123">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




