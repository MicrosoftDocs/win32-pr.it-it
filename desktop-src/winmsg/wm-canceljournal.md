---
description: Pubblicato in un'applicazione quando un utente annulla le attività di inserimento nel journal dell'applicazione. Il messaggio viene inviato con un handle di finestra NULL.
ms.assetid: 7515acb5-4526-40f7-abb7-822a073ac7dc
title: WM_CANCELJOURNAL messaggio (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8672f86393275c46383c6eb27c7eb1884178b86635ea93bf758de16521e6d2c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117849337"
---
# <a name="wm_canceljournal-message"></a>Messaggio WM \_ CANCELJOURNAL

Pubblicato in un'applicazione quando un utente annulla le attività di inserimento nel journal dell'applicazione. Il messaggio viene inviato con un handle di finestra **NULL.**


```C++
#define WM_CANCELJOURNAL                0x004B
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **void**

Questo messaggio non restituisce un valore. Deve essere elaborato dall'interno del ciclo principale di un'applicazione o di una routine hook [**GetMessage,**](/windows/win32/api/winuser/nf-winuser-getmessage) non da una routine finestra.

## <a name="remarks"></a>Commenti

Le modalità di registrazione e riproduzione del journal sono modalità imposte al sistema che consentono a un'applicazione di registrare o riprodurre in sequenza l'input dell'utente. Il sistema entra in queste modalità quando un'applicazione installa una routine hook [*JournalRecordProc*](/previous-versions/windows/desktop/legacy/ms644983(v=vs.85)) o [*JournalPlaybackProc.*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85)) Quando il sistema si trova in una di queste modalità di inserimento nel journal, le applicazioni devono leggere a turno l'input dalla coda di input. Se un'applicazione interrompe la lettura dell'input mentre il sistema è in modalità di inserimento nel journal, le altre applicazioni sono obbligate ad attendere.

Per garantire un sistema affidabile, che non può essere reso non risponde da una sola applicazione, il sistema annulla automaticamente tutte le attività di inserimento nel journal quando un utente preme CTRL+ESC o CTRL+ALT+CANC. Il sistema esegue quindi l'unhook di tutte le routine hook di inserimento nel journal e invia un messaggio **WM \_ CANCELJOURNAL,** con un handle di finestra **NULL,** all'applicazione che ha impostato l'hook di inserimento nel journal.

Il **messaggio WM \_ CANCELJOURNAL** ha un handle di finestra **NULL,** pertanto non può essere inviato a una routine della finestra. Un'applicazione può visualizzare un messaggio **WM \_ CANCELJOURNAL** in due modi: se l'applicazione è in esecuzione nel proprio ciclo principale, deve intercettare il messaggio tra la chiamata a [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) o [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) e la chiamata a [**DispatchMessage.**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) Se l'applicazione non è in esecuzione nel proprio ciclo principale, deve impostare una routine hook [*GetMsgProc*](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85)) (tramite una chiamata a [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) che specifica il tipo di hook **WH \_ GETMESSAGE)** che controlla il messaggio.

Quando un'applicazione visualizza un messaggio **WM \_ CANCELJOURNAL,** può presupporre due aspetti: l'utente ha intenzionalmente annullato la modalità di registrazione o riproduzione del journal e il sistema ha già annullato l'associazione di record journal o riproduzione.

Si noti che le combinazioni di tasti indicate in precedenza (CTRL+ESC o CTRL+ALT+CANC) causano l'annullamento dell'inserimento nel journal da parte del sistema. Se un'applicazione non risponde, assegna all'utente un mezzo di ripristino. Il codice tasto virtuale [**\_ CANCEL VK**](../inputdev/virtual-key-codes.md) (in genere implementato come combinazione di tasti CTRL+INTERR) è ciò che un'applicazione in modalità record journal deve controllare come segnale che l'utente vuole annullare l'attività di inserimento nel journal. La differenza è che il controllo di **VK \_ CANCEL** è un comportamento consigliato per le applicazioni di inserimento nel journal, mentre CTRL+ESC o CTRL+ALT+CANC determinano l'annullamento dell'inserimento nel journal da parte del sistema indipendentemente dal comportamento di un'applicazione di inserimento nel journal.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[*JournalPlaybackProc*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85))
</dt> <dt>

[*JournalRecordProc*](/previous-versions/windows/desktop/legacy/ms644983(v=vs.85))
</dt> <dt>

[*GetMsgProc*](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85))
</dt> <dt>

[**Setwindowshookex**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Hook](hooks.md)
</dt> </dl>

 

 
