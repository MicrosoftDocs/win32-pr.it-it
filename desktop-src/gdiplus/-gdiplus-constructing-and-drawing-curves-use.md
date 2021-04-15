---
description: 'GDI+ supporta diversi tipi di curve: ellissi, archi, spline cardinali e B&\# 233; Zier spline.'
ms.assetid: 97a1342c-4edb-4671-b36d-b6992efad498
title: Costruzione e creazione di curve
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f61c1aa12e3152ed65cca2da6911d2d53def81b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994309"
---
# <a name="constructing-and-drawing-curves"></a><span data-ttu-id="99ff7-103">Costruzione e creazione di curve</span><span class="sxs-lookup"><span data-stu-id="99ff7-103">Constructing and Drawing Curves</span></span>

<span data-ttu-id="99ff7-104">GDI+ supporta diversi tipi di curve: ellissi, archi, spline cardinali e spline di Bézier.</span><span class="sxs-lookup"><span data-stu-id="99ff7-104">GDI+ supports several types of curves: ellipses, arcs, cardinal splines, and Bézier splines.</span></span> <span data-ttu-id="99ff7-105">Un'ellisse è definita dal relativo rettangolo di delimitazione; un arco è una parte di un'ellisse definita da un angolo iniziale e da un angolo di sweep.</span><span class="sxs-lookup"><span data-stu-id="99ff7-105">An ellipse is defined by its bounding rectangle; an arc is a portion of an ellipse defined by a starting angle and a sweep angle.</span></span> <span data-ttu-id="99ff7-106">Una spline di tipo Cardinal viene definita da una matrice di punti e da un parametro di tensionamento, ovvero la curva passa in modo graduale attraverso ogni punto della matrice e il parametro di tensione influenza la curva.</span><span class="sxs-lookup"><span data-stu-id="99ff7-106">A cardinal spline is defined by an array of points and a tension parameter — the curve passes smoothly through each point in the array, and the tension parameter influences the way the curve bends.</span></span> <span data-ttu-id="99ff7-107">Una spline di Bézier è definita da due punti finali e due punti di controllo: la curva non passa attraverso i punti di controllo, ma i punti di controllo influenzano la direzione e la curva quando la curva passa da un punto finale all'altro.</span><span class="sxs-lookup"><span data-stu-id="99ff7-107">A Bézier spline is defined by two end points and two control points — the curve does not pass through the control points, but the control points influence the direction and bend as the curve goes from one end point to the other.</span></span>

<span data-ttu-id="99ff7-108">Gli argomenti seguenti illustrano le spline cardinali e le spline di Bézier in modo più dettagliato:</span><span class="sxs-lookup"><span data-stu-id="99ff7-108">The following topics cover cardinal splines and Bézier splines in more detail:</span></span>

-   [<span data-ttu-id="99ff7-109">Disegno di spline di cardinalità</span><span class="sxs-lookup"><span data-stu-id="99ff7-109">Drawing Cardinal Splines</span></span>](-gdiplus-drawing-cardinal-splines-use.md)
-   [<span data-ttu-id="99ff7-110">Disegno di spline Bézier</span><span class="sxs-lookup"><span data-stu-id="99ff7-110">Drawing Bézier Splines</span></span>](-gdiplus-drawing-bezier-splines-use.md)

 

 



