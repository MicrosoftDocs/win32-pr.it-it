---
title: Process2DQuadTessFactorsAvg (funzione)
description: Genera i fattori a mosaico corretti per una patch quad. | Process2DQuadTessFactorsAvg (funzione)
ms.assetid: 7f96f634-0ad5-4037-a08e-b0b99b89cd91
keywords:
- Funzione Process2DQuadTessFactorsAvg HLSL
topic_type:
- apiref
api_name:
- Process2DQuadTessFactorsAvg
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4012d99a1f7714fae68f4679991aedcf810d1b4e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103761656"
---
# <a name="process2dquadtessfactorsavg-function"></a><span data-ttu-id="0a568-105">Process2DQuadTessFactorsAvg (funzione)</span><span class="sxs-lookup"><span data-stu-id="0a568-105">Process2DQuadTessFactorsAvg function</span></span>

<span data-ttu-id="0a568-106">Genera i fattori a mosaico corretti per una patch quad.</span><span class="sxs-lookup"><span data-stu-id="0a568-106">Generates the corrected tessellation factors for a quad patch.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a568-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0a568-107">Syntax</span></span>

``` syntax
void Process2DQuadTessFactorsAvg(
  in  float4 RawEdgeFactors,
  in  float2 InsideScale,
  out float4 RoundedEdgeTessFactors,
  out float2 RoundedInsideTessFactors,
  out float2 UnroundedInsideTessFactors
);
```

## <a name="parameters"></a><span data-ttu-id="0a568-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="0a568-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a568-109">*RawEdgeFactors* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0a568-109">*RawEdgeFactors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a568-110">Tipo: **float4**</span><span class="sxs-lookup"><span data-stu-id="0a568-110">Type: **float4**</span></span>

<span data-ttu-id="0a568-111">Fattori a mosaico perimetrale passati alla fase mosaico.</span><span class="sxs-lookup"><span data-stu-id="0a568-111">The edge tessellation factors, passed into the tessellator stage.</span></span>

</dd> <dt>

<span data-ttu-id="0a568-112">*InsideScale* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0a568-112">*InsideScale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a568-113">Tipo: **float2**</span><span class="sxs-lookup"><span data-stu-id="0a568-113">Type: **float2**</span></span>

<span data-ttu-id="0a568-114">Fattore di scala applicato ai fattori a mosaico UV calcolati dalla fase a mosaico.</span><span class="sxs-lookup"><span data-stu-id="0a568-114">The scale factor applied to the UV tessellation factors computed by the tessellation stage.</span></span> <span data-ttu-id="0a568-115">L'intervallo consentito per InsideScale è compreso tra 0,0 e 1,0.</span><span class="sxs-lookup"><span data-stu-id="0a568-115">The allowable range for InsideScale is 0.0 to 1.0.</span></span>

</dd> <dt>

<span data-ttu-id="0a568-116">*RoundedEdgeTessFactors* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0a568-116">*RoundedEdgeTessFactors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0a568-117">Tipo: **float4**</span><span class="sxs-lookup"><span data-stu-id="0a568-117">Type: **float4**</span></span>

<span data-ttu-id="0a568-118">Fattori arrotondati a mosaico perimetrale calcolati dalla fase mosaico.</span><span class="sxs-lookup"><span data-stu-id="0a568-118">The rounded edge-tessellation factors calculated by the tessellator stage.</span></span>

</dd> <dt>

<span data-ttu-id="0a568-119">*RoundedInsideTessFactors* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0a568-119">*RoundedInsideTessFactors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0a568-120">Tipo: **float2**</span><span class="sxs-lookup"><span data-stu-id="0a568-120">Type: **float2**</span></span>

<span data-ttu-id="0a568-121">Fattori a mosaico arrotondati calcolati dalla fase mosaico per i bordi interni.</span><span class="sxs-lookup"><span data-stu-id="0a568-121">The rounded tessellation factors calculated by the tessellator stage for inside edges.</span></span>

