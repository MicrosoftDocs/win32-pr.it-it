---
title: Costanti D3DCOMPILE (D3DCompiler. h)
description: Le costanti D3DCOMPILE specificano la modalità di compilazione del codice HLSL da parte del compilatore.
ms.assetid: 039627DD-D6A4-4EA3-8E91-D2A20770E6FF
topic_type:
- apiref
api_name:
- D3DCOMPILE_DEBUG
- D3DCOMPILE_SKIP_VALIDATION
- D3DCOMPILE_SKIP_OPTIMIZATION
- D3DCOMPILE_PACK_MATRIX_ROW_MAJOR
- D3DCOMPILE_PACK_MATRIX_COLUMN_MAJOR
- D3DCOMPILE_PARTIAL_PRECISION
- D3DCOMPILE_FORCE_VS_SOFTWARE_NO_OPT
- D3DCOMPILE_FORCE_PS_SOFTWARE_NO_OPT
- D3DCOMPILE_NO_PRESHADER
- D3DCOMPILE_AVOID_FLOW_CONTROL
- D3DCOMPILE_PREFER_FLOW_CONTROL
- D3DCOMPILE_ENABLE_STRICTNESS
- D3DCOMPILE_ENABLE_BACKWARDS_COMPATIBILITY
- D3DCOMPILE_IEEE_STRICTNESS
- D3DCOMPILE_OPTIMIZATION_LEVEL0
- D3DCOMPILE_OPTIMIZATION_LEVEL1
- D3DCOMPILE_OPTIMIZATION_LEVEL2
- D3DCOMPILE_OPTIMIZATION_LEVEL3
- D3DCOMPILE_WARNINGS_ARE_ERRORS
- D3DCOMPILE_RESOURCES_MAY_ALIAS
- D3DCOMPILE_ENABLE_UNBOUNDED_DESCRIPTOR_TABLES
- D3DCOMPILE_ALL_RESOURCES_BOUND
api_location:
- D3DCompiler.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfd396eef06260ae879a3bb816d0bd89a078ea53
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104234957"
---
# <a name="d3dcompile-constants"></a><span data-ttu-id="433d6-103">Costanti D3DCOMPILE</span><span class="sxs-lookup"><span data-stu-id="433d6-103">D3DCOMPILE Constants</span></span>

<span data-ttu-id="433d6-104">Le costanti D3DCOMPILE specificano la modalità di compilazione del codice HLSL da parte del compilatore.</span><span class="sxs-lookup"><span data-stu-id="433d6-104">The D3DCOMPILE constants specify how the compiler compiles the HLSL code.</span></span>

<dl> <dt>

<span data-ttu-id="433d6-105"><span id="D3DCOMPILE_DEBUG"></span><span id="d3dcompile_debug"></span>**\_Debug D3DCOMPILE**</span><span class="sxs-lookup"><span data-stu-id="433d6-105"><span id="D3DCOMPILE_DEBUG"></span><span id="d3dcompile_debug"></span>**D3DCOMPILE\_DEBUG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="433d6-106">(1 << 0)</span><span class="sxs-lookup"><span data-stu-id="433d6-106">(1 << 0)</span></span>
</dt> <dt>



<span data-ttu-id="433d6-107">Indica al compilatore di inserire le informazioni relative al file di debug, alla riga, al tipo o al simbolo nel codice di output.</span><span class="sxs-lookup"><span data-stu-id="433d6-107">Directs the compiler to insert debug file/line/type/symbol information into the output code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="433d6-108"><span id="D3DCOMPILE_SKIP_VALIDATION"></span><span id="d3dcompile_skip_validation"></span>**D3DCOMPILE \_ ignorare la \_ convalida**</span><span class="sxs-lookup"><span data-stu-id="433d6-108"><span id="D3DCOMPILE_SKIP_VALIDATION"></span><span id="d3dcompile_skip_validation"></span>**D3DCOMPILE\_SKIP\_VALIDATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="433d6-109">(1 << 1)</span><span class="sxs-lookup"><span data-stu-id="433d6-109">(1 << 1)</span></span>
</dt> <dt>



