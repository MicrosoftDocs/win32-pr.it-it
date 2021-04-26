---
title: frc (sm4 - asm)
description: Componente per componente, estrazione del componente frazionario.
ms.assetid: 17C88BCE-7F2F-446C-9BB4-860098B5E42A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f59b747f38fb970b92b5e48610873efe781d63d
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993918"
---
# <a name="frc-sm4---asm"></a><span data-ttu-id="0c523-103">frc (sm4 - asm)</span><span class="sxs-lookup"><span data-stu-id="0c523-103">frc (sm4 - asm)</span></span>

<span data-ttu-id="0c523-104">Componente per componente, estrazione del componente frazionario.</span><span class="sxs-lookup"><span data-stu-id="0c523-104">Component-wise, extract fractional component.</span></span>



| <span data-ttu-id="0c523-105">frc \[ \_ sat \] dest \[ .mask \] , \[ - \] src0 \[ \_ abs \] \[ .swizzle\]</span><span class="sxs-lookup"><span data-stu-id="0c523-105">frc\[\_sat\] dest\[.mask\], \[-\] src0\[\_abs\]\[.swizzle\]</span></span> |
|-------------------------------------------------------------|



 



| <span data-ttu-id="0c523-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="0c523-106">Item</span></span>                                                            | <span data-ttu-id="0c523-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0c523-107">Description</span></span>                                                                                                                              |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c523-108"><span id="dest"></span><span id="DEST"></span>*Dest*</span><span class="sxs-lookup"><span data-stu-id="0c523-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="0c523-109">\[in \] Indirizzo del risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="0c523-109">\[in\] The address of the result of the operation.</span></span><br/> <span data-ttu-id="0c523-110">*dest*  =  *src0*  -  [round \_ ni](round-ni--sm4---asm-.md)(*src0*)</span><span class="sxs-lookup"><span data-stu-id="0c523-110">*dest* = *src0* - [round\_ni](round-ni--sm4---asm-.md)(*src0*)</span></span><br/> |
| <span data-ttu-id="0c523-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="0c523-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="0c523-112">\[in \] Componente nell'operazione.</span><span class="sxs-lookup"><span data-stu-id="0c523-112">\[in\] The component in the operation.</span></span><br/>                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="0c523-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="0c523-113">Remarks</span></span>

<span data-ttu-id="0c523-114">La tabella seguente mostra i risultati ottenuti quando si esegue l'istruzione con varie classi di numeri.</span><span class="sxs-lookup"><span data-stu-id="0c523-114">The following table shows the results obtained when executing the instruction with various classes of numbers.</span></span>



| <span data-ttu-id="0c523-115">**src**</span><span class="sxs-lookup"><span data-stu-id="0c523-115">**src**</span></span>  | <span data-ttu-id="0c523-116">**-inf**</span><span class="sxs-lookup"><span data-stu-id="0c523-116">**-inf**</span></span> | <span data-ttu-id="0c523-117">**-F**</span><span class="sxs-lookup"><span data-stu-id="0c523-117">**-F**</span></span>     | <span data-ttu-id="0c523-118">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="0c523-118">**-denorm**</span></span> | <span data-ttu-id="0c523-119">**-0**</span><span class="sxs-lookup"><span data-stu-id="0c523-119">**-0**</span></span> | <span data-ttu-id="0c523-120">**+0**</span><span class="sxs-lookup"><span data-stu-id="0c523-120">**+0**</span></span> | <span data-ttu-id="0c523-121">**+denorm**</span><span class="sxs-lookup"><span data-stu-id="0c523-121">**+denorm**</span></span> | <span data-ttu-id="0c523-122">**+F**</span><span class="sxs-lookup"><span data-stu-id="0c523-122">**+F**</span></span>     | <span data-ttu-id="0c523-123">**+inf**</span><span class="sxs-lookup"><span data-stu-id="0c523-123">**+inf**</span></span> | <span data-ttu-id="0c523-124">**NaN**</span><span class="sxs-lookup"><span data-stu-id="0c523-124">**NaN**</span></span> |
|----------|----------|------------|-------------|--------|--------|-------------|------------|----------|---------|
| <span data-ttu-id="0c523-125">**Dest**</span><span class="sxs-lookup"><span data-stu-id="0c523-125">**dest**</span></span> | <span data-ttu-id="0c523-126">NaN</span><span class="sxs-lookup"><span data-stu-id="0c523-126">NaN</span></span>      | <span data-ttu-id="0c523-127">\[+0 a 1)</span><span class="sxs-lookup"><span data-stu-id="0c523-127">\[+0 to 1)</span></span> | <span data-ttu-id="0c523-128">+0</span><span class="sxs-lookup"><span data-stu-id="0c523-128">+0</span></span>          | <span data-ttu-id="0c523-129">+0</span><span class="sxs-lookup"><span data-stu-id="0c523-129">+0</span></span>     | <span data-ttu-id="0c523-130">+0</span><span class="sxs-lookup"><span data-stu-id="0c523-130">+0</span></span>     | <span data-ttu-id="0c523-131">+0</span><span class="sxs-lookup"><span data-stu-id="0c523-131">+0</span></span>          | <span data-ttu-id="0c523-132">\[+0 a 1)</span><span class="sxs-lookup"><span data-stu-id="0c523-132">\[+0 to 1)</span></span> | <span data-ttu-id="0c523-133">NaN</span><span class="sxs-lookup"><span data-stu-id="0c523-133">NaN</span></span>      | <span data-ttu-id="0c523-134">NaN</span><span class="sxs-lookup"><span data-stu-id="0c523-134">NaN</span></span>     |



 

