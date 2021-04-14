---
description: È possibile limitare la quantità di disegno eseguita dall'applicazione durante l'elaborazione del \_ messaggio di disegno WM determinando le dimensioni e la posizione dell'area di aggiornamento.
ms.assetid: 3407014d-6427-45e9-8be4-b8037ca5438f
title: Ridisegno nell'area di aggiornamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f4f90518db1a66b98fc7f4bd5961f2cfa581bb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993880"
---
# <a name="redrawing-in-the-update-region"></a><span data-ttu-id="6c3ff-103">Ridisegno nell'area di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="6c3ff-103">Redrawing in the Update Region</span></span>

<span data-ttu-id="6c3ff-104">È possibile limitare la quantità di disegno eseguita dall'applicazione durante l'elaborazione del [**messaggio \_ di disegno WM**](wm-paint.md) determinando le dimensioni e la posizione dell'area di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="6c3ff-104">You can limit the amount of drawing your application carries out when processing the [**WM\_PAINT**](wm-paint.md) message by determining the size and location of the update region.</span></span> <span data-ttu-id="6c3ff-105">Poiché il sistema usa l'area di aggiornamento quando si crea l'area di ridimensionamento per il contesto del dispositivo di visualizzazione della finestra, è possibile determinare indirettamente l'area di aggiornamento esaminando l'area di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="6c3ff-105">Because the system uses the update region when creating the clipping region for the window's display device context, you can indirectly determine the update region by examining the clipping region.</span></span>

<span data-ttu-id="6c3ff-106">Nell'esempio seguente, la routine della finestra Disegna un triangolo, un rettangolo, un Pentagono e un esagono, ma solo se tutte o una parte di ogni figura si trova all'interno dell'area di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="6c3ff-106">In the following example, the window procedure draws a triangle, a rectangle, a pentagon, and a hexagon, but only if all or a portion of each figure lies within the update region.</span></span> <span data-ttu-id="6c3ff-107">La procedura della finestra usa la funzione [**RectVisible**](/windows/desktop/api/Wingdi/nf-wingdi-rectvisible) e un rettangolo 100 per 100 per determinare se una figura si trova all'interno dell'area di ridimensionamento (e di conseguenza l'area di aggiornamento) per il contesto di dispositivo comune recuperato da [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint).</span><span class="sxs-lookup"><span data-stu-id="6c3ff-107">The window procedure uses the [**RectVisible**](/windows/desktop/api/Wingdi/nf-wingdi-rectvisible) function and a 100-by-100 rectangle to determine whether a figure is within the clipping region (and therefore the update region) for the common device context retrieved by [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint).</span></span>


```C++
POINT aptTriangle[4]  = {50,2, 98,86,  2,86, 50,2}, 
      aptRectangle[5] = { 2,2, 98,2,  98,98,  2,98, 2,2}, 
      aptPentagon[6]  = {50,2, 98,35, 79,90, 21,90, 2,35, 50,2}, 
      aptHexagon[7]   = {50,2, 93,25, 93,75, 50,98, 7,75, 7,25, 50,2}; 
  . 
  . 
  . 
 
        case WM_PAINT: 
            hdc = BeginPaint(hwnd, &ps); 
            SetRect(&rc, 0, 0, 100, 100); 
 
            if (RectVisible(hdc, &rc)) 
                Polyline(hdc, aptTriangle, 4); 
 
            SetViewportOrgEx(hdc, 100, 0, NULL); 
            if (RectVisible(hdc, &rc)) 
                Polyline(hdc, aptRectangle, 5); 
 
            SetViewportOrgEx(hdc, 0, 100, NULL); 
            if (RectVisible(hdc, &rc)) 
                Polyline(hdc, aptPentagon, 6); 
 
            SetViewportOrgEx(hdc, 100, 100, NULL); 
            if (RectVisible(hdc, &rc)) 
                Polyline(hdc, aptHexagon, 7); 
            EndPaint(hwnd, &ps); 
            return 0L; 
 
  . 
  . 
  . 
```



<span data-ttu-id="6c3ff-108">Le coordinate di ogni figura in questo esempio si trovano nello stesso rettangolo 100 per 100.</span><span class="sxs-lookup"><span data-stu-id="6c3ff-108">The coordinates of each figure in this example lie within the same 100-by-100 rectangle.</span></span> <span data-ttu-id="6c3ff-109">Prima di disegnare una figura, la routine della finestra Imposta l'origine del viewport su una parte diversa dell'area client usando la funzione [**SetViewportOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-setviewportorgex) .</span><span class="sxs-lookup"><span data-stu-id="6c3ff-109">Before drawing a figure, the window procedure sets the viewport origin to a different part of the client area by using the [**SetViewportOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-setviewportorgex) function.</span></span> <span data-ttu-id="6c3ff-110">In questo modo si impedisce che le cifre vengano disegnate una sopra l'altra.</span><span class="sxs-lookup"><span data-stu-id="6c3ff-110">This prevents figures from being drawn one on top of the other.</span></span> <span data-ttu-id="6c3ff-111">La modifica dell'origine del viewport non influisce sull'area di visualizzazione, ma influisce sul modo in cui vengono interpretate le coordinate del rettangolo passato a [**RectVisible**](/windows/desktop/api/Wingdi/nf-wingdi-rectvisible) .</span><span class="sxs-lookup"><span data-stu-id="6c3ff-111">Changing the viewport origin does not affect the clipping region, but does affect how the coordinates of the rectangle passed to [**RectVisible**](/windows/desktop/api/Wingdi/nf-wingdi-rectvisible) are interpreted.</span></span> <span data-ttu-id="6c3ff-112">La modifica dell'origine consente inoltre di utilizzare un solo rettangolo per controllare l'area di aggiornamento anziché singoli rettangoli per ogni figura.</span><span class="sxs-lookup"><span data-stu-id="6c3ff-112">Changing the origin also allows you to use a single rectangle to check the update region rather than individual rectangles for each figure.</span></span>

 

 



