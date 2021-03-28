---
description: Usare le funzioni BeginPaint e EndPaint per preparare e completare il disegno nell'area client.
ms.assetid: ed995bfd-a791-4d73-9a0b-daf65a9f7709
title: Disegno nell'area client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1e14c8492a11a7ad9764416b2453cea3264fbf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880297"
---
# <a name="drawing-in-the-client-area"></a><span data-ttu-id="4d936-103">Disegno nell'area client</span><span class="sxs-lookup"><span data-stu-id="4d936-103">Drawing in the Client Area</span></span>

<span data-ttu-id="4d936-104">Usare le funzioni [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) e [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) per preparare e completare il disegno nell'area client.</span><span class="sxs-lookup"><span data-stu-id="4d936-104">You use the [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) and [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) functions to prepare for and complete the drawing in the client area.</span></span> <span data-ttu-id="4d936-105">**BeginPaint** restituisce un handle al contesto del dispositivo di visualizzazione usato per il disegno nell'area client; **EndPaint** termina la richiesta di disegno e rilascia il contesto di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4d936-105">**BeginPaint** returns a handle to the display device context used for drawing in the client area; **EndPaint** ends the paint request and releases the device context.</span></span>

<span data-ttu-id="4d936-106">Nell'esempio seguente, la routine della finestra scrive il messaggio "Hello, Windows!"</span><span class="sxs-lookup"><span data-stu-id="4d936-106">In the following example, the window procedure writes the message "Hello, Windows!"</span></span> <span data-ttu-id="4d936-107">nell'area client.</span><span class="sxs-lookup"><span data-stu-id="4d936-107">in the client area.</span></span> <span data-ttu-id="4d936-108">Per assicurarsi che la stringa sia visibile quando la finestra viene creata per la prima volta, la funzione [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) chiama [**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow) immediatamente dopo la creazione e la visualizzazione della finestra.</span><span class="sxs-lookup"><span data-stu-id="4d936-108">To make sure the string is visible when the window is first created, the [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) function calls [**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow) immediately after creating and showing the window.</span></span> <span data-ttu-id="4d936-109">In questo modo viene inviato immediatamente un messaggio di [**\_ disegno WM**](wm-paint.md) alla routine della finestra.</span><span class="sxs-lookup"><span data-stu-id="4d936-109">This causes a [**WM\_PAINT**](wm-paint.md) message to be sent immediately to the window procedure.</span></span>


```C++
LRESULT APIENTRY WndProc(HWND hwnd, UINT message, WPARAM wParam, LPARAM lParam) 
{ 
    PAINTSTRUCT ps; 
    HDC hdc; 
 
    switch (message) 
    { 
        case WM_PAINT: 
            hdc = BeginPaint(hwnd, &ps); 
            TextOut(hdc, 0, 0, "Hello, Windows!", 15); 
            EndPaint(hwnd, &ps); 
            return 0L; 

        // Process other messages.   
    } 
} 
 
int APIENTRY WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, LPSTR lpCmdLine, int nCmdShow) 
{ 
    HWND hwnd; 
 
    hwnd = CreateWindowEx( 
        // parameters  
        ); 
 
    ShowWindow(hwnd, SW_SHOW); 
    UpdateWindow(hwnd); 
 
    return msg.wParam; 
} 
```



 

 
