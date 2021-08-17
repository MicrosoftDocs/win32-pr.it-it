---
description: È possibile usare le funzioni di linea per disegnare marcatori.
ms.assetid: 69114875-f3e0-45e9-8e87-1f4e9de08db1
title: Marcatori di disegno
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b5e05c651bf95aa48a8ef11fd0819523ee5da7652e27ecebaeff8ee9de4f1e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117887119"
---
# <a name="drawing-markers"></a>Marcatori di disegno

È possibile usare le funzioni di linea per disegnare marcatori. Un marcatore è un simbolo centrato su un punto. Le applicazioni di disegno usano marcatori per designare i punti di partenza, i punti finali e i punti di controllo. Le applicazioni foglio di calcolo usano i marcatori per designare i punti di interesse in un grafico.

Nell'esempio di codice seguente la funzione Marker definita dall'applicazione crea un marcatore usando le [**funzioni MoveToEx**](/windows/desktop/api/Wingdi/nf-wingdi-movetoex) [**e LineTo.**](/windows/desktop/api/Wingdi/nf-wingdi-lineto) Queste funzioni disegnano due linee intersecate, di 20 pixel, centrate sulle coordinate del cursore.


```C++
void Marker(LONG x, LONG y, HWND hwnd) 
{ 
    HDC hdc; 
 
    hdc = GetDC(hwnd); 
        MoveToEx(hdc, (int) x - 10, (int) y, (LPPOINT) NULL); 
        LineTo(hdc, (int) x + 10, (int) y); 
        MoveToEx(hdc, (int) x, (int) y - 10, (LPPOINT) NULL); 
        LineTo(hdc, (int) x, (int) y + 10); 

    ReleaseDC(hwnd, hdc); 
} 
```



Il sistema archivia le coordinate del cursore nel parametro *lParam* del messaggio [**WM \_ LBUTTONDOWN**](../inputdev/wm-lbuttondown.md) quando l'utente preme il pulsante sinistro del mouse. Il codice seguente illustra come un'applicazione ottiene queste coordinate, determina se si trovano all'interno della relativa area client e le passa alla funzione Marker per disegnare il marcatore.


```C++
// Line- and arc-drawing variables  
 
static BOOL bCollectPoints; 
static POINT ptMouseDown[32]; 
static int index; 
POINTS ptTmp; 
RECT rc; 
 
    case WM_LBUTTONDOWN: 
 
 
        if (bCollectPoints && index < 32)
        { 
            // Create the region from the client area.  
 
            GetClientRect(hwnd, &rc); 
            hrgn = CreateRectRgn(rc.left, rc.top, 
                rc.right, rc.bottom); 
 
            ptTmp = MAKEPOINTS((POINTS FAR *) lParam); 
            ptMouseDown[index].x = (LONG) ptTmp.x; 
            ptMouseDown[index].y = (LONG) ptTmp.y; 
 
            // Test for a hit in the client rectangle.  
 
            if (PtInRegion(hrgn, ptMouseDown[index].x, 
                    ptMouseDown[index].y)) 
            { 
                // If a hit occurs, record the mouse coords.  
 
                Marker(ptMouseDown[index].x, ptMouseDown[index].y, 
                    hwnd); 
                index++; 
            } 
        } 
        break; 
```



 

 
