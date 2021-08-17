---
description: È possibile riempire un percorso passando l'indirizzo di un oggetto GraphicsPath al metodo Graphics::FillPath.
ms.assetid: 4cf293cf-5155-4ce2-afeb-cc9ca9395764
title: Riempimento di figure aperte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 198a1a9e3a3cffa6aa5c0f3627c1415a54c8842c9f90a2ebdd6ebc2a9e0f3fb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118977541"
---
# <a name="filling-open-figures"></a>Riempimento di figure aperte

È possibile riempire un percorso passando l'indirizzo di un [**oggetto GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) al [**metodo Graphics::FillPath.**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) Il **metodo Graphics::FillPath** riempie il percorso in base alla modalità di riempimento (alternativa o avvolgimento) attualmente impostata per il percorso. Se il percorso ha figure aperte, il percorso viene riempito come se tali figure fossero chiuse. GDI+ una figura disegnando una linea retta dal punto finale al punto iniziale.

Nell'esempio seguente viene creato un percorso con una figura aperta (un arco) e una figura chiusa (un ellisse). Il [**metodo Graphics::FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) riempie il percorso in base alla modalità di riempimento predefinita, ovvero FillModeAlternate.


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



Nella figura seguente viene illustrato l'output del codice precedente. Si noti che il percorso viene riempito (in base a FillModeAlternate) come se la figura aperta fosse chiusa da una linea retta dal punto finale al punto iniziale.

![figura che mostra un'ellisse alta che si sovrappone alla metà inferiore di un'ellisse larga; l'unione viene riempita, ma l'intersezione è vuota](images/fillopenpath.png)

 

 



