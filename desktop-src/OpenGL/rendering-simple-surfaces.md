---
title: Rendering di superfici semplici
description: La libreria GLU include un set di funzioni per il disegno di varie superfici semplici (sfere, cilindri, dischi e parti dei dischi) in diversi stili e orientamenti. Queste funzioni sono descritte in dettaglio nel manuale di riferimento di OpenGL.
ms.assetid: 403bdf8d-de4c-49e2-87d0-11109061b4c2
keywords:
- Utilità OpenGL (GLU), superfici semplici
- GLU (utilità OpenGL), superfici semplici
- OpenGL con superfici semplici
- Utilità OpenGL (GLU), sfere
- GLU (utilità OpenGL), sfere
- sfere OpenGL
- Utilità OpenGL (GLU), cilindri
- GLU (utilità OpenGL), cilindri
- cilindri OpenGL
- Utilità OpenGL (GLU), dischi
- GLU (utilità OpenGL), dischi
- dischi OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab766c661f89cbdec30b3295dfef8dc85b59f7fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396934"
---
# <a name="rendering-simple-surfaces"></a><span data-ttu-id="c74ff-116">Rendering di superfici semplici</span><span class="sxs-lookup"><span data-stu-id="c74ff-116">Rendering Simple Surfaces</span></span>

<span data-ttu-id="c74ff-117">La libreria GLU include un set di funzioni per il disegno di varie superfici semplici (sfere, cilindri, dischi e parti dei dischi) in diversi stili e orientamenti.</span><span class="sxs-lookup"><span data-stu-id="c74ff-117">The GLU library includes a set of functions for drawing various simple surfaces (spheres, cylinders, disks, and parts of disks) in a variety of styles and orientations.</span></span> <span data-ttu-id="c74ff-118">Queste funzioni sono descritte in dettaglio nel *Manuale di riferimento di OpenGL*.</span><span class="sxs-lookup"><span data-stu-id="c74ff-118">These functions are described in detail in the *OpenGL Reference Manual*.</span></span>

<span data-ttu-id="c74ff-119">**Per eseguire il rendering di superfici semplici**</span><span class="sxs-lookup"><span data-stu-id="c74ff-119">**To render simple surfaces**</span></span>

1.  <span data-ttu-id="c74ff-120">Creare un oggetto quadrica con [**gluNewQuadric**](glunewquadric.md).</span><span class="sxs-lookup"><span data-stu-id="c74ff-120">Create a quadric object with [**gluNewQuadric**](glunewquadric.md).</span></span>

    <span data-ttu-id="c74ff-121">Per eliminare definitivamente l'oggetto al termine dell'operazione, usare [**gluDeleteQuadric**](gludeletequadric.md).</span><span class="sxs-lookup"><span data-stu-id="c74ff-121">To destroy this object when you're finished with it, use [**gluDeleteQuadric**](gludeletequadric.md).</span></span>

2.  <span data-ttu-id="c74ff-122">Specificare lo stile di rendering desiderato, come elencato di seguito, con la funzione appropriata (a meno che non si siano soddisfatti i valori predefiniti):</span><span class="sxs-lookup"><span data-stu-id="c74ff-122">Specify the desired rendering style, as listed below, with the appropriate function (unless you're satisfied with the default values):</span></span>
    -   <span data-ttu-id="c74ff-123">Indica se devono essere generate le normalità della superficie e, in tal caso, se deve essere presente una normale per ogni vertice o una normale per ogni volto: [ **gluQuadricNormals**](gluquadricnormals.md)</span><span class="sxs-lookup"><span data-stu-id="c74ff-123">Whether surface normals should be generated, and if so, whether there should be one normal per vertex or one normal per face: [**gluQuadricNormals**](gluquadricnormals.md)</span></span>
    -   <span data-ttu-id="c74ff-124">Indica se devono essere generate le coordinate di trama: [ **gluQuadricTexture**](gluquadrictexture.md)</span><span class="sxs-lookup"><span data-stu-id="c74ff-124">Whether texture coordinates should be generated: [**gluQuadricTexture**](gluquadrictexture.md)</span></span>
    -   <span data-ttu-id="c74ff-125">Quale lato di quadrica deve essere considerato l'esterno e il quale l'interno: [ **gluQuadricOrientation**](gluquadricorientation.md)</span><span class="sxs-lookup"><span data-stu-id="c74ff-125">Which side of the quadric should be considered the outside and which the inside: [**gluQuadricOrientation**](gluquadricorientation.md)</span></span>
    -   <span data-ttu-id="c74ff-126">Indica se il quadrica deve essere disegnato come un set di poligoni, linee o punti: [ **gluQuadricDrawStyle**](gluquadricdrawstyle.md)</span><span class="sxs-lookup"><span data-stu-id="c74ff-126">Whether the quadric should be drawn as a set of polygons, lines, or points: [**gluQuadricDrawStyle**](gluquadricdrawstyle.md)</span></span>
3.  <span data-ttu-id="c74ff-127">Dopo aver specificato lo stile di rendering, richiamare la funzione di rendering per il tipo desiderato di oggetto quadrica: [**gluSphere**](glusphere.md), [**gluCylinder**](glucylinder.md), [**gluDisk**](gludisk.md)o [**gluPartialDisk**](glupartialdisk.md).</span><span class="sxs-lookup"><span data-stu-id="c74ff-127">After specifying the rendering style, invoke the rendering function for the desired type of quadric object: [**gluSphere**](glusphere.md), [**gluCylinder**](glucylinder.md), [**gluDisk**](gludisk.md), or [**gluPartialDisk**](glupartialdisk.md).</span></span>

    <span data-ttu-id="c74ff-128">Se si verifica un errore durante il rendering, viene richiamata la funzione di gestione degli errori specificata con [*gluQuadricCallBack*](gluquadric.md) .</span><span class="sxs-lookup"><span data-stu-id="c74ff-128">If an error occurs during rendering, the error-handling function you've specified with [*gluQuadricCallBack*](gluquadric.md) is invoked.</span></span>

<span data-ttu-id="c74ff-129">Usare gli argomenti *\* RADIUS*, *Height* e simili, anziché la funzione [**glScale**](glscale.md) , per ridimensionare il quadriche, in modo da non dover rinormalizzare le normali di lunghezza dell'unità generate.</span><span class="sxs-lookup"><span data-stu-id="c74ff-129">Use the *\*Radius*, *height*, and similar arguments, rather than the [**glScale**](glscale.md) function, to scale the quadrics, so that you don't have to renormalize any unit-length normals that are generated.</span></span> <span data-ttu-id="c74ff-130">Per forzare i calcoli di illuminazione a una granularità più fine, soprattutto se la specularità del materiale è elevata, impostare gli argomenti *Loops* e *Stacks* su valori diversi da 1.</span><span class="sxs-lookup"><span data-stu-id="c74ff-130">To force lighting calculations at a finer granularity, especially if the material specularity is high, set the *loops* and *stacks* arguments to values other than 1.</span></span>

 

 




