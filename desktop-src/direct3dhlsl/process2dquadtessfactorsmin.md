---
title: Process2DQuadTessFactorsMin (funzione)
description: Genera i fattori a mosaico corretti per una patch quad. | Process2DQuadTessFactorsMin (funzione)
ms.assetid: 45adf78a-9386-4460-97df-59d7739a1eee
keywords:
- Funzione Process2DQuadTessFactorsMin HLSL
topic_type:
- apiref
api_name:
- Process2DQuadTessFactorsMin
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 471e244936d6322e31cfd50260151bc56a9764cf
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103969086"
---
# <a name="process2dquadtessfactorsmin-function"></a><span data-ttu-id="0732d-105">Process2DQuadTessFactorsMin (funzione)</span><span class="sxs-lookup"><span data-stu-id="0732d-105">Process2DQuadTessFactorsMin function</span></span>

<span data-ttu-id="0732d-106">Genera i fattori a mosaico corretti per una patch quad.</span><span class="sxs-lookup"><span data-stu-id="0732d-106">Generates the corrected tessellation factors for a quad patch.</span></span>

## <a name="syntax"></a><span data-ttu-id="0732d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0732d-107">Syntax</span></span>

``` syntax
void Process2DQuadTessFactorsMin(
  in  float4 RawEdgeFactors,
  in  float2 InsideScale,
  out float4 RoundedEdgeTessFactors,
  out float2 RoundedInsideTessFactors,
  out float2 UnroundedInsideTessFactors
);
```

## <a name="parameters"></a><span data-ttu-id="0732d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="0732d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0732d-109">*RawEdgeFactors* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0732d-109">*RawEdgeFactors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0732d-110">Tipo: **float4**</span><span class="sxs-lookup"><span data-stu-id="0732d-110">Type: **float4**</span></span>

<span data-ttu-id="0732d-111">Fattori a mosaico perimetrale passati alla fase mosaico.</span><span class="sxs-lookup"><span data-stu-id="0732d-111">The edge tessellation factors, passed into the tessellator stage.</span></span>

</dd> <dt>

<span data-ttu-id="0732d-112">*InsideScale* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0732d-112">*InsideScale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0732d-113">Tipo: **float2**</span><span class="sxs-lookup"><span data-stu-id="0732d-113">Type: **float2**</span></span>

<span data-ttu-id="0732d-114">Fattore di scala applicato ai fattori a mosaico UV calcolati dalla fase a mosaico.</span><span class="sxs-lookup"><span data-stu-id="0732d-114">The scale factor applied to the UV tessellation factors computed by the tessellation stage.</span></span> <span data-ttu-id="0732d-115">L'intervallo consentito per InsideScale è compreso tra 0,0 e 1,0.</span><span class="sxs-lookup"><span data-stu-id="0732d-115">The allowable range for InsideScale is 0.0 to 1.0.</span></span>

</dd> <dt>

<span data-ttu-id="0732d-116">*RoundedEdgeTessFactors* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0732d-116">*RoundedEdgeTessFactors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0732d-117">Tipo: **float4**</span><span class="sxs-lookup"><span data-stu-id="0732d-117">Type: **float4**</span></span>

<span data-ttu-id="0732d-118">Fattori arrotondati a mosaico perimetrale calcolati dalla fase mosaico.</span><span class="sxs-lookup"><span data-stu-id="0732d-118">The rounded edge-tessellation factors calculated by the tessellator stage.</span></span>

</dd> <dt>

<span data-ttu-id="0732d-119">*RoundedInsideTessFactors* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0732d-119">*RoundedInsideTessFactors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0732d-120">Tipo: **float2**</span><span class="sxs-lookup"><span data-stu-id="0732d-120">Type: **float2**</span></span>

<span data-ttu-id="0732d-121">Fattori a mosaico arrotondati calcolati dalla fase mosaico per i bordi interni.</span><span class="sxs-lookup"><span data-stu-id="0732d-121">The rounded tessellation factors calculated by the tessellator stage for inside edges.</span></span>

