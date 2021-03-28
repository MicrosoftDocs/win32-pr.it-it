---
title: 'Funzione RWTexture2D:: operator'
description: 'Restituisce una variabile di risorsa. | Funzione RWTexture2D:: operator'
ms.assetid: 339dba7d-b0c6-4112-ae40-555661577a3e
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
ms.openlocfilehash: 8c1ff25cdf4a0f33d041500f6a81220261f216c4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981634"
---
# <a name="rwtexture2doperator--function"></a><span data-ttu-id="081ff-105">Funzione RWTexture2D:: operator</span><span class="sxs-lookup"><span data-stu-id="081ff-105">RWTexture2D::Operator  function</span></span>

<span data-ttu-id="081ff-106">Restituisce una variabile di risorsa.</span><span class="sxs-lookup"><span data-stu-id="081ff-106">Returns a resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="081ff-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="081ff-107">Syntax</span></span>

``` syntax
R Operator[](
  in uint2 pos
);
```

## <a name="parameters"></a><span data-ttu-id="081ff-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="081ff-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="081ff-109">*pos* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="081ff-109">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="081ff-110">Tipo: **uint2**</span><span class="sxs-lookup"><span data-stu-id="081ff-110">Type: **uint2**</span></span>

<span data-ttu-id="081ff-111">Posizione dell'indice.</span><span class="sxs-lookup"><span data-stu-id="081ff-111">The index position.</span></span> <span data-ttu-id="081ff-112">Contiene le coordinate (x, y).</span><span class="sxs-lookup"><span data-stu-id="081ff-112">Contains the (x, y) coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="081ff-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="081ff-113">Return value</span></span>

<span data-ttu-id="081ff-114">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="081ff-114">Type: **R**</span></span>

<span data-ttu-id="081ff-115">Variabile di risorsa.</span><span class="sxs-lookup"><span data-stu-id="081ff-115">A resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="081ff-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="081ff-116">Remarks</span></span>

<span data-ttu-id="081ff-117">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="081ff-117">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="081ff-118">Vertice</span><span class="sxs-lookup"><span data-stu-id="081ff-118">Vertex</span></span> | <span data-ttu-id="081ff-119">Hull</span><span class="sxs-lookup"><span data-stu-id="081ff-119">Hull</span></span> | <span data-ttu-id="081ff-120">Dominio</span><span class="sxs-lookup"><span data-stu-id="081ff-120">Domain</span></span> | <span data-ttu-id="081ff-121">Geometria</span><span class="sxs-lookup"><span data-stu-id="081ff-121">Geometry</span></span> | <span data-ttu-id="081ff-122">Pixel</span><span class="sxs-lookup"><span data-stu-id="081ff-122">Pixel</span></span> | <span data-ttu-id="081ff-123">Calcolo</span><span class="sxs-lookup"><span data-stu-id="081ff-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="081ff-124">x</span><span class="sxs-lookup"><span data-stu-id="081ff-124">x</span></span>     | <span data-ttu-id="081ff-125">x</span><span class="sxs-lookup"><span data-stu-id="081ff-125">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="081ff-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="081ff-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="081ff-127">RWTexture2D</span><span class="sxs-lookup"><span data-stu-id="081ff-127">RWTexture2D</span></span>](sm5-object-rwtexture2d.md)
</dt> <dt>

[<span data-ttu-id="081ff-128">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="081ff-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




