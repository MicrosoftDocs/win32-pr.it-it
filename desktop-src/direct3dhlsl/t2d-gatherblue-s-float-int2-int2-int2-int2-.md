---
title: 'Funzione Texture2D:: GatherBlue (S, float, int2, int2, int2, int2)'
description: "Restituisce i componenti blu dei quattro valori Texel che verrebbero usati in un'operazione di filtraggio bilineare. | Funzione Texture2D:: GatherBlue (S, float, int2, int2, int2, int2)"
ms.assetid: 0FFD3D82-E849-4C19-BEBC-85B9CCA40CA0
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
ms.openlocfilehash: 21f44482d82e8246391389289f0c90ea6c97de9a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981874"
---
# <a name="gatherbluesfloatint2int2int2int2-function"></a><span data-ttu-id="ff5cd-105">Funzione GatherBlue (S, float, int2, int2, int2, int2)</span><span class="sxs-lookup"><span data-stu-id="ff5cd-105">GatherBlue(S,float,int2,int2,int2,int2) function</span></span>

<span data-ttu-id="ff5cd-106">Restituisce i componenti blu dei quattro valori Texel che verrebbero usati in un'operazione di filtraggio bilineare.</span><span class="sxs-lookup"><span data-stu-id="ff5cd-106">Returns the blue components of the four texel values that would be used in a bi-linear filtering operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff5cd-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ff5cd-107">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="ff5cd-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ff5cd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff5cd-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ff5cd-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff5cd-110">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="ff5cd-110">Type: **SamplerState**</span></span>

<span data-ttu-id="ff5cd-111">Indice del campionatore in base zero.</span><span class="sxs-lookup"><span data-stu-id="ff5cd-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="ff5cd-112">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ff5cd-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff5cd-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="ff5cd-113">Type: **float**</span></span>

<span data-ttu-id="ff5cd-114">Coordinate di esempio (u, v).</span><span class="sxs-lookup"><span data-stu-id="ff5cd-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="ff5cd-115">*Offset1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ff5cd-115">*Offset1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff5cd-116">Tipo: **int2**</span><span class="sxs-lookup"><span data-stu-id="ff5cd-116">Type: **int2**</span></span>

<span data-ttu-id="ff5cd-117">Primo componente di offset applicato alle coordinate di trama prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="ff5cd-117">The first offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="ff5cd-118">*Offset2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ff5cd-118">*Offset2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff5cd-119">Tipo: **int2**</span><span class="sxs-lookup"><span data-stu-id="ff5cd-119">Type: **int2**</span></span>

<span data-ttu-id="ff5cd-120">Secondo componente di offset applicato alle coordinate di trama prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="ff5cd-120">The second offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="ff5cd-121">*Offset3* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ff5cd-121">*Offset3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff5cd-122">Tipo: **int2**</span><span class="sxs-lookup"><span data-stu-id="ff5cd-122">Type: **int2**</span></span>

<span data-ttu-id="ff5cd-123">Terzo componente di offset applicato alle coordinate di trama prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="ff5cd-123">The third offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="ff5cd-124">*Offset4* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ff5cd-124">*Offset4* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff5cd-125">Tipo: **int2**</span><span class="sxs-lookup"><span data-stu-id="ff5cd-125">Type: **int2**</span></span>

<span data-ttu-id="ff5cd-126">Quarto componente di offset applicato alle coordinate di trama prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="ff5cd-126">The fourth offset component applied to the texture coordinates before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff5cd-127">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ff5cd-127">Return value</span></span>

<span data-ttu-id="ff5cd-128">Tipo: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="ff5cd-128">Type: **TemplateType**</span></span>

<span data-ttu-id="ff5cd-129">Valore a quattro componenti il cui tipo corrisponde al tipo di modello.</span><span class="sxs-lookup"><span data-stu-id="ff5cd-129">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff5cd-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="ff5cd-130">Remarks</span></span>

<span data-ttu-id="ff5cd-131">Gli esempi di trama possono essere usati per l'interpolazione bilineare.</span><span class="sxs-lookup"><span data-stu-id="ff5cd-131">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="ff5cd-132">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="ff5cd-132">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="ff5cd-133">Vertice</span><span class="sxs-lookup"><span data-stu-id="ff5cd-133">Vertex</span></span> | <span data-ttu-id="ff5cd-134">Hull</span><span class="sxs-lookup"><span data-stu-id="ff5cd-134">Hull</span></span> | <span data-ttu-id="ff5cd-135">Dominio</span><span class="sxs-lookup"><span data-stu-id="ff5cd-135">Domain</span></span> | <span data-ttu-id="ff5cd-136">Geometria</span><span class="sxs-lookup"><span data-stu-id="ff5cd-136">Geometry</span></span> | <span data-ttu-id="ff5cd-137">Pixel</span><span class="sxs-lookup"><span data-stu-id="ff5cd-137">Pixel</span></span> | <span data-ttu-id="ff5cd-138">Calcolo</span><span class="sxs-lookup"><span data-stu-id="ff5cd-138">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="ff5cd-139">x</span><span class="sxs-lookup"><span data-stu-id="ff5cd-139">x</span></span>      | <span data-ttu-id="ff5cd-140">x</span><span class="sxs-lookup"><span data-stu-id="ff5cd-140">x</span></span>    | <span data-ttu-id="ff5cd-141">x</span><span class="sxs-lookup"><span data-stu-id="ff5cd-141">x</span></span>      | <span data-ttu-id="ff5cd-142">x</span><span class="sxs-lookup"><span data-stu-id="ff5cd-142">x</span></span>        | <span data-ttu-id="ff5cd-143">x</span><span class="sxs-lookup"><span data-stu-id="ff5cd-143">x</span></span>     | <span data-ttu-id="ff5cd-144">x</span><span class="sxs-lookup"><span data-stu-id="ff5cd-144">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="ff5cd-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ff5cd-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff5cd-146">Metodi GatherBlue</span><span class="sxs-lookup"><span data-stu-id="ff5cd-146">GatherBlue methods</span></span>](texture2d-gatherblue.md)
</dt> </dl>

 

 




