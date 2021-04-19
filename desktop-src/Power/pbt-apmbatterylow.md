---
description: Notifica alle applicazioni che l'energia elettrica della batteria è insufficiente.
ms.assetid: ef24b8cf-d801-4452-a03c-3f2bdbdd7e5d
title: Evento PBT_APMBATTERYLOW (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64884f9bb01e37883e1be61b2de88862e8b119fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312040"
---
# <a name="pbt_apmbatterylow-event"></a><span data-ttu-id="31777-103">\_Evento APMBATTERYLOW PBT</span><span class="sxs-lookup"><span data-stu-id="31777-103">PBT\_APMBATTERYLOW event</span></span>

<span data-ttu-id="31777-104">\[PBT \_ APMBATTERYLOW è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="31777-104">\[PBT\_APMBATTERYLOW is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="31777-105">Il supporto per questo evento è stato rimosso in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="31777-105">Support for this event was removed in Windows Vista.</span></span> <span data-ttu-id="31777-106">In alternativa, usare [PBT \_ APMPOWERSTATUSCHANGE](pbt-apmpowerstatuschange.md) .\]</span><span class="sxs-lookup"><span data-stu-id="31777-106">Use [PBT\_APMPOWERSTATUSCHANGE](pbt-apmpowerstatuschange.md) instead.\]</span></span>

<span data-ttu-id="31777-107">Notifica alle applicazioni che l'energia elettrica della batteria è insufficiente.</span><span class="sxs-lookup"><span data-stu-id="31777-107">Notifies applications that the battery power is low.</span></span>

<span data-ttu-id="31777-108">Una finestra riceve questo evento tramite il messaggio [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) .</span><span class="sxs-lookup"><span data-stu-id="31777-108">A window receives this event through the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message.</span></span> <span data-ttu-id="31777-109">I parametri *wParam* e *lParam* sono impostati come descritto di seguito.</span><span class="sxs-lookup"><span data-stu-id="31777-109">The *wParam* and *lParam* parameters are set as described following.</span></span>


```C++
LRESULT 
CALLBACK 
WindowProc( HWND   hwnd,    // handle to window
            UINT   uMsg,    // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMBATTERYLOW
            LPARAM lParam); // zero
```



## <a name="parameters"></a><span data-ttu-id="31777-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="31777-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31777-111">*HWND*</span><span class="sxs-lookup"><span data-stu-id="31777-111">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="31777-112">Handle per la finestra.</span><span class="sxs-lookup"><span data-stu-id="31777-112">A handle to the window.</span></span>

<span data-ttu-id="31777-113"></dd> <dt>*uMsg*</dt> </span><span class="sxs-lookup"><span data-stu-id="31777-113"></dd> <dt>*uMsg* </dt> </span></span><dd> 

| <span data-ttu-id="31777-114">Valore</span><span class="sxs-lookup"><span data-stu-id="31777-114">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="31777-115">Significato</span><span class="sxs-lookup"><span data-stu-id="31777-115">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <span data-ttu-id="31777-116"><dt>**[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span><span class="sxs-lookup"><span data-stu-id="31777-116"><dt>**[**WM\_POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span></span> </dl> | <span data-ttu-id="31777-117">Identificatore del messaggio.</span><span class="sxs-lookup"><span data-stu-id="31777-117">Message identifier.</span></span><br/> |



 

<span data-ttu-id="31777-118"></dd> <dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="31777-118"></dd> <dt>*wParam* </dt> </span></span><dd> 

| <span data-ttu-id="31777-119">Valore</span><span class="sxs-lookup"><span data-stu-id="31777-119">Value</span></span>                                                                                                                                                                                                                                  | <span data-ttu-id="31777-120">Significato</span><span class="sxs-lookup"><span data-stu-id="31777-120">Meaning</span></span>                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMBATTERYLOW"></span><span id="pbt_apmbatterylow"></span><dl> <span data-ttu-id="31777-121"><dt>**PBT \_ APMBATTERYLOW**</dt> <dt>9 (0x9)</dt></span><span class="sxs-lookup"><span data-stu-id="31777-121"><dt>**PBT\_APMBATTERYLOW**</dt> <dt>9 (0x9)</dt></span></span> </dl> | <span data-ttu-id="31777-122">Identificatore dell'evento.</span><span class="sxs-lookup"><span data-stu-id="31777-122">Event identifier.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="31777-123">*lParam*</span><span class="sxs-lookup"><span data-stu-id="31777-123">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="31777-124">Riservato, deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="31777-124">Reserved, must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31777-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="31777-125">Return value</span></span>

<span data-ttu-id="31777-126">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="31777-126">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="31777-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="31777-127">Remarks</span></span>

<span data-ttu-id="31777-128">Questo evento viene trasmesso quando un BIOS APM del sistema segnala una notifica di batteria insufficiente per APM.</span><span class="sxs-lookup"><span data-stu-id="31777-128">This event is broadcast when a system's APM BIOS signals an APM battery low notification.</span></span> <span data-ttu-id="31777-129">Poiché alcune implementazioni del BIOS APM non forniscono notifiche quando le batterie sono insufficienti, questo evento potrebbe non essere mai trasmesso in alcuni computer.</span><span class="sxs-lookup"><span data-stu-id="31777-129">Because some APM BIOS implementations do not provide notifications when batteries are low, this event may never be broadcast on some computers.</span></span>

## <a name="requirements"></a><span data-ttu-id="31777-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="31777-130">Requirements</span></span>



| <span data-ttu-id="31777-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="31777-131">Requirement</span></span> | <span data-ttu-id="31777-132">Valore</span><span class="sxs-lookup"><span data-stu-id="31777-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31777-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="31777-133">Minimum supported client</span></span><br/> | <span data-ttu-id="31777-134">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="31777-134">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="31777-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="31777-135">Minimum supported server</span></span><br/> | <span data-ttu-id="31777-136">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="31777-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="31777-137">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="31777-137">End of client support</span></span><br/>    | <span data-ttu-id="31777-138">Windows XP</span><span class="sxs-lookup"><span data-stu-id="31777-138">Windows XP</span></span><br/>                                                                                    |
| <span data-ttu-id="31777-139">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="31777-139">End of server support</span></span><br/>    | <span data-ttu-id="31777-140">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="31777-140">Windows Server 2003</span></span><br/>                                                                           |
| <span data-ttu-id="31777-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="31777-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="31777-142"><dt>WinUser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="31777-142"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31777-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="31777-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31777-144">Eventi di risparmio energia</span><span class="sxs-lookup"><span data-stu-id="31777-144">Power Management Events</span></span>](power-management-events.md)
</dt> <dt>

[<span data-ttu-id="31777-145">**\_POWERBROADCAST WM**</span><span class="sxs-lookup"><span data-stu-id="31777-145">**WM\_POWERBROADCAST**</span></span>](wm-powerbroadcast.md)
</dt> </dl>

 

 




