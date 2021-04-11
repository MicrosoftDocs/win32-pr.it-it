---
title: Uso di curve e superfici NURBS
description: Le funzioni NURBS B-spline (NURBS) non uniformi forniscono descrizioni generali e potenti di curve e superfici in due e tre dimensioni, convertendo le curve e le superfici negli analizzatori OpenGL.
ms.assetid: 0b55659d-9fa2-47fc-ae15-0c296bd94dcb
keywords:
- Utilità OpenGL (GLU), B-spline razionale non uniforme (NURBS)
- GLU (utilità OpenGL), B-spline razionale non uniforme (NURBS)
- OpenGL B-spline (NURBS) non uniforme
- OpenGL (non-Uniform Rational B-spline) OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f85e9a2045c417007c34d714ae6635ebfaf1180
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329199"
---
# <a name="using-nurbs-curves-and-surfaces"></a><span data-ttu-id="6e33b-107">Uso di curve e superfici NURBS</span><span class="sxs-lookup"><span data-stu-id="6e33b-107">Using NURBS Curves and Surfaces</span></span>

<span data-ttu-id="6e33b-108">Le funzioni NURBS B-spline (NURBS) non uniformi forniscono descrizioni generali e potenti di curve e superfici in due e tre dimensioni, convertendo le curve e le superfici negli analizzatori OpenGL.</span><span class="sxs-lookup"><span data-stu-id="6e33b-108">Non-Uniform Rational B-Spline (NURBS) functions provide general and powerful descriptions of curves and surfaces in two and three dimensions, converting the curves and surfaces to OpenGL evaluators.</span></span> <span data-ttu-id="6e33b-109">Le funzioni NURBS possono rappresentare la geometria in molti sistemi di progettazione meccanica computerizzati.</span><span class="sxs-lookup"><span data-stu-id="6e33b-109">The NURBS functions can represent geometry in many computer-aided mechanical design systems.</span></span> <span data-ttu-id="6e33b-110">Possono eseguire il rendering di curve e superfici in un'ampia gamma di stili e possono gestire automaticamente la suddivisione adattiva che tessellates il dominio in triangoli più piccoli in aree di curvatura elevata e bordi vicino alla silhouette.</span><span class="sxs-lookup"><span data-stu-id="6e33b-110">They can render curves and surfaces in a variety of styles, and they can automatically handle adaptive subdivision that tessellates the domain into smaller triangles in regions of high curvature and near silhouette edges.</span></span> <span data-ttu-id="6e33b-111">Le funzioni NURBS rientrano nelle categorie seguenti.</span><span class="sxs-lookup"><span data-stu-id="6e33b-111">NURBS functions fall into the following categories.</span></span>

<span data-ttu-id="6e33b-112">Per gestire un oggetto NURBS, usare:</span><span class="sxs-lookup"><span data-stu-id="6e33b-112">To manage a NURBS object, use:</span></span>

-   <span data-ttu-id="6e33b-113">[**gluNewNurbsRenderer**](glunewnurbsrenderer.md) (crea un oggetto NURBS)</span><span class="sxs-lookup"><span data-stu-id="6e33b-113">[**gluNewNurbsRenderer**](glunewnurbsrenderer.md) (create a NURBS object)</span></span>
-   <span data-ttu-id="6e33b-114">[**gluDeleteNurbsRenderer**](gludeletenurbsrenderer.md) (Elimina un oggetto NURBS)</span><span class="sxs-lookup"><span data-stu-id="6e33b-114">[**gluDeleteNurbsRenderer**](gludeletenurbsrenderer.md) (deletes a NURBS object)</span></span>
-   <span data-ttu-id="6e33b-115">[*gluNurbsCallback*](glunurbs.md) (stabilisce una funzione di gestione degli errori)</span><span class="sxs-lookup"><span data-stu-id="6e33b-115">[*gluNurbsCallback*](glunurbs.md) (establishes an error-handling function)</span></span>

<span data-ttu-id="6e33b-116">Per specificare le curve desiderate, usare:</span><span class="sxs-lookup"><span data-stu-id="6e33b-116">To specify the desired curves, use:</span></span>

-   [<span data-ttu-id="6e33b-117">**gluBeginCurve**</span><span class="sxs-lookup"><span data-stu-id="6e33b-117">**gluBeginCurve**</span></span>](glubegincurve.md)
-   [<span data-ttu-id="6e33b-118">**gluNurbsCurve**</span><span class="sxs-lookup"><span data-stu-id="6e33b-118">**gluNurbsCurve**</span></span>](glunurbscurve.md)
-   [<span data-ttu-id="6e33b-119">**gluEndCurve**</span><span class="sxs-lookup"><span data-stu-id="6e33b-119">**gluEndCurve**</span></span>](gluendcurve.md)

