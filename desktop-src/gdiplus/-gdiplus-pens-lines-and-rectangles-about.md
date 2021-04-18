---
description: Per creare linee con Windows GDI+ è necessario creare un oggetto Graphics e un oggetto Pen.
ms.assetid: d91562ab-41e6-4bca-a320-74f490a4f88f
title: Penne, linee e rettangoli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5e9749b1c1af6ca4808e797d016267bb251e6fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978959"
---
# <a name="pens-lines-and-rectangles"></a><span data-ttu-id="214cb-103">Penne, linee e rettangoli</span><span class="sxs-lookup"><span data-stu-id="214cb-103">Pens, Lines, and Rectangles</span></span>

<span data-ttu-id="214cb-104">Per creare linee con Windows GDI+ è necessario creare un oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e un oggetto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) .</span><span class="sxs-lookup"><span data-stu-id="214cb-104">To draw lines with Windows GDI+ you need to create a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object.</span></span> <span data-ttu-id="214cb-105">L'oggetto **Graphics** fornisce i metodi che eseguono effettivamente il disegno e l'oggetto **Pen** archivia gli attributi della riga, ad esempio il colore, la larghezza e lo stile.</span><span class="sxs-lookup"><span data-stu-id="214cb-105">The **Graphics** object provides the methods that actually do the drawing, and the **Pen** object stores attributes of the line, such as color, width, and style.</span></span> <span data-ttu-id="214cb-106">Il disegno di una linea consiste semplicemente nella chiamata al metodo [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) dell'oggetto **Graphics** .</span><span class="sxs-lookup"><span data-stu-id="214cb-106">Drawing a line is simply a matter of calling the [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) method of the **Graphics** object.</span></span> <span data-ttu-id="214cb-107">L'indirizzo dell'oggetto **Pen** viene passato come uno degli argomenti al metodo DrawLine.</span><span class="sxs-lookup"><span data-stu-id="214cb-107">The address of the **Pen** object is passed as one of the arguments to the DrawLine method.</span></span> <span data-ttu-id="214cb-108">Nell'esempio seguente viene disegnata una riga dal punto (4, 2) al punto (12, 6).</span><span class="sxs-lookup"><span data-stu-id="214cb-108">The following example draws a line from the point (4, 2) to the point (12, 6).</span></span>


```
myGraphics.DrawLine(&myPen, 4, 2, 12, 6);
```



<span data-ttu-id="214cb-109">[DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inconstpoint__inconstpoint_)) è un metodo di overload della classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , quindi è possibile fornire gli argomenti in diversi modi.</span><span class="sxs-lookup"><span data-stu-id="214cb-109">[DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inconstpoint__inconstpoint_)) is an overloaded method of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class, so there are several ways you can supply it with arguments.</span></span> <span data-ttu-id="214cb-110">È ad esempio possibile costruire due oggetti [**punto**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) e passare i riferimenti agli oggetti **punto** come argomenti al metodo DrawLine.</span><span class="sxs-lookup"><span data-stu-id="214cb-110">For example, you can construct two [**Point**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) objects and pass references to the **Point** objects as arguments to the DrawLine method.</span></span>


```
Point myStartPoint(4, 2);
Point myEndPoint(12, 6);
myGraphics.DrawLine(&myPen, myStartPoint, myEndPoint);
```



<span data-ttu-id="214cb-111">È possibile specificare determinati attributi quando si costruisce un oggetto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) .</span><span class="sxs-lookup"><span data-stu-id="214cb-111">You can specify certain attributes when you construct a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object.</span></span> <span data-ttu-id="214cb-112">Un costruttore [Pen](/windows/win32/api/gdipluspen/nf-gdipluspen-pen-pen(constpen_)) , ad esempio, consente di specificare il colore e la larghezza.</span><span class="sxs-lookup"><span data-stu-id="214cb-112">For example, one [Pen](/windows/win32/api/gdipluspen/nf-gdipluspen-pen-pen(constpen_)) constructor allows you to specify color and width.</span></span> <span data-ttu-id="214cb-113">Nell'esempio seguente viene disegnata una linea blu di larghezza 2 da (0, 0) a (60).</span><span class="sxs-lookup"><span data-stu-id="214cb-113">The following example draws a blue line of width 2 from (0, 0) to (60, 30).</span></span>


```
Pen myPen(Color(255, 0, 0, 255), 2);
myGraphics.DrawLine(&myPen, 0, 0, 60, 30);
```



<span data-ttu-id="214cb-114">L'oggetto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) dispone inoltre di attributi, ad esempio Dash Style, che è possibile utilizzare per specificare le funzionalità della linea.</span><span class="sxs-lookup"><span data-stu-id="214cb-114">The [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object also has attributes, such as dash style, that you can use to specify features of the line.</span></span> <span data-ttu-id="214cb-115">Ad esempio, nell'esempio seguente viene disegnata una linea tratteggiata da (100, 50) a (300, 80).</span><span class="sxs-lookup"><span data-stu-id="214cb-115">For example, the following example draws a dashed line from (100, 50) to (300, 80).</span></span>


```
myPen.SetDashStyle(DashStyleDash);
myGraphics.DrawLine(&myPen, 100, 50, 300, 80);
```



