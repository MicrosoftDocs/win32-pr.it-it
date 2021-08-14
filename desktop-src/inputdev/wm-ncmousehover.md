---
title: WM_NCMOUSEHOVER messaggio (Winuser.h)
description: Inviato a una finestra quando il cursore si posiziona sull'area non client della finestra per il periodo di tempo specificato in una chiamata precedente a TrackMouseEvent.
ms.assetid: ca1afdc2-7884-445e-b9b7-4d7dd5dcea38
keywords:
- WM_NCMOUSEHOVER messaggio Input da tastiera e mouse
topic_type:
- apiref
api_name:
- WM_NCMOUSEHOVER
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 323464d32a2529475823003e51d5bbf0b15c616e32edb0622efe5be7f94dfb4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119611461"
---
# <a name="wm_ncmousehover-message"></a>Messaggio \_ WM NCMOUSEHOVER

Inviato a una finestra quando il cursore si posiziona sull'area non client della finestra per il periodo di tempo specificato in una chiamata precedente a [**TrackMouseEvent.**](/windows/win32/api/winuser/nf-winuser-trackmouseevent)

Una finestra riceve questo messaggio tramite la [**relativa funzione WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_NCMOUSEHOVER                 0x02A0
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

Il rilevamento al passaggio del mouse si interrompe quando viene generato questo messaggio. L'applicazione deve chiamare [**nuovamente TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) se richiede un ulteriore rilevamento del comportamento del passaggio del mouse.

È anche possibile usare le macro [**GET \_ X \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) e [**GET Y \_ \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) per estrarre i valori delle coordinate x e y da *lParam*.


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



> [!IMPORTANT]
> Non usare le macro [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) per estrarre le coordinate x e y della posizione del cursore perché queste macro restituiscono risultati non corretti nei sistemi con più monitor. I sistemi con più monitor possono avere coordinate x e y negative e **LOWORD** e **HIWORD** trattano le coordinate come quantità senza segno.

 

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

[**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent)
</dt> <dt>

[**TRACKMOUSEEVENT**](/windows/win32/api/winuser/ns-winuser-trackmouseevent)
</dt> <dt>

[**WM \_ NCHITTEST**](wm-nchittest.md)
</dt> <dt>

[**WM \_ MOUSEHOVER**](wm-mousehover.md)
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

 

