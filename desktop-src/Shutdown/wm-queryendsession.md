---
description: Il messaggio WM QUERYENDSESSION viene inviato quando l'utente sceglie di terminare la sessione o quando un'applicazione chiama \_ una delle funzioni di arresto del sistema.
ms.assetid: 7ad73444-f1f6-4b73-8450-0580b146a5a6
title: WM_QUERYENDSESSION messaggio (WinUser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6807a861ffb0670013a1d1f5b98a2f202e5d7470a6c306b3ed29c42baad6e6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119664211"
---
# <a name="wm_queryendsession-message"></a>Messaggio \_ WM QUERYENDSESSION

Il **messaggio WM \_ QUERYENDSESSION** viene inviato quando l'utente sceglie di terminare la sessione o quando un'applicazione chiama una delle funzioni di arresto del sistema. Se un'applicazione restituisce zero, la sessione non viene terminata. Il sistema smette di inviare **messaggi WM \_ QUERYENDSESSION** non appena un'applicazione restituisce zero.

Dopo l'elaborazione di questo messaggio, il sistema invia il messaggio [**\_ ENDSESSION WM**](wm-endsession.md) con il parametro *wParam* impostato sui risultati del messaggio **WM \_ QUERYENDSESSION.**

Una finestra riceve questo messaggio tramite la [**relativa funzione WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


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

*Hwnd* 
</dt> <dd>

Handle per la finestra.

</dd> <dt>

*Umsg* 
</dt> <dd>

Identificatore **WM \_ QUERYENDSESSION.**

</dd> <dt>

*wParam* 
</dt> <dd>

Questo parametro è riservato per usi futuri.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro può essere uno o più dei valori seguenti. Se questo parametro è 0, il sistema viene arrestato o riavviato (non è possibile determinare quale evento si sta verificando).



| Valore                                                                                                                                                                                                                                           | Significato                                                                                                                                                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ENDSESSION_CLOSEAPP"></span><span id="endsession_closeapp"></span><dl> <dt>**ENDSESSION \_ CloseAPP**</dt> <dt>0x00000001</dt> </dl> | L'applicazione usa un file che deve essere sostituito, il sistema è in fase di gestione o le risorse di sistema sono esaurite. Per altre informazioni, vedere [Linee guida per le applicazioni.](../rstmgr/guidelines-for-applications.md)<br/> |
| <span id="ENDSESSION_CRITICAL"></span><span id="endsession_critical"></span><dl> <dt>**ENDSESSION \_ ERRORE CRITICO**</dt> <dt>0x40000000</dt> </dl> | L'applicazione deve essere arrestata.<br/>                                                                                                                                                                              |
| <span id="ENDSESSION_LOGOFF"></span><span id="endsession_logoff"></span><dl> <dt>**ENDSESSION \_ LogoFF**</dt> <dt>0x80000000</dt> </dl>       | L'utente si disconnette. Per altre informazioni, vedere [Disconnessione.](logging-off.md)<br/>                                                                                                                                   |



 

Si noti che questo parametro è una maschera di bit. Per verificare questo valore, usare un'operazione bit per bit. non verificano l'uguaglianza.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Le applicazioni devono rispettare le intenzioni dell'utente e restituire **TRUE.** Per impostazione predefinita, [**la funzione DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) restituisce **TRUE** per questo messaggio.

Se l'arresto danneggia il sistema o i supporti che vengono danneggiati, l'applicazione può restituire **FALSE.** È tuttavia consigliabile rispettare le azioni dell'utente.

## <a name="remarks"></a>Commenti

Quando un'applicazione restituisce **TRUE** per questo messaggio, riceve il messaggio [**\_ ENDSESSION WM,**](wm-endsession.md) indipendentemente dal modo in cui le altre applicazioni rispondono al messaggio **WM \_ QUERYENDSESSION.** Ogni applicazione deve restituire **TRUE** o **FALSE** immediatamente alla ricezione di questo messaggio e rinviare le operazioni di pulizia fino a quando non riceve il **messaggio \_ ENDSESSION WM.**

Le applicazioni possono visualizzare un'interfaccia utente che richiede all'utente informazioni all'arresto, ma non è consigliabile. Dopo cinque secondi, il sistema visualizza informazioni sulle applicazioni che impediscono l'arresto e consente all'utente di terminarle. Ad esempio, Windows XP visualizza una finestra di dialogo, mentre Windows Vista visualizza una schermata intera con informazioni aggiuntive sulle applicazioni che bloccano l'arresto. Se l'applicazione deve bloccare o posticipare l'arresto del sistema, usare la [**funzione ShutdownBlockReasonCreate.**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate) Per altre informazioni, vedere [Shutdown Changes for Windows Vista](shutdown-changes-for-windows-vista.md).

Le applicazioni console possono usare la [**funzione SetConsoleCtrlHandler**](/windows/console/setconsolectrlhandler) per ricevere la notifica di arresto.

Le applicazioni di servizio possono usare la [**funzione RegisterServiceCtrlHandlerEx**](/windows/win32/api/winsvc/nf-winsvc-registerservicectrlhandlerexa) per ricevere notifiche di arresto in una routine del gestore.

## <a name="examples"></a>Esempio

Per un esempio, vedere [Disconnessione.](logging-off.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows App \[ desktop XP per app \| UWP\]<br/>                                                       |
| Server minimo supportato<br/> | Windows App desktop di Server 2003 \[ \| per app UWP\]<br/>                                              |
| Intestazione<br/>                   | <dl> <dt>WinUser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Disconnessione](logging-off.md)
</dt> <dt>

[Arresto](shutting-down.md)
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**ExitWindows**](/windows/desktop/api/Winuser/nf-winuser-exitwindows)
</dt> <dt>

[**SetProcessShutdownParameters**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocessshutdownparameters)
</dt> <dt>

[**WM \_ ENDSESSION**](wm-endsession.md)
</dt> </dl>

 

 
