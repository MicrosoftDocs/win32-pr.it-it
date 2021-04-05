---
title: Porting di poligoni e quadrilateri
description: 'Quando si portano poligoni e quadrilateri, tenere presenti i seguenti aspetti:'
ms.assetid: 2b752437-caf9-4336-a906-d06b2aa8bb04
keywords:
- Porting di IRIS GL, quadrilateri
- porting da IRIS GL, quadrilateri
- porting in OpenGL da IRIS GL, quadrilateri
- Porting OpenGL da IRIS GL, quadrilateri
- funzioni di disegno, quadrilateri
- quadrilateri
- Porting di IRIS GL, poligoni
- porting da IRIS GL, poligoni
- porting in OpenGL da IRIS GL, poligoni
- Porting OpenGL da IRIS GL, poligoni
- funzioni di disegno, poligoni
- poligoni, porting da IRIS GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c95d654b101c5eeb86cfcc4ea342e8196b8749e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712502"
---
# <a name="porting-polygons-and-quadrilaterals"></a><span data-ttu-id="ff881-115">Porting di poligoni e quadrilateri</span><span class="sxs-lookup"><span data-stu-id="ff881-115">Porting Polygons and Quadrilaterals</span></span>

<span data-ttu-id="ff881-116">Quando si portano poligoni e quadrilateri, tenere presenti i seguenti aspetti:</span><span class="sxs-lookup"><span data-stu-id="ff881-116">Keep the following points in mind when porting polygons and quadrilaterals:</span></span>

-   <span data-ttu-id="ff881-117">Non esiste un equivalente diretto per **concavo**(**true**).</span><span class="sxs-lookup"><span data-stu-id="ff881-117">There is no direct equivalent for **concave**(**TRUE**).</span></span> <span data-ttu-id="ff881-118">È invece possibile usare le routine a mosaico in GLU, descritte in [poligoni tessellating](tessellating-polygons.md).</span><span class="sxs-lookup"><span data-stu-id="ff881-118">Instead you can use the tessellation routines in the GLU, described in [Tessellating Polygons](tessellating-polygons.md).</span></span>
-   <span data-ttu-id="ff881-119">Le modalità poligono sono impostate in modo diverso.</span><span class="sxs-lookup"><span data-stu-id="ff881-119">Polygon modes are set differently.</span></span>
-   <span data-ttu-id="ff881-120">Queste funzioni di disegno Polygon non hanno equivalenti diretti in OpenGL: la famiglia **Poly** di routine; famiglia di routine **POLF** . **PMV**, **PDR** e **PCLOS**; **rpmv** e **rpdr**; **splf**; e **spclos**.</span><span class="sxs-lookup"><span data-stu-id="ff881-120">These polygon drawing functions have no direct equivalents in OpenGL: the **poly** family of routines; the **polf** family of routines; **pmv**, **pdr**, and **pclos**; **rpmv** and **rpdr**; **splf**; and **spclos**.</span></span>

<span data-ttu-id="ff881-121">Se il codice di IRIS GL usa queste funzioni, sarà necessario riscrivere il codice usando [**glBegin**](glbegin.md)(GL \_ Polygon).</span><span class="sxs-lookup"><span data-stu-id="ff881-121">If your IRIS GL code uses these functions, you'll have to rewrite the code using [**glBegin**](glbegin.md)( GL\_POLYGON ).</span></span>