<span data-ttu-id="6e33b-120">Per specificare le superfici desiderate, usare:</span><span class="sxs-lookup"><span data-stu-id="6e33b-120">To specify the desired surfaces, use:</span></span>

-   [<span data-ttu-id="6e33b-121">**gluBeginSurface**</span><span class="sxs-lookup"><span data-stu-id="6e33b-121">**gluBeginSurface**</span></span>](glubeginsurface.md)
-   [<span data-ttu-id="6e33b-122">**gluNurbsSurface**</span><span class="sxs-lookup"><span data-stu-id="6e33b-122">**gluNurbsSurface**</span></span>](glunurbssurface.md)
-   [<span data-ttu-id="6e33b-123">**gluEndSurface**</span><span class="sxs-lookup"><span data-stu-id="6e33b-123">**gluEndSurface**</span></span>](gluendsurface.md)

<span data-ttu-id="6e33b-124">È anche possibile specificare un'area di trimming, che definisce un subset del dominio della superficie NURBS da valutare, in modo da poter creare superfici con limiti smussati o che contengono buchi.</span><span class="sxs-lookup"><span data-stu-id="6e33b-124">You can also specify a trimming region, which defines a subset of the NURBS surface domain to be evaluated so you can create surfaces that have smooth boundaries or that contain holes.</span></span>

<span data-ttu-id="6e33b-125">Per specificare l'area di trimming, usare:</span><span class="sxs-lookup"><span data-stu-id="6e33b-125">To specify the trimming region, use:</span></span>

-   [<span data-ttu-id="6e33b-126">**gluBeginTrim**</span><span class="sxs-lookup"><span data-stu-id="6e33b-126">**gluBeginTrim**</span></span>](glubegintrim.md)
-   [<span data-ttu-id="6e33b-127">**gluPwlCurve**</span><span class="sxs-lookup"><span data-stu-id="6e33b-127">**gluPwlCurve**</span></span>](glupwlcurve.md)
-   [<span data-ttu-id="6e33b-128">**gluNurbsCurve**</span><span class="sxs-lookup"><span data-stu-id="6e33b-128">**gluNurbsCurve**</span></span>](glunurbscurve.md)
-   [<span data-ttu-id="6e33b-129">**gluEndTrim**</span><span class="sxs-lookup"><span data-stu-id="6e33b-129">**gluEndTrim**</span></span>](gluendtrim.md)

<span data-ttu-id="6e33b-130">Come per gli oggetti quadrica, è possibile controllare la modalità di rendering delle curve e delle superfici NURBS.</span><span class="sxs-lookup"><span data-stu-id="6e33b-130">As with quadric objects, you can control how NURBS curves and surfaces are rendered.</span></span> <span data-ttu-id="6e33b-131">È possibile determinare:</span><span class="sxs-lookup"><span data-stu-id="6e33b-131">You can determine:</span></span>

-   <span data-ttu-id="6e33b-132">Indica se rimuovere una curva o una superficie il cui poliedro di controllo si trova al di fuori del viewport corrente.</span><span class="sxs-lookup"><span data-stu-id="6e33b-132">Whether to discard a curve or surface whose control polyhedron lies outside the current viewport.</span></span>
-   <span data-ttu-id="6e33b-133">Lunghezza massima (in pixel) dei bordi dei poligoni utilizzati per il rendering di curve e superfici.</span><span class="sxs-lookup"><span data-stu-id="6e33b-133">The maximum length (in pixels) of edges of polygons used to render curves and surfaces.</span></span>
-   <span data-ttu-id="6e33b-134">Sia che si tratti della matrice di proiezione, della matrice Modelview e del viewport dal server OpenGL o di fornire loro esplicitamente con [**gluLoadSamplingMatrices**](gluloadsamplingmatrices.md).</span><span class="sxs-lookup"><span data-stu-id="6e33b-134">Whether you will take the projection matrix, modelview matrix, and viewport from the OpenGL server or supply them explictly with [**gluLoadSamplingMatrices**](gluloadsamplingmatrices.md).</span></span>

<span data-ttu-id="6e33b-135">Usare [**gluNurbsProperty**](glunurbsproperty.md) per impostare queste proprietà o usare i valori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="6e33b-135">Use [**gluNurbsProperty**](glunurbsproperty.md) to set these properties, or use the default values.</span></span> <span data-ttu-id="6e33b-136">È possibile eseguire una query su un oggetto NURBS sullo stile di rendering con [**gluGetNurbsProperty**](glugetnurbsproperty.md).</span><span class="sxs-lookup"><span data-stu-id="6e33b-136">You can query a NURBS object about its rendering style with [**gluGetNurbsProperty**](glugetnurbsproperty.md).</span></span>

 

 




