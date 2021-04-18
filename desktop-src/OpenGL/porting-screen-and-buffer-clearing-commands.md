---
title: Porting dei comandi di cancellazione dello schermo e del buffer
description: OpenGL sostituisce un'ampia gamma di funzioni Clear di IRIS GL, ad esempio zclear, aClear, sClear e così via, con una singola funzione, glClear. Specificare esattamente ciò che si vuole cancellare passando le maschere a glClear.
ms.assetid: 52ba503d-e412-4815-a039-a039b41327f4
keywords:
- Porting di IRIS GL, funzioni Clear
- porting da IRIS GL, funzioni Clear
- porting in OpenGL da IRIS GL, funzioni Clear
- Porting OpenGL da IRIS GL, funzioni Clear
- funzioni Clear
- Porting di IRIS GL, comandi di cancellazione dello schermo
- porting da IRIS GL, comandi di cancellazione dello schermo
- porting in OpenGL da IRIS GL, comandi di cancellazione dello schermo
- Porting OpenGL da IRIS GL, comandi di cancellazione dello schermo
- comandi di cancellazione dello schermo
- Porting di IRIS GL, comandi di cancellazione del buffer
- porting da IRIS GL, comandi di cancellazione del buffer
- porting in OpenGL da IRIS GL, comandi di cancellazione del buffer
- Porting OpenGL da IRIS GL, comandi di cancellazione del buffer
- comandi di cancellazione del buffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e53566c9fe14922f3965133cef9e30cbea4548b4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298537"
---
# <a name="porting-screen-and-buffer-clearing-commands"></a><span data-ttu-id="5fccf-119">Porting dei comandi di cancellazione dello schermo e del buffer</span><span class="sxs-lookup"><span data-stu-id="5fccf-119">Porting Screen and Buffer Clearing Commands</span></span>

<span data-ttu-id="5fccf-120">OpenGL sostituisce un'ampia gamma di funzioni **Clear** di Iris GL, ad esempio **zclear**, **aClear**, **sClear** e così via, con una singola funzione, [**glClear**](glclear.md).</span><span class="sxs-lookup"><span data-stu-id="5fccf-120">OpenGL replaces a variety of IRIS GL **clear** functions (such as **zclear**, **aclear**, **sclear**, and so on) with a single function, [**glClear**](glclear.md).</span></span> <span data-ttu-id="5fccf-121">Specificare esattamente ciò che si vuole cancellare passando le maschere a **glClear**.</span><span class="sxs-lookup"><span data-stu-id="5fccf-121">Specify exactly what you want to clear by passing masks to **glClear**.</span></span>

<span data-ttu-id="5fccf-122">Quando si portano i comandi dello schermo e del buffer, tenere presente quanto segue:</span><span class="sxs-lookup"><span data-stu-id="5fccf-122">Keep the following points in mind when porting screen and buffer commands:</span></span>

-   <span data-ttu-id="5fccf-123">OpenGL mantiene la cancellazione dei colori separatamente dai colori di disegno, con chiamate come [**glClearColor**](glclearcolor.md) e [**glClearIndex**](glclearindex.md).</span><span class="sxs-lookup"><span data-stu-id="5fccf-123">OpenGL maintains clearing colors separately from drawing colors, with calls like [**glClearColor**](glclearcolor.md) and [**glClearIndex**](glclearindex.md).</span></span> <span data-ttu-id="5fccf-124">Assicurarsi di impostare il colore chiaro per ogni buffer prima della cancellazione.</span><span class="sxs-lookup"><span data-stu-id="5fccf-124">Be sure to set the clear color for each buffer before clearing.</span></span>
-   <span data-ttu-id="5fccf-125">Anziché utilizzare una delle diverse chiamate Clear denominate in modo diverso, è ora possibile cancellare diversi buffer con una sola chiamata, [**glClear**](glclear.md), **o** insieme a maschere del buffer.</span><span class="sxs-lookup"><span data-stu-id="5fccf-125">Instead of using one of several differently named clear calls, you now clear several buffers with one call, [**glClear**](glclear.md), by **OR** ing together buffer masks.</span></span> <span data-ttu-id="5fccf-126">**Czclear** , ad esempio, viene sostituito da:</span><span class="sxs-lookup"><span data-stu-id="5fccf-126">For example, **czclear** is replaced by:</span></span>

    ``` syntax
    glClear( GL_COLOR_BUFFER_BIT | GL_DEPTH_BUFFER_BIT )
    ```

