---
title: rcp (sm5 - asm)
description: Reciproco a livello di componente.
ms.assetid: 499A14D6-36DB-4860-94D1-887D931E60D4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa37499a981bae86333b071c2e96a37ccb8ac1a6
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998248"
---
# <a name="rcp-sm5---asm"></a><span data-ttu-id="0928a-103">rcp (sm5 - asm)</span><span class="sxs-lookup"><span data-stu-id="0928a-103">rcp (sm5 - asm)</span></span>

<span data-ttu-id="0928a-104">Reciproco a livello di componente.</span><span class="sxs-lookup"><span data-stu-id="0928a-104">Component-wise reciprocal.</span></span>



| <span data-ttu-id="0928a-105">rcp \[ \_ sat \] dest \[ .mask \] , \[ - \] src0 \[ \_ abs \] \[ .swizzle\]</span><span class="sxs-lookup"><span data-stu-id="0928a-105">rcp\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------|



 



| <span data-ttu-id="0928a-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="0928a-106">Item</span></span>                                                            | <span data-ttu-id="0928a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0928a-107">Description</span></span>                                                                         |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0928a-108"><span id="dest"></span><span id="DEST"></span>*Dest*</span><span class="sxs-lookup"><span data-stu-id="0928a-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="0928a-109">\[in \] Indirizzo dei risultati</span><span class="sxs-lookup"><span data-stu-id="0928a-109">\[in\] The address of the results</span></span><br/> <span data-ttu-id="0928a-110">*dest*  =  **1.0f**  /  *src0*.</span><span class="sxs-lookup"><span data-stu-id="0928a-110">*dest* = **1.0f** / *src0*.</span></span><br/> |
| <span data-ttu-id="0928a-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="0928a-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="0928a-112">\[in \] Numero di cui prendere il reciproco.</span><span class="sxs-lookup"><span data-stu-id="0928a-112">\[in\] The number to take the reciprocal of.</span></span><br/>                             |



 

## <a name="remarks"></a><span data-ttu-id="0928a-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="0928a-113">Remarks</span></span>

<span data-ttu-id="0928a-114">Usare questa istruzione per il reciproco a precisione ridotta, indipendentemente dai requisiti rigorosi per la divisione.</span><span class="sxs-lookup"><span data-stu-id="0928a-114">Use this instruction for reduced precision reciprocal, independent of the strict requirements for divide.</span></span>

<span data-ttu-id="0928a-115">L'errore relativo massimo è 2-21.</span><span class="sxs-lookup"><span data-stu-id="0928a-115">Maximum relative error is 2-21.</span></span> <span data-ttu-id="0928a-116">(La tolleranza di errore corrisponde solo a rsq)</span><span class="sxs-lookup"><span data-stu-id="0928a-116">(The error tolerance just matches rsq)</span></span>

<span data-ttu-id="0928a-117">La tabella seguente mostra i risultati ottenuti quando si esegue l'istruzione con varie classi di numeri.</span><span class="sxs-lookup"><span data-stu-id="0928a-117">The following table shows the results obtained when executing the instruction with various classes of numbers.</span></span>



| <span data-ttu-id="0928a-118">*src*</span><span class="sxs-lookup"><span data-stu-id="0928a-118">*src*</span></span>  | <span data-ttu-id="0928a-119">**-inf**</span><span class="sxs-lookup"><span data-stu-id="0928a-119">**-inf**</span></span> | <span data-ttu-id="0928a-120">**-F**</span><span class="sxs-lookup"><span data-stu-id="0928a-120">**-F**</span></span> | <span data-ttu-id="0928a-121">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="0928a-121">**-denorm**</span></span> | <span data-ttu-id="0928a-122">**-0**</span><span class="sxs-lookup"><span data-stu-id="0928a-122">**-0**</span></span> | <span data-ttu-id="0928a-123">**+0**</span><span class="sxs-lookup"><span data-stu-id="0928a-123">**+0**</span></span> | <span data-ttu-id="0928a-124">**+denorm**</span><span class="sxs-lookup"><span data-stu-id="0928a-124">**+denorm**</span></span> | <span data-ttu-id="0928a-125">**+F**</span><span class="sxs-lookup"><span data-stu-id="0928a-125">**+F**</span></span> | <span data-ttu-id="0928a-126">**+inf**</span><span class="sxs-lookup"><span data-stu-id="0928a-126">**+inf**</span></span> | <span data-ttu-id="0928a-127">**NaN**</span><span class="sxs-lookup"><span data-stu-id="0928a-127">**NaN**</span></span> |
|--------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="0928a-128">*Dest*</span><span class="sxs-lookup"><span data-stu-id="0928a-128">*dest*</span></span> | <span data-ttu-id="0928a-129">-0</span><span class="sxs-lookup"><span data-stu-id="0928a-129">-0</span></span>       | <span data-ttu-id="0928a-130">-F</span><span class="sxs-lookup"><span data-stu-id="0928a-130">-F</span></span>     | <span data-ttu-id="0928a-131">-inf</span><span class="sxs-lookup"><span data-stu-id="0928a-131">-inf</span></span>        | <span data-ttu-id="0928a-132">-inf</span><span class="sxs-lookup"><span data-stu-id="0928a-132">-inf</span></span>   | <span data-ttu-id="0928a-133">+inf</span><span class="sxs-lookup"><span data-stu-id="0928a-133">+inf</span></span>   | <span data-ttu-id="0928a-134">+inf</span><span class="sxs-lookup"><span data-stu-id="0928a-134">+inf</span></span>        | <span data-ttu-id="0928a-135">+F</span><span class="sxs-lookup"><span data-stu-id="0928a-135">+F</span></span>     | <span data-ttu-id="0928a-136">+0</span><span class="sxs-lookup"><span data-stu-id="0928a-136">+0</span></span>       | <span data-ttu-id="0928a-137">NaN</span><span class="sxs-lookup"><span data-stu-id="0928a-137">NaN</span></span>     |



 

