---
title: Annotazioni di intestazione
description: Le annotazioni di intestazione descrivono il modo in cui una funzione usa i parametri e il valore restituito.
ms.assetid: 4f9e42b1-2fe4-4173-946e-ab1805a96b9e
keywords:
- API Windows, annotazioni di file di intestazione
- annotazioni file di intestazione
- Specstrings. h
- linguaggio di annotazione standard (SAL)
- _bcount
- _deref
- _deref_opt
- _ecount
- _full
- _in
- _inout
- _opt
- _out
- _part
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8535118383a97d6c48f19246ad24ce324e8bb528
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300291"
---
# <a name="header-annotations"></a><span data-ttu-id="bd928-117">Annotazioni di intestazione</span><span class="sxs-lookup"><span data-stu-id="bd928-117">Header Annotations</span></span>

<span data-ttu-id="bd928-118">\[In questo argomento vengono descritte le annotazioni supportate nelle intestazioni di Windows tramite Windows 7.</span><span class="sxs-lookup"><span data-stu-id="bd928-118">\[This topic describes the annotations supported in the Windows headers through Windows 7.</span></span> <span data-ttu-id="bd928-119">Se si sta sviluppando per Windows 8, è necessario usare le annotazioni descritte nelle [annotazioni SAL]( /previous-versions/visualstudio/visual-studio-2013/ms182032(v=vs.120)).\]</span><span class="sxs-lookup"><span data-stu-id="bd928-119">If you are developing for Windows 8, you should use the annotations described in [SAL Annotations]( /previous-versions/visualstudio/visual-studio-2013/ms182032(v=vs.120)).\]</span></span>

<span data-ttu-id="bd928-120">Le annotazioni di intestazione descrivono il modo in cui una funzione usa i parametri e il valore restituito.</span><span class="sxs-lookup"><span data-stu-id="bd928-120">Header annotations describe how a function uses its parameters and return value.</span></span> <span data-ttu-id="bd928-121">Queste annotazioni sono state aggiunte a molti dei file di intestazione di Windows per garantire la corretta chiamata dell'API Windows.</span><span class="sxs-lookup"><span data-stu-id="bd928-121">These annotations have been added to many of the Windows header files to help you ensure that you are calling the Windows API correctly.</span></span> <span data-ttu-id="bd928-122">Se si Abilita l'analisi del codice, disponibile a partire da Visual Studio 2005, il compilatore produrrà avvisi di livello 6000 se non si chiamano queste funzioni in base all'utilizzo descritto tramite le annotazioni.</span><span class="sxs-lookup"><span data-stu-id="bd928-122">If you enable code analysis, which is available starting with the Visual Studio 2005, the compiler will produce level 6000 warnings if you are not calling these functions per the usage described through the annotations.</span></span> <span data-ttu-id="bd928-123">È anche possibile aggiungere queste annotazioni nel codice per assicurarsi che venga chiamato correttamente.</span><span class="sxs-lookup"><span data-stu-id="bd928-123">You can also add these annotations in your own code to ensure that it is being called correctly.</span></span> <span data-ttu-id="bd928-124">Per abilitare l'analisi del codice in Visual Studio, vedere la documentazione per la versione di Visual Studio in uso.</span><span class="sxs-lookup"><span data-stu-id="bd928-124">To enable code analysis in Visual Studio, see the documentation for your version of Visual Studio.</span></span>

<span data-ttu-id="bd928-125">Queste annotazioni sono definite in Specstrings. h.</span><span class="sxs-lookup"><span data-stu-id="bd928-125">These annotations are defined in Specstrings.h.</span></span> <span data-ttu-id="bd928-126">Si basano sulle primitive che fanno parte del linguaggio di annotazione standard (SAL) e implementate tramite `_declspec("SAL_*")` .</span><span class="sxs-lookup"><span data-stu-id="bd928-126">They are built on primitives that are part of the Standard Annotation Language (SAL) and implemented using `_declspec("SAL_*")`.</span></span>

<span data-ttu-id="bd928-127">Esistono due classi di annotazioni: le annotazioni del buffer e le annotazioni avanzate.</span><span class="sxs-lookup"><span data-stu-id="bd928-127">There are two classes of annotations: buffer annotations and advanced annotations.</span></span>

## <a name="buffer-annotations"></a><span data-ttu-id="bd928-128">Annotazioni del buffer</span><span class="sxs-lookup"><span data-stu-id="bd928-128">Buffer Annotations</span></span>

<span data-ttu-id="bd928-129">Le annotazioni del buffer descrivono il modo in cui le funzioni utilizzano i puntatori e possono essere utilizzate per rilevare i sovraccarichi del buffer.</span><span class="sxs-lookup"><span data-stu-id="bd928-129">Buffer annotations describe how functions use their pointers and can be used to detect buffer overruns.</span></span> <span data-ttu-id="bd928-130">Ogni parametro può usare un'annotazione di buffer zero o uno.</span><span class="sxs-lookup"><span data-stu-id="bd928-130">Each parameter may use zero or one buffer annotation.</span></span> <span data-ttu-id="bd928-131">Un'annotazione del buffer viene costruita con un carattere di sottolineatura principale e i componenti descritti nelle sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="bd928-131">A buffer annotation is constructed with a leading underscore and the components described in the following sections.</span></span>



| <span data-ttu-id="bd928-132">Dimensioni del buffer</span><span class="sxs-lookup"><span data-stu-id="bd928-132">Buffer size</span></span>                                                                                  | <span data-ttu-id="bd928-133">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bd928-133">Description</span></span>                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd928-134"><span id="_size_"></span><span id="_SIZE_"></span>(*dimensioni*)</span><span class="sxs-lookup"><span data-stu-id="bd928-134"><span id="_size_"></span><span id="_SIZE_"></span>(*size*)</span></span><br/>                        | <span data-ttu-id="bd928-135">Specifica la dimensione totale del buffer.</span><span class="sxs-lookup"><span data-stu-id="bd928-135">Specifies the total size of the buffer.</span></span> <span data-ttu-id="bd928-136">Usare with \_ bcount e \_ ecount; non usare with \_ part.</span><span class="sxs-lookup"><span data-stu-id="bd928-136">Use with \_bcount and \_ecount; do not use with \_part.</span></span> <span data-ttu-id="bd928-137">Questo valore è lo spazio accessibile; può essere minore dello spazio allocato.</span><span class="sxs-lookup"><span data-stu-id="bd928-137">This value is the accessible space; it may be less than the allocated space.</span></span><br/> |
| <span data-ttu-id="bd928-138"><span id="_size_length_"></span><span id="_SIZE_LENGTH_"></span>(*dimensioni*,*lunghezza*)</span><span class="sxs-lookup"><span data-stu-id="bd928-138"><span id="_size_length_"></span><span id="_SIZE_LENGTH_"></span>(*size*,*length*)</span></span><br/> | <span data-ttu-id="bd928-139">Specifica la dimensione totale e la lunghezza inizializzata del buffer.</span><span class="sxs-lookup"><span data-stu-id="bd928-139">Specifies the total size and initialized length of the buffer.</span></span> <span data-ttu-id="bd928-140">Usare con la parte \_ bcount \_ e \_ ecount \_ .</span><span class="sxs-lookup"><span data-stu-id="bd928-140">Use with \_bcount\_part and \_ecount\_part.</span></span> <span data-ttu-id="bd928-141">Le dimensioni totali possono essere inferiori allo spazio allocato.</span><span class="sxs-lookup"><span data-stu-id="bd928-141">The total size may be less than the allocated space.</span></span><br/>              |



 



