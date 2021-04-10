---
description: Notifica alle applicazioni che il computer sta per entrare in uno stato di sospensione.
ms.assetid: 61b177a0-4cff-4740-bed8-a46c06c43be8
title: Evento PBT_APMSUSPEND (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fc6982e00565329c85e06765879b9b72b07fe6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104231529"
---
# <a name="pbt_apmsuspend-event"></a><span data-ttu-id="e371c-103">\_Evento APMSUSPEND PBT</span><span class="sxs-lookup"><span data-stu-id="e371c-103">PBT\_APMSUSPEND event</span></span>

<span data-ttu-id="e371c-104">Notifica alle applicazioni che il computer sta per entrare in uno stato di sospensione.</span><span class="sxs-lookup"><span data-stu-id="e371c-104">Notifies applications that the computer is about to enter a suspended state.</span></span> <span data-ttu-id="e371c-105">Questo evento viene in genere trasmesso quando tutte le applicazioni e i driver installabili restituiscono **true** a un evento [ \_ APMQUERYSUSPEND PBT](pbt-apmquerysuspend.md) precedente.</span><span class="sxs-lookup"><span data-stu-id="e371c-105">This event is typically broadcast when all applications and installable drivers have returned **TRUE** to a previous [PBT\_APMQUERYSUSPEND](pbt-apmquerysuspend.md) event.</span></span>

<span data-ttu-id="e371c-106">Una finestra riceve questo evento tramite il messaggio [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) .</span><span class="sxs-lookup"><span data-stu-id="e371c-106">A window receives this event through the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message.</span></span> <span data-ttu-id="e371c-107">I parametri *wParam* e *lParam* sono impostati come descritto di seguito.</span><span class="sxs-lookup"><span data-stu-id="e371c-107">The *wParam* and *lParam* parameters are set as described following.</span></span>


```C++
LRESULT 
CALLBACK 
WindowProc( HWND hwnd,      // handle to window
            UINT uMsg,      // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMSUSPEND
            LPARAM lParam); // zero
```



## <a name="parameters"></a><span data-ttu-id="e371c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e371c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e371c-109">*HWND*</span><span class="sxs-lookup"><span data-stu-id="e371c-109">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="e371c-110">Handle per la finestra.</span><span class="sxs-lookup"><span data-stu-id="e371c-110">A handle to window.</span></span>

<span data-ttu-id="e371c-111"></dd> <dt>*uMsg*</dt> </span><span class="sxs-lookup"><span data-stu-id="e371c-111"></dd> <dt>*uMsg* </dt> </span></span><dd> 

| <span data-ttu-id="e371c-112">Valore</span><span class="sxs-lookup"><span data-stu-id="e371c-112">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="e371c-113">Significato</span><span class="sxs-lookup"><span data-stu-id="e371c-113">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <span data-ttu-id="e371c-114"><dt>**[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span><span class="sxs-lookup"><span data-stu-id="e371c-114"><dt>**[**WM\_POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span></span> </dl> | <span data-ttu-id="e371c-115">Identificatore del messaggio.</span><span class="sxs-lookup"><span data-stu-id="e371c-115">Message identifier.</span></span><br/> |



 

<span data-ttu-id="e371c-116"></dd> <dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="e371c-116"></dd> <dt>*wParam* </dt> </span></span><dd> 

| <span data-ttu-id="e371c-117">Valore</span><span class="sxs-lookup"><span data-stu-id="e371c-117">Value</span></span>                                                                                                                                                                                                                         | <span data-ttu-id="e371c-118">Significato</span><span class="sxs-lookup"><span data-stu-id="e371c-118">Meaning</span></span>                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMSUSPEND"></span><span id="pbt_apmsuspend"></span><dl> <span data-ttu-id="e371c-119"><dt>**PBT \_ APMSUSPEND**</dt> <dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="e371c-119"><dt>**PBT\_APMSUSPEND**</dt> <dt>4 (0x4)</dt></span></span> </dl> | <span data-ttu-id="e371c-120">Identificatore dell'evento.</span><span class="sxs-lookup"><span data-stu-id="e371c-120">Event identifier.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e371c-121">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e371c-121">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e371c-122">Riservati deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="e371c-122">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e371c-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e371c-123">Return value</span></span>

<span data-ttu-id="e371c-124">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="e371c-124">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e371c-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="e371c-125">Remarks</span></span>

<span data-ttu-id="e371c-126">Un'applicazione deve elaborare questo evento completando tutte le attività necessarie per salvare i dati.</span><span class="sxs-lookup"><span data-stu-id="e371c-126">An application should process this event by completing all tasks necessary to save data.</span></span>

<span data-ttu-id="e371c-127">Il sistema consente circa due secondi per la gestione della notifica da parte di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e371c-127">The system allows approximately two seconds for an application to handle this notification.</span></span> <span data-ttu-id="e371c-128">Se un'applicazione sta ancora eseguendo operazioni dopo la scadenza dell'intervallo di tempo, il sistema potrebbe interrompere l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e371c-128">If an application is still performing operations after its time allotment has expired, the system may interrupt the application.</span></span>

## <a name="requirements"></a><span data-ttu-id="e371c-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e371c-129">Requirements</span></span>



| <span data-ttu-id="e371c-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="e371c-130">Requirement</span></span> | <span data-ttu-id="e371c-131">Valore</span><span class="sxs-lookup"><span data-stu-id="e371c-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e371c-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e371c-132">Minimum supported client</span></span><br/> | <span data-ttu-id="e371c-133">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e371c-133">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e371c-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e371c-134">Minimum supported server</span></span><br/> | <span data-ttu-id="e371c-135">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e371c-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e371c-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e371c-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="e371c-137"><dt>WinUser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e371c-137"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e371c-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e371c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e371c-139">Criteri di sospensione del sistema</span><span class="sxs-lookup"><span data-stu-id="e371c-139">System Sleep Criteria</span></span>](system-sleep-criteria.md)
</dt> <dt>

[<span data-ttu-id="e371c-140">Eventi di riattivazione del sistema</span><span class="sxs-lookup"><span data-stu-id="e371c-140">System Wake-up Events</span></span>](system-wake-up-events.md)
</dt> <dt>

[<span data-ttu-id="e371c-141">Eventi di risparmio energia</span><span class="sxs-lookup"><span data-stu-id="e371c-141">Power Management Events</span></span>](power-management-events.md)
</dt> <dt>

[<span data-ttu-id="e371c-142">\_APMQUERYSUSPEND PBT</span><span class="sxs-lookup"><span data-stu-id="e371c-142">PBT\_APMQUERYSUSPEND</span></span>](pbt-apmquerysuspend.md)
</dt> <dt>

[<span data-ttu-id="e371c-143">**SetSystemPowerState**</span><span class="sxs-lookup"><span data-stu-id="e371c-143">**SetSystemPowerState**</span></span>](/windows/desktop/api/WinBase/nf-winbase-setsystempowerstate)
</dt> <dt>

[<span data-ttu-id="e371c-144">**\_POWERBROADCAST WM**</span><span class="sxs-lookup"><span data-stu-id="e371c-144">**WM\_POWERBROADCAST**</span></span>](wm-powerbroadcast.md)
</dt> </dl>

 

 




