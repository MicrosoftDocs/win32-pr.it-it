---
title: 'Funzione RWStructuredBuffer:: GetDimensions'
description: 'Ottiene le dimensioni della risorsa. | Funzione RWStructuredBuffer:: GetDimensions'
ms.assetid: 842b3d21-2e2b-4906-93ee-0252b2e8cf85
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
ms.openlocfilehash: 0e3868f33e372472999c29bffdd8e12bc8ef09b7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981082"
---
# <a name="rwstructuredbuffergetdimensions-function"></a><span data-ttu-id="871a1-105">Funzione RWStructuredBuffer:: GetDimensions</span><span class="sxs-lookup"><span data-stu-id="871a1-105">RWStructuredBuffer::GetDimensions function</span></span>

<span data-ttu-id="871a1-106">Ottiene le dimensioni della risorsa.</span><span class="sxs-lookup"><span data-stu-id="871a1-106">Gets the resource dimensions.</span></span>

## <a name="syntax"></a><span data-ttu-id="871a1-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="871a1-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out uint numStructs,
  out uint stride
);
```

## <a name="parameters"></a><span data-ttu-id="871a1-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="871a1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="871a1-109">*numStructs* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="871a1-109">*numStructs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="871a1-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="871a1-110">Type: **uint**</span></span>

<span data-ttu-id="871a1-111">Numero di strutture nella risorsa.</span><span class="sxs-lookup"><span data-stu-id="871a1-111">The number of structures in the resource.</span></span>

</dd> <dt>

<span data-ttu-id="871a1-112">*stride* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="871a1-112">*stride* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="871a1-113">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="871a1-113">Type: **uint**</span></span>

<span data-ttu-id="871a1-114">Stride, in byte, di ogni elemento della struttura.</span><span class="sxs-lookup"><span data-stu-id="871a1-114">The stride, in bytes, of each structure element.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="871a1-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="871a1-115">Return value</span></span>

<span data-ttu-id="871a1-116">Nothing</span><span class="sxs-lookup"><span data-stu-id="871a1-116">Nothing</span></span>

## <a name="remarks"></a><span data-ttu-id="871a1-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="871a1-117">Remarks</span></span>

<span data-ttu-id="871a1-118">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="871a1-118">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="871a1-119">Vertice</span><span class="sxs-lookup"><span data-stu-id="871a1-119">Vertex</span></span> | <span data-ttu-id="871a1-120">Hull</span><span class="sxs-lookup"><span data-stu-id="871a1-120">Hull</span></span> | <span data-ttu-id="871a1-121">Dominio</span><span class="sxs-lookup"><span data-stu-id="871a1-121">Domain</span></span> | <span data-ttu-id="871a1-122">Geometria</span><span class="sxs-lookup"><span data-stu-id="871a1-122">Geometry</span></span> | <span data-ttu-id="871a1-123">Pixel</span><span class="sxs-lookup"><span data-stu-id="871a1-123">Pixel</span></span> | <span data-ttu-id="871a1-124">Calcolo</span><span class="sxs-lookup"><span data-stu-id="871a1-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="871a1-125">x</span><span class="sxs-lookup"><span data-stu-id="871a1-125">x</span></span>     | <span data-ttu-id="871a1-126">x</span><span class="sxs-lookup"><span data-stu-id="871a1-126">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="871a1-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="871a1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="871a1-128">RWStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="871a1-128">RWStructuredBuffer</span></span>](sm5-object-rwstructuredbuffer.md)
</dt> <dt>

[<span data-ttu-id="871a1-129">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="871a1-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




