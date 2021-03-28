---
title: Funzioni intrinseche del modello shader 5
description: Shader Model 5 implementa le funzioni intrinseche dal modello di Shader 4 e versioni precedenti (vedere funzioni intrinseche (DirectX HLSL) per un elenco completo delle funzioni supportate), nonché le nuove funzioni seguenti
ms.assetid: 6f91fb40-d6d0-459f-adf7-cff263d7d346
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0cd5976526f75b676a853ef7480d4e81e0e00a91
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398219"
---
# <a name="shader-model-5-intrinsic-functions"></a><span data-ttu-id="0779b-103">Funzioni intrinseche del modello shader 5</span><span class="sxs-lookup"><span data-stu-id="0779b-103">Shader Model 5 Intrinsic Functions</span></span>

<span data-ttu-id="0779b-104">Shader Model 5 implementa le funzioni intrinseche dal modello di Shader 4 e versioni precedenti (vedere [**funzioni intrinseche (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md) per un elenco completo delle funzioni supportate), nonché le nuove funzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="0779b-104">Shader Model 5 implements the intrinsic functions from Shader Model 4 and below (see [**Intrinsic Functions (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md) for a complete list of supported functions), as well as the following new functions:</span></span>

-   [<span data-ttu-id="0779b-105">**AllMemoryBarrier**</span><span class="sxs-lookup"><span data-stu-id="0779b-105">**AllMemoryBarrier**</span></span>](allmemorybarrier.md)
-   [<span data-ttu-id="0779b-106">**AllMemoryBarrierWithGroupSync**</span><span class="sxs-lookup"><span data-stu-id="0779b-106">**AllMemoryBarrierWithGroupSync**</span></span>](allmemorybarrierwithgroupsync.md)
-   [<span data-ttu-id="0779b-107">**AsDouble**</span><span class="sxs-lookup"><span data-stu-id="0779b-107">**asdouble**</span></span>](asdouble.md)
-   [<span data-ttu-id="0779b-108">**asuint**</span><span class="sxs-lookup"><span data-stu-id="0779b-108">**asuint**</span></span>](asuint.md)
-   [<span data-ttu-id="0779b-109">**countbits**</span><span class="sxs-lookup"><span data-stu-id="0779b-109">**countbits**</span></span>](countbits.md)
-   [<span data-ttu-id="0779b-110">**DDX \_ grossolano**</span><span class="sxs-lookup"><span data-stu-id="0779b-110">**ddx\_coarse**</span></span>](ddx-coarse.md)
-   [<span data-ttu-id="0779b-111">**ddy \_ grossolano**</span><span class="sxs-lookup"><span data-stu-id="0779b-111">**ddy\_coarse**</span></span>](ddy-coarse.md)
-   [<span data-ttu-id="0779b-112">**DeviceMemoryBarrier**</span><span class="sxs-lookup"><span data-stu-id="0779b-112">**DeviceMemoryBarrier**</span></span>](devicememorybarrier.md)
-   [<span data-ttu-id="0779b-113">**DeviceMemoryBarrierWithGroupSync**</span><span class="sxs-lookup"><span data-stu-id="0779b-113">**DeviceMemoryBarrierWithGroupSync**</span></span>](devicememorybarrierwithgroupsync.md)
-   [<span data-ttu-id="0779b-114">**EvaluateAttributeAtCentroid**</span><span class="sxs-lookup"><span data-stu-id="0779b-114">**EvaluateAttributeAtCentroid**</span></span>](evaluateattributeatcentroid.md)
-   [<span data-ttu-id="0779b-115">**EvaluateAttributeAtSample**</span><span class="sxs-lookup"><span data-stu-id="0779b-115">**EvaluateAttributeAtSample**</span></span>](evaluateattributeatsample.md)
-   [<span data-ttu-id="0779b-116">**f16tof32**</span><span class="sxs-lookup"><span data-stu-id="0779b-116">**f16tof32**</span></span>](f16tof32.md)
-   [<span data-ttu-id="0779b-117">**f32tof16**</span><span class="sxs-lookup"><span data-stu-id="0779b-117">**f32tof16**</span></span>](f32tof16.md)
-   [<span data-ttu-id="0779b-118">**firstbithigh**</span><span class="sxs-lookup"><span data-stu-id="0779b-118">**firstbithigh**</span></span>](firstbithigh.md)
-   [<span data-ttu-id="0779b-119">**firstbitlow**</span><span class="sxs-lookup"><span data-stu-id="0779b-119">**firstbitlow**</span></span>](firstbitlow.md)
-   [<span data-ttu-id="0779b-120">**FMA**</span><span class="sxs-lookup"><span data-stu-id="0779b-120">**fma**</span></span>](dx-graphics-hlsl-fma.md)
-   [<span data-ttu-id="0779b-121">**GroupMemoryBarrier**</span><span class="sxs-lookup"><span data-stu-id="0779b-121">**GroupMemoryBarrier**</span></span>](groupmemorybarrier.md)
-   [<span data-ttu-id="0779b-122">**GroupMemoryBarrierWithGroupSync**</span><span class="sxs-lookup"><span data-stu-id="0779b-122">**GroupMemoryBarrierWithGroupSync**</span></span>](groupmemorybarrierwithgroupsync.md)
-   [<span data-ttu-id="0779b-123">**InterlockedAdd**</span><span class="sxs-lookup"><span data-stu-id="0779b-123">**InterlockedAdd**</span></span>](interlockedadd.md)
-   [<span data-ttu-id="0779b-124">**InterlockedAnd**</span><span class="sxs-lookup"><span data-stu-id="0779b-124">**InterlockedAnd**</span></span>](interlockedand.md)
-   [<span data-ttu-id="0779b-125">**InterlockedCompareExchange**</span><span class="sxs-lookup"><span data-stu-id="0779b-125">**InterlockedCompareExchange**</span></span>](interlockedcompareexchange.md)
-   [<span data-ttu-id="0779b-126">**InterlockedCompareStore**</span><span class="sxs-lookup"><span data-stu-id="0779b-126">**InterlockedCompareStore**</span></span>](interlockedcomparestore.md)
-   [<span data-ttu-id="0779b-127">**InterlockedExchange**</span><span class="sxs-lookup"><span data-stu-id="0779b-127">**InterlockedExchange**</span></span>](interlockedexchange.md)
-   [<span data-ttu-id="0779b-128">**InterlockedMax**</span><span class="sxs-lookup"><span data-stu-id="0779b-128">**InterlockedMax**</span></span>](interlockedmax.md)
-   [<span data-ttu-id="0779b-129">**InterlockedMin**</span><span class="sxs-lookup"><span data-stu-id="0779b-129">**InterlockedMin**</span></span>](interlockedmin.md)
-   [<span data-ttu-id="0779b-130">**Interblocco**</span><span class="sxs-lookup"><span data-stu-id="0779b-130">**InterlockedOr**</span></span>](interlockedor.md)
-   [<span data-ttu-id="0779b-131">**InterlockedXor**</span><span class="sxs-lookup"><span data-stu-id="0779b-131">**InterlockedXor**</span></span>](interlockedxor.md)
-   [<span data-ttu-id="0779b-132">**msad4**</span><span class="sxs-lookup"><span data-stu-id="0779b-132">**msad4**</span></span>](dx-graphics-hlsl-msad4.md)
-   [<span data-ttu-id="0779b-133">**Process2DQuadTessFactorsAvg**</span><span class="sxs-lookup"><span data-stu-id="0779b-133">**Process2DQuadTessFactorsAvg**</span></span>](process2dquadtessfactorsavg.md)
-   [<span data-ttu-id="0779b-134">**Process2DQuadTessFactorsMax**</span><span class="sxs-lookup"><span data-stu-id="0779b-134">**Process2DQuadTessFactorsMax**</span></span>](process2dquadtessfactorsmax.md)
-   [<span data-ttu-id="0779b-135">**Process2DQuadTessFactorsMin**</span><span class="sxs-lookup"><span data-stu-id="0779b-135">**Process2DQuadTessFactorsMin**</span></span>](process2dquadtessfactorsmin.md)
-   [<span data-ttu-id="0779b-136">**ProcessIsolineTessFactors**</span><span class="sxs-lookup"><span data-stu-id="0779b-136">**ProcessIsolineTessFactors**</span></span>](processisolinetessfactors.md)
-   [<span data-ttu-id="0779b-137">**ProcessQuadTessFactorsAvg**</span><span class="sxs-lookup"><span data-stu-id="0779b-137">**ProcessQuadTessFactorsAvg**</span></span>](processquadtessfactorsavg.md)
-   [<span data-ttu-id="0779b-138">**ProcessQuadTessFactorsMax**</span><span class="sxs-lookup"><span data-stu-id="0779b-138">**ProcessQuadTessFactorsMax**</span></span>](processquadtessfactorsmax.md)
-   [<span data-ttu-id="0779b-139">**ProcessQuadTessFactorsMin**</span><span class="sxs-lookup"><span data-stu-id="0779b-139">**ProcessQuadTessFactorsMin**</span></span>](processquadtessfactorsmin.md)
-   [<span data-ttu-id="0779b-140">**ProcessTriTessFactorsAvg**</span><span class="sxs-lookup"><span data-stu-id="0779b-140">**ProcessTriTessFactorsAvg**</span></span>](processtritessfactorsavg.md)
-   [<span data-ttu-id="0779b-141">**ProcessTriTessFactorsMax**</span><span class="sxs-lookup"><span data-stu-id="0779b-141">**ProcessTriTessFactorsMax**</span></span>](processtritessfactorsmax.md)
-   [<span data-ttu-id="0779b-142">**ProcessTriTessFactorsMin**</span><span class="sxs-lookup"><span data-stu-id="0779b-142">**ProcessTriTessFactorsMin**</span></span>](processtritessfactorsmin.md)
-   [<span data-ttu-id="0779b-143">**rcp**</span><span class="sxs-lookup"><span data-stu-id="0779b-143">**rcp**</span></span>](rcp.md)
-   [<span data-ttu-id="0779b-144">**reversebits**</span><span class="sxs-lookup"><span data-stu-id="0779b-144">**reversebits**</span></span>](reversebits.md)

## <a name="related-topics"></a><span data-ttu-id="0779b-145">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0779b-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0779b-146">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="0779b-146">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




