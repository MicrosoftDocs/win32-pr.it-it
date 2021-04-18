---
title: Libreria IRIS GL Sphere
description: OpenGL non supporta la libreria IRIS GL Sphere. È possibile sostituire le chiamate della libreria Sphere con le routine quadriche dalla libreria GLU. Per ulteriori informazioni sulla libreria GLU, vedere la guida per programmatori Open GL e la libreria di utilità OpenGL.
ms.assetid: 2b7e6a3d-d2d0-4b54-8dff-8c4d6b113007
keywords:
- Porting di IRIS GL, libreria Sphere
- porting da IRIS GL, Sphere Library
- porting in OpenGL da IRIS GL, Sphere Library
- Porting OpenGL da IRIS GL, Sphere Library
- funzioni di disegno, libreria Sphere
- libreria Sphere
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 586974c5874aee73121e536cbadca4564a18c250
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330639"
---
# <a name="the-iris-gl-sphere-library"></a><span data-ttu-id="a0435-111">Libreria IRIS GL Sphere</span><span class="sxs-lookup"><span data-stu-id="a0435-111">The IRIS GL Sphere Library</span></span>

<span data-ttu-id="a0435-112">OpenGL non supporta la libreria IRIS GL Sphere.</span><span class="sxs-lookup"><span data-stu-id="a0435-112">OpenGL does not support the IRIS GL sphere library.</span></span> <span data-ttu-id="a0435-113">È possibile sostituire le chiamate della libreria Sphere con le routine quadriche dalla libreria GLU.</span><span class="sxs-lookup"><span data-stu-id="a0435-113">You can replace your sphere library calls with quadrics routines from the GLU library.</span></span> <span data-ttu-id="a0435-114">Per ulteriori informazioni sulla libreria GLU, vedere la *Guida per programmatori Open GL* e la [libreria di utilità OpenGL](opengl-utility-library.md).</span><span class="sxs-lookup"><span data-stu-id="a0435-114">For more information about the GLU library, see the *Open GL Programming Guide* and [OpenGL Utility Library](opengl-utility-library.md).</span></span>

<span data-ttu-id="a0435-115">La tabella seguente elenca le funzioni OpenGL quadriche.</span><span class="sxs-lookup"><span data-stu-id="a0435-115">The following table lists the OpenGL quadrics functions.</span></span>



