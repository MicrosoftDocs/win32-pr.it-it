---
title: f32tof16 (SM5-ASM)
description: Conversione da float16 a float32 a livello di componente. | f32tof16 (SM5-ASM)
ms.assetid: 36BCCFC5-722A-45EB-8A66-7544833BBBA5
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b54a101f370f9c53d1d3f43f9e1cf6c4da82933d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104982031"
---
# <a name="f32tof16-sm5---asm"></a><span data-ttu-id="01d3a-104">f32tof16 (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="01d3a-104">f32tof16 (sm5 - asm)</span></span>

<span data-ttu-id="01d3a-105">Conversione da float16 a float32 a livello di componente.</span><span class="sxs-lookup"><span data-stu-id="01d3a-105">Component-wise float16 to float32 conversion.</span></span>



| <span data-ttu-id="01d3a-106">f32tof16 dest \[ . mask \] , \[ - \] src \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="01d3a-106">f32tof16 dest\[.mask\], \[-\]src\[.swizzle\]</span></span> |
|----------------------------------------------|



 



| <span data-ttu-id="01d3a-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="01d3a-107">Item</span></span>                                                            | <span data-ttu-id="01d3a-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="01d3a-108">Description</span></span>                                      |
|-----------------------------------------------------------------|--------------------------------------------------|
| <span data-ttu-id="01d3a-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="01d3a-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="01d3a-110">\[nell' \] indirizzo del risultato di float16.</span><span class="sxs-lookup"><span data-stu-id="01d3a-110">\[in\] The address of float16 result.</span></span><br/> |
| <span data-ttu-id="01d3a-111"><span id="src"></span><span id="SRC"></span>*src*</span><span class="sxs-lookup"><span data-stu-id="01d3a-111"><span id="src"></span><span id="SRC"></span>*src*</span></span><br/>    | <span data-ttu-id="01d3a-112">\[nel \] valore float32 da convertire.</span><span class="sxs-lookup"><span data-stu-id="01d3a-112">\[in\] The float32 value to convert.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="01d3a-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="01d3a-113">Remarks</span></span>

<span data-ttu-id="01d3a-114">Questa istruzione esegue una conversione a livello di componente di un valore float32 in un risultato di valore float16 inserito in LSB 16 bit.</span><span class="sxs-lookup"><span data-stu-id="01d3a-114">This instruction performs a component-wise conversion of a float32 value to a float16 value result placed in LSB 16 bits.</span></span>

<span data-ttu-id="01d3a-115">Questa istruzione segue le regole D3D per la conversione a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="01d3a-115">This instruction follows D3D rules for floating point conversion.</span></span>

<span data-ttu-id="01d3a-116">Usare questa istruzione per la compressione dei dati basata su shader.</span><span class="sxs-lookup"><span data-stu-id="01d3a-116">Use this instruction for shader-driven data compression.</span></span>

<span data-ttu-id="01d3a-117">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="01d3a-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="01d3a-118">Vertice</span><span class="sxs-lookup"><span data-stu-id="01d3a-118">Vertex</span></span> | <span data-ttu-id="01d3a-119">Hull</span><span class="sxs-lookup"><span data-stu-id="01d3a-119">Hull</span></span> | <span data-ttu-id="01d3a-120">Dominio</span><span class="sxs-lookup"><span data-stu-id="01d3a-120">Domain</span></span> | <span data-ttu-id="01d3a-121">Geometria</span><span class="sxs-lookup"><span data-stu-id="01d3a-121">Geometry</span></span> | <span data-ttu-id="01d3a-122">Pixel</span><span class="sxs-lookup"><span data-stu-id="01d3a-122">Pixel</span></span> | <span data-ttu-id="01d3a-123">Calcolo</span><span class="sxs-lookup"><span data-stu-id="01d3a-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="01d3a-124">X</span><span class="sxs-lookup"><span data-stu-id="01d3a-124">X</span></span>      | <span data-ttu-id="01d3a-125">X</span><span class="sxs-lookup"><span data-stu-id="01d3a-125">X</span></span>    | <span data-ttu-id="01d3a-126">X</span><span class="sxs-lookup"><span data-stu-id="01d3a-126">X</span></span>      | <span data-ttu-id="01d3a-127">X</span><span class="sxs-lookup"><span data-stu-id="01d3a-127">X</span></span>        | <span data-ttu-id="01d3a-128">X</span><span class="sxs-lookup"><span data-stu-id="01d3a-128">X</span></span>     | <span data-ttu-id="01d3a-129">X</span><span class="sxs-lookup"><span data-stu-id="01d3a-129">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="01d3a-130">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="01d3a-130">Minimum Shader Model</span></span>

<span data-ttu-id="01d3a-131">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="01d3a-131">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="01d3a-132">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="01d3a-132">Shader Model</span></span>                                              | <span data-ttu-id="01d3a-133">Supportato</span><span class="sxs-lookup"><span data-stu-id="01d3a-133">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="01d3a-134">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="01d3a-134">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="01d3a-135">sì</span><span class="sxs-lookup"><span data-stu-id="01d3a-135">yes</span></span>       |
| [<span data-ttu-id="01d3a-136">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="01d3a-136">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="01d3a-137">no</span><span class="sxs-lookup"><span data-stu-id="01d3a-137">no</span></span>        |
| [<span data-ttu-id="01d3a-138">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="01d3a-138">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="01d3a-139">no</span><span class="sxs-lookup"><span data-stu-id="01d3a-139">no</span></span>        |
| [<span data-ttu-id="01d3a-140">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="01d3a-140">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="01d3a-141">no</span><span class="sxs-lookup"><span data-stu-id="01d3a-141">no</span></span>        |
| [<span data-ttu-id="01d3a-142">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="01d3a-142">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="01d3a-143">no</span><span class="sxs-lookup"><span data-stu-id="01d3a-143">no</span></span>        |
| [<span data-ttu-id="01d3a-144">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="01d3a-144">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="01d3a-145">no</span><span class="sxs-lookup"><span data-stu-id="01d3a-145">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="01d3a-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="01d3a-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01d3a-147">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="01d3a-147">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





