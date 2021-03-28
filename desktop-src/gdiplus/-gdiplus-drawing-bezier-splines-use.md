---
description: 'A B&\# 233; la spline Zier è definita da quattro punti: un punto iniziale, due punti di controllo e un punto finale.'
ms.assetid: af19e82b-0d13-4fb0-981e-8d5dd1bbfb36
title: Disegno di spline di Bezier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ea97d25f482372c387239e8f9083b31e3b2d912
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755714"
---
# <a name="drawing-bezier-splines"></a>Disegno di spline di Bezier

Una spline di Bézier è definita da quattro punti: un punto iniziale, due punti di controllo e un punto finale. Nell'esempio seguente viene disegnata una spline Bézier con punto iniziale (10, 100) e punto finale (200, 100). I punti di controllo sono (100, 10) e (150, 150):


```
Point p1(10, 100);   // start point
Point c1(100, 10);   // first control point
Point c2(150, 150);  // second control point
Point p2(200, 100);  // end point
Pen pen(Color(255, 0, 0, 255));
graphics.DrawBezier(&pen, p1, c1, c2, p2);
```



La figura seguente mostra la spline di Bézier risultante insieme al punto iniziale, ai punti di controllo e al punto finale. L'illustrazione mostra anche la struttura convessa della spline, ovvero un poligono formato dalla connessione dei quattro punti con linee rette.

![illustrazione che mostra una spline di Bezier con due punti finali e due punti di controllo](images/bezierspline1.png)

È possibile usare il metodo [DrawBeziers](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawbeziers(inconstpen_inconstpoint_inint)) della classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) per creare una sequenza di spline di Bézier connesse. Nell'esempio seguente viene disegnata una curva costituita da due spline di Bézier connesse. Il punto finale della prima spline di Bézier è il punto iniziale della seconda spline di Bézier.


```
Point p[] = {
   Point(10, 100),   // start point of first spline
   Point(75, 10),    // first control point of first spline
   Point(80, 50),    // second control point of first spline
   Point(100, 150),  // end point of first spline and 
                     // start point of second spline
   Point(125, 80),   // first control point of second spline
   Point(175, 200),  // second control point of second spline
   Point(200, 80)};  // end point of second spline
Pen pen(Color(255, 0, 0, 255));
graphics.DrawBeziers(&pen, p, 7);
```



Nella figura seguente sono illustrate le spline connesse insieme ai sette punti.

![illustrazione che Mostra gli endpoint e i punti di controllo di due spline che condividono uno dei punti finali](images/bezierspline2.png)

 

 



