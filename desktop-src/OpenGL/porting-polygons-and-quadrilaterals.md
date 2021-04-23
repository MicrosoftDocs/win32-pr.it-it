---
title: Porting di poligoni e quadrilateri
description: Tenere presente quanto segue durante la portabilità di poligoni e quadrilateri
ms.assetid: 2b752437-caf9-4336-a906-d06b2aa8bb04
keywords:
- Portabilità IRIS GL, quadrilaterali
- porting da IRIS GL, quadrilaterali
- porting to OpenGL from IRIS GL,quadrilaterals
- Portabilità OpenGL da IRIS GL, quadrilaterali
- funzioni di disegno, quadrilaterali
- Quadrilateri
- Portabilità IRIS GL, poligoni
- porting da IRIS GL, poligoni
- porting to OpenGL from IRIS GL,polygons
- Portabilità OpenGL da IRIS GL, poligoni
- funzioni di disegno, poligoni
- poligoni, porting da IRIS GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7900b44051cab9590be11198c8b01af0b7c10244
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908459"
---
# <a name="porting-polygons-and-quadrilaterals"></a><span data-ttu-id="b0567-115">Porting di poligoni e quadrilateri</span><span class="sxs-lookup"><span data-stu-id="b0567-115">Porting Polygons and Quadrilaterals</span></span>

<span data-ttu-id="b0567-116">Quando si esegue la portabilità di poligoni e quadrilateri, tenere presente quanto segue:</span><span class="sxs-lookup"><span data-stu-id="b0567-116">Keep the following points in mind when porting polygons and quadrilaterals:</span></span>

-   <span data-ttu-id="b0567-117">Non esiste alcun equivalente diretto per **concave**(**TRUE**).</span><span class="sxs-lookup"><span data-stu-id="b0567-117">There is no direct equivalent for **concave**(**TRUE**).</span></span> <span data-ttu-id="b0567-118">È invece possibile usare le routine a tessellazione in GLU, descritte in [Tessellating Polygons](tessellating-polygons.md).</span><span class="sxs-lookup"><span data-stu-id="b0567-118">Instead you can use the tessellation routines in the GLU, described in [Tessellating Polygons](tessellating-polygons.md).</span></span>
-   <span data-ttu-id="b0567-119">Le modalità poligono sono impostate in modo diverso.</span><span class="sxs-lookup"><span data-stu-id="b0567-119">Polygon modes are set differently.</span></span>
-   <span data-ttu-id="b0567-120">Queste funzioni di disegno poligono non hanno equivalenti diretti in OpenGL: la **famiglia** poli di routine; la famiglia di routine **polf;** **pmv**, **pdr** e **pclos**; **rpmv** e **rpdr**; **splf**; e **spclos**.</span><span class="sxs-lookup"><span data-stu-id="b0567-120">These polygon drawing functions have no direct equivalents in OpenGL: the **poly** family of routines; the **polf** family of routines; **pmv**, **pdr**, and **pclos**; **rpmv** and **rpdr**; **splf**; and **spclos**.</span></span>

<span data-ttu-id="b0567-121">Se il codice IRIS GL usa queste funzioni, sarà necessario riscrivere il codice usando [**glBegin**](glbegin.md)( GL \_ POLYGON ).</span><span class="sxs-lookup"><span data-stu-id="b0567-121">If your IRIS GL code uses these functions, you'll have to rewrite the code using [**glBegin**](glbegin.md)( GL\_POLYGON ).</span></span>

