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
# <a name="drawing-markers"></a><span data-ttu-id="d471a-103">Disegno di marcatori</span><span class="sxs-lookup"><span data-stu-id="d471a-103">Drawing Markers</span></span>

<span data-ttu-id="d471a-104">È possibile utilizzare le funzioni linea per creare marcatori.</span><span class="sxs-lookup"><span data-stu-id="d471a-104">You can use the line functions to draw markers.</span></span> <span data-ttu-id="d471a-105">Un marcatore è un simbolo centrato su un punto.</span><span class="sxs-lookup"><span data-stu-id="d471a-105">A marker is a symbol centered over a point.</span></span> <span data-ttu-id="d471a-106">Il disegno di applicazioni usa marcatori per designare punti di partenza, punti finali e punti di controllo.</span><span class="sxs-lookup"><span data-stu-id="d471a-106">Drawing applications use markers to designate starting points, ending points, and control points.</span></span> <span data-ttu-id="d471a-107">Nelle applicazioni di fogli di calcolo vengono utilizzati marcatori per designare punti di interesse su un grafico o un grafico.</span><span class="sxs-lookup"><span data-stu-id="d471a-107">Spreadsheet applications use markers to designate points of interest on a chart or graph.</span></span>

<span data-ttu-id="d471a-108">Nell'esempio di codice seguente la funzione marcatore definita dall'applicazione crea un marcatore usando le funzioni [**MoveToEx**](/windows/desktop/api/Wingdi/nf-wingdi-movetoex) e [**LineTo**](/windows/desktop/api/Wingdi/nf-wingdi-lineto) .</span><span class="sxs-lookup"><span data-stu-id="d471a-108">In the following code sample, the application-defined Marker function creates a marker by using the [**MoveToEx**](/windows/desktop/api/Wingdi/nf-wingdi-movetoex) and [**LineTo**](/windows/desktop/api/Wingdi/nf-wingdi-lineto) functions.</span></span> <span data-ttu-id="d471a-109">Queste funzioni traggono due linee di intersezione, 20 pixel di lunghezza, centrate sulle coordinate del cursore.</span><span class="sxs-lookup"><span data-stu-id="d471a-109">These functions draw two intersecting lines, 20 pixels in length, centered over the cursor coordinates.</span></span>


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



<span data-ttu-id="d471a-110">Il sistema archivia le coordinate del cursore nel parametro *lParam* del messaggio [**WM \_ LBUTTONDOWN**](../inputdev/wm-lbuttondown.md) quando l'utente preme il pulsante sinistro del mouse.</span><span class="sxs-lookup"><span data-stu-id="d471a-110">The system stores the coordinates of the cursor in the *lParam* parameter of the [**WM\_LBUTTONDOWN**](../inputdev/wm-lbuttondown.md) message when the user presses the left mouse button.</span></span> <span data-ttu-id="d471a-111">Il codice seguente illustra il modo in cui un'applicazione ottiene queste coordinate, determina se si trovano all'interno dell'area client e le passa alla funzione marcatore per creare il marcatore.</span><span class="sxs-lookup"><span data-stu-id="d471a-111">The following code demonstrates how an application gets these coordinates, determines whether they lie within its client area, and passes them to the Marker function to draw the marker.</span></span>


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



 

 