-   <span data-ttu-id="5fccf-127">IRIS GL fa riferimento al poligono stipple e al colore writemask.</span><span class="sxs-lookup"><span data-stu-id="5fccf-127">IRIS GL references the polygon stipple and the color writemask.</span></span> <span data-ttu-id="5fccf-128">OpenGL ignora il poligono stipple, ma fa riferimento al colore writemask.</span><span class="sxs-lookup"><span data-stu-id="5fccf-128">OpenGL ignores the polygon stipple but references the color writemask.</span></span> <span data-ttu-id="5fccf-129">La funzione **czclear** ignora sia il poligono stipple che il colore writemask.</span><span class="sxs-lookup"><span data-stu-id="5fccf-129">(The **czclear** function ignores both the polygon stipple and the color writemask.)</span></span>

<span data-ttu-id="5fccf-130">La tabella seguente elenca le varie funzioni Clear di IRIS GL con le funzioni OpenGL equivalenti.</span><span class="sxs-lookup"><span data-stu-id="5fccf-130">The following table lists the various IRIS GL clear functions with their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="5fccf-131">Chiamata a IRIS GL</span><span class="sxs-lookup"><span data-stu-id="5fccf-131">IRIS GL call</span></span>         | <span data-ttu-id="5fccf-132">Chiamata OpenGL</span><span class="sxs-lookup"><span data-stu-id="5fccf-132">OpenGL call</span></span>                                                               | <span data-ttu-id="5fccf-133">Significato</span><span class="sxs-lookup"><span data-stu-id="5fccf-133">Meaning</span></span>                                           |
|----------------------|---------------------------------------------------------------------------|---------------------------------------------------|
| <span data-ttu-id="5fccf-134">**acbuf**( \_ Clear AC)</span><span class="sxs-lookup"><span data-stu-id="5fccf-134">**acbuf**(AC\_CLEAR)</span></span> | <span data-ttu-id="5fccf-135">**glClear**( \_ bit del buffer di accut GL \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="5fccf-135">**glClear**( GL\_ACCUM\_BUFFER\_BIT )</span></span>                                     | <span data-ttu-id="5fccf-136">Cancellare il buffer di accumulo.</span><span class="sxs-lookup"><span data-stu-id="5fccf-136">Clear the accumulation buffer.</span></span>                    |
|                      | <span data-ttu-id="5fccf-137">**glClearColor**</span><span class="sxs-lookup"><span data-stu-id="5fccf-137">**glClearColor**</span></span>                                                          | <span data-ttu-id="5fccf-138">Impostare il colore di RGBA Clear.</span><span class="sxs-lookup"><span data-stu-id="5fccf-138">Set the RGBA clear color.</span></span>                         |
|                      | <span data-ttu-id="5fccf-139">**glClearIndex**</span><span class="sxs-lookup"><span data-stu-id="5fccf-139">**glClearIndex**</span></span>                                                          | <span data-ttu-id="5fccf-140">Impostare l'indice Clear-Color.</span><span class="sxs-lookup"><span data-stu-id="5fccf-140">Set the clear-color index.</span></span>                        |
| <span data-ttu-id="5fccf-141">**deselezionare**</span><span class="sxs-lookup"><span data-stu-id="5fccf-141">**clear**</span></span>            | <span data-ttu-id="5fccf-142">**glClear**( \_ bit del buffer dei colori GL \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="5fccf-142">**glClear**( GL\_COLOR\_BUFFER\_BIT )</span></span>                                     | <span data-ttu-id="5fccf-143">Cancellare il buffer dei colori.</span><span class="sxs-lookup"><span data-stu-id="5fccf-143">Clear the color buffer.</span></span>                           |
|                      | <span data-ttu-id="5fccf-144">**glClearDepth**</span><span class="sxs-lookup"><span data-stu-id="5fccf-144">**glClearDepth**</span></span>                                                          | <span data-ttu-id="5fccf-145">Specificare il valore Clear per il buffer di profondità.</span><span class="sxs-lookup"><span data-stu-id="5fccf-145">Specify the clear value for the depth buffer.</span></span>     |
| <span data-ttu-id="5fccf-146">**zclear**</span><span class="sxs-lookup"><span data-stu-id="5fccf-146">**zclear**</span></span>           | <span data-ttu-id="5fccf-147">**glClear**( \_ bit del buffer di profondità GL \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="5fccf-147">**glClear**( GL\_DEPTH\_BUFFER\_BIT )</span></span>                                     | <span data-ttu-id="5fccf-148">Cancellare il buffer di profondità.</span><span class="sxs-lookup"><span data-stu-id="5fccf-148">Clear the depth buffer.</span></span>                           |
| <span data-ttu-id="5fccf-149">**czclear**</span><span class="sxs-lookup"><span data-stu-id="5fccf-149">**czclear**</span></span>          | <span data-ttu-id="5fccf-150">**glClear**(bit del buffer di \_ bit GL del buffer dei colori GL \_ \_ \| \_ \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="5fccf-150">**glClear**( GL\_COLOR\_BUFFER\_BIT \|GL\_DEPTH\_BUFFER\_BIT )</span></span><br/> | <span data-ttu-id="5fccf-151">Cancellare il buffer dei colori e il buffer di profondità.</span><span class="sxs-lookup"><span data-stu-id="5fccf-151">Clear the color buffer and the depth buffer.</span></span>      |
|                      | <span data-ttu-id="5fccf-152">**glClearAccum**</span><span class="sxs-lookup"><span data-stu-id="5fccf-152">**glClearAccum**</span></span>                                                          | <span data-ttu-id="5fccf-153">Specificare valori non crittografati per il buffer di accumulo.</span><span class="sxs-lookup"><span data-stu-id="5fccf-153">Specify clear values for the accumulation buffer.</span></span> |
|                      | <span data-ttu-id="5fccf-154">**glClearStencil**</span><span class="sxs-lookup"><span data-stu-id="5fccf-154">**glClearStencil**</span></span>                                                        | <span data-ttu-id="5fccf-155">Specificare il valore Clear per il buffer dello stencil.</span><span class="sxs-lookup"><span data-stu-id="5fccf-155">Specify the clear value for the stencil buffer.</span></span>   |
| <span data-ttu-id="5fccf-156">**sclear**</span><span class="sxs-lookup"><span data-stu-id="5fccf-156">**sclear**</span></span>           | <span data-ttu-id="5fccf-157">**glClear**( \_ bit del buffer dello stencil GL \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="5fccf-157">**glClear**( GL\_STENCIL\_BUFFER\_BIT )</span></span>                                   | <span data-ttu-id="5fccf-158">Cancellare il buffer dello stencil.</span><span class="sxs-lookup"><span data-stu-id="5fccf-158">Clear the stencil buffer.</span></span>                         |



 

<span data-ttu-id="5fccf-159">Quando il codice di IRIS GL USA sia **gclear** che **sClear**, è possibile combinarli in una singola chiamata **glClear** ; può migliorare le prestazioni del programma.</span><span class="sxs-lookup"><span data-stu-id="5fccf-159">When your IRIS GL code uses both **gclear** and **sclear**, you can combine them into a single **glClear** call; can improve your program's performance.</span></span>

 

 





