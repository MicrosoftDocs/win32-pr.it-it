---
title: WM_CHARTOITEM messaggio (Winuser.h)
description: Inviato da una casella di riepilogo con lo stile WANTKEYBOARDINPUT di LBS al proprietario in risposta \_ a un messaggio WM \_ CHAR.
ms.assetid: f941c00b-b836-4f1b-b8cf-8ac2b0704af3
keywords:
- WM_CHARTOITEM controlli Windows messaggio
topic_type:
- apiref
api_name:
- WM_CHARTOITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f3809ae800cfc753925e7c27d87f970ce56c10d90ace7c23e87b46f3e0067fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957530"
---
# <a name="wm_chartoitem-message"></a>Messaggio \_ WM CHARTOITEM

Inviato da una casella di riepilogo con lo stile [**\_ WANTKEYBOARDINPUT di LBS**](list-box-styles.md) al proprietario in risposta a un [**messaggio WM \_ CHAR.**](/windows/desktop/inputdev/wm-char)


```C++
WM_CHARTOITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

LoWORD [**specifica**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) il codice carattere del tasto premuto dall'utente. HiWORD [**specifica**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) la posizione corrente del cursore.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per la casella di riepilogo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito specifica l'azione eseguita dall'applicazione in risposta al messaggio. Il valore restituito -1 o -2 indica che l'applicazione ha gestito tutti gli aspetti della selezione dell'elemento e non richiede ulteriori azioni da parte della casella di riepilogo. Un valore restituito pari a 0 o superiore specifica l'indice in base zero di un elemento nella casella di riepilogo e indica che la casella di riepilogo deve eseguire l'azione predefinita per la sequenza di tasti sull'elemento specificato.

## <a name="remarks"></a>Commenti

La [**funzione DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) restituisce -1.

Solo le caselle di riepilogo disegnate dal proprietario che non hanno lo stile [**\_ HASSTRINGS di LBS**](list-box-styles.md) possono ricevere questo messaggio.

Se il messaggio viene gestito da una routine della finestra di dialogo, è necessario eseguire il cast del valore restituito desiderato in un valore **BOOL** e restituire direttamente il valore. Il *valore \_ MSGRESULT DWL* impostato dalla funzione [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) viene ignorato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**WM \_ VKEYTOITEM**](wm-vkeytoitem.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**WM \_ CHAR**](/windows/desktop/inputdev/wm-char)
</dt> </dl>

 