<span data-ttu-id="0928a-138">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="0928a-138">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="0928a-139">Vertice</span><span class="sxs-lookup"><span data-stu-id="0928a-139">Vertex</span></span> | <span data-ttu-id="0928a-140">Scafo</span><span class="sxs-lookup"><span data-stu-id="0928a-140">Hull</span></span> | <span data-ttu-id="0928a-141">Dominio</span><span class="sxs-lookup"><span data-stu-id="0928a-141">Domain</span></span> | <span data-ttu-id="0928a-142">Geometria</span><span class="sxs-lookup"><span data-stu-id="0928a-142">Geometry</span></span> | <span data-ttu-id="0928a-143">Pixel</span><span class="sxs-lookup"><span data-stu-id="0928a-143">Pixel</span></span> | <span data-ttu-id="0928a-144">Calcolo</span><span class="sxs-lookup"><span data-stu-id="0928a-144">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="0928a-145">X</span><span class="sxs-lookup"><span data-stu-id="0928a-145">X</span></span>      | <span data-ttu-id="0928a-146">X</span><span class="sxs-lookup"><span data-stu-id="0928a-146">X</span></span>    | <span data-ttu-id="0928a-147">X</span><span class="sxs-lookup"><span data-stu-id="0928a-147">X</span></span>      | <span data-ttu-id="0928a-148">X</span><span class="sxs-lookup"><span data-stu-id="0928a-148">X</span></span>        | <span data-ttu-id="0928a-149">X</span><span class="sxs-lookup"><span data-stu-id="0928a-149">X</span></span>     | <span data-ttu-id="0928a-150">X</span><span class="sxs-lookup"><span data-stu-id="0928a-150">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="0928a-151">Modello di shader minimo</span><span class="sxs-lookup"><span data-stu-id="0928a-151">Minimum Shader Model</span></span>

<span data-ttu-id="0928a-152">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="0928a-152">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="0928a-153">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="0928a-153">Shader Model</span></span>                                              | <span data-ttu-id="0928a-154">Supportato</span><span class="sxs-lookup"><span data-stu-id="0928a-154">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="0928a-155">Modello shader 5</span><span class="sxs-lookup"><span data-stu-id="0928a-155">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="0928a-156">sì</span><span class="sxs-lookup"><span data-stu-id="0928a-156">yes</span></span>       |
| [<span data-ttu-id="0928a-157">Modello shader 4.1</span><span class="sxs-lookup"><span data-stu-id="0928a-157">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="0928a-158">no</span><span class="sxs-lookup"><span data-stu-id="0928a-158">no</span></span>        |
| [<span data-ttu-id="0928a-159">Modello shader 4</span><span class="sxs-lookup"><span data-stu-id="0928a-159">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="0928a-160">no</span><span class="sxs-lookup"><span data-stu-id="0928a-160">no</span></span>        |
| [<span data-ttu-id="0928a-161">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0928a-161">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="0928a-162">no</span><span class="sxs-lookup"><span data-stu-id="0928a-162">no</span></span>        |
| [<span data-ttu-id="0928a-163">Modello shader 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0928a-163">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="0928a-164">no</span><span class="sxs-lookup"><span data-stu-id="0928a-164">no</span></span>        |
| [<span data-ttu-id="0928a-165">Modello shader 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0928a-165">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="0928a-166">no</span><span class="sxs-lookup"><span data-stu-id="0928a-166">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="0928a-167">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0928a-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0928a-168">Assembly del modello shader 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0928a-168">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





