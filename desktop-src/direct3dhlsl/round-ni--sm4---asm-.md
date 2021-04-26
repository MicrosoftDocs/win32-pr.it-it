---
title: round_ni (sm4 - asm)
description: Arrotondamento a virgola mobile a float integrale. | round_ni (sm4 - asm)
ms.assetid: 6DEF818B-AFF9-4B44-950E-320EACE1CAC4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2487715bbb2596653b1ca985a2e0390457feecbf
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998578"
---
# <a name="round_ni-sm4---asm"></a><span data-ttu-id="efb06-104">round \_ ni (sm4 - asm)</span><span class="sxs-lookup"><span data-stu-id="efb06-104">round\_ni (sm4 - asm)</span></span>

<span data-ttu-id="efb06-105">Arrotondamento a virgola mobile a float integrale.</span><span class="sxs-lookup"><span data-stu-id="efb06-105">Floating-point round to integral float.</span></span>



| <span data-ttu-id="efb06-106">round \_ ni \[ \_ sat \] dest \[ .mask , \] \[ - \] src0 \[ \_ abs \] \[ .swizzle\]</span><span class="sxs-lookup"><span data-stu-id="efb06-106">round\_ni\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------------|



 



| <span data-ttu-id="efb06-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="efb06-107">Item</span></span>                                                            | <span data-ttu-id="efb06-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="efb06-108">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="efb06-109"><span id="dest"></span><span id="DEST"></span>*Dest*</span><span class="sxs-lookup"><span data-stu-id="efb06-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="efb06-110">\[in \] Indirizzo dei risultati dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="efb06-110">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="efb06-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="efb06-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="efb06-112">\[in \] Componenti dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="efb06-112">\[in\] The components in the operation.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="efb06-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="efb06-113">Remarks</span></span>

<span data-ttu-id="efb06-114">Questa istruzione esegue un round a virgola mobile per componente dei valori in *src0*, scrivendo valori a virgola mobile integrali *in dest*.</span><span class="sxs-lookup"><span data-stu-id="efb06-114">This instruction performs a component-wise floating-point round of the values in *src0*, writing integral floating-point values to *dest*.</span></span> <span data-ttu-id="efb06-115">**round \_ ni** arrotonda verso -infinity, comunemente noto come floor().</span><span class="sxs-lookup"><span data-stu-id="efb06-115">**round\_ni** rounds toward -infinity, commonly known as floor().</span></span>

<span data-ttu-id="efb06-116">La tabella seguente mostra i risultati ottenuti durante l'esecuzione dell'istruzione con diverse classi di numeri.</span><span class="sxs-lookup"><span data-stu-id="efb06-116">The following table shows the results obtained when executing the instruction with various classes of numbers.</span></span>

<span data-ttu-id="efb06-117">F indica un numero finito-reale.</span><span class="sxs-lookup"><span data-stu-id="efb06-117">F means finite-real number.</span></span>