<span data-ttu-id="b0567-122">Nella tabella seguente sono elencate le funzioni di disegno poligono IRIS GL e le funzioni OpenGL equivalenti.</span><span class="sxs-lookup"><span data-stu-id="b0567-122">The following table lists the IRIS GL polygon drawing functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="b0567-123">Funzione GL IRIS</span><span class="sxs-lookup"><span data-stu-id="b0567-123">IRIS GL function</span></span>         | <span data-ttu-id="b0567-124">Funzione OpenGL</span><span class="sxs-lookup"><span data-stu-id="b0567-124">OpenGL function</span></span>                                                    | <span data-ttu-id="b0567-125">Significato</span><span class="sxs-lookup"><span data-stu-id="b0567-125">Meaning</span></span>                                                 |
|--------------------------|--------------------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="b0567-126">**bgnpolygonendpolygon**</span><span class="sxs-lookup"><span data-stu-id="b0567-126">**bgnpolygonendpolygon**</span></span> | <span data-ttu-id="b0567-127">[**glBegin**](glbegin.md) ( GL \_ POLYGON )[**glEnd**](glend.md)</span><span class="sxs-lookup"><span data-stu-id="b0567-127">[**glBegin**](glbegin.md) ( GL\_POLYGON )[**glEnd**](glend.md)</span></span>   | <span data-ttu-id="b0567-128">I vertici definiscono il limite di un poligono convesso semplice.</span><span class="sxs-lookup"><span data-stu-id="b0567-128">Vertices define boundary of a simple convex polygon.</span></span>    |
|                          | <span data-ttu-id="b0567-129">**glBegin**( GL \_ QUADS )**glEnd**</span><span class="sxs-lookup"><span data-stu-id="b0567-129">**glBegin**( GL\_QUADS )**glEnd**</span></span><br/>                       | <span data-ttu-id="b0567-130">Interpreta i quadrilateri dei vertici come quadrilaterali.</span><span class="sxs-lookup"><span data-stu-id="b0567-130">Interprets quadruples of vertices as quadrilaterals.</span></span>    |
| <span data-ttu-id="b0567-131">**bgnqstripendqstrip**</span><span class="sxs-lookup"><span data-stu-id="b0567-131">**bgnqstripendqstrip**</span></span>   | <span data-ttu-id="b0567-132">[**glBegin**](glbegin.md) ( GL \_ QUAD STRIP ) \_ **glEnd**</span><span class="sxs-lookup"><span data-stu-id="b0567-132">[**glBegin**](glbegin.md) ( GL\_QUAD\_STRIP )**glEnd**</span></span><br/> | <span data-ttu-id="b0567-133">Interpreta i vertici come strisce collegate di quadrilaterali.</span><span class="sxs-lookup"><span data-stu-id="b0567-133">Interprets vertices as linked strips of quadrilaterals.</span></span> |
|                          | [<span data-ttu-id="b0567-134">glEdgeFlag</span><span class="sxs-lookup"><span data-stu-id="b0567-134">glEdgeFlag</span></span>](gledgeflag-functions.md)                             |                                                         |
| <span data-ttu-id="b0567-135">**polymode**</span><span class="sxs-lookup"><span data-stu-id="b0567-135">**polymode**</span></span>             | [<span data-ttu-id="b0567-136">**glPolygonMode**</span><span class="sxs-lookup"><span data-stu-id="b0567-136">**glPolygonMode**</span></span>](glpolygonmode.md)                             | <span data-ttu-id="b0567-137">Imposta la modalità di disegno poligono.</span><span class="sxs-lookup"><span data-stu-id="b0567-137">Sets polygon drawing mode.</span></span>                              |
| <span data-ttu-id="b0567-138">**rectrectf**</span><span class="sxs-lookup"><span data-stu-id="b0567-138">**rectrectf**</span></span><br/> | [<span data-ttu-id="b0567-139">glRect</span><span class="sxs-lookup"><span data-stu-id="b0567-139">glRect</span></span>](glrect-functions.md)                                     | <span data-ttu-id="b0567-140">Disegna un rettangolo.</span><span class="sxs-lookup"><span data-stu-id="b0567-140">Draws a rectangle.</span></span>                                      |
| <span data-ttu-id="b0567-141">**sboxsboxf**</span><span class="sxs-lookup"><span data-stu-id="b0567-141">**sboxsboxf**</span></span><br/> |                                                                    | <span data-ttu-id="b0567-142">Disegna un rettangolo allineato a schermo.</span><span class="sxs-lookup"><span data-stu-id="b0567-142">Draws a screen-aligned rectangle.</span></span>                       |



 

