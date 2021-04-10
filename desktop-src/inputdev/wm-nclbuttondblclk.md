---
title: Messaggio WM_NCLBUTTONDBLCLK (winuser. h)
description: Inviato quando l'utente fa doppio clic con il pulsante sinistro del mouse mentre il cursore si trova all'interno dell'area non client di una finestra. Questo messaggio viene inserito nella finestra che contiene il cursore. Se una finestra ha acquisito il mouse, questo messaggio non viene inviato.
ms.assetid: fc655631-64d0-4cc5-b85e-25d274182994
keywords:
- Input della tastiera e del mouse WM_NCLBUTTONDBLCLK messaggio
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
ms.openlocfilehash: db66edcb3b1645c6c34c72e35df53afc516dafc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119503"
---
# <a name="wm_nclbuttondblclk-message"></a>\_Messaggio NCLBUTTONDBLCLK WM

Inviato quando l'utente fa doppio clic con il pulsante sinistro del mouse mentre il cursore si trova all'interno dell'area non client di una finestra. Questo messaggio viene inserito nella finestra che contiene il cursore. Se una finestra ha acquisito il mouse, questo messaggio non viene inviato.

Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_NCLBUTTONDBLCLK              0x00A3
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Valore di hit test restituito dalla funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) come risultato dell'elaborazione del messaggio [**WM \_ NCHITTEST**](wm-nchittest.md) . Per un elenco dei valori di hit test, vedere **WM \_ NCHITTEST**.

</dd> <dt>

*lParam* 
</dt> <dd>

Struttura [**Points**](/previous-versions//dd162808(v=vs.85)) che contiene le coordinate x e y del cursore. Le coordinate sono relative all'angolo superiore sinistro dello schermo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora il messaggio, deve restituire zero.

## <a name="remarks"></a>Commenti

È anche possibile usare le macro [**get \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) e [**get \_ y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) per estrarre i valori delle coordinate X e Y da *lParam*.


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



> [!IMPORTANT]
> Non usare le macro [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) per estrarre le coordinate x e y della posizione del cursore perché queste macro restituiscono risultati non corretti nei sistemi con più monitoraggi. I sistemi con più monitoraggi possono avere coordinate x e y negative e **LOWORD** e **HIWORD** considerano le coordinate come quantità senza segno.

 

Per impostazione predefinita, la funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) verifica il punto specificato per individuare la posizione del cursore ed esegue l'azione appropriata. Se appropriato, **DefWindowProc** invia il messaggio [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) alla finestra.

Una finestra non deve avere lo stile **cs \_ DBLCLKS** per ricevere i messaggi **WM \_ NCLBUTTONDBLCLK** .

Il sistema genera un messaggio **WM \_ NCLBUTTONDBLCLK** quando l'utente preme, rilascia e preme di nuovo il pulsante sinistro del mouse nel limite di tempo doppio clic del sistema. Se si fa doppio clic con il pulsante sinistro del mouse, vengono effettivamente generati quattro messaggi: [**WM \_ NCLBUTTONDOWN**](wm-nclbuttondown.md), [**WM \_ NCLBUTTONUP**](wm-nclbuttonup.md), **WM \_ NCLBUTTONDBLCLK** e **WM \_ NCLBUTTONUP** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include WINDOWSX. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**Ottieni \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[**OTTENERE \_ il \_ lParam Y**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[**\_NCHITTEST WM**](wm-nchittest.md)
</dt> <dt>

[**\_NCLBUTTONDOWN WM**](wm-nclbuttondown.md)
</dt> <dt>

[**\_NCLBUTTONUP WM**](wm-nclbuttonup.md)
</dt> <dt>

[**\_SYSCOMMAND WM**](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Input del mouse](mouse-input.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

[**PUNTI**](/previous-versions//dd162808(v=vs.85))
</dt> </dl>

 

