---
title: 'Texture2DArray:: MIPS. Funzione operator'
description: 'Restituisce una variabile di risorsa di sola lettura. | Texture2DArray:: MIPS. Funzione operator'
ms.assetid: 66639bf6-74dd-4c69-9cc1-74cc9314de57
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
ms.openlocfilehash: 17f24dd54768f3583f508527b7e03f72399bf98e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103761825"
---
# <a name="texture2darraymipsoperator----function"></a><span data-ttu-id="060ca-105">Texture2DArray:: MIPS. Funzione operator</span><span class="sxs-lookup"><span data-stu-id="060ca-105">Texture2DArray::mips.Operator    function</span></span>

<span data-ttu-id="060ca-106">Restituisce una variabile di risorsa di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="060ca-106">Returns a read-only resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="060ca-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="060ca-107">Syntax</span></span>

``` syntax
R mips.Operator[][](
  in uint mipSlice,
  in uint3 pos
);
```

## <a name="parameters"></a><span data-ttu-id="060ca-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="060ca-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="060ca-109">*mipSlice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="060ca-109">*mipSlice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="060ca-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="060ca-110">Type: **uint**</span></span>

<span data-ttu-id="060ca-111">Indice della sezione MIP.</span><span class="sxs-lookup"><span data-stu-id="060ca-111">The mip slice index.</span></span>

</dd> <dt>

<span data-ttu-id="060ca-112">*pos* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="060ca-112">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="060ca-113">Tipo: **uint3**</span><span class="sxs-lookup"><span data-stu-id="060ca-113">Type: **uint3**</span></span>

<span data-ttu-id="060ca-114">Posizione dell'indice.</span><span class="sxs-lookup"><span data-stu-id="060ca-114">The index position.</span></span> <span data-ttu-id="060ca-115">Il primo e il secondo componente contengono le coordinate (x, y).</span><span class="sxs-lookup"><span data-stu-id="060ca-115">The first and second components contain the (x, y) coordinates.</span></span> <span data-ttu-id="060ca-116">Il terzo componente indica la sezione della matrice desiderata.</span><span class="sxs-lookup"><span data-stu-id="060ca-116">The third component indicates the desired array slice.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="060ca-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="060ca-117">Return value</span></span>

<span data-ttu-id="060ca-118">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="060ca-118">Type: **R**</span></span>

<span data-ttu-id="060ca-119">Variabile di sola lettura di una risorsa.</span><span class="sxs-lookup"><span data-stu-id="060ca-119">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="060ca-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="060ca-120">Remarks</span></span>

### <a name="usage-example"></a><span data-ttu-id="060ca-121">Esempio di utilizzo</span><span class="sxs-lookup"><span data-stu-id="060ca-121">Usage Example</span></span>


```
Texture2DArray<float4> tex;
uint mip = 2;
uint2 pos_xy_and_array = {123, 456, 3};
float4 f = tex.mips[mip][pos_xy_and_array];
        
```



<span data-ttu-id="060ca-122">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="060ca-122">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="060ca-123">Vertice</span><span class="sxs-lookup"><span data-stu-id="060ca-123">Vertex</span></span> | <span data-ttu-id="060ca-124">Hull</span><span class="sxs-lookup"><span data-stu-id="060ca-124">Hull</span></span> | <span data-ttu-id="060ca-125">Dominio</span><span class="sxs-lookup"><span data-stu-id="060ca-125">Domain</span></span> | <span data-ttu-id="060ca-126">Geometria</span><span class="sxs-lookup"><span data-stu-id="060ca-126">Geometry</span></span> | <span data-ttu-id="060ca-127">Pixel</span><span class="sxs-lookup"><span data-stu-id="060ca-127">Pixel</span></span> | <span data-ttu-id="060ca-128">Calcolo</span><span class="sxs-lookup"><span data-stu-id="060ca-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="060ca-129">x</span><span class="sxs-lookup"><span data-stu-id="060ca-129">x</span></span>      | <span data-ttu-id="060ca-130">x</span><span class="sxs-lookup"><span data-stu-id="060ca-130">x</span></span>    | <span data-ttu-id="060ca-131">x</span><span class="sxs-lookup"><span data-stu-id="060ca-131">x</span></span>      | <span data-ttu-id="060ca-132">x</span><span class="sxs-lookup"><span data-stu-id="060ca-132">x</span></span>        | <span data-ttu-id="060ca-133">x</span><span class="sxs-lookup"><span data-stu-id="060ca-133">x</span></span>     | <span data-ttu-id="060ca-134">x</span><span class="sxs-lookup"><span data-stu-id="060ca-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="060ca-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="060ca-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="060ca-136">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="060ca-136">Texture2DArray</span></span>](sm5-object-texture2darray.md)
</dt> <dt>

[<span data-ttu-id="060ca-137">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="060ca-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




