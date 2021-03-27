---
title: XOR (SM4-ASM)
description: XOR bit per bit.
ms.assetid: 6B949653-6DDA-402B-8ABE-B93858B68470
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7a998bd1e95793f463d7f234b464a542bed4fc0
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398198"
---
# <a name="xor-sm4---asm"></a><span data-ttu-id="c577c-103">XOR (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="c577c-103">xor (sm4 - asm)</span></span>

<span data-ttu-id="c577c-104">XOR bit per bit.</span><span class="sxs-lookup"><span data-stu-id="c577c-104">Bitwise xor.</span></span>



| <span data-ttu-id="c577c-105">XOR dest \[ . mask \] , src0 \[ . Swizzle \] , src1 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="c577c-105">xor dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|-------------------------------------------------------|



 



| <span data-ttu-id="c577c-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="c577c-106">Item</span></span>                                                            | <span data-ttu-id="c577c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c577c-107">Description</span></span>                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c577c-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="c577c-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="c577c-109">\[nel \] risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="c577c-109">\[in\] The result of the operation.</span></span><br/>       |
| <span data-ttu-id="c577c-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="c577c-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="c577c-111">\[nei \] componenti per XOR con *src1*.</span><span class="sxs-lookup"><span data-stu-id="c577c-111">\[in\] The components to XOR with *src1*.</span></span><br/> |
| <span data-ttu-id="c577c-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="c577c-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="c577c-113">\[nei \] componenti per XOR con *src0*.</span><span class="sxs-lookup"><span data-stu-id="c577c-113">\[in\] The components to XOR with *src0*.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c577c-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="c577c-114">Remarks</span></span>

<span data-ttu-id="c577c-115">Questa istruzione esegue un XOR logico a livello di componente di ogni coppia di valori a 32 bit da *src0* e *src1*.</span><span class="sxs-lookup"><span data-stu-id="c577c-115">This instruction performs a component-wise logical XOR of each pair of 32-bit values from *src0* and *src1*.</span></span> <span data-ttu-id="c577c-116">i risultati a 32 bit sono posizionati in *dest*.</span><span class="sxs-lookup"><span data-stu-id="c577c-116">32-bit results are placed in *dest*.</span></span>

<span data-ttu-id="c577c-117">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="c577c-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="c577c-118">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="c577c-118">Vertex Shader</span></span> | <span data-ttu-id="c577c-119">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="c577c-119">Geometry Shader</span></span> | <span data-ttu-id="c577c-120">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="c577c-120">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="c577c-121">x</span><span class="sxs-lookup"><span data-stu-id="c577c-121">x</span></span>             | <span data-ttu-id="c577c-122">x</span><span class="sxs-lookup"><span data-stu-id="c577c-122">x</span></span>               | <span data-ttu-id="c577c-123">x</span><span class="sxs-lookup"><span data-stu-id="c577c-123">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="c577c-124">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="c577c-124">Minimum Shader Model</span></span>

<span data-ttu-id="c577c-125">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="c577c-125">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="c577c-126">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="c577c-126">Shader Model</span></span>                                              | <span data-ttu-id="c577c-127">Supportato</span><span class="sxs-lookup"><span data-stu-id="c577c-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="c577c-128">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="c577c-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="c577c-129">sì</span><span class="sxs-lookup"><span data-stu-id="c577c-129">yes</span></span>       |
| [<span data-ttu-id="c577c-130">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="c577c-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="c577c-131">sì</span><span class="sxs-lookup"><span data-stu-id="c577c-131">yes</span></span>       |
| [<span data-ttu-id="c577c-132">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="c577c-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="c577c-133">sì</span><span class="sxs-lookup"><span data-stu-id="c577c-133">yes</span></span>       |
| [<span data-ttu-id="c577c-134">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c577c-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="c577c-135">no</span><span class="sxs-lookup"><span data-stu-id="c577c-135">no</span></span>        |
| [<span data-ttu-id="c577c-136">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c577c-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="c577c-137">no</span><span class="sxs-lookup"><span data-stu-id="c577c-137">no</span></span>        |
| [<span data-ttu-id="c577c-138">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c577c-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="c577c-139">no</span><span class="sxs-lookup"><span data-stu-id="c577c-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="c577c-140">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c577c-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c577c-141">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c577c-141">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