<span data-ttu-id="0c523-135">F indica un numero finito reale.</span><span class="sxs-lookup"><span data-stu-id="0c523-135">F means finite-real number.</span></span>

<span data-ttu-id="0c523-136">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="0c523-136">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="0c523-137">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="0c523-137">Vertex Shader</span></span> | <span data-ttu-id="0c523-138">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="0c523-138">Geometry Shader</span></span> | <span data-ttu-id="0c523-139">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="0c523-139">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="0c523-140">x</span><span class="sxs-lookup"><span data-stu-id="0c523-140">x</span></span>             | <span data-ttu-id="0c523-141">x</span><span class="sxs-lookup"><span data-stu-id="0c523-141">x</span></span>               | <span data-ttu-id="0c523-142">x</span><span class="sxs-lookup"><span data-stu-id="0c523-142">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="0c523-143">Modello di shader minimo</span><span class="sxs-lookup"><span data-stu-id="0c523-143">Minimum Shader Model</span></span>

<span data-ttu-id="0c523-144">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="0c523-144">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="0c523-145">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="0c523-145">Shader Model</span></span>                                              | <span data-ttu-id="0c523-146">Supportato</span><span class="sxs-lookup"><span data-stu-id="0c523-146">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="0c523-147">Modello shader 5</span><span class="sxs-lookup"><span data-stu-id="0c523-147">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="0c523-148">sì</span><span class="sxs-lookup"><span data-stu-id="0c523-148">yes</span></span>       |
| [<span data-ttu-id="0c523-149">Modello shader 4.1</span><span class="sxs-lookup"><span data-stu-id="0c523-149">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="0c523-150">sì</span><span class="sxs-lookup"><span data-stu-id="0c523-150">yes</span></span>       |
| [<span data-ttu-id="0c523-151">Modello shader 4</span><span class="sxs-lookup"><span data-stu-id="0c523-151">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="0c523-152">sì</span><span class="sxs-lookup"><span data-stu-id="0c523-152">yes</span></span>       |
| [<span data-ttu-id="0c523-153">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0c523-153">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="0c523-154">no</span><span class="sxs-lookup"><span data-stu-id="0c523-154">no</span></span>        |
| [<span data-ttu-id="0c523-155">Modello shader 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0c523-155">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="0c523-156">no</span><span class="sxs-lookup"><span data-stu-id="0c523-156">no</span></span>        |
| [<span data-ttu-id="0c523-157">Modello shader 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0c523-157">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="0c523-158">no</span><span class="sxs-lookup"><span data-stu-id="0c523-158">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="0c523-159">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0c523-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c523-160">Shader Model 4 Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0c523-160">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





