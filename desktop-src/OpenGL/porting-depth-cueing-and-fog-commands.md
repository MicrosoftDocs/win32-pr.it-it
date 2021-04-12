---
title: Porting di profondità e comandi di nebbia
description: Porting di profondità e comandi di nebbia
ms.assetid: 16982d11-88a1-4a35-960f-28f10491e0ac
keywords:
- Porting di IRIS GL, CUE Depth
- porting da IRIS GL, incue Depth
- porting in OpenGL da IRIS GL, incue Depth
- Porting OpenGL da IRIS GL, incue di profondità
- Porting di IRIS GL, nebbia
- porting da IRIS GL, Fog
- porting in OpenGL da IRIS GL, Fog
- Porting OpenGL da IRIS GL, nebbia
- Cue di profondità
- nebbia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fd9f65a29e0ae594bf9344cd960d3fc2b9aa646
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221824"
---
# <a name="porting-depth-cueing-and-fog-commands"></a><span data-ttu-id="8ba3a-113">Porting di profondità e comandi di nebbia</span><span class="sxs-lookup"><span data-stu-id="8ba3a-113">Porting Depth Cueing and Fog Commands</span></span>

<span data-ttu-id="8ba3a-114">Quando si esegue il porting dei comandi Depth-cue e Fog, tenere presente quanto segue:</span><span class="sxs-lookup"><span data-stu-id="8ba3a-114">When porting depth-cueing and fog commands, keep the following points in mind:</span></span>

-   <span data-ttu-id="8ba3a-115">La chiamata a IRIS GL, **fogvertex**, imposta una modalità e i parametri che interessano tale modalità.</span><span class="sxs-lookup"><span data-stu-id="8ba3a-115">The IRIS GL call, **fogvertex**, sets a mode and the parameters affecting that mode.</span></span> <span data-ttu-id="8ba3a-116">In OpenGL è possibile chiamare [**glFog**](glfog.md) una volta per impostare la modalità e quindi di nuovo due volte o più per impostare vari parametri.</span><span class="sxs-lookup"><span data-stu-id="8ba3a-116">In OpenGL, you call [**glFog**](glfog.md) once to set the mode, and then again twice or more to set various parameters.</span></span>
-   <span data-ttu-id="8ba3a-117">In OpenGL il ripasso della profondità non è una funzionalità separata.</span><span class="sxs-lookup"><span data-stu-id="8ba3a-117">In OpenGL, depth cueing is not a separate feature.</span></span> <span data-ttu-id="8ba3a-118">Utilizzare la nebbia lineare anziché il ripasso della profondità.</span><span class="sxs-lookup"><span data-stu-id="8ba3a-118">Use linear fog instead of depth cueing.</span></span> <span data-ttu-id="8ba3a-119">Questa sezione fornisce un esempio di come eseguire questa operazione. Le seguenti funzioni di IRIS GL non hanno un equivalente OpenGL diretto:</span><span class="sxs-lookup"><span data-stu-id="8ba3a-119">(This section gives an example of how to do this.) The following IRIS GL functions have no direct OpenGL equivalent:</span></span>

    <span data-ttu-id="8ba3a-120">**depthcue**</span><span class="sxs-lookup"><span data-stu-id="8ba3a-120">**depthcue**</span></span>

    <span data-ttu-id="8ba3a-121">**lRGBrange**</span><span class="sxs-lookup"><span data-stu-id="8ba3a-121">**lRGBrange**</span></span>

    <span data-ttu-id="8ba3a-122">**lshaderange**</span><span class="sxs-lookup"><span data-stu-id="8ba3a-122">**lshaderange**</span></span>

    <span data-ttu-id="8ba3a-123">**getdcm**</span><span class="sxs-lookup"><span data-stu-id="8ba3a-123">**getdcm**</span></span>

-   <span data-ttu-id="8ba3a-124">Per modificare la qualità di nebbia, usare [**glHint**](glhint.md)( \_ hint di nebbia GL \_ ).</span><span class="sxs-lookup"><span data-stu-id="8ba3a-124">To adjust fog quality, use [**glHint**](glhint.md)( GL\_FOG\_HINT ).</span></span>