<span data-ttu-id="214cb-116">È possibile usare diversi metodi dell'oggetto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) per impostare molti più attributi della riga.</span><span class="sxs-lookup"><span data-stu-id="214cb-116">You can use various methods of the [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object to set many more attributes of the line.</span></span> <span data-ttu-id="214cb-117">I metodi [**Pen:: SetStartCap**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setstartcap) e [**Pen:: SetEndCap**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setendcap) specificano l'aspetto delle estremità della linea; il termine può essere flat, Square, arrotondato, triangolare o una forma personalizzata.</span><span class="sxs-lookup"><span data-stu-id="214cb-117">The [**Pen::SetStartCap**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setstartcap) and [**Pen::SetEndCap**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setendcap) methods specify the appearance of the ends of the line; the ends can be flat, square, rounded, triangular, or a custom shape.</span></span> <span data-ttu-id="214cb-118">Il metodo [**Pen:: SetLineJoin**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setlinejoin) consente di specificare se le linee connesse sono sgolato (unite da angoli acuti), smussate, arrotondate o ritagliate.</span><span class="sxs-lookup"><span data-stu-id="214cb-118">The [**Pen::SetLineJoin**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setlinejoin) method lets you specify whether connected lines are mitered (joined with sharp corners), beveled, rounded, or clipped.</span></span> <span data-ttu-id="214cb-119">Nella figura seguente sono illustrate le righe con diversi stili di terminazione e di join.</span><span class="sxs-lookup"><span data-stu-id="214cb-119">The following illustration shows lines with various cap and join styles.</span></span>

![illustrazione di due righe che dimostrano le estremità arrotondate e circolari, gli angoli arrotondati e sgolato e due stili di freccia](images/aboutgdip02-art04.png)

<span data-ttu-id="214cb-121">Il disegno di rettangoli con GDI+ è simile a quello delle linee di disegno.</span><span class="sxs-lookup"><span data-stu-id="214cb-121">Drawing rectangles with GDI+ is similar to drawing lines.</span></span> <span data-ttu-id="214cb-122">Per creare un rettangolo, sono necessari un oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e un oggetto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) .</span><span class="sxs-lookup"><span data-stu-id="214cb-122">To draw a rectangle, you need a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object.</span></span> <span data-ttu-id="214cb-123">L'oggetto **Graphics** fornisce un metodo [DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) e l'oggetto **Pen** archivia gli attributi, ad esempio la lunghezza della linea e il colore.</span><span class="sxs-lookup"><span data-stu-id="214cb-123">The **Graphics** object provides a [DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) method, and the **Pen** object stores attributes, such as line width and color.</span></span> <span data-ttu-id="214cb-124">L'indirizzo dell'oggetto **Pen** viene passato come uno degli argomenti al metodo DrawRectangle.</span><span class="sxs-lookup"><span data-stu-id="214cb-124">The address of the **Pen** object is passed as one of the arguments to the DrawRectangle method.</span></span> <span data-ttu-id="214cb-125">Nell'esempio seguente viene disegnato un rettangolo con l'angolo superiore sinistro in (100, 50), una larghezza di 80 e un'altezza pari a 40.</span><span class="sxs-lookup"><span data-stu-id="214cb-125">The following example draws a rectangle with its upper-left corner at (100, 50), a width of 80, and a height of 40.</span></span>


```
myGraphics.DrawRectangle(&myPen, 100, 50, 80, 40);
```



<span data-ttu-id="214cb-126">[DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) è un metodo di overload della classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , quindi è possibile fornire gli argomenti in diversi modi.</span><span class="sxs-lookup"><span data-stu-id="214cb-126">[DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) is an overloaded method of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class, so there are several ways you can supply it with arguments.</span></span> <span data-ttu-id="214cb-127">È ad esempio possibile costruire un oggetto [**Rect**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect) e passare un riferimento all'oggetto **Rect** come argomento al metodo DrawRectangle.</span><span class="sxs-lookup"><span data-stu-id="214cb-127">For example, you can construct a [**Rect**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect) object and pass a reference to the **Rect** object as an argument to the DrawRectangle method.</span></span>


```
Rect myRect(100, 50, 80, 40);
myGraphics.DrawRectangle(&myPen, myRect);
```



<span data-ttu-id="214cb-128">Un oggetto [**Rect**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect) dispone di metodi per la modifica e la raccolta di informazioni sul rettangolo.</span><span class="sxs-lookup"><span data-stu-id="214cb-128">A [**Rect**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect) object has methods for manipulating and gathering information about the rectangle.</span></span> <span data-ttu-id="214cb-129">I metodi [inflat](/windows/win32/api/gdiplustypes/nf-gdiplustypes-rect-inflate(inint_inint)) e [offset](/windows/win32/api/gdiplustypes/nf-gdiplustypes-rect-offset(inconstpoint_)) , ad esempio, modificano le dimensioni e la posizione del rettangolo.</span><span class="sxs-lookup"><span data-stu-id="214cb-129">For example, the [Inflate](/windows/win32/api/gdiplustypes/nf-gdiplustypes-rect-inflate(inint_inint)) and [Offset](/windows/win32/api/gdiplustypes/nf-gdiplustypes-rect-offset(inconstpoint_)) methods change the size and position of the rectangle.</span></span> <span data-ttu-id="214cb-130">Il metodo [**Rect:: IntersectsWith**](/windows/win32/api/Gdiplustypes/nf-gdiplustypes-rect-intersectswith) indica se il rettangolo interseca un altro rettangolo specificato e il metodo [Contains](/windows/win32/api/gdiplustypes/nf-gdiplustypes-rect-contains(inint_inint)) indica se un punto specificato si trova all'interno del rettangolo.</span><span class="sxs-lookup"><span data-stu-id="214cb-130">The [**Rect::IntersectsWith**](/windows/win32/api/Gdiplustypes/nf-gdiplustypes-rect-intersectswith) method tells you whether the rectangle intersects another given rectangle, and the [Contains](/windows/win32/api/gdiplustypes/nf-gdiplustypes-rect-contains(inint_inint)) method tells you whether a given point is inside the rectangle.</span></span>

 

 
