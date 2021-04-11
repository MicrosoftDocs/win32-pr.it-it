---
description: Inviato a un'applicazione dall'IME per notificare all'applicazione la pressione di un tasto e per mantenere l'ordine dei messaggi. Una finestra riceve questo messaggio tramite la funzione WindowProc.
ms.assetid: db7075fb-b3d4-4d32-a0db-096d17d67c72
title: Messaggio WM_IME_KEYDOWN (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3089af3c839f70e7f55895ae13158e7b2240605
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226131"
---
# <a name="wm_ime_keydown-message"></a>\_ \_ Messaggio KeyDown IME WM

Inviato a un'applicazione dall'IME per notificare all'applicazione la pressione di un tasto e per mantenere l'ordine dei messaggi. Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,        
  WM_IME_KEYDOWN,  
  WPARAM wParam, 
  LPARAM lParam      
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*HWND* 
</dt> <dd>

Handle per la finestra.

</dd> <dt>

*wParam* 
</dt> <dd>

Codice chiave virtuale della chiave.

</dd> <dt>

*lParam* 
</dt> <dd>

Numero di ripetizioni, codice di analisi, flag di chiave estesa, codice del contesto, flag di stato della chiave precedente e flag di stato di transizione, come illustrato nella tabella seguente.



| bit   | Significato                                                                     |
|-------|-----------------------------------------------------------------------------|
| 0-15  | Numero di ripetizioni.                                                               |
| 16-23 | Analizzare il codice.                                                                  |
| 24    | Chiave estesa. Questo valore è 1 se è una chiave estesa. Negli altri casi è 0. |
| 25-28 | Non usato.                                                                   |
| 29    | Codice del contesto. Il valore è sempre 0 .                                       |
| 30    | Stato precedente della chiave. Questo valore è 1 se la chiave è inattiva o 0 se è attiva.    |
| 31    | Stato di transizione. Il valore è sempre 0 .                                   |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Un'applicazione deve restituire 0 se elabora questo messaggio.

## <a name="remarks"></a>Commenti

Un'applicazione può elaborare questo messaggio o passarlo alla funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  per generare un messaggio [**WM \_ KeyDown**](../inputdev/wm-keydown.md) corrispondente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Gestione metodo di input](input-method-manager.md)
</dt> <dt>

[Messaggi di gestione metodo di input](input-method-manager-messages.md)
</dt> </dl>

 

 
