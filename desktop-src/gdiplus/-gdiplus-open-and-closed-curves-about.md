---
description: 'La figura seguente mostra due curve: una aperta e una chiusa.'
ms.assetid: e0fb8ba1-1783-4b36-93d8-f1242425d8bd
title: Curve aperte e chiuse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 383f7c68909a73291c00c6e760d1cc6554b061d5749b33e6e90ba3a986c71906
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117885126"
---
# <a name="open-and-closed-curves"></a>Curve aperte e chiuse

La figura seguente mostra due curve: una aperta e una chiusa.

![illustrazione di una curva aperta (una linea curva) e una curva chiusa (il contorno di una forma)](images/aboutgdip02-art24.png)

Le curve chiuse hanno un interno e pertanto possono essere riempite con un pennello. La classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) in Windows GDI+ fornisce i metodi seguenti per riempire figure e curve chiuse: [FillRectangle,](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(constbrush_constrect_)) [FillEllipse,](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(constbrush_constrect_)) [FillPie,](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpie(inconstbrush_inreal_inreal_inreal_inreal_inreal_inreal)) [FillPolygon,](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpolygon(inconstbrush_inconstpoint_inint)) [FillClosedCurve,](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillclosedcurve(inconstbrush_inconstpoint_inint)) [**Graphics::FillPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath)e [**Graphics::FillRegion**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillregion). Ogni volta che si chiama uno di questi metodi, è necessario passare l'indirizzo di uno dei tipi di pennello specifici ([**SolidBrush,**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) [**HatchBrush,**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush) [**TextureBrush,**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) [**LinearGradientBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush)o [**PathGradientBrush**](/windows/win32/api/gdipluspath/nl-gdipluspath-pathgradientbrush)) come argomento.

Il [metodo FillPie](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpie(inconstbrush_inreal_inreal_inreal_inreal_inreal_inreal)) è complementare al [metodo DrawArc.](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawarc(inconstpen_inint_inint_inint_inint_inreal_inreal)) Proprio come il metodo DrawArc disegna una parte del contorno di un'ellisse, il metodo FillPie riempie una parte dell'interno di un'ellisse. Nell'esempio seguente viene disegnato un arco e viene riempita la parte corrispondente dell'area interna dell'ellisse.


```
myGraphics.FillPie(&mySolidBrush, 0, 0, 140, 70, 0, 120);
myGraphics.DrawArc(&myPen, 0, 0, 140, 70, 0, 120);
```



La figura seguente mostra l'arco e la torta riempita.

![Illustrazione che mostra un segmento di un'ellisse piena](images/aboutgdip02-art25.png)

Il [metodo FillClosedCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillclosedcurve(inconstbrush_inconstpoint_inint)) è complementare al [metodo DrawClosedCurve.](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawclosedcurve(inconstpen_inconstpoint_inint)) Entrambi i metodi chiudono automaticamente la curva connettendo il punto finale al punto iniziale. Nell'esempio seguente viene disegnata una curva che passa attraverso (0, 0), (60, 20) e (40, 50). Quindi, la curva viene chiusa automaticamente connettendosi (40, 50) al punto iniziale (0, 0) e l'interno viene riempito con un colore a tinta unita.


```
Point myPointArray[] =
   {Point(10, 10), Point(60, 20),Point(40, 50)};
myGraphics.DrawClosedCurve(&myPen, myPointArray, 3);
myGraphics.FillClosedCurve(&mySolidBrush, myPointArray, 3, FillModeAlternate)
```



Un percorso può essere costituito da diverse figure (sottopercorso). Il [**metodo Graphics::FillPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) riempie l'interno di ogni figura. Se una figura non è chiusa, il **metodo Graphics::FillPath** riempie l'area che verrebbe racchiusa se la figura fosse chiusa. L'esempio seguente disegna e riempie un percorso costituito da un arco, una spline cardinale, una stringa e una torta.


```
myGraphics.FillPath(&mySolidBrush, &myGraphicsPath);
myGraphics.DrawPath(&myPen, &myGraphicsPath);
```



La figura seguente mostra il percorso prima e dopo il riempimento con un pennello a tinta unita. Si noti che il testo nella stringa è delineato, ma non riempito, dal [**metodo Graphics::D rawPath.**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) È il [**metodo Graphics::FillPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) che disegna gli interni dei caratteri nella stringa.

![figura che mostra due volte il testo e una curva aperta e chiusa; questi sono vuoti la prima volta e riempiti la seconda volta](images/aboutgdip02-art26.png)

 

 



