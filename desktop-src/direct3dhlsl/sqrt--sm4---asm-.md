---
title: sqrt (sm4 - asm)
description: Radice quadrata per componente.
ms.assetid: B860D656-7F01-484F-909F-A5C9A61C52C3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 628601e0a3a78784a5fd1a089ef7608a0cf9ca05
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996608"
---
# <a name="sqrt-sm4---asm"></a><span data-ttu-id="7a685-103">sqrt (sm4 - asm)</span><span class="sxs-lookup"><span data-stu-id="7a685-103">sqrt (sm4 - asm)</span></span>

<span data-ttu-id="7a685-104">Radice quadrata per componente.</span><span class="sxs-lookup"><span data-stu-id="7a685-104">Component-wise square root.</span></span>



| <span data-ttu-id="7a685-105">sqrt \[ \_ sat \] dest \[ .mask \] , \[ - \] src0 \[ \_ abs \] \[ .swizzle\]</span><span class="sxs-lookup"><span data-stu-id="7a685-105">sqrt\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|-------------------------------------------------------------|



 



| <span data-ttu-id="7a685-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="7a685-106">Item</span></span>                                                            | <span data-ttu-id="7a685-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7a685-107">Description</span></span>                                                                     |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="7a685-108"><span id="dest"></span><span id="DEST"></span>*Dest*</span><span class="sxs-lookup"><span data-stu-id="7a685-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="7a685-109">\[in \] Risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="7a685-109">\[in\] The result of the operation.</span></span><br/> <span data-ttu-id="7a685-110">*dest* = sqrt(*src0*)</span><span class="sxs-lookup"><span data-stu-id="7a685-110">*dest* = sqrt(*src0*)</span></span><br/> |
| <span data-ttu-id="7a685-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="7a685-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="7a685-112">\[in \] Componenti per i quali prendere la radice quadrata.</span><span class="sxs-lookup"><span data-stu-id="7a685-112">\[in\] The components for which to take the square root.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="7a685-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="7a685-113">Remarks</span></span>

<span data-ttu-id="7a685-114">La precisione è 1 ulp.</span><span class="sxs-lookup"><span data-stu-id="7a685-114">Precision is 1 ulp.</span></span>

<span data-ttu-id="7a685-115">La tabella seguente mostra i risultati ottenuti durante l'esecuzione dell'istruzione con diverse classi di numeri, presupponendo che non si verifichino overflow o underflow.</span><span class="sxs-lookup"><span data-stu-id="7a685-115">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span>

<span data-ttu-id="7a685-116">F indica un numero finito reale.</span><span class="sxs-lookup"><span data-stu-id="7a685-116">F means finite-real number.</span></span>



