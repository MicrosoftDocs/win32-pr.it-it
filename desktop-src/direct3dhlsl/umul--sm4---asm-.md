---
title: umul (SM4-ASM)
description: Integer senza segno moltiplicato.
ms.assetid: C84AF349-32E6-40C4-9973-BCFA73EFBF0B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 581696ef5aa7d027c30b4ae866d06401275ef4bc
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398238"
---
# <a name="umul-sm4---asm"></a><span data-ttu-id="9f2d3-103">umul (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="9f2d3-103">umul (sm4 - asm)</span></span>

<span data-ttu-id="9f2d3-104">Integer senza segno moltiplicato.</span><span class="sxs-lookup"><span data-stu-id="9f2d3-104">Unsigned integer multiply.</span></span>



| <span data-ttu-id="9f2d3-105">umul destHI \[ . mask \] , destLO \[ . mask \] , src0 \[ . Swizzle \] , src1 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="9f2d3-105">umul destHI\[.mask\], destLO\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|---------------------------------------------------------------------------|



 



| <span data-ttu-id="9f2d3-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="9f2d3-106">Item</span></span>                                                                                           | <span data-ttu-id="9f2d3-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9f2d3-107">Description</span></span>                                                      |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="9f2d3-108"><span id="destHI"></span><span id="desthi"></span><span id="DESTHI"></span>*destHI*</span><span class="sxs-lookup"><span data-stu-id="9f2d3-108"><span id="destHI"></span><span id="desthi"></span><span id="DESTHI"></span>*destHI*</span></span><br/> | <span data-ttu-id="9f2d3-109">\[nei \] bit 32 alti del risultato, per componente.</span><span class="sxs-lookup"><span data-stu-id="9f2d3-109">\[in\] The high 32 bits of the result, per component.</span></span><br/> |
| <span data-ttu-id="9f2d3-110"><span id="destLO"></span><span id="destlo"></span><span id="DESTLO"></span>*destLO*</span><span class="sxs-lookup"><span data-stu-id="9f2d3-110"><span id="destLO"></span><span id="destlo"></span><span id="DESTLO"></span>*destLO*</span></span><br/> | <span data-ttu-id="9f2d3-111">\[nei \] 32 bit bassi del risultato, per componente.</span><span class="sxs-lookup"><span data-stu-id="9f2d3-111">\[in\] The low 32 bits of the result, per component.</span></span><br/>  |
| <span data-ttu-id="9f2d3-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="9f2d3-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                | <span data-ttu-id="9f2d3-113">\[nei \] componenti in base ai quali moltiplicare *src1*.</span><span class="sxs-lookup"><span data-stu-id="9f2d3-113">\[in\] The components by which to multiply *src1*.</span></span><br/>    |
| <span data-ttu-id="9f2d3-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="9f2d3-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/>                                | <span data-ttu-id="9f2d3-115">\[nei \] componenti in base ai quali moltiplicare *src0*.</span><span class="sxs-lookup"><span data-stu-id="9f2d3-115">\[in\] The components by which to multiply *src0*.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="9f2d3-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="9f2d3-116">Remarks</span></span>

<span data-ttu-id="9f2d3-117">Questa istruzione esegue una moltiplicazione per componente degli operandi senza segno a 32 bit *src0* e *src1*, producendo il risultato corretto a 64 bit completo per ogni componente.</span><span class="sxs-lookup"><span data-stu-id="9f2d3-117">This instruction performs a component-wise multiply of unsigned 32-bit operands *src0* and *src1*, producing the correct full 64-bit result per component.</span></span> <span data-ttu-id="9f2d3-118">I 32 bit inferiori per ogni componente sono posizionati in *destLO*.</span><span class="sxs-lookup"><span data-stu-id="9f2d3-118">The low 32 bits per component are placed in *destLO*.</span></span> <span data-ttu-id="9f2d3-119">I 32 bit alti per componente sono posizionati in *destHI*.</span><span class="sxs-lookup"><span data-stu-id="9f2d3-119">The high 32 bits per component are placed in *destHI*.</span></span>

<span data-ttu-id="9f2d3-120">È possibile specificare *destHI* o *destLO* come null invece di specificare un registro se non sono necessari i bit 32 massimi o bassi del risultato 64 bit.</span><span class="sxs-lookup"><span data-stu-id="9f2d3-120">You can specify either *destHI* or *destLO* as NULL instead of specifying a register if the high or low 32 bits of the 64-bit result are not needed.</span></span>

<span data-ttu-id="9f2d3-121">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="9f2d3-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="9f2d3-122">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="9f2d3-122">Vertex Shader</span></span> | <span data-ttu-id="9f2d3-123">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="9f2d3-123">Geometry Shader</span></span> | <span data-ttu-id="9f2d3-124">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="9f2d3-124">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="9f2d3-125">x</span><span class="sxs-lookup"><span data-stu-id="9f2d3-125">x</span></span>             | <span data-ttu-id="9f2d3-126">x</span><span class="sxs-lookup"><span data-stu-id="9f2d3-126">x</span></span>               | <span data-ttu-id="9f2d3-127">x</span><span class="sxs-lookup"><span data-stu-id="9f2d3-127">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="9f2d3-128">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="9f2d3-128">Minimum Shader Model</span></span>

<span data-ttu-id="9f2d3-129">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="9f2d3-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="9f2d3-130">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="9f2d3-130">Shader Model</span></span>                                              | <span data-ttu-id="9f2d3-131">Supportato</span><span class="sxs-lookup"><span data-stu-id="9f2d3-131">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="9f2d3-132">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="9f2d3-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="9f2d3-133">sì</span><span class="sxs-lookup"><span data-stu-id="9f2d3-133">yes</span></span>       |
| [<span data-ttu-id="9f2d3-134">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="9f2d3-134">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="9f2d3-135">sì</span><span class="sxs-lookup"><span data-stu-id="9f2d3-135">yes</span></span>       |
| [<span data-ttu-id="9f2d3-136">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="9f2d3-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="9f2d3-137">sì</span><span class="sxs-lookup"><span data-stu-id="9f2d3-137">yes</span></span>       |
| [<span data-ttu-id="9f2d3-138">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9f2d3-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="9f2d3-139">no</span><span class="sxs-lookup"><span data-stu-id="9f2d3-139">no</span></span>        |
| [<span data-ttu-id="9f2d3-140">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9f2d3-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="9f2d3-141">no</span><span class="sxs-lookup"><span data-stu-id="9f2d3-141">no</span></span>        |
| [<span data-ttu-id="9f2d3-142">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9f2d3-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="9f2d3-143">no</span><span class="sxs-lookup"><span data-stu-id="9f2d3-143">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="9f2d3-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9f2d3-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9f2d3-145">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9f2d3-145">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





