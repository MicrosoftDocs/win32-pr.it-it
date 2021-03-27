---
title: 'Funzione Texture1DArray:: operator'
description: 'Restituisce una variabile di risorsa di sola lettura. | Funzione Texture1DArray:: operator'
ms.assetid: 05ec9652-b5dd-41cf-8bef-730c507c5ba4
keywords:
- Funzione operator HLSL
topic_type:
- apiref
api_name:
- Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 578d778cd1e0e064c435c19fb094feb66f651e05
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981631"
---
# <a name="texture1darrayoperator--function"></a><span data-ttu-id="a0351-105">Funzione Texture1DArray:: operator</span><span class="sxs-lookup"><span data-stu-id="a0351-105">Texture1DArray::Operator  function</span></span>

<span data-ttu-id="a0351-106">Restituisce una variabile di risorsa di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="a0351-106">Returns a read-only resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0351-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a0351-107">Syntax</span></span>

``` syntax
R Operator[](
  in uint2 pos
);
```

## <a name="parameters"></a><span data-ttu-id="a0351-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a0351-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0351-109">*pos* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a0351-109">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0351-110">Tipo: **uint2**</span><span class="sxs-lookup"><span data-stu-id="a0351-110">Type: **uint2**</span></span>

<span data-ttu-id="a0351-111">Posizione dell'indice.</span><span class="sxs-lookup"><span data-stu-id="a0351-111">The index position.</span></span> <span data-ttu-id="a0351-112">Il primo componente contiene la coordinata x.</span><span class="sxs-lookup"><span data-stu-id="a0351-112">The first component contains the x-coordinate.</span></span> <span data-ttu-id="a0351-113">Il secondo componente indica la sezione della matrice desiderata.</span><span class="sxs-lookup"><span data-stu-id="a0351-113">The second component indicates the desired array slice.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0351-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a0351-114">Return value</span></span>

<span data-ttu-id="a0351-115">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="a0351-115">Type: **R**</span></span>

<span data-ttu-id="a0351-116">Variabile di sola lettura di una risorsa.</span><span class="sxs-lookup"><span data-stu-id="a0351-116">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0351-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="a0351-117">Remarks</span></span>

<span data-ttu-id="a0351-118">Questo metodo accede sempre al primo livello MIP.</span><span class="sxs-lookup"><span data-stu-id="a0351-118">This method always accesses the first mip level.</span></span> <span data-ttu-id="a0351-119">Per specificare altri livelli MIP, usare invece il metodo [**MIP \[ \] \[ \] . operator**](sm5-object-texture1darray-mipsoperatorindex.md) .</span><span class="sxs-lookup"><span data-stu-id="a0351-119">To specify other mip levels, use the [**mip.operator\[\]\[\]**](sm5-object-texture1darray-mipsoperatorindex.md) method instead.</span></span>

<span data-ttu-id="a0351-120">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="a0351-120">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="a0351-121">Vertice</span><span class="sxs-lookup"><span data-stu-id="a0351-121">Vertex</span></span> | <span data-ttu-id="a0351-122">Hull</span><span class="sxs-lookup"><span data-stu-id="a0351-122">Hull</span></span> | <span data-ttu-id="a0351-123">Dominio</span><span class="sxs-lookup"><span data-stu-id="a0351-123">Domain</span></span> | <span data-ttu-id="a0351-124">Geometria</span><span class="sxs-lookup"><span data-stu-id="a0351-124">Geometry</span></span> | <span data-ttu-id="a0351-125">Pixel</span><span class="sxs-lookup"><span data-stu-id="a0351-125">Pixel</span></span> | <span data-ttu-id="a0351-126">Calcolo</span><span class="sxs-lookup"><span data-stu-id="a0351-126">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="a0351-127">x</span><span class="sxs-lookup"><span data-stu-id="a0351-127">x</span></span>      | <span data-ttu-id="a0351-128">x</span><span class="sxs-lookup"><span data-stu-id="a0351-128">x</span></span>    | <span data-ttu-id="a0351-129">x</span><span class="sxs-lookup"><span data-stu-id="a0351-129">x</span></span>      | <span data-ttu-id="a0351-130">x</span><span class="sxs-lookup"><span data-stu-id="a0351-130">x</span></span>        | <span data-ttu-id="a0351-131">x</span><span class="sxs-lookup"><span data-stu-id="a0351-131">x</span></span>     | <span data-ttu-id="a0351-132">x</span><span class="sxs-lookup"><span data-stu-id="a0351-132">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="a0351-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a0351-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0351-134">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="a0351-134">Texture1DArray</span></span>](sm5-object-texture1darray.md)
</dt> <dt>

[<span data-ttu-id="a0351-135">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="a0351-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




