---
title: 'Funzione TextureCubeArray:: GatherCmpBlue (S, float, float, uint)'
description: "Per quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce un confronto tra il relativo componente blu e un valore di confronto con lo stato del mapping dei riquadri. | Funzione TextureCubeArray:: GatherCmpBlue (S, float, float, uint)"
ms.assetid: 81F82EB1-D662-4A18-856F-26AE5C1A41C6
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
ms.openlocfilehash: 9de8d578706cd0799bd2132f05b8a31b7daa8afe
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104234720"
---
# <a name="texturecubearraygathercmpbluesfloatfloatuint-function"></a><span data-ttu-id="da081-105">Funzione TextureCubeArray:: GatherCmpBlue (S, float, float, uint)</span><span class="sxs-lookup"><span data-stu-id="da081-105">TextureCubeArray::GatherCmpBlue(S,float,float,uint) function</span></span>

<span data-ttu-id="da081-106">Per quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce un confronto tra il relativo componente blu e un valore di confronto con lo stato del mapping dei riquadri.</span><span class="sxs-lookup"><span data-stu-id="da081-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their blue component against a compare value along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="da081-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="da081-107">Syntax</span></span>


``` syntax
TemplateType GatherCmpBlue(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="da081-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="da081-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da081-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="da081-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da081-110">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="da081-110">Type: **SamplerState**</span></span>

<span data-ttu-id="da081-111">Indice del campionatore in base zero.</span><span class="sxs-lookup"><span data-stu-id="da081-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="da081-112">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="da081-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da081-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="da081-113">Type: **float**</span></span>

<span data-ttu-id="da081-114">Coordinate di esempio (u, v).</span><span class="sxs-lookup"><span data-stu-id="da081-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="da081-115">*CompareValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="da081-115">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da081-116">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="da081-116">Type: **float**</span></span>

<span data-ttu-id="da081-117">Valore da confrontare con ogni valore campionato.</span><span class="sxs-lookup"><span data-stu-id="da081-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="da081-118">*Stato* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="da081-118">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="da081-119">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="da081-119">Type: **uint**</span></span>

<span data-ttu-id="da081-120">Stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="da081-120">The status of the operation.</span></span> <span data-ttu-id="da081-121">Non è possibile accedere direttamente allo stato; passare invece lo stato alla funzione intrinseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="da081-121">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="da081-122">**CheckAccessFullyMapped** restituisce **true** se tutti i valori dell'operazione di **campionamento**, **raccolta** o **caricamento** corrispondente hanno eseguito l'accesso ai riquadri mappati in una [risorsa affiancata](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="da081-122">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="da081-123">Se sono stati ricavati valori da un riquadro non mappato, **CheckAccessFullyMapped** restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="da081-123">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da081-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="da081-124">Return value</span></span>

<span data-ttu-id="da081-125">Tipo: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="da081-125">Type: **TemplateType**</span></span>

<span data-ttu-id="da081-126">Valore a quattro componenti il cui tipo corrisponde al tipo di modello.</span><span class="sxs-lookup"><span data-stu-id="da081-126">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="da081-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="da081-127">Remarks</span></span>

<span data-ttu-id="da081-128">Gli esempi di trama possono essere usati per l'interpolazione bilineare.</span><span class="sxs-lookup"><span data-stu-id="da081-128">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="da081-129">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="da081-129">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="da081-130">Vertice</span><span class="sxs-lookup"><span data-stu-id="da081-130">Vertex</span></span> | <span data-ttu-id="da081-131">Hull</span><span class="sxs-lookup"><span data-stu-id="da081-131">Hull</span></span> | <span data-ttu-id="da081-132">Dominio</span><span class="sxs-lookup"><span data-stu-id="da081-132">Domain</span></span> | <span data-ttu-id="da081-133">Geometria</span><span class="sxs-lookup"><span data-stu-id="da081-133">Geometry</span></span> | <span data-ttu-id="da081-134">Pixel</span><span class="sxs-lookup"><span data-stu-id="da081-134">Pixel</span></span> | <span data-ttu-id="da081-135">Calcolo</span><span class="sxs-lookup"><span data-stu-id="da081-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="da081-136">x</span><span class="sxs-lookup"><span data-stu-id="da081-136">x</span></span>      | <span data-ttu-id="da081-137">x</span><span class="sxs-lookup"><span data-stu-id="da081-137">x</span></span>    | <span data-ttu-id="da081-138">x</span><span class="sxs-lookup"><span data-stu-id="da081-138">x</span></span>      | <span data-ttu-id="da081-139">x</span><span class="sxs-lookup"><span data-stu-id="da081-139">x</span></span>        | <span data-ttu-id="da081-140">x</span><span class="sxs-lookup"><span data-stu-id="da081-140">x</span></span>     | <span data-ttu-id="da081-141">x</span><span class="sxs-lookup"><span data-stu-id="da081-141">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="da081-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="da081-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da081-143">Metodi GatherCmpBlue</span><span class="sxs-lookup"><span data-stu-id="da081-143">GatherCmpBlue methods</span></span>](texturecubearray-gathercmpblue.md)
</dt> <dt>

[<span data-ttu-id="da081-144">**TextureCubeArray**</span><span class="sxs-lookup"><span data-stu-id="da081-144">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
