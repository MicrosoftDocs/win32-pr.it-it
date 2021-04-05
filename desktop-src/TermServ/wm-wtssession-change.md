---
title: Messaggio WM_WTSSESSION_CHANGE (winuser. h)
description: Notifica alle applicazioni le modifiche dello stato della sessione.
ms.assetid: 758a130c-b75a-40fd-8530-3766aa86c5ba
ms.tgt_platform: multiple
keywords:
- Messaggio WM_WTSSESSION_CHANGE Servizi Desktop remoto
topic_type:
- apiref
api_name:
- WM_WTSSESSION_CHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db8f1dc421aa160824a194588711e84f961ea4dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740170"
---
# <a name="wm_wtssession_change-message"></a><span data-ttu-id="ec6d8-104">Messaggio di modifica di WM \_ WTSSESSION \_</span><span class="sxs-lookup"><span data-stu-id="ec6d8-104">WM\_WTSSESSION\_CHANGE message</span></span>

<span data-ttu-id="ec6d8-105">Notifica alle applicazioni le modifiche dello stato della sessione.</span><span class="sxs-lookup"><span data-stu-id="ec6d8-105">Notifies applications of changes in session state.</span></span>

<span data-ttu-id="ec6d8-106">La finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="ec6d8-106">The window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hWnd,       // handle to window
  UINT Msg,        // WM_WTSSESSION_CHANGE
  WPARAM wParam,   // session state change event
  LPARAM lParam    // session ID
);
```



## <a name="parameters"></a><span data-ttu-id="ec6d8-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="ec6d8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec6d8-108">*HWND* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ec6d8-108">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec6d8-109">Handle per la finestra.</span><span class="sxs-lookup"><span data-stu-id="ec6d8-109">Handle to the window.</span></span>

</dd> <dt>

<span data-ttu-id="ec6d8-110">*Messaggio* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ec6d8-110">*Msg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec6d8-111">Specifica il messaggio (**\_ \_ modifica WM WTSSESSION**).</span><span class="sxs-lookup"><span data-stu-id="ec6d8-111">Specifies the message (**WM\_WTSSESSION\_CHANGE**).</span></span>

</dd> <dt>

<span data-ttu-id="ec6d8-112">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ec6d8-112">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec6d8-113">Codice di stato che descrive il motivo per cui è stata inviata la notifica di modifica dello stato della sessione.</span><span class="sxs-lookup"><span data-stu-id="ec6d8-113">Status code describing the reason the session state change notification was sent.</span></span> <span data-ttu-id="ec6d8-114">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="ec6d8-114">This parameter can be one of the following values.</span></span>

<dt>

<span id="WTS_CONSOLE_CONNECT"></span><span id="wts_console_connect"></span>

<span data-ttu-id="ec6d8-115"><span id="WTS_CONSOLE_CONNECT"></span><span id="wts_console_connect"></span>**WTS \_ \_Connessione alla console** (0x1)</span><span class="sxs-lookup"><span data-stu-id="ec6d8-115"><span id="WTS_CONSOLE_CONNECT"></span><span id="wts_console_connect"></span>**WTS\_CONSOLE\_CONNECT** (0x1)</span></span>


</dt> <dd>

<span data-ttu-id="ec6d8-116">La sessione identificata da *lParam* è stata connessa al terminale della console o alla sessione RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="ec6d8-116">The session identified by *lParam* was connected to the console terminal or RemoteFX session.</span></span>

</dd> <dt>

<span id="WTS_CONSOLE_DISCONNECT"></span><span id="wts_console_disconnect"></span>

<span data-ttu-id="ec6d8-117"><span id="WTS_CONSOLE_DISCONNECT"></span><span id="wts_console_disconnect"></span>**WTS \_ \_Disconnessione della console** (0x2)</span><span class="sxs-lookup"><span data-stu-id="ec6d8-117"><span id="WTS_CONSOLE_DISCONNECT"></span><span id="wts_console_disconnect"></span>**WTS\_CONSOLE\_DISCONNECT** (0x2)</span></span>


</dt> <dd>

<span data-ttu-id="ec6d8-118">La sessione identificata da *lParam* è stata disconnessa dal terminale della console o dalla sessione RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="ec6d8-118">The session identified by *lParam* was disconnected from the console terminal or RemoteFX session.</span></span>

</dd> <dt>

<span id="WTS_REMOTE_CONNECT"></span><span id="wts_remote_connect"></span>

<span data-ttu-id="ec6d8-119"><span id="WTS_REMOTE_CONNECT"></span><span id="wts_remote_connect"></span>**WTS \_ \_Connessione remota** (0x3)</span><span class="sxs-lookup"><span data-stu-id="ec6d8-119"><span id="WTS_REMOTE_CONNECT"></span><span id="wts_remote_connect"></span>**WTS\_REMOTE\_CONNECT** (0x3)</span></span>


</dt> <dd>

<span data-ttu-id="ec6d8-120">La sessione identificata da *lParam* è stata connessa al terminale remoto.</span><span class="sxs-lookup"><span data-stu-id="ec6d8-120">The session identified by *lParam* was connected to the remote terminal.</span></span>

</dd> <dt>

<span id="WTS_REMOTE_DISCONNECT"></span><span id="wts_remote_disconnect"></span>

<span data-ttu-id="ec6d8-121"><span id="WTS_REMOTE_DISCONNECT"></span><span id="wts_remote_disconnect"></span>**WTS \_ \_Disconnessione remota** (0x4)</span><span class="sxs-lookup"><span data-stu-id="ec6d8-121"><span id="WTS_REMOTE_DISCONNECT"></span><span id="wts_remote_disconnect"></span>**WTS\_REMOTE\_DISCONNECT** (0x4)</span></span>


</dt> <dd>

<span data-ttu-id="ec6d8-122">La sessione identificata da *lParam* è stata disconnessa dal terminale remoto.</span><span class="sxs-lookup"><span data-stu-id="ec6d8-122">The session identified by *lParam* was disconnected from the remote terminal.</span></span>

</dd> <dt>

<span id="WTS_SESSION_LOGON"></span><span id="wts_session_logon"></span>

<span data-ttu-id="ec6d8-123"><span id="WTS_SESSION_LOGON"></span><span id="wts_session_logon"></span>**WTS \_ \_Accesso alla sessione** (0x5)</span><span class="sxs-lookup"><span data-stu-id="ec6d8-123"><span id="WTS_SESSION_LOGON"></span><span id="wts_session_logon"></span>**WTS\_SESSION\_LOGON** (0x5)</span></span>


</dt> <dd>

<span data-ttu-id="ec6d8-124">Un utente ha effettuato l'accesso alla sessione identificata da *lParam*.</span><span class="sxs-lookup"><span data-stu-id="ec6d8-124">A user has logged on to the session identified by *lParam*.</span></span>

</dd> <dt>

<span id="WTS_SESSION_LOGOFF"></span><span id="wts_session_logoff"></span>

<span data-ttu-id="ec6d8-125"><span id="WTS_SESSION_LOGOFF"></span><span id="wts_session_logoff"></span>**WTS \_ \_Disconnessione della sessione** (0x6)</span><span class="sxs-lookup"><span data-stu-id="ec6d8-125"><span id="WTS_SESSION_LOGOFF"></span><span id="wts_session_logoff"></span>**WTS\_SESSION\_LOGOFF** (0x6)</span></span>


</dt> <dd>

<span data-ttu-id="ec6d8-126">Un utente ha disconnesso la sessione identificata da *lParam*.</span><span class="sxs-lookup"><span data-stu-id="ec6d8-126">A user has logged off the session identified by *lParam*.</span></span>

</dd> <dt>

<span id="WTS_SESSION_LOCK"></span><span id="wts_session_lock"></span>

<span data-ttu-id="ec6d8-127"><span id="WTS_SESSION_LOCK"></span><span id="wts_session_lock"></span>**WTS \_ \_Blocco della sessione** (0x7)</span><span class="sxs-lookup"><span data-stu-id="ec6d8-127"><span id="WTS_SESSION_LOCK"></span><span id="wts_session_lock"></span>**WTS\_SESSION\_LOCK** (0x7)</span></span>


</dt> <dd>

<span data-ttu-id="ec6d8-128">La sessione identificata da *lParam* è stata bloccata.</span><span class="sxs-lookup"><span data-stu-id="ec6d8-128">The session identified by *lParam* has been locked.</span></span>

</dd> <dt>

<span id="WTS_SESSION_UNLOCK"></span><span id="wts_session_unlock"></span>

<span data-ttu-id="ec6d8-129"><span id="WTS_SESSION_UNLOCK"></span><span id="wts_session_unlock"></span>**WTS \_ \_Sblocco della sessione** (0x8)</span><span class="sxs-lookup"><span data-stu-id="ec6d8-129"><span id="WTS_SESSION_UNLOCK"></span><span id="wts_session_unlock"></span>**WTS\_SESSION\_UNLOCK** (0x8)</span></span>


</dt> <dd>

<span data-ttu-id="ec6d8-130">La sessione identificata da *lParam* è stata sbloccata.</span><span class="sxs-lookup"><span data-stu-id="ec6d8-130">The session identified by *lParam* has been unlocked.</span></span>

</dd> <dt>

<span id="WTS_SESSION_REMOTE_CONTROL"></span><span id="wts_session_remote_control"></span>

<span data-ttu-id="ec6d8-131"><span id="WTS_SESSION_REMOTE_CONTROL"></span><span id="wts_session_remote_control"></span>**WTS \_ \_ \_ Controllo remoto sessione** (0x9)</span><span class="sxs-lookup"><span data-stu-id="ec6d8-131"><span id="WTS_SESSION_REMOTE_CONTROL"></span><span id="wts_session_remote_control"></span>**WTS\_SESSION\_REMOTE\_CONTROL** (0x9)</span></span>


</dt> <dd>

<span data-ttu-id="ec6d8-132">La sessione identificata da *lParam* ha modificato lo stato di controllo remoto.</span><span class="sxs-lookup"><span data-stu-id="ec6d8-132">The session identified by *lParam* has changed its remote controlled status.</span></span> <span data-ttu-id="ec6d8-133">Per determinare lo stato, chiamare [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) e controllare la **metrica \_ RemoteControl di SM** .</span><span class="sxs-lookup"><span data-stu-id="ec6d8-133">To determine the status, call [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) and check the **SM\_REMOTECONTROL** metric.</span></span>

</dd> <dt>

<span id="WTS_SESSION_CREATE"></span><span id="wts_session_create"></span>

<span data-ttu-id="ec6d8-134"><span id="WTS_SESSION_CREATE"></span><span id="wts_session_create"></span>**WTS \_ \_Creazione della sessione** (0xA)</span><span class="sxs-lookup"><span data-stu-id="ec6d8-134"><span id="WTS_SESSION_CREATE"></span><span id="wts_session_create"></span>**WTS\_SESSION\_CREATE** (0xA)</span></span>


</dt> <dd>

<span data-ttu-id="ec6d8-135">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="ec6d8-135">Reserved for future use.</span></span>

</dd> <dt>

<span id="WTS_SESSION_TERMINATE"></span><span id="wts_session_terminate"></span>

<span data-ttu-id="ec6d8-136"><span id="WTS_SESSION_TERMINATE"></span><span id="wts_session_terminate"></span>**WTS \_ \_Terminazione sessione** (0xB)</span><span class="sxs-lookup"><span data-stu-id="ec6d8-136"><span id="WTS_SESSION_TERMINATE"></span><span id="wts_session_terminate"></span>**WTS\_SESSION\_TERMINATE** (0xB)</span></span>


</dt> <dd>

<span data-ttu-id="ec6d8-137">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="ec6d8-137">Reserved for future use.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="ec6d8-138">*lParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ec6d8-138">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec6d8-139">Identificatore della sessione.</span><span class="sxs-lookup"><span data-stu-id="ec6d8-139">The identifier of the session.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec6d8-140">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ec6d8-140">Return value</span></span>

<span data-ttu-id="ec6d8-141">Il valore restituito viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="ec6d8-141">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec6d8-142">Commenti</span><span class="sxs-lookup"><span data-stu-id="ec6d8-142">Remarks</span></span>

<span data-ttu-id="ec6d8-143">Questo messaggio viene inviato solo alle applicazioni che hanno effettuato la registrazione per ricevere questo messaggio chiamando [**WTSRegisterSessionNotification**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsregistersessionnotification).</span><span class="sxs-lookup"><span data-stu-id="ec6d8-143">This message is sent only to applications that have registered to receive this message by calling [**WTSRegisterSessionNotification**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsregistersessionnotification).</span></span>

<span data-ttu-id="ec6d8-144">Esempi di come le applicazioni possono rispondere a questo messaggio includono il rilascio o l'acquisizione di risorse specifiche della console, la determinazione della modalità di disegno di una schermata o l'attivazione degli effetti di animazione della console.</span><span class="sxs-lookup"><span data-stu-id="ec6d8-144">Examples of how applications can respond to this message include releasing or acquiring console-specific resources, determining how a screen is to be painted, or triggering console animation effects.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec6d8-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ec6d8-145">Requirements</span></span>



| <span data-ttu-id="ec6d8-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec6d8-146">Requirement</span></span> | <span data-ttu-id="ec6d8-147">Valore</span><span class="sxs-lookup"><span data-stu-id="ec6d8-147">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec6d8-148">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ec6d8-148">Minimum supported client</span></span><br/> | <span data-ttu-id="ec6d8-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ec6d8-149">Windows Vista</span></span><br/>                                                                                 |
| <span data-ttu-id="ec6d8-150">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ec6d8-150">Minimum supported server</span></span><br/> | <span data-ttu-id="ec6d8-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ec6d8-151">Windows Server 2008</span></span><br/>                                                                           |
| <span data-ttu-id="ec6d8-152">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ec6d8-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec6d8-153"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ec6d8-153"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec6d8-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ec6d8-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec6d8-155">**WTSRegisterSessionNotification**</span><span class="sxs-lookup"><span data-stu-id="ec6d8-155">**WTSRegisterSessionNotification**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsregistersessionnotification)
</dt> <dt>

[<span data-ttu-id="ec6d8-156">**WTSUnRegisterSessionNotification**</span><span class="sxs-lookup"><span data-stu-id="ec6d8-156">**WTSUnRegisterSessionNotification**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsunregistersessionnotification)
</dt> </dl>

 

