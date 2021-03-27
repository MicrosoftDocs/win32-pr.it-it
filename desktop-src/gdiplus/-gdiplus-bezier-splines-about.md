---
description: 'A B&\# 233; Zier spline è una curva specificata da quattro punti: due punti finali (P1 e P2) e due punti di controllo (C1 e C2).'
ms.assetid: 3ee279ea-20cc-4089-b1a5-13bf1c7c4942
title: Spline Bezier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8dd725e64f9ba0035849d2d1d6fbc03d5efa0b17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131386"
---
# <a name="bezier-splines"></a><span data-ttu-id="7855b-103">Spline Bezier</span><span class="sxs-lookup"><span data-stu-id="7855b-103">Bezier Splines</span></span>

<span data-ttu-id="7855b-104">Una spline di Bézier è una curva specificata da quattro punti: due punti finali (P1 e P2) e due punti di controllo (C1 e C2).</span><span class="sxs-lookup"><span data-stu-id="7855b-104">A Bézier spline is a curve specified by four points: two end points (p1 and p2) and two control points (c1 and c2).</span></span> <span data-ttu-id="7855b-105">La curva inizia a P1 e termina in corrispondenza di P2.</span><span class="sxs-lookup"><span data-stu-id="7855b-105">The curve begins at p1 and ends at p2.</span></span> <span data-ttu-id="7855b-106">La curva non passa attraverso i punti di controllo, ma i punti di controllo fungono da magneti, spostando la curva in determinate direzioni e influenzando il modo in cui la curva curva.</span><span class="sxs-lookup"><span data-stu-id="7855b-106">The curve doesn't pass through the control points, but the control points act as magnets, pulling the curve in certain directions and influencing the way the curve bends.</span></span> <span data-ttu-id="7855b-107">La figura seguente mostra una curva di Bézier insieme ai relativi endpoint e punti di controllo.</span><span class="sxs-lookup"><span data-stu-id="7855b-107">The following illustration shows a Bézier curve along with its endpoints and control points.</span></span>

![illustrazione che mostra una spline di Bezier con due punti finali e due punti di controllo](images/aboutgdip02-art11a.png)

<span data-ttu-id="7855b-109">Si noti che la curva inizia da P1 e viene spostata verso il punto di controllo C1.</span><span class="sxs-lookup"><span data-stu-id="7855b-109">Note that the curve starts at p1 and moves toward the control point c1.</span></span> <span data-ttu-id="7855b-110">La linea tangente alla curva in P1 è la linea disegnata da P1 a C1.</span><span class="sxs-lookup"><span data-stu-id="7855b-110">The tangent line to the curve at p1 is the line drawn from p1 to c1.</span></span> <span data-ttu-id="7855b-111">Si noti inoltre che la linea tangente nell'endpoint P2 è la linea disegnata da C2 a P2.</span><span class="sxs-lookup"><span data-stu-id="7855b-111">Also note that the tangent line at the endpoint p2 is the line drawn from c2 to p2.</span></span>

<span data-ttu-id="7855b-112">Per creare una spline di Bézier, sono necessari un oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e un oggetto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) .</span><span class="sxs-lookup"><span data-stu-id="7855b-112">To draw a Bézier spline, you need a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object.</span></span> <span data-ttu-id="7855b-113">L'oggetto **Graphics** fornisce il metodo [DrawBezier](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawbezier(inconstpen_inint_inint_inint_inint_inint_inint_inint_inint)) e l'oggetto **Pen** archivia gli attributi della curva, ad esempio la lunghezza della linea e il colore.</span><span class="sxs-lookup"><span data-stu-id="7855b-113">The **Graphics** object provides the [DrawBezier](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawbezier(inconstpen_inint_inint_inint_inint_inint_inint_inint_inint)) method, and the **Pen** object stores attributes of the curve, such as line width and color.</span></span> <span data-ttu-id="7855b-114">L'indirizzo dell'oggetto **Pen** viene passato come uno degli argomenti al metodo DrawBezier.</span><span class="sxs-lookup"><span data-stu-id="7855b-114">The address of the **Pen** object is passed as one of the arguments to the DrawBezier method.</span></span> <span data-ttu-id="7855b-115">Gli argomenti rimanenti passati al metodo DrawBezier sono gli endpoint e i punti di controllo.</span><span class="sxs-lookup"><span data-stu-id="7855b-115">The remaining arguments passed to the DrawBezier method are the endpoints and the control points.</span></span> <span data-ttu-id="7855b-116">Nell'esempio seguente viene disegnata una spline Bézier con punto iniziale (0,0), punti di controllo (40, 20) e (80, 150) e punto finale (100, 10).</span><span class="sxs-lookup"><span data-stu-id="7855b-116">The following example draws a Bézier spline with starting point (0, 0), control points (40, 20) and (80, 150), and ending point (100, 10).</span></span>


```
myGraphics.DrawBezier(&myPen, 0, 0, 40, 20, 80, 150, 100, 10);
```



<span data-ttu-id="7855b-117">Nella figura seguente vengono illustrati la curva, i punti di controllo e due linee tangente.</span><span class="sxs-lookup"><span data-stu-id="7855b-117">The following illustration shows the curve, the control points, and two tangent lines.</span></span>

![illustrazione che mostra una spline di Bezier con due punti finali, due punti di controllo e due linee tangente](images/aboutgdip02-art12.png)

<span data-ttu-id="7855b-119">Le spline di Bézier sono state originariamente sviluppate da Pierre Bézier per la progettazione nel settore automobilistico.</span><span class="sxs-lookup"><span data-stu-id="7855b-119">Bézier splines were originally developed by Pierre Bézier for design in the automotive industry.</span></span> <span data-ttu-id="7855b-120">Hanno dimostrato di essere molto utile in molti tipi di progettazione assistita da computer e vengono usati anche per definire le strutture dei tipi di carattere.</span><span class="sxs-lookup"><span data-stu-id="7855b-120">They have since proven to be very useful in many types of computer-aided design and are also used to define the outlines of fonts.</span></span> <span data-ttu-id="7855b-121">Le spline di Bézier possono produrre un'ampia gamma di forme, alcune delle quali sono illustrate nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="7855b-121">Bézier splines can yield a wide variety of shapes, some of which are shown in the following illustration.</span></span>

![illustrazione che mostra tre spline di Bezier](images/aboutgdip02-art13.png)

 

 



