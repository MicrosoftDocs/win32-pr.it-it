---
description: Inviato a una finestra la cui dimensione, posizione o posizione nella z order sta per essere modificata in seguito a una chiamata alla funzione SetWindowPos o a un'altra funzione di gestione della finestra.
ms.assetid: 45ecd966-5222-4738-9e99-8a6edbdd435a
title: Messaggio WM_WINDOWPOSCHANGING (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 015a31aac31d38506d1798f83c8dd7f9aa646f85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758462"
---
# <a name="wm_windowposchanging-message"></a>\_Messaggio WINDOWPOSCHANGING WM

Inviato a una finestra la cui dimensione, posizione o posizione nella z order sta per essere modificata in seguito a una chiamata alla funzione [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) o a un'altra funzione di gestione della finestra.

Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_WINDOWPOSCHANGING            0x0046
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos) che contiene informazioni sulle nuove dimensioni e posizione della finestra.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **LRESULT**

Se un'applicazione elabora il messaggio, deve restituire zero.

## <a name="remarks"></a>Commenti

Per una finestra con lo [**stile \_ WS Overlapped**](window-styles.md) o **WS \_ THICKFRAME** , la funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) invia il messaggio [**WM \_ GETMINMAXINFO**](wm-getminmaxinfo.md) alla finestra. Questa operazione viene eseguita per convalidare le nuove dimensioni e la nuova posizione della finestra e per applicare gli stili del client [cs \_ BYTEALIGNCLIENT](about-window-classes.md) e cs \_ BYTEALIGNWINDOW. Se non si passa il messaggio **WM \_ WINDOWPOSCHANGING** alla funzione **DefWindowProc** , un'applicazione può eseguire l'override di queste impostazioni predefinite.

Durante l'elaborazione di questo messaggio, la modifica di uno dei valori di [**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos) influiscono sulla nuova dimensione, posizione o posizione della finestra nella z order. Un'applicazione può impedire modifiche alla finestra impostando o deselezionando i bit appropriati nel membro **Flags** di **WINDOWPOS**.

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

[**EndDeferWindowPos**](/windows/win32/api/winuser/nf-winuser-enddeferwindowpos)
</dt> <dt>

[**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos)
</dt> <dt>

[**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos)
</dt> <dt>

[**\_GETMINMAXINFO WM**](wm-getminmaxinfo.md)
</dt> <dt>

[**\_spostamento WM**](wm-move.md)
</dt> <dt>

[**\_dimensioni WM**](wm-size.md)
</dt> <dt>

[**\_WINDOWPOSCHANGED WM**](wm-windowposchanged.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
