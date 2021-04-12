---
title: Porting di comandi BGN/end
description: IRIS GL usa il paradigma begin/end ma ha una funzione diversa per ogni primitiva grafica.
ms.assetid: 4191344b-614a-42d6-8a31-7a708f17371e
keywords:
- Porting di IRIS GL, comandi BGN/end
- porting da comandi IRIS GL, BGN/end
- porting in OpenGL da IRIS GL, BGN/end Commands
- Porting OpenGL da IRIS GL, comandi BGN/end
- funzioni di disegno, comandi BGN/end
- comandi BGN/end
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c25118d4e5050ea22d4b18fab596dfb9c92f562e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396627"
---
# <a name="porting-bgnend-commands"></a><span data-ttu-id="f37c7-109">Porting di comandi BGN/end</span><span class="sxs-lookup"><span data-stu-id="f37c7-109">Porting bgn/end Commands</span></span>

<span data-ttu-id="f37c7-110">IRIS GL usa il paradigma begin/end ma ha una funzione diversa per ogni primitiva grafica.</span><span class="sxs-lookup"><span data-stu-id="f37c7-110">IRIS GL uses the begin/end paradigm but has a different function for each graphics primitive.</span></span> <span data-ttu-id="f37c7-111">È possibile, ad esempio, usare **bgnpolygon** e **endpolygon** per creare poligoni, **bgnline** e **EndLine** per creare linee.</span><span class="sxs-lookup"><span data-stu-id="f37c7-111">For example, you probably use **bgnpolygon** and **endpolygon** to draw polygons, and **bgnline** and **endline** to draw lines.</span></span> <span data-ttu-id="f37c7-112">In OpenGL si usa la struttura [**glBegin**](glbegin.md)  /  [**glEnd**](glend.md) per entrambi.</span><span class="sxs-lookup"><span data-stu-id="f37c7-112">In OpenGL, you use the [**glBegin**](glbegin.md) / [**glEnd**](glend.md) structure for both.</span></span> <span data-ttu-id="f37c7-113">In OpenGL è possibile creare la maggior parte degli oggetti geometrici racchiudendo una serie di funzioni che specificano i vertici, le normali, le trame e i colori tra le coppie di **glBegin** e le chiamate **glEnd** .</span><span class="sxs-lookup"><span data-stu-id="f37c7-113">In OpenGL you draw most geometric objects by enclosing a series of functions that specify vertices, normals, textures, and colors between pairs of **glBegin** and **glEnd** calls.</span></span> <span data-ttu-id="f37c7-114">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="f37c7-114">For example:</span></span>

``` syntax
void glBegin( GLenum mode) ; 
   /* vertex list, colors, normals, textures, materials */ 
void glEnd( void );
```

<span data-ttu-id="f37c7-115">La funzione **glBegin** accetta un singolo parametro che specifica la modalità di disegno e quindi la primitiva.</span><span class="sxs-lookup"><span data-stu-id="f37c7-115">The **glBegin** function takes a single parameter that specifies the drawing mode, and thus the primitive.</span></span> <span data-ttu-id="f37c7-116">Ecco un esempio di codice OpenGL che disegna un poligono e una riga:</span><span class="sxs-lookup"><span data-stu-id="f37c7-116">Here's an OpenGL code sample that draws a polygon and then a line:</span></span>

``` syntax
glBegin( GL_POLYGON ) ; 
   glVertex2f(20.0, 10.0); 
   glVertex2f(10.0, 30.0); 
   glVertex2f(20.0, 50.0); 
   glVertex2f(40.0, 50.0); 
   glVertex2f(50.0, 30.0); 
   glVertex2f(40.0, 10.0); 
glEnd(); 
glBegin( GL_LINES ) ; 
   glVertex2i(100,100); 
   glVertex2i(500,500); 
glEnd();
```

<span data-ttu-id="f37c7-117">Con OpenGL è possibile creare oggetti geometrici diversi specificando parametri diversi per [**glBegin**](glbegin.md).</span><span class="sxs-lookup"><span data-stu-id="f37c7-117">With OpenGL, you draw different geometric objects by specifying different parameters for [**glBegin**](glbegin.md).</span></span> <span data-ttu-id="f37c7-118">La tabella seguente elenca i parametri OpenGL **glBegin** che corrispondono alle funzioni di Iris GL equivalenti.</span><span class="sxs-lookup"><span data-stu-id="f37c7-118">The following table lists the OpenGL **glBegin** parameters that correspond to equivalent IRIS GL functions.</span></span>



