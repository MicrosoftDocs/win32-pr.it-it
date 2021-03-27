---
title: 'Funzione Texture2D:: Gather (S, float, int)'
description: "Restituisce i quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare. | Funzione Texture2D:: Gather (S, float, int)"
ms.assetid: 5d196c1c-8cc9-4add-9d33-654294314ee2
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
ms.openlocfilehash: 4d0a58be0580572441f91a3b3f637601d70cd9c8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103761759"
---
# <a name="texture2dgathersfloatint-function"></a><span data-ttu-id="4cad5-105">Funzione Texture2D:: Gather (S, float, int)</span><span class="sxs-lookup"><span data-stu-id="4cad5-105">Texture2D::Gather(S,float,int) function</span></span>

<span data-ttu-id="4cad5-106">Restituisce i quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare.</span><span class="sxs-lookup"><span data-stu-id="4cad5-106">Returns the four texel values that would be used in a bi-linear filtering operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cad5-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4cad5-107">Syntax</span></span>

``` syntax
TemplateType Gather(
  in sampler s,
  in float2 location,
  in int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="4cad5-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="4cad5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cad5-109">*s* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4cad5-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cad5-110">Tipo: **Sampler**</span><span class="sxs-lookup"><span data-stu-id="4cad5-110">Type: **sampler**</span></span>

<span data-ttu-id="4cad5-111">Indice del campionatore in base zero.</span><span class="sxs-lookup"><span data-stu-id="4cad5-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="4cad5-112">*posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4cad5-112">*location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cad5-113">Tipo: **float2**</span><span class="sxs-lookup"><span data-stu-id="4cad5-113">Type: **float2**</span></span>

<span data-ttu-id="4cad5-114">Coordinate di esempio (u, v).</span><span class="sxs-lookup"><span data-stu-id="4cad5-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="4cad5-115">*offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4cad5-115">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cad5-116">Tipo: **int2**</span><span class="sxs-lookup"><span data-stu-id="4cad5-116">Type: **int2**</span></span>

<span data-ttu-id="4cad5-117">Offset applicato alle coordinate di trama prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="4cad5-117">The offset applied to the texture coordinates before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4cad5-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4cad5-118">Return value</span></span>

<span data-ttu-id="4cad5-119">Tipo: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="4cad5-119">Type: **TemplateType**</span></span>

<span data-ttu-id="4cad5-120">Valore a quattro componenti il cui tipo corrisponde al tipo di modello.</span><span class="sxs-lookup"><span data-stu-id="4cad5-120">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="4cad5-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="4cad5-121">Remarks</span></span>

<span data-ttu-id="4cad5-122">Gli esempi di trama possono essere usati per l'interpolazione bilineare.</span><span class="sxs-lookup"><span data-stu-id="4cad5-122">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="4cad5-123">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="4cad5-123">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="4cad5-124">Vertice</span><span class="sxs-lookup"><span data-stu-id="4cad5-124">Vertex</span></span> | <span data-ttu-id="4cad5-125">Hull</span><span class="sxs-lookup"><span data-stu-id="4cad5-125">Hull</span></span> | <span data-ttu-id="4cad5-126">Dominio</span><span class="sxs-lookup"><span data-stu-id="4cad5-126">Domain</span></span> | <span data-ttu-id="4cad5-127">Geometria</span><span class="sxs-lookup"><span data-stu-id="4cad5-127">Geometry</span></span> | <span data-ttu-id="4cad5-128">Pixel</span><span class="sxs-lookup"><span data-stu-id="4cad5-128">Pixel</span></span> | <span data-ttu-id="4cad5-129">Calcolo</span><span class="sxs-lookup"><span data-stu-id="4cad5-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="4cad5-130">x</span><span class="sxs-lookup"><span data-stu-id="4cad5-130">x</span></span>      | <span data-ttu-id="4cad5-131">x</span><span class="sxs-lookup"><span data-stu-id="4cad5-131">x</span></span>    | <span data-ttu-id="4cad5-132">x</span><span class="sxs-lookup"><span data-stu-id="4cad5-132">x</span></span>      | <span data-ttu-id="4cad5-133">x</span><span class="sxs-lookup"><span data-stu-id="4cad5-133">x</span></span>        | <span data-ttu-id="4cad5-134">x</span><span class="sxs-lookup"><span data-stu-id="4cad5-134">x</span></span>     | <span data-ttu-id="4cad5-135">x</span><span class="sxs-lookup"><span data-stu-id="4cad5-135">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="4cad5-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4cad5-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cad5-137">Metodi di raccolta</span><span class="sxs-lookup"><span data-stu-id="4cad5-137">Gather methods</span></span>](texture2d-gather.md)
</dt> <dt>

[<span data-ttu-id="4cad5-138">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="4cad5-138">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




