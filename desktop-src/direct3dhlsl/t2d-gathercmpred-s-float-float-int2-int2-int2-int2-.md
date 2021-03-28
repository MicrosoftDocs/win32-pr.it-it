---
title: 'Funzione Texture2D:: GatherCmpRed (S, float, float, int2, int2, int2, int2)'
description: "Per quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce un confronto tra il relativo componente rosso e un valore di confronto. | Funzione Texture2D:: GatherCmpRed (S, float, float, int2, int2, int2, int2)"
ms.assetid: B20A766E-0B4F-4FBA-A691-70ACE7BECF33
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
ms.openlocfilehash: f84467c798337ac2cc81283637636900933c9e41
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103969121"
---
# <a name="texture2dgathercmpredsfloatfloatint2int2int2int2-function"></a><span data-ttu-id="08704-105">Funzione Texture2D:: GatherCmpRed (S, float, float, int2, int2, int2, int2)</span><span class="sxs-lookup"><span data-stu-id="08704-105">Texture2D::GatherCmpRed(S,float,float,int2,int2,int2,int2) function</span></span>

<span data-ttu-id="08704-106">Per quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce un confronto tra il relativo componente rosso e un valore di confronto.</span><span class="sxs-lookup"><span data-stu-id="08704-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their red component against a compare value.</span></span>

## <a name="syntax"></a><span data-ttu-id="08704-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="08704-107">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="08704-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="08704-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08704-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="08704-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08704-110">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="08704-110">Type: **SamplerState**</span></span>

<span data-ttu-id="08704-111">Indice del campionatore in base zero.</span><span class="sxs-lookup"><span data-stu-id="08704-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="08704-112">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="08704-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08704-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="08704-113">Type: **float**</span></span>

<span data-ttu-id="08704-114">Coordinate di esempio (u, v).</span><span class="sxs-lookup"><span data-stu-id="08704-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="08704-115">*CompareValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="08704-115">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08704-116">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="08704-116">Type: **float**</span></span>

<span data-ttu-id="08704-117">Valore da confrontare con ogni valore campionato.</span><span class="sxs-lookup"><span data-stu-id="08704-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="08704-118">*Offset1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="08704-118">*Offset1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08704-119">Tipo: **int2**</span><span class="sxs-lookup"><span data-stu-id="08704-119">Type: **int2**</span></span>

<span data-ttu-id="08704-120">Primo componente di offset applicato alle coordinate di trama prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="08704-120">The first offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="08704-121">*Offset2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="08704-121">*Offset2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08704-122">Tipo: **int2**</span><span class="sxs-lookup"><span data-stu-id="08704-122">Type: **int2**</span></span>

<span data-ttu-id="08704-123">Secondo componente di offset applicato alle coordinate di trama prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="08704-123">The second offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="08704-124">*Offset3* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="08704-124">*Offset3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08704-125">Tipo: **int2**</span><span class="sxs-lookup"><span data-stu-id="08704-125">Type: **int2**</span></span>

<span data-ttu-id="08704-126">Terzo componente di offset applicato alle coordinate di trama prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="08704-126">The third offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="08704-127">*Offset4* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="08704-127">*Offset4* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08704-128">Tipo: **int2**</span><span class="sxs-lookup"><span data-stu-id="08704-128">Type: **int2**</span></span>

<span data-ttu-id="08704-129">Quarto componente di offset applicato alle coordinate di trama prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="08704-129">The fourth offset component applied to the texture coordinates before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08704-130">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="08704-130">Return value</span></span>

<span data-ttu-id="08704-131">Tipo: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="08704-131">Type: **TemplateType**</span></span>

<span data-ttu-id="08704-132">Valore a quattro componenti il cui tipo corrisponde al tipo di modello.</span><span class="sxs-lookup"><span data-stu-id="08704-132">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="08704-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="08704-133">Remarks</span></span>

<span data-ttu-id="08704-134">Gli esempi di trama possono essere usati per l'interpolazione bilineare.</span><span class="sxs-lookup"><span data-stu-id="08704-134">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="08704-135">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="08704-135">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="08704-136">Vertice</span><span class="sxs-lookup"><span data-stu-id="08704-136">Vertex</span></span> | <span data-ttu-id="08704-137">Hull</span><span class="sxs-lookup"><span data-stu-id="08704-137">Hull</span></span> | <span data-ttu-id="08704-138">Dominio</span><span class="sxs-lookup"><span data-stu-id="08704-138">Domain</span></span> | <span data-ttu-id="08704-139">Geometria</span><span class="sxs-lookup"><span data-stu-id="08704-139">Geometry</span></span> | <span data-ttu-id="08704-140">Pixel</span><span class="sxs-lookup"><span data-stu-id="08704-140">Pixel</span></span> | <span data-ttu-id="08704-141">Calcolo</span><span class="sxs-lookup"><span data-stu-id="08704-141">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="08704-142">x</span><span class="sxs-lookup"><span data-stu-id="08704-142">x</span></span>      | <span data-ttu-id="08704-143">x</span><span class="sxs-lookup"><span data-stu-id="08704-143">x</span></span>    | <span data-ttu-id="08704-144">x</span><span class="sxs-lookup"><span data-stu-id="08704-144">x</span></span>      | <span data-ttu-id="08704-145">x</span><span class="sxs-lookup"><span data-stu-id="08704-145">x</span></span>        | <span data-ttu-id="08704-146">x</span><span class="sxs-lookup"><span data-stu-id="08704-146">x</span></span>     | <span data-ttu-id="08704-147">x</span><span class="sxs-lookup"><span data-stu-id="08704-147">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="08704-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="08704-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08704-149">Metodi GatherCmpRed</span><span class="sxs-lookup"><span data-stu-id="08704-149">GatherCmpRed methods</span></span>](texture2d-gathercmpred.md)
</dt> </dl>

 

 




