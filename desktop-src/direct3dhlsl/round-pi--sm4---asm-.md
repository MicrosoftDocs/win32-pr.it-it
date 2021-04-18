---
title: round_pi (SM4-ASM)
description: Arrotondamento a virgola mobile al valore float integrale. | round_pi (SM4-ASM)
ms.assetid: AA4E4C2E-A4B0-4892-8660-1EF57767F4C4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6016cc03f28852c938b1be62d3aaca39dae5dcfb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995640"
---
# <a name="round_pi-sm4---asm"></a><span data-ttu-id="d8fff-104">Round \_ pi (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="d8fff-104">round\_pi (sm4 - asm)</span></span>

<span data-ttu-id="d8fff-105">Arrotondamento a virgola mobile al valore float integrale.</span><span class="sxs-lookup"><span data-stu-id="d8fff-105">Floating-point round to integral float.</span></span>



| <span data-ttu-id="d8fff-106">il round \_ pi \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="d8fff-106">round\_pi\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------------|



 



| <span data-ttu-id="d8fff-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="d8fff-107">Item</span></span>                                                            | <span data-ttu-id="d8fff-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d8fff-108">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="d8fff-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="d8fff-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="d8fff-110">\[nell' \] indirizzo dei risultati dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="d8fff-110">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="d8fff-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="d8fff-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="d8fff-112">\[nei \] componenti dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="d8fff-112">\[in\] The components in the operation.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="d8fff-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="d8fff-113">Remarks</span></span>

<span data-ttu-id="d8fff-114">Questa istruzione esegue un arrotondamento a virgola mobile per componente dei valori in *src0*, scrivendo valori a virgola mobile integrali in *dest*.</span><span class="sxs-lookup"><span data-stu-id="d8fff-114">This instruction performs a component-wise floating-point round of the values in *src0*, writing integral floating-point values to *dest*.</span></span>

<span data-ttu-id="d8fff-115">**round \_ pi** arrotonda verso + Infinity, comunemente noto come cella ().</span><span class="sxs-lookup"><span data-stu-id="d8fff-115">**round\_pi** rounds towards +infinity, commonly known as ceil().</span></span>

<span data-ttu-id="d8fff-116">Nella tabella seguente vengono illustrati i risultati ottenuti quando si esegue l'istruzione con varie classi di numeri.</span><span class="sxs-lookup"><span data-stu-id="d8fff-116">The following table shows the results obtained when executing the instruction with various classes of numbers.</span></span>

<span data-ttu-id="d8fff-117">F indica un numero reale finito.</span><span class="sxs-lookup"><span data-stu-id="d8fff-117">F means finite-real number.</span></span>



