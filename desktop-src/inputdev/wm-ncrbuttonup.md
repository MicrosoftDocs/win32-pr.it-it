---
title: WM_NCRBUTTONUP messaggio (Winuser.h)
description: Inviato quando l'utente rilascia il pulsante destro del mouse mentre il cursore si trova all'interno dell'area non client di una finestra. Questo messaggio viene inviato alla finestra che contiene il cursore. Se il mouse è stato acquisito da una finestra, questo messaggio non viene inviato.
ms.assetid: dc77c235-9e57-4051-b197-bd7ee7535a6f
keywords:
- WM_NCRBUTTONUP messaggio Input da tastiera e mouse
topic_type:
- apiref
api_name:
- WM_NCRBUTTONUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b17d21429193c84ae71121c1841d54e19d5f12793a6916f1ed14c4c3b34d3d82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119611421"
---
# <a name="wm_ncrbuttonup-message"></a>Messaggio \_ NCRBUTTONUP WM

Inviato quando l'utente rilascia il pulsante destro del mouse mentre il cursore si trova all'interno dell'area non client di una finestra. Questo messaggio viene inviato alla finestra che contiene il cursore. Se il mouse è stato acquisito da una finestra, questo messaggio non viene inviato.

Una finestra riceve questo messaggio tramite la [**relativa funzione WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_NCRBUTTONUP                  0x00A5
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Valore dell'hit test restituito [**dalla funzione DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) in seguito all'elaborazione del [**messaggio WM \_ NCHITTEST.**](wm-nchittest.md) Per un elenco di valori di hit test, vedere **WM \_ NCHITTEST.**

</dd> <dt>

*lParam* 
</dt> <dd>

Struttura [**POINTS**](/previous-versions//dd162808(v=vs.85)) contenente le coordinate x e y del cursore. Le coordinate sono relative all'angolo superiore sinistro dello schermo.

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

 

Se è appropriato, il sistema invia il messaggio [**\_ SYSCOMMAND WM**](/windows/desktop/menurc/wm-syscommand) alla finestra.

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

[**WM \_ NCRBUTTONDBLCLK**](wm-ncrbuttondblclk.md)
</dt> <dt>

[**WM \_ NCRBUTTONDOWN**](wm-ncrbuttondown.md)
</dt> <dt>

[**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Mouse Input](mouse-input.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**PUNTI DI APPLICAZIONE**](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

[**Punti**](/previous-versions//dd162808(v=vs.85))
</dt> </dl>

 

