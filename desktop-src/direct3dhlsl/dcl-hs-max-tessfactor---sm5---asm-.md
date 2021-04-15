---
title: dcl_hs_max_tessfactor (SM5-ASM)
description: Dichiarare il maxTessFactor per la patch.
ms.assetid: 7EF0FD81-69FE-49F6-95DF-0C452A90A713
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69bd20fc8f4a3687988e8b100975f74016a45ae6
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993245"
---
# <a name="dcl_hs_max_tessfactor-sm5---asm"></a><span data-ttu-id="e6d73-103">\_ \_ Max \_ tessfactor di DCL HS (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="e6d73-103">dcl\_hs\_max\_tessfactor (sm5 - asm)</span></span>

<span data-ttu-id="e6d73-104">Dichiarare il maxTessFactor per la patch.</span><span class="sxs-lookup"><span data-stu-id="e6d73-104">Declare the maxTessFactor for the patch.</span></span>



| <span data-ttu-id="e6d73-105">\_tessfactor max di DCL HS \_ \_ n</span><span class="sxs-lookup"><span data-stu-id="e6d73-105">dcl\_hs\_max\_tessfactor n</span></span> |
|----------------------------|



 



| <span data-ttu-id="e6d73-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="e6d73-106">Item</span></span>                                                   | <span data-ttu-id="e6d73-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e6d73-107">Description</span></span>                          |
|--------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="e6d73-108"><span id="n"></span><span id="N"></span>*n*</span><span class="sxs-lookup"><span data-stu-id="e6d73-108"><span id="n"></span><span id="N"></span>*n*</span></span><br/> | <span data-ttu-id="e6d73-109">\[in \] maxTessFactor.</span><span class="sxs-lookup"><span data-stu-id="e6d73-109">\[in\] The maxTessFactor.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e6d73-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="e6d73-110">Remarks</span></span>

<span data-ttu-id="e6d73-111">MaxTessFactor è un valore float32 compreso nell'intervallo {1,0... 64,0}.</span><span class="sxs-lookup"><span data-stu-id="e6d73-111">The maxTessFactor is a float32 value in the range {1.0 ... 64.0}.</span></span>

<span data-ttu-id="e6d73-112">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="e6d73-112">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="e6d73-113">Vertice</span><span class="sxs-lookup"><span data-stu-id="e6d73-113">Vertex</span></span> | <span data-ttu-id="e6d73-114">Hull</span><span class="sxs-lookup"><span data-stu-id="e6d73-114">Hull</span></span> | <span data-ttu-id="e6d73-115">Dominio</span><span class="sxs-lookup"><span data-stu-id="e6d73-115">Domain</span></span> | <span data-ttu-id="e6d73-116">Geometria</span><span class="sxs-lookup"><span data-stu-id="e6d73-116">Geometry</span></span> | <span data-ttu-id="e6d73-117">Pixel</span><span class="sxs-lookup"><span data-stu-id="e6d73-117">Pixel</span></span> | <span data-ttu-id="e6d73-118">Calcolo</span><span class="sxs-lookup"><span data-stu-id="e6d73-118">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="e6d73-119">X</span><span class="sxs-lookup"><span data-stu-id="e6d73-119">X</span></span>    |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="e6d73-120">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="e6d73-120">Minimum Shader Model</span></span>

<span data-ttu-id="e6d73-121">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="e6d73-121">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="e6d73-122">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="e6d73-122">Shader Model</span></span>                                              | <span data-ttu-id="e6d73-123">Supportato</span><span class="sxs-lookup"><span data-stu-id="e6d73-123">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="e6d73-124">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="e6d73-124">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="e6d73-125">sì</span><span class="sxs-lookup"><span data-stu-id="e6d73-125">yes</span></span>       |
| [<span data-ttu-id="e6d73-126">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="e6d73-126">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="e6d73-127">no</span><span class="sxs-lookup"><span data-stu-id="e6d73-127">no</span></span>        |
| [<span data-ttu-id="e6d73-128">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="e6d73-128">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="e6d73-129">no</span><span class="sxs-lookup"><span data-stu-id="e6d73-129">no</span></span>        |
| [<span data-ttu-id="e6d73-130">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e6d73-130">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="e6d73-131">no</span><span class="sxs-lookup"><span data-stu-id="e6d73-131">no</span></span>        |
| [<span data-ttu-id="e6d73-132">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e6d73-132">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="e6d73-133">no</span><span class="sxs-lookup"><span data-stu-id="e6d73-133">no</span></span>        |
| [<span data-ttu-id="e6d73-134">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e6d73-134">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="e6d73-135">no</span><span class="sxs-lookup"><span data-stu-id="e6d73-135">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="e6d73-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e6d73-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e6d73-137">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e6d73-137">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





