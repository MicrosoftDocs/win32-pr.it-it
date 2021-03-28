---
title: RSQ (SM4-ASM)
description: Radice quadrata reciproca a livello di componente.
ms.assetid: CDA3C2DF-2793-4CE3-87CE-4E0AA945A1BB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc274f927151938be055150d5b17287f9be0004d
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104046110"
---
# <a name="rsq-sm4---asm"></a><span data-ttu-id="642ed-103">RSQ (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="642ed-103">rsq (sm4 - asm)</span></span>

<span data-ttu-id="642ed-104">Radice quadrata reciproca a livello di componente.</span><span class="sxs-lookup"><span data-stu-id="642ed-104">Component-wise reciprocal square root.</span></span>



| <span data-ttu-id="642ed-105">RSQ \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="642ed-105">rsq\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------|



 



| <span data-ttu-id="642ed-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="642ed-106">Item</span></span>                                                            | <span data-ttu-id="642ed-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="642ed-107">Description</span></span>                                                                                      |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="642ed-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="642ed-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="642ed-109">\[in \] contiene i risultati dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="642ed-109">\[in\] Contains the results of the operation.</span></span><br/> <span data-ttu-id="642ed-110">*dest* = 1.0 f/sqrt (*src0*)</span><span class="sxs-lookup"><span data-stu-id="642ed-110">*dest* = 1.0f / sqrt(*src0*)</span></span><br/> |
| <span data-ttu-id="642ed-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="642ed-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="642ed-112">\[nei \] componenti per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="642ed-112">\[in\] The components for the operation.</span></span><br/>                                              |



 

## <a name="remarks"></a><span data-ttu-id="642ed-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="642ed-113">Remarks</span></span>

<span data-ttu-id="642ed-114">L'errore relativo massimo è 2-21.</span><span class="sxs-lookup"><span data-stu-id="642ed-114">The maximum relative error is 2-21.</span></span>

<span data-ttu-id="642ed-115">Nella tabella seguente vengono illustrati i risultati ottenuti quando si esegue l'istruzione con varie classi di numeri, presupponendo che non si verifichino overflow o underflow.</span><span class="sxs-lookup"><span data-stu-id="642ed-115">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span>

<span data-ttu-id="642ed-116">F indica un numero reale finito.</span><span class="sxs-lookup"><span data-stu-id="642ed-116">F means finite-real number.</span></span>



|          |          |        |             |        |        |             |        |          |         |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="642ed-117">**src**</span><span class="sxs-lookup"><span data-stu-id="642ed-117">**src**</span></span>  | <span data-ttu-id="642ed-118">**-INF**</span><span class="sxs-lookup"><span data-stu-id="642ed-118">**-inf**</span></span> | <span data-ttu-id="642ed-119">**-F**</span><span class="sxs-lookup"><span data-stu-id="642ed-119">**-F**</span></span> | <span data-ttu-id="642ed-120">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="642ed-120">**-denorm**</span></span> | <span data-ttu-id="642ed-121">**-0**</span><span class="sxs-lookup"><span data-stu-id="642ed-121">**-0**</span></span> | <span data-ttu-id="642ed-122">**+0**</span><span class="sxs-lookup"><span data-stu-id="642ed-122">**+0**</span></span> | <span data-ttu-id="642ed-123">**+ denorm**</span><span class="sxs-lookup"><span data-stu-id="642ed-123">**+denorm**</span></span> | <span data-ttu-id="642ed-124">**+ F**</span><span class="sxs-lookup"><span data-stu-id="642ed-124">**+F**</span></span> | <span data-ttu-id="642ed-125">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="642ed-125">**+inf**</span></span> | <span data-ttu-id="642ed-126">**NaN**</span><span class="sxs-lookup"><span data-stu-id="642ed-126">**NaN**</span></span> |
| <span data-ttu-id="642ed-127">**dest**</span><span class="sxs-lookup"><span data-stu-id="642ed-127">**dest**</span></span> | <span data-ttu-id="642ed-128">NaN</span><span class="sxs-lookup"><span data-stu-id="642ed-128">NaN</span></span>      | <span data-ttu-id="642ed-129">NaN</span><span class="sxs-lookup"><span data-stu-id="642ed-129">NaN</span></span>    | <span data-ttu-id="642ed-130">-inf</span><span class="sxs-lookup"><span data-stu-id="642ed-130">-inf</span></span>        | <span data-ttu-id="642ed-131">-inf</span><span class="sxs-lookup"><span data-stu-id="642ed-131">-inf</span></span>   | <span data-ttu-id="642ed-132">+inf</span><span class="sxs-lookup"><span data-stu-id="642ed-132">+inf</span></span>   | <span data-ttu-id="642ed-133">+inf</span><span class="sxs-lookup"><span data-stu-id="642ed-133">+inf</span></span>        | <span data-ttu-id="642ed-134">+ F</span><span class="sxs-lookup"><span data-stu-id="642ed-134">+F</span></span>     | <span data-ttu-id="642ed-135">+0</span><span class="sxs-lookup"><span data-stu-id="642ed-135">+0</span></span>       | <span data-ttu-id="642ed-136">NaN</span><span class="sxs-lookup"><span data-stu-id="642ed-136">NaN</span></span>     |



 

<span data-ttu-id="642ed-137">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="642ed-137">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="642ed-138">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="642ed-138">Vertex Shader</span></span> | <span data-ttu-id="642ed-139">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="642ed-139">Geometry Shader</span></span> | <span data-ttu-id="642ed-140">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="642ed-140">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="642ed-141">x</span><span class="sxs-lookup"><span data-stu-id="642ed-141">x</span></span>             | <span data-ttu-id="642ed-142">x</span><span class="sxs-lookup"><span data-stu-id="642ed-142">x</span></span>               | <span data-ttu-id="642ed-143">x</span><span class="sxs-lookup"><span data-stu-id="642ed-143">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="642ed-144">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="642ed-144">Minimum Shader Model</span></span>

<span data-ttu-id="642ed-145">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="642ed-145">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="642ed-146">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="642ed-146">Shader Model</span></span>                                              | <span data-ttu-id="642ed-147">Supportato</span><span class="sxs-lookup"><span data-stu-id="642ed-147">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="642ed-148">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="642ed-148">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="642ed-149">sì</span><span class="sxs-lookup"><span data-stu-id="642ed-149">yes</span></span>       |
| [<span data-ttu-id="642ed-150">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="642ed-150">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="642ed-151">sì</span><span class="sxs-lookup"><span data-stu-id="642ed-151">yes</span></span>       |
| [<span data-ttu-id="642ed-152">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="642ed-152">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="642ed-153">sì</span><span class="sxs-lookup"><span data-stu-id="642ed-153">yes</span></span>       |
| [<span data-ttu-id="642ed-154">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="642ed-154">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="642ed-155">no</span><span class="sxs-lookup"><span data-stu-id="642ed-155">no</span></span>        |
| [<span data-ttu-id="642ed-156">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="642ed-156">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="642ed-157">no</span><span class="sxs-lookup"><span data-stu-id="642ed-157">no</span></span>        |
| [<span data-ttu-id="642ed-158">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="642ed-158">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="642ed-159">no</span><span class="sxs-lookup"><span data-stu-id="642ed-159">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="642ed-160">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="642ed-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="642ed-161">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="642ed-161">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





