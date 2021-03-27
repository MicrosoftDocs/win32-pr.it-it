---
title: DMAX (SM5-ASM)
description: Valore massimo a precisione doppia a livello di componente.
ms.assetid: 34ED8B34-2592-4BBB-BCF0-F2222E4D51D9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 703b277a98b16570de6f5ab7e0e7643ddfdcc705
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398214"
---
# <a name="dmax-sm5---asm"></a><span data-ttu-id="87568-103">DMAX (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="87568-103">dmax (sm5 - asm)</span></span>

<span data-ttu-id="87568-104">Valore massimo a precisione doppia a livello di componente.</span><span class="sxs-lookup"><span data-stu-id="87568-104">Component-wise double-precision maximum.</span></span>



| <span data-ttu-id="87568-105">DMAX \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="87568-105">dmax\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|---------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="87568-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="87568-106">Item</span></span>                                                            | <span data-ttu-id="87568-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="87568-107">Description</span></span>                                                                                                                                                                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87568-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="87568-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="87568-109">\[nell' \] indirizzo dei risultati dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="87568-109">\[in\] The address of the results of the operation.</span></span><br/> <span data-ttu-id="87568-110">*dest*  =  *src0*  >=  *src1* ?</span><span class="sxs-lookup"><span data-stu-id="87568-110">*dest* = *src0* >= *src1* ?</span></span> <span data-ttu-id="87568-111">*src0* : *src1*</span><span class="sxs-lookup"><span data-stu-id="87568-111">*src0* : *src1*</span></span><br/> <span data-ttu-id="87568-112">>= viene usato al posto di > in modo che se min (x, y) = x then Max (x, y) = y.</span><span class="sxs-lookup"><span data-stu-id="87568-112">>= is used instead of > so that if min(x,y) = x then max(x,y) = y.</span></span> <br/> |
| <span data-ttu-id="87568-113"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="87568-113"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="87568-114">\[nel \] valore da confrontare con *src1*.</span><span class="sxs-lookup"><span data-stu-id="87568-114">\[in\] The value to compare with *src1*.</span></span><br/>                                                                                                                                                           |
| <span data-ttu-id="87568-115"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="87568-115"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="87568-116">\[nel \] valore da confrontare con *src0*.</span><span class="sxs-lookup"><span data-stu-id="87568-116">\[in\] The value to compare with *src0*.</span></span><br/>                                                                                                                                                           |



 

## <a name="remarks"></a><span data-ttu-id="87568-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="87568-117">Remarks</span></span>

<span data-ttu-id="87568-118">NaN ha una gestione speciale.</span><span class="sxs-lookup"><span data-stu-id="87568-118">NaN has special handling.</span></span> <span data-ttu-id="87568-119">Se un operando di origine è NaN, viene restituito l'altro operando di origine.</span><span class="sxs-lookup"><span data-stu-id="87568-119">If one source operand is NaN, then the other source operand is returned.</span></span> <span data-ttu-id="87568-120">La scelta viene effettuata per ogni componente.</span><span class="sxs-lookup"><span data-stu-id="87568-120">The choice is made per-component.</span></span> <span data-ttu-id="87568-121">Se entrambi sono NaN, viene restituita qualsiasi rappresentazione NaN.</span><span class="sxs-lookup"><span data-stu-id="87568-121">If both are NaN, any NaN representation is returned.</span></span>

<span data-ttu-id="87568-122">I swizzles validi per i parametri di origine sono xyzw, Xyxy, zwxy, zwzw.</span><span class="sxs-lookup"><span data-stu-id="87568-122">The valid swizzles for the source parameters are .xyzw, .xyxy, .zwxy, .zwzw.</span></span> <span data-ttu-id="87568-123">Le maschere *dest* valide sono. XY,. ZW e. xyzw.</span><span class="sxs-lookup"><span data-stu-id="87568-123">The valid *dest* masks are .xy, .zw, and .xyzw.</span></span> <span data-ttu-id="87568-124">I mapping *src* seguenti sono post-swizzle:</span><span class="sxs-lookup"><span data-stu-id="87568-124">The following *src* mappings are post-swizzle:</span></span>

-   <span data-ttu-id="87568-125">*dest* è un doppio vec2 tra (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="87568-125">*dest* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="87568-126">*src0* è un vec2 doppio tra (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="87568-126">*src0* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="87568-127">*src1* è un vec2 doppio tra (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="87568-127">*src1* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>

<span data-ttu-id="87568-128">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="87568-128">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="87568-129">Vertice</span><span class="sxs-lookup"><span data-stu-id="87568-129">Vertex</span></span> | <span data-ttu-id="87568-130">Hull</span><span class="sxs-lookup"><span data-stu-id="87568-130">Hull</span></span> | <span data-ttu-id="87568-131">Dominio</span><span class="sxs-lookup"><span data-stu-id="87568-131">Domain</span></span> | <span data-ttu-id="87568-132">Geometria</span><span class="sxs-lookup"><span data-stu-id="87568-132">Geometry</span></span> | <span data-ttu-id="87568-133">Pixel</span><span class="sxs-lookup"><span data-stu-id="87568-133">Pixel</span></span> | <span data-ttu-id="87568-134">Calcolo</span><span class="sxs-lookup"><span data-stu-id="87568-134">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="87568-135">X</span><span class="sxs-lookup"><span data-stu-id="87568-135">X</span></span>      | <span data-ttu-id="87568-136">X</span><span class="sxs-lookup"><span data-stu-id="87568-136">X</span></span>    | <span data-ttu-id="87568-137">X</span><span class="sxs-lookup"><span data-stu-id="87568-137">X</span></span>      | <span data-ttu-id="87568-138">X</span><span class="sxs-lookup"><span data-stu-id="87568-138">X</span></span>        | <span data-ttu-id="87568-139">X</span><span class="sxs-lookup"><span data-stu-id="87568-139">X</span></span>     | <span data-ttu-id="87568-140">X</span><span class="sxs-lookup"><span data-stu-id="87568-140">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="87568-141">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="87568-141">Minimum Shader Model</span></span>

<span data-ttu-id="87568-142">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="87568-142">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="87568-143">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="87568-143">Shader Model</span></span>                                              | <span data-ttu-id="87568-144">Supportato</span><span class="sxs-lookup"><span data-stu-id="87568-144">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="87568-145">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="87568-145">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="87568-146">sì</span><span class="sxs-lookup"><span data-stu-id="87568-146">yes</span></span>       |
| [<span data-ttu-id="87568-147">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="87568-147">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="87568-148">no</span><span class="sxs-lookup"><span data-stu-id="87568-148">no</span></span>        |
| [<span data-ttu-id="87568-149">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="87568-149">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="87568-150">no</span><span class="sxs-lookup"><span data-stu-id="87568-150">no</span></span>        |
| [<span data-ttu-id="87568-151">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="87568-151">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="87568-152">no</span><span class="sxs-lookup"><span data-stu-id="87568-152">no</span></span>        |
| [<span data-ttu-id="87568-153">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="87568-153">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="87568-154">no</span><span class="sxs-lookup"><span data-stu-id="87568-154">no</span></span>        |
| [<span data-ttu-id="87568-155">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="87568-155">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="87568-156">no</span><span class="sxs-lookup"><span data-stu-id="87568-156">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="87568-157">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="87568-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87568-158">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="87568-158">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





