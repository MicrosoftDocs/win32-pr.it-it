---
title: 'Funzione Texture2DArray:: GatherGreen (S, float, int, uint)'
description: "Restituisce i componenti verdi dei quattro valori Texel che verrebbero usati in un'operazione di filtraggio bilineare, insieme allo stato di mapping dei riquadri. | Funzione Texture2DArray:: GatherGreen (S, float, int, uint)"
ms.assetid: 90BEB8B3-F851-469B-B55A-E51CB8463CC8
keywords:
- Funzione GatherGreen HLSL
topic_type:
- apiref
api_name:
- GatherGreen
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3f34470e589ac2d8155124d51813213869bbdfd6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981951"
---
# <a name="texture2darraygathergreensfloatintuint-function"></a><span data-ttu-id="9b4a1-105">Funzione Texture2DArray:: GatherGreen (S, float, int, uint)</span><span class="sxs-lookup"><span data-stu-id="9b4a1-105">Texture2DArray::GatherGreen(S,float,int,uint) function</span></span>

<span data-ttu-id="9b4a1-106">Restituisce i componenti verdi dei quattro valori Texel che verrebbero usati in un'operazione di filtraggio bilineare, insieme allo stato di mapping dei riquadri.</span><span class="sxs-lookup"><span data-stu-id="9b4a1-106">Returns the green components of the four texel values that would be used in a bi-linear filtering operation, along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b4a1-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9b4a1-107">Syntax</span></span>


``` syntax
TemplateType GatherGreen(
  in  SamplerState S,
  in  float        Location,
  in  int          Offset,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="9b4a1-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="9b4a1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b4a1-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9b4a1-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b4a1-110">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="9b4a1-110">Type: **SamplerState**</span></span>

<span data-ttu-id="9b4a1-111">Indice del campionatore in base zero.</span><span class="sxs-lookup"><span data-stu-id="9b4a1-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="9b4a1-112">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9b4a1-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b4a1-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="9b4a1-113">Type: **float**</span></span>

<span data-ttu-id="9b4a1-114">Coordinate di esempio (u, v).</span><span class="sxs-lookup"><span data-stu-id="9b4a1-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="9b4a1-115">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9b4a1-115">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b4a1-116">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="9b4a1-116">Type: **int**</span></span>

<span data-ttu-id="9b4a1-117">Offset applicato alle coordinate di trama prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="9b4a1-117">The offset applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="9b4a1-118">*Stato* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="9b4a1-118">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9b4a1-119">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="9b4a1-119">Type: **uint**</span></span>

<span data-ttu-id="9b4a1-120">Stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="9b4a1-120">The status of the operation.</span></span> <span data-ttu-id="9b4a1-121">Non è possibile accedere direttamente allo stato; passare invece lo stato alla funzione intrinseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="9b4a1-121">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="9b4a1-122">**CheckAccessFullyMapped** restituisce **true** se tutti i valori dell'operazione di **campionamento**, **raccolta** o **caricamento** corrispondente hanno eseguito l'accesso ai riquadri mappati in una [risorsa affiancata](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="9b4a1-122">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="9b4a1-123">Se sono stati ricavati valori da un riquadro non mappato, **CheckAccessFullyMapped** restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="9b4a1-123">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b4a1-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9b4a1-124">Return value</span></span>

<span data-ttu-id="9b4a1-125">Tipo: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="9b4a1-125">Type: **TemplateType**</span></span>

<span data-ttu-id="9b4a1-126">Valore a quattro componenti il cui tipo corrisponde al tipo di modello.</span><span class="sxs-lookup"><span data-stu-id="9b4a1-126">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b4a1-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="9b4a1-127">Remarks</span></span>

<span data-ttu-id="9b4a1-128">Gli esempi di trama possono essere usati per l'interpolazione bilineare.</span><span class="sxs-lookup"><span data-stu-id="9b4a1-128">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="9b4a1-129">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="9b4a1-129">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="9b4a1-130">Vertice</span><span class="sxs-lookup"><span data-stu-id="9b4a1-130">Vertex</span></span> | <span data-ttu-id="9b4a1-131">Hull</span><span class="sxs-lookup"><span data-stu-id="9b4a1-131">Hull</span></span> | <span data-ttu-id="9b4a1-132">Dominio</span><span class="sxs-lookup"><span data-stu-id="9b4a1-132">Domain</span></span> | <span data-ttu-id="9b4a1-133">Geometria</span><span class="sxs-lookup"><span data-stu-id="9b4a1-133">Geometry</span></span> | <span data-ttu-id="9b4a1-134">Pixel</span><span class="sxs-lookup"><span data-stu-id="9b4a1-134">Pixel</span></span> | <span data-ttu-id="9b4a1-135">Calcolo</span><span class="sxs-lookup"><span data-stu-id="9b4a1-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="9b4a1-136">x</span><span class="sxs-lookup"><span data-stu-id="9b4a1-136">x</span></span>      | <span data-ttu-id="9b4a1-137">x</span><span class="sxs-lookup"><span data-stu-id="9b4a1-137">x</span></span>    | <span data-ttu-id="9b4a1-138">x</span><span class="sxs-lookup"><span data-stu-id="9b4a1-138">x</span></span>      | <span data-ttu-id="9b4a1-139">x</span><span class="sxs-lookup"><span data-stu-id="9b4a1-139">x</span></span>        | <span data-ttu-id="9b4a1-140">x</span><span class="sxs-lookup"><span data-stu-id="9b4a1-140">x</span></span>     | <span data-ttu-id="9b4a1-141">x</span><span class="sxs-lookup"><span data-stu-id="9b4a1-141">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="9b4a1-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9b4a1-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b4a1-143">Metodi GatherGreen</span><span class="sxs-lookup"><span data-stu-id="9b4a1-143">GatherGreen methods</span></span>](texture2darray-gathergreen.md)
</dt> </dl>

 

 
