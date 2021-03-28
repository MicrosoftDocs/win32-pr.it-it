---
title: ishl (sm5 - asm)
description: Spostamento a sinistra. | ISHL (SM5-ASM)
ms.assetid: 3EE669BA-252D-4617-85B0-AEBB7F7E4C5E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 230034e66ca9adfbd6c94cc99351b485c6577fdf
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353126"
---
# <a name="ishl-sm5---asm"></a><span data-ttu-id="f44ac-104">ishl (sm5 - asm)</span><span class="sxs-lookup"><span data-stu-id="f44ac-104">ishl (sm5 - asm)</span></span>

<span data-ttu-id="f44ac-105">Spostamento a sinistra.</span><span class="sxs-lookup"><span data-stu-id="f44ac-105">Shift left.</span></span>



| <span data-ttu-id="f44ac-106">ISHL dest \[ . mask \] , src0 \[ . Swizzle \] , src1 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="f44ac-106">ishl dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|--------------------------------------------------------|



 



| <span data-ttu-id="f44ac-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="f44ac-107">Item</span></span>                                                            | <span data-ttu-id="f44ac-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f44ac-108">Description</span></span>                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f44ac-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="f44ac-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="f44ac-110">\[in \] contiene i risultati dello spostamento.</span><span class="sxs-lookup"><span data-stu-id="f44ac-110">\[in\] Contains the results of the shift.</span></span><br/> |
| <span data-ttu-id="f44ac-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="f44ac-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="f44ac-112">\[nei \] valori a 32 bit da spostare.</span><span class="sxs-lookup"><span data-stu-id="f44ac-112">\[in\] The 32-bit values to shift.</span></span><br/>       |
| <span data-ttu-id="f44ac-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="f44ac-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="f44ac-114">\[\]numero di bit da spostare.</span><span class="sxs-lookup"><span data-stu-id="f44ac-114">\[in\] The number of bits to shift.</span></span><br/>        |



 

## <a name="remarks"></a><span data-ttu-id="f44ac-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="f44ac-115">Remarks</span></span>

<span data-ttu-id="f44ac-116">Questa istruzione esegue uno spostamento a livello di componente di ogni valore a 32 bit in *src0* a sinistra di un numero di bit unsigned integer fornito da LSB 5 bits (intervallo 0-31) in *src1*, inserendo 0.</span><span class="sxs-lookup"><span data-stu-id="f44ac-116">This instruction performs a component-wise shift of each 32-bit value in *src0* left by an unsigned integer bit count provided by the LSB 5 bits (0-31 range) in *src1*, inserting 0.</span></span> <span data-ttu-id="f44ac-117">I risultati a 32 bit per componente sono posizionati in *dest*.</span><span class="sxs-lookup"><span data-stu-id="f44ac-117">The 32-bit per component results are placed in *dest*.</span></span>

<span data-ttu-id="f44ac-118">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="f44ac-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="f44ac-119">Vertice</span><span class="sxs-lookup"><span data-stu-id="f44ac-119">Vertex</span></span> | <span data-ttu-id="f44ac-120">Hull</span><span class="sxs-lookup"><span data-stu-id="f44ac-120">Hull</span></span> | <span data-ttu-id="f44ac-121">Dominio</span><span class="sxs-lookup"><span data-stu-id="f44ac-121">Domain</span></span> | <span data-ttu-id="f44ac-122">Geometria</span><span class="sxs-lookup"><span data-stu-id="f44ac-122">Geometry</span></span> | <span data-ttu-id="f44ac-123">Pixel</span><span class="sxs-lookup"><span data-stu-id="f44ac-123">Pixel</span></span> | <span data-ttu-id="f44ac-124">Calcolo</span><span class="sxs-lookup"><span data-stu-id="f44ac-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="f44ac-125">X</span><span class="sxs-lookup"><span data-stu-id="f44ac-125">X</span></span>      | <span data-ttu-id="f44ac-126">X</span><span class="sxs-lookup"><span data-stu-id="f44ac-126">X</span></span>    | <span data-ttu-id="f44ac-127">X</span><span class="sxs-lookup"><span data-stu-id="f44ac-127">X</span></span>      | <span data-ttu-id="f44ac-128">X</span><span class="sxs-lookup"><span data-stu-id="f44ac-128">X</span></span>        | <span data-ttu-id="f44ac-129">X</span><span class="sxs-lookup"><span data-stu-id="f44ac-129">X</span></span>     | <span data-ttu-id="f44ac-130">X</span><span class="sxs-lookup"><span data-stu-id="f44ac-130">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="f44ac-131">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="f44ac-131">Minimum Shader Model</span></span>

<span data-ttu-id="f44ac-132">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="f44ac-132">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="f44ac-133">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="f44ac-133">Shader Model</span></span>                                              | <span data-ttu-id="f44ac-134">Supportato</span><span class="sxs-lookup"><span data-stu-id="f44ac-134">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="f44ac-135">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="f44ac-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="f44ac-136">sì</span><span class="sxs-lookup"><span data-stu-id="f44ac-136">yes</span></span>       |
| [<span data-ttu-id="f44ac-137">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="f44ac-137">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="f44ac-138">no</span><span class="sxs-lookup"><span data-stu-id="f44ac-138">no</span></span>        |
| [<span data-ttu-id="f44ac-139">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="f44ac-139">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="f44ac-140">no</span><span class="sxs-lookup"><span data-stu-id="f44ac-140">no</span></span>        |
| [<span data-ttu-id="f44ac-141">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f44ac-141">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="f44ac-142">no</span><span class="sxs-lookup"><span data-stu-id="f44ac-142">no</span></span>        |
| [<span data-ttu-id="f44ac-143">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f44ac-143">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="f44ac-144">no</span><span class="sxs-lookup"><span data-stu-id="f44ac-144">no</span></span>        |
| [<span data-ttu-id="f44ac-145">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f44ac-145">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="f44ac-146">no</span><span class="sxs-lookup"><span data-stu-id="f44ac-146">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="f44ac-147">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f44ac-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f44ac-148">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f44ac-148">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





