---
title: countbits (SM5-ASM)
description: Conta il numero di bit impostati in un numero.
ms.assetid: ED75487F-46FF-45F5-BEAA-7A32BEFB0571
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55d46fe9c750790d65630a743dd9ddc347fea50e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "103857774"
---
# <a name="countbits-sm5---asm"></a><span data-ttu-id="a70e6-103">countbits (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="a70e6-103">countbits (sm5 - asm)</span></span>

<span data-ttu-id="a70e6-104">Conta il numero di bit impostati in un numero.</span><span class="sxs-lookup"><span data-stu-id="a70e6-104">Counts the number of bits set in a number.</span></span>



| <span data-ttu-id="a70e6-105">countbits dest \[ . mask \] , src0 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="a70e6-105">countbits dest\[.mask\], src0\[.swizzle\]</span></span> |
|-------------------------------------------|



 



| <span data-ttu-id="a70e6-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="a70e6-106">Item</span></span>                                                            | <span data-ttu-id="a70e6-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a70e6-107">Description</span></span>                                   |
|-----------------------------------------------------------------|-----------------------------------------------|
| <span data-ttu-id="a70e6-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="a70e6-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="a70e6-109">\[nell' \] indirizzo dei risultati.</span><span class="sxs-lookup"><span data-stu-id="a70e6-109">\[in\] The address of the results.</span></span><br/> |
| <span data-ttu-id="a70e6-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="a70e6-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="a70e6-111">\[nel \] numero di input a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="a70e6-111">\[in\] The input 32-bit number.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="a70e6-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="a70e6-112">Remarks</span></span>

<span data-ttu-id="a70e6-113">Questa istruzione può essere utilizzata per calcolare la percentuale di code coverage input di shader.</span><span class="sxs-lookup"><span data-stu-id="a70e6-113">This instruction can be used to compute shader input coverage percentage.</span></span>

<span data-ttu-id="a70e6-114">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="a70e6-114">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="a70e6-115">Vertice</span><span class="sxs-lookup"><span data-stu-id="a70e6-115">Vertex</span></span> | <span data-ttu-id="a70e6-116">Hull</span><span class="sxs-lookup"><span data-stu-id="a70e6-116">Hull</span></span> | <span data-ttu-id="a70e6-117">Dominio</span><span class="sxs-lookup"><span data-stu-id="a70e6-117">Domain</span></span> | <span data-ttu-id="a70e6-118">Geometria</span><span class="sxs-lookup"><span data-stu-id="a70e6-118">Geometry</span></span> | <span data-ttu-id="a70e6-119">Pixel</span><span class="sxs-lookup"><span data-stu-id="a70e6-119">Pixel</span></span> | <span data-ttu-id="a70e6-120">Calcolo</span><span class="sxs-lookup"><span data-stu-id="a70e6-120">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="a70e6-121">X</span><span class="sxs-lookup"><span data-stu-id="a70e6-121">X</span></span>      | <span data-ttu-id="a70e6-122">X</span><span class="sxs-lookup"><span data-stu-id="a70e6-122">X</span></span>    | <span data-ttu-id="a70e6-123">X</span><span class="sxs-lookup"><span data-stu-id="a70e6-123">X</span></span>      | <span data-ttu-id="a70e6-124">X</span><span class="sxs-lookup"><span data-stu-id="a70e6-124">X</span></span>        | <span data-ttu-id="a70e6-125">X</span><span class="sxs-lookup"><span data-stu-id="a70e6-125">X</span></span>     | <span data-ttu-id="a70e6-126">X</span><span class="sxs-lookup"><span data-stu-id="a70e6-126">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="a70e6-127">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="a70e6-127">Minimum Shader Model</span></span>

<span data-ttu-id="a70e6-128">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="a70e6-128">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="a70e6-129">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="a70e6-129">Shader Model</span></span>                                              | <span data-ttu-id="a70e6-130">Supportato</span><span class="sxs-lookup"><span data-stu-id="a70e6-130">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="a70e6-131">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="a70e6-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="a70e6-132">sì</span><span class="sxs-lookup"><span data-stu-id="a70e6-132">yes</span></span>       |
| [<span data-ttu-id="a70e6-133">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="a70e6-133">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="a70e6-134">no</span><span class="sxs-lookup"><span data-stu-id="a70e6-134">no</span></span>        |
| [<span data-ttu-id="a70e6-135">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="a70e6-135">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="a70e6-136">no</span><span class="sxs-lookup"><span data-stu-id="a70e6-136">no</span></span>        |
| [<span data-ttu-id="a70e6-137">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a70e6-137">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="a70e6-138">no</span><span class="sxs-lookup"><span data-stu-id="a70e6-138">no</span></span>        |
| [<span data-ttu-id="a70e6-139">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a70e6-139">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="a70e6-140">no</span><span class="sxs-lookup"><span data-stu-id="a70e6-140">no</span></span>        |
| [<span data-ttu-id="a70e6-141">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a70e6-141">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="a70e6-142">no</span><span class="sxs-lookup"><span data-stu-id="a70e6-142">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="a70e6-143">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a70e6-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a70e6-144">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a70e6-144">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





