---
title: WM_SYSKEYDOWN messaggio (Winuser.h)
description: Inviato alla finestra con lo stato attivo quando l'utente preme F10 (che attiva la barra dei menu) o tiene premuto ALT e quindi preme un altro tasto.
ms.assetid: a3c03dbf-1be7-49ff-b931-1981786b74ce
keywords:
- WM_SYSKEYDOWN messaggio Input da tastiera e mouse
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
ms.openlocfilehash: 30b1398d843711e868a6b5b96cf6a66893bf74fef1e50bfdd61fa36f81f05c13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119611321"
---
# <a name="wm_syskeydown-message"></a>Messaggio \_ SYSKEYDOWN WM

Inviato alla finestra con lo stato attivo quando l'utente preme F10 (che attiva la barra dei menu) o tiene premuto ALT e quindi preme un altro tasto. Si verifica anche quando nessuna finestra ha attualmente lo stato attivo della tastiera. In questo caso, **il \_ messaggio WM SYSKEYDOWN** viene inviato alla finestra attiva. La finestra che riceve il messaggio può distinguere tra questi due contesti controllando il codice del contesto nel *parametro lParam.*


```C++
#define WM_SYSKEYDOWN                   0x0104
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Codice del tasto virtuale del tasto premuto. Vedere [**Codici di chiave virtuale.**](virtual-key-codes.md)

</dd> <dt>

*lParam* 
</dt> <dd>

Il conteggio delle ripetizioni, il codice di analisi, il flag di chiave estesa, il codice di contesto, il flag di stato della chiave precedente e il flag dello stato di transizione, come illustrato nella tabella seguente.



| BITS  | Significato                                                                                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0-15  | Numero di ripetizioni per il messaggio corrente. Il valore è il numero di volte in cui la sequenza di tasti viene ripetuta in modo automatico in seguito al fatto che l'utente tiene premuto il tasto. Se la pressione del tasto è sufficientemente lunga, vengono inviati più messaggi. Tuttavia, il conteggio delle ripetizioni non è cumulativo. |
| 16-23 | Codice di analisi. Il valore dipende dall'OEM.                                                                                                                                                                                                                          |
| 24    | Indica se il tasto è un tasto esteso, ad esempio i tasti ALT e CTRL di destra visualizzati su una tastiera avanzata di 101 o 102 tasti. Il valore è 1 se si tratta di una chiave estesa. in caso contrario, è 0.                                                              |
| 25-28 | Riservato; non utilizzare .                                                                                                                                                                                                                                                 |
| 29    | Codice di contesto. Il valore è 1 se il tasto ALT è premuto; è 0 se il messaggio **WM \_ SYSKEYDOWN** viene inviato alla finestra attiva perché nessuna finestra ha lo stato attivo.                                                                  |
| 30    | Stato precedente della chiave. Il valore è 1 se la chiave non è disponibile prima dell'invio del messaggio oppure è 0 se la chiave è in alto.                                                                                                                                                    |
| 31    | Stato della transizione. Il valore è sempre 0 per un **messaggio \_ SYSKEYDOWN WM.**                                                                                                                                                                                         |

Per altri dettagli, vedere [Flag di messaggi di sequenza di tasti.](about-keyboard-input.md#keystroke-message-flags)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Un'applicazione deve restituire zero se elabora questo messaggio.

## <a name="remarks"></a>Commenti

La [**funzione DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) esamina il tasto specificato e genera un messaggio [**\_ SYSCOMMAND WM**](/windows/desktop/menurc/wm-syscommand) se il tasto è TAB o INVIO.

Quando il codice di contesto è zero, il messaggio può essere passato alla funzione [**TranslateAccelerator,**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) che lo gestirà come se fosse un normale messaggio chiave anziché un messaggio di tipo carattere. In questo modo è possibile usare i tasti di scelta rapida con la finestra attiva anche se la finestra attiva non ha lo stato attivo della tastiera.

A causa della ripetizione automatica, possono verificarsi più messaggi **\_ SYSKEYDOWN WM** prima dell'invio di un messaggio [**\_ SYSKEYUP WM.**](wm-syskeyup.md) Lo stato precedente della chiave (bit 30) può essere usato per determinare se il messaggio **\_ WM SYSKEYDOWN** indica la prima transizione verso il basso o una transizione ripetuta verso il basso.

Per le tastiere a 101 e 102 tasti avanzate, i tasti migliorati sono i tasti ALT e CTRL di destra nella sezione principale della tastiera; i tasti INS, DEL, HOME, END, PGGIER, PGGI GIÙ e i tasti di direzione nei cluster a sinistra del tastierino numerico; e i tasti di divisione (/) e INVIO nel tastierino numerico. Altre tastiere possono supportare il bit del tasto esteso nel *parametro lParam.*

Questo messaggio viene inviato anche ogni volta che l'utente preme F10 senza il tasto ALT.

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

[**WM \_ SYSKEYUP**](wm-syskeyup.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Input da tastiera](keyboard-input.md)
</dt> </dl>

 