<span data-ttu-id="b0567-143">??</span><span class="sxs-lookup"><span data-stu-id="b0567-143">??</span></span>

## <a name="porting-polygon-modes"></a><span data-ttu-id="b0567-144">Portabilità delle modalità poligono</span><span class="sxs-lookup"><span data-stu-id="b0567-144">Porting Polygon Modes</span></span>

<span data-ttu-id="b0567-145">La funzione OpenGL [**glPolygonMode**](glpolygonmode.md) consente di specificare a quale lato di un poligono (la parte posteriore o anteriore) si applica la modalità.</span><span class="sxs-lookup"><span data-stu-id="b0567-145">The OpenGL function [**glPolygonMode**](glpolygonmode.md) lets you specify which side of a polygon (the back or the front) the mode applies to.</span></span> <span data-ttu-id="b0567-146">La relativa sintassi è la seguente:</span><span class="sxs-lookup"><span data-stu-id="b0567-146">Its syntax is:</span></span>

``` syntax
void glPolygonMode( GLenum face, GLenum mode ); 
 
```

<span data-ttu-id="b0567-147">dove face è uno dei seguenti:</span><span class="sxs-lookup"><span data-stu-id="b0567-147">where face is one of:</span></span>



|<span data-ttu-id="b0567-148">Valore GLenum</span><span class="sxs-lookup"><span data-stu-id="b0567-148">GLenum value</span></span>                      |  <span data-ttu-id="b0567-149">Significato</span><span class="sxs-lookup"><span data-stu-id="b0567-149">Meaning</span></span>                                                          |
|----------------------|------------------------------------------------------------|
| <span data-ttu-id="b0567-150">GL \_ FRONT</span><span class="sxs-lookup"><span data-stu-id="b0567-150">GL\_FRONT</span></span>            | <span data-ttu-id="b0567-151">modalità che si applica ai poligoni rivolti anteriore</span><span class="sxs-lookup"><span data-stu-id="b0567-151">mode which applies to front-facing polygons</span></span>                |
| <span data-ttu-id="b0567-152">GL \_ BACK</span><span class="sxs-lookup"><span data-stu-id="b0567-152">GL\_BACK</span></span>             | <span data-ttu-id="b0567-153">modalità che si applica ai poligoni rivolti all'indietro</span><span class="sxs-lookup"><span data-stu-id="b0567-153">mode which applies to back-facing polygons</span></span>                 |
| <span data-ttu-id="b0567-154">GL \_ FRONT \_ AND \_ BACK</span><span class="sxs-lookup"><span data-stu-id="b0567-154">GL\_FRONT\_AND\_BACK</span></span> | <span data-ttu-id="b0567-155">modalità che si applica sia ai poligoni anteriore che a quello posteriore</span><span class="sxs-lookup"><span data-stu-id="b0567-155">mode which applies to both front- and back-facing polygons</span></span> |



 

<span data-ttu-id="b0567-156">La modalità \_ GL FRONT E BACK è equivalente alla funzione \_ \_ **polimode** IRIS GL.</span><span class="sxs-lookup"><span data-stu-id="b0567-156">The GL\_FRONT\_AND\_BACK mode is equivalent to the IRIS GL **polymode** function.</span></span> <span data-ttu-id="b0567-157">La tabella seguente elenca le modalità poligono IRIS GL e le modalità OpenGL equivalenti.</span><span class="sxs-lookup"><span data-stu-id="b0567-157">The following table lists IRIS GL polygon modes and their equivalent OpenGL modes.</span></span>



