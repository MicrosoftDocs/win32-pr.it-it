---
title: 'Funzione AppendStructuredBuffer:: GetDimensions'
description: 'Ottiene le dimensioni della risorsa. | Funzione AppendStructuredBuffer:: GetDimensions'
ms.assetid: 41ed86d5-25c0-48bd-add9-792eb89605c3
keywords:
- Funzione GetDimensions HLSL
topic_type:
- apiref
api_name:
- GetDimensions
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 93db905ae40f1bec7488eca292f4ea44d87950d3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981095"
---
# <a name="appendstructuredbuffergetdimensions-function"></a><span data-ttu-id="edd61-105">Funzione AppendStructuredBuffer:: GetDimensions</span><span class="sxs-lookup"><span data-stu-id="edd61-105">AppendStructuredBuffer::GetDimensions function</span></span>

<span data-ttu-id="edd61-106">Ottiene le dimensioni della risorsa.</span><span class="sxs-lookup"><span data-stu-id="edd61-106">Gets the resource dimensions.</span></span>

## <a name="syntax"></a><span data-ttu-id="edd61-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="edd61-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out uint numStructs,
  out uint stride
);
```

## <a name="parameters"></a><span data-ttu-id="edd61-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="edd61-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="edd61-109">*numStructs* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="edd61-109">*numStructs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="edd61-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="edd61-110">Type: **uint**</span></span>

<span data-ttu-id="edd61-111">Numero di strutture.</span><span class="sxs-lookup"><span data-stu-id="edd61-111">The number of structures.</span></span>

</dd> <dt>

<span data-ttu-id="edd61-112">*stride* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="edd61-112">*stride* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="edd61-113">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="edd61-113">Type: **uint**</span></span>

<span data-ttu-id="edd61-114">Numero di byte in ogni elemento.</span><span class="sxs-lookup"><span data-stu-id="edd61-114">The number of bytes in each element.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="edd61-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="edd61-115">Return value</span></span>

<span data-ttu-id="edd61-116">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="edd61-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="edd61-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="edd61-117">Remarks</span></span>

<span data-ttu-id="edd61-118">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="edd61-118">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="edd61-119">Vertice</span><span class="sxs-lookup"><span data-stu-id="edd61-119">Vertex</span></span> | <span data-ttu-id="edd61-120">Hull</span><span class="sxs-lookup"><span data-stu-id="edd61-120">Hull</span></span> | <span data-ttu-id="edd61-121">Dominio</span><span class="sxs-lookup"><span data-stu-id="edd61-121">Domain</span></span> | <span data-ttu-id="edd61-122">Geometria</span><span class="sxs-lookup"><span data-stu-id="edd61-122">Geometry</span></span> | <span data-ttu-id="edd61-123">Pixel</span><span class="sxs-lookup"><span data-stu-id="edd61-123">Pixel</span></span> | <span data-ttu-id="edd61-124">Calcolo</span><span class="sxs-lookup"><span data-stu-id="edd61-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="edd61-125">x</span><span class="sxs-lookup"><span data-stu-id="edd61-125">x</span></span>      | <span data-ttu-id="edd61-126">x</span><span class="sxs-lookup"><span data-stu-id="edd61-126">x</span></span>    | <span data-ttu-id="edd61-127">x</span><span class="sxs-lookup"><span data-stu-id="edd61-127">x</span></span>      | <span data-ttu-id="edd61-128">x</span><span class="sxs-lookup"><span data-stu-id="edd61-128">x</span></span>        | <span data-ttu-id="edd61-129">x</span><span class="sxs-lookup"><span data-stu-id="edd61-129">x</span></span>     | <span data-ttu-id="edd61-130">x</span><span class="sxs-lookup"><span data-stu-id="edd61-130">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="edd61-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="edd61-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edd61-132">AppendStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="edd61-132">AppendStructuredBuffer</span></span>](sm5-object-appendstructuredbuffer.md)
</dt> <dt>

[<span data-ttu-id="edd61-133">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="edd61-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




