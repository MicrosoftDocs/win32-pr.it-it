---
description: Notifica alle applicazioni una modifica dello stato di alimentazione del computer, ad esempio un passaggio dalla batteria a A/C.
ms.assetid: dc56fee3-e0df-4f8e-8a41-92460279280a
title: Evento PBT_APMPOWERSTATUSCHANGE (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18ed67f7ba064d44614196da4190ce18a996bd5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104231530"
---
# <a name="pbt_apmpowerstatuschange-event"></a><span data-ttu-id="53205-103">\_Evento APMPOWERSTATUSCHANGE PBT</span><span class="sxs-lookup"><span data-stu-id="53205-103">PBT\_APMPOWERSTATUSCHANGE event</span></span>

<span data-ttu-id="53205-104">Notifica alle applicazioni una modifica dello stato di alimentazione del computer, ad esempio un passaggio dalla batteria a A/C.</span><span class="sxs-lookup"><span data-stu-id="53205-104">Notifies applications of a change in the power status of the computer, such as a switch from battery power to A/C.</span></span> <span data-ttu-id="53205-105">Il sistema trasmette questo evento anche quando l'autonomia della batteria scende sotto la soglia specificata dall'utente o se lo stato di carica della batteria cambia di una percentuale specificata.</span><span class="sxs-lookup"><span data-stu-id="53205-105">The system also broadcasts this event when remaining battery power slips below the threshold specified by the user or if the battery power changes by a specified percentage.</span></span>

<span data-ttu-id="53205-106">Una finestra riceve questo evento tramite il messaggio [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) .</span><span class="sxs-lookup"><span data-stu-id="53205-106">A window receives this event through the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message.</span></span> <span data-ttu-id="53205-107">I parametri *wParam* e *lParam* sono impostati come descritto di seguito.</span><span class="sxs-lookup"><span data-stu-id="53205-107">The *wParam* and *lParam* parameters are set as described following.</span></span>


```C++
LRESULT 
CALLBACK 
WindowProc( HWND hwnd,      // handle to window
            UINT uMsg,      // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMPOWERSTATUSCHANGE
            LPARAM lParam); // zero
```



## <a name="parameters"></a><span data-ttu-id="53205-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="53205-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53205-109">*HWND*</span><span class="sxs-lookup"><span data-stu-id="53205-109">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="53205-110">Handle per la finestra.</span><span class="sxs-lookup"><span data-stu-id="53205-110">A handle to window.</span></span>

<span data-ttu-id="53205-111"></dd> <dt>*uMsg*</dt> </span><span class="sxs-lookup"><span data-stu-id="53205-111"></dd> <dt>*uMsg* </dt> </span></span><dd> 

| <span data-ttu-id="53205-112">Valore</span><span class="sxs-lookup"><span data-stu-id="53205-112">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="53205-113">Significato</span><span class="sxs-lookup"><span data-stu-id="53205-113">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <span data-ttu-id="53205-114"><dt>**[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span><span class="sxs-lookup"><span data-stu-id="53205-114"><dt>**[**WM\_POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span></span> </dl> | <span data-ttu-id="53205-115">Identificatore del messaggio.</span><span class="sxs-lookup"><span data-stu-id="53205-115">Message identifier.</span></span><br/> |



 

<span data-ttu-id="53205-116"></dd> <dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="53205-116"></dd> <dt>*wParam* </dt> </span></span><dd> 

| <span data-ttu-id="53205-117">Valore</span><span class="sxs-lookup"><span data-stu-id="53205-117">Value</span></span>                                                                                                                                                                                                                                                        | <span data-ttu-id="53205-118">Significato</span><span class="sxs-lookup"><span data-stu-id="53205-118">Meaning</span></span>                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMPOWERSTATUSCHANGE"></span><span id="pbt_apmpowerstatuschange"></span><dl> <span data-ttu-id="53205-119"><dt>**PBT \_ APMPOWERSTATUSCHANGE**</dt> <dt>10 (0xA)</dt></span><span class="sxs-lookup"><span data-stu-id="53205-119"><dt>**PBT\_APMPOWERSTATUSCHANGE**</dt> <dt>10 (0xA)</dt></span></span> </dl> | <span data-ttu-id="53205-120">Identificatore dell'evento.</span><span class="sxs-lookup"><span data-stu-id="53205-120">Event identifier.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="53205-121">*lParam*</span><span class="sxs-lookup"><span data-stu-id="53205-121">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="53205-122">Riservati deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="53205-122">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53205-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="53205-123">Return value</span></span>

<span data-ttu-id="53205-124">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="53205-124">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="53205-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="53205-125">Remarks</span></span>

<span data-ttu-id="53205-126">Un'applicazione deve elaborare questo evento chiamando la funzione [**GetSystemPowerStatus**](/windows/desktop/api/Winbase/nf-winbase-getsystempowerstatus) per recuperare lo stato corrente di alimentazione del computer.</span><span class="sxs-lookup"><span data-stu-id="53205-126">An application should process this event by calling the [**GetSystemPowerStatus**](/windows/desktop/api/Winbase/nf-winbase-getsystempowerstatus) function to retrieve the current power status of the computer.</span></span> <span data-ttu-id="53205-127">In particolare, l'applicazione deve verificare i membri **ACLineStatus**, **BatteryFlag**, **BatteryLifetime** e **BatteryLifePercent** della struttura di [**\_ \_ stato dell'alimentazione del sistema**](/windows/desktop/api/Winbase/ns-winbase-system_power_status) per qualsiasi modifica.</span><span class="sxs-lookup"><span data-stu-id="53205-127">In particular, the application should check the **ACLineStatus**, **BatteryFlag**, **BatteryLifeTime**, and **BatteryLifePercent** members of the [**SYSTEM\_POWER\_STATUS**](/windows/desktop/api/Winbase/ns-winbase-system_power_status) structure for any changes.</span></span> <span data-ttu-id="53205-128">Questo evento può verificarsi quando la durata della batteria scende a meno di 5 minuti o quando la percentuale di durata della batteria scende sotto il 10% o se la durata della batteria viene modificata del 3%.</span><span class="sxs-lookup"><span data-stu-id="53205-128">This event can occur when battery life drops to less than 5 minutes, or when the percentage of battery life drops below 10 percent, or if the battery life changes by 3 percent.</span></span>

## <a name="requirements"></a><span data-ttu-id="53205-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="53205-129">Requirements</span></span>



| <span data-ttu-id="53205-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="53205-130">Requirement</span></span> | <span data-ttu-id="53205-131">Valore</span><span class="sxs-lookup"><span data-stu-id="53205-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53205-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="53205-132">Minimum supported client</span></span><br/> | <span data-ttu-id="53205-133">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="53205-133">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="53205-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="53205-134">Minimum supported server</span></span><br/> | <span data-ttu-id="53205-135">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="53205-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="53205-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="53205-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="53205-137"><dt>WinUser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="53205-137"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53205-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="53205-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53205-139">Stato di alimentazione del sistema</span><span class="sxs-lookup"><span data-stu-id="53205-139">System Power Status</span></span>](system-power-status.md)
</dt> <dt>

[<span data-ttu-id="53205-140">Eventi di risparmio energia</span><span class="sxs-lookup"><span data-stu-id="53205-140">Power Management Events</span></span>](power-management-events.md)
</dt> <dt>

[<span data-ttu-id="53205-141">**GetSystemPowerStatus**</span><span class="sxs-lookup"><span data-stu-id="53205-141">**GetSystemPowerStatus**</span></span>](/windows/desktop/api/Winbase/nf-winbase-getsystempowerstatus)
</dt> <dt>

[<span data-ttu-id="53205-142">**\_stato di alimentazione del sistema \_**</span><span class="sxs-lookup"><span data-stu-id="53205-142">**SYSTEM\_POWER\_STATUS**</span></span>](/windows/desktop/api/Winbase/ns-winbase-system_power_status)
</dt> <dt>

[<span data-ttu-id="53205-143">**\_POWERBROADCAST WM**</span><span class="sxs-lookup"><span data-stu-id="53205-143">**WM\_POWERBROADCAST**</span></span>](wm-powerbroadcast.md)
</dt> </dl>

 

 




