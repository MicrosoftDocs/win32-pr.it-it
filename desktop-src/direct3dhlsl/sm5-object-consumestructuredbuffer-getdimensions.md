---
title: 'Funzione ConsumeStructuredBuffer:: GetDimensions'
description: 'Ottiene le dimensioni della risorsa. | Funzione ConsumeStructuredBuffer:: GetDimensions'
ms.assetid: 0710a4fb-23b0-4b19-b9ed-21bbb9874d33
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
ms.openlocfilehash: a204ed44c90c60b327ceb201037c6758763b3a05
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995317"
---
# <a name="consumestructuredbuffergetdimensions-function"></a><span data-ttu-id="5a335-105">Funzione ConsumeStructuredBuffer:: GetDimensions</span><span class="sxs-lookup"><span data-stu-id="5a335-105">ConsumeStructuredBuffer::GetDimensions function</span></span>

<span data-ttu-id="5a335-106">Ottiene le dimensioni della risorsa.</span><span class="sxs-lookup"><span data-stu-id="5a335-106">Gets the resource dimensions.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a335-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5a335-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out uint numStructs,
  out uint stride
);
```

## <a name="parameters"></a><span data-ttu-id="5a335-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="5a335-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a335-109">*numStructs* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="5a335-109">*numStructs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5a335-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="5a335-110">Type: **uint**</span></span>

<span data-ttu-id="5a335-111">Numero di strutture.</span><span class="sxs-lookup"><span data-stu-id="5a335-111">The number of structures.</span></span>

</dd> <dt>

<span data-ttu-id="5a335-112">*stride* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="5a335-112">*stride* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5a335-113">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="5a335-113">Type: **uint**</span></span>

<span data-ttu-id="5a335-114">Stride, in byte, di ogni elemento.</span><span class="sxs-lookup"><span data-stu-id="5a335-114">The stride, in bytes, of each element.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a335-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5a335-115">Return value</span></span>

<span data-ttu-id="5a335-116">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="5a335-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a335-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="5a335-117">Remarks</span></span>

<span data-ttu-id="5a335-118">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="5a335-118">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="5a335-119">Vertice</span><span class="sxs-lookup"><span data-stu-id="5a335-119">Vertex</span></span> | <span data-ttu-id="5a335-120">Hull</span><span class="sxs-lookup"><span data-stu-id="5a335-120">Hull</span></span> | <span data-ttu-id="5a335-121">Dominio</span><span class="sxs-lookup"><span data-stu-id="5a335-121">Domain</span></span> | <span data-ttu-id="5a335-122">Geometria</span><span class="sxs-lookup"><span data-stu-id="5a335-122">Geometry</span></span> | <span data-ttu-id="5a335-123">Pixel</span><span class="sxs-lookup"><span data-stu-id="5a335-123">Pixel</span></span> | <span data-ttu-id="5a335-124">Calcolo</span><span class="sxs-lookup"><span data-stu-id="5a335-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="5a335-125">x</span><span class="sxs-lookup"><span data-stu-id="5a335-125">x</span></span>      | <span data-ttu-id="5a335-126">x</span><span class="sxs-lookup"><span data-stu-id="5a335-126">x</span></span>    | <span data-ttu-id="5a335-127">x</span><span class="sxs-lookup"><span data-stu-id="5a335-127">x</span></span>      | <span data-ttu-id="5a335-128">x</span><span class="sxs-lookup"><span data-stu-id="5a335-128">x</span></span>        | <span data-ttu-id="5a335-129">x</span><span class="sxs-lookup"><span data-stu-id="5a335-129">x</span></span>     | <span data-ttu-id="5a335-130">x</span><span class="sxs-lookup"><span data-stu-id="5a335-130">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="5a335-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5a335-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a335-132">ConsumeStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="5a335-132">ConsumeStructuredBuffer</span></span>](sm5-object-consumestructuredbuffer.md)
</dt> <dt>

[<span data-ttu-id="5a335-133">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="5a335-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




