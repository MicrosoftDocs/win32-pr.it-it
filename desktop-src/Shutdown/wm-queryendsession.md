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
# <a name="wm_queryendsession-message"></a>\_Messaggio QUERYENDSESSION WM

Il messaggio **WM \_ QUERYENDSESSION** viene inviato quando l'utente sceglie di terminare la sessione o quando un'applicazione chiama una delle funzioni di arresto del sistema. Se un'applicazione restituisce zero, la sessione non viene terminata. Il sistema smette di inviare messaggi **WM \_ QUERYENDSESSION** non appena un'applicazione restituisce zero.

Dopo l'elaborazione del messaggio, il sistema invia il messaggio [**WM \_ ENDSESSION**](wm-endsession.md) con il parametro *wParam* impostato sui risultati del messaggio **WM \_ QUERYENDSESSION** .

Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
LRESULT CALLBACK WindowProc( 
  HWND hwnd,      // handle to window 
  UINT uMsg,      // message identifier 
  WPARAM wParam,  // not used 
  LPARAM lParam   // logoff option
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*HWND* 
</dt> <dd>

Handle per la finestra.

</dd> <dt>

*uMsg* 
</dt> <dd>

Identificatore **WM \_ QUERYENDSESSION** .

</dd> <dt>

*wParam* 
</dt> <dd>

Questo parametro è riservato per usi futuri.

</dd> <dt>

*lParam* 
</dt> <dd>

Il parametro può essere costituito da uno o più dei valori seguenti. Se questo parametro è 0, il sistema viene arrestato o riavviato. non è possibile determinare l'evento che si sta verificando.



| Valore                                                                                                                                                                                                                                           | Significato                                                                                                                                                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ENDSESSION_CLOSEAPP"></span><span id="endsession_closeapp"></span><dl> <dt>**ENDSESSION \_**</dt> <dt>0x00000001</dt> CLOSEAPP </dl> | L'applicazione usa un file che deve essere sostituito, il sistema è in fase di manutenzione oppure le risorse di sistema sono esaurite. Per ulteriori informazioni, vedere [linee guida per le applicazioni](../rstmgr/guidelines-for-applications.md).<br/> |
| <span id="ENDSESSION_CRITICAL"></span><span id="endsession_critical"></span><dl> <dt>**ENDSESSION \_**</dt> <dt>0x40000000</dt> critico </dl> | È necessario arrestare l'applicazione.<br/>                                                                                                                                                                              |
| <span id="ENDSESSION_LOGOFF"></span><span id="endsession_logoff"></span><dl> <dt>**ENDSESSION \_**</dt> <dt>0x80000000</dt> di disconnessione </dl>       | L'utente si sta disconnettendo. Per ulteriori informazioni, vedere [disconnessione](logging-off.md).<br/>                                                                                                                                   |



 

Si noti che questo parametro è una maschera di bit. Per eseguire il test di questo valore, utilizzare un'operazione bit. non verificare l'uguaglianza.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Le applicazioni devono rispettare le intenzioni dell'utente e restituire **true**. Per impostazione predefinita, la funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) restituisce **true** per questo messaggio.

Se la chiusura danneggia il sistema o i supporti in fase di masterizzazione, l'applicazione può restituire **false**. Tuttavia, è consigliabile rispettare le azioni dell'utente.

## <a name="remarks"></a>Commenti

Quando un'applicazione restituisce **true** per questo messaggio, riceve il messaggio [**WM \_ ENDSESSION**](wm-endsession.md) , indipendentemente dal modo in cui le altre applicazioni rispondono al messaggio **WM \_ QUERYENDSESSION** . Ogni applicazione deve restituire **true** o **false** immediatamente dopo la ricezione del messaggio e rinviare le operazioni di pulizia fino a quando non riceve il messaggio **WM \_ ENDSESSION** .

Le applicazioni possono visualizzare un'interfaccia utente che richiede all'utente informazioni alla chiusura, tuttavia non è consigliabile. Dopo cinque secondi, il sistema Visualizza le informazioni sulle applicazioni che impediscono l'arresto e consente all'utente di terminarle. Windows XP, ad esempio, Visualizza una finestra di dialogo, mentre Windows Vista Visualizza una schermata a schermo intero con informazioni aggiuntive sulle applicazioni che bloccano l'arresto. Se l'applicazione deve bloccare o posticipare l'arresto del sistema, usare la funzione [**ShutdownBlockReasonCreate**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate) . Per ulteriori informazioni, vedere [Shutdown changes for Windows Vista](shutdown-changes-for-windows-vista.md).

Le applicazioni console possono utilizzare la funzione [**SetConsoleCtrlHandler**](/windows/console/setconsolectrlhandler) per ricevere la notifica di arresto.

Le applicazioni di servizio possono utilizzare la funzione [**RegisterServiceCtrlHandlerEx**](/windows/win32/api/winsvc/nf-winsvc-registerservicectrlhandlerexa) per ricevere le notifiche di arresto in una routine di gestione.

## <a name="examples"></a>Esempio

Per un esempio, vedere [disconnessione](logging-off.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows XP \[ \| UWP\]<br/>                                                       |
| Server minimo supportato<br/> | App UWP per \[ app desktop di Windows Server 2003 \|\]<br/>                                              |
| Intestazione<br/>                   | <dl> <dt>WinUser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Disconnessione](logging-off.md)
</dt> <dt>

[Chiusura in corso](shutting-down.md)
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**ExitWindows**](/windows/desktop/api/Winuser/nf-winuser-exitwindows)
</dt> <dt>

[**SetProcessShutdownParameters**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocessshutdownparameters)
</dt> <dt>

[**\_ENDSESSION WM**](wm-endsession.md)
</dt> </dl>

 

 
