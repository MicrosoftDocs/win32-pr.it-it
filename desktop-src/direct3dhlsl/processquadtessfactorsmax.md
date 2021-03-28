---
title: ProcessQuadTessFactorsMax (funzione)
description: Genera i fattori a mosaico corretti per una patch quad. | ProcessQuadTessFactorsMax (funzione)
ms.assetid: a0c91430-db25-49c9-bcc8-d2be1d0e6f6c
keywords:
- Funzione ProcessQuadTessFactorsMax HLSL
topic_type:
- apiref
api_name:
- ProcessQuadTessFactorsMax
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 62219301e93bebf7825328fd381b5d2fbb607925
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981802"
---
# <a name="processquadtessfactorsmax-function"></a><span data-ttu-id="5b6c4-105">ProcessQuadTessFactorsMax (funzione)</span><span class="sxs-lookup"><span data-stu-id="5b6c4-105">ProcessQuadTessFactorsMax function</span></span>

<span data-ttu-id="5b6c4-106">Genera i fattori a mosaico corretti per una patch quad.</span><span class="sxs-lookup"><span data-stu-id="5b6c4-106">Generates the corrected tessellation factors for a quad patch.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b6c4-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5b6c4-107">Syntax</span></span>

``` syntax
void ProcessQuadTessFactorsMax(
  in  float4 RawEdgeFactors,
  in  float InsideScale,
  out float4 RoundedEdgeTessFactors,
  out float2 RoundedInsideTessFactors,
  out float2 UnroundedInsideTessFactors
);
```

## <a name="parameters"></a><span data-ttu-id="5b6c4-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="5b6c4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b6c4-109">*RawEdgeFactors* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5b6c4-109">*RawEdgeFactors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b6c4-110">Tipo: **float4**</span><span class="sxs-lookup"><span data-stu-id="5b6c4-110">Type: **float4**</span></span>

<span data-ttu-id="5b6c4-111">Fattori a mosaico perimetrale passati alla fase mosaico.</span><span class="sxs-lookup"><span data-stu-id="5b6c4-111">The edge tessellation factors, passed into the tessellator stage.</span></span>

</dd> <dt>

<span data-ttu-id="5b6c4-112">*InsideScale* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5b6c4-112">*InsideScale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b6c4-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="5b6c4-113">Type: **float**</span></span>

<span data-ttu-id="5b6c4-114">Fattore di scala applicato ai fattori a mosaico UV calcolati dalla fase a mosaico.</span><span class="sxs-lookup"><span data-stu-id="5b6c4-114">The scale factor applied to the UV tessellation factors computed by the tessellation stage.</span></span> <span data-ttu-id="5b6c4-115">L'intervallo consentito per InsideScale è compreso tra 0,0 e 1,0.</span><span class="sxs-lookup"><span data-stu-id="5b6c4-115">The allowable range for InsideScale is 0.0 to 1.0.</span></span>

</dd> <dt>

<span data-ttu-id="5b6c4-116">*RoundedEdgeTessFactors* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="5b6c4-116">*RoundedEdgeTessFactors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5b6c4-117">Tipo: **float4**</span><span class="sxs-lookup"><span data-stu-id="5b6c4-117">Type: **float4**</span></span>

<span data-ttu-id="5b6c4-118">Fattori arrotondati a mosaico perimetrale calcolati dalla fase mosaico.</span><span class="sxs-lookup"><span data-stu-id="5b6c4-118">The rounded edge-tessellation factors calculated by the tessellator stage.</span></span>

</dd> <dt>

<span data-ttu-id="5b6c4-119">*RoundedInsideTessFactors* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="5b6c4-119">*RoundedInsideTessFactors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5b6c4-120">Tipo: **float2**</span><span class="sxs-lookup"><span data-stu-id="5b6c4-120">Type: **float2**</span></span>

<span data-ttu-id="5b6c4-121">Fattori a mosaico arrotondati calcolati dalla fase mosaico per i bordi interni.</span><span class="sxs-lookup"><span data-stu-id="5b6c4-121">The rounded tessellation factors calculated by the tessellator stage for inside edges.</span></span>

