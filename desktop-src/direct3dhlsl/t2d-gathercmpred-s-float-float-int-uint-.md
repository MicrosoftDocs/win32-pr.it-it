---
title: 'Funzione Texture2D:: GatherCmpRed (S, float, float, int, uint)'
description: "Per quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce un confronto tra il relativo componente rosso e un valore di confronto insieme allo stato del mapping dei riquadri. | Funzione Texture2D:: GatherCmpRed (S, float, float, int, uint)"
ms.assetid: 0FE5AB82-3FC1-46CF-AE9A-4B0B25385973
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
ms.openlocfilehash: c0956b999104929cde9ea126e683e7db4ba2b7c5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981983"
---
# <a name="texture2dgathercmpredsfloatfloatintuint-function"></a><span data-ttu-id="2aab8-105">Funzione Texture2D:: GatherCmpRed (S, float, float, int, uint)</span><span class="sxs-lookup"><span data-stu-id="2aab8-105">Texture2D::GatherCmpRed(S,float,float,int,uint) function</span></span>

<span data-ttu-id="2aab8-106">Per quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce un confronto tra il relativo componente rosso e un valore di confronto insieme allo stato del mapping dei riquadri.</span><span class="sxs-lookup"><span data-stu-id="2aab8-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their red component against a compare value along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="2aab8-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2aab8-107">Syntax</span></span>


``` syntax
TemplateType GatherCmpRed(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  in  int          Offset,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="2aab8-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="2aab8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2aab8-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2aab8-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2aab8-110">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="2aab8-110">Type: **SamplerState**</span></span>

<span data-ttu-id="2aab8-111">Indice del campionatore in base zero.</span><span class="sxs-lookup"><span data-stu-id="2aab8-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="2aab8-112">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2aab8-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2aab8-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="2aab8-113">Type: **float**</span></span>

<span data-ttu-id="2aab8-114">Coordinate di esempio (u, v).</span><span class="sxs-lookup"><span data-stu-id="2aab8-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="2aab8-115">*CompareValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2aab8-115">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2aab8-116">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="2aab8-116">Type: **float**</span></span>

<span data-ttu-id="2aab8-117">Valore da confrontare con ogni valore campionato.</span><span class="sxs-lookup"><span data-stu-id="2aab8-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="2aab8-118">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2aab8-118">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2aab8-119">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="2aab8-119">Type: **int**</span></span>

<span data-ttu-id="2aab8-120">Offset applicato alle coordinate di trama prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="2aab8-120">The offset applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="2aab8-121">*Stato* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="2aab8-121">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2aab8-122">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="2aab8-122">Type: **uint**</span></span>

<span data-ttu-id="2aab8-123">Stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="2aab8-123">The status of the operation.</span></span> <span data-ttu-id="2aab8-124">Non è possibile accedere direttamente allo stato; passare invece lo stato alla funzione intrinseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="2aab8-124">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="2aab8-125">**CheckAccessFullyMapped** restituisce **true** se tutti i valori dell'operazione di **campionamento**, **raccolta** o **caricamento** corrispondente hanno eseguito l'accesso ai riquadri mappati in una [risorsa affiancata](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="2aab8-125">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="2aab8-126">Se sono stati ricavati valori da un riquadro non mappato, **CheckAccessFullyMapped** restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="2aab8-126">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2aab8-127">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2aab8-127">Return value</span></span>

<span data-ttu-id="2aab8-128">Tipo: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="2aab8-128">Type: **TemplateType**</span></span>

<span data-ttu-id="2aab8-129">Valore a quattro componenti il cui tipo corrisponde al tipo di modello.</span><span class="sxs-lookup"><span data-stu-id="2aab8-129">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="2aab8-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="2aab8-130">Remarks</span></span>

<span data-ttu-id="2aab8-131">Gli esempi di trama possono essere usati per l'interpolazione bilineare.</span><span class="sxs-lookup"><span data-stu-id="2aab8-131">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="2aab8-132">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="2aab8-132">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="2aab8-133">Vertice</span><span class="sxs-lookup"><span data-stu-id="2aab8-133">Vertex</span></span> | <span data-ttu-id="2aab8-134">Hull</span><span class="sxs-lookup"><span data-stu-id="2aab8-134">Hull</span></span> | <span data-ttu-id="2aab8-135">Dominio</span><span class="sxs-lookup"><span data-stu-id="2aab8-135">Domain</span></span> | <span data-ttu-id="2aab8-136">Geometria</span><span class="sxs-lookup"><span data-stu-id="2aab8-136">Geometry</span></span> | <span data-ttu-id="2aab8-137">Pixel</span><span class="sxs-lookup"><span data-stu-id="2aab8-137">Pixel</span></span> | <span data-ttu-id="2aab8-138">Calcolo</span><span class="sxs-lookup"><span data-stu-id="2aab8-138">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="2aab8-139">x</span><span class="sxs-lookup"><span data-stu-id="2aab8-139">x</span></span>      | <span data-ttu-id="2aab8-140">x</span><span class="sxs-lookup"><span data-stu-id="2aab8-140">x</span></span>    | <span data-ttu-id="2aab8-141">x</span><span class="sxs-lookup"><span data-stu-id="2aab8-141">x</span></span>      | <span data-ttu-id="2aab8-142">x</span><span class="sxs-lookup"><span data-stu-id="2aab8-142">x</span></span>        | <span data-ttu-id="2aab8-143">x</span><span class="sxs-lookup"><span data-stu-id="2aab8-143">x</span></span>     | <span data-ttu-id="2aab8-144">x</span><span class="sxs-lookup"><span data-stu-id="2aab8-144">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="2aab8-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2aab8-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2aab8-146">Metodi GatherCmpRed</span><span class="sxs-lookup"><span data-stu-id="2aab8-146">GatherCmpRed methods</span></span>](texture2d-gathercmpred.md)
</dt> </dl>

 

 
