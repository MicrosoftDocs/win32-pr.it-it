---
description: Per creare un percorso e selezionarlo in un controller di dominio, è necessario innanzitutto definire i punti che lo descrivono.
ms.assetid: 3691c3ab-f634-476d-a56b-1c187cb12120
title: Creazione percorso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caec86d5d7ca5548d021e3c959eac93633f8880c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226678"
---
# <a name="path-creation"></a><span data-ttu-id="9fdc3-103">Creazione percorso</span><span class="sxs-lookup"><span data-stu-id="9fdc3-103">Path Creation</span></span>

<span data-ttu-id="9fdc3-104">Per creare un percorso e selezionarlo in un controller di dominio, è necessario innanzitutto definire i punti che lo descrivono.</span><span class="sxs-lookup"><span data-stu-id="9fdc3-104">To create a path and select it into a DC, it is first necessary to define the points that describe it.</span></span> <span data-ttu-id="9fdc3-105">Questa operazione viene eseguita chiamando la funzione [**beginPath**](/windows/desktop/api/Wingdi/nf-wingdi-beginpath) , specificando le funzioni di disegno appropriate, quindi chiamando la funzione [**EndPath**](/windows/desktop/api/Wingdi/nf-wingdi-endpath) .</span><span class="sxs-lookup"><span data-stu-id="9fdc3-105">This is done by calling the [**BeginPath**](/windows/desktop/api/Wingdi/nf-wingdi-beginpath) function, specifying the appropriate drawing functions, and then by calling the [**EndPath**](/windows/desktop/api/Wingdi/nf-wingdi-endpath) function.</span></span> <span data-ttu-id="9fdc3-106">Questa combinazione di funzioni (**beginPath**, Drawing Functions e **EndPath**) costituisce una *parentesi del percorso*.</span><span class="sxs-lookup"><span data-stu-id="9fdc3-106">This combination of functions (**BeginPath**, drawing functions, and **EndPath**) constitute a *path bracket*.</span></span> <span data-ttu-id="9fdc3-107">Di seguito è riportato l'elenco delle funzioni di disegno che è possibile utilizzare.</span><span class="sxs-lookup"><span data-stu-id="9fdc3-107">The following is the list of drawing functions that can be used.</span></span>

-   [<span data-ttu-id="9fdc3-108">**AngleArc**</span><span class="sxs-lookup"><span data-stu-id="9fdc3-108">**AngleArc**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-anglearc)
-   [<span data-ttu-id="9fdc3-109">**Arc**</span><span class="sxs-lookup"><span data-stu-id="9fdc3-109">**Arc**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-arc)
-   [<span data-ttu-id="9fdc3-110">**ArcTo**</span><span class="sxs-lookup"><span data-stu-id="9fdc3-110">**ArcTo**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-arcto)
-   [<span data-ttu-id="9fdc3-111">**Chord**</span><span class="sxs-lookup"><span data-stu-id="9fdc3-111">**Chord**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-chord)
-   [<span data-ttu-id="9fdc3-112">**CloseFigure**</span><span class="sxs-lookup"><span data-stu-id="9fdc3-112">**CloseFigure**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-closefigure)
-   [<span data-ttu-id="9fdc3-113">**Ellisse**</span><span class="sxs-lookup"><span data-stu-id="9fdc3-113">**Ellipse**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-ellipse)
-   [<span data-ttu-id="9fdc3-114">**ExtTextOut**</span><span class="sxs-lookup"><span data-stu-id="9fdc3-114">**ExtTextOut**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta)
-   [<span data-ttu-id="9fdc3-115">**LineTo**</span><span class="sxs-lookup"><span data-stu-id="9fdc3-115">**LineTo**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-lineto)
-   [<span data-ttu-id="9fdc3-116">**MoveToEx**</span><span class="sxs-lookup"><span data-stu-id="9fdc3-116">**MoveToEx**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-movetoex)
-   [<span data-ttu-id="9fdc3-117">**Torta**</span><span class="sxs-lookup"><span data-stu-id="9fdc3-117">**Pie**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-pie)
-   [<span data-ttu-id="9fdc3-118">**Polibezier**</span><span class="sxs-lookup"><span data-stu-id="9fdc3-118">**PolyBezier**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polybezier)
-   [<span data-ttu-id="9fdc3-119">**PolyBezierTo**</span><span class="sxs-lookup"><span data-stu-id="9fdc3-119">**PolyBezierTo**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polybezierto)
-   [<span data-ttu-id="9fdc3-120">**Polidisegni**</span><span class="sxs-lookup"><span data-stu-id="9fdc3-120">**PolyDraw**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polydraw)
-   [<span data-ttu-id="9fdc3-121">**Polygon**</span><span class="sxs-lookup"><span data-stu-id="9fdc3-121">**Polygon**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polygon)
-   [<span data-ttu-id="9fdc3-122">**Polilinea**</span><span class="sxs-lookup"><span data-stu-id="9fdc3-122">**Polyline**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polyline)
-   [<span data-ttu-id="9fdc3-123">**PolylineTo**</span><span class="sxs-lookup"><span data-stu-id="9fdc3-123">**PolylineTo**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polylineto)
-   [<span data-ttu-id="9fdc3-124">**PolyPolygon**</span><span class="sxs-lookup"><span data-stu-id="9fdc3-124">**PolyPolygon**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polypolygon)
-   [<span data-ttu-id="9fdc3-125">**Polilinea**</span><span class="sxs-lookup"><span data-stu-id="9fdc3-125">**PolyPolyline**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polypolyline)
-   [<span data-ttu-id="9fdc3-126">**Rettangolo**</span><span class="sxs-lookup"><span data-stu-id="9fdc3-126">**Rectangle**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-rectangle)
-   [<span data-ttu-id="9fdc3-127">**RoundRect**</span><span class="sxs-lookup"><span data-stu-id="9fdc3-127">**RoundRect**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-roundrect)
-   [<span data-ttu-id="9fdc3-128">**TextOut**</span><span class="sxs-lookup"><span data-stu-id="9fdc3-128">**TextOut**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-textouta)

