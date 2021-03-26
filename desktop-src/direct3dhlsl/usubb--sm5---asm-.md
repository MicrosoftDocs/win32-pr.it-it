---
title: usubb (SM5-ASM)
description: Sottrazione di interi senza segno con prestito.
ms.assetid: 6D42E3CA-5A37-4194-AB42-7A2337C5AB9D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 111ffd134a75b8cfe19f63597cd80655201359c4
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398202"
---
# <a name="usubb-sm5---asm"></a><span data-ttu-id="05a14-103">usubb (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="05a14-103">usubb (sm5 - asm)</span></span>

<span data-ttu-id="05a14-104">Sottrazione di interi senza segno con prestito.</span><span class="sxs-lookup"><span data-stu-id="05a14-104">Unsigned integer subtract with borrow.</span></span>



| <span data-ttu-id="05a14-105">usubb dest0 \[ . mask \] , DesT1 \[ . mask \] , src0 \[ . Swizzle \] , src1 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="05a14-105">usubb dest0\[.mask\], dest1\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------|



 



| <span data-ttu-id="05a14-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="05a14-106">Item</span></span>                                                               | <span data-ttu-id="05a14-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="05a14-107">Description</span></span>                                                                                       |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05a14-108"><span id="dest0"></span><span id="DEST0"></span>*dest0*</span><span class="sxs-lookup"><span data-stu-id="05a14-108"><span id="dest0"></span><span id="DEST0"></span>*dest0*</span></span><br/> | <span data-ttu-id="05a14-109">\[in \] contiene i risultati di LSAB dell'istruzione.</span><span class="sxs-lookup"><span data-stu-id="05a14-109">\[in\] Contains the LSAB results of the instruction.</span></span><br/>                                   |
| <span data-ttu-id="05a14-110"><span id="dest1"></span><span id="DEST1"></span>*dest1*</span><span class="sxs-lookup"><span data-stu-id="05a14-110"><span id="dest1"></span><span id="DEST1"></span>*dest1*</span></span><br/> | <span data-ttu-id="05a14-111">\[nel \] componente corrispondente di *dest0* che specifica se è stato generato un prestito.</span><span class="sxs-lookup"><span data-stu-id="05a14-111">\[in\] The corresponding component of *dest0* that specifies if a borrow was produced.</span></span><br/> |
| <span data-ttu-id="05a14-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="05a14-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>    | <span data-ttu-id="05a14-113">\[\]valore da cui sottrarre.</span><span class="sxs-lookup"><span data-stu-id="05a14-113">\[in\] The value from which to subtract.</span></span><br/>                                               |
| <span data-ttu-id="05a14-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="05a14-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/>    | <span data-ttu-id="05a14-115">\[\]valore da sottrarre da *src0*.</span><span class="sxs-lookup"><span data-stu-id="05a14-115">\[in\] The amount to subtract from *src0*.</span></span><br/>                                             |



 

## <a name="remarks"></a><span data-ttu-id="05a14-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="05a14-116">Remarks</span></span>

<span data-ttu-id="05a14-117">Questa istruzione esegue una sottrazione senza segno a livello di componente di operandi a 32 bit *src1* da *src0*, inserendo la parte LSB del risultato 32 bit in *dest0*.</span><span class="sxs-lookup"><span data-stu-id="05a14-117">This instruction performs a component-wise unsigned subtract of 32-bit operands *src1* from *src0*, placing the LSB part of the 32-bit result in *dest0*.</span></span>

<span data-ttu-id="05a14-118">Il componente corrispondente in *DesT1* viene scritto con 1 se viene prodotto un prestito, 0 in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="05a14-118">The corresponding component in *dest1* is written with 1 if a borrow is produced, 0 otherwise.</span></span>

<span data-ttu-id="05a14-119">*DesT1* può essere null se il prestito non è necessario.</span><span class="sxs-lookup"><span data-stu-id="05a14-119">*dest1* can be NULL if the borrow is not needed.</span></span>

<span data-ttu-id="05a14-120">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="05a14-120">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="05a14-121">Vertice</span><span class="sxs-lookup"><span data-stu-id="05a14-121">Vertex</span></span> | <span data-ttu-id="05a14-122">Hull</span><span class="sxs-lookup"><span data-stu-id="05a14-122">Hull</span></span> | <span data-ttu-id="05a14-123">Dominio</span><span class="sxs-lookup"><span data-stu-id="05a14-123">Domain</span></span> | <span data-ttu-id="05a14-124">Geometria</span><span class="sxs-lookup"><span data-stu-id="05a14-124">Geometry</span></span> | <span data-ttu-id="05a14-125">Pixel</span><span class="sxs-lookup"><span data-stu-id="05a14-125">Pixel</span></span> | <span data-ttu-id="05a14-126">Calcolo</span><span class="sxs-lookup"><span data-stu-id="05a14-126">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="05a14-127">X</span><span class="sxs-lookup"><span data-stu-id="05a14-127">X</span></span>      | <span data-ttu-id="05a14-128">X</span><span class="sxs-lookup"><span data-stu-id="05a14-128">X</span></span>    | <span data-ttu-id="05a14-129">X</span><span class="sxs-lookup"><span data-stu-id="05a14-129">X</span></span>      | <span data-ttu-id="05a14-130">X</span><span class="sxs-lookup"><span data-stu-id="05a14-130">X</span></span>        | <span data-ttu-id="05a14-131">X</span><span class="sxs-lookup"><span data-stu-id="05a14-131">X</span></span>     | <span data-ttu-id="05a14-132">X</span><span class="sxs-lookup"><span data-stu-id="05a14-132">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="05a14-133">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="05a14-133">Minimum Shader Model</span></span>

<span data-ttu-id="05a14-134">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="05a14-134">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="05a14-135">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="05a14-135">Shader Model</span></span>                                              | <span data-ttu-id="05a14-136">Supportato</span><span class="sxs-lookup"><span data-stu-id="05a14-136">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="05a14-137">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="05a14-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="05a14-138">sì</span><span class="sxs-lookup"><span data-stu-id="05a14-138">yes</span></span>       |
| [<span data-ttu-id="05a14-139">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="05a14-139">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="05a14-140">no</span><span class="sxs-lookup"><span data-stu-id="05a14-140">no</span></span>        |
| [<span data-ttu-id="05a14-141">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="05a14-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="05a14-142">no</span><span class="sxs-lookup"><span data-stu-id="05a14-142">no</span></span>        |
| [<span data-ttu-id="05a14-143">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="05a14-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="05a14-144">no</span><span class="sxs-lookup"><span data-stu-id="05a14-144">no</span></span>        |
| [<span data-ttu-id="05a14-145">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="05a14-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="05a14-146">no</span><span class="sxs-lookup"><span data-stu-id="05a14-146">no</span></span>        |
| [<span data-ttu-id="05a14-147">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="05a14-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="05a14-148">no</span><span class="sxs-lookup"><span data-stu-id="05a14-148">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="05a14-149">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="05a14-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="05a14-150">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="05a14-150">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





