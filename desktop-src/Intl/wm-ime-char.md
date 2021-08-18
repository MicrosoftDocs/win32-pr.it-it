---
description: Inviato a un'applicazione quando l'IME ottiene un carattere del risultato della conversione. Una finestra riceve questo messaggio tramite la relativa funzione WindowProc.
ms.assetid: 1e1353c3-5215-4829-a00a-2fee47a430eb
title: WM_IME_CHAR messaggio (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 337ca982cbd755e01f3dfab465d8b82948dfdbf053a4a7c03417a1d508bc42d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146784"
---
# <a name="wm_ime_char-message"></a>Messaggio WM \_ IME \_ CHAR

Inviato a un'applicazione quando l'IME ottiene un carattere del risultato della conversione. Una finestra riceve questo messaggio tramite la relativa [**funzione WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


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

*Hwnd* 
</dt> <dd>

Handle per la finestra.

</dd> <dt>

*wParam* 
</dt> <dd>

**DBCS:** Valore a byte singolo o a byte doppio. Per un carattere a byte doppio, (BYTE)(wParam >> 8) contiene il byte iniziale. Si noti che le parentesi sono necessarie perché l'operatore cast ha una precedenza maggiore rispetto all'operatore shift.

**Unicode:** Valore di carattere Unicode.

</dd> <dt>

*lParam* 
</dt> <dd>

Il conteggio delle ripetizioni, il codice di analisi, il flag della chiave estesa, il codice di contesto, il flag di stato della chiave precedente e il flag dello stato di transizione, con i valori definiti di seguito.



| bit   | Significato                                                                              |
|-------|--------------------------------------------------------------------------------------|
| 0-15  | Numero di ripetizioni. Poiché il primo byte e il secondo byte sono continui, è sempre 1. |
| 16-23 | Analizzare il codice per cercare un carattere asiano completo.                                            |
| 24    | Chiave estesa.                                                                        |
| 25-28 | Non usato.                                                                            |
| 29    | Codice di contesto.                                                                        |
| 30    | Stato precedente della chiave.                                                                  |
| 31    | Stato di transizione.                                                                    |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

A differenza [**del messaggio WM \_ CHAR**](../inputdev/wm-char.md) per una finestra non Unicode, questo messaggio può includere valori di caratteri a byte doppio e a byte singolo. Per una finestra Unicode, questo messaggio corrisponde a WM \_ CHAR.

Per una finestra non Unicode, se il messaggio WM IME CHAR include un carattere a byte doppio e l'applicazione passa questo messaggio \_ \_ a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), l'IME converte questo messaggio in due messaggi WM CHAR, ognuno contenente un byte del carattere a \_ byte doppio.

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

 

 
