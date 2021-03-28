---
title: swapc (SM5-ASM)
description: Esegue uno scambio condizionale per componente dei valori tra due registri di input.
ms.assetid: 3DFCEB82-076E-4AFA-915F-47390A355B7C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46d2ee674a1cb1067594b0e96c739ff8df73b152
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993088"
---
# <a name="swapc-sm5---asm"></a><span data-ttu-id="8e19e-103">swapc (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="8e19e-103">swapc (sm5 - asm)</span></span>

<span data-ttu-id="8e19e-104">Esegue uno scambio condizionale per componente dei valori tra due registri di input.</span><span class="sxs-lookup"><span data-stu-id="8e19e-104">Performs a component-wise conditional swap of the values between two input registers.</span></span>



| <span data-ttu-id="8e19e-105">swapc dest0 \[ . mask \] , DesT1 \[ . mask \] , src0 \[ . Swizzle \] , src1 \[ . Swizzle \] , src2 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="8e19e-105">swapc dest0\[.mask\], dest1\[.mask\], src0\[.swizzle\], src1\[.swizzle\], src2\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="8e19e-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="8e19e-106">Item</span></span>                                                               | <span data-ttu-id="8e19e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8e19e-107">Description</span></span>                                                                                     |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e19e-108"><span id="dest0"></span><span id="DEST0"></span>*dest0*</span><span class="sxs-lookup"><span data-stu-id="8e19e-108"><span id="dest0"></span><span id="DEST0"></span>*dest0*</span></span><br/> | <span data-ttu-id="8e19e-109">\[in \] registra con maschere di scrittura non vuote arbitrarie.</span><span class="sxs-lookup"><span data-stu-id="8e19e-109">\[in\] Register with arbitrary nonempty write masks.</span></span> <span data-ttu-id="8e19e-110">Deve essere diverso da *DesT1*.</span><span class="sxs-lookup"><span data-stu-id="8e19e-110">Must be different than *dest1*.</span></span><br/> |
| <span data-ttu-id="8e19e-111"><span id="dest1"></span><span id="DEST1"></span>*dest1*</span><span class="sxs-lookup"><span data-stu-id="8e19e-111"><span id="dest1"></span><span id="DEST1"></span>*dest1*</span></span><br/> | <span data-ttu-id="8e19e-112">\[in \] registra con maschere di scrittura non vuote arbitrarie.</span><span class="sxs-lookup"><span data-stu-id="8e19e-112">\[in\] Register with arbitrary nonempty write masks.</span></span> <span data-ttu-id="8e19e-113">Deve essere diverso da *dest0*.</span><span class="sxs-lookup"><span data-stu-id="8e19e-113">Must be different than *dest0*.</span></span><br/> |
| <span data-ttu-id="8e19e-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="8e19e-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>    | <span data-ttu-id="8e19e-115">\[in \] fornisce 4 condizioni.</span><span class="sxs-lookup"><span data-stu-id="8e19e-115">\[in\] Provides 4 conditions.</span></span> <span data-ttu-id="8e19e-116">Un valore integer diverso da zero indica **true**.</span><span class="sxs-lookup"><span data-stu-id="8e19e-116">A nonzero integer value means **true**.</span></span> <br/>               |
| <span data-ttu-id="8e19e-117"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="8e19e-117"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/>    | <span data-ttu-id="8e19e-118">\[in \] uno dei valori da scambiare.</span><span class="sxs-lookup"><span data-stu-id="8e19e-118">\[in\] One of the values to be swapped.</span></span><br/>                                              |
| <span data-ttu-id="8e19e-119"><span id="src2"></span><span id="SRC2"></span>*src2*</span><span class="sxs-lookup"><span data-stu-id="8e19e-119"><span id="src2"></span><span id="SRC2"></span>*src2*</span></span><br/>    | <span data-ttu-id="8e19e-120">\[in \] uno dei valori da scambiare.</span><span class="sxs-lookup"><span data-stu-id="8e19e-120">\[in\] One of the values to be swapped.</span></span><br/>                                              |



 

## <a name="remarks"></a><span data-ttu-id="8e19e-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="8e19e-121">Remarks</span></span>

<span data-ttu-id="8e19e-122">La codifica di questa istruzione tenta di esprimere in modo compatto più scambi condizionali paralleli di scalari tra i registri dei componenti 2 4, con una minore flessibilità nella disposizione delle coppie di numeri interessati dallo scambio.</span><span class="sxs-lookup"><span data-stu-id="8e19e-122">The encoding of this instruction attempts to compactly express multiple parallel conditional swaps of scalars across two 4-component registers, with minor flexibility in the arrangement of the pairs of numbers involved in swapping.</span></span>

<span data-ttu-id="8e19e-123">La scelta del registro e del valore per *src0*, *src1* e *src2* non è vincolata in alcun modo, ad esempio [MOVC](movc--sm4---asm-.md).</span><span class="sxs-lookup"><span data-stu-id="8e19e-123">The choice of register and value for *src0*, *src1*, and *src2* are unconstrained in any way, like [movc](movc--sm4---asm-.md).</span></span>

