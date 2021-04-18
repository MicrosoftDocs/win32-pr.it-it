---
title: 'Texture2DMSArray:: Sample. Funzione operator'
description: 'Restituisce una variabile di risorsa di sola lettura. | Texture2DMSArray:: Sample. Funzione operator'
ms.assetid: 5334c1d5-dfbd-4987-875c-0b92967b0f13
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
ms.openlocfilehash: e78746e0afe03e65a313982ca35c27a75ea14f1b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104982004"
---
# <a name="texture2dmsarraysampleoperator----function"></a><span data-ttu-id="2b7c4-105">Texture2DMSArray:: Sample. Funzione operator</span><span class="sxs-lookup"><span data-stu-id="2b7c4-105">Texture2DMSArray::sample.Operator    function</span></span>

<span data-ttu-id="2b7c4-106">Restituisce una variabile di risorsa di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="2b7c4-106">Returns a read-only resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b7c4-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2b7c4-107">Syntax</span></span>

``` syntax
R sample.Operator[][](
  in uint sampleSlice,
  in uint3 pos
);
```

## <a name="parameters"></a><span data-ttu-id="2b7c4-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="2b7c4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b7c4-109">*sampleSlice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2b7c4-109">*sampleSlice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b7c4-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="2b7c4-110">Type: **uint**</span></span>

<span data-ttu-id="2b7c4-111">Indice della sezione di esempio.</span><span class="sxs-lookup"><span data-stu-id="2b7c4-111">The sample slice index.</span></span>

</dd> <dt>

<span data-ttu-id="2b7c4-112">*pos* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2b7c4-112">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b7c4-113">Tipo: **uint3**</span><span class="sxs-lookup"><span data-stu-id="2b7c4-113">Type: **uint3**</span></span>

<span data-ttu-id="2b7c4-114">Posizione dell'indice.</span><span class="sxs-lookup"><span data-stu-id="2b7c4-114">The index position.</span></span> <span data-ttu-id="2b7c4-115">Il primo e il secondo componente contengono le coordinate (x, y).</span><span class="sxs-lookup"><span data-stu-id="2b7c4-115">The first and second components contain the (x, y) coordinates.</span></span> <span data-ttu-id="2b7c4-116">Il terzo componente indica la sezione della matrice desiderata.</span><span class="sxs-lookup"><span data-stu-id="2b7c4-116">The third component indicates the desired array slice.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b7c4-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2b7c4-117">Return value</span></span>

<span data-ttu-id="2b7c4-118">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="2b7c4-118">Type: **R**</span></span>

<span data-ttu-id="2b7c4-119">Variabile di sola lettura di una risorsa.</span><span class="sxs-lookup"><span data-stu-id="2b7c4-119">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b7c4-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="2b7c4-120">Remarks</span></span>

### <a name="usage-example"></a><span data-ttu-id="2b7c4-121">Esempio di utilizzo</span><span class="sxs-lookup"><span data-stu-id="2b7c4-121">Usage Example</span></span>


```
Texture2DMSArray<float4, 4> alpha;

float4 main( float3 tcoord : texturecoord0 ) : SV_Target
{
     return s_msTexture.sample[2][tcoord];
}
```



<span data-ttu-id="2b7c4-122">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="2b7c4-122">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="2b7c4-123">Vertice</span><span class="sxs-lookup"><span data-stu-id="2b7c4-123">Vertex</span></span> | <span data-ttu-id="2b7c4-124">Hull</span><span class="sxs-lookup"><span data-stu-id="2b7c4-124">Hull</span></span> | <span data-ttu-id="2b7c4-125">Dominio</span><span class="sxs-lookup"><span data-stu-id="2b7c4-125">Domain</span></span> | <span data-ttu-id="2b7c4-126">Geometria</span><span class="sxs-lookup"><span data-stu-id="2b7c4-126">Geometry</span></span> | <span data-ttu-id="2b7c4-127">Pixel</span><span class="sxs-lookup"><span data-stu-id="2b7c4-127">Pixel</span></span> | <span data-ttu-id="2b7c4-128">Calcolo</span><span class="sxs-lookup"><span data-stu-id="2b7c4-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="2b7c4-129">x</span><span class="sxs-lookup"><span data-stu-id="2b7c4-129">x</span></span>      | <span data-ttu-id="2b7c4-130">x</span><span class="sxs-lookup"><span data-stu-id="2b7c4-130">x</span></span>    | <span data-ttu-id="2b7c4-131">x</span><span class="sxs-lookup"><span data-stu-id="2b7c4-131">x</span></span>      | <span data-ttu-id="2b7c4-132">x</span><span class="sxs-lookup"><span data-stu-id="2b7c4-132">x</span></span>        | <span data-ttu-id="2b7c4-133">x</span><span class="sxs-lookup"><span data-stu-id="2b7c4-133">x</span></span>     | <span data-ttu-id="2b7c4-134">x</span><span class="sxs-lookup"><span data-stu-id="2b7c4-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="2b7c4-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2b7c4-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b7c4-136">Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="2b7c4-136">Texture2DMSArray</span></span>](sm5-object-texture2dmsarray.md)
</dt> <dt>

[<span data-ttu-id="2b7c4-137">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="2b7c4-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




