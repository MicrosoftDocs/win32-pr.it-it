---
title: uaddc (SM5-ASM)
description: Intero senza segno aggiungere con Carry.
ms.assetid: 1007253C-F920-4003-B266-D124A255F731
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f57f75be617e32c15212207110851520a7a281e2
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104516483"
---
# <a name="uaddc-sm5---asm"></a><span data-ttu-id="a849b-103">uaddc (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="a849b-103">uaddc (sm5 - asm)</span></span>

<span data-ttu-id="a849b-104">Intero senza segno aggiungere con Carry.</span><span class="sxs-lookup"><span data-stu-id="a849b-104">Unsigned integer add with carry.</span></span>



| <span data-ttu-id="a849b-105">uaddc dest0 \[ . mask \] , DesT1 \[ . mask \] , src0 \[ . Swizzle \] , src1 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="a849b-105">uaddc dest0\[.mask\], dest1\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------|



 



| <span data-ttu-id="a849b-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="a849b-106">Item</span></span>                                                               | <span data-ttu-id="a849b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a849b-107">Description</span></span>                                            |
|--------------------------------------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="a849b-108"><span id="dest0"></span><span id="DEST0"></span>*dest0*</span><span class="sxs-lookup"><span data-stu-id="a849b-108"><span id="dest0"></span><span id="DEST0"></span>*dest0*</span></span><br/> | <span data-ttu-id="a849b-109">\[\]indirizzo del risultato.</span><span class="sxs-lookup"><span data-stu-id="a849b-109">\[in\] Address of the result.</span></span><br/>               |
| <span data-ttu-id="a849b-110"><span id="dest1"></span><span id="DEST1"></span>*dest1*</span><span class="sxs-lookup"><span data-stu-id="a849b-110"><span id="dest1"></span><span id="DEST1"></span>*dest1*</span></span><br/> | <span data-ttu-id="a849b-111">\[in \] 1 se viene prodotto Carry.</span><span class="sxs-lookup"><span data-stu-id="a849b-111">\[in\] 1 if carry is produced.</span></span> <span data-ttu-id="a849b-112">In caso contrario, 0</span><span class="sxs-lookup"><span data-stu-id="a849b-112">Otherwise 0.</span></span><br/> |
| <span data-ttu-id="a849b-113"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="a849b-113"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>    | <span data-ttu-id="a849b-114">\[nell' \] operando a 32 bit da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="a849b-114">\[in\] 32-bit operand to be added.</span></span><br/>          |
| <span data-ttu-id="a849b-115"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="a849b-115"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/>    | <span data-ttu-id="a849b-116">\[nell' \] operando a 32 bit da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="a849b-116">\[in\] 32-bit operand to be added.</span></span><br/>          |



 

## <a name="remarks"></a><span data-ttu-id="a849b-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="a849b-117">Remarks</span></span>

<span data-ttu-id="a849b-118">*DesT1* può essere null se il trasporto non è necessario.</span><span class="sxs-lookup"><span data-stu-id="a849b-118">*dest1* can be NULL if the carry is not needed.</span></span>

<span data-ttu-id="a849b-119">Usare questa istruzione per operazioni aritmetiche con precisione elevata.</span><span class="sxs-lookup"><span data-stu-id="a849b-119">Use this instruction for high precision arithmetic.</span></span>

<span data-ttu-id="a849b-120">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="a849b-120">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="a849b-121">Vertice</span><span class="sxs-lookup"><span data-stu-id="a849b-121">Vertex</span></span> | <span data-ttu-id="a849b-122">Hull</span><span class="sxs-lookup"><span data-stu-id="a849b-122">Hull</span></span> | <span data-ttu-id="a849b-123">Dominio</span><span class="sxs-lookup"><span data-stu-id="a849b-123">Domain</span></span> | <span data-ttu-id="a849b-124">Geometria</span><span class="sxs-lookup"><span data-stu-id="a849b-124">Geometry</span></span> | <span data-ttu-id="a849b-125">Pixel</span><span class="sxs-lookup"><span data-stu-id="a849b-125">Pixel</span></span> | <span data-ttu-id="a849b-126">Calcolo</span><span class="sxs-lookup"><span data-stu-id="a849b-126">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="a849b-127">X</span><span class="sxs-lookup"><span data-stu-id="a849b-127">X</span></span>      | <span data-ttu-id="a849b-128">X</span><span class="sxs-lookup"><span data-stu-id="a849b-128">X</span></span>    | <span data-ttu-id="a849b-129">X</span><span class="sxs-lookup"><span data-stu-id="a849b-129">X</span></span>      | <span data-ttu-id="a849b-130">X</span><span class="sxs-lookup"><span data-stu-id="a849b-130">X</span></span>        | <span data-ttu-id="a849b-131">X</span><span class="sxs-lookup"><span data-stu-id="a849b-131">X</span></span>     | <span data-ttu-id="a849b-132">X</span><span class="sxs-lookup"><span data-stu-id="a849b-132">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="a849b-133">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="a849b-133">Minimum Shader Model</span></span>

<span data-ttu-id="a849b-134">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="a849b-134">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="a849b-135">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="a849b-135">Shader Model</span></span>                                              | <span data-ttu-id="a849b-136">Supportato</span><span class="sxs-lookup"><span data-stu-id="a849b-136">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="a849b-137">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="a849b-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="a849b-138">sì</span><span class="sxs-lookup"><span data-stu-id="a849b-138">yes</span></span>       |
| [<span data-ttu-id="a849b-139">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="a849b-139">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="a849b-140">no</span><span class="sxs-lookup"><span data-stu-id="a849b-140">no</span></span>        |
| [<span data-ttu-id="a849b-141">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="a849b-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="a849b-142">no</span><span class="sxs-lookup"><span data-stu-id="a849b-142">no</span></span>        |
| [<span data-ttu-id="a849b-143">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a849b-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="a849b-144">no</span><span class="sxs-lookup"><span data-stu-id="a849b-144">no</span></span>        |
| [<span data-ttu-id="a849b-145">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a849b-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="a849b-146">no</span><span class="sxs-lookup"><span data-stu-id="a849b-146">no</span></span>        |
| [<span data-ttu-id="a849b-147">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a849b-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="a849b-148">no</span><span class="sxs-lookup"><span data-stu-id="a849b-148">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="a849b-149">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a849b-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a849b-150">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a849b-150">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