<span data-ttu-id="433d6-110">Indica al compilatore di non convalidare il codice generato in base alle funzionalità note e ai vincoli.</span><span class="sxs-lookup"><span data-stu-id="433d6-110">Directs the compiler not to validate the generated code against known capabilities and constraints.</span></span> <span data-ttu-id="433d6-111">È consigliabile usare questa costante solo con gli shader che sono stati compilati correttamente in precedenza.</span><span class="sxs-lookup"><span data-stu-id="433d6-111">We recommend that you use this constant only with shaders that have been successfully compiled in the past.</span></span> <span data-ttu-id="433d6-112">DirectX convalida sempre gli shader prima di impostarli su un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="433d6-112">DirectX always validates shaders before it sets them to a device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="433d6-113"><span id="D3DCOMPILE_SKIP_OPTIMIZATION"></span><span id="d3dcompile_skip_optimization"></span>**Ottimizzazione di D3DCOMPILE \_ Skip \_**</span><span class="sxs-lookup"><span data-stu-id="433d6-113"><span id="D3DCOMPILE_SKIP_OPTIMIZATION"></span><span id="d3dcompile_skip_optimization"></span>**D3DCOMPILE\_SKIP\_OPTIMIZATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="433d6-114">(1 << 2)</span><span class="sxs-lookup"><span data-stu-id="433d6-114">(1 << 2)</span></span>
</dt> <dt>



<span data-ttu-id="433d6-115">Indica al compilatore di ignorare i passaggi di ottimizzazione durante la generazione del codice.</span><span class="sxs-lookup"><span data-stu-id="433d6-115">Directs the compiler to skip optimization steps during code generation.</span></span> <span data-ttu-id="433d6-116">Si consiglia di impostare questa costante solo a scopo di debug.</span><span class="sxs-lookup"><span data-stu-id="433d6-116">We recommend that you set this constant for debug purposes only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="433d6-117"><span id="D3DCOMPILE_PACK_MATRIX_ROW_MAJOR"></span><span id="d3dcompile_pack_matrix_row_major"></span>**\_ \_ \_ Riga principale della matrice di D3DCOMPILE Pack \_**</span><span class="sxs-lookup"><span data-stu-id="433d6-117"><span id="D3DCOMPILE_PACK_MATRIX_ROW_MAJOR"></span><span id="d3dcompile_pack_matrix_row_major"></span>**D3DCOMPILE\_PACK\_MATRIX\_ROW\_MAJOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="433d6-118">(1 << 3)</span><span class="sxs-lookup"><span data-stu-id="433d6-118">(1 << 3)</span></span>
</dt> <dt>



<span data-ttu-id="433d6-119">Indica al compilatore di comprimere le matrici in ordine di riga, in base all'input e all'output dello shader.</span><span class="sxs-lookup"><span data-stu-id="433d6-119">Directs the compiler to pack matrices in row-major order on input and output from the shader.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="433d6-120"><span id="D3DCOMPILE_PACK_MATRIX_COLUMN_MAJOR"></span><span id="d3dcompile_pack_matrix_column_major"></span>**\_ \_ Colonna matrice D3DCOMPILE \_ pack \_ principale**</span><span class="sxs-lookup"><span data-stu-id="433d6-120"><span id="D3DCOMPILE_PACK_MATRIX_COLUMN_MAJOR"></span><span id="d3dcompile_pack_matrix_column_major"></span>**D3DCOMPILE\_PACK\_MATRIX\_COLUMN\_MAJOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="433d6-121">(1 << 4)</span><span class="sxs-lookup"><span data-stu-id="433d6-121">(1 << 4)</span></span>
</dt> <dt>



