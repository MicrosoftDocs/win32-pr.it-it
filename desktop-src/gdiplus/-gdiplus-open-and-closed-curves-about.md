---
description: 'Nella figura seguente sono illustrate due curve: una aperta e una chiusa.'
ms.assetid: e0fb8ba1-1783-4b36-93d8-f1242425d8bd
title: Curve aperte e chiuse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7587ec950f8a0abc21f8c9cfb000a7333e87297
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104569596"
---
# <a name="open-and-closed-curves"></a>Curve aperte e chiuse

Nella figura seguente sono illustrate due curve: una aperta e una chiusa.

![illustrazione di una curva aperta (linea curva) e una curva chiusa (il contorno di una forma)](images/aboutgdip02-art24.png)

Le curve chiuse hanno una parte interna e pertanto possono essere riempite con un pennello. La [**classe grafica**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) in Windows GDI+ fornisce i metodi seguenti per compilare le curve e le cifre chiuse: [FillRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(constbrush_constrect_)), [FillEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(constbrush_constrect_)), [FillPie](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpie(inconstbrush_inreal_inreal_inreal_inreal_inreal_inreal)), [FillPolygon](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpolygon(inconstbrush_inconstpoint_inint)), [FillClosedCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillclosedcurve(inconstbrush_inconstpoint_inint)), [**Graphics:: FillPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath)e [**Graphics:: FillRegion**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillregion). Ogni volta che si chiama uno di questi metodi, è necessario passare l'indirizzo di uno dei tipi di pennello specifici ([**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush), [**HatchBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush), [**TextureBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-texturebrush), [**LinearGradientBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush)o [**PathGradientBrush**](/windows/win32/api/gdipluspath/nl-gdipluspath-pathgradientbrush)) come argomento.

Il metodo [FillPie](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpie(inconstbrush_inreal_inreal_inreal_inreal_inreal_inreal)) è un complemento al metodo [DrawArc](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawarc(inconstpen_inint_inint_inint_inint_inreal_inreal)) . Proprio come il metodo DrawArc disegna una parte del contorno di un'ellisse, il metodo FillPie riempie una parte dell'area interna di un'ellisse. Nell'esempio seguente viene disegnato un arco e viene riempita la parte corrispondente dell'interno dell'ellisse.


```
myGraphics.FillPie(&mySolidBrush, 0, 0, 140, 70, 0, 120);
myGraphics.DrawArc(&myPen, 0, 0, 140, 70, 0, 120);
```



Nella figura seguente vengono illustrati l'arco e la torta piena.

![illustrazione che mostra un segmento di un'ellisse piena](images/aboutgdip02-art25.png)

Il metodo [FillClosedCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillclosedcurve(inconstbrush_inconstpoint_inint)) è un complemento al metodo [DrawClosedCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawclosedcurve(inconstpen_inconstpoint_inint)) . Entrambi i metodi chiudono automaticamente la curva connettendo il punto finale al punto iniziale. Nell'esempio seguente viene disegnata una curva che passa attraverso (0, 0), (60, 20) e (40, 50). La curva viene quindi chiusa automaticamente connettendosi (40, 50) al punto iniziale (0, 0) e l'interno viene riempito con un colore a tinta unita.


```
Point myPointArray[] =
   {Point(10, 10), Point(60, 20),Point(40, 50)};
myGraphics.DrawClosedCurve(&myPen, myPointArray, 3);
myGraphics.FillClosedCurve(&mySolidBrush, myPointArray, 3, FillModeAlternate)
```



Un percorso può essere costituito da più figure (sottopercorsi). Il metodo [**Graphics:: FillPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) riempie l'area interna di ogni figura. Se una figura non è chiusa, il metodo **Graphics:: FillPath** riempie l'area che verrebbe racchiusa se la figura venisse chiusa. Nell'esempio seguente viene disegnato e compilato un percorso costituito da un arco, una spline di cardinalità, una stringa e una torta.


```
myGraphics.FillPath(&mySolidBrush, &myGraphicsPath);
myGraphics.DrawPath(&myPen, &myGraphicsPath);
```



Nella figura seguente viene mostrato il percorso prima e dopo che è stato riempito con un pennello a tinta unita. Si noti che il testo nella stringa è delineato, ma non riempito, dal metodo [**Graphics::D rawpath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) . Si tratta del metodo [**Graphics:: FillPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) che dipinge gli interni dei caratteri nella stringa.

![illustrazione che mostra due volte il testo e una curva aperta e chiusa; Questi sono vuoti la prima volta e riempiti la seconda volta](images/aboutgdip02-art26.png)

 

 



