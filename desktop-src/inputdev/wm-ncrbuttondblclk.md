---
title: WM_NCRBUTTONDBLCLK messaggio (Winuser.h)
description: Inviato quando l'utente fa doppio clic sul pulsante destro del mouse mentre il cursore si trova all'interno dell'area non client di una finestra. Questo messaggio viene inviato alla finestra che contiene il cursore. Se il mouse è stato acquisito da una finestra, questo messaggio non viene inviato.
ms.assetid: 20d62b05-07de-49da-b160-29fa1f5067fa
keywords:
- WM_NCRBUTTONDBLCLK messaggio Input da tastiera e mouse
topic_type:
- apiref
api_name:
- WM_NCRBUTTONDBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9af62a21da645a265e5264ffae47ad8cb0907ec6fb0106cfb9e7cee97b7f42e3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119666301"
---
# <a name="wm_ncrbuttondblclk-message"></a>Messaggio \_ WM NCRBUTTONDBLCLK

Inviato quando l'utente fa doppio clic sul pulsante destro del mouse mentre il cursore si trova all'interno dell'area non client di una finestra. Questo messaggio viene inviato alla finestra che contiene il cursore. Se il mouse è stato acquisito da una finestra, questo messaggio non viene inviato.

Una finestra riceve questo messaggio tramite la [**relativa funzione WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_NCRBUTTONDBLCLK              0x00A6
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

Una finestra non deve avere lo stile **\_ CS DBLCLKS** per ricevere **messaggi WM \_ NCRBUTTONDBLCLK.**

Il sistema genera un messaggio **WM \_ NCRBUTTONDBLCLK** quando l'utente preme, rilascia e di nuovo preme il pulsante destro del mouse entro il limite di tempo del doppio clic del sistema. Facendo doppio clic con il pulsante destro del mouse vengono effettivamente generati quattro messaggi: [**WM \_ NCRBUTTONDOWN**](wm-ncrbuttondown.md), [**WM \_ NCRBUTTONUP**](wm-ncrbuttonup.md), **WM \_ NCRBUTTONDBLCLK** e **WM \_ NCRBUTTONUP.**

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

[**WM \_ NCRBUTTONDOWN**](wm-ncrbuttondown.md)
</dt> <dt>

[**WM \_ NCRBUTTONUP**](wm-ncrbuttonup.md)
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

 