| <span data-ttu-id="b0567-158">Modalità GL IRIS</span><span class="sxs-lookup"><span data-stu-id="b0567-158">IRIS GL mode</span></span> | <span data-ttu-id="b0567-159">Modalità OpenGL</span><span class="sxs-lookup"><span data-stu-id="b0567-159">OpenGL mode</span></span> | <span data-ttu-id="b0567-160">Significato</span><span class="sxs-lookup"><span data-stu-id="b0567-160">Meaning</span></span>                                       |
|--------------|-------------|-----------------------------------------------|
| <span data-ttu-id="b0567-161">PYM \_ POINT</span><span class="sxs-lookup"><span data-stu-id="b0567-161">PYM\_POINT</span></span>   | <span data-ttu-id="b0567-162">PUNTO \_ GL</span><span class="sxs-lookup"><span data-stu-id="b0567-162">GL\_POINT</span></span>   | <span data-ttu-id="b0567-163">Disegna i vertici come punti.</span><span class="sxs-lookup"><span data-stu-id="b0567-163">Draws vertices as points.</span></span>                     |
| <span data-ttu-id="b0567-164">PYM \_ LINE</span><span class="sxs-lookup"><span data-stu-id="b0567-164">PYM\_LINE</span></span>    | <span data-ttu-id="b0567-165">GL \_ LINE</span><span class="sxs-lookup"><span data-stu-id="b0567-165">GL\_LINE</span></span>    | <span data-ttu-id="b0567-166">Disegna i bordi dei limiti come segmenti di linea.</span><span class="sxs-lookup"><span data-stu-id="b0567-166">Draws boundary edges as line segments.</span></span>        |
| <span data-ttu-id="b0567-167">RIEMPIMENTO \_ PYM</span><span class="sxs-lookup"><span data-stu-id="b0567-167">PYM\_FILL</span></span>    | <span data-ttu-id="b0567-168">GL \_ FILL</span><span class="sxs-lookup"><span data-stu-id="b0567-168">GL\_FILL</span></span>    | <span data-ttu-id="b0567-169">Disegna il riempimento interno del poligono.</span><span class="sxs-lookup"><span data-stu-id="b0567-169">Draws polygon interior filled.</span></span>                |
| <span data-ttu-id="b0567-170">PYM \_ INSODEME</span><span class="sxs-lookup"><span data-stu-id="b0567-170">PYM\_HOLLOW</span></span>  |             | <span data-ttu-id="b0567-171">Riempie solo i pixel interni ai limiti.</span><span class="sxs-lookup"><span data-stu-id="b0567-171">Fills only interior pixels at the boundaries.</span></span> |



 

## <a name="porting-polygon-stipples"></a><span data-ttu-id="b0567-172">Porting Polygon Stipples</span><span class="sxs-lookup"><span data-stu-id="b0567-172">Porting Polygon Stipples</span></span>

<span data-ttu-id="b0567-173">Quando si esegue il porting degli stipple poligoni IRIS GL, tenere presenti i punti seguenti:</span><span class="sxs-lookup"><span data-stu-id="b0567-173">When porting IRIS GL polygon stipples, keep the following points in mind:</span></span>

-   <span data-ttu-id="b0567-174">OpenGL non usa tabelle per gli stipples poligonali. viene mantenuto un solo modello di punta.</span><span class="sxs-lookup"><span data-stu-id="b0567-174">OpenGL doesn't use tables for polygon stipples; only one stipple pattern is kept.</span></span> <span data-ttu-id="b0567-175">È possibile usare elenchi di visualizzazione per archiviare modelli di stili diversi.</span><span class="sxs-lookup"><span data-stu-id="b0567-175">You can use display lists to store different stipple patterns.</span></span>
-   <span data-ttu-id="b0567-176">La dimensione della bitmap dello stipple poligono OpenGL è sempre un modello a 32x32 bit.</span><span class="sxs-lookup"><span data-stu-id="b0567-176">The OpenGL polygon stipple bitmap size is always a 32x32 bit pattern.</span></span>
-   <span data-ttu-id="b0567-177">La codifica Stipple è interessata [**da glPixelStore**](glpixelstore-functions.md).</span><span class="sxs-lookup"><span data-stu-id="b0567-177">Stipple encoding is affected by [**glPixelStore**](glpixelstore-functions.md).</span></span>