| <span data-ttu-id="bd928-142">Unità dimensioni buffer</span><span class="sxs-lookup"><span data-stu-id="bd928-142">Buffer size units</span></span>                                                       | <span data-ttu-id="bd928-143">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bd928-143">Description</span></span>                                |
|-------------------------------------------------------------------------|--------------------------------------------|
| <span data-ttu-id="bd928-144"><span id="_bcount"></span><span id="_BCOUNT"></span>\_bcount</span><span class="sxs-lookup"><span data-stu-id="bd928-144"><span id="_bcount"></span><span id="_BCOUNT"></span>\_bcount</span></span><br/> | <span data-ttu-id="bd928-145">Dimensioni del buffer in byte.</span><span class="sxs-lookup"><span data-stu-id="bd928-145">The buffer size is in bytes.</span></span><br/>    |
| <span data-ttu-id="bd928-146"><span id="_ecount"></span><span id="_ECOUNT"></span>\_ecount</span><span class="sxs-lookup"><span data-stu-id="bd928-146"><span id="_ecount"></span><span id="_ECOUNT"></span>\_ecount</span></span><br/> | <span data-ttu-id="bd928-147">La dimensione del buffer è in elementi.</span><span class="sxs-lookup"><span data-stu-id="bd928-147">The buffer size is in elements.</span></span><br/> |



 



| <span data-ttu-id="bd928-148">Direzione</span><span class="sxs-lookup"><span data-stu-id="bd928-148">Direction</span></span>                                                            | <span data-ttu-id="bd928-149">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bd928-149">Description</span></span>                                                                                                                                                                                                                |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd928-150"><span id="_in"></span><span id="_IN"></span>\_in</span><span class="sxs-lookup"><span data-stu-id="bd928-150"><span id="_in"></span><span id="_IN"></span>\_in</span></span><br/>          | <span data-ttu-id="bd928-151">La funzione legge dal buffer.</span><span class="sxs-lookup"><span data-stu-id="bd928-151">The function reads from the buffer.</span></span> <span data-ttu-id="bd928-152">Il chiamante fornisce il buffer e lo inizializza.</span><span class="sxs-lookup"><span data-stu-id="bd928-152">The caller provides the buffer and initializes it.</span></span><br/>                                                                                                                          |
| <span data-ttu-id="bd928-153"><span id="_inout"></span><span id="_INOUT"></span>\_Inout</span><span class="sxs-lookup"><span data-stu-id="bd928-153"><span id="_inout"></span><span id="_INOUT"></span>\_inout</span></span><br/> | <span data-ttu-id="bd928-154">La funzione legge e scrive nel buffer.</span><span class="sxs-lookup"><span data-stu-id="bd928-154">The function both reads from and writes to buffer.</span></span> <span data-ttu-id="bd928-155">Il chiamante fornisce il buffer e lo inizializza.</span><span class="sxs-lookup"><span data-stu-id="bd928-155">The caller provides the buffer and initializes it.</span></span> <span data-ttu-id="bd928-156">Se usato con \_ Deref, il buffer può essere riallocato dalla funzione.</span><span class="sxs-lookup"><span data-stu-id="bd928-156">If used with \_deref, the buffer may be reallocated by the function.</span></span><br/>                                      |
| <span data-ttu-id="bd928-157"><span id="_out"></span><span id="_OUT"></span>\_out</span><span class="sxs-lookup"><span data-stu-id="bd928-157"><span id="_out"></span><span id="_OUT"></span>\_out</span></span><br/>       | <span data-ttu-id="bd928-158">La funzione scrive nel buffer.</span><span class="sxs-lookup"><span data-stu-id="bd928-158">The function writes to the buffer.</span></span> <span data-ttu-id="bd928-159">Se usato sul valore restituito o con \_ Deref, la funzione fornisce il buffer e lo inizializza.</span><span class="sxs-lookup"><span data-stu-id="bd928-159">If used on the return value or with \_deref, the function provides the buffer and initializes it.</span></span> <span data-ttu-id="bd928-160">In caso contrario, il chiamante fornisce il buffer e la funzione la Inizializza.</span><span class="sxs-lookup"><span data-stu-id="bd928-160">Otherwise, the caller provides the buffer and the function initializes it.</span></span><br/> |



 



| <span data-ttu-id="bd928-161">Riferimento indiretto</span><span class="sxs-lookup"><span data-stu-id="bd928-161">Indirection</span></span>                                                                       | <span data-ttu-id="bd928-162">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bd928-162">Description</span></span>                                                                                            |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd928-163"><span id="_deref"></span><span id="_DEREF"></span>\_Deref</span><span class="sxs-lookup"><span data-stu-id="bd928-163"><span id="_deref"></span><span id="_DEREF"></span>\_deref</span></span><br/>              | <span data-ttu-id="bd928-164">Dereferenziare il parametro per ottenere il puntatore del buffer.</span><span class="sxs-lookup"><span data-stu-id="bd928-164">Dereference the parameter to obtain the buffer pointer.</span></span> <span data-ttu-id="bd928-165">Questo parametro non può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="bd928-165">This parameter may not be **NULL**.</span></span><br/> |
| <span data-ttu-id="bd928-166"><span id="_deref_opt"></span><span id="_DEREF_OPT"></span>\_Deref \_ opt</span><span class="sxs-lookup"><span data-stu-id="bd928-166"><span id="_deref_opt"></span><span id="_DEREF_OPT"></span>\_deref\_opt</span></span><br/> | <span data-ttu-id="bd928-167">Dereferenziare il parametro per ottenere il puntatore del buffer.</span><span class="sxs-lookup"><span data-stu-id="bd928-167">Dereference the parameter to obtain the buffer pointer.</span></span> <span data-ttu-id="bd928-168">Questo parametro può essere **NULL**.</span><span class="sxs-lookup"><span data-stu-id="bd928-168">This parameter can be **NULL**.</span></span><br/>     |



 