<span data-ttu-id="9fdc3-129">Quando un'applicazione chiama [**EndPath**](/windows/desktop/api/Wingdi/nf-wingdi-endpath), il sistema seleziona il percorso associato nel controller di dominio specificato.</span><span class="sxs-lookup"><span data-stu-id="9fdc3-129">When an application calls [**EndPath**](/windows/desktop/api/Wingdi/nf-wingdi-endpath), the system selects the associated path into the specified DC.</span></span> <span data-ttu-id="9fdc3-130">Se in precedenza è stato selezionato un altro percorso nel controller di dominio, il sistema elimina tale percorso senza salvarlo. Quando il sistema seleziona il percorso nel controller di dominio, un'applicazione può operare sul percorso in uno dei modi seguenti:</span><span class="sxs-lookup"><span data-stu-id="9fdc3-130">(If another path had previously been selected into the DC, the system deletes that path without saving it.) After the system selects the path into the DC, an application can operate on the path in one of the following ways:</span></span>

-   <span data-ttu-id="9fdc3-131">Disegnare la struttura del percorso (usando la penna corrente).</span><span class="sxs-lookup"><span data-stu-id="9fdc3-131">Draw the outline of the path (using the current pen).</span></span>
-   <span data-ttu-id="9fdc3-132">Disegnare l'interno del tracciato (usando il pennello corrente).</span><span class="sxs-lookup"><span data-stu-id="9fdc3-132">Paint the interior of the path (using the current brush).</span></span>
-   <span data-ttu-id="9fdc3-133">Disegnare la struttura e riempire la parte interna del percorso.</span><span class="sxs-lookup"><span data-stu-id="9fdc3-133">Draw the outline and fill the interior of the path.</span></span>
-   <span data-ttu-id="9fdc3-134">Modificare il percorso (convertendo le curve in segmenti di linea).</span><span class="sxs-lookup"><span data-stu-id="9fdc3-134">Modify the path (converting curves to line segments).</span></span>
-   <span data-ttu-id="9fdc3-135">Converte il percorso in un tracciato di ritaglio.</span><span class="sxs-lookup"><span data-stu-id="9fdc3-135">Convert the path into a clip path.</span></span>
-   <span data-ttu-id="9fdc3-136">Convertire il percorso in un'area.</span><span class="sxs-lookup"><span data-stu-id="9fdc3-136">Convert the path into a region.</span></span>
-   <span data-ttu-id="9fdc3-137">Rendere flat il percorso convertendo ogni curva del tracciato in una serie di segmenti di linea.</span><span class="sxs-lookup"><span data-stu-id="9fdc3-137">Flatten the path by converting each curve in the path into a series of line segments.</span></span>
-   <span data-ttu-id="9fdc3-138">Recuperare le coordinate delle linee e delle curve che compongono un percorso.</span><span class="sxs-lookup"><span data-stu-id="9fdc3-138">Retrieve the coordinates of the lines and curves that compose a path.</span></span>

 

 



