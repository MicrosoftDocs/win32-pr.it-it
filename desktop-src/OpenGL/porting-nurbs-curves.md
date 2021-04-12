---
title: Porting di curve NURBS
description: Le funzioni OpenGL per il disegno di curve NURBS sono molto simili alle funzioni GL di IRIS. È possibile specificare sequenze di nodi e punti di controllo utilizzando una funzione gluNurbsCurve, che deve essere contenuta all'interno di una coppia gluBeginCurve/gluEndCurve.
ms.assetid: 954e8029-06bd-4072-9b84-53ecba1d05da
keywords:
- Porting di IRIS GL, curve NURBS
- porting da IRIS GL, curve NURBS
- porting in OpenGL da IRIS GL, curve NURBS
- Porting OpenGL da IRIS GL, curve NURBS
- Curve NURBS
- curve
- Porting di IRIS GL, curve
- porting da IRIS GL, curve
- porting in OpenGL da IRIS GL, curve
- Porting OpenGL da IRIS GL, curve
- NURBS (B-spline razionale non uniforme)
- B-spline razionale non uniforme (NURBS)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f539e466ce8ade17d135c9369e1f641831792e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396335"
---
# <a name="porting-nurbs-curves"></a><span data-ttu-id="35438-116">Porting di curve NURBS</span><span class="sxs-lookup"><span data-stu-id="35438-116">Porting NURBS Curves</span></span>

<span data-ttu-id="35438-117">Le funzioni OpenGL per il disegno di curve NURBS sono molto simili alle funzioni GL di IRIS.</span><span class="sxs-lookup"><span data-stu-id="35438-117">The OpenGL functions for drawing NURBS curves are very similar to the IRIS GL functions.</span></span> <span data-ttu-id="35438-118">È possibile specificare sequenze di nodi e punti di controllo utilizzando una funzione [**gluNurbsCurve**](glunurbscurve.md) , che deve essere contenuta all'interno di una [](glubegincurve.md)  /  coppia [**gluEndCurve**](gluendcurve.md) gluBeginCurve.</span><span class="sxs-lookup"><span data-stu-id="35438-118">You specify knot sequences and control points using a [**gluNurbsCurve**](glunurbscurve.md) function, which must be contained within a [**gluBeginCurve**](glubegincurve.md) / [**gluEndCurve**](gluendcurve.md) pair.</span></span>

<span data-ttu-id="35438-119">La tabella seguente elenca le funzioni di IRIS GL per la creazione di curve NURBS e le relative funzioni OpenGL equivalenti.</span><span class="sxs-lookup"><span data-stu-id="35438-119">The following table lists the IRIS GL functions for drawing NURBS curves and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="35438-120">Funzione IRIS GL</span><span class="sxs-lookup"><span data-stu-id="35438-120">IRIS GL function</span></span> | <span data-ttu-id="35438-121">OpenGL (funzione)</span><span class="sxs-lookup"><span data-stu-id="35438-121">OpenGL function</span></span>                        | <span data-ttu-id="35438-122">Significato</span><span class="sxs-lookup"><span data-stu-id="35438-122">Meaning</span></span>                     |
|------------------|----------------------------------------|-----------------------------|
| <span data-ttu-id="35438-123">**bgncurve**</span><span class="sxs-lookup"><span data-stu-id="35438-123">**bgncurve**</span></span>     | [<span data-ttu-id="35438-124">**gluBeginCurve**</span><span class="sxs-lookup"><span data-stu-id="35438-124">**gluBeginCurve**</span></span>](glubegincurve.md) | <span data-ttu-id="35438-125">Inizia una definizione della curva.</span><span class="sxs-lookup"><span data-stu-id="35438-125">Begins a curve definition.</span></span>  |
| <span data-ttu-id="35438-126">**NurbsCurve**</span><span class="sxs-lookup"><span data-stu-id="35438-126">**nurbscurve**</span></span>   | [<span data-ttu-id="35438-127">**gluNurbsCurve**</span><span class="sxs-lookup"><span data-stu-id="35438-127">**gluNurbsCurve**</span></span>](glunurbscurve.md) | <span data-ttu-id="35438-128">Specifica gli attributi della curva.</span><span class="sxs-lookup"><span data-stu-id="35438-128">Specifies curve attributes.</span></span> |
| <span data-ttu-id="35438-129">**endcurve**</span><span class="sxs-lookup"><span data-stu-id="35438-129">**endcurve**</span></span>     | [<span data-ttu-id="35438-130">**gluEndCurve**</span><span class="sxs-lookup"><span data-stu-id="35438-130">**gluEndCurve**</span></span>](gluendcurve.md)     | <span data-ttu-id="35438-131">Termina una definizione di curva.</span><span class="sxs-lookup"><span data-stu-id="35438-131">Ends a curve definition.</span></span>    |



 

