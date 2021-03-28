---
title: RCP (SM5-ASM)
description: Reciproco a livello di componente.
ms.assetid: 499A14D6-36DB-4860-94D1-887D931E60D4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abbaa2ffc29a4c3373009d9dec1b895710186e67
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104516513"
---
# <a name="rcp-sm5---asm"></a><span data-ttu-id="41def-103">RCP (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="41def-103">rcp (sm5 - asm)</span></span>

<span data-ttu-id="41def-104">Reciproco a livello di componente.</span><span class="sxs-lookup"><span data-stu-id="41def-104">Component-wise reciprocal.</span></span>



| <span data-ttu-id="41def-105">RCP \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="41def-105">rcp\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------|



 



| <span data-ttu-id="41def-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="41def-106">Item</span></span>                                                            | <span data-ttu-id="41def-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="41def-107">Description</span></span>                                                                         |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="41def-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="41def-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="41def-109">\[nell' \] indirizzo dei risultati</span><span class="sxs-lookup"><span data-stu-id="41def-109">\[in\] The address of the results</span></span><br/> <span data-ttu-id="41def-110">*dest*  =  **1,0 f**  /  *src0*.</span><span class="sxs-lookup"><span data-stu-id="41def-110">*dest* = **1.0f** / *src0*.</span></span><br/> |
| <span data-ttu-id="41def-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="41def-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="41def-112">\[nel \] numero da cui assumere il reciproco.</span><span class="sxs-lookup"><span data-stu-id="41def-112">\[in\] The number to take the reciprocal of.</span></span><br/>                             |



 

## <a name="remarks"></a><span data-ttu-id="41def-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="41def-113">Remarks</span></span>

<span data-ttu-id="41def-114">Usare questa istruzione per reciproco precisione, indipendentemente dai requisiti rigidi per la divisione.</span><span class="sxs-lookup"><span data-stu-id="41def-114">Use this instruction for reduced precision reciprocal, independent of the strict requirements for divide.</span></span>

<span data-ttu-id="41def-115">Il numero massimo di errori relativi è 2-21.</span><span class="sxs-lookup"><span data-stu-id="41def-115">Maximum relative error is 2-21.</span></span> <span data-ttu-id="41def-116">(La tolleranza di errore corrisponde solo a RSQ)</span><span class="sxs-lookup"><span data-stu-id="41def-116">(The error tolerance just matches rsq)</span></span>

<span data-ttu-id="41def-117">Nella tabella seguente vengono illustrati i risultati ottenuti quando si esegue l'istruzione con varie classi di numeri.</span><span class="sxs-lookup"><span data-stu-id="41def-117">The following table shows the results obtained when executing the instruction with various classes of numbers.</span></span>



|        |          |        |             |        |        |             |        |          |         |
|--------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="41def-118">*src*</span><span class="sxs-lookup"><span data-stu-id="41def-118">*src*</span></span>  | <span data-ttu-id="41def-119">**-INF**</span><span class="sxs-lookup"><span data-stu-id="41def-119">**-inf**</span></span> | <span data-ttu-id="41def-120">**-F**</span><span class="sxs-lookup"><span data-stu-id="41def-120">**-F**</span></span> | <span data-ttu-id="41def-121">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="41def-121">**-denorm**</span></span> | <span data-ttu-id="41def-122">**-0**</span><span class="sxs-lookup"><span data-stu-id="41def-122">**-0**</span></span> | <span data-ttu-id="41def-123">**+0**</span><span class="sxs-lookup"><span data-stu-id="41def-123">**+0**</span></span> | <span data-ttu-id="41def-124">**+ denorm**</span><span class="sxs-lookup"><span data-stu-id="41def-124">**+denorm**</span></span> | <span data-ttu-id="41def-125">**+ F**</span><span class="sxs-lookup"><span data-stu-id="41def-125">**+F**</span></span> | <span data-ttu-id="41def-126">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="41def-126">**+inf**</span></span> | <span data-ttu-id="41def-127">**NaN**</span><span class="sxs-lookup"><span data-stu-id="41def-127">**NaN**</span></span> |
| <span data-ttu-id="41def-128">*dest*</span><span class="sxs-lookup"><span data-stu-id="41def-128">*dest*</span></span> | <span data-ttu-id="41def-129">-0</span><span class="sxs-lookup"><span data-stu-id="41def-129">-0</span></span>       | <span data-ttu-id="41def-130">-F</span><span class="sxs-lookup"><span data-stu-id="41def-130">-F</span></span>     | <span data-ttu-id="41def-131">-inf</span><span class="sxs-lookup"><span data-stu-id="41def-131">-inf</span></span>        | <span data-ttu-id="41def-132">-inf</span><span class="sxs-lookup"><span data-stu-id="41def-132">-inf</span></span>   | <span data-ttu-id="41def-133">+inf</span><span class="sxs-lookup"><span data-stu-id="41def-133">+inf</span></span>   | <span data-ttu-id="41def-134">+inf</span><span class="sxs-lookup"><span data-stu-id="41def-134">+inf</span></span>        | <span data-ttu-id="41def-135">+ F</span><span class="sxs-lookup"><span data-stu-id="41def-135">+F</span></span>     | <span data-ttu-id="41def-136">+0</span><span class="sxs-lookup"><span data-stu-id="41def-136">+0</span></span>       | <span data-ttu-id="41def-137">NaN</span><span class="sxs-lookup"><span data-stu-id="41def-137">NaN</span></span>     |



 

<span data-ttu-id="41def-138">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="41def-138">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="41def-139">Vertice</span><span class="sxs-lookup"><span data-stu-id="41def-139">Vertex</span></span> | <span data-ttu-id="41def-140">Hull</span><span class="sxs-lookup"><span data-stu-id="41def-140">Hull</span></span> | <span data-ttu-id="41def-141">Dominio</span><span class="sxs-lookup"><span data-stu-id="41def-141">Domain</span></span> | <span data-ttu-id="41def-142">Geometria</span><span class="sxs-lookup"><span data-stu-id="41def-142">Geometry</span></span> | <span data-ttu-id="41def-143">Pixel</span><span class="sxs-lookup"><span data-stu-id="41def-143">Pixel</span></span> | <span data-ttu-id="41def-144">Calcolo</span><span class="sxs-lookup"><span data-stu-id="41def-144">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="41def-145">X</span><span class="sxs-lookup"><span data-stu-id="41def-145">X</span></span>      | <span data-ttu-id="41def-146">X</span><span class="sxs-lookup"><span data-stu-id="41def-146">X</span></span>    | <span data-ttu-id="41def-147">X</span><span class="sxs-lookup"><span data-stu-id="41def-147">X</span></span>      | <span data-ttu-id="41def-148">X</span><span class="sxs-lookup"><span data-stu-id="41def-148">X</span></span>        | <span data-ttu-id="41def-149">X</span><span class="sxs-lookup"><span data-stu-id="41def-149">X</span></span>     | <span data-ttu-id="41def-150">X</span><span class="sxs-lookup"><span data-stu-id="41def-150">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="41def-151">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="41def-151">Minimum Shader Model</span></span>

<span data-ttu-id="41def-152">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="41def-152">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="41def-153">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="41def-153">Shader Model</span></span>                                              | <span data-ttu-id="41def-154">Supportato</span><span class="sxs-lookup"><span data-stu-id="41def-154">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="41def-155">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="41def-155">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="41def-156">sì</span><span class="sxs-lookup"><span data-stu-id="41def-156">yes</span></span>       |
| [<span data-ttu-id="41def-157">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="41def-157">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="41def-158">no</span><span class="sxs-lookup"><span data-stu-id="41def-158">no</span></span>        |
| [<span data-ttu-id="41def-159">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="41def-159">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="41def-160">no</span><span class="sxs-lookup"><span data-stu-id="41def-160">no</span></span>        |
| [<span data-ttu-id="41def-161">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="41def-161">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="41def-162">no</span><span class="sxs-lookup"><span data-stu-id="41def-162">no</span></span>        |
| [<span data-ttu-id="41def-163">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="41def-163">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="41def-164">no</span><span class="sxs-lookup"><span data-stu-id="41def-164">no</span></span>        |
| [<span data-ttu-id="41def-165">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="41def-165">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="41def-166">no</span><span class="sxs-lookup"><span data-stu-id="41def-166">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="41def-167">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="41def-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41def-168">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="41def-168">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





