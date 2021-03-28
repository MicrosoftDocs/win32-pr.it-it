---
description: I percorsi vengono formati combinando linee, rettangoli e curve semplici. Dal Panoramica della grafica vettoriale, i blocchi predefiniti di base seguenti si sono rivelati particolarmente utili per il disegno di immagini.
ms.assetid: 88fea2ec-7b53-44bb-841d-486c5c879c68
title: Percorsi (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 768d01d2d945c8252125a43ee2dc79f985703da1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104564670"
---
# <a name="paths-gdi"></a><span data-ttu-id="4307d-104">Percorsi (GDI+)</span><span class="sxs-lookup"><span data-stu-id="4307d-104">Paths (GDI+)</span></span>

<span data-ttu-id="4307d-105">I percorsi vengono formati combinando linee, rettangoli e curve semplici.</span><span class="sxs-lookup"><span data-stu-id="4307d-105">Paths are formed by combining lines, rectangles, and simple curves.</span></span> <span data-ttu-id="4307d-106">Dal [Panoramica della grafica vettoriale](-gdiplus-overview-of-vector-graphics-about.md) , i blocchi predefiniti di base seguenti si sono rivelati particolarmente utili per il disegno di immagini.</span><span class="sxs-lookup"><span data-stu-id="4307d-106">Recall from the [Overview of Vector Graphics](-gdiplus-overview-of-vector-graphics-about.md) that the following basic building blocks have proven to be the most useful for drawing pictures.</span></span>

-   <span data-ttu-id="4307d-107">Linee</span><span class="sxs-lookup"><span data-stu-id="4307d-107">Lines</span></span>
-   <span data-ttu-id="4307d-108">Rettangoli</span><span class="sxs-lookup"><span data-stu-id="4307d-108">Rectangles</span></span>
-   <span data-ttu-id="4307d-109">Ellissi</span><span class="sxs-lookup"><span data-stu-id="4307d-109">Ellipses</span></span>
-   <span data-ttu-id="4307d-110">Archi</span><span class="sxs-lookup"><span data-stu-id="4307d-110">Arcs</span></span>
-   <span data-ttu-id="4307d-111">Poligoni</span><span class="sxs-lookup"><span data-stu-id="4307d-111">Polygons</span></span>
-   <span data-ttu-id="4307d-112">Spline cardinali</span><span class="sxs-lookup"><span data-stu-id="4307d-112">Cardinal splines</span></span>
-   <span data-ttu-id="4307d-113">Spline di Bézier</span><span class="sxs-lookup"><span data-stu-id="4307d-113">Bézier splines</span></span>

<span data-ttu-id="4307d-114">In Windows GDI+, l'oggetto [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) consente di raccogliere una sequenza di questi blocchi predefiniti in un'unica unità.</span><span class="sxs-lookup"><span data-stu-id="4307d-114">In Windows GDI+, the [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) object allows you to collect a sequence of these building blocks into a single unit.</span></span> <span data-ttu-id="4307d-115">L'intera sequenza di linee, rettangoli, poligoni e curve può quindi essere disegnata con una chiamata al metodo [**Graphics::D rawpath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) della classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="4307d-115">The entire sequence of lines, rectangles, polygons, and curves can then be drawn with one call to the [**Graphics::DrawPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) method of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span> <span data-ttu-id="4307d-116">Nella figura seguente viene illustrato un percorso creato combinando una linea, un arco, una spline di Bézier e una spline di cardinalità.</span><span class="sxs-lookup"><span data-stu-id="4307d-116">The following illustration shows a path created by combining a line, an arc, a Bézier spline, and a cardinal spline.</span></span>

![illustrazione di un tracciato che combina una linea, un arco, una spline di Bezier e una spline Cardinal](images/aboutgdip02-art14.png)

<span data-ttu-id="4307d-118">La classe [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) fornisce i metodi seguenti per la creazione di una sequenza di elementi da disegnare: [AddLine](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addline(inint_inint_inint_inint)), [AddRectangle](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addrectangle(inconstrectf_)), [AddEllipse](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addellipse(inint_inint_inint_inint)), [AddArc](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addarc(inint_inint_inint_inint_inreal_inreal)), [AddPolygon](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addpolygon(inconstpointf_inint)), [AddCurve](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addcurve(inconstpoint_inint)) (per le spline cardinalhe) e [AddBezier](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addbezier(inint_inint_inint_inint_inint_inint_inint_inint)).</span><span class="sxs-lookup"><span data-stu-id="4307d-118">The [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) class provides the following methods for creating a sequence of items to be drawn: [AddLine](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addline(inint_inint_inint_inint)), [AddRectangle](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addrectangle(inconstrectf_)), [AddEllipse](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addellipse(inint_inint_inint_inint)), [AddArc](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addarc(inint_inint_inint_inint_inreal_inreal)), [AddPolygon](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addpolygon(inconstpointf_inint)), [AddCurve](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addcurve(inconstpoint_inint)) (for cardinal splines), and [AddBezier](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addbezier(inint_inint_inint_inint_inint_inint_inint_inint)).</span></span> <span data-ttu-id="4307d-119">Ognuno di questi metodi è sovraccarico; in altre termini, ogni metodo è presente in diverse varianti con elenchi di parametri diversi.</span><span class="sxs-lookup"><span data-stu-id="4307d-119">Each of these methods is overloaded; that is, each method comes in several variations with different parameter lists.</span></span> <span data-ttu-id="4307d-120">Ad esempio, una variante del metodo AddLine riceve quattro numeri interi e un'altra variante del metodo AddLine riceve due oggetti [**punto**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) .</span><span class="sxs-lookup"><span data-stu-id="4307d-120">For example, one variation of the AddLine method receives four integers, and another variation of the AddLine method receives two [**Point**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) objects.</span></span>

<span data-ttu-id="4307d-121">I metodi per aggiungere linee, rettangoli e spline di Bézier a un percorso hanno metodi complementari plurali che aggiungono più elementi al percorso in una singola chiamata: [AddLines](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addlines(inconstpoint_inint)), [AddRectangles](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addrectangles(inconstrectf_inint))e [AddBeziers](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addbeziers(inconstpointf_inint)).</span><span class="sxs-lookup"><span data-stu-id="4307d-121">The methods for adding lines, rectangles, and Bézier splines to a path have plural companion methods that add several items to the path in a single call: [AddLines](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addlines(inconstpoint_inint)), [AddRectangles](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addrectangles(inconstrectf_inint)), and [AddBeziers](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addbeziers(inconstpointf_inint)).</span></span> <span data-ttu-id="4307d-122">Inoltre, il metodo [AddCurve](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addcurve(inconstpoint_inint)) dispone di un metodo complementare, [AddClosedCurve](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addclosedcurve(inconstpointf_inint)), che aggiunge una curva chiusa al percorso.</span><span class="sxs-lookup"><span data-stu-id="4307d-122">Also, the [AddCurve](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addcurve(inconstpoint_inint)) method has a companion method, [AddClosedCurve](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addclosedcurve(inconstpointf_inint)), that adds a closed curve to the path.</span></span>

<span data-ttu-id="4307d-123">Per tracciare un percorso, sono necessari un oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , un oggetto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) e un oggetto [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) .</span><span class="sxs-lookup"><span data-stu-id="4307d-123">To draw a path, you need a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object, a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object, and a [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) object.</span></span> <span data-ttu-id="4307d-124">L'oggetto **Graphics** fornisce il metodo [**Graphics::D rawpath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) e l'oggetto **Pen** archivia gli attributi del percorso, ad esempio la lunghezza della linea e il colore.</span><span class="sxs-lookup"><span data-stu-id="4307d-124">The **Graphics** object provides the [**Graphics::DrawPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) method, and the **Pen** object stores attributes of the path, such as line width and color.</span></span> <span data-ttu-id="4307d-125">L'oggetto **GraphicsPath** archivia la sequenza di linee, rettangoli e curve che costituiscono il percorso.</span><span class="sxs-lookup"><span data-stu-id="4307d-125">The **GraphicsPath** object stores the sequence of lines, rectangles, and curves that make up the path.</span></span> <span data-ttu-id="4307d-126">Gli indirizzi dell'oggetto **Pen** e dell'oggetto **GraphicsPath** vengono passati come argomenti al metodo **Graphics::D rawpath** .</span><span class="sxs-lookup"><span data-stu-id="4307d-126">The addresses of the **Pen** object and the **GraphicsPath** object are passed as arguments to the **Graphics::DrawPath** method.</span></span> <span data-ttu-id="4307d-127">Nell'esempio seguente viene disegnato un percorso costituito da una linea, un'ellisse e una spline di Bézier.</span><span class="sxs-lookup"><span data-stu-id="4307d-127">The following example draws a path that consists of a line, an ellipse, and a Bézier spline.</span></span>


