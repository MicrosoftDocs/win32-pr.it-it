---
title: 'Funzione Texture2DArray:: Gather (S, float, int)'
description: "Restituisce i quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare. | Funzione Texture2DArray:: Gather (S, float, int)"
ms.assetid: b0355158-01c8-45a1-bb5d-29a8c43b1685
keywords:
- Raccolta HLSL funzione
topic_type:
- apiref
api_name:
- Gather
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 46866df18a0836b311443a3dd411d74dfa7fb126
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995328"
---
# <a name="texture2darraygathersfloatint-function"></a><span data-ttu-id="f3841-105">Funzione Texture2DArray:: Gather (S, float, int)</span><span class="sxs-lookup"><span data-stu-id="f3841-105">Texture2DArray::Gather(S,float,int) function</span></span>

<span data-ttu-id="f3841-106">Restituisce i quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare.</span><span class="sxs-lookup"><span data-stu-id="f3841-106">Returns the four texel values that would be used in a bi-linear filtering operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3841-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f3841-107">Syntax</span></span>

``` syntax
TemplateType Gather(
  in sampler s,
  in float3 location,
  in int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="f3841-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f3841-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3841-109">*s* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f3841-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3841-110">Tipo: **Sampler**</span><span class="sxs-lookup"><span data-stu-id="f3841-110">Type: **sampler**</span></span>

<span data-ttu-id="f3841-111">Indice del campionatore in base zero.</span><span class="sxs-lookup"><span data-stu-id="f3841-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="f3841-112">*posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f3841-112">*location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3841-113">Tipo: **float3**</span><span class="sxs-lookup"><span data-stu-id="f3841-113">Type: **float3**</span></span>

<span data-ttu-id="f3841-114">Coordinate di esempio (u, v).</span><span class="sxs-lookup"><span data-stu-id="f3841-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="f3841-115">*offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f3841-115">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3841-116">Tipo: **int2**</span><span class="sxs-lookup"><span data-stu-id="f3841-116">Type: **int2**</span></span>

<span data-ttu-id="f3841-117">Offset applicato alle coordinate di trama prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="f3841-117">The offset applied to the texture coordinates before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3841-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f3841-118">Return value</span></span>

<span data-ttu-id="f3841-119">Tipo: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="f3841-119">Type: **TemplateType**</span></span>

<span data-ttu-id="f3841-120">Valore a quattro componenti il cui tipo corrisponde al tipo di modello.</span><span class="sxs-lookup"><span data-stu-id="f3841-120">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3841-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="f3841-121">Remarks</span></span>

<span data-ttu-id="f3841-122">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="f3841-122">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="f3841-123">Vertice</span><span class="sxs-lookup"><span data-stu-id="f3841-123">Vertex</span></span> | <span data-ttu-id="f3841-124">Hull</span><span class="sxs-lookup"><span data-stu-id="f3841-124">Hull</span></span> | <span data-ttu-id="f3841-125">Dominio</span><span class="sxs-lookup"><span data-stu-id="f3841-125">Domain</span></span> | <span data-ttu-id="f3841-126">Geometria</span><span class="sxs-lookup"><span data-stu-id="f3841-126">Geometry</span></span> | <span data-ttu-id="f3841-127">Pixel</span><span class="sxs-lookup"><span data-stu-id="f3841-127">Pixel</span></span> | <span data-ttu-id="f3841-128">Calcolo</span><span class="sxs-lookup"><span data-stu-id="f3841-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="f3841-129">x</span><span class="sxs-lookup"><span data-stu-id="f3841-129">x</span></span>      | <span data-ttu-id="f3841-130">x</span><span class="sxs-lookup"><span data-stu-id="f3841-130">x</span></span>    | <span data-ttu-id="f3841-131">x</span><span class="sxs-lookup"><span data-stu-id="f3841-131">x</span></span>      | <span data-ttu-id="f3841-132">x</span><span class="sxs-lookup"><span data-stu-id="f3841-132">x</span></span>        | <span data-ttu-id="f3841-133">x</span><span class="sxs-lookup"><span data-stu-id="f3841-133">x</span></span>     | <span data-ttu-id="f3841-134">x</span><span class="sxs-lookup"><span data-stu-id="f3841-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="f3841-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f3841-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3841-136">Metodi di raccolta</span><span class="sxs-lookup"><span data-stu-id="f3841-136">Gather methods</span></span>](texture2darray-gather.md)
</dt> <dt>

[<span data-ttu-id="f3841-137">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="f3841-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




