---
title: WM_DEADCHAR messaggio (Winuser.h)
description: Inviato alla finestra con lo stato attivo della tastiera quando un messaggio WM \_ KEYUP viene convertito dalla funzione TranslateMessage.
ms.assetid: ada9a61c-dabf-447b-ae13-91803c097f0d
keywords:
- WM_DEADCHAR messaggio Input tastiera e mouse
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
ms.openlocfilehash: 4e4921d399c4a1c7a86596bfcc907b52d9c834235d133d6455b88c5a5a40c89a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778751"
---
# <a name="wm_deadchar-message"></a>Messaggio \_ DEADCHAR WM

Inviato alla finestra con lo stato attivo della tastiera quando un [**messaggio WM \_ KEYUP**](wm-keyup.md) viene convertito dalla [**funzione TranslateMessage.**](/windows/desktop/api/winuser/nf-winuser-translatemessage) **WM \_ DEADCHAR** specifica un codice carattere generato da una chiave non in esecuzione. Una chiave non disponibile è una chiave che genera un carattere, ad esempio umlaut (doppio punto), combinato con un altro carattere per formare un carattere composito. Ad esempio, il carattere umlaut-O ( ) viene generato digitando il tasto non disponibile per il carattere umlaut e quindi digitando il tasto O.


```C++
#define WM_DEADCHAR                     0x0103
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Codice carattere generato dalla chiave non in esecuzione.

</dd> <dt>

*lParam* 
</dt> <dd>

Numero di ripetizioni, codice di analisi, flag di chiave estesa, codice di contesto, flag di stato della chiave precedente e flag di stato di transizione, come illustrato nella tabella seguente.



| BITS  | Significato                                                                                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0-15  | Numero di ripetizioni per il messaggio corrente. Il valore è il numero di volte in cui la sequenza di tasti viene ripetuta in modo automatico a causa del fatto che l'utente tiene premuto il tasto. Se la sequenza di tasti viene mantenuta abbastanza a lungo, vengono inviati più messaggi. Tuttavia, il conteggio delle ripetizioni non è cumulativo. |
| 16-23 | Codice di analisi. Il valore dipende dall'OEM.                                                                                                                                                                                                                          |
| 24    | Indica se il tasto è un tasto esteso, ad esempio i tasti ALT e CTRL di destra visualizzati su una tastiera avanzata a 101 o 102 tasti. Il valore è 1 se è una chiave estesa. in caso contrario, è 0.                                                              |
| 25-28 | Riservato; non utilizzare .                                                                                                                                                                                                                                                 |
| 29    | Codice del contesto. Il valore è 1 se il tasto ALT viene premuto mentre il tasto viene premuto; In caso contrario, il valore è 0.                                                                                                                                                     |
| 30    | Stato della chiave precedente. Il valore è 1 se la chiave non è disponibile prima dell'invio del messaggio oppure è 0 se la chiave è in alto.                                                                                                                                                    |
| 31    | Stato della transizione. Il valore è 1 se il tasto viene rilasciato o è 0 se il tasto viene premuto.                                                                                                                                                            |

Per altre informazioni, vedere [Flag dei messaggi di sequenza di tasti](about-keyboard-input.md#keystroke-message-flags).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Un'applicazione deve restituire zero se elabora questo messaggio.

## <a name="remarks"></a>Commenti

Il **messaggio \_ WM DEADCHAR** viene in genere usato dalle applicazioni per fornire all'utente commenti e suggerimenti su ogni tasto premuto. Ad esempio, un'applicazione può visualizzare l'accento nella posizione del carattere corrente senza spostare il cursore.

Poiché non esiste necessariamente una corrispondenza uno-a-uno tra i tasti premuti e i messaggi di tipo carattere generati, le informazioni nella parola più alta del parametro *lParam* non sono in genere utili per le applicazioni. Le informazioni nella parola di ordine generale si applicano solo al messaggio [**WM \_ KEYDOWN**](wm-keydown.md) più recente che precede la pubblicazione del **messaggio WM \_ DEADCHAR.**

Per le tastiere avanzate da 101 e 102 tasti, i tasti estesi sono i tasti ALT di destra e CTRL destro nella sezione principale della tastiera; i tasti INS, DEL, HOME, END, PGGIS, PGGIUTO e i tasti di direzione nei cluster a sinistra del tastierino numerico; e i tasti di divisione (/) e INVIO nel tastierino numerico. Alcune altre tastiere possono supportare il bit del tasto esteso nel *parametro lParam.*

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

[**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[**WM \_ KEYDOWN**](wm-keydown.md)
</dt> <dt>

[**WM \_ KEYUP**](wm-keyup.md)
</dt> <dt>

[**WM \_ SYSDEADCHAR**](wm-sysdeadchar.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Input da tastiera](keyboard-input.md)
</dt> </dl>

 

