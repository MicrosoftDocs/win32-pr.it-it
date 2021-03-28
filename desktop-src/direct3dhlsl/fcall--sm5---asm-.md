---
title: fcall (SM5-ASM)
description: Chiamata di funzione dell'interfaccia.
ms.assetid: C21784A0-D2F4-4DDE-9AC4-4F21351BCA6E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c57ea40fec51cf4155b0932f6ce4a7b80d3180dd
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398290"
---
# <a name="fcall-sm5---asm"></a><span data-ttu-id="b3f6f-103">fcall (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="b3f6f-103">fcall (sm5 - asm)</span></span>

<span data-ttu-id="b3f6f-104">Chiamata di funzione dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="b3f6f-104">Interface function call.</span></span>



| <span data-ttu-id="b3f6f-105">fcall FP \# \[ arrayIndex \] \[ chiamata\]</span><span class="sxs-lookup"><span data-stu-id="b3f6f-105">fcall fp\#\[arrayIndex\]\[callSite\]</span></span> |
|--------------------------------------|



 



| <span data-ttu-id="b3f6f-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="b3f6f-106">Item</span></span>                                                                                                           | <span data-ttu-id="b3f6f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b3f6f-107">Description</span></span>                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3f6f-108"><span id="fp_"></span><span id="FP_"></span>*FP\#*</span><span class="sxs-lookup"><span data-stu-id="b3f6f-108"><span id="fp_"></span><span id="FP_"></span>*fp\#*</span></span><br/>                                                  | <span data-ttu-id="b3f6f-109">\[nel \] puntatore a funzione.</span><span class="sxs-lookup"><span data-stu-id="b3f6f-109">\[in\] The function pointer.</span></span><br/>                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="b3f6f-110"><span id="arrayIndex"></span><span id="arrayindex"></span><span id="ARRAYINDEX"></span>*arrayIndex*</span><span class="sxs-lookup"><span data-stu-id="b3f6f-110"><span id="arrayIndex"></span><span id="arrayindex"></span><span id="ARRAYINDEX"></span>*arrayIndex*</span></span><br/> | <span data-ttu-id="b3f6f-111">\[in \] facoltativo.</span><span class="sxs-lookup"><span data-stu-id="b3f6f-111">\[in\] Optional.</span></span> <span data-ttu-id="b3f6f-112">Specifica un offset nella matrice del puntatore a funzione.</span><span class="sxs-lookup"><span data-stu-id="b3f6f-112">Specifies an offset into the function pointer array.</span></span> <span data-ttu-id="b3f6f-113">Questo parametro deve essere un valore letterale Unsigned Integer se FP \# non è stato dichiarato come indicizzabile.</span><span class="sxs-lookup"><span data-stu-id="b3f6f-113">This parameter must be a literal unsigned integer if fp\# was not declared as indexable.</span></span> <span data-ttu-id="b3f6f-114">In caso contrario, arrayIndex può essere del formato letterale base + offset da un registro shader.</span><span class="sxs-lookup"><span data-stu-id="b3f6f-114">Otherwise, arrayIndex may be of the form literal base + offset from a shader register.</span></span> <span data-ttu-id="b3f6f-115">Ad esempio, fcall FP1 \[ R1. w + 0 \] \[ 0 \] .</span><span class="sxs-lookup"><span data-stu-id="b3f6f-115">For example, fcall fp1\[r1.w + 0\]\[0\] .</span></span><br/> |
| <span data-ttu-id="b3f6f-116"><span id="_callSite"></span><span id="_callsite"></span><span id="_CALLSITE"></span>*chiamata*</span><span class="sxs-lookup"><span data-stu-id="b3f6f-116"><span id="_callSite"></span><span id="_callsite"></span><span id="_CALLSITE"></span> *callSite*</span></span><br/>     | <span data-ttu-id="b3f6f-117">\[in \] facoltativo.</span><span class="sxs-lookup"><span data-stu-id="b3f6f-117">\[in\] Optional.</span></span> <span data-ttu-id="b3f6f-118">Un valore letterale Unsigned Integer offset nella tabella della funzione selezionata, selezionando un corpo della funzione FB \# da eseguire.</span><span class="sxs-lookup"><span data-stu-id="b3f6f-118">A literal unsigned integer offset into the selected function table, selecting a function body fb\# to execute.</span></span> <br/>                                                                                                                                                                |



 

