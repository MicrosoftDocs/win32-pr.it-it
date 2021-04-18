---
description: Inviato a un'applicazione quando un utente annulla le attività di inserimento nel journal dell'applicazione. Il messaggio viene pubblicato con un handle di finestra NULL.
ms.assetid: 7515acb5-4526-40f7-abb7-822a073ac7dc
title: Messaggio WM_CANCELJOURNAL (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a5676472d12c8cef2a03e508eca6bb742596a36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314878"
---
# <a name="wm_canceljournal-message"></a>\_Messaggio CANCELJOURNAL WM

Inviato a un'applicazione quando un utente annulla le attività di inserimento nel journal dell'applicazione. Il messaggio viene pubblicato con un handle di finestra **null** .


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

Questo messaggio non restituisce alcun valore. È concepita per essere elaborata dall'interno del ciclo principale di un'applicazione o da una routine hook [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) , non da una routine di finestra.

## <a name="remarks"></a>Commenti

Le modalità di riproduzione e registrazione del journal sono modalità imposte nel sistema che consentono a un'applicazione di registrare o riprodurre l'input dell'utente. Il sistema immette queste modalità quando un'applicazione installa una procedura di hook [*JournalRecordProc*](/previous-versions/windows/desktop/legacy/ms644983(v=vs.85)) o [*JournalPlaybackProc*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85)) . Quando il sistema si trova in una di queste modalità di inserimento nel journal, le applicazioni devono eseguire la lettura degli input dalla coda di input. Se un'applicazione interrompe la lettura dell'input mentre il sistema è in modalità di inserimento nel journal, è necessario attendere le altre applicazioni.

Per garantire un sistema affidabile, che non può essere reso non risposta da alcuna applicazione, il sistema annulla automaticamente le attività di inserimento nel journal quando un utente preme CTRL + ESC o CTRL + ALT + CANC. Il sistema quindi sgancia le procedure di hook di inserimento nel journal e inserisce un messaggio **WM \_ CANCELJOURNAL** , con un handle di finestra **null** , per l'applicazione che ha impostato l'hook di inserimento nel journal.

Il messaggio **WM \_ CANCELJOURNAL** ha un handle di finestra **null** , pertanto non può essere inviato a una routine di finestra. Per un'applicazione è possibile visualizzare un messaggio **WM \_ CANCELJOURNAL** in due modi: se l'applicazione è in esecuzione nel proprio ciclo principale, deve intercettare il messaggio tra la chiamata a [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) o [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) e la relativa chiamata a [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage). Se l'applicazione non è in esecuzione nel proprio ciclo principale, deve impostare una procedura [*GetMsgProc*](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85)) Hook (tramite una chiamata a [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) che specifica il tipo di hook **WH \_ GetMessage** ) che controlla il messaggio.

Quando un'applicazione visualizza un messaggio **WM \_ CANCELJOURNAL** , può ipotizzare due elementi: l'utente ha intenzionalmente annullato il record Journal o la modalità di riproduzione e il sistema ha già annullato le procedure di hook di riproduzione o di record Journal.

Si noti che le combinazioni di tasti indicate in precedenza (CTRL + ESC o CTRL + ALT + CANC) determinano l'annullamento del journaling da parte del sistema. Se un'applicazione non risponde, concede all'utente un mezzo di ripristino. Il codice della chiave virtuale di [**\_ annullamento VK**](../inputdev/virtual-key-codes.md) (in genere implementato come combinazione di tasti Ctrl + Break) indica il modo in cui un'applicazione che si trova in una modalità di registrazione journal deve controllare come un segnale che l'utente desidera annullare l'attività di inserimento nel journal. La differenza consiste nel fatto che la verifica dell' **\_ annullamento del VK** è un comportamento suggerito per le applicazioni di inserimento nel journal, mentre CTRL + ESC o CTRL + ALT + CANC provocano l'annullamento del journaling da parte del sistema, indipendentemente dal comportamento di un'applicazione di journaling.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



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

[**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Hook](hooks.md)
</dt> </dl>

 

 
