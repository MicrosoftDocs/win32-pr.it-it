---
title: 'Funzione Texture2D:: operator'
description: 'Restituisce una variabile di risorsa di sola lettura. | Funzione Texture2D:: operator'
ms.assetid: 72ba3fc8-04c3-479a-b307-525020898bac
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
ms.openlocfilehash: 2c397b1b80836f48cb856d03ccdf52ad2c95ce48
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981703"
---
# <a name="texture2doperator--function"></a><span data-ttu-id="6bcfb-105">Funzione Texture2D:: operator</span><span class="sxs-lookup"><span data-stu-id="6bcfb-105">Texture2D::Operator  function</span></span>

<span data-ttu-id="6bcfb-106">Restituisce una variabile di risorsa di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="6bcfb-106">Returns a read-only resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="6bcfb-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6bcfb-107">Syntax</span></span>

``` syntax
R Operator[](
  in uint2 pos
);
```

## <a name="parameters"></a><span data-ttu-id="6bcfb-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="6bcfb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6bcfb-109">*pos* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6bcfb-109">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6bcfb-110">Tipo: **uint2**</span><span class="sxs-lookup"><span data-stu-id="6bcfb-110">Type: **uint2**</span></span>

<span data-ttu-id="6bcfb-111">Posizione dell'indice.</span><span class="sxs-lookup"><span data-stu-id="6bcfb-111">The index position.</span></span> <span data-ttu-id="6bcfb-112">Contiene le coordinate (x, y).</span><span class="sxs-lookup"><span data-stu-id="6bcfb-112">Contains the (x, y) coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6bcfb-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6bcfb-113">Return value</span></span>

<span data-ttu-id="6bcfb-114">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="6bcfb-114">Type: **R**</span></span>

<span data-ttu-id="6bcfb-115">Variabile di sola lettura di una risorsa.</span><span class="sxs-lookup"><span data-stu-id="6bcfb-115">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="6bcfb-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="6bcfb-116">Remarks</span></span>

<span data-ttu-id="6bcfb-117">Questo metodo accede sempre al primo livello MIP.</span><span class="sxs-lookup"><span data-stu-id="6bcfb-117">This method always accesses the first mip level.</span></span> <span data-ttu-id="6bcfb-118">Per specificare altri livelli MIP, usare invece il metodo [**MIP \[ \] \[ \] . operator**](sm5-object-texture2d-mipsoperatorindex.md) .</span><span class="sxs-lookup"><span data-stu-id="6bcfb-118">To specify other mip levels, use the [**mip.operator\[\]\[\]**](sm5-object-texture2d-mipsoperatorindex.md) method instead.</span></span>

<span data-ttu-id="6bcfb-119">Gli esempi di trama possono essere usati per l'interpolazione bilineare.</span><span class="sxs-lookup"><span data-stu-id="6bcfb-119">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="6bcfb-120">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="6bcfb-120">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="6bcfb-121">Vertice</span><span class="sxs-lookup"><span data-stu-id="6bcfb-121">Vertex</span></span> | <span data-ttu-id="6bcfb-122">Hull</span><span class="sxs-lookup"><span data-stu-id="6bcfb-122">Hull</span></span> | <span data-ttu-id="6bcfb-123">Dominio</span><span class="sxs-lookup"><span data-stu-id="6bcfb-123">Domain</span></span> | <span data-ttu-id="6bcfb-124">Geometria</span><span class="sxs-lookup"><span data-stu-id="6bcfb-124">Geometry</span></span> | <span data-ttu-id="6bcfb-125">Pixel</span><span class="sxs-lookup"><span data-stu-id="6bcfb-125">Pixel</span></span> | <span data-ttu-id="6bcfb-126">Calcolo</span><span class="sxs-lookup"><span data-stu-id="6bcfb-126">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="6bcfb-127">x</span><span class="sxs-lookup"><span data-stu-id="6bcfb-127">x</span></span>      | <span data-ttu-id="6bcfb-128">x</span><span class="sxs-lookup"><span data-stu-id="6bcfb-128">x</span></span>    | <span data-ttu-id="6bcfb-129">x</span><span class="sxs-lookup"><span data-stu-id="6bcfb-129">x</span></span>      | <span data-ttu-id="6bcfb-130">x</span><span class="sxs-lookup"><span data-stu-id="6bcfb-130">x</span></span>        | <span data-ttu-id="6bcfb-131">x</span><span class="sxs-lookup"><span data-stu-id="6bcfb-131">x</span></span>     | <span data-ttu-id="6bcfb-132">x</span><span class="sxs-lookup"><span data-stu-id="6bcfb-132">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="6bcfb-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6bcfb-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bcfb-134">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6bcfb-134">Texture2D</span></span>](sm5-object-texture2d.md)
</dt> <dt>

[<span data-ttu-id="6bcfb-135">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="6bcfb-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




