---
title: 'Funzione Texture2D:: GatherCmpGreen (S, float, float, int)'
description: "Per quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce un confronto tra il relativo componente verde e un valore di confronto. | Funzione Texture2D:: GatherCmpGreen (S, float, float, int)"
ms.assetid: 5a11ce0c-56b2-460a-95d7-15688dd158ff
keywords:
- Funzione GatherCmpGreen HLSL
topic_type:
- apiref
api_name:
- GatherCmpGreen
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9346d8b66f90ed780e48e6fcae88e71dc9d9ca1b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353096"
---
# <a name="texture2dgathercmpgreensfloatfloatint-function"></a><span data-ttu-id="2562f-105">Funzione Texture2D:: GatherCmpGreen (S, float, float, int)</span><span class="sxs-lookup"><span data-stu-id="2562f-105">Texture2D::GatherCmpGreen(S,float,float,int) function</span></span>

<span data-ttu-id="2562f-106">Per quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce un confronto tra il relativo componente verde e un valore di confronto.</span><span class="sxs-lookup"><span data-stu-id="2562f-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their green component against a compare value.</span></span>

## <a name="syntax"></a><span data-ttu-id="2562f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2562f-107">Syntax</span></span>

``` syntax
float4 GatherCmpGreen(
  in SamplerComparisonState s,
  in float2 location,
  in float compare_value,
  in int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="2562f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="2562f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2562f-109">*s* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2562f-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2562f-110">Tipo: **SamplerComparisonState**</span><span class="sxs-lookup"><span data-stu-id="2562f-110">Type: **SamplerComparisonState**</span></span>

<span data-ttu-id="2562f-111">Indice del campionatore in base zero.</span><span class="sxs-lookup"><span data-stu-id="2562f-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="2562f-112">*posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2562f-112">*location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2562f-113">Tipo: **float2**</span><span class="sxs-lookup"><span data-stu-id="2562f-113">Type: **float2**</span></span>

<span data-ttu-id="2562f-114">Coordinate di esempio (u, v).</span><span class="sxs-lookup"><span data-stu-id="2562f-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="2562f-115">*Confronta \_ valore* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2562f-115">*compare\_value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2562f-116">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="2562f-116">Type: **float**</span></span>

<span data-ttu-id="2562f-117">Valore da confrontare con ogni valore campionato.</span><span class="sxs-lookup"><span data-stu-id="2562f-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="2562f-118">*offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2562f-118">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2562f-119">Tipo: **int2**</span><span class="sxs-lookup"><span data-stu-id="2562f-119">Type: **int2**</span></span>

<span data-ttu-id="2562f-120">Offset applicato alla coordinata di trama prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="2562f-120">An offset that is applied to the texture coordinate before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2562f-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2562f-121">Return value</span></span>

<span data-ttu-id="2562f-122">Tipo: **float4**</span><span class="sxs-lookup"><span data-stu-id="2562f-122">Type: **float4**</span></span>

<span data-ttu-id="2562f-123">Un valore a quattro componenti, ogni componente è il risultato di un confronto per ogni componente.</span><span class="sxs-lookup"><span data-stu-id="2562f-123">A four-component value, each component is the result of a per-component comparison.</span></span>

## <a name="remarks"></a><span data-ttu-id="2562f-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="2562f-124">Remarks</span></span>

<span data-ttu-id="2562f-125">Gli esempi di trama possono essere usati per l'interpolazione bilineare.</span><span class="sxs-lookup"><span data-stu-id="2562f-125">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="2562f-126">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="2562f-126">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="2562f-127">Vertice</span><span class="sxs-lookup"><span data-stu-id="2562f-127">Vertex</span></span> | <span data-ttu-id="2562f-128">Hull</span><span class="sxs-lookup"><span data-stu-id="2562f-128">Hull</span></span> | <span data-ttu-id="2562f-129">Dominio</span><span class="sxs-lookup"><span data-stu-id="2562f-129">Domain</span></span> | <span data-ttu-id="2562f-130">Geometria</span><span class="sxs-lookup"><span data-stu-id="2562f-130">Geometry</span></span> | <span data-ttu-id="2562f-131">Pixel</span><span class="sxs-lookup"><span data-stu-id="2562f-131">Pixel</span></span> | <span data-ttu-id="2562f-132">Calcolo</span><span class="sxs-lookup"><span data-stu-id="2562f-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="2562f-133">x</span><span class="sxs-lookup"><span data-stu-id="2562f-133">x</span></span>      | <span data-ttu-id="2562f-134">x</span><span class="sxs-lookup"><span data-stu-id="2562f-134">x</span></span>    | <span data-ttu-id="2562f-135">x</span><span class="sxs-lookup"><span data-stu-id="2562f-135">x</span></span>      | <span data-ttu-id="2562f-136">x</span><span class="sxs-lookup"><span data-stu-id="2562f-136">x</span></span>        | <span data-ttu-id="2562f-137">x</span><span class="sxs-lookup"><span data-stu-id="2562f-137">x</span></span>     | <span data-ttu-id="2562f-138">x</span><span class="sxs-lookup"><span data-stu-id="2562f-138">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="2562f-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2562f-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2562f-140">Metodi GatherCmpGreen</span><span class="sxs-lookup"><span data-stu-id="2562f-140">GatherCmpGreen methods</span></span>](texture2d-gathercmpgreen.md)
</dt> <dt>

[<span data-ttu-id="2562f-141">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="2562f-141">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




