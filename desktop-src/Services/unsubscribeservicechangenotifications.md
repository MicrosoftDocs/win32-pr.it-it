---
description: Annulla la sottoscrizione delle notifiche di modifica dello stato del servizio.
ms.assetid: 8c04ebf7-4d61-4617-b120-dbe26b2f9ad2
title: Funzione UnsubscribeServiceChangeNotifications (Winsvcp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UnsubscribeServiceChangeNotifications
api_type:
- DllExport
api_location:
- SecHost.dll
- API-MS-Win-Service-Private-L1-1-0.dll
- API-MS-Win-Service-Private-L1-1-1.dll
- Advapi32.dll
- API-MS-Win-Service-Private-L1-1-2.dll
ms.openlocfilehash: ebecfb133172c9c7a56ed6d28f7ad6b395d8afce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883270"
---
# <a name="unsubscribeservicechangenotifications-function"></a><span data-ttu-id="ecaa4-103">UnsubscribeServiceChangeNotifications (funzione)</span><span class="sxs-lookup"><span data-stu-id="ecaa4-103">UnsubscribeServiceChangeNotifications function</span></span>

<span data-ttu-id="ecaa4-104">Annulla la sottoscrizione delle notifiche di modifica dello stato del servizio.</span><span class="sxs-lookup"><span data-stu-id="ecaa4-104">Unsubscribes from service status change notifications.</span></span> <span data-ttu-id="ecaa4-105">Questa funzione usa le sottoscrizioni restituite da [**SubscribeServiceChangeNotifications**](subscribeservicechangenotifications.md).</span><span class="sxs-lookup"><span data-stu-id="ecaa4-105">This function uses subscriptions returned by [**SubscribeServiceChangeNotifications**](subscribeservicechangenotifications.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ecaa4-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ecaa4-106">Syntax</span></span>


```C++
 VOID WINAPI UnsubscribeServiceChangeNotifications(
  _In_ PSC_NOTIFICATION_REGISTRATION pSubscription
);
```



## <a name="parameters"></a><span data-ttu-id="ecaa4-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="ecaa4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ecaa4-108">*pSubscription* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ecaa4-108">*pSubscription* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ecaa4-109">Puntatore alla sottoscrizione di cui annullare la sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="ecaa4-109">A pointer to the subscription to be unsubscribed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ecaa4-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ecaa4-110">Return value</span></span>

<span data-ttu-id="ecaa4-111">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="ecaa4-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ecaa4-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="ecaa4-112">Remarks</span></span>

<span data-ttu-id="ecaa4-113">**UnsubscribeServiceChangeNotifications** non restituisce alcun risultato finché non vengono completate le richiamate in-process.</span><span class="sxs-lookup"><span data-stu-id="ecaa4-113">**UnsubscribeServiceChangeNotifications** does not return until outstanding in-process callbacks are complete.</span></span> <span data-ttu-id="ecaa4-114">Pertanto, non è possibile chiamare **UnsubscribeServiceChangeNotifications** all'interno del callback senza causare un deadlock.</span><span class="sxs-lookup"><span data-stu-id="ecaa4-114">So, you cannot call **UnsubscribeServiceChangeNotifications** within the callback without causing a deadlock.</span></span>

## <a name="requirements"></a><span data-ttu-id="ecaa4-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ecaa4-115">Requirements</span></span>



| <span data-ttu-id="ecaa4-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ecaa4-116">Requirement</span></span> | <span data-ttu-id="ecaa4-117">Valore</span><span class="sxs-lookup"><span data-stu-id="ecaa4-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ecaa4-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ecaa4-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ecaa4-119">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="ecaa4-119">Windows 8 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ecaa4-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ecaa4-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ecaa4-121">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="ecaa4-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ecaa4-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ecaa4-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ecaa4-123"><dt>Winsvcp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ecaa4-123"><dt>Winsvcp.h</dt></span></span> </dl>   |
| <span data-ttu-id="ecaa4-124">DLL</span><span class="sxs-lookup"><span data-stu-id="ecaa4-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ecaa4-125"><dt>SecHost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ecaa4-125"><dt>SecHost.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ecaa4-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ecaa4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecaa4-127">**CreateService**</span><span class="sxs-lookup"><span data-stu-id="ecaa4-127">**CreateService**</span></span>](/windows/desktop/api/Winsvc/nf-winsvc-createservicea)
</dt> <dt>

[<span data-ttu-id="ecaa4-128">**OpenService**</span><span class="sxs-lookup"><span data-stu-id="ecaa4-128">**OpenService**</span></span>](/windows/desktop/api/Winsvc/nf-winsvc-openservicea)
</dt> <dt>

[<span data-ttu-id="ecaa4-129">**OpenSCManager**</span><span class="sxs-lookup"><span data-stu-id="ecaa4-129">**OpenSCManager**</span></span>](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera)
</dt> <dt>

[<span data-ttu-id="ecaa4-130">**SubscribeServiceChangeNotifications**</span><span class="sxs-lookup"><span data-stu-id="ecaa4-130">**SubscribeServiceChangeNotifications**</span></span>](subscribeservicechangenotifications.md)
</dt> <dt>

[<span data-ttu-id="ecaa4-131">**QueryServiceDynamicInformation**</span><span class="sxs-lookup"><span data-stu-id="ecaa4-131">**QueryServiceDynamicInformation**</span></span>](/windows/desktop/api/Winsvc/nf-winsvc-queryservicedynamicinformation)
</dt> </dl>

 

 