```
myGraphicsPath.AddLine(0, 0, 30, 20);
myGraphicsPath.AddEllipse(20, 20, 20, 40);
myGraphicsPath.AddBezier(30, 60, 70, 60, 50, 30, 100, 10);
myGraphics.DrawPath(&myPen, &myGraphicsPath);
```



<span data-ttu-id="4307d-128">Nella figura seguente viene illustrato il percorso.</span><span class="sxs-lookup"><span data-stu-id="4307d-128">The following illustration shows the path.</span></span>

![illustrazione di un tracciato costituito da una linea, un'ellisse e una spline di Bezier](images/aboutgdip02-art15.png)

<span data-ttu-id="4307d-130">Oltre ad aggiungere linee, rettangoli e curve a un tracciato, è possibile aggiungere percorsi a un percorso.</span><span class="sxs-lookup"><span data-stu-id="4307d-130">In addition to adding lines, rectangles, and curves to a path, you can add paths to a path.</span></span> <span data-ttu-id="4307d-131">In questo modo è possibile combinare i percorsi esistenti per formare percorsi complessi e di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="4307d-131">This allows you to combine existing paths to form large, complex paths.</span></span> <span data-ttu-id="4307d-132">Il codice seguente aggiunge **graphicsPath1** e **graphicsPath2** a **GraphicsPath**.</span><span class="sxs-lookup"><span data-stu-id="4307d-132">The following code adds **graphicsPath1** and **graphicsPath2** to **myGraphicsPath**.</span></span> <span data-ttu-id="4307d-133">Il secondo parametro del metodo [**GraphicsPath:: addpath**](/windows/win32/api/Gdipluspath/nf-gdipluspath-graphicspath-addpath) specifica se il percorso aggiunto è connesso al percorso esistente.</span><span class="sxs-lookup"><span data-stu-id="4307d-133">The second parameter of the [**GraphicsPath::AddPath**](/windows/win32/api/Gdipluspath/nf-gdipluspath-graphicspath-addpath) method specifies whether the added path is connected to the existing path.</span></span>


```
myGraphicsPath.AddPath(&graphicsPath1, FALSE);
myGraphicsPath.AddPath(&graphicsPath2, TRUE);
```



<span data-ttu-id="4307d-134">Esistono altri due elementi che è possibile aggiungere a un percorso: stringhe e torte.</span><span class="sxs-lookup"><span data-stu-id="4307d-134">There are two other items you can add to a path: strings and pies.</span></span> <span data-ttu-id="4307d-135">Una torta è una parte dell'area interna di un'ellisse.</span><span class="sxs-lookup"><span data-stu-id="4307d-135">A pie is a portion of the interior of an ellipse.</span></span> <span data-ttu-id="4307d-136">Nell'esempio seguente viene creato un percorso da un arco, una spline Cardinal, una stringa e una torta.</span><span class="sxs-lookup"><span data-stu-id="4307d-136">The following example creates a path from an arc, a cardinal spline, a string, and a pie.</span></span>


```
myGraphicsPath.AddArc(0, 0, 30, 20, -90, 180);
myGraphicsPath.AddCurve(myPointArray, 3);
myGraphicsPath.AddString(L"a string in a path", 18, &myFontFamily, 
   0, 24, myPointF, &myStringFormat);
myGraphicsPath.AddPie(230, 10, 40, 40, 40, 110);
myGraphics.DrawPath(&myPen, &myGraphicsPath);
```



<span data-ttu-id="4307d-137">Nella figura seguente viene illustrato il percorso.</span><span class="sxs-lookup"><span data-stu-id="4307d-137">The following illustration shows the path.</span></span> <span data-ttu-id="4307d-138">Si noti che non è necessario che un percorso sia connesso; l'arco, la spline di cardinalità, la stringa e la torta sono separate.</span><span class="sxs-lookup"><span data-stu-id="4307d-138">Note that a path does not have to be connected; the arc, cardinal spline, string, and pie are separated.</span></span>

![illustrazione di un percorso costituito da righe disconnesse: un arco, una spline cardinala, una stringa e una torta](images/aboutgdip02-art16.png)

 

 



