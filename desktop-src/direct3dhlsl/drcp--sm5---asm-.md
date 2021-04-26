---
title: drcp (sm5 - asm)
description: Calcola un reciproco a precisione doppia per componente.
ms.assetid: 499A14D6-36DB-4860-94D1-887D931E60D4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 770159f5007b08f5482ba8b58634b44e7f3e6ef0
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998338"
---
# <a name="drcp-sm5---asm"></a><span data-ttu-id="6bdc1-103">drcp (sm5 - asm)</span><span class="sxs-lookup"><span data-stu-id="6bdc1-103">drcp (sm5 - asm)</span></span>

<span data-ttu-id="6bdc1-104">Calcola un reciproco a precisione doppia per componente.</span><span class="sxs-lookup"><span data-stu-id="6bdc1-104">Computes a component-wise double-precision reciprocal.</span></span>



| <span data-ttu-id="6bdc1-105">rcp \[ \_ sat \] dest \[ .mask \] , \[ - \] src0 \[ \_ abs \] \[ .swizzle\]</span><span class="sxs-lookup"><span data-stu-id="6bdc1-105">rcp\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------|



 



| <span data-ttu-id="6bdc1-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="6bdc1-106">Item</span></span>                                                            | <span data-ttu-id="6bdc1-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6bdc1-107">Description</span></span>                                                                                                                     |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6bdc1-108"><span id="dest"></span><span id="DEST"></span>*Dest*</span><span class="sxs-lookup"><span data-stu-id="6bdc1-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="6bdc1-109">\[in \] L'indirizzo dei risultati</span><span class="sxs-lookup"><span data-stu-id="6bdc1-109">\[in\] The address of the results</span></span><br/> <span data-ttu-id="6bdc1-110">*dest*  =  **1.0**  /  *src0*.</span><span class="sxs-lookup"><span data-stu-id="6bdc1-110">*dest* = **1.0** / *src0*.</span></span> <span data-ttu-id="6bdc1-111">Il valore del risultato deve essere accurato a 1,0 ULP</span><span class="sxs-lookup"><span data-stu-id="6bdc1-111">The result value must be accurate to 1.0 ULP</span></span><br/> |
| <span data-ttu-id="6bdc1-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="6bdc1-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="6bdc1-113">\[in \] Numero di cui prendere il reciproco.</span><span class="sxs-lookup"><span data-stu-id="6bdc1-113">\[in\] The number to take the reciprocal of.</span></span><br/>                                                                         |



 

## <a name="remarks"></a><span data-ttu-id="6bdc1-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="6bdc1-114">Remarks</span></span>

<span data-ttu-id="6bdc1-115">L'istruzione DRCP viene generata dal compilatore HLSL solo quando viene chiamata in modo esplicito tramite la funzione intrinseca rcp(), quando come argomento viene usato un valore double.</span><span class="sxs-lookup"><span data-stu-id="6bdc1-115">The DRCP instruction is emitted by the HLSL compiler only when explicitly called via the rcp() intrinsic, when a double is used as the argument.</span></span> <span data-ttu-id="6bdc1-116">L'accuratezza di questa istruzione deve essere 1,0 ULP.</span><span class="sxs-lookup"><span data-stu-id="6bdc1-116">The accuracy of this instruction is required to be 1.0 ULP.</span></span>

<span data-ttu-id="6bdc1-117">Gli shader che usano questa istruzione verranno contrassegnati con un flag shader che ne causerà l'associazione a meno che non vengano soddisfatte tutte le condizioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="6bdc1-117">Shaders that use this instruction will be marked with a shader flag that will cause them to fail to bind unless all the following conditions are met.</span></span>

