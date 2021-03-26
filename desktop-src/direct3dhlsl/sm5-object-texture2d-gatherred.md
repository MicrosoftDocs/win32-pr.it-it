---
title: 'Funzione Texture2D:: GatherRed (S, float, int)'
description: "Per quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce un confronto tra il relativo componente rosso e un valore di confronto. | Funzione Texture2D:: GatherRed (S, float, int)"
ms.assetid: 6d2d1556-d52f-4625-93ca-34da399f9a8b
keywords:
- Funzione GatherRed HLSL
topic_type:
- apiref
api_name:
- GatherRed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f05196063f6a17cc34865157c17a92bc2bb116bf
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981706"
---
# <a name="texture2dgatherredsfloatint-function"></a><span data-ttu-id="b2d0a-105">Funzione Texture2D:: GatherRed (S, float, int)</span><span class="sxs-lookup"><span data-stu-id="b2d0a-105">Texture2D::GatherRed(S,float,int) function</span></span>

<span data-ttu-id="b2d0a-106">Per quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce un confronto tra il relativo componente rosso e un valore di confronto.</span><span class="sxs-lookup"><span data-stu-id="b2d0a-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their red component against a compare value.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2d0a-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b2d0a-107">Syntax</span></span>

``` syntax
TemplateType GatherRed(
  in sampler s,
  in float2 location,
  in int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="b2d0a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b2d0a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2d0a-109">*s* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b2d0a-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2d0a-110">Tipo: **Sampler**</span><span class="sxs-lookup"><span data-stu-id="b2d0a-110">Type: **sampler**</span></span>

<span data-ttu-id="b2d0a-111">Indice del campionatore in base zero.</span><span class="sxs-lookup"><span data-stu-id="b2d0a-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="b2d0a-112">*posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b2d0a-112">*location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2d0a-113">Tipo: **float2**</span><span class="sxs-lookup"><span data-stu-id="b2d0a-113">Type: **float2**</span></span>

<span data-ttu-id="b2d0a-114">Coordinate di esempio (u, v).</span><span class="sxs-lookup"><span data-stu-id="b2d0a-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="b2d0a-115">*offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b2d0a-115">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2d0a-116">Tipo: **int2**</span><span class="sxs-lookup"><span data-stu-id="b2d0a-116">Type: **int2**</span></span>

<span data-ttu-id="b2d0a-117">Offset applicato alla coordinata di trama prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="b2d0a-117">An offset that is applied to the texture coordinate before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2d0a-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b2d0a-118">Return value</span></span>

<span data-ttu-id="b2d0a-119">Tipo: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="b2d0a-119">Type: **TemplateType**</span></span>

<span data-ttu-id="b2d0a-120">Valore a quattro componenti il cui tipo corrisponde al tipo di modello.</span><span class="sxs-lookup"><span data-stu-id="b2d0a-120">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2d0a-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="b2d0a-121">Remarks</span></span>

<span data-ttu-id="b2d0a-122">Gli esempi di trama possono essere usati per l'interpolazione bilineare.</span><span class="sxs-lookup"><span data-stu-id="b2d0a-122">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="b2d0a-123">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="b2d0a-123">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="b2d0a-124">Vertice</span><span class="sxs-lookup"><span data-stu-id="b2d0a-124">Vertex</span></span> | <span data-ttu-id="b2d0a-125">Hull</span><span class="sxs-lookup"><span data-stu-id="b2d0a-125">Hull</span></span> | <span data-ttu-id="b2d0a-126">Dominio</span><span class="sxs-lookup"><span data-stu-id="b2d0a-126">Domain</span></span> | <span data-ttu-id="b2d0a-127">Geometria</span><span class="sxs-lookup"><span data-stu-id="b2d0a-127">Geometry</span></span> | <span data-ttu-id="b2d0a-128">Pixel</span><span class="sxs-lookup"><span data-stu-id="b2d0a-128">Pixel</span></span> | <span data-ttu-id="b2d0a-129">Calcolo</span><span class="sxs-lookup"><span data-stu-id="b2d0a-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="b2d0a-130">x</span><span class="sxs-lookup"><span data-stu-id="b2d0a-130">x</span></span>      | <span data-ttu-id="b2d0a-131">x</span><span class="sxs-lookup"><span data-stu-id="b2d0a-131">x</span></span>    | <span data-ttu-id="b2d0a-132">x</span><span class="sxs-lookup"><span data-stu-id="b2d0a-132">x</span></span>      | <span data-ttu-id="b2d0a-133">x</span><span class="sxs-lookup"><span data-stu-id="b2d0a-133">x</span></span>        | <span data-ttu-id="b2d0a-134">x</span><span class="sxs-lookup"><span data-stu-id="b2d0a-134">x</span></span>     | <span data-ttu-id="b2d0a-135">x</span><span class="sxs-lookup"><span data-stu-id="b2d0a-135">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="b2d0a-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b2d0a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2d0a-137">Metodi GatherRed</span><span class="sxs-lookup"><span data-stu-id="b2d0a-137">GatherRed methods</span></span>](texture2d-gatherred.md)
</dt> <dt>

[<span data-ttu-id="b2d0a-138">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="b2d0a-138">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