|          | <span data-ttu-id="7a685-117">**-inf**</span><span class="sxs-lookup"><span data-stu-id="7a685-117">**-inf**</span></span> | <span data-ttu-id="7a685-118">**-F**</span><span class="sxs-lookup"><span data-stu-id="7a685-118">**-F**</span></span> | <span data-ttu-id="7a685-119">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="7a685-119">**-denorm**</span></span> | <span data-ttu-id="7a685-120">**-0**</span><span class="sxs-lookup"><span data-stu-id="7a685-120">**-0**</span></span> | <span data-ttu-id="7a685-121">**+0**</span><span class="sxs-lookup"><span data-stu-id="7a685-121">**+0**</span></span> | <span data-ttu-id="7a685-122">**+denorm**</span><span class="sxs-lookup"><span data-stu-id="7a685-122">**+denorm**</span></span> | <span data-ttu-id="7a685-123">**+F**</span><span class="sxs-lookup"><span data-stu-id="7a685-123">**+F**</span></span> | <span data-ttu-id="7a685-124">**+inf**</span><span class="sxs-lookup"><span data-stu-id="7a685-124">**+inf**</span></span> | <span data-ttu-id="7a685-125">**NaN**</span><span class="sxs-lookup"><span data-stu-id="7a685-125">**NaN**</span></span> |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="7a685-126">**Dest**</span><span class="sxs-lookup"><span data-stu-id="7a685-126">**dest**</span></span> | <span data-ttu-id="7a685-127">NaN</span><span class="sxs-lookup"><span data-stu-id="7a685-127">NaN</span></span>      | <span data-ttu-id="7a685-128">NaN</span><span class="sxs-lookup"><span data-stu-id="7a685-128">NaN</span></span>    | <span data-ttu-id="7a685-129">-0</span><span class="sxs-lookup"><span data-stu-id="7a685-129">-0</span></span>          | <span data-ttu-id="7a685-130">-0</span><span class="sxs-lookup"><span data-stu-id="7a685-130">-0</span></span>     | <span data-ttu-id="7a685-131">+0</span><span class="sxs-lookup"><span data-stu-id="7a685-131">+0</span></span>     | <span data-ttu-id="7a685-132">+0</span><span class="sxs-lookup"><span data-stu-id="7a685-132">+0</span></span>          | <span data-ttu-id="7a685-133">+F</span><span class="sxs-lookup"><span data-stu-id="7a685-133">+F</span></span>     | <span data-ttu-id="7a685-134">+inf</span><span class="sxs-lookup"><span data-stu-id="7a685-134">+inf</span></span>     | <span data-ttu-id="7a685-135">NaN</span><span class="sxs-lookup"><span data-stu-id="7a685-135">NaN</span></span>     |



 

<span data-ttu-id="7a685-136">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="7a685-136">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="7a685-137">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="7a685-137">Vertex Shader</span></span> | <span data-ttu-id="7a685-138">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="7a685-138">Geometry Shader</span></span> | <span data-ttu-id="7a685-139">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="7a685-139">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="7a685-140">x</span><span class="sxs-lookup"><span data-stu-id="7a685-140">x</span></span>             | <span data-ttu-id="7a685-141">x</span><span class="sxs-lookup"><span data-stu-id="7a685-141">x</span></span>               | <span data-ttu-id="7a685-142">x</span><span class="sxs-lookup"><span data-stu-id="7a685-142">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="7a685-143">Modello di shader minimo</span><span class="sxs-lookup"><span data-stu-id="7a685-143">Minimum Shader Model</span></span>

<span data-ttu-id="7a685-144">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="7a685-144">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="7a685-145">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="7a685-145">Shader Model</span></span>                                              | <span data-ttu-id="7a685-146">Supportato</span><span class="sxs-lookup"><span data-stu-id="7a685-146">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="7a685-147">Modello shader 5</span><span class="sxs-lookup"><span data-stu-id="7a685-147">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="7a685-148">sì</span><span class="sxs-lookup"><span data-stu-id="7a685-148">yes</span></span>       |
| [<span data-ttu-id="7a685-149">Modello shader 4.1</span><span class="sxs-lookup"><span data-stu-id="7a685-149">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="7a685-150">sì</span><span class="sxs-lookup"><span data-stu-id="7a685-150">yes</span></span>       |
| [<span data-ttu-id="7a685-151">Modello shader 4</span><span class="sxs-lookup"><span data-stu-id="7a685-151">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="7a685-152">sì</span><span class="sxs-lookup"><span data-stu-id="7a685-152">yes</span></span>       |
| [<span data-ttu-id="7a685-153">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7a685-153">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="7a685-154">no</span><span class="sxs-lookup"><span data-stu-id="7a685-154">no</span></span>        |
| [<span data-ttu-id="7a685-155">Modello shader 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7a685-155">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="7a685-156">no</span><span class="sxs-lookup"><span data-stu-id="7a685-156">no</span></span>        |
| [<span data-ttu-id="7a685-157">Modello shader 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7a685-157">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="7a685-158">no</span><span class="sxs-lookup"><span data-stu-id="7a685-158">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="7a685-159">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7a685-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a685-160">Shader Model 4 Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7a685-160">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





