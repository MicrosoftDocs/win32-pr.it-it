---
title: 'Funzione Texture2D:: GatherCmpAlpha (S, float, float, int2, int2, int2, int2, uint)'
description: "Per quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce un confronto tra il relativo componente alfa e un valore di confronto con lo stato del mapping dei riquadri. | Funzione Texture2D:: GatherCmpAlpha (S, float, float, int2, int2, int2, int2, uint)"
ms.assetid: 4DB56BE2-503A-4D51-89FB-E4DD91EBF028
keywords:
- Funzione GatherCmpAlpha HLSL
topic_type:
- apiref
api_name:
- GatherCmpAlpha
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5e1962dc10b5ef45ba3ad7d7196872fd4d27708c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104234846"
---
# <a name="texture2dgathercmpalphasfloatfloatint2int2int2int2uint-function"></a><span data-ttu-id="611cd-105">Funzione Texture2D:: GatherCmpAlpha (S, float, float, int2, int2, int2, int2, uint)</span><span class="sxs-lookup"><span data-stu-id="611cd-105">Texture2D::GatherCmpAlpha(S,float,float,int2,int2,int2,int2,uint) function</span></span>

<span data-ttu-id="611cd-106">Per quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce un confronto tra il relativo componente alfa e un valore di confronto con lo stato del mapping dei riquadri.</span><span class="sxs-lookup"><span data-stu-id="611cd-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their alpha component against a compare value along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="611cd-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="611cd-107">Syntax</span></span>


``` syntax
TemplateType GatherCmpAlpha(
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



## <a name="parameters"></a><span data-ttu-id="611cd-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="611cd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="611cd-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="611cd-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="611cd-110">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="611cd-110">Type: **SamplerState**</span></span>

<span data-ttu-id="611cd-111">Indice del campionatore in base zero.</span><span class="sxs-lookup"><span data-stu-id="611cd-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="611cd-112">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="611cd-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="611cd-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="611cd-113">Type: **float**</span></span>

<span data-ttu-id="611cd-114">Coordinate di esempio (u, v).</span><span class="sxs-lookup"><span data-stu-id="611cd-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="611cd-115">*CompareValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="611cd-115">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="611cd-116">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="611cd-116">Type: **float**</span></span>

<span data-ttu-id="611cd-117">Valore da confrontare con ogni valore campionato.</span><span class="sxs-lookup"><span data-stu-id="611cd-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="611cd-118">*Offset1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="611cd-118">*Offset1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="611cd-119">Tipo: **int2**</span><span class="sxs-lookup"><span data-stu-id="611cd-119">Type: **int2**</span></span>

<span data-ttu-id="611cd-120">Primo componente di offset applicato alle coordinate di trama prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="611cd-120">The first offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="611cd-121">*Offset2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="611cd-121">*Offset2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="611cd-122">Tipo: **int2**</span><span class="sxs-lookup"><span data-stu-id="611cd-122">Type: **int2**</span></span>

<span data-ttu-id="611cd-123">Secondo componente di offset applicato alle coordinate di trama prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="611cd-123">The second offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="611cd-124">*Offset3* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="611cd-124">*Offset3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="611cd-125">Tipo: **int2**</span><span class="sxs-lookup"><span data-stu-id="611cd-125">Type: **int2**</span></span>

<span data-ttu-id="611cd-126">Terzo componente di offset applicato alle coordinate di trama prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="611cd-126">The third offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="611cd-127">*Offset4* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="611cd-127">*Offset4* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="611cd-128">Tipo: **int2**</span><span class="sxs-lookup"><span data-stu-id="611cd-128">Type: **int2**</span></span>

<span data-ttu-id="611cd-129">Quarto componente di offset applicato alle coordinate di trama prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="611cd-129">The fourth offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="611cd-130">*Stato* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="611cd-130">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="611cd-131">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="611cd-131">Type: **uint**</span></span>

<span data-ttu-id="611cd-132">Stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="611cd-132">The status of the operation.</span></span> <span data-ttu-id="611cd-133">Non è possibile accedere direttamente allo stato; passare invece lo stato alla funzione intrinseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="611cd-133">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="611cd-134">**CheckAccessFullyMapped** restituisce **true** se tutti i valori dell'operazione di **campionamento**, **raccolta** o **caricamento** corrispondente hanno eseguito l'accesso ai riquadri mappati in una [risorsa affiancata](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="611cd-134">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="611cd-135">Se sono stati ricavati valori da un riquadro non mappato, **CheckAccessFullyMapped** restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="611cd-135">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="611cd-136">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="611cd-136">Return value</span></span>

<span data-ttu-id="611cd-137">Tipo: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="611cd-137">Type: **TemplateType**</span></span>

<span data-ttu-id="611cd-138">Valore a quattro componenti il cui tipo corrisponde al tipo di modello.</span><span class="sxs-lookup"><span data-stu-id="611cd-138">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="611cd-139">Commenti</span><span class="sxs-lookup"><span data-stu-id="611cd-139">Remarks</span></span>

<span data-ttu-id="611cd-140">Gli esempi di trama possono essere usati per l'interpolazione bilineare.</span><span class="sxs-lookup"><span data-stu-id="611cd-140">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="611cd-141">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="611cd-141">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="611cd-142">Vertice</span><span class="sxs-lookup"><span data-stu-id="611cd-142">Vertex</span></span> | <span data-ttu-id="611cd-143">Hull</span><span class="sxs-lookup"><span data-stu-id="611cd-143">Hull</span></span> | <span data-ttu-id="611cd-144">Dominio</span><span class="sxs-lookup"><span data-stu-id="611cd-144">Domain</span></span> | <span data-ttu-id="611cd-145">Geometria</span><span class="sxs-lookup"><span data-stu-id="611cd-145">Geometry</span></span> | <span data-ttu-id="611cd-146">Pixel</span><span class="sxs-lookup"><span data-stu-id="611cd-146">Pixel</span></span> | <span data-ttu-id="611cd-147">Calcolo</span><span class="sxs-lookup"><span data-stu-id="611cd-147">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="611cd-148">x</span><span class="sxs-lookup"><span data-stu-id="611cd-148">x</span></span>      | <span data-ttu-id="611cd-149">x</span><span class="sxs-lookup"><span data-stu-id="611cd-149">x</span></span>    | <span data-ttu-id="611cd-150">x</span><span class="sxs-lookup"><span data-stu-id="611cd-150">x</span></span>      | <span data-ttu-id="611cd-151">x</span><span class="sxs-lookup"><span data-stu-id="611cd-151">x</span></span>        | <span data-ttu-id="611cd-152">x</span><span class="sxs-lookup"><span data-stu-id="611cd-152">x</span></span>     | <span data-ttu-id="611cd-153">x</span><span class="sxs-lookup"><span data-stu-id="611cd-153">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="611cd-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="611cd-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="611cd-155">Metodi GatherCmpAlpha</span><span class="sxs-lookup"><span data-stu-id="611cd-155">GatherCmpAlpha methods</span></span>](texture2d-gathercmpalpha.md)
</dt> </dl>

 

 
