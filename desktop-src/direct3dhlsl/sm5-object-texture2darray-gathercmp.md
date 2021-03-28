---
title: 'Funzione Texture2DArray:: GatherCmp (S, float, float, int)'
description: "Per quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce il confronto rispetto a un valore di confronto. | Funzione Texture2DArray:: GatherCmp (S, float, float, int)"
ms.assetid: 7bb86448-cc73-4423-9ef4-149427cffc95
keywords:
- Funzione GatherCmp HLSL
topic_type:
- apiref
api_name:
- GatherCmp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fbac4c231f7a7070d3ca4549f3d1189b81292b8c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981199"
---
# <a name="texture2darraygathercmpsfloatfloatint-function"></a><span data-ttu-id="4d001-105">Funzione Texture2DArray:: GatherCmp (S, float, float, int)</span><span class="sxs-lookup"><span data-stu-id="4d001-105">Texture2DArray::GatherCmp(S,float,float,int) function</span></span>

<span data-ttu-id="4d001-106">Per quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce il confronto rispetto a un valore di confronto.</span><span class="sxs-lookup"><span data-stu-id="4d001-106">For four texel values that would be used in a bi-linear filtering operation, returns their comparison against a compare value.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d001-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4d001-107">Syntax</span></span>

``` syntax
float4 GatherCmp(
  in SamplerComparisonState s,
  in float3 location,
  in float compare_value,
  in int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="4d001-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="4d001-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d001-109">*s* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4d001-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d001-110">Tipo: **SamplerComparisonState**</span><span class="sxs-lookup"><span data-stu-id="4d001-110">Type: **SamplerComparisonState**</span></span>

<span data-ttu-id="4d001-111">Indice del campionatore in base zero.</span><span class="sxs-lookup"><span data-stu-id="4d001-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="4d001-112">*posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4d001-112">*location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d001-113">Tipo: **float3**</span><span class="sxs-lookup"><span data-stu-id="4d001-113">Type: **float3**</span></span>

<span data-ttu-id="4d001-114">Coordinate di esempio (u, v).</span><span class="sxs-lookup"><span data-stu-id="4d001-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="4d001-115">*Confronta \_ valore* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4d001-115">*compare\_value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d001-116">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="4d001-116">Type: **float**</span></span>

<span data-ttu-id="4d001-117">Valore da confrontare con ogni valore campionato.</span><span class="sxs-lookup"><span data-stu-id="4d001-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="4d001-118">*offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4d001-118">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d001-119">Tipo: **int2**</span><span class="sxs-lookup"><span data-stu-id="4d001-119">Type: **int2**</span></span>

<span data-ttu-id="4d001-120">Offset applicato alla coordinata di trama prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="4d001-120">An offset that is applied to the texture coordinate before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d001-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4d001-121">Return value</span></span>

<span data-ttu-id="4d001-122">Tipo: **float4**</span><span class="sxs-lookup"><span data-stu-id="4d001-122">Type: **float4**</span></span>

<span data-ttu-id="4d001-123">Un valore a quattro componenti, ogni componente è il risultato di un confronto per ogni componente.</span><span class="sxs-lookup"><span data-stu-id="4d001-123">A four-component value, each component is the result of a per-component comparison.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d001-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="4d001-124">Remarks</span></span>

<span data-ttu-id="4d001-125">Gli esempi di trama possono essere usati per l'interpolazione bilineare.</span><span class="sxs-lookup"><span data-stu-id="4d001-125">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="4d001-126">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="4d001-126">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="4d001-127">Vertice</span><span class="sxs-lookup"><span data-stu-id="4d001-127">Vertex</span></span> | <span data-ttu-id="4d001-128">Hull</span><span class="sxs-lookup"><span data-stu-id="4d001-128">Hull</span></span> | <span data-ttu-id="4d001-129">Dominio</span><span class="sxs-lookup"><span data-stu-id="4d001-129">Domain</span></span> | <span data-ttu-id="4d001-130">Geometria</span><span class="sxs-lookup"><span data-stu-id="4d001-130">Geometry</span></span> | <span data-ttu-id="4d001-131">Pixel</span><span class="sxs-lookup"><span data-stu-id="4d001-131">Pixel</span></span> | <span data-ttu-id="4d001-132">Calcolo</span><span class="sxs-lookup"><span data-stu-id="4d001-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="4d001-133">x</span><span class="sxs-lookup"><span data-stu-id="4d001-133">x</span></span>      | <span data-ttu-id="4d001-134">x</span><span class="sxs-lookup"><span data-stu-id="4d001-134">x</span></span>    | <span data-ttu-id="4d001-135">x</span><span class="sxs-lookup"><span data-stu-id="4d001-135">x</span></span>      | <span data-ttu-id="4d001-136">x</span><span class="sxs-lookup"><span data-stu-id="4d001-136">x</span></span>        | <span data-ttu-id="4d001-137">x</span><span class="sxs-lookup"><span data-stu-id="4d001-137">x</span></span>     | <span data-ttu-id="4d001-138">x</span><span class="sxs-lookup"><span data-stu-id="4d001-138">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="4d001-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4d001-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d001-140">Metodi GatherCmp</span><span class="sxs-lookup"><span data-stu-id="4d001-140">GatherCmp methods</span></span>](texture2darray-gathercmp.md)
</dt> <dt>

[<span data-ttu-id="4d001-141">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="4d001-141">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




