---
title: 'Funzione Texture2DArray:: GatherAlpha (S, float, int2, int2, int2, int2)'
description: "Restituisce i componenti alfa dei quattro valori Texel che verrebbero usati in un'operazione di filtraggio bilineare. | Funzione Texture2DArray:: GatherAlpha (S, float, int2, int2, int2, int2)"
ms.assetid: A7F96B45-A097-437B-A0D0-18555FF76544
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
ms.openlocfilehash: ff6910152c9ac133c819456b9ec7aaeb2406b791
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103969084"
---
# <a name="texture2darraygatheralphasfloatint2int2int2int2-function"></a><span data-ttu-id="be59e-105">Funzione Texture2DArray:: GatherAlpha (S, float, int2, int2, int2, int2)</span><span class="sxs-lookup"><span data-stu-id="be59e-105">Texture2DArray::GatherAlpha(S,float,int2,int2,int2,int2) function</span></span>

<span data-ttu-id="be59e-106">Restituisce i componenti alfa dei quattro valori Texel che verrebbero usati in un'operazione di filtraggio bilineare.</span><span class="sxs-lookup"><span data-stu-id="be59e-106">Returns the alpha components of the four texel values that would be used in a bi-linear filtering operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="be59e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="be59e-107">Syntax</span></span>


``` syntax
TemplateType GatherAlpha(
  in SamplerState S,
  in float        Location,
  in int2         Offset1,
  in int2         Offset2,
  in int2         Offset3,
  in int2         Offset4
);
```



## <a name="parameters"></a><span data-ttu-id="be59e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="be59e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be59e-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="be59e-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be59e-110">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="be59e-110">Type: **SamplerState**</span></span>

<span data-ttu-id="be59e-111">Indice del campionatore in base zero.</span><span class="sxs-lookup"><span data-stu-id="be59e-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="be59e-112">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="be59e-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be59e-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="be59e-113">Type: **float**</span></span>

<span data-ttu-id="be59e-114">Coordinate di esempio (u, v).</span><span class="sxs-lookup"><span data-stu-id="be59e-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="be59e-115">*Offset1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="be59e-115">*Offset1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be59e-116">Tipo: **int2**</span><span class="sxs-lookup"><span data-stu-id="be59e-116">Type: **int2**</span></span>

<span data-ttu-id="be59e-117">Primo componente di offset applicato alle coordinate di trama prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="be59e-117">The first offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="be59e-118">*Offset2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="be59e-118">*Offset2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be59e-119">Tipo: **int2**</span><span class="sxs-lookup"><span data-stu-id="be59e-119">Type: **int2**</span></span>

<span data-ttu-id="be59e-120">Secondo componente di offset applicato alle coordinate di trama prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="be59e-120">The second offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="be59e-121">*Offset3* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="be59e-121">*Offset3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be59e-122">Tipo: **int2**</span><span class="sxs-lookup"><span data-stu-id="be59e-122">Type: **int2**</span></span>

<span data-ttu-id="be59e-123">Terzo componente di offset applicato alle coordinate di trama prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="be59e-123">The third offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="be59e-124">*Offset4* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="be59e-124">*Offset4* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be59e-125">Tipo: **int2**</span><span class="sxs-lookup"><span data-stu-id="be59e-125">Type: **int2**</span></span>

<span data-ttu-id="be59e-126">Quarto componente di offset applicato alle coordinate di trama prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="be59e-126">The fourth offset component applied to the texture coordinates before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be59e-127">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="be59e-127">Return value</span></span>

<span data-ttu-id="be59e-128">Tipo: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="be59e-128">Type: **TemplateType**</span></span>

<span data-ttu-id="be59e-129">Valore a quattro componenti il cui tipo corrisponde al tipo di modello.</span><span class="sxs-lookup"><span data-stu-id="be59e-129">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="be59e-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="be59e-130">Remarks</span></span>

<span data-ttu-id="be59e-131">Gli esempi di trama possono essere usati per l'interpolazione bilineare.</span><span class="sxs-lookup"><span data-stu-id="be59e-131">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="be59e-132">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="be59e-132">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="be59e-133">Vertice</span><span class="sxs-lookup"><span data-stu-id="be59e-133">Vertex</span></span> | <span data-ttu-id="be59e-134">Hull</span><span class="sxs-lookup"><span data-stu-id="be59e-134">Hull</span></span> | <span data-ttu-id="be59e-135">Dominio</span><span class="sxs-lookup"><span data-stu-id="be59e-135">Domain</span></span> | <span data-ttu-id="be59e-136">Geometria</span><span class="sxs-lookup"><span data-stu-id="be59e-136">Geometry</span></span> | <span data-ttu-id="be59e-137">Pixel</span><span class="sxs-lookup"><span data-stu-id="be59e-137">Pixel</span></span> | <span data-ttu-id="be59e-138">Calcolo</span><span class="sxs-lookup"><span data-stu-id="be59e-138">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="be59e-139">x</span><span class="sxs-lookup"><span data-stu-id="be59e-139">x</span></span>      | <span data-ttu-id="be59e-140">x</span><span class="sxs-lookup"><span data-stu-id="be59e-140">x</span></span>    | <span data-ttu-id="be59e-141">x</span><span class="sxs-lookup"><span data-stu-id="be59e-141">x</span></span>      | <span data-ttu-id="be59e-142">x</span><span class="sxs-lookup"><span data-stu-id="be59e-142">x</span></span>        | <span data-ttu-id="be59e-143">x</span><span class="sxs-lookup"><span data-stu-id="be59e-143">x</span></span>     | <span data-ttu-id="be59e-144">x</span><span class="sxs-lookup"><span data-stu-id="be59e-144">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="be59e-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="be59e-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be59e-146">Metodi GatherAlpha</span><span class="sxs-lookup"><span data-stu-id="be59e-146">GatherAlpha methods</span></span>](texture2darray-gatheralpha.md)
</dt> </dl>

 

 




