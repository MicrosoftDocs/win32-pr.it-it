---
title: 'Funzione TextureCubeArray:: GatherAlpha (S, float, uint)'
description: "Restituisce i componenti alfa dei quattro valori Texel che verrebbero usati in un'operazione di filtraggio bilineare, insieme allo stato del mapping dei riquadri. | Funzione TextureCubeArray:: GatherAlpha (S, float, uint)"
ms.assetid: C6AF896A-C68E-44EA-A779-DD9DBA30A039
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
ms.openlocfilehash: c1f9b692d81f6e26753496bb58ac114145ed21de
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104530750"
---
# <a name="texturecubearraygatheralphasfloatuint-function"></a><span data-ttu-id="21f98-105">Funzione TextureCubeArray:: GatherAlpha (S, float, uint)</span><span class="sxs-lookup"><span data-stu-id="21f98-105">TextureCubeArray::GatherAlpha(S,float,uint) function</span></span>

<span data-ttu-id="21f98-106">Restituisce i componenti alfa dei quattro valori Texel che verrebbero usati in un'operazione di filtraggio bilineare, insieme allo stato del mapping dei riquadri.</span><span class="sxs-lookup"><span data-stu-id="21f98-106">Returns the alpha components of the four texel values that would be used in a bi-linear filtering operation, along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="21f98-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="21f98-107">Syntax</span></span>


``` syntax
TemplateType GatherAlpha(
  in  SamplerState S,
  in  float        Location,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="21f98-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="21f98-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21f98-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="21f98-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21f98-110">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="21f98-110">Type: **SamplerState**</span></span>

<span data-ttu-id="21f98-111">Indice del campionatore in base zero.</span><span class="sxs-lookup"><span data-stu-id="21f98-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="21f98-112">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="21f98-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21f98-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="21f98-113">Type: **float**</span></span>

<span data-ttu-id="21f98-114">Coordinate di esempio (u, v).</span><span class="sxs-lookup"><span data-stu-id="21f98-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="21f98-115">*Stato* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="21f98-115">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="21f98-116">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="21f98-116">Type: **uint**</span></span>

<span data-ttu-id="21f98-117">Stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="21f98-117">The status of the operation.</span></span> <span data-ttu-id="21f98-118">Non è possibile accedere direttamente allo stato; passare invece lo stato alla funzione intrinseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="21f98-118">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="21f98-119">**CheckAccessFullyMapped** restituisce **true** se tutti i valori dell'operazione di **campionamento**, **raccolta** o **caricamento** corrispondente hanno eseguito l'accesso ai riquadri mappati in una [risorsa affiancata](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="21f98-119">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="21f98-120">Se sono stati ricavati valori da un riquadro non mappato, **CheckAccessFullyMapped** restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="21f98-120">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21f98-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="21f98-121">Return value</span></span>

<span data-ttu-id="21f98-122">Tipo: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="21f98-122">Type: **TemplateType**</span></span>

<span data-ttu-id="21f98-123">Valore a quattro componenti il cui tipo corrisponde al tipo di modello.</span><span class="sxs-lookup"><span data-stu-id="21f98-123">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="21f98-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="21f98-124">Remarks</span></span>

<span data-ttu-id="21f98-125">Gli esempi di trama possono essere usati per l'interpolazione bilineare.</span><span class="sxs-lookup"><span data-stu-id="21f98-125">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="21f98-126">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="21f98-126">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="21f98-127">Vertice</span><span class="sxs-lookup"><span data-stu-id="21f98-127">Vertex</span></span> | <span data-ttu-id="21f98-128">Hull</span><span class="sxs-lookup"><span data-stu-id="21f98-128">Hull</span></span> | <span data-ttu-id="21f98-129">Dominio</span><span class="sxs-lookup"><span data-stu-id="21f98-129">Domain</span></span> | <span data-ttu-id="21f98-130">Geometria</span><span class="sxs-lookup"><span data-stu-id="21f98-130">Geometry</span></span> | <span data-ttu-id="21f98-131">Pixel</span><span class="sxs-lookup"><span data-stu-id="21f98-131">Pixel</span></span> | <span data-ttu-id="21f98-132">Calcolo</span><span class="sxs-lookup"><span data-stu-id="21f98-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="21f98-133">x</span><span class="sxs-lookup"><span data-stu-id="21f98-133">x</span></span>      | <span data-ttu-id="21f98-134">x</span><span class="sxs-lookup"><span data-stu-id="21f98-134">x</span></span>    | <span data-ttu-id="21f98-135">x</span><span class="sxs-lookup"><span data-stu-id="21f98-135">x</span></span>      | <span data-ttu-id="21f98-136">x</span><span class="sxs-lookup"><span data-stu-id="21f98-136">x</span></span>        | <span data-ttu-id="21f98-137">x</span><span class="sxs-lookup"><span data-stu-id="21f98-137">x</span></span>     | <span data-ttu-id="21f98-138">x</span><span class="sxs-lookup"><span data-stu-id="21f98-138">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="21f98-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="21f98-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21f98-140">Metodi GatherAlpha</span><span class="sxs-lookup"><span data-stu-id="21f98-140">GatherAlpha methods</span></span>](texturecubearray-gatheralpha.md)
</dt> <dt>

[<span data-ttu-id="21f98-141">**TextureCubeArray**</span><span class="sxs-lookup"><span data-stu-id="21f98-141">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