-   <span data-ttu-id="6bdc1-118">Il sistema supporta DirectX 11.1.</span><span class="sxs-lookup"><span data-stu-id="6bdc1-118">The system supports DirectX 11.1.</span></span>
-   <span data-ttu-id="6bdc1-119">Il sistema include un driver WDDM 1.2.</span><span class="sxs-lookup"><span data-stu-id="6bdc1-119">The system includes a WDDM 1.2 driver.</span></span>
-   <span data-ttu-id="6bdc1-120">Il driver segnala il supporto per questa istruzione **tramite D3D11 \_ FEATURE DATA \_ \_ D3D11 \_ OPTIONS. ExtendedDoublesShaderInstructions** impostato su **TRUE.**</span><span class="sxs-lookup"><span data-stu-id="6bdc1-120">The driver reports support for this instruction via **D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS.ExtendedDoublesShaderInstructions** set to **TRUE**.</span></span>

<span data-ttu-id="6bdc1-121">Nella tabella seguente vengono illustrati i risultati ottenuti durante l'esecuzione dell'istruzione con diverse classi di numeri, presupponendo che non si verifichi alcun overflow o underflow.</span><span class="sxs-lookup"><span data-stu-id="6bdc1-121">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span>

<span data-ttu-id="6bdc1-122">In questa tabella F indica un numero finito-reale.</span><span class="sxs-lookup"><span data-stu-id="6bdc1-122">In this table F means finite-real number.</span></span>



| <span data-ttu-id="6bdc1-123">**Src**-></span><span class="sxs-lookup"><span data-stu-id="6bdc1-123">**src**-></span></span>  | <span data-ttu-id="6bdc1-124">**-inf**</span><span class="sxs-lookup"><span data-stu-id="6bdc1-124">**-inf**</span></span> | <span data-ttu-id="6bdc1-125">**-F**</span><span class="sxs-lookup"><span data-stu-id="6bdc1-125">**-F**</span></span> | <span data-ttu-id="6bdc1-126">**-0**</span><span class="sxs-lookup"><span data-stu-id="6bdc1-126">**-0**</span></span> | <span data-ttu-id="6bdc1-127">**+0**</span><span class="sxs-lookup"><span data-stu-id="6bdc1-127">**+0**</span></span> | <span data-ttu-id="6bdc1-128">**+F**</span><span class="sxs-lookup"><span data-stu-id="6bdc1-128">**+F**</span></span> | <span data-ttu-id="6bdc1-129">**+inf**</span><span class="sxs-lookup"><span data-stu-id="6bdc1-129">**+inf**</span></span> | <span data-ttu-id="6bdc1-130">**NaN**</span><span class="sxs-lookup"><span data-stu-id="6bdc1-130">**NaN**</span></span> |
|---------------|----------|--------|--------|--------|--------|----------|---------|
| <span data-ttu-id="6bdc1-131">**Dest**-></span><span class="sxs-lookup"><span data-stu-id="6bdc1-131">**dest**-></span></span> | <span data-ttu-id="6bdc1-132">-0</span><span class="sxs-lookup"><span data-stu-id="6bdc1-132">-0</span></span>       | <span data-ttu-id="6bdc1-133">-F</span><span class="sxs-lookup"><span data-stu-id="6bdc1-133">-F</span></span>     | <span data-ttu-id="6bdc1-134">-inf</span><span class="sxs-lookup"><span data-stu-id="6bdc1-134">-inf</span></span>   | <span data-ttu-id="6bdc1-135">+inf</span><span class="sxs-lookup"><span data-stu-id="6bdc1-135">+inf</span></span>   | <span data-ttu-id="6bdc1-136">+F</span><span class="sxs-lookup"><span data-stu-id="6bdc1-136">+F</span></span>     | <span data-ttu-id="6bdc1-137">+0</span><span class="sxs-lookup"><span data-stu-id="6bdc1-137">+0</span></span>       | <span data-ttu-id="6bdc1-138">NaN</span><span class="sxs-lookup"><span data-stu-id="6bdc1-138">NaN</span></span>     |



 

