---
title: ProcessTriTessFactorsMin (funzione)
description: Genera i fattori a mosaico corretti per una patch Tri. | ProcessTriTessFactorsMin (funzione)
ms.assetid: fa1e19c2-fadf-42d4-9574-834eaf871393
keywords:
- Funzione ProcessTriTessFactorsMin HLSL
topic_type:
- apiref
api_name:
- ProcessTriTessFactorsMin
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 33f82c7935d47813d833ccc21a7ec0134adee1cc
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104530649"
---
# <a name="processtritessfactorsmin-function"></a><span data-ttu-id="f295e-105">ProcessTriTessFactorsMin (funzione)</span><span class="sxs-lookup"><span data-stu-id="f295e-105">ProcessTriTessFactorsMin function</span></span>

<span data-ttu-id="f295e-106">Genera i fattori a mosaico corretti per una patch Tri.</span><span class="sxs-lookup"><span data-stu-id="f295e-106">Generates the corrected tessellation factors for a tri patch.</span></span>

## <a name="syntax"></a><span data-ttu-id="f295e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f295e-107">Syntax</span></span>

``` syntax
void ProcessTriTessFactorsMin(
  in  float3 RawEdgeFactors,
  in  float InsideScale,
  out float3 RoundedEdgeTessFactors,
  out float RoundedInsideTessFactors,
  out float UnroundedInsideTessFactors
);
```

## <a name="parameters"></a><span data-ttu-id="f295e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f295e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f295e-109">*RawEdgeFactors* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f295e-109">*RawEdgeFactors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f295e-110">Tipo: **float3**</span><span class="sxs-lookup"><span data-stu-id="f295e-110">Type: **float3**</span></span>

<span data-ttu-id="f295e-111">Fattori a mosaico perimetrale passati alla fase mosaico.</span><span class="sxs-lookup"><span data-stu-id="f295e-111">The edge tessellation factors, passed into the tessellator stage.</span></span>

</dd> <dt>

<span data-ttu-id="f295e-112">*InsideScale* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f295e-112">*InsideScale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f295e-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="f295e-113">Type: **float**</span></span>

<span data-ttu-id="f295e-114">Fattore di scala applicato ai fattori a mosaico UV calcolati dalla fase a mosaico.</span><span class="sxs-lookup"><span data-stu-id="f295e-114">The scale factor applied to the UV tessellation factors computed by the tessellation stage.</span></span> <span data-ttu-id="f295e-115">L'intervallo consentito per InsideScale è compreso tra 0,0 e 1,0.</span><span class="sxs-lookup"><span data-stu-id="f295e-115">The allowable range for InsideScale is 0.0 to 1.0.</span></span>

</dd> <dt>

<span data-ttu-id="f295e-116">*RoundedEdgeTessFactors* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f295e-116">*RoundedEdgeTessFactors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f295e-117">Tipo: **float3**</span><span class="sxs-lookup"><span data-stu-id="f295e-117">Type: **float3**</span></span>

<span data-ttu-id="f295e-118">Fattori arrotondati a mosaico perimetrale calcolati dalla fase mosaico.</span><span class="sxs-lookup"><span data-stu-id="f295e-118">The rounded edge-tessellation factors calculated by the tessellator stage.</span></span>

</dd> <dt>

<span data-ttu-id="f295e-119">*RoundedInsideTessFactors* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f295e-119">*RoundedInsideTessFactors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f295e-120">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="f295e-120">Type: **float**</span></span>

<span data-ttu-id="f295e-121">Fattori a mosaico arrotondati calcolati dalla fase mosaico per i bordi interni.</span><span class="sxs-lookup"><span data-stu-id="f295e-121">The rounded tessellation factors calculated by the tessellator stage for inside edges.</span></span>

</dd> <dt>

<span data-ttu-id="f295e-122">*UnroundedInsideTessFactors* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f295e-122">*UnroundedInsideTessFactors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f295e-123">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="f295e-123">Type: **float**</span></span>

<span data-ttu-id="f295e-124">Fattori a mosaico calcolati dalla fase mosaico per i bordi interni.</span><span class="sxs-lookup"><span data-stu-id="f295e-124">The tessellation factors calculated by the tessellator stage for inside edges.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f295e-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f295e-125">Return value</span></span>

<span data-ttu-id="f295e-126">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="f295e-126">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f295e-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="f295e-127">Remarks</span></span>

<span data-ttu-id="f295e-128">Genera i fattori a mosaico corretti per una patch Tri, calcolando il fattore a mosaico interno come minimo dei fattori di mosaico perimetrale, che viene quindi ridimensionato da InsideScale.</span><span class="sxs-lookup"><span data-stu-id="f295e-128">Generates the corrected tessellation factors for a tri patch, computing the inside tessellation factor as the minimum of the edge tessellation factors, which is then scaled by InsideScale.</span></span> <span data-ttu-id="f295e-129">Il risultato viene quindi arrotondato in base alla modalità di partizionamento, ma i risultati non arrotondati sono disponibili tramite il parametro UnroundedInsideTessFactor.</span><span class="sxs-lookup"><span data-stu-id="f295e-129">The result is then rounded based on the partitioning mode, but the unrounded results are available using the UnroundedInsideTessFactor parameter.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="f295e-130">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="f295e-130">Minimum Shader Model</span></span>

<span data-ttu-id="f295e-131">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="f295e-131">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="f295e-132">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="f295e-132">Shader Model</span></span>                                                                | <span data-ttu-id="f295e-133">Supportato</span><span class="sxs-lookup"><span data-stu-id="f295e-133">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="f295e-134">[Shader Model 5](d3d11-graphics-reference-sm5.md) e versioni successive shader Models</span><span class="sxs-lookup"><span data-stu-id="f295e-134">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="f295e-135">sì</span><span class="sxs-lookup"><span data-stu-id="f295e-135">yes</span></span>       |



 

<span data-ttu-id="f295e-136">Questa funzione è supportata nei tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="f295e-136">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="f295e-137">Vertice</span><span class="sxs-lookup"><span data-stu-id="f295e-137">Vertex</span></span> | <span data-ttu-id="f295e-138">Hull</span><span class="sxs-lookup"><span data-stu-id="f295e-138">Hull</span></span> | <span data-ttu-id="f295e-139">Dominio</span><span class="sxs-lookup"><span data-stu-id="f295e-139">Domain</span></span> | <span data-ttu-id="f295e-140">Geometria</span><span class="sxs-lookup"><span data-stu-id="f295e-140">Geometry</span></span> | <span data-ttu-id="f295e-141">Pixel</span><span class="sxs-lookup"><span data-stu-id="f295e-141">Pixel</span></span> | <span data-ttu-id="f295e-142">Calcolo</span><span class="sxs-lookup"><span data-stu-id="f295e-142">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="f295e-143">x</span><span class="sxs-lookup"><span data-stu-id="f295e-143">x</span></span>    |        |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="f295e-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f295e-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f295e-145">Funzioni intrinseche</span><span class="sxs-lookup"><span data-stu-id="f295e-145">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="f295e-146">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="f295e-146">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




