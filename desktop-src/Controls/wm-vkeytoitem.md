---
title: WM_VKEYTOITEM messaggio (Winuser.h)
description: Inviato da una casella di riepilogo con lo stile WANTKEYBOARDINPUT di LBS al proprietario in risposta \_ a un messaggio WM \_ KEYDOWN.
ms.assetid: 2eab922f-7298-436f-bd94-0eefae7284d5
keywords:
- WM_VKEYTOITEM di Windows messaggi
topic_type:
- apiref
api_name:
- WM_VKEYTOITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47c054952c74b8e66bb109b925cfbdc353ec97f7bebfb5b5cafaedf8857ccb5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957470"
---
# <a name="wm_vkeytoitem-message"></a>Messaggio \_ WM VKEYTOITEM

Inviato da una casella di riepilogo con lo stile [**\_ WANTKEYBOARDINPUT**](list-box-styles.md) di LBS al proprietario in risposta a un [**messaggio WM \_ KEYDOWN.**](/windows/desktop/inputdev/wm-keydown)


```C++
WM_VKEYTOITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

LoWORD [**specifica**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) il codice del tasto virtuale del tasto premuto dall'utente. HiWORD [**specifica**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) la posizione corrente del cursore.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per la casella di riepilogo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito specifica l'azione eseguita dall'applicazione in risposta al messaggio. Il valore restituito -2 indica che l'applicazione ha gestito tutti gli aspetti della selezione dell'elemento e non richiede ulteriori azioni da parte della casella di riepilogo. Vedere la sezione Osservazioni. Il valore restituito -1 indica che la casella di riepilogo deve eseguire l'azione predefinita in risposta alla pressione del tasto. Un valore restituito pari a 0 o superiore specifica l'indice di un elemento nella casella di riepilogo e indica che la casella di riepilogo deve eseguire l'azione predefinita per la sequenza di tasti sull'elemento specificato.

## <a name="remarks"></a>Commenti

Il valore restituito -2 è valido solo per le chiavi che non vengono convertite in caratteri dal controllo casella di riepilogo. Se il messaggio [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown) viene tradotto in un messaggio [**WM \_ CHAR**](/windows/desktop/inputdev/wm-char) e l'applicazione elabora il messaggio **WM \_ VKEYTOITEM** generato in seguito alla pressione del tasto, la casella di riepilogo ignora il valore restituito ed esegue l'elaborazione predefinita per tale carattere. **WM \_ I messaggi KEYDOWN** generati da chiavi come VK \_ UP, VK DOWN, VK NEXT e VK PREVIOUS non vengono convertiti \_ in messaggi WM \_ \_ **\_ CHAR.** In questi casi, il trapping del messaggio **\_ WM VKEYTOITEM** e la restituzione di -2 impediscono alla casella di riepilogo di eseguire l'elaborazione predefinita per tale chiave.

Per generare trap per le chiavi che generano un messaggio char ed eno un'elaborazione speciale, l'applicazione deve creare una sottoclasse della casella di riepilogo, intercettare i messaggi [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown) e [**WM \_ CHAR**](/windows/desktop/inputdev/wm-char) ed elaborare i messaggi in modo appropriato nella routine della sottoclasse.

Le osservazioni precedenti si applicano alle normali caselle di riepilogo create con lo stile [**\_ WANTKEYBOARDINPUT di LBS.**](list-box-styles.md) Se la casella di riepilogo è disegnata dal proprietario, l'applicazione deve elaborare il [**messaggio WM \_ CHARTOITEM.**](wm-chartoitem.md)

La [**funzione DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) restituisce -1.

Se il messaggio viene gestito da una routine della finestra di dialogo, è necessario eseguire il cast del valore restituito desiderato in un valore **BOOL** e restituire direttamente il valore. Il valore MSGRESULT DWL \_ impostato dalla funzione [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) viene ignorato.

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

[**WM \_ CHARTOITEM**](wm-chartoitem.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown)
</dt> </dl>

 

