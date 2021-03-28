---
title: bfrev (SM5-ASM)
description: Invertire un numero a 32 bit.
ms.assetid: 24F8209A-093E-4737-BF50-12F228024E9D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11bf0f07b6c66babf8e7f91108f86ba753420fc2
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993120"
---
# <a name="bfrev-sm5---asm"></a><span data-ttu-id="03266-103">bfrev (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="03266-103">bfrev (sm5 - asm)</span></span>

<span data-ttu-id="03266-104">Invertire un numero a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="03266-104">Reverse a 32-bit number.</span></span>



| <span data-ttu-id="03266-105">bfrev dest \[ . mask \] , src0 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="03266-105">bfrev dest\[.mask\], src0\[.swizzle\]</span></span> |
|---------------------------------------|



 



| <span data-ttu-id="03266-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="03266-106">Item</span></span>                                                            | <span data-ttu-id="03266-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="03266-107">Description</span></span>                                                  |
|-----------------------------------------------------------------|--------------------------------------------------------------|
| <span data-ttu-id="03266-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="03266-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="03266-109">\[nell' \] indirizzo per *src0* con BITS invertito.</span><span class="sxs-lookup"><span data-stu-id="03266-109">\[in\] The address for *src0* with bits reversed.</span></span><br/> |
| <span data-ttu-id="03266-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="03266-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="03266-111">\[nel \] numero a 32 bit da invertire.</span><span class="sxs-lookup"><span data-stu-id="03266-111">\[in\] The 32-bit number to reverse.</span></span><br/>              |



 

## <a name="remarks"></a><span data-ttu-id="03266-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="03266-112">Remarks</span></span>

<span data-ttu-id="03266-113">Se ad esempio si specifica 0x12345678., il risultato sarà 0x1e6a2c48.</span><span class="sxs-lookup"><span data-stu-id="03266-113">For example, given 0x12345678 the result would be 0x1e6a2c48.</span></span>

<span data-ttu-id="03266-114">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="03266-114">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="03266-115">Vertice</span><span class="sxs-lookup"><span data-stu-id="03266-115">Vertex</span></span> | <span data-ttu-id="03266-116">Hull</span><span class="sxs-lookup"><span data-stu-id="03266-116">Hull</span></span> | <span data-ttu-id="03266-117">Dominio</span><span class="sxs-lookup"><span data-stu-id="03266-117">Domain</span></span> | <span data-ttu-id="03266-118">Geometria</span><span class="sxs-lookup"><span data-stu-id="03266-118">Geometry</span></span> | <span data-ttu-id="03266-119">Pixel</span><span class="sxs-lookup"><span data-stu-id="03266-119">Pixel</span></span> | <span data-ttu-id="03266-120">Calcolo</span><span class="sxs-lookup"><span data-stu-id="03266-120">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="03266-121">X</span><span class="sxs-lookup"><span data-stu-id="03266-121">X</span></span>      | <span data-ttu-id="03266-122">X</span><span class="sxs-lookup"><span data-stu-id="03266-122">X</span></span>    | <span data-ttu-id="03266-123">X</span><span class="sxs-lookup"><span data-stu-id="03266-123">X</span></span>      | <span data-ttu-id="03266-124">X</span><span class="sxs-lookup"><span data-stu-id="03266-124">X</span></span>        | <span data-ttu-id="03266-125">X</span><span class="sxs-lookup"><span data-stu-id="03266-125">X</span></span>     | <span data-ttu-id="03266-126">X</span><span class="sxs-lookup"><span data-stu-id="03266-126">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="03266-127">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="03266-127">Minimum Shader Model</span></span>

<span data-ttu-id="03266-128">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="03266-128">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="03266-129">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="03266-129">Shader Model</span></span>                                              | <span data-ttu-id="03266-130">Supportato</span><span class="sxs-lookup"><span data-stu-id="03266-130">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="03266-131">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="03266-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="03266-132">sì</span><span class="sxs-lookup"><span data-stu-id="03266-132">yes</span></span>       |
| [<span data-ttu-id="03266-133">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="03266-133">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="03266-134">no</span><span class="sxs-lookup"><span data-stu-id="03266-134">no</span></span>        |
| [<span data-ttu-id="03266-135">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="03266-135">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="03266-136">no</span><span class="sxs-lookup"><span data-stu-id="03266-136">no</span></span>        |
| [<span data-ttu-id="03266-137">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="03266-137">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="03266-138">no</span><span class="sxs-lookup"><span data-stu-id="03266-138">no</span></span>        |
| [<span data-ttu-id="03266-139">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="03266-139">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="03266-140">no</span><span class="sxs-lookup"><span data-stu-id="03266-140">no</span></span>        |
| [<span data-ttu-id="03266-141">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="03266-141">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="03266-142">no</span><span class="sxs-lookup"><span data-stu-id="03266-142">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="03266-143">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="03266-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03266-144">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="03266-144">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





