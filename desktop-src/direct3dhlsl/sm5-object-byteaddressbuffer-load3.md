---
title: 'Funzione ByteAddressBuffer:: Load3 (uint)'
description: 'Ottiene tre valori. | Funzione ByteAddressBuffer:: Load3 (uint)'
ms.assetid: 79afeb36-e0e7-44a2-b252-8e3577f4c1a5
keywords:
- Funzione Load3 HLSL
topic_type:
- apiref
api_name:
- Load3
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8e3975d454fcbb8c5dfa8cdef8d7f5718143546f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981930"
---
# <a name="byteaddressbufferload3uint-function"></a><span data-ttu-id="3929b-105">Funzione ByteAddressBuffer:: Load3 (uint)</span><span class="sxs-lookup"><span data-stu-id="3929b-105">ByteAddressBuffer::Load3(uint) function</span></span>

<span data-ttu-id="3929b-106">Ottiene tre valori.</span><span class="sxs-lookup"><span data-stu-id="3929b-106">Gets three values.</span></span>

## <a name="syntax"></a><span data-ttu-id="3929b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3929b-107">Syntax</span></span>

``` syntax
uint3 Load3(
  in uint address
);
```

## <a name="parameters"></a><span data-ttu-id="3929b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="3929b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3929b-109">*Indirizzo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3929b-109">*address* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3929b-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="3929b-110">Type: **uint**</span></span>

<span data-ttu-id="3929b-111">Indirizzo di input in byte, che deve essere un multiplo di 4.</span><span class="sxs-lookup"><span data-stu-id="3929b-111">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3929b-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3929b-112">Return value</span></span>

<span data-ttu-id="3929b-113">Tipo: **uint3**</span><span class="sxs-lookup"><span data-stu-id="3929b-113">Type: **uint3**</span></span>

<span data-ttu-id="3929b-114">Tre valori.</span><span class="sxs-lookup"><span data-stu-id="3929b-114">Three values.</span></span>

## <a name="remarks"></a><span data-ttu-id="3929b-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="3929b-115">Remarks</span></span>

<span data-ttu-id="3929b-116">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="3929b-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="3929b-117">Vertice</span><span class="sxs-lookup"><span data-stu-id="3929b-117">Vertex</span></span> | <span data-ttu-id="3929b-118">Hull</span><span class="sxs-lookup"><span data-stu-id="3929b-118">Hull</span></span> | <span data-ttu-id="3929b-119">Dominio</span><span class="sxs-lookup"><span data-stu-id="3929b-119">Domain</span></span> | <span data-ttu-id="3929b-120">Geometria</span><span class="sxs-lookup"><span data-stu-id="3929b-120">Geometry</span></span> | <span data-ttu-id="3929b-121">Pixel</span><span class="sxs-lookup"><span data-stu-id="3929b-121">Pixel</span></span> | <span data-ttu-id="3929b-122">Calcolo</span><span class="sxs-lookup"><span data-stu-id="3929b-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="3929b-123">x</span><span class="sxs-lookup"><span data-stu-id="3929b-123">x</span></span>      | <span data-ttu-id="3929b-124">x</span><span class="sxs-lookup"><span data-stu-id="3929b-124">x</span></span>    | <span data-ttu-id="3929b-125">x</span><span class="sxs-lookup"><span data-stu-id="3929b-125">x</span></span>      | <span data-ttu-id="3929b-126">x</span><span class="sxs-lookup"><span data-stu-id="3929b-126">x</span></span>        | <span data-ttu-id="3929b-127">x</span><span class="sxs-lookup"><span data-stu-id="3929b-127">x</span></span>     | <span data-ttu-id="3929b-128">x</span><span class="sxs-lookup"><span data-stu-id="3929b-128">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="3929b-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3929b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3929b-130">Metodi Load3</span><span class="sxs-lookup"><span data-stu-id="3929b-130">Load3 methods</span></span>](byteaddressbuffer-load3.md)
</dt> <dt>

[<span data-ttu-id="3929b-131">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="3929b-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




