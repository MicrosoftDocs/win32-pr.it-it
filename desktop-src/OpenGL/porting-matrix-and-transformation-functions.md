---
title: Porting di matrici e funzioni di trasformazione
description: IRIS GL e OpenGL gestiscono matrici e trasformazioni in modo analogo.
ms.assetid: 732ba65a-d776-43ea-a605-0f59209c9a46
keywords:
- Porting di IRIS GL, matrici
- porting da IRIS GL, matrici
- porting in OpenGL da IRIS GL, matrici
- Porting OpenGL da IRIS GL, matrici
- matrici
- Porting, trasformazioni di IRIS GL
- porting da IRIS GL, trasformazioni
- porting in OpenGL da IRIS GL, trasformazioni
- Porting OpenGL da IRIS GL, trasformazioni
- trasformazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1c6219640085370202b8dbebad9a2e9d4992b4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331015"
---
# <a name="porting-matrix-and-transformation-functions"></a><span data-ttu-id="55337-113">Porting di matrici e funzioni di trasformazione</span><span class="sxs-lookup"><span data-stu-id="55337-113">Porting Matrix and Transformation Functions</span></span>

<span data-ttu-id="55337-114">IRIS GL e OpenGL gestiscono matrici e trasformazioni in modo analogo.</span><span class="sxs-lookup"><span data-stu-id="55337-114">IRIS GL and OpenGL handle matrices and transformations in a similar manner.</span></span> <span data-ttu-id="55337-115">Esistono tuttavia diverse differenze da tenere presenti quando si porta il codice da IRIS GL:</span><span class="sxs-lookup"><span data-stu-id="55337-115">But there are several differences to keep in mind when porting code from IRIS GL:</span></span>

-   <span data-ttu-id="55337-116">In OpenGL si è sempre in modalità a doppia matrice; non esiste alcuna modalità a matrice singola.</span><span class="sxs-lookup"><span data-stu-id="55337-116">In OpenGL you are always in double-matrix mode; there is no single-matrix mode.</span></span>
-   <span data-ttu-id="55337-117">Gli angoli sono misurati in gradi, anziché decimi di gradi.</span><span class="sxs-lookup"><span data-stu-id="55337-117">Angles are measured in degrees, instead of tenths of degrees.</span></span>
-   <span data-ttu-id="55337-118">Le chiamate della matrice di proiezione, ad esempio [**glFrustum**](glfrustum.md) e [**glOrtho**](glortho.md), ora si moltiplicano per la matrice corrente anziché essere caricate nella matrice corrente.</span><span class="sxs-lookup"><span data-stu-id="55337-118">Projection matrix calls, like [**glFrustum**](glfrustum.md) and [**glOrtho**](glortho.md), now multiply onto the current matrix, instead of being loaded onto the current matrix.</span></span>
-   <span data-ttu-id="55337-119">La funzione OpenGL, [**glRotate**](glrotate.md), è molto diversa da **ruotare**.</span><span class="sxs-lookup"><span data-stu-id="55337-119">The OpenGL function, [**glRotate**](glrotate.md), is very different from **rotate**.</span></span> <span data-ttu-id="55337-120">È possibile ruotare intorno a qualsiasi asse arbitrario, anziché essere limitato agli assi x, y e z.</span><span class="sxs-lookup"><span data-stu-id="55337-120">You can rotate around any arbitrary axis, instead of being confined to the x-, y-, and z- axes.</span></span> <span data-ttu-id="55337-121">Ad esempio, è possibile tradurre:</span><span class="sxs-lookup"><span data-stu-id="55337-121">For example, you can translate:</span></span>

    ```C++
    rotate(200*(i+1), 'z');
    ```

    

    <span data-ttu-id="55337-122">in:</span><span class="sxs-lookup"><span data-stu-id="55337-122">to:</span></span>

    ```C++
    glRotate(.1*(200*(i+1), 0.0, 0.0, 1.0);
    ```

    

    <span data-ttu-id="55337-123">Quando si esegue la conversione da **ruota** a **glRotate** , si passa a gradi da decimi di gradi e si sostituisce "z" con un vettore per l'asse z.</span><span class="sxs-lookup"><span data-stu-id="55337-123">When translating from **rotate** to **glRotate** you switch to degrees from tenths of degrees and replace 'z' with a vector for the z-axis.</span></span>

