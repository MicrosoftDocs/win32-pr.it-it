---
description: Il \_ messaggio WM QUERYENDSESSION viene inviato quando l'utente sceglie di terminare la sessione o quando un'applicazione chiama una delle funzioni di arresto del sistema.
ms.assetid: 7ad73444-f1f6-4b73-8450-0580b146a5a6
title: Messaggio WM_QUERYENDSESSION (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff2e2f82388b229523f371c680d6ccc7c4b1e27f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318612"
---
# <a name="wm_queryendsession-message"></a><span data-ttu-id="9e232-103">\_Messaggio QUERYENDSESSION WM</span><span class="sxs-lookup"><span data-stu-id="9e232-103">WM\_QUERYENDSESSION message</span></span>

<span data-ttu-id="9e232-104">Il messaggio **WM \_ QUERYENDSESSION** viene inviato quando l'utente sceglie di terminare la sessione o quando un'applicazione chiama una delle funzioni di arresto del sistema.</span><span class="sxs-lookup"><span data-stu-id="9e232-104">The **WM\_QUERYENDSESSION** message is sent when the user chooses to end the session or when an application calls one of the system shutdown functions.</span></span> <span data-ttu-id="9e232-105">Se un'applicazione restituisce zero, la sessione non viene terminata.</span><span class="sxs-lookup"><span data-stu-id="9e232-105">If any application returns zero, the session is not ended.</span></span> <span data-ttu-id="9e232-106">Il sistema smette di inviare messaggi **WM \_ QUERYENDSESSION** non appena un'applicazione restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="9e232-106">The system stops sending **WM\_QUERYENDSESSION** messages as soon as one application returns zero.</span></span>

<span data-ttu-id="9e232-107">Dopo l'elaborazione del messaggio, il sistema invia il messaggio [**WM \_ ENDSESSION**](wm-endsession.md) con il parametro *wParam* impostato sui risultati del messaggio **WM \_ QUERYENDSESSION** .</span><span class="sxs-lookup"><span data-stu-id="9e232-107">After processing this message, the system sends the [**WM\_ENDSESSION**](wm-endsession.md) message with the *wParam* parameter set to the results of the **WM\_QUERYENDSESSION** message.</span></span>

<span data-ttu-id="9e232-108">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="9e232-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc( 
  HWND hwnd,      // handle to window 
  UINT uMsg,      // message identifier 
  WPARAM wParam,  // not used 
  LPARAM lParam   // logoff option
);
```



## <a name="parameters"></a><span data-ttu-id="9e232-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="9e232-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e232-110">*HWND*</span><span class="sxs-lookup"><span data-stu-id="9e232-110">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="9e232-111">Handle per la finestra.</span><span class="sxs-lookup"><span data-stu-id="9e232-111">A handle to the window.</span></span>

</dd> <dt>

<span data-ttu-id="9e232-112">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="9e232-112">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="9e232-113">Identificatore **WM \_ QUERYENDSESSION** .</span><span class="sxs-lookup"><span data-stu-id="9e232-113">The **WM\_QUERYENDSESSION** identifier.</span></span>

</dd> <dt>

<span data-ttu-id="9e232-114">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9e232-114">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9e232-115">Questo parametro è riservato per usi futuri.</span><span class="sxs-lookup"><span data-stu-id="9e232-115">This parameter is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="9e232-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9e232-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9e232-117">Il parametro può essere costituito da uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="9e232-117">This parameter can be one or more of the following values.</span></span> <span data-ttu-id="9e232-118">Se questo parametro è 0, il sistema viene arrestato o riavviato. non è possibile determinare l'evento che si sta verificando.</span><span class="sxs-lookup"><span data-stu-id="9e232-118">If this parameter is 0, the system is shutting down or restarting (it is not possible to determine which event is occurring).</span></span>



| <span data-ttu-id="9e232-119">Valore</span><span class="sxs-lookup"><span data-stu-id="9e232-119">Value</span></span>                                                                                                                                                                                                                                           | <span data-ttu-id="9e232-120">Significato</span><span class="sxs-lookup"><span data-stu-id="9e232-120">Meaning</span></span>                                                                                                                                                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ENDSESSION_CLOSEAPP"></span><span id="endsession_closeapp"></span><dl> <span data-ttu-id="9e232-121"><dt>**ENDSESSION \_**</dt> <dt>0x00000001</dt> CLOSEAPP</span><span class="sxs-lookup"><span data-stu-id="9e232-121"><dt>**ENDSESSION\_CLOSEAPP**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="9e232-122">L'applicazione usa un file che deve essere sostituito, il sistema è in fase di manutenzione oppure le risorse di sistema sono esaurite.</span><span class="sxs-lookup"><span data-stu-id="9e232-122">The application is using a file that must be replaced, the system is being serviced, or system resources are exhausted.</span></span> <span data-ttu-id="9e232-123">Per ulteriori informazioni, vedere [linee guida per le applicazioni](../rstmgr/guidelines-for-applications.md).</span><span class="sxs-lookup"><span data-stu-id="9e232-123">For more information, see [Guidelines for Applications](../rstmgr/guidelines-for-applications.md).</span></span><br/> |
| <span id="ENDSESSION_CRITICAL"></span><span id="endsession_critical"></span><dl> <span data-ttu-id="9e232-124"><dt>**ENDSESSION \_**</dt> <dt>0x40000000</dt> critico</span><span class="sxs-lookup"><span data-stu-id="9e232-124"><dt>**ENDSESSION\_CRITICAL**</dt> <dt>0x40000000</dt></span></span> </dl> | <span data-ttu-id="9e232-125">È necessario arrestare l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9e232-125">The application is forced to shut down.</span></span><br/>                                                                                                                                                                              |
| <span id="ENDSESSION_LOGOFF"></span><span id="endsession_logoff"></span><dl> <span data-ttu-id="9e232-126"><dt>**ENDSESSION \_**</dt> <dt>0x80000000</dt> di disconnessione</span><span class="sxs-lookup"><span data-stu-id="9e232-126"><dt>**ENDSESSION\_LOGOFF**</dt> <dt>0x80000000</dt></span></span> </dl>       | <span data-ttu-id="9e232-127">L'utente si sta disconnettendo.</span><span class="sxs-lookup"><span data-stu-id="9e232-127">The user is logging off.</span></span> <span data-ttu-id="9e232-128">Per ulteriori informazioni, vedere [disconnessione](logging-off.md).</span><span class="sxs-lookup"><span data-stu-id="9e232-128">For more information, see [Logging Off](logging-off.md).</span></span><br/>                                                                                                                                   |



 

<span data-ttu-id="9e232-129">Si noti che questo parametro è una maschera di bit.</span><span class="sxs-lookup"><span data-stu-id="9e232-129">Note that this parameter is a bit mask.</span></span> <span data-ttu-id="9e232-130">Per eseguire il test di questo valore, utilizzare un'operazione bit. non verificare l'uguaglianza.</span><span class="sxs-lookup"><span data-stu-id="9e232-130">To test for this value, use a bit-wise operation; do not test for equality.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e232-131">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9e232-131">Return value</span></span>

<span data-ttu-id="9e232-132">Le applicazioni devono rispettare le intenzioni dell'utente e restituire **true**.</span><span class="sxs-lookup"><span data-stu-id="9e232-132">Applications should respect the user's intentions and return **TRUE**.</span></span> <span data-ttu-id="9e232-133">Per impostazione predefinita, la funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) restituisce **true** per questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="9e232-133">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function returns **TRUE** for this message.</span></span>

<span data-ttu-id="9e232-134">Se la chiusura danneggia il sistema o i supporti in fase di masterizzazione, l'applicazione può restituire **false**.</span><span class="sxs-lookup"><span data-stu-id="9e232-134">If shutting down would corrupt the system or media that is being burned, the application can return **FALSE**.</span></span> <span data-ttu-id="9e232-135">Tuttavia, è consigliabile rispettare le azioni dell'utente.</span><span class="sxs-lookup"><span data-stu-id="9e232-135">However, it is good practice to respect the user's actions.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e232-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="9e232-136">Remarks</span></span>

<span data-ttu-id="9e232-137">Quando un'applicazione restituisce **true** per questo messaggio, riceve il messaggio [**WM \_ ENDSESSION**](wm-endsession.md) , indipendentemente dal modo in cui le altre applicazioni rispondono al messaggio **WM \_ QUERYENDSESSION** .</span><span class="sxs-lookup"><span data-stu-id="9e232-137">When an application returns **TRUE** for this message, it receives the [**WM\_ENDSESSION**](wm-endsession.md) message, regardless of how the other applications respond to the **WM\_QUERYENDSESSION** message.</span></span> <span data-ttu-id="9e232-138">Ogni applicazione deve restituire **true** o **false** immediatamente dopo la ricezione del messaggio e rinviare le operazioni di pulizia fino a quando non riceve il messaggio **WM \_ ENDSESSION** .</span><span class="sxs-lookup"><span data-stu-id="9e232-138">Each application should return **TRUE** or **FALSE** immediately upon receiving this message, and defer any cleanup operations until it receives the **WM\_ENDSESSION** message.</span></span>

<span data-ttu-id="9e232-139">Le applicazioni possono visualizzare un'interfaccia utente che richiede all'utente informazioni alla chiusura, tuttavia non è consigliabile.</span><span class="sxs-lookup"><span data-stu-id="9e232-139">Applications can display a user interface prompting the user for information at shutdown, however it is not recommended.</span></span> <span data-ttu-id="9e232-140">Dopo cinque secondi, il sistema Visualizza le informazioni sulle applicazioni che impediscono l'arresto e consente all'utente di terminarle.</span><span class="sxs-lookup"><span data-stu-id="9e232-140">After five seconds, the system displays information about the applications that are preventing shutdown and allows the user to terminate them.</span></span> <span data-ttu-id="9e232-141">Windows XP, ad esempio, Visualizza una finestra di dialogo, mentre Windows Vista Visualizza una schermata a schermo intero con informazioni aggiuntive sulle applicazioni che bloccano l'arresto.</span><span class="sxs-lookup"><span data-stu-id="9e232-141">For example, Windows XP displays a dialog box, while Windows Vista displays a full screen with additional information about the applications blocking shutdown.</span></span> <span data-ttu-id="9e232-142">Se l'applicazione deve bloccare o posticipare l'arresto del sistema, usare la funzione [**ShutdownBlockReasonCreate**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate) .</span><span class="sxs-lookup"><span data-stu-id="9e232-142">If your application must block or postpone system shutdown, use the [**ShutdownBlockReasonCreate**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate) function.</span></span> <span data-ttu-id="9e232-143">Per ulteriori informazioni, vedere [Shutdown changes for Windows Vista](shutdown-changes-for-windows-vista.md).</span><span class="sxs-lookup"><span data-stu-id="9e232-143">For more information, see [Shutdown Changes for Windows Vista](shutdown-changes-for-windows-vista.md).</span></span>

<span data-ttu-id="9e232-144">Le applicazioni console possono utilizzare la funzione [**SetConsoleCtrlHandler**](/windows/console/setconsolectrlhandler) per ricevere la notifica di arresto.</span><span class="sxs-lookup"><span data-stu-id="9e232-144">Console applications can use the [**SetConsoleCtrlHandler**](/windows/console/setconsolectrlhandler) function to receive shutdown notification.</span></span>

<span data-ttu-id="9e232-145">Le applicazioni di servizio possono utilizzare la funzione [**RegisterServiceCtrlHandlerEx**](/windows/win32/api/winsvc/nf-winsvc-registerservicectrlhandlerexa) per ricevere le notifiche di arresto in una routine di gestione.</span><span class="sxs-lookup"><span data-stu-id="9e232-145">Service applications can use the [**RegisterServiceCtrlHandlerEx**](/windows/win32/api/winsvc/nf-winsvc-registerservicectrlhandlerexa) function to receive shutdown notifications in a handler routine.</span></span>

## <a name="examples"></a><span data-ttu-id="9e232-146">Esempio</span><span class="sxs-lookup"><span data-stu-id="9e232-146">Examples</span></span>

<span data-ttu-id="9e232-147">Per un esempio, vedere [disconnessione](logging-off.md).</span><span class="sxs-lookup"><span data-stu-id="9e232-147">For an example, see [Logging Off](logging-off.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9e232-148">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9e232-148">Requirements</span></span>



| <span data-ttu-id="9e232-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e232-149">Requirement</span></span> | <span data-ttu-id="9e232-150">Valore</span><span class="sxs-lookup"><span data-stu-id="9e232-150">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e232-151">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9e232-151">Minimum supported client</span></span><br/> | <span data-ttu-id="9e232-152">App desktop di Windows XP \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="9e232-152">Windows XP \[desktop apps \| UWP apps\]</span></span><br/>                                                       |
| <span data-ttu-id="9e232-153">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9e232-153">Minimum supported server</span></span><br/> | <span data-ttu-id="9e232-154">App UWP per \[ app desktop di Windows Server 2003 \|\]</span><span class="sxs-lookup"><span data-stu-id="9e232-154">Windows Server 2003 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="9e232-155">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9e232-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e232-156"><dt>WinUser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9e232-156"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e232-157">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9e232-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e232-158">Disconnessione</span><span class="sxs-lookup"><span data-stu-id="9e232-158">Logging Off</span></span>](logging-off.md)
</dt> <dt>

[<span data-ttu-id="9e232-159">Chiusura in corso</span><span class="sxs-lookup"><span data-stu-id="9e232-159">Shutting Down</span></span>](shutting-down.md)
</dt> <dt>

[<span data-ttu-id="9e232-160">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="9e232-160">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="9e232-161">**ExitWindows**</span><span class="sxs-lookup"><span data-stu-id="9e232-161">**ExitWindows**</span></span>](/windows/desktop/api/Winuser/nf-winuser-exitwindows)
</dt> <dt>

[<span data-ttu-id="9e232-162">**SetProcessShutdownParameters**</span><span class="sxs-lookup"><span data-stu-id="9e232-162">**SetProcessShutdownParameters**</span></span>](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocessshutdownparameters)
</dt> <dt>

[<span data-ttu-id="9e232-163">**\_ENDSESSION WM**</span><span class="sxs-lookup"><span data-stu-id="9e232-163">**WM\_ENDSESSION**</span></span>](wm-endsession.md)
</dt> </dl>

 

 
