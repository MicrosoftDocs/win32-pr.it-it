---
description: I percorsi vengono formati combinando linee, rettangoli e curve semplici. Dal Panoramica della grafica vettoriale, i blocchi predefiniti di base seguenti si sono rivelati particolarmente utili per il disegno di immagini.
ms.assetid: 88fea2ec-7b53-44bb-841d-486c5c879c68
title: Percorsi (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 768d01d2d945c8252125a43ee2dc79f985703da1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104564670"
---
# <a name="paths-gdi"></a>Percorsi (GDI+)

I percorsi vengono formati combinando linee, rettangoli e curve semplici. Dal [Panoramica della grafica vettoriale](-gdiplus-overview-of-vector-graphics-about.md) , i blocchi predefiniti di base seguenti si sono rivelati particolarmente utili per il disegno di immagini.

-   Linee
-   Rettangoli
-   Ellissi
-   Archi
-   Poligoni
-   Spline cardinali
-   Spline di Bézier

In Windows GDI+, l'oggetto [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) consente di raccogliere una sequenza di questi blocchi predefiniti in un'unica unità. L'intera sequenza di linee, rettangoli, poligoni e curve può quindi essere disegnata con una chiamata al metodo [**Graphics::D rawpath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) della classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . Nella figura seguente viene illustrato un percorso creato combinando una linea, un arco, una spline di Bézier e una spline di cardinalità.

![illustrazione di un tracciato che combina una linea, un arco, una spline di Bezier e una spline Cardinal](images/aboutgdip02-art14.png)

La classe [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) fornisce i metodi seguenti per la creazione di una sequenza di elementi da disegnare: [AddLine](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addline(inint_inint_inint_inint)), [AddRectangle](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addrectangle(inconstrectf_)), [AddEllipse](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addellipse(inint_inint_inint_inint)), [AddArc](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addarc(inint_inint_inint_inint_inreal_inreal)), [AddPolygon](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addpolygon(inconstpointf_inint)), [AddCurve](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addcurve(inconstpoint_inint)) (per le spline cardinalhe) e [AddBezier](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addbezier(inint_inint_inint_inint_inint_inint_inint_inint)). Ognuno di questi metodi è sovraccarico; in altre termini, ogni metodo è presente in diverse varianti con elenchi di parametri diversi. Ad esempio, una variante del metodo AddLine riceve quattro numeri interi e un'altra variante del metodo AddLine riceve due oggetti [**punto**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) .

I metodi per aggiungere linee, rettangoli e spline di Bézier a un percorso hanno metodi complementari plurali che aggiungono più elementi al percorso in una singola chiamata: [AddLines](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addlines(inconstpoint_inint)), [AddRectangles](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addrectangles(inconstrectf_inint))e [AddBeziers](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addbeziers(inconstpointf_inint)). Inoltre, il metodo [AddCurve](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addcurve(inconstpoint_inint)) dispone di un metodo complementare, [AddClosedCurve](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addclosedcurve(inconstpointf_inint)), che aggiunge una curva chiusa al percorso.

Per tracciare un percorso, sono necessari un oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , un oggetto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) e un oggetto [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) . L'oggetto **Graphics** fornisce il metodo [**Graphics::D rawpath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) e l'oggetto **Pen** archivia gli attributi del percorso, ad esempio la lunghezza della linea e il colore. L'oggetto **GraphicsPath** archivia la sequenza di linee, rettangoli e curve che costituiscono il percorso. Gli indirizzi dell'oggetto **Pen** e dell'oggetto **GraphicsPath** vengono passati come argomenti al metodo **Graphics::D rawpath** . Nell'esempio seguente viene disegnato un percorso costituito da una linea, un'ellisse e una spline di Bézier.


```
myGraphicsPath.AddLine(0, 0, 30, 20);
myGraphicsPath.AddEllipse(20, 20, 20, 40);
myGraphicsPath.AddBezier(30, 60, 70, 60, 50, 30, 100, 10);
myGraphics.DrawPath(&myPen, &myGraphicsPath);
```



Nella figura seguente viene illustrato il percorso.

![illustrazione di un tracciato costituito da una linea, un'ellisse e una spline di Bezier](images/aboutgdip02-art15.png)

Oltre ad aggiungere linee, rettangoli e curve a un tracciato, è possibile aggiungere percorsi a un percorso. In questo modo è possibile combinare i percorsi esistenti per formare percorsi complessi e di grandi dimensioni. Il codice seguente aggiunge **graphicsPath1** e **graphicsPath2** a **GraphicsPath**. Il secondo parametro del metodo [**GraphicsPath:: addpath**](/windows/win32/api/Gdipluspath/nf-gdipluspath-graphicspath-addpath) specifica se il percorso aggiunto è connesso al percorso esistente.


```
myGraphicsPath.AddPath(&graphicsPath1, FALSE);
myGraphicsPath.AddPath(&graphicsPath2, TRUE);
```



Esistono altri due elementi che è possibile aggiungere a un percorso: stringhe e torte. Una torta è una parte dell'area interna di un'ellisse. Nell'esempio seguente viene creato un percorso da un arco, una spline Cardinal, una stringa e una torta.


```
myGraphicsPath.AddArc(0, 0, 30, 20, -90, 180);
myGraphicsPath.AddCurve(myPointArray, 3);
myGraphicsPath.AddString(L"a string in a path", 18, &myFontFamily, 
   0, 24, myPointF, &myStringFormat);
myGraphicsPath.AddPie(230, 10, 40, 40, 40, 110);
myGraphics.DrawPath(&myPen, &myGraphicsPath);
```



Nella figura seguente viene illustrato il percorso. Si noti che non è necessario che un percorso sia connesso; l'arco, la spline di cardinalità, la stringa e la torta sono separate.

![illustrazione di un percorso costituito da righe disconnesse: un arco, una spline cardinala, una stringa e una torta](images/aboutgdip02-art16.png)

 

 



