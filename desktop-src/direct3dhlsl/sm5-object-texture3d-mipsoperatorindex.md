---
title: 'Texture3D:: MIPS. Funzione operator'
description: 'Restituisce una variabile di risorsa di sola lettura. | Texture3D:: MIPS. Funzione operator'
ms.assetid: d5f6cb3b-4163-44c2-8379-ac8a412b1aa6
keywords:
- MIPS. Funzione operator HLSL
topic_type:
- apiref
api_name:
- mips.Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e8f7064459354ec4827ba6d96795e82ccab3800c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104234693"
---
# <a name="texture3dmipsoperator----function"></a><span data-ttu-id="bf8d8-105">Texture3D:: MIPS. Funzione operator</span><span class="sxs-lookup"><span data-stu-id="bf8d8-105">Texture3D::mips.Operator    function</span></span>

<span data-ttu-id="bf8d8-106">Restituisce una variabile di risorsa di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="bf8d8-106">Returns a read-only resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf8d8-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bf8d8-107">Syntax</span></span>

``` syntax
R mips.Operator[][](
  in uint mipSlice,
  in uint3 pos
);
```

## <a name="parameters"></a><span data-ttu-id="bf8d8-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="bf8d8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf8d8-109">*mipSlice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bf8d8-109">*mipSlice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf8d8-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="bf8d8-110">Type: **uint**</span></span>

<span data-ttu-id="bf8d8-111">Indice della sezione MIP.</span><span class="sxs-lookup"><span data-stu-id="bf8d8-111">The mip slice index.</span></span>

</dd> <dt>

<span data-ttu-id="bf8d8-112">*pos* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bf8d8-112">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf8d8-113">Tipo: **uint3**</span><span class="sxs-lookup"><span data-stu-id="bf8d8-113">Type: **uint3**</span></span>

<span data-ttu-id="bf8d8-114">Posizione dell'indice.</span><span class="sxs-lookup"><span data-stu-id="bf8d8-114">The index position.</span></span> <span data-ttu-id="bf8d8-115">Contiene le coordinate (x, y, z).</span><span class="sxs-lookup"><span data-stu-id="bf8d8-115">Contains the (x, y, z) coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf8d8-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bf8d8-116">Return value</span></span>

<span data-ttu-id="bf8d8-117">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="bf8d8-117">Type: **R**</span></span>

<span data-ttu-id="bf8d8-118">Variabile di sola lettura di una risorsa.</span><span class="sxs-lookup"><span data-stu-id="bf8d8-118">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf8d8-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="bf8d8-119">Remarks</span></span>

### <a name="usage-example"></a><span data-ttu-id="bf8d8-120">Esempio di utilizzo</span><span class="sxs-lookup"><span data-stu-id="bf8d8-120">Usage Example</span></span>


```
Texture3D<float4> tex;
uint mip = 2;
uint3 pos_xyz = {123, 456, 789};
float4 f = tex.mips[mip][pos_xyz];
        
```



<span data-ttu-id="bf8d8-121">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="bf8d8-121">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="bf8d8-122">Vertice</span><span class="sxs-lookup"><span data-stu-id="bf8d8-122">Vertex</span></span> | <span data-ttu-id="bf8d8-123">Hull</span><span class="sxs-lookup"><span data-stu-id="bf8d8-123">Hull</span></span> | <span data-ttu-id="bf8d8-124">Dominio</span><span class="sxs-lookup"><span data-stu-id="bf8d8-124">Domain</span></span> | <span data-ttu-id="bf8d8-125">Geometria</span><span class="sxs-lookup"><span data-stu-id="bf8d8-125">Geometry</span></span> | <span data-ttu-id="bf8d8-126">Pixel</span><span class="sxs-lookup"><span data-stu-id="bf8d8-126">Pixel</span></span> | <span data-ttu-id="bf8d8-127">Calcolo</span><span class="sxs-lookup"><span data-stu-id="bf8d8-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="bf8d8-128">x</span><span class="sxs-lookup"><span data-stu-id="bf8d8-128">x</span></span>      | <span data-ttu-id="bf8d8-129">x</span><span class="sxs-lookup"><span data-stu-id="bf8d8-129">x</span></span>    | <span data-ttu-id="bf8d8-130">x</span><span class="sxs-lookup"><span data-stu-id="bf8d8-130">x</span></span>      | <span data-ttu-id="bf8d8-131">x</span><span class="sxs-lookup"><span data-stu-id="bf8d8-131">x</span></span>        | <span data-ttu-id="bf8d8-132">x</span><span class="sxs-lookup"><span data-stu-id="bf8d8-132">x</span></span>     | <span data-ttu-id="bf8d8-133">x</span><span class="sxs-lookup"><span data-stu-id="bf8d8-133">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="bf8d8-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bf8d8-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf8d8-135">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf8d8-135">Texture3D</span></span>](sm5-object-texture3d.md)
</dt> <dt>

[<span data-ttu-id="bf8d8-136">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="bf8d8-136">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




