---
title: Cenni preliminari sulle geometrie del percorso
description: Viene descritto come usare le geometrie di tracciato per definire forme complesse.
ms.assetid: 38a290be-b915-4317-b9b1-0e49e40dc8ec
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 0189c46f50e2ccc9ecc4523a4bb6f34006e59139
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/28/2021
ms.locfileid: "104566295"
---
# <a name="path-geometries-overview"></a><span data-ttu-id="b197a-103">Cenni preliminari sulle geometrie del percorso</span><span class="sxs-lookup"><span data-stu-id="b197a-103">Path Geometries Overview</span></span>

<span data-ttu-id="b197a-104">Questo argomento descrive come usare le geometrie del percorso Direct2D per creare disegni complessi.</span><span class="sxs-lookup"><span data-stu-id="b197a-104">This topic describes how to use Direct2D path geometries to create complex drawings.</span></span> <span data-ttu-id="b197a-105">Include le sezioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="b197a-105">It contains the following sections.</span></span>

-   [<span data-ttu-id="b197a-106">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="b197a-106">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="b197a-107">Geometrie di percorso in Direct2D</span><span class="sxs-lookup"><span data-stu-id="b197a-107">Path Geometries in Direct2D</span></span>](#path-geometries-in-direct2d)
-   [<span data-ttu-id="b197a-108">Uso di un ID2D1GeometrySink per popolare una geometria del percorso</span><span class="sxs-lookup"><span data-stu-id="b197a-108">Using an ID2D1GeometrySink to Populate a Path Geometry</span></span>](#using-an-id2d1geometrysink-to-populate-a-path-geometry)
-   [<span data-ttu-id="b197a-109">Esempio: creare un disegno complesso</span><span class="sxs-lookup"><span data-stu-id="b197a-109">Example: Create a Complex Drawing</span></span>](#example-create-a-complex-drawing)
    -   [<span data-ttu-id="b197a-110">Creare una geometria del percorso per la montagna sinistra</span><span class="sxs-lookup"><span data-stu-id="b197a-110">Create a Path Geometry for the Left Mountain</span></span>](#create-a-path-geometry-for-the-left-mountain)
    -   [<span data-ttu-id="b197a-111">Creare una geometria del percorso per la montagna corretta</span><span class="sxs-lookup"><span data-stu-id="b197a-111">Create a Path Geometry for the Right Mountain</span></span>](#create-a-path-geometry-for-the-right-mountain)
    -   [<span data-ttu-id="b197a-112">Creare una geometria del percorso per il sole</span><span class="sxs-lookup"><span data-stu-id="b197a-112">Create a Path Geometry for the Sun</span></span>](#create-a-path-geometry-for-the-sun)
    -   [<span data-ttu-id="b197a-113">Creare una geometria del percorso per il fiume</span><span class="sxs-lookup"><span data-stu-id="b197a-113">Create a Path Geometry for the River</span></span>](#create-a-path-geometry-for-the-river)
    -   [<span data-ttu-id="b197a-114">Eseguire il rendering delle geometrie di tracciato sullo schermo</span><span class="sxs-lookup"><span data-stu-id="b197a-114">Render the Path Geometries onto the Display</span></span>](#render-the-path-geometries-onto-the-display)
-   [<span data-ttu-id="b197a-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b197a-115">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="b197a-116">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="b197a-116">Prerequisites</span></span>

<span data-ttu-id="b197a-117">In questa panoramica si presuppone che l'utente abbia familiarità con la creazione di applicazioni Direct2D di base, come descritto in [creazione di una semplice applicazione Direct2D](direct2d-quickstart.md).</span><span class="sxs-lookup"><span data-stu-id="b197a-117">This overview assumes that you are familiar with creating basic Direct2D applications, as described in [Creating a Simple Direct2D Application](direct2d-quickstart.md).</span></span> <span data-ttu-id="b197a-118">Si presuppone anche che l'utente abbia familiarità con le funzionalità di base delle geometrie Direct2D, come descritto in [Cenni preliminari sulle geometrie](direct2d-geometries-overview.md).</span><span class="sxs-lookup"><span data-stu-id="b197a-118">It also assumes that you are familiar with the basic features of Direct2D geometries, as described in the [Geometries Overview](direct2d-geometries-overview.md).</span></span>

## <a name="path-geometries-in-direct2d"></a><span data-ttu-id="b197a-119">Geometrie di percorso in Direct2D</span><span class="sxs-lookup"><span data-stu-id="b197a-119">Path Geometries in Direct2D</span></span>

<span data-ttu-id="b197a-120">Le geometrie del percorso sono rappresentate dall'interfaccia [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) .</span><span class="sxs-lookup"><span data-stu-id="b197a-120">Path geometries are represented by the [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) interface.</span></span> <span data-ttu-id="b197a-121">Per creare un'istanza di una geometria del percorso, chiamare il metodo [**ID2D1Factory:: CreatePathGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createpathgeometry) .</span><span class="sxs-lookup"><span data-stu-id="b197a-121">To instantiate a path geometry, call the [**ID2D1Factory::CreatePathGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createpathgeometry) method.</span></span> <span data-ttu-id="b197a-122">Questi oggetti possono essere usati per descrivere figure geometriche complesse costituite da segmenti come archi, curve e linee.</span><span class="sxs-lookup"><span data-stu-id="b197a-122">These objects can be used to describe complex geometric figures composed of segments such as arcs, curves, and lines.</span></span> <span data-ttu-id="b197a-123">Per popolare una geometria del percorso con figure e segmenti, chiamare il metodo [**Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) per recuperare un [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) e usare i metodi del sink Geometry per aggiungere figure e segmenti alla geometria del percorso.</span><span class="sxs-lookup"><span data-stu-id="b197a-123">To populate a path geometry with figures and segments, call the [**Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) method to retrieve an [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) and use the geometry sink's methods to add figures and segments to the path geometry.</span></span>

## <a name="using-an-id2d1geometrysink-to-populate-a-path-geometry"></a><span data-ttu-id="b197a-124">Uso di un ID2D1GeometrySink per popolare una geometria del percorso</span><span class="sxs-lookup"><span data-stu-id="b197a-124">Using an ID2D1GeometrySink to Populate a Path Geometry</span></span>

<span data-ttu-id="b197a-125">[**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) descrive un percorso geometrico che può contenere linee, archi, curve di Bézier cubiche e curve di Bézier quadratiche.</span><span class="sxs-lookup"><span data-stu-id="b197a-125">[**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) describes a geometric path that can contain lines, arcs, cubic Bezier curves, and quadratic Bezier curves.</span></span>

<span data-ttu-id="b197a-126">Un sink di geometria è costituito da una o più cifre.</span><span class="sxs-lookup"><span data-stu-id="b197a-126">A geometry sink consists of one or more figures.</span></span> <span data-ttu-id="b197a-127">Ogni figura è costituita da uno o più segmenti di linea, curva o arco.</span><span class="sxs-lookup"><span data-stu-id="b197a-127">Each figure is made up of one or more line, curve, or arc segments.</span></span> <span data-ttu-id="b197a-128">Per creare una figura, chiamare il metodo [**BeginFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-beginfigure) , passando il punto di partenza della figura, quindi usare i metodi Add, ad esempio [**AddLine**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometrysink-addline) e [**AddBezier**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) per aggiungere segmenti.</span><span class="sxs-lookup"><span data-stu-id="b197a-128">To create a figure, call the [**BeginFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-beginfigure) method, passing in the figure's starting point, and then use its Add methods (such as [**AddLine**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometrysink-addline) and [**AddBezier**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) to add segments.</span></span> <span data-ttu-id="b197a-129">Al termine dell'aggiunta dei segmenti, chiamare il metodo [**EndFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-endfigure) .</span><span class="sxs-lookup"><span data-stu-id="b197a-129">When you are finished adding segments, call the [**EndFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-endfigure) method.</span></span> <span data-ttu-id="b197a-130">È possibile ripetere questa sequenza per creare figure aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="b197a-130">You can repeat this sequence to create additional figures.</span></span> <span data-ttu-id="b197a-131">Al termine della creazione delle figure, chiamare il metodo [**Close**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-close) .</span><span class="sxs-lookup"><span data-stu-id="b197a-131">When you are finished creating figures, call the [**Close**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-close) method.</span></span>

## <a name="example-create-a-complex-drawing"></a><span data-ttu-id="b197a-132">Esempio: creare un disegno complesso</span><span class="sxs-lookup"><span data-stu-id="b197a-132">Example: Create a Complex Drawing</span></span>

<span data-ttu-id="b197a-133">Nella figura seguente viene illustrato un disegno complesso con linee, archi e curve di Bezier.</span><span class="sxs-lookup"><span data-stu-id="b197a-133">The following illustration shows a complex drawing with lines, arcs, and Bezier curves.</span></span> <span data-ttu-id="b197a-134">Nell'esempio di codice seguente viene illustrato come creare il disegno usando quattro oggetti Geometry di percorso, uno per la montagna sinistra, uno per la montagna destra, uno per il fiume e uno per il sole con flare.</span><span class="sxs-lookup"><span data-stu-id="b197a-134">The code example that follows shows how to create the drawing by using four path geometry objects, one for the left mountain, one for the right mountain, one for the river, and one for the sun with flares.</span></span>

![illustrazione di un fiume, delle montagne e del sole, usando geometrie di percorso](images/path-geo-mnts.png)

### <a name="create-a-path-geometry-for-the-left-mountain"></a><span data-ttu-id="b197a-136">Creare una geometria del percorso per la montagna sinistra</span><span class="sxs-lookup"><span data-stu-id="b197a-136">Create a Path Geometry for the Left Mountain</span></span>

<span data-ttu-id="b197a-137">Nell'esempio viene innanzitutto creata una geometria del percorso per la montagna sinistra, come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="b197a-137">The example first creates a path geometry for the left mountain as shown in the following illustration.</span></span>

![Mostra un disegno complesso di un poligono che mostra una montagna.](images/path-geo-leftmnt.png)

<span data-ttu-id="b197a-139">Per creare la montagna sinistra, nell'esempio viene chiamato il metodo [**ID2D1Factory:: CreatePathGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createpathgeometry) per creare un [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry).</span><span class="sxs-lookup"><span data-stu-id="b197a-139">To create the left mountain, the example calls the [**ID2D1Factory::CreatePathGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createpathgeometry) method to create an [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry).</span></span>


```C++
hr = m_pD2DFactory->CreatePathGeometry(&m_pLeftMountainGeometry);
```



<span data-ttu-id="b197a-140">Nell'esempio viene quindi usato il metodo [**Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) per ottenere un sink di geometria da un [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) e archiviarlo nella variabile *pSink* .</span><span class="sxs-lookup"><span data-stu-id="b197a-140">The example then uses the [**Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) method to obtain a geometry sink from an [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) and stores it in the *pSink* variable.</span></span>


```C++
ID2D1GeometrySink *pSink = NULL;
hr = m_pLeftMountainGeometry->Open(&pSink);
```



<span data-ttu-id="b197a-141">Nell'esempio viene quindi chiamato [**BeginFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-beginfigure), passando [**nella \_ Figura d2d1 \_ Begin \_ filled**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_figure_begin) che indica che questa figura è compilata, quindi chiama [**AddLines**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-addlines), passando una matrice di punti di [**d2d1 \_ punto \_ 2F**](d2d1-point-2f.md) , (267, 177), (236, 192), (212, 160), (156, 255) e (346, 255).</span><span class="sxs-lookup"><span data-stu-id="b197a-141">The example then calls [**BeginFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-beginfigure), passing in [**D2D1\_FIGURE\_BEGIN\_FILLED**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_figure_begin) that indicates this figure is filled, then calls [**AddLines**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-addlines), passing in an array of [**D2D1\_POINT\_2F**](d2d1-point-2f.md) points, (267, 177), (236, 192), (212, 160), (156, 255) and (346, 255).</span></span>

<span data-ttu-id="b197a-142">A tal fine, osservare il codice indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="b197a-142">The following code shows how to do this.</span></span>


```C++
pSink->SetFillMode(D2D1_FILL_MODE_WINDING);

pSink->BeginFigure(
    D2D1::Point2F(346,255),
    D2D1_FIGURE_BEGIN_FILLED
    );
D2D1_POINT_2F points[5] = {
   D2D1::Point2F(267, 177),
   D2D1::Point2F(236, 192),
   D2D1::Point2F(212, 160),
   D2D1::Point2F(156, 255),
   D2D1::Point2F(346, 255), 
   };
pSink->AddLines(points, ARRAYSIZE(points));
pSink->EndFigure(D2D1_FIGURE_END_CLOSED);
```



### <a name="create-a-path-geometry-for-the-right-mountain"></a><span data-ttu-id="b197a-143">Creare una geometria del percorso per la montagna corretta</span><span class="sxs-lookup"><span data-stu-id="b197a-143">Create a Path Geometry for the Right Mountain</span></span>

<span data-ttu-id="b197a-144">Nell'esempio viene quindi creata un'altra geometria del percorso per la montagna corretta con i punti (481, 146), (449, 181), (433, 159), (401, 214), (381, 199), (323, 263) e (575, 263).</span><span class="sxs-lookup"><span data-stu-id="b197a-144">The example then creates another path geometry for the right mountain with points (481, 146), (449, 181), (433, 159), (401, 214), (381, 199), (323, 263), and (575, 263).</span></span> <span data-ttu-id="b197a-145">L'illustrazione seguente mostra come viene visualizzata la montagna corretta.</span><span class="sxs-lookup"><span data-stu-id="b197a-145">The following illustration shows how the right mountain is displayed.</span></span>

![illustrazione di un poligono che mostra una montagna](images/path-geo-rightmnt.png)

<span data-ttu-id="b197a-147">A tal fine, osservare il codice indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="b197a-147">The following code shows how to do this.</span></span>


```C++
        hr = m_pD2DFactory->CreatePathGeometry(&m_pRightMountainGeometry);
        if(SUCCEEDED(hr))
        {
            ID2D1GeometrySink *pSink = NULL;

            hr = m_pRightMountainGeometry->Open(&pSink);
            if (SUCCEEDED(hr))
            {
                pSink->SetFillMode(D2D1_FILL_MODE_WINDING);

                pSink->BeginFigure(
                    D2D1::Point2F(575,263),
                    D2D1_FIGURE_BEGIN_FILLED
                    );
                D2D1_POINT_2F points[] = {
                   D2D1::Point2F(481, 146),
                   D2D1::Point2F(449, 181),
                   D2D1::Point2F(433, 159),
                   D2D1::Point2F(401, 214),
                   D2D1::Point2F(381, 199), 
                   D2D1::Point2F(323, 263), 
                   D2D1::Point2F(575, 263)
                   };
                pSink->AddLines(points, ARRAYSIZE(points));
                pSink->EndFigure(D2D1_FIGURE_END_CLOSED);
            }
            hr = pSink->Close();

            SafeRelease(&pSink);
       }
```



### <a name="create-a-path-geometry-for-the-sun"></a><span data-ttu-id="b197a-148">Creare una geometria del percorso per il sole</span><span class="sxs-lookup"><span data-stu-id="b197a-148">Create a Path Geometry for the Sun</span></span>

<span data-ttu-id="b197a-149">Nell'esempio viene quindi popolata un'altra geometria del percorso per il Dom, come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="b197a-149">The example then populates another path geometry for the sun as shown in the following illustration.</span></span>

![illustrazione di curve arco e Bezier che mostrano il sole](images/path-geo-sun.png)

<span data-ttu-id="b197a-151">A tale scopo, la geometria del percorso crea un sink e aggiunge una figura per l'arco e una figura per ogni bagliore al sink.</span><span class="sxs-lookup"><span data-stu-id="b197a-151">To do this, the path geometry creates a sink, and adds a figure for the arc and a figure for each flare to the sink.</span></span> <span data-ttu-id="b197a-152">Ripetendo la sequenza di [**BeginFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-beginfigure), i metodi Add (ad esempio [**AddBezier**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget))) e [**EndFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-endfigure), vengono aggiunte più cifre al sink.</span><span class="sxs-lookup"><span data-stu-id="b197a-152">By repeating the sequence of [**BeginFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-beginfigure), its Add (such as [**AddBezier**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget))) methods, and [**EndFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-endfigure), multiple figures are added to the sink.</span></span>

<span data-ttu-id="b197a-153">A tal fine, osservare il codice indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="b197a-153">The following code shows how to do this.</span></span>


```C++
        hr = m_pD2DFactory->CreatePathGeometry(&m_pSunGeometry);
        if(SUCCEEDED(hr))
        {
            ID2D1GeometrySink *pSink = NULL;

            hr = m_pSunGeometry->Open(&pSink);
            if (SUCCEEDED(hr))
            {
                pSink->SetFillMode(D2D1_FILL_MODE_WINDING);
            
                pSink->BeginFigure(
                    D2D1::Point2F(270, 255),
                    D2D1_FIGURE_BEGIN_FILLED
                    );
                pSink->AddArc(
                    D2D1::ArcSegment(
                        D2D1::Point2F(440, 255), // end point
                        D2D1::SizeF(85, 85),
                        0.0f, // rotation angle
                        D2D1_SWEEP_DIRECTION_CLOCKWISE,
                        D2D1_ARC_SIZE_SMALL
                        ));            
                pSink->EndFigure(D2D1_FIGURE_END_CLOSED);

                pSink->BeginFigure(
                    D2D1::Point2F(299, 182),
                    D2D1_FIGURE_BEGIN_HOLLOW
                    );
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(299, 182),
                       D2D1::Point2F(294, 176),
                       D2D1::Point2F(285, 178)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(276, 179),
                       D2D1::Point2F(272, 173),
                       D2D1::Point2F(272, 173)
                       ));
                pSink->EndFigure(D2D1_FIGURE_END_OPEN);

                pSink->BeginFigure(
                    D2D1::Point2F(354, 156),
                    D2D1_FIGURE_BEGIN_HOLLOW
                    );
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(354, 156),
                       D2D1::Point2F(358, 149),
                       D2D1::Point2F(354, 142)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(349, 134),
                       D2D1::Point2F(354, 127),
                       D2D1::Point2F(354, 127)
                       ));
                pSink->EndFigure(D2D1_FIGURE_END_OPEN);

                pSink->BeginFigure(
                    D2D1::Point2F(322,164),
                    D2D1_FIGURE_BEGIN_HOLLOW
                    );
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(322, 164),
                       D2D1::Point2F(322, 156),
                       D2D1::Point2F(314, 152)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(306, 149),
                       D2D1::Point2F(305, 141),
                       D2D1::Point2F(305, 141)
                       ));              
                pSink->EndFigure(D2D1_FIGURE_END_OPEN);

                pSink->BeginFigure(
                    D2D1::Point2F(385, 164),
                    D2D1_FIGURE_BEGIN_HOLLOW
                    );
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(385,164),
                       D2D1::Point2F(392,161),
                       D2D1::Point2F(394,152)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(395,144),
                       D2D1::Point2F(402,141),
                       D2D1::Point2F(402,142)
                       ));                
                pSink->EndFigure(D2D1_FIGURE_END_OPEN);

                pSink->BeginFigure(
                    D2D1::Point2F(408,182),
                    D2D1_FIGURE_BEGIN_HOLLOW
                    );
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(408,182),
                       D2D1::Point2F(416,184),
                       D2D1::Point2F(422,178)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(428,171),
                       D2D1::Point2F(435,173),
                       D2D1::Point2F(435,173)
                       ));
                pSink->EndFigure(D2D1_FIGURE_END_OPEN);
            }
            hr = pSink->Close();

            SafeRelease(&pSink);
       }
```



### <a name="create-a-path-geometry-for-the-river"></a><span data-ttu-id="b197a-154">Creare una geometria del percorso per il fiume</span><span class="sxs-lookup"><span data-stu-id="b197a-154">Create a Path Geometry for the River</span></span>

<span data-ttu-id="b197a-155">Nell'esempio viene quindi creato un altro percorso geometrico per il fiume che contiene curve di Bezier.</span><span class="sxs-lookup"><span data-stu-id="b197a-155">The example then creates another geometry path for the river that contains Bezier curves.</span></span> <span data-ttu-id="b197a-156">La figura seguente mostra come viene visualizzato il fiume.</span><span class="sxs-lookup"><span data-stu-id="b197a-156">The following illustration shows how the river is displayed.</span></span>

![illustrazione delle curve di Bezier che mostrano un fiume](images/path-geo-river.png)

<span data-ttu-id="b197a-158">A tal fine, osservare il codice indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="b197a-158">The following code shows how to do this.</span></span>


```C++
        hr = m_pD2DFactory->CreatePathGeometry(&m_pRiverGeometry);
    
        if(SUCCEEDED(hr))
        {
            ID2D1GeometrySink *pSink = NULL;

            hr = m_pRiverGeometry->Open(&pSink);
            if (SUCCEEDED(hr))
            {
                pSink->SetFillMode(D2D1_FILL_MODE_WINDING);
                pSink->BeginFigure(
                    D2D1::Point2F(183, 392),
                    D2D1_FIGURE_BEGIN_FILLED
                    );
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(238, 284),
                       D2D1::Point2F(472, 345),
                       D2D1::Point2F(356, 303)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(237, 261),
                       D2D1::Point2F(333, 256),
                       D2D1::Point2F(333, 256)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(335, 257),
                       D2D1::Point2F(241, 261),
                       D2D1::Point2F(411, 306)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(574, 350),
                       D2D1::Point2F(288, 324),
                       D2D1::Point2F(296, 392)
                       ));
                pSink->EndFigure(D2D1_FIGURE_END_OPEN);
            }
```



### <a name="render-the-path-geometries-onto-the-display"></a><span data-ttu-id="b197a-159">Eseguire il rendering delle geometrie di tracciato sullo schermo</span><span class="sxs-lookup"><span data-stu-id="b197a-159">Render the Path Geometries onto the Display</span></span>

<span data-ttu-id="b197a-160">Il codice seguente illustra come eseguire il rendering delle geometrie del percorso popolato sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="b197a-160">The following code shows how to render the populated path geometries on the display.</span></span> <span data-ttu-id="b197a-161">Disegna e disegna prima di tutto la geometria solare, successiva la geometria della montagna sinistra, quindi la geometria del fiume e infine la geometria della montagna corretta.</span><span class="sxs-lookup"><span data-stu-id="b197a-161">It first draws and paints the sun geometry, next the left mountain geometry, then the river geometry, and finally the right mountain geometry.</span></span>


```C++
 m_pRenderTarget->BeginDraw();

 m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

 m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::White));

 D2D1_SIZE_F rtSize = m_pRenderTarget->GetSize();
 m_pRenderTarget->FillRectangle(
     D2D1::RectF(0, 0, rtSize.width, rtSize.height),
     m_pGridPatternBitmapBrush
     );

 m_pRenderTarget->FillGeometry(m_pSunGeometry, m_pRadialGradientBrush);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::Black, 1.f));
 m_pRenderTarget->DrawGeometry(m_pSunGeometry, m_pSceneBrush, 1.f);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::OliveDrab, 1.f));
 m_pRenderTarget->FillGeometry(m_pLeftMountainGeometry, m_pSceneBrush);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::Black, 1.f));
 m_pRenderTarget->DrawGeometry(m_pLeftMountainGeometry, m_pSceneBrush, 1.f);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::LightSkyBlue, 1.f));
 m_pRenderTarget->FillGeometry(m_pRiverGeometry, m_pSceneBrush);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::Black, 1.f));
 m_pRenderTarget->DrawGeometry(m_pRiverGeometry, m_pSceneBrush, 1.f);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::YellowGreen, 1.f));
 m_pRenderTarget->FillGeometry(m_pRightMountainGeometry, m_pSceneBrush);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::Black, 1.f));
 m_pRenderTarget->DrawGeometry(m_pRightMountainGeometry, m_pSceneBrush, 1.f);


 hr = m_pRenderTarget->EndDraw();
```



<span data-ttu-id="b197a-162">Nell'esempio completo viene restituita la figura seguente.</span><span class="sxs-lookup"><span data-stu-id="b197a-162">The complete example outputs the following illustration.</span></span>

![illustrazione di un fiume, delle montagne e del sole, usando geometrie di percorso](images/path-geo-mnts.png)

## <a name="related-topics"></a><span data-ttu-id="b197a-164">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b197a-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b197a-165">Creazione di un'applicazione Direct2D semplice</span><span class="sxs-lookup"><span data-stu-id="b197a-165">Creating a Simple Direct2D Application</span></span>](direct2d-quickstart.md)
</dt> <dt>

[<span data-ttu-id="b197a-166">Panoramica delle geometrie</span><span class="sxs-lookup"><span data-stu-id="b197a-166">Geometries Overview</span></span>](direct2d-geometries-overview.md)
</dt> </dl>

 

 