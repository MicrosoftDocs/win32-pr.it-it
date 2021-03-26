---
title: IBFE (SM5-ASM)
description: Dato un intervallo di bit in un numero, spostare tali bit in LSB e firmare estendendo l'MSB dell'intervallo.
ms.assetid: 1ED39812-A89F-4325-82A0-DA2CCC55A99A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 805d5c1137e25d8b8fa560588b9e876ccc5c8748
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "103719369"
---
# <a name="ibfe-sm5---asm"></a><span data-ttu-id="80d0c-103">IBFE (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="80d0c-103">ibfe (sm5 - asm)</span></span>

<span data-ttu-id="80d0c-104">Dato un intervallo di bit in un numero, spostare tali bit in LSB e firmare estendendo l'MSB dell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="80d0c-104">Given a range of bits in a number, shift those bits to the LSB and sign extend the MSB of the range.</span></span>



| <span data-ttu-id="80d0c-105">IBFE dest \[ . mask \] , src0 \[ . Swizzle \] , src1 \[ . Swizzle \] , src2 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="80d0c-105">ibfe dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\], src2\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------|



 



| <span data-ttu-id="80d0c-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="80d0c-106">Item</span></span>                                                            | <span data-ttu-id="80d0c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="80d0c-107">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="80d0c-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="80d0c-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="80d0c-109">\[nell' \] indirizzo dei risultati dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="80d0c-109">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="80d0c-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="80d0c-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="80d0c-111">\[nella \] larghezza bit.</span><span class="sxs-lookup"><span data-stu-id="80d0c-111">\[in\] The bitfield width.</span></span><br/>                          |
| <span data-ttu-id="80d0c-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="80d0c-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="80d0c-113">\[nell' \] offset bit.</span><span class="sxs-lookup"><span data-stu-id="80d0c-113">\[in\] The bitfield offset.</span></span><br/>                         |
| <span data-ttu-id="80d0c-114"><span id="src2"></span><span id="SRC2"></span>*src2*</span><span class="sxs-lookup"><span data-stu-id="80d0c-114"><span id="src2"></span><span id="SRC2"></span>*src2*</span></span><br/> | <span data-ttu-id="80d0c-115">\[nel \] valore da spostare.</span><span class="sxs-lookup"><span data-stu-id="80d0c-115">\[in\] The value to shift.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="80d0c-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="80d0c-116">Remarks</span></span>

<span data-ttu-id="80d0c-117">I LSB 5 bit di src0 forniscono la larghezza bit (0-31).</span><span class="sxs-lookup"><span data-stu-id="80d0c-117">The LSB 5 bits of src0 provide the bitfield width (0-31).</span></span>

<span data-ttu-id="80d0c-118">Il LSB 5 bit di src1 fornisce l'offset bit (0-31).</span><span class="sxs-lookup"><span data-stu-id="80d0c-118">The LSB 5 bits of src1 provide the bitfield offset (0-31).</span></span>

<span data-ttu-id="80d0c-119">Nell'esempio seguente viene illustrato come utilizzare questa istruzione.</span><span class="sxs-lookup"><span data-stu-id="80d0c-119">The following example shows how to use this instruction.</span></span>

``` syntax
        Given width, offset:
                if( width == 0 )
                {
                    dest = 0
                }
                else if( width + offset < 32 )
                {
                    shl dest, src2, 32-(width+offset)
                    ishr dest, dest, 32-width
                }
                else
                {
                    ishr dest, src2, offset
                }
```

<span data-ttu-id="80d0c-120">Usare questa istruzione per decomprimere interi o flag con segno.</span><span class="sxs-lookup"><span data-stu-id="80d0c-120">Use this instruction to unpack signed integers or flags.</span></span>

<span data-ttu-id="80d0c-121">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="80d0c-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="80d0c-122">Vertice</span><span class="sxs-lookup"><span data-stu-id="80d0c-122">Vertex</span></span> | <span data-ttu-id="80d0c-123">Hull</span><span class="sxs-lookup"><span data-stu-id="80d0c-123">Hull</span></span> | <span data-ttu-id="80d0c-124">Dominio</span><span class="sxs-lookup"><span data-stu-id="80d0c-124">Domain</span></span> | <span data-ttu-id="80d0c-125">Geometria</span><span class="sxs-lookup"><span data-stu-id="80d0c-125">Geometry</span></span> | <span data-ttu-id="80d0c-126">Pixel</span><span class="sxs-lookup"><span data-stu-id="80d0c-126">Pixel</span></span> | <span data-ttu-id="80d0c-127">Calcolo</span><span class="sxs-lookup"><span data-stu-id="80d0c-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="80d0c-128">X</span><span class="sxs-lookup"><span data-stu-id="80d0c-128">X</span></span>      | <span data-ttu-id="80d0c-129">X</span><span class="sxs-lookup"><span data-stu-id="80d0c-129">X</span></span>    | <span data-ttu-id="80d0c-130">X</span><span class="sxs-lookup"><span data-stu-id="80d0c-130">X</span></span>      | <span data-ttu-id="80d0c-131">X</span><span class="sxs-lookup"><span data-stu-id="80d0c-131">X</span></span>        | <span data-ttu-id="80d0c-132">X</span><span class="sxs-lookup"><span data-stu-id="80d0c-132">X</span></span>     | <span data-ttu-id="80d0c-133">X</span><span class="sxs-lookup"><span data-stu-id="80d0c-133">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="80d0c-134">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="80d0c-134">Minimum Shader Model</span></span>

<span data-ttu-id="80d0c-135">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="80d0c-135">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="80d0c-136">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="80d0c-136">Shader Model</span></span>                                              | <span data-ttu-id="80d0c-137">Supportato</span><span class="sxs-lookup"><span data-stu-id="80d0c-137">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="80d0c-138">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="80d0c-138">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="80d0c-139">sì</span><span class="sxs-lookup"><span data-stu-id="80d0c-139">yes</span></span>       |
| [<span data-ttu-id="80d0c-140">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="80d0c-140">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="80d0c-141">no</span><span class="sxs-lookup"><span data-stu-id="80d0c-141">no</span></span>        |
| [<span data-ttu-id="80d0c-142">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="80d0c-142">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="80d0c-143">no</span><span class="sxs-lookup"><span data-stu-id="80d0c-143">no</span></span>        |
| [<span data-ttu-id="80d0c-144">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="80d0c-144">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="80d0c-145">no</span><span class="sxs-lookup"><span data-stu-id="80d0c-145">no</span></span>        |
| [<span data-ttu-id="80d0c-146">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="80d0c-146">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="80d0c-147">no</span><span class="sxs-lookup"><span data-stu-id="80d0c-147">no</span></span>        |
| [<span data-ttu-id="80d0c-148">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="80d0c-148">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="80d0c-149">no</span><span class="sxs-lookup"><span data-stu-id="80d0c-149">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="80d0c-150">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="80d0c-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80d0c-151">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="80d0c-151">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