| <span data-ttu-id="bd928-169">Inizializzazione</span><span class="sxs-lookup"><span data-stu-id="bd928-169">Initialization</span></span>                                                    | <span data-ttu-id="bd928-170">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bd928-170">Description</span></span>                                                                                                              |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd928-171"><span id="_full"></span><span id="_FULL"></span>\_completo</span><span class="sxs-lookup"><span data-stu-id="bd928-171"><span id="_full"></span><span id="_FULL"></span>\_full</span></span><br/> | <span data-ttu-id="bd928-172">La funzione Inizializza l'intero buffer.</span><span class="sxs-lookup"><span data-stu-id="bd928-172">The function initializes the entire buffer.</span></span> <span data-ttu-id="bd928-173">Utilizzare solo con i buffer di output.</span><span class="sxs-lookup"><span data-stu-id="bd928-173">Use only with output buffers.</span></span><br/>                                     |
| <span data-ttu-id="bd928-174"><span id="_part"></span><span id="_PART"></span>\_parte</span><span class="sxs-lookup"><span data-stu-id="bd928-174"><span id="_part"></span><span id="_PART"></span>\_part</span></span><br/> | <span data-ttu-id="bd928-175">La funzione Inizializza parte del buffer e indica in modo esplicito la quantità.</span><span class="sxs-lookup"><span data-stu-id="bd928-175">The function initializes part of the buffer, and explicitly indicates how much.</span></span> <span data-ttu-id="bd928-176">Utilizzare solo con i buffer di output.</span><span class="sxs-lookup"><span data-stu-id="bd928-176">Use only with output buffers.</span></span><br/> |



 



| <span data-ttu-id="bd928-177">Buffer obbligatorio o facoltativo</span><span class="sxs-lookup"><span data-stu-id="bd928-177">Required or optional buffer</span></span>                                    | <span data-ttu-id="bd928-178">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bd928-178">Description</span></span>                                |
|----------------------------------------------------------------|--------------------------------------------|
| <span data-ttu-id="bd928-179"><span id="_opt"></span><span id="_OPT"></span>\_consenso esplicito</span><span class="sxs-lookup"><span data-stu-id="bd928-179"><span id="_opt"></span><span id="_OPT"></span>\_opt</span></span><br/> | <span data-ttu-id="bd928-180">Questo parametro può essere **NULL**.</span><span class="sxs-lookup"><span data-stu-id="bd928-180">This parameter can be **NULL**.</span></span><br/> |



 

<span data-ttu-id="bd928-181">Nell'esempio seguente vengono illustrate le annotazioni per la funzione **GetModuleFileName** .</span><span class="sxs-lookup"><span data-stu-id="bd928-181">The following example shows the annotations for the **GetModuleFileName** function.</span></span> <span data-ttu-id="bd928-182">Il parametro *hmodule* è un parametro di input facoltativo.</span><span class="sxs-lookup"><span data-stu-id="bd928-182">The *hModule* parameter is an optional input parameter .</span></span> <span data-ttu-id="bd928-183">Il parametro *lpFileName* è un parametro di output. la relativa dimensione in caratteri viene specificata dal parametro *nSize* e la relativa lunghezza include il carattere di terminazione **null**.</span><span class="sxs-lookup"><span data-stu-id="bd928-183">The *lpFilename* parameter is an output parameter; its size in characters is specified by the *nSize* parameter and its length includes the **null**-terminating character.</span></span> <span data-ttu-id="bd928-184">Il parametro *nSize* è un parametro di input.</span><span class="sxs-lookup"><span data-stu-id="bd928-184">The *nSize* parameter is an input parameter.</span></span>


```C++
DWORD
WINAPI
GetModuleFileName(
    __in_opt HMODULE hModule,
    __out_ecount_part(nSize, return + 1) LPTSTR lpFilename,
    __in DWORD nSize
    );
```



<span data-ttu-id="bd928-185">Di seguito sono riportate le annotazioni definite in Specstrings. h.</span><span class="sxs-lookup"><span data-stu-id="bd928-185">The following are the annotations defined in Specstrings.h.</span></span> <span data-ttu-id="bd928-186">Utilizzare le informazioni nelle tabelle precedenti per interpretarne il significato.</span><span class="sxs-lookup"><span data-stu-id="bd928-186">Use the information in the tables above to interpret their meaning.</span></span>

