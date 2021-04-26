---
title: rsq (sm4 - asm)
description: Radice quadrata reciproca per componente.
ms.assetid: CDA3C2DF-2793-4CE3-87CE-4E0AA945A1BB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1528e9f187ff7d4fb6074d42a1c574686f3b22f
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998168"
---
# <a name="rsq-sm4---asm"></a><span data-ttu-id="ac1cd-103">rsq (sm4 - asm)</span><span class="sxs-lookup"><span data-stu-id="ac1cd-103">rsq (sm4 - asm)</span></span>

<span data-ttu-id="ac1cd-104">Radice quadrata reciproca per componente.</span><span class="sxs-lookup"><span data-stu-id="ac1cd-104">Component-wise reciprocal square root.</span></span>



| <span data-ttu-id="ac1cd-105">rsq \[ \_ sat \] dest \[ .mask \] , \[ - \] src0 \[ \_ abs \] \[ .swizzle\]</span><span class="sxs-lookup"><span data-stu-id="ac1cd-105">rsq\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------|



 



| <span data-ttu-id="ac1cd-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="ac1cd-106">Item</span></span>                                                            | <span data-ttu-id="ac1cd-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ac1cd-107">Description</span></span>                                                                                      |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac1cd-108"><span id="dest"></span><span id="DEST"></span>*Dest*</span><span class="sxs-lookup"><span data-stu-id="ac1cd-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="ac1cd-109">\[in \] Contiene i risultati dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="ac1cd-109">\[in\] Contains the results of the operation.</span></span><br/> <span data-ttu-id="ac1cd-110">*dest* = 1.0f/sqrt(*src0*)</span><span class="sxs-lookup"><span data-stu-id="ac1cd-110">*dest* = 1.0f / sqrt(*src0*)</span></span><br/> |
| <span data-ttu-id="ac1cd-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="ac1cd-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="ac1cd-112">\[in \] Componenti per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="ac1cd-112">\[in\] The components for the operation.</span></span><br/>                                              |



 

## <a name="remarks"></a><span data-ttu-id="ac1cd-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="ac1cd-113">Remarks</span></span>

<span data-ttu-id="ac1cd-114">L'errore relativo massimo è 2-21.</span><span class="sxs-lookup"><span data-stu-id="ac1cd-114">The maximum relative error is 2-21.</span></span>

<span data-ttu-id="ac1cd-115">La tabella seguente mostra i risultati ottenuti durante l'esecuzione dell'istruzione con diverse classi di numeri, presupponendo che non si verifichino overflow o underflow.</span><span class="sxs-lookup"><span data-stu-id="ac1cd-115">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span>

<span data-ttu-id="ac1cd-116">F indica un numero finito reale.</span><span class="sxs-lookup"><span data-stu-id="ac1cd-116">F means finite-real number.</span></span>