</dd> <dt>

<span data-ttu-id="5b6c4-122">*UnroundedInsideTessFactors* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="5b6c4-122">*UnroundedInsideTessFactors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5b6c4-123">Tipo: **float2**</span><span class="sxs-lookup"><span data-stu-id="5b6c4-123">Type: **float2**</span></span>

<span data-ttu-id="5b6c4-124">Fattori a mosaico calcolati dalla fase mosaico per i bordi interni.</span><span class="sxs-lookup"><span data-stu-id="5b6c4-124">The tessellation factors calculated by the tessellator stage for inside edges.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b6c4-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5b6c4-125">Return value</span></span>

<span data-ttu-id="5b6c4-126">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="5b6c4-126">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b6c4-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="5b6c4-127">Remarks</span></span>

<span data-ttu-id="5b6c4-128">Genera i fattori a mosaico corretti per una patch quad, calcolando i fattori interni a mosaico come massimo dei fattori di mosaico perimetrale.</span><span class="sxs-lookup"><span data-stu-id="5b6c4-128">Generates the corrected tessellation factors for a quad patch, computing the inside tessellation factors as the maximum of the edge tessellation factors.</span></span> <span data-ttu-id="5b6c4-129">I fattori all'interno di Tess saranno valori identici determinati dal numero massimo di tutti e quattro i bordi ridimensionati da InsideScale.</span><span class="sxs-lookup"><span data-stu-id="5b6c4-129">The inside tess factors will be identical values determined by the maximum of all four edges scaled by InsideScale.</span></span> <span data-ttu-id="5b6c4-130">Il risultato viene quindi arrotondato in base alla modalità di partizionamento, ma i risultati non arrotondati sono disponibili tramite il parametro *UnroundedInsideTessFactors* .</span><span class="sxs-lookup"><span data-stu-id="5b6c4-130">The result is then rounded based on the partitioning mode, but the unrounded results are available using the *UnroundedInsideTessFactors* parameter.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="5b6c4-131">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="5b6c4-131">Minimum Shader Model</span></span>

<span data-ttu-id="5b6c4-132">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="5b6c4-132">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="5b6c4-133">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="5b6c4-133">Shader Model</span></span>                                                                | <span data-ttu-id="5b6c4-134">Supportato</span><span class="sxs-lookup"><span data-stu-id="5b6c4-134">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="5b6c4-135">[Shader Model 5](d3d11-graphics-reference-sm5.md) e versioni successive shader Models</span><span class="sxs-lookup"><span data-stu-id="5b6c4-135">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="5b6c4-136">sì</span><span class="sxs-lookup"><span data-stu-id="5b6c4-136">yes</span></span>       |



 

<span data-ttu-id="5b6c4-137">Questa funzione è supportata nei tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="5b6c4-137">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="5b6c4-138">Vertice</span><span class="sxs-lookup"><span data-stu-id="5b6c4-138">Vertex</span></span> | <span data-ttu-id="5b6c4-139">Hull</span><span class="sxs-lookup"><span data-stu-id="5b6c4-139">Hull</span></span> | <span data-ttu-id="5b6c4-140">Dominio</span><span class="sxs-lookup"><span data-stu-id="5b6c4-140">Domain</span></span> | <span data-ttu-id="5b6c4-141">Geometria</span><span class="sxs-lookup"><span data-stu-id="5b6c4-141">Geometry</span></span> | <span data-ttu-id="5b6c4-142">Pixel</span><span class="sxs-lookup"><span data-stu-id="5b6c4-142">Pixel</span></span> | <span data-ttu-id="5b6c4-143">Calcolo</span><span class="sxs-lookup"><span data-stu-id="5b6c4-143">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="5b6c4-144">x</span><span class="sxs-lookup"><span data-stu-id="5b6c4-144">x</span></span>    |        |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="5b6c4-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5b6c4-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b6c4-146">Funzioni intrinseche</span><span class="sxs-lookup"><span data-stu-id="5b6c4-146">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="5b6c4-147">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="5b6c4-147">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




