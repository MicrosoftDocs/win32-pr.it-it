---
title: dcl_thread_group (SM5-ASM)
description: Dichiarare le dimensioni del gruppo di thread.
ms.assetid: CB8192C4-100D-49B6-94E7-6CD3AEC28149
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8141c80e82f1dfd1ae5a4d360d04fac32ba5221
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104046112"
---
# <a name="dcl_thread_group-sm5---asm"></a><span data-ttu-id="0e89d-103">\_ \_ gruppo di thread DCL (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="0e89d-103">dcl\_thread\_group (sm5 - asm)</span></span>

<span data-ttu-id="0e89d-104">Dichiarare le dimensioni del gruppo di thread.</span><span class="sxs-lookup"><span data-stu-id="0e89d-104">Declare thread group size.</span></span>



| <span data-ttu-id="0e89d-105">\_ \_ gruppo di thread DCL x, y, z</span><span class="sxs-lookup"><span data-stu-id="0e89d-105">dcl\_thread\_group x, y, z</span></span> |
|----------------------------|



 



| <span data-ttu-id="0e89d-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="0e89d-106">Item</span></span>                                                   | <span data-ttu-id="0e89d-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0e89d-107">Description</span></span>                                                        |
|--------------------------------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="0e89d-108"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="0e89d-108"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="0e89d-109">\[in \] un intero usigned a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="0e89d-109">\[in\] An usigned 32-bit integer.</span></span> <span data-ttu-id="0e89d-110">1 <= x <= 1024</span><span class="sxs-lookup"><span data-stu-id="0e89d-110">1 <= x <= 1024</span></span> <br/> |
| <span data-ttu-id="0e89d-111"><span id="y"></span><span id="Y"></span>*y*</span><span class="sxs-lookup"><span data-stu-id="0e89d-111"><span id="y"></span><span id="Y"></span>*y*</span></span><br/> | <span data-ttu-id="0e89d-112">\[in \] un intero usigned a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="0e89d-112">\[in\] An usigned 32-bit integer.</span></span> <span data-ttu-id="0e89d-113">1 <= y <= 1024</span><span class="sxs-lookup"><span data-stu-id="0e89d-113">1 <= y <= 1024</span></span><br/>  |
| <span data-ttu-id="0e89d-114"><span id="z"></span><span id="Z"></span>*z*</span><span class="sxs-lookup"><span data-stu-id="0e89d-114"><span id="z"></span><span id="Z"></span>*z*</span></span><br/> | <span data-ttu-id="0e89d-115">\[in \] un intero usigned a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="0e89d-115">\[in\] An usigned 32-bit integer.</span></span> <span data-ttu-id="0e89d-116">1 <= z <= 64</span><span class="sxs-lookup"><span data-stu-id="0e89d-116">1 <= z <= 64</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="0e89d-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="0e89d-117">Remarks</span></span>

<span data-ttu-id="0e89d-118">x \* y \* z <= 1024</span><span class="sxs-lookup"><span data-stu-id="0e89d-118">x\*y\*z <= 1024</span></span>

<span data-ttu-id="0e89d-119">Questa dichiarazione del gruppo di thread deve essere visualizzata una sola volta in un compute shader.</span><span class="sxs-lookup"><span data-stu-id="0e89d-119">This thread group declaration must appear once in a compute shader.</span></span>

<span data-ttu-id="0e89d-120">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="0e89d-120">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="0e89d-121">Vertice</span><span class="sxs-lookup"><span data-stu-id="0e89d-121">Vertex</span></span> | <span data-ttu-id="0e89d-122">Hull</span><span class="sxs-lookup"><span data-stu-id="0e89d-122">Hull</span></span> | <span data-ttu-id="0e89d-123">Dominio</span><span class="sxs-lookup"><span data-stu-id="0e89d-123">Domain</span></span> | <span data-ttu-id="0e89d-124">Geometria</span><span class="sxs-lookup"><span data-stu-id="0e89d-124">Geometry</span></span> | <span data-ttu-id="0e89d-125">Pixel</span><span class="sxs-lookup"><span data-stu-id="0e89d-125">Pixel</span></span> | <span data-ttu-id="0e89d-126">Calcolo</span><span class="sxs-lookup"><span data-stu-id="0e89d-126">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="0e89d-127">X</span><span class="sxs-lookup"><span data-stu-id="0e89d-127">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="0e89d-128">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="0e89d-128">Minimum Shader Model</span></span>

<span data-ttu-id="0e89d-129">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="0e89d-129">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="0e89d-130">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="0e89d-130">Shader Model</span></span>                                              | <span data-ttu-id="0e89d-131">Supportato</span><span class="sxs-lookup"><span data-stu-id="0e89d-131">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="0e89d-132">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="0e89d-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="0e89d-133">sì</span><span class="sxs-lookup"><span data-stu-id="0e89d-133">yes</span></span>       |
| [<span data-ttu-id="0e89d-134">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="0e89d-134">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="0e89d-135">no</span><span class="sxs-lookup"><span data-stu-id="0e89d-135">no</span></span>        |
| [<span data-ttu-id="0e89d-136">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="0e89d-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="0e89d-137">no</span><span class="sxs-lookup"><span data-stu-id="0e89d-137">no</span></span>        |
| [<span data-ttu-id="0e89d-138">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0e89d-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="0e89d-139">no</span><span class="sxs-lookup"><span data-stu-id="0e89d-139">no</span></span>        |
| [<span data-ttu-id="0e89d-140">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0e89d-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="0e89d-141">no</span><span class="sxs-lookup"><span data-stu-id="0e89d-141">no</span></span>        |
| [<span data-ttu-id="0e89d-142">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0e89d-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="0e89d-143">no</span><span class="sxs-lookup"><span data-stu-id="0e89d-143">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="0e89d-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0e89d-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e89d-145">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0e89d-145">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