| <span data-ttu-id="ac1cd-117">**src**</span><span class="sxs-lookup"><span data-stu-id="ac1cd-117">**src**</span></span>  | <span data-ttu-id="ac1cd-118">**-inf**</span><span class="sxs-lookup"><span data-stu-id="ac1cd-118">**-inf**</span></span> | <span data-ttu-id="ac1cd-119">**-F**</span><span class="sxs-lookup"><span data-stu-id="ac1cd-119">**-F**</span></span> | <span data-ttu-id="ac1cd-120">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="ac1cd-120">**-denorm**</span></span> | <span data-ttu-id="ac1cd-121">**-0**</span><span class="sxs-lookup"><span data-stu-id="ac1cd-121">**-0**</span></span> | <span data-ttu-id="ac1cd-122">**+0**</span><span class="sxs-lookup"><span data-stu-id="ac1cd-122">**+0**</span></span> | <span data-ttu-id="ac1cd-123">**+denorm**</span><span class="sxs-lookup"><span data-stu-id="ac1cd-123">**+denorm**</span></span> | <span data-ttu-id="ac1cd-124">**+F**</span><span class="sxs-lookup"><span data-stu-id="ac1cd-124">**+F**</span></span> | <span data-ttu-id="ac1cd-125">**+inf**</span><span class="sxs-lookup"><span data-stu-id="ac1cd-125">**+inf**</span></span> | <span data-ttu-id="ac1cd-126">**NaN**</span><span class="sxs-lookup"><span data-stu-id="ac1cd-126">**NaN**</span></span> |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="ac1cd-127">**Dest**</span><span class="sxs-lookup"><span data-stu-id="ac1cd-127">**dest**</span></span> | <span data-ttu-id="ac1cd-128">NaN</span><span class="sxs-lookup"><span data-stu-id="ac1cd-128">NaN</span></span>      | <span data-ttu-id="ac1cd-129">NaN</span><span class="sxs-lookup"><span data-stu-id="ac1cd-129">NaN</span></span>    | <span data-ttu-id="ac1cd-130">-inf</span><span class="sxs-lookup"><span data-stu-id="ac1cd-130">-inf</span></span>        | <span data-ttu-id="ac1cd-131">-inf</span><span class="sxs-lookup"><span data-stu-id="ac1cd-131">-inf</span></span>   | <span data-ttu-id="ac1cd-132">+inf</span><span class="sxs-lookup"><span data-stu-id="ac1cd-132">+inf</span></span>   | <span data-ttu-id="ac1cd-133">+inf</span><span class="sxs-lookup"><span data-stu-id="ac1cd-133">+inf</span></span>        | <span data-ttu-id="ac1cd-134">+F</span><span class="sxs-lookup"><span data-stu-id="ac1cd-134">+F</span></span>     | <span data-ttu-id="ac1cd-135">+0</span><span class="sxs-lookup"><span data-stu-id="ac1cd-135">+0</span></span>       | <span data-ttu-id="ac1cd-136">NaN</span><span class="sxs-lookup"><span data-stu-id="ac1cd-136">NaN</span></span>     |



 

<span data-ttu-id="ac1cd-137">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="ac1cd-137">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="ac1cd-138">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="ac1cd-138">Vertex Shader</span></span> | <span data-ttu-id="ac1cd-139">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="ac1cd-139">Geometry Shader</span></span> | <span data-ttu-id="ac1cd-140">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="ac1cd-140">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="ac1cd-141">x</span><span class="sxs-lookup"><span data-stu-id="ac1cd-141">x</span></span>             | <span data-ttu-id="ac1cd-142">x</span><span class="sxs-lookup"><span data-stu-id="ac1cd-142">x</span></span>               | <span data-ttu-id="ac1cd-143">x</span><span class="sxs-lookup"><span data-stu-id="ac1cd-143">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="ac1cd-144">Modello di shader minimo</span><span class="sxs-lookup"><span data-stu-id="ac1cd-144">Minimum Shader Model</span></span>

<span data-ttu-id="ac1cd-145">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="ac1cd-145">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="ac1cd-146">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="ac1cd-146">Shader Model</span></span>                                              | <span data-ttu-id="ac1cd-147">Supportato</span><span class="sxs-lookup"><span data-stu-id="ac1cd-147">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="ac1cd-148">Modello shader 5</span><span class="sxs-lookup"><span data-stu-id="ac1cd-148">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="ac1cd-149">sì</span><span class="sxs-lookup"><span data-stu-id="ac1cd-149">yes</span></span>       |
| [<span data-ttu-id="ac1cd-150">Modello shader 4.1</span><span class="sxs-lookup"><span data-stu-id="ac1cd-150">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="ac1cd-151">sì</span><span class="sxs-lookup"><span data-stu-id="ac1cd-151">yes</span></span>       |
| [<span data-ttu-id="ac1cd-152">Modello shader 4</span><span class="sxs-lookup"><span data-stu-id="ac1cd-152">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="ac1cd-153">sì</span><span class="sxs-lookup"><span data-stu-id="ac1cd-153">yes</span></span>       |
| [<span data-ttu-id="ac1cd-154">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ac1cd-154">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="ac1cd-155">no</span><span class="sxs-lookup"><span data-stu-id="ac1cd-155">no</span></span>        |
| [<span data-ttu-id="ac1cd-156">Modello shader 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ac1cd-156">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="ac1cd-157">no</span><span class="sxs-lookup"><span data-stu-id="ac1cd-157">no</span></span>        |
| [<span data-ttu-id="ac1cd-158">Modello shader 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ac1cd-158">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="ac1cd-159">no</span><span class="sxs-lookup"><span data-stu-id="ac1cd-159">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="ac1cd-160">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ac1cd-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ac1cd-161">Shader Model 4 Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ac1cd-161">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





