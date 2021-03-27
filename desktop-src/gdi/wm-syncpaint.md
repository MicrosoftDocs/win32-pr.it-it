---
description: Il \_ messaggio WM SYNCPAINT viene usato per sincronizzare il disegno evitando il collegamento di thread GUI indipendenti.
ms.assetid: 4446be4e-e0b9-46ce-95b2-bea876348c25
title: Messaggio WM_SYNCPAINT (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5602e867af9b7ce467e8979c9f341758414ad287
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994549"
---
# <a name="wm_syncpaint-message"></a>\_Messaggio SYNCPAINT WM

Il messaggio **WM \_ SYNCPAINT** viene usato per sincronizzare il disegno evitando il collegamento di thread GUI indipendenti.

Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


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

Questo parametro non viene usato.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Un'applicazione restituisce zero se elabora questo messaggio.

## <a name="remarks"></a>Commenti

Quando una finestra è stata nascosta, mostrata, spostata o ridimensionata, il sistema può determinare che è necessario inviare un messaggio **WM \_ SYNCPAINT** alle finestre di primo livello di altri thread. Le applicazioni devono passare **WM \_ SYNCPAINT** a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  per l'elaborazione. La funzione **DefWindowProc** invierà un messaggio [**WM \_ NCPAINT**](wm-ncpaint.md) alla routine della finestra se la cornice della finestra deve essere disegnata e invierà un messaggio [**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md) se lo sfondo della finestra deve essere cancellato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Cenni preliminari su disegno e disegno](painting-and-drawing.md)
</dt> <dt>

[Disegno e creazione di messaggi](painting-and-drawing-messages.md)
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex)
</dt> <dt>

[**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc)
</dt> <dt>

[**\_disegno WM**](wm-paint.md)
</dt> </dl>

 

 
