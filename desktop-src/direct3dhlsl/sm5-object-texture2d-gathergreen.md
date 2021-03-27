---
title: 'Funzione Texture2D:: GatherGreen (S, float, int)'
description: "Per quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce un confronto tra il relativo componente verde e un valore di confronto. | Funzione Texture2D:: GatherGreen (S, float, int)"
ms.assetid: 97e1fb52-75f4-4e73-93f1-98b7a5925efc
keywords:
- Funzione GatherGreen HLSL
topic_type:
- apiref
api_name:
- GatherGreen
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 722d7a3ac90fa3083b8f42f7704f5c9e0aeb1829
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995557"
---
# <a name="texture2dgathergreensfloatint-function"></a><span data-ttu-id="33242-105">Funzione Texture2D:: GatherGreen (S, float, int)</span><span class="sxs-lookup"><span data-stu-id="33242-105">Texture2D::GatherGreen(S,float,int) function</span></span>

<span data-ttu-id="33242-106">Per quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce un confronto tra il relativo componente verde e un valore di confronto.</span><span class="sxs-lookup"><span data-stu-id="33242-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their green component against a compare value.</span></span>

## <a name="syntax"></a><span data-ttu-id="33242-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="33242-107">Syntax</span></span>

``` syntax
TemplateType GatherGreen(
  in sampler s,
  in float2 location,
  in int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="33242-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="33242-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33242-109">*s* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="33242-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33242-110">Tipo: **Sampler**</span><span class="sxs-lookup"><span data-stu-id="33242-110">Type: **sampler**</span></span>

<span data-ttu-id="33242-111">Indice del campionatore in base zero.</span><span class="sxs-lookup"><span data-stu-id="33242-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="33242-112">*posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="33242-112">*location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33242-113">Tipo: **float2**</span><span class="sxs-lookup"><span data-stu-id="33242-113">Type: **float2**</span></span>

<span data-ttu-id="33242-114">Coordinate di esempio (u, v).</span><span class="sxs-lookup"><span data-stu-id="33242-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="33242-115">*offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="33242-115">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33242-116">Tipo: **int2**</span><span class="sxs-lookup"><span data-stu-id="33242-116">Type: **int2**</span></span>

<span data-ttu-id="33242-117">Offset applicato alla coordinata di trama prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="33242-117">An offset that is applied to the texture coordinate before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33242-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="33242-118">Return value</span></span>

<span data-ttu-id="33242-119">Tipo: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="33242-119">Type: **TemplateType**</span></span>

<span data-ttu-id="33242-120">Valore a quattro componenti il cui tipo corrisponde al tipo di modello.</span><span class="sxs-lookup"><span data-stu-id="33242-120">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="33242-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="33242-121">Remarks</span></span>

<span data-ttu-id="33242-122">Gli esempi di trama possono essere usati per l'interpolazione bilineare.</span><span class="sxs-lookup"><span data-stu-id="33242-122">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="33242-123">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="33242-123">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="33242-124">Vertice</span><span class="sxs-lookup"><span data-stu-id="33242-124">Vertex</span></span> | <span data-ttu-id="33242-125">Hull</span><span class="sxs-lookup"><span data-stu-id="33242-125">Hull</span></span> | <span data-ttu-id="33242-126">Dominio</span><span class="sxs-lookup"><span data-stu-id="33242-126">Domain</span></span> | <span data-ttu-id="33242-127">Geometria</span><span class="sxs-lookup"><span data-stu-id="33242-127">Geometry</span></span> | <span data-ttu-id="33242-128">Pixel</span><span class="sxs-lookup"><span data-stu-id="33242-128">Pixel</span></span> | <span data-ttu-id="33242-129">Calcolo</span><span class="sxs-lookup"><span data-stu-id="33242-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="33242-130">x</span><span class="sxs-lookup"><span data-stu-id="33242-130">x</span></span>      | <span data-ttu-id="33242-131">x</span><span class="sxs-lookup"><span data-stu-id="33242-131">x</span></span>    | <span data-ttu-id="33242-132">x</span><span class="sxs-lookup"><span data-stu-id="33242-132">x</span></span>      | <span data-ttu-id="33242-133">x</span><span class="sxs-lookup"><span data-stu-id="33242-133">x</span></span>        | <span data-ttu-id="33242-134">x</span><span class="sxs-lookup"><span data-stu-id="33242-134">x</span></span>     | <span data-ttu-id="33242-135">x</span><span class="sxs-lookup"><span data-stu-id="33242-135">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="33242-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="33242-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33242-137">Metodi GatherGreen</span><span class="sxs-lookup"><span data-stu-id="33242-137">GatherGreen methods</span></span>](texture2d-gathergreen.md)
</dt> <dt>

[<span data-ttu-id="33242-138">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="33242-138">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




