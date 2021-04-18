---
description: Notifica alle applicazioni che il sistema ha ripreso l'operazione dopo essere stata sospesa.
ms.assetid: 9058a2ff-9b8e-48e5-accb-4810c8598294
title: Evento PBT_APMRESUMESUSPEND (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d26357215853e0989851b6a9e731340a8dc2e6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312033"
---
# <a name="pbt_apmresumesuspend-event"></a><span data-ttu-id="97e61-103">\_Evento APMRESUMESUSPEND PBT</span><span class="sxs-lookup"><span data-stu-id="97e61-103">PBT\_APMRESUMESUSPEND event</span></span>

<span data-ttu-id="97e61-104">Notifica alle applicazioni che il sistema ha ripreso l'operazione dopo essere stata sospesa.</span><span class="sxs-lookup"><span data-stu-id="97e61-104">Notifies applications that the system has resumed operation after being suspended.</span></span>

<span data-ttu-id="97e61-105">Una finestra riceve questo evento tramite il messaggio [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) .</span><span class="sxs-lookup"><span data-stu-id="97e61-105">A window receives this event through the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message.</span></span> <span data-ttu-id="97e61-106">I parametri *wParam* e *lParam* sono impostati come descritto di seguito.</span><span class="sxs-lookup"><span data-stu-id="97e61-106">The *wParam* and *lParam* parameters are set as described following.</span></span>


```C++
LRESULT 
CALLBACK 
WindowProc( HWND hwnd,      // handle to window
            UINT uMsg,      // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMRESUMESUSPEND
            LPARAM lParam); // zero
```



## <a name="parameters"></a><span data-ttu-id="97e61-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="97e61-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97e61-108">*HWND*</span><span class="sxs-lookup"><span data-stu-id="97e61-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="97e61-109">Handle per la finestra.</span><span class="sxs-lookup"><span data-stu-id="97e61-109">A handle to window.</span></span>

<span data-ttu-id="97e61-110"></dd> <dt>*uMsg*</dt> </span><span class="sxs-lookup"><span data-stu-id="97e61-110"></dd> <dt>*uMsg* </dt> </span></span><dd> 

| <span data-ttu-id="97e61-111">Valore</span><span class="sxs-lookup"><span data-stu-id="97e61-111">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="97e61-112">Significato</span><span class="sxs-lookup"><span data-stu-id="97e61-112">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <span data-ttu-id="97e61-113"><dt>**[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span><span class="sxs-lookup"><span data-stu-id="97e61-113"><dt>**[**WM\_POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span></span> </dl> | <span data-ttu-id="97e61-114">Identificatore del messaggio.</span><span class="sxs-lookup"><span data-stu-id="97e61-114">Message identifier.</span></span><br/> |



 

<span data-ttu-id="97e61-115"></dd> <dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="97e61-115"></dd> <dt>*wParam* </dt> </span></span><dd> 

| <span data-ttu-id="97e61-116">Valore</span><span class="sxs-lookup"><span data-stu-id="97e61-116">Value</span></span>                                                                                                                                                                                                                                           | <span data-ttu-id="97e61-117">Significato</span><span class="sxs-lookup"><span data-stu-id="97e61-117">Meaning</span></span>                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMRESUMESUSPEND"></span><span id="pbt_apmresumesuspend"></span><dl> <span data-ttu-id="97e61-118"><dt>**PBT \_ APMRESUMESUSPEND**</dt> <dt>7 (0x7)</dt></span><span class="sxs-lookup"><span data-stu-id="97e61-118"><dt>**PBT\_APMRESUMESUSPEND**</dt> <dt>7 (0x7)</dt></span></span> </dl> | <span data-ttu-id="97e61-119">Identificatore dell'evento.</span><span class="sxs-lookup"><span data-stu-id="97e61-119">Event identifier.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="97e61-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="97e61-120">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="97e61-121">Riservati deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="97e61-121">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97e61-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="97e61-122">Return value</span></span>

<span data-ttu-id="97e61-123">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="97e61-123">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="97e61-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="97e61-124">Remarks</span></span>

<span data-ttu-id="97e61-125">Un'applicazione può ricevere questo evento solo se ha ricevuto l' [evento \_ APMSUSPEND PBT](pbt-apmsuspend.md) prima della sospensione del computer.</span><span class="sxs-lookup"><span data-stu-id="97e61-125">An application can receive this event only if it received the [PBT\_APMSUSPEND](pbt-apmsuspend.md) event before the computer was suspended.</span></span> <span data-ttu-id="97e61-126">In caso contrario, l'applicazione riceverà un evento [PBT \_ APMRESUMECRITICAL](pbt-apmresumecritical.md) .</span><span class="sxs-lookup"><span data-stu-id="97e61-126">Otherwise, the application will receive a [PBT\_APMRESUMECRITICAL](pbt-apmresumecritical.md) event.</span></span>

<span data-ttu-id="97e61-127">Se il sistema viene riattivato a causa dell'attività dell'utente, ad esempio premendo il pulsante di alimentazione, o se il sistema rileva l'interazione dell'utente sulla console fisica (ad esempio, l'input del mouse o della tastiera) dopo la riattivazione automatica, il sistema trasmette prima di tutto l'evento [PBT \_ APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) , quindi trasmette l' \_ evento PBT APMRESUMESUSPEND.</span><span class="sxs-lookup"><span data-stu-id="97e61-127">If the system wakes due to user activity (such as pressing the power button) or if the system detects user interaction at the physical console (such as mouse or keyboard input) after waking unattended, the system first broadcasts the [PBT\_APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) event, then it broadcasts the PBT\_APMRESUMESUSPEND event.</span></span> <span data-ttu-id="97e61-128">Inoltre, il sistema attiva la visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="97e61-128">In addition, the system turns on the display.</span></span> <span data-ttu-id="97e61-129">L'applicazione deve riaprire i file chiusi quando il sistema entra in sospensione e prepara l'input dell'utente.</span><span class="sxs-lookup"><span data-stu-id="97e61-129">Your application should reopen files that it closed when the system entered sleep and prepare for user input.</span></span>

<span data-ttu-id="97e61-130">Se il sistema viene riattivato a causa di un segnale di riattivazione esterno (riattivazione remota), il sistema trasmette solo l'evento [PBT \_ APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) .</span><span class="sxs-lookup"><span data-stu-id="97e61-130">If the system wakes due to an external wake signal (remote wake), the system broadcasts only the [PBT\_APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) event.</span></span> <span data-ttu-id="97e61-131">L' \_ evento APMRESUMESUSPEND PBT non viene inviato.</span><span class="sxs-lookup"><span data-stu-id="97e61-131">The PBT\_APMRESUMESUSPEND event is not sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="97e61-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="97e61-132">Requirements</span></span>



| <span data-ttu-id="97e61-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="97e61-133">Requirement</span></span> | <span data-ttu-id="97e61-134">Valore</span><span class="sxs-lookup"><span data-stu-id="97e61-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97e61-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="97e61-135">Minimum supported client</span></span><br/> | <span data-ttu-id="97e61-136">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="97e61-136">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="97e61-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="97e61-137">Minimum supported server</span></span><br/> | <span data-ttu-id="97e61-138">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="97e61-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="97e61-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="97e61-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="97e61-140"><dt>WinUser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="97e61-140"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97e61-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="97e61-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97e61-142">Eventi di riattivazione del sistema</span><span class="sxs-lookup"><span data-stu-id="97e61-142">System Wake-up Events</span></span>](system-wake-up-events.md)
</dt> <dt>

[<span data-ttu-id="97e61-143">Eventi di risparmio energia</span><span class="sxs-lookup"><span data-stu-id="97e61-143">Power Management Events</span></span>](power-management-events.md)
</dt> <dt>

[<span data-ttu-id="97e61-144">\_APMSUSPEND PBT</span><span class="sxs-lookup"><span data-stu-id="97e61-144">PBT\_APMSUSPEND</span></span>](pbt-apmsuspend.md)
</dt> <dt>

[<span data-ttu-id="97e61-145">\_APMRESUMECRITICAL PBT</span><span class="sxs-lookup"><span data-stu-id="97e61-145">PBT\_APMRESUMECRITICAL</span></span>](pbt-apmresumecritical.md)
</dt> <dt>

[<span data-ttu-id="97e61-146">**\_POWERBROADCAST WM**</span><span class="sxs-lookup"><span data-stu-id="97e61-146">**WM\_POWERBROADCAST**</span></span>](wm-powerbroadcast.md)
</dt> </dl>

 

 




