---
title: exp (sm4 - asm)
description: 2exponent a livello di componente.
ms.assetid: 12EB865A-BF71-4B4B-854F-9DA056B18AE0
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b24c74394a5e8ac7a6c945e2c9b63e6f242daa1
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999078"
---
# <a name="exp-sm4---asm"></a><span data-ttu-id="989ac-103">exp (sm4 - asm)</span><span class="sxs-lookup"><span data-stu-id="989ac-103">exp (sm4 - asm)</span></span>

<span data-ttu-id="989ac-104">2exponent a livello di componente.</span><span class="sxs-lookup"><span data-stu-id="989ac-104">Component-wise 2exponent.</span></span>



| <span data-ttu-id="989ac-105">exp \[ \_ sat \] dest \[ .mask \] , \[ - \] src0 \[ \_ abs \] \[ .swizzle\]</span><span class="sxs-lookup"><span data-stu-id="989ac-105">exp\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------|



 



| <span data-ttu-id="989ac-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="989ac-106">Item</span></span>                                                            | <span data-ttu-id="989ac-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="989ac-107">Description</span></span>                                                                |
|-----------------------------------------------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="989ac-108"><span id="dest"></span><span id="DEST"></span>*Dest*</span><span class="sxs-lookup"><span data-stu-id="989ac-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="989ac-109">\[in \] Risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="989ac-109">\[in\] The result of the operation.</span></span><br/> <span data-ttu-id="989ac-110">*dest* = 2 *src0*</span><span class="sxs-lookup"><span data-stu-id="989ac-110">*dest* = 2 *src0*</span></span><br/> |
| <span data-ttu-id="989ac-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="989ac-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="989ac-112">\[in \] Esponente.</span><span class="sxs-lookup"><span data-stu-id="989ac-112">\[in\] The exponent.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="989ac-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="989ac-113">Remarks</span></span>

<span data-ttu-id="989ac-114">Questa istruzione segue la teoria dei limiti.</span><span class="sxs-lookup"><span data-stu-id="989ac-114">This instruction follows limit theory.</span></span> <span data-ttu-id="989ac-115">L'errore relativo massimo è 2-21.</span><span class="sxs-lookup"><span data-stu-id="989ac-115">The maximum relative error is 2-21.</span></span>

<span data-ttu-id="989ac-116">La tabella seguente mostra i risultati ottenuti durante l'esecuzione dell'istruzione con diverse classi di numeri, presupponendo che non si verifichino overflow o underflow.</span><span class="sxs-lookup"><span data-stu-id="989ac-116">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span> <span data-ttu-id="989ac-117">In questa tabella F significa numero finito-reale.</span><span class="sxs-lookup"><span data-stu-id="989ac-117">In this table F means finite-real number.</span></span>



