---
title: 'Funzione Texture3D:: operator'
description: 'Restituisce una variabile di risorsa di sola lettura. | Funzione Texture3D:: operator'
ms.assetid: d7e27778-6a96-47f8-a58a-1966452adf04
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
ms.openlocfilehash: 5c3bb3718094ee859d1e33a046fde7016973a0aa
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103761723"
---
# <a name="texture3doperator--function"></a><span data-ttu-id="15018-105">Funzione Texture3D:: operator</span><span class="sxs-lookup"><span data-stu-id="15018-105">Texture3D::Operator  function</span></span>

<span data-ttu-id="15018-106">Restituisce una variabile di risorsa di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="15018-106">Returns a read-only resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="15018-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="15018-107">Syntax</span></span>

``` syntax
R Operator[](
  in uint3 pos
);
```

## <a name="parameters"></a><span data-ttu-id="15018-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="15018-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15018-109">*pos* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="15018-109">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15018-110">Tipo: **uint3**</span><span class="sxs-lookup"><span data-stu-id="15018-110">Type: **uint3**</span></span>

<span data-ttu-id="15018-111">Posizione dell'indice.</span><span class="sxs-lookup"><span data-stu-id="15018-111">The index position.</span></span> <span data-ttu-id="15018-112">Contiene le coordinate (x, y, z).</span><span class="sxs-lookup"><span data-stu-id="15018-112">Contains the (x, y, z) coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15018-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="15018-113">Return value</span></span>

<span data-ttu-id="15018-114">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="15018-114">Type: **R**</span></span>

<span data-ttu-id="15018-115">Variabile di sola lettura di una risorsa.</span><span class="sxs-lookup"><span data-stu-id="15018-115">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="15018-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="15018-116">Remarks</span></span>

<span data-ttu-id="15018-117">Questo metodo accede sempre al primo livello MIP.</span><span class="sxs-lookup"><span data-stu-id="15018-117">This method always accesses the first mip level.</span></span> <span data-ttu-id="15018-118">Per specificare altri livelli MIP, usare invece l' [**operatore \[ \] \[ \] MIP.**](sm5-object-texture3d-mipsoperatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="15018-118">To specify other mip levels use the [**mip.operator\[\]\[\]**](sm5-object-texture3d-mipsoperatorindex.md) instead.</span></span>

<span data-ttu-id="15018-119">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="15018-119">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="15018-120">Vertice</span><span class="sxs-lookup"><span data-stu-id="15018-120">Vertex</span></span> | <span data-ttu-id="15018-121">Hull</span><span class="sxs-lookup"><span data-stu-id="15018-121">Hull</span></span> | <span data-ttu-id="15018-122">Dominio</span><span class="sxs-lookup"><span data-stu-id="15018-122">Domain</span></span> | <span data-ttu-id="15018-123">Geometria</span><span class="sxs-lookup"><span data-stu-id="15018-123">Geometry</span></span> | <span data-ttu-id="15018-124">Pixel</span><span class="sxs-lookup"><span data-stu-id="15018-124">Pixel</span></span> | <span data-ttu-id="15018-125">Calcolo</span><span class="sxs-lookup"><span data-stu-id="15018-125">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="15018-126">x</span><span class="sxs-lookup"><span data-stu-id="15018-126">x</span></span>      | <span data-ttu-id="15018-127">x</span><span class="sxs-lookup"><span data-stu-id="15018-127">x</span></span>    | <span data-ttu-id="15018-128">x</span><span class="sxs-lookup"><span data-stu-id="15018-128">x</span></span>      | <span data-ttu-id="15018-129">x</span><span class="sxs-lookup"><span data-stu-id="15018-129">x</span></span>        | <span data-ttu-id="15018-130">x</span><span class="sxs-lookup"><span data-stu-id="15018-130">x</span></span>     | <span data-ttu-id="15018-131">x</span><span class="sxs-lookup"><span data-stu-id="15018-131">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="15018-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="15018-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15018-133">Texture3D</span><span class="sxs-lookup"><span data-stu-id="15018-133">Texture3D</span></span>](sm5-object-texture3d.md)
</dt> <dt>

[<span data-ttu-id="15018-134">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="15018-134">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




