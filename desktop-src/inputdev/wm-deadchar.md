---
title: Messaggio WM_DEADCHAR (winuser. h)
description: Inserito nella finestra con lo stato attivo quando un messaggio WM \_ KEYUP viene convertito dalla funzione TranslateMessage.
ms.assetid: ada9a61c-dabf-447b-ae13-91803c097f0d
keywords:
- Input della tastiera e del mouse WM_DEADCHAR messaggio
topic_type:
- apiref
api_name:
- WM_DEADCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6053095b912360e9875fa062c2daba7cafcfd43b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476163"
---
# <a name="wm_deadchar-message"></a>\_Messaggio DEADCHAR WM

Inserito nella finestra con lo stato attivo quando un messaggio [**WM \_ KEYUP**](wm-keyup.md) viene convertito dalla funzione [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) . **WM \_ DEADCHAR** specifica un codice carattere generato da una chiave non recapitabile. Una chiave non recapitabile è una chiave che genera un carattere, ad esempio il dieresto (punto doppio), combinato con un altro carattere per formare un carattere composito. Il carattere dieresto (), ad esempio, viene generato digitando la chiave non recapitabile per il carattere dieresto, quindi digitando il tasto O.


```C++
#define WM_DEADCHAR                     0x0103
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Codice carattere generato dalla chiave non recapitabile.

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

Il messaggio **WM \_ DEADCHAR** viene in genere usato dalle applicazioni per fornire commenti e suggerimenti degli utenti su ogni tasto premuto. Ad esempio, un'applicazione può visualizzare l'accento nella posizione del carattere corrente senza lo stato spostato.

Poiché non esiste necessariamente una corrispondenza uno-a-uno tra i tasti premuti e i messaggi di tipo carattere generati, le informazioni nella parola più significativa del parametro *lParam* non sono in genere utili per le applicazioni. Le informazioni nella parola più ordinata si applicano solo al messaggio più recente del [**\_ KeyDown di WM**](wm-keydown.md) che precede la pubblicazione del messaggio **WM \_ DEADCHAR** .

Per le tastiere avanzate 101 e 102-Key, le chiavi estese sono i tasti ALT e CTRL destro nella sezione principale della tastiera; i tasti INS, CANC, HOME, END, PGSU, PGGIÙ e freccia nei cluster a sinistra del tastierino numerico; e la divisione (/) e immettere le chiavi nel tastierino numerico. È possibile che alcune altre tastiere supportino il bit della chiave estesa nel parametro *lParam* .

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

[**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[**KeyDown di WM \_**](wm-keydown.md)
</dt> <dt>

[**KEYUP di WM \_**](wm-keyup.md)
</dt> <dt>

[**\_SYSDEADCHAR WM**](wm-sysdeadchar.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Input da tastiera](keyboard-input.md)
</dt> </dl>

 

