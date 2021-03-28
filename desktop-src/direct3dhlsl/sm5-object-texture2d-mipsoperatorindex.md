---
title: 'Texture2D:: MIPS. Funzione operator'
description: 'Restituisce una variabile di risorsa di sola lettura. | Texture2D:: MIPS. Funzione operator'
ms.assetid: 201996a7-741f-4457-ab77-9cd653f3682b
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
ms.openlocfilehash: 994ede49563b1d4e568769be48a0e60592fe3dde
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981170"
---
# <a name="texture2dmipsoperator----function"></a><span data-ttu-id="fcbbe-105">Texture2D:: MIPS. Funzione operator</span><span class="sxs-lookup"><span data-stu-id="fcbbe-105">Texture2D::mips.Operator    function</span></span>

<span data-ttu-id="fcbbe-106">Restituisce una variabile di risorsa di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="fcbbe-106">Returns a read-only resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="fcbbe-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fcbbe-107">Syntax</span></span>

``` syntax
R mips.Operator[][](
  in uint mipSlice,
  in uint2 pos
);
```

## <a name="parameters"></a><span data-ttu-id="fcbbe-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="fcbbe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fcbbe-109">*mipSlice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fcbbe-109">*mipSlice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcbbe-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="fcbbe-110">Type: **uint**</span></span>

<span data-ttu-id="fcbbe-111">Indice della sezione MIP.</span><span class="sxs-lookup"><span data-stu-id="fcbbe-111">The mip slice index.</span></span>

</dd> <dt>

<span data-ttu-id="fcbbe-112">*pos* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fcbbe-112">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcbbe-113">Tipo: **uint2**</span><span class="sxs-lookup"><span data-stu-id="fcbbe-113">Type: **uint2**</span></span>

<span data-ttu-id="fcbbe-114">Posizione dell'indice.</span><span class="sxs-lookup"><span data-stu-id="fcbbe-114">The index position.</span></span> <span data-ttu-id="fcbbe-115">Contiene le coordinate (x, y).</span><span class="sxs-lookup"><span data-stu-id="fcbbe-115">Contains the (x, y) coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fcbbe-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fcbbe-116">Return value</span></span>

<span data-ttu-id="fcbbe-117">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="fcbbe-117">Type: **R**</span></span>

<span data-ttu-id="fcbbe-118">Variabile di sola lettura di una risorsa.</span><span class="sxs-lookup"><span data-stu-id="fcbbe-118">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="fcbbe-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="fcbbe-119">Remarks</span></span>

### <a name="usage-example"></a><span data-ttu-id="fcbbe-120">Esempio di utilizzo</span><span class="sxs-lookup"><span data-stu-id="fcbbe-120">Usage Example</span></span>


```
Texture2D<float4> tex;
uint mip = 2;
uint2 pos_xy = {123, 456};
float4 f = tex.mips[mip][pos_xy];
        
```



<span data-ttu-id="fcbbe-121">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="fcbbe-121">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="fcbbe-122">Vertice</span><span class="sxs-lookup"><span data-stu-id="fcbbe-122">Vertex</span></span> | <span data-ttu-id="fcbbe-123">Hull</span><span class="sxs-lookup"><span data-stu-id="fcbbe-123">Hull</span></span> | <span data-ttu-id="fcbbe-124">Dominio</span><span class="sxs-lookup"><span data-stu-id="fcbbe-124">Domain</span></span> | <span data-ttu-id="fcbbe-125">Geometria</span><span class="sxs-lookup"><span data-stu-id="fcbbe-125">Geometry</span></span> | <span data-ttu-id="fcbbe-126">Pixel</span><span class="sxs-lookup"><span data-stu-id="fcbbe-126">Pixel</span></span> | <span data-ttu-id="fcbbe-127">Calcolo</span><span class="sxs-lookup"><span data-stu-id="fcbbe-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="fcbbe-128">x</span><span class="sxs-lookup"><span data-stu-id="fcbbe-128">x</span></span>      | <span data-ttu-id="fcbbe-129">x</span><span class="sxs-lookup"><span data-stu-id="fcbbe-129">x</span></span>    | <span data-ttu-id="fcbbe-130">x</span><span class="sxs-lookup"><span data-stu-id="fcbbe-130">x</span></span>      | <span data-ttu-id="fcbbe-131">x</span><span class="sxs-lookup"><span data-stu-id="fcbbe-131">x</span></span>        | <span data-ttu-id="fcbbe-132">x</span><span class="sxs-lookup"><span data-stu-id="fcbbe-132">x</span></span>     | <span data-ttu-id="fcbbe-133">x</span><span class="sxs-lookup"><span data-stu-id="fcbbe-133">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="fcbbe-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fcbbe-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fcbbe-135">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fcbbe-135">Texture2D</span></span>](sm5-object-texture2d.md)
</dt> <dt>

[<span data-ttu-id="fcbbe-136">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="fcbbe-136">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




