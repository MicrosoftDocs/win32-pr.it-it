---
title: round_z (SM4-ASM)
description: Arrotondamento a virgola mobile al valore float integrale. | round_z (SM4-ASM)
ms.assetid: 97C0E0F2-2571-4A94-BB04-B0CDBA0B5C0C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ed79a60bf122163b49411a3b3197ccdacba1311
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103886089"
---
# <a name="round_z-sm4---asm"></a><span data-ttu-id="a0f24-104">Round \_ z (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="a0f24-104">round\_z (sm4 - asm)</span></span>

<span data-ttu-id="a0f24-105">Arrotondamento a virgola mobile al valore float integrale.</span><span class="sxs-lookup"><span data-stu-id="a0f24-105">Floating-point round to integral float.</span></span>



| <span data-ttu-id="a0f24-106">\_ \[ \_ \] dest. mask round z Sat \[ \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="a0f24-106">round\_z\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|-----------------------------------------------------------------|



 



| <span data-ttu-id="a0f24-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="a0f24-107">Item</span></span>                                                            | <span data-ttu-id="a0f24-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a0f24-108">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="a0f24-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="a0f24-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="a0f24-110">\[nell' \] indirizzo dei risultati dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="a0f24-110">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="a0f24-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="a0f24-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="a0f24-112">\[nei \] componenti dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="a0f24-112">\[in\] The components in the operation.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="a0f24-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="a0f24-113">Remarks</span></span>

<span data-ttu-id="a0f24-114">Questa istruzione esegue un arrotondamento a virgola mobile per componente dei valori in *src0*, scrivendo valori a virgola mobile integrali in *dest*.</span><span class="sxs-lookup"><span data-stu-id="a0f24-114">This instruction performs a component-wise floating-point round of the values in *src0*, writing integral floating-point values to *dest*.</span></span>

<span data-ttu-id="a0f24-115">**round \_ z** Arrotonda per eccesso a zero.</span><span class="sxs-lookup"><span data-stu-id="a0f24-115">**round\_z** rounds towards zero.</span></span>

<span data-ttu-id="a0f24-116">Nella tabella seguente vengono illustrati i risultati ottenuti quando si esegue l'istruzione con varie classi di numeri.</span><span class="sxs-lookup"><span data-stu-id="a0f24-116">The following table shows the results obtained when executing the instruction with various classes of numbers.</span></span>



|          |          |        |             |        |        |             |        |          |         |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="a0f24-117">**src**</span><span class="sxs-lookup"><span data-stu-id="a0f24-117">**src**</span></span>  | <span data-ttu-id="a0f24-118">**-INF**</span><span class="sxs-lookup"><span data-stu-id="a0f24-118">**-inf**</span></span> | <span data-ttu-id="a0f24-119">**-F**</span><span class="sxs-lookup"><span data-stu-id="a0f24-119">**-F**</span></span> | <span data-ttu-id="a0f24-120">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="a0f24-120">**-denorm**</span></span> | <span data-ttu-id="a0f24-121">**-0**</span><span class="sxs-lookup"><span data-stu-id="a0f24-121">**-0**</span></span> | <span data-ttu-id="a0f24-122">**+0**</span><span class="sxs-lookup"><span data-stu-id="a0f24-122">**+0**</span></span> | <span data-ttu-id="a0f24-123">**+ denorm**</span><span class="sxs-lookup"><span data-stu-id="a0f24-123">**+denorm**</span></span> | <span data-ttu-id="a0f24-124">**+ F**</span><span class="sxs-lookup"><span data-stu-id="a0f24-124">**+F**</span></span> | <span data-ttu-id="a0f24-125">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="a0f24-125">**+inf**</span></span> | <span data-ttu-id="a0f24-126">**NaN**</span><span class="sxs-lookup"><span data-stu-id="a0f24-126">**NaN**</span></span> |
| <span data-ttu-id="a0f24-127">**dest**</span><span class="sxs-lookup"><span data-stu-id="a0f24-127">**dest**</span></span> | <span data-ttu-id="a0f24-128">-inf</span><span class="sxs-lookup"><span data-stu-id="a0f24-128">-inf</span></span>     | <span data-ttu-id="a0f24-129">-F</span><span class="sxs-lookup"><span data-stu-id="a0f24-129">-F</span></span>     | <span data-ttu-id="a0f24-130">-0</span><span class="sxs-lookup"><span data-stu-id="a0f24-130">-0</span></span>          | <span data-ttu-id="a0f24-131">-0</span><span class="sxs-lookup"><span data-stu-id="a0f24-131">-0</span></span>     | <span data-ttu-id="a0f24-132">+0</span><span class="sxs-lookup"><span data-stu-id="a0f24-132">+0</span></span>     | <span data-ttu-id="a0f24-133">+0</span><span class="sxs-lookup"><span data-stu-id="a0f24-133">+0</span></span>          | <span data-ttu-id="a0f24-134">+ F</span><span class="sxs-lookup"><span data-stu-id="a0f24-134">+F</span></span>     | <span data-ttu-id="a0f24-135">+inf</span><span class="sxs-lookup"><span data-stu-id="a0f24-135">+inf</span></span>     | <span data-ttu-id="a0f24-136">NaN</span><span class="sxs-lookup"><span data-stu-id="a0f24-136">NaN</span></span>     |



 

<span data-ttu-id="a0f24-137">F indica un numero reale finito.</span><span class="sxs-lookup"><span data-stu-id="a0f24-137">F means finite-real number.</span></span>

<span data-ttu-id="a0f24-138">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="a0f24-138">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="a0f24-139">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="a0f24-139">Vertex Shader</span></span> | <span data-ttu-id="a0f24-140">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="a0f24-140">Geometry Shader</span></span> | <span data-ttu-id="a0f24-141">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="a0f24-141">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="a0f24-142">x</span><span class="sxs-lookup"><span data-stu-id="a0f24-142">x</span></span>             | <span data-ttu-id="a0f24-143">x</span><span class="sxs-lookup"><span data-stu-id="a0f24-143">x</span></span>               | <span data-ttu-id="a0f24-144">x</span><span class="sxs-lookup"><span data-stu-id="a0f24-144">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="a0f24-145">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="a0f24-145">Minimum Shader Model</span></span>

<span data-ttu-id="a0f24-146">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="a0f24-146">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="a0f24-147">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="a0f24-147">Shader Model</span></span>                                              | <span data-ttu-id="a0f24-148">Supportato</span><span class="sxs-lookup"><span data-stu-id="a0f24-148">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="a0f24-149">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="a0f24-149">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="a0f24-150">sì</span><span class="sxs-lookup"><span data-stu-id="a0f24-150">yes</span></span>       |
| [<span data-ttu-id="a0f24-151">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="a0f24-151">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="a0f24-152">sì</span><span class="sxs-lookup"><span data-stu-id="a0f24-152">yes</span></span>       |
| [<span data-ttu-id="a0f24-153">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="a0f24-153">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="a0f24-154">sì</span><span class="sxs-lookup"><span data-stu-id="a0f24-154">yes</span></span>       |
| [<span data-ttu-id="a0f24-155">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a0f24-155">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="a0f24-156">no</span><span class="sxs-lookup"><span data-stu-id="a0f24-156">no</span></span>        |
| [<span data-ttu-id="a0f24-157">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a0f24-157">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="a0f24-158">no</span><span class="sxs-lookup"><span data-stu-id="a0f24-158">no</span></span>        |
| [<span data-ttu-id="a0f24-159">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a0f24-159">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="a0f24-160">no</span><span class="sxs-lookup"><span data-stu-id="a0f24-160">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="a0f24-161">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a0f24-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0f24-162">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a0f24-162">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





