---
title: 'Funzione Texture2DArray:: GatherGreen (S, float, int2, int2, int2, int2, uint)'
description: "Restituisce i componenti verdi dei quattro valori Texel che verrebbero usati in un'operazione di filtraggio bilineare, insieme allo stato di mapping dei riquadri. | Funzione Texture2DArray:: GatherGreen (S, float, int2, int2, int2, int2, uint)"
ms.assetid: 994320C6-3BE5-40F9-9B9F-1913134DA71A
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
ms.openlocfilehash: 37e307ea9be68f48b8d53b813abffb1fbfd86853
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103886245"
---
# <a name="texture2darraygathergreensfloatint2int2int2int2uint-function"></a><span data-ttu-id="0446c-105">Funzione Texture2DArray:: GatherGreen (S, float, int2, int2, int2, int2, uint)</span><span class="sxs-lookup"><span data-stu-id="0446c-105">Texture2DArray::GatherGreen(S,float,int2,int2,int2,int2,uint) function</span></span>

<span data-ttu-id="0446c-106">Restituisce i componenti verdi dei quattro valori Texel che verrebbero usati in un'operazione di filtraggio bilineare, insieme allo stato di mapping dei riquadri.</span><span class="sxs-lookup"><span data-stu-id="0446c-106">Returns the green components of the four texel values that would be used in a bi-linear filtering operation, along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="0446c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0446c-107">Syntax</span></span>


``` syntax
TemplateType GatherGreen(
  in  SamplerState S,
  in  float        Location,
  in  int2         Offset1,
  in  int2         Offset2,
  in  int2         Offset3,
  in  int2         Offset4,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="0446c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="0446c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0446c-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0446c-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0446c-110">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="0446c-110">Type: **SamplerState**</span></span>

<span data-ttu-id="0446c-111">Indice del campionatore in base zero.</span><span class="sxs-lookup"><span data-stu-id="0446c-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="0446c-112">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0446c-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0446c-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="0446c-113">Type: **float**</span></span>

<span data-ttu-id="0446c-114">Coordinate di esempio (u, v).</span><span class="sxs-lookup"><span data-stu-id="0446c-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="0446c-115">*Offset1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0446c-115">*Offset1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0446c-116">Tipo: **int2**</span><span class="sxs-lookup"><span data-stu-id="0446c-116">Type: **int2**</span></span>

<span data-ttu-id="0446c-117">Primo componente di offset applicato alle coordinate di trama prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="0446c-117">The first offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="0446c-118">*Offset2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0446c-118">*Offset2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0446c-119">Tipo: **int2**</span><span class="sxs-lookup"><span data-stu-id="0446c-119">Type: **int2**</span></span>

<span data-ttu-id="0446c-120">Secondo componente di offset applicato alle coordinate di trama prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="0446c-120">The second offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="0446c-121">*Offset3* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0446c-121">*Offset3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0446c-122">Tipo: **int2**</span><span class="sxs-lookup"><span data-stu-id="0446c-122">Type: **int2**</span></span>

<span data-ttu-id="0446c-123">Terzo componente di offset applicato alle coordinate di trama prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="0446c-123">The third offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="0446c-124">*Offset4* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0446c-124">*Offset4* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0446c-125">Tipo: **int2**</span><span class="sxs-lookup"><span data-stu-id="0446c-125">Type: **int2**</span></span>

<span data-ttu-id="0446c-126">Quarto componente di offset applicato alle coordinate di trama prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="0446c-126">The fourth offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="0446c-127">*Stato* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="0446c-127">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0446c-128">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="0446c-128">Type: **uint**</span></span>

<span data-ttu-id="0446c-129">Stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="0446c-129">The status of the operation.</span></span> <span data-ttu-id="0446c-130">Non è possibile accedere direttamente allo stato; passare invece lo stato alla funzione intrinseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="0446c-130">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="0446c-131">**CheckAccessFullyMapped** restituisce **true** se tutti i valori dell'operazione di **campionamento**, **raccolta** o **caricamento** corrispondente hanno eseguito l'accesso ai riquadri mappati in una [risorsa affiancata](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="0446c-131">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="0446c-132">Se sono stati ricavati valori da un riquadro non mappato, **CheckAccessFullyMapped** restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="0446c-132">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0446c-133">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0446c-133">Return value</span></span>

<span data-ttu-id="0446c-134">Tipo: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="0446c-134">Type: **TemplateType**</span></span>

<span data-ttu-id="0446c-135">Valore a quattro componenti il cui tipo corrisponde al tipo di modello.</span><span class="sxs-lookup"><span data-stu-id="0446c-135">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="0446c-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="0446c-136">Remarks</span></span>

<span data-ttu-id="0446c-137">Gli esempi di trama possono essere usati per l'interpolazione bilineare.</span><span class="sxs-lookup"><span data-stu-id="0446c-137">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="0446c-138">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="0446c-138">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="0446c-139">Vertice</span><span class="sxs-lookup"><span data-stu-id="0446c-139">Vertex</span></span> | <span data-ttu-id="0446c-140">Hull</span><span class="sxs-lookup"><span data-stu-id="0446c-140">Hull</span></span> | <span data-ttu-id="0446c-141">Dominio</span><span class="sxs-lookup"><span data-stu-id="0446c-141">Domain</span></span> | <span data-ttu-id="0446c-142">Geometria</span><span class="sxs-lookup"><span data-stu-id="0446c-142">Geometry</span></span> | <span data-ttu-id="0446c-143">Pixel</span><span class="sxs-lookup"><span data-stu-id="0446c-143">Pixel</span></span> | <span data-ttu-id="0446c-144">Calcolo</span><span class="sxs-lookup"><span data-stu-id="0446c-144">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="0446c-145">x</span><span class="sxs-lookup"><span data-stu-id="0446c-145">x</span></span>      | <span data-ttu-id="0446c-146">x</span><span class="sxs-lookup"><span data-stu-id="0446c-146">x</span></span>    | <span data-ttu-id="0446c-147">x</span><span class="sxs-lookup"><span data-stu-id="0446c-147">x</span></span>      | <span data-ttu-id="0446c-148">x</span><span class="sxs-lookup"><span data-stu-id="0446c-148">x</span></span>        | <span data-ttu-id="0446c-149">x</span><span class="sxs-lookup"><span data-stu-id="0446c-149">x</span></span>     | <span data-ttu-id="0446c-150">x</span><span class="sxs-lookup"><span data-stu-id="0446c-150">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="0446c-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0446c-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0446c-152">Metodi GatherGreen</span><span class="sxs-lookup"><span data-stu-id="0446c-152">GatherGreen methods</span></span>](texture2darray-gathergreen.md)
</dt> </dl>

 

 