## <a name="remarks"></a><span data-ttu-id="b3f6f-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="b3f6f-119">Remarks</span></span>

<span data-ttu-id="b3f6f-120">*FP \#* \[  \] \[ arrayIndex \] viene risolto in una particolare tabella di funzioni, selezionata dall'API al di fuori dello shader dalle opzioni della tabella di funzioni elencate nella dichiarazione di *FP \#*.</span><span class="sxs-lookup"><span data-stu-id="b3f6f-120">*fp\#*\[*arrayIndex*\]\[\] resolves to a particular function table, selected from the API outside the shader from the function table choices listed in the declaration of *fp\#*.</span></span>

<span data-ttu-id="b3f6f-121">La somma di \# in *FP \#* e *arrayIndex* consente di selezionare la tabella function.</span><span class="sxs-lookup"><span data-stu-id="b3f6f-121">The sum of \# in *fp\#* and *arrayIndex* select the function table.</span></span> <span data-ttu-id="b3f6f-122">Se, ad esempio, un'interfaccia viene dichiarata come 4PQ \[ 4 \] \[ 3 \] (dimensione della matrice 4), i **fcall** seguenti sono equivalenti: fcall 4PQ \[ 2 \] \[ 3 \] e FP5 \[ 1 \] \[ 3 \] , perché 4 + 2 = 5 + 1.</span><span class="sxs-lookup"><span data-stu-id="b3f6f-122">For example, if an interface is declared as fp4\[4\]\[3\] (array size of 4), the following **fcall** s are equivalent: fcall fp4\[2\]\[3\] and fp5\[1\]\[3\], because 4+2 = 5+1.</span></span>

### <a name="restrictions"></a><span data-ttu-id="b3f6f-123">Restrizioni</span><span class="sxs-lookup"><span data-stu-id="b3f6f-123">Restrictions</span></span>

-   <span data-ttu-id="b3f6f-124">Se *arrayIndex* usa l'indicizzazione dinamica, il comportamento non è definito se *arrayIndex* diverge sulle chiamate shader adiacenti, che potrebbero essere in esecuzione in contemporanea.</span><span class="sxs-lookup"><span data-stu-id="b3f6f-124">If *arrayIndex* uses dynamic indexing, behavior is undefined if *arrayIndex* diverges on adjacent shader invocations, which could be executing in lockstep.</span></span> <span data-ttu-id="b3f6f-125">Il compilatore HLSL tenterà di non consentire questo caso.</span><span class="sxs-lookup"><span data-stu-id="b3f6f-125">The HLSL compiler will attempt to disallow this case.</span></span>

    <span data-ttu-id="b3f6f-126">Le chiamate adiacenti possono essere inattive a causa del controllo di flusso, perché non interrompe l'esecuzione del contemporanea.</span><span class="sxs-lookup"><span data-stu-id="b3f6f-126">Adjacent invocations can be inactive due to flow control, because it doesn t break lockstep execution.</span></span>

-   <span data-ttu-id="b3f6f-127">Se *FP \#*  +  *arrayIndex* specifica un indice fuori limite, il comportamento non è definito.</span><span class="sxs-lookup"><span data-stu-id="b3f6f-127">If *fp\#* + *arrayIndex* specifies an out of bounds index, behavior is undefined.</span></span>
-   <span data-ttu-id="b3f6f-128">Per i casi non definiti descritti, significa che il comportamento del dispositivo D3D corrente diventa non definito, inclusa la possibilità di perdita del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b3f6f-128">For the undefined cases described here, it means the behavior of the current D3D device becomes undefined, including the possibility of Device Lost.</span></span> <span data-ttu-id="b3f6f-129">Tuttavia, non sarà possibile accedere alla memoria esterna al dispositivo D3D corrente o eseguirla come codice.</span><span class="sxs-lookup"><span data-stu-id="b3f6f-129">However no memory outside the current D3D device will be accessed or executed as code.</span></span>