| <span data-ttu-id="efb06-118">**src**</span><span class="sxs-lookup"><span data-stu-id="efb06-118">**src**</span></span>  | <span data-ttu-id="efb06-119">**-inf**</span><span class="sxs-lookup"><span data-stu-id="efb06-119">**-inf**</span></span> | <span data-ttu-id="efb06-120">**-F**</span><span class="sxs-lookup"><span data-stu-id="efb06-120">**-F**</span></span> | <span data-ttu-id="efb06-121">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="efb06-121">**-denorm**</span></span> | <span data-ttu-id="efb06-122">**-0**</span><span class="sxs-lookup"><span data-stu-id="efb06-122">**-0**</span></span> | <span data-ttu-id="efb06-123">**+0**</span><span class="sxs-lookup"><span data-stu-id="efb06-123">**+0**</span></span> | <span data-ttu-id="efb06-124">**+denorm**</span><span class="sxs-lookup"><span data-stu-id="efb06-124">**+denorm**</span></span> | <span data-ttu-id="efb06-125">**+F**</span><span class="sxs-lookup"><span data-stu-id="efb06-125">**+F**</span></span> | <span data-ttu-id="efb06-126">**+inf**</span><span class="sxs-lookup"><span data-stu-id="efb06-126">**+inf**</span></span> | <span data-ttu-id="efb06-127">**NaN**</span><span class="sxs-lookup"><span data-stu-id="efb06-127">**NaN**</span></span> |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="efb06-128">**Dest**</span><span class="sxs-lookup"><span data-stu-id="efb06-128">**dest**</span></span> | <span data-ttu-id="efb06-129">-inf</span><span class="sxs-lookup"><span data-stu-id="efb06-129">-inf</span></span>     | <span data-ttu-id="efb06-130">-F</span><span class="sxs-lookup"><span data-stu-id="efb06-130">-F</span></span>     | <span data-ttu-id="efb06-131">-0</span><span class="sxs-lookup"><span data-stu-id="efb06-131">-0</span></span>          | <span data-ttu-id="efb06-132">-0</span><span class="sxs-lookup"><span data-stu-id="efb06-132">-0</span></span>     | <span data-ttu-id="efb06-133">+0</span><span class="sxs-lookup"><span data-stu-id="efb06-133">+0</span></span>     | <span data-ttu-id="efb06-134">+0</span><span class="sxs-lookup"><span data-stu-id="efb06-134">+0</span></span>          | <span data-ttu-id="efb06-135">+F</span><span class="sxs-lookup"><span data-stu-id="efb06-135">+F</span></span>     | <span data-ttu-id="efb06-136">+inf</span><span class="sxs-lookup"><span data-stu-id="efb06-136">+inf</span></span>     | <span data-ttu-id="efb06-137">NaN</span><span class="sxs-lookup"><span data-stu-id="efb06-137">NaN</span></span>     |



 

<span data-ttu-id="efb06-138">Questa istruzione si applica alle fasi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="efb06-138">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="efb06-139">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="efb06-139">Vertex Shader</span></span> | <span data-ttu-id="efb06-140">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="efb06-140">Geometry Shader</span></span> | <span data-ttu-id="efb06-141">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="efb06-141">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="efb06-142">x</span><span class="sxs-lookup"><span data-stu-id="efb06-142">x</span></span>             | <span data-ttu-id="efb06-143">x</span><span class="sxs-lookup"><span data-stu-id="efb06-143">x</span></span>               | <span data-ttu-id="efb06-144">x</span><span class="sxs-lookup"><span data-stu-id="efb06-144">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="efb06-145">Modello di shader minimo</span><span class="sxs-lookup"><span data-stu-id="efb06-145">Minimum Shader Model</span></span>

<span data-ttu-id="efb06-146">Questa funzione è supportata nei modelli di shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="efb06-146">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="efb06-147">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="efb06-147">Shader Model</span></span>                                              | <span data-ttu-id="efb06-148">Supportato</span><span class="sxs-lookup"><span data-stu-id="efb06-148">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="efb06-149">Modello shader 5</span><span class="sxs-lookup"><span data-stu-id="efb06-149">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="efb06-150">sì</span><span class="sxs-lookup"><span data-stu-id="efb06-150">yes</span></span>       |
| [<span data-ttu-id="efb06-151">Modello shader 4.1</span><span class="sxs-lookup"><span data-stu-id="efb06-151">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="efb06-152">sì</span><span class="sxs-lookup"><span data-stu-id="efb06-152">yes</span></span>       |
| [<span data-ttu-id="efb06-153">Modello shader 4</span><span class="sxs-lookup"><span data-stu-id="efb06-153">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="efb06-154">sì</span><span class="sxs-lookup"><span data-stu-id="efb06-154">yes</span></span>       |
| [<span data-ttu-id="efb06-155">Modello shader 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="efb06-155">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="efb06-156">no</span><span class="sxs-lookup"><span data-stu-id="efb06-156">no</span></span>        |
| [<span data-ttu-id="efb06-157">Modello shader 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="efb06-157">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="efb06-158">no</span><span class="sxs-lookup"><span data-stu-id="efb06-158">no</span></span>        |
| [<span data-ttu-id="efb06-159">Modello shader 1 (HLSL DirectX)</span><span class="sxs-lookup"><span data-stu-id="efb06-159">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="efb06-160">no</span><span class="sxs-lookup"><span data-stu-id="efb06-160">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="efb06-161">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="efb06-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="efb06-162">Assembly del modello shader 4 (HLSL DirectX)</span><span class="sxs-lookup"><span data-stu-id="efb06-162">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





