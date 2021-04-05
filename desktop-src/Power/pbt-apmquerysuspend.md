---
description: Richiede l'autorizzazione per sospendere il computer. È necessario che l'applicazione preposta alla concessione delle autorizzazioni effettui tutti i preparativi per la sospensione prima della restituzione.
ms.assetid: 83cb0fdc-437e-4d03-87f0-6a416281c0d5
title: Evento PBT_APMQUERYSUSPEND (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 277e4faf7617037b917dedab3193e421a381166a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881717"
---
# <a name="pbt_apmquerysuspend-event"></a><span data-ttu-id="9dfaf-104">\_Evento APMQUERYSUSPEND PBT</span><span class="sxs-lookup"><span data-stu-id="9dfaf-104">PBT\_APMQUERYSUSPEND event</span></span>

<span data-ttu-id="9dfaf-105">\[PBT \_ APMQUERYSUSPEND è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="9dfaf-105">\[PBT\_APMQUERYSUSPEND is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="9dfaf-106">Il supporto per questo evento è stato rimosso in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9dfaf-106">Support for this event was removed in Windows Vista.</span></span> <span data-ttu-id="9dfaf-107">In alternativa, usare [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) .\]</span><span class="sxs-lookup"><span data-stu-id="9dfaf-107">Use [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) instead.\]</span></span>

<span data-ttu-id="9dfaf-108">Richiede l'autorizzazione per sospendere il computer.</span><span class="sxs-lookup"><span data-stu-id="9dfaf-108">Requests permission to suspend the computer.</span></span> <span data-ttu-id="9dfaf-109">È necessario che l'applicazione preposta alla concessione delle autorizzazioni effettui tutti i preparativi per la sospensione prima della restituzione.</span><span class="sxs-lookup"><span data-stu-id="9dfaf-109">An application that grants permission should carry out preparations for the suspension before returning.</span></span>

<span data-ttu-id="9dfaf-110">Una finestra riceve questo evento tramite il messaggio [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) .</span><span class="sxs-lookup"><span data-stu-id="9dfaf-110">A window receives this event through the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message.</span></span> <span data-ttu-id="9dfaf-111">I parametri *wParam* e *lParam* sono impostati come descritto di seguito.</span><span class="sxs-lookup"><span data-stu-id="9dfaf-111">The *wParam* and *lParam* parameters are set as described following.</span></span>


```C++
LRESULT 
CALLBACK 
WindowProc( HWND   hwnd,    // handle to window
            UINT   uMsg,    // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMQUERYSUSPEND
            LPARAM lParam); // action flags
```



## <a name="parameters"></a><span data-ttu-id="9dfaf-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="9dfaf-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9dfaf-113">*HWND*</span><span class="sxs-lookup"><span data-stu-id="9dfaf-113">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="9dfaf-114">Handle per la finestra.</span><span class="sxs-lookup"><span data-stu-id="9dfaf-114">A handle to window.</span></span>

<span data-ttu-id="9dfaf-115"></dd> <dt>*uMsg*</dt> </span><span class="sxs-lookup"><span data-stu-id="9dfaf-115"></dd> <dt>*uMsg* </dt> </span></span><dd> 

| <span data-ttu-id="9dfaf-116">Valore</span><span class="sxs-lookup"><span data-stu-id="9dfaf-116">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="9dfaf-117">Significato</span><span class="sxs-lookup"><span data-stu-id="9dfaf-117">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <span data-ttu-id="9dfaf-118"><dt>**[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span><span class="sxs-lookup"><span data-stu-id="9dfaf-118"><dt>**[**WM\_POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span></span> </dl> | <span data-ttu-id="9dfaf-119">Identificatore del messaggio.</span><span class="sxs-lookup"><span data-stu-id="9dfaf-119">Message identifier.</span></span><br/> |



 

<span data-ttu-id="9dfaf-120"></dd> <dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="9dfaf-120"></dd> <dt>*wParam* </dt> </span></span><dd> 

| <span data-ttu-id="9dfaf-121">Valore</span><span class="sxs-lookup"><span data-stu-id="9dfaf-121">Value</span></span>                                                                                                                                                                                                                                        | <span data-ttu-id="9dfaf-122">Significato</span><span class="sxs-lookup"><span data-stu-id="9dfaf-122">Meaning</span></span>                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMQUERYSUSPEND"></span><span id="pbt_apmquerysuspend"></span><dl> <span data-ttu-id="9dfaf-123"><dt>**PBT \_ APMQUERYSUSPEND**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="9dfaf-123"><dt>**PBT\_APMQUERYSUSPEND**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="9dfaf-124">Identificatore dell'evento.</span><span class="sxs-lookup"><span data-stu-id="9dfaf-124">Event identifier.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9dfaf-125">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9dfaf-125">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9dfaf-126">Flag di azione.</span><span class="sxs-lookup"><span data-stu-id="9dfaf-126">The action flags.</span></span> <span data-ttu-id="9dfaf-127">Se il bit 0 è 1, l'applicazione può richiedere all'utente le istruzioni per la preparazione della sospensione. in caso contrario, l'applicazione deve essere preparata senza interazione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="9dfaf-127">If bit 0 is 1, the application can prompt the user for directions on how to prepare for the suspension; otherwise, the application must prepare without user interaction.</span></span> <span data-ttu-id="9dfaf-128">Tutti gli altri valori di bit sono riservati.</span><span class="sxs-lookup"><span data-stu-id="9dfaf-128">All other bit values are reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9dfaf-129">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9dfaf-129">Return value</span></span>

<span data-ttu-id="9dfaf-130">Restituisce **true** per concedere la richiesta di sospensione.</span><span class="sxs-lookup"><span data-stu-id="9dfaf-130">Return **TRUE** to grant the request to suspend.</span></span> <span data-ttu-id="9dfaf-131">Per negare la richiesta, restituire la **\_ query broadcast \_ Deny**.</span><span class="sxs-lookup"><span data-stu-id="9dfaf-131">To deny the request, return **BROADCAST\_QUERY\_DENY**.</span></span>

## <a name="remarks"></a><span data-ttu-id="9dfaf-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="9dfaf-132">Remarks</span></span>

<span data-ttu-id="9dfaf-133">Un'applicazione deve elaborare questo evento il più rapidamente possibile.</span><span class="sxs-lookup"><span data-stu-id="9dfaf-133">An application should process this event as quickly as possible.</span></span> <span data-ttu-id="9dfaf-134">L'applicazione può richiedere all'utente indicazioni su come prepararsi per la sospensione solo se è impostato il bit 0 nel parametro *Flags* .</span><span class="sxs-lookup"><span data-stu-id="9dfaf-134">The application can prompt the user for directions on how to prepare for suspension only if bit 0 in the *Flags* parameter is set.</span></span> <span data-ttu-id="9dfaf-135">Tuttavia, se questo messaggio viene emesso perché l'utente sta chiudendo il coperchio del portatile, non sarà possibile richiedere l'intervento dell'utente.</span><span class="sxs-lookup"><span data-stu-id="9dfaf-135">However, if this message is issued because the user is closing the laptop lid, it will not be possible to prompt the user.</span></span> <span data-ttu-id="9dfaf-136">Le applicazioni devono rispettare il fatto che l'utente si aspetta un certo comportamento quando chiude il coperchio del portatile oppure preme il pulsante di alimentazione e consente la riuscita della transizione.</span><span class="sxs-lookup"><span data-stu-id="9dfaf-136">Applications should respect that the user expects a certain behavior when they close the laptop lid or press the power button and allow the transition to succeed.</span></span>

<span data-ttu-id="9dfaf-137">Il sistema consente circa 20 secondi prima che un'applicazione rimuova il messaggio [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) che invia l' \_ evento PBT APMQUERYSUSPEND dalla coda di messaggi dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9dfaf-137">The system allows approximately 20 seconds for an application to remove the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message that is sending the PBT\_APMQUERYSUSPEND event from the application's message queue.</span></span> <span data-ttu-id="9dfaf-138">Se un'applicazione non rimuove il messaggio dalla coda in meno di 20 secondi, il sistema presuppone che l'applicazione sia in uno stato non reattivo e che l'applicazione accetti la richiesta di sospensione.</span><span class="sxs-lookup"><span data-stu-id="9dfaf-138">If an application does not remove the message from its queue in less than 20 seconds, the system will assume that the application is in a non-responsive state, and that the application agrees to the sleep request.</span></span> <span data-ttu-id="9dfaf-139">Le operazioni delle applicazioni che non elaborano le code di messaggi potrebbero essere interrotte.</span><span class="sxs-lookup"><span data-stu-id="9dfaf-139">Applications that do not process their message queues may have their operations interrupted.</span></span> <span data-ttu-id="9dfaf-140">Dopo la rimozione del messaggio dalla coda di messaggi, un'applicazione può richiedere il tempo necessario per eseguire le operazioni necessarie prima di entrare nello stato di sospensione.</span><span class="sxs-lookup"><span data-stu-id="9dfaf-140">After it removes the message from the message queue, an application can take as much time as needed to perform any required operations before entering the sleep state.</span></span> <span data-ttu-id="9dfaf-141">Tutte le operazioni che potrebbero richiedere più di 20 secondi devono essere eseguite in questo momento, perché il sistema consente solo 20 secondi per il completamento delle operazioni durante l'elaborazione del [ \_ APMSUSPEND PBT](pbt-apmsuspend.md) .</span><span class="sxs-lookup"><span data-stu-id="9dfaf-141">Any operations that could take longer then 20 seconds should be performed at this time, since the system allows only 20 seconds for operations to complete during [PBT\_APMSUSPEND](pbt-apmsuspend.md) processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="9dfaf-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9dfaf-142">Requirements</span></span>



| <span data-ttu-id="9dfaf-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="9dfaf-143">Requirement</span></span> | <span data-ttu-id="9dfaf-144">Valore</span><span class="sxs-lookup"><span data-stu-id="9dfaf-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9dfaf-145">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9dfaf-145">Minimum supported client</span></span><br/> | <span data-ttu-id="9dfaf-146">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="9dfaf-146">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="9dfaf-147">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9dfaf-147">Minimum supported server</span></span><br/> | <span data-ttu-id="9dfaf-148">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9dfaf-148">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9dfaf-149">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="9dfaf-149">End of client support</span></span><br/>    | <span data-ttu-id="9dfaf-150">Windows XP</span><span class="sxs-lookup"><span data-stu-id="9dfaf-150">Windows XP</span></span><br/>                                                                                    |
| <span data-ttu-id="9dfaf-151">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="9dfaf-151">End of server support</span></span><br/>    | <span data-ttu-id="9dfaf-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9dfaf-152">Windows Server 2003</span></span><br/>                                                                           |
| <span data-ttu-id="9dfaf-153">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9dfaf-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="9dfaf-154"><dt>WinUser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9dfaf-154"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9dfaf-155">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9dfaf-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9dfaf-156">Eventi di riattivazione del sistema</span><span class="sxs-lookup"><span data-stu-id="9dfaf-156">System Wake-up Events</span></span>](system-wake-up-events.md)
</dt> <dt>

[<span data-ttu-id="9dfaf-157">Eventi di risparmio energia</span><span class="sxs-lookup"><span data-stu-id="9dfaf-157">Power Management Events</span></span>](power-management-events.md)
</dt> <dt>

[<span data-ttu-id="9dfaf-158">\_APMSUSPEND PBT</span><span class="sxs-lookup"><span data-stu-id="9dfaf-158">PBT\_APMSUSPEND</span></span>](pbt-apmsuspend.md)
</dt> <dt>

[<span data-ttu-id="9dfaf-159">**\_POWERBROADCAST WM**</span><span class="sxs-lookup"><span data-stu-id="9dfaf-159">**WM\_POWERBROADCAST**</span></span>](wm-powerbroadcast.md)
</dt> </dl>

 

 




