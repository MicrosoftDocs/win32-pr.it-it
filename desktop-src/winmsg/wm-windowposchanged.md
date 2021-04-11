---
description: Inviato a una finestra la cui dimensione, posizione o posizione nella z order è cambiata in seguito a una chiamata alla funzione SetWindowPos o a un'altra funzione di gestione della finestra.
ms.assetid: 1eabd0b1-1f92-4576-b7fb-8af50fb04526
title: Messaggio WM_WINDOWPOSCHANGED (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d9bda353a1c7546727818a8a3975696000da0e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128958"
---
# <a name="wm_windowposchanged-message"></a>\_Messaggio WINDOWPOSCHANGED WM

Inviato a una finestra la cui dimensione, posizione o posizione nella z order è cambiata in seguito a una chiamata alla funzione [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) o a un'altra funzione di gestione della finestra.

Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


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

Puntatore a una struttura [**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos) che contiene informazioni sulle nuove dimensioni e posizione della finestra.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **LRESULT**

Se un'applicazione elabora il messaggio, deve restituire zero.

## <a name="remarks"></a>Commenti

Per impostazione predefinita, la funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) invia i messaggi di [**\_ dimensioni WM**](wm-size.md) e di [**\_ spostamento WM**](wm-move.md) alla finestra. I messaggi WM **\_ size** e **WM \_ Move** non vengono inviati se un'applicazione gestisce il messaggio **WM \_ WINDOWPOSCHANGED** senza chiamare **DefWindowProc**. È più efficiente eseguire un'elaborazione delle modifiche di spostamento o di ridimensionamento durante il messaggio **WM \_ WINDOWPOSCHANGED** senza chiamare **DefWindowProc**.

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

[**\_spostamento WM**](wm-move.md)
</dt> <dt>

[**\_dimensioni WM**](wm-size.md)
</dt> <dt>

[**\_WINDOWPOSCHANGING WM**](wm-windowposchanging.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
