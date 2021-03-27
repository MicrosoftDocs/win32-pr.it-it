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
# <a name="polygons"></a>Poligoni

Un poligono è una figura chiusa con tre o più lati dritti. Ad esempio, un triangolo è un poligono con tre lati, un rettangolo è un poligono con quattro lati e un pentagono è un poligono con cinque lati. Nella figura seguente vengono illustrati diversi poligoni.

![illustrazione che mostra cinque poligoni di forme, dimensioni e colori diversi](images/aboutgdip02-art07.png)

Per creare un poligono, sono necessari un oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , un oggetto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) e una matrice di oggetti [**Point**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) (o [**PointF**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-pointf)). L'oggetto **Graphics** fornisce il metodo [DrawPolygon](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpolygon(inconstpen_inconstpoint_inint)) . L'oggetto **Pen** archivia gli attributi del poligono, ad esempio la lunghezza della linea e il colore, e la matrice di oggetti **punto** archivia i punti da connettere tramite linee rette. Gli indirizzi dell'oggetto **Pen** e la matrice di oggetti **Point** vengono passati come argomenti al Metodo DrawPolygon. Nell'esempio seguente viene disegnato un poligono a tre facce. Si noti che sono presenti solo tre punti in **myPointArray**: (0, 0), (50, 30) e (30, 60). Il metodo DrawPolygon chiude automaticamente il poligono disegnando una riga da (30, 60) al punto iniziale (0,0);


```
Point myPointArray[] =
   {Point(0, 0), Point(50, 30), Point(30, 60)};
myGraphics.DrawPolygon(&myPen, myPointArray, 3);
```



Nella figura seguente viene illustrato il poligono.

![illustrazione che mostra un triangolo rispetto agli assi delle coordinate](images/aboutgdip02-art08.png)

 

 



