---
title: WM_NCLBUTTONUP messaggio (Winuser.h)
description: Pubblicato quando l'utente rilascia il pulsante sinistro del mouse mentre il cursore si trova all'interno dell'area non client di una finestra. Questo messaggio viene inviato alla finestra che contiene il cursore. Se una finestra ha acquisito il mouse, questo messaggio non viene pubblicato.
ms.assetid: 0c30dcbd-a4ff-43da-bbd2-fbac1a347c11
keywords:
- WM_NCLBUTTONUP messaggio Input tastiera e mouse
topic_type:
- apiref
api_name:
- WM_NCLBUTTONUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae3a79d7bd5c8747efc42e25c71527c35e47598d6d1d1c9f88ae3ed929ea68ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119451431"
---
# <a name="wm_nclbuttonup-message"></a>Messaggio \_ WM NCLBUTTONUP

Pubblicato quando l'utente rilascia il pulsante sinistro del mouse mentre il cursore si trova all'interno dell'area non client di una finestra. Questo messaggio viene inviato alla finestra che contiene il cursore. Se una finestra ha acquisito il mouse, questo messaggio non viene pubblicato.

Una finestra riceve questo messaggio tramite la relativa [**funzione WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_NCLBUTTONUP                  0x00A2
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Valore dell'hit test restituito dalla [**funzione DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) come risultato dell'elaborazione del [**messaggio WM \_ NCHITTEST.**](wm-nchittest.md) Per un elenco dei valori di hit test, vedere **WM \_ NCHITTEST**.

</dd> <dt>

*lParam* 
</dt> <dd>

Struttura [**POINTS**](/previous-versions//dd162808(v=vs.85)) che contiene le coordinate x e y del cursore. Le coordinate sono relative all'angolo superiore sinistro dello schermo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora questo messaggio, deve restituire zero.

## <a name="remarks"></a>Commenti

La [**funzione DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) verifica il punto specificato per individuare la posizione del cursore ed esegue l'azione appropriata. Se appropriato, **DefWindowProc** invia il [**messaggio \_ SYSCOMMAND WM**](/windows/desktop/menurc/wm-syscommand) alla finestra.

È anche possibile usare le macro [**GET \_ X \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) e [**GET Y \_ \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) per estrarre i valori delle coordinate x e y da *lParam*.


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



> [!IMPORTANT]
> Non usare le macro [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) per estrarre le coordinate x e y della posizione del cursore perché queste macro restituiscono risultati non corretti nei sistemi con più monitor. I sistemi con più monitor possono avere coordinate x e y negative e **LOWORD** e **HIWORD** trattano le coordinate come quantità senza segno.

 

Se è appropriato, il sistema invia il [**messaggio \_ SYSCOMMAND WM**](/windows/desktop/menurc/wm-syscommand) alla finestra.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windowsx.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**GET \_ X \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[**GET \_ Y \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[**WM \_ NCHITTEST**](wm-nchittest.md)
</dt> <dt>

[**WM \_ NCLBUTTONDBLCLK**](wm-nclbuttondblclk.md)
</dt> <dt>

[**WM \_ NCLBUTTONDOWN**](wm-nclbuttondown.md)
</dt> <dt>

[**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Mouse Input](mouse-input.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**MAKEPOINT**](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

[**Punti**](/previous-versions//dd162808(v=vs.85))
</dt> </dl>

 

