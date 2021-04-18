---
title: Messaggio WM_SYSKEYDOWN (winuser. h)
description: Inserito nella finestra con lo stato attivo quando l'utente preme il tasto F10 (che attiva la barra dei menu) o tiene premuto il tasto ALT, quindi preme un altro tasto.
ms.assetid: a3c03dbf-1be7-49ff-b931-1981786b74ce
keywords:
- Input della tastiera e del mouse WM_SYSKEYDOWN messaggio
topic_type:
- apiref
api_name:
- WM_SYSKEYDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3053c5933a0388e3c8522b0d7201b491aaa4fa2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301677"
---
# <a name="wm_syskeydown-message"></a>\_Messaggio SYSKEYDOWN WM

Inserito nella finestra con lo stato attivo quando l'utente preme il tasto F10 (che attiva la barra dei menu) o tiene premuto il tasto ALT, quindi preme un altro tasto. Si verifica anche quando nessuna finestra dispone attualmente dello stato attivo della tastiera; in questo caso, il messaggio **WM \_ SYSKEYDOWN** viene inviato alla finestra attiva. La finestra che riceve il messaggio può distinguere tra questi due contesti controllando il codice del contesto nel parametro *lParam* .


```C++
#define WM_SYSKEYDOWN                   0x0104
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Codice della chiave virtuale del tasto premuto. Vedere [**codici chiave virtuale**](virtual-key-codes.md).

</dd> <dt>

*lParam* 
</dt> <dd>

Il numero di ripetizioni, il codice di analisi, il flag di chiave estesa, il codice del contesto, il flag di stato precedente e il flag di stato di transizione, come illustrato nella tabella seguente.



| BITS  | Significato                                                                                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0-15  | Numero di ripetizioni per il messaggio corrente. Il valore è il numero di volte in cui la sequenza di tasti viene ripetuta in modo ripetitivo a causa dell'arresto della chiave da parte dell'utente. Se la sequenza di tasti viene mantenuta abbastanza a lungo, vengono inviati più messaggi. Tuttavia, il numero di ripetizioni non è cumulativo. |
| 16-23 | Codice di analisi. Il valore dipende dall'OEM.                                                                                                                                                                                                                          |
| 24    | Indica se la chiave è una chiave estesa, ad esempio i tasti ALT e CTRL a destra che vengono visualizzati in una tastiera migliorata 101 o 102. Il valore è 1 se è una chiave estesa; in caso contrario, è 0.                                                              |
| 25-28 | Riservati Non usare.                                                                                                                                                                                                                                                 |
| 29    | Codice del contesto. Il valore è 1 se il tasto ALT è premuto mentre il tasto è premuto; è 0 se il messaggio **WM \_ SYSKEYDOWN** viene inserito nella finestra attiva perché nessuna finestra dispone dello stato attivo della tastiera.                                                                  |
| 30    | Stato precedente della chiave. Il valore è 1 se la chiave è inattiva prima dell'invio del messaggio oppure è 0 se la chiave è attiva.                                                                                                                                                    |
| 31    | Stato di transizione. Il valore è sempre 0 per un messaggio **WM \_ SYSKEYDOWN** .                                                                                                                                                                                         |

Per informazioni dettagliate, vedere [flag dei messaggi di sequenza di tasti](about-keyboard-input.md#keystroke-message-flags).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Un'applicazione deve restituire zero se elabora questo messaggio.

## <a name="remarks"></a>Commenti

La funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) esamina la chiave specificata e genera un messaggio [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) se la chiave è Tab o ENTER.

Quando il codice del contesto è zero, il messaggio può essere passato alla funzione [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) , che lo gestirà come se fosse un normale messaggio chiave invece di un messaggio chiave-carattere. In questo modo è possibile utilizzare i tasti di scelta rapida con la finestra attiva anche se la finestra attiva non dispone dello stato attivo della tastiera.

A causa della ripetizione automatica, possono verificarsi più di un messaggio **WM \_ SYSKEYDOWN** prima dell'invio di un messaggio [**WM \_ SYSKEYUP**](wm-syskeyup.md) . Lo stato precedente della chiave (bit 30) può essere usato per determinare se il messaggio **WM \_ SYSKEYDOWN** indica la prima transizione verso il basso o una transizione ripetuta verso il basso.

Per le tastiere ottimizzate 101 e 102, le chiavi avanzate sono i tasti ALT e CTRL corretti nella sezione principale della tastiera; i tasti INS, CANC, HOME, END, PGSU, PGGIÙ e frecce nei cluster a sinistra del tastierino numerico; e la divisione (/) e immettere le chiavi nel tastierino numerico. Altre tastiere possono supportare il bit della chiave estesa nel parametro *lParam* .

Questo messaggio viene inviato anche ogni volta che l'utente preme il tasto F10 senza il tasto ALT.

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

[**\_SYSKEYUP WM**](wm-syskeyup.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Input da tastiera](keyboard-input.md)
</dt> </dl>

 

