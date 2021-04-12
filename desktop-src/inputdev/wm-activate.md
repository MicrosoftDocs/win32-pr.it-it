---
title: Messaggio WM_ACTIVATE (winuser. h)
description: Inviato sia alla finestra attivata che alla finestra da disattivare.
ms.assetid: a62bb9f7-f286-4d0d-a1ca-370950c188b2
keywords:
- Input della tastiera e del mouse WM_ACTIVATE messaggio
topic_type:
- apiref
api_name:
- WM_ACTIVATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dec28662aa2219ee9b3ad2e8cc8efac861d292f6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119514"
---
# <a name="wm_activate-message"></a>\_Messaggio di attivazione WM

Inviato sia alla finestra attivata che alla finestra da disattivare. Se le finestre utilizzano la stessa coda di input, il messaggio viene inviato in modo sincrono, prima alla routine della finestra della finestra di primo livello da disattivare, quindi alla routine della finestra della finestra di primo livello attivata. Se le finestre utilizzano code di input diverse, il messaggio viene inviato in modo asincrono, quindi la finestra viene attivata immediatamente.


```C++
#define WM_ACTIVATE                     0x0006
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

La parola di ordine inferiore specifica se la finestra viene attivata o disattivata. Questo parametro può avere uno dei valori seguenti. La parola più ordinata specifica lo stato ridotto a icona della finestra attivata o disattivata. Un valore diverso da zero indica che la finestra è ridotta A icona.



| Valore                                                                                                                                                                                                                   | Significato                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WA_ACTIVE"></span><span id="wa_active"></span><dl> <dt>**WA \_ ATTIVO**</dt> <dt>1</dt> </dl>                | Attivato da un metodo diverso da un clic del mouse, ad esempio tramite una chiamata alla funzione [**SetActiveWindow**](/windows/win32/api/winuser/nf-winuser-setactivewindow) o usando l'interfaccia della tastiera per selezionare la finestra.<br/> |
| <span id="WA_CLICKACTIVE"></span><span id="wa_clickactive"></span><dl> <dt>**WA \_ CLICKACTIVE**</dt> <dt>2</dt> </dl> | Attivato con un clic del mouse.<br/>                                                                                                                                                                     |
| <span id="WA_INACTIVE"></span><span id="wa_inactive"></span><dl> <dt>**WA \_ Inattivo**</dt> <dt>0</dt> </dl>          | Disattivato.<br/>                                                                                                                                                                                    |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per la finestra da attivare o disattivare, a seconda del valore del parametro *wParam* . Se la parola più bassa di *wParam* è **WA \_ inactive**, *lParam* è l'handle per la finestra attivata. Se la parola più bassa di *wParam* è **WA \_ Active** o **WA \_ CLICKACTIVE**, *lParam* è l'handle per la finestra da disattivare. Questo handle può essere **null**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora il messaggio, deve restituire zero.

## <a name="remarks"></a>Commenti

Se la finestra viene attivata e non è ridotta a icona, la funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) imposta lo stato attivo della tastiera sulla finestra. Se la finestra viene attivata con un clic del mouse, riceve anche un messaggio [**WM \_ MOUSEACTIVATE**](wm-mouseactivate.md) .

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

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**SetActiveWindow**](/windows/win32/api/winuser/nf-winuser-setactivewindow)
</dt> <dt>

[**\_MOUSEACTIVATE WM**](wm-mouseactivate.md)
</dt> <dt>

[**\_NCACTIVATE WM**](/windows/desktop/winmsg/wm-ncactivate)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Input da tastiera](keyboard-input.md)
</dt> </dl>

 

