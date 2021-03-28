---
description: Una delle proprietà della classe Graphics è l'area di ridimensionamento. Il disegno eseguito da un determinato oggetto Graphics è limitato all'area di visualizzazione dell'oggetto Graphics. È possibile impostare l'area di ridimensionamento chiamando il metodo seclip.
ms.assetid: 816a5845-ca03-46c6-bdda-e6a7d02ff614
title: Ritaglio con un'area
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa19426d62d5d3af99150bf9ac8e8099628fe2f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104550637"
---
# <a name="clipping-with-a-region"></a>Ritaglio con un'area

Una delle proprietà della classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) è l'area di ridimensionamento. Il disegno eseguito da un determinato oggetto **Graphics** è limitato all'area di visualizzazione dell'oggetto **Graphics** . È possibile impostare l'area di ridimensionamento chiamando il metodo **seclip** .

Nell'esempio seguente viene costruito un percorso costituito da un singolo poligono. Il codice costruisce quindi un'area in base a tale percorso. L'indirizzo dell'area viene passato **al metodo di** troncamento di un oggetto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , quindi vengono disegnate due stringhe.


```
// Create a path that consists of a single polygon.
Point polyPoints[] = {Point(10, 10), Point(150, 10), 
   Point(100, 75), Point(100, 150)};
GraphicsPath path;
path.AddPolygon(polyPoints, 4);
// Construct a region based on the path.
Region region(&path);
// Draw the outline of the region.
Pen pen(Color(255, 0, 0, 0));
graphics.DrawPath(&pen, &path);
// Set the clipping region of the Graphics object.
graphics.SetClip(&region);
// Draw some clipped strings.
FontFamily fontFamily(L"Arial");
Font font(&fontFamily, 36, FontStyleBold, UnitPixel);
SolidBrush solidBrush(Color(255, 255, 0, 0));
graphics.DrawString(L"A Clipping Region", 20, &font, 
   PointF(15, 25), &solidBrush);
graphics.DrawString(L"A Clipping Region", 20, &font, 
   PointF(15, 68), &solidBrush);
```



Nella figura seguente sono illustrate le stringhe ritagliate.

![illustrazione che mostra parti di due frasi visualizzate all'interno di una forma a quattro lati](images/clip1.png)

 

 