| <span data-ttu-id="989ac-118">**src**</span><span class="sxs-lookup"><span data-stu-id="989ac-118">**src**</span></span>  | <span data-ttu-id="989ac-119">**-inf**</span><span class="sxs-lookup"><span data-stu-id="989ac-119">**-inf**</span></span> | <span data-ttu-id="989ac-120">**-F**</span><span class="sxs-lookup"><span data-stu-id="989ac-120">**-F**</span></span> | <span data-ttu-id="989ac-121">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="989ac-121">**-denorm**</span></span> | <span data-ttu-id="989ac-122">**-0**</span><span class="sxs-lookup"><span data-stu-id="989ac-122">**-0**</span></span> | <span data-ttu-id="989ac-123">**+0**</span><span class="sxs-lookup"><span data-stu-id="989ac-123">**+0**</span></span> | <span data-ttu-id="989ac-124">**+denorm**</span><span class="sxs-lookup"><span data-stu-id="989ac-124">**+denorm**</span></span> | <span data-ttu-id="989ac-125">**+F**</span><span class="sxs-lookup"><span data-stu-id="989ac-125">**+F**</span></span> | <span data-ttu-id="989ac-126">**+inf**</span><span class="sxs-lookup"><span data-stu-id="989ac-126">**+inf**</span></span> | <span data-ttu-id="989ac-127">**NaN**</span><span class="sxs-lookup"><span data-stu-id="989ac-127">**NaN**</span></span> |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="989ac-128">**Dest**</span><span class="sxs-lookup"><span data-stu-id="989ac-128">**dest**</span></span> | <span data-ttu-id="989ac-129">0</span><span class="sxs-lookup"><span data-stu-id="989ac-129">0</span></span>        | <span data-ttu-id="989ac-130">+F</span><span class="sxs-lookup"><span data-stu-id="989ac-130">+F</span></span>     | <span data-ttu-id="989ac-131">1</span><span class="sxs-lookup"><span data-stu-id="989ac-131">1</span></span>           | <span data-ttu-id="989ac-132">1</span><span class="sxs-lookup"><span data-stu-id="989ac-132">1</span></span>      | <span data-ttu-id="989ac-133">1</span><span class="sxs-lookup"><span data-stu-id="989ac-133">1</span></span>      | <span data-ttu-id="989ac-134">1</span><span class="sxs-lookup"><span data-stu-id="989ac-134">1</span></span>           | <span data-ttu-id="989ac-135">+F</span><span class="sxs-lookup"><span data-stu-id="989ac-135">+F</span></span>     | <span data-ttu-id="989ac-136">+inf</span><span class="sxs-lookup"><span data-stu-id="989ac-136">+inf</span></span>     | <span data-ttu-id="989ac-137">NaN</span><span class="sxs-lookup"><span data-stu-id="989ac-137">NaN</span></span>     |



 

<span data-ttu-id="989ac-138">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="989ac-138">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="989ac-139">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="989ac-139">Vertex Shader</span></span> | <span data-ttu-id="989ac-140">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="989ac-140">Geometry Shader</span></span> | <span data-ttu-id="989ac-141">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="989ac-141">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="989ac-142">x</span><span class="sxs-lookup"><span data-stu-id="989ac-142">x</span></span>             | <span data-ttu-id="989ac-143">x</span><span class="sxs-lookup"><span data-stu-id="989ac-143">x</span></span>               | <span data-ttu-id="989ac-144">x</span><span class="sxs-lookup"><span data-stu-id="989ac-144">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="989ac-145">Modello di shader minimo</span><span class="sxs-lookup"><span data-stu-id="989ac-145">Minimum Shader Model</span></span>

<span data-ttu-id="989ac-146">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="989ac-146">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="989ac-147">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="989ac-147">Shader Model</span></span>                                              | <span data-ttu-id="989ac-148">Supportato</span><span class="sxs-lookup"><span data-stu-id="989ac-148">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="989ac-149">Modello shader 5</span><span class="sxs-lookup"><span data-stu-id="989ac-149">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="989ac-150">sì</span><span class="sxs-lookup"><span data-stu-id="989ac-150">yes</span></span>       |
| [<span data-ttu-id="989ac-151">Modello shader 4.1</span><span class="sxs-lookup"><span data-stu-id="989ac-151">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="989ac-152">sì</span><span class="sxs-lookup"><span data-stu-id="989ac-152">yes</span></span>       |
| [<span data-ttu-id="989ac-153">Modello shader 4</span><span class="sxs-lookup"><span data-stu-id="989ac-153">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="989ac-154">sì</span><span class="sxs-lookup"><span data-stu-id="989ac-154">yes</span></span>       |
| [<span data-ttu-id="989ac-155">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="989ac-155">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="989ac-156">no</span><span class="sxs-lookup"><span data-stu-id="989ac-156">no</span></span>        |
| [<span data-ttu-id="989ac-157">Modello shader 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="989ac-157">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="989ac-158">no</span><span class="sxs-lookup"><span data-stu-id="989ac-158">no</span></span>        |
| [<span data-ttu-id="989ac-159">Modello shader 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="989ac-159">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="989ac-160">no</span><span class="sxs-lookup"><span data-stu-id="989ac-160">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="989ac-161">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="989ac-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="989ac-162">Shader Model 4 Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="989ac-162">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





