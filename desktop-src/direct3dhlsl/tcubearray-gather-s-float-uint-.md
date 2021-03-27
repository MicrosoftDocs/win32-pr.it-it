---
title: 'Funzione TextureCubeArray:: Gather (S, float, uint)'
description: "Restituisce i quattro valori Texel che verrebbero usati in un'operazione di filtraggio bilineare, insieme allo stato del mapping dei riquadri. | Funzione TextureCubeArray:: Gather (S, float, uint)"
ms.assetid: B5C1843C-8DE4-4007-B619-2CC09B8A023B
keywords:
- Raccolta HLSL funzione
topic_type:
- apiref
api_name:
- Gather
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2b9c3f7be9189daa045f378f62856ddb68a2be89
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103886215"
---
# <a name="texturecubearraygathersfloatuint-function"></a><span data-ttu-id="f8934-105">Funzione TextureCubeArray:: Gather (S, float, uint)</span><span class="sxs-lookup"><span data-stu-id="f8934-105">TextureCubeArray::Gather(S,float,uint) function</span></span>

<span data-ttu-id="f8934-106">Restituisce i quattro valori Texel che verrebbero usati in un'operazione di filtraggio bilineare, insieme allo stato del mapping dei riquadri.</span><span class="sxs-lookup"><span data-stu-id="f8934-106">Returns the four texel values that would be used in a bi-linear filtering operation, along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8934-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f8934-107">Syntax</span></span>


``` syntax
TemplateType Gather(
  in  SamplerState S,
  in  float        Location,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="f8934-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f8934-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8934-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f8934-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8934-110">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="f8934-110">Type: **SamplerState**</span></span>

<span data-ttu-id="f8934-111">Indice del campionatore in base zero.</span><span class="sxs-lookup"><span data-stu-id="f8934-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="f8934-112">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f8934-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8934-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="f8934-113">Type: **float**</span></span>

<span data-ttu-id="f8934-114">Coordinate di esempio (u, v).</span><span class="sxs-lookup"><span data-stu-id="f8934-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="f8934-115">*Stato* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="f8934-115">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f8934-116">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="f8934-116">Type: **uint**</span></span>

<span data-ttu-id="f8934-117">Stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="f8934-117">The status of the operation.</span></span> <span data-ttu-id="f8934-118">Non è possibile accedere direttamente allo stato; passare invece lo stato alla funzione intrinseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="f8934-118">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="f8934-119">**CheckAccessFullyMapped** restituisce **true** se tutti i valori dell'operazione di **campionamento**, **raccolta** o **caricamento** corrispondente hanno eseguito l'accesso ai riquadri mappati in una [risorsa affiancata](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="f8934-119">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="f8934-120">Se sono stati ricavati valori da un riquadro non mappato, **CheckAccessFullyMapped** restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="f8934-120">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8934-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f8934-121">Return value</span></span>

<span data-ttu-id="f8934-122">Tipo: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="f8934-122">Type: **TemplateType**</span></span>

<span data-ttu-id="f8934-123">Valore a quattro componenti il cui tipo corrisponde al tipo di modello.</span><span class="sxs-lookup"><span data-stu-id="f8934-123">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8934-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="f8934-124">Remarks</span></span>

<span data-ttu-id="f8934-125">Gli esempi di trama possono essere usati per l'interpolazione bilineare.</span><span class="sxs-lookup"><span data-stu-id="f8934-125">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="f8934-126">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="f8934-126">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="f8934-127">Vertice</span><span class="sxs-lookup"><span data-stu-id="f8934-127">Vertex</span></span> | <span data-ttu-id="f8934-128">Hull</span><span class="sxs-lookup"><span data-stu-id="f8934-128">Hull</span></span> | <span data-ttu-id="f8934-129">Dominio</span><span class="sxs-lookup"><span data-stu-id="f8934-129">Domain</span></span> | <span data-ttu-id="f8934-130">Geometria</span><span class="sxs-lookup"><span data-stu-id="f8934-130">Geometry</span></span> | <span data-ttu-id="f8934-131">Pixel</span><span class="sxs-lookup"><span data-stu-id="f8934-131">Pixel</span></span> | <span data-ttu-id="f8934-132">Calcolo</span><span class="sxs-lookup"><span data-stu-id="f8934-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="f8934-133">x</span><span class="sxs-lookup"><span data-stu-id="f8934-133">x</span></span>      | <span data-ttu-id="f8934-134">x</span><span class="sxs-lookup"><span data-stu-id="f8934-134">x</span></span>    | <span data-ttu-id="f8934-135">x</span><span class="sxs-lookup"><span data-stu-id="f8934-135">x</span></span>      | <span data-ttu-id="f8934-136">x</span><span class="sxs-lookup"><span data-stu-id="f8934-136">x</span></span>        | <span data-ttu-id="f8934-137">x</span><span class="sxs-lookup"><span data-stu-id="f8934-137">x</span></span>     | <span data-ttu-id="f8934-138">x</span><span class="sxs-lookup"><span data-stu-id="f8934-138">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="f8934-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f8934-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8934-140">Metodi di raccolta</span><span class="sxs-lookup"><span data-stu-id="f8934-140">Gather methods</span></span>](texturecubearray-gather.md)
</dt> <dt>

[<span data-ttu-id="f8934-141">**TextureCubeArray**</span><span class="sxs-lookup"><span data-stu-id="f8934-141">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
