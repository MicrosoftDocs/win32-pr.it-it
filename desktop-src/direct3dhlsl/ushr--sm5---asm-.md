---
title: USHR (SM5-ASM)
description: Spostamento a destra. | USHR (SM5-ASM)
ms.assetid: C695CB6C-A6C9-4DC8-8EBE-70A0CFFC4981
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f33c627ec4aa985b5ac8a27cf0babd6219c9247c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981687"
---
# <a name="ushr-sm5---asm"></a><span data-ttu-id="b6fac-104">USHR (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="b6fac-104">ushr (sm5 - asm)</span></span>

<span data-ttu-id="b6fac-105">Spostamento a destra.</span><span class="sxs-lookup"><span data-stu-id="b6fac-105">Shift right.</span></span>



| <span data-ttu-id="b6fac-106">ubfe dest \[ . mask \] , src0 \[ . Swizzle \] , src1 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="b6fac-106">ubfe dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|--------------------------------------------------------|



 



| <span data-ttu-id="b6fac-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="b6fac-107">Item</span></span>                                                            | <span data-ttu-id="b6fac-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b6fac-108">Description</span></span>                                                                  |
|-----------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="b6fac-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="b6fac-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="b6fac-110">\[in \] contiene i risultati dell'istruzione.</span><span class="sxs-lookup"><span data-stu-id="b6fac-110">\[in\] Contains the results of the instruction.</span></span><br/>                   |
| <span data-ttu-id="b6fac-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="b6fac-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="b6fac-112">\[nei \] valori a 32 bit da spostare.</span><span class="sxs-lookup"><span data-stu-id="b6fac-112">\[in\] The 32-bit values to shift.</span></span><br/>                                |
| <span data-ttu-id="b6fac-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="b6fac-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="b6fac-114">\[in \] LSB 5 bits specificare il numero di bit da spostare (0-31).</span><span class="sxs-lookup"><span data-stu-id="b6fac-114">\[in\] The LSB 5 bits provide the number of bits to shift (0-31).</span></span><br/> |



 

<span data-ttu-id="b6fac-115">Questa istruzione esegue uno spostamento a livello di componente di ogni valore a 32 bit in *src0* a destra di un numero di bit unsigned integer fornito da LSB 5 bits (intervallo 0-31) in *src1*, inserendo 0.</span><span class="sxs-lookup"><span data-stu-id="b6fac-115">This instruction performs a component-wise shift of each 32-bit value in *src0* right by an unsigned integer bit count provided by the LSB 5 bits (0-31 range) in *src1*, inserting 0.</span></span> <span data-ttu-id="b6fac-116">I risultati a 32 bit per componente sono posizionati in *dest*.</span><span class="sxs-lookup"><span data-stu-id="b6fac-116">The 32-bit per component results is placed in *dest*.</span></span>

<span data-ttu-id="b6fac-117">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="b6fac-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="b6fac-118">Vertice</span><span class="sxs-lookup"><span data-stu-id="b6fac-118">Vertex</span></span> | <span data-ttu-id="b6fac-119">Hull</span><span class="sxs-lookup"><span data-stu-id="b6fac-119">Hull</span></span> | <span data-ttu-id="b6fac-120">Dominio</span><span class="sxs-lookup"><span data-stu-id="b6fac-120">Domain</span></span> | <span data-ttu-id="b6fac-121">Geometria</span><span class="sxs-lookup"><span data-stu-id="b6fac-121">Geometry</span></span> | <span data-ttu-id="b6fac-122">Pixel</span><span class="sxs-lookup"><span data-stu-id="b6fac-122">Pixel</span></span> | <span data-ttu-id="b6fac-123">Calcolo</span><span class="sxs-lookup"><span data-stu-id="b6fac-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="b6fac-124">X</span><span class="sxs-lookup"><span data-stu-id="b6fac-124">X</span></span>      | <span data-ttu-id="b6fac-125">X</span><span class="sxs-lookup"><span data-stu-id="b6fac-125">X</span></span>    | <span data-ttu-id="b6fac-126">X</span><span class="sxs-lookup"><span data-stu-id="b6fac-126">X</span></span>      | <span data-ttu-id="b6fac-127">X</span><span class="sxs-lookup"><span data-stu-id="b6fac-127">X</span></span>        | <span data-ttu-id="b6fac-128">X</span><span class="sxs-lookup"><span data-stu-id="b6fac-128">X</span></span>     | <span data-ttu-id="b6fac-129">X</span><span class="sxs-lookup"><span data-stu-id="b6fac-129">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="b6fac-130">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="b6fac-130">Minimum Shader Model</span></span>

<span data-ttu-id="b6fac-131">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="b6fac-131">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="b6fac-132">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="b6fac-132">Shader Model</span></span>                                              | <span data-ttu-id="b6fac-133">Supportato</span><span class="sxs-lookup"><span data-stu-id="b6fac-133">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="b6fac-134">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="b6fac-134">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="b6fac-135">sì</span><span class="sxs-lookup"><span data-stu-id="b6fac-135">yes</span></span>       |
| [<span data-ttu-id="b6fac-136">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="b6fac-136">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="b6fac-137">no</span><span class="sxs-lookup"><span data-stu-id="b6fac-137">no</span></span>        |
| [<span data-ttu-id="b6fac-138">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="b6fac-138">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="b6fac-139">no</span><span class="sxs-lookup"><span data-stu-id="b6fac-139">no</span></span>        |
| [<span data-ttu-id="b6fac-140">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b6fac-140">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="b6fac-141">no</span><span class="sxs-lookup"><span data-stu-id="b6fac-141">no</span></span>        |
| [<span data-ttu-id="b6fac-142">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b6fac-142">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="b6fac-143">no</span><span class="sxs-lookup"><span data-stu-id="b6fac-143">no</span></span>        |
| [<span data-ttu-id="b6fac-144">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b6fac-144">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="b6fac-145">no</span><span class="sxs-lookup"><span data-stu-id="b6fac-145">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="b6fac-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b6fac-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b6fac-147">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b6fac-147">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





