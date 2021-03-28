---
title: 'Texture2DMS:: Sample. Funzione operator'
description: "Recupera un valore dalla risorsa nella posizione e nell'indice di esempio forniti. | Texture2DMS:: Sample. Funzione operator"
ms.assetid: 5bc24129-b690-44dd-ae85-8533b10befaa
keywords:
- esempio. Funzione operator HLSL
topic_type:
- apiref
api_name:
- sample.Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1a73577fa67992b212b4769059f1523e584acbaf
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104234885"
---
# <a name="texture2dmssampleoperator----function"></a><span data-ttu-id="3fd50-105">Texture2DMS:: Sample. Funzione operator</span><span class="sxs-lookup"><span data-stu-id="3fd50-105">Texture2DMS::sample.Operator    function</span></span>

<span data-ttu-id="3fd50-106">Recupera un valore dalla risorsa nella posizione e nell'indice di esempio forniti.</span><span class="sxs-lookup"><span data-stu-id="3fd50-106">Retrieves a value from the resource at the location and sample index provided.</span></span>

## <a name="syntax"></a><span data-ttu-id="3fd50-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3fd50-107">Syntax</span></span>

``` syntax
R sample.Operator[][](
  in uint sampleSlice,
  in uint2 pos
);
```

## <a name="parameters"></a><span data-ttu-id="3fd50-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="3fd50-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3fd50-109">*sampleSlice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3fd50-109">*sampleSlice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3fd50-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="3fd50-110">Type: **uint**</span></span>

<span data-ttu-id="3fd50-111">Indice della sezione di esempio.</span><span class="sxs-lookup"><span data-stu-id="3fd50-111">The sample slice index.</span></span>

</dd> <dt>

<span data-ttu-id="3fd50-112">*pos* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3fd50-112">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3fd50-113">Tipo: **uint2**</span><span class="sxs-lookup"><span data-stu-id="3fd50-113">Type: **uint2**</span></span>

<span data-ttu-id="3fd50-114">Posizione dell'indice.</span><span class="sxs-lookup"><span data-stu-id="3fd50-114">The index position.</span></span> <span data-ttu-id="3fd50-115">I componenti contengono le coordinate (x, y).</span><span class="sxs-lookup"><span data-stu-id="3fd50-115">The components contain the (x, y) coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3fd50-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3fd50-116">Return value</span></span>

<span data-ttu-id="3fd50-117">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="3fd50-117">Type: **R**</span></span>

<span data-ttu-id="3fd50-118">Variabile di sola lettura di una risorsa.</span><span class="sxs-lookup"><span data-stu-id="3fd50-118">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="3fd50-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="3fd50-119">Remarks</span></span>

### <a name="usage-example"></a><span data-ttu-id="3fd50-120">Esempio di utilizzo</span><span class="sxs-lookup"><span data-stu-id="3fd50-120">Usage Example</span></span>


```
Texture2DMS<float4, 8> tex;

float4 main( float3 tcoord : texturecoord0 ) : SV_Target
{
     return s_msTexture.sample[2][tcoord];
}
```



<span data-ttu-id="3fd50-121">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="3fd50-121">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="3fd50-122">Vertice</span><span class="sxs-lookup"><span data-stu-id="3fd50-122">Vertex</span></span> | <span data-ttu-id="3fd50-123">Hull</span><span class="sxs-lookup"><span data-stu-id="3fd50-123">Hull</span></span> | <span data-ttu-id="3fd50-124">Dominio</span><span class="sxs-lookup"><span data-stu-id="3fd50-124">Domain</span></span> | <span data-ttu-id="3fd50-125">Geometria</span><span class="sxs-lookup"><span data-stu-id="3fd50-125">Geometry</span></span> | <span data-ttu-id="3fd50-126">Pixel</span><span class="sxs-lookup"><span data-stu-id="3fd50-126">Pixel</span></span> | <span data-ttu-id="3fd50-127">Calcolo</span><span class="sxs-lookup"><span data-stu-id="3fd50-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="3fd50-128">x</span><span class="sxs-lookup"><span data-stu-id="3fd50-128">x</span></span>      | <span data-ttu-id="3fd50-129">x</span><span class="sxs-lookup"><span data-stu-id="3fd50-129">x</span></span>    | <span data-ttu-id="3fd50-130">x</span><span class="sxs-lookup"><span data-stu-id="3fd50-130">x</span></span>      | <span data-ttu-id="3fd50-131">x</span><span class="sxs-lookup"><span data-stu-id="3fd50-131">x</span></span>        | <span data-ttu-id="3fd50-132">x</span><span class="sxs-lookup"><span data-stu-id="3fd50-132">x</span></span>     | <span data-ttu-id="3fd50-133">x</span><span class="sxs-lookup"><span data-stu-id="3fd50-133">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="3fd50-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3fd50-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fd50-135">Texture2DMS</span><span class="sxs-lookup"><span data-stu-id="3fd50-135">Texture2DMS</span></span>](sm5-object-texture2dms.md)
</dt> <dt>

[<span data-ttu-id="3fd50-136">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="3fd50-136">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




