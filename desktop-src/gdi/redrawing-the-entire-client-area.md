---
description: È possibile fare in modo che l'applicazione ridisegni l'intero contenuto dell'area client ogni volta che le dimensioni della finestra cambiano impostando gli stili CS \_ HREDRAW e CS \_ VREDRAW per la classe della finestra.
ms.assetid: ed68b85e-8382-4450-b07d-0422b44dc2e3
title: Ridisegno dell'intera area client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e3c438fe36160f27b1015daf7874e237035f927825199b93b3a508668f40bd5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118759147"
---
# <a name="redrawing-the-entire-client-area"></a>Ridisegno dell'intera area client

È possibile fare in modo che l'applicazione ridisegni l'intero contenuto dell'area client ogni volta che le dimensioni della finestra cambiano impostando gli stili CS \_ HREDRAW e CS \_ VREDRAW per la classe della finestra. Le applicazioni che regolano le dimensioni del disegno in base alle dimensioni della finestra usano questi stili per assicurarsi che inizino con un'area client completamente vuota durante il disegno.

Nell'esempio seguente la routine della finestra disegna una stella a cinque punte che si adatta perfettamente all'area client. Usa un contesto di dispositivo comune e deve impostare la modalità di mapping, nonché gli extent della finestra e del viewport ogni volta che viene elaborato il messaggio [**WM \_ PAINT.**](wm-paint.md)


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



 

 



