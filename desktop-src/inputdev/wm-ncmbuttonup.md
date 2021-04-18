---
title: Messaggio WM_NCMBUTTONUP (winuser. h)
description: Inviato quando l'utente rilascia il pulsante centrale del mouse mentre il cursore si trova all'interno dell'area non client di una finestra. Questo messaggio viene inserito nella finestra che contiene il cursore. Se una finestra ha acquisito il mouse, questo messaggio non viene inviato.
ms.assetid: 93335e46-c72b-4139-9785-67ce2a6bcb4a
keywords:
- Input della tastiera e del mouse WM_NCMBUTTONUP messaggio
topic_type:
- apiref
api_name:
- WM_NCMBUTTONUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a890c79f6835dc0f44257fc1adf5d00b976a87c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301419"
---
# <a name="wm_ncmbuttonup-message"></a>\_Messaggio NCMBUTTONUP WM

Inviato quando l'utente rilascia il pulsante centrale del mouse mentre il cursore si trova all'interno dell'area non client di una finestra. Questo messaggio viene inserito nella finestra che contiene il cursore. Se una finestra ha acquisito il mouse, questo messaggio non viene inviato.

Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_NCMBUTTONUP                  0x00A8
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

 

Se è appropriato, il sistema invia il messaggio [**\_ SYSCOMMAND WM**](/windows/desktop/menurc/wm-syscommand) alla finestra.

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

[**\_NCMBUTTONDBLCLK WM**](wm-ncmbuttondblclk.md)
</dt> <dt>

[**\_NCMBUTTONDOWN WM**](wm-ncmbuttondown.md)
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

 

