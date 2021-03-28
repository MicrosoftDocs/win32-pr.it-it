---
description: È possibile creare a intervalli temporizzati creando un timer con la funzione setimer.
ms.assetid: 82f9aa5e-8e42-49cf-bcd0-785bc78fe159
title: Disegno a intervalli temporizzati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1757aca4e6be8f169aea378c52038420519ee879
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528357"
---
# <a name="drawing-at-timed-intervals"></a>Disegno a intervalli temporizzati

È possibile creare a intervalli temporizzati creando un timer con la funzione [**setimer**](/windows/win32/api/winuser/nf-winuser-settimer) . Utilizzando un timer per inviare messaggi [**del \_ timer WM**](../winmsg/wm-timer.md) alla routine della finestra a intervalli regolari, un'applicazione può eseguire un'animazione semplice nell'area client mentre altre applicazioni continuano l'esecuzione.

Nell'esempio seguente l'applicazione rimbalza una stella da un lato all'altro nell'area client. Ogni volta che la routine della finestra riceve un messaggio di [**\_ timer WM**](../winmsg/wm-timer.md) , la procedura cancella la stella in corrispondenza della posizione corrente, calcola una nuova posizione e disegna la stella all'interno della nuova posizione. La procedura avvia il timer chiamando il metodo [**Sqltimer**](/windows/win32/api/winuser/nf-winuser-settimer) durante l'elaborazione del messaggio [**WM \_ create**](../winmsg/wm-create.md) .


```C++
RECT rcCurrent = {0,0,20,20}; 
POINT aptStar[6] = {10,1, 1,19, 19,6, 1,6, 19,19, 10,1}; 
int X = 2, Y = -1, idTimer = -1; 
BOOL fVisible = FALSE; 
HDC hdc; 
 
LRESULT APIENTRY WndProc(HWND hwnd, UINT message, WPARAM wParam, LPARAM lParam) 
{ 
    PAINTSTRUCT ps; 
    RECT rc; 
 
    switch (message) 
    { 
        case WM_CREATE: 
 
            // Calculate the starting point.  
 
            GetClientRect(hwnd, &rc); 
            OffsetRect(&rcCurrent, rc.right / 2, rc.bottom / 2); 
 
            // Initialize the private DC.  
 
            hdc = GetDC(hwnd); 
            SetViewportOrgEx(hdc, rcCurrent.left, 
                rcCurrent.top, NULL); 
            SetROP2(hdc, R2_NOT); 
 
            // Start the timer.  
 
            SetTimer(hwnd, idTimer = 1, 10, NULL); 
            return 0L; 
 
        case WM_DESTROY: 
            KillTimer(hwnd, 1); 
            PostQuitMessage(0); 
            return 0L; 
 
        case WM_SIZE: 
            switch (wParam) 
            { 
                case SIZE_MINIMIZED: 
 
                    // Stop the timer if the window is minimized. 
 
                    KillTimer(hwnd, 1); 
                    idTimer = -1; 
                    break; 
 
                case SIZE_RESTORED: 
 
                    // Move the star back into the client area  
                    // if necessary.  
 
                    if (rcCurrent.right > (int) LOWORD(lParam)) 
                    {
                        rcCurrent.left = 
                            (rcCurrent.right = 
                                (int) LOWORD(lParam)) - 20; 
                    }
                    if (rcCurrent.bottom > (int) HIWORD(lParam)) 
                    {
                        rcCurrent.top = 
                            (rcCurrent.bottom = 
                                (int) HIWORD(lParam)) - 20; 
                    }
 
                    // Fall through to the next case.  
 
                case SIZE_MAXIMIZED: 
 
                    // Start the timer if it had been stopped.  
 
                    if (idTimer == -1) 
                        SetTimer(hwnd, idTimer = 1, 10, NULL); 
                    break; 
            } 
            return 0L; 
 
        case WM_TIMER: 
 
            // Hide the star if it is visible.  
 
            if (fVisible) 
                Polyline(hdc, aptStar, 6); 
 
            // Bounce the star off a side if necessary.  
 
            GetClientRect(hwnd, &rc); 
            if (rcCurrent.left + X < rc.left || 
                rcCurrent.right + X > rc.right) 
                X = -X; 
            if (rcCurrent.top + Y < rc.top || 
                rcCurrent.bottom + Y > rc.bottom) 
                Y = -Y; 
 
            // Show the star in its new position.  
 
            OffsetRect(&rcCurrent, X, Y); 
            SetViewportOrgEx(hdc, rcCurrent.left, 
                rcCurrent.top, NULL); 
            fVisible = Polyline(hdc, aptStar, 6); 
 
            return 0L; 
 
        case WM_ERASEBKGND: 
 
            // Erase the star.  
 
            fVisible = FALSE; 
            return DefWindowProc(hwnd, message, wParam, lParam); 
 
        case WM_PAINT: 
 
            // Show the star if it is not visible. Use BeginPaint  
            // to clear the update region.  
 
            BeginPaint(hwnd, &ps); 
            if (!fVisible) 
                fVisible = Polyline(hdc, aptStar, 6); 
            EndPaint(hwnd, &ps); 
            return 0L; 
    } 
    return DefWindowProc(hwnd, message, wParam, lParam); 
} 
```



Questa applicazione usa un contesto di dispositivo privato per ridurre al minimo il tempo necessario per preparare il contesto di dispositivo per il disegno. La routine della finestra Recupera e inizializza il contesto di dispositivo privato durante l'elaborazione del messaggio [**WM \_ create**](../winmsg/wm-create.md) , impostando la modalità di operazione raster binaria per consentire la cancellazione e la traccia della stella utilizzando la stessa chiamata alla funzione [**polilinea**](/windows/desktop/api/Wingdi/nf-wingdi-polyline) . La routine della finestra Imposta anche l'origine del viewport per consentire il disegno della stella utilizzando lo stesso set di punti indipendentemente dalla posizione della stella nell'area client.

L'applicazione usa il messaggio di [**\_ disegno WM**](wm-paint.md) per disegnare la stella ogni volta che è necessario aggiornare la finestra. La routine della finestra Disegna la stella solo se non è visibile. ovvero solo se è stato cancellato dal messaggio [**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md) . La routine della finestra intercetta il messaggio **WM \_ ERASEBKGND** per impostare la variabile *fVisible* , ma passa il messaggio a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) in modo che il sistema possa creare lo sfondo della finestra.

L'applicazione usa il messaggio di [**\_ dimensioni WM**](../winmsg/wm-size.md) per arrestare il timer quando la finestra è ridotta a icona e riavviare il timer quando viene ripristinata la finestra ridotta a icona. La routine della finestra usa anche il messaggio per aggiornare la posizione corrente della stella se le dimensioni della finestra sono state ridotte in modo che la stella non sia più presente nell'area client. L'applicazione tiene traccia della posizione corrente della stella usando la struttura specificata da rcCurrent, che definisce il rettangolo di delimitazione per la stella. Mantenendo tutti gli angoli del rettangolo nell'area client si mantiene la stella nell'area. La routine della finestra centra inizialmente la stella nell'area client durante l'elaborazione del messaggio [**WM \_ create**](../winmsg/wm-create.md) .

 

 
