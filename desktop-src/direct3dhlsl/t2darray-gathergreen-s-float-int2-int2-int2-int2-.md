---
title: 'Funzione Texture2DArray:: GatherGreen (S, float, int2, int2, int2, int2)'
description: "Restituisce i componenti verdi dei quattro valori Texel che verrebbero usati in un'operazione di filtraggio bilineare. | Funzione Texture2DArray:: GatherGreen (S, float, int2, int2, int2, int2)"
ms.assetid: 7E79442E-286F-4BDB-8D7A-2C20A0933585
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
ms.openlocfilehash: 12e8649882c7e3c8fd4d9f88cd37d1a27952eb2b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103969241"
---
# <a name="texture2darraygathergreensfloatint2int2int2int2-function"></a><span data-ttu-id="57473-105">Funzione Texture2DArray:: GatherGreen (S, float, int2, int2, int2, int2)</span><span class="sxs-lookup"><span data-stu-id="57473-105">Texture2DArray::GatherGreen(S,float,int2,int2,int2,int2) function</span></span>

<span data-ttu-id="57473-106">Restituisce i componenti verdi dei quattro valori Texel che verrebbero usati in un'operazione di filtraggio bilineare.</span><span class="sxs-lookup"><span data-stu-id="57473-106">Returns the green components of the four texel values that would be used in a bi-linear filtering operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="57473-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="57473-107">Syntax</span></span>


``` syntax
TemplateType GatherGreen(
  in SamplerState S,
  in float        Location,
  in int2         Offset1,
  in int2         Offset2,
  in int2         Offset3,
  in int2         Offset4
);
```



## <a name="parameters"></a><span data-ttu-id="57473-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="57473-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57473-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="57473-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57473-110">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="57473-110">Type: **SamplerState**</span></span>

<span data-ttu-id="57473-111">Indice del campionatore in base zero.</span><span class="sxs-lookup"><span data-stu-id="57473-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="57473-112">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="57473-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57473-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="57473-113">Type: **float**</span></span>

<span data-ttu-id="57473-114">Coordinate di esempio (u, v).</span><span class="sxs-lookup"><span data-stu-id="57473-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="57473-115">*Offset1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="57473-115">*Offset1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57473-116">Tipo: **int2**</span><span class="sxs-lookup"><span data-stu-id="57473-116">Type: **int2**</span></span>

<span data-ttu-id="57473-117">Primo componente di offset applicato alle coordinate di trama prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="57473-117">The first offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="57473-118">*Offset2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="57473-118">*Offset2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57473-119">Tipo: **int2**</span><span class="sxs-lookup"><span data-stu-id="57473-119">Type: **int2**</span></span>

<span data-ttu-id="57473-120">Secondo componente di offset applicato alle coordinate di trama prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="57473-120">The second offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="57473-121">*Offset3* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="57473-121">*Offset3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57473-122">Tipo: **int2**</span><span class="sxs-lookup"><span data-stu-id="57473-122">Type: **int2**</span></span>

<span data-ttu-id="57473-123">Terzo componente di offset applicato alle coordinate di trama prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="57473-123">The third offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="57473-124">*Offset4* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="57473-124">*Offset4* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57473-125">Tipo: **int2**</span><span class="sxs-lookup"><span data-stu-id="57473-125">Type: **int2**</span></span>

<span data-ttu-id="57473-126">Quarto componente di offset applicato alle coordinate di trama prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="57473-126">The fourth offset component applied to the texture coordinates before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57473-127">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="57473-127">Return value</span></span>

<span data-ttu-id="57473-128">Tipo: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="57473-128">Type: **TemplateType**</span></span>

<span data-ttu-id="57473-129">Valore a quattro componenti il cui tipo corrisponde al tipo di modello.</span><span class="sxs-lookup"><span data-stu-id="57473-129">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="57473-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="57473-130">Remarks</span></span>

<span data-ttu-id="57473-131">Gli esempi di trama possono essere usati per l'interpolazione bilineare.</span><span class="sxs-lookup"><span data-stu-id="57473-131">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="57473-132">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="57473-132">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="57473-133">Vertice</span><span class="sxs-lookup"><span data-stu-id="57473-133">Vertex</span></span> | <span data-ttu-id="57473-134">Hull</span><span class="sxs-lookup"><span data-stu-id="57473-134">Hull</span></span> | <span data-ttu-id="57473-135">Dominio</span><span class="sxs-lookup"><span data-stu-id="57473-135">Domain</span></span> | <span data-ttu-id="57473-136">Geometria</span><span class="sxs-lookup"><span data-stu-id="57473-136">Geometry</span></span> | <span data-ttu-id="57473-137">Pixel</span><span class="sxs-lookup"><span data-stu-id="57473-137">Pixel</span></span> | <span data-ttu-id="57473-138">Calcolo</span><span class="sxs-lookup"><span data-stu-id="57473-138">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="57473-139">x</span><span class="sxs-lookup"><span data-stu-id="57473-139">x</span></span>      | <span data-ttu-id="57473-140">x</span><span class="sxs-lookup"><span data-stu-id="57473-140">x</span></span>    | <span data-ttu-id="57473-141">x</span><span class="sxs-lookup"><span data-stu-id="57473-141">x</span></span>      | <span data-ttu-id="57473-142">x</span><span class="sxs-lookup"><span data-stu-id="57473-142">x</span></span>        | <span data-ttu-id="57473-143">x</span><span class="sxs-lookup"><span data-stu-id="57473-143">x</span></span>     | <span data-ttu-id="57473-144">x</span><span class="sxs-lookup"><span data-stu-id="57473-144">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="57473-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="57473-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57473-146">Metodi GatherGreen</span><span class="sxs-lookup"><span data-stu-id="57473-146">GatherGreen methods</span></span>](texture2darray-gathergreen.md)
</dt> </dl>

 

 