<span data-ttu-id="433d6-122">Indica al compilatore di comprimere matrici in base all'ordine delle colonne in base all'input e all'output dello shader.</span><span class="sxs-lookup"><span data-stu-id="433d6-122">Directs the compiler to pack matrices in column-major order on input and output from the shader.</span></span> <span data-ttu-id="433d6-123">Questo tipo di compressione è in genere più efficiente perché una serie di prodotti punto può quindi eseguire la moltiplicazione della matrice vettoriale.</span><span class="sxs-lookup"><span data-stu-id="433d6-123">This type of packing is generally more efficient because a series of dot-products can then perform vector-matrix multiplication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="433d6-124"><span id="D3DCOMPILE_PARTIAL_PRECISION"></span><span id="d3dcompile_partial_precision"></span>**\_Precisione parziale \_ D3DCOMPILE**</span><span class="sxs-lookup"><span data-stu-id="433d6-124"><span id="D3DCOMPILE_PARTIAL_PRECISION"></span><span id="d3dcompile_partial_precision"></span>**D3DCOMPILE\_PARTIAL\_PRECISION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="433d6-125">(1 << 5)</span><span class="sxs-lookup"><span data-stu-id="433d6-125">(1 << 5)</span></span>
</dt> <dt>



<span data-ttu-id="433d6-126">Indica al compilatore di eseguire tutti i calcoli con precisione parziale.</span><span class="sxs-lookup"><span data-stu-id="433d6-126">Directs the compiler to perform all computations with partial precision.</span></span> <span data-ttu-id="433d6-127">Se si imposta questa costante, il codice compilato potrebbe essere eseguito più velocemente su hardware.</span><span class="sxs-lookup"><span data-stu-id="433d6-127">If you set this constant, the compiled code might run faster on some hardware.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="433d6-128"><span id="D3DCOMPILE_FORCE_VS_SOFTWARE_NO_OPT"></span><span id="d3dcompile_force_vs_software_no_opt"></span>**D3DCOMPILE \_ Force \_ vs \_ software \_ No \_ opt**</span><span class="sxs-lookup"><span data-stu-id="433d6-128"><span id="D3DCOMPILE_FORCE_VS_SOFTWARE_NO_OPT"></span><span id="d3dcompile_force_vs_software_no_opt"></span>**D3DCOMPILE\_FORCE\_VS\_SOFTWARE\_NO\_OPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="433d6-129">(1 << 6)</span><span class="sxs-lookup"><span data-stu-id="433d6-129">(1 << 6)</span></span>
</dt> <dt>



<span data-ttu-id="433d6-130">Indica al compilatore di compilare un vertex shader per il successivo profilo dello shader più alto.</span><span class="sxs-lookup"><span data-stu-id="433d6-130">Directs the compiler to compile a vertex shader for the next highest shader profile.</span></span> <span data-ttu-id="433d6-131">Questa costante disattiva il debug e le ottimizzazioni.</span><span class="sxs-lookup"><span data-stu-id="433d6-131">This constant turns debugging on and optimizations off.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="433d6-132"><span id="D3DCOMPILE_FORCE_PS_SOFTWARE_NO_OPT"></span><span id="d3dcompile_force_ps_software_no_opt"></span>**D3DCOMPILE \_ Force \_ PS \_ software \_ No \_ opt**</span><span class="sxs-lookup"><span data-stu-id="433d6-132"><span id="D3DCOMPILE_FORCE_PS_SOFTWARE_NO_OPT"></span><span id="d3dcompile_force_ps_software_no_opt"></span>**D3DCOMPILE\_FORCE\_PS\_SOFTWARE\_NO\_OPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="433d6-133">(1 << 7)</span><span class="sxs-lookup"><span data-stu-id="433d6-133">(1 << 7)</span></span>
</dt> <dt>



<span data-ttu-id="433d6-134">Indica al compilatore di compilare un pixel shader per il successivo profilo dello shader più alto.</span><span class="sxs-lookup"><span data-stu-id="433d6-134">Directs the compiler to compile a pixel shader for the next highest shader profile.</span></span> <span data-ttu-id="433d6-135">Questa costante disattiva anche il debug e le ottimizzazioni.</span><span class="sxs-lookup"><span data-stu-id="433d6-135">This constant also turns debugging on and optimizations off.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="433d6-136"><span id="D3DCOMPILE_NO_PRESHADER"></span><span id="d3dcompile_no_preshader"></span>**D3DCOMPILE \_ senza \_ preshader**</span><span class="sxs-lookup"><span data-stu-id="433d6-136"><span id="D3DCOMPILE_NO_PRESHADER"></span><span id="d3dcompile_no_preshader"></span>**D3DCOMPILE\_NO\_PRESHADER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="433d6-137">(1 << 8)</span><span class="sxs-lookup"><span data-stu-id="433d6-137">(1 << 8)</span></span>
</dt> <dt>



