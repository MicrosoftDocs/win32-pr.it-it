---
title: DMin (SM5-ASM)
description: Valore minimo a precisione doppia per componente.
ms.assetid: 77331B4D-C4B5-49B2-BB6A-77BD5050B575
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e199b01c68acca6609123425438f309af872fb4
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104046090"
---
# <a name="dmin-sm5---asm"></a><span data-ttu-id="64360-103">DMin (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="64360-103">dmin (sm5 - asm)</span></span>

<span data-ttu-id="64360-104">Valore minimo a precisione doppia per componente.</span><span class="sxs-lookup"><span data-stu-id="64360-104">Component-wise double-precision minimum.</span></span>



| <span data-ttu-id="64360-105">dmin \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="64360-105">dmin\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|---------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="64360-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="64360-106">Item</span></span>                                                            | <span data-ttu-id="64360-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="64360-107">Description</span></span>                                                                                                                                                                                                  |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64360-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="64360-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="64360-109">\[nell' \] indirizzo dei risultati dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="64360-109">\[in\] The address of the results of the operation.</span></span><br/> <span data-ttu-id="64360-110">*dest*  =  *src0*  <  *src1* ?</span><span class="sxs-lookup"><span data-stu-id="64360-110">*dest* = *src0* < *src1* ?</span></span> <span data-ttu-id="64360-111">*src0* : *src1*</span><span class="sxs-lookup"><span data-stu-id="64360-111">*src0* : *src1*</span></span><br/> <span data-ttu-id="64360-112">< viene usato al posto di <= in modo che se min (x, y) = x then Max (x, y) = y.</span><span class="sxs-lookup"><span data-stu-id="64360-112">< is used instead of <= so that if min(x,y) = x then max(x,y) = y.</span></span> <br/> |
| <span data-ttu-id="64360-113"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="64360-113"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="64360-114">\[nei \] componenti da confrontare con *src1*.</span><span class="sxs-lookup"><span data-stu-id="64360-114">\[in\] The components to compare with *src1*.</span></span><br/>                                                                                                                                                     |
| <span data-ttu-id="64360-115"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="64360-115"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="64360-116">\[nei \] componenti da confrontare con *src0*.</span><span class="sxs-lookup"><span data-stu-id="64360-116">\[in\] The components to compare with *src0*.</span></span><br/>                                                                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="64360-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="64360-117">Remarks</span></span>

<span data-ttu-id="64360-118">NaN ha una gestione speciale.</span><span class="sxs-lookup"><span data-stu-id="64360-118">NaN has special handling.</span></span> <span data-ttu-id="64360-119">Se un operando di origine è NaN, viene restituito l'altro operando di origine.</span><span class="sxs-lookup"><span data-stu-id="64360-119">If one source operand is NaN, then the other source operand is returned.</span></span> <span data-ttu-id="64360-120">La scelta viene effettuata per ogni componente.</span><span class="sxs-lookup"><span data-stu-id="64360-120">The choice is made per-component.</span></span> <span data-ttu-id="64360-121">Se entrambi sono NaN, viene restituita qualsiasi rappresentazione NaN.</span><span class="sxs-lookup"><span data-stu-id="64360-121">If both are NaN, any NaN representation is returned.</span></span>

<span data-ttu-id="64360-122">I swizzles validi per i parametri di origine sono xyzw, Xyxy, zwxy, zwzw.</span><span class="sxs-lookup"><span data-stu-id="64360-122">The valid swizzles for the source parameters are .xyzw, .xyxy, .zwxy, .zwzw.</span></span> <span data-ttu-id="64360-123">Le maschere *dest* valide sono. XY,. ZW e. xyzw.</span><span class="sxs-lookup"><span data-stu-id="64360-123">The valid *dest* masks are .xy, .zw, and .xyzw.</span></span> <span data-ttu-id="64360-124">I mapping *src* seguenti sono post-swizzle:</span><span class="sxs-lookup"><span data-stu-id="64360-124">The following *src* mappings are post-swizzle:</span></span>

-   <span data-ttu-id="64360-125">*dest* è un doppio vec2 tra (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="64360-125">*dest* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="64360-126">*src0* è un vec2 doppio tra (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="64360-126">*src0* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="64360-127">*src1* è un vec2 doppio tra (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="64360-127">*src1* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>

<span data-ttu-id="64360-128">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="64360-128">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="64360-129">Vertice</span><span class="sxs-lookup"><span data-stu-id="64360-129">Vertex</span></span> | <span data-ttu-id="64360-130">Hull</span><span class="sxs-lookup"><span data-stu-id="64360-130">Hull</span></span> | <span data-ttu-id="64360-131">Dominio</span><span class="sxs-lookup"><span data-stu-id="64360-131">Domain</span></span> | <span data-ttu-id="64360-132">Geometria</span><span class="sxs-lookup"><span data-stu-id="64360-132">Geometry</span></span> | <span data-ttu-id="64360-133">Pixel</span><span class="sxs-lookup"><span data-stu-id="64360-133">Pixel</span></span> | <span data-ttu-id="64360-134">Calcolo</span><span class="sxs-lookup"><span data-stu-id="64360-134">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="64360-135">X</span><span class="sxs-lookup"><span data-stu-id="64360-135">X</span></span>      | <span data-ttu-id="64360-136">X</span><span class="sxs-lookup"><span data-stu-id="64360-136">X</span></span>    | <span data-ttu-id="64360-137">X</span><span class="sxs-lookup"><span data-stu-id="64360-137">X</span></span>      | <span data-ttu-id="64360-138">X</span><span class="sxs-lookup"><span data-stu-id="64360-138">X</span></span>        | <span data-ttu-id="64360-139">X</span><span class="sxs-lookup"><span data-stu-id="64360-139">X</span></span>     | <span data-ttu-id="64360-140">X</span><span class="sxs-lookup"><span data-stu-id="64360-140">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="64360-141">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="64360-141">Minimum Shader Model</span></span>

<span data-ttu-id="64360-142">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="64360-142">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="64360-143">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="64360-143">Shader Model</span></span>                                              | <span data-ttu-id="64360-144">Supportato</span><span class="sxs-lookup"><span data-stu-id="64360-144">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="64360-145">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="64360-145">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="64360-146">sì</span><span class="sxs-lookup"><span data-stu-id="64360-146">yes</span></span>       |
| [<span data-ttu-id="64360-147">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="64360-147">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="64360-148">no</span><span class="sxs-lookup"><span data-stu-id="64360-148">no</span></span>        |
| [<span data-ttu-id="64360-149">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="64360-149">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="64360-150">no</span><span class="sxs-lookup"><span data-stu-id="64360-150">no</span></span>        |
| [<span data-ttu-id="64360-151">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="64360-151">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="64360-152">no</span><span class="sxs-lookup"><span data-stu-id="64360-152">no</span></span>        |
| [<span data-ttu-id="64360-153">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="64360-153">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="64360-154">no</span><span class="sxs-lookup"><span data-stu-id="64360-154">no</span></span>        |
| [<span data-ttu-id="64360-155">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="64360-155">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="64360-156">no</span><span class="sxs-lookup"><span data-stu-id="64360-156">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="64360-157">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="64360-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="64360-158">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="64360-158">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





