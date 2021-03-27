---
title: dcl_hs_join_phase_instance_count (SM5-ASM)
description: Dichiarare il numero di istanze della fase di join in una fase di join Hull shader.
ms.assetid: 9951B849-0537-4D08-9ADE-8CF6FF51A193
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34c3acc7074170ab4561a54e67668698d58b7ac1
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398310"
---
# <a name="dcl_hs_join_phase_instance_count-sm5---asm"></a><span data-ttu-id="885ad-103">\_ \_ \_ conteggio istanze fase join DCL HS \_ \_ (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="885ad-103">dcl\_hs\_join\_phase\_instance\_count (sm5 - asm)</span></span>

<span data-ttu-id="885ad-104">Dichiarare il numero di istanze della fase di join in una fase di join Hull shader.</span><span class="sxs-lookup"><span data-stu-id="885ad-104">Declare the join phase instance count in a hull shader join phase.</span></span>



| <span data-ttu-id="885ad-105">\_ \_ numero di istanze della fase join di DCL HS \_ \_ \_ {1... max 32 bit uint}</span><span class="sxs-lookup"><span data-stu-id="885ad-105">dcl\_hs\_join\_phase\_instance\_count {1... max 32-bit UINT}</span></span> |
|--------------------------------------------------------------|



 



| <span data-ttu-id="885ad-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="885ad-106">Item</span></span>                                                   | <span data-ttu-id="885ad-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="885ad-107">Description</span></span>                           |
|--------------------------------------------------------|---------------------------------------|
| <span data-ttu-id="885ad-108"><span id="N"></span><span id="n"></span>*N*</span><span class="sxs-lookup"><span data-stu-id="885ad-108"><span id="N"></span><span id="n"></span>*N*</span></span><br/> | <span data-ttu-id="885ad-109">\[nel \] conteggio delle istanze.</span><span class="sxs-lookup"><span data-stu-id="885ad-109">\[in\] The instance count.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="885ad-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="885ad-110">Remarks</span></span>

<span data-ttu-id="885ad-111">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="885ad-111">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="885ad-112">Vertice</span><span class="sxs-lookup"><span data-stu-id="885ad-112">Vertex</span></span> | <span data-ttu-id="885ad-113">Hull</span><span class="sxs-lookup"><span data-stu-id="885ad-113">Hull</span></span> | <span data-ttu-id="885ad-114">Dominio</span><span class="sxs-lookup"><span data-stu-id="885ad-114">Domain</span></span> | <span data-ttu-id="885ad-115">Geometria</span><span class="sxs-lookup"><span data-stu-id="885ad-115">Geometry</span></span> | <span data-ttu-id="885ad-116">Pixel</span><span class="sxs-lookup"><span data-stu-id="885ad-116">Pixel</span></span> | <span data-ttu-id="885ad-117">Calcolo</span><span class="sxs-lookup"><span data-stu-id="885ad-117">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="885ad-118">X</span><span class="sxs-lookup"><span data-stu-id="885ad-118">X</span></span>    |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="885ad-119">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="885ad-119">Minimum Shader Model</span></span>

<span data-ttu-id="885ad-120">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="885ad-120">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="885ad-121">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="885ad-121">Shader Model</span></span>                                              | <span data-ttu-id="885ad-122">Supportato</span><span class="sxs-lookup"><span data-stu-id="885ad-122">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="885ad-123">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="885ad-123">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="885ad-124">sì</span><span class="sxs-lookup"><span data-stu-id="885ad-124">yes</span></span>       |
| [<span data-ttu-id="885ad-125">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="885ad-125">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="885ad-126">no</span><span class="sxs-lookup"><span data-stu-id="885ad-126">no</span></span>        |
| [<span data-ttu-id="885ad-127">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="885ad-127">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="885ad-128">no</span><span class="sxs-lookup"><span data-stu-id="885ad-128">no</span></span>        |
| [<span data-ttu-id="885ad-129">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="885ad-129">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="885ad-130">no</span><span class="sxs-lookup"><span data-stu-id="885ad-130">no</span></span>        |
| [<span data-ttu-id="885ad-131">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="885ad-131">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="885ad-132">no</span><span class="sxs-lookup"><span data-stu-id="885ad-132">no</span></span>        |
| [<span data-ttu-id="885ad-133">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="885ad-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="885ad-134">no</span><span class="sxs-lookup"><span data-stu-id="885ad-134">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="885ad-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="885ad-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="885ad-136">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="885ad-136">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