|          |          |        |             |        |        |             |        |          |         |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="d8fff-118">**src**</span><span class="sxs-lookup"><span data-stu-id="d8fff-118">**src**</span></span>  | <span data-ttu-id="d8fff-119">**-INF**</span><span class="sxs-lookup"><span data-stu-id="d8fff-119">**-inf**</span></span> | <span data-ttu-id="d8fff-120">**-F**</span><span class="sxs-lookup"><span data-stu-id="d8fff-120">**-F**</span></span> | <span data-ttu-id="d8fff-121">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="d8fff-121">**-denorm**</span></span> | <span data-ttu-id="d8fff-122">**-0**</span><span class="sxs-lookup"><span data-stu-id="d8fff-122">**-0**</span></span> | <span data-ttu-id="d8fff-123">**+0**</span><span class="sxs-lookup"><span data-stu-id="d8fff-123">**+0**</span></span> | <span data-ttu-id="d8fff-124">**+ denorm**</span><span class="sxs-lookup"><span data-stu-id="d8fff-124">**+denorm**</span></span> | <span data-ttu-id="d8fff-125">**+ F**</span><span class="sxs-lookup"><span data-stu-id="d8fff-125">**+F**</span></span> | <span data-ttu-id="d8fff-126">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="d8fff-126">**+inf**</span></span> | <span data-ttu-id="d8fff-127">**NaN**</span><span class="sxs-lookup"><span data-stu-id="d8fff-127">**NaN**</span></span> |
| <span data-ttu-id="d8fff-128">**dest**</span><span class="sxs-lookup"><span data-stu-id="d8fff-128">**dest**</span></span> | <span data-ttu-id="d8fff-129">-inf</span><span class="sxs-lookup"><span data-stu-id="d8fff-129">-inf</span></span>     | <span data-ttu-id="d8fff-130">-F</span><span class="sxs-lookup"><span data-stu-id="d8fff-130">-F</span></span>     | <span data-ttu-id="d8fff-131">-0</span><span class="sxs-lookup"><span data-stu-id="d8fff-131">-0</span></span>          | <span data-ttu-id="d8fff-132">-0</span><span class="sxs-lookup"><span data-stu-id="d8fff-132">-0</span></span>     | <span data-ttu-id="d8fff-133">+0</span><span class="sxs-lookup"><span data-stu-id="d8fff-133">+0</span></span>     | <span data-ttu-id="d8fff-134">+0</span><span class="sxs-lookup"><span data-stu-id="d8fff-134">+0</span></span>          | <span data-ttu-id="d8fff-135">+ F</span><span class="sxs-lookup"><span data-stu-id="d8fff-135">+F</span></span>     | <span data-ttu-id="d8fff-136">+inf</span><span class="sxs-lookup"><span data-stu-id="d8fff-136">+inf</span></span>     | <span data-ttu-id="d8fff-137">NaN</span><span class="sxs-lookup"><span data-stu-id="d8fff-137">NaN</span></span>     |



 

<span data-ttu-id="d8fff-138">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="d8fff-138">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="d8fff-139">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="d8fff-139">Vertex Shader</span></span> | <span data-ttu-id="d8fff-140">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="d8fff-140">Geometry Shader</span></span> | <span data-ttu-id="d8fff-141">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="d8fff-141">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="d8fff-142">x</span><span class="sxs-lookup"><span data-stu-id="d8fff-142">x</span></span>             | <span data-ttu-id="d8fff-143">x</span><span class="sxs-lookup"><span data-stu-id="d8fff-143">x</span></span>               | <span data-ttu-id="d8fff-144">x</span><span class="sxs-lookup"><span data-stu-id="d8fff-144">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d8fff-145">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="d8fff-145">Minimum Shader Model</span></span>

<span data-ttu-id="d8fff-146">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="d8fff-146">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="d8fff-147">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="d8fff-147">Shader Model</span></span>                                              | <span data-ttu-id="d8fff-148">Supportato</span><span class="sxs-lookup"><span data-stu-id="d8fff-148">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="d8fff-149">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="d8fff-149">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="d8fff-150">sì</span><span class="sxs-lookup"><span data-stu-id="d8fff-150">yes</span></span>       |
| [<span data-ttu-id="d8fff-151">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="d8fff-151">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="d8fff-152">sì</span><span class="sxs-lookup"><span data-stu-id="d8fff-152">yes</span></span>       |
| [<span data-ttu-id="d8fff-153">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="d8fff-153">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="d8fff-154">sì</span><span class="sxs-lookup"><span data-stu-id="d8fff-154">yes</span></span>       |
| [<span data-ttu-id="d8fff-155">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d8fff-155">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="d8fff-156">no</span><span class="sxs-lookup"><span data-stu-id="d8fff-156">no</span></span>        |
| [<span data-ttu-id="d8fff-157">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d8fff-157">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="d8fff-158">no</span><span class="sxs-lookup"><span data-stu-id="d8fff-158">no</span></span>        |
| [<span data-ttu-id="d8fff-159">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d8fff-159">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="d8fff-160">no</span><span class="sxs-lookup"><span data-stu-id="d8fff-160">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="d8fff-161">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d8fff-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8fff-162">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d8fff-162">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





