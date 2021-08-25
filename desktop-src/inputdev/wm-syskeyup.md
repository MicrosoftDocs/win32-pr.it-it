---
title: WM_SYSKEYUP messaggio (Winuser.h)
description: Inviato alla finestra con lo stato attivo della tastiera quando l'utente rilascia un tasto premuto mentre il tasto ALT è stato premuto.
ms.assetid: a4f62575-fb84-4390-a1d1-1a62629de55f
keywords:
- WM_SYSKEYUP messaggio Input tastiera e mouse
topic_type:
- apiref
api_name:
- WM_SYSKEYUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e35a0267d29e473a3c2e5a6a00a0635a466f46c2917b913c3950aa6567e3cd9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829861"
---
# <a name="wm_syskeyup-message"></a>Messaggio \_ SYSKEYUP WM

Inviato alla finestra con lo stato attivo della tastiera quando l'utente rilascia un tasto premuto mentre il tasto ALT è stato premuto. Si verifica anche quando nessuna finestra ha attualmente lo stato attivo della tastiera. In questo caso, il **messaggio WM \_ SYSKEYUP** viene inviato alla finestra attiva. La finestra che riceve il messaggio può distinguere questi due contesti controllando il codice del contesto nel *parametro lParam.*

Una finestra riceve questo messaggio tramite la relativa [**funzione WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_SYSKEYUP                     0x0105
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Codice della chiave virtuale della chiave rilasciata. Vedere [**Codici di chiave virtuale**](virtual-key-codes.md).

</dd> <dt>

*lParam* 
</dt> <dd>

Numero di ripetizioni, codice di analisi, flag di chiave estesa, codice di contesto, flag di stato della chiave precedente e flag di stato di transizione, come illustrato nella tabella seguente.



| BITS  | Significato                                                                                                                                                                                                                       |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0-15  | Numero di ripetizioni per il messaggio corrente. Il valore è il numero di volte in cui la sequenza di tasti viene ripetuta in modo automatico a causa del fatto che l'utente tiene premuto il tasto. Il numero di ripetizioni è sempre uno per un **messaggio \_ SYSKEYUP WM.**         |
| 16-23 | Codice di analisi. Il valore dipende dall'OEM.                                                                                                                                                                                  |
| 24    | Indica se il tasto è un tasto esteso, ad esempio i tasti ALT e CTRL di destra visualizzati su una tastiera avanzata a 101 o 102 tasti. Il valore è 1 se è una chiave estesa. in caso contrario, è zero.                   |
| 25-28 | Riservato; non utilizzare .                                                                                                                                                                                                         |
| 29    | Codice del contesto. Il valore è 1 se il tasto ALT è premuto mentre il tasto viene rilasciato; è zero se il **messaggio WM \_ SYSKEYUP** viene inviato alla finestra attiva perché nessuna finestra ha lo stato attivo della tastiera. |
| 30    | Stato della chiave precedente. Il valore è sempre 1 per un **messaggio \_ SYSKEYUP WM.**                                                                                                                                                 |
| 31    | Stato della transizione. Il valore è sempre 1 per un **messaggio \_ SYSKEYUP WM.**                                                                                                                                                   |

Per altre informazioni, vedere [Flag dei messaggi di sequenza di tasti](about-keyboard-input.md#keystroke-message-flags).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Un'applicazione deve restituire zero se elabora questo messaggio.

## <a name="remarks"></a>Commenti

La [**funzione DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) invia un [**messaggio \_ SYSCOMMAND WM**](/windows/desktop/menurc/wm-syscommand) alla finestra di primo livello se è stato rilasciato il tasto F10 o ALT. Il *parametro wParam* del messaggio è impostato su **SC \_ KEYMENU.**

Quando il codice di contesto è zero, il messaggio può essere passato alla funzione [**TranslateAccelerator,**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) che lo gestirà come se fosse un normale messaggio chiave invece di un messaggio con caratteri. In questo modo è possibile usare i tasti di scelta rapida con la finestra attiva anche se la finestra attiva non ha lo stato attivo della tastiera.

Per le tastiere avanzate da 101 e 102 tasti, i tasti estesi sono i tasti ALT e CTRL di destra nella sezione principale della tastiera; i tasti INS, DEL, HOME, END, PGGIS, PGGIUTO e i tasti di direzione nei cluster a sinistra del tastierino numerico; e i tasti di divisione (/) e INVIO nel tastierino numerico. Altre tastiere possono supportare il bit del tasto esteso nel *parametro lParam.*

Per utenti non statunitensi tastiere a 102 tasti avanzate, il tasto ALT di destra viene gestito come tasto CTRL+ALT. La tabella seguente illustra la sequenza di messaggi che si verificano quando l'utente preme e rilascia questo tasto.



| Message                           | Codice della chiave virtuale |
|-----------------------------------|------------------|
| [**WM \_ KEYDOWN**](wm-keydown.md) | **CONTROLLO \_ VK**  |
| [**WM \_ KEYDOWN**](wm-keydown.md) | **VK \_ MENU**     |
| [**WM \_ KEYUP**](wm-keyup.md)     | **CONTROLLO \_ VK**  |
| **WM \_ SYSKEYUP**                  | **VK \_ MENU**     |



 

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

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora)
</dt> <dt>

[**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

[**WM \_ SYSKEYDOWN**](wm-syskeydown.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Input da tastiera](keyboard-input.md)
</dt> </dl>

 

