---
description: Il \_ messaggio WM ENDSESSION viene inviato a un'applicazione dopo che il sistema ha elaborato i risultati del \_ messaggio WM QUERYENDSESSION. Il \_ messaggio WM ENDSESSION informa l'applicazione se la sessione sta terminando.
ms.assetid: 9bf04f24-da1e-4680-a47b-28e9c500635e
title: Messaggio WM_ENDSESSION (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa62f356d881182dd6e6fd9e0558332bcc1b3fc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308621"
---
# <a name="wm_endsession-message"></a><span data-ttu-id="bd485-104">\_Messaggio ENDSESSION WM</span><span class="sxs-lookup"><span data-stu-id="bd485-104">WM\_ENDSESSION message</span></span>

<span data-ttu-id="bd485-105">Il messaggio **WM \_ ENDSESSION** viene inviato a un'applicazione dopo che il sistema ha elaborato i risultati del messaggio [**WM \_ QUERYENDSESSION**](wm-queryendsession.md) .</span><span class="sxs-lookup"><span data-stu-id="bd485-105">The **WM\_ENDSESSION** message is sent to an application after the system processes the results of the [**WM\_QUERYENDSESSION**](wm-queryendsession.md) message.</span></span> <span data-ttu-id="bd485-106">Il messaggio **WM \_ ENDSESSION** informa l'applicazione se la sessione sta terminando.</span><span class="sxs-lookup"><span data-stu-id="bd485-106">The **WM\_ENDSESSION** message informs the application whether the session is ending.</span></span>

<span data-ttu-id="bd485-107">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="bd485-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc( 
  HWND hwnd,      // handle to window 
  UINT uMsg,      // message identifier 
  WPARAM wParam,  // end-session option 
  LPARAM lParam   // logoff option
);
```



## <a name="parameters"></a><span data-ttu-id="bd485-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="bd485-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd485-109">*HWND*</span><span class="sxs-lookup"><span data-stu-id="bd485-109">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="bd485-110">Handle per la finestra.</span><span class="sxs-lookup"><span data-stu-id="bd485-110">A handle to the window.</span></span>

</dd> <dt>

<span data-ttu-id="bd485-111">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="bd485-111">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="bd485-112">Identificatore **WM \_ ENDSESSION** .</span><span class="sxs-lookup"><span data-stu-id="bd485-112">The **WM\_ENDSESSION** identifier.</span></span>

</dd> <dt>

<span data-ttu-id="bd485-113">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bd485-113">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bd485-114">Se la sessione viene terminata, questo parametro è **true**; la sessione può terminare in qualsiasi momento dopo che tutte le applicazioni sono state restituite dall'elaborazione del messaggio.</span><span class="sxs-lookup"><span data-stu-id="bd485-114">If the session is being ended, this parameter is **TRUE**; the session can end any time after all applications have returned from processing this message.</span></span> <span data-ttu-id="bd485-115">In caso contrario, è **false**.</span><span class="sxs-lookup"><span data-stu-id="bd485-115">Otherwise, it is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="bd485-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bd485-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bd485-117">Il parametro può essere costituito da uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="bd485-117">This parameter can be one or more of the following values.</span></span> <span data-ttu-id="bd485-118">Se questo parametro è 0, il sistema viene arrestato o riavviato. non è possibile determinare l'evento che si sta verificando.</span><span class="sxs-lookup"><span data-stu-id="bd485-118">If this parameter is 0, the system is shutting down or restarting (it is not possible to determine which event is occurring).</span></span>



| <span data-ttu-id="bd485-119">Valore</span><span class="sxs-lookup"><span data-stu-id="bd485-119">Value</span></span>                                                                                                                                                                                                                                           | <span data-ttu-id="bd485-120">Significato</span><span class="sxs-lookup"><span data-stu-id="bd485-120">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ENDSESSION_CLOSEAPP"></span><span id="endsession_closeapp"></span><dl> <span data-ttu-id="bd485-121"><dt>**ENDSESSION \_**</dt> <dt>0x1</dt> CLOSEAPP</span><span class="sxs-lookup"><span data-stu-id="bd485-121"><dt>**ENDSESSION\_CLOSEAPP**</dt> <dt>0x1</dt></span></span> </dl>        | <span data-ttu-id="bd485-122">Se *wParam* è **true**, l'applicazione deve essere arrestata.</span><span class="sxs-lookup"><span data-stu-id="bd485-122">If *wParam* is **TRUE**, the application must shut down.</span></span> <span data-ttu-id="bd485-123">Tutti i dati devono essere salvati automaticamente senza richiedere conferma all'utente. per ulteriori informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="bd485-123">Any data should be saved automatically without prompting the user (for more information, see Remarks).</span></span> <span data-ttu-id="bd485-124">Gestione riavvio Invia questo messaggio quando l'applicazione utilizza un file che deve essere sostituito, quando deve servire il sistema o quando le risorse di sistema sono esaurite.</span><span class="sxs-lookup"><span data-stu-id="bd485-124">The Restart Manager sends this message when the application is using a file that needs to be replaced, when it must service the system, or when system resources are exhausted.</span></span> <span data-ttu-id="bd485-125">L'applicazione verrà riavviata se è stata registrata per il riavvio utilizzando la funzione [**RegisterApplicationRestart**](/windows/win32/api/winbase/nf-winbase-registerapplicationrestart) .</span><span class="sxs-lookup"><span data-stu-id="bd485-125">The application will be restarted if it has registered for restart using the [**RegisterApplicationRestart**](/windows/win32/api/winbase/nf-winbase-registerapplicationrestart) function.</span></span> <span data-ttu-id="bd485-126">Per ulteriori informazioni, vedere [linee guida per le applicazioni](../rstmgr/guidelines-for-applications.md).</span><span class="sxs-lookup"><span data-stu-id="bd485-126">For more information, see [Guidelines for Applications](../rstmgr/guidelines-for-applications.md).</span></span> <br/> <span data-ttu-id="bd485-127">Se *wParam* è **false**, l'applicazione non deve essere arrestata.</span><span class="sxs-lookup"><span data-stu-id="bd485-127">If *wParam* is **FALSE**, the application should not shut down.</span></span><br/> |
| <span id="ENDSESSION_CRITICAL"></span><span id="endsession_critical"></span><dl> <span data-ttu-id="bd485-128"><dt>**ENDSESSION \_**</dt> <dt>0x40000000</dt> critico</span><span class="sxs-lookup"><span data-stu-id="bd485-128"><dt>**ENDSESSION\_CRITICAL**</dt> <dt>0x40000000</dt></span></span> </dl> | <span data-ttu-id="bd485-129">È necessario arrestare l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bd485-129">The application is forced to shut down.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="ENDSESSION_LOGOFF"></span><span id="endsession_logoff"></span><dl> <span data-ttu-id="bd485-130"><dt>**ENDSESSION \_**</dt> <dt>0x80000000</dt> di disconnessione</span><span class="sxs-lookup"><span data-stu-id="bd485-130"><dt>**ENDSESSION\_LOGOFF**</dt> <dt>0x80000000</dt></span></span> </dl>       | <span data-ttu-id="bd485-131">L'utente si sta disconnettendo.</span><span class="sxs-lookup"><span data-stu-id="bd485-131">The user is logging off.</span></span> <span data-ttu-id="bd485-132">Per ulteriori informazioni, vedere [disconnessione](logging-off.md).</span><span class="sxs-lookup"><span data-stu-id="bd485-132">For more information, see [Logging Off](logging-off.md).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

<span data-ttu-id="bd485-133">Si noti che questo parametro è una maschera di bit.</span><span class="sxs-lookup"><span data-stu-id="bd485-133">Note that this parameter is a bit mask.</span></span> <span data-ttu-id="bd485-134">Per eseguire il test di questo valore, utilizzare un'operazione bit. non verificare l'uguaglianza.</span><span class="sxs-lookup"><span data-stu-id="bd485-134">To test for this value, use a bit-wise operation; do not test for equality.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd485-135">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bd485-135">Return value</span></span>

<span data-ttu-id="bd485-136">Se un'applicazione elabora il messaggio, deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="bd485-136">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd485-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="bd485-137">Remarks</span></span>

<span data-ttu-id="bd485-138">Le applicazioni con dati non salvati potrebbero salvare i dati in un percorso temporaneo e ripristinarli al successivo avvio dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bd485-138">Applications that have unsaved data could save the data to a temporary location and restore it the next time the application starts.</span></span> <span data-ttu-id="bd485-139">È consigliabile che le applicazioni salvino i dati e lo stato di frequente; ad esempio, salvare automaticamente i dati tra le operazioni di salvataggio avviate dall'utente per ridurre la quantità di dati da salvare al momento dell'arresto.</span><span class="sxs-lookup"><span data-stu-id="bd485-139">It is recommended that applications save their data and state frequently; for example, automatically save data between save operations initiated by the user to reduce the amount of data to be saved at shutdown.</span></span>

<span data-ttu-id="bd485-140">L'applicazione non deve chiamare la funzione [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) o [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) alla fine della sessione.</span><span class="sxs-lookup"><span data-stu-id="bd485-140">The application need not call the [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) or [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) function when the session is ending.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd485-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bd485-141">Requirements</span></span>



| <span data-ttu-id="bd485-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd485-142">Requirement</span></span> | <span data-ttu-id="bd485-143">Valore</span><span class="sxs-lookup"><span data-stu-id="bd485-143">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd485-144">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bd485-144">Minimum supported client</span></span><br/> | <span data-ttu-id="bd485-145">App desktop di Windows XP \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="bd485-145">Windows XP \[desktop apps \| UWP apps\]</span></span><br/>                                                       |
| <span data-ttu-id="bd485-146">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bd485-146">Minimum supported server</span></span><br/> | <span data-ttu-id="bd485-147">App UWP per \[ app desktop di Windows Server 2003 \|\]</span><span class="sxs-lookup"><span data-stu-id="bd485-147">Windows Server 2003 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="bd485-148">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bd485-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd485-149"><dt>WinUser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bd485-149"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd485-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bd485-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd485-151">Disconnessione</span><span class="sxs-lookup"><span data-stu-id="bd485-151">Logging Off</span></span>](logging-off.md)
</dt> <dt>

[<span data-ttu-id="bd485-152">Chiusura in corso</span><span class="sxs-lookup"><span data-stu-id="bd485-152">Shutting Down</span></span>](shutting-down.md)
</dt> <dt>

[<span data-ttu-id="bd485-153">**DestroyWindow**</span><span class="sxs-lookup"><span data-stu-id="bd485-153">**DestroyWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-destroywindow)
</dt> <dt>

[<span data-ttu-id="bd485-154">**PostQuitMessage**</span><span class="sxs-lookup"><span data-stu-id="bd485-154">**PostQuitMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-postquitmessage)
</dt> <dt>

[<span data-ttu-id="bd485-155">**SetProcessShutdownParameters**</span><span class="sxs-lookup"><span data-stu-id="bd485-155">**SetProcessShutdownParameters**</span></span>](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocessshutdownparameters)
</dt> <dt>

[<span data-ttu-id="bd485-156">**\_QUERYENDSESSION WM**</span><span class="sxs-lookup"><span data-stu-id="bd485-156">**WM\_QUERYENDSESSION**</span></span>](wm-queryendsession.md)
</dt> </dl>

 

 
