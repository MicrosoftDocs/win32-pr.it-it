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
# <a name="wm_wtssession_change-message"></a>Messaggio di modifica di WM \_ WTSSESSION \_

Notifica alle applicazioni le modifiche dello stato della sessione.

La finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
LRESULT CALLBACK WindowProc(
  HWND hWnd,       // handle to window
  UINT Msg,        // WM_WTSSESSION_CHANGE
  WPARAM wParam,   // session state change event
  LPARAM lParam    // session ID
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*HWND* \[ in\]
</dt> <dd>

Handle per la finestra.

</dd> <dt>

*Messaggio* \[ in\]
</dt> <dd>

Specifica il messaggio (**\_ \_ modifica WM WTSSESSION**).

</dd> <dt>

*wParam* \[ in\]
</dt> <dd>

Codice di stato che descrive il motivo per cui è stata inviata la notifica di modifica dello stato della sessione. Questo parametro può avere uno dei valori seguenti.

<dt>

<span id="WTS_CONSOLE_CONNECT"></span><span id="wts_console_connect"></span>

<span id="WTS_CONSOLE_CONNECT"></span><span id="wts_console_connect"></span>**WTS \_ \_Connessione alla console** (0x1)


</dt> <dd>

La sessione identificata da *lParam* è stata connessa al terminale della console o alla sessione RemoteFX.

</dd> <dt>

<span id="WTS_CONSOLE_DISCONNECT"></span><span id="wts_console_disconnect"></span>

<span id="WTS_CONSOLE_DISCONNECT"></span><span id="wts_console_disconnect"></span>**WTS \_ \_Disconnessione della console** (0x2)


</dt> <dd>

La sessione identificata da *lParam* è stata disconnessa dal terminale della console o dalla sessione RemoteFX.

</dd> <dt>

<span id="WTS_REMOTE_CONNECT"></span><span id="wts_remote_connect"></span>

<span id="WTS_REMOTE_CONNECT"></span><span id="wts_remote_connect"></span>**WTS \_ \_Connessione remota** (0x3)


</dt> <dd>

La sessione identificata da *lParam* è stata connessa al terminale remoto.

</dd> <dt>

<span id="WTS_REMOTE_DISCONNECT"></span><span id="wts_remote_disconnect"></span>

<span id="WTS_REMOTE_DISCONNECT"></span><span id="wts_remote_disconnect"></span>**WTS \_ \_Disconnessione remota** (0x4)


</dt> <dd>

La sessione identificata da *lParam* è stata disconnessa dal terminale remoto.

</dd> <dt>

<span id="WTS_SESSION_LOGON"></span><span id="wts_session_logon"></span>

<span id="WTS_SESSION_LOGON"></span><span id="wts_session_logon"></span>**WTS \_ \_Accesso alla sessione** (0x5)


</dt> <dd>

Un utente ha effettuato l'accesso alla sessione identificata da *lParam*.

</dd> <dt>

<span id="WTS_SESSION_LOGOFF"></span><span id="wts_session_logoff"></span>

<span id="WTS_SESSION_LOGOFF"></span><span id="wts_session_logoff"></span>**WTS \_ \_Disconnessione della sessione** (0x6)


</dt> <dd>

Un utente ha disconnesso la sessione identificata da *lParam*.

</dd> <dt>

<span id="WTS_SESSION_LOCK"></span><span id="wts_session_lock"></span>

<span id="WTS_SESSION_LOCK"></span><span id="wts_session_lock"></span>**WTS \_ \_Blocco della sessione** (0x7)


</dt> <dd>

La sessione identificata da *lParam* è stata bloccata.

</dd> <dt>

<span id="WTS_SESSION_UNLOCK"></span><span id="wts_session_unlock"></span>

<span id="WTS_SESSION_UNLOCK"></span><span id="wts_session_unlock"></span>**WTS \_ \_Sblocco della sessione** (0x8)


</dt> <dd>

La sessione identificata da *lParam* è stata sbloccata.

</dd> <dt>

<span id="WTS_SESSION_REMOTE_CONTROL"></span><span id="wts_session_remote_control"></span>

<span id="WTS_SESSION_REMOTE_CONTROL"></span><span id="wts_session_remote_control"></span>**WTS \_ \_ \_ Controllo remoto sessione** (0x9)


</dt> <dd>

La sessione identificata da *lParam* ha modificato lo stato di controllo remoto. Per determinare lo stato, chiamare [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) e controllare la **metrica \_ RemoteControl di SM** .

</dd> <dt>

<span id="WTS_SESSION_CREATE"></span><span id="wts_session_create"></span>

<span id="WTS_SESSION_CREATE"></span><span id="wts_session_create"></span>**WTS \_ \_Creazione della sessione** (0xA)


</dt> <dd>

Riservato per utilizzi futuri.

</dd> <dt>

<span id="WTS_SESSION_TERMINATE"></span><span id="wts_session_terminate"></span>

<span id="WTS_SESSION_TERMINATE"></span><span id="wts_session_terminate"></span>**WTS \_ \_Terminazione sessione** (0xB)


</dt> <dd>

Riservato per utilizzi futuri.

</dd> </dl> </dd> <dt>

*lParam* \[ in\]
</dt> <dd>

Identificatore della sessione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito viene ignorato.

## <a name="remarks"></a>Commenti

Questo messaggio viene inviato solo alle applicazioni che hanno effettuato la registrazione per ricevere questo messaggio chiamando [**WTSRegisterSessionNotification**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsregistersessionnotification).

Esempi di come le applicazioni possono rispondere a questo messaggio includono il rilascio o l'acquisizione di risorse specifiche della console, la determinazione della modalità di disegno di una schermata o l'attivazione degli effetti di animazione della console.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                                 |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                           |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**WTSRegisterSessionNotification**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsregistersessionnotification)
</dt> <dt>

[**WTSUnRegisterSessionNotification**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsunregistersessionnotification)
</dt> </dl>

 

