---
description: Per disegnare linee con Windows GDI+ è necessario creare un oggetto Graphics e un oggetto Pen.
ms.assetid: d91562ab-41e6-4bca-a320-74f490a4f88f
title: Penne, linee e rettangoli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb8ac54d1e98a617492aa6f5f1194767fc56a34ffcaaee71ba71753dda08f8bd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119359591"
---
# <a name="pens-lines-and-rectangles"></a>Penne, linee e rettangoli

Per disegnare linee con Windows GDI+ è necessario creare un [**oggetto Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e un [**oggetto**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) Pen. **L'oggetto Graphics** fornisce i metodi che esere effettivamente il disegno e l'oggetto **Pen** archivia gli attributi della linea, ad esempio colore, larghezza e stile. Disegnare una linea è semplicemente una questione di chiamare il [metodo DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) dell'oggetto Graphics.  L'indirizzo **dell'oggetto Pen** viene passato come uno degli argomenti al metodo DrawLine. Nell'esempio seguente viene disegnata una linea dal punto (4, 2) al punto (12, 6).


```
myGraphics.DrawLine(&myPen, 4, 2, 12, 6);
```



[DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inconstpoint__inconstpoint_)) è un metodo di overload della [**classe Graphics,**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) quindi è possibile fornire argomenti in diversi modi. Ad esempio, è possibile costruire due [**oggetti Point**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) e passare riferimenti agli **oggetti Point** come argomenti al metodo DrawLine.


```
Point myStartPoint(4, 2);
Point myEndPoint(12, 6);
myGraphics.DrawLine(&myPen, myStartPoint, myEndPoint);
```



È possibile specificare determinati attributi quando si costruisce un [**oggetto**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) Pen. Ad esempio, un [costruttore Pen](/windows/win32/api/gdipluspen/nf-gdipluspen-pen-pen(constpen_)) consente di specificare colore e larghezza. Nell'esempio seguente viene disegnata una linea blu di larghezza 2 da (0, 0) a (60, 30).


```
Pen myPen(Color(255, 0, 0, 255), 2);
myGraphics.DrawLine(&myPen, 0, 0, 60, 30);
```



[**L'oggetto Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) include anche attributi, ad esempio lo stile del trattino, che è possibile usare per specificare le caratteristiche della linea. Ad esempio, nell'esempio seguente viene disegnata una linea tratteggiata da (100, 50) a (300, 80).


```
myPen.SetDashStyle(DashStyleDash);
myGraphics.DrawLine(&myPen, 100, 50, 300, 80);
```



È possibile usare vari metodi [**dell'oggetto Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) per impostare molti altri attributi della linea. I [**metodi Pen::SetStartCap**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setstartcap) e [**Pen::SetEndCap**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setendcap) specificano l'aspetto delle estremità della riga; le estremità possono essere flat, quadrate, arrotondate, triangolari o personalizzate. Il [**metodo Pen::SetLineJoin**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setlinejoin) consente di specificare se le linee connesse sono arrotondate (unite con angoli acuti), smussate, arrotondate o ritagliate. La figura seguente mostra le linee con vari stili di estremità e join.

![Illustrazione di due linee che illustrano le estremità arrotondate e circolari, gli angoli arrotondati e arrotondati e due stili freccia](images/aboutgdip02-art04.png)

Il disegno di rettangoli con GDI+ è simile al disegno di linee. Per disegnare un rettangolo, sono necessari un [**oggetto Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e un [**oggetto Pen.**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) **L'oggetto Graphics** fornisce [un metodo DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) e l'oggetto **Pen** archivia gli attributi, ad esempio lo spessore e il colore della linea. L'indirizzo **dell'oggetto Pen** viene passato come uno degli argomenti al metodo DrawRectangle. L'esempio seguente disegna un rettangolo con l'angolo superiore sinistro in corrispondenza di (100, 50), una larghezza di 80 e un'altezza di 40.


```
myGraphics.DrawRectangle(&myPen, 100, 50, 80, 40);
```



[DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) è un metodo di overload della [**classe Graphics,**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) quindi è possibile specificarlo in diversi modi con argomenti. Ad esempio, è possibile costruire un [**oggetto Rect**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect) e passare un riferimento all'oggetto **Rect** come argomento al metodo DrawRectangle.


```
Rect myRect(100, 50, 80, 40);
myGraphics.DrawRectangle(&myPen, myRect);
```



Un [**oggetto Rect**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect) dispone di metodi per la modifica e la raccolta di informazioni sul rettangolo. Ad esempio, i [metodi Inflate](/windows/win32/api/gdiplustypes/nf-gdiplustypes-rect-inflate(inint_inint)) [e Offset](/windows/win32/api/gdiplustypes/nf-gdiplustypes-rect-offset(inconstpoint_)) modificano le dimensioni e la posizione del rettangolo. Il [**metodo Rect::IntersectsWith**](/windows/win32/api/Gdiplustypes/nf-gdiplustypes-rect-intersectswith) indica se il rettangolo interseca un altro rettangolo specificato e il metodo [Contains](/windows/win32/api/gdiplustypes/nf-gdiplustypes-rect-contains(inint_inint)) indica se un determinato punto si trova all'interno del rettangolo.

 

 