<span data-ttu-id="433d6-138">Indica al compilatore di disabilitare i preshader.</span><span class="sxs-lookup"><span data-stu-id="433d6-138">Directs the compiler to disable Preshaders.</span></span> <span data-ttu-id="433d6-139">Se si imposta questa costante, il compilatore non estrae l'espressione statica per la valutazione.</span><span class="sxs-lookup"><span data-stu-id="433d6-139">If you set this constant, the compiler does not pull out static expression for evaluation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="433d6-140"><span id="D3DCOMPILE_AVOID_FLOW_CONTROL"></span><span id="d3dcompile_avoid_flow_control"></span>**D3DCOMPILE \_ evitare \_ il \_ controllo di flusso**</span><span class="sxs-lookup"><span data-stu-id="433d6-140"><span id="D3DCOMPILE_AVOID_FLOW_CONTROL"></span><span id="d3dcompile_avoid_flow_control"></span>**D3DCOMPILE\_AVOID\_FLOW\_CONTROL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="433d6-141">(1 << 9)</span><span class="sxs-lookup"><span data-stu-id="433d6-141">(1 << 9)</span></span>
</dt> <dt>



<span data-ttu-id="433d6-142">Indica al compilatore di non usare i costrutti di controllo del flusso laddove possibile.</span><span class="sxs-lookup"><span data-stu-id="433d6-142">Directs the compiler to not use flow-control constructs where possible.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="433d6-143"><span id="D3DCOMPILE_PREFER_FLOW_CONTROL"></span><span id="d3dcompile_prefer_flow_control"></span>**D3DCOMPILE \_ preferisce \_ il \_ controllo di flusso**</span><span class="sxs-lookup"><span data-stu-id="433d6-143"><span id="D3DCOMPILE_PREFER_FLOW_CONTROL"></span><span id="d3dcompile_prefer_flow_control"></span>**D3DCOMPILE\_PREFER\_FLOW\_CONTROL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="433d6-144">(1 << 10)</span><span class="sxs-lookup"><span data-stu-id="433d6-144">(1 << 10)</span></span>
</dt> <dt>



<span data-ttu-id="433d6-145">Indica al compilatore di usare i costrutti di controllo del flusso laddove possibile.</span><span class="sxs-lookup"><span data-stu-id="433d6-145">Directs the compiler to use flow-control constructs where possible.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="433d6-146"><span id="D3DCOMPILE_ENABLE_STRICTNESS"></span><span id="d3dcompile_enable_strictness"></span>**D3DCOMPILE \_ Abilita la \_ rigidità**</span><span class="sxs-lookup"><span data-stu-id="433d6-146"><span id="D3DCOMPILE_ENABLE_STRICTNESS"></span><span id="d3dcompile_enable_strictness"></span>**D3DCOMPILE\_ENABLE\_STRICTNESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="433d6-147">(1 << 11)</span><span class="sxs-lookup"><span data-stu-id="433d6-147">(1 << 11)</span></span>
</dt> <dt>



<span data-ttu-id="433d6-148">Forza la compilazione strict, che potrebbe non consentire la sintassi legacy.</span><span class="sxs-lookup"><span data-stu-id="433d6-148">Forces strict compile, which might not allow for legacy syntax.</span></span>

<span data-ttu-id="433d6-149">Per impostazione predefinita, il compilatore Disabilita la limitazione della sintassi deprecata.</span><span class="sxs-lookup"><span data-stu-id="433d6-149">By default, the compiler disables strictness on deprecated syntax.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="433d6-150"><span id="D3DCOMPILE_ENABLE_BACKWARDS_COMPATIBILITY"></span><span id="d3dcompile_enable_backwards_compatibility"></span>**D3DCOMPILE \_ Abilita \_ compatibilità con le versioni precedenti \_**</span><span class="sxs-lookup"><span data-stu-id="433d6-150"><span id="D3DCOMPILE_ENABLE_BACKWARDS_COMPATIBILITY"></span><span id="d3dcompile_enable_backwards_compatibility"></span>**D3DCOMPILE\_ENABLE\_BACKWARDS\_COMPATIBILITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="433d6-151">(1 << 12)</span><span class="sxs-lookup"><span data-stu-id="433d6-151">(1 << 12)</span></span>
</dt> <dt>



