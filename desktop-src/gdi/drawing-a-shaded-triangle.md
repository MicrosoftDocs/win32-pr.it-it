---
description: Per creare un triangolo ombreggiato, definire una struttura a trivertici con tre elementi e una singola struttura del triangolo a SFUMAtura \_ .
ms.assetid: 78834f92-00cb-4899-851a-1de5e3c1f4fa
title: Disegno di un triangolo ombreggiato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3200a1ec061d7513cbac56c8c66104154005cef9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130791"
---
# <a name="drawing-a-shaded-triangle"></a>Disegno di un triangolo ombreggiato

Per creare un triangolo ombreggiato, definire una struttura a [**TRIvertici**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex) con tre elementi e una singola struttura del [**\_ triangolo a sfumatura**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_triangle) . Nell'esempio di codice seguente viene illustrato come creare un triangolo ombreggiato utilizzando la funzione [**GradientFill**](/windows/desktop/api/WinGdi/nf-wingdi-gradientfill) con la \_ modalità triangolo di riempimento sfumatura \_ definita.


```C++
LRESULT CALLBACK WndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    int wmId, wmEvent;
    PAINTSTRUCT ps;
    HDC hdc;

    switch (message)
    {
    case WM_COMMAND:
        wmId    = LOWORD(wParam);
        wmEvent = HIWORD(wParam);
        // Parse the menu selections:
        switch (wmId)
        {
        case IDM_ABOUT:
            DialogBox(hInst, MAKEINTRESOURCE(IDD_ABOUTBOX), hWnd, About);
            break;
        case IDM_EXIT:
            DestroyWindow(hWnd);
            break;
        default:
            return DefWindowProc(hWnd, message, wParam, lParam);
        }
        break;
    case WM_PAINT:
        {hdc = BeginPaint(hWnd, &ps);
// Create an array of TRIVERTEX structures that describe
// positional and color values for each vertex.
TRIVERTEX vertex[3];
vertex[0].x     = 150;
vertex[0].y     = 0;
vertex[0].Red   = 0xff00;
vertex[0].Green = 0x8000;
vertex[0].Blue  = 0x0000;
vertex[0].Alpha = 0x0000;

vertex[1].x     = 0;
vertex[1].y     = 150;
vertex[1].Red   = 0x9000;
vertex[1].Green = 0x0000;
vertex[1].Blue  = 0x9000;
vertex[1].Alpha = 0x0000;

vertex[2].x     = 300;
vertex[2].y     = 150; 
vertex[2].Red   = 0x9000;
vertex[2].Green = 0x0000;
vertex[2].Blue  = 0x9000;
vertex[2].Alpha = 0x0000;

// Create a GRADIENT_TRIANGLE structure that
// references the TRIVERTEX vertices.
GRADIENT_TRIANGLE gTriangle;
gTriangle.Vertex1 = 0;
gTriangle.Vertex2 = 1;
gTriangle.Vertex3 = 2;

// Draw a shaded triangle.
GradientFill(hdc, vertex, 3, &gTriangle, 1, GRADIENT_FILL_TRIANGLE);
        EndPaint(hWnd, &ps);
        break;}
    case WM_DESTROY:
        PostQuitMessage(0);
        break;
    default:
        return DefWindowProc(hWnd, message, wParam, lParam);
    }
    return 0;
}
```



Nell'immagine seguente viene illustrato l'output del disegno dell'esempio di codice precedente.

![illustrazione che mostra un triangolo che si riempie da arancione al punto superiore verso il magenta sul bordo inferiore](images/gradientfilltriangle.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Panoramica di bitmap](bitmaps.md)
</dt> <dt>

[Funzioni bitmap](bitmap-functions.md)
</dt> <dt>

[Disegno di un rettangolo ombreggiato](drawing-a-shaded-rectangle.md)
</dt> <dt>

[**EMRGRADIENTFILL**](/windows/win32/api/wingdi/ns-wingdi-emrgradientfill)
</dt> <dt>

[**triangolo SFUMAto \_**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_triangle)
</dt> <dt>

[**GradientFill**](/windows/desktop/api/WinGdi/nf-wingdi-gradientfill)
</dt> <dt>

[**Trivertice**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex)
</dt> </dl>

 

 



