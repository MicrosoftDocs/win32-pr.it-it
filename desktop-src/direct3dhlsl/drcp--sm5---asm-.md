---
title: drcp (SM5-ASM)
description: Calcola un reciproco a precisione doppia a livello di componente.
ms.assetid: 499A14D6-36DB-4860-94D1-887D931E60D4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b678f4e8b3464817215de9132298fdde1f6feec
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104335551"
---
# <a name="drcp-sm5---asm"></a><span data-ttu-id="37e73-103">drcp (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="37e73-103">drcp (sm5 - asm)</span></span>

<span data-ttu-id="37e73-104">Calcola un reciproco a precisione doppia a livello di componente.</span><span class="sxs-lookup"><span data-stu-id="37e73-104">Computes a component-wise double-precision reciprocal.</span></span>



| <span data-ttu-id="37e73-105">RCP \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="37e73-105">rcp\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------|



 



| <span data-ttu-id="37e73-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="37e73-106">Item</span></span>                                                            | <span data-ttu-id="37e73-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="37e73-107">Description</span></span>                                                                                                                     |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37e73-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="37e73-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="37e73-109">\[nell' \] indirizzo dei risultati</span><span class="sxs-lookup"><span data-stu-id="37e73-109">\[in\] The address of the results</span></span><br/> <span data-ttu-id="37e73-110">*dest*  =  **1,0**  /  *src0*.</span><span class="sxs-lookup"><span data-stu-id="37e73-110">*dest* = **1.0** / *src0*.</span></span> <span data-ttu-id="37e73-111">Il valore del risultato deve essere accurato per 1,0 ULP rispetto</span><span class="sxs-lookup"><span data-stu-id="37e73-111">The result value must be accurate to 1.0 ULP</span></span><br/> |
| <span data-ttu-id="37e73-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="37e73-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="37e73-113">\[nel \] numero da cui assumere il reciproco.</span><span class="sxs-lookup"><span data-stu-id="37e73-113">\[in\] The number to take the reciprocal of.</span></span><br/>                                                                         |



 

## <a name="remarks"></a><span data-ttu-id="37e73-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="37e73-114">Remarks</span></span>

<span data-ttu-id="37e73-115">L'istruzione DRCP viene generata dal compilatore HLSL solo quando viene chiamata in modo esplicito tramite l'oggetto intrinseco RCP (), quando viene usato un valore Double come argomento.</span><span class="sxs-lookup"><span data-stu-id="37e73-115">The DRCP instruction is emitted by the HLSL compiler only when explicitly called via the rcp() intrinsic, when a double is used as the argument.</span></span> <span data-ttu-id="37e73-116">L'accuratezza di questa istruzione deve essere 1,0 ULP rispetto.</span><span class="sxs-lookup"><span data-stu-id="37e73-116">The accuracy of this instruction is required to be 1.0 ULP.</span></span>

<span data-ttu-id="37e73-117">Gli shader che usano questa istruzione verranno contrassegnati con un flag shader che ne causerà la mancata associazione a meno che non vengano soddisfatte tutte le condizioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="37e73-117">Shaders that use this instruction will be marked with a shader flag that will cause them to fail to bind unless all the following conditions are met.</span></span>

-   <span data-ttu-id="37e73-118">Il sistema supporta DirectX 11,1.</span><span class="sxs-lookup"><span data-stu-id="37e73-118">The system supports DirectX 11.1.</span></span>
-   <span data-ttu-id="37e73-119">Il sistema include un driver WDDM 1,2.</span><span class="sxs-lookup"><span data-stu-id="37e73-119">The system includes a WDDM 1.2 driver.</span></span>
-   <span data-ttu-id="37e73-120">Il driver segnala il supporto per questa istruzione tramite le **\_ \_ Opzioni d3d11 dei dati della funzionalità d3d11 \_ \_ . ExtendedDoublesShaderInstructions** impostato su **true**.</span><span class="sxs-lookup"><span data-stu-id="37e73-120">The driver reports support for this instruction via **D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS.ExtendedDoublesShaderInstructions** set to **TRUE**.</span></span>

<span data-ttu-id="37e73-121">Nella tabella seguente vengono illustrati i risultati ottenuti quando si esegue l'istruzione con varie classi di numeri, presupponendo che non si verifichino overflow o underflow.</span><span class="sxs-lookup"><span data-stu-id="37e73-121">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span>

<span data-ttu-id="37e73-122">In questa tabella F indica un numero reale finito.</span><span class="sxs-lookup"><span data-stu-id="37e73-122">In this table F means finite-real number.</span></span>