<span data-ttu-id="35438-132">Associare le coordinate della posizione, della trama e del colore presentando ognuno come **gluNurbsCurve** separato all'interno della coppia di inizio/fine.</span><span class="sxs-lookup"><span data-stu-id="35438-132">Associate position, texture, and color coordinates by presenting each as a separate **gluNurbsCurve** inside the begin/end pair.</span></span> <span data-ttu-id="35438-133">È possibile non eseguire più di una chiamata a **gluNurbsCurve** per ogni parte dei dati di colore, posizione e trama all'interno di una singola coppia **gluBeginCurve/gluEndCurve** .</span><span class="sxs-lookup"><span data-stu-id="35438-133">You can make no more than one call to **gluNurbsCurve** for each piece of color, position, and texture data within a single **gluBeginCurve/gluEndCurve** pair.</span></span> <span data-ttu-id="35438-134">È necessario effettuare esattamente una chiamata per descrivere la posizione della curva (una descrizione di GL \_ Mappa1 \_ Vertex \_ 3 o GL \_ Mappa1 \_ Vertex \_ 4).</span><span class="sxs-lookup"><span data-stu-id="35438-134">You must make exactly one call to describe the position of the curve (a GL\_MAP1\_VERTEX\_3 or GL\_MAP1\_VERTEX\_4 description).</span></span> <span data-ttu-id="35438-135">Quando si chiama **gluEndCurve**, la curva è tassellati in segmenti di linea e viene quindi sottoposta a rendering.</span><span class="sxs-lookup"><span data-stu-id="35438-135">When you call **gluEndCurve**, the curve is tessellated into line segments and then rendered.</span></span>

<span data-ttu-id="35438-136">La tabella seguente elenca i tipi di curve NURBS IRIS e OpenGL.</span><span class="sxs-lookup"><span data-stu-id="35438-136">The following table lists IRIS GL and OpenGL NURBS curve types.</span></span>



| <span data-ttu-id="35438-137">Tipo GL IRIS</span><span class="sxs-lookup"><span data-stu-id="35438-137">IRIS GL type</span></span> | <span data-ttu-id="35438-138">Tipo OpenGL</span><span class="sxs-lookup"><span data-stu-id="35438-138">OpenGL type</span></span>                  | <span data-ttu-id="35438-139">Significato</span><span class="sxs-lookup"><span data-stu-id="35438-139">Meaning</span></span>                                 |
|--------------|------------------------------|-----------------------------------------|
| <span data-ttu-id="35438-140">N \_ V3D</span><span class="sxs-lookup"><span data-stu-id="35438-140">N\_V3D</span></span>       | <span data-ttu-id="35438-141">\_Vertice GL \_ Mappa1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="35438-141">GL\_MAP1\_VERTEX\_3</span></span>          | <span data-ttu-id="35438-142">Curva polinomiale.</span><span class="sxs-lookup"><span data-stu-id="35438-142">Polynomial curve.</span></span>                       |
| <span data-ttu-id="35438-143">N \_ V3DR</span><span class="sxs-lookup"><span data-stu-id="35438-143">N\_V3DR</span></span>      | <span data-ttu-id="35438-144">\_Mappa1 \_ Vertex \_ 4</span><span class="sxs-lookup"><span data-stu-id="35438-144">GL\_MAP1\_VERTEX\_4</span></span>          | <span data-ttu-id="35438-145">Curva razionale.</span><span class="sxs-lookup"><span data-stu-id="35438-145">Rational curve.</span></span>                         |
|              | <span data-ttu-id="35438-146">\_ \_ Coord trama GL \_ Mappa1\_\*</span><span class="sxs-lookup"><span data-stu-id="35438-146">GL\_MAP1\_TEXTURE\_COORD\_\*</span></span> | <span data-ttu-id="35438-147">I punti di controllo sono coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="35438-147">Control points are texture coordinates.</span></span> |
|              | <span data-ttu-id="35438-148">\_Normale MAPPA1 \_ GL</span><span class="sxs-lookup"><span data-stu-id="35438-148">GL\_MAP1\_NORMAL</span></span>             | <span data-ttu-id="35438-149">I punti di controllo sono normali.</span><span class="sxs-lookup"><span data-stu-id="35438-149">Control points are normals.</span></span>             |



 

<span data-ttu-id="35438-150">Per ulteriori informazioni sui tipi di analizzatore disponibili, vedere [**glMap1**](glmap1.md).</span><span class="sxs-lookup"><span data-stu-id="35438-150">For more information on available evaluator types, see [**glMap1**](glmap1.md).</span></span>

<span data-ttu-id="35438-151">??</span><span class="sxs-lookup"><span data-stu-id="35438-151">??</span></span>

 

 




