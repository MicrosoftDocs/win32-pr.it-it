---
title: f16tof32 (SM5-ASM)
description: Conversione da float16 a float32 a livello di componente. | f16tof32 (SM5-ASM)
ms.assetid: CFAA1350-DA7F-4105-A90A-72052C5E2FB3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d53af1f2eab1f50dfded820bf27b2cda8f23e6b4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981535"
---
# <a name="f16tof32-sm5---asm"></a><span data-ttu-id="7e1ac-104">f16tof32 (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="7e1ac-104">f16tof32 (sm5 - asm)</span></span>

<span data-ttu-id="7e1ac-105">Conversione da float16 a float32 a livello di componente.</span><span class="sxs-lookup"><span data-stu-id="7e1ac-105">Component-wise float16 to float32 conversion.</span></span>



| <span data-ttu-id="7e1ac-106">f16tof32 dest \[ . mask \] , \[ - \] src \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="7e1ac-106">f16tof32 dest\[.mask\], \[-\]src\[.swizzle\]</span></span> |
|----------------------------------------------|



 



| <span data-ttu-id="7e1ac-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="7e1ac-107">Item</span></span>                                                            | <span data-ttu-id="7e1ac-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7e1ac-108">Description</span></span>                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7e1ac-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="7e1ac-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="7e1ac-110">\[nell' \] indirizzo del risultato di float32.</span><span class="sxs-lookup"><span data-stu-id="7e1ac-110">\[in\] The address of the float32 result.</span></span><br/> |
| <span data-ttu-id="7e1ac-111"><span id="src"></span><span id="SRC"></span>*src*</span><span class="sxs-lookup"><span data-stu-id="7e1ac-111"><span id="src"></span><span id="SRC"></span>*src*</span></span><br/>    | <span data-ttu-id="7e1ac-112">\[nel \] valore float16 da convertire.</span><span class="sxs-lookup"><span data-stu-id="7e1ac-112">\[in\] The float16 value to convert.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="7e1ac-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="7e1ac-113">Remarks</span></span>

<span data-ttu-id="7e1ac-114">Questa operazione esegue una conversione componente per un valore float16 da bit LSB a un risultato float32.</span><span class="sxs-lookup"><span data-stu-id="7e1ac-114">This operation performs a component-wise conversion of a float16 value from LSB bits to a float32 result.</span></span>

<span data-ttu-id="7e1ac-115">Questa operazione segue le regole D3D per la conversione a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="7e1ac-115">This operation follows D3D rules for floating point conversion.</span></span>

<span data-ttu-id="7e1ac-116">Usare questa istruzione per la decompressione dei dati basata su shader.</span><span class="sxs-lookup"><span data-stu-id="7e1ac-116">Use this instruction for shader-driven data decompression.</span></span>

<span data-ttu-id="7e1ac-117">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="7e1ac-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="7e1ac-118">Vertice</span><span class="sxs-lookup"><span data-stu-id="7e1ac-118">Vertex</span></span> | <span data-ttu-id="7e1ac-119">Hull</span><span class="sxs-lookup"><span data-stu-id="7e1ac-119">Hull</span></span> | <span data-ttu-id="7e1ac-120">Dominio</span><span class="sxs-lookup"><span data-stu-id="7e1ac-120">Domain</span></span> | <span data-ttu-id="7e1ac-121">Geometria</span><span class="sxs-lookup"><span data-stu-id="7e1ac-121">Geometry</span></span> | <span data-ttu-id="7e1ac-122">Pixel</span><span class="sxs-lookup"><span data-stu-id="7e1ac-122">Pixel</span></span> | <span data-ttu-id="7e1ac-123">Calcolo</span><span class="sxs-lookup"><span data-stu-id="7e1ac-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="7e1ac-124">X</span><span class="sxs-lookup"><span data-stu-id="7e1ac-124">X</span></span>      | <span data-ttu-id="7e1ac-125">X</span><span class="sxs-lookup"><span data-stu-id="7e1ac-125">X</span></span>    | <span data-ttu-id="7e1ac-126">X</span><span class="sxs-lookup"><span data-stu-id="7e1ac-126">X</span></span>      | <span data-ttu-id="7e1ac-127">X</span><span class="sxs-lookup"><span data-stu-id="7e1ac-127">X</span></span>        | <span data-ttu-id="7e1ac-128">X</span><span class="sxs-lookup"><span data-stu-id="7e1ac-128">X</span></span>     | <span data-ttu-id="7e1ac-129">X</span><span class="sxs-lookup"><span data-stu-id="7e1ac-129">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="7e1ac-130">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="7e1ac-130">Minimum Shader Model</span></span>

<span data-ttu-id="7e1ac-131">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="7e1ac-131">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="7e1ac-132">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="7e1ac-132">Shader Model</span></span>                                              | <span data-ttu-id="7e1ac-133">Supportato</span><span class="sxs-lookup"><span data-stu-id="7e1ac-133">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="7e1ac-134">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="7e1ac-134">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="7e1ac-135">sì</span><span class="sxs-lookup"><span data-stu-id="7e1ac-135">yes</span></span>       |
| [<span data-ttu-id="7e1ac-136">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="7e1ac-136">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="7e1ac-137">no</span><span class="sxs-lookup"><span data-stu-id="7e1ac-137">no</span></span>        |
| [<span data-ttu-id="7e1ac-138">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="7e1ac-138">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="7e1ac-139">no</span><span class="sxs-lookup"><span data-stu-id="7e1ac-139">no</span></span>        |
| [<span data-ttu-id="7e1ac-140">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7e1ac-140">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="7e1ac-141">no</span><span class="sxs-lookup"><span data-stu-id="7e1ac-141">no</span></span>        |
| [<span data-ttu-id="7e1ac-142">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7e1ac-142">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="7e1ac-143">no</span><span class="sxs-lookup"><span data-stu-id="7e1ac-143">no</span></span>        |
| [<span data-ttu-id="7e1ac-144">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7e1ac-144">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="7e1ac-145">no</span><span class="sxs-lookup"><span data-stu-id="7e1ac-145">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="7e1ac-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7e1ac-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e1ac-147">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7e1ac-147">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