<span data-ttu-id="ff881-122">La tabella seguente elenca le funzioni di disegno del poligono IRIS GL e le relative funzioni OpenGL equivalenti.</span><span class="sxs-lookup"><span data-stu-id="ff881-122">The following table lists the IRIS GL polygon drawing functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="ff881-123">Funzione IRIS GL</span><span class="sxs-lookup"><span data-stu-id="ff881-123">IRIS GL function</span></span>         | <span data-ttu-id="ff881-124">OpenGL (funzione)</span><span class="sxs-lookup"><span data-stu-id="ff881-124">OpenGL function</span></span>                                                    | <span data-ttu-id="ff881-125">Significato</span><span class="sxs-lookup"><span data-stu-id="ff881-125">Meaning</span></span>                                                 |
|--------------------------|--------------------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="ff881-126">**bgnpolygonendpolygon**</span><span class="sxs-lookup"><span data-stu-id="ff881-126">**bgnpolygonendpolygon**</span></span> | <span data-ttu-id="ff881-127">[**glBegin**](glbegin.md) ( \_ poligono GL)[**glEnd**](glend.md)</span><span class="sxs-lookup"><span data-stu-id="ff881-127">[**glBegin**](glbegin.md) ( GL\_POLYGON )[**glEnd**](glend.md)</span></span>   | <span data-ttu-id="ff881-128">I vertici definiscono il limite di un poligono convesso semplice.</span><span class="sxs-lookup"><span data-stu-id="ff881-128">Vertices define boundary of a simple convex polygon.</span></span>    |
|                          | <span data-ttu-id="ff881-129">**glBegin**(GL \_ quad)**glEnd**</span><span class="sxs-lookup"><span data-stu-id="ff881-129">**glBegin**( GL\_QUADS )**glEnd**</span></span><br/>                       | <span data-ttu-id="ff881-130">Interpreta le quadruple dei vertici come quadrilateri.</span><span class="sxs-lookup"><span data-stu-id="ff881-130">Interprets quadruples of vertices as quadrilaterals.</span></span>    |
| <span data-ttu-id="ff881-131">**bgnqstripendqstrip**</span><span class="sxs-lookup"><span data-stu-id="ff881-131">**bgnqstripendqstrip**</span></span>   | <span data-ttu-id="ff881-132">[**glBegin**](glbegin.md) (GL \_ Quad \_ Strip)**glEnd**</span><span class="sxs-lookup"><span data-stu-id="ff881-132">[**glBegin**](glbegin.md) ( GL\_QUAD\_STRIP )**glEnd**</span></span><br/> | <span data-ttu-id="ff881-133">Interpreta i vertici come strisce collegate di quadrilateri.</span><span class="sxs-lookup"><span data-stu-id="ff881-133">Interprets vertices as linked strips of quadrilaterals.</span></span> |
|                          | [<span data-ttu-id="ff881-134">glEdgeFlag</span><span class="sxs-lookup"><span data-stu-id="ff881-134">glEdgeFlag</span></span>](gledgeflag-functions.md)                             |                                                         |
| <span data-ttu-id="ff881-135">**modalità multifunzione**</span><span class="sxs-lookup"><span data-stu-id="ff881-135">**polymode**</span></span>             | [<span data-ttu-id="ff881-136">**glPolygonMode**</span><span class="sxs-lookup"><span data-stu-id="ff881-136">**glPolygonMode**</span></span>](glpolygonmode.md)                             | <span data-ttu-id="ff881-137">Imposta la modalità di disegno poligono.</span><span class="sxs-lookup"><span data-stu-id="ff881-137">Sets polygon drawing mode.</span></span>                              |
| <span data-ttu-id="ff881-138">**rectrectf**</span><span class="sxs-lookup"><span data-stu-id="ff881-138">**rectrectf**</span></span><br/> | [<span data-ttu-id="ff881-139">glRect</span><span class="sxs-lookup"><span data-stu-id="ff881-139">glRect</span></span>](glrect-functions.md)                                     | <span data-ttu-id="ff881-140">Disegna un rettangolo.</span><span class="sxs-lookup"><span data-stu-id="ff881-140">Draws a rectangle.</span></span>                                      |
| <span data-ttu-id="ff881-141">**sboxsboxf**</span><span class="sxs-lookup"><span data-stu-id="ff881-141">**sboxsboxf**</span></span><br/> |                                                                    | <span data-ttu-id="ff881-142">Disegna un rettangolo allineato allo schermo.</span><span class="sxs-lookup"><span data-stu-id="ff881-142">Draws a screen-aligned rectangle.</span></span>                       |



 

<span data-ttu-id="ff881-143">??</span><span class="sxs-lookup"><span data-stu-id="ff881-143">??</span></span>