| <span data-ttu-id="a0435-116">OpenGL (funzione)</span><span class="sxs-lookup"><span data-stu-id="a0435-116">OpenGL function</span></span>                                        | <span data-ttu-id="a0435-117">Significato</span><span class="sxs-lookup"><span data-stu-id="a0435-117">Meaning</span></span>                                                          |
|--------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="a0435-118">**gluNewQuadric**</span><span class="sxs-lookup"><span data-stu-id="a0435-118">**gluNewQuadric**</span></span>](glunewquadric.md)                 | <span data-ttu-id="a0435-119">Crea un nuovo oggetto quadrica.</span><span class="sxs-lookup"><span data-stu-id="a0435-119">Creates a new quadric object.</span></span>                                    |
| [<span data-ttu-id="a0435-120">**gluDeleteQuadric**</span><span class="sxs-lookup"><span data-stu-id="a0435-120">**gluDeleteQuadric**</span></span>](gludeletequadric.md)           | <span data-ttu-id="a0435-121">Elimina un oggetto quadrica.</span><span class="sxs-lookup"><span data-stu-id="a0435-121">Deletes a quadric object.</span></span>                                        |
| [<span data-ttu-id="a0435-122">*gluQuadricCallback*</span><span class="sxs-lookup"><span data-stu-id="a0435-122">*gluQuadricCallback*</span></span>](gluquadric.md)                 | <span data-ttu-id="a0435-123">Associa un callback a un oggetto quadrica per la gestione degli errori.</span><span class="sxs-lookup"><span data-stu-id="a0435-123">Associates a callback with a quadric object, for error handling.</span></span> |
| [<span data-ttu-id="a0435-124">**gluQuadricNormals**</span><span class="sxs-lookup"><span data-stu-id="a0435-124">**gluQuadricNormals**</span></span>](gluquadricnormals.md)         | <span data-ttu-id="a0435-125">Specifica i normali: nessun normale, uno per volto o uno per vertice.</span><span class="sxs-lookup"><span data-stu-id="a0435-125">Specifies normals: no normals, one per face, or one per vertex.</span></span>  |
| [<span data-ttu-id="a0435-126">**gluQuadricOrientation**</span><span class="sxs-lookup"><span data-stu-id="a0435-126">**gluQuadricOrientation**</span></span>](gluquadricorientation.md) | <span data-ttu-id="a0435-127">Specifica la direzione dei normali: verso l'esterno o verso l'interno.</span><span class="sxs-lookup"><span data-stu-id="a0435-127">Specifies direction of normals: outward or inward.</span></span>               |
| [<span data-ttu-id="a0435-128">**gluQuadricTexture**</span><span class="sxs-lookup"><span data-stu-id="a0435-128">**gluQuadricTexture**</span></span>](gluquadrictexture.md)         | <span data-ttu-id="a0435-129">Attiva o disattiva la generazione della coordinata della trama.</span><span class="sxs-lookup"><span data-stu-id="a0435-129">Turns texture-coordinate generation on or off.</span></span>                   |
| [<span data-ttu-id="a0435-130">**gluQuadricDrawstyle**</span><span class="sxs-lookup"><span data-stu-id="a0435-130">**gluQuadricDrawstyle**</span></span>](gluquadricdrawstyle.md)     | <span data-ttu-id="a0435-131">Specifica lo stile di disegno: poligoni, linee, punti e così via.</span><span class="sxs-lookup"><span data-stu-id="a0435-131">Specifies drawing style: polygons, lines, points, and so on.</span></span>     |
| [<span data-ttu-id="a0435-132">**gluSphere**</span><span class="sxs-lookup"><span data-stu-id="a0435-132">**gluSphere**</span></span>](glusphere.md)                         | <span data-ttu-id="a0435-133">Disegna una sfera.</span><span class="sxs-lookup"><span data-stu-id="a0435-133">Draws a sphere.</span></span>                                                  |
| [<span data-ttu-id="a0435-134">**gluCylinder**</span><span class="sxs-lookup"><span data-stu-id="a0435-134">**gluCylinder**</span></span>](glucylinder.md)                     | <span data-ttu-id="a0435-135">Disegna un cilindro o un cono.</span><span class="sxs-lookup"><span data-stu-id="a0435-135">Draws a cylinder or cone.</span></span>                                        |
| [<span data-ttu-id="a0435-136">**gluPartialDisk**</span><span class="sxs-lookup"><span data-stu-id="a0435-136">**gluPartialDisk**</span></span>](glupartialdisk.md)               | <span data-ttu-id="a0435-137">Disegna un arco.</span><span class="sxs-lookup"><span data-stu-id="a0435-137">Draws an arc.</span></span>                                                    |
| [<span data-ttu-id="a0435-138">**gluDisk**</span><span class="sxs-lookup"><span data-stu-id="a0435-138">**gluDisk**</span></span>](gludisk.md)                             | <span data-ttu-id="a0435-139">Disegna un cerchio o un disco.</span><span class="sxs-lookup"><span data-stu-id="a0435-139">Draws a circle or disk.</span></span>                                          |



 

<span data-ttu-id="a0435-140">È possibile usare un oggetto quadrica per tutti quadriche di cui si vuole eseguire il rendering in modo analogo.</span><span class="sxs-lookup"><span data-stu-id="a0435-140">You can use one quadric object for all quadrics you want to render in similar ways.</span></span> <span data-ttu-id="a0435-141">Nell'esempio di codice seguente vengono usati due oggetti quadrica per creare quattro quadriche, due dei quali con trama.</span><span class="sxs-lookup"><span data-stu-id="a0435-141">The following code sample uses two quadric objects to draw four quadrics, two of them textured.</span></span>


```C++
GLUquadricObj    *texturedQuad, *plainQuad; 
 
texturedQuad = gluNewQuadric(void); 
gluQuadricTexture(texturedQuad, GL_TRUE); 
gluQuadricOrientation(texturedQuad, GLU_OUTSIDE); 
gluQuadricDrawStyle(texturedQuad, GLU_FILL); 
 
plainQuad = gluNewQuadric(void); 
gluQuadricDrawStyle(plainQuad, GLU_LINE); 
 
glColor3f (1.0, 1.0, 1.0); 
 
gluSphere(texturedQuad, 5.0, 20, 20); 
glTranslatef(10.0, 10.0, 0.0); 
gluCylinder(texturedQuad, 2.5, 5, 5, 10, 10); 
glTranslatef(10.0, 10.0, 0.0); 
gluDisk(plainQuad, 2.0, 5.0, 10, 10); 
glTranslatef(10.0, 10.0, 0.0); 
gluSphere(plainQuad, 5.0, 20, 20);
```



 

 




