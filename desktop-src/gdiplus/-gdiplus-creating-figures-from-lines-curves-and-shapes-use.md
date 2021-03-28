---
description: Per creare un percorso, costruire un oggetto GraphicsPath, quindi chiamare i metodi, ad esempio AddLine e AddCurve, per aggiungere primitive al percorso.
ms.assetid: 66faeb73-16fb-4b7f-a4d5-a90ec2590d8c
title: Creazione di figure da linee, curve e forme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c473dfececcaa86347dc02efdfd62131eb9a63d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967207"
---
# <a name="creating-figures-from-lines-curves-and-shapes"></a>Creazione di figure da linee, curve e forme

Per creare un percorso, costruire un oggetto [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) , quindi chiamare i metodi, ad esempio [AddLine](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addline(inint_inint_inint_inint)) e [AddCurve](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addcurve(inconstpoint_inint)), per aggiungere primitive al percorso.

Nell'esempio seguente viene creato un percorso con un singolo arco. L'arco ha un angolo di sweep di – 180 gradi, che è in senso antiorario nel sistema di coordinate predefinito.


```
Pen pen(Color(255, 255, 0, 0));
GraphicsPath path;
path.AddArc(175, 50, 50, 50, 0, -180);
graphics.DrawPath(&pen, &path);
```



Nell'esempio seguente viene creato un percorso con due figure. La prima figura è un arco seguito da una riga. La seconda figura è una riga seguita da una curva, seguita da una riga. La prima figura viene lasciata aperta e la seconda figura viene chiusa.


```
Point points[] = {Point(40, 60), Point(50, 70), Point(30, 90)};

Pen pen(Color(255, 255, 0, 0), 2);
GraphicsPath path;

// The first figure is started automatically, so there is
// no need to call StartFigure here.
path.AddArc(175, 50, 50, 50, 0.0f, -180.0f);
path.AddLine(100, 0, 250, 20);

path.StartFigure();
path.AddLine(50, 20, 5, 90);
path.AddCurve(points, 3);
path.AddLine(50, 150, 150, 180);
path.CloseFigure();

graphics.DrawPath(&pen, &path);
```



Oltre ad aggiungere linee e curve ai percorsi, è possibile aggiungere forme chiuse: rettangoli, ellissi, torte e poligoni. Nell'esempio seguente viene creato un percorso con due linee, un rettangolo e un'ellisse. Il codice usa una penna per tracciare il percorso e un pennello per riempire il percorso.


```
GraphicsPath path;
Pen          pen(Color(255, 255, 0, 0), 2);
SolidBrush   brush(Color(255, 0, 0, 200));

path.AddLine(10, 10, 100, 40);
path.AddLine(100, 60, 30, 60);
path.AddRectangle(Rect(50, 35, 20, 40));
path.AddEllipse(10, 75, 40, 30);

graphics.DrawPath(&pen, &path);
graphics.FillPath(&brush, &path);
```



Il percorso nell'esempio precedente è costituito da tre cifre. La prima figura è costituita dalle due righe, la seconda è costituita dal rettangolo e la terza figura è costituita dall'ellisse. Anche se non sono presenti chiamate a [**GraphicsPath:: CloseFigure**](/windows/win32/api/Gdipluspath/nf-gdipluspath-graphicspath-closefigure) o [**GraphicsPath:: StartFigure**](/windows/win32/api/Gdipluspath/nf-gdipluspath-graphicspath-startfigure), le forme intrinsecamente chiuse, ad esempio rettangoli ed ellissi, sono considerate figure separate.

 

 