<span data-ttu-id="b0567-178">Per altre informazioni sul porting degli stipples poligoni, vedere Porting Pixel Operations ( [Porting Pixel Operations](porting-pixel-operations.md)).</span><span class="sxs-lookup"><span data-stu-id="b0567-178">For more information on porting polygon stipples, see [Porting Pixel Operations](porting-pixel-operations.md).</span></span>

<span data-ttu-id="b0567-179">Nella tabella seguente sono elencate le funzioni di punta del poligono IRIS GL e le funzioni OpenGL equivalenti.</span><span class="sxs-lookup"><span data-stu-id="b0567-179">The following table lists IRIS GL polygon stipple functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="b0567-180">Funzione GL IRIS</span><span class="sxs-lookup"><span data-stu-id="b0567-180">IRIS GL function</span></span> | <span data-ttu-id="b0567-181">Funzione OpenGL</span><span class="sxs-lookup"><span data-stu-id="b0567-181">OpenGL function</span></span>                                    | <span data-ttu-id="b0567-182">Significato</span><span class="sxs-lookup"><span data-stu-id="b0567-182">Meaning</span></span>                                               |
|------------------|----------------------------------------------------|-------------------------------------------------------|
| <span data-ttu-id="b0567-183">**defpattern**</span><span class="sxs-lookup"><span data-stu-id="b0567-183">**defpattern**</span></span>   | [<span data-ttu-id="b0567-184">**glPolygonStipple**</span><span class="sxs-lookup"><span data-stu-id="b0567-184">**glPolygonStipple**</span></span>](glpolygonstipple.md)       | <span data-ttu-id="b0567-185">Imposta il modello di stipla.</span><span class="sxs-lookup"><span data-stu-id="b0567-185">Sets the stipple pattern.</span></span>                             |
| <span data-ttu-id="b0567-186">**setpattern**</span><span class="sxs-lookup"><span data-stu-id="b0567-186">**setpattern**</span></span>   |                                                    | <span data-ttu-id="b0567-187">OpenGL mantiene un solo motivo a punta poligono.</span><span class="sxs-lookup"><span data-stu-id="b0567-187">OpenGL keeps only one polygon stipple pattern.</span></span>        |
| <span data-ttu-id="b0567-188">**Getpattern**</span><span class="sxs-lookup"><span data-stu-id="b0567-188">**getpattern**</span></span>   | [<span data-ttu-id="b0567-189">**glGetPolygonStipple**</span><span class="sxs-lookup"><span data-stu-id="b0567-189">**glGetPolygonStipple**</span></span>](glgetpolygonstipple.md) | <span data-ttu-id="b0567-190">Restituisce la bitmap stipple (usata per restituire un indice).</span><span class="sxs-lookup"><span data-stu-id="b0567-190">Returns the stipple bitmap (used to return an index).</span></span> |



 

<span data-ttu-id="b0567-191">In OpenGL si abilita e disabilita lo stippling dei poligoni passando GL POLYGON STIPPLE come parametro \_ \_ per [**glEnable**](glenable.md) e [**glDisable.**](gldisable.md)</span><span class="sxs-lookup"><span data-stu-id="b0567-191">In OpenGL, you enable and disable polygon stippling by passing GL\_POLYGON\_STIPPLE as a parameter for [**glEnable**](glenable.md) and [**glDisable**](gldisable.md).</span></span>

<span data-ttu-id="b0567-192">L'esempio di codice OpenGL seguente illustra lo stippling dei poligoni:</span><span class="sxs-lookup"><span data-stu-id="b0567-192">The following OpenGL code sample demonstrates polygon stippling:</span></span>


