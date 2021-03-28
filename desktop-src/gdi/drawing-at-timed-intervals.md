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
# <a name="drawing-at-timed-intervals"></a><span data-ttu-id="c9343-103">Disegno a intervalli temporizzati</span><span class="sxs-lookup"><span data-stu-id="c9343-103">Drawing at Timed Intervals</span></span>

<span data-ttu-id="c9343-104">È possibile creare a intervalli temporizzati creando un timer con la funzione [**setimer**](/windows/win32/api/winuser/nf-winuser-settimer) .</span><span class="sxs-lookup"><span data-stu-id="c9343-104">You can draw at timed intervals by creating a timer with the [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer) function.</span></span> <span data-ttu-id="c9343-105">Utilizzando un timer per inviare messaggi [**del \_ timer WM**](../winmsg/wm-timer.md) alla routine della finestra a intervalli regolari, un'applicazione può eseguire un'animazione semplice nell'area client mentre altre applicazioni continuano l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="c9343-105">By using a timer to send [**WM\_TIMER**](../winmsg/wm-timer.md) messages to the window procedure at regular intervals, an application can carry out simple animation in the client area while other applications continue running.</span></span>

<span data-ttu-id="c9343-106">Nell'esempio seguente l'applicazione rimbalza una stella da un lato all'altro nell'area client.</span><span class="sxs-lookup"><span data-stu-id="c9343-106">In the following example, the application bounces a star from side to side in the client area.</span></span> <span data-ttu-id="c9343-107">Ogni volta che la routine della finestra riceve un messaggio di [**\_ timer WM**](../winmsg/wm-timer.md) , la procedura cancella la stella in corrispondenza della posizione corrente, calcola una nuova posizione e disegna la stella all'interno della nuova posizione.</span><span class="sxs-lookup"><span data-stu-id="c9343-107">Each time the window procedure receives a [**WM\_TIMER**](../winmsg/wm-timer.md) message, the procedure erases the star at the current position, calculates a new position, and draws the star within the new position.</span></span> <span data-ttu-id="c9343-108">La procedura avvia il timer chiamando il metodo [**Sqltimer**](/windows/win32/api/winuser/nf-winuser-settimer) durante l'elaborazione del messaggio [**WM \_ create**](../winmsg/wm-create.md) .</span><span class="sxs-lookup"><span data-stu-id="c9343-108">The procedure starts the timer by calling [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer) while processing the [**WM\_CREATE**](../winmsg/wm-create.md) message.</span></span>


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



<span data-ttu-id="c9343-109">Questa applicazione usa un contesto di dispositivo privato per ridurre al minimo il tempo necessario per preparare il contesto di dispositivo per il disegno.</span><span class="sxs-lookup"><span data-stu-id="c9343-109">This application uses a private device context to minimize the time required to prepare the device context for drawing.</span></span> <span data-ttu-id="c9343-110">La routine della finestra Recupera e inizializza il contesto di dispositivo privato durante l'elaborazione del messaggio [**WM \_ create**](../winmsg/wm-create.md) , impostando la modalità di operazione raster binaria per consentire la cancellazione e la traccia della stella utilizzando la stessa chiamata alla funzione [**polilinea**](/windows/desktop/api/Wingdi/nf-wingdi-polyline) .</span><span class="sxs-lookup"><span data-stu-id="c9343-110">The window procedure retrieves and initializes the private device context when processing the [**WM\_CREATE**](../winmsg/wm-create.md) message, setting the binary raster operation mode to allow the star to be erased and drawn using the same call to the [**Polyline**](/windows/desktop/api/Wingdi/nf-wingdi-polyline) function.</span></span> <span data-ttu-id="c9343-111">La routine della finestra Imposta anche l'origine del viewport per consentire il disegno della stella utilizzando lo stesso set di punti indipendentemente dalla posizione della stella nell'area client.</span><span class="sxs-lookup"><span data-stu-id="c9343-111">The window procedure also sets the viewport origin to allow the star to be drawn using the same set of points regardless of the star's position in the client area.</span></span>

<span data-ttu-id="c9343-112">L'applicazione usa il messaggio di [**\_ disegno WM**](wm-paint.md) per disegnare la stella ogni volta che è necessario aggiornare la finestra.</span><span class="sxs-lookup"><span data-stu-id="c9343-112">The application uses the [**WM\_PAINT**](wm-paint.md) message to draw the star whenever the window must be updated.</span></span> <span data-ttu-id="c9343-113">La routine della finestra Disegna la stella solo se non è visibile. ovvero solo se è stato cancellato dal messaggio [**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md) .</span><span class="sxs-lookup"><span data-stu-id="c9343-113">The window procedure draws the star only if it is not visible; that is, only if it has been erased by the [**WM\_ERASEBKGND**](../winmsg/wm-erasebkgnd.md) message.</span></span> <span data-ttu-id="c9343-114">La routine della finestra intercetta il messaggio **WM \_ ERASEBKGND** per impostare la variabile *fVisible* , ma passa il messaggio a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) in modo che il sistema possa creare lo sfondo della finestra.</span><span class="sxs-lookup"><span data-stu-id="c9343-114">The window procedure intercepts the **WM\_ERASEBKGND** message to set the *fVisible* variable, but passes the message to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) so that the system can draw the window background.</span></span>

<span data-ttu-id="c9343-115">L'applicazione usa il messaggio di [**\_ dimensioni WM**](../winmsg/wm-size.md) per arrestare il timer quando la finestra è ridotta a icona e riavviare il timer quando viene ripristinata la finestra ridotta a icona.</span><span class="sxs-lookup"><span data-stu-id="c9343-115">The application uses the [**WM\_SIZE**](../winmsg/wm-size.md) message to stop the timer when the window is minimized and to restart the timer when the minimized window is restored.</span></span> <span data-ttu-id="c9343-116">La routine della finestra usa anche il messaggio per aggiornare la posizione corrente della stella se le dimensioni della finestra sono state ridotte in modo che la stella non sia più presente nell'area client.</span><span class="sxs-lookup"><span data-stu-id="c9343-116">The window procedure also uses the message to update the current position of the star if the size of the window has been reduced so that the star is no longer in the client area.</span></span> <span data-ttu-id="c9343-117">L'applicazione tiene traccia della posizione corrente della stella usando la struttura specificata da rcCurrent, che definisce il rettangolo di delimitazione per la stella.</span><span class="sxs-lookup"><span data-stu-id="c9343-117">The application keeps track of the star's current position by using the structure specified by rcCurrent, which defines the bounding rectangle for the star.</span></span> <span data-ttu-id="c9343-118">Mantenendo tutti gli angoli del rettangolo nell'area client si mantiene la stella nell'area.</span><span class="sxs-lookup"><span data-stu-id="c9343-118">Keeping all corners of the rectangle in the client area keeps the star in the area.</span></span> <span data-ttu-id="c9343-119">La routine della finestra centra inizialmente la stella nell'area client durante l'elaborazione del messaggio [**WM \_ create**](../winmsg/wm-create.md) .</span><span class="sxs-lookup"><span data-stu-id="c9343-119">The window procedure initially centers the star in the client area when processing the [**WM\_CREATE**](../winmsg/wm-create.md) message.</span></span>

 

 
