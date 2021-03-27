---
title: 'Funzione TextureCube:: GatherCmp (S, float, float, uint)'
description: "Per quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce il confronto rispetto a un valore di confronto. | Funzione TextureCube:: GatherCmp (S, float, float, uint)"
ms.assetid: 655F4851-708A-478B-BB31-9DC8CDD480D0
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
ms.openlocfilehash: 827132338c3ba2b858a329ec108ef37b36ed54c2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981847"
---
# <a name="texturecubegathercmpsfloatfloatuint-function"></a><span data-ttu-id="202c6-105">Funzione TextureCube:: GatherCmp (S, float, float, uint)</span><span class="sxs-lookup"><span data-stu-id="202c6-105">TextureCube::GatherCmp(S,float,float,uint) function</span></span>

<span data-ttu-id="202c6-106">Per quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce il confronto rispetto a un valore di confronto.</span><span class="sxs-lookup"><span data-stu-id="202c6-106">For four texel values that would be used in a bi-linear filtering operation, returns their comparison against a compare value.</span></span>

## <a name="syntax"></a><span data-ttu-id="202c6-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="202c6-107">Syntax</span></span>


``` syntax
TemplateType GatherCmp(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="202c6-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="202c6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="202c6-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="202c6-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="202c6-110">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="202c6-110">Type: **SamplerState**</span></span>

<span data-ttu-id="202c6-111">Indice del campionatore in base zero.</span><span class="sxs-lookup"><span data-stu-id="202c6-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="202c6-112">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="202c6-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="202c6-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="202c6-113">Type: **float**</span></span>

<span data-ttu-id="202c6-114">Coordinate di esempio (u, v).</span><span class="sxs-lookup"><span data-stu-id="202c6-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="202c6-115">*CompareValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="202c6-115">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="202c6-116">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="202c6-116">Type: **float**</span></span>

<span data-ttu-id="202c6-117">Valore da confrontare con ogni valore campionato.</span><span class="sxs-lookup"><span data-stu-id="202c6-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="202c6-118">*Stato* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="202c6-118">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="202c6-119">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="202c6-119">Type: **uint**</span></span>

<span data-ttu-id="202c6-120">Stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="202c6-120">The status of the operation.</span></span> <span data-ttu-id="202c6-121">Non è possibile accedere direttamente allo stato; passare invece lo stato alla funzione intrinseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="202c6-121">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="202c6-122">**CheckAccessFullyMapped** restituisce **true** se tutti i valori dell'operazione di **campionamento**, **raccolta** o **caricamento** corrispondente hanno eseguito l'accesso ai riquadri mappati in una [risorsa affiancata](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="202c6-122">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="202c6-123">Se sono stati ricavati valori da un riquadro non mappato, **CheckAccessFullyMapped** restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="202c6-123">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="202c6-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="202c6-124">Return value</span></span>

<span data-ttu-id="202c6-125">Tipo: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="202c6-125">Type: **TemplateType**</span></span>

<span data-ttu-id="202c6-126">Valore a quattro componenti il cui tipo corrisponde al tipo di modello.</span><span class="sxs-lookup"><span data-stu-id="202c6-126">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="202c6-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="202c6-127">Remarks</span></span>

<span data-ttu-id="202c6-128">Gli esempi di trama possono essere usati per l'interpolazione bilineare.</span><span class="sxs-lookup"><span data-stu-id="202c6-128">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="202c6-129">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="202c6-129">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="202c6-130">Vertice</span><span class="sxs-lookup"><span data-stu-id="202c6-130">Vertex</span></span> | <span data-ttu-id="202c6-131">Hull</span><span class="sxs-lookup"><span data-stu-id="202c6-131">Hull</span></span> | <span data-ttu-id="202c6-132">Dominio</span><span class="sxs-lookup"><span data-stu-id="202c6-132">Domain</span></span> | <span data-ttu-id="202c6-133">Geometria</span><span class="sxs-lookup"><span data-stu-id="202c6-133">Geometry</span></span> | <span data-ttu-id="202c6-134">Pixel</span><span class="sxs-lookup"><span data-stu-id="202c6-134">Pixel</span></span> | <span data-ttu-id="202c6-135">Calcolo</span><span class="sxs-lookup"><span data-stu-id="202c6-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="202c6-136">x</span><span class="sxs-lookup"><span data-stu-id="202c6-136">x</span></span>      | <span data-ttu-id="202c6-137">x</span><span class="sxs-lookup"><span data-stu-id="202c6-137">x</span></span>    | <span data-ttu-id="202c6-138">x</span><span class="sxs-lookup"><span data-stu-id="202c6-138">x</span></span>      | <span data-ttu-id="202c6-139">x</span><span class="sxs-lookup"><span data-stu-id="202c6-139">x</span></span>        | <span data-ttu-id="202c6-140">x</span><span class="sxs-lookup"><span data-stu-id="202c6-140">x</span></span>     | <span data-ttu-id="202c6-141">x</span><span class="sxs-lookup"><span data-stu-id="202c6-141">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="202c6-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="202c6-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="202c6-143">Metodi GatherCmp</span><span class="sxs-lookup"><span data-stu-id="202c6-143">GatherCmp methods</span></span>](texturecube-gathercmp.md)
</dt> <dt>

[<span data-ttu-id="202c6-144">**TextureCube**</span><span class="sxs-lookup"><span data-stu-id="202c6-144">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
