---
description: Un poligono è una figura chiusa con tre o più lati dritti.
ms.assetid: f1155341-83f3-4805-8d42-a1910515db31
title: Poligoni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe67ec2d062579df0510c100a80d06715be4199e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751319"
---
# <a name="polygons"></a><span data-ttu-id="df876-103">Poligoni</span><span class="sxs-lookup"><span data-stu-id="df876-103">Polygons</span></span>

<span data-ttu-id="df876-104">Un poligono è una figura chiusa con tre o più lati dritti.</span><span class="sxs-lookup"><span data-stu-id="df876-104">A polygon is a closed figure with three or more straight sides.</span></span> <span data-ttu-id="df876-105">Ad esempio, un triangolo è un poligono con tre lati, un rettangolo è un poligono con quattro lati e un pentagono è un poligono con cinque lati.</span><span class="sxs-lookup"><span data-stu-id="df876-105">For example, a triangle is a polygon with three sides, a rectangle is a polygon with four sides, and a pentagon is a polygon with five sides.</span></span> <span data-ttu-id="df876-106">Nella figura seguente vengono illustrati diversi poligoni.</span><span class="sxs-lookup"><span data-stu-id="df876-106">The following illustration shows several polygons.</span></span>

![illustrazione che mostra cinque poligoni di forme, dimensioni e colori diversi](images/aboutgdip02-art07.png)

<span data-ttu-id="df876-108">Per creare un poligono, sono necessari un oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , un oggetto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) e una matrice di oggetti [**Point**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) (o [**PointF**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-pointf)).</span><span class="sxs-lookup"><span data-stu-id="df876-108">To draw a polygon, you need a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object, a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object, and an array of [**Point**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) (or [**PointF**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-pointf)) objects.</span></span> <span data-ttu-id="df876-109">L'oggetto **Graphics** fornisce il metodo [DrawPolygon](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpolygon(inconstpen_inconstpoint_inint)) .</span><span class="sxs-lookup"><span data-stu-id="df876-109">The **Graphics** object provides the [DrawPolygon](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpolygon(inconstpen_inconstpoint_inint)) method.</span></span> <span data-ttu-id="df876-110">L'oggetto **Pen** archivia gli attributi del poligono, ad esempio la lunghezza della linea e il colore, e la matrice di oggetti **punto** archivia i punti da connettere tramite linee rette.</span><span class="sxs-lookup"><span data-stu-id="df876-110">The **Pen** object stores attributes of the polygon, such as line width and color, and the array of **Point** objects stores the points to be connected by straight lines.</span></span> <span data-ttu-id="df876-111">Gli indirizzi dell'oggetto **Pen** e la matrice di oggetti **Point** vengono passati come argomenti al Metodo DrawPolygon.</span><span class="sxs-lookup"><span data-stu-id="df876-111">The addresses of the **Pen** object and the array of **Point** objects are passed as arguments to the DrawPolygon method.</span></span> <span data-ttu-id="df876-112">Nell'esempio seguente viene disegnato un poligono a tre facce.</span><span class="sxs-lookup"><span data-stu-id="df876-112">The following example draws a three-sided polygon.</span></span> <span data-ttu-id="df876-113">Si noti che sono presenti solo tre punti in **myPointArray**: (0, 0), (50, 30) e (30, 60).</span><span class="sxs-lookup"><span data-stu-id="df876-113">Note that there are only three points in **myPointArray**: (0, 0), (50, 30), and (30, 60).</span></span> <span data-ttu-id="df876-114">Il metodo DrawPolygon chiude automaticamente il poligono disegnando una riga da (30, 60) al punto iniziale (0,0);</span><span class="sxs-lookup"><span data-stu-id="df876-114">The DrawPolygon method automatically closes the polygon by drawing a line from (30, 60) back to the starting point (0, 0);</span></span>


```
Point myPointArray[] =
   {Point(0, 0), Point(50, 30), Point(30, 60)};
myGraphics.DrawPolygon(&myPen, myPointArray, 3);
```



<span data-ttu-id="df876-115">Nella figura seguente viene illustrato il poligono.</span><span class="sxs-lookup"><span data-stu-id="df876-115">The following illustration shows the polygon.</span></span>

![illustrazione che mostra un triangolo rispetto agli assi delle coordinate](images/aboutgdip02-art08.png)

 

 



