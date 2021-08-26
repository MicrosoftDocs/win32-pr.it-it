---
Description: Il messaggio WM PAINT viene inviato quando il sistema o un'altra applicazione effettua una richiesta per disegnare una parte della finestra \_ di un'applicazione.
ms.assetid: afebaa07-cf00-47db-a919-46436f164881
title: WM_PAINT messaggio (Winuser.h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: b5efec4bc92fcb3c90a8def59b2e85d98342cf641dfe959fc2a651f81ffc1f77
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092511"
---
# <a name="wm_paint-message"></a>Messaggio WM \_ PAINT

Il **messaggio WM \_ PAINT** viene inviato quando il sistema o un'altra applicazione effettua una richiesta per disegnare una parte della finestra di un'applicazione. Il messaggio viene inviato quando viene chiamata la funzione [**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow) o [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) oppure dalla funzione [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) quando l'applicazione ottiene un messaggio **WM \_ PAINT** usando la funzione [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) o [**PeekMessage.**](/windows/win32/api/winuser/nf-winuser-peekmessagea)

Una finestra riceve questo messaggio tramite la [**relativa funzione WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


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

Un'applicazione restituisce zero se elabora il messaggio.

## <a name="example"></a>Esempio

```c
LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
    case WM_DESTROY:
        PostQuitMessage(0);
        return 0;

    case WM_PAINT:
        {
            PAINTSTRUCT ps;
            HDC hdc = BeginPaint(hwnd, &ps);

            // All painting occurs here, between BeginPaint and EndPaint.
            FillRect(hdc, &ps.rcPaint, (HBRUSH) (COLOR_WINDOW+1));
            EndPaint(hwnd, &ps);
        }
        return 0;
    }

    return DefWindowProc(hwnd, uMsg, wParam, lParam);
}

```

Esempio di [Windows esempi classici](https://github.com/microsoft/Windows-classic-samples/blob/18cbd05ee44455cd7552804dcf2c9d6db619b412/Samples/Win7Samples/begin/LearnWin32/HelloWorld/cpp/main.cpp) in GitHub.

## <a name="remarks"></a>Commenti

Il **messaggio WM \_ PAINT** viene generato dal sistema e non deve essere inviato da un'applicazione. Per forzare il disegno di una finestra in un contesto di dispositivo specifico, usare il [**messaggio WM \_ PRINT**](wm-print.md) o [**WM \_ PRINTCLIENT.**](wm-printclient.md) Si noti che questa operazione richiede che la finestra di destinazione supporti **il messaggio \_ PRINTCLIENT WM.** I controlli più comuni supportano **il messaggio \_ PRINTCLIENT WM.**

La [**funzione DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  convalida l'area di aggiornamento. La funzione può anche inviare il messaggio [**\_ WM NCPAINT**](wm-ncpaint.md) alla routine della finestra se è necessario disegnare la cornice della finestra e inviare il messaggio [**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md) se lo sfondo della finestra deve essere cancellato.

Il sistema invia questo messaggio quando non sono presenti altri messaggi nella coda di messaggi dell'applicazione. [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) determina dove inviare il messaggio. [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) determina quale messaggio inviare. **GetMessage** restituisce il **messaggio WM \_ PAINT** quando non sono presenti altri messaggi nella coda di messaggi dell'applicazione e **DispatchMessage** invia il messaggio alla routine della finestra appropriata.

Una finestra può ricevere messaggi di disegno interni in seguito alla chiamata di [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) con il \_ flag RDW INTERNALPAINT impostato. In questo caso, la finestra potrebbe non avere un'area di aggiornamento. Un'applicazione può chiamare la [**funzione GetUpdateRect**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect) per determinare se la finestra ha un'area di aggiornamento. Se **GetUpdateRect restituisce** zero, l'applicazione non deve chiamare le [**funzioni BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) [**ed EndPaint.**](/windows/desktop/api/Winuser/nf-winuser-endpaint)

Un'applicazione deve verificare la presenza del disegno interno necessario esaminando le strutture di dati interne per ogni messaggio **WM \_ PAINT,** perché un messaggio **WM \_ PAINT** potrebbe essere stato causato da un'area di aggiornamento non NULL e da una chiamata a [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) con il flag RDW \_ INTERNALPAINT impostato.

Il sistema invia un messaggio **WM \_ PAINT** interno una sola volta. Dopo che un messaggio **WM \_ PAINT** interno viene restituito da [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) o [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) o viene inviato a una finestra da [**UpdateWindow,**](/windows/desktop/api/Winuser/nf-winuser-updatewindow)il sistema non pubblica o invia altri messaggi **WM \_ PAINT** fino a quando la finestra non viene invalidata o finché non viene chiamato di nuovo [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) con il flag RDW \_ INTERNALPAINT impostato.

Per alcuni controlli comuni, l'elaborazione **predefinita dei messaggi WM \_ PAINT** controlla il *parametro wParam.* Se *wParam* è diverso da NULL, il controllo presuppone che il valore sia un HDC e disegna usando tale contesto di dispositivo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Cenni preliminari sul disegno e sul disegno](painting-and-drawing.md)
</dt> <dt>

[Disegnare e disegnare messaggi](painting-and-drawing-messages.md)
</dt> <dt>

[**Beginpaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint)
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage)
</dt> <dt>

[**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint)
</dt> <dt>

[**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage)
</dt> <dt>

[**GetUpdateRect**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect)
</dt> <dt>

[**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea)
</dt> <dt>

[**RidisegnaFinestra**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow)
</dt> <dt>

[**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow)
</dt> <dt>

[**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md)
</dt> <dt>

[**WM \_ NCPAINT**](wm-ncpaint.md)
</dt> <dt>

[**WM \_ PRINT**](wm-print.md)
</dt> <dt>

[**WM \_ PRINTCLIENT**](wm-printclient.md)
</dt> </dl>

 

 
