---
title: WM_SYSDEADCHAR messaggio (Winuser.h)
description: Inviato alla finestra con lo stato attivo della tastiera quando un messaggio WM \_ SYSKEYDOWN viene convertito dalla funzione TranslateMessage.
ms.assetid: cf9a1171-a47c-4d7b-b351-31f41a893b20
keywords:
- WM_SYSDEADCHAR messaggio Input tastiera e mouse
topic_type:
- apiref
api_name:
- WM_SYSDEADCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e7ddf63ab4643ef59e45a4850a18a9823753c16a59b4519fe099326fe071704
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118757223"
---
# <a name="wm_sysdeadchar-message"></a>Messaggio \_ WM SYSDEADCHAR

Inviato alla finestra con lo stato attivo della tastiera quando [**un messaggio WM \_ SYSKEYDOWN**](wm-syskeydown.md) viene convertito dalla [**funzione TranslateMessage.**](/windows/desktop/api/winuser/nf-winuser-translatemessage) **WM \_ SYSDEADCHAR** specifica il codice carattere di un tasto di scelta rapida di sistema, un tasto non in esecuzione premuto mentre si tiene premuto ALT.


```C++
#define WM_SYSDEADCHAR                  0x0107
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Codice carattere generato dal tasto di scelta rapida del sistema, un tasto non premuto mentre si tiene premuto ALT.

</dd> <dt>

*lParam* 
</dt> <dd>

Numero di ripetizioni, codice di analisi, flag di chiave estesa, codice di contesto, flag di stato della chiave precedente e flag di stato di transizione, come illustrato nella tabella seguente.



| BITS  | Significato                                                                                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0-15  | Numero di ripetizioni per il messaggio corrente. Il valore è il numero di volte in cui la sequenza di tasti viene ripetuta in modo automatico in seguito all'utente che tiene premuto il tasto. Se la sequenza di tasti viene mantenuta abbastanza a lungo, vengono inviati più messaggi. Tuttavia, il conteggio delle ripetizioni non è cumulativo. |
| 16-23 | Codice di analisi. Il valore dipende dall'OEM.                                                                                                                                                                                                                          |
| 24    | Indica se il tasto è un tasto esteso, ad esempio i tasti ALT e CTRL di destra visualizzati su una tastiera avanzata a 101 o 102 tasti. Il valore è 1 se è una chiave estesa. in caso contrario, è 0.                                                              |
| 25-28 | Riservato; non utilizzare .                                                                                                                                                                                                                                                 |
| 29    | Codice del contesto. Il valore è 1 se il tasto ALT viene premuto mentre il tasto viene premuto; in caso contrario, il valore è 0.                                                                                                                                                     |
| 30    | Stato della chiave precedente. Il valore è 1 se la chiave non è disponibile prima dell'invio del messaggio oppure è 0 se la chiave è in alto.                                                                                                                                                    |
| 31    | Stato di transizione. Il valore è 1 se il tasto viene rilasciato oppure è 0 se il tasto viene premuto.                                                                                                                                                                |

Per altre informazioni, vedere [Flag dei messaggi di sequenza di tasti](about-keyboard-input.md#keystroke-message-flags).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Un'applicazione deve restituire zero se elabora questo messaggio.

## <a name="remarks"></a>Commenti

Per le tastiere avanzate da 101 e 102 tasti, i tasti estesi sono i tasti ALT e CTRL di destra nella sezione principale della tastiera; i tasti INS, DEL, HOME, END, PGGIS, PGGIUTO e i tasti di direzione nei cluster a sinistra del tastierino numerico; e i tasti di divisione (/) e INVIO nel tastierino numerico. Altre tastiere possono supportare il bit del tasto esteso nel *parametro lParam.*

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

[**WM \_ DEADCHAR**](wm-deadchar.md)
</dt> <dt>

[**WM \_ SYSKEYDOWN**](wm-syskeydown.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Input da tastiera](keyboard-input.md)
</dt> </dl>

 

