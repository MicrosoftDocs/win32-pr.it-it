---
title: 'Funzione Texture1D:: operator'
description: Restituisce una variabile di risorse di sola lettura per un Texture1D.
ms.assetid: df54097d-4d1b-496a-a17d-6e9a10cfb996
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
ms.openlocfilehash: 44e5b502c7ae8b766363956920d7922858b4d771
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104118822"
---
# <a name="texture1doperator--function"></a><span data-ttu-id="1d89e-104">Funzione Texture1D:: operator</span><span class="sxs-lookup"><span data-stu-id="1d89e-104">Texture1D::Operator  function</span></span>

<span data-ttu-id="1d89e-105">Restituisce una variabile di risorse di sola lettura per un [**Texture1D**](sm5-object-texture1d.md).</span><span class="sxs-lookup"><span data-stu-id="1d89e-105">Returns a read-only resource variable for a [**Texture1D**](sm5-object-texture1d.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="1d89e-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1d89e-106">Syntax</span></span>

``` syntax
R Operator[](
  in uint pos
);
```

## <a name="parameters"></a><span data-ttu-id="1d89e-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="1d89e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d89e-108">*pos* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1d89e-108">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d89e-109">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="1d89e-109">Type: **uint**</span></span>

<span data-ttu-id="1d89e-110">Posizione dell'indice.</span><span class="sxs-lookup"><span data-stu-id="1d89e-110">The index position.</span></span> <span data-ttu-id="1d89e-111">Contiene la coordinata x.</span><span class="sxs-lookup"><span data-stu-id="1d89e-111">Contains the x-coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d89e-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1d89e-112">Return value</span></span>

<span data-ttu-id="1d89e-113">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="1d89e-113">Type: **R**</span></span>

<span data-ttu-id="1d89e-114">Variabile di sola lettura di una risorsa.</span><span class="sxs-lookup"><span data-stu-id="1d89e-114">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d89e-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="1d89e-115">Remarks</span></span>

<span data-ttu-id="1d89e-116">Questo metodo accede sempre al primo livello MIP.</span><span class="sxs-lookup"><span data-stu-id="1d89e-116">This method always accesses the first mip level.</span></span> <span data-ttu-id="1d89e-117">Per specificare altri livelli MIP, usare invece l' [**\[ \] \[ \] operatore MIP.**](sm5-object-texture1d-mipsoperatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="1d89e-117">To specify other mip levels, use the [**mip.operator\[\]\[\]**](sm5-object-texture1d-mipsoperatorindex.md) instead.</span></span>

<span data-ttu-id="1d89e-118">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="1d89e-118">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="1d89e-119">Vertice</span><span class="sxs-lookup"><span data-stu-id="1d89e-119">Vertex</span></span> | <span data-ttu-id="1d89e-120">Hull</span><span class="sxs-lookup"><span data-stu-id="1d89e-120">Hull</span></span> | <span data-ttu-id="1d89e-121">Dominio</span><span class="sxs-lookup"><span data-stu-id="1d89e-121">Domain</span></span> | <span data-ttu-id="1d89e-122">Geometria</span><span class="sxs-lookup"><span data-stu-id="1d89e-122">Geometry</span></span> | <span data-ttu-id="1d89e-123">Pixel</span><span class="sxs-lookup"><span data-stu-id="1d89e-123">Pixel</span></span> | <span data-ttu-id="1d89e-124">Calcolo</span><span class="sxs-lookup"><span data-stu-id="1d89e-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="1d89e-125">x</span><span class="sxs-lookup"><span data-stu-id="1d89e-125">x</span></span>      | <span data-ttu-id="1d89e-126">x</span><span class="sxs-lookup"><span data-stu-id="1d89e-126">x</span></span>    | <span data-ttu-id="1d89e-127">x</span><span class="sxs-lookup"><span data-stu-id="1d89e-127">x</span></span>      | <span data-ttu-id="1d89e-128">x</span><span class="sxs-lookup"><span data-stu-id="1d89e-128">x</span></span>        | <span data-ttu-id="1d89e-129">x</span><span class="sxs-lookup"><span data-stu-id="1d89e-129">x</span></span>     | <span data-ttu-id="1d89e-130">x</span><span class="sxs-lookup"><span data-stu-id="1d89e-130">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="1d89e-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1d89e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d89e-132">Texture1D</span><span class="sxs-lookup"><span data-stu-id="1d89e-132">Texture1D</span></span>](sm5-object-texture1d.md)
</dt> <dt>

[<span data-ttu-id="1d89e-133">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="1d89e-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




