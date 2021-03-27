---
title: 'Funzione Texture2DArray:: GatherCmpGreen (S, float, float, int)'
description: "Per quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce un confronto tra il relativo componente verde e un valore di confronto. | Funzione Texture2DArray:: GatherCmpGreen (S, float, float, int)"
ms.assetid: baf14de9-5237-42a5-bffc-848e55cbc28f
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
ms.openlocfilehash: 4f29da331d71c1fa8a2ceff783e4daec4a886d06
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995714"
---
# <a name="texture2darraygathercmpgreensfloatfloatint-function"></a><span data-ttu-id="c1975-105">Funzione Texture2DArray:: GatherCmpGreen (S, float, float, int)</span><span class="sxs-lookup"><span data-stu-id="c1975-105">Texture2DArray::GatherCmpGreen(S,float,float,int) function</span></span>

<span data-ttu-id="c1975-106">Per quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce un confronto tra il relativo componente verde e un valore di confronto.</span><span class="sxs-lookup"><span data-stu-id="c1975-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their green component against a compare value.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1975-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c1975-107">Syntax</span></span>

``` syntax
float4 GatherCmpGreen(
  in SamplerComparisonState s,
  in float3 location,
  in float compare_value,
  in int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="c1975-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="c1975-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1975-109">*s* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c1975-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1975-110">Tipo: **SamplerComparisonState**</span><span class="sxs-lookup"><span data-stu-id="c1975-110">Type: **SamplerComparisonState**</span></span>

<span data-ttu-id="c1975-111">Indice del campionatore in base zero.</span><span class="sxs-lookup"><span data-stu-id="c1975-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="c1975-112">*posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c1975-112">*location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1975-113">Tipo: **float3**</span><span class="sxs-lookup"><span data-stu-id="c1975-113">Type: **float3**</span></span>

<span data-ttu-id="c1975-114">Coordinate di esempio (u, v).</span><span class="sxs-lookup"><span data-stu-id="c1975-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="c1975-115">*Confronta \_ valore* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c1975-115">*compare\_value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1975-116">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="c1975-116">Type: **float**</span></span>

<span data-ttu-id="c1975-117">Valore da confrontare con ogni valore campionato.</span><span class="sxs-lookup"><span data-stu-id="c1975-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="c1975-118">*offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c1975-118">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1975-119">Tipo: **int2**</span><span class="sxs-lookup"><span data-stu-id="c1975-119">Type: **int2**</span></span>

<span data-ttu-id="c1975-120">Offset applicato alla coordinata di trama prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="c1975-120">An offset that is applied to the texture coordinate before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1975-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c1975-121">Return value</span></span>

<span data-ttu-id="c1975-122">Tipo: **float4**</span><span class="sxs-lookup"><span data-stu-id="c1975-122">Type: **float4**</span></span>

<span data-ttu-id="c1975-123">Un valore a quattro componenti, ogni componente è il risultato di un confronto per ogni componente.</span><span class="sxs-lookup"><span data-stu-id="c1975-123">A four-component value, each component is the result of a per-component comparison.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1975-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="c1975-124">Remarks</span></span>

<span data-ttu-id="c1975-125">Gli esempi di trama possono essere usati per l'interpolazione bilineare.</span><span class="sxs-lookup"><span data-stu-id="c1975-125">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="c1975-126">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="c1975-126">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="c1975-127">Vertice</span><span class="sxs-lookup"><span data-stu-id="c1975-127">Vertex</span></span> | <span data-ttu-id="c1975-128">Hull</span><span class="sxs-lookup"><span data-stu-id="c1975-128">Hull</span></span> | <span data-ttu-id="c1975-129">Dominio</span><span class="sxs-lookup"><span data-stu-id="c1975-129">Domain</span></span> | <span data-ttu-id="c1975-130">Geometria</span><span class="sxs-lookup"><span data-stu-id="c1975-130">Geometry</span></span> | <span data-ttu-id="c1975-131">Pixel</span><span class="sxs-lookup"><span data-stu-id="c1975-131">Pixel</span></span> | <span data-ttu-id="c1975-132">Calcolo</span><span class="sxs-lookup"><span data-stu-id="c1975-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="c1975-133">x</span><span class="sxs-lookup"><span data-stu-id="c1975-133">x</span></span>      | <span data-ttu-id="c1975-134">x</span><span class="sxs-lookup"><span data-stu-id="c1975-134">x</span></span>    | <span data-ttu-id="c1975-135">x</span><span class="sxs-lookup"><span data-stu-id="c1975-135">x</span></span>      | <span data-ttu-id="c1975-136">x</span><span class="sxs-lookup"><span data-stu-id="c1975-136">x</span></span>        | <span data-ttu-id="c1975-137">x</span><span class="sxs-lookup"><span data-stu-id="c1975-137">x</span></span>     | <span data-ttu-id="c1975-138">x</span><span class="sxs-lookup"><span data-stu-id="c1975-138">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="c1975-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c1975-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1975-140">Metodi GatherCmpGreen</span><span class="sxs-lookup"><span data-stu-id="c1975-140">GatherCmpGreen methods</span></span>](texture2darray-gathercmpgreen.md)
</dt> <dt>

[<span data-ttu-id="c1975-141">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="c1975-141">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