<span data-ttu-id="433d6-152">Indica al compilatore di abilitare gli shader meno recenti da compilare fino a 5 \_ 0 destinazioni.</span><span class="sxs-lookup"><span data-stu-id="433d6-152">Directs the compiler to enable older shaders to compile to 5\_0 targets.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="433d6-153"><span id="D3DCOMPILE_IEEE_STRICTNESS"></span><span id="d3dcompile_ieee_strictness"></span>**D3DCOMPILE \_ IEEE \_ strictity**</span><span class="sxs-lookup"><span data-stu-id="433d6-153"><span id="D3DCOMPILE_IEEE_STRICTNESS"></span><span id="d3dcompile_ieee_strictness"></span>**D3DCOMPILE\_IEEE\_STRICTNESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="433d6-154">(1 << 13)</span><span class="sxs-lookup"><span data-stu-id="433d6-154">(1 << 13)</span></span>
</dt> <dt>



<span data-ttu-id="433d6-155">Impone la compilazione di IEEE Strict.</span><span class="sxs-lookup"><span data-stu-id="433d6-155">Forces the IEEE strict compile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="433d6-156"><span id="D3DCOMPILE_OPTIMIZATION_LEVEL0"></span><span id="d3dcompile_optimization_level0"></span>**\_Ottimizzazione D3DCOMPILE \_ level0**</span><span class="sxs-lookup"><span data-stu-id="433d6-156"><span id="D3DCOMPILE_OPTIMIZATION_LEVEL0"></span><span id="d3dcompile_optimization_level0"></span>**D3DCOMPILE\_OPTIMIZATION\_LEVEL0**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="433d6-157">(1 << 14)</span><span class="sxs-lookup"><span data-stu-id="433d6-157">(1 << 14)</span></span>
</dt> <dt>



<span data-ttu-id="433d6-158">Indica al compilatore di utilizzare il livello di ottimizzazione più basso.</span><span class="sxs-lookup"><span data-stu-id="433d6-158">Directs the compiler to use the lowest optimization level.</span></span> <span data-ttu-id="433d6-159">Se si imposta questa costante, il compilatore potrebbe produrre codice più lento, ma produrrà il codice più rapidamente.</span><span class="sxs-lookup"><span data-stu-id="433d6-159">If you set this constant, the compiler might produce slower code but produces the code more quickly.</span></span> <span data-ttu-id="433d6-160">Impostare questa costante quando si sviluppa lo shader in modo iterativo.</span><span class="sxs-lookup"><span data-stu-id="433d6-160">Set this constant when you develop the shader iteratively.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="433d6-161"><span id="D3DCOMPILE_OPTIMIZATION_LEVEL1"></span><span id="d3dcompile_optimization_level1"></span>**\_Ottimizzazione D3DCOMPILE \_ Level1**</span><span class="sxs-lookup"><span data-stu-id="433d6-161"><span id="D3DCOMPILE_OPTIMIZATION_LEVEL1"></span><span id="d3dcompile_optimization_level1"></span>**D3DCOMPILE\_OPTIMIZATION\_LEVEL1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="433d6-162">0</span><span class="sxs-lookup"><span data-stu-id="433d6-162">0</span></span>
</dt> <dt>



<span data-ttu-id="433d6-163">Indica al compilatore di utilizzare il secondo livello di ottimizzazione più basso.</span><span class="sxs-lookup"><span data-stu-id="433d6-163">Directs the compiler to use the second lowest optimization level.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="433d6-164"><span id="D3DCOMPILE_OPTIMIZATION_LEVEL2"></span><span id="d3dcompile_optimization_level2"></span>**\_Ottimizzazione D3DCOMPILE \_ Level2**</span><span class="sxs-lookup"><span data-stu-id="433d6-164"><span id="D3DCOMPILE_OPTIMIZATION_LEVEL2"></span><span id="d3dcompile_optimization_level2"></span>**D3DCOMPILE\_OPTIMIZATION\_LEVEL2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="433d6-165">((1 << 14) \| (1 << 15))</span><span class="sxs-lookup"><span data-stu-id="433d6-165">((1 << 14) \| (1 << 15))</span></span>
</dt> <dt>



