---
title: Messaggio WM_SYSDEADCHAR (winuser. h)
description: Inviato alla finestra con lo stato attivo quando un messaggio WM \_ SYSKEYDOWN viene convertito dalla funzione TranslateMessage.
ms.assetid: cf9a1171-a47c-4d7b-b351-31f41a893b20
keywords:
- Input della tastiera e del mouse WM_SYSDEADCHAR messaggio
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
ms.openlocfilehash: 2052f8ced24ac998a56a4365552fee4bc5e0b21e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302388"
---
# <a name="wm_sysdeadchar-message"></a>\_Messaggio SYSDEADCHAR WM

Inviato alla finestra con lo stato attivo quando un messaggio [**WM \_ SYSKEYDOWN**](wm-syskeydown.md) viene convertito dalla funzione [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) . **WM \_ SYSDEADCHAR** specifica il codice carattere di una chiave di sistema non recapitabile, ovvero un tasto inattivo premuto tenendo premuto il tasto ALT.


```C++
#define WM_SYSDEADCHAR                  0x0107
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Il codice carattere generato dalla chiave di sistema non recapitabile, ovvero un tasto inattivo premuto tenendo premuto il tasto ALT.

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
| 31    | Stato di transizione. Il valore è 1 se la chiave viene rilasciata oppure è 0 se viene premuto il tasto.                                                                                                                                                                |

Per informazioni dettagliate, vedere [flag dei messaggi di sequenza di tasti](about-keyboard-input.md#keystroke-message-flags).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Un'applicazione deve restituire zero se elabora questo messaggio.

## <a name="remarks"></a>Commenti

Per le tastiere avanzate 101 e 102-Key, le chiavi estese sono i tasti ALT e CTRL corretti nella sezione principale della tastiera; i tasti INS, CANC, HOME, END, PGSU, PGGIÙ e frecce nei cluster a sinistra del tastierino numerico; e la divisione (/) e immettere le chiavi nel tastierino numerico. Altre tastiere possono supportare il bit della chiave estesa nel parametro *lParam* .

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

[**\_DEADCHAR WM**](wm-deadchar.md)
</dt> <dt>

[**\_SYSKEYDOWN WM**](wm-syskeydown.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Input da tastiera](keyboard-input.md)
</dt> </dl>

 

