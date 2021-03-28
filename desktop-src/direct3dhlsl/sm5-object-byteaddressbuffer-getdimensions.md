---
title: 'Funzione ByteAddressBuffer:: GetDimensions'
description: 'Ottiene la lunghezza del buffer. | Funzione ByteAddressBuffer:: GetDimensions'
ms.assetid: 32099118-8d8a-440e-96ba-2580d905f068
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
ms.openlocfilehash: 1cbb705789e444a6fa54aeb87190912996f65621
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995293"
---
# <a name="byteaddressbuffergetdimensions-function"></a><span data-ttu-id="59570-105">Funzione ByteAddressBuffer:: GetDimensions</span><span class="sxs-lookup"><span data-stu-id="59570-105">ByteAddressBuffer::GetDimensions function</span></span>

<span data-ttu-id="59570-106">Ottiene la lunghezza del buffer.</span><span class="sxs-lookup"><span data-stu-id="59570-106">Gets the length of the buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="59570-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="59570-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out uint dim
);
```

## <a name="parameters"></a><span data-ttu-id="59570-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="59570-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59570-109">*Dim* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="59570-109">*dim* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="59570-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="59570-110">Type: **uint**</span></span>

<span data-ttu-id="59570-111">Lunghezza, in byte, del buffer.</span><span class="sxs-lookup"><span data-stu-id="59570-111">The length, in bytes, of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59570-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="59570-112">Return value</span></span>

<span data-ttu-id="59570-113">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="59570-113">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="59570-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="59570-114">Remarks</span></span>

<span data-ttu-id="59570-115">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="59570-115">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="59570-116">Vertice</span><span class="sxs-lookup"><span data-stu-id="59570-116">Vertex</span></span> | <span data-ttu-id="59570-117">Hull</span><span class="sxs-lookup"><span data-stu-id="59570-117">Hull</span></span> | <span data-ttu-id="59570-118">Dominio</span><span class="sxs-lookup"><span data-stu-id="59570-118">Domain</span></span> | <span data-ttu-id="59570-119">Geometria</span><span class="sxs-lookup"><span data-stu-id="59570-119">Geometry</span></span> | <span data-ttu-id="59570-120">Pixel</span><span class="sxs-lookup"><span data-stu-id="59570-120">Pixel</span></span> | <span data-ttu-id="59570-121">Calcolo</span><span class="sxs-lookup"><span data-stu-id="59570-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="59570-122">x</span><span class="sxs-lookup"><span data-stu-id="59570-122">x</span></span>      | <span data-ttu-id="59570-123">x</span><span class="sxs-lookup"><span data-stu-id="59570-123">x</span></span>    | <span data-ttu-id="59570-124">x</span><span class="sxs-lookup"><span data-stu-id="59570-124">x</span></span>      | <span data-ttu-id="59570-125">x</span><span class="sxs-lookup"><span data-stu-id="59570-125">x</span></span>        | <span data-ttu-id="59570-126">x</span><span class="sxs-lookup"><span data-stu-id="59570-126">x</span></span>     | <span data-ttu-id="59570-127">x</span><span class="sxs-lookup"><span data-stu-id="59570-127">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="59570-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="59570-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59570-129">ByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="59570-129">ByteAddressBuffer</span></span>](sm5-object-byteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="59570-130">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="59570-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