<span data-ttu-id="bd928-187">__bcount (*dimensioni*)</span><span class="sxs-lookup"><span data-stu-id="bd928-187">__bcount(*size*)</span></span>  
<span data-ttu-id="bd928-188">__bcount_opt (*dimensioni*)</span><span class="sxs-lookup"><span data-stu-id="bd928-188">__bcount_opt(*size*)</span></span>  
<span data-ttu-id="bd928-189">__deref_bcount (*dimensioni*)</span><span class="sxs-lookup"><span data-stu-id="bd928-189">__deref_bcount(*size*)</span></span>  
<span data-ttu-id="bd928-190">__deref_bcount_opt (*dimensioni*)</span><span class="sxs-lookup"><span data-stu-id="bd928-190">__deref_bcount_opt(*size*)</span></span>  
<span data-ttu-id="bd928-191">__deref_ecount (*dimensioni*)</span><span class="sxs-lookup"><span data-stu-id="bd928-191">__deref_ecount(*size*)</span></span>  
<span data-ttu-id="bd928-192">__deref_ecount_opt (*dimensioni*)</span><span class="sxs-lookup"><span data-stu-id="bd928-192">__deref_ecount_opt(*size*)</span></span>  
<span data-ttu-id="bd928-193">__deref_in</span><span class="sxs-lookup"><span data-stu-id="bd928-193">__deref_in</span></span>  
<span data-ttu-id="bd928-194">__deref_in_bcount (*dimensioni*)</span><span class="sxs-lookup"><span data-stu-id="bd928-194">__deref_in_bcount(*size*)</span></span>  
<span data-ttu-id="bd928-195">__deref_in_bcount_opt (*dimensioni*)</span><span class="sxs-lookup"><span data-stu-id="bd928-195">__deref_in_bcount_opt(*size*)</span></span>  
<span data-ttu-id="bd928-196">__deref_in_ecount (*dimensioni*)</span><span class="sxs-lookup"><span data-stu-id="bd928-196">__deref_in_ecount(*size*)</span></span>  
<span data-ttu-id="bd928-197">__deref_in_ecount_opt (*dimensioni*)</span><span class="sxs-lookup"><span data-stu-id="bd928-197">__deref_in_ecount_opt(*size*)</span></span>  
<span data-ttu-id="bd928-198">__deref_in_opt</span><span class="sxs-lookup"><span data-stu-id="bd928-198">__deref_in_opt</span></span>  
<span data-ttu-id="bd928-199">__deref_inout</span><span class="sxs-lookup"><span data-stu-id="bd928-199">__deref_inout</span></span>  
<span data-ttu-id="bd928-200">__deref_inout_bcount (*dimensioni*)</span><span class="sxs-lookup"><span data-stu-id="bd928-200">__deref_inout_bcount(*size*)</span></span>  
<span data-ttu-id="bd928-201">__deref_inout_bcount_full (*dimensioni*)</span><span class="sxs-lookup"><span data-stu-id="bd928-201">__deref_inout_bcount_full(*size*)</span></span>  
<span data-ttu-id="bd928-202">__deref_inout_bcount_full_opt (*dimensioni*)</span><span class="sxs-lookup"><span data-stu-id="bd928-202">__deref_inout_bcount_full_opt(*size*)</span></span>  
<span data-ttu-id="bd928-203">__deref_inout_bcount_opt (*dimensioni*)</span><span class="sxs-lookup"><span data-stu-id="bd928-203">__deref_inout_bcount_opt(*size*)</span></span>  
<span data-ttu-id="bd928-204">__deref_inout_bcount_part (*dimensioni*,*lunghezza*)</span><span class="sxs-lookup"><span data-stu-id="bd928-204">__deref_inout_bcount_part(*size*,*length*)</span></span>  
<span data-ttu-id="bd928-205">__deref_inout_bcount_part_opt (*dimensioni*,*lunghezza*)</span><span class="sxs-lookup"><span data-stu-id="bd928-205">__deref_inout_bcount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="bd928-206">__deref_inout_ecount (*dimensioni*)</span><span class="sxs-lookup"><span data-stu-id="bd928-206">__deref_inout_ecount(*size*)</span></span>  
<span data-ttu-id="bd928-207">__deref_inout_ecount_full (*dimensioni*)</span><span class="sxs-lookup"><span data-stu-id="bd928-207">__deref_inout_ecount_full(*size*)</span></span>  
<span data-ttu-id="bd928-208">__deref_inout_ecount_full_opt (*dimensioni*)</span><span class="sxs-lookup"><span data-stu-id="bd928-208">__deref_inout_ecount_full_opt(*size*)</span></span>  
<span data-ttu-id="bd928-209">__deref_inout_ecount_opt (*dimensioni*)</span><span class="sxs-lookup"><span data-stu-id="bd928-209">__deref_inout_ecount_opt(*size*)</span></span>  
<span data-ttu-id="bd928-210">__deref_inout_ecount_part (*dimensioni*,*lunghezza*)</span><span class="sxs-lookup"><span data-stu-id="bd928-210">__deref_inout_ecount_part(*size*,*length*)</span></span>  
<span data-ttu-id="bd928-211">__deref_inout_ecount_part_opt (*dimensioni*,*lunghezza*)</span><span class="sxs-lookup"><span data-stu-id="bd928-211">__deref_inout_ecount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="bd928-212">__deref_inout_opt</span><span class="sxs-lookup"><span data-stu-id="bd928-212">__deref_inout_opt</span></span>  
<span data-ttu-id="bd928-213">__deref_opt_bcount (*dimensioni*)</span><span class="sxs-lookup"><span data-stu-id="bd928-213">__deref_opt_bcount(*size*)</span></span>  
<span data-ttu-id="bd928-214">__deref_opt_bcount_opt (*dimensioni*)</span><span class="sxs-lookup"><span data-stu-id="bd928-214">__deref_opt_bcount_opt(*size*)</span></span>  
<span data-ttu-id="bd928-215">__deref_opt_ecount (*dimensioni*)</span><span class="sxs-lookup"><span data-stu-id="bd928-215">__deref_opt_ecount(*size*)</span></span>  
<span data-ttu-id="bd928-216">__deref_opt_ecount_opt (*dimensioni*)</span><span class="sxs-lookup"><span data-stu-id="bd928-216">__deref_opt_ecount_opt(*size*)</span></span>  
<span data-ttu-id="bd928-217">__deref_opt_in</span><span class="sxs-lookup"><span data-stu-id="bd928-217">__deref_opt_in</span></span>  
<span data-ttu-id="bd928-218">__deref_opt_in_bcount (*dimensioni*)</span><span class="sxs-lookup"><span data-stu-id="bd928-218">__deref_opt_in_bcount(*size*)</span></span>  
<span data-ttu-id="bd928-219">__deref_opt_in_bcount_opt (*dimensioni*)</span><span class="sxs-lookup"><span data-stu-id="bd928-219">__deref_opt_in_bcount_opt(*size*)</span></span>  
<span data-ttu-id="bd928-220">__deref_opt_in_ecount (*dimensioni*)</span><span class="sxs-lookup"><span data-stu-id="bd928-220">__deref_opt_in_ecount(*size*)</span></span>  
<span data-ttu-id="bd928-221">__deref_opt_in_ecount_opt (*dimensioni*)</span><span class="sxs-lookup"><span data-stu-id="bd928-221">__deref_opt_in_ecount_opt(*size*)</span></span>  
<span data-ttu-id="bd928-222">__deref_opt_in_opt</span><span class="sxs-lookup"><span data-stu-id="bd928-222">__deref_opt_in_opt</span></span>  
<span data-ttu-id="bd928-223">__deref_opt_inout</span><span class="sxs-lookup"><span data-stu-id="bd928-223">__deref_opt_inout</span></span>  
<span data-ttu-id="bd928-224">__deref_opt_inout_bcount (*dimensioni*)</span><span class="sxs-lookup"><span data-stu-id="bd928-224">__deref_opt_inout_bcount(*size*)</span></span>  
<span data-ttu-id="bd928-225">__deref_opt_inout_bcount_full (*dimensioni*)</span><span class="sxs-lookup"><span data-stu-id="bd928-225">__deref_opt_inout_bcount_full(*size*)</span></span>  
<span data-ttu-id="bd928-226">__deref_opt_inout_bcount_full_opt (*dimensioni*)</span><span class="sxs-lookup"><span data-stu-id="bd928-226">__deref_opt_inout_bcount_full_opt(*size*)</span></span>  
<span data-ttu-id="bd928-227">__deref_opt_inout_bcount_opt (*dimensioni*)</span><span class="sxs-lookup"><span data-stu-id="bd928-227">__deref_opt_inout_bcount_opt(*size*)</span></span>  
<span data-ttu-id="bd928-228">__deref_opt_inout_bcount_part (*dimensioni*,*lunghezza*)</span><span class="sxs-lookup"><span data-stu-id="bd928-228">__deref_opt_inout_bcount_part(*size*,*length*)</span></span>  
<span data-ttu-id="bd928-229">__deref_opt_inout_bcount_part_opt (*dimensioni*,*lunghezza*)</span><span class="sxs-lookup"><span data-stu-id="bd928-229">__deref_opt_inout_bcount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="bd928-230">__deref_opt_inout_ecount (*dimensioni*)</span><span class="sxs-lookup"><span data-stu-id="bd928-230">__deref_opt_inout_ecount(*size*)</span></span>  
<span data-ttu-id="bd928-231">__deref_opt_inout_ecount_full (*dimensioni*)</span><span class="sxs-lookup"><span data-stu-id="bd928-231">__deref_opt_inout_ecount_full(*size*)</span></span>  
<span data-ttu-id="bd928-232">__deref_opt_inout_ecount_full_opt (*dimensioni*)</span><span class="sxs-lookup"><span data-stu-id="bd928-232">__deref_opt_inout_ecount_full_opt(*size*)</span></span>  
<span data-ttu-id="bd928-233">__deref_opt_inout_ecount_opt (*dimensioni*)</span><span class="sxs-lookup"><span data-stu-id="bd928-233">__deref_opt_inout_ecount_opt(*size*)</span></span>  
<span data-ttu-id="bd928-234">__deref_opt_inout_ecount_part (*dimensioni*,*lunghezza*)</span><span class="sxs-lookup"><span data-stu-id="bd928-234">__deref_opt_inout_ecount_part(*size*,*length*)</span></span>  
<span data-ttu-id="bd928-235">__deref_opt_inout_ecount_part_opt (*dimensioni*,*lunghezza*)</span><span class="sxs-lookup"><span data-stu-id="bd928-235">__deref_opt_inout_ecount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="bd928-236">__deref_opt_inout_opt</span><span class="sxs-lookup"><span data-stu-id="bd928-236">__deref_opt_inout_opt</span></span>  
<span data-ttu-id="bd928-237">__deref_opt_out</span><span class="sxs-lookup"><span data-stu-id="bd928-237">__deref_opt_out</span></span>  
<span data-ttu-id="bd928-238">__deref_opt_out_bcount (*dimensioni*)</span><span class="sxs-lookup"><span data-stu-id="bd928-238">__deref_opt_out_bcount(*size*)</span></span>  
<span data-ttu-id="bd928-239">__deref_opt_out_bcount_full (*dimensioni*)</span><span class="sxs-lookup"><span data-stu-id="bd928-239">__deref_opt_out_bcount_full(*size*)</span></span>  
<span data-ttu-id="bd928-240">__deref_opt_out_bcount_full_opt (*dimensioni*)</span><span class="sxs-lookup"><span data-stu-id="bd928-240">__deref_opt_out_bcount_full_opt(*size*)</span></span>  
<span data-ttu-id="bd928-241">__deref_opt_out_bcount_opt (*dimensioni*)</span><span class="sxs-lookup"><span data-stu-id="bd928-241">__deref_opt_out_bcount_opt(*size*)</span></span>  
<span data-ttu-id="bd928-242">__deref_opt_out_bcount_part (*dimensioni*,*lunghezza*)</span><span class="sxs-lookup"><span data-stu-id="bd928-242">__deref_opt_out_bcount_part(*size*,*length*)</span></span>  
<span data-ttu-id="bd928-243">__deref_opt_out_bcount_part_opt (*dimensioni*,*lunghezza*)</span><span class="sxs-lookup"><span data-stu-id="bd928-243">__deref_opt_out_bcount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="bd928-244">__deref_opt_out_ecount (*dimensioni*)</span><span class="sxs-lookup"><span data-stu-id="bd928-244">__deref_opt_out_ecount(*size*)</span></span>  
<span data-ttu-id="bd928-245">__deref_opt_out_ecount_full (*dimensioni*)</span><span class="sxs-lookup"><span data-stu-id="bd928-245">__deref_opt_out_ecount_full(*size*)</span></span>  
<span data-ttu-id="bd928-246">__deref_opt_out_ecount_full_opt (*dimensioni*)</span><span class="sxs-lookup"><span data-stu-id="bd928-246">__deref_opt_out_ecount_full_opt(*size*)</span></span>  
<span data-ttu-id="bd928-247">__deref_opt_out_ecount_opt (*dimensioni*)</span><span class="sxs-lookup"><span data-stu-id="bd928-247">__deref_opt_out_ecount_opt(*size*)</span></span>  
<span data-ttu-id="bd928-248">__deref_opt_out_ecount_part (*dimensioni*,*lunghezza*)</span><span class="sxs-lookup"><span data-stu-id="bd928-248">__deref_opt_out_ecount_part(*size*,*length*)</span></span>  
<span data-ttu-id="bd928-249">__deref_opt_out_ecount_part_opt (*dimensioni*,*lunghezza*)</span><span class="sxs-lookup"><span data-stu-id="bd928-249">__deref_opt_out_ecount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="bd928-250">__deref_opt_out_opt</span><span class="sxs-lookup"><span data-stu-id="bd928-250">__deref_opt_out_opt</span></span>  
<span data-ttu-id="bd928-251">__deref_out</span><span class="sxs-lookup"><span data-stu-id="bd928-251">__deref_out</span></span>  
<span data-ttu-id="bd928-252">__deref_out_bcount (*dimensioni*)</span><span class="sxs-lookup"><span data-stu-id="bd928-252">__deref_out_bcount(*size*)</span></span>  
<span data-ttu-id="bd928-253">__deref_out_bcount_full (*dimensioni*)</span><span class="sxs-lookup"><span data-stu-id="bd928-253">__deref_out_bcount_full(*size*)</span></span>  
<span data-ttu-id="bd928-254">__deref_out_bcount_full_opt (*dimensioni*)</span><span class="sxs-lookup"><span data-stu-id="bd928-254">__deref_out_bcount_full_opt(*size*)</span></span>  
<span data-ttu-id="bd928-255">__deref_out_bcount_opt (*dimensioni*)</span><span class="sxs-lookup"><span data-stu-id="bd928-255">__deref_out_bcount_opt(*size*)</span></span>  
<span data-ttu-id="bd928-256">__deref_out_bcount_part (*dimensioni*,*lunghezza*)</span><span class="sxs-lookup"><span data-stu-id="bd928-256">__deref_out_bcount_part(*size*,*length*)</span></span>  
<span data-ttu-id="bd928-257">__deref_out_bcount_part_opt (*dimensioni*,*lunghezza*)</span><span class="sxs-lookup"><span data-stu-id="bd928-257">__deref_out_bcount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="bd928-258">__deref_out_ecount (*dimensioni*)</span><span class="sxs-lookup"><span data-stu-id="bd928-258">__deref_out_ecount(*size*)</span></span>  
<span data-ttu-id="bd928-259">__deref_out_ecount_full (*dimensioni*)</span><span class="sxs-lookup"><span data-stu-id="bd928-259">__deref_out_ecount_full(*size*)</span></span>  
<span data-ttu-id="bd928-260">__deref_out_ecount_full_opt (*dimensioni*)</span><span class="sxs-lookup"><span data-stu-id="bd928-260">__deref_out_ecount_full_opt(*size*)</span></span>  
<span data-ttu-id="bd928-261">__deref_out_ecount_opt (*dimensioni*)</span><span class="sxs-lookup"><span data-stu-id="bd928-261">__deref_out_ecount_opt(*size*)</span></span>  
<span data-ttu-id="bd928-262">__deref_out_ecount_part (*dimensioni*,*lunghezza*)</span><span class="sxs-lookup"><span data-stu-id="bd928-262">__deref_out_ecount_part(*size*,*length*)</span></span>  
<span data-ttu-id="bd928-263">__deref_out_ecount_part_opt (*dimensioni*,*lunghezza*)</span><span class="sxs-lookup"><span data-stu-id="bd928-263">__deref_out_ecount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="bd928-264">__deref_out_opt</span><span class="sxs-lookup"><span data-stu-id="bd928-264">__deref_out_opt</span></span>  
<span data-ttu-id="bd928-265">__ecount (*dimensioni*)</span><span class="sxs-lookup"><span data-stu-id="bd928-265">__ecount(*size*)</span></span>  
<span data-ttu-id="bd928-266">__ecount_opt (*dimensioni*)</span><span class="sxs-lookup"><span data-stu-id="bd928-266">__ecount_opt(*size*)</span></span>  
<span data-ttu-id="bd928-267">__in</span><span class="sxs-lookup"><span data-stu-id="bd928-267">__in</span></span>  
<span data-ttu-id="bd928-268">__in_bcount (*dimensioni*)</span><span class="sxs-lookup"><span data-stu-id="bd928-268">__in_bcount(*size*)</span></span>  
<span data-ttu-id="bd928-269">__in_bcount_opt (*dimensioni*)</span><span class="sxs-lookup"><span data-stu-id="bd928-269">__in_bcount_opt(*size*)</span></span>  
<span data-ttu-id="bd928-270">__in_ecount (*dimensioni*)</span><span class="sxs-lookup"><span data-stu-id="bd928-270">__in_ecount(*size*)</span></span>  
<span data-ttu-id="bd928-271">__in_ecount_opt (*dimensioni*)</span><span class="sxs-lookup"><span data-stu-id="bd928-271">__in_ecount_opt(*size*)</span></span>  
<span data-ttu-id="bd928-272">__in_opt</span><span class="sxs-lookup"><span data-stu-id="bd928-272">__in_opt</span></span>  
<span data-ttu-id="bd928-273">__inout</span><span class="sxs-lookup"><span data-stu-id="bd928-273">__inout</span></span>  
<span data-ttu-id="bd928-274">__inout_bcount (*dimensioni*)</span><span class="sxs-lookup"><span data-stu-id="bd928-274">__inout_bcount(*size*)</span></span>  
<span data-ttu-id="bd928-275">__inout_bcount_full (*dimensioni*)</span><span class="sxs-lookup"><span data-stu-id="bd928-275">__inout_bcount_full(*size*)</span></span>  
<span data-ttu-id="bd928-276">__inout_bcount_full_opt (*dimensioni*)</span><span class="sxs-lookup"><span data-stu-id="bd928-276">__inout_bcount_full_opt(*size*)</span></span>  
<span data-ttu-id="bd928-277">__inout_bcount_opt (*dimensioni*)</span><span class="sxs-lookup"><span data-stu-id="bd928-277">__inout_bcount_opt(*size*)</span></span>  
<span data-ttu-id="bd928-278">__inout_bcount_part (*dimensioni*,*lunghezza*)</span><span class="sxs-lookup"><span data-stu-id="bd928-278">__inout_bcount_part(*size*,*length*)</span></span>  
<span data-ttu-id="bd928-279">__inout_bcount_part_opt (*dimensioni*,*lunghezza*)</span><span class="sxs-lookup"><span data-stu-id="bd928-279">__inout_bcount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="bd928-280">__inout_ecount (*dimensioni*)</span><span class="sxs-lookup"><span data-stu-id="bd928-280">__inout_ecount(*size*)</span></span>  
<span data-ttu-id="bd928-281">__inout_ecount_full (*dimensioni*)</span><span class="sxs-lookup"><span data-stu-id="bd928-281">__inout_ecount_full(*size*)</span></span>  
<span data-ttu-id="bd928-282">__inout_ecount_full_opt (*dimensioni*)</span><span class="sxs-lookup"><span data-stu-id="bd928-282">__inout_ecount_full_opt(*size*)</span></span>  
<span data-ttu-id="bd928-283">__inout_ecount_opt (*dimensioni*)</span><span class="sxs-lookup"><span data-stu-id="bd928-283">__inout_ecount_opt(*size*)</span></span>  
<span data-ttu-id="bd928-284">__inout_ecount_part (*dimensioni*,*lunghezza*)</span><span class="sxs-lookup"><span data-stu-id="bd928-284">__inout_ecount_part(*size*,*length*)</span></span>  
<span data-ttu-id="bd928-285">__inout_ecount_part_opt (*dimensioni*,*lunghezza*)</span><span class="sxs-lookup"><span data-stu-id="bd928-285">__inout_ecount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="bd928-286">__inout_opt</span><span class="sxs-lookup"><span data-stu-id="bd928-286">__inout_opt</span></span>  
<span data-ttu-id="bd928-287">__out</span><span class="sxs-lookup"><span data-stu-id="bd928-287">__out</span></span>  
<span data-ttu-id="bd928-288">__out_bcount (*dimensioni*)</span><span class="sxs-lookup"><span data-stu-id="bd928-288">__out_bcount(*size*)</span></span>  
<span data-ttu-id="bd928-289">__out_bcount_full (*dimensioni*)</span><span class="sxs-lookup"><span data-stu-id="bd928-289">__out_bcount_full(*size*)</span></span>  
<span data-ttu-id="bd928-290">__out_bcount_full_opt (*dimensioni*)</span><span class="sxs-lookup"><span data-stu-id="bd928-290">__out_bcount_full_opt(*size*)</span></span>  
<span data-ttu-id="bd928-291">__out_bcount_opt (*dimensioni*)</span><span class="sxs-lookup"><span data-stu-id="bd928-291">__out_bcount_opt(*size*)</span></span>  
<span data-ttu-id="bd928-292">__out_bcount_part (*dimensioni*,*lunghezza*)</span><span class="sxs-lookup"><span data-stu-id="bd928-292">__out_bcount_part(*size*,*length*)</span></span>  
<span data-ttu-id="bd928-293">__out_bcount_part_opt (*dimensioni*,*lunghezza*)</span><span class="sxs-lookup"><span data-stu-id="bd928-293">__out_bcount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="bd928-294">__out_ecount (*dimensioni*)</span><span class="sxs-lookup"><span data-stu-id="bd928-294">__out_ecount(*size*)</span></span>  
<span data-ttu-id="bd928-295">__out_ecount_full (*dimensioni*)</span><span class="sxs-lookup"><span data-stu-id="bd928-295">__out_ecount_full(*size*)</span></span>  
<span data-ttu-id="bd928-296">__out_ecount_full_opt (*dimensioni*)</span><span class="sxs-lookup"><span data-stu-id="bd928-296">__out_ecount_full_opt(*size*)</span></span>  
<span data-ttu-id="bd928-297">__out_ecount_opt (*dimensioni*)</span><span class="sxs-lookup"><span data-stu-id="bd928-297">__out_ecount_opt(*size*)</span></span>  
<span data-ttu-id="bd928-298">__out_ecount_part (*dimensioni*,*lunghezza*)</span><span class="sxs-lookup"><span data-stu-id="bd928-298">__out_ecount_part(*size*,*length*)</span></span>  
<span data-ttu-id="bd928-299">__out_ecount_part_opt (*dimensioni*,*lunghezza*)</span><span class="sxs-lookup"><span data-stu-id="bd928-299">__out_ecount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="bd928-300">__out_opt</span><span class="sxs-lookup"><span data-stu-id="bd928-300">__out_opt</span></span>  

