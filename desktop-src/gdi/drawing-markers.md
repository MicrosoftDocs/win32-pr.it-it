---
description: È possibile utilizzare le funzioni linea per creare marcatori.
ms.assetid: 69114875-f3e0-45e9-8e87-1f4e9de08db1
title: Disegno di marcatori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 497b725e3a266e296950394a9bb9b2b76a17cb25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754431"
---
# <a name="drawing-markers"></a>Disegno di marcatori

È possibile utilizzare le funzioni linea per creare marcatori. Un marcatore è un simbolo centrato su un punto. Il disegno di applicazioni usa marcatori per designare punti di partenza, punti finali e punti di controllo. Nelle applicazioni di fogli di calcolo vengono utilizzati marcatori per designare punti di interesse su un grafico o un grafico.

Nell'esempio di codice seguente la funzione marcatore definita dall'applicazione crea un marcatore usando le funzioni [**MoveToEx**](/windows/desktop/api/Wingdi/nf-wingdi-movetoex) e [**LineTo**](/windows/desktop/api/Wingdi/nf-wingdi-lineto) . Queste funzioni traggono due linee di intersezione, 20 pixel di lunghezza, centrate sulle coordinate del cursore.


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



Il sistema archivia le coordinate del cursore nel parametro *lParam* del messaggio [**WM \_ LBUTTONDOWN**](../inputdev/wm-lbuttondown.md) quando l'utente preme il pulsante sinistro del mouse. Il codice seguente illustra il modo in cui un'applicazione ottiene queste coordinate, determina se si trovano all'interno dell'area client e le passa alla funzione marcatore per creare il marcatore.


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



 

 
