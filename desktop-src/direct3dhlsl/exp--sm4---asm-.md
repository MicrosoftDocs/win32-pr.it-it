---
title: Exp (SM4-ASM)
description: 2exponent a livello di componente.
ms.assetid: 12EB865A-BF71-4B4B-854F-9DA056B18AE0
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 774be1230bdb02a6179ea5662ca2237c2cefc200
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104046062"
---
# <a name="exp-sm4---asm"></a><span data-ttu-id="0b179-103">Exp (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="0b179-103">exp (sm4 - asm)</span></span>

<span data-ttu-id="0b179-104">2exponent a livello di componente.</span><span class="sxs-lookup"><span data-stu-id="0b179-104">Component-wise 2exponent.</span></span>



| <span data-ttu-id="0b179-105">da Exp \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="0b179-105">exp\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------|



 



| <span data-ttu-id="0b179-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="0b179-106">Item</span></span>                                                            | <span data-ttu-id="0b179-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0b179-107">Description</span></span>                                                                |
|-----------------------------------------------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="0b179-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="0b179-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="0b179-109">\[nel \] risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="0b179-109">\[in\] The result of the operation.</span></span><br/> <span data-ttu-id="0b179-110">*dest* = 2 *src0*</span><span class="sxs-lookup"><span data-stu-id="0b179-110">*dest* = 2 *src0*</span></span><br/> |
| <span data-ttu-id="0b179-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="0b179-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="0b179-112">\[nell' \] esponente.</span><span class="sxs-lookup"><span data-stu-id="0b179-112">\[in\] The exponent.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="0b179-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="0b179-113">Remarks</span></span>

<span data-ttu-id="0b179-114">Questa istruzione segue la teoria del limite.</span><span class="sxs-lookup"><span data-stu-id="0b179-114">This instruction follows limit theory.</span></span> <span data-ttu-id="0b179-115">L'errore relativo massimo è 2-21.</span><span class="sxs-lookup"><span data-stu-id="0b179-115">The maximum relative error is 2-21.</span></span>

<span data-ttu-id="0b179-116">Nella tabella seguente vengono illustrati i risultati ottenuti quando si esegue l'istruzione con varie classi di numeri, presupponendo che non si verifichino overflow o underflow.</span><span class="sxs-lookup"><span data-stu-id="0b179-116">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span> <span data-ttu-id="0b179-117">In questa tabella F indica un numero reale finito.</span><span class="sxs-lookup"><span data-stu-id="0b179-117">In this table F means finite-real number.</span></span>



|          |          |        |             |        |        |             |        |          |         |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="0b179-118">**src**</span><span class="sxs-lookup"><span data-stu-id="0b179-118">**src**</span></span>  | <span data-ttu-id="0b179-119">**-INF**</span><span class="sxs-lookup"><span data-stu-id="0b179-119">**-inf**</span></span> | <span data-ttu-id="0b179-120">**-F**</span><span class="sxs-lookup"><span data-stu-id="0b179-120">**-F**</span></span> | <span data-ttu-id="0b179-121">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="0b179-121">**-denorm**</span></span> | <span data-ttu-id="0b179-122">**-0**</span><span class="sxs-lookup"><span data-stu-id="0b179-122">**-0**</span></span> | <span data-ttu-id="0b179-123">**+0**</span><span class="sxs-lookup"><span data-stu-id="0b179-123">**+0**</span></span> | <span data-ttu-id="0b179-124">**+ denorm**</span><span class="sxs-lookup"><span data-stu-id="0b179-124">**+denorm**</span></span> | <span data-ttu-id="0b179-125">**+ F**</span><span class="sxs-lookup"><span data-stu-id="0b179-125">**+F**</span></span> | <span data-ttu-id="0b179-126">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="0b179-126">**+inf**</span></span> | <span data-ttu-id="0b179-127">**NaN**</span><span class="sxs-lookup"><span data-stu-id="0b179-127">**NaN**</span></span> |
| <span data-ttu-id="0b179-128">**dest**</span><span class="sxs-lookup"><span data-stu-id="0b179-128">**dest**</span></span> | <span data-ttu-id="0b179-129">0</span><span class="sxs-lookup"><span data-stu-id="0b179-129">0</span></span>        | <span data-ttu-id="0b179-130">+ F</span><span class="sxs-lookup"><span data-stu-id="0b179-130">+F</span></span>     | <span data-ttu-id="0b179-131">1</span><span class="sxs-lookup"><span data-stu-id="0b179-131">1</span></span>           | <span data-ttu-id="0b179-132">1</span><span class="sxs-lookup"><span data-stu-id="0b179-132">1</span></span>      | <span data-ttu-id="0b179-133">1</span><span class="sxs-lookup"><span data-stu-id="0b179-133">1</span></span>      | <span data-ttu-id="0b179-134">1</span><span class="sxs-lookup"><span data-stu-id="0b179-134">1</span></span>           | <span data-ttu-id="0b179-135">+ F</span><span class="sxs-lookup"><span data-stu-id="0b179-135">+F</span></span>     | <span data-ttu-id="0b179-136">+inf</span><span class="sxs-lookup"><span data-stu-id="0b179-136">+inf</span></span>     | <span data-ttu-id="0b179-137">NaN</span><span class="sxs-lookup"><span data-stu-id="0b179-137">NaN</span></span>     |



 

<span data-ttu-id="0b179-138">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="0b179-138">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="0b179-139">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="0b179-139">Vertex Shader</span></span> | <span data-ttu-id="0b179-140">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="0b179-140">Geometry Shader</span></span> | <span data-ttu-id="0b179-141">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="0b179-141">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="0b179-142">x</span><span class="sxs-lookup"><span data-stu-id="0b179-142">x</span></span>             | <span data-ttu-id="0b179-143">x</span><span class="sxs-lookup"><span data-stu-id="0b179-143">x</span></span>               | <span data-ttu-id="0b179-144">x</span><span class="sxs-lookup"><span data-stu-id="0b179-144">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="0b179-145">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="0b179-145">Minimum Shader Model</span></span>

<span data-ttu-id="0b179-146">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="0b179-146">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="0b179-147">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="0b179-147">Shader Model</span></span>                                              | <span data-ttu-id="0b179-148">Supportato</span><span class="sxs-lookup"><span data-stu-id="0b179-148">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="0b179-149">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="0b179-149">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="0b179-150">sì</span><span class="sxs-lookup"><span data-stu-id="0b179-150">yes</span></span>       |
| [<span data-ttu-id="0b179-151">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="0b179-151">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="0b179-152">sì</span><span class="sxs-lookup"><span data-stu-id="0b179-152">yes</span></span>       |
| [<span data-ttu-id="0b179-153">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="0b179-153">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="0b179-154">sì</span><span class="sxs-lookup"><span data-stu-id="0b179-154">yes</span></span>       |
| [<span data-ttu-id="0b179-155">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0b179-155">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="0b179-156">no</span><span class="sxs-lookup"><span data-stu-id="0b179-156">no</span></span>        |
| [<span data-ttu-id="0b179-157">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0b179-157">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="0b179-158">no</span><span class="sxs-lookup"><span data-stu-id="0b179-158">no</span></span>        |
| [<span data-ttu-id="0b179-159">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0b179-159">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="0b179-160">no</span><span class="sxs-lookup"><span data-stu-id="0b179-160">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="0b179-161">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0b179-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b179-162">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0b179-162">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





