---
title: BFI (SM5-ASM)
description: Dato un intervallo di bit dall'LSB di un numero, inserire tale numero di bit in un altro numero a qualsiasi offset.
ms.assetid: BA84C882-A141-4AD2-8FD9-C60F1483FC65
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a14f8b9f6ef126ec3c6a31bf330dfd89cf0770c4
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104046098"
---
# <a name="bfi-sm5---asm"></a><span data-ttu-id="23840-103">BFI (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="23840-103">bfi (sm5 - asm)</span></span>

<span data-ttu-id="23840-104">Dato un intervallo di bit dall'LSB di un numero, inserire tale numero di bit in un altro numero a qualsiasi offset.</span><span class="sxs-lookup"><span data-stu-id="23840-104">Given a bit range from the LSB of a number, place that number of bits in another number at any offset.</span></span>



| <span data-ttu-id="23840-105">BFI dest \[ . mask \] , src0 \[ . Swizzle \] , src1 \[ . Swizzle \] , src2 \[ . Swizzle \] , src3 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="23840-105">bfi dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\], src2\[.swizzle\], src3\[.swizzle\]</span></span> |
|-------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="23840-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="23840-106">Item</span></span>                                                            | <span data-ttu-id="23840-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="23840-107">Description</span></span>                                                         |
|-----------------------------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="23840-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="23840-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="23840-109">\[nell' \] indirizzo dei risultati.</span><span class="sxs-lookup"><span data-stu-id="23840-109">\[in\] The address of the results.</span></span><br/>                       |
| <span data-ttu-id="23840-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="23840-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="23840-111">\[nella \] larghezza bit da *src2*.</span><span class="sxs-lookup"><span data-stu-id="23840-111">\[in\] The bitfield width to take from *src2*.</span></span><br/>           |
| <span data-ttu-id="23840-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="23840-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="23840-113">\[nell' \] offset bit per la sostituzione di bit in *src3*.</span><span class="sxs-lookup"><span data-stu-id="23840-113">\[in\] The bitfield offset for replacing bits in *src3*.</span></span><br/> |
| <span data-ttu-id="23840-114"><span id="src2"></span><span id="SRC2"></span>*src2*</span><span class="sxs-lookup"><span data-stu-id="23840-114"><span id="src2"></span><span id="SRC2"></span>*src2*</span></span><br/> | <span data-ttu-id="23840-115">\[il \] numero di bit da cui vengono ricavati i bit.</span><span class="sxs-lookup"><span data-stu-id="23840-115">\[in\] The number the bits are taken from.</span></span> <br/>              |
| <span data-ttu-id="23840-116"><span id="src3"></span><span id="SRC3"></span>*src3*</span><span class="sxs-lookup"><span data-stu-id="23840-116"><span id="src3"></span><span id="SRC3"></span>*src3*</span></span><br/> | <span data-ttu-id="23840-117">\[nel \] numero con bit da sostituire.</span><span class="sxs-lookup"><span data-stu-id="23840-117">\[in\] The number with bits to be replaced.</span></span><br/>              |



 

## <a name="remarks"></a><span data-ttu-id="23840-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="23840-118">Remarks</span></span>

<span data-ttu-id="23840-119">I LSB 5 bit di *src0* forniscono la larghezza bit (0-31) da *src2*.</span><span class="sxs-lookup"><span data-stu-id="23840-119">The LSB 5 bits of *src0* provide the bitfield width (0-31) to take from *src2*.</span></span>

<span data-ttu-id="23840-120">I LSB 5 bit di *src1* forniscono l'offset bit (0-31) per iniziare a sostituire bits nel numero letto da *src3*.</span><span class="sxs-lookup"><span data-stu-id="23840-120">The LSB 5 bits of *src1* provide the bitfield offset (0-31) to start replacing bits in the number read from *src3*.</span></span>

``` syntax
Given width, offset:
                bitmask = (((1 << width)-1) << offset) & 0xffffffff
                dest = ((src2 << offset) & bitmask) | (src3 & ~bitmask)
```

<span data-ttu-id="23840-121">Questa istruzione viene utilizzata per la compressione di interi o flag.</span><span class="sxs-lookup"><span data-stu-id="23840-121">This instruction is used for packing integers or flags.</span></span>

<span data-ttu-id="23840-122">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="23840-122">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="23840-123">Vertice</span><span class="sxs-lookup"><span data-stu-id="23840-123">Vertex</span></span> | <span data-ttu-id="23840-124">Hull</span><span class="sxs-lookup"><span data-stu-id="23840-124">Hull</span></span> | <span data-ttu-id="23840-125">Dominio</span><span class="sxs-lookup"><span data-stu-id="23840-125">Domain</span></span> | <span data-ttu-id="23840-126">Geometria</span><span class="sxs-lookup"><span data-stu-id="23840-126">Geometry</span></span> | <span data-ttu-id="23840-127">Pixel</span><span class="sxs-lookup"><span data-stu-id="23840-127">Pixel</span></span> | <span data-ttu-id="23840-128">Calcolo</span><span class="sxs-lookup"><span data-stu-id="23840-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="23840-129">X</span><span class="sxs-lookup"><span data-stu-id="23840-129">X</span></span>      | <span data-ttu-id="23840-130">X</span><span class="sxs-lookup"><span data-stu-id="23840-130">X</span></span>    | <span data-ttu-id="23840-131">X</span><span class="sxs-lookup"><span data-stu-id="23840-131">X</span></span>      | <span data-ttu-id="23840-132">X</span><span class="sxs-lookup"><span data-stu-id="23840-132">X</span></span>        | <span data-ttu-id="23840-133">X</span><span class="sxs-lookup"><span data-stu-id="23840-133">X</span></span>     | <span data-ttu-id="23840-134">X</span><span class="sxs-lookup"><span data-stu-id="23840-134">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="23840-135">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="23840-135">Minimum Shader Model</span></span>

<span data-ttu-id="23840-136">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="23840-136">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="23840-137">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="23840-137">Shader Model</span></span>                                              | <span data-ttu-id="23840-138">Supportato</span><span class="sxs-lookup"><span data-stu-id="23840-138">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="23840-139">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="23840-139">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="23840-140">sì</span><span class="sxs-lookup"><span data-stu-id="23840-140">yes</span></span>       |
| [<span data-ttu-id="23840-141">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="23840-141">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="23840-142">no</span><span class="sxs-lookup"><span data-stu-id="23840-142">no</span></span>        |
| [<span data-ttu-id="23840-143">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="23840-143">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="23840-144">no</span><span class="sxs-lookup"><span data-stu-id="23840-144">no</span></span>        |
| [<span data-ttu-id="23840-145">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="23840-145">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="23840-146">no</span><span class="sxs-lookup"><span data-stu-id="23840-146">no</span></span>        |
| [<span data-ttu-id="23840-147">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="23840-147">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="23840-148">no</span><span class="sxs-lookup"><span data-stu-id="23840-148">no</span></span>        |
| [<span data-ttu-id="23840-149">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="23840-149">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="23840-150">no</span><span class="sxs-lookup"><span data-stu-id="23840-150">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="23840-151">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="23840-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23840-152">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="23840-152">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