## <a name="porting-polygon-modes"></a><span data-ttu-id="ff881-144">Modalità poligono di porting</span><span class="sxs-lookup"><span data-stu-id="ff881-144">Porting Polygon Modes</span></span>

<span data-ttu-id="ff881-145">La funzione OpenGL [**glPolygonMode**](glpolygonmode.md) consente di specificare il lato di un poligono (back o front) a cui si applica la modalità.</span><span class="sxs-lookup"><span data-stu-id="ff881-145">The OpenGL function [**glPolygonMode**](glpolygonmode.md) lets you specify which side of a polygon (the back or the front) the mode applies to.</span></span> <span data-ttu-id="ff881-146">La relativa sintassi è la seguente:</span><span class="sxs-lookup"><span data-stu-id="ff881-146">Its syntax is:</span></span>

``` syntax
void glPolygonMode( GLenum face, GLenum mode ); 
 
```

<span data-ttu-id="ff881-147">dove Face è uno dei seguenti:</span><span class="sxs-lookup"><span data-stu-id="ff881-147">where face is one of:</span></span>



|                      |                                                            |
|----------------------|------------------------------------------------------------|
| <span data-ttu-id="ff881-148">\_primo piano GL</span><span class="sxs-lookup"><span data-stu-id="ff881-148">GL\_FRONT</span></span>            | <span data-ttu-id="ff881-149">modalità che si applica ai poligoni in primo piano</span><span class="sxs-lookup"><span data-stu-id="ff881-149">mode which applies to front-facing polygons</span></span>                |
| <span data-ttu-id="ff881-150">indietro per GL \_</span><span class="sxs-lookup"><span data-stu-id="ff881-150">GL\_BACK</span></span>             | <span data-ttu-id="ff881-151">modalità applicabile ai poligoni sottoposti a back-end</span><span class="sxs-lookup"><span data-stu-id="ff881-151">mode which applies to back-facing polygons</span></span>                 |
| <span data-ttu-id="ff881-152">\_primo \_ e \_ indietro GL</span><span class="sxs-lookup"><span data-stu-id="ff881-152">GL\_FRONT\_AND\_BACK</span></span> | <span data-ttu-id="ff881-153">modalità che si applica sia ai poligoni anteriori che al back-end</span><span class="sxs-lookup"><span data-stu-id="ff881-153">mode which applies to both front- and back-facing polygons</span></span> |



 

<span data-ttu-id="ff881-154">La \_ modalità Front \_ e \_ back GL è equivalente alla funzione di **polimodalità** di Iris GL.</span><span class="sxs-lookup"><span data-stu-id="ff881-154">The GL\_FRONT\_AND\_BACK mode is equivalent to the IRIS GL **polymode** function.</span></span> <span data-ttu-id="ff881-155">La tabella seguente elenca le modalità poligono di IRIS GL e le modalità OpenGL equivalenti.</span><span class="sxs-lookup"><span data-stu-id="ff881-155">The following table lists IRIS GL polygon modes and their equivalent OpenGL modes.</span></span>



