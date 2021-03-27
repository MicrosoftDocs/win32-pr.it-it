---
title: 'Funzione Texture2DArray:: GatherAlpha (S, float, int)'
description: "Restituisce i componenti alfa dei quattro valori Texel che verrebbero usati in un'operazione di filtraggio bilineare. | Funzione Texture2DArray:: GatherAlpha (S, float, int)"
ms.assetid: d7270277-53c1-4034-bf66-9a95bc1b51e4
keywords:
- Funzione GatherAlpha HLSL
topic_type:
- apiref
api_name:
- GatherAlpha
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2052b780ab628a6a5bc174729119a9c2c8b8c8f4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352826"
---
# <a name="texture2darraygatheralphasfloatint-function"></a><span data-ttu-id="38a07-105">Funzione Texture2DArray:: GatherAlpha (S, float, int)</span><span class="sxs-lookup"><span data-stu-id="38a07-105">Texture2DArray::GatherAlpha(S,float,int) function</span></span>

<span data-ttu-id="38a07-106">Restituisce i componenti alfa dei quattro valori Texel che verrebbero usati in un'operazione di filtraggio bilineare.</span><span class="sxs-lookup"><span data-stu-id="38a07-106">Returns the alpha components of the four texel values that would be used in a bi-linear filtering operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="38a07-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="38a07-107">Syntax</span></span>

``` syntax
TemplateType GatherAlpha(
  in sampler s,
  in float3 location,
  in int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="38a07-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="38a07-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38a07-109">*s* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="38a07-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38a07-110">Tipo: **Sampler**</span><span class="sxs-lookup"><span data-stu-id="38a07-110">Type: **sampler**</span></span>

<span data-ttu-id="38a07-111">Indice del campionatore in base zero.</span><span class="sxs-lookup"><span data-stu-id="38a07-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="38a07-112">*posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="38a07-112">*location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38a07-113">Tipo: **float3**</span><span class="sxs-lookup"><span data-stu-id="38a07-113">Type: **float3**</span></span>

<span data-ttu-id="38a07-114">Coordinate di esempio (u, v).</span><span class="sxs-lookup"><span data-stu-id="38a07-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="38a07-115">*offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="38a07-115">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38a07-116">Tipo: **int2**</span><span class="sxs-lookup"><span data-stu-id="38a07-116">Type: **int2**</span></span>

<span data-ttu-id="38a07-117">Offset applicato alla coordinata di trama prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="38a07-117">An offset that is applied to the texture coordinate before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38a07-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="38a07-118">Return value</span></span>

<span data-ttu-id="38a07-119">Tipo: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="38a07-119">Type: **TemplateType**</span></span>

<span data-ttu-id="38a07-120">Valore a quattro componenti il cui tipo corrisponde al tipo di modello.</span><span class="sxs-lookup"><span data-stu-id="38a07-120">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="38a07-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="38a07-121">Remarks</span></span>

<span data-ttu-id="38a07-122">Gli esempi di trama possono essere usati per l'interpolazione bilineare.</span><span class="sxs-lookup"><span data-stu-id="38a07-122">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="38a07-123">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="38a07-123">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="38a07-124">Vertice</span><span class="sxs-lookup"><span data-stu-id="38a07-124">Vertex</span></span> | <span data-ttu-id="38a07-125">Hull</span><span class="sxs-lookup"><span data-stu-id="38a07-125">Hull</span></span> | <span data-ttu-id="38a07-126">Dominio</span><span class="sxs-lookup"><span data-stu-id="38a07-126">Domain</span></span> | <span data-ttu-id="38a07-127">Geometria</span><span class="sxs-lookup"><span data-stu-id="38a07-127">Geometry</span></span> | <span data-ttu-id="38a07-128">Pixel</span><span class="sxs-lookup"><span data-stu-id="38a07-128">Pixel</span></span> | <span data-ttu-id="38a07-129">Calcolo</span><span class="sxs-lookup"><span data-stu-id="38a07-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="38a07-130">x</span><span class="sxs-lookup"><span data-stu-id="38a07-130">x</span></span>      | <span data-ttu-id="38a07-131">x</span><span class="sxs-lookup"><span data-stu-id="38a07-131">x</span></span>    | <span data-ttu-id="38a07-132">x</span><span class="sxs-lookup"><span data-stu-id="38a07-132">x</span></span>      | <span data-ttu-id="38a07-133">x</span><span class="sxs-lookup"><span data-stu-id="38a07-133">x</span></span>        | <span data-ttu-id="38a07-134">x</span><span class="sxs-lookup"><span data-stu-id="38a07-134">x</span></span>     | <span data-ttu-id="38a07-135">x</span><span class="sxs-lookup"><span data-stu-id="38a07-135">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="38a07-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="38a07-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38a07-137">Metodi GatherAlpha</span><span class="sxs-lookup"><span data-stu-id="38a07-137">GatherAlpha methods</span></span>](texture2darray-gatheralpha.md)
</dt> <dt>

[<span data-ttu-id="38a07-138">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="38a07-138">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




