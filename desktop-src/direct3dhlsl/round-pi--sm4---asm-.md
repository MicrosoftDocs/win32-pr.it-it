---
title: round_pi (sm4 - asm)
description: Arrotondamento a virgola mobile a float integrale. | round_pi (sm4 - asm)
ms.assetid: AA4E4C2E-A4B0-4892-8660-1EF57767F4C4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b61282078b3639681eed756e2899d06744f0369e
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997108"
---
# <a name="round_pi-sm4---asm"></a><span data-ttu-id="a77e5-104">pi \_ greco arrotondato (sm4 - asm)</span><span class="sxs-lookup"><span data-stu-id="a77e5-104">round\_pi (sm4 - asm)</span></span>

<span data-ttu-id="a77e5-105">Arrotondamento a virgola mobile a float integrale.</span><span class="sxs-lookup"><span data-stu-id="a77e5-105">Floating-point round to integral float.</span></span>



| <span data-ttu-id="a77e5-106">round \_ pi \[ \_ sat \] dest \[ \] .mask, \[ - \] src0 \[ \_ abs \] \[ .swizzle\]</span><span class="sxs-lookup"><span data-stu-id="a77e5-106">round\_pi\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------------|



 



| <span data-ttu-id="a77e5-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="a77e5-107">Item</span></span>                                                            | <span data-ttu-id="a77e5-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a77e5-108">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="a77e5-109"><span id="dest"></span><span id="DEST"></span>*Dest*</span><span class="sxs-lookup"><span data-stu-id="a77e5-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="a77e5-110">\[in \] Indirizzo dei risultati dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="a77e5-110">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="a77e5-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="a77e5-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="a77e5-112">\[in \] Componenti dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="a77e5-112">\[in\] The components in the operation.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="a77e5-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="a77e5-113">Remarks</span></span>

<span data-ttu-id="a77e5-114">Questa istruzione esegue un round a virgola mobile per componente dei valori in *src0*, scrivendo valori a virgola mobile integrali *in dest*.</span><span class="sxs-lookup"><span data-stu-id="a77e5-114">This instruction performs a component-wise floating-point round of the values in *src0*, writing integral floating-point values to *dest*.</span></span>

<span data-ttu-id="a77e5-115">**pi \_ greco arrotondato** arrotonda verso +infinito, comunemente noto come ceil().</span><span class="sxs-lookup"><span data-stu-id="a77e5-115">**round\_pi** rounds towards +infinity, commonly known as ceil().</span></span>

<span data-ttu-id="a77e5-116">La tabella seguente mostra i risultati ottenuti durante l'esecuzione dell'istruzione con diverse classi di numeri.</span><span class="sxs-lookup"><span data-stu-id="a77e5-116">The following table shows the results obtained when executing the instruction with various classes of numbers.</span></span>

<span data-ttu-id="a77e5-117">F indica un numero finito-reale.</span><span class="sxs-lookup"><span data-stu-id="a77e5-117">F means finite-real number.</span></span>



