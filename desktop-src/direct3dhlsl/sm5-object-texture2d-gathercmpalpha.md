---
title: 'Funzione Texture2D:: GatherCmpAlpha (S, float, float, int)'
description: "Per quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce un confronto tra il relativo componente alfa e un valore di confronto. | Funzione Texture2D:: GatherCmpAlpha (S, float, float, int)"
ms.assetid: 6fa60604-1eac-405d-bffa-3055569b7a09
keywords:
- Funzione GatherCmpAlpha HLSL
topic_type:
- apiref
api_name:
- GatherCmpAlpha
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3a7f7fcdc6e24cac5c04068fda7f781d0bdd376a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104401854"
---
# <a name="texture2dgathercmpalphasfloatfloatint-function"></a><span data-ttu-id="0ce91-105">Funzione Texture2D:: GatherCmpAlpha (S, float, float, int)</span><span class="sxs-lookup"><span data-stu-id="0ce91-105">Texture2D::GatherCmpAlpha(S,float,float,int) function</span></span>

<span data-ttu-id="0ce91-106">Per quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce un confronto tra il relativo componente alfa e un valore di confronto.</span><span class="sxs-lookup"><span data-stu-id="0ce91-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their alpha component against a compare value.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ce91-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0ce91-107">Syntax</span></span>

``` syntax
float4 GatherCmpAlpha(
  in SamplerComparisonState s,
  in float2 location,
  in float compare_value,
  in int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="0ce91-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="0ce91-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ce91-109">*s* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0ce91-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ce91-110">Tipo: **SamplerComparisonState**</span><span class="sxs-lookup"><span data-stu-id="0ce91-110">Type: **SamplerComparisonState**</span></span>

<span data-ttu-id="0ce91-111">Indice del campionatore in base zero.</span><span class="sxs-lookup"><span data-stu-id="0ce91-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="0ce91-112">*posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0ce91-112">*location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ce91-113">Tipo: **float2**</span><span class="sxs-lookup"><span data-stu-id="0ce91-113">Type: **float2**</span></span>

<span data-ttu-id="0ce91-114">Coordinate di esempio (u, v).</span><span class="sxs-lookup"><span data-stu-id="0ce91-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="0ce91-115">*Confronta \_ valore* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0ce91-115">*compare\_value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ce91-116">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="0ce91-116">Type: **float**</span></span>

<span data-ttu-id="0ce91-117">Valore da confrontare con ogni valore campionato.</span><span class="sxs-lookup"><span data-stu-id="0ce91-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="0ce91-118">*offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0ce91-118">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ce91-119">Tipo: **int2**</span><span class="sxs-lookup"><span data-stu-id="0ce91-119">Type: **int2**</span></span>

<span data-ttu-id="0ce91-120">Offset applicato alla coordinata di trama prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="0ce91-120">An offset that is applied to the texture coordinate before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ce91-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0ce91-121">Return value</span></span>

<span data-ttu-id="0ce91-122">Tipo: **float4**</span><span class="sxs-lookup"><span data-stu-id="0ce91-122">Type: **float4**</span></span>

<span data-ttu-id="0ce91-123">Un valore a quattro componenti, ogni componente è il risultato di un confronto per ogni componente.</span><span class="sxs-lookup"><span data-stu-id="0ce91-123">A four-component value, each component is the result of a per-component comparison.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ce91-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="0ce91-124">Remarks</span></span>

<span data-ttu-id="0ce91-125">Gli esempi di trama possono essere usati per l'interpolazione bilineare.</span><span class="sxs-lookup"><span data-stu-id="0ce91-125">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="0ce91-126">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="0ce91-126">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="0ce91-127">Vertice</span><span class="sxs-lookup"><span data-stu-id="0ce91-127">Vertex</span></span> | <span data-ttu-id="0ce91-128">Hull</span><span class="sxs-lookup"><span data-stu-id="0ce91-128">Hull</span></span> | <span data-ttu-id="0ce91-129">Dominio</span><span class="sxs-lookup"><span data-stu-id="0ce91-129">Domain</span></span> | <span data-ttu-id="0ce91-130">Geometria</span><span class="sxs-lookup"><span data-stu-id="0ce91-130">Geometry</span></span> | <span data-ttu-id="0ce91-131">Pixel</span><span class="sxs-lookup"><span data-stu-id="0ce91-131">Pixel</span></span> | <span data-ttu-id="0ce91-132">Calcolo</span><span class="sxs-lookup"><span data-stu-id="0ce91-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="0ce91-133">x</span><span class="sxs-lookup"><span data-stu-id="0ce91-133">x</span></span>      | <span data-ttu-id="0ce91-134">x</span><span class="sxs-lookup"><span data-stu-id="0ce91-134">x</span></span>    | <span data-ttu-id="0ce91-135">x</span><span class="sxs-lookup"><span data-stu-id="0ce91-135">x</span></span>      | <span data-ttu-id="0ce91-136">x</span><span class="sxs-lookup"><span data-stu-id="0ce91-136">x</span></span>        | <span data-ttu-id="0ce91-137">x</span><span class="sxs-lookup"><span data-stu-id="0ce91-137">x</span></span>     | <span data-ttu-id="0ce91-138">x</span><span class="sxs-lookup"><span data-stu-id="0ce91-138">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="0ce91-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0ce91-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ce91-140">Metodi GatherCmpAlpha</span><span class="sxs-lookup"><span data-stu-id="0ce91-140">GatherCmpAlpha methods</span></span>](texture2d-gathercmpalpha.md)
</dt> <dt>

[<span data-ttu-id="0ce91-141">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="0ce91-141">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