| <span data-ttu-id="ff881-156">Modalità di IRIS GL</span><span class="sxs-lookup"><span data-stu-id="ff881-156">IRIS GL mode</span></span> | <span data-ttu-id="ff881-157">Modalità OpenGL</span><span class="sxs-lookup"><span data-stu-id="ff881-157">OpenGL mode</span></span> | <span data-ttu-id="ff881-158">Significato</span><span class="sxs-lookup"><span data-stu-id="ff881-158">Meaning</span></span>                                       |
|--------------|-------------|-----------------------------------------------|
| <span data-ttu-id="ff881-159">punto di PYM \_</span><span class="sxs-lookup"><span data-stu-id="ff881-159">PYM\_POINT</span></span>   | <span data-ttu-id="ff881-160">\_punto GL</span><span class="sxs-lookup"><span data-stu-id="ff881-160">GL\_POINT</span></span>   | <span data-ttu-id="ff881-161">Disegna i vertici come punti.</span><span class="sxs-lookup"><span data-stu-id="ff881-161">Draws vertices as points.</span></span>                     |
| <span data-ttu-id="ff881-162">\_linea Pym</span><span class="sxs-lookup"><span data-stu-id="ff881-162">PYM\_LINE</span></span>    | <span data-ttu-id="ff881-163">\_linea GL</span><span class="sxs-lookup"><span data-stu-id="ff881-163">GL\_LINE</span></span>    | <span data-ttu-id="ff881-164">Disegna i bordi del limite come segmenti di linea.</span><span class="sxs-lookup"><span data-stu-id="ff881-164">Draws boundary edges as line segments.</span></span>        |
| <span data-ttu-id="ff881-165">\_riempimento Pym</span><span class="sxs-lookup"><span data-stu-id="ff881-165">PYM\_FILL</span></span>    | <span data-ttu-id="ff881-166">\_riempimento GL</span><span class="sxs-lookup"><span data-stu-id="ff881-166">GL\_FILL</span></span>    | <span data-ttu-id="ff881-167">Disegna il riempimento interno del poligono.</span><span class="sxs-lookup"><span data-stu-id="ff881-167">Draws polygon interior filled.</span></span>                |
| <span data-ttu-id="ff881-168">PYM \_ Hollow</span><span class="sxs-lookup"><span data-stu-id="ff881-168">PYM\_HOLLOW</span></span>  |             | <span data-ttu-id="ff881-169">Riempie solo i pixel interni ai limiti.</span><span class="sxs-lookup"><span data-stu-id="ff881-169">Fills only interior pixels at the boundaries.</span></span> |



 

## <a name="porting-polygon-stipples"></a><span data-ttu-id="ff881-170">Porting poligono Stipples</span><span class="sxs-lookup"><span data-stu-id="ff881-170">Porting Polygon Stipples</span></span>

<span data-ttu-id="ff881-171">Quando si esegue il porting di IRIS GL Polygon stipples, tenere presente quanto segue:</span><span class="sxs-lookup"><span data-stu-id="ff881-171">When porting IRIS GL polygon stipples, keep the following points in mind:</span></span>

-   <span data-ttu-id="ff881-172">OpenGL non usa le tabelle per poligono stipples; viene mantenuto solo un modello stipple.</span><span class="sxs-lookup"><span data-stu-id="ff881-172">OpenGL doesn't use tables for polygon stipples; only one stipple pattern is kept.</span></span> <span data-ttu-id="ff881-173">È possibile usare gli elenchi di visualizzazione per archiviare modelli stipple diversi.</span><span class="sxs-lookup"><span data-stu-id="ff881-173">You can use display lists to store different stipple patterns.</span></span>
-   <span data-ttu-id="ff881-174">La dimensione bitmap stipple del poligono OpenGL è sempre un modello di bit 32x32.</span><span class="sxs-lookup"><span data-stu-id="ff881-174">The OpenGL polygon stipple bitmap size is always a 32x32 bit pattern.</span></span>
-   <span data-ttu-id="ff881-175">La codifica stipple è interessata da [**glPixelStore**](glpixelstore-functions.md).</span><span class="sxs-lookup"><span data-stu-id="ff881-175">Stipple encoding is affected by [**glPixelStore**](glpixelstore-functions.md).</span></span>

<span data-ttu-id="ff881-176">Per altre informazioni sul porting del poligono stipples, vedere [porting pixel Operations](porting-pixel-operations.md).</span><span class="sxs-lookup"><span data-stu-id="ff881-176">For more information on porting polygon stipples, see [Porting Pixel Operations](porting-pixel-operations.md).</span></span>

