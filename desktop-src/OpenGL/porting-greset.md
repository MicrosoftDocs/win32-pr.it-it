---
title: Portabilità del porting
description: OpenGL sostituisce la funzione IRIS GL, il Grest, con le funzioni glPushAttrib e glPopAttrib.
ms.assetid: 348e8b18-4f12-45d1-a4d2-6533a983236b
keywords:
- Porting di IRIS GL, variabili di stato
- porting da IRIS GL, variabili di stato
- porting in OpenGL da IRIS GL, variabili di stato
- Porting OpenGL da IRIS GL, variabili di stato
- variabili di stato
- Porting di IRIS GL, funzione Grest
- porting da IRIS GL, funzione Grest
- porting in OpenGL da IRIS GL, funzione Grest
- Porting OpenGL da IRIS GL, funzione Grest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 078482f47dcaf7fd5f84605e2e0fa32d0cf14729
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396346"
---
# <a name="porting-greset"></a><span data-ttu-id="9dcad-112">Portabilità del porting</span><span class="sxs-lookup"><span data-stu-id="9dcad-112">Porting greset</span></span>

<span data-ttu-id="9dcad-113">OpenGL sostituisce la funzione IRIS GL, il **Grest**, con le funzioni [**glPushAttrib**](glpushattrib.md) e [**glPopAttrib**](glpopattrib.md).</span><span class="sxs-lookup"><span data-stu-id="9dcad-113">OpenGL replaces the IRIS GL function, **greset**, with the functions, [**glPushAttrib**](glpushattrib.md) and [**glPopAttrib**](glpopattrib.md).</span></span> <span data-ttu-id="9dcad-114">Usare queste funzioni per salvare e ripristinare i gruppi di variabili di stato.</span><span class="sxs-lookup"><span data-stu-id="9dcad-114">Use these functions to save and restore groups of state variables.</span></span> <span data-ttu-id="9dcad-115">Ad esempio,</span><span class="sxs-lookup"><span data-stu-id="9dcad-115">For example,</span></span>

``` syntax
void glPushAttrib( GLbitfield mask );
```

<span data-ttu-id="9dcad-116">Questo esempio accetta un operatore OR bit per bit di costanti simboliche, che indica i gruppi di variabili di stato da inserire nello stack di attributi.</span><span class="sxs-lookup"><span data-stu-id="9dcad-116">This example takes a bitwise OR of symbolic constants, indicating which groups of state variables to push onto an attribute stack.</span></span> <span data-ttu-id="9dcad-117">Ogni costante fa riferimento a un gruppo di variabili di stato.</span><span class="sxs-lookup"><span data-stu-id="9dcad-117">Each constant refers to a group of state variables.</span></span> <span data-ttu-id="9dcad-118">Nella tabella seguente vengono illustrati i gruppi di attributi con i nomi di costanti simbolici equivalenti.</span><span class="sxs-lookup"><span data-stu-id="9dcad-118">The following table shows the attribute groups with their equivalent symbolic constant names.</span></span> <span data-ttu-id="9dcad-119">Per un elenco completo delle variabili di stato OpenGL associate a ogni costante, vedere [**glPushAttrib**](glpushattrib.md).</span><span class="sxs-lookup"><span data-stu-id="9dcad-119">For a complete list of the OpenGL state variables associated with each constant, see [**glPushAttrib**](glpushattrib.md).</span></span>



