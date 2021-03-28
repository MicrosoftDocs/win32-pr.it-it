---
title: 'Funzione Texture2DArray:: GatherCmp (S, float, float, int, uint)'
description: "Per quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce il confronto rispetto a un valore di confronto con lo stato del mapping dei riquadri. | Funzione Texture2DArray:: GatherCmp (S, float, float, int, uint)"
ms.assetid: E68619B2-6AB0-4C57-9604-7759FD987446
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
ms.openlocfilehash: a9ac68e6f7701ddfccf0c58321a526f33c2ceeea
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981378"
---
# <a name="texture2darraygathercmpsfloatfloatintuint-function"></a><span data-ttu-id="90376-105">Funzione Texture2DArray:: GatherCmp (S, float, float, int, uint)</span><span class="sxs-lookup"><span data-stu-id="90376-105">Texture2DArray::GatherCmp(S,float,float,int,uint) function</span></span>

<span data-ttu-id="90376-106">Per quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce il confronto rispetto a un valore di confronto con lo stato del mapping dei riquadri.</span><span class="sxs-lookup"><span data-stu-id="90376-106">For four texel values that would be used in a bi-linear filtering operation, returns their comparison against a compare value along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="90376-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="90376-107">Syntax</span></span>


``` syntax
TemplateType GatherCmp(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  in  int          Offset,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="90376-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="90376-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90376-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="90376-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90376-110">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="90376-110">Type: **SamplerState**</span></span>

<span data-ttu-id="90376-111">Indice del campionatore in base zero.</span><span class="sxs-lookup"><span data-stu-id="90376-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="90376-112">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="90376-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90376-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="90376-113">Type: **float**</span></span>

<span data-ttu-id="90376-114">Coordinate di esempio (u, v).</span><span class="sxs-lookup"><span data-stu-id="90376-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="90376-115">*CompareValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="90376-115">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90376-116">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="90376-116">Type: **float**</span></span>

<span data-ttu-id="90376-117">Valore da confrontare con ogni valore campionato.</span><span class="sxs-lookup"><span data-stu-id="90376-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="90376-118">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="90376-118">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90376-119">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="90376-119">Type: **int**</span></span>

<span data-ttu-id="90376-120">Offset applicato alle coordinate di trama prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="90376-120">The offset applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="90376-121">*Stato* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="90376-121">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="90376-122">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="90376-122">Type: **uint**</span></span>

<span data-ttu-id="90376-123">Stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="90376-123">The status of the operation.</span></span> <span data-ttu-id="90376-124">Non è possibile accedere direttamente allo stato; passare invece lo stato alla funzione intrinseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="90376-124">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="90376-125">**CheckAccessFullyMapped** restituisce **true** se tutti i valori dell'operazione di **campionamento**, **raccolta** o **caricamento** corrispondente hanno eseguito l'accesso ai riquadri mappati in una [risorsa affiancata](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="90376-125">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="90376-126">Se sono stati ricavati valori da un riquadro non mappato, **CheckAccessFullyMapped** restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="90376-126">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90376-127">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="90376-127">Return value</span></span>

<span data-ttu-id="90376-128">Tipo: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="90376-128">Type: **TemplateType**</span></span>

<span data-ttu-id="90376-129">Valore a quattro componenti il cui tipo corrisponde al tipo di modello.</span><span class="sxs-lookup"><span data-stu-id="90376-129">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="90376-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="90376-130">Remarks</span></span>

<span data-ttu-id="90376-131">Gli esempi di trama possono essere usati per l'interpolazione bilineare.</span><span class="sxs-lookup"><span data-stu-id="90376-131">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="90376-132">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="90376-132">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="90376-133">Vertice</span><span class="sxs-lookup"><span data-stu-id="90376-133">Vertex</span></span> | <span data-ttu-id="90376-134">Hull</span><span class="sxs-lookup"><span data-stu-id="90376-134">Hull</span></span> | <span data-ttu-id="90376-135">Dominio</span><span class="sxs-lookup"><span data-stu-id="90376-135">Domain</span></span> | <span data-ttu-id="90376-136">Geometria</span><span class="sxs-lookup"><span data-stu-id="90376-136">Geometry</span></span> | <span data-ttu-id="90376-137">Pixel</span><span class="sxs-lookup"><span data-stu-id="90376-137">Pixel</span></span> | <span data-ttu-id="90376-138">Calcolo</span><span class="sxs-lookup"><span data-stu-id="90376-138">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="90376-139">x</span><span class="sxs-lookup"><span data-stu-id="90376-139">x</span></span>      | <span data-ttu-id="90376-140">x</span><span class="sxs-lookup"><span data-stu-id="90376-140">x</span></span>    | <span data-ttu-id="90376-141">x</span><span class="sxs-lookup"><span data-stu-id="90376-141">x</span></span>      | <span data-ttu-id="90376-142">x</span><span class="sxs-lookup"><span data-stu-id="90376-142">x</span></span>        | <span data-ttu-id="90376-143">x</span><span class="sxs-lookup"><span data-stu-id="90376-143">x</span></span>     | <span data-ttu-id="90376-144">x</span><span class="sxs-lookup"><span data-stu-id="90376-144">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="90376-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="90376-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90376-146">Metodi GatherCmp</span><span class="sxs-lookup"><span data-stu-id="90376-146">GatherCmp methods</span></span>](texture2darray-gathercmp.md)
</dt> </dl>

 

 