-   <span data-ttu-id="55337-124">OpenGL non è equivalente alla funzione **PolarView** .</span><span class="sxs-lookup"><span data-stu-id="55337-124">OpenGL has no equivalent to the **polarview** function.</span></span> <span data-ttu-id="55337-125">È possibile sostituirlo facilmente con una traduzione e tre rotazioni.</span><span class="sxs-lookup"><span data-stu-id="55337-125">You can replace it easily with a translation and three rotations.</span></span> <span data-ttu-id="55337-126">Ad esempio, è possibile tradurre:</span><span class="sxs-lookup"><span data-stu-id="55337-126">For example, you can translate:</span></span>

    ```C++
    polarview(distance, azimuth, incidence, twist);
     
    ```

    

    <span data-ttu-id="55337-127">in:</span><span class="sxs-lookup"><span data-stu-id="55337-127">to:</span></span>

    ```C++
    glTranslatef( 0.0, 0.0, -distance); 
    glRotatef( -twist * 10.0, 0.0, 0.0, 1.0); 
    glRotatef( -incidence * 10.0, 1.0, 0.0, 0.0); 
    glRotatef( -azimuth * 10.0, 0.0, 0.0, 1.0);
    ```

    

<span data-ttu-id="55337-128">La tabella seguente elenca le funzioni di matrice OpenGL e le rispettive funzioni di IRIS GL equivalenti.</span><span class="sxs-lookup"><span data-stu-id="55337-128">The following table lists the OpenGL matrix functions and their equivalent IRIS GL functions.</span></span>



