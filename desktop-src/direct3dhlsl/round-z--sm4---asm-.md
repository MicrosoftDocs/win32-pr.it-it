---
title: round_z (sm4 - asm)
description: Arrotondamento a virgola mobile a float integrale. | round_z (sm4 - asm)
ms.assetid: 97C0E0F2-2571-4A94-BB04-B0CDBA0B5C0C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc874c6d0a1f26902086af300784c55950b71569
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997128"
---
# <a name="round_z-sm4---asm"></a><span data-ttu-id="1d5e8-104">round \_ z (sm4 - asm)</span><span class="sxs-lookup"><span data-stu-id="1d5e8-104">round\_z (sm4 - asm)</span></span>

<span data-ttu-id="1d5e8-105">Arrotondamento a virgola mobile a float integrale.</span><span class="sxs-lookup"><span data-stu-id="1d5e8-105">Floating-point round to integral float.</span></span>



| <span data-ttu-id="1d5e8-106">round \_ z \[ \_ sat \] dest \[ .mask , \] \[ - \] src0 \[ \_ abs \] \[ .swizzle\]</span><span class="sxs-lookup"><span data-stu-id="1d5e8-106">round\_z\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|-----------------------------------------------------------------|



 



| <span data-ttu-id="1d5e8-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="1d5e8-107">Item</span></span>                                                            | <span data-ttu-id="1d5e8-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1d5e8-108">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="1d5e8-109"><span id="dest"></span><span id="DEST"></span>*Dest*</span><span class="sxs-lookup"><span data-stu-id="1d5e8-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="1d5e8-110">\[in \] Indirizzo dei risultati dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="1d5e8-110">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="1d5e8-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="1d5e8-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="1d5e8-112">\[in \] Componenti dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="1d5e8-112">\[in\] The components in the operation.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="1d5e8-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="1d5e8-113">Remarks</span></span>

<span data-ttu-id="1d5e8-114">Questa istruzione esegue un round a virgola mobile a livello di componente dei valori in *src0*, scrivendo valori a virgola mobile integrali *in dest*.</span><span class="sxs-lookup"><span data-stu-id="1d5e8-114">This instruction performs a component-wise floating-point round of the values in *src0*, writing integral floating-point values to *dest*.</span></span>

<span data-ttu-id="1d5e8-115">**round \_ z** arrotonda verso zero.</span><span class="sxs-lookup"><span data-stu-id="1d5e8-115">**round\_z** rounds towards zero.</span></span>

<span data-ttu-id="1d5e8-116">La tabella seguente mostra i risultati ottenuti quando si esegue l'istruzione con varie classi di numeri.</span><span class="sxs-lookup"><span data-stu-id="1d5e8-116">The following table shows the results obtained when executing the instruction with various classes of numbers.</span></span>



| <span data-ttu-id="1d5e8-117">**src**</span><span class="sxs-lookup"><span data-stu-id="1d5e8-117">**src**</span></span>  | <span data-ttu-id="1d5e8-118">**-inf**</span><span class="sxs-lookup"><span data-stu-id="1d5e8-118">**-inf**</span></span> | <span data-ttu-id="1d5e8-119">**-F**</span><span class="sxs-lookup"><span data-stu-id="1d5e8-119">**-F**</span></span> | <span data-ttu-id="1d5e8-120">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="1d5e8-120">**-denorm**</span></span> | <span data-ttu-id="1d5e8-121">**-0**</span><span class="sxs-lookup"><span data-stu-id="1d5e8-121">**-0**</span></span> | <span data-ttu-id="1d5e8-122">**+0**</span><span class="sxs-lookup"><span data-stu-id="1d5e8-122">**+0**</span></span> | <span data-ttu-id="1d5e8-123">**+denorm**</span><span class="sxs-lookup"><span data-stu-id="1d5e8-123">**+denorm**</span></span> | <span data-ttu-id="1d5e8-124">**+F**</span><span class="sxs-lookup"><span data-stu-id="1d5e8-124">**+F**</span></span> | <span data-ttu-id="1d5e8-125">**+inf**</span><span class="sxs-lookup"><span data-stu-id="1d5e8-125">**+inf**</span></span> | <span data-ttu-id="1d5e8-126">**NaN**</span><span class="sxs-lookup"><span data-stu-id="1d5e8-126">**NaN**</span></span> |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="1d5e8-127">**Dest**</span><span class="sxs-lookup"><span data-stu-id="1d5e8-127">**dest**</span></span> | <span data-ttu-id="1d5e8-128">-inf</span><span class="sxs-lookup"><span data-stu-id="1d5e8-128">-inf</span></span>     | <span data-ttu-id="1d5e8-129">-F</span><span class="sxs-lookup"><span data-stu-id="1d5e8-129">-F</span></span>     | <span data-ttu-id="1d5e8-130">-0</span><span class="sxs-lookup"><span data-stu-id="1d5e8-130">-0</span></span>          | <span data-ttu-id="1d5e8-131">-0</span><span class="sxs-lookup"><span data-stu-id="1d5e8-131">-0</span></span>     | <span data-ttu-id="1d5e8-132">+0</span><span class="sxs-lookup"><span data-stu-id="1d5e8-132">+0</span></span>     | <span data-ttu-id="1d5e8-133">+0</span><span class="sxs-lookup"><span data-stu-id="1d5e8-133">+0</span></span>          | <span data-ttu-id="1d5e8-134">+F</span><span class="sxs-lookup"><span data-stu-id="1d5e8-134">+F</span></span>     | <span data-ttu-id="1d5e8-135">+inf</span><span class="sxs-lookup"><span data-stu-id="1d5e8-135">+inf</span></span>     | <span data-ttu-id="1d5e8-136">NaN</span><span class="sxs-lookup"><span data-stu-id="1d5e8-136">NaN</span></span>     |



 

