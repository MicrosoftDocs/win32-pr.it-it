---
description: 'È possibile abilitare la correzione gamma per un pennello sfumatura passando TRUE al Metodo PathGradientBrush:: SetGammaCorrection del pennello.'
ms.assetid: 47472e41-f469-44f4-8b39-cf3982b79f9e
title: Applicazione della correzione gamma a una sfumatura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80e51673e8be4fd289286ce5e4e3e8f7c5469724
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131387"
---
# <a name="applying-gamma-correction-to-a-gradient"></a>Applicazione della correzione gamma a una sfumatura

È possibile abilitare la correzione gamma per un pennello sfumatura passando **true** al metodo [**PathGradientBrush:: SetGammaCorrection**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setgammacorrection) del pennello. È possibile disabilitare la correzione gamma passando **false** al metodo **PathGradientBrush:: SetGammaCorrection** . Per impostazione predefinita, la correzione gamma è disabilitata.

Nell'esempio seguente viene creato un pennello sfumato lineare e tale pennello viene utilizzato per riempire due rettangoli. Il primo rettangolo viene riempito senza correzione gamma e il secondo rettangolo viene riempito con la correzione gamma.


```
LinearGradientBrush linGrBrush(
   Point(0, 10),
   Point(200, 10),
   Color(255, 255, 0, 0),   // Opaque red
   Color(255, 0, 0, 255));  // Opaque blue

graphics.FillRectangle(&linGrBrush, 0, 0, 200, 50);
linGrBrush.SetGammaCorrection(TRUE);
graphics.FillRectangle(&linGrBrush, 0, 60, 200, 50); 
```



Nella figura seguente sono illustrati i due rettangoli riempiti. Il rettangolo superiore, che non ha la correzione gamma, appare scuro al centro. Il rettangolo inferiore, con correzione gamma, sembra avere un'intensità più uniforme.

![illustrazione che mostra due rettangoli: il riempimento colorato del primo varia in intensità, il riempimento del secondo varia in meno](images/gammagradient1.png)

Nell'esempio seguente viene creato un pennello sfumatura del percorso basato su un percorso a forma di stella. Il codice usa il pennello sfumatura del percorso con la correzione gamma disabilitata (impostazione predefinita) per riempire il percorso. Quindi il codice passa **true** al metodo [**PathGradientBrush:: SetGammaCorrection**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setgammacorrection) per abilitare la correzione gamma per il pennello sfumatura del percorso. La chiamata a [**Graphics:: TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform) imposta la trasformazione globale di un oggetto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) in modo che la chiamata successiva a [**Graphics:: FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) riempia una stella che si trova a destra della prima stella.


```
// Put the points of a polygon in an array.
Point points[] = {Point(75, 0), Point(100, 50), 
                  Point(150, 50), Point(112, 75),
                  Point(150, 150), Point(75, 100), 
                  Point(0, 150), Point(37, 75), 
                  Point(0, 50), Point(50, 50)};

// Use the array of points to construct a path.
GraphicsPath path;
path.AddLines(points, 10);

// Use the path to construct a path gradient brush.
PathGradientBrush pthGrBrush(&path);

// Set the color at the center of the path to red.
pthGrBrush.SetCenterColor(Color(255, 255, 0, 0));

// Set the colors of the points in the array.
Color colors[] = {Color(255, 0, 0, 0),   Color(255, 0, 255, 0),
                  Color(255, 0, 0, 255), Color(255, 255, 255, 255), 
                  Color(255, 0, 0, 0),   Color(255, 0, 255, 0), 
                  Color(255, 0, 0, 255), Color(255, 255, 255, 255),
                  Color(255, 0, 0, 0),   Color(255, 0, 255, 0)};

int count = 10;
pthGrBrush.SetSurroundColors(colors, &count);

// Fill the path with the path gradient brush.
graphics.FillPath(&pthGrBrush, &path);
pthGrBrush.SetGammaCorrection(TRUE);
graphics.TranslateTransform(200.0f, 0.0f);
graphics.FillPath(&pthGrBrush, &path);
```



Nella figura seguente viene illustrato l'output del codice precedente. La stella a destra ha la correzione gamma. Si noti che la stella a sinistra, che non ha la correzione gamma, presenta aree che appaiono scure.

![illustrazione di 2 5-puntato inizia con riempimento sfumato colorato; il primo ha aree scure, il secondo non](images/gammagradient2.png)

 

 



