---
title: 'Funzione Texture2DArray:: GatherCmpRed (S, float, float, int2, int2, int2, int2)'
description: "Per quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce un confronto tra il relativo componente rosso e un valore di confronto. | Funzione Texture2DArray:: GatherCmpRed (S, float, float, int2, int2, int2, int2)"
ms.assetid: B436FB9A-C55C-477F-B8BE-933B1EB04AE1
keywords:
- Funzione GatherCmpRed HLSL
topic_type:
- apiref
api_name:
- GatherCmpRed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2d621bf26d097eeac17962fd14557f73f295a2e3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104058544"
---
# <a name="texture2darraygathercmpredsfloatfloatint2int2int2int2-function"></a><span data-ttu-id="207cf-105">Funzione Texture2DArray:: GatherCmpRed (S, float, float, int2, int2, int2, int2)</span><span class="sxs-lookup"><span data-stu-id="207cf-105">Texture2DArray::GatherCmpRed(S,float,float,int2,int2,int2,int2) function</span></span>

<span data-ttu-id="207cf-106">Per quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce un confronto tra il relativo componente rosso e un valore di confronto.</span><span class="sxs-lookup"><span data-stu-id="207cf-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their red component against a compare value.</span></span>

## <a name="syntax"></a><span data-ttu-id="207cf-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="207cf-107">Syntax</span></span>


``` syntax
TemplateType GatherCmpRed(
  in SamplerState S,
  in float        Location,
  in float        CompareValue,
  in int2         Offset1,
  in int2         Offset2,
  in int2         Offset3,
  in int2         Offset4
);
```



## <a name="parameters"></a><span data-ttu-id="207cf-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="207cf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="207cf-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="207cf-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="207cf-110">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="207cf-110">Type: **SamplerState**</span></span>

<span data-ttu-id="207cf-111">Indice del campionatore in base zero.</span><span class="sxs-lookup"><span data-stu-id="207cf-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="207cf-112">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="207cf-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="207cf-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="207cf-113">Type: **float**</span></span>

<span data-ttu-id="207cf-114">Coordinate di esempio (u, v).</span><span class="sxs-lookup"><span data-stu-id="207cf-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="207cf-115">*CompareValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="207cf-115">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="207cf-116">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="207cf-116">Type: **float**</span></span>

<span data-ttu-id="207cf-117">Valore da confrontare con ogni valore campionato.</span><span class="sxs-lookup"><span data-stu-id="207cf-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="207cf-118">*Offset1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="207cf-118">*Offset1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="207cf-119">Tipo: **int2**</span><span class="sxs-lookup"><span data-stu-id="207cf-119">Type: **int2**</span></span>

<span data-ttu-id="207cf-120">Primo componente di offset applicato alle coordinate di trama prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="207cf-120">The first offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="207cf-121">*Offset2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="207cf-121">*Offset2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="207cf-122">Tipo: **int2**</span><span class="sxs-lookup"><span data-stu-id="207cf-122">Type: **int2**</span></span>

<span data-ttu-id="207cf-123">Secondo componente di offset applicato alle coordinate di trama prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="207cf-123">The second offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="207cf-124">*Offset3* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="207cf-124">*Offset3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="207cf-125">Tipo: **int2**</span><span class="sxs-lookup"><span data-stu-id="207cf-125">Type: **int2**</span></span>

<span data-ttu-id="207cf-126">Terzo componente di offset applicato alle coordinate di trama prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="207cf-126">The third offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="207cf-127">*Offset4* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="207cf-127">*Offset4* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="207cf-128">Tipo: **int2**</span><span class="sxs-lookup"><span data-stu-id="207cf-128">Type: **int2**</span></span>

<span data-ttu-id="207cf-129">Quarto componente di offset applicato alle coordinate di trama prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="207cf-129">The fourth offset component applied to the texture coordinates before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="207cf-130">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="207cf-130">Return value</span></span>

<span data-ttu-id="207cf-131">Tipo: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="207cf-131">Type: **TemplateType**</span></span>

<span data-ttu-id="207cf-132">Valore a quattro componenti il cui tipo corrisponde al tipo di modello.</span><span class="sxs-lookup"><span data-stu-id="207cf-132">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="207cf-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="207cf-133">Remarks</span></span>

<span data-ttu-id="207cf-134">Gli esempi di trama possono essere usati per l'interpolazione bilineare.</span><span class="sxs-lookup"><span data-stu-id="207cf-134">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="207cf-135">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="207cf-135">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="207cf-136">Vertice</span><span class="sxs-lookup"><span data-stu-id="207cf-136">Vertex</span></span> | <span data-ttu-id="207cf-137">Hull</span><span class="sxs-lookup"><span data-stu-id="207cf-137">Hull</span></span> | <span data-ttu-id="207cf-138">Dominio</span><span class="sxs-lookup"><span data-stu-id="207cf-138">Domain</span></span> | <span data-ttu-id="207cf-139">Geometria</span><span class="sxs-lookup"><span data-stu-id="207cf-139">Geometry</span></span> | <span data-ttu-id="207cf-140">Pixel</span><span class="sxs-lookup"><span data-stu-id="207cf-140">Pixel</span></span> | <span data-ttu-id="207cf-141">Calcolo</span><span class="sxs-lookup"><span data-stu-id="207cf-141">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="207cf-142">x</span><span class="sxs-lookup"><span data-stu-id="207cf-142">x</span></span>      | <span data-ttu-id="207cf-143">x</span><span class="sxs-lookup"><span data-stu-id="207cf-143">x</span></span>    | <span data-ttu-id="207cf-144">x</span><span class="sxs-lookup"><span data-stu-id="207cf-144">x</span></span>      | <span data-ttu-id="207cf-145">x</span><span class="sxs-lookup"><span data-stu-id="207cf-145">x</span></span>        | <span data-ttu-id="207cf-146">x</span><span class="sxs-lookup"><span data-stu-id="207cf-146">x</span></span>     | <span data-ttu-id="207cf-147">x</span><span class="sxs-lookup"><span data-stu-id="207cf-147">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="207cf-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="207cf-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="207cf-149">Metodi GatherCmpRed</span><span class="sxs-lookup"><span data-stu-id="207cf-149">GatherCmpRed methods</span></span>](texture2darray-gathercmpred.md)
</dt> </dl>

 

 