<span data-ttu-id="8ba3a-125">La tabella seguente elenca le funzioni di IRIS GL per la gestione della nebbia e delle funzioni OpenGL equivalenti.</span><span class="sxs-lookup"><span data-stu-id="8ba3a-125">The following table lists the IRIS GL functions for managing fog and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="8ba3a-126">Funzione IRIS GL</span><span class="sxs-lookup"><span data-stu-id="8ba3a-126">IRIS GL function</span></span>         | <span data-ttu-id="8ba3a-127">OpenGL (funzione)</span><span class="sxs-lookup"><span data-stu-id="8ba3a-127">OpenGL function</span></span>                                     | <span data-ttu-id="8ba3a-128">Significato</span><span class="sxs-lookup"><span data-stu-id="8ba3a-128">Meaning</span></span>                           |
|--------------------------|-----------------------------------------------------|-----------------------------------|
| <span data-ttu-id="8ba3a-129">**fogvertex**</span><span class="sxs-lookup"><span data-stu-id="8ba3a-129">**fogvertex**</span></span>            | [<span data-ttu-id="8ba3a-130">**glFog**</span><span class="sxs-lookup"><span data-stu-id="8ba3a-130">**glFog**</span></span>](glfog.md)                              | <span data-ttu-id="8ba3a-131">Imposta vari parametri di nebbia.</span><span class="sxs-lookup"><span data-stu-id="8ba3a-131">Sets various fog parameters.</span></span>      |
| <span data-ttu-id="8ba3a-132">**fogvertex**(FG \_ su)</span><span class="sxs-lookup"><span data-stu-id="8ba3a-132">**fogvertex**( FG\_ON )</span></span>  | <span data-ttu-id="8ba3a-133">[**glEnable**](glenable.md) (GL \_ Fog)</span><span class="sxs-lookup"><span data-stu-id="8ba3a-133">[**glEnable**](glenable.md) ( GL\_FOG )</span></span>            | <span data-ttu-id="8ba3a-134">Attiva la nebbia.</span><span class="sxs-lookup"><span data-stu-id="8ba3a-134">Turns on fog.</span></span>                     |
| <span data-ttu-id="8ba3a-135">**fogvertex**(FG \_ disattivato)</span><span class="sxs-lookup"><span data-stu-id="8ba3a-135">**fogvertex**( FG\_OFF )</span></span> | <span data-ttu-id="8ba3a-136">[**glDisable**](gldisable.md) (GL \_ Fog)</span><span class="sxs-lookup"><span data-stu-id="8ba3a-136">[**glDisable**](gldisable.md) ( GL\_FOG )</span></span>          | <span data-ttu-id="8ba3a-137">Disattiva la nebbia.</span><span class="sxs-lookup"><span data-stu-id="8ba3a-137">Turns off fog.</span></span>                    |
| <span data-ttu-id="8ba3a-138">**depthcue**</span><span class="sxs-lookup"><span data-stu-id="8ba3a-138">**depthcue**</span></span>             | <span data-ttu-id="8ba3a-139">[**glFog**](glfog.md) (GL \_ Fog \_ mod, GL \_ lineare)</span><span class="sxs-lookup"><span data-stu-id="8ba3a-139">[**glFog**](glfog.md) ( GL\_FOG\_MOD, GL\_LINEAR )</span></span> | <span data-ttu-id="8ba3a-140">Usa la nebbia lineare per il ripasso della profondità.</span><span class="sxs-lookup"><span data-stu-id="8ba3a-140">Uses linear fog for depth cueing.</span></span> |



 

<span data-ttu-id="8ba3a-141">La tabella seguente elenca i parametri che è possibile passare a **glFog**.</span><span class="sxs-lookup"><span data-stu-id="8ba3a-141">The following table lists the parameters you can pass to **glFog**.</span></span>



