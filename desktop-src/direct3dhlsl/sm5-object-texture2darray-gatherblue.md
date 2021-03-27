---
title: 'Funzione Texture2DArray:: GatherBlue (S, float, int)'
description: "Restituisce i componenti blu dei quattro valori Texel che verrebbero usati in un'operazione di filtraggio bilineare. | Funzione Texture2DArray:: GatherBlue (S, float, int)"
ms.assetid: f81596b5-afd1-4baf-b6c0-ca4661a3ef22
keywords:
- Funzione GatherBlue HLSL
topic_type:
- apiref
api_name:
- GatherBlue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1844b898deca767b04aba438f4784a54a5afa112
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995408"
---
# <a name="texture2darraygatherbluesfloatint-function"></a><span data-ttu-id="ab01e-105">Funzione Texture2DArray:: GatherBlue (S, float, int)</span><span class="sxs-lookup"><span data-stu-id="ab01e-105">Texture2DArray::GatherBlue(S,float,int) function</span></span>

<span data-ttu-id="ab01e-106">Restituisce i componenti blu dei quattro valori Texel che verrebbero usati in un'operazione di filtraggio bilineare.</span><span class="sxs-lookup"><span data-stu-id="ab01e-106">Returns the blue components of the four texel values that would be used in a bi-linear filtering operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab01e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ab01e-107">Syntax</span></span>

``` syntax
TemplateType GatherBlue(
  in sampler s,
  in float3 location,
  in int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="ab01e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ab01e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab01e-109">*s* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ab01e-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab01e-110">Tipo: **Sampler**</span><span class="sxs-lookup"><span data-stu-id="ab01e-110">Type: **sampler**</span></span>

<span data-ttu-id="ab01e-111">Indice del campionatore in base zero.</span><span class="sxs-lookup"><span data-stu-id="ab01e-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="ab01e-112">*posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ab01e-112">*location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab01e-113">Tipo: **float3**</span><span class="sxs-lookup"><span data-stu-id="ab01e-113">Type: **float3**</span></span>

<span data-ttu-id="ab01e-114">Coordinate di esempio (u, v).</span><span class="sxs-lookup"><span data-stu-id="ab01e-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="ab01e-115">*offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ab01e-115">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab01e-116">Tipo: **int2**</span><span class="sxs-lookup"><span data-stu-id="ab01e-116">Type: **int2**</span></span>

<span data-ttu-id="ab01e-117">Offset applicato alla coordinata di trama prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="ab01e-117">An offset that is applied to the texture coordinate before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab01e-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ab01e-118">Return value</span></span>

<span data-ttu-id="ab01e-119">Tipo: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="ab01e-119">Type: **TemplateType**</span></span>

<span data-ttu-id="ab01e-120">Valore a quattro componenti il cui tipo corrisponde al tipo di modello.</span><span class="sxs-lookup"><span data-stu-id="ab01e-120">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab01e-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="ab01e-121">Remarks</span></span>

<span data-ttu-id="ab01e-122">Gli esempi di trama possono essere usati per l'interpolazione bilineare.</span><span class="sxs-lookup"><span data-stu-id="ab01e-122">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="ab01e-123">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="ab01e-123">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="ab01e-124">Vertice</span><span class="sxs-lookup"><span data-stu-id="ab01e-124">Vertex</span></span> | <span data-ttu-id="ab01e-125">Hull</span><span class="sxs-lookup"><span data-stu-id="ab01e-125">Hull</span></span> | <span data-ttu-id="ab01e-126">Dominio</span><span class="sxs-lookup"><span data-stu-id="ab01e-126">Domain</span></span> | <span data-ttu-id="ab01e-127">Geometria</span><span class="sxs-lookup"><span data-stu-id="ab01e-127">Geometry</span></span> | <span data-ttu-id="ab01e-128">Pixel</span><span class="sxs-lookup"><span data-stu-id="ab01e-128">Pixel</span></span> | <span data-ttu-id="ab01e-129">Calcolo</span><span class="sxs-lookup"><span data-stu-id="ab01e-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="ab01e-130">x</span><span class="sxs-lookup"><span data-stu-id="ab01e-130">x</span></span>      | <span data-ttu-id="ab01e-131">x</span><span class="sxs-lookup"><span data-stu-id="ab01e-131">x</span></span>    | <span data-ttu-id="ab01e-132">x</span><span class="sxs-lookup"><span data-stu-id="ab01e-132">x</span></span>      | <span data-ttu-id="ab01e-133">x</span><span class="sxs-lookup"><span data-stu-id="ab01e-133">x</span></span>        | <span data-ttu-id="ab01e-134">x</span><span class="sxs-lookup"><span data-stu-id="ab01e-134">x</span></span>     | <span data-ttu-id="ab01e-135">x</span><span class="sxs-lookup"><span data-stu-id="ab01e-135">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="ab01e-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ab01e-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab01e-137">Metodi GatherBlue</span><span class="sxs-lookup"><span data-stu-id="ab01e-137">GatherBlue methods</span></span>](texture2darray-gatherblue.md)
</dt> <dt>

[<span data-ttu-id="ab01e-138">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="ab01e-138">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