```C++
void display(void) 
{ 
    GLubyte fly[] = { 
      0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 
      0x03, 0x80, 0x01, 0xC0, 0x06, 0xC0, 0x03, 0x60, 
      0x04, 0x60, 0x06, 0x20, 0x04, 0x30, 0x0C, 0x20, 
      0x04, 0x18, 0x18, 0x20, 0x04, 0x0C, 0x30, 0x20, 
      0x04, 0x06, 0x60, 0x20, 0x44, 0x03, 0xC0, 0x22, 
      0x44, 0x01, 0x80, 0x22, 0x44, 0x01, 0x80, 0x22, 
      0x44, 0x01, 0x80, 0x22, 0x44, 0x01, 0x80, 0x22, 
      0x44, 0x01, 0x80, 0x22, 0x44, 0x01, 0x80, 0x22, 
      0x66, 0x01, 0x80, 0x66, 0x33, 0x01, 0x80, 0xCC, 
      0x19, 0x81, 0x81, 0x98, 0x0C, 0xC1, 0x83, 0x30, 
      0x07, 0xe1, 0x87, 0xe0, 0x03, 0x3f, 0xfc, 0xc0, 
      0x03, 0x31, 0x8c, 0xc0, 0x03, 0x33, 0xcc, 0xc0, 
      0x06, 0x64, 0x26, 0x60, 0x0c, 0xcc, 0x33, 0x30, 
      0x18, 0xcc, 0x33, 0x18, 0x10, 0xc4, 0x23, 0x08, 
      0x10, 0x63, 0xC6, 0x08, 0x10, 0x30, 0x0c, 0x08, 
      0x10, 0x18, 0x18, 0x08, 0x10, 0x00, 0x00, 0x08 
    }; 
    GLubyte halftone[] = { 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55 
    }; 
 
    glClear (GL_COLOR_BUFFER_BIT); 
 
/*  draw all polygons in white*/ 
    glColor3f (1.0, 1.0, 1.0); 
 
/*  draw one solid, unstippled rectangle,*/ 
/*  then two stippled rectangles*/ 
    glRectf (25.0, 25.0, 125.0, 125.0); 
    glEnable (GL_POLYGON_STIPPLE); 
    glPolygonStipple (fly); 
    glRectf (125.0, 25.0, 225.0, 125.0); 
    glPolygonStipple (halftone); 
    glRectf (225.0, 25.0, 325.0, 125.0); 
    glDisable (GL_POLYGON_STIPPLE); 
 
    glFlush (); 
}
```



## <a name="porting-tessellated-polygons"></a><span data-ttu-id="b0567-193">Portabilità di poligoni a tessellatura</span><span class="sxs-lookup"><span data-stu-id="b0567-193">Porting Tessellated Polygons</span></span>

<span data-ttu-id="b0567-194">In IRIS GL si usa **concave**(**TRUE**) e quindi **bgnpolygon** per disegnare poligoni concavi.</span><span class="sxs-lookup"><span data-stu-id="b0567-194">In IRIS GL, you use **concave**(**TRUE**) and then **bgnpolygon** to draw concave polygons.</span></span> <span data-ttu-id="b0567-195">OpenGL GLU include funzioni che è possibile usare per disegnare poligoni concavi.</span><span class="sxs-lookup"><span data-stu-id="b0567-195">The OpenGL GLU includes functions you can use to draw concave polygons.</span></span>

<span data-ttu-id="b0567-196">**Per disegnare un poligono concavo con OpenGL**</span><span class="sxs-lookup"><span data-stu-id="b0567-196">**To draw a concave polygon with OpenGL**</span></span>

