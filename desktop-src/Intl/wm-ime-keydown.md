---
description: Inviato a un'applicazione dall'IME per notificare all'applicazione la pressione di un tasto e mantenere l'ordine dei messaggi. Una finestra riceve questo messaggio tramite la relativa funzione WindowProc.
ms.assetid: db7075fb-b3d4-4d32-a0db-096d17d67c72
title: WM_IME_KEYDOWN messaggio (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: beed8bb074e1bae300d52c52867cc8d1f26b84bb8abf358ad2858df7356a0a0c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119535311"
---
# <a name="wm_ime_keydown-message"></a>Messaggio WM \_ IME \_ KEYDOWN

Inviato a un'applicazione dall'IME per notificare all'applicazione la pressione di un tasto e mantenere l'ordine dei messaggi. Una finestra riceve questo messaggio tramite la relativa [**funzione WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


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

*Hwnd* 
</dt> <dd>

Handle per la finestra.

</dd> <dt>

*wParam* 
</dt> <dd>

Codice della chiave virtuale della chiave.

</dd> <dt>

*lParam* 
</dt> <dd>

Numero di ripetizioni, codice di analisi, flag della chiave estesa, codice di contesto, flag di stato della chiave precedente e flag dello stato di transizione, come illustrato nella tabella seguente.



| bit   | Significato                                                                     |
|-------|-----------------------------------------------------------------------------|
| 0-15  | Numero di ripetizioni.                                                               |
| 16-23 | Analizzare il codice.                                                                  |
| 24    | Chiave estesa. Questo valore è 1 se è una chiave estesa. Negli altri casi è 0. |
| 25-28 | Non usato.                                                                   |
| 29    | Codice di contesto. Il valore è sempre 0 .                                       |
| 30    | Stato precedente della chiave. Questo valore è 1 se la chiave è in giù o 0 se è in alto.    |
| 31    | Stato di transizione. Il valore è sempre 0 .                                   |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Un'applicazione deve restituire 0 se elabora questo messaggio.

## <a name="remarks"></a>Commenti

Un'applicazione può elaborare questo messaggio o passarlo alla funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  per generare un messaggio [**WM \_ KEYDOWN**](../inputdev/wm-keydown.md) corrispondente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Gestione metodi di input](input-method-manager.md)
</dt> <dt>

[Messaggi di Gestione metodi di input](input-method-manager-messages.md)
</dt> </dl>

 

 