## <a name="advanced-annotations"></a><span data-ttu-id="bd928-301">Annotazioni avanzate</span><span class="sxs-lookup"><span data-stu-id="bd928-301">Advanced Annotations</span></span>

<span data-ttu-id="bd928-302">Le annotazioni avanzate forniscono informazioni aggiuntive sul parametro o sul valore restituito.</span><span class="sxs-lookup"><span data-stu-id="bd928-302">Advanced annotations provide additional information about the parameter or return value.</span></span> <span data-ttu-id="bd928-303">Ogni parametro o valore restituito può utilizzare una o più annotazioni avanzate.</span><span class="sxs-lookup"><span data-stu-id="bd928-303">Each parameter or return value may use zero or one advanced annotation.</span></span>



| <span data-ttu-id="bd928-304">Annotazione</span><span class="sxs-lookup"><span data-stu-id="bd928-304">Annotation</span></span>                                                                                                                                               | <span data-ttu-id="bd928-305">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bd928-305">Description</span></span>                                                                                                                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd928-306"><span id="__blocksOn_resource_"></span><span id="__blockson_resource_"></span><span id="__BLOCKSON_RESOURCE_"></span>\_\_blocksOn (*risorsa*)</span><span class="sxs-lookup"><span data-stu-id="bd928-306"><span id="__blocksOn_resource_"></span><span id="__blockson_resource_"></span><span id="__BLOCKSON_RESOURCE_"></span>\_\_blocksOn(*resource*)</span></span><br/> | <span data-ttu-id="bd928-307">Le funzioni vengono bloccate sulla risorsa specificata.</span><span class="sxs-lookup"><span data-stu-id="bd928-307">The functions blocks on the specified resource.</span></span><br/>                                                                                                                                                                                                                      |
| <span data-ttu-id="bd928-308"><span id="__callback"></span><span id="__CALLBACK"></span>\_\_callback</span><span class="sxs-lookup"><span data-stu-id="bd928-308"><span id="__callback"></span><span id="__CALLBACK"></span>\_\_callback</span></span><br/>                                                                        | <span data-ttu-id="bd928-309">La funzione può essere usata come puntatore a funzione.</span><span class="sxs-lookup"><span data-stu-id="bd928-309">The function can be used as a function pointer.</span></span><br/>                                                                                                                                                                                                                      |
| <span data-ttu-id="bd928-310"><span id="__checkReturn"></span><span id="__checkreturn"></span><span id="__CHECKRETURN"></span>\_\_checkReturn</span><span class="sxs-lookup"><span data-stu-id="bd928-310"><span id="__checkReturn"></span><span id="__checkreturn"></span><span id="__CHECKRETURN"></span>\_\_checkReturn</span></span><br/>                               | <span data-ttu-id="bd928-311">I chiamanti devono controllare il valore restituito.</span><span class="sxs-lookup"><span data-stu-id="bd928-311">Callers must check the return value.</span></span><br/>                                                                                                                                                                                                                                 |
| <span data-ttu-id="bd928-312"><span id="__format_string"></span><span id="__FORMAT_STRING"></span>\_\_stringa di formato \_</span><span class="sxs-lookup"><span data-stu-id="bd928-312"><span id="__format_string"></span><span id="__FORMAT_STRING"></span>\_\_format\_string</span></span><br/>                                                        | <span data-ttu-id="bd928-313">Il parametro è una stringa che contiene i marcatori% di tipo printf.</span><span class="sxs-lookup"><span data-stu-id="bd928-313">The parameter is a string that contains printf-style % markers.</span></span><br/>                                                                                                                                                                                                      |
| <span data-ttu-id="bd928-314"><span id="__in_awcount_expr_size_"></span><span id="__IN_AWCOUNT_EXPR_SIZE_"></span>\_\_in \_ awcount (*expr*,*size*)</span><span class="sxs-lookup"><span data-stu-id="bd928-314"><span id="__in_awcount_expr_size_"></span><span id="__IN_AWCOUNT_EXPR_SIZE_"></span>\_\_in\_awcount(*expr*,*size*)</span></span><br/>                            | <span data-ttu-id="bd928-315">Se l'espressione è true all'uscita, la dimensione del buffer di input viene specificata in byte.</span><span class="sxs-lookup"><span data-stu-id="bd928-315">If the expression is true at exit, the size of the input buffer is specified in bytes.</span></span> <span data-ttu-id="bd928-316">Se l'espressione è false, la dimensione viene specificata in Elements.</span><span class="sxs-lookup"><span data-stu-id="bd928-316">If the expression is false, the size is specified in elements.</span></span><br/>                                                                                                                |
| <span data-ttu-id="bd928-317"><span id="__nullnullterminated"></span><span id="__NULLNULLTERMINATED"></span>\_\_nullnullterminated</span><span class="sxs-lookup"><span data-stu-id="bd928-317"><span id="__nullnullterminated"></span><span id="__NULLNULLTERMINATED"></span>\_\_nullnullterminated</span></span><br/>                                          | <span data-ttu-id="bd928-318">È possibile accedere al buffer fino a includere la prima sequenza di due caratteri **null** o puntatori.</span><span class="sxs-lookup"><span data-stu-id="bd928-318">The buffer may be accessed up to and including the first sequence of two **null** characters or pointers.</span></span><br/>                                                                                                                                                            |
| <span data-ttu-id="bd928-319"><span id="__nullterminated"></span><span id="__NULLTERMINATED"></span>\_\_NullTerminated</span><span class="sxs-lookup"><span data-stu-id="bd928-319"><span id="__nullterminated"></span><span id="__NULLTERMINATED"></span>\_\_nullterminated</span></span><br/>                                                      | <span data-ttu-id="bd928-320">È possibile accedere al buffer fino a includere il primo carattere o puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="bd928-320">The buffer may be accessed up to and including the first **null** character or pointer.</span></span><br/>                                                                                                                                                                              |
| <span data-ttu-id="bd928-321"><span id="__out_awcount_expr_size_"></span><span id="__OUT_AWCOUNT_EXPR_SIZE_"></span>\_\_out \_ awcount (*expr*,*size*)</span><span class="sxs-lookup"><span data-stu-id="bd928-321"><span id="__out_awcount_expr_size_"></span><span id="__OUT_AWCOUNT_EXPR_SIZE_"></span>\_\_out\_awcount(*expr*,*size*)</span></span><br/>                         | <span data-ttu-id="bd928-322">Se l'espressione è true all'uscita, la dimensione del buffer di output viene specificata in byte.</span><span class="sxs-lookup"><span data-stu-id="bd928-322">If the expression is true at exit, the size of the output buffer is specified in bytes.</span></span> <span data-ttu-id="bd928-323">Se l'espressione è false, la dimensione viene specificata in Elements.</span><span class="sxs-lookup"><span data-stu-id="bd928-323">If the expression is false, the size is specified in elements.</span></span> <br/>                                                                                                              |
| <span data-ttu-id="bd928-324"><span id="__override"></span><span id="__OVERRIDE"></span>\_\_override</span><span class="sxs-lookup"><span data-stu-id="bd928-324"><span id="__override"></span><span id="__OVERRIDE"></span>\_\_override</span></span><br/>                                                                        | <span data-ttu-id="bd928-325">Specifica il comportamento di override di tipo C# per i metodi virtuali.</span><span class="sxs-lookup"><span data-stu-id="bd928-325">Specifies C#-style override behavior for virtual methods.</span></span><br/>                                                                                                                                                                                                           |
| <span data-ttu-id="bd928-326"><span id="__reserved"></span><span id="__RESERVED"></span>\_\_riservati</span><span class="sxs-lookup"><span data-stu-id="bd928-326"><span id="__reserved"></span><span id="__RESERVED"></span>\_\_reserved</span></span><br/>                                                                        | <span data-ttu-id="bd928-327">Il parametro è riservato per utilizzi futuri e deve essere zero o **null**.</span><span class="sxs-lookup"><span data-stu-id="bd928-327">The parameter is reserved for future use and must be zero or **NULL**.</span></span><br/>                                                                                                                                                                                               |
| <span data-ttu-id="bd928-328"><span id="__success_expr_"></span><span id="__SUCCESS_EXPR_"></span>\_\_operazione riuscita (*expr*)</span><span class="sxs-lookup"><span data-stu-id="bd928-328"><span id="__success_expr_"></span><span id="__SUCCESS_EXPR_"></span>\_\_success(*expr*)</span></span><br/>                                                       | <span data-ttu-id="bd928-329">Se l'espressione è true all'uscita, il chiamante può basarsi su tutte le garanzie specificate da altre annotazioni.</span><span class="sxs-lookup"><span data-stu-id="bd928-329">If the expression is true at exit, the caller can rely on all guarantees specified by other annotations.</span></span> <span data-ttu-id="bd928-330">Se l'espressione è false, il chiamante non può basarsi sulle garanzie.</span><span class="sxs-lookup"><span data-stu-id="bd928-330">If the expression is false, the caller cannot rely on the guarantees.</span></span> <span data-ttu-id="bd928-331">Questa annotazione viene aggiunta automaticamente alle funzioni che restituiscono un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bd928-331">This annotation is automatically added to functions that return an **HRESULT** value.</span></span><br/> |
| <span data-ttu-id="bd928-332"><span id="__typefix_ctype_"></span><span id="__TYPEFIX_CTYPE_"></span>\_\_typefix (*CType*)</span><span class="sxs-lookup"><span data-stu-id="bd928-332"><span id="__typefix_ctype_"></span><span id="__TYPEFIX_CTYPE_"></span>\_\_typefix(*ctype*)</span></span><br/>                                                    | <span data-ttu-id="bd928-333">Considera il parametro come il tipo specificato anziché il tipo dichiarato.</span><span class="sxs-lookup"><span data-stu-id="bd928-333">Treat the parameter as the specified type rather than its declared type.</span></span><br/>                                                                                                                                                                                             |



 

