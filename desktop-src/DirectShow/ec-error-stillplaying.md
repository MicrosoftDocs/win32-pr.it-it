---
description: Un comando asincrono per eseguire il grafo non è riuscito.
ms.assetid: 0bfcf4b4-b35a-4593-9956-8e1e8c9139cb
title: EC_ERROR_STILLPLAYING (dshow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d1c99db8c6b332ad4531f04171d960c5cfa9824
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325183"
---
# <a name="ec_error_stillplaying"></a><span data-ttu-id="dcd4b-103">\_STILLPLAYING errore \_ EC</span><span class="sxs-lookup"><span data-stu-id="dcd4b-103">EC\_ERROR\_STILLPLAYING</span></span>

<span data-ttu-id="dcd4b-104">Un comando asincrono per eseguire il grafo non è riuscito.</span><span class="sxs-lookup"><span data-stu-id="dcd4b-104">An asynchronous command to run the graph has failed.</span></span>

## <a name="parameters"></a><span data-ttu-id="dcd4b-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="dcd4b-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dcd4b-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="dcd4b-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="dcd4b-107">(**HRESULT**) Codice di errore dell'operazione non riuscita.</span><span class="sxs-lookup"><span data-stu-id="dcd4b-107">(**HRESULT**) Failure code of the operation that failed.</span></span>

</dd> <dt>

<span data-ttu-id="dcd4b-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="dcd4b-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="dcd4b-109">Zero.</span><span class="sxs-lookup"><span data-stu-id="dcd4b-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="dcd4b-110">Azione predefinita</span><span class="sxs-lookup"><span data-stu-id="dcd4b-110">Default Action</span></span>

<span data-ttu-id="dcd4b-111">No.</span><span class="sxs-lookup"><span data-stu-id="dcd4b-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="dcd4b-112">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="dcd4b-112">Remarks</span></span>

<span data-ttu-id="dcd4b-113">Se il gestore del grafico dei filtri rilascia un comando di esecuzione asincrona che ha esito negativo, questo evento viene inviato all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="dcd4b-113">If the filter graph manager issues an asynchronous run command that fails, it sends this event to the application.</span></span> <span data-ttu-id="dcd4b-114">Il grafo rimane in stato di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="dcd4b-114">The graph remains in a running state.</span></span> <span data-ttu-id="dcd4b-115">Lo stato dei filtri sottostanti è indeterminato.</span><span class="sxs-lookup"><span data-stu-id="dcd4b-115">The state of the underlying filters is indeterminate.</span></span> <span data-ttu-id="dcd4b-116">Alcuni filtri potrebbero essere in esecuzione, altri no.</span><span class="sxs-lookup"><span data-stu-id="dcd4b-116">Some filters might be running, others might not.</span></span>

## <a name="requirements"></a><span data-ttu-id="dcd4b-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dcd4b-117">Requirements</span></span>



| <span data-ttu-id="dcd4b-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="dcd4b-118">Requirement</span></span> | <span data-ttu-id="dcd4b-119">Valore</span><span class="sxs-lookup"><span data-stu-id="dcd4b-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dcd4b-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dcd4b-120">Header</span></span><br/> | <dl> <span data-ttu-id="dcd4b-121"><dt>Dshow. h</dt></span><span class="sxs-lookup"><span data-stu-id="dcd4b-121"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dcd4b-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dcd4b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcd4b-123">Codici di notifica degli eventi</span><span class="sxs-lookup"><span data-stu-id="dcd4b-123">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="dcd4b-124">Notifica degli eventi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="dcd4b-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




