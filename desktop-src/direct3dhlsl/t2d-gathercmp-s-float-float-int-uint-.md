---
title: 'Funzione Texture2D:: GatherCmp (S, float, float, int, uint)'
description: "Per quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce il confronto rispetto a un valore di confronto con lo stato del mapping dei riquadri. | Funzione Texture2D:: GatherCmp (S, float, float, int, uint)"
ms.assetid: A6610587-97C3-4CE5-86A7-3411D422BC8F
keywords:
- Funzione GatherCmp HLSL
topic_type:
- apiref
api_name:
- GatherCmp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: be8246053e0f7ba6357bdd68dc59059fd225bbc8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981871"
---
# <a name="texture2dgathercmpsfloatfloatintuint-function"></a><span data-ttu-id="14e5b-105">Funzione Texture2D:: GatherCmp (S, float, float, int, uint)</span><span class="sxs-lookup"><span data-stu-id="14e5b-105">Texture2D::GatherCmp(S,float,float,int,uint) function</span></span>

<span data-ttu-id="14e5b-106">Per quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce il confronto rispetto a un valore di confronto con lo stato del mapping dei riquadri.</span><span class="sxs-lookup"><span data-stu-id="14e5b-106">For four texel values that would be used in a bi-linear filtering operation, returns their comparison against a compare value along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="14e5b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="14e5b-107">Syntax</span></span>


``` syntax
TemplateType GatherCmp(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  in  int2         Offset,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="14e5b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="14e5b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14e5b-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="14e5b-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14e5b-110">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="14e5b-110">Type: **SamplerState**</span></span>

<span data-ttu-id="14e5b-111">Indice del campionatore in base zero.</span><span class="sxs-lookup"><span data-stu-id="14e5b-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="14e5b-112">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="14e5b-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14e5b-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="14e5b-113">Type: **float**</span></span>

<span data-ttu-id="14e5b-114">Coordinate di esempio (u, v).</span><span class="sxs-lookup"><span data-stu-id="14e5b-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="14e5b-115">*CompareValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="14e5b-115">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14e5b-116">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="14e5b-116">Type: **float**</span></span>

<span data-ttu-id="14e5b-117">Valore da confrontare con ogni valore campionato.</span><span class="sxs-lookup"><span data-stu-id="14e5b-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="14e5b-118">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="14e5b-118">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14e5b-119">Tipo: **int2**</span><span class="sxs-lookup"><span data-stu-id="14e5b-119">Type: **int2**</span></span>

<span data-ttu-id="14e5b-120">Offset in Texel applicato alle coordinate di trama prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="14e5b-120">The offset in texels applied to the texture coordinates before sampling.</span></span> <span data-ttu-id="14e5b-121">Deve essere un valore letterale.</span><span class="sxs-lookup"><span data-stu-id="14e5b-121">Must be a literal value.</span></span>

</dd> <dt>

<span data-ttu-id="14e5b-122">*Stato* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="14e5b-122">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="14e5b-123">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="14e5b-123">Type: **uint**</span></span>

<span data-ttu-id="14e5b-124">Stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="14e5b-124">The status of the operation.</span></span> <span data-ttu-id="14e5b-125">Non è possibile accedere direttamente allo stato; passare invece lo stato alla funzione intrinseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="14e5b-125">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="14e5b-126">**CheckAccessFullyMapped** restituisce **true** se tutti i valori dell'operazione di **campionamento**, **raccolta** o **caricamento** corrispondente hanno eseguito l'accesso ai riquadri mappati in una [risorsa affiancata](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="14e5b-126">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="14e5b-127">Se sono stati ricavati valori da un riquadro non mappato, **CheckAccessFullyMapped** restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="14e5b-127">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14e5b-128">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="14e5b-128">Return value</span></span>

<span data-ttu-id="14e5b-129">Tipo: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="14e5b-129">Type: **TemplateType**</span></span>

<span data-ttu-id="14e5b-130">Valore a quattro componenti il cui tipo corrisponde al tipo di modello.</span><span class="sxs-lookup"><span data-stu-id="14e5b-130">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="14e5b-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="14e5b-131">Remarks</span></span>

<span data-ttu-id="14e5b-132">Gli esempi di trama possono essere usati per l'interpolazione bilineare.</span><span class="sxs-lookup"><span data-stu-id="14e5b-132">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="14e5b-133">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="14e5b-133">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="14e5b-134">Vertice</span><span class="sxs-lookup"><span data-stu-id="14e5b-134">Vertex</span></span> | <span data-ttu-id="14e5b-135">Hull</span><span class="sxs-lookup"><span data-stu-id="14e5b-135">Hull</span></span> | <span data-ttu-id="14e5b-136">Dominio</span><span class="sxs-lookup"><span data-stu-id="14e5b-136">Domain</span></span> | <span data-ttu-id="14e5b-137">Geometria</span><span class="sxs-lookup"><span data-stu-id="14e5b-137">Geometry</span></span> | <span data-ttu-id="14e5b-138">Pixel</span><span class="sxs-lookup"><span data-stu-id="14e5b-138">Pixel</span></span> | <span data-ttu-id="14e5b-139">Calcolo</span><span class="sxs-lookup"><span data-stu-id="14e5b-139">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="14e5b-140">x</span><span class="sxs-lookup"><span data-stu-id="14e5b-140">x</span></span>      | <span data-ttu-id="14e5b-141">x</span><span class="sxs-lookup"><span data-stu-id="14e5b-141">x</span></span>    | <span data-ttu-id="14e5b-142">x</span><span class="sxs-lookup"><span data-stu-id="14e5b-142">x</span></span>      | <span data-ttu-id="14e5b-143">x</span><span class="sxs-lookup"><span data-stu-id="14e5b-143">x</span></span>        | <span data-ttu-id="14e5b-144">x</span><span class="sxs-lookup"><span data-stu-id="14e5b-144">x</span></span>     | <span data-ttu-id="14e5b-145">x</span><span class="sxs-lookup"><span data-stu-id="14e5b-145">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="14e5b-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="14e5b-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14e5b-147">Metodi GatherCmp</span><span class="sxs-lookup"><span data-stu-id="14e5b-147">GatherCmp methods</span></span>](texture2d-gathercmp.md)
</dt> </dl>

 

 
