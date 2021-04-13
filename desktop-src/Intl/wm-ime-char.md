---
description: Inviato a un'applicazione quando l'IME ottiene un carattere del risultato della conversione. Una finestra riceve questo messaggio tramite la funzione WindowProc.
ms.assetid: 1e1353c3-5215-4829-a00a-2fee47a430eb
title: Messaggio WM_IME_CHAR (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be0e2df06d9d837b0c1fbc0f9c9d9eb852252c47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104401787"
---
# <a name="wm_ime_char-message"></a>\_ \_ Messaggio char IME WM

Inviato a un'applicazione quando l'IME ottiene un carattere del risultato della conversione. Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
LRESULT CALLBACK WindowProc(
 HWND  hwnd,
 WM_IME_CHAR,
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

**DBCS:** Valore di carattere A byte singolo o a byte doppio. Per un carattere a due byte, (BYTE) (wParam >> 8) contiene il byte di apertura. Si noti che le parentesi sono necessarie perché l'operatore cast ha una precedenza più alta rispetto all'operatore Shift.

**Unicode:** Valore del carattere Unicode.

</dd> <dt>

*lParam* 
</dt> <dd>

Il numero di ripetizioni, il codice di analisi, il flag di chiave estesa, il codice del contesto, il flag di stato della chiave precedente e il flag di stato di transizione con i valori definiti di seguito.



| bit   | Significato                                                                              |
|-------|--------------------------------------------------------------------------------------|
| 0-15  | Numero di ripetizioni. Poiché il primo byte e il secondo byte sono continui, è sempre 1. |
| 16-23 | Analizza il codice per un carattere asiatico completo.                                            |
| 24    | Chiave estesa.                                                                        |
| 25-28 | Non usato.                                                                            |
| 29    | Codice del contesto.                                                                        |
| 30    | Stato precedente della chiave.                                                                  |
| 31    | Stato di transizione.                                                                    |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

A differenza del messaggio [**WM \_ char**](../inputdev/wm-char.md) per una finestra non Unicode, questo messaggio può includere valori di caratteri a doppio byte e a byte singolo. Per una finestra Unicode, questo messaggio è uguale a WM \_ Char.

Per una finestra non Unicode, se il messaggio WM \_ IME \_ char include un carattere a due byte e l'applicazione passa il messaggio a [**DEFWINDOWPROC**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), l'IME converte questo messaggio in due messaggi WM \_ Char, ognuno dei quali contiene un byte del carattere a byte doppio.

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

 

 