| <span data-ttu-id="a77e5-118">**src**</span><span class="sxs-lookup"><span data-stu-id="a77e5-118">**src**</span></span>  | <span data-ttu-id="a77e5-119">**-inf**</span><span class="sxs-lookup"><span data-stu-id="a77e5-119">**-inf**</span></span> | <span data-ttu-id="a77e5-120">**-F**</span><span class="sxs-lookup"><span data-stu-id="a77e5-120">**-F**</span></span> | <span data-ttu-id="a77e5-121">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="a77e5-121">**-denorm**</span></span> | <span data-ttu-id="a77e5-122">**-0**</span><span class="sxs-lookup"><span data-stu-id="a77e5-122">**-0**</span></span> | <span data-ttu-id="a77e5-123">**+0**</span><span class="sxs-lookup"><span data-stu-id="a77e5-123">**+0**</span></span> | <span data-ttu-id="a77e5-124">**+denorm**</span><span class="sxs-lookup"><span data-stu-id="a77e5-124">**+denorm**</span></span> | <span data-ttu-id="a77e5-125">**+F**</span><span class="sxs-lookup"><span data-stu-id="a77e5-125">**+F**</span></span> | <span data-ttu-id="a77e5-126">**+inf**</span><span class="sxs-lookup"><span data-stu-id="a77e5-126">**+inf**</span></span> | <span data-ttu-id="a77e5-127">**NaN**</span><span class="sxs-lookup"><span data-stu-id="a77e5-127">**NaN**</span></span> |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="a77e5-128">**Dest**</span><span class="sxs-lookup"><span data-stu-id="a77e5-128">**dest**</span></span> | <span data-ttu-id="a77e5-129">-inf</span><span class="sxs-lookup"><span data-stu-id="a77e5-129">-inf</span></span>     | <span data-ttu-id="a77e5-130">-F</span><span class="sxs-lookup"><span data-stu-id="a77e5-130">-F</span></span>     | <span data-ttu-id="a77e5-131">-0</span><span class="sxs-lookup"><span data-stu-id="a77e5-131">-0</span></span>          | <span data-ttu-id="a77e5-132">-0</span><span class="sxs-lookup"><span data-stu-id="a77e5-132">-0</span></span>     | <span data-ttu-id="a77e5-133">+0</span><span class="sxs-lookup"><span data-stu-id="a77e5-133">+0</span></span>     | <span data-ttu-id="a77e5-134">+0</span><span class="sxs-lookup"><span data-stu-id="a77e5-134">+0</span></span>          | <span data-ttu-id="a77e5-135">+F</span><span class="sxs-lookup"><span data-stu-id="a77e5-135">+F</span></span>     | <span data-ttu-id="a77e5-136">+inf</span><span class="sxs-lookup"><span data-stu-id="a77e5-136">+inf</span></span>     | <span data-ttu-id="a77e5-137">NaN</span><span class="sxs-lookup"><span data-stu-id="a77e5-137">NaN</span></span>     |



 

<span data-ttu-id="a77e5-138">Questa istruzione si applica alle fasi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="a77e5-138">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="a77e5-139">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="a77e5-139">Vertex Shader</span></span> | <span data-ttu-id="a77e5-140">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="a77e5-140">Geometry Shader</span></span> | <span data-ttu-id="a77e5-141">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="a77e5-141">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="a77e5-142">x</span><span class="sxs-lookup"><span data-stu-id="a77e5-142">x</span></span>             | <span data-ttu-id="a77e5-143">x</span><span class="sxs-lookup"><span data-stu-id="a77e5-143">x</span></span>               | <span data-ttu-id="a77e5-144">x</span><span class="sxs-lookup"><span data-stu-id="a77e5-144">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="a77e5-145">Modello di shader minimo</span><span class="sxs-lookup"><span data-stu-id="a77e5-145">Minimum Shader Model</span></span>

<span data-ttu-id="a77e5-146">Questa funzione è supportata nei modelli di shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="a77e5-146">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="a77e5-147">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="a77e5-147">Shader Model</span></span>                                              | <span data-ttu-id="a77e5-148">Supportato</span><span class="sxs-lookup"><span data-stu-id="a77e5-148">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="a77e5-149">Modello shader 5</span><span class="sxs-lookup"><span data-stu-id="a77e5-149">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="a77e5-150">sì</span><span class="sxs-lookup"><span data-stu-id="a77e5-150">yes</span></span>       |
| [<span data-ttu-id="a77e5-151">Modello shader 4.1</span><span class="sxs-lookup"><span data-stu-id="a77e5-151">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="a77e5-152">sì</span><span class="sxs-lookup"><span data-stu-id="a77e5-152">yes</span></span>       |
| [<span data-ttu-id="a77e5-153">Modello shader 4</span><span class="sxs-lookup"><span data-stu-id="a77e5-153">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="a77e5-154">sì</span><span class="sxs-lookup"><span data-stu-id="a77e5-154">yes</span></span>       |
| [<span data-ttu-id="a77e5-155">Modello shader 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a77e5-155">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="a77e5-156">no</span><span class="sxs-lookup"><span data-stu-id="a77e5-156">no</span></span>        |
| [<span data-ttu-id="a77e5-157">Modello shader 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a77e5-157">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="a77e5-158">no</span><span class="sxs-lookup"><span data-stu-id="a77e5-158">no</span></span>        |
| [<span data-ttu-id="a77e5-159">Modello shader 1 (HLSL DirectX)</span><span class="sxs-lookup"><span data-stu-id="a77e5-159">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="a77e5-160">no</span><span class="sxs-lookup"><span data-stu-id="a77e5-160">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="a77e5-161">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a77e5-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a77e5-162">Assembly del modello shader 4 (HLSL DirectX)</span><span class="sxs-lookup"><span data-stu-id="a77e5-162">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





