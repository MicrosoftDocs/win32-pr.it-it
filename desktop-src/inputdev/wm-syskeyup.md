---
title: Messaggio WM_SYSKEYUP (winuser. h)
description: Inserito nella finestra con lo stato attivo quando l'utente rilascia un tasto premuto mentre il tasto ALT è stato premuto.
ms.assetid: a4f62575-fb84-4390-a1d1-1a62629de55f
keywords:
- Input della tastiera e del mouse WM_SYSKEYUP messaggio
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
ms.openlocfilehash: 2139c11558eccc3fb3b225f0cc1a87bcf6fb084d
ms.sourcegitcommit: cea2889abb43350c38cd120e877d8471dae78beb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352056"
---
# <a name="wm_syskeyup-message"></a>\_Messaggio SYSKEYUP WM

Inserito nella finestra con lo stato attivo quando l'utente rilascia un tasto premuto mentre il tasto ALT è stato premuto. Si verifica anche quando nessuna finestra dispone attualmente dello stato attivo della tastiera; in questo caso, il messaggio **WM \_ SYSKEYUP** viene inviato alla finestra attiva. La finestra che riceve il messaggio può distinguere tra questi due contesti controllando il codice del contesto nel parametro *lParam* .

Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_SYSKEYUP                     0x0105
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Codice della chiave virtuale della chiave da rilasciare. Vedere [**codici chiave virtuale**](virtual-key-codes.md).

</dd> <dt>

*lParam* 
</dt> <dd>

Il numero di ripetizioni, il codice di analisi, il flag di chiave estesa, il codice del contesto, il flag di stato precedente e il flag di stato di transizione, come illustrato nella tabella seguente.



| BITS  | Significato                                                                                                                                                                                                                       |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0-15  | Numero di ripetizioni per il messaggio corrente. Il valore è il numero di volte in cui la sequenza di tasti viene ripetuta in modo ripetitivo a causa dell'arresto della chiave da parte dell'utente. Il numero di ripetizioni è sempre uno per un messaggio **WM \_ SYSKEYUP** .         |
| 16-23 | Codice di analisi. Il valore dipende dall'OEM.                                                                                                                                                                                  |
| 24    | Indica se la chiave è una chiave estesa, ad esempio i tasti ALT e CTRL a destra che vengono visualizzati in una tastiera migliorata 101 o 102. Il valore è 1 se è una chiave estesa; in caso contrario, è zero.                   |
| 25-28 | Riservati Non usare.                                                                                                                                                                                                         |
| 29    | Codice del contesto. Il valore è 1 se il tasto ALT è premuto mentre la chiave viene rilasciata; è zero se il messaggio **WM \_ SYSKEYUP** viene inserito nella finestra attiva perché nessuna finestra dispone dello stato attivo della tastiera. |
| 30    | Stato precedente della chiave. Il valore è sempre 1 per un messaggio **WM \_ SYSKEYUP** .                                                                                                                                                 |
| 31    | Stato di transizione. Il valore è sempre 1 per un messaggio **WM \_ SYSKEYUP** .                                                                                                                                                   |

Per informazioni dettagliate, vedere [flag dei messaggi di sequenza di tasti](about-keyboard-input.md#keystroke-message-flags).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Un'applicazione deve restituire zero se elabora questo messaggio.

## <a name="remarks"></a>Commenti

La funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) Invia un messaggio [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) alla finestra di primo livello se è stato rilasciato il tasto F10 o il tasto ALT. Il parametro *wParam* del messaggio viene impostato sul **\_ menu SC**.

Quando il codice del contesto è zero, il messaggio può essere passato alla funzione [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) , che lo gestirà come se fosse un normale messaggio chiave invece di un messaggio chiave-carattere. In questo modo è possibile utilizzare i tasti di scelta rapida con la finestra attiva anche se la finestra attiva non dispone dello stato attivo della tastiera.

Per le tastiere avanzate 101 e 102-Key, le chiavi estese sono i tasti ALT e CTRL corretti nella sezione principale della tastiera; i tasti INS, CANC, HOME, END, PGSU, PGGIÙ e frecce nei cluster a sinistra del tastierino numerico; e la divisione (/) e immettere le chiavi nel tastierino numerico. Altre tastiere possono supportare il bit della chiave estesa nel parametro *lParam* .

Per non-U. S. tastiere ottimizzate a 102 chiavi, il tasto ALT destro viene gestito come tasto CTRL + ALT. Nella tabella seguente viene illustrata la sequenza di messaggi risultante quando l'utente preme e rilascia tale chiave.



| Message                           | Codice chiave virtuale |
|-----------------------------------|------------------|
| [**KeyDown di WM \_**](wm-keydown.md) | **\_controllo VK**  |
| [**KeyDown di WM \_**](wm-keydown.md) | **\_menu VK**     |
| [**KEYUP di WM \_**](wm-keyup.md)     | **\_controllo VK**  |
| **\_SYSKEYUP WM**                  | **\_menu VK**     |



 

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

[**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora)
</dt> <dt>

[**\_SYSCOMMAND WM**](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

[**\_SYSKEYDOWN WM**](wm-syskeydown.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Input da tastiera](keyboard-input.md)
</dt> </dl>

 