| <span data-ttu-id="f37c7-119">Funzione IRIS GL</span><span class="sxs-lookup"><span data-stu-id="f37c7-119">IRIS GL function</span></span>  | <span data-ttu-id="f37c7-120">Valore della modalità glBegin</span><span class="sxs-lookup"><span data-stu-id="f37c7-120">Value of glBegin mode</span></span> | <span data-ttu-id="f37c7-121">Significato</span><span class="sxs-lookup"><span data-stu-id="f37c7-121">Meaning</span></span>                                                                                  |
|-------------------|-----------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f37c7-122">**bgnpoint**</span><span class="sxs-lookup"><span data-stu-id="f37c7-122">**bgnpoint**</span></span>      | <span data-ttu-id="f37c7-123">\_punti GL</span><span class="sxs-lookup"><span data-stu-id="f37c7-123">GL\_POINTS</span></span>            | <span data-ttu-id="f37c7-124">Punti singoli.</span><span class="sxs-lookup"><span data-stu-id="f37c7-124">Individual points.</span></span>                                                                       |
| <span data-ttu-id="f37c7-125">**bgnline**</span><span class="sxs-lookup"><span data-stu-id="f37c7-125">**bgnline**</span></span>       | <span data-ttu-id="f37c7-126">\_striscia linea \_ GL</span><span class="sxs-lookup"><span data-stu-id="f37c7-126">GL\_LINE\_STRIP</span></span>       | <span data-ttu-id="f37c7-127">Serie di segmenti di linea collegati.</span><span class="sxs-lookup"><span data-stu-id="f37c7-127">Series of connected line segments.</span></span>                                                       |
| <span data-ttu-id="f37c7-128">**bgnclosedline**</span><span class="sxs-lookup"><span data-stu-id="f37c7-128">**bgnclosedline**</span></span> | <span data-ttu-id="f37c7-129">\_ciclo linea \_ GL</span><span class="sxs-lookup"><span data-stu-id="f37c7-129">GL\_LINE\_LOOP</span></span>        | <span data-ttu-id="f37c7-130">Serie di segmenti di linea collegati, con un segmento aggiunto tra il primo e l'ultimo vertice.</span><span class="sxs-lookup"><span data-stu-id="f37c7-130">Series of connected line segments, with a segment added between first and last vertices.</span></span> |
|                   | <span data-ttu-id="f37c7-131">\_righe GL</span><span class="sxs-lookup"><span data-stu-id="f37c7-131">GL\_LINES</span></span>             | <span data-ttu-id="f37c7-132">Coppie di vertici interpretate come singoli segmenti di linea.</span><span class="sxs-lookup"><span data-stu-id="f37c7-132">Pairs of vertices interpreted as individual line segments.</span></span>                               |
| <span data-ttu-id="f37c7-133">**bgnpolygon**</span><span class="sxs-lookup"><span data-stu-id="f37c7-133">**bgnpolygon**</span></span>    | <span data-ttu-id="f37c7-134">\_poligono GL</span><span class="sxs-lookup"><span data-stu-id="f37c7-134">GL\_POLYGON</span></span>           | <span data-ttu-id="f37c7-135">Limite di un poligono convesso semplice.</span><span class="sxs-lookup"><span data-stu-id="f37c7-135">Boundary of a simple convex polygon.</span></span>                                                     |
|                   | <span data-ttu-id="f37c7-136">triangoli GL \_</span><span class="sxs-lookup"><span data-stu-id="f37c7-136">GL\_TRIANGLES</span></span>         | <span data-ttu-id="f37c7-137">Triple di vertici interpretati come triangoli.</span><span class="sxs-lookup"><span data-stu-id="f37c7-137">Triples of vertices interpreted as triangles.</span></span>                                            |
| <span data-ttu-id="f37c7-138">**bgntmesh**</span><span class="sxs-lookup"><span data-stu-id="f37c7-138">**bgntmesh**</span></span>      | <span data-ttu-id="f37c7-139">\_striscia del triangolo GL \_</span><span class="sxs-lookup"><span data-stu-id="f37c7-139">GL\_TRIANGLE\_STRIP</span></span>   | <span data-ttu-id="f37c7-140">Strisce collegate di triangoli.</span><span class="sxs-lookup"><span data-stu-id="f37c7-140">Linked strips of triangles.</span></span>                                                              |
|                   | <span data-ttu-id="f37c7-141">\_ventola del triangolo GL \_</span><span class="sxs-lookup"><span data-stu-id="f37c7-141">GL\_TRIANGLE\_FAN</span></span>     | <span data-ttu-id="f37c7-142">Fan collegati di triangoli.</span><span class="sxs-lookup"><span data-stu-id="f37c7-142">Linked fans of triangles.</span></span>                                                                |
|                   | <span data-ttu-id="f37c7-143">\_Quad GL</span><span class="sxs-lookup"><span data-stu-id="f37c7-143">GL\_QUADS</span></span>             | <span data-ttu-id="f37c7-144">Quadruple di vertici interpretate come quadrilateri.</span><span class="sxs-lookup"><span data-stu-id="f37c7-144">Quadruples of vertices interpreted as quadrilaterals.</span></span>                                    |
| <span data-ttu-id="f37c7-145">**bgnqstrip**</span><span class="sxs-lookup"><span data-stu-id="f37c7-145">**bgnqstrip**</span></span>     | <span data-ttu-id="f37c7-146">\_ \_ striping GL quad</span><span class="sxs-lookup"><span data-stu-id="f37c7-146">GL\_QUAD\_STRIP</span></span>       | <span data-ttu-id="f37c7-147">Strisce collegate di quadrilateri.</span><span class="sxs-lookup"><span data-stu-id="f37c7-147">Linked strips of quadrilaterals.</span></span>                                                         |



 

