---
title: Messaggio WM_UNICHAR (winuser. h)
description: Il messaggio di WM \_ UNICHAR può essere usato da un'applicazione per inserire l'input in altre finestre.
ms.assetid: edbfcf14-0371-43ce-9676-eb10d964d0b7
keywords:
- Input della tastiera e del mouse WM_UNICHAR messaggio
topic_type:
- apiref
api_name:
- WM_UNICHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 833b5cb59095f5aecc8c0172857c8761fd92449a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301676"
---
# <a name="wm_unichar-message"></a>\_Messaggio UNICHAR WM

Il messaggio di **WM \_ UNICHAR** può essere usato da un'applicazione per inserire l'input in altre finestre. Questo messaggio contiene il codice carattere della chiave che è stata premuta. (Verificare se un'app di destinazione può elaborare messaggi **WM \_ UNICHAR** inviando il messaggio con *wParam* impostato su **Unicode \_ nochar**).


```C++
#define WM_UNICHAR                      0x0109
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Codice carattere della chiave.

Se *wParam* è **Unicode \_ nochar** e l'applicazione elabora il messaggio, restituisce **true**. La funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) restituirà **false** (impostazione predefinita).

Se *wParam* non è **Unicode \_ nochar**, restituisce **false**. Il  [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) Unicode Invia un messaggio [**WM \_ char**](wm-char.md) con gli stessi parametri e la funzione **DefWindowProc** ANSI invia uno o due messaggi **WM \_ char** con i caratteri ANSI corrispondenti.

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
| 29    | Codice del contesto. Il valore è 1 se il tasto ALT è premuto mentre il tasto è premuto; in caso contrario, il valore è 0.                                                                                                                                                     |
| 30    | Stato precedente della chiave. Il valore è 1 se la chiave è inattiva prima dell'invio del messaggio oppure è 0 se la chiave è attiva.                                                                                                                                                    |
| 31    | Stato di transizione. Il valore è 1 se la chiave viene rilasciata oppure è 0 se viene premuto il tasto.                                                                                                                                                            |

Per informazioni dettagliate, vedere [flag dei messaggi di sequenza di tasti](about-keyboard-input.md#keystroke-message-flags).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Un'applicazione deve restituire zero se elabora questo messaggio.

## <a name="remarks"></a>Commenti

Il messaggio di **WM \_ UNICHAR** è simile a [**WM \_ char**](wm-char.md), ma usa Unicode Transformation Format (UTF)-32, mentre **WM \_ char** usa la codifica UTF-16.

Questo messaggio è progettato per inviare o inviare caratteri Unicode alle finestre ANSI e può gestire i caratteri del piano supplementare Unicode.

Poiché non esiste necessariamente una corrispondenza uno-a-uno tra i tasti premuti e i messaggi di tipo carattere generati, le informazioni nella parola più significativa del parametro *lParam* non sono in genere utili per le applicazioni. Le informazioni nella parola più ordinata si applicano solo al messaggio più recente di [**WM \_ KeyDown**](wm-keydown.md) che precede l'inserimento del messaggio **WM \_ UNICHAR** .

Per le tastiere avanzate 101 e 102-Key, le chiavi estese sono i tasti ALT e CTRL destro nella sezione principale della tastiera; i tasti INS, CANC, HOME, END, PGSU, PGGIÙ e freccia nei cluster a sinistra del tastierino numerico; e la divisione (/) e immettere le chiavi nel tastierino numerico. È possibile che alcune altre tastiere supportino il bit della chiave estesa nel parametro *lParam* .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[**\_carattere WM**](wm-char.md)
</dt> <dt>

[**KeyDown di WM \_**](wm-keydown.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Input da tastiera](keyboard-input.md)
</dt> </dl>

 