</dd> <dt>

<span data-ttu-id="0a568-122">*UnroundedInsideTessFactors* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0a568-122">*UnroundedInsideTessFactors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0a568-123">Tipo: **float2**</span><span class="sxs-lookup"><span data-stu-id="0a568-123">Type: **float2**</span></span>

<span data-ttu-id="0a568-124">Fattori a mosaico calcolati dalla fase mosaico per i bordi interni.</span><span class="sxs-lookup"><span data-stu-id="0a568-124">The tessellation factors calculated by the tessellator stage for inside edges.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a568-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0a568-125">Return value</span></span>

<span data-ttu-id="0a568-126">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="0a568-126">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a568-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="0a568-127">Remarks</span></span>

<span data-ttu-id="0a568-128">Genera i fattori a mosaico corretti per una patch quad, calcolando i fattori interni a mosaico come media dei fattori di mosaico perimetrale.</span><span class="sxs-lookup"><span data-stu-id="0a568-128">Generates the corrected tessellation factors for a quad patch, computing the inside tessellation factors as the average of the edge tessellation factors.</span></span> <span data-ttu-id="0a568-129">I fattori di suddivisione a mosaico interni vengono calcolati in modo indipendente utilizzando la media dei lati opposti del dominio, quindi vengono ridimensionati in base a InsideScale.</span><span class="sxs-lookup"><span data-stu-id="0a568-129">The U and V inside tessellation factors are computed independently using the average of opposing sides of the domain, then are scaled by InsideScale.</span></span> <span data-ttu-id="0a568-130">Il risultato viene quindi arrotondato in base alla modalità di partizionamento, ma i risultati non arrotondati sono disponibili tramite il parametro UnroundedInsideTessFactors.</span><span class="sxs-lookup"><span data-stu-id="0a568-130">The result is then rounded based on the partitioning mode, but the unrounded results are available using the UnroundedInsideTessFactors parameter.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="0a568-131">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="0a568-131">Minimum Shader Model</span></span>

<span data-ttu-id="0a568-132">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="0a568-132">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="0a568-133">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="0a568-133">Shader Model</span></span>                                                                | <span data-ttu-id="0a568-134">Supportato</span><span class="sxs-lookup"><span data-stu-id="0a568-134">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="0a568-135">[Shader Model 5](d3d11-graphics-reference-sm5.md) e versioni successive shader Models</span><span class="sxs-lookup"><span data-stu-id="0a568-135">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="0a568-136">sì</span><span class="sxs-lookup"><span data-stu-id="0a568-136">yes</span></span>       |



 

<span data-ttu-id="0a568-137">Questa funzione è supportata nei tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="0a568-137">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="0a568-138">Vertice</span><span class="sxs-lookup"><span data-stu-id="0a568-138">Vertex</span></span> | <span data-ttu-id="0a568-139">Hull</span><span class="sxs-lookup"><span data-stu-id="0a568-139">Hull</span></span> | <span data-ttu-id="0a568-140">Dominio</span><span class="sxs-lookup"><span data-stu-id="0a568-140">Domain</span></span> | <span data-ttu-id="0a568-141">Geometria</span><span class="sxs-lookup"><span data-stu-id="0a568-141">Geometry</span></span> | <span data-ttu-id="0a568-142">Pixel</span><span class="sxs-lookup"><span data-stu-id="0a568-142">Pixel</span></span> | <span data-ttu-id="0a568-143">Calcolo</span><span class="sxs-lookup"><span data-stu-id="0a568-143">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="0a568-144">x</span><span class="sxs-lookup"><span data-stu-id="0a568-144">x</span></span>    |        |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="0a568-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0a568-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a568-146">Funzioni intrinseche</span><span class="sxs-lookup"><span data-stu-id="0a568-146">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="0a568-147">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="0a568-147">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