1.  <span data-ttu-id="b0567-197">Creare un oggetto a tessellazione.</span><span class="sxs-lookup"><span data-stu-id="b0567-197">Create a tessellation object.</span></span>
2.  <span data-ttu-id="b0567-198">Definire i callback che verranno usati per elaborare i triangoli generati dal tessellatore.</span><span class="sxs-lookup"><span data-stu-id="b0567-198">Define callbacks that will be used to process the triangles generated by the tessellator.</span></span>
3.  <span data-ttu-id="b0567-199">Specificare il poligono concavo da a tessire.</span><span class="sxs-lookup"><span data-stu-id="b0567-199">Specify the concave polygon to be tessellated.</span></span>

<span data-ttu-id="b0567-200">Nella tabella seguente sono elencate le funzioni OpenGL per il disegno di poligoni a colonne.</span><span class="sxs-lookup"><span data-stu-id="b0567-200">The following table lists the OpenGL functions for drawing tessellated polygons.</span></span>



| <span data-ttu-id="b0567-201">Funzione GLU OpenGL</span><span class="sxs-lookup"><span data-stu-id="b0567-201">OpenGL GLU function</span></span>                        | <span data-ttu-id="b0567-202">Significato</span><span class="sxs-lookup"><span data-stu-id="b0567-202">Meaning</span></span>                                                            |
|--------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="b0567-203">**gluNewTess**</span><span class="sxs-lookup"><span data-stu-id="b0567-203">**gluNewTess**</span></span>](glunewtess.md)           | <span data-ttu-id="b0567-204">Crea un nuovo oggetto a tessellazione.</span><span class="sxs-lookup"><span data-stu-id="b0567-204">Creates a new tessellation object.</span></span>                                 |
| [<span data-ttu-id="b0567-205">**gluDeleteTess**</span><span class="sxs-lookup"><span data-stu-id="b0567-205">**gluDeleteTess**</span></span>](gludeletetess.md)     | <span data-ttu-id="b0567-206">Elimina un oggetto a tessellazione.</span><span class="sxs-lookup"><span data-stu-id="b0567-206">Deletes a tessellation object.</span></span>                                     |
| [<span data-ttu-id="b0567-207">*gluTessCallback*</span><span class="sxs-lookup"><span data-stu-id="b0567-207">*gluTessCallback*</span></span>](glutess.md)           |                                                                    |
| [<span data-ttu-id="b0567-208">**gluBeginPolygon**</span><span class="sxs-lookup"><span data-stu-id="b0567-208">**gluBeginPolygon**</span></span>](glubeginpolygon.md) | <span data-ttu-id="b0567-209">Avvia la specifica del poligono.</span><span class="sxs-lookup"><span data-stu-id="b0567-209">Begins the polygon specification.</span></span>                                  |
| [<span data-ttu-id="b0567-210">**gluTessVertex**</span><span class="sxs-lookup"><span data-stu-id="b0567-210">**gluTessVertex**</span></span>](glutessvertex.md)     | <span data-ttu-id="b0567-211">Specifica un vertice poligonale in un contorno.</span><span class="sxs-lookup"><span data-stu-id="b0567-211">Specifies a polygon vertex in a contour.</span></span>                           |
| [<span data-ttu-id="b0567-212">**gluNextContour**</span><span class="sxs-lookup"><span data-stu-id="b0567-212">**gluNextContour**</span></span>](glunextcontour.md)   | <span data-ttu-id="b0567-213">Indica che la serie successiva di vertici descrive un nuovo contorno.</span><span class="sxs-lookup"><span data-stu-id="b0567-213">Indicates that the next series of vertices describe a new contour.</span></span> |
| [<span data-ttu-id="b0567-214">**gluEndPolygon**</span><span class="sxs-lookup"><span data-stu-id="b0567-214">**gluEndPolygon**</span></span>](gluendpolygon.md)     | <span data-ttu-id="b0567-215">Termina la specifica del poligono.</span><span class="sxs-lookup"><span data-stu-id="b0567-215">Ends the polygon specification.</span></span>                                    |



 

 

 





