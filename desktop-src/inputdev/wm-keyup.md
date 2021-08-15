---
title: WM_KEYUP messaggio (Winuser.h)
description: Inviato alla finestra con lo stato attivo della tastiera quando viene rilasciato un tasto non di sistema. Un tasto non di sistema è un tasto premuto quando il tasto ALT non viene premuto o un tasto della tastiera che viene premuto quando una finestra ha lo stato attivo della tastiera.
ms.assetid: 67d9d82d-fab0-4aec-a337-7a9cb2b0b586
keywords:
- WM_KEYUP messaggio Input tastiera e mouse
topic_type:
- apiref
api_name:
- WM_KEYUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc23b941f232007a781ca160538f28d864f818639df47a180de472f54cd89a8a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118247823"
---
# <a name="wm_keyup-message"></a>Messaggio \_ WM KEYUP

Inviato alla finestra con lo stato attivo della tastiera quando viene rilasciato un tasto non di sistema. Un tasto non di sistema è un tasto  premuto quando il tasto ALT non viene premuto o un tasto della tastiera che viene premuto quando una finestra ha lo stato attivo della tastiera.


```C++
#define WM_KEYUP                        0x0101
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Codice della chiave virtuale della chiave non di sistema. Vedere [Codici di chiave virtuale](virtual-key-codes.md).

</dd> <dt>

*lParam* 
</dt> <dd>

Numero di ripetizioni, codice di analisi, flag di chiave estesa, codice di contesto, flag di stato della chiave precedente e flag di stato di transizione, come illustrato nella tabella seguente.



| BITS  | Significato                                                                                                                                                                                                          |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0-15  | Numero di ripetizioni per il messaggio corrente. Il valore è il numero di volte in cui la sequenza di tasti viene ripetuta come risultato dell'utente che tiene premuto il tasto. Il numero di ripetizioni è sempre 1 per un **messaggio WM \_ KEYUP.** |
| 16-23 | Codice di analisi. Il valore dipende dall'OEM.                                                                                                                                                                     |
| 24    | Indica se il tasto è un tasto esteso, ad esempio i tasti ALT e CTRL di destra visualizzati su una tastiera avanzata a 101 o 102 tasti. Il valore è 1 se è una chiave estesa. in caso contrario, è 0.         |
| 25-28 | Riservato; non utilizzare .                                                                                                                                                                                            |
| 29    | Codice del contesto. Il valore è sempre 0 per un **messaggio WM \_ KEYUP.**                                                                                                                                             |
| 30    | Stato della chiave precedente. Il valore è sempre 1 per un **messaggio WM \_ KEYUP.**                                                                                                                                       |
| 31    | Stato della transizione. Il valore è sempre 1 per un **messaggio WM \_ KEYUP.**                                                                                                                                         |

Per altre informazioni, vedere [Flag dei messaggi di sequenza di tasti](about-keyboard-input.md#keystroke-message-flags).
 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Un'applicazione deve restituire zero se elabora questo messaggio.

## <a name="remarks"></a>Commenti

La [**funzione DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) invia un [**messaggio \_ SYSCOMMAND WM**](/windows/desktop/menurc/wm-syscommand) alla finestra di primo livello se è stato rilasciato il tasto F10 o ALT. Il *parametro wParam* del messaggio è impostato su SC \_ KEYMENU.

Per le tastiere avanzate da 101 e 102 tasti, i tasti estesi sono i tasti ALT e CTRL di destra nella sezione principale della tastiera; i tasti INS, DEL, HOME, END, PGGIS, PGGIUTO e i tasti di direzione nei cluster a sinistra del tastierino numerico; e i tasti di divisione (/) e INVIO nel tastierino numerico. Altre tastiere possono supportare il bit del tasto esteso nel *parametro lParam.*

Le applicazioni devono *passare wParam* [**a TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) senza modificarlo affatto.

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

[**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[**WM \_ KEYDOWN**](wm-keydown.md)
</dt> <dt>

[**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Input da tastiera](keyboard-input.md)
</dt> </dl>

 