| <span data-ttu-id="55337-129">Funzione IRIS GL</span><span class="sxs-lookup"><span data-stu-id="55337-129">IRIS GL function</span></span>              | <span data-ttu-id="55337-130">OpenGL (funzione)</span><span class="sxs-lookup"><span data-stu-id="55337-130">OpenGL function</span></span>                                                                        | <span data-ttu-id="55337-131">Significato</span><span class="sxs-lookup"><span data-stu-id="55337-131">Meaning</span></span>                                                                                                                                                                        |
|-------------------------------|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55337-132">**mMode**</span><span class="sxs-lookup"><span data-stu-id="55337-132">**mmode**</span></span>                     | [<span data-ttu-id="55337-133">**glMatrixMode**</span><span class="sxs-lookup"><span data-stu-id="55337-133">**glMatrixMode**</span></span>](glmatrixmode.md)                                                   | <span data-ttu-id="55337-134">Imposta la modalità della matrice corrente.</span><span class="sxs-lookup"><span data-stu-id="55337-134">Sets current matrix mode.</span></span>                                                                                                                                                      |
|                               | [<span data-ttu-id="55337-135">**glLoadIdentity**</span><span class="sxs-lookup"><span data-stu-id="55337-135">**glLoadIdentity**</span></span>](glloadidentity.md)                                               | <span data-ttu-id="55337-136">Sostituisce la matrice corrente con la matrice di identità.</span><span class="sxs-lookup"><span data-stu-id="55337-136">Replaces current matrix with the identity matrix.</span></span>                                                                                                                              |
| <span data-ttu-id="55337-137">**loadmatrix**</span><span class="sxs-lookup"><span data-stu-id="55337-137">**loadmatrix**</span></span>                | <span data-ttu-id="55337-138">[**glLoadMatrixf**](glloadmatrix.md),[**glLoadMatrixd**](glloadmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="55337-138">[**glLoadMatrixf**](glloadmatrix.md),[**glLoadMatrixd**](glloadmatrix.md)</span></span><br/> | <span data-ttu-id="55337-139">Sostituisce la matrice corrente con la matrice specificata.</span><span class="sxs-lookup"><span data-stu-id="55337-139">Replaces current matrix with the specified matrix.</span></span>                                                                                                                             |
| <span data-ttu-id="55337-140">**multmatrix**</span><span class="sxs-lookup"><span data-stu-id="55337-140">**multmatrix**</span></span>                | <span data-ttu-id="55337-141">[**glMultMatrixf**](glmultmatrix.md),[**glMultMatrixd**](glmultmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="55337-141">[**glMultMatrixf**](glmultmatrix.md),[**glMultMatrixd**](glmultmatrix.md)</span></span><br/> | <span data-ttu-id="55337-142">Post-moltiplica la matrice corrente con la matrice specificata (si noti che **multmatrix** è pre-moltiplicato).</span><span class="sxs-lookup"><span data-stu-id="55337-142">Post-multiplies current matrix with the specified matrix (note that **multmatrix** pre-multiplied).</span></span>                                                                            |
| <span data-ttu-id="55337-143">**MAPW**, **mapw2**</span><span class="sxs-lookup"><span data-stu-id="55337-143">**mapw**, **mapw2**</span></span>           | [<span data-ttu-id="55337-144">**gluUnProject**</span><span class="sxs-lookup"><span data-stu-id="55337-144">**gluUnProject**</span></span>](gluunproject.md)                                                   | <span data-ttu-id="55337-145">Proietta le coordinate dello spazio globale nello spazio degli oggetti (vedere anche [**gluProject**](gluproject.md)).</span><span class="sxs-lookup"><span data-stu-id="55337-145">Projects world-space coordinates to object space (see also [**gluProject**](gluproject.md)).</span></span>                                                                                  |
| <span data-ttu-id="55337-146">**Ortho**</span><span class="sxs-lookup"><span data-stu-id="55337-146">**ortho**</span></span>                     | [<span data-ttu-id="55337-147">**glOrtho**</span><span class="sxs-lookup"><span data-stu-id="55337-147">**glOrtho**</span></span>](glortho.md)                                                             | <span data-ttu-id="55337-148">Moltiplica la matrice corrente per una matrice di proiezione ortogonale.</span><span class="sxs-lookup"><span data-stu-id="55337-148">Multiplies current matrix by an orthographic projection matrix.</span></span>                                                                                                                |
| <span data-ttu-id="55337-149">**ortho2**</span><span class="sxs-lookup"><span data-stu-id="55337-149">**ortho2**</span></span>                    | [<span data-ttu-id="55337-150">**gluOrtho2D**</span><span class="sxs-lookup"><span data-stu-id="55337-150">**gluOrtho2D**</span></span>](gluortho2d.md)                                                       | <span data-ttu-id="55337-151">Definisce una matrice di proiezione ortogonale bidimensionale.</span><span class="sxs-lookup"><span data-stu-id="55337-151">Defines a two-dimensional orthographic projection matrix.</span></span>                                                                                                                      |
| <span data-ttu-id="55337-152">**prospettiva**</span><span class="sxs-lookup"><span data-stu-id="55337-152">**perspective**</span></span>               | [<span data-ttu-id="55337-153">**gluPerspective**</span><span class="sxs-lookup"><span data-stu-id="55337-153">**gluPerspective**</span></span>](gluperspective.md)                                               | <span data-ttu-id="55337-154">Definisce una matrice di proiezione prospettica.</span><span class="sxs-lookup"><span data-stu-id="55337-154">Defines a perspective projection matrix.</span></span>                                                                                                                                       |
| <span data-ttu-id="55337-155">**picksize**</span><span class="sxs-lookup"><span data-stu-id="55337-155">**picksize**</span></span>                  | [<span data-ttu-id="55337-156">**gluPickMatrix**</span><span class="sxs-lookup"><span data-stu-id="55337-156">**gluPickMatrix**</span></span>](glupickmatrix.md)                                                 | <span data-ttu-id="55337-157">Definisce un'area di selezione.</span><span class="sxs-lookup"><span data-stu-id="55337-157">Defines a picking region.</span></span>                                                                                                                                                      |
| <span data-ttu-id="55337-158">**popmatrix**</span><span class="sxs-lookup"><span data-stu-id="55337-158">**popmatrix**</span></span>                 | [<span data-ttu-id="55337-159">**glPopMatrix**</span><span class="sxs-lookup"><span data-stu-id="55337-159">**glPopMatrix**</span></span>](glpopmatrix.md)                                                     | <span data-ttu-id="55337-160">Estrae lo stack della matrice corrente, sostituendo la matrice corrente con quello sottostante.</span><span class="sxs-lookup"><span data-stu-id="55337-160">Pops current matrix stack, replacing the current matrix with the one below it.</span></span>                                                                                                 |
| <span data-ttu-id="55337-161">**pushmatrix**</span><span class="sxs-lookup"><span data-stu-id="55337-161">**pushmatrix**</span></span>                | [<span data-ttu-id="55337-162">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="55337-162">**glPushMatrix**</span></span>](glpushmatrix.md)                                                   | <span data-ttu-id="55337-163">Esegue il push dello stack di matrici corrente di uno, duplicando la matrice corrente.</span><span class="sxs-lookup"><span data-stu-id="55337-163">Pushes current matrix stack down by one, duplicating the current matrix.</span></span>                                                                                                       |
| <span data-ttu-id="55337-164">**ruota**,**Rot**</span><span class="sxs-lookup"><span data-stu-id="55337-164">**rotate**,**rot**</span></span><br/> | <span data-ttu-id="55337-165">[**glRotated**](glrotate.md),[**glRotatef**](glrotate.md)</span><span class="sxs-lookup"><span data-stu-id="55337-165">[**glRotated**](glrotate.md),[**glRotatef**](glrotate.md)</span></span><br/>                 | <span data-ttu-id="55337-166">Ruota il sistema di coordinate corrente in base all'angolo specificato sul vettore dall'origine fino al punto specificato.</span><span class="sxs-lookup"><span data-stu-id="55337-166">Rotates current coordinate system by the given angle about the vector from the origin through the given point.</span></span> <span data-ttu-id="55337-167">Si noti che la **rotazione** ruotata riguarda solo gli assi x, y e z.</span><span class="sxs-lookup"><span data-stu-id="55337-167">Note that **rotate** rotated only about the x-, y-, and z-axes.</span></span> |
| <span data-ttu-id="55337-168">**scale**</span><span class="sxs-lookup"><span data-stu-id="55337-168">**scale**</span></span>                     | <span data-ttu-id="55337-169">[**glScaled**](glscale.md),[**glScalef**](glscale.md)</span><span class="sxs-lookup"><span data-stu-id="55337-169">[**glScaled**](glscale.md),[**glScalef**](glscale.md)</span></span><br/>                     | <span data-ttu-id="55337-170">Moltiplica la matrice corrente per una matrice di scala.</span><span class="sxs-lookup"><span data-stu-id="55337-170">Multiplies current matrix by a scaling matrix.</span></span>                                                                                                                                 |
| <span data-ttu-id="55337-171">**Traduci**</span><span class="sxs-lookup"><span data-stu-id="55337-171">**translate**</span></span>                 | <span data-ttu-id="55337-172">[**glTranslatef**](gltranslate.md),[**glTranslated**](gltranslate.md)</span><span class="sxs-lookup"><span data-stu-id="55337-172">[**glTranslatef**](gltranslate.md),[**glTranslated**](gltranslate.md)</span></span><br/>     | <span data-ttu-id="55337-173">Sposta l'origine del sistema di coordinate nel punto specificato, moltiplicando la matrice corrente con una matrice di traslazione.</span><span class="sxs-lookup"><span data-stu-id="55337-173">Moves coordinate-system origin to the point specified, by multiplying the current matrix by a translation matrix.</span></span>                                                              |
| <span data-ttu-id="55337-174">**finestra**</span><span class="sxs-lookup"><span data-stu-id="55337-174">**window**</span></span>                    | [<span data-ttu-id="55337-175">**glFrustum**</span><span class="sxs-lookup"><span data-stu-id="55337-175">**glFrustum**</span></span>](glfrustum.md)                                                         | <span data-ttu-id="55337-176">Date le coordinate per i piani di ritaglio, moltiplica la matrice corrente in base a una matrice di prospettive.</span><span class="sxs-lookup"><span data-stu-id="55337-176">Given coordinates for clipping planes, multiplies the current matrix by a perspective matrix.</span></span>                                                                                  |



 

<span data-ttu-id="55337-177">OpenGL dispone di tre modalità Matrix, che vengono impostate con [**glMatrixMode**](glmatrixmode.md).</span><span class="sxs-lookup"><span data-stu-id="55337-177">OpenGL has three matrix modes, which are set with [**glMatrixMode**](glmatrixmode.md).</span></span> <span data-ttu-id="55337-178">Nella tabella seguente sono elencate le modalità disponibili come parametri per **glMatrixMode**.</span><span class="sxs-lookup"><span data-stu-id="55337-178">The following table lists the modes available as parameters for **glMatrixMode**.</span></span>



| <span data-ttu-id="55337-179">Modalità matrice GL IRIS</span><span class="sxs-lookup"><span data-stu-id="55337-179">IRIS GL matrix mode</span></span> | <span data-ttu-id="55337-180">Modalità OpenGL</span><span class="sxs-lookup"><span data-stu-id="55337-180">OpenGL mode</span></span>    | <span data-ttu-id="55337-181">Significato</span><span class="sxs-lookup"><span data-stu-id="55337-181">Meaning</span></span>                                  | <span data-ttu-id="55337-182">Profondità dello stack minima</span><span class="sxs-lookup"><span data-stu-id="55337-182">Min stack depth</span></span> |
|---------------------|----------------|------------------------------------------|-----------------|
| <span data-ttu-id="55337-183">**MTEXTURE**</span><span class="sxs-lookup"><span data-stu-id="55337-183">**MTEXTURE**</span></span>        | <span data-ttu-id="55337-184">\_trama GL</span><span class="sxs-lookup"><span data-stu-id="55337-184">GL\_TEXTURE</span></span>    | <span data-ttu-id="55337-185">Opera sullo stack della matrice di trame.</span><span class="sxs-lookup"><span data-stu-id="55337-185">Operates on the texture matrix stack.</span></span>    | <span data-ttu-id="55337-186">2</span><span class="sxs-lookup"><span data-stu-id="55337-186">2</span></span>               |
| <span data-ttu-id="55337-187">**MVIEWING**</span><span class="sxs-lookup"><span data-stu-id="55337-187">**MVIEWING**</span></span>        | <span data-ttu-id="55337-188">\_MODELVIEW GL</span><span class="sxs-lookup"><span data-stu-id="55337-188">GL\_MODELVIEW</span></span>  | <span data-ttu-id="55337-189">Opera nello stack della matrice della vista del modello.</span><span class="sxs-lookup"><span data-stu-id="55337-189">Operates on the model view matrix stack.</span></span> | <span data-ttu-id="55337-190">32</span><span class="sxs-lookup"><span data-stu-id="55337-190">32</span></span>              |
| <span data-ttu-id="55337-191">**MPROJECTION**</span><span class="sxs-lookup"><span data-stu-id="55337-191">**MPROJECTION**</span></span>     | <span data-ttu-id="55337-192">\_proiezione GL</span><span class="sxs-lookup"><span data-stu-id="55337-192">GL\_PROJECTION</span></span> | <span data-ttu-id="55337-193">Opera sullo stack della matrice di proiezione.</span><span class="sxs-lookup"><span data-stu-id="55337-193">Operates on the projection matrix stack.</span></span> | <span data-ttu-id="55337-194">2</span><span class="sxs-lookup"><span data-stu-id="55337-194">2</span></span>               |



 

 

 





