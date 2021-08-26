---
description: Puoi abilitare la correzione gamma per un pennello sfumato passando TRUE al metodo PathGradientBrush::SetGammaCorrection di tale pennello.
ms.assetid: 47472e41-f469-44f4-8b39-cf3982b79f9e
title: Applicazione della correzione gamma a una sfumatura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eae76306e5c68804d76777d9fc80c65d06904702487a8b60f80659b9d16a96ae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119888541"
---
# <a name="applying-gamma-correction-to-a-gradient"></a>Applicazione della correzione gamma a una sfumatura

Puoi abilitare la correzione gamma per un pennello sfumato passando **TRUE** al [**metodo PathGradientBrush::SetGammaCorrection**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setgammacorrection) di tale pennello. Puoi disabilitare la correzione gamma passando **FALSE** al **metodo PathGradientBrush::SetGammaCorrection.** La correzione gamma è disabilitata per impostazione predefinita.

L'esempio seguente crea un pennello sfumato lineare e lo usa per riempire due rettangoli. Il primo rettangolo viene riempito senza correzione gamma e il secondo rettangolo viene riempito con la correzione gamma.


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



La figura seguente mostra i due rettangoli riempiti. Il rettangolo superiore, senza correzione gamma, appare scuro al centro. Il rettangolo inferiore, con correzione gamma, sembra avere un'intensità più uniforme.

![illustrazione che mostra due rettangoli: il riempimento colorato del primo varia in intensità, il riempimento del secondo varia meno](images/gammagradient1.png)

L'esempio seguente crea un pennello sfumato basato su un tracciato a forma di stella. Il codice usa il pennello sfumatura tracciato con la correzione gamma disabilitata (impostazione predefinita) per riempire il tracciato. Il codice passa quindi **TRUE** al [**metodo PathGradientBrush::SetGammaCorrection**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setgammacorrection) per abilitare la correzione gamma per il pennello sfumatura del tracciato. La chiamata a [**Graphics::TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform) imposta la trasformazione globale di un oggetto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) in modo che la chiamata successiva a [**Graphics::FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) riempia una stella a destra della prima stella.


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



La figura seguente mostra l'output del codice precedente. La stella a destra ha una correzione gamma. Si noti che la stella a sinistra, che non ha una correzione gamma, ha aree che appaiono scuri.

![illustrazione di due inizi a cinque punte con riempimento sfumato colorato; il primo ha aree scura, il secondo no](images/gammagradient2.png)

 

 