<span data-ttu-id="8e19e-124">La semantica di questa istruzione può essere descritta dalle operazioni equivalenti con l'istruzione **MOVC** .</span><span class="sxs-lookup"><span data-stu-id="8e19e-124">The semantics of this instruction can be described by the equivalent operations with the **movc** instruction.</span></span> <span data-ttu-id="8e19e-125">Il caso peggiore è illustrato nell'esempio seguente, assicurandosi che i registri di destinazione non vengano aggiornati fino alla fine.</span><span class="sxs-lookup"><span data-stu-id="8e19e-125">The worst case is shown in the following example, making sure destination registers are not updated until the end.</span></span>

``` syntax
                swapc dest0[.mask], 
                      dest1[.mask],
                      src0[.swizzle],
                      src1[.swizzle],
                      src2[.swizzle]

                expands to:

                movc temp[dest0 s mask], 
                     src0[.swizzle], 
                     src2[.swizzle], src1[.swizzle]

                movc dest1[.mask], 
                     src0[.swizzle], 
                     src1[.swizzle], src2[.swizzle]

                mov  dest0.mask, temp
```

<span data-ttu-id="8e19e-126">È possibile scegliere come affrontare l'attività, se non direttamente.</span><span class="sxs-lookup"><span data-stu-id="8e19e-126">You can choose how to tackle the task, if not directly.</span></span> <span data-ttu-id="8e19e-127">Ad esempio, lo stesso effetto può essere ottenuto da una sequenza di un massimo di quattro scambi condizionali semplici scalari, o come sopra, due istruzioni **MOVC** vettoriali, oltre a qualsiasi overhead per assicurarsi che i valori di origine non vengano compromessi dalle operazioni precedenti durante l'espansione.</span><span class="sxs-lookup"><span data-stu-id="8e19e-127">For example, the same effect can be achieved by a sequence of up to 4 simple scalar conditional swaps, or as above, two vector **movc** instructions, plus any overhead to make sure the source values are not clobbered by earlier operations in the midst of the expansion.</span></span>

<span data-ttu-id="8e19e-128">Usare questa istruzione per l'ordinamento.</span><span class="sxs-lookup"><span data-stu-id="8e19e-128">Use this instruction for sorting.</span></span>

<span data-ttu-id="8e19e-129">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="8e19e-129">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="8e19e-130">Vertice</span><span class="sxs-lookup"><span data-stu-id="8e19e-130">Vertex</span></span> | <span data-ttu-id="8e19e-131">Hull</span><span class="sxs-lookup"><span data-stu-id="8e19e-131">Hull</span></span> | <span data-ttu-id="8e19e-132">Dominio</span><span class="sxs-lookup"><span data-stu-id="8e19e-132">Domain</span></span> | <span data-ttu-id="8e19e-133">Geometria</span><span class="sxs-lookup"><span data-stu-id="8e19e-133">Geometry</span></span> | <span data-ttu-id="8e19e-134">Pixel</span><span class="sxs-lookup"><span data-stu-id="8e19e-134">Pixel</span></span> | <span data-ttu-id="8e19e-135">Calcolo</span><span class="sxs-lookup"><span data-stu-id="8e19e-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="8e19e-136">X</span><span class="sxs-lookup"><span data-stu-id="8e19e-136">X</span></span>      | <span data-ttu-id="8e19e-137">X</span><span class="sxs-lookup"><span data-stu-id="8e19e-137">X</span></span>    | <span data-ttu-id="8e19e-138">X</span><span class="sxs-lookup"><span data-stu-id="8e19e-138">X</span></span>      | <span data-ttu-id="8e19e-139">X</span><span class="sxs-lookup"><span data-stu-id="8e19e-139">X</span></span>        | <span data-ttu-id="8e19e-140">X</span><span class="sxs-lookup"><span data-stu-id="8e19e-140">X</span></span>     | <span data-ttu-id="8e19e-141">X</span><span class="sxs-lookup"><span data-stu-id="8e19e-141">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="8e19e-142">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="8e19e-142">Minimum Shader Model</span></span>

<span data-ttu-id="8e19e-143">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="8e19e-143">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="8e19e-144">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="8e19e-144">Shader Model</span></span>                                              | <span data-ttu-id="8e19e-145">Supportato</span><span class="sxs-lookup"><span data-stu-id="8e19e-145">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="8e19e-146">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="8e19e-146">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="8e19e-147">sì</span><span class="sxs-lookup"><span data-stu-id="8e19e-147">yes</span></span>       |
| [<span data-ttu-id="8e19e-148">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="8e19e-148">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="8e19e-149">no</span><span class="sxs-lookup"><span data-stu-id="8e19e-149">no</span></span>        |
| [<span data-ttu-id="8e19e-150">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="8e19e-150">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="8e19e-151">no</span><span class="sxs-lookup"><span data-stu-id="8e19e-151">no</span></span>        |
| [<span data-ttu-id="8e19e-152">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8e19e-152">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="8e19e-153">no</span><span class="sxs-lookup"><span data-stu-id="8e19e-153">no</span></span>        |
| [<span data-ttu-id="8e19e-154">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8e19e-154">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="8e19e-155">no</span><span class="sxs-lookup"><span data-stu-id="8e19e-155">no</span></span>        |
| [<span data-ttu-id="8e19e-156">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8e19e-156">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="8e19e-157">no</span><span class="sxs-lookup"><span data-stu-id="8e19e-157">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="8e19e-158">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8e19e-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e19e-159">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8e19e-159">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





