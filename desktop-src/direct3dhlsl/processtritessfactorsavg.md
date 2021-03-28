---
title: ProcessTriTessFactorsAvg (funzione)
description: Genera i fattori a mosaico corretti per una patch Tri. | ProcessTriTessFactorsAvg (funzione)
ms.assetid: 005a63b6-f35d-42d6-bb29-f4ebb374080e
keywords:
- Funzione ProcessTriTessFactorsAvg HLSL
topic_type:
- apiref
api_name:
- ProcessTriTessFactorsAvg
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 90cfa86a09e0e76c90f0013cfa6121917ca25378
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995429"
---
# <a name="processtritessfactorsavg-function"></a><span data-ttu-id="877b2-105">ProcessTriTessFactorsAvg (funzione)</span><span class="sxs-lookup"><span data-stu-id="877b2-105">ProcessTriTessFactorsAvg function</span></span>

<span data-ttu-id="877b2-106">Genera i fattori a mosaico corretti per una patch Tri.</span><span class="sxs-lookup"><span data-stu-id="877b2-106">Generates the corrected tessellation factors for a tri patch.</span></span>

## <a name="syntax"></a><span data-ttu-id="877b2-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="877b2-107">Syntax</span></span>

``` syntax
void ProcessTriTessFactorsAvg(
  in  float3 RawEdgeFactors,
  in  float InsideScale,
  out float3 RoundedEdgeTessFactors,
  out float RoundedInsideTessFactor,
  out float UnroundedInsideTessFactor
);
```

## <a name="parameters"></a><span data-ttu-id="877b2-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="877b2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="877b2-109">*RawEdgeFactors* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="877b2-109">*RawEdgeFactors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="877b2-110">Tipo: **float3**</span><span class="sxs-lookup"><span data-stu-id="877b2-110">Type: **float3**</span></span>

<span data-ttu-id="877b2-111">Fattori a mosaico perimetrale passati alla fase mosaico.</span><span class="sxs-lookup"><span data-stu-id="877b2-111">The edge tessellation factors, passed into the tessellator stage.</span></span>

</dd> <dt>

<span data-ttu-id="877b2-112">*InsideScale* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="877b2-112">*InsideScale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="877b2-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="877b2-113">Type: **float**</span></span>

<span data-ttu-id="877b2-114">Fattore di scala applicato ai fattori a mosaico UV calcolati dalla fase a mosaico.</span><span class="sxs-lookup"><span data-stu-id="877b2-114">The scale factor applied to the UV tessellation factors computed by the tessellation stage.</span></span> <span data-ttu-id="877b2-115">L'intervallo consentito per InsideScale è compreso tra 0,0 e 1,0.</span><span class="sxs-lookup"><span data-stu-id="877b2-115">The allowable range for InsideScale is 0.0 to 1.0.</span></span>

</dd> <dt>

<span data-ttu-id="877b2-116">*RoundedEdgeTessFactors* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="877b2-116">*RoundedEdgeTessFactors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="877b2-117">Tipo: **float3**</span><span class="sxs-lookup"><span data-stu-id="877b2-117">Type: **float3**</span></span>

<span data-ttu-id="877b2-118">Fattori arrotondati a mosaico perimetrale calcolati dalla fase mosaico.</span><span class="sxs-lookup"><span data-stu-id="877b2-118">The rounded edge-tessellation factors calculated by the tessellator stage.</span></span>

</dd> <dt>

<span data-ttu-id="877b2-119">*RoundedInsideTessFactor* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="877b2-119">*RoundedInsideTessFactor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="877b2-120">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="877b2-120">Type: **float**</span></span>

<span data-ttu-id="877b2-121">Fattori a mosaico calcolati dalla fase mosaico e arrotondati.</span><span class="sxs-lookup"><span data-stu-id="877b2-121">The tessellation factors calculated by the tessellator stage, and rounded.</span></span>

</dd> <dt>

<span data-ttu-id="877b2-122">*UnroundedInsideTessFactor* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="877b2-122">*UnroundedInsideTessFactor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="877b2-123">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="877b2-123">Type: **float**</span></span>

<span data-ttu-id="877b2-124">Fattori a mosaico UV originali, non arrotondati calcolati dalla fase di suddivisione a mosaico.</span><span class="sxs-lookup"><span data-stu-id="877b2-124">The original, unrounded, UV tessellation factors computed by the tessellation stage.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="877b2-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="877b2-125">Return value</span></span>

<span data-ttu-id="877b2-126">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="877b2-126">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="877b2-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="877b2-127">Remarks</span></span>

<span data-ttu-id="877b2-128">Genera i fattori a mosaico corretti per una patch Tri, calcolando il fattore a mosaico interno come media dei fattori di mosaico perimetrale, che viene quindi ridimensionato da InsideScale.</span><span class="sxs-lookup"><span data-stu-id="877b2-128">Generates the corrected tessellation factors for a tri patch, computing the inside tessellation factor as the average of the edge tessellation factors, which is then scaled by InsideScale.</span></span> <span data-ttu-id="877b2-129">Il risultato viene quindi arrotondato in base alla modalità di partizionamento, ma i risultati non arrotondati sono disponibili tramite il parametro UnroundedInsideTessFactor.</span><span class="sxs-lookup"><span data-stu-id="877b2-129">The result is then rounded based on the partitioning mode, but the unrounded results are available using the UnroundedInsideTessFactor parameter.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="877b2-130">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="877b2-130">Minimum Shader Model</span></span>

<span data-ttu-id="877b2-131">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="877b2-131">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="877b2-132">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="877b2-132">Shader Model</span></span>                                                                | <span data-ttu-id="877b2-133">Supportato</span><span class="sxs-lookup"><span data-stu-id="877b2-133">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="877b2-134">[Shader Model 5](d3d11-graphics-reference-sm5.md) e versioni successive shader Models</span><span class="sxs-lookup"><span data-stu-id="877b2-134">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="877b2-135">sì</span><span class="sxs-lookup"><span data-stu-id="877b2-135">yes</span></span>       |



 

<span data-ttu-id="877b2-136">Questa funzione è supportata nei tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="877b2-136">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="877b2-137">Vertice</span><span class="sxs-lookup"><span data-stu-id="877b2-137">Vertex</span></span> | <span data-ttu-id="877b2-138">Hull</span><span class="sxs-lookup"><span data-stu-id="877b2-138">Hull</span></span> | <span data-ttu-id="877b2-139">Dominio</span><span class="sxs-lookup"><span data-stu-id="877b2-139">Domain</span></span> | <span data-ttu-id="877b2-140">Geometria</span><span class="sxs-lookup"><span data-stu-id="877b2-140">Geometry</span></span> | <span data-ttu-id="877b2-141">Pixel</span><span class="sxs-lookup"><span data-stu-id="877b2-141">Pixel</span></span> | <span data-ttu-id="877b2-142">Calcolo</span><span class="sxs-lookup"><span data-stu-id="877b2-142">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="877b2-143">x</span><span class="sxs-lookup"><span data-stu-id="877b2-143">x</span></span>    |        |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="877b2-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="877b2-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="877b2-145">Funzioni intrinseche</span><span class="sxs-lookup"><span data-stu-id="877b2-145">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="877b2-146">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="877b2-146">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




