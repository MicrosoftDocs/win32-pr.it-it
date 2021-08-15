---
description: Il messaggio WM \_ NCPAINT viene inviato a una finestra quando è necessario disegnare il frame.
ms.assetid: d8a2a8b9-2c5d-484c-be09-67eb33de67c0
title: WM_NCPAINT messaggio (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6be5fa951d50dbaf8663e34a5d9476ecb62576c203095bed9427dcef44425690
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118978001"
---
# <a name="wm_ncpaint-message"></a>Messaggio \_ WM NCPAINT

Il **messaggio WM \_ NCPAINT** viene inviato a una finestra quando è necessario disegnare il frame.

Una finestra riceve questo messaggio tramite la relativa [**funzione WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per l'area di aggiornamento della finestra. L'area di aggiornamento viene ritagliata nella cornice della finestra.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Un'applicazione restituisce zero se elabora questo messaggio.

## <a name="remarks"></a>Commenti

La [**funzione DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) disegna la cornice della finestra.

Un'applicazione può intercettare **il messaggio \_ WM NCPAINT** e disegnare la propria cornice di finestra personalizzata. L'area di ritaglio per una finestra è sempre rettangolare, anche se la forma della cornice viene modificata.

Il *valore wParam* può essere passato a [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) come nell'esempio seguente.


```C++
case WM_NCPAINT:
{
    HDC hdc;
    hdc = GetDCEx(hwnd, (HRGN)wParam, DCX_WINDOW|DCX_INTERSECTRGN);
    // Paint into this DC 
    ReleaseDC(hwnd, hdc);
}
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Panoramica di disegno e disegno](painting-and-drawing.md)
</dt> <dt>

[Disegno e disegno di messaggi](painting-and-drawing-messages.md)
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc)
</dt> <dt>

[**WM \_ PAINT**](wm-paint.md)
</dt> <dt>

[**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex)
</dt> </dl>

 

 
