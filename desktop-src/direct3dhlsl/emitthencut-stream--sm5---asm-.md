---
title: emitThenCut_stream (SM5-ASM)
description: Equivale a un comando Emit seguito da un comando Cut. | emitThenCut_stream (SM5-ASM)
ms.assetid: E9D84647-E29B-4E31-9E95-9F7A173293D4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ae3129f2a3fb50664a5dbf070c7a1dae9bf5d6e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981210"
---
# <a name="emitthencut_stream-sm5---asm"></a><span data-ttu-id="af803-104">\_flusso emitThenCut (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="af803-104">emitThenCut\_stream (sm5 - asm)</span></span>

<span data-ttu-id="af803-105">Equivale a un comando [Emit](emit--sm4---asm-.md) seguito da un comando [Cut](cut--sm4---asm-.md) .</span><span class="sxs-lookup"><span data-stu-id="af803-105">Equivalent to an [emit](emit--sm4---asm-.md) command followed by a [cut](cut--sm4---asm-.md) command.</span></span>



| <span data-ttu-id="af803-106">\_flusso EmitThenCut streamIndex</span><span class="sxs-lookup"><span data-stu-id="af803-106">emitThenCut\_stream streamIndex</span></span> |
|---------------------------------|



 



| <span data-ttu-id="af803-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="af803-107">Item</span></span>                                                                                                               | <span data-ttu-id="af803-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="af803-108">Description</span></span>                         |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| <span data-ttu-id="af803-109"><span id="streamIndex"></span><span id="streamindex"></span><span id="STREAMINDEX"></span>*streamIndex*</span><span class="sxs-lookup"><span data-stu-id="af803-109"><span id="streamIndex"></span><span id="streamindex"></span><span id="STREAMINDEX"></span>*streamIndex*</span></span><br/> | <span data-ttu-id="af803-110">\[nell' \] indice del flusso.</span><span class="sxs-lookup"><span data-stu-id="af803-110">\[in\] The stream index.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="af803-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="af803-111">Remarks</span></span>

<span data-ttu-id="af803-112">Questa operazione è utile in caso di output noto dell'ultimo vertice di una topologia.</span><span class="sxs-lookup"><span data-stu-id="af803-112">This operation is useful when knowingly outputting the last vertex in a topology.</span></span>

<span data-ttu-id="af803-113">Se i flussi non sono stati dichiarati, è necessario usare [emitThenCut](emitthencut--sm4---asm-.md) anziché **emitThenCut \_ Stream**.</span><span class="sxs-lookup"><span data-stu-id="af803-113">If streams have not been declared, then you must use [emitThenCut](emitthencut--sm4---asm-.md) instead of **emitThenCut\_stream**.</span></span>

<span data-ttu-id="af803-114">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="af803-114">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="af803-115">Vertice</span><span class="sxs-lookup"><span data-stu-id="af803-115">Vertex</span></span> | <span data-ttu-id="af803-116">Hull</span><span class="sxs-lookup"><span data-stu-id="af803-116">Hull</span></span> | <span data-ttu-id="af803-117">Dominio</span><span class="sxs-lookup"><span data-stu-id="af803-117">Domain</span></span> | <span data-ttu-id="af803-118">Geometria</span><span class="sxs-lookup"><span data-stu-id="af803-118">Geometry</span></span> | <span data-ttu-id="af803-119">Pixel</span><span class="sxs-lookup"><span data-stu-id="af803-119">Pixel</span></span> | <span data-ttu-id="af803-120">Calcolo</span><span class="sxs-lookup"><span data-stu-id="af803-120">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        | <span data-ttu-id="af803-121">X</span><span class="sxs-lookup"><span data-stu-id="af803-121">X</span></span>        |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="af803-122">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="af803-122">Minimum Shader Model</span></span>

<span data-ttu-id="af803-123">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="af803-123">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="af803-124">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="af803-124">Shader Model</span></span>                                              | <span data-ttu-id="af803-125">Supportato</span><span class="sxs-lookup"><span data-stu-id="af803-125">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="af803-126">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="af803-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="af803-127">sì</span><span class="sxs-lookup"><span data-stu-id="af803-127">yes</span></span>       |
| [<span data-ttu-id="af803-128">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="af803-128">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="af803-129">no</span><span class="sxs-lookup"><span data-stu-id="af803-129">no</span></span>        |
| [<span data-ttu-id="af803-130">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="af803-130">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="af803-131">no</span><span class="sxs-lookup"><span data-stu-id="af803-131">no</span></span>        |
| [<span data-ttu-id="af803-132">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="af803-132">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="af803-133">no</span><span class="sxs-lookup"><span data-stu-id="af803-133">no</span></span>        |
| [<span data-ttu-id="af803-134">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="af803-134">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="af803-135">no</span><span class="sxs-lookup"><span data-stu-id="af803-135">no</span></span>        |
| [<span data-ttu-id="af803-136">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="af803-136">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="af803-137">no</span><span class="sxs-lookup"><span data-stu-id="af803-137">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="af803-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="af803-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af803-139">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="af803-139">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





