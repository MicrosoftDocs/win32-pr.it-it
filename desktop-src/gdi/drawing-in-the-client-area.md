---
description: Usare le funzioni BeginPaint ed EndPaint per preparare e completare il disegno nell'area client.
ms.assetid: ed995bfd-a791-4d73-9a0b-daf65a9f7709
title: Disegno nell'area client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5d01331ae60a7814602f6c10c0d9109ae665da39aa140223e31ac03303048b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119832021"
---
# <a name="drawing-in-the-client-area"></a>Disegno nell'area client

Usare le [**funzioni BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) ed [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) per preparare e completare il disegno nell'area client. **BeginPaint** restituisce un handle al contesto di dispositivo di visualizzazione usato per disegnare nell'area client; **EndPaint** termina la richiesta di disegno e rilascia il contesto di dispositivo.

Nell'esempio seguente la routine window scrive il messaggio "Hello, Windows!" nell'area client. Per assicurarsi che la stringa sia visibile quando la finestra viene creata per la prima volta, la funzione [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) chiama [**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow) immediatamente dopo la creazione e la visualizzazione della finestra. In questo modo [**un \_ messaggio WM PAINT**](wm-paint.md) viene inviato immediatamente alla routine della finestra.


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



 

 
