---
title: Poligoni tessellating
description: Poligoni tessellating
ms.assetid: 3b219af0-96c3-4a83-8a40-bd7966d58398
keywords:
- Utilità OpenGL (GLU), a mosaico
- GLU (utilità OpenGL), mosaico
- Utilità OpenGL (GLU), poligoni semplici
- GLU (utilità OpenGL), poligoni semplici
- poligoni semplici OpenGL
- Utilità OpenGL (GLU), poligoni complessi
- GLU (utilità OpenGL), poligoni complessi
- poligoni complessi OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 475076f6372042d61c1662b445b7573709134c65
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298814"
---
# <a name="tessellating-polygons"></a><span data-ttu-id="11eb7-111">Poligoni tessellating</span><span class="sxs-lookup"><span data-stu-id="11eb7-111">Tessellating Polygons</span></span>

<span data-ttu-id="11eb7-112">OpenGL può visualizzare direttamente solo poligoni convessi semplici.</span><span class="sxs-lookup"><span data-stu-id="11eb7-112">OpenGL can directly display only simple convex polygons.</span></span> <span data-ttu-id="11eb7-113">Un poligono è semplice se:</span><span class="sxs-lookup"><span data-stu-id="11eb7-113">A polygon is simple if:</span></span>

-   <span data-ttu-id="11eb7-114">I bordi si intersecano solo ai vertici.</span><span class="sxs-lookup"><span data-stu-id="11eb7-114">The edges intersect only at vertices.</span></span>
-   <span data-ttu-id="11eb7-115">Nessun vertice duplicato.</span><span class="sxs-lookup"><span data-stu-id="11eb7-115">There are no duplicate vertices.</span></span>
-   <span data-ttu-id="11eb7-116">Esattamente due bordi sono conformi a qualsiasi vertice.</span><span class="sxs-lookup"><span data-stu-id="11eb7-116">Exactly two edges meet at any vertex.</span></span>

<span data-ttu-id="11eb7-117">Per visualizzare semplici poligoni non convessi o poligoni semplici contenenti buchi, è necessario innanzitutto triangolare i poligoni (suddividerli in poligoni convessi).</span><span class="sxs-lookup"><span data-stu-id="11eb7-117">To display simple nonconvex polygons or simple polygons containing holes, you must first triangulate the polygons (subdivide them into convex polygons).</span></span> <span data-ttu-id="11eb7-118">Tale suddivisione viene chiamata *mosaico*.</span><span class="sxs-lookup"><span data-stu-id="11eb7-118">Such subdivision is called *tessellation*.</span></span> <span data-ttu-id="11eb7-119">GLU fornisce una raccolta di funzioni che eseguono lo schema a mosaico.</span><span class="sxs-lookup"><span data-stu-id="11eb7-119">GLU provides a collection of functions that perform tessellation.</span></span> <span data-ttu-id="11eb7-120">Si noti che le funzioni a mosaico di GLU non possono gestire poligoni non semplici; non esiste un metodo OpenGL standard per gestire tali poligoni.</span><span class="sxs-lookup"><span data-stu-id="11eb7-120">Note that the GLU tessellation functions can't handle nonsimple polygons; there is no standard OpenGL method to handle such polygons.</span></span>

<span data-ttu-id="11eb7-121">Poiché il mosaico è spesso necessario e può essere piuttosto complesso, in questa sezione vengono descritte in dettaglio le funzioni di suddivisione a mosaico di GLU.</span><span class="sxs-lookup"><span data-stu-id="11eb7-121">Because tessellation is often required and can be rather tricky, this section describes the GLU tessellation functions in detail.</span></span> <span data-ttu-id="11eb7-122">Queste funzioni accettano un poligono semplice di input arbitrario che potrebbe includere buchi, che restituiscono una combinazione di triangoli, mesh triangolari e ventole di triangolo.</span><span class="sxs-lookup"><span data-stu-id="11eb7-122">These functions take as input arbitrary simple polygons that might include holes, and they return some combination of triangles, triangle meshes, and triangle fans.</span></span> <span data-ttu-id="11eb7-123">Se non si desidera gestire mesh o fan, è possibile specificare che le funzioni a mosaico restituiscano solo triangoli.</span><span class="sxs-lookup"><span data-stu-id="11eb7-123">If you don't want to deal with meshes or fans, you can specify that the tessellation functions return only triangles.</span></span> <span data-ttu-id="11eb7-124">Tuttavia, le informazioni sulla rete e sulla ventola migliorano le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="11eb7-124">However, mesh and fan information improves performance.</span></span> <span data-ttu-id="11eb7-125">Le funzioni a mosaico poligono triangolano un poligono concavo con uno o più contorni.</span><span class="sxs-lookup"><span data-stu-id="11eb7-125">The polygon tessellation functions triangulate a concave polygon with one or more contours.</span></span>

<span data-ttu-id="11eb7-126">**Per utilizzare la suddivisione a mosaico Polygon**</span><span class="sxs-lookup"><span data-stu-id="11eb7-126">**To use polygon tessellation**</span></span>

1.  <span data-ttu-id="11eb7-127">Creare un oggetto a mosaico con [**gluNewTess**](glunewtess.md).</span><span class="sxs-lookup"><span data-stu-id="11eb7-127">Create a tessellation object with [**gluNewTess**](glunewtess.md).</span></span>
2.  <span data-ttu-id="11eb7-128">Utilizzare [*gluTessCallBack*](glutess.md) per definire le funzioni di callback che si utilizzeranno per elaborare i triangoli generati da mosaico.</span><span class="sxs-lookup"><span data-stu-id="11eb7-128">Use [*gluTessCallBack*](glutess.md) to define callback functions you will use to process the triangles generated by the tessellator.</span></span>
3.  <span data-ttu-id="11eb7-129">Con [**gluBeginPolygon**](glubeginpolygon.md), [**gluTessVertex**](glutessvertex.md), [**gluNextContour**](glunextcontour.md)e [**gluEndPolygon**](gluendpolygon.md), specificare il poligono con buchi o il Poligono concavo da tassellati.</span><span class="sxs-lookup"><span data-stu-id="11eb7-129">With [**gluBeginPolygon**](glubeginpolygon.md), [**gluTessVertex**](glutessvertex.md), [**gluNextContour**](glunextcontour.md), and [**gluEndPolygon**](gluendpolygon.md), specify the polygon with holes or the concave polygon to be tessellated.</span></span>

    <span data-ttu-id="11eb7-130">Quando la descrizione del poligono è completa, la struttura a mosaico richiama le funzioni di callback secondo necessità.</span><span class="sxs-lookup"><span data-stu-id="11eb7-130">When the polygon description is complete, the tessellation facility invokes your callback functions as necessary.</span></span>

    <span data-ttu-id="11eb7-131">È possibile eliminare gli oggetti mosaico non necessari con [**gluDeleteTess**](gludeletetess.md).</span><span class="sxs-lookup"><span data-stu-id="11eb7-131">You can destroy unneeded tessellation objects with [**gluDeleteTess**](gludeletetess.md).</span></span>

<span data-ttu-id="11eb7-132">Per ulteriori informazioni sul salvataggio dei dati a mosaico, vedere [using callback Functions](using-callback-functions.md).</span><span class="sxs-lookup"><span data-stu-id="11eb7-132">For more information on saving the tessellation data, see [Using Callback Functions](using-callback-functions.md).</span></span>

 

 




