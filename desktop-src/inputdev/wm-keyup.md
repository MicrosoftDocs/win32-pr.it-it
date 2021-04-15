---
title: Messaggio WM_KEYUP (winuser. h)
description: Inviato alla finestra con lo stato attivo quando viene rilasciato un tasto non di sistema. Una chiave non di sistema è una chiave che viene premuto quando il tasto ALT non viene premuto oppure un tasto di scelta rapida quando una finestra ha lo stato attivo della tastiera.
ms.assetid: 67d9d82d-fab0-4aec-a337-7a9cb2b0b586
keywords:
- Input della tastiera e del mouse WM_KEYUP messaggio
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
ms.openlocfilehash: 28aa02dd73f1706bb12ae30825f50241be7bb0d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400504"
---
# <a name="wm_keyup-message"></a>\_Messaggio WM KEYUP

Inviato alla finestra con lo stato attivo quando viene rilasciato un tasto non di sistema. Una chiave non di sistema è una chiave che viene premuto quando il tasto ALT *non* viene premuto oppure un tasto di scelta rapida quando una finestra ha lo stato attivo della tastiera.


```C++
#define WM_KEYUP                        0x0101
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Codice della chiave virtuale della chiave non di sistema. Vedere [codici chiave virtuale](virtual-key-codes.md).

</dd> <dt>

*lParam* 
</dt> <dd>

Il numero di ripetizioni, il codice di analisi, il flag di chiave estesa, il codice del contesto, il flag di stato precedente e il flag di stato di transizione, come illustrato nella tabella seguente.



| BITS  | Significato                                                                                                                                                                                                          |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0-15  | Numero di ripetizioni per il messaggio corrente. Il valore è il numero di volte in cui la sequenza di tasti viene ripetuta in modo ripetitivo a causa dell'arresto della chiave da parte dell'utente. Il numero di ripetizioni è sempre 1 per un messaggio **WM \_ KEYUP** . |
| 16-23 | Codice di analisi. Il valore dipende dall'OEM.                                                                                                                                                                     |
| 24    | Indica se la chiave è una chiave estesa, ad esempio i tasti ALT e CTRL a destra che vengono visualizzati in una tastiera migliorata 101 o 102. Il valore è 1 se è una chiave estesa; in caso contrario, è 0.         |
| 25-28 | Riservati Non usare.                                                                                                                                                                                            |
| 29    | Codice del contesto. Il valore è sempre 0 per un messaggio **WM \_ KEYUP** .                                                                                                                                             |
| 30    | Stato precedente della chiave. Il valore è sempre 1 per un messaggio **WM \_ KEYUP** .                                                                                                                                       |
| 31    | Stato di transizione. Il valore è sempre 1 per un messaggio **WM \_ KEYUP** .                                                                                                                                         |

Per informazioni dettagliate, vedere [flag dei messaggi di sequenza di tasti](about-keyboard-input.md#keystroke-message-flags).
 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Un'applicazione deve restituire zero se elabora questo messaggio.

## <a name="remarks"></a>Commenti

La funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) Invia un messaggio [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) alla finestra di primo livello se è stato rilasciato il tasto F10 o il tasto ALT. Il parametro *wParam* del messaggio viene impostato sul menu SC \_ .

Per le tastiere avanzate 101 e 102-Key, le chiavi estese sono i tasti ALT e CTRL corretti nella sezione principale della tastiera; i tasti INS, CANC, HOME, END, PGSU, PGGIÙ e frecce nei cluster a sinistra del tastierino numerico; e la divisione (/) e immettere le chiavi nel tastierino numerico. Altre tastiere possono supportare il bit della chiave estesa nel parametro *lParam* .

Le applicazioni devono passare *wParam* a [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) senza modificarlo.

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

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[**KeyDown di WM \_**](wm-keydown.md)
</dt> <dt>

[**\_SYSCOMMAND WM**](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Input da tastiera](keyboard-input.md)
</dt> </dl>

 