<span data-ttu-id="ff881-177">La tabella seguente elenca le funzioni stipple di IRIS GL Polygon e le relative funzioni OpenGL equivalenti.</span><span class="sxs-lookup"><span data-stu-id="ff881-177">The following table lists IRIS GL polygon stipple functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="ff881-178">Funzione IRIS GL</span><span class="sxs-lookup"><span data-stu-id="ff881-178">IRIS GL function</span></span> | <span data-ttu-id="ff881-179">OpenGL (funzione)</span><span class="sxs-lookup"><span data-stu-id="ff881-179">OpenGL function</span></span>                                    | <span data-ttu-id="ff881-180">Significato</span><span class="sxs-lookup"><span data-stu-id="ff881-180">Meaning</span></span>                                               |
|------------------|----------------------------------------------------|-------------------------------------------------------|
| <span data-ttu-id="ff881-181">**defpattern**</span><span class="sxs-lookup"><span data-stu-id="ff881-181">**defpattern**</span></span>   | [<span data-ttu-id="ff881-182">**glPolygonStipple**</span><span class="sxs-lookup"><span data-stu-id="ff881-182">**glPolygonStipple**</span></span>](glpolygonstipple.md)       | <span data-ttu-id="ff881-183">Imposta il pattern stipple.</span><span class="sxs-lookup"><span data-stu-id="ff881-183">Sets the stipple pattern.</span></span>                             |
| <span data-ttu-id="ff881-184">**criteri di ricerca**</span><span class="sxs-lookup"><span data-stu-id="ff881-184">**setpattern**</span></span>   |                                                    | <span data-ttu-id="ff881-185">OpenGL mantiene solo un modello stipple poligono.</span><span class="sxs-lookup"><span data-stu-id="ff881-185">OpenGL keeps only one polygon stipple pattern.</span></span>        |
| <span data-ttu-id="ff881-186">**GetPattern**</span><span class="sxs-lookup"><span data-stu-id="ff881-186">**getpattern**</span></span>   | [<span data-ttu-id="ff881-187">**glGetPolygonStipple**</span><span class="sxs-lookup"><span data-stu-id="ff881-187">**glGetPolygonStipple**</span></span>](glgetpolygonstipple.md) | <span data-ttu-id="ff881-188">Restituisce la bitmap stipple (utilizzata per restituire un indice).</span><span class="sxs-lookup"><span data-stu-id="ff881-188">Returns the stipple bitmap (used to return an index).</span></span> |



 

<span data-ttu-id="ff881-189">In OpenGL è possibile abilitare e disabilitare poligono punteggiatura passando GL \_ Polygon \_ stipple come parametro per [**glEnable**](glenable.md) e [**glDisable**](gldisable.md).</span><span class="sxs-lookup"><span data-stu-id="ff881-189">In OpenGL, you enable and disable polygon stippling by passing GL\_POLYGON\_STIPPLE as a parameter for [**glEnable**](glenable.md) and [**glDisable**](gldisable.md).</span></span>

<span data-ttu-id="ff881-190">Nell'esempio di codice OpenGL seguente viene illustrato il poligono punteggiatura:</span><span class="sxs-lookup"><span data-stu-id="ff881-190">The following OpenGL code sample demonstrates polygon stippling:</span></span>


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



## <a name="porting-tessellated-polygons"></a><span data-ttu-id="ff881-191">Porting di poligoni tassellati</span><span class="sxs-lookup"><span data-stu-id="ff881-191">Porting Tessellated Polygons</span></span>

<span data-ttu-id="ff881-192">In IRIS GL usare **concavo**(**true**) e quindi **bgnpolygon** per creare poligoni concavi.</span><span class="sxs-lookup"><span data-stu-id="ff881-192">In IRIS GL, you use **concave**(**TRUE**) and then **bgnpolygon** to draw concave polygons.</span></span> <span data-ttu-id="ff881-193">OpenGL GLU include funzioni che è possibile usare per creare poligoni concavi.</span><span class="sxs-lookup"><span data-stu-id="ff881-193">The OpenGL GLU includes functions you can use to draw concave polygons.</span></span>

<span data-ttu-id="ff881-194">**Per creare un poligono concavo con OpenGL**</span><span class="sxs-lookup"><span data-stu-id="ff881-194">**To draw a concave polygon with OpenGL**</span></span>