<span data-ttu-id="f37c7-148">Per una descrizione dettagliata delle differenze tra le mesh, le strisce e le ventole del triangolo, vedere la sezione relativa ai [triangoli di porting](porting-triangles.md).</span><span class="sxs-lookup"><span data-stu-id="f37c7-148">For a detailed discussion of the differences between triangle meshes, strips, and fans, see [Porting Triangles](porting-triangles.md).</span></span>

<span data-ttu-id="f37c7-149">Non esiste alcun limite al numero di vertici che è possibile specificare tra una coppia [**glBegin**](glbegin.md)  /  [**glEnd**](glend.md) .</span><span class="sxs-lookup"><span data-stu-id="f37c7-149">There is no limit to the number of vertices you can specify between a [**glBegin**](glbegin.md) / [**glEnd**](glend.md) pair.</span></span>

<span data-ttu-id="f37c7-150">Oltre a specificare i vertici all'interno di una coppia **glBegin**  /  **glEnd** , è possibile specificare un normale corrente, coordinate di trama correnti e un colore corrente.</span><span class="sxs-lookup"><span data-stu-id="f37c7-150">In addition to specifying vertices inside a **glBegin** / **glEnd** pair, you can specify a current normal, current texture coordinates, and a current color.</span></span> <span data-ttu-id="f37c7-151">La tabella seguente elenca i comandi validi all'interno di una coppia **glBegin**  /  **glEnd** .</span><span class="sxs-lookup"><span data-stu-id="f37c7-151">The following table lists the commands valid inside a **glBegin** / **glEnd** pair.</span></span>



