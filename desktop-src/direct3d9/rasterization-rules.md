---
description: Spesso i punti specificati per i vertici non corrispondono esattamente ai pixel sullo schermo. Quando si verifica questa situazione, Direct3D applica le regole di rasterizzazione dei triangoli per decidere quali pixel applicare a un determinato triangolo.
ms.assetid: 919b36f1-d4de-4d5d-ba1a-0605bf59a6cd
title: Regole di rasterizzazione (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5115b2f12e0064202fcbca58f52cb163166d0a82
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/04/2021
ms.locfileid: "104234414"
---
# <a name="rasterization-rules-direct3d-9"></a><span data-ttu-id="ebe32-104">Regole di rasterizzazione (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="ebe32-104">Rasterization Rules (Direct3D 9)</span></span>

<span data-ttu-id="ebe32-105">Spesso i punti specificati per i vertici non corrispondono esattamente ai pixel sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="ebe32-105">Often, the points specified for vertices do not precisely match the pixels on the screen.</span></span> <span data-ttu-id="ebe32-106">Quando si verifica questa situazione, Direct3D applica le regole di rasterizzazione dei triangoli per decidere quali pixel applicare a un determinato triangolo.</span><span class="sxs-lookup"><span data-stu-id="ebe32-106">When this happens, Direct3D applies triangle rasterization rules to decide which pixels apply to a given triangle.</span></span>

-   [<span data-ttu-id="ebe32-107">Regole di rasterizzazione triangolare</span><span class="sxs-lookup"><span data-stu-id="ebe32-107">Triangle Rasterization Rules</span></span>](#triangle-rasterization-rules)
-   [<span data-ttu-id="ebe32-108">Regole per punti e linee</span><span class="sxs-lookup"><span data-stu-id="ebe32-108">Point and Line Rules</span></span>](#point-and-line-rules)
-   [<span data-ttu-id="ebe32-109">Regole sprite punto</span><span class="sxs-lookup"><span data-stu-id="ebe32-109">Point Sprite Rules</span></span>](#point-sprite-rules)

## <a name="triangle-rasterization-rules"></a><span data-ttu-id="ebe32-110">Regole di rasterizzazione triangolare</span><span class="sxs-lookup"><span data-stu-id="ebe32-110">Triangle Rasterization Rules</span></span>

<span data-ttu-id="ebe32-111">Direct3D utilizza una convenzione di riempimento in alto a sinistra per riempire la geometria.</span><span class="sxs-lookup"><span data-stu-id="ebe32-111">Direct3D uses a top-left filling convention for filling geometry.</span></span> <span data-ttu-id="ebe32-112">Si tratta della stessa convenzione utilizzata per i rettangoli in GDI e OpenGL.</span><span class="sxs-lookup"><span data-stu-id="ebe32-112">This is the same convention that is used for rectangles in GDI and OpenGL.</span></span> <span data-ttu-id="ebe32-113">In Direct3D, il centro del pixel è il punto decisivo.</span><span class="sxs-lookup"><span data-stu-id="ebe32-113">In Direct3D, the center of the pixel is the decisive point.</span></span> <span data-ttu-id="ebe32-114">Se il centro si trova all'interno di un triangolo, il pixel fa parte del triangolo.</span><span class="sxs-lookup"><span data-stu-id="ebe32-114">If the center is inside a triangle, the pixel is part of the triangle.</span></span> <span data-ttu-id="ebe32-115">I pixel Center sono coordinate di tipo Integer.</span><span class="sxs-lookup"><span data-stu-id="ebe32-115">Pixel centers are at integer coordinates.</span></span>

<span data-ttu-id="ebe32-116">Questa descrizione delle regole di rasterizzazione dei triangolari utilizzate da Direct3D non si applica necessariamente a tutti i componenti hardware disponibili.</span><span class="sxs-lookup"><span data-stu-id="ebe32-116">This description of triangle-rasterization rules used by Direct3D does not necessarily apply to all available hardware.</span></span> <span data-ttu-id="ebe32-117">I test possono individuare variazioni minime nell'implementazione di queste regole.</span><span class="sxs-lookup"><span data-stu-id="ebe32-117">Your testing may uncover minor variations in the implementation of these rules.</span></span>

<span data-ttu-id="ebe32-118">Nella figura seguente viene illustrato un rettangolo il cui angolo superiore sinistro è (0,0) e il cui angolo inferiore destro è (5, 5).</span><span class="sxs-lookup"><span data-stu-id="ebe32-118">The following illustration shows a rectangle whose upper-left corner is at (0, 0) and whose lower-right corner is at (5, 5).</span></span> <span data-ttu-id="ebe32-119">Questo rettangolo riempie 25 pixel, esattamente come ci si aspetterebbe.</span><span class="sxs-lookup"><span data-stu-id="ebe32-119">This rectangle fills 25 pixels, just as you would expect.</span></span> <span data-ttu-id="ebe32-120">La larghezza del rettangolo è definita come Right minu Left.</span><span class="sxs-lookup"><span data-stu-id="ebe32-120">The width of the rectangle is defined as right minus left.</span></span> <span data-ttu-id="ebe32-121">L'altezza è definita come inferiore meno in alto.</span><span class="sxs-lookup"><span data-stu-id="ebe32-121">The height is defined as bottom minus top.</span></span>

![illustrazione di un quadrato numerato diviso in sei righe e colonne](images/pixmap.png)

<span data-ttu-id="ebe32-123">Nella convenzione di riempimento in alto a sinistra, *Top* si riferisce alla posizione verticale degli intervalli orizzontali e a *sinistra* si riferisce alla posizione orizzontale dei pixel all'interno di un intervallo.</span><span class="sxs-lookup"><span data-stu-id="ebe32-123">In the top-left filling convention, *top* refers to the vertical location of horizontal spans, and *left* refers to the horizontal location of pixels within a span.</span></span> <span data-ttu-id="ebe32-124">Un bordo non può essere un bordo superiore a meno che non sia orizzontale.</span><span class="sxs-lookup"><span data-stu-id="ebe32-124">An edge cannot be a top edge unless it is horizontal.</span></span> <span data-ttu-id="ebe32-125">In generale, la maggior parte dei triangoli ha solo bordi sinistro e destro.</span><span class="sxs-lookup"><span data-stu-id="ebe32-125">In general, most triangles have only left and right edges.</span></span> <span data-ttu-id="ebe32-126">La figura seguente mostra un bordo superiore e un bordo destro.</span><span class="sxs-lookup"><span data-stu-id="ebe32-126">The following illustration shows a top edge and a right edge.</span></span>

![illustrazione di un quadrato numerato che contiene due triangoli](images/triedge.png)

<span data-ttu-id="ebe32-128">La convenzione di riempimento in alto a sinistra determina l'azione eseguita da Direct3D quando un triangolo passa attraverso il centro di un pixel.</span><span class="sxs-lookup"><span data-stu-id="ebe32-128">The top-left filling convention determines the action taken by Direct3D when a triangle passes through the center of a pixel.</span></span> <span data-ttu-id="ebe32-129">Nella figura seguente vengono mostrati due triangoli, uno a (0,0), (5, 0) e (5, 5) e l'altro in (0,5), (0, 0) e (5, 5).</span><span class="sxs-lookup"><span data-stu-id="ebe32-129">The following illustration shows two triangles, one at (0, 0), (5, 0), and (5, 5), and the other at (0, 5), (0, 0), and (5, 5).</span></span> <span data-ttu-id="ebe32-130">Il primo triangolo in questo caso ottiene 15 pixel (visualizzato in nero), mentre il secondo ottiene solo 10 pixel (visualizzati in grigio) perché il bordo condiviso è il bordo sinistro del primo triangolo.</span><span class="sxs-lookup"><span data-stu-id="ebe32-130">The first triangle in this case gets 15 pixels (shown in black), whereas the second gets only 10 pixels (shown in gray) because the shared edge is the left edge of the first triangle.</span></span>

![illustrazione di un quadrato numerato che mostra due triangoli](images/twotris.png)

<span data-ttu-id="ebe32-132">Se si definisce un rettangolo con l'angolo superiore sinistro in (0,5, 0,5) e l'angolo inferiore destro in (2,5, 4,5), il punto centrale di questo rettangolo è (1,5, 2,5).</span><span class="sxs-lookup"><span data-stu-id="ebe32-132">If you define a rectangle with its upper-left corner at (0.5, 0.5) and its lower-right corner at (2.5, 4.5), the center point of this rectangle is at (1.5, 2.5).</span></span> <span data-ttu-id="ebe32-133">Quando l'rasterizzatore Direct3D tessellates questo rettangolo, il centro di ogni pixel non è ambiguo all'interno di ognuno dei quattro triangoli e la convenzione di riempimento in alto a sinistra non è necessaria.</span><span class="sxs-lookup"><span data-stu-id="ebe32-133">When the Direct3D rasterizer tessellates this rectangle, the center of each pixel is unambiguously inside each of the four triangles, and the top-left filling convention is not needed.</span></span> <span data-ttu-id="ebe32-134">La figura seguente illustra questa situazione.</span><span class="sxs-lookup"><span data-stu-id="ebe32-134">The following illustration shows this.</span></span> <span data-ttu-id="ebe32-135">I pixel nel rettangolo sono contrassegnati in base al triangolo in cui vengono inclusi in Direct3D.</span><span class="sxs-lookup"><span data-stu-id="ebe32-135">The pixels in the rectangle are labeled according to the triangle in which Direct3D includes them.</span></span>

![Mostra un quadrato numerato contenente un rettangolo diviso in quattro triangoli.](images/noambig.png)

<span data-ttu-id="ebe32-137">Se si sposta il rettangolo nell'illustrazione precedente in modo che l'angolo superiore sinistro si trovi in (1,0, 1,0), nell'angolo inferiore destro in (3,0, 5,0) e nel punto centrale in (2,0, 3,0), Direct3D applica la convenzione di riempimento superiore sinistro.</span><span class="sxs-lookup"><span data-stu-id="ebe32-137">If you move the rectangle in the preceding illustration so that its upper-left corner is at (1.0, 1.0), its lower-right corner at (3.0, 5.0), and its center point at (2.0, 3.0), Direct3D applies the top-left filling convention.</span></span> <span data-ttu-id="ebe32-138">La maggior parte dei pixel in questo rettangolo è a cavalcioni del bordo tra due o più triangoli, come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="ebe32-138">Most pixels in this rectangle straddle the border between two or more triangles, as the following illustration shows.</span></span>

![illustrazione di un quadrato numerato contenente un rettangolo diviso in quattro triangoli](images/fillrule.png)

<span data-ttu-id="ebe32-140">Per entrambi i rettangoli, sono interessati gli stessi pixel, come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="ebe32-140">For both rectangles, the same pixels are affected, as shown in the following illustration.</span></span>

![illustrazione dei pixel interessati dai due quadrati numerati precedenti](images/samepix.png)

## <a name="point-and-line-rules"></a><span data-ttu-id="ebe32-142">Regole per punti e linee</span><span class="sxs-lookup"><span data-stu-id="ebe32-142">Point and Line Rules</span></span>

<span data-ttu-id="ebe32-143">Il rendering dei punti viene eseguito come gli sprite di punti, che vengono entrambi sottoposti a rendering come quadrilateri allineati allo schermo e quindi rispettano le stesse regole del rendering poligono.</span><span class="sxs-lookup"><span data-stu-id="ebe32-143">Points are rendered the same as point sprites, which are both rendered as screen-aligned quadrilaterals and thus adhere to the same rules as polygon rendering.</span></span>

<span data-ttu-id="ebe32-144">Le regole di rendering della linea non con alias sono identiche a quelle per le [righe GDI](../gdi/lines.md).</span><span class="sxs-lookup"><span data-stu-id="ebe32-144">Non-antialiased line rendering rules are exactly the same as those for [GDI lines](../gdi/lines.md).</span></span>

<span data-ttu-id="ebe32-145">Per informazioni sul rendering di linee con anti-aliasing, vedere [**ID3DXLine**](id3dxline.md).</span><span class="sxs-lookup"><span data-stu-id="ebe32-145">For information about antialiased line rendering, see [**ID3DXLine**](id3dxline.md).</span></span>

## <a name="point-sprite-rules"></a><span data-ttu-id="ebe32-146">Regole sprite punto</span><span class="sxs-lookup"><span data-stu-id="ebe32-146">Point Sprite Rules</span></span>

<span data-ttu-id="ebe32-147">Gli sprite di punti e le primitive patch vengono rasterizzati come se le primitive fossero prima tassellati in triangoli e i triangoli risultanti rasterizzati.</span><span class="sxs-lookup"><span data-stu-id="ebe32-147">Point sprites and patch primitives are rasterized as if the primitives were first tessellated into triangles and the resulting triangles rasterized.</span></span> <span data-ttu-id="ebe32-148">Per altre informazioni, vedere [punti sprite (Direct3D 9)](point-sprites.md).</span><span class="sxs-lookup"><span data-stu-id="ebe32-148">For more information, see [Point Sprites (Direct3D 9)](point-sprites.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ebe32-149">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ebe32-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ebe32-150">Sistemi di coordinate e geometria</span><span class="sxs-lookup"><span data-stu-id="ebe32-150">Coordinate Systems and Geometry</span></span>](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 
