---
title: ubfe (SM5-ASM)
description: Dato un intervallo di bit in un numero, spostare tali bit in LSB e impostare i bit rimanenti su 0.
ms.assetid: CC6BE378-2726-47A2-8E23-B8151521F72D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43ebbe853ec1b53b452f32d79c9c2ec120e826b8
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "103857770"
---
# <a name="ubfe-sm5---asm"></a><span data-ttu-id="31ff6-103">ubfe (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="31ff6-103">ubfe (sm5 - asm)</span></span>

<span data-ttu-id="31ff6-104">Dato un intervallo di bit in un numero, spostare tali bit in LSB e impostare i bit rimanenti su 0.</span><span class="sxs-lookup"><span data-stu-id="31ff6-104">Given a range of bits in a number, shift those bits to the LSB and set remaining bits to 0.</span></span>



| <span data-ttu-id="31ff6-105">ubfe dest \[ . mask \] , src0 \[ . Swizzle \] , src1 \[ . Swizzle \] , src2 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="31ff6-105">ubfe dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\], src2\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------|



 



| <span data-ttu-id="31ff6-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="31ff6-106">Item</span></span>                                                            | <span data-ttu-id="31ff6-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="31ff6-107">Description</span></span>                                                                    |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="31ff6-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="31ff6-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="31ff6-109">\[in \] contiene i risultati dell'istruzione.</span><span class="sxs-lookup"><span data-stu-id="31ff6-109">\[in\] Contains the results of the instruction.</span></span><br/>                     |
| <span data-ttu-id="31ff6-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="31ff6-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="31ff6-111">\[in \] LSB 5 bits specificare la larghezza bit (0-31).</span><span class="sxs-lookup"><span data-stu-id="31ff6-111">\[in\] The LSB 5 bits provide the bitfield width (0-31).</span></span><br/>            |
| <span data-ttu-id="31ff6-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="31ff6-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="31ff6-113">\[nei \] bit LSB 5 di *src1* specificare l'offset bit (0-31).</span><span class="sxs-lookup"><span data-stu-id="31ff6-113">\[in\] The LSB 5 bits of *src1* provide the bitfield offset (0-31).</span></span><br/> |
| <span data-ttu-id="31ff6-114"><span id="src2"></span><span id="SRC2"></span>*src2*</span><span class="sxs-lookup"><span data-stu-id="31ff6-114"><span id="src2"></span><span id="SRC2"></span>*src2*</span></span><br/> | <span data-ttu-id="31ff6-115">\[nel \] numero da spostare.</span><span class="sxs-lookup"><span data-stu-id="31ff6-115">\[in\] The number to shift.</span></span><br/>                                         |



 

## <a name="remarks"></a><span data-ttu-id="31ff6-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="31ff6-116">Remarks</span></span>

``` syntax
 
        Given width, offset:
                if( width == 0 )
                {
                    dest = 0
                }
                else if( width + offset < 32 )
                {
                    shl dest, src2, 32-(width+offset)
                    ushr dest, dest, 32-width
                }
                else
                {
                    ushr dest, src2, offset
                }
```

<span data-ttu-id="31ff6-117">Usare questa istruzione per decomprimere interi senza segno o flag.</span><span class="sxs-lookup"><span data-stu-id="31ff6-117">Use this instruction to unpack unsigned integers or flags.</span></span>

<span data-ttu-id="31ff6-118">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="31ff6-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="31ff6-119">Vertice</span><span class="sxs-lookup"><span data-stu-id="31ff6-119">Vertex</span></span> | <span data-ttu-id="31ff6-120">Hull</span><span class="sxs-lookup"><span data-stu-id="31ff6-120">Hull</span></span> | <span data-ttu-id="31ff6-121">Dominio</span><span class="sxs-lookup"><span data-stu-id="31ff6-121">Domain</span></span> | <span data-ttu-id="31ff6-122">Geometria</span><span class="sxs-lookup"><span data-stu-id="31ff6-122">Geometry</span></span> | <span data-ttu-id="31ff6-123">Pixel</span><span class="sxs-lookup"><span data-stu-id="31ff6-123">Pixel</span></span> | <span data-ttu-id="31ff6-124">Calcolo</span><span class="sxs-lookup"><span data-stu-id="31ff6-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="31ff6-125">X</span><span class="sxs-lookup"><span data-stu-id="31ff6-125">X</span></span>      | <span data-ttu-id="31ff6-126">X</span><span class="sxs-lookup"><span data-stu-id="31ff6-126">X</span></span>    | <span data-ttu-id="31ff6-127">X</span><span class="sxs-lookup"><span data-stu-id="31ff6-127">X</span></span>      | <span data-ttu-id="31ff6-128">X</span><span class="sxs-lookup"><span data-stu-id="31ff6-128">X</span></span>        | <span data-ttu-id="31ff6-129">X</span><span class="sxs-lookup"><span data-stu-id="31ff6-129">X</span></span>     | <span data-ttu-id="31ff6-130">X</span><span class="sxs-lookup"><span data-stu-id="31ff6-130">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="31ff6-131">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="31ff6-131">Minimum Shader Model</span></span>

<span data-ttu-id="31ff6-132">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="31ff6-132">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="31ff6-133">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="31ff6-133">Shader Model</span></span>                                              | <span data-ttu-id="31ff6-134">Supportato</span><span class="sxs-lookup"><span data-stu-id="31ff6-134">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="31ff6-135">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="31ff6-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="31ff6-136">sì</span><span class="sxs-lookup"><span data-stu-id="31ff6-136">yes</span></span>       |
| [<span data-ttu-id="31ff6-137">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="31ff6-137">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="31ff6-138">no</span><span class="sxs-lookup"><span data-stu-id="31ff6-138">no</span></span>        |
| [<span data-ttu-id="31ff6-139">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="31ff6-139">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="31ff6-140">no</span><span class="sxs-lookup"><span data-stu-id="31ff6-140">no</span></span>        |
| [<span data-ttu-id="31ff6-141">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="31ff6-141">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="31ff6-142">no</span><span class="sxs-lookup"><span data-stu-id="31ff6-142">no</span></span>        |
| [<span data-ttu-id="31ff6-143">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="31ff6-143">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="31ff6-144">no</span><span class="sxs-lookup"><span data-stu-id="31ff6-144">no</span></span>        |
| [<span data-ttu-id="31ff6-145">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="31ff6-145">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="31ff6-146">no</span><span class="sxs-lookup"><span data-stu-id="31ff6-146">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="31ff6-147">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="31ff6-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="31ff6-148">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="31ff6-148">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





