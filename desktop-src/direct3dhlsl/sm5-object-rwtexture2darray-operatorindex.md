---
title: 'Funzione RWTexture2DArray:: operator'
description: 'Restituisce una variabile di risorsa. | Funzione RWTexture2DArray:: operator'
ms.assetid: ae3d0697-ea0a-450d-bdfe-7bc5d8faf11a
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
ms.openlocfilehash: faf49c48fbf5042ce2765005cd8daea4d1227255
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104058501"
---
# <a name="rwtexture2darrayoperator--function"></a><span data-ttu-id="0ee0b-105">Funzione RWTexture2DArray:: operator</span><span class="sxs-lookup"><span data-stu-id="0ee0b-105">RWTexture2DArray::Operator  function</span></span>

<span data-ttu-id="0ee0b-106">Restituisce una variabile di risorsa.</span><span class="sxs-lookup"><span data-stu-id="0ee0b-106">Returns a resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ee0b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0ee0b-107">Syntax</span></span>

``` syntax
R Operator[](
  in uint3 pos
);
```

## <a name="parameters"></a><span data-ttu-id="0ee0b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="0ee0b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ee0b-109">*pos* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0ee0b-109">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ee0b-110">Tipo: **uint3**</span><span class="sxs-lookup"><span data-stu-id="0ee0b-110">Type: **uint3**</span></span>

<span data-ttu-id="0ee0b-111">Posizione dell'indice.</span><span class="sxs-lookup"><span data-stu-id="0ee0b-111">The index position.</span></span> <span data-ttu-id="0ee0b-112">Il primo e il secondo componente contengono le coordinate (x, y).</span><span class="sxs-lookup"><span data-stu-id="0ee0b-112">The first and second components contain the (x, y) coordinates.</span></span> <span data-ttu-id="0ee0b-113">Il terzo componente indica la sezione della matrice desiderata.</span><span class="sxs-lookup"><span data-stu-id="0ee0b-113">The third component indicates the desired array slice.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ee0b-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0ee0b-114">Return value</span></span>

<span data-ttu-id="0ee0b-115">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="0ee0b-115">Type: **R**</span></span>

<span data-ttu-id="0ee0b-116">Variabile di risorsa.</span><span class="sxs-lookup"><span data-stu-id="0ee0b-116">A resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ee0b-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="0ee0b-117">Remarks</span></span>

<span data-ttu-id="0ee0b-118">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="0ee0b-118">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="0ee0b-119">Vertice</span><span class="sxs-lookup"><span data-stu-id="0ee0b-119">Vertex</span></span> | <span data-ttu-id="0ee0b-120">Hull</span><span class="sxs-lookup"><span data-stu-id="0ee0b-120">Hull</span></span> | <span data-ttu-id="0ee0b-121">Dominio</span><span class="sxs-lookup"><span data-stu-id="0ee0b-121">Domain</span></span> | <span data-ttu-id="0ee0b-122">Geometria</span><span class="sxs-lookup"><span data-stu-id="0ee0b-122">Geometry</span></span> | <span data-ttu-id="0ee0b-123">Pixel</span><span class="sxs-lookup"><span data-stu-id="0ee0b-123">Pixel</span></span> | <span data-ttu-id="0ee0b-124">Calcolo</span><span class="sxs-lookup"><span data-stu-id="0ee0b-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="0ee0b-125">x</span><span class="sxs-lookup"><span data-stu-id="0ee0b-125">x</span></span>     | <span data-ttu-id="0ee0b-126">x</span><span class="sxs-lookup"><span data-stu-id="0ee0b-126">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="0ee0b-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0ee0b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ee0b-128">RWTexture2DArray</span><span class="sxs-lookup"><span data-stu-id="0ee0b-128">RWTexture2DArray</span></span>](sm5-object-rwtexture2darray.md)
</dt> <dt>

[<span data-ttu-id="0ee0b-129">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="0ee0b-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