<span data-ttu-id="b3f6f-130">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="b3f6f-130">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="b3f6f-131">Vertice</span><span class="sxs-lookup"><span data-stu-id="b3f6f-131">Vertex</span></span> | <span data-ttu-id="b3f6f-132">Hull</span><span class="sxs-lookup"><span data-stu-id="b3f6f-132">Hull</span></span> | <span data-ttu-id="b3f6f-133">Dominio</span><span class="sxs-lookup"><span data-stu-id="b3f6f-133">Domain</span></span> | <span data-ttu-id="b3f6f-134">Geometria</span><span class="sxs-lookup"><span data-stu-id="b3f6f-134">Geometry</span></span> | <span data-ttu-id="b3f6f-135">Pixel</span><span class="sxs-lookup"><span data-stu-id="b3f6f-135">Pixel</span></span> | <span data-ttu-id="b3f6f-136">Calcolo</span><span class="sxs-lookup"><span data-stu-id="b3f6f-136">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="b3f6f-137">X</span><span class="sxs-lookup"><span data-stu-id="b3f6f-137">X</span></span>      | <span data-ttu-id="b3f6f-138">X</span><span class="sxs-lookup"><span data-stu-id="b3f6f-138">X</span></span>    | <span data-ttu-id="b3f6f-139">X</span><span class="sxs-lookup"><span data-stu-id="b3f6f-139">X</span></span>      | <span data-ttu-id="b3f6f-140">X</span><span class="sxs-lookup"><span data-stu-id="b3f6f-140">X</span></span>        | <span data-ttu-id="b3f6f-141">X</span><span class="sxs-lookup"><span data-stu-id="b3f6f-141">X</span></span>     | <span data-ttu-id="b3f6f-142">X</span><span class="sxs-lookup"><span data-stu-id="b3f6f-142">X</span></span>       |



 

### <a name="minimum-shader-model"></a><span data-ttu-id="b3f6f-143">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="b3f6f-143">Minimum Shader Model</span></span>

<span data-ttu-id="b3f6f-144">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="b3f6f-144">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="b3f6f-145">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="b3f6f-145">Shader Model</span></span>                                              | <span data-ttu-id="b3f6f-146">Supportato</span><span class="sxs-lookup"><span data-stu-id="b3f6f-146">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="b3f6f-147">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="b3f6f-147">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="b3f6f-148">sì</span><span class="sxs-lookup"><span data-stu-id="b3f6f-148">yes</span></span>       |
| [<span data-ttu-id="b3f6f-149">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="b3f6f-149">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="b3f6f-150">no</span><span class="sxs-lookup"><span data-stu-id="b3f6f-150">no</span></span>        |
| [<span data-ttu-id="b3f6f-151">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="b3f6f-151">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="b3f6f-152">no</span><span class="sxs-lookup"><span data-stu-id="b3f6f-152">no</span></span>        |
| [<span data-ttu-id="b3f6f-153">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b3f6f-153">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="b3f6f-154">no</span><span class="sxs-lookup"><span data-stu-id="b3f6f-154">no</span></span>        |
| [<span data-ttu-id="b3f6f-155">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b3f6f-155">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="b3f6f-156">no</span><span class="sxs-lookup"><span data-stu-id="b3f6f-156">no</span></span>        |
| [<span data-ttu-id="b3f6f-157">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b3f6f-157">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="b3f6f-158">no</span><span class="sxs-lookup"><span data-stu-id="b3f6f-158">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="b3f6f-159">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b3f6f-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3f6f-160">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b3f6f-160">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





