---
description: Per creare linee con Windows GDI+ è necessario creare un oggetto Graphics e un oggetto Pen.
ms.assetid: d91562ab-41e6-4bca-a320-74f490a4f88f
title: Penne, linee e rettangoli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5e9749b1c1af6ca4808e797d016267bb251e6fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978959"
---
# <a name="pens-lines-and-rectangles"></a>Penne, linee e rettangoli

Per creare linee con Windows GDI+ è necessario creare un oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e un oggetto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) . L'oggetto **Graphics** fornisce i metodi che eseguono effettivamente il disegno e l'oggetto **Pen** archivia gli attributi della riga, ad esempio il colore, la larghezza e lo stile. Il disegno di una linea consiste semplicemente nella chiamata al metodo [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) dell'oggetto **Graphics** . L'indirizzo dell'oggetto **Pen** viene passato come uno degli argomenti al metodo DrawLine. Nell'esempio seguente viene disegnata una riga dal punto (4, 2) al punto (12, 6).


```
myGraphics.DrawLine(&myPen, 4, 2, 12, 6);
```



[DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inconstpoint__inconstpoint_)) è un metodo di overload della classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , quindi è possibile fornire gli argomenti in diversi modi. È ad esempio possibile costruire due oggetti [**punto**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) e passare i riferimenti agli oggetti **punto** come argomenti al metodo DrawLine.


```
Point myStartPoint(4, 2);
Point myEndPoint(12, 6);
myGraphics.DrawLine(&myPen, myStartPoint, myEndPoint);
```



È possibile specificare determinati attributi quando si costruisce un oggetto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) . Un costruttore [Pen](/windows/win32/api/gdipluspen/nf-gdipluspen-pen-pen(constpen_)) , ad esempio, consente di specificare il colore e la larghezza. Nell'esempio seguente viene disegnata una linea blu di larghezza 2 da (0, 0) a (60).


```
Pen myPen(Color(255, 0, 0, 255), 2);
myGraphics.DrawLine(&myPen, 0, 0, 60, 30);
```



L'oggetto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) dispone inoltre di attributi, ad esempio Dash Style, che è possibile utilizzare per specificare le funzionalità della linea. Ad esempio, nell'esempio seguente viene disegnata una linea tratteggiata da (100, 50) a (300, 80).


```
myPen.SetDashStyle(DashStyleDash);
myGraphics.DrawLine(&myPen, 100, 50, 300, 80);
```



È possibile usare diversi metodi dell'oggetto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) per impostare molti più attributi della riga. I metodi [**Pen:: SetStartCap**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setstartcap) e [**Pen:: SetEndCap**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setendcap) specificano l'aspetto delle estremità della linea; il termine può essere flat, Square, arrotondato, triangolare o una forma personalizzata. Il metodo [**Pen:: SetLineJoin**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setlinejoin) consente di specificare se le linee connesse sono sgolato (unite da angoli acuti), smussate, arrotondate o ritagliate. Nella figura seguente sono illustrate le righe con diversi stili di terminazione e di join.

![illustrazione di due righe che dimostrano le estremità arrotondate e circolari, gli angoli arrotondati e sgolato e due stili di freccia](images/aboutgdip02-art04.png)

Il disegno di rettangoli con GDI+ è simile a quello delle linee di disegno. Per creare un rettangolo, sono necessari un oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e un oggetto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) . L'oggetto **Graphics** fornisce un metodo [DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) e l'oggetto **Pen** archivia gli attributi, ad esempio la lunghezza della linea e il colore. L'indirizzo dell'oggetto **Pen** viene passato come uno degli argomenti al metodo DrawRectangle. Nell'esempio seguente viene disegnato un rettangolo con l'angolo superiore sinistro in (100, 50), una larghezza di 80 e un'altezza pari a 40.


```
myGraphics.DrawRectangle(&myPen, 100, 50, 80, 40);
```



[DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) è un metodo di overload della classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , quindi è possibile fornire gli argomenti in diversi modi. È ad esempio possibile costruire un oggetto [**Rect**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect) e passare un riferimento all'oggetto **Rect** come argomento al metodo DrawRectangle.


```
Rect myRect(100, 50, 80, 40);
myGraphics.DrawRectangle(&myPen, myRect);
```



Un oggetto [**Rect**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect) dispone di metodi per la modifica e la raccolta di informazioni sul rettangolo. I metodi [inflat](/windows/win32/api/gdiplustypes/nf-gdiplustypes-rect-inflate(inint_inint)) e [offset](/windows/win32/api/gdiplustypes/nf-gdiplustypes-rect-offset(inconstpoint_)) , ad esempio, modificano le dimensioni e la posizione del rettangolo. Il metodo [**Rect:: IntersectsWith**](/windows/win32/api/Gdiplustypes/nf-gdiplustypes-rect-intersectswith) indica se il rettangolo interseca un altro rettangolo specificato e il metodo [Contains](/windows/win32/api/gdiplustypes/nf-gdiplustypes-rect-contains(inint_inint)) indica se un punto specificato si trova all'interno del rettangolo.

 

 