<span data-ttu-id="6bdc1-139">Questa istruzione si applica alle fasi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="6bdc1-139">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="6bdc1-140">Vertice</span><span class="sxs-lookup"><span data-stu-id="6bdc1-140">Vertex</span></span> | <span data-ttu-id="6bdc1-141">Scafo</span><span class="sxs-lookup"><span data-stu-id="6bdc1-141">Hull</span></span> | <span data-ttu-id="6bdc1-142">Dominio</span><span class="sxs-lookup"><span data-stu-id="6bdc1-142">Domain</span></span> | <span data-ttu-id="6bdc1-143">Geometria</span><span class="sxs-lookup"><span data-stu-id="6bdc1-143">Geometry</span></span> | <span data-ttu-id="6bdc1-144">Pixel</span><span class="sxs-lookup"><span data-stu-id="6bdc1-144">Pixel</span></span> | <span data-ttu-id="6bdc1-145">Calcolo</span><span class="sxs-lookup"><span data-stu-id="6bdc1-145">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="6bdc1-146">X</span><span class="sxs-lookup"><span data-stu-id="6bdc1-146">X</span></span>      | <span data-ttu-id="6bdc1-147">X</span><span class="sxs-lookup"><span data-stu-id="6bdc1-147">X</span></span>    | <span data-ttu-id="6bdc1-148">X</span><span class="sxs-lookup"><span data-stu-id="6bdc1-148">X</span></span>      | <span data-ttu-id="6bdc1-149">X</span><span class="sxs-lookup"><span data-stu-id="6bdc1-149">X</span></span>        | <span data-ttu-id="6bdc1-150">X</span><span class="sxs-lookup"><span data-stu-id="6bdc1-150">X</span></span>     | <span data-ttu-id="6bdc1-151">X</span><span class="sxs-lookup"><span data-stu-id="6bdc1-151">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="6bdc1-152">Modello di shader minimo</span><span class="sxs-lookup"><span data-stu-id="6bdc1-152">Minimum Shader Model</span></span>

<span data-ttu-id="6bdc1-153">Questa istruzione è supportata nei modelli di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="6bdc1-153">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="6bdc1-154">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="6bdc1-154">Shader Model</span></span>                                              | <span data-ttu-id="6bdc1-155">Supportato</span><span class="sxs-lookup"><span data-stu-id="6bdc1-155">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="6bdc1-156">Modello shader 5</span><span class="sxs-lookup"><span data-stu-id="6bdc1-156">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="6bdc1-157">sì</span><span class="sxs-lookup"><span data-stu-id="6bdc1-157">yes</span></span>       |
| [<span data-ttu-id="6bdc1-158">Modello shader 4.1</span><span class="sxs-lookup"><span data-stu-id="6bdc1-158">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="6bdc1-159">no</span><span class="sxs-lookup"><span data-stu-id="6bdc1-159">no</span></span>        |
| [<span data-ttu-id="6bdc1-160">Modello shader 4</span><span class="sxs-lookup"><span data-stu-id="6bdc1-160">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="6bdc1-161">no</span><span class="sxs-lookup"><span data-stu-id="6bdc1-161">no</span></span>        |
| [<span data-ttu-id="6bdc1-162">Modello shader 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6bdc1-162">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="6bdc1-163">no</span><span class="sxs-lookup"><span data-stu-id="6bdc1-163">no</span></span>        |
| [<span data-ttu-id="6bdc1-164">Modello shader 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6bdc1-164">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="6bdc1-165">no</span><span class="sxs-lookup"><span data-stu-id="6bdc1-165">no</span></span>        |
| [<span data-ttu-id="6bdc1-166">Modello shader 1 (HLSL DirectX)</span><span class="sxs-lookup"><span data-stu-id="6bdc1-166">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="6bdc1-167">no</span><span class="sxs-lookup"><span data-stu-id="6bdc1-167">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="6bdc1-168">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6bdc1-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6bdc1-169">Assembly del modello shader 5 (HLSL DirectX)</span><span class="sxs-lookup"><span data-stu-id="6bdc1-169">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





