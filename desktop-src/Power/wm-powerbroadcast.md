---
description: Notifica alle applicazioni che si è verificato un evento di risparmio energia.
ms.assetid: 46452909-ac0e-4c06-8542-0b94d00e6556
title: Messaggio WM_POWERBROADCAST (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82f1b273462d8de27c19d715836d168ab8bf8c90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104529095"
---
# <a name="wm_powerbroadcast-message"></a><span data-ttu-id="7342a-103">\_Messaggio POWERBROADCAST WM</span><span class="sxs-lookup"><span data-stu-id="7342a-103">WM\_POWERBROADCAST message</span></span>

<span data-ttu-id="7342a-104">Notifica alle applicazioni che si è verificato un evento di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="7342a-104">Notifies applications that a power-management event has occurred.</span></span>

<span data-ttu-id="7342a-105">Una finestra riceve questo messaggio tramite la funzione **WindowProc** .</span><span class="sxs-lookup"><span data-stu-id="7342a-105">A window receives this message through its **WindowProc** function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND   hwnd,    // handle to window
  UINT   uMsg,    // WM_POWERBROADCAST
  WPARAM wParam,  // power-management event
  LPARAM lParam   // function-specific data
);
```



## <a name="parameters"></a><span data-ttu-id="7342a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7342a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7342a-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="7342a-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="7342a-108">Handle per la finestra.</span><span class="sxs-lookup"><span data-stu-id="7342a-108">A handle to window.</span></span>

<span data-ttu-id="7342a-109"></dd> <dt>*uMsg*</dt> </span><span class="sxs-lookup"><span data-stu-id="7342a-109"></dd> <dt>*uMsg* </dt> </span></span><dd> 

| <span data-ttu-id="7342a-110">Valore</span><span class="sxs-lookup"><span data-stu-id="7342a-110">Value</span></span>                                                                                                                                                                                                                                          | <span data-ttu-id="7342a-111">Significato</span><span class="sxs-lookup"><span data-stu-id="7342a-111">Meaning</span></span>                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <span data-ttu-id="7342a-112"><dt>\* \* \* \* WM \_ POWERBROADCAST \* \*</dt> \* \* <dt>536 (0x218)</dt></span><span class="sxs-lookup"><span data-stu-id="7342a-112"><dt>\*\*\*\*WM\_POWERBROADCAST\*\*\*\*</dt> <dt>536 (0x218)</dt></span></span> </dl> | <span data-ttu-id="7342a-113">Identificatore del messaggio.</span><span class="sxs-lookup"><span data-stu-id="7342a-113">Message identifier.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="7342a-114">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7342a-114">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7342a-115">Evento di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="7342a-115">The power-management event.</span></span> <span data-ttu-id="7342a-116">Questo parametro può essere uno dei seguenti identificatori di evento.</span><span class="sxs-lookup"><span data-stu-id="7342a-116">This parameter can be one of the following event identifiers.</span></span>



| <span data-ttu-id="7342a-117">Evento</span><span class="sxs-lookup"><span data-stu-id="7342a-117">Event</span></span>                                                                                                                                                                                                                                                                                        | <span data-ttu-id="7342a-118">Significato</span><span class="sxs-lookup"><span data-stu-id="7342a-118">Meaning</span></span>                                                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PBT_APMPOWERSTATUSCHANGE"></span><span id="pbt_apmpowerstatuschange"></span><dl> <span data-ttu-id="7342a-119"><dt>**[PBT \_ APMPOWERSTATUSCHANGE](pbt-apmpowerstatuschange.md)**</dt> <dt>10 (0xA)</dt></span><span class="sxs-lookup"><span data-stu-id="7342a-119"><dt>**[PBT\_APMPOWERSTATUSCHANGE](pbt-apmpowerstatuschange.md)**</dt> <dt>10 (0xA)</dt></span></span> </dl> | <span data-ttu-id="7342a-120">Lo stato di alimentazione è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="7342a-120">Power status has changed.</span></span><br/>                                                                                                                                                                        |
| <span id="PBT_APMRESUMEAUTOMATIC"></span><span id="pbt_apmresumeautomatic"></span><dl> <span data-ttu-id="7342a-121"><dt>**[PBT \_ APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md)**</dt> <dt>18 (0x12)</dt></span><span class="sxs-lookup"><span data-stu-id="7342a-121"><dt>**[PBT\_APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md)**</dt> <dt>18 (0x12)</dt></span></span> </dl>        | <span data-ttu-id="7342a-122">L'operazione viene ripresa automaticamente da uno stato di basso consumo.</span><span class="sxs-lookup"><span data-stu-id="7342a-122">Operation is resuming automatically from a low-power state.</span></span> <span data-ttu-id="7342a-123">Questo messaggio viene inviato ogni volta che il sistema riprende.</span><span class="sxs-lookup"><span data-stu-id="7342a-123">This message is sent every time the system resumes.</span></span><br/>                                                                                  |
| <span id="PBT_APMRESUMESUSPEND"></span><span id="pbt_apmresumesuspend"></span><dl> <span data-ttu-id="7342a-124"><dt>**[PBT \_ APMRESUMESUSPEND](pbt-apmresumesuspend.md)**</dt> <dt>7 (0x7)</dt></span><span class="sxs-lookup"><span data-stu-id="7342a-124"><dt>**[PBT\_APMRESUMESUSPEND](pbt-apmresumesuspend.md)**</dt> <dt>7 (0x7)</dt></span></span> </dl>                  | <span data-ttu-id="7342a-125">Operazione ripresa da uno stato di basso consumo.</span><span class="sxs-lookup"><span data-stu-id="7342a-125">Operation is resuming from a low-power state.</span></span> <span data-ttu-id="7342a-126">Questo messaggio viene inviato dopo [ \_ APMRESUMEAUTOMATIC PBT](pbt-apmresumeautomatic.md) se il resume viene attivato dall'input dell'utente, ad esempio premendo un tasto.</span><span class="sxs-lookup"><span data-stu-id="7342a-126">This message is sent after [PBT\_APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) if the resume is triggered by user input, such as pressing a key.</span></span><br/> |
| <span id="PBT_APMSUSPEND"></span><span id="pbt_apmsuspend"></span><dl> <span data-ttu-id="7342a-127"><dt>**[PBT \_ APMSUSPEND](pbt-apmsuspend.md)**</dt> <dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="7342a-127"><dt>**[PBT\_APMSUSPEND](pbt-apmsuspend.md)**</dt> <dt>4 (0x4)</dt></span></span> </dl>                                          | <span data-ttu-id="7342a-128">Il sistema sta per sospendere l'operazione.</span><span class="sxs-lookup"><span data-stu-id="7342a-128">System is suspending operation.</span></span><br/>                                                                                                                                                                  |
| <span id="PBT_POWERSETTINGCHANGE"></span><span id="pbt_powersettingchange"></span><dl> <span data-ttu-id="7342a-129"><dt>**[PBT \_ POWERSETTINGCHANGE](pbt-powersettingchange.md)**</dt> <dt>32787 (0x8013)</dt></span><span class="sxs-lookup"><span data-stu-id="7342a-129"><dt>**[PBT\_POWERSETTINGCHANGE](pbt-powersettingchange.md)**</dt> <dt>32787 (0x8013)</dt></span></span> </dl>   | <span data-ttu-id="7342a-130">È stato ricevuto un evento di modifica dell'impostazione di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="7342a-130">A power setting change event has been received.</span></span> <br/>                                                                                                                                                 |



 

</dd> <dt>

<span data-ttu-id="7342a-131">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7342a-131">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7342a-132">Dati specifici dell'evento.</span><span class="sxs-lookup"><span data-stu-id="7342a-132">The event-specific data.</span></span> <span data-ttu-id="7342a-133">Per la maggior parte degli eventi, questo parametro è riservato e non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="7342a-133">For most events, this parameter is reserved and not used.</span></span>

<span data-ttu-id="7342a-134">Se il parametro *wParam* è [PBT \_ POWERSETTINGCHANGE](pbt-powersettingchange.md), il parametro *lParam* è un puntatore a una struttura di [**\_ impostazione POWERBROADCAST**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) .</span><span class="sxs-lookup"><span data-stu-id="7342a-134">If the *wParam* parameter is [PBT\_POWERSETTINGCHANGE](pbt-powersettingchange.md), the *lParam* parameter is a pointer to a [**POWERBROADCAST\_SETTING**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7342a-135">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7342a-135">Return value</span></span>

<span data-ttu-id="7342a-136">Un'applicazione deve restituire **true** se elabora questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="7342a-136">An application should return **TRUE** if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="7342a-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="7342a-137">Remarks</span></span>

<span data-ttu-id="7342a-138">Il sistema invia sempre un messaggio [PBT \_ APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) ogni volta che il sistema riprende.</span><span class="sxs-lookup"><span data-stu-id="7342a-138">The system always sends a [PBT\_APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) message whenever the system resumes.</span></span> <span data-ttu-id="7342a-139">Se il sistema riprende in risposta all'input dell'utente, ad esempio premendo un tasto, il sistema invia anche un messaggio **\_ APMRESUMESUSPEND PBT** dopo l'invio di \_ APMRESUMEAUTOMATIC PBT.</span><span class="sxs-lookup"><span data-stu-id="7342a-139">If the system resumes in response to user input such as pressing a key, the system also sends a **PBT\_APMRESUMESUSPEND** message after sending PBT\_APMRESUMEAUTOMATIC.</span></span>

<span data-ttu-id="7342a-140">**WM \_** I messaggi POWERBROADCAST non fanno distinzione tra Stati a bassa potenza diversi.</span><span class="sxs-lookup"><span data-stu-id="7342a-140">**WM\_POWERBROADCAST** messages do not distinguish between different low-power states.</span></span> <span data-ttu-id="7342a-141">Un'applicazione può determinare solo che il sistema è in entrata o è stato ripreso da uno stato di basso consumo; non è in grado di determinare lo stato di alimentazione specifico.</span><span class="sxs-lookup"><span data-stu-id="7342a-141">An application can determine only that the system is entering or has resumed from a low-power state; it cannot determine the specific power state.</span></span> <span data-ttu-id="7342a-142">Il sistema registra informazioni dettagliate sulle transizioni di stato dell'alimentazione nel registro eventi di sistema di Windows.</span><span class="sxs-lookup"><span data-stu-id="7342a-142">The system records details about power state transitions in the Windows System event log.</span></span>

<span data-ttu-id="7342a-143">Per impedire che il sistema passi a uno stato di basso consumo in Windows Vista, un'applicazione deve chiamare [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) per informare il sistema che è in uso.</span><span class="sxs-lookup"><span data-stu-id="7342a-143">To prevent the system from transitioning to a low-power state in Windows Vista, an application must call [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) to inform the system that it is in use.</span></span>

<span data-ttu-id="7342a-144">I messaggi seguenti non sono supportati in nessuno dei sistemi operativi specificati nella sezione requisiti:</span><span class="sxs-lookup"><span data-stu-id="7342a-144">The following messages are not supported on any of the operating systems specified in the Requirements section:</span></span>

- <span data-ttu-id="7342a-145">PBT_APMQUERYSTANDBY</span><span class="sxs-lookup"><span data-stu-id="7342a-145">PBT_APMQUERYSTANDBY</span></span>  
- <span data-ttu-id="7342a-146">PBT_APMQUERYSTANDBYFAILED</span><span class="sxs-lookup"><span data-stu-id="7342a-146">PBT_APMQUERYSTANDBYFAILED</span></span>  
- <span data-ttu-id="7342a-147">PBT_APMSTANDBY</span><span class="sxs-lookup"><span data-stu-id="7342a-147">PBT_APMSTANDBY</span></span>  
- <span data-ttu-id="7342a-148">PBT_APMRESUMESTANDBY</span><span class="sxs-lookup"><span data-stu-id="7342a-148">PBT_APMRESUMESTANDBY</span></span>  

## <a name="requirements"></a><span data-ttu-id="7342a-149">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7342a-149">Requirements</span></span>



| <span data-ttu-id="7342a-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="7342a-150">Requirement</span></span> | <span data-ttu-id="7342a-151">Valore</span><span class="sxs-lookup"><span data-stu-id="7342a-151">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7342a-152">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7342a-152">Minimum supported client</span></span><br/> | <span data-ttu-id="7342a-153">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="7342a-153">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="7342a-154">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7342a-154">Minimum supported server</span></span><br/> | <span data-ttu-id="7342a-155">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7342a-155">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7342a-156">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7342a-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="7342a-157"><dt>WinUser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7342a-157"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7342a-158">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7342a-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7342a-159">\_Messaggi WM POWERBROADCAST</span><span class="sxs-lookup"><span data-stu-id="7342a-159">WM\_POWERBROADCAST Messages</span></span>](wm-powerbroadcast-messages.md)
</dt> <dt>

[<span data-ttu-id="7342a-160">Messaggi di risparmio energia</span><span class="sxs-lookup"><span data-stu-id="7342a-160">Power Management Messages</span></span>](power-management-messages.md)
</dt> </dl>

 

 




