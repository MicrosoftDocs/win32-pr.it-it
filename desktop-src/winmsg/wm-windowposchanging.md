---
description: Inviato a una finestra la cui dimensione, posizione o posizione nell'ordine Z sta per cambiare in seguito a una chiamata alla funzione SetWindowPos o a un'altra funzione di gestione della finestra.
ms.assetid: 45ecd966-5222-4738-9e99-8a6edbdd435a
title: WM_WINDOWPOSCHANGING messaggio (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68f10abcb0692374209c2070a465df7c4a5f18672eebf376378d6fb16cbca537
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119771941"
---
# <a name="wm_windowposchanging-message"></a>Messaggio \_ WM WINDOWPOSCHANGING

Inviato a una finestra la cui dimensione, posizione o posizione nell'ordine Z sta per cambiare in seguito a una chiamata alla funzione [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) o a un'altra funzione di gestione della finestra.

Una finestra riceve questo messaggio tramite la relativa [**funzione WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


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

Puntatore a una [**struttura WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos) che contiene informazioni sulle nuove dimensioni e posizione della finestra.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **LRESULT**

Se un'applicazione elabora questo messaggio, deve restituire zero.

## <a name="remarks"></a>Commenti

Per una finestra con [**lo stile WS \_ OVERLAPPED**](window-styles.md) o **WS \_ THICKFRAME,** la funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) invia il messaggio [**WM \_ GETMINMAXINFO**](wm-getminmaxinfo.md) alla finestra. Questa operazione viene eseguita per convalidare le nuove dimensioni e posizione della finestra e per applicare gli stili client [CS \_ BYTEALIGNCLIENT](about-window-classes.md) e CS \_ BYTEALIGNWINDOW. Non passando il **messaggio WM \_ WINDOWPOSCHANGING** alla **funzione DefWindowProc,** un'applicazione può eseguire l'override di queste impostazioni predefinite.

Durante l'elaborazione di questo messaggio, la modifica di uno dei valori in [**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos) influisce sulle nuove dimensioni, posizione o posizione della finestra nell'ordine Z. Un'applicazione può impedire modifiche alla finestra impostando o cancellando i bit appropriati nel membro **flags** di **WINDOWPOS**.

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

[**WM \_ GETMINMAXINFO**](wm-getminmaxinfo.md)
</dt> <dt>

[**WM \_ MOVE**](wm-move.md)
</dt> <dt>

[**DIMENSIONI \_ WM**](wm-size.md)
</dt> <dt>

[**WM \_ WINDOWPOSCHANGED**](wm-windowposchanged.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
