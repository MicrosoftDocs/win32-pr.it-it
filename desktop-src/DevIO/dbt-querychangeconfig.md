---
description: Il sistema trasmette l'evento DBT \_ QUERYCHANGECONFIG Device per richiedere l'autorizzazione per modificare la configurazione corrente (dock o Undock). Qualsiasi applicazione può negare questa richiesta e annullare la modifica.
ms.assetid: 2e452ea7-e2bf-4500-952a-ee7d891533a0
title: Evento DBT_QUERYCHANGECONFIG (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48367da1788ae2985b21fad6e960153008e9ffd2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523650"
---
# <a name="dbt_querychangeconfig-event"></a><span data-ttu-id="5510f-104">\_Evento QUERYCHANGECONFIG DBT</span><span class="sxs-lookup"><span data-stu-id="5510f-104">DBT\_QUERYCHANGECONFIG event</span></span>

<span data-ttu-id="5510f-105">Il sistema trasmette l'evento DBT \_ QUERYCHANGECONFIG Device per richiedere l'autorizzazione per modificare la configurazione corrente (dock o Undock).</span><span class="sxs-lookup"><span data-stu-id="5510f-105">The system broadcasts the DBT\_QUERYCHANGECONFIG device event to request permission to change the current configuration (dock or undock).</span></span> <span data-ttu-id="5510f-106">Qualsiasi applicazione può negare questa richiesta e annullare la modifica.</span><span class="sxs-lookup"><span data-stu-id="5510f-106">Any application can deny this request and cancel the change.</span></span>

<span data-ttu-id="5510f-107">Per trasmettere questo evento del dispositivo, il sistema usa il messaggio [**WM \_ DEVICECHANGE**](wm-devicechange.md) con *wParam* impostato su DBT \_ QUERYCHANGECONFIG e *lParam* impostati su zero.</span><span class="sxs-lookup"><span data-stu-id="5510f-107">To broadcast this device event, the system uses the [**WM\_DEVICECHANGE**](wm-devicechange.md) message with *wParam* set to DBT\_QUERYCHANGECONFIG and *lParam* set to zero.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // WM_DEVICECHANGE
  WPARAM wParam,   // device-change event
  LPARAM lParam    // event-specific data
);
```



## <a name="parameters"></a><span data-ttu-id="5510f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="5510f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5510f-109">*HWND*</span><span class="sxs-lookup"><span data-stu-id="5510f-109">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="5510f-110">Handle di una finestra.</span><span class="sxs-lookup"><span data-stu-id="5510f-110">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="5510f-111">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="5510f-111">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="5510f-112">Identificatore del messaggio [**WM \_ DEVICECHANGE**](wm-devicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="5510f-112">The [**WM\_DEVICECHANGE**](wm-devicechange.md) message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="5510f-113">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5510f-113">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5510f-114">Impostare su DBT \_ QUERYCHANGECONFIG.</span><span class="sxs-lookup"><span data-stu-id="5510f-114">Set to DBT\_QUERYCHANGECONFIG.</span></span>

</dd> <dt>

<span data-ttu-id="5510f-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5510f-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5510f-116">Imposta su zero.</span><span class="sxs-lookup"><span data-stu-id="5510f-116">Set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5510f-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5510f-117">Return value</span></span>

<span data-ttu-id="5510f-118">Restituisce **true** per concedere l'autorizzazione per modificare la configurazione.</span><span class="sxs-lookup"><span data-stu-id="5510f-118">Return **TRUE** to grant permission to change the configuration.</span></span>

<span data-ttu-id="5510f-119">Return BROADCAST \_ query \_ Deny per negare l'autorizzazione per modificare la configurazione.</span><span class="sxs-lookup"><span data-stu-id="5510f-119">Return BROADCAST\_QUERY\_DENY to deny permission to change the configuration.</span></span>

## <a name="requirements"></a><span data-ttu-id="5510f-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5510f-120">Requirements</span></span>



| <span data-ttu-id="5510f-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="5510f-121">Requirement</span></span> | <span data-ttu-id="5510f-122">Valore</span><span class="sxs-lookup"><span data-stu-id="5510f-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="5510f-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5510f-123">Minimum supported client</span></span><br/> | <span data-ttu-id="5510f-124">Windows XP</span><span class="sxs-lookup"><span data-stu-id="5510f-124">Windows XP</span></span><br/>                                                            |
| <span data-ttu-id="5510f-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5510f-125">Minimum supported server</span></span><br/> | <span data-ttu-id="5510f-126">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5510f-126">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="5510f-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5510f-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="5510f-128"><dt>DBT. h</dt></span><span class="sxs-lookup"><span data-stu-id="5510f-128"><dt>Dbt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5510f-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5510f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5510f-130">Eventi dispositivo</span><span class="sxs-lookup"><span data-stu-id="5510f-130">Device Events</span></span>](device-events.md)
</dt> <dt>

[<span data-ttu-id="5510f-131">Eventi di gestione dei dispositivi</span><span class="sxs-lookup"><span data-stu-id="5510f-131">Device Management Events</span></span>](device-management-events.md)
</dt> <dt>

[<span data-ttu-id="5510f-132">**\_DEVICECHANGE WM**</span><span class="sxs-lookup"><span data-stu-id="5510f-132">**WM\_DEVICECHANGE**</span></span>](wm-devicechange.md)
</dt> </dl>

 

 




