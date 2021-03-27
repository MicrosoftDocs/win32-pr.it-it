---
title: 'Funzione StructuredBuffer:: GetDimensions'
description: 'Ottiene le dimensioni della risorsa. | Funzione StructuredBuffer:: GetDimensions'
ms.assetid: 423ea79c-4440-4837-b637-95180a1d5019
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
ms.openlocfilehash: 2b3d7c879c77386ddee80a63053711b8ae34ee8c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352961"
---
# <a name="structuredbuffergetdimensions-function"></a><span data-ttu-id="dc8a3-105">Funzione StructuredBuffer:: GetDimensions</span><span class="sxs-lookup"><span data-stu-id="dc8a3-105">StructuredBuffer::GetDimensions function</span></span>

<span data-ttu-id="dc8a3-106">Ottiene le dimensioni della risorsa.</span><span class="sxs-lookup"><span data-stu-id="dc8a3-106">Gets the resource dimensions.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc8a3-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dc8a3-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out uint numStructs,
  out uint stride
);
```

## <a name="parameters"></a><span data-ttu-id="dc8a3-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="dc8a3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc8a3-109">*numStructs* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="dc8a3-109">*numStructs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dc8a3-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="dc8a3-110">Type: **uint**</span></span>

<span data-ttu-id="dc8a3-111">Numero di strutture nella risorsa.</span><span class="sxs-lookup"><span data-stu-id="dc8a3-111">The number of structures in the resource.</span></span>

</dd> <dt>

<span data-ttu-id="dc8a3-112">*stride* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="dc8a3-112">*stride* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dc8a3-113">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="dc8a3-113">Type: **uint**</span></span>

<span data-ttu-id="dc8a3-114">Stride, in byte, di ogni elemento della struttura.</span><span class="sxs-lookup"><span data-stu-id="dc8a3-114">The stride, in bytes, of each structure element.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc8a3-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dc8a3-115">Return value</span></span>

<span data-ttu-id="dc8a3-116">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="dc8a3-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc8a3-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="dc8a3-117">Remarks</span></span>

<span data-ttu-id="dc8a3-118">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="dc8a3-118">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="dc8a3-119">Vertice</span><span class="sxs-lookup"><span data-stu-id="dc8a3-119">Vertex</span></span> | <span data-ttu-id="dc8a3-120">Hull</span><span class="sxs-lookup"><span data-stu-id="dc8a3-120">Hull</span></span> | <span data-ttu-id="dc8a3-121">Dominio</span><span class="sxs-lookup"><span data-stu-id="dc8a3-121">Domain</span></span> | <span data-ttu-id="dc8a3-122">Geometria</span><span class="sxs-lookup"><span data-stu-id="dc8a3-122">Geometry</span></span> | <span data-ttu-id="dc8a3-123">Pixel</span><span class="sxs-lookup"><span data-stu-id="dc8a3-123">Pixel</span></span> | <span data-ttu-id="dc8a3-124">Calcolo</span><span class="sxs-lookup"><span data-stu-id="dc8a3-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="dc8a3-125">x</span><span class="sxs-lookup"><span data-stu-id="dc8a3-125">x</span></span>      | <span data-ttu-id="dc8a3-126">x</span><span class="sxs-lookup"><span data-stu-id="dc8a3-126">x</span></span>    | <span data-ttu-id="dc8a3-127">x</span><span class="sxs-lookup"><span data-stu-id="dc8a3-127">x</span></span>      | <span data-ttu-id="dc8a3-128">x</span><span class="sxs-lookup"><span data-stu-id="dc8a3-128">x</span></span>        | <span data-ttu-id="dc8a3-129">x</span><span class="sxs-lookup"><span data-stu-id="dc8a3-129">x</span></span>     | <span data-ttu-id="dc8a3-130">x</span><span class="sxs-lookup"><span data-stu-id="dc8a3-130">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="dc8a3-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dc8a3-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc8a3-132">StructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="dc8a3-132">StructuredBuffer</span></span>](sm5-object-structuredbuffer.md)
</dt> <dt>

[<span data-ttu-id="dc8a3-133">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="dc8a3-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