|               |          |        |        |        |        |          |         |
|---------------|----------|--------|--------|--------|--------|----------|---------|
| <span data-ttu-id="37e73-123">**src**-></span><span class="sxs-lookup"><span data-stu-id="37e73-123">**src**-></span></span>  | <span data-ttu-id="37e73-124">**-INF**</span><span class="sxs-lookup"><span data-stu-id="37e73-124">**-inf**</span></span> | <span data-ttu-id="37e73-125">**-F**</span><span class="sxs-lookup"><span data-stu-id="37e73-125">**-F**</span></span> | <span data-ttu-id="37e73-126">**-0**</span><span class="sxs-lookup"><span data-stu-id="37e73-126">**-0**</span></span> | <span data-ttu-id="37e73-127">**+0**</span><span class="sxs-lookup"><span data-stu-id="37e73-127">**+0**</span></span> | <span data-ttu-id="37e73-128">**+ F**</span><span class="sxs-lookup"><span data-stu-id="37e73-128">**+F**</span></span> | <span data-ttu-id="37e73-129">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="37e73-129">**+inf**</span></span> | <span data-ttu-id="37e73-130">**NaN**</span><span class="sxs-lookup"><span data-stu-id="37e73-130">**NaN**</span></span> |
| <span data-ttu-id="37e73-131">**dest**-></span><span class="sxs-lookup"><span data-stu-id="37e73-131">**dest**-></span></span> | <span data-ttu-id="37e73-132">-0</span><span class="sxs-lookup"><span data-stu-id="37e73-132">-0</span></span>       | <span data-ttu-id="37e73-133">-F</span><span class="sxs-lookup"><span data-stu-id="37e73-133">-F</span></span>     | <span data-ttu-id="37e73-134">-inf</span><span class="sxs-lookup"><span data-stu-id="37e73-134">-inf</span></span>   | <span data-ttu-id="37e73-135">+inf</span><span class="sxs-lookup"><span data-stu-id="37e73-135">+inf</span></span>   | <span data-ttu-id="37e73-136">+ F</span><span class="sxs-lookup"><span data-stu-id="37e73-136">+F</span></span>     | <span data-ttu-id="37e73-137">+0</span><span class="sxs-lookup"><span data-stu-id="37e73-137">+0</span></span>       | <span data-ttu-id="37e73-138">NaN</span><span class="sxs-lookup"><span data-stu-id="37e73-138">NaN</span></span>     |



 

<span data-ttu-id="37e73-139">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="37e73-139">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="37e73-140">Vertice</span><span class="sxs-lookup"><span data-stu-id="37e73-140">Vertex</span></span> | <span data-ttu-id="37e73-141">Hull</span><span class="sxs-lookup"><span data-stu-id="37e73-141">Hull</span></span> | <span data-ttu-id="37e73-142">Dominio</span><span class="sxs-lookup"><span data-stu-id="37e73-142">Domain</span></span> | <span data-ttu-id="37e73-143">Geometria</span><span class="sxs-lookup"><span data-stu-id="37e73-143">Geometry</span></span> | <span data-ttu-id="37e73-144">Pixel</span><span class="sxs-lookup"><span data-stu-id="37e73-144">Pixel</span></span> | <span data-ttu-id="37e73-145">Calcolo</span><span class="sxs-lookup"><span data-stu-id="37e73-145">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="37e73-146">X</span><span class="sxs-lookup"><span data-stu-id="37e73-146">X</span></span>      | <span data-ttu-id="37e73-147">X</span><span class="sxs-lookup"><span data-stu-id="37e73-147">X</span></span>    | <span data-ttu-id="37e73-148">X</span><span class="sxs-lookup"><span data-stu-id="37e73-148">X</span></span>      | <span data-ttu-id="37e73-149">X</span><span class="sxs-lookup"><span data-stu-id="37e73-149">X</span></span>        | <span data-ttu-id="37e73-150">X</span><span class="sxs-lookup"><span data-stu-id="37e73-150">X</span></span>     | <span data-ttu-id="37e73-151">X</span><span class="sxs-lookup"><span data-stu-id="37e73-151">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="37e73-152">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="37e73-152">Minimum Shader Model</span></span>

<span data-ttu-id="37e73-153">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="37e73-153">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="37e73-154">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="37e73-154">Shader Model</span></span>                                              | <span data-ttu-id="37e73-155">Supportato</span><span class="sxs-lookup"><span data-stu-id="37e73-155">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="37e73-156">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="37e73-156">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="37e73-157">sì</span><span class="sxs-lookup"><span data-stu-id="37e73-157">yes</span></span>       |
| [<span data-ttu-id="37e73-158">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="37e73-158">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="37e73-159">no</span><span class="sxs-lookup"><span data-stu-id="37e73-159">no</span></span>        |
| [<span data-ttu-id="37e73-160">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="37e73-160">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="37e73-161">no</span><span class="sxs-lookup"><span data-stu-id="37e73-161">no</span></span>        |
| [<span data-ttu-id="37e73-162">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="37e73-162">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="37e73-163">no</span><span class="sxs-lookup"><span data-stu-id="37e73-163">no</span></span>        |
| [<span data-ttu-id="37e73-164">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="37e73-164">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="37e73-165">no</span><span class="sxs-lookup"><span data-stu-id="37e73-165">no</span></span>        |
| [<span data-ttu-id="37e73-166">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="37e73-166">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="37e73-167">no</span><span class="sxs-lookup"><span data-stu-id="37e73-167">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="37e73-168">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="37e73-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="37e73-169">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="37e73-169">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





