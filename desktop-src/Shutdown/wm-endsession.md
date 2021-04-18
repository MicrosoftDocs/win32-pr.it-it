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
# <a name="wm_endsession-message"></a>\_Messaggio ENDSESSION WM

Il messaggio **WM \_ ENDSESSION** viene inviato a un'applicazione dopo che il sistema ha elaborato i risultati del messaggio [**WM \_ QUERYENDSESSION**](wm-queryendsession.md) . Il messaggio **WM \_ ENDSESSION** informa l'applicazione se la sessione sta terminando.

Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
LRESULT CALLBACK WindowProc( 
  HWND hwnd,      // handle to window 
  UINT uMsg,      // message identifier 
  WPARAM wParam,  // end-session option 
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

Identificatore **WM \_ ENDSESSION** .

</dd> <dt>

*wParam* 
</dt> <dd>

Se la sessione viene terminata, questo parametro è **true**; la sessione può terminare in qualsiasi momento dopo che tutte le applicazioni sono state restituite dall'elaborazione del messaggio. In caso contrario, è **false**.

</dd> <dt>

*lParam* 
</dt> <dd>

Il parametro può essere costituito da uno o più dei valori seguenti. Se questo parametro è 0, il sistema viene arrestato o riavviato. non è possibile determinare l'evento che si sta verificando.



| Valore                                                                                                                                                                                                                                           | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ENDSESSION_CLOSEAPP"></span><span id="endsession_closeapp"></span><dl> <dt>**ENDSESSION \_**</dt> <dt>0x1</dt> CLOSEAPP </dl>        | Se *wParam* è **true**, l'applicazione deve essere arrestata. Tutti i dati devono essere salvati automaticamente senza richiedere conferma all'utente. per ulteriori informazioni, vedere la sezione Osservazioni. Gestione riavvio Invia questo messaggio quando l'applicazione utilizza un file che deve essere sostituito, quando deve servire il sistema o quando le risorse di sistema sono esaurite. L'applicazione verrà riavviata se è stata registrata per il riavvio utilizzando la funzione [**RegisterApplicationRestart**](/windows/win32/api/winbase/nf-winbase-registerapplicationrestart) . Per ulteriori informazioni, vedere [linee guida per le applicazioni](../rstmgr/guidelines-for-applications.md). <br/> Se *wParam* è **false**, l'applicazione non deve essere arrestata.<br/> |
| <span id="ENDSESSION_CRITICAL"></span><span id="endsession_critical"></span><dl> <dt>**ENDSESSION \_**</dt> <dt>0x40000000</dt> critico </dl> | È necessario arrestare l'applicazione.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="ENDSESSION_LOGOFF"></span><span id="endsession_logoff"></span><dl> <dt>**ENDSESSION \_**</dt> <dt>0x80000000</dt> di disconnessione </dl>       | L'utente si sta disconnettendo. Per ulteriori informazioni, vedere [disconnessione](logging-off.md).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

Si noti che questo parametro è una maschera di bit. Per eseguire il test di questo valore, utilizzare un'operazione bit. non verificare l'uguaglianza.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora il messaggio, deve restituire zero.

## <a name="remarks"></a>Commenti

Le applicazioni con dati non salvati potrebbero salvare i dati in un percorso temporaneo e ripristinarli al successivo avvio dell'applicazione. È consigliabile che le applicazioni salvino i dati e lo stato di frequente; ad esempio, salvare automaticamente i dati tra le operazioni di salvataggio avviate dall'utente per ridurre la quantità di dati da salvare al momento dell'arresto.

L'applicazione non deve chiamare la funzione [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) o [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) alla fine della sessione.

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

[**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow)
</dt> <dt>

[**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage)
</dt> <dt>

[**SetProcessShutdownParameters**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocessshutdownparameters)
</dt> <dt>

[**\_QUERYENDSESSION WM**](wm-queryendsession.md)
</dt> </dl>

 

 
