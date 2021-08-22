---
title: WM_NCLBUTTONDBLCLK messaggio (Winuser.h)
description: Pubblicato quando l'utente fa doppio clic sul pulsante sinistro del mouse mentre il cursore si trova all'interno dell'area non client di una finestra. Questo messaggio viene inviato alla finestra che contiene il cursore. Se una finestra ha acquisito il mouse, questo messaggio non viene pubblicato.
ms.assetid: fc655631-64d0-4cc5-b85e-25d274182994
keywords:
- WM_NCLBUTTONDBLCLK messaggio Input tastiera e mouse
topic_type:
- apiref
api_name:
- WM_NCLBUTTONDBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bdf24cbd2e204e3d16f5b9a4038c21c590c23556941acdb4cc5a215c5376c13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119351281"
---
# <a name="wm_nclbuttondblclk-message"></a>Messaggio \_ WM NCLBUTTONDBLCLK

Pubblicato quando l'utente fa doppio clic sul pulsante sinistro del mouse mentre il cursore si trova all'interno dell'area non client di una finestra. Questo messaggio viene inviato alla finestra che contiene il cursore. Se una finestra ha acquisito il mouse, questo messaggio non viene pubblicato.

Una finestra riceve questo messaggio tramite la relativa [**funzione WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_NCLBUTTONDBLCLK              0x00A3
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Valore dell'hit test restituito dalla [**funzione DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) come risultato dell'elaborazione del [**messaggio WM \_ NCHITTEST.**](wm-nchittest.md) Per un elenco di valori di hit test, vedere **WM \_ NCHITTEST**.

</dd> <dt>

*lParam* 
</dt> <dd>

Struttura [**POINTS**](/previous-versions//dd162808(v=vs.85)) che contiene le coordinate x e y del cursore. Le coordinate sono relative all'angolo superiore sinistro dello schermo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora questo messaggio, deve restituire zero.

## <a name="remarks"></a>Commenti

È anche possibile usare le macro [**GET \_ X \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) e [**GET Y \_ \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) per estrarre i valori delle coordinate x e y da *lParam*.


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



> [!IMPORTANT]
> Non usare le macro [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) per estrarre le coordinate x e y della posizione del cursore perché queste macro restituiscono risultati non corretti nei sistemi con più monitor. I sistemi con più monitor possono avere coordinate x e y negative e **LOWORD** e **HIWORD** trattano le coordinate come quantità senza segno.

 

Per impostazione predefinita, la [**funzione DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) verifica il punto specificato per individuare la posizione del cursore ed esegue l'azione appropriata. Se appropriato, **DefWindowProc** invia il [**messaggio \_ SYSCOMMAND WM**](/windows/desktop/menurc/wm-syscommand) alla finestra.

Una finestra non deve avere lo stile **\_ CS DBLCLKS** per ricevere **messaggi WM \_ NCLBUTTONDBLCLK.**

Il sistema genera un messaggio **WM \_ NCLBUTTONDBLCLK** quando l'utente preme, rilascia e preme di nuovo il pulsante sinistro del mouse entro il limite di tempo del doppio clic del sistema. Facendo doppio clic sul pulsante sinistro del mouse vengono effettivamente generati quattro messaggi: [**WM \_ NCLBUTTONDOWN,**](wm-nclbuttondown.md) [**WM \_ NCLBUTTONUP,**](wm-nclbuttonup.md) **WM \_ NCLBUTTONDBLCLK** e **WM \_ NCLBUTTONUP.**

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

[**WM \_ NCLBUTTONDOWN**](wm-nclbuttondown.md)
</dt> <dt>

[**WM \_ NCLBUTTONUP**](wm-nclbuttonup.md)
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

 

