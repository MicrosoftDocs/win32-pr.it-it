---
description: Un filtro non riceve dati sufficienti.
ms.assetid: c9cdfe46-02bb-4ea9-ac58-7d63e03c26d8
title: EC_STARVATION (dshow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 988d550b93ecb9a3c2f78f2d07f50a3965be945d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324647"
---
# <a name="ec_starvation"></a><span data-ttu-id="76d1d-103">scadenza \_ EC</span><span class="sxs-lookup"><span data-stu-id="76d1d-103">EC\_STARVATION</span></span>

<span data-ttu-id="76d1d-104">Un filtro non riceve dati sufficienti.</span><span class="sxs-lookup"><span data-stu-id="76d1d-104">A filter is not receiving enough data.</span></span>

## <a name="parameters"></a><span data-ttu-id="76d1d-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="76d1d-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76d1d-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="76d1d-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="76d1d-107">Zero.</span><span class="sxs-lookup"><span data-stu-id="76d1d-107">Zero.</span></span>

</dd> <dt>

<span data-ttu-id="76d1d-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="76d1d-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="76d1d-109">Zero.</span><span class="sxs-lookup"><span data-stu-id="76d1d-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="76d1d-110">Azione predefinita</span><span class="sxs-lookup"><span data-stu-id="76d1d-110">Default Action</span></span>

<span data-ttu-id="76d1d-111">L'evento non viene inviato all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="76d1d-111">The event is not sent to the application.</span></span> <span data-ttu-id="76d1d-112">Se il grafico del filtro è in esecuzione, il gestore del grafico del filtro sospende il grafico e attende il completamento della sospensione.</span><span class="sxs-lookup"><span data-stu-id="76d1d-112">If the filter graph is running, the filter graph manager pauses the graph and waits for the pause to complete.</span></span> <span data-ttu-id="76d1d-113">Quindi esegue di nuovo il grafico.</span><span class="sxs-lookup"><span data-stu-id="76d1d-113">Then it runs the graph again.</span></span> <span data-ttu-id="76d1d-114">Il filtro che invia l'evento non deve completare la transizione alla sospensione fino a quando non dispone di dati sufficienti da riprendere.</span><span class="sxs-lookup"><span data-stu-id="76d1d-114">The filter sending the event should not complete its transition to paused until it has enough data to resume.</span></span> <span data-ttu-id="76d1d-115">Se il grafico del filtro non è in esecuzione, il gestore del grafico del filtro ignorerà questo evento.</span><span class="sxs-lookup"><span data-stu-id="76d1d-115">If the filter graph is not running, the filter graph manager ignores this event.</span></span>

## <a name="remarks"></a><span data-ttu-id="76d1d-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="76d1d-116">Remarks</span></span>

<span data-ttu-id="76d1d-117">Un parser o un filtro di origine può inviare questo evento se sono in arrivo dati troppo piccoli.</span><span class="sxs-lookup"><span data-stu-id="76d1d-117">A parser or source filter can send this event if too little data is arriving.</span></span>

## <a name="requirements"></a><span data-ttu-id="76d1d-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="76d1d-118">Requirements</span></span>



| <span data-ttu-id="76d1d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="76d1d-119">Requirement</span></span> | <span data-ttu-id="76d1d-120">Valore</span><span class="sxs-lookup"><span data-stu-id="76d1d-120">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="76d1d-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="76d1d-121">Header</span></span><br/> | <dl> <span data-ttu-id="76d1d-122"><dt>Dshow. h</dt></span><span class="sxs-lookup"><span data-stu-id="76d1d-122"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76d1d-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="76d1d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76d1d-124">Codici di notifica degli eventi</span><span class="sxs-lookup"><span data-stu-id="76d1d-124">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="76d1d-125">Notifica degli eventi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="76d1d-125">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




