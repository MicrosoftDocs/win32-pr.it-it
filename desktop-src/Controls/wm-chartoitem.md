---
title: Messaggio WM_CHARTOITEM (winuser. h)
description: Inviato da una casella di riepilogo con lo \_ stile WANTKEYBOARDINPUT lbs al relativo proprietario in risposta a un \_ messaggio WM Char.
ms.assetid: f941c00b-b836-4f1b-b8cf-8ac2b0704af3
keywords:
- Controlli di Windows Message WM_CHARTOITEM
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
ms.openlocfilehash: 2dc9df55dcf9f507cb57e91fe0214eab94c53f22
ms.sourcegitcommit: ac62be2f60f757f61ea647a95c168c9841ffabac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/10/2021
ms.locfileid: "104353916"
---
# <a name="wm_chartoitem-message"></a>\_Messaggio CHARTOITEM WM

Inviato da una casella di riepilogo con lo stile [**\_ WANTKEYBOARDINPUT lbs**](list-box-styles.md) al relativo proprietario in risposta a un messaggio [**WM \_ char**](/windows/desktop/inputdev/wm-char) .


```C++
WM_CHARTOITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifica il codice carattere della chiave che l'utente ha premuto. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica la posizione corrente del punto di inserimento.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per la casella di riepilogo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito specifica l'azione eseguita dall'applicazione in risposta al messaggio. Il valore restituito-1 o-2 indica che l'applicazione ha gestito tutti gli aspetti della selezione dell'elemento e non richiede ulteriori azioni da parte della casella di riepilogo. Un valore restituito pari a 0 o superiore specifica l'indice in base zero di un elemento nella casella di riepilogo e indica che la casella di riepilogo deve eseguire l'azione predefinita per la sequenza di tasti sull'elemento specificato.

## <a name="remarks"></a>Commenti

La funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) restituisce-1.

Solo le caselle di riepilogo create dal proprietario che non hanno lo stile [**\_ HASSTRINGS lbs**](list-box-styles.md) possono ricevere questo messaggio.

Se una routine della finestra di dialogo gestisce questo messaggio, deve eseguire il cast del valore restituito desiderato a un **bool** e restituire direttamente il valore. Il valore *DWL \_ MSGRESULT* impostato dalla funzione [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) viene ignorato.

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

[**\_VKEYTOITEM WM**](wm-vkeytoitem.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**\_carattere WM**](/windows/desktop/inputdev/wm-char)
</dt> </dl>

 

