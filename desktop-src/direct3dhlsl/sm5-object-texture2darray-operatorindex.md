---
title: 'Funzione Texture2DArray:: operator'
description: 'Restituisce una variabile di risorsa di sola lettura. | Funzione Texture2DArray:: operator'
ms.assetid: eb6ff496-c46f-405f-a172-ab747415a2f9
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
ms.openlocfilehash: 1b86aad839fbf28a4fc666b3a5fe5c5788b7b3ae
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104058500"
---
# <a name="texture2darrayoperator--function"></a><span data-ttu-id="a057b-105">Funzione Texture2DArray:: operator</span><span class="sxs-lookup"><span data-stu-id="a057b-105">Texture2DArray::Operator  function</span></span>

<span data-ttu-id="a057b-106">Restituisce una variabile di risorsa di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="a057b-106">Returns a read-only resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="a057b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a057b-107">Syntax</span></span>

``` syntax
R Operator[](
  in uint3 pos
);
```

## <a name="parameters"></a><span data-ttu-id="a057b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a057b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a057b-109">*pos* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a057b-109">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a057b-110">Tipo: **uint3**</span><span class="sxs-lookup"><span data-stu-id="a057b-110">Type: **uint3**</span></span>

<span data-ttu-id="a057b-111">Posizione dell'indice.</span><span class="sxs-lookup"><span data-stu-id="a057b-111">The index position.</span></span> <span data-ttu-id="a057b-112">Il primo e il secondo componente contengono le coordinate (x, y).</span><span class="sxs-lookup"><span data-stu-id="a057b-112">The first and second components contain the (x, y) coordinates.</span></span> <span data-ttu-id="a057b-113">Il terzo componente indica la sezione della matrice desiderata.</span><span class="sxs-lookup"><span data-stu-id="a057b-113">The third component indicates the desired array slice.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a057b-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a057b-114">Return value</span></span>

<span data-ttu-id="a057b-115">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="a057b-115">Type: **R**</span></span>

<span data-ttu-id="a057b-116">Variabile di sola lettura di una risorsa.</span><span class="sxs-lookup"><span data-stu-id="a057b-116">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="a057b-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="a057b-117">Remarks</span></span>

<span data-ttu-id="a057b-118">Questo metodo accede sempre al primo livello MIP.</span><span class="sxs-lookup"><span data-stu-id="a057b-118">This method always accesses the first mip level.</span></span> <span data-ttu-id="a057b-119">Per specificare altri livelli MIP, usare invece il metodo [**MIP \[ \] \[ \] . operator**](sm5-object-texture2darray-mipsoperatorindex.md) .</span><span class="sxs-lookup"><span data-stu-id="a057b-119">To specify other mip levels, use the [**mip.operator\[\]\[\]**](sm5-object-texture2darray-mipsoperatorindex.md) method instead.</span></span>

<span data-ttu-id="a057b-120">Gli esempi di trama possono essere usati per l'interpolazione bilineare.</span><span class="sxs-lookup"><span data-stu-id="a057b-120">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="a057b-121">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="a057b-121">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="a057b-122">Vertice</span><span class="sxs-lookup"><span data-stu-id="a057b-122">Vertex</span></span> | <span data-ttu-id="a057b-123">Hull</span><span class="sxs-lookup"><span data-stu-id="a057b-123">Hull</span></span> | <span data-ttu-id="a057b-124">Dominio</span><span class="sxs-lookup"><span data-stu-id="a057b-124">Domain</span></span> | <span data-ttu-id="a057b-125">Geometria</span><span class="sxs-lookup"><span data-stu-id="a057b-125">Geometry</span></span> | <span data-ttu-id="a057b-126">Pixel</span><span class="sxs-lookup"><span data-stu-id="a057b-126">Pixel</span></span> | <span data-ttu-id="a057b-127">Calcolo</span><span class="sxs-lookup"><span data-stu-id="a057b-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="a057b-128">x</span><span class="sxs-lookup"><span data-stu-id="a057b-128">x</span></span>      | <span data-ttu-id="a057b-129">x</span><span class="sxs-lookup"><span data-stu-id="a057b-129">x</span></span>    | <span data-ttu-id="a057b-130">x</span><span class="sxs-lookup"><span data-stu-id="a057b-130">x</span></span>      | <span data-ttu-id="a057b-131">x</span><span class="sxs-lookup"><span data-stu-id="a057b-131">x</span></span>        | <span data-ttu-id="a057b-132">x</span><span class="sxs-lookup"><span data-stu-id="a057b-132">x</span></span>     | <span data-ttu-id="a057b-133">x</span><span class="sxs-lookup"><span data-stu-id="a057b-133">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="a057b-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a057b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a057b-135">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="a057b-135">Texture2DArray</span></span>](sm5-object-texture2darray.md)
</dt> <dt>

[<span data-ttu-id="a057b-136">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="a057b-136">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




