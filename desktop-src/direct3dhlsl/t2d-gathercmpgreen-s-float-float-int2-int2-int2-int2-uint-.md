---
title: 'Funzione Texture2D:: GatherCmpGreen (S, float, float, int2, int2, int2, int2, uint)'
description: "Per quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce un confronto del relativo componente verde rispetto a un valore di confronto insieme allo stato del mapping dei riquadri. | Funzione Texture2D:: GatherCmpGreen (S, float, float, int2, int2, int2, int2, uint)"
ms.assetid: E7EB3D17-3110-4167-B255-C451BA4EFB27
keywords:
- Funzione GatherCmpGreen HLSL
topic_type:
- apiref
api_name:
- GatherCmpGreen
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8b490fd47bd9346c4f514867de63df7a4d090e5b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104234794"
---
# <a name="texture2dgathercmpgreensfloatfloatint2int2int2int2uint-function"></a><span data-ttu-id="4e43a-105">Funzione Texture2D:: GatherCmpGreen (S, float, float, int2, int2, int2, int2, uint)</span><span class="sxs-lookup"><span data-stu-id="4e43a-105">Texture2D::GatherCmpGreen(S,float,float,int2,int2,int2,int2,uint) function</span></span>

<span data-ttu-id="4e43a-106">Per quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce un confronto del relativo componente verde rispetto a un valore di confronto insieme allo stato del mapping dei riquadri.</span><span class="sxs-lookup"><span data-stu-id="4e43a-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their green component against a compare value along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e43a-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4e43a-107">Syntax</span></span>


``` syntax
TemplateType GatherCmpGreen(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  in  int2         Offset1,
  in  int2         Offset2,
  in  int2         Offset3,
  in  int2         Offset4,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="4e43a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="4e43a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e43a-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4e43a-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e43a-110">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="4e43a-110">Type: **SamplerState**</span></span>

<span data-ttu-id="4e43a-111">Indice del campionatore in base zero.</span><span class="sxs-lookup"><span data-stu-id="4e43a-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="4e43a-112">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4e43a-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e43a-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="4e43a-113">Type: **float**</span></span>

<span data-ttu-id="4e43a-114">Coordinate di esempio (u, v).</span><span class="sxs-lookup"><span data-stu-id="4e43a-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="4e43a-115">*CompareValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4e43a-115">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e43a-116">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="4e43a-116">Type: **float**</span></span>

<span data-ttu-id="4e43a-117">Valore da confrontare con ogni valore campionato.</span><span class="sxs-lookup"><span data-stu-id="4e43a-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="4e43a-118">*Offset1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4e43a-118">*Offset1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e43a-119">Tipo: **int2**</span><span class="sxs-lookup"><span data-stu-id="4e43a-119">Type: **int2**</span></span>

<span data-ttu-id="4e43a-120">Primo componente di offset applicato alle coordinate di trama prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="4e43a-120">The first offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="4e43a-121">*Offset2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4e43a-121">*Offset2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e43a-122">Tipo: **int2**</span><span class="sxs-lookup"><span data-stu-id="4e43a-122">Type: **int2**</span></span>

<span data-ttu-id="4e43a-123">Secondo componente di offset applicato alle coordinate di trama prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="4e43a-123">The second offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="4e43a-124">*Offset3* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4e43a-124">*Offset3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e43a-125">Tipo: **int2**</span><span class="sxs-lookup"><span data-stu-id="4e43a-125">Type: **int2**</span></span>

<span data-ttu-id="4e43a-126">Terzo componente di offset applicato alle coordinate di trama prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="4e43a-126">The third offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="4e43a-127">*Offset4* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4e43a-127">*Offset4* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e43a-128">Tipo: **int2**</span><span class="sxs-lookup"><span data-stu-id="4e43a-128">Type: **int2**</span></span>

<span data-ttu-id="4e43a-129">Quarto componente di offset applicato alle coordinate di trama prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="4e43a-129">The fourth offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="4e43a-130">*Stato* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="4e43a-130">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4e43a-131">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="4e43a-131">Type: **uint**</span></span>

<span data-ttu-id="4e43a-132">Stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="4e43a-132">The status of the operation.</span></span> <span data-ttu-id="4e43a-133">Non è possibile accedere direttamente allo stato; passare invece lo stato alla funzione intrinseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="4e43a-133">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="4e43a-134">**CheckAccessFullyMapped** restituisce **true** se tutti i valori dell'operazione di **campionamento**, **raccolta** o **caricamento** corrispondente hanno eseguito l'accesso ai riquadri mappati in una [risorsa affiancata](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="4e43a-134">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="4e43a-135">Se sono stati ricavati valori da un riquadro non mappato, **CheckAccessFullyMapped** restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="4e43a-135">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e43a-136">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4e43a-136">Return value</span></span>

<span data-ttu-id="4e43a-137">Tipo: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="4e43a-137">Type: **TemplateType**</span></span>

<span data-ttu-id="4e43a-138">Valore a quattro componenti il cui tipo corrisponde al tipo di modello.</span><span class="sxs-lookup"><span data-stu-id="4e43a-138">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e43a-139">Commenti</span><span class="sxs-lookup"><span data-stu-id="4e43a-139">Remarks</span></span>

<span data-ttu-id="4e43a-140">Gli esempi di trama possono essere usati per l'interpolazione bilineare.</span><span class="sxs-lookup"><span data-stu-id="4e43a-140">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="4e43a-141">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="4e43a-141">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="4e43a-142">Vertice</span><span class="sxs-lookup"><span data-stu-id="4e43a-142">Vertex</span></span> | <span data-ttu-id="4e43a-143">Hull</span><span class="sxs-lookup"><span data-stu-id="4e43a-143">Hull</span></span> | <span data-ttu-id="4e43a-144">Dominio</span><span class="sxs-lookup"><span data-stu-id="4e43a-144">Domain</span></span> | <span data-ttu-id="4e43a-145">Geometria</span><span class="sxs-lookup"><span data-stu-id="4e43a-145">Geometry</span></span> | <span data-ttu-id="4e43a-146">Pixel</span><span class="sxs-lookup"><span data-stu-id="4e43a-146">Pixel</span></span> | <span data-ttu-id="4e43a-147">Calcolo</span><span class="sxs-lookup"><span data-stu-id="4e43a-147">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="4e43a-148">x</span><span class="sxs-lookup"><span data-stu-id="4e43a-148">x</span></span>      | <span data-ttu-id="4e43a-149">x</span><span class="sxs-lookup"><span data-stu-id="4e43a-149">x</span></span>    | <span data-ttu-id="4e43a-150">x</span><span class="sxs-lookup"><span data-stu-id="4e43a-150">x</span></span>      | <span data-ttu-id="4e43a-151">x</span><span class="sxs-lookup"><span data-stu-id="4e43a-151">x</span></span>        | <span data-ttu-id="4e43a-152">x</span><span class="sxs-lookup"><span data-stu-id="4e43a-152">x</span></span>     | <span data-ttu-id="4e43a-153">x</span><span class="sxs-lookup"><span data-stu-id="4e43a-153">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="4e43a-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4e43a-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e43a-155">Metodi GatherCmpGreen</span><span class="sxs-lookup"><span data-stu-id="4e43a-155">GatherCmpGreen methods</span></span>](texture2d-gathercmpgreen.md)
</dt> </dl>

 

 
