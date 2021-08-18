---
description: Una spline cardinale è una curva che passa senza problemi attraverso un determinato set di punti.
ms.assetid: 0bb84f55-18d0-4a4c-bc5b-7803aa807954
title: Disegno di spline cardinali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f9124e27254fc77135d265d9bab98d2332c02d345e60add1fcd96fc68c814df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036819"
---
# <a name="drawing-cardinal-splines"></a>Disegno di spline cardinali

Una spline cardinale è una curva che passa senza problemi attraverso un determinato set di punti. Per disegnare una spline cardinale, creare un [**oggetto Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e passare l'indirizzo di una matrice di punti al [**metodo Graphics::D rawCurve.**](/previous-versions//ms536070(v=vs.85)) L'esempio seguente disegna una spline cardinale a forma di campana che passa attraverso cinque punti designati:


```
Point points[] = {Point(0, 100),
                  Point(50, 80),
                  Point(100, 20),
                  Point(150, 80),
                  Point(200, 100)};

Pen pen(Color(255, 0, 0, 255));
graphics.DrawCurve(&pen, points, 5);
```



La figura seguente mostra la curva e i cinque punti.

![illustrazione di una spline cardinale che passa attraverso un set di cinque punti](images/cardinalspline1.png)

È possibile usare il [**metodo Graphics::D rawClosedCurve**](/previous-versions//ms536143(v=vs.85)) della classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) per disegnare una spline cardinale chiusa. In una spline cardinale chiusa, la curva continua fino all'ultimo punto della matrice e si connette al primo punto della matrice.

Nell'esempio seguente viene disegnata una spline cardinale chiusa che passa attraverso sei punti designati.


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



La figura seguente mostra la spline chiusa insieme ai sei punti:

![illustrazione di una spline cardinale chiusa che passa attraverso un set di sei punti](images/cardinalspline1a.png)

È possibile modificare il modo in cui una spline cardinale curva passando un argomento di tensione al [**metodo Graphics::D rawCurve.**](/previous-versions//ms536070(v=vs.85)) Nell'esempio seguente vengono disegnate tre spline cardinali che passano attraverso lo stesso set di punti:


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



La figura seguente mostra le tre spline insieme ai relativi valori di tensione. Si noti che quando la tensione è 0, i punti sono connessi da linee rette.

![illustrazione di tre spline cardinali che passano attraverso lo stesso set di punti, ma a diverse tensione](images/cardinalspline2.png)

 

 