<span data-ttu-id="1d5e8-137">F indica un numero finito-reale.</span><span class="sxs-lookup"><span data-stu-id="1d5e8-137">F means finite-real number.</span></span>

<span data-ttu-id="1d5e8-138">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="1d5e8-138">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="1d5e8-139">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="1d5e8-139">Vertex Shader</span></span> | <span data-ttu-id="1d5e8-140">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="1d5e8-140">Geometry Shader</span></span> | <span data-ttu-id="1d5e8-141">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="1d5e8-141">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="1d5e8-142">x</span><span class="sxs-lookup"><span data-stu-id="1d5e8-142">x</span></span>             | <span data-ttu-id="1d5e8-143">x</span><span class="sxs-lookup"><span data-stu-id="1d5e8-143">x</span></span>               | <span data-ttu-id="1d5e8-144">x</span><span class="sxs-lookup"><span data-stu-id="1d5e8-144">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="1d5e8-145">Modello di shader minimo</span><span class="sxs-lookup"><span data-stu-id="1d5e8-145">Minimum Shader Model</span></span>

<span data-ttu-id="1d5e8-146">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="1d5e8-146">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="1d5e8-147">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="1d5e8-147">Shader Model</span></span>                                              | <span data-ttu-id="1d5e8-148">Supportato</span><span class="sxs-lookup"><span data-stu-id="1d5e8-148">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="1d5e8-149">Modello shader 5</span><span class="sxs-lookup"><span data-stu-id="1d5e8-149">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="1d5e8-150">sì</span><span class="sxs-lookup"><span data-stu-id="1d5e8-150">yes</span></span>       |
| [<span data-ttu-id="1d5e8-151">Modello shader 4.1</span><span class="sxs-lookup"><span data-stu-id="1d5e8-151">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="1d5e8-152">sì</span><span class="sxs-lookup"><span data-stu-id="1d5e8-152">yes</span></span>       |
| [<span data-ttu-id="1d5e8-153">Modello shader 4</span><span class="sxs-lookup"><span data-stu-id="1d5e8-153">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="1d5e8-154">sì</span><span class="sxs-lookup"><span data-stu-id="1d5e8-154">yes</span></span>       |
| [<span data-ttu-id="1d5e8-155">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1d5e8-155">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="1d5e8-156">no</span><span class="sxs-lookup"><span data-stu-id="1d5e8-156">no</span></span>        |
| [<span data-ttu-id="1d5e8-157">Modello shader 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1d5e8-157">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="1d5e8-158">no</span><span class="sxs-lookup"><span data-stu-id="1d5e8-158">no</span></span>        |
| [<span data-ttu-id="1d5e8-159">Modello shader 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1d5e8-159">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="1d5e8-160">no</span><span class="sxs-lookup"><span data-stu-id="1d5e8-160">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="1d5e8-161">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1d5e8-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d5e8-162">Shader Model 4 Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1d5e8-162">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





