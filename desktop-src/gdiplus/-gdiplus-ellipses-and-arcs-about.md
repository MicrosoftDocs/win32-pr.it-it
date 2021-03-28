---
description: Un'ellisse è specificata dal relativo rettangolo di delimitazione. Nell'illustrazione seguente viene mostrata un'ellisse insieme al rettangolo di delimitazione.
ms.assetid: 45e80501-4d64-480b-a7c7-3af52c00a0aa
title: Ellissi e archi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8b1aaaff5ff27191ed7f0bf64ddbcb414be6319
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131346"
---
# <a name="ellipses-and-arcs"></a><span data-ttu-id="e335d-104">Ellissi e archi</span><span class="sxs-lookup"><span data-stu-id="e335d-104">Ellipses and Arcs</span></span>

<span data-ttu-id="e335d-105">Un'ellisse è specificata dal relativo rettangolo di delimitazione.</span><span class="sxs-lookup"><span data-stu-id="e335d-105">An ellipse is specified by its bounding rectangle.</span></span> <span data-ttu-id="e335d-106">Nell'illustrazione seguente viene mostrata un'ellisse insieme al rettangolo di delimitazione.</span><span class="sxs-lookup"><span data-stu-id="e335d-106">The following illustration shows an ellipse along with its bounding rectangle.</span></span>

![illustrazione di un'ellisse racchiusa all'interno di un rettangolo di delimitazione](images/aboutgdip02-art05.png)

<span data-ttu-id="e335d-108">Per creare un'ellisse, è necessario un oggetto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e un oggetto [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) .</span><span class="sxs-lookup"><span data-stu-id="e335d-108">To draw an ellipse, you need a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and a [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) object.</span></span> <span data-ttu-id="e335d-109">L'oggetto **Graphics** fornisce il metodo [DrawEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrect_)) e l'oggetto **Pen** archivia gli attributi dell'ellisse, ad esempio la lunghezza della linea e il colore.</span><span class="sxs-lookup"><span data-stu-id="e335d-109">The **Graphics** object provides the [DrawEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrect_)) method, and the **Pen** object stores attributes of the ellipse, such as line width and color.</span></span> <span data-ttu-id="e335d-110">L'indirizzo dell'oggetto **Pen** viene passato come uno degli argomenti al metodo DrawEllipse.</span><span class="sxs-lookup"><span data-stu-id="e335d-110">The address of the **Pen** object is passed as one of the arguments to the DrawEllipse method.</span></span> <span data-ttu-id="e335d-111">Gli argomenti rimanenti passati al metodo DrawEllipse specificano il rettangolo di delimitazione per l'ellisse.</span><span class="sxs-lookup"><span data-stu-id="e335d-111">The remaining arguments passed to the DrawEllipse method specify the bounding rectangle for the ellipse.</span></span> <span data-ttu-id="e335d-112">Nell'esempio seguente viene disegnata un'ellisse. il rettangolo di delimitazione ha una larghezza di 160, un'altezza di 80 e un angolo superiore sinistro di (100, 50).</span><span class="sxs-lookup"><span data-stu-id="e335d-112">The following example draws an ellipse; the bounding rectangle has a width of 160, a height of 80, and an upper-left corner of (100, 50).</span></span>


```
myGraphics.DrawEllipse(&myPen, 100, 50, 160, 80);
```



<span data-ttu-id="e335d-113">[DrawEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrect_)) è un metodo di overload della classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , quindi è possibile fornire gli argomenti in diversi modi.</span><span class="sxs-lookup"><span data-stu-id="e335d-113">[DrawEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrect_)) is an overloaded method of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class, so there are several ways you can supply it with arguments.</span></span> <span data-ttu-id="e335d-114">È ad esempio possibile costruire un oggetto [**Rect**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect) e passare un riferimento all'oggetto **Rect** come argomento al metodo DrawEllipse.</span><span class="sxs-lookup"><span data-stu-id="e335d-114">For example, you can construct a [**Rect**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect) object and pass a reference to the **Rect** object as an argument to the DrawEllipse method.</span></span>


```
Rect myRect(100, 50, 160, 80);
myGraphics.DrawEllipse(&myPen, myRect);
```



<span data-ttu-id="e335d-115">Un arco è una parte di un'ellisse.</span><span class="sxs-lookup"><span data-stu-id="e335d-115">An arc is a portion of an ellipse.</span></span> <span data-ttu-id="e335d-116">Per creare un arco, chiamare il metodo [DrawArc](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawarc(inconstpen_inint_inint_inint_inint_inreal_inreal)) della classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="e335d-116">To draw an arc, you call the [DrawArc](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawarc(inconstpen_inint_inint_inint_inint_inreal_inreal)) method of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span> <span data-ttu-id="e335d-117">I parametri del metodo DrawArc corrispondono ai parametri del metodo [DrawEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrect_)) , ad eccezione del fatto che DrawArc richiede un angolo iniziale e un angolo di apertura.</span><span class="sxs-lookup"><span data-stu-id="e335d-117">The parameters of the DrawArc method are the same as the parameters of the [DrawEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrect_)) method, except that DrawArc requires a starting angle and sweep angle.</span></span> <span data-ttu-id="e335d-118">Nell'esempio seguente viene disegnato un arco con un angolo iniziale di 30 gradi e un angolo di apertura di 180 gradi.</span><span class="sxs-lookup"><span data-stu-id="e335d-118">The following example draws an arc with a starting angle of 30 degrees and a sweep angle of 180 degrees.</span></span>


```
myGraphics.DrawArc(&myPen, 100, 50, 160, 80, 30, 180);
```



<span data-ttu-id="e335d-119">Nella figura seguente vengono illustrati l'arco, l'ellisse e il rettangolo di delimitazione.</span><span class="sxs-lookup"><span data-stu-id="e335d-119">The following illustration shows the arc, the ellipse, and the bounding rectangle.</span></span>

![illustrazione di un'ellisse all'interno di un rettangolo di delimitazione; la metà sinistra inferiore dell'ellisse viene disegnata in rosso](images/aboutgdip02-art06.png)

 

 