<span data-ttu-id="433d6-166">Indica al compilatore di utilizzare il secondo livello di ottimizzazione più elevato.</span><span class="sxs-lookup"><span data-stu-id="433d6-166">Directs the compiler to use the second highest optimization level.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="433d6-167"><span id="D3DCOMPILE_OPTIMIZATION_LEVEL3"></span><span id="d3dcompile_optimization_level3"></span>**\_Ottimizzazione D3DCOMPILE \_ Level3**</span><span class="sxs-lookup"><span data-stu-id="433d6-167"><span id="D3DCOMPILE_OPTIMIZATION_LEVEL3"></span><span id="d3dcompile_optimization_level3"></span>**D3DCOMPILE\_OPTIMIZATION\_LEVEL3**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="433d6-168">(1 << 15)</span><span class="sxs-lookup"><span data-stu-id="433d6-168">(1 << 15)</span></span>
</dt> <dt>



<span data-ttu-id="433d6-169">Indica al compilatore di usare il livello di ottimizzazione più elevato.</span><span class="sxs-lookup"><span data-stu-id="433d6-169">Directs the compiler to use the highest optimization level.</span></span> <span data-ttu-id="433d6-170">Se si imposta questa costante, il compilatore produce il migliore codice possibile, ma può richiedere molto più tempo.</span><span class="sxs-lookup"><span data-stu-id="433d6-170">If you set this constant, the compiler produces the best possible code but might take significantly longer to do so.</span></span> <span data-ttu-id="433d6-171">Impostare questa costante per le compilazioni finali di un'applicazione quando le prestazioni sono il fattore più importante.</span><span class="sxs-lookup"><span data-stu-id="433d6-171">Set this constant for final builds of an application when performance is the most important factor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="433d6-172"><span id="D3DCOMPILE_WARNINGS_ARE_ERRORS"></span><span id="d3dcompile_warnings_are_errors"></span>**Gli \_ avvisi di D3DCOMPILE \_ sono \_ errori**</span><span class="sxs-lookup"><span data-stu-id="433d6-172"><span id="D3DCOMPILE_WARNINGS_ARE_ERRORS"></span><span id="d3dcompile_warnings_are_errors"></span>**D3DCOMPILE\_WARNINGS\_ARE\_ERRORS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="433d6-173">(1 << 18)</span><span class="sxs-lookup"><span data-stu-id="433d6-173">(1 << 18)</span></span>
</dt> <dt>



<span data-ttu-id="433d6-174">Indica al compilatore di considerare tutti gli avvisi come errori durante la compilazione del codice dello shader.</span><span class="sxs-lookup"><span data-stu-id="433d6-174">Directs the compiler to treat all warnings as errors when it compiles the shader code.</span></span> <span data-ttu-id="433d6-175">Si consiglia di usare questa costante per il nuovo codice dello shader, in modo che sia possibile risolvere tutti gli avvisi e ridurre il numero di difetti del codice di difficile individuazione.</span><span class="sxs-lookup"><span data-stu-id="433d6-175">We recommend that you use this constant for new shader code, so that you can resolve all warnings and lower the number of hard-to-find code defects.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="433d6-176"><span id="D3DCOMPILE_RESOURCES_MAY_ALIAS"></span><span id="d3dcompile_resources_may_alias"></span>**\_Alias delle risorse di D3DCOMPILE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="433d6-176"><span id="D3DCOMPILE_RESOURCES_MAY_ALIAS"></span><span id="d3dcompile_resources_may_alias"></span>**D3DCOMPILE\_RESOURCES\_MAY\_ALIAS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="433d6-177">(1 << 19)</span><span class="sxs-lookup"><span data-stu-id="433d6-177">(1 << 19)</span></span>
</dt> <dt>



