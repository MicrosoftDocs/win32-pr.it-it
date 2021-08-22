---
description: Inviato a una finestra per recuperare un handle per l'icona grande o piccola associata a una finestra. Il sistema visualizza l'icona grande nella finestra di dialogo ALT+TAB e l'icona piccola nella didascalia della finestra.
ms.assetid: d3101a9b-9658-4a21-b1f6-2920b723926c
title: WM_GETICON messaggio (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2df8922fa09cf425594a07768f0d7c9ae0ac09222647f181f45331c2b0d47fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119587421"
---
# <a name="wm_geticon-message"></a>Messaggio \_ WM GETICON

Inviato a una finestra per recuperare un handle per l'icona grande o piccola associata a una finestra. Il sistema visualizza l'icona grande nella finestra di dialogo ALT+TAB e l'icona piccola nella didascalia della finestra.

Una finestra riceve questo messaggio tramite la relativa [**funzione WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_GETICON                      0x007F
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Tipo di icona recuperata. Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                                                                          | Significato                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ICON_BIG"></span><span id="icon_big"></span><dl> <dt>**ICONA \_ BIG**</dt> <dt>1</dt> </dl>          | Recuperare l'icona grande per la finestra.<br/>                                                                                                                   |
| <span id="ICON_SMALL"></span><span id="icon_small"></span><dl> <dt>**ICONA \_ SMALL**</dt> <dt>0</dt> </dl>    | Recuperare la piccola icona per la finestra.<br/>                                                                                                                   |
| <span id="ICON_SMALL2"></span><span id="icon_small2"></span><dl> <dt>**ICONA \_ SMALL2**</dt> <dt>2</dt> </dl> | Recupera la piccola icona fornita dall'applicazione. Se l'applicazione non ne fornisce una, il sistema usa l'icona generata dal sistema per tale finestra.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Valore DPI dell'icona recuperata. Può essere usato per fornire icone diverse a seconda delle dimensioni dell'icona.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HICON**

Il valore restituito è un handle per l'icona grande o piccola, a seconda del valore di *wParam*. Quando un'applicazione riceve questo messaggio, può restituire un handle a un'icona grande o piccola o passare il messaggio alla [**funzione DefWindowProc.**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)

## <a name="remarks"></a>Commenti

Quando un'applicazione riceve questo messaggio, può restituire un handle a un'icona grande o piccola o passare il messaggio a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).

[**DefWindowProc restituisce**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) un handle per l'icona grande o piccola associata alla finestra, a seconda del valore di *wParam*.

Una finestra senza icona impostata in modo esplicito (con **WM \_ SETICON**) usa l'icona per la classe finestra registrata e in questo caso [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) restituirà 0 per un messaggio **WM \_ GETICON.** Se **l'invio di un messaggio WM \_ GETICON** a una finestra restituisce 0, provare a chiamare la [**funzione GetClassLongPtr**](/windows/win32/api/winuser/nf-winuser-getclasslongptra) per la finestra. Se restituisce 0, provare la [**funzione LoadIcon.**](/windows/win32/api/winuser/nf-winuser-loadicona)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**WM \_ SETICON**](wm-seticon.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
