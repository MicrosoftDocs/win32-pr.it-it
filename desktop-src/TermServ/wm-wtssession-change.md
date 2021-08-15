---
title: WM_WTSSESSION_CHANGE messaggio (Winuser.h)
description: Notifica alle applicazioni le modifiche apportate allo stato della sessione.
ms.assetid: 758a130c-b75a-40fd-8530-3766aa86c5ba
ms.tgt_platform: multiple
keywords:
- WM_WTSSESSION_CHANGE messaggio Servizi Desktop remoto
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
ms.openlocfilehash: f29bef7eb7778602a256f80cb04e47eae905a245783906c3388b576aecedee18
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119419841"
---
# <a name="wm_wtssession_change-message"></a>Messaggio WM \_ WTSSESSION \_ CHANGE

Notifica alle applicazioni le modifiche apportate allo stato della sessione.

La finestra riceve questo messaggio tramite la [**relativa funzione WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


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

*hWnd* \[ Pollici\]
</dt> <dd>

Handle per la finestra.

</dd> <dt>

*Msg* \[ Pollici\]
</dt> <dd>

Specifica il messaggio (**WM \_ WTSSESSION \_ CHANGE**).

</dd> <dt>

*wParam* \[ Pollici\]
</dt> <dd>

Codice di stato che descrive il motivo per cui è stata inviata la notifica di modifica dello stato della sessione. Questo parametro può avere uno dei valori seguenti.

<dt>

<span id="WTS_CONSOLE_CONNECT"></span><span id="wts_console_connect"></span>

<span id="WTS_CONSOLE_CONNECT"></span><span id="wts_console_connect"></span>**WTS \_ CONSOLE \_ CONNECT** (0x1)


</dt> <dd>

La sessione identificata da *lParam è* stata connessa al terminale della console o RemoteFX sessione.

</dd> <dt>

<span id="WTS_CONSOLE_DISCONNECT"></span><span id="wts_console_disconnect"></span>

<span id="WTS_CONSOLE_DISCONNECT"></span><span id="wts_console_disconnect"></span>**WTS \_ CONSOLE \_ DISCONNECT** (0x2)


</dt> <dd>

La sessione identificata da *lParam è* stata disconnessa dal terminale della console o RemoteFX sessione.

</dd> <dt>

<span id="WTS_REMOTE_CONNECT"></span><span id="wts_remote_connect"></span>

<span id="WTS_REMOTE_CONNECT"></span><span id="wts_remote_connect"></span>**WTS \_ REMOTE \_ CONNECT** (0x3)


</dt> <dd>

La sessione identificata *da lParam* è connessa al terminale remoto.

</dd> <dt>

<span id="WTS_REMOTE_DISCONNECT"></span><span id="wts_remote_disconnect"></span>

<span id="WTS_REMOTE_DISCONNECT"></span><span id="wts_remote_disconnect"></span>**WTS \_ REMOTE \_ DISCONNECT** (0x4)


</dt> <dd>

La sessione identificata *da lParam* è stata disconnessa dal terminale remoto.

</dd> <dt>

<span id="WTS_SESSION_LOGON"></span><span id="wts_session_logon"></span>

<span id="WTS_SESSION_LOGON"></span><span id="wts_session_logon"></span>**WTS \_ SESSION \_ LOGON** (0x5)


</dt> <dd>

Un utente ha eseguito l'accesso alla sessione identificata da *lParam*.

</dd> <dt>

<span id="WTS_SESSION_LOGOFF"></span><span id="wts_session_logoff"></span>

<span id="WTS_SESSION_LOGOFF"></span><span id="wts_session_logoff"></span>**WTS \_ DISCONNESSIONE \_ SESSIONE** (0x6)


</dt> <dd>

Un utente ha disconnesso la sessione identificata da *lParam*.

</dd> <dt>

<span id="WTS_SESSION_LOCK"></span><span id="wts_session_lock"></span>

<span id="WTS_SESSION_LOCK"></span><span id="wts_session_lock"></span>**WTS \_ SESSION \_ LOCK** (0x7)


</dt> <dd>

La sessione identificata *da lParam* è stata bloccata.

</dd> <dt>

<span id="WTS_SESSION_UNLOCK"></span><span id="wts_session_unlock"></span>

<span id="WTS_SESSION_UNLOCK"></span><span id="wts_session_unlock"></span>**WTS \_ SESSION \_ UNLOCK** (0x8)


</dt> <dd>

La sessione identificata *da lParam* è stata sbloccata.

</dd> <dt>

<span id="WTS_SESSION_REMOTE_CONTROL"></span><span id="wts_session_remote_control"></span>

<span id="WTS_SESSION_REMOTE_CONTROL"></span><span id="wts_session_remote_control"></span>**WTS \_ SESSION \_ REMOTE \_ CONTROL** (0x9)


</dt> <dd>

La sessione identificata da *lParam ha* modificato lo stato controllato da remoto. Per determinare lo stato, chiamare [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) e controllare la **metrica \_ SM REMOTECONTROL.**

</dd> <dt>

<span id="WTS_SESSION_CREATE"></span><span id="wts_session_create"></span>

<span id="WTS_SESSION_CREATE"></span><span id="wts_session_create"></span>**WTS \_ SESSION \_ CREATE** (0xA)


</dt> <dd>

Riservato per utilizzi futuri.

</dd> <dt>

<span id="WTS_SESSION_TERMINATE"></span><span id="wts_session_terminate"></span>

<span id="WTS_SESSION_TERMINATE"></span><span id="wts_session_terminate"></span>**WTS \_ SESSION \_ TERMINATE** (0xB)


</dt> <dd>

Riservato per utilizzi futuri.

</dd> </dl> </dd> <dt>

*lParam* \[ Pollici\]
</dt> <dd>

Identificatore della sessione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito viene ignorato.

## <a name="remarks"></a>Commenti

Questo messaggio viene inviato solo alle applicazioni registrate per ricevere questo messaggio chiamando [**WTSRegisterSessionNotification.**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsregistersessionnotification)

Alcuni esempi di come le applicazioni possono rispondere a questo messaggio includono il rilascio o l'acquisizione di risorse specifiche della console, la determinazione della modalità di disegno di una schermata o l'attivazione di effetti di animazione della console.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                                 |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                           |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**WTSRegisterSessionNotification**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsregistersessionnotification)
</dt> <dt>

[**WTSUnRegisterSessionNotification**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsunregistersessionnotification)
</dt> </dl>

 

