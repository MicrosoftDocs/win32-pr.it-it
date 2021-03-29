---
title: round_ne (SM4-ASM)
description: Arrotondamento a virgola mobile al valore float integrale. | round_ne (SM4-ASM)
ms.assetid: 2D1A0786-F7DB-4D69-9F56-82ECD1EE7ABA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1c6f5e332453318dc0ad1a7806c3506343ff3b6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981650"
---
# <a name="round_ne-sm4---asm"></a><span data-ttu-id="202a1-104">Round \_ ne (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="202a1-104">round\_ne (sm4 - asm)</span></span>

<span data-ttu-id="202a1-105">Arrotondamento a virgola mobile al valore float integrale.</span><span class="sxs-lookup"><span data-stu-id="202a1-105">Floating-point round to integral float.</span></span>



| <span data-ttu-id="202a1-106">Round \_ ne \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="202a1-106">round\_ne\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------------|



 



| <span data-ttu-id="202a1-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="202a1-107">Item</span></span>                                                            | <span data-ttu-id="202a1-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="202a1-108">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="202a1-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="202a1-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="202a1-110">\[nell' \] indirizzo dei risultati dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="202a1-110">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="202a1-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="202a1-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="202a1-112">\[nei \] componenti dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="202a1-112">\[in\] The components in the operation.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="202a1-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="202a1-113">Remarks</span></span>

<span data-ttu-id="202a1-114">Questa istruzione esegue un arrotondamento a virgola mobile per componente dei valori in *src0*, scrivendo valori a virgola mobile integrali in *dest*.</span><span class="sxs-lookup"><span data-stu-id="202a1-114">This instruction performs a component-wise floating-point round of the values in *src0*, writing integral floating-point values to *dest*.</span></span> <span data-ttu-id="202a1-115">**arrotondare \_ ne** arrotonda al pari più vicino.</span><span class="sxs-lookup"><span data-stu-id="202a1-115">**round\_ne** rounds towards nearest even.</span></span>

<span data-ttu-id="202a1-116">Nella tabella seguente vengono illustrati i risultati ottenuti quando si esegue l'istruzione con varie classi di numeri.</span><span class="sxs-lookup"><span data-stu-id="202a1-116">The following table shows the results obtained when executing the instruction with various classes of numbers.</span></span>

<span data-ttu-id="202a1-117">F indica un numero reale finito.</span><span class="sxs-lookup"><span data-stu-id="202a1-117">F means finite-real number.</span></span>



|          |          |        |             |        |        |             |        |          |         |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="202a1-118">**src**</span><span class="sxs-lookup"><span data-stu-id="202a1-118">**src**</span></span>  | <span data-ttu-id="202a1-119">**-INF**</span><span class="sxs-lookup"><span data-stu-id="202a1-119">**-inf**</span></span> | <span data-ttu-id="202a1-120">**-F**</span><span class="sxs-lookup"><span data-stu-id="202a1-120">**-F**</span></span> | <span data-ttu-id="202a1-121">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="202a1-121">**-denorm**</span></span> | <span data-ttu-id="202a1-122">**-0**</span><span class="sxs-lookup"><span data-stu-id="202a1-122">**-0**</span></span> | <span data-ttu-id="202a1-123">**+0**</span><span class="sxs-lookup"><span data-stu-id="202a1-123">**+0**</span></span> | <span data-ttu-id="202a1-124">**+ denorm**</span><span class="sxs-lookup"><span data-stu-id="202a1-124">**+denorm**</span></span> | <span data-ttu-id="202a1-125">**+ F**</span><span class="sxs-lookup"><span data-stu-id="202a1-125">**+F**</span></span> | <span data-ttu-id="202a1-126">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="202a1-126">**+inf**</span></span> | <span data-ttu-id="202a1-127">**NaN**</span><span class="sxs-lookup"><span data-stu-id="202a1-127">**NaN**</span></span> |
| <span data-ttu-id="202a1-128">**dest**</span><span class="sxs-lookup"><span data-stu-id="202a1-128">**dest**</span></span> | <span data-ttu-id="202a1-129">-inf</span><span class="sxs-lookup"><span data-stu-id="202a1-129">-inf</span></span>     | <span data-ttu-id="202a1-130">-F</span><span class="sxs-lookup"><span data-stu-id="202a1-130">-F</span></span>     | <span data-ttu-id="202a1-131">-0</span><span class="sxs-lookup"><span data-stu-id="202a1-131">-0</span></span>          | <span data-ttu-id="202a1-132">-0</span><span class="sxs-lookup"><span data-stu-id="202a1-132">-0</span></span>     | <span data-ttu-id="202a1-133">+0</span><span class="sxs-lookup"><span data-stu-id="202a1-133">+0</span></span>     | <span data-ttu-id="202a1-134">+0</span><span class="sxs-lookup"><span data-stu-id="202a1-134">+0</span></span>          | <span data-ttu-id="202a1-135">+ F</span><span class="sxs-lookup"><span data-stu-id="202a1-135">+F</span></span>     | <span data-ttu-id="202a1-136">+inf</span><span class="sxs-lookup"><span data-stu-id="202a1-136">+inf</span></span>     | <span data-ttu-id="202a1-137">NaN</span><span class="sxs-lookup"><span data-stu-id="202a1-137">NaN</span></span>     |



 

<span data-ttu-id="202a1-138">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="202a1-138">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="202a1-139">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="202a1-139">Vertex Shader</span></span> | <span data-ttu-id="202a1-140">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="202a1-140">Geometry Shader</span></span> | <span data-ttu-id="202a1-141">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="202a1-141">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="202a1-142">x</span><span class="sxs-lookup"><span data-stu-id="202a1-142">x</span></span>             | <span data-ttu-id="202a1-143">x</span><span class="sxs-lookup"><span data-stu-id="202a1-143">x</span></span>               | <span data-ttu-id="202a1-144">x</span><span class="sxs-lookup"><span data-stu-id="202a1-144">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="202a1-145">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="202a1-145">Minimum Shader Model</span></span>

<span data-ttu-id="202a1-146">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="202a1-146">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="202a1-147">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="202a1-147">Shader Model</span></span>                                              | <span data-ttu-id="202a1-148">Supportato</span><span class="sxs-lookup"><span data-stu-id="202a1-148">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="202a1-149">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="202a1-149">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="202a1-150">sì</span><span class="sxs-lookup"><span data-stu-id="202a1-150">yes</span></span>       |
| [<span data-ttu-id="202a1-151">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="202a1-151">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="202a1-152">sì</span><span class="sxs-lookup"><span data-stu-id="202a1-152">yes</span></span>       |
| [<span data-ttu-id="202a1-153">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="202a1-153">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="202a1-154">sì</span><span class="sxs-lookup"><span data-stu-id="202a1-154">yes</span></span>       |
| [<span data-ttu-id="202a1-155">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="202a1-155">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="202a1-156">no</span><span class="sxs-lookup"><span data-stu-id="202a1-156">no</span></span>        |
| [<span data-ttu-id="202a1-157">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="202a1-157">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="202a1-158">no</span><span class="sxs-lookup"><span data-stu-id="202a1-158">no</span></span>        |
| [<span data-ttu-id="202a1-159">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="202a1-159">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="202a1-160">no</span><span class="sxs-lookup"><span data-stu-id="202a1-160">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="202a1-161">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="202a1-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="202a1-162">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="202a1-162">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





