---
description: L'applicazione può ridisegnare l'intero contenuto dell'area client ogni volta che le dimensioni della finestra cambiano impostando gli \_ stili CS HREDRAW e cs \_ VREDRAW per la classe Window.
ms.assetid: ed68b85e-8382-4450-b07d-0422b44dc2e3
title: Ridisegno dell'intera area client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d67640d1b464173755029bef1d0feb91f215cda6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993877"
---
# <a name="redrawing-the-entire-client-area"></a><span data-ttu-id="40031-103">Ridisegno dell'intera area client</span><span class="sxs-lookup"><span data-stu-id="40031-103">Redrawing the Entire Client Area</span></span>

<span data-ttu-id="40031-104">L'applicazione può ridisegnare l'intero contenuto dell'area client ogni volta che le dimensioni della finestra cambiano impostando gli \_ stili CS HREDRAW e cs \_ VREDRAW per la classe Window.</span><span class="sxs-lookup"><span data-stu-id="40031-104">You can have your application redraw the entire contents of the client area whenever the window changes size by setting the CS\_HREDRAW and CS\_VREDRAW styles for the window class.</span></span> <span data-ttu-id="40031-105">Le applicazioni che modificano le dimensioni del disegno in base alle dimensioni della finestra utilizzano questi stili per assicurarsi che inizino con un'area client completamente vuota durante il disegno.</span><span class="sxs-lookup"><span data-stu-id="40031-105">Applications that adjust the size of the drawing based on the size of the window use these styles to ensure that they start with a completely empty client area when drawing.</span></span>

<span data-ttu-id="40031-106">Nell'esempio seguente, la routine della finestra Disegna una stella a cinque punte che si integra perfettamente nell'area client.</span><span class="sxs-lookup"><span data-stu-id="40031-106">In the following example, the window procedure draws a five-pointed star that fits neatly in the client area.</span></span> <span data-ttu-id="40031-107">Usa un contesto di dispositivo comune e deve impostare la modalità di mapping, nonché gli extent di finestra e Viewport ogni volta che viene elaborato il messaggio di [**\_ disegno WM**](wm-paint.md) .</span><span class="sxs-lookup"><span data-stu-id="40031-107">It uses a common device context and must set the mapping mode as well as window and viewport extents each time the [**WM\_PAINT**](wm-paint.md) message is processed.</span></span>


```C++
LRESULT APIENTRY WndProc(HWMD hwnd, UINT message, WPARAM wParam, LPARAM lParam) 
{ 
    PAINTSTRUCT ps; 
    HDC hdc; 
    RECT rc; 
    POINT aptStar[6] = {50,2, 2,98, 98,33, 2,33, 98,98, 50,2}; 
 
    . 
    . 
    . 
 
        case WM_PAINT: 
            hdc = BeginPaint(hwnd, &ps); 
            GetClientRect(hwnd, &rc); 
            SetMapMode(hdc, MM_ANISOTROPIC); 
            SetWindowExtEx(hdc, 100, 100, NULL); 
            SetViewportExtEx(hdc, rc.right, rc.bottom, NULL); 
            Polyline(hdc, aptStar, 6); 
            EndPaint(hwnd, &ps); 
            return 0L; 
 
        . 
        . 
        . 
} 
 
 
int APIENTRY WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, LPSTR lpCmdLine, int nCmdShow) 
{ 
    WNDCLASS wc; 
 
    . 
    . 
    . 
 
        wc.style = CS_HREDRAW | CS_VREDRAW; 
        wc.lpfnWndProc = (WNDPROC) WndProc; 
 
    . 
    . 
    . 
 
        RegisterClass(&wc); 
 
    . 
    . 
    . 
 
    return msg.wParam; 
} 
```



 

 



