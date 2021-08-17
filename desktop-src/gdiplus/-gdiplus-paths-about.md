---
description: I percorsi vengono formati combinando linee, rettangoli e curve semplici. Si ricordi dalla panoramica della grafica vettoriale che i blocchi predefiniti di base seguenti si sono rivelati i più utili per disegnare immagini.
ms.assetid: 88fea2ec-7b53-44bb-841d-486c5c879c68
title: Percorsi (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f54dae290138314cac3dae8d259591939490764d371e9a2caf9423801e985ec2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117695477"
---
# <a name="paths-gdi"></a>Percorsi (GDI+)

I percorsi vengono formati combinando linee, rettangoli e curve semplici. Si ricordi dalla [panoramica della grafica vettoriale che](-gdiplus-overview-of-vector-graphics-about.md) i blocchi predefiniti di base seguenti si sono rivelati i più utili per disegnare immagini.

-   Linee
-   Rettangoli
-   Ellissi
-   Archi
-   Poligoni
-   Spline di tipo cardinal
-   Spline di Bézier

In Windows GDI+, [**l'oggetto GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) consente di raccogliere una sequenza di questi blocchi predefiniti in una singola unità. L'intera sequenza di linee, rettangoli, poligoni e curve può quindi essere disegnata con una chiamata al metodo [**Graphics::D rawPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) della [**classe Graphics.**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) La figura seguente mostra un tracciato creato combinando una linea, un arco, una spline di Bézier e una spline di cardinalità.

![illustrazione di un tracciato che combina una linea, un arco, una spline di Bézier e una spline cardinale](images/aboutgdip02-art14.png)

La classe [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) fornisce i metodi seguenti per la creazione di una sequenza di elementi da disegnare: [AddLine](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addline(inint_inint_inint_inint)), [AddRectangle](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addrectangle(inconstrectf_)), [AddEllipse](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addellipse(inint_inint_inint_inint)), [AddArc](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addarc(inint_inint_inint_inint_inreal_inreal)), [AddPolygon](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addpolygon(inconstpointf_inint)), [AddCurve](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addcurve(inconstpoint_inint)) (per spline cardinali) e [AddBezier](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addbezier(inint_inint_inint_inint_inint_inint_inint_inint)). Ognuno di questi metodi è sottoposto a overload. in altre parole, ogni metodo presenta diverse varianti con elenchi di parametri diversi. Ad esempio, una variante del metodo AddLine riceve quattro numeri interi e un'altra variante del metodo AddLine riceve due [**oggetti Point.**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point)

I metodi per l'aggiunta di linee, rettangoli e spline di Bézier a un tracciato hanno metodi complementari plurali che aggiungono diversi elementi al percorso in una singola chiamata: [AddLines,](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addlines(inconstpoint_inint)) [AddRectangles](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addrectangles(inconstrectf_inint))e [AddBeziers.](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addbeziers(inconstpointf_inint)) Il metodo [AddCurve ha](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addcurve(inconstpoint_inint)) anche un metodo complementare, [AddClosedCurve,](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addclosedcurve(inconstpointf_inint))che aggiunge una curva chiusa al percorso.

Per disegnare un tracciato, sono necessari [**un oggetto Graphics,**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) un [**oggetto Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) e un [**oggetto GraphicsPath.**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) **L'oggetto Graphics** fornisce il [**metodo Graphics::D rawPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) e l'oggetto **Pen** archivia gli attributi del tracciato, ad esempio lo spessore e il colore della linea. **L'oggetto GraphicsPath** archivia la sequenza di linee, rettangoli e curve che costituiscono il tracciato. Gli indirizzi **dell'oggetto Pen** e **dell'oggetto GraphicsPath** vengono passati come argomenti al **metodo Graphics::D rawPath.** L'esempio seguente disegna un tracciato costituito da una linea, un'ellisse e una spline di Bézier.


```
myGraphicsPath.AddLine(0, 0, 30, 20);
myGraphicsPath.AddEllipse(20, 20, 20, 40);
myGraphicsPath.AddBezier(30, 60, 70, 60, 50, 30, 100, 10);
myGraphics.DrawPath(&myPen, &myGraphicsPath);
```



La figura seguente mostra il percorso.

![illustrazione di un tracciato costituito da una linea, un'ellisse e una spline di Bézier](images/aboutgdip02-art15.png)

Oltre ad aggiungere linee, rettangoli e curve a un tracciato, è possibile aggiungere tracciati a un tracciato. In questo modo è possibile combinare i percorsi esistenti per formare percorsi complessi di grandi dimensioni. Il codice seguente aggiunge **graphicsPath1** **e graphicsPath2** a **myGraphicsPath.** Il secondo parametro del [**metodo GraphicsPath::AddPath**](/windows/win32/api/Gdipluspath/nf-gdipluspath-graphicspath-addpath) specifica se il percorso aggiunto è connesso al percorso esistente.


```
myGraphicsPath.AddPath(&graphicsPath1, FALSE);
myGraphicsPath.AddPath(&graphicsPath2, TRUE);
```



A un percorso è possibile aggiungere altri due elementi: stringhe e torta. Una torta è una parte interna di un'ellisse. Nell'esempio seguente viene creato un percorso da un arco, una spline cardinale, una stringa e una torta.


```
myGraphicsPath.AddArc(0, 0, 30, 20, -90, 180);
myGraphicsPath.AddCurve(myPointArray, 3);
myGraphicsPath.AddString(L"a string in a path", 18, &myFontFamily, 
   0, 24, myPointF, &myStringFormat);
myGraphicsPath.AddPie(230, 10, 40, 40, 40, 110);
myGraphics.DrawPath(&myPen, &myGraphicsPath);
```



La figura seguente mostra il percorso. Si noti che non è necessario che un percorso sia connesso. l'arco, la spline cardinale, la stringa e la torta sono separati.

![illustrazione di un percorso costituito da linee disconnesse: arco, spline cardinale, stringa e torta](images/aboutgdip02-art16.png)

 

 



