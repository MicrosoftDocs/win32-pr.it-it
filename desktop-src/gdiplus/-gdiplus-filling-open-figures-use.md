---
description: "È possibile riempire un percorso passando l'indirizzo di un oggetto GraphicsPath al metodo Graphics:: FillPath."
ms.assetid: 4cf293cf-5155-4ce2-afeb-cc9ca9395764
title: Riempimento di figure aperte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53f4a4608b787d8b0af8b9e9c7100a43c0c76dc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104551869"
---
# <a name="filling-open-figures"></a>Riempimento di figure aperte

È possibile riempire un percorso passando l'indirizzo di un oggetto [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) al metodo [**Graphics:: FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) . Il metodo **Graphics:: FillPath** riempie il percorso in base alla modalità di riempimento (alternativa o di avvolgimento) attualmente impostata per il percorso. Se il percorso contiene figure aperte, il percorso viene riempito come se tali figure fossero chiuse. GDI+ chiude una figura disegnando una linea retta dal punto finale al punto iniziale.

Nell'esempio seguente viene creato un percorso con una figura aperta (un arco) e una figura chiusa (un'ellisse). Il metodo [**Graphics:: FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) riempie il percorso in base alla modalità di riempimento predefinita, ovvero FillModeAlternate.


```
GraphicsPath path;

// Add an open figure.
path.AddArc(0, 0, 150, 120, 30, 120);

// Add an intrinsically closed figure.
path.AddEllipse(50, 50, 50, 100);

Pen pen(Color(128, 0, 0, 255), 5);
SolidBrush brush(Color(255, 255, 0, 0));

// The fill mode is FillModeAlternate by default.
graphics.FillPath(&brush, &path);
graphics.DrawPath(&pen, &path);
```



Nella figura seguente viene illustrato l'output del codice precedente. Si noti che il percorso è riempito (in base a FillModeAlternate) come se la figura aperta fosse chiusa da una linea retta dal punto finale al punto di partenza.

![illustrazione che mostra un'ellisse alta che si sovrappone alla metà inferiore di un'ellisse ampia. l'Unione è compilata, ma l'intersezione è vuota](images/fillopenpath.png)

 

 



