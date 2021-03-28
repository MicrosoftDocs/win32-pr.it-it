---
title: 'Texture1DArray:: MIPS. Funzione operator'
description: 'Restituisce una variabile di risorsa di sola lettura. | Texture1DArray:: MIPS. Funzione operator'
ms.assetid: b8f2ef78-4b50-4051-a00f-5b81cd77d1e0
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
ms.openlocfilehash: cbe2d1116839cede8dda69f1b0b8cf9a049595e9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104058538"
---
# <a name="texture1darraymipsoperator----function"></a><span data-ttu-id="89de9-105">Texture1DArray:: MIPS. Funzione operator</span><span class="sxs-lookup"><span data-stu-id="89de9-105">Texture1DArray::mips.Operator    function</span></span>

<span data-ttu-id="89de9-106">Restituisce una variabile di risorsa di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="89de9-106">Returns a read-only resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="89de9-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="89de9-107">Syntax</span></span>

``` syntax
R mips.Operator[][](
  in uint mipSlice,
  in uint2 pos
);
```

## <a name="parameters"></a><span data-ttu-id="89de9-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="89de9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89de9-109">*mipSlice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="89de9-109">*mipSlice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89de9-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="89de9-110">Type: **uint**</span></span>

<span data-ttu-id="89de9-111">Indice della sezione MIP.</span><span class="sxs-lookup"><span data-stu-id="89de9-111">The mip slice index.</span></span>

</dd> <dt>

<span data-ttu-id="89de9-112">*pos* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="89de9-112">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89de9-113">Tipo: **uint2**</span><span class="sxs-lookup"><span data-stu-id="89de9-113">Type: **uint2**</span></span>

<span data-ttu-id="89de9-114">Posizione dell'indice.</span><span class="sxs-lookup"><span data-stu-id="89de9-114">The index position.</span></span> <span data-ttu-id="89de9-115">Il primo componente contiene la coordinata x.</span><span class="sxs-lookup"><span data-stu-id="89de9-115">The first component contains the x-coordinate.</span></span> <span data-ttu-id="89de9-116">Il secondo componente indica la sezione della matrice desiderata.</span><span class="sxs-lookup"><span data-stu-id="89de9-116">The second component indicates the desired array slice.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89de9-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="89de9-117">Return value</span></span>

<span data-ttu-id="89de9-118">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="89de9-118">Type: **R**</span></span>

<span data-ttu-id="89de9-119">Variabile di sola lettura di una risorsa.</span><span class="sxs-lookup"><span data-stu-id="89de9-119">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="89de9-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="89de9-120">Remarks</span></span>

### <a name="usage-example"></a><span data-ttu-id="89de9-121">Esempio di utilizzo</span><span class="sxs-lookup"><span data-stu-id="89de9-121">Usage Example</span></span>


```
Texture1DArray<float4> tex;
uint mip = 2;
uint2 pos_x_and_array = {1234, 3};
float4 f = tex.mips[mip][pos_x_and_array];        
        
```



<span data-ttu-id="89de9-122">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="89de9-122">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="89de9-123">Vertice</span><span class="sxs-lookup"><span data-stu-id="89de9-123">Vertex</span></span> | <span data-ttu-id="89de9-124">Hull</span><span class="sxs-lookup"><span data-stu-id="89de9-124">Hull</span></span> | <span data-ttu-id="89de9-125">Dominio</span><span class="sxs-lookup"><span data-stu-id="89de9-125">Domain</span></span> | <span data-ttu-id="89de9-126">Geometria</span><span class="sxs-lookup"><span data-stu-id="89de9-126">Geometry</span></span> | <span data-ttu-id="89de9-127">Pixel</span><span class="sxs-lookup"><span data-stu-id="89de9-127">Pixel</span></span> | <span data-ttu-id="89de9-128">Calcolo</span><span class="sxs-lookup"><span data-stu-id="89de9-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="89de9-129">x</span><span class="sxs-lookup"><span data-stu-id="89de9-129">x</span></span>      | <span data-ttu-id="89de9-130">x</span><span class="sxs-lookup"><span data-stu-id="89de9-130">x</span></span>    | <span data-ttu-id="89de9-131">x</span><span class="sxs-lookup"><span data-stu-id="89de9-131">x</span></span>      | <span data-ttu-id="89de9-132">x</span><span class="sxs-lookup"><span data-stu-id="89de9-132">x</span></span>        | <span data-ttu-id="89de9-133">x</span><span class="sxs-lookup"><span data-stu-id="89de9-133">x</span></span>     | <span data-ttu-id="89de9-134">x</span><span class="sxs-lookup"><span data-stu-id="89de9-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="89de9-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="89de9-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89de9-136">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="89de9-136">Texture1DArray</span></span>](sm5-object-texture1darray.md)
</dt> <dt>

[<span data-ttu-id="89de9-137">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="89de9-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