| <span data-ttu-id="9dcad-120">Attributo</span><span class="sxs-lookup"><span data-stu-id="9dcad-120">Attribute</span></span>                       | <span data-ttu-id="9dcad-121">Costante</span><span class="sxs-lookup"><span data-stu-id="9dcad-121">Constant</span></span>                  |
|---------------------------------|---------------------------|
| <span data-ttu-id="9dcad-122">valore Clear buffer accumulo</span><span class="sxs-lookup"><span data-stu-id="9dcad-122">accumulation buffer clear value</span></span> | <span data-ttu-id="9dcad-123">\_bit del buffer di accut GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="9dcad-123">GL\_ACCUM\_BUFFER\_BIT</span></span>    |
| <span data-ttu-id="9dcad-124">buffer dei colori</span><span class="sxs-lookup"><span data-stu-id="9dcad-124">color buffer</span></span>                    | <span data-ttu-id="9dcad-125">\_bit del \_ buffer dei colori GL \_</span><span class="sxs-lookup"><span data-stu-id="9dcad-125">GL\_COLOR\_BUFFER\_BIT</span></span>    |
| <span data-ttu-id="9dcad-126">corrente</span><span class="sxs-lookup"><span data-stu-id="9dcad-126">current</span></span>                         | <span data-ttu-id="9dcad-127">\_bit corrente \_ GL</span><span class="sxs-lookup"><span data-stu-id="9dcad-127">GL\_CURRENT\_BIT</span></span>          |
| <span data-ttu-id="9dcad-128">buffer profondità</span><span class="sxs-lookup"><span data-stu-id="9dcad-128">depth buffer</span></span>                    | <span data-ttu-id="9dcad-129">\_ \_ bit buffer di profondità GL \_</span><span class="sxs-lookup"><span data-stu-id="9dcad-129">GL\_DEPTH\_BUFFER\_BIT</span></span>    |
| <span data-ttu-id="9dcad-130">abilitare</span><span class="sxs-lookup"><span data-stu-id="9dcad-130">enable</span></span>                          | <span data-ttu-id="9dcad-131">\_bit di abilitazione GL \_</span><span class="sxs-lookup"><span data-stu-id="9dcad-131">GL\_ENABLE\_BIT</span></span>           |
| <span data-ttu-id="9dcad-132">analizzatori</span><span class="sxs-lookup"><span data-stu-id="9dcad-132">evaluators</span></span>                      | <span data-ttu-id="9dcad-133">EGL \_ Val \_ bit</span><span class="sxs-lookup"><span data-stu-id="9dcad-133">EGL\_VAL\_BIT</span></span>             |
| <span data-ttu-id="9dcad-134">nebbia</span><span class="sxs-lookup"><span data-stu-id="9dcad-134">fog</span></span>                             | <span data-ttu-id="9dcad-135">\_bit di nebbia GL \_</span><span class="sxs-lookup"><span data-stu-id="9dcad-135">GL\_FOG\_BIT</span></span>              |
| <span data-ttu-id="9dcad-136">\_ \_ Impostazione base elenco GL</span><span class="sxs-lookup"><span data-stu-id="9dcad-136">GL\_LIST\_BASE setting</span></span>          | <span data-ttu-id="9dcad-137">\_bit elenco \_ GL</span><span class="sxs-lookup"><span data-stu-id="9dcad-137">GL\_LIST\_BIT</span></span>             |
| <span data-ttu-id="9dcad-138">variabili hint</span><span class="sxs-lookup"><span data-stu-id="9dcad-138">hint variables</span></span>                  | <span data-ttu-id="9dcad-139">\_bit suggerimento \_ GL</span><span class="sxs-lookup"><span data-stu-id="9dcad-139">GL\_HINT\_BIT</span></span>             |
| <span data-ttu-id="9dcad-140">variabili di illuminazione</span><span class="sxs-lookup"><span data-stu-id="9dcad-140">lighting variables</span></span>              | <span data-ttu-id="9dcad-141">\_bit di illuminazione GL \_</span><span class="sxs-lookup"><span data-stu-id="9dcad-141">GL\_LIGHTING\_BIT</span></span>         |
| <span data-ttu-id="9dcad-142">modalità di disegno linea</span><span class="sxs-lookup"><span data-stu-id="9dcad-142">line drawing mode</span></span>               | <span data-ttu-id="9dcad-143">\_bit linea \_ GL</span><span class="sxs-lookup"><span data-stu-id="9dcad-143">GL\_LINE\_BIT</span></span>             |
| <span data-ttu-id="9dcad-144">variabili in modalità pixel</span><span class="sxs-lookup"><span data-stu-id="9dcad-144">pixel mode variables</span></span>            | <span data-ttu-id="9dcad-145">\_bit in \_ modalità GL pixel \_</span><span class="sxs-lookup"><span data-stu-id="9dcad-145">GL\_PIXEL\_MODE\_BIT</span></span>      |
| <span data-ttu-id="9dcad-146">variabili punto</span><span class="sxs-lookup"><span data-stu-id="9dcad-146">point variables</span></span>                 | <span data-ttu-id="9dcad-147">\_bit punto \_ GL</span><span class="sxs-lookup"><span data-stu-id="9dcad-147">GL\_POINT\_BIT</span></span>            |
| <span data-ttu-id="9dcad-148">polygon</span><span class="sxs-lookup"><span data-stu-id="9dcad-148">polygon</span></span>                         | <span data-ttu-id="9dcad-149">\_bit poligono GL \_</span><span class="sxs-lookup"><span data-stu-id="9dcad-149">GL\_POLYGON\_BIT</span></span>          |
| <span data-ttu-id="9dcad-150">poligono stipple</span><span class="sxs-lookup"><span data-stu-id="9dcad-150">polygon stipple</span></span>                 | <span data-ttu-id="9dcad-151">\_bit stipple poligono GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="9dcad-151">GL\_POLYGON\_STIPPLE\_BIT</span></span> |
| <span data-ttu-id="9dcad-152">ritaglio</span><span class="sxs-lookup"><span data-stu-id="9dcad-152">scissor</span></span>                         | <span data-ttu-id="9dcad-153">\_bit a forbice GL \_</span><span class="sxs-lookup"><span data-stu-id="9dcad-153">GL\_SCISSOR\_BIT</span></span>          |
| <span data-ttu-id="9dcad-154">buffer stencil</span><span class="sxs-lookup"><span data-stu-id="9dcad-154">stencil buffer</span></span>                  | <span data-ttu-id="9dcad-155">\_ \_ bit buffer dello stencil GL \_</span><span class="sxs-lookup"><span data-stu-id="9dcad-155">GL\_STENCIL\_BUFFER\_BIT</span></span>  |
| <span data-ttu-id="9dcad-156">trama</span><span class="sxs-lookup"><span data-stu-id="9dcad-156">texture</span></span>                         | <span data-ttu-id="9dcad-157">\_bit trama \_ GL</span><span class="sxs-lookup"><span data-stu-id="9dcad-157">GL\_TEXTURE\_BIT</span></span>          |
| <span data-ttu-id="9dcad-158">trasformazione</span><span class="sxs-lookup"><span data-stu-id="9dcad-158">transform</span></span>                       | <span data-ttu-id="9dcad-159">\_bit di trasformazione GL \_</span><span class="sxs-lookup"><span data-stu-id="9dcad-159">GL\_TRANSFORM\_BIT</span></span>        |
| <span data-ttu-id="9dcad-160">riquadro di visualizzazione</span><span class="sxs-lookup"><span data-stu-id="9dcad-160">viewport</span></span>                        | <span data-ttu-id="9dcad-161">\_bit del viewport GL \_</span><span class="sxs-lookup"><span data-stu-id="9dcad-161">GL\_VIEWPORT\_BIT</span></span>         |
|                                 | <span data-ttu-id="9dcad-162">\_tutti i \_ \_ bit attrib (GL)</span><span class="sxs-lookup"><span data-stu-id="9dcad-162">GL\_ALL\_ATTRIB\_BITS</span></span>     |



 

<span data-ttu-id="9dcad-163">Per ripristinare i valori delle variabili di stato in quelli salvati con l'ultimo [**glPushAttrib**](glpushattrib.md), è sufficiente chiamare [**glPopAttrib**](glpopattrib.md).</span><span class="sxs-lookup"><span data-stu-id="9dcad-163">To restore the values of the state variables to those saved with the last [**glPushAttrib**](glpushattrib.md), simply call [**glPopAttrib**](glpopattrib.md).</span></span> <span data-ttu-id="9dcad-164">Le variabili non salvate rimarranno invariate.</span><span class="sxs-lookup"><span data-stu-id="9dcad-164">The variables you didn't save will remain unchanged.</span></span> <span data-ttu-id="9dcad-165">Lo stack degli attributi ha una profondità finita di almeno 16.</span><span class="sxs-lookup"><span data-stu-id="9dcad-165">The attribute stack has a finite depth of at least 16.</span></span>

 

 