<span data-ttu-id="bd928-334">Negli esempi seguenti vengono illustrati il buffer e le annotazioni avanzate per le funzioni [**DeleteTimerQueueTimer ha provocato**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueuetimer), [**FreeEnvironmentStrings**](/windows/desktop/api/processenv/nf-processenv-freeenvironmentstringsa)e [**UnhandledExceptionFilter**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-unhandledexceptionfilter) .</span><span class="sxs-lookup"><span data-stu-id="bd928-334">The following examples show the buffer and advanced annotations for the [**DeleteTimerQueueTimer**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueuetimer), [**FreeEnvironmentStrings**](/windows/desktop/api/processenv/nf-processenv-freeenvironmentstringsa), and [**UnhandledExceptionFilter**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-unhandledexceptionfilter) functions.</span></span>


```C++
__checkReturn
BOOL
WINAPI
DeleteTimerQueueTimer(
    __in_opt HANDLE TimerQueue,
    __in     HANDLE Timer,
    __in_opt HANDLE CompletionEvent
    );

BOOL
WINAPI
FreeEnvironmentStrings(
    __in __nullnullterminated LPTCH
    );

__callback
LONG
WINAPI
UnhandledExceptionFilter(
    __in struct _EXCEPTION_POINTERS *ExceptionInfo
    );

```



## <a name="related-topics"></a><span data-ttu-id="bd928-335">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bd928-335">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bd928-336">Annotazioni SAL</span><span class="sxs-lookup"><span data-stu-id="bd928-336">SAL Annotations</span></span>](/cpp/c-runtime-library/sal-annotations?view=vs-2019)
</dt> <dt>

[<span data-ttu-id="bd928-337">Procedura guidata: analisi del codice C/C++ per l'identificazione degli errori</span><span class="sxs-lookup"><span data-stu-id="bd928-337">Walkthrough: Analyzing C/C++ Code for Defects</span></span>](/visualstudio/code-quality/walkthrough-analyzing-c-cpp-code-for-defects?view=vs-2015)
</dt> </dl>

 