| <span data-ttu-id="8ba3a-142">Parametro Fog</span><span class="sxs-lookup"><span data-stu-id="8ba3a-142">Fog parameter</span></span>    | <span data-ttu-id="8ba3a-143">Significato</span><span class="sxs-lookup"><span data-stu-id="8ba3a-143">Meaning</span></span>                       | <span data-ttu-id="8ba3a-144">Predefinito</span><span class="sxs-lookup"><span data-stu-id="8ba3a-144">Default</span></span>                  |
|------------------|-------------------------------|--------------------------|
| <span data-ttu-id="8ba3a-145">\_densità di nebbia GL \_</span><span class="sxs-lookup"><span data-stu-id="8ba3a-145">GL\_FOG\_DENSITY</span></span> | <span data-ttu-id="8ba3a-146">Densità di nebbia.</span><span class="sxs-lookup"><span data-stu-id="8ba3a-146">Fog density.</span></span>                  | <span data-ttu-id="8ba3a-147">1.0</span><span class="sxs-lookup"><span data-stu-id="8ba3a-147">1.0</span></span>                      |
| <span data-ttu-id="8ba3a-148">\_inizio di nebbia GL \_</span><span class="sxs-lookup"><span data-stu-id="8ba3a-148">GL\_FOG\_START</span></span>   | <span data-ttu-id="8ba3a-149">Near distance per la nebbia lineare.</span><span class="sxs-lookup"><span data-stu-id="8ba3a-149">Near distance for linear fog.</span></span> | <span data-ttu-id="8ba3a-150">0,0</span><span class="sxs-lookup"><span data-stu-id="8ba3a-150">0.0</span></span>                      |
| <span data-ttu-id="8ba3a-151">\_fine nebbia \_ GL</span><span class="sxs-lookup"><span data-stu-id="8ba3a-151">GL\_FOG\_END</span></span>     | <span data-ttu-id="8ba3a-152">Distanza per la nebbia lineare.</span><span class="sxs-lookup"><span data-stu-id="8ba3a-152">Far distance for linear fog.</span></span>  | <span data-ttu-id="8ba3a-153">1.0</span><span class="sxs-lookup"><span data-stu-id="8ba3a-153">1.0</span></span>                      |
| <span data-ttu-id="8ba3a-154">\_indice di nebbia GL \_</span><span class="sxs-lookup"><span data-stu-id="8ba3a-154">GL\_FOG\_INDEX</span></span>   | <span data-ttu-id="8ba3a-155">Indice colori nebbia.</span><span class="sxs-lookup"><span data-stu-id="8ba3a-155">Fog color index.</span></span>              | <span data-ttu-id="8ba3a-156">0,0</span><span class="sxs-lookup"><span data-stu-id="8ba3a-156">0.0</span></span>                      |
| <span data-ttu-id="8ba3a-157">\_colore di nebbia GL \_</span><span class="sxs-lookup"><span data-stu-id="8ba3a-157">GL\_FOG\_COLOR</span></span>   | <span data-ttu-id="8ba3a-158">Colore RGBA nebbia.</span><span class="sxs-lookup"><span data-stu-id="8ba3a-158">Fog RGBA color.</span></span>               | <span data-ttu-id="8ba3a-159">(0, 0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="8ba3a-159">(0, 0, 0, 0)</span></span>             |
| <span data-ttu-id="8ba3a-160">\_modalità di nebbia GL \_</span><span class="sxs-lookup"><span data-stu-id="8ba3a-160">GL\_FOG\_MODE</span></span>    | <span data-ttu-id="8ba3a-161">Modalità nebbia.</span><span class="sxs-lookup"><span data-stu-id="8ba3a-161">Fog mode.</span></span>                     | <span data-ttu-id="8ba3a-162">Vedere la tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="8ba3a-162">See the following table.</span></span> |



 

<span data-ttu-id="8ba3a-163">Il parametro di densità della nebbia di OpenGL è diverso da quello in IRIS GL.</span><span class="sxs-lookup"><span data-stu-id="8ba3a-163">The fog-density parameter of OpenGL differs from the one in IRIS GL.</span></span> <span data-ttu-id="8ba3a-164">Sono correlate come segue:</span><span class="sxs-lookup"><span data-stu-id="8ba3a-164">They are related as follows:</span></span>

-   <span data-ttu-id="8ba3a-165">Se *fogMode* = exp2</span><span class="sxs-lookup"><span data-stu-id="8ba3a-165">if *fogMode* = EXP2</span></span>
     

    <span data-ttu-id="8ba3a-166">*openGLfogDensity* = (*irisGLfogDensity* ) ( **Sqrt** ( **log** (1/255)))</span><span class="sxs-lookup"><span data-stu-id="8ba3a-166">*openGLfogDensity* = (*irisGLfogDensity* ) ( **sqrt** ( **log** ( 1 / 255 ) ))</span></span>
-   <span data-ttu-id="8ba3a-167">Se *fogMode* = exp</span><span class="sxs-lookup"><span data-stu-id="8ba3a-167">if *fogMode* = EXP</span></span>
     

    <span data-ttu-id="8ba3a-168">*openGLfogDensity* = (*irisGLfogDensity* ) ( **log** (1/255))</span><span class="sxs-lookup"><span data-stu-id="8ba3a-168">*openGLfogDensity* = (*irisGLfogDensity* ) ( **log** ( 1 / 255 ) )</span></span>

<span data-ttu-id="8ba3a-169">dove **Sqrt** è l'operazione radice quadrata, **log** è il logaritmo naturale, *irisGLfogDensity* è la densità di nebbia di Iris GL e *OpenGLfogDensity* è la densità di nebbia di OpenGL.</span><span class="sxs-lookup"><span data-stu-id="8ba3a-169">where **sqrt** is the square root operation, **log** is the natural logarithm, *irisGLfogDensity* is the IRIS GL fog density, and *openGLfogDensity* is the OpenGL fog density.</span></span>

<span data-ttu-id="8ba3a-170">Per passare da una modalità all'altra in modalità per pixel e per ogni vertice, utilizzare [**glHint**](glhint.md)(GL \_ Fog \_ hint, *hintMode*).</span><span class="sxs-lookup"><span data-stu-id="8ba3a-170">To switch between calculating fog in per-pixel mode and per-vertex mode, use [**glHint**](glhint.md)( GL\_FOG\_HINT, *hintMode*).</span></span> <span data-ttu-id="8ba3a-171">Sono disponibili due modalità di suggerimento:</span><span class="sxs-lookup"><span data-stu-id="8ba3a-171">Two hint modes are available:</span></span>

-   <span data-ttu-id="8ba3a-172">\_Calcolo della nebbia per pixel più gradevole</span><span class="sxs-lookup"><span data-stu-id="8ba3a-172">GL\_NICEST per-pixel fog calculation</span></span>
-   <span data-ttu-id="8ba3a-173">\_Calcolo della nebbia più veloce per vertice di GL</span><span class="sxs-lookup"><span data-stu-id="8ba3a-173">GL\_FASTEST per-vertex fog calculation</span></span>

<span data-ttu-id="8ba3a-174">La tabella seguente elenca le modalità di nebbia di IRIS GL e i rispettivi equivalenti di OpenGL.</span><span class="sxs-lookup"><span data-stu-id="8ba3a-174">The following table lists the IRIS GL fog modes and their OpenGL equivalents.</span></span>



| <span data-ttu-id="8ba3a-175">Modalità di nebbia di IRIS GL</span><span class="sxs-lookup"><span data-stu-id="8ba3a-175">IRIS GL fog mode</span></span>                       | <span data-ttu-id="8ba3a-176">Modalità nebbia di OpenGL</span><span class="sxs-lookup"><span data-stu-id="8ba3a-176">OpenGL fog mode</span></span> | <span data-ttu-id="8ba3a-177">Modalità hint</span><span class="sxs-lookup"><span data-stu-id="8ba3a-177">Hint mode</span></span>                         | <span data-ttu-id="8ba3a-178">Significato</span><span class="sxs-lookup"><span data-stu-id="8ba3a-178">Meaning</span></span>                                  |
|----------------------------------------|-----------------|-----------------------------------|------------------------------------------|
| <span data-ttu-id="8ba3a-179">FG \_ VTX \_ Exp, FG \_ pix \_ Exp</span><span class="sxs-lookup"><span data-stu-id="8ba3a-179">FG\_VTX\_EXP,FG\_PIX\_EXP</span></span><br/>   | <span data-ttu-id="8ba3a-180">\_Exp GL</span><span class="sxs-lookup"><span data-stu-id="8ba3a-180">GL\_EXP</span></span>         | <span data-ttu-id="8ba3a-181">GL più \_ veloce, GL più \_ bello</span><span class="sxs-lookup"><span data-stu-id="8ba3a-181">GL\_FASTEST,GL\_NICEST</span></span><br/> | <span data-ttu-id="8ba3a-182">Modalità di nebbia intensa (impostazione predefinita).</span><span class="sxs-lookup"><span data-stu-id="8ba3a-182">Heavy fog mode (default).</span></span>                |
| <span data-ttu-id="8ba3a-183">FG \_ VTX \_ exp2, FG \_ pix \_ exp2</span><span class="sxs-lookup"><span data-stu-id="8ba3a-183">FG\_VTX\_EXP2,FG\_PIX\_EXP2</span></span><br/> | <span data-ttu-id="8ba3a-184">\_Exp2 GL</span><span class="sxs-lookup"><span data-stu-id="8ba3a-184">GL\_EXP2</span></span>        | <span data-ttu-id="8ba3a-185">GL più \_ veloce, GL più \_ bello</span><span class="sxs-lookup"><span data-stu-id="8ba3a-185">GL\_FASTEST,GL\_NICEST</span></span><br/> | <span data-ttu-id="8ba3a-186">Modalità Haze.</span><span class="sxs-lookup"><span data-stu-id="8ba3a-186">Haze mode.</span></span>                               |
| <span data-ttu-id="8ba3a-187">FG \_ VTX \_ Lin, FG \_ pix \_ Lin</span><span class="sxs-lookup"><span data-stu-id="8ba3a-187">FG\_VTX\_LIN,FG\_PIX\_LIN</span></span><br/>   | <span data-ttu-id="8ba3a-188">\_linea GL</span><span class="sxs-lookup"><span data-stu-id="8ba3a-188">GL\_LINEAR</span></span>      | <span data-ttu-id="8ba3a-189">GL più \_ veloce, GL più \_ bello</span><span class="sxs-lookup"><span data-stu-id="8ba3a-189">GL\_FASTEST,GL\_NICEST</span></span><br/> | <span data-ttu-id="8ba3a-190">Modalità nebbia lineare.</span><span class="sxs-lookup"><span data-stu-id="8ba3a-190">Linear fog mode.</span></span> <span data-ttu-id="8ba3a-191">(Usare per il ripasso della profondità).</span><span class="sxs-lookup"><span data-stu-id="8ba3a-191">(Use for depth cueing.)</span></span> |



 

<span data-ttu-id="8ba3a-192">Nell'esempio di codice riportato di seguito viene illustrata la profondità in OpenGL:</span><span class="sxs-lookup"><span data-stu-id="8ba3a-192">The following code example demonstrates depth cueing in OpenGL:</span></span>


```C++
/* 
 *  depthcue.c 
 *  This program draws a wire frame model, which uses 
 *  intensity (brightness) to give clues to distance 
 *  Fog is used to achieve this effect 
 */ 
#include <GL/gl.h> 
#include <GL/glu.h> 
#include "aux.h" 
 
/*  Initialize linear fog for depth cueing 
 */ 
void myinit(void) 
{ 
    GLfloat fogColor[4] = {0.0, 0.0, 0.0, 1.0}; 
 
    glEnable(GL_FOG); 
    glFogi (GL_FOG_MODE, GL_LINEAR); 
    glHint (GL_FOG_HINT, GL_NICEST);  /*  per pixel  */ 
    glFogf (GL_FOG_START, 3.0); 
    glFogf (GL_FOG_END, 5.0); 
    glFogfv (GL_FOG_COLOR, fogColor); 
    glClearColor(0.0, 0.0, 0.0, 1.0); 
 
    glDepthFunc(GL_LEQUAL); 
    glEnable(GL_DEPTH_TEST); 
    glShadeModel(GL_FLAT); 
} 
 
/*  display() draws an icosahedron 
 */ 
void display(void) 
{ 
    glClear(GL_COLOR_BUFFER_BIT | GL_DEPTH_BUFFER_BIT); 
    glColor3f (1.0, 1.0, 1.0); 
    auxWireIcosahedron(1.0); 
    glFlush(); 
} 
 
void myReshape(GLsizei w, GLsizei h) 
{ 
    glViewport(0, 0, w, h); 
    glMatrixMode(GL_PROJECTION); 
    glLoadIdentity(); 
    gluPerspective (45.0, (GLfloat) w/(GLfloat) h, 3.0, 5.0); 
    glMatrixMode(GL_MODELVIEW); 
    glLoadIdentity (); 
    glTranslatef (0.0, 0.0, -4.0); /*move object into view*/ 
} 
/*  Main Loop 
 */ 
int main(int argc, char** argv) 
{ 
    auxInitDisplayMode (AUX_SINGLE | AUX_RGBA | AUX_DEPTH); 
    auxInitPosition (0, 0, 400, 400); 
    auxInitWindow (argv[0]); 
    myinit(); 
    auxReshapeFunc (myReshape); 
    auxMainLoop(display); 
}
```



 

 





