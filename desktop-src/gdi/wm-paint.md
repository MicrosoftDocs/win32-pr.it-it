---
Description: Il \_ messaggio di disegno WM viene inviato quando il sistema o un'altra applicazione esegue una richiesta per disegnare una parte della finestra di un'applicazione.
ms.assetid: afebaa07-cf00-47db-a919-46436f164881
title: Messaggio WM_PAINT (winuser. h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: b13e1779fb54a3db7905cb8fc738ef45558400f5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "104982955"
---
# <a name="wm_paint-message"></a>\_Messaggio di disegno WM

Il messaggio di **\_ disegno WM** viene inviato quando il sistema o un'altra applicazione esegue una richiesta per disegnare una parte della finestra di un'applicazione. Il messaggio viene inviato quando viene chiamata la funzione [**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow) o [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) oppure tramite la funzione [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) quando l'applicazione ottiene un messaggio di **\_ disegno WM** utilizzando la funzione [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) o [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) .

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

Esempio di [esempi di Windows classico](https://github.com/microsoft/Windows-classic-samples/blob/18cbd05ee44455cd7552804dcf2c9d6db619b412/Samples/Win7Samples/begin/LearnWin32/HelloWorld/cpp/main.cpp) in GitHub.

## <a name="remarks"></a>Commenti

Il messaggio di **\_ disegno WM** viene generato dal sistema e non deve essere inviato da un'applicazione. Per forzare una finestra a creare un contesto di dispositivo specifico, usare il messaggio [**WM \_ Print**](wm-print.md) o [**WM \_ PRINTCLIENT**](wm-printclient.md) . Si noti che questa operazione richiede che la finestra di destinazione supporti il messaggio **WM \_ PRINTCLIENT** . I controlli più comuni supportano il messaggio **WM \_ PRINTCLIENT** .

La funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  convalida l'area di aggiornamento. La funzione può anche inviare il messaggio [**WM \_ NCPAINT**](wm-ncpaint.md) alla routine della finestra se è necessario disegnare la cornice della finestra e inviare il messaggio [**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md) se lo sfondo della finestra deve essere cancellato.

Il sistema invia questo messaggio quando non sono presenti altri messaggi nella coda di messaggi dell'applicazione. [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) determina la posizione in cui inviare il messaggio. [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) determina il messaggio da inviare. **GetMessage** restituisce il messaggio di **\_ disegno WM** quando non sono presenti altri messaggi nella coda di messaggi dell'applicazione e **DispatchMessage** invia il messaggio alla routine della finestra appropriata.

Una finestra può ricevere messaggi di disegno interni in seguito alla chiamata di [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) con il \_ flag RDW INTERNALPAINT impostato. In questo caso, è possibile che la finestra non disponga di un'area di aggiornamento. Un'applicazione può chiamare la funzione [**GetUpdateRect**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect) per determinare se la finestra dispone di un'area di aggiornamento. Se **GetUpdateRect** restituisce zero, l'applicazione non deve chiamare le funzioni [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) e [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) .

Un'applicazione deve verificare la presenza di un disegno interno necessario esaminando le strutture di dati interne per ogni messaggio di **\_ disegno WM** , perché un messaggio di **\_ disegno WM** potrebbe essere stato causato da un'area di aggiornamento non null e da una chiamata a [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) con il \_ flag RDW INTERNALPAINT impostato.

Il sistema invia un messaggio **di \_ disegno WM** interno una sola volta. Dopo che un messaggio di **\_ disegno WM** interno viene restituito da [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) o [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) o viene inviato a una finestra da [**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow), il sistema non pubblica o invia ulteriori messaggi di **\_ disegno WM** fino a quando la finestra non viene invalidata o fino a quando [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) viene richiamato con il \_ flag RDW INTERNALPAINT impostato.

Per alcuni controlli comuni, l'elaborazione predefinita del messaggio di **\_ disegno WM** controlla il parametro *wParam* . Se *wParam* è diverso da null, il controllo presuppone che il valore sia un HDC e i colori che usano tale contesto di dispositivo.

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

[**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint)
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

[**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow)
</dt> <dt>

[**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow)
</dt> <dt>

[**\_ERASEBKGND WM**](../winmsg/wm-erasebkgnd.md)
</dt> <dt>

[**\_NCPAINT WM**](wm-ncpaint.md)
</dt> <dt>

[**\_stampa WM**](wm-print.md)
</dt> <dt>

[**\_PRINTCLIENT WM**](wm-printclient.md)
</dt> </dl>

 

 