| <span data-ttu-id="f37c7-152">Funzione IRIS GL</span><span class="sxs-lookup"><span data-stu-id="f37c7-152">IRIS GL function</span></span>        | <span data-ttu-id="f37c7-153">OpenGL (funzione)</span><span class="sxs-lookup"><span data-stu-id="f37c7-153">OpenGL function</span></span>                                                      | <span data-ttu-id="f37c7-154">Significato</span><span class="sxs-lookup"><span data-stu-id="f37c7-154">Meaning</span></span>                                          |
|-------------------------|----------------------------------------------------------------------|--------------------------------------------------|
| <span data-ttu-id="f37c7-155">**v2**, **v3**, **V4**</span><span class="sxs-lookup"><span data-stu-id="f37c7-155">**v2**, **v3**, **v4**</span></span>  | [<span data-ttu-id="f37c7-156">glVertex</span><span class="sxs-lookup"><span data-stu-id="f37c7-156">glVertex</span></span>](glvertex-functions.md)                                   | <span data-ttu-id="f37c7-157">Imposta le coordinate del vertice.</span><span class="sxs-lookup"><span data-stu-id="f37c7-157">Sets vertex coordinates.</span></span>                         |
| <span data-ttu-id="f37c7-158">**RGBcolor**, **CPack**</span><span class="sxs-lookup"><span data-stu-id="f37c7-158">**RGBcolor**, **cpack**</span></span> | [<span data-ttu-id="f37c7-159">glColor</span><span class="sxs-lookup"><span data-stu-id="f37c7-159">glColor</span></span>](glcolor-functions.md)                                     | <span data-ttu-id="f37c7-160">Imposta il colore corrente.</span><span class="sxs-lookup"><span data-stu-id="f37c7-160">Sets current color.</span></span>                              |
| <span data-ttu-id="f37c7-161">**color**</span><span class="sxs-lookup"><span data-stu-id="f37c7-161">**color**</span></span>               | [<span data-ttu-id="f37c7-162">glIndex</span><span class="sxs-lookup"><span data-stu-id="f37c7-162">glIndex</span></span>](glindex-functions.md)                                     | <span data-ttu-id="f37c7-163">Imposta l'indice del colore corrente.</span><span class="sxs-lookup"><span data-stu-id="f37c7-163">Sets current color index.</span></span>                        |
| <span data-ttu-id="f37c7-164">**n3f**</span><span class="sxs-lookup"><span data-stu-id="f37c7-164">**n3f**</span></span>                 | [<span data-ttu-id="f37c7-165">glNormal</span><span class="sxs-lookup"><span data-stu-id="f37c7-165">glNormal</span></span>](glnormal-functions.md)                                   | <span data-ttu-id="f37c7-166">Imposta le normali coordinate del vettore.</span><span class="sxs-lookup"><span data-stu-id="f37c7-166">Sets normal vector coordinates.</span></span>                  |
|                         | [<span data-ttu-id="f37c7-167">glEvalCoord</span><span class="sxs-lookup"><span data-stu-id="f37c7-167">glEvalCoord</span></span>](glevalcoord-functions.md)                             | <span data-ttu-id="f37c7-168">Valuta le mappe con una e due dimensioni abilitate.</span><span class="sxs-lookup"><span data-stu-id="f37c7-168">Evaluates enabled one- and two-dimensional maps.</span></span> |
| <span data-ttu-id="f37c7-169">**callobj**</span><span class="sxs-lookup"><span data-stu-id="f37c7-169">**callobj**</span></span>             | <span data-ttu-id="f37c7-170">[**glCallList**](glcalllist.md), [ **glCallLists**](glcalllists.md)</span><span class="sxs-lookup"><span data-stu-id="f37c7-170">[**glCallList**](glcalllist.md), [**glCallLists**](glcalllists.md)</span></span> | <span data-ttu-id="f37c7-171">Esegue gli elenchi di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="f37c7-171">Executes display list(s).</span></span>                        |
| <span data-ttu-id="f37c7-172">**T2**</span><span class="sxs-lookup"><span data-stu-id="f37c7-172">**t2**</span></span>                  | [<span data-ttu-id="f37c7-173">glTexCoord</span><span class="sxs-lookup"><span data-stu-id="f37c7-173">glTexCoord</span></span>](gltexcoord-functions.md)                               | <span data-ttu-id="f37c7-174">Imposta le coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="f37c7-174">Sets texture coordinates.</span></span>                        |
|                         | [<span data-ttu-id="f37c7-175">glEdgeFlag</span><span class="sxs-lookup"><span data-stu-id="f37c7-175">glEdgeFlag</span></span>](gledgeflag-functions.md)                               | <span data-ttu-id="f37c7-176">Controlla i bordi del disegno.</span><span class="sxs-lookup"><span data-stu-id="f37c7-176">Controls drawing edges.</span></span>                          |
| <span data-ttu-id="f37c7-177">**lmbind**</span><span class="sxs-lookup"><span data-stu-id="f37c7-177">**lmbind**</span></span>              | [<span data-ttu-id="f37c7-178">glMaterial</span><span class="sxs-lookup"><span data-stu-id="f37c7-178">glMaterial</span></span>](glmaterial-functions.md)                               | <span data-ttu-id="f37c7-179">Imposta le proprietà del materiale.</span><span class="sxs-lookup"><span data-stu-id="f37c7-179">Sets material properties.</span></span>                        |



 

> [!Note]
>
> <span data-ttu-id="f37c7-180">Se si usa una funzione OpenGL diversa da quelle elencate nella tabella precedente all'interno di una coppia [**glBegin**](glbegin.md)  /  [**glEnd**](glend.md) , si otterranno risultati imprevedibili o probabilmente un errore.</span><span class="sxs-lookup"><span data-stu-id="f37c7-180">If you use any OpenGL function other than those listed in the preceding table inside a [**glBegin**](glbegin.md) / [**glEnd**](glend.md) pair, you'll get unpredictable results, or possibly an error.</span></span>

 

 

 