</dd> <dt>

<span data-ttu-id="0732d-122">*UnroundedInsideTessFactors* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0732d-122">*UnroundedInsideTessFactors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0732d-123">Tipo: **float2**</span><span class="sxs-lookup"><span data-stu-id="0732d-123">Type: **float2**</span></span>

<span data-ttu-id="0732d-124">Fattori a mosaico calcolati dalla fase mosaico per i bordi interni.</span><span class="sxs-lookup"><span data-stu-id="0732d-124">The tessellation factors calculated by the tessellator stage for inside edges.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0732d-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0732d-125">Return value</span></span>

<span data-ttu-id="0732d-126">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="0732d-126">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0732d-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="0732d-127">Remarks</span></span>

<span data-ttu-id="0732d-128">Genera i fattori a mosaico corretti per una patch quad, calcolando i fattori interni a mosaico come minimo dei fattori di mosaico perimetrale.</span><span class="sxs-lookup"><span data-stu-id="0732d-128">Generates the corrected tessellation factors for a quad patch, computing the inside tessellation factors as the minimum of the edge tessellation factors.</span></span> <span data-ttu-id="0732d-129">I fattori di suddivisione a mosaico all'interno dell'utente e della V vengono calcolati in modo indipendente usando i valori minimi dei lati opposti del dominio, quindi vengono ridimensionati in base a InsideScale.</span><span class="sxs-lookup"><span data-stu-id="0732d-129">The U and V inside tessellation factors are computed independently using the minimums of opposing sides of the domain, then are scaled by InsideScale.</span></span> <span data-ttu-id="0732d-130">Il risultato viene quindi arrotondato in base alla modalità di partizionamento, ma i risultati non arrotondati sono disponibili tramite il parametro UnroundedInsideTessFactors.</span><span class="sxs-lookup"><span data-stu-id="0732d-130">The result is then rounded based on the partitioning mode, but the unrounded results are available using the UnroundedInsideTessFactors parameter.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="0732d-131">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="0732d-131">Minimum Shader Model</span></span>

<span data-ttu-id="0732d-132">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="0732d-132">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="0732d-133">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="0732d-133">Shader Model</span></span>                                                                | <span data-ttu-id="0732d-134">Supportato</span><span class="sxs-lookup"><span data-stu-id="0732d-134">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="0732d-135">[Shader Model 5](d3d11-graphics-reference-sm5.md) e versioni successive shader Models</span><span class="sxs-lookup"><span data-stu-id="0732d-135">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="0732d-136">sì</span><span class="sxs-lookup"><span data-stu-id="0732d-136">yes</span></span>       |



 

<span data-ttu-id="0732d-137">Questa funzione è supportata nei tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="0732d-137">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="0732d-138">Vertice</span><span class="sxs-lookup"><span data-stu-id="0732d-138">Vertex</span></span> | <span data-ttu-id="0732d-139">Hull</span><span class="sxs-lookup"><span data-stu-id="0732d-139">Hull</span></span> | <span data-ttu-id="0732d-140">Dominio</span><span class="sxs-lookup"><span data-stu-id="0732d-140">Domain</span></span> | <span data-ttu-id="0732d-141">Geometria</span><span class="sxs-lookup"><span data-stu-id="0732d-141">Geometry</span></span> | <span data-ttu-id="0732d-142">Pixel</span><span class="sxs-lookup"><span data-stu-id="0732d-142">Pixel</span></span> | <span data-ttu-id="0732d-143">Calcolo</span><span class="sxs-lookup"><span data-stu-id="0732d-143">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="0732d-144">x</span><span class="sxs-lookup"><span data-stu-id="0732d-144">x</span></span>    |        |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="0732d-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0732d-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0732d-146">Funzioni intrinseche</span><span class="sxs-lookup"><span data-stu-id="0732d-146">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="0732d-147">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="0732d-147">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




