---
title: 'Funzione TextureCube:: Gather (S, float, uint)'
description: "Restituisce i quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare. | Funzione TextureCube:: Gather (S, float, uint)"
ms.assetid: 23FA8135-ECF0-4CAE-9A1C-B05DA3676453
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
ms.openlocfilehash: e9710343ff9b09e4425bc133db6dab4d118d807e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981183"
---
# <a name="texturecubegathersfloatuint-function"></a><span data-ttu-id="19fb7-105">Funzione TextureCube:: Gather (S, float, uint)</span><span class="sxs-lookup"><span data-stu-id="19fb7-105">TextureCube::Gather(S,float,uint) function</span></span>

<span data-ttu-id="19fb7-106">Restituisce i quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare.</span><span class="sxs-lookup"><span data-stu-id="19fb7-106">Returns the four texel values that would be used in a bi-linear filtering operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="19fb7-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="19fb7-107">Syntax</span></span>


``` syntax
TemplateType Gather(
  in  SamplerState S,
  in  float        Location,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="19fb7-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="19fb7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19fb7-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="19fb7-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19fb7-110">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="19fb7-110">Type: **SamplerState**</span></span>

<span data-ttu-id="19fb7-111">Indice del campionatore in base zero.</span><span class="sxs-lookup"><span data-stu-id="19fb7-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="19fb7-112">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="19fb7-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19fb7-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="19fb7-113">Type: **float**</span></span>

<span data-ttu-id="19fb7-114">Coordinate di esempio (u, v).</span><span class="sxs-lookup"><span data-stu-id="19fb7-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="19fb7-115">*Stato* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="19fb7-115">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="19fb7-116">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="19fb7-116">Type: **uint**</span></span>

<span data-ttu-id="19fb7-117">Stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="19fb7-117">The status of the operation.</span></span> <span data-ttu-id="19fb7-118">Non è possibile accedere direttamente allo stato; passare invece lo stato alla funzione intrinseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="19fb7-118">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="19fb7-119">**CheckAccessFullyMapped** restituisce **true** se tutti i valori dell'operazione di **campionamento**, **raccolta** o **caricamento** corrispondente hanno eseguito l'accesso ai riquadri mappati in una [risorsa affiancata](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="19fb7-119">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="19fb7-120">Se sono stati ricavati valori da un riquadro non mappato, **CheckAccessFullyMapped** restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="19fb7-120">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19fb7-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="19fb7-121">Return value</span></span>

<span data-ttu-id="19fb7-122">Tipo: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="19fb7-122">Type: **TemplateType**</span></span>

<span data-ttu-id="19fb7-123">Valore a quattro componenti il cui tipo corrisponde al tipo di modello.</span><span class="sxs-lookup"><span data-stu-id="19fb7-123">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="19fb7-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="19fb7-124">Remarks</span></span>

<span data-ttu-id="19fb7-125">Gli esempi di trama possono essere usati per l'interpolazione bilineare.</span><span class="sxs-lookup"><span data-stu-id="19fb7-125">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="19fb7-126">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="19fb7-126">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="19fb7-127">Vertice</span><span class="sxs-lookup"><span data-stu-id="19fb7-127">Vertex</span></span> | <span data-ttu-id="19fb7-128">Hull</span><span class="sxs-lookup"><span data-stu-id="19fb7-128">Hull</span></span> | <span data-ttu-id="19fb7-129">Dominio</span><span class="sxs-lookup"><span data-stu-id="19fb7-129">Domain</span></span> | <span data-ttu-id="19fb7-130">Geometria</span><span class="sxs-lookup"><span data-stu-id="19fb7-130">Geometry</span></span> | <span data-ttu-id="19fb7-131">Pixel</span><span class="sxs-lookup"><span data-stu-id="19fb7-131">Pixel</span></span> | <span data-ttu-id="19fb7-132">Calcolo</span><span class="sxs-lookup"><span data-stu-id="19fb7-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="19fb7-133">x</span><span class="sxs-lookup"><span data-stu-id="19fb7-133">x</span></span>      | <span data-ttu-id="19fb7-134">x</span><span class="sxs-lookup"><span data-stu-id="19fb7-134">x</span></span>    | <span data-ttu-id="19fb7-135">x</span><span class="sxs-lookup"><span data-stu-id="19fb7-135">x</span></span>      | <span data-ttu-id="19fb7-136">x</span><span class="sxs-lookup"><span data-stu-id="19fb7-136">x</span></span>        | <span data-ttu-id="19fb7-137">x</span><span class="sxs-lookup"><span data-stu-id="19fb7-137">x</span></span>     | <span data-ttu-id="19fb7-138">x</span><span class="sxs-lookup"><span data-stu-id="19fb7-138">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="19fb7-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="19fb7-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19fb7-140">Metodi di raccolta</span><span class="sxs-lookup"><span data-stu-id="19fb7-140">Gather methods</span></span>](texturecube-gather.md)
</dt> <dt>

[<span data-ttu-id="19fb7-141">**TextureCube**</span><span class="sxs-lookup"><span data-stu-id="19fb7-141">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
