---
title: FRC (SM4-ASM)
description: Componente frazionario Extract.
ms.assetid: 17C88BCE-7F2F-446C-9BB4-860098B5E42A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4abcfd56e7d6051e9c476097b3e5eef4d97563e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104976431"
---
# <a name="frc-sm4---asm"></a><span data-ttu-id="87993-103">FRC (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="87993-103">frc (sm4 - asm)</span></span>

<span data-ttu-id="87993-104">Componente frazionario Extract.</span><span class="sxs-lookup"><span data-stu-id="87993-104">Component-wise, extract fractional component.</span></span>



| <span data-ttu-id="87993-105">FRC \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="87993-105">frc\[\_sat\] dest\[.mask\], \[-\] src0\[\_abs\]\[.swizzle\]</span></span> |
|-------------------------------------------------------------|



 



| <span data-ttu-id="87993-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="87993-106">Item</span></span>                                                            | <span data-ttu-id="87993-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="87993-107">Description</span></span>                                                                                                                              |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87993-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="87993-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="87993-109">\[nell' \] indirizzo del risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="87993-109">\[in\] The address of the result of the operation.</span></span><br/> <span data-ttu-id="87993-110">*dest*  =  *src0*  -  [round \_ NI](round-ni--sm4---asm-.md)(*src0*)</span><span class="sxs-lookup"><span data-stu-id="87993-110">*dest* = *src0* - [round\_ni](round-ni--sm4---asm-.md)(*src0*)</span></span><br/> |
| <span data-ttu-id="87993-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="87993-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="87993-112">\[nel \] componente dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="87993-112">\[in\] The component in the operation.</span></span><br/>                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="87993-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="87993-113">Remarks</span></span>

<span data-ttu-id="87993-114">Nella tabella seguente vengono illustrati i risultati ottenuti quando si esegue l'istruzione con varie classi di numeri.</span><span class="sxs-lookup"><span data-stu-id="87993-114">The following table shows the results obtained when executing the instruction with various classes of numbers.</span></span>



|          |          |            |             |        |        |             |            |          |         |
|----------|----------|------------|-------------|--------|--------|-------------|------------|----------|---------|
| <span data-ttu-id="87993-115">**src**</span><span class="sxs-lookup"><span data-stu-id="87993-115">**src**</span></span>  | <span data-ttu-id="87993-116">**-INF**</span><span class="sxs-lookup"><span data-stu-id="87993-116">**-inf**</span></span> | <span data-ttu-id="87993-117">**-F**</span><span class="sxs-lookup"><span data-stu-id="87993-117">**-F**</span></span>     | <span data-ttu-id="87993-118">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="87993-118">**-denorm**</span></span> | <span data-ttu-id="87993-119">**-0**</span><span class="sxs-lookup"><span data-stu-id="87993-119">**-0**</span></span> | <span data-ttu-id="87993-120">**+0**</span><span class="sxs-lookup"><span data-stu-id="87993-120">**+0**</span></span> | <span data-ttu-id="87993-121">**+ denorm**</span><span class="sxs-lookup"><span data-stu-id="87993-121">**+denorm**</span></span> | <span data-ttu-id="87993-122">**+ F**</span><span class="sxs-lookup"><span data-stu-id="87993-122">**+F**</span></span>     | <span data-ttu-id="87993-123">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="87993-123">**+inf**</span></span> | <span data-ttu-id="87993-124">**NaN**</span><span class="sxs-lookup"><span data-stu-id="87993-124">**NaN**</span></span> |
| <span data-ttu-id="87993-125">**dest**</span><span class="sxs-lookup"><span data-stu-id="87993-125">**dest**</span></span> | <span data-ttu-id="87993-126">NaN</span><span class="sxs-lookup"><span data-stu-id="87993-126">NaN</span></span>      | <span data-ttu-id="87993-127">\[da + 0 a 1)</span><span class="sxs-lookup"><span data-stu-id="87993-127">\[+0 to 1)</span></span> | <span data-ttu-id="87993-128">+0</span><span class="sxs-lookup"><span data-stu-id="87993-128">+0</span></span>          | <span data-ttu-id="87993-129">+0</span><span class="sxs-lookup"><span data-stu-id="87993-129">+0</span></span>     | <span data-ttu-id="87993-130">+0</span><span class="sxs-lookup"><span data-stu-id="87993-130">+0</span></span>     | <span data-ttu-id="87993-131">+0</span><span class="sxs-lookup"><span data-stu-id="87993-131">+0</span></span>          | <span data-ttu-id="87993-132">\[da + 0 a 1)</span><span class="sxs-lookup"><span data-stu-id="87993-132">\[+0 to 1)</span></span> | <span data-ttu-id="87993-133">NaN</span><span class="sxs-lookup"><span data-stu-id="87993-133">NaN</span></span>      | <span data-ttu-id="87993-134">NaN</span><span class="sxs-lookup"><span data-stu-id="87993-134">NaN</span></span>     |



 

<span data-ttu-id="87993-135">F indica un numero reale finito.</span><span class="sxs-lookup"><span data-stu-id="87993-135">F means finite-real number.</span></span>

<span data-ttu-id="87993-136">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="87993-136">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="87993-137">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="87993-137">Vertex Shader</span></span> | <span data-ttu-id="87993-138">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="87993-138">Geometry Shader</span></span> | <span data-ttu-id="87993-139">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="87993-139">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="87993-140">x</span><span class="sxs-lookup"><span data-stu-id="87993-140">x</span></span>             | <span data-ttu-id="87993-141">x</span><span class="sxs-lookup"><span data-stu-id="87993-141">x</span></span>               | <span data-ttu-id="87993-142">x</span><span class="sxs-lookup"><span data-stu-id="87993-142">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="87993-143">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="87993-143">Minimum Shader Model</span></span>

<span data-ttu-id="87993-144">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="87993-144">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="87993-145">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="87993-145">Shader Model</span></span>                                              | <span data-ttu-id="87993-146">Supportato</span><span class="sxs-lookup"><span data-stu-id="87993-146">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="87993-147">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="87993-147">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="87993-148">sì</span><span class="sxs-lookup"><span data-stu-id="87993-148">yes</span></span>       |
| [<span data-ttu-id="87993-149">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="87993-149">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="87993-150">sì</span><span class="sxs-lookup"><span data-stu-id="87993-150">yes</span></span>       |
| [<span data-ttu-id="87993-151">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="87993-151">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="87993-152">sì</span><span class="sxs-lookup"><span data-stu-id="87993-152">yes</span></span>       |
| [<span data-ttu-id="87993-153">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="87993-153">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="87993-154">no</span><span class="sxs-lookup"><span data-stu-id="87993-154">no</span></span>        |
| [<span data-ttu-id="87993-155">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="87993-155">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="87993-156">no</span><span class="sxs-lookup"><span data-stu-id="87993-156">no</span></span>        |
| [<span data-ttu-id="87993-157">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="87993-157">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="87993-158">no</span><span class="sxs-lookup"><span data-stu-id="87993-158">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="87993-159">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="87993-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87993-160">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="87993-160">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