<span data-ttu-id="433d6-178">Indica al compilatore di presumere che le visualizzazioni di accesso non ordinate (UAV) e le visualizzazioni delle risorse dello shader (SRVs) possano avere alias per cs \_ 5 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="433d6-178">Directs the compiler to assume that unordered access views (UAVs) and shader resource views (SRVs) may alias for cs\_5\_0.</span></span>

> [!Note]  
> <span data-ttu-id="433d6-179">Questa costante del compilatore è nuova a partire da D3dcompiler \_47.dll.</span><span class="sxs-lookup"><span data-stu-id="433d6-179">This compiler constant is new starting with the D3dcompiler\_47.dll.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="433d6-180"><span id="D3DCOMPILE_ENABLE_UNBOUNDED_DESCRIPTOR_TABLES"></span><span id="d3dcompile_enable_unbounded_descriptor_tables"></span>**D3DCOMPILE \_ Abilita \_ \_ tabelle descrittore senza limiti \_**</span><span class="sxs-lookup"><span data-stu-id="433d6-180"><span id="D3DCOMPILE_ENABLE_UNBOUNDED_DESCRIPTOR_TABLES"></span><span id="d3dcompile_enable_unbounded_descriptor_tables"></span>**D3DCOMPILE\_ENABLE\_UNBOUNDED\_DESCRIPTOR\_TABLES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="433d6-181">(1 << 20)</span><span class="sxs-lookup"><span data-stu-id="433d6-181">(1 << 20)</span></span>
</dt> <dt>



<span data-ttu-id="433d6-182">Indica al compilatore di abilitare le tabelle di descrittori non vincolate.</span><span class="sxs-lookup"><span data-stu-id="433d6-182">Directs the compiler to enable unbounded descriptor tables.</span></span>

> [!Note]  
> <span data-ttu-id="433d6-183">Questa costante del compilatore è nuova a partire da D3dcompiler \_47.dll.</span><span class="sxs-lookup"><span data-stu-id="433d6-183">This compiler constant is new starting with the D3dcompiler\_47.dll.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="433d6-184"><span id="D3DCOMPILE_ALL_RESOURCES_BOUND"></span><span id="d3dcompile_all_resources_bound"></span>**D3DCOMPILE \_ tutte \_ le risorse \_ associato**</span><span class="sxs-lookup"><span data-stu-id="433d6-184"><span id="D3DCOMPILE_ALL_RESOURCES_BOUND"></span><span id="d3dcompile_all_resources_bound"></span>**D3DCOMPILE\_ALL\_RESOURCES\_BOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="433d6-185">(1 << 21)</span><span class="sxs-lookup"><span data-stu-id="433d6-185">(1 << 21)</span></span>
</dt> <dt>



<span data-ttu-id="433d6-186">Indica al compilatore di verificare che tutte le risorse siano associate.</span><span class="sxs-lookup"><span data-stu-id="433d6-186">Directs the compiler to ensure all resources are bound.</span></span>

> [!Note]  
> <span data-ttu-id="433d6-187">Questa costante del compilatore è nuova a partire da D3dcompiler \_47.dll.</span><span class="sxs-lookup"><span data-stu-id="433d6-187">This compiler constant is new starting with the D3dcompiler\_47.dll.</span></span>

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="433d6-188">Requisiti</span><span class="sxs-lookup"><span data-stu-id="433d6-188">Requirements</span></span>



| <span data-ttu-id="433d6-189">Requisito</span><span class="sxs-lookup"><span data-stu-id="433d6-189">Requirement</span></span> | <span data-ttu-id="433d6-190">Valore</span><span class="sxs-lookup"><span data-stu-id="433d6-190">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="433d6-191">Intestazione</span><span class="sxs-lookup"><span data-stu-id="433d6-191">Header</span></span><br/> | <dl> <span data-ttu-id="433d6-192"><dt>D3DCompiler. h</dt></span><span class="sxs-lookup"><span data-stu-id="433d6-192"><dt>D3DCompiler.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="433d6-193">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="433d6-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="433d6-194">Costanti D3DCompiler</span><span class="sxs-lookup"><span data-stu-id="433d6-194">D3DCompiler Constants</span></span>](dx-graphics-d3dcompiler-reference-constants.md)
</dt> </dl>

 

 





