---
title: Funzione GatherBlue (S, float, int2, int2, int2, int2) (riferimenti per HLSL)
description: Restituisce i componenti blu dei quattro valori Texel che verrebbero usati in un'operazione di filtraggio bilineare. | Funzione GatherBlue (S, float, int2, int2, int2, int2) (riferimenti per HLSL)
ms.assetid: 0DDD3235-4F12-4D74-975A-F70A271C1FC0
keywords:
- Funzione GatherBlue HLSL
topic_type:
- apiref
api_name:
- GatherBlue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a5676d9d6b25c6e67123c59dac14efa234386d4e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353541"
---
# <a name="gatherbluesfloatint2int2int2int2-function-hlsl-reference"></a><span data-ttu-id="01e77-105">Funzione GatherBlue (S, float, int2, int2, int2, int2) (riferimenti per HLSL)</span><span class="sxs-lookup"><span data-stu-id="01e77-105">GatherBlue(S,float,int2,int2,int2,int2) function (HLSL reference)</span></span>

<span data-ttu-id="01e77-106">Restituisce i componenti blu dei quattro valori Texel che verrebbero usati in un'operazione di filtraggio bilineare.</span><span class="sxs-lookup"><span data-stu-id="01e77-106">Returns the blue components of the four texel values that would be used in a bi-linear filtering operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="01e77-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="01e77-107">Syntax</span></span>


``` syntax
TemplateType GatherBlue(
  in SamplerState S,
  in float        Location,
  in int2         Offset1,
  in int2         Offset2,
  in int2         Offset3,
  in int2         Offset4
);
```



## <a name="parameters"></a><span data-ttu-id="01e77-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="01e77-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01e77-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="01e77-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01e77-110">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="01e77-110">Type: **SamplerState**</span></span>

<span data-ttu-id="01e77-111">Indice del campionatore in base zero.</span><span class="sxs-lookup"><span data-stu-id="01e77-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="01e77-112">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="01e77-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01e77-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="01e77-113">Type: **float**</span></span>

<span data-ttu-id="01e77-114">Coordinate di esempio (u, v).</span><span class="sxs-lookup"><span data-stu-id="01e77-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="01e77-115">*Offset1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="01e77-115">*Offset1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01e77-116">Tipo: **int2**</span><span class="sxs-lookup"><span data-stu-id="01e77-116">Type: **int2**</span></span>

<span data-ttu-id="01e77-117">Primo componente di offset applicato alle coordinate di trama prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="01e77-117">The first offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="01e77-118">*Offset2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="01e77-118">*Offset2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01e77-119">Tipo: **int2**</span><span class="sxs-lookup"><span data-stu-id="01e77-119">Type: **int2**</span></span>

<span data-ttu-id="01e77-120">Secondo componente di offset applicato alle coordinate di trama prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="01e77-120">The second offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="01e77-121">*Offset3* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="01e77-121">*Offset3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01e77-122">Tipo: **int2**</span><span class="sxs-lookup"><span data-stu-id="01e77-122">Type: **int2**</span></span>

<span data-ttu-id="01e77-123">Terzo componente di offset applicato alle coordinate di trama prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="01e77-123">The third offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="01e77-124">*Offset4* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="01e77-124">*Offset4* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01e77-125">Tipo: **int2**</span><span class="sxs-lookup"><span data-stu-id="01e77-125">Type: **int2**</span></span>

<span data-ttu-id="01e77-126">Quarto componente di offset applicato alle coordinate di trama prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="01e77-126">The fourth offset component applied to the texture coordinates before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01e77-127">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="01e77-127">Return value</span></span>

<span data-ttu-id="01e77-128">Tipo: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="01e77-128">Type: **TemplateType**</span></span>

<span data-ttu-id="01e77-129">Valore a quattro componenti il cui tipo corrisponde al tipo di modello.</span><span class="sxs-lookup"><span data-stu-id="01e77-129">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="01e77-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="01e77-130">Remarks</span></span>

<span data-ttu-id="01e77-131">Gli esempi di trama possono essere usati per l'interpolazione bilineare.</span><span class="sxs-lookup"><span data-stu-id="01e77-131">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="01e77-132">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="01e77-132">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="01e77-133">Vertice</span><span class="sxs-lookup"><span data-stu-id="01e77-133">Vertex</span></span> | <span data-ttu-id="01e77-134">Hull</span><span class="sxs-lookup"><span data-stu-id="01e77-134">Hull</span></span> | <span data-ttu-id="01e77-135">Dominio</span><span class="sxs-lookup"><span data-stu-id="01e77-135">Domain</span></span> | <span data-ttu-id="01e77-136">Geometria</span><span class="sxs-lookup"><span data-stu-id="01e77-136">Geometry</span></span> | <span data-ttu-id="01e77-137">Pixel</span><span class="sxs-lookup"><span data-stu-id="01e77-137">Pixel</span></span> | <span data-ttu-id="01e77-138">Calcolo</span><span class="sxs-lookup"><span data-stu-id="01e77-138">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="01e77-139">x</span><span class="sxs-lookup"><span data-stu-id="01e77-139">x</span></span>      | <span data-ttu-id="01e77-140">x</span><span class="sxs-lookup"><span data-stu-id="01e77-140">x</span></span>    | <span data-ttu-id="01e77-141">x</span><span class="sxs-lookup"><span data-stu-id="01e77-141">x</span></span>      | <span data-ttu-id="01e77-142">x</span><span class="sxs-lookup"><span data-stu-id="01e77-142">x</span></span>        | <span data-ttu-id="01e77-143">x</span><span class="sxs-lookup"><span data-stu-id="01e77-143">x</span></span>     | <span data-ttu-id="01e77-144">x</span><span class="sxs-lookup"><span data-stu-id="01e77-144">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="01e77-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="01e77-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01e77-146">Metodi GatherBlue</span><span class="sxs-lookup"><span data-stu-id="01e77-146">GatherBlue methods</span></span>](texture2darray-gatherblue.md)
</dt> </dl>

 

 




