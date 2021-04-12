---
title: Messaggio WM_VKEYTOITEM (winuser. h)
description: Inviato da una casella di riepilogo con lo \_ stile WANTKEYBOARDINPUT di lbs al suo proprietario in risposta a un messaggio del KeyDown di WM \_ .
ms.assetid: 2eab922f-7298-436f-bd94-0eefae7284d5
keywords:
- Controlli di Windows Message WM_VKEYTOITEM
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
ms.openlocfilehash: 7d1685682d8305fff5d9d93ef59d8859e099e6ce
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "104351731"
---
# <a name="wm_vkeytoitem-message"></a>\_Messaggio VKEYTOITEM WM

Inviato da una casella di riepilogo con lo stile [**\_ WANTKEYBOARDINPUT di lbs**](list-box-styles.md) al suo proprietario in risposta a un messaggio del [**\_ KeyDown di WM**](/windows/desktop/inputdev/wm-keydown) .


```C++
WM_VKEYTOITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifica il codice della chiave virtuale della chiave che l'utente ha premuto. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica la posizione corrente del punto di inserimento.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per la casella di riepilogo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito specifica l'azione eseguita dall'applicazione in risposta al messaggio. Un valore restituito pari a-2 indica che l'applicazione ha gestito tutti gli aspetti della selezione dell'elemento e non richiede ulteriori azioni da parte della casella di riepilogo. (Vedere la sezione Osservazioni). Un valore restituito-1 indica che la casella di riepilogo deve eseguire l'azione predefinita in risposta alla sequenza di tasti. Un valore restituito pari a 0 o superiore specifica l'indice di un elemento nella casella di riepilogo e indica che la casella di riepilogo deve eseguire l'azione predefinita per la sequenza di tasti sull'elemento specificato.

## <a name="remarks"></a>Commenti

Un valore restituito di-2 è valido solo per le chiavi non convertite in caratteri dal controllo casella di riepilogo. Se il messaggio [**WM \_ KeyDown**](/windows/desktop/inputdev/wm-keydown) viene convertito in un messaggio [**WM \_ char**](/windows/desktop/inputdev/wm-char) e l'applicazione elabora il messaggio **WM \_ VKEYTOITEM** generato come risultato della pressione della chiave, la casella di riepilogo ignora il valore restituito ed esegue l'elaborazione predefinita per tale carattere. **WM \_** I messaggi KeyDown generati da chiavi quali VK \_ up, VK \_ Down, VK \_ Next e VK \_ Previous non vengono convertiti in messaggi **WM \_ char** . In questi casi, l'intercettazione del messaggio **WM \_ VKEYTOITEM** e la restituzione di-2 impedisce alla casella di riepilogo di eseguire l'elaborazione predefinita per tale chiave.

Per intercettare le chiavi che generano un messaggio char ed eseguire un'elaborazione speciale, l'applicazione deve sottocreare una sottoclasse della casella di riepilogo, intercettare i messaggi [**WM \_ KeyDown**](/windows/desktop/inputdev/wm-keydown) e [**WM \_ char**](/windows/desktop/inputdev/wm-char) ed elaborare i messaggi in modo appropriato nella procedura di sottoclasse.

Le osservazioni precedenti si applicano alle caselle di riepilogo normali create con lo stile [**\_ WANTKEYBOARDINPUT di lbs**](list-box-styles.md) . Se la casella di riepilogo è disegnata dal proprietario, l'applicazione deve elaborare il messaggio [**WM \_ CHARTOITEM**](wm-chartoitem.md) .

La funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) restituisce-1.

Se una routine della finestra di dialogo gestisce questo messaggio, deve eseguire il cast del valore restituito desiderato a un **bool** e restituire direttamente il valore. Il \_ valore DWL MSGRESULT impostato dalla funzione [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) viene ignorato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**\_CHARTOITEM WM**](wm-chartoitem.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**KeyDown di WM \_**](/windows/desktop/inputdev/wm-keydown)
</dt> </dl>

 

