---
title: 'Funzione Texture2DArray:: Gather (S, float, int, uint)'
description: "Restituisce i quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare. | Funzione Texture2DArray:: Gather (S, float, int, uint)"
ms.assetid: 311A5042-19AA-41C7-8B22-2E34E4554250
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
ms.openlocfilehash: a1677fae87d8bbec3c0144cc8da0b5d13f0e0ae9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104530696"
---
# <a name="texture2darraygathersfloatintuint-function"></a><span data-ttu-id="ab1aa-105">Funzione Texture2DArray:: Gather (S, float, int, uint)</span><span class="sxs-lookup"><span data-stu-id="ab1aa-105">Texture2DArray::Gather(S,float,int,uint) function</span></span>

<span data-ttu-id="ab1aa-106">Restituisce i quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare.</span><span class="sxs-lookup"><span data-stu-id="ab1aa-106">Returns the four texel values that would be used in a bi-linear filtering operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab1aa-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ab1aa-107">Syntax</span></span>


``` syntax
TemplateType Gather(
  in  SamplerState S,
  in  float        Location,
  in  int          Offset,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="ab1aa-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ab1aa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab1aa-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ab1aa-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab1aa-110">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="ab1aa-110">Type: **SamplerState**</span></span>

<span data-ttu-id="ab1aa-111">Indice del campionatore in base zero.</span><span class="sxs-lookup"><span data-stu-id="ab1aa-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="ab1aa-112">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ab1aa-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab1aa-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="ab1aa-113">Type: **float**</span></span>

<span data-ttu-id="ab1aa-114">Coordinate di esempio (u, v).</span><span class="sxs-lookup"><span data-stu-id="ab1aa-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="ab1aa-115">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ab1aa-115">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab1aa-116">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="ab1aa-116">Type: **int**</span></span>

<span data-ttu-id="ab1aa-117">Offset applicato alle coordinate di trama prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="ab1aa-117">The offset applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="ab1aa-118">*Stato* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="ab1aa-118">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ab1aa-119">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="ab1aa-119">Type: **uint**</span></span>

<span data-ttu-id="ab1aa-120">Stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="ab1aa-120">The status of the operation.</span></span> <span data-ttu-id="ab1aa-121">Non è possibile accedere direttamente allo stato; passare invece lo stato alla funzione intrinseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="ab1aa-121">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="ab1aa-122">**CheckAccessFullyMapped** restituisce **true** se tutti i valori dell'operazione di **campionamento**, **raccolta** o **caricamento** corrispondente hanno eseguito l'accesso ai riquadri mappati in una [risorsa affiancata](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="ab1aa-122">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="ab1aa-123">Se sono stati ricavati valori da un riquadro non mappato, **CheckAccessFullyMapped** restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="ab1aa-123">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab1aa-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ab1aa-124">Return value</span></span>

<span data-ttu-id="ab1aa-125">Tipo: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="ab1aa-125">Type: **TemplateType**</span></span>

<span data-ttu-id="ab1aa-126">Valore a quattro componenti il cui tipo corrisponde al tipo di modello.</span><span class="sxs-lookup"><span data-stu-id="ab1aa-126">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab1aa-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="ab1aa-127">Remarks</span></span>

<span data-ttu-id="ab1aa-128">Gli esempi di trama possono essere usati per l'interpolazione bilineare.</span><span class="sxs-lookup"><span data-stu-id="ab1aa-128">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="ab1aa-129">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="ab1aa-129">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="ab1aa-130">Vertice</span><span class="sxs-lookup"><span data-stu-id="ab1aa-130">Vertex</span></span> | <span data-ttu-id="ab1aa-131">Hull</span><span class="sxs-lookup"><span data-stu-id="ab1aa-131">Hull</span></span> | <span data-ttu-id="ab1aa-132">Dominio</span><span class="sxs-lookup"><span data-stu-id="ab1aa-132">Domain</span></span> | <span data-ttu-id="ab1aa-133">Geometria</span><span class="sxs-lookup"><span data-stu-id="ab1aa-133">Geometry</span></span> | <span data-ttu-id="ab1aa-134">Pixel</span><span class="sxs-lookup"><span data-stu-id="ab1aa-134">Pixel</span></span> | <span data-ttu-id="ab1aa-135">Calcolo</span><span class="sxs-lookup"><span data-stu-id="ab1aa-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="ab1aa-136">x</span><span class="sxs-lookup"><span data-stu-id="ab1aa-136">x</span></span>      | <span data-ttu-id="ab1aa-137">x</span><span class="sxs-lookup"><span data-stu-id="ab1aa-137">x</span></span>    | <span data-ttu-id="ab1aa-138">x</span><span class="sxs-lookup"><span data-stu-id="ab1aa-138">x</span></span>      | <span data-ttu-id="ab1aa-139">x</span><span class="sxs-lookup"><span data-stu-id="ab1aa-139">x</span></span>        | <span data-ttu-id="ab1aa-140">x</span><span class="sxs-lookup"><span data-stu-id="ab1aa-140">x</span></span>     | <span data-ttu-id="ab1aa-141">x</span><span class="sxs-lookup"><span data-stu-id="ab1aa-141">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="ab1aa-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ab1aa-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab1aa-143">Metodi di raccolta</span><span class="sxs-lookup"><span data-stu-id="ab1aa-143">Gather methods</span></span>](texture2darray-gather.md)
</dt> </dl>

 

 
