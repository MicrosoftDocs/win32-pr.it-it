---
title: 'Funzione Texture2D:: GatherCmpBlue (S, float, float, int2, int2, int2, int2)'
description: "Per quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce un confronto tra il relativo componente blu e un valore di confronto. | Funzione Texture2D:: GatherCmpBlue (S, float, float, int2, int2, int2, int2)"
ms.assetid: DAA41BF3-6037-404F-9B35-C5F1302367B9
keywords:
- Funzione GatherCmpBlue HLSL
topic_type:
- apiref
api_name:
- GatherCmpBlue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d66364dd1c07d692c87a9e3a05501a56a587cb3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104982046"
---
# <a name="texture2dgathercmpbluesfloatfloatint2int2int2int2-function"></a><span data-ttu-id="7ba55-105">Funzione Texture2D:: GatherCmpBlue (S, float, float, int2, int2, int2, int2)</span><span class="sxs-lookup"><span data-stu-id="7ba55-105">Texture2D::GatherCmpBlue(S,float,float,int2,int2,int2,int2) function</span></span>

<span data-ttu-id="7ba55-106">Per quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce un confronto tra il relativo componente blu e un valore di confronto.</span><span class="sxs-lookup"><span data-stu-id="7ba55-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their blue component against a compare value.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ba55-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7ba55-107">Syntax</span></span>


``` syntax
TemplateType GatherCmpBlue(
  in SamplerState S,
  in float        Location,
  in float        CompareValue,
  in int2         Offset1,
  in int2         Offset2,
  in int2         Offset3,
  in int2         Offset4
);
```



## <a name="parameters"></a><span data-ttu-id="7ba55-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7ba55-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ba55-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7ba55-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ba55-110">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="7ba55-110">Type: **SamplerState**</span></span>

<span data-ttu-id="7ba55-111">Indice del campionatore in base zero.</span><span class="sxs-lookup"><span data-stu-id="7ba55-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="7ba55-112">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7ba55-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ba55-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="7ba55-113">Type: **float**</span></span>

<span data-ttu-id="7ba55-114">Coordinate di esempio (u, v).</span><span class="sxs-lookup"><span data-stu-id="7ba55-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="7ba55-115">*CompareValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7ba55-115">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ba55-116">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="7ba55-116">Type: **float**</span></span>

<span data-ttu-id="7ba55-117">Valore da confrontare con ogni valore campionato.</span><span class="sxs-lookup"><span data-stu-id="7ba55-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="7ba55-118">*Offset1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7ba55-118">*Offset1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ba55-119">Tipo: **int2**</span><span class="sxs-lookup"><span data-stu-id="7ba55-119">Type: **int2**</span></span>

<span data-ttu-id="7ba55-120">Primo componente di offset applicato alle coordinate di trama prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="7ba55-120">The first offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="7ba55-121">*Offset2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7ba55-121">*Offset2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ba55-122">Tipo: **int2**</span><span class="sxs-lookup"><span data-stu-id="7ba55-122">Type: **int2**</span></span>

<span data-ttu-id="7ba55-123">Secondo componente di offset applicato alle coordinate di trama prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="7ba55-123">The second offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="7ba55-124">*Offset3* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7ba55-124">*Offset3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ba55-125">Tipo: **int2**</span><span class="sxs-lookup"><span data-stu-id="7ba55-125">Type: **int2**</span></span>

<span data-ttu-id="7ba55-126">Terzo componente di offset applicato alle coordinate di trama prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="7ba55-126">The third offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="7ba55-127">*Offset4* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7ba55-127">*Offset4* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ba55-128">Tipo: **int2**</span><span class="sxs-lookup"><span data-stu-id="7ba55-128">Type: **int2**</span></span>

<span data-ttu-id="7ba55-129">Quarto componente di offset applicato alle coordinate di trama prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="7ba55-129">The fourth offset component applied to the texture coordinates before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ba55-130">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7ba55-130">Return value</span></span>

<span data-ttu-id="7ba55-131">Tipo: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="7ba55-131">Type: **TemplateType**</span></span>

<span data-ttu-id="7ba55-132">Valore a quattro componenti il cui tipo corrisponde al tipo di modello.</span><span class="sxs-lookup"><span data-stu-id="7ba55-132">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ba55-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="7ba55-133">Remarks</span></span>

<span data-ttu-id="7ba55-134">Gli esempi di trama possono essere usati per l'interpolazione bilineare.</span><span class="sxs-lookup"><span data-stu-id="7ba55-134">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="7ba55-135">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="7ba55-135">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="7ba55-136">Vertice</span><span class="sxs-lookup"><span data-stu-id="7ba55-136">Vertex</span></span> | <span data-ttu-id="7ba55-137">Hull</span><span class="sxs-lookup"><span data-stu-id="7ba55-137">Hull</span></span> | <span data-ttu-id="7ba55-138">Dominio</span><span class="sxs-lookup"><span data-stu-id="7ba55-138">Domain</span></span> | <span data-ttu-id="7ba55-139">Geometria</span><span class="sxs-lookup"><span data-stu-id="7ba55-139">Geometry</span></span> | <span data-ttu-id="7ba55-140">Pixel</span><span class="sxs-lookup"><span data-stu-id="7ba55-140">Pixel</span></span> | <span data-ttu-id="7ba55-141">Calcolo</span><span class="sxs-lookup"><span data-stu-id="7ba55-141">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="7ba55-142">x</span><span class="sxs-lookup"><span data-stu-id="7ba55-142">x</span></span>      | <span data-ttu-id="7ba55-143">x</span><span class="sxs-lookup"><span data-stu-id="7ba55-143">x</span></span>    | <span data-ttu-id="7ba55-144">x</span><span class="sxs-lookup"><span data-stu-id="7ba55-144">x</span></span>      | <span data-ttu-id="7ba55-145">x</span><span class="sxs-lookup"><span data-stu-id="7ba55-145">x</span></span>        | <span data-ttu-id="7ba55-146">x</span><span class="sxs-lookup"><span data-stu-id="7ba55-146">x</span></span>     | <span data-ttu-id="7ba55-147">x</span><span class="sxs-lookup"><span data-stu-id="7ba55-147">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="7ba55-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7ba55-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ba55-149">Metodi GatherCmpBlue</span><span class="sxs-lookup"><span data-stu-id="7ba55-149">GatherCmpBlue methods</span></span>](texture2d-gathercmpblue.md)
</dt> </dl>

 

 




