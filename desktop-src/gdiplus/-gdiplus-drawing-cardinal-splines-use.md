---
description: Una spline di cardinalità è una curva che passa in modo uniforme attraverso un set di punti specificato.
ms.assetid: 0bb84f55-18d0-4a4c-bc5b-7803aa807954
title: Disegno di spline di cardinalità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c780cb4486f579acb57170a8eda4fd187a421ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104568789"
---
# <a name="drawing-cardinal-splines"></a>Disegno di spline di cardinalità

Una spline di cardinalità è una curva che passa in modo uniforme attraverso un set di punti specificato. Per creare una spline di cardinalità, creare un oggetto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e passare l'indirizzo di una matrice di punti al metodo [**Graphics::D rawcurve**](/previous-versions//ms536070(v=vs.85)) . Nell'esempio seguente viene disegnata una spline di cardinalità a forma di campana che passa attraverso cinque punti designati:


```
Point points[] = {Point(0, 100),
                  Point(50, 80),
                  Point(100, 20),
                  Point(150, 80),
                  Point(200, 100)};

Pen pen(Color(255, 0, 0, 255));
graphics.DrawCurve(&pen, points, 5);
```



Nella figura seguente vengono illustrati la curva e cinque punti.

![illustrazione di una spline di Cardinal che passa attraverso un set di cinque punti](images/cardinalspline1.png)

È possibile usare il metodo [**Graphics::D rawclosedcurve**](/previous-versions//ms536143(v=vs.85)) della classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) per creare una spline Cardinal chiusa. In una spline di Cardinal chiusa la curva continua fino all'ultimo punto nella matrice e si connette con il primo punto nella matrice.

Nell'esempio seguente viene disegnata una spline di Cardinal chiusa che passa attraverso sei punti designati.


```
Point points[] = {Point(60, 60),
   Point(150, 80),
   Point(200, 40),
   Point(180, 120),
   Point(120, 100),
   Point(80, 160)};

Pen pen(Color(255, 0, 0, 255));
graphics.DrawClosedCurve(&pen, points, 6);
```



Nella figura seguente viene illustrata la spline chiusa insieme ai sei punti:

![illustrazione di una spline di Cardinal chiusa che passa attraverso un set di sei punti](images/cardinalspline1a.png)

È possibile modificare la curva di una spline di tipo Cardinal passando un argomento di tensionamento al metodo [**Graphics::D rawcurve**](/previous-versions//ms536070(v=vs.85)) . Nell'esempio seguente vengono disegnate tre spline cardinali che passano attraverso lo stesso set di punti:


```
Point points[] = {Point(20, 50),
                  Point(100, 10),
                  Point(200, 100),
                  Point(300, 50),
                  Point(400, 80)};

Pen pen(Color(255, 0, 0, 255));
graphics.DrawCurve(&pen, points, 5, 0.0f);  // tension 0.0
graphics.DrawCurve(&pen, points, 5, 0.6f);  // tension 0.6
graphics.DrawCurve(&pen, points, 5, 1.0f);  // tension 1.0
```



Nella figura seguente sono illustrate le tre spline insieme ai relativi valori di tensione. Si noti che quando la tensione è 0, i punti sono collegati da linee rette.

![illustrazione di tre spline cardinali che passano attraverso lo stesso set di punti ma con tensioni diverse](images/cardinalspline2.png)

 

 
