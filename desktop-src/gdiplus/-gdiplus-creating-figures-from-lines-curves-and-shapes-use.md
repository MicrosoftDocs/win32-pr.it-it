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
# <a name="creating-figures-from-lines-curves-and-shapes"></a><span data-ttu-id="0612f-103">Creazione di figure da linee, curve e forme</span><span class="sxs-lookup"><span data-stu-id="0612f-103">Creating Figures from Lines, Curves, and Shapes</span></span>

<span data-ttu-id="0612f-104">Per creare un percorso, costruire un oggetto [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) , quindi chiamare i metodi, ad esempio [AddLine](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addline(inint_inint_inint_inint)) e [AddCurve](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addcurve(inconstpoint_inint)), per aggiungere primitive al percorso.</span><span class="sxs-lookup"><span data-stu-id="0612f-104">To create a path, construct a [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) object, and then call methods, such as [AddLine](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addline(inint_inint_inint_inint)) and [AddCurve](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addcurve(inconstpoint_inint)), to add primitives to the path.</span></span>

<span data-ttu-id="0612f-105">Nell'esempio seguente viene creato un percorso con un singolo arco. L'arco ha un angolo di sweep di – 180 gradi, che è in senso antiorario nel sistema di coordinate predefinito.</span><span class="sxs-lookup"><span data-stu-id="0612f-105">The following example creates a path that has a single arc. The arc has a sweep angle of –180 degrees, which is counterclockwise in the default coordinate system.</span></span>


```
Pen pen(Color(255, 255, 0, 0));
GraphicsPath path;
path.AddArc(175, 50, 50, 50, 0, -180);
graphics.DrawPath(&pen, &path);
```



<span data-ttu-id="0612f-106">Nell'esempio seguente viene creato un percorso con due figure.</span><span class="sxs-lookup"><span data-stu-id="0612f-106">The following example creates a path that has two figures.</span></span> <span data-ttu-id="0612f-107">La prima figura è un arco seguito da una riga.</span><span class="sxs-lookup"><span data-stu-id="0612f-107">The first figure is an arc followed by a line.</span></span> <span data-ttu-id="0612f-108">La seconda figura è una riga seguita da una curva, seguita da una riga.</span><span class="sxs-lookup"><span data-stu-id="0612f-108">The second figure is a line followed by a curve, followed by a line.</span></span> <span data-ttu-id="0612f-109">La prima figura viene lasciata aperta e la seconda figura viene chiusa.</span><span class="sxs-lookup"><span data-stu-id="0612f-109">The first figure is left open, and the second figure is closed.</span></span>


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



<span data-ttu-id="0612f-110">Oltre ad aggiungere linee e curve ai percorsi, è possibile aggiungere forme chiuse: rettangoli, ellissi, torte e poligoni.</span><span class="sxs-lookup"><span data-stu-id="0612f-110">In addition to adding lines and curves to paths, you can add closed shapes: rectangles, ellipses, pies, and polygons.</span></span> <span data-ttu-id="0612f-111">Nell'esempio seguente viene creato un percorso con due linee, un rettangolo e un'ellisse.</span><span class="sxs-lookup"><span data-stu-id="0612f-111">The following example creates a path that has two lines, a rectangle, and an ellipse.</span></span> <span data-ttu-id="0612f-112">Il codice usa una penna per tracciare il percorso e un pennello per riempire il percorso.</span><span class="sxs-lookup"><span data-stu-id="0612f-112">The code uses a pen to draw the path and a brush to fill the path.</span></span>


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



<span data-ttu-id="0612f-113">Il percorso nell'esempio precedente è costituito da tre cifre.</span><span class="sxs-lookup"><span data-stu-id="0612f-113">The path in the preceding example has three figures.</span></span> <span data-ttu-id="0612f-114">La prima figura è costituita dalle due righe, la seconda è costituita dal rettangolo e la terza figura è costituita dall'ellisse.</span><span class="sxs-lookup"><span data-stu-id="0612f-114">The first figure consists of the two lines, the second figure consists of the rectangle, and the third figure consists of the ellipse.</span></span> <span data-ttu-id="0612f-115">Anche se non sono presenti chiamate a [**GraphicsPath:: CloseFigure**](/windows/win32/api/Gdipluspath/nf-gdipluspath-graphicspath-closefigure) o [**GraphicsPath:: StartFigure**](/windows/win32/api/Gdipluspath/nf-gdipluspath-graphicspath-startfigure), le forme intrinsecamente chiuse, ad esempio rettangoli ed ellissi, sono considerate figure separate.</span><span class="sxs-lookup"><span data-stu-id="0612f-115">Even when there are no calls to [**GraphicsPath::CloseFigure**](/windows/win32/api/Gdipluspath/nf-gdipluspath-graphicspath-closefigure) or [**GraphicsPath::StartFigure**](/windows/win32/api/Gdipluspath/nf-gdipluspath-graphicspath-startfigure), intrinsically closed shapes, such as rectangles and ellipses, are considered separate figures.</span></span>

 

 



