---
description: Inviato a una finestra la cui dimensione, posizione o posizione nell'ordine Z è cambiata in seguito a una chiamata alla funzione SetWindowPos o a un'altra funzione di gestione delle finestre.
ms.assetid: 1eabd0b1-1f92-4576-b7fb-8af50fb04526
title: WM_WINDOWPOSCHANGED messaggio (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14e0900ba4f48b100bad9faf8112df974dee9ba8bfe89c95422698f94cf165c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118030826"
---
# <a name="wm_windowposchanged-message"></a>Messaggio \_ WM WINDOWPOSCHANGED

Inviato a una finestra la cui dimensione, posizione o posizione nell'ordine Z è cambiata in seguito a una chiamata alla funzione [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) o a un'altra funzione di gestione delle finestre.

Una finestra riceve questo messaggio tramite la [**relativa funzione WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_WINDOWPOSCHANGED             0x0047
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos) che contiene informazioni sulle nuove dimensioni e posizione della finestra.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **LRESULT**

Se un'applicazione elabora questo messaggio, deve restituire zero.

## <a name="remarks"></a>Commenti

Per impostazione predefinita, [**la funzione DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) invia i [**messaggi WM \_ SIZE**](wm-size.md) e [**WM \_ MOVE**](wm-move.md) alla finestra. I **messaggi WM \_ SIZE** e **WM \_ MOVE** non vengono inviati se un'applicazione gestisce il messaggio **WM \_ WINDOWPOSCHANGED** senza **chiamare DefWindowProc.** È più efficiente eseguire qualsiasi elaborazione di spostamento o modifica delle dimensioni durante il messaggio **WM \_ WINDOWPOSCHANGED** senza **chiamare DefWindowProc.**

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

[**EndDeferWindowPos**](/windows/win32/api/winuser/nf-winuser-enddeferwindowpos)
</dt> <dt>

[**Setwindowpos**](/windows/win32/api/winuser/nf-winuser-setwindowpos)
</dt> <dt>

[**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos)
</dt> <dt>

[**WM \_ MOVE**](wm-move.md)
</dt> <dt>

[**DIMENSIONI \_ WM**](wm-size.md)
</dt> <dt>

[**FINESTRA \_ WMPOSCHANGING**](wm-windowposchanging.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
