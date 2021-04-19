---
description: Inviato a una finestra per recuperare un handle per l'icona grande o piccola associata a una finestra. Il sistema Visualizza l'icona grande nella finestra di dialogo ALT + TAB e l'icona piccola nella didascalia della finestra.
ms.assetid: d3101a9b-9658-4a21-b1f6-2920b723926c
title: Messaggio WM_GETICON (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83d2444e70646d8122a7228094187738811a3f68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314862"
---
# <a name="wm_geticon-message"></a>\_Messaggio WM GETicon

Inviato a una finestra per recuperare un handle per l'icona grande o piccola associata a una finestra. Il sistema Visualizza l'icona grande nella finestra di dialogo ALT + TAB e l'icona piccola nella didascalia della finestra.

Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_GETICON                      0x007F
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Tipo di icona da recuperare. Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                                                                          | Significato                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ICON_BIG"></span><span id="icon_big"></span><dl> <dt>**Icona \_ di BIG**</dt> <dt>1</dt> </dl>          | Recuperare l'icona grande per la finestra.<br/>                                                                                                                   |
| <span id="ICON_SMALL"></span><span id="icon_small"></span><dl> <dt>**Icona \_ di PICCOLO**</dt> <dt>0</dt> </dl>    | Recuperare l'icona piccola per la finestra.<br/>                                                                                                                   |
| <span id="ICON_SMALL2"></span><span id="icon_small2"></span><dl> <dt>**Icona \_ di SMALL2**</dt> <dt>2</dt> </dl> | Recupera l'icona piccola fornita dall'applicazione. Se l'applicazione non ne fornisce uno, il sistema utilizza l'icona generata dal sistema per tale finestra.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Valore DPI dell'icona da recuperare. Questa operazione può essere utilizzata per fornire icone diverse a seconda delle dimensioni dell'icona.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HICON**

Il valore restituito è un handle per l'icona grande o piccola, a seconda del valore di *wParam*. Quando un'applicazione riceve questo messaggio, può restituire un handle a un'icona grande o piccola oppure passare il messaggio alla funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) .

## <a name="remarks"></a>Commenti

Quando un'applicazione riceve questo messaggio, può restituire un handle a un'icona grande o piccola oppure passare il messaggio a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) restituisce un handle per l'icona grande o piccola associata alla finestra, a seconda del valore di *wParam*.

Una finestra priva di icona impostata in modo esplicito (con l' **\_ icona WM**) usa l'icona per la classe della finestra registrata e in questo caso [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) restituirà 0 per un messaggio **WM \_ GetIcon** . Se l'invio di un messaggio **WM \_ GetIcon** a una finestra restituisce 0, provare a chiamare la funzione [**GetClassLongPtr**](/windows/win32/api/winuser/nf-winuser-getclasslongptra) per la finestra. Se restituisce 0, provare la funzione [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona) .

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

[**ICONA di WM \_**](wm-seticon.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