1.  <span data-ttu-id="ff881-195">Creare un oggetto a mosaico.</span><span class="sxs-lookup"><span data-stu-id="ff881-195">Create a tessellation object.</span></span>
2.  <span data-ttu-id="ff881-196">Definire callback che saranno usati per elaborare i triangoli generati da mosaico.</span><span class="sxs-lookup"><span data-stu-id="ff881-196">Define callbacks that will be used to process the triangles generated by the tessellator.</span></span>
3.  <span data-ttu-id="ff881-197">Specificare il Poligono concavo da tassellati.</span><span class="sxs-lookup"><span data-stu-id="ff881-197">Specify the concave polygon to be tessellated.</span></span>

<span data-ttu-id="ff881-198">La tabella seguente elenca le funzioni OpenGL per il disegno di poligoni tassellati.</span><span class="sxs-lookup"><span data-stu-id="ff881-198">The following table lists the OpenGL functions for drawing tessellated polygons.</span></span>



| <span data-ttu-id="ff881-199">Funzione OpenGL GLU</span><span class="sxs-lookup"><span data-stu-id="ff881-199">OpenGL GLU function</span></span>                        | <span data-ttu-id="ff881-200">Significato</span><span class="sxs-lookup"><span data-stu-id="ff881-200">Meaning</span></span>                                                            |
|--------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="ff881-201">**gluNewTess**</span><span class="sxs-lookup"><span data-stu-id="ff881-201">**gluNewTess**</span></span>](glunewtess.md)           | <span data-ttu-id="ff881-202">Crea un nuovo oggetto a mosaico.</span><span class="sxs-lookup"><span data-stu-id="ff881-202">Creates a new tessellation object.</span></span>                                 |
| [<span data-ttu-id="ff881-203">**gluDeleteTess**</span><span class="sxs-lookup"><span data-stu-id="ff881-203">**gluDeleteTess**</span></span>](gludeletetess.md)     | <span data-ttu-id="ff881-204">Elimina un oggetto a mosaico.</span><span class="sxs-lookup"><span data-stu-id="ff881-204">Deletes a tessellation object.</span></span>                                     |
| [<span data-ttu-id="ff881-205">*gluTessCallback*</span><span class="sxs-lookup"><span data-stu-id="ff881-205">*gluTessCallback*</span></span>](glutess.md)           |                                                                    |
| [<span data-ttu-id="ff881-206">**gluBeginPolygon**</span><span class="sxs-lookup"><span data-stu-id="ff881-206">**gluBeginPolygon**</span></span>](glubeginpolygon.md) | <span data-ttu-id="ff881-207">Inizia la specifica del poligono.</span><span class="sxs-lookup"><span data-stu-id="ff881-207">Begins the polygon specification.</span></span>                                  |
| [<span data-ttu-id="ff881-208">**gluTessVertex**</span><span class="sxs-lookup"><span data-stu-id="ff881-208">**gluTessVertex**</span></span>](glutessvertex.md)     | <span data-ttu-id="ff881-209">Specifica un vertice del poligono in un contorno.</span><span class="sxs-lookup"><span data-stu-id="ff881-209">Specifies a polygon vertex in a contour.</span></span>                           |
| [<span data-ttu-id="ff881-210">**gluNextContour**</span><span class="sxs-lookup"><span data-stu-id="ff881-210">**gluNextContour**</span></span>](glunextcontour.md)   | <span data-ttu-id="ff881-211">Indica che la serie successiva di vertici descrive un nuovo contorno.</span><span class="sxs-lookup"><span data-stu-id="ff881-211">Indicates that the next series of vertices describe a new contour.</span></span> |
| [<span data-ttu-id="ff881-212">**gluEndPolygon**</span><span class="sxs-lookup"><span data-stu-id="ff881-212">**gluEndPolygon**</span></span>](gluendpolygon.md)     | <span data-ttu-id="ff881-213">Termina la specifica del poligono.</span><span class="sxs-lookup"><span data-stu-id="ff881-213">Ends the polygon specification.</span></span>                                    |



 

 

 





