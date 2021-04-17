---
title: 'Funzione RWByteAddressBuffer:: GetDimensions'
description: 'Ottiene la lunghezza del buffer. | Funzione RWByteAddressBuffer:: GetDimensions'
ms.assetid: 7d78aa0d-75b8-43d5-85d9-0a6fb04ae64f
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
ms.openlocfilehash: 0d22b6f655802d77a92611fe8699a405aa323873
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353581"
---
# <a name="rwbyteaddressbuffergetdimensions-function"></a><span data-ttu-id="8165d-105">Funzione RWByteAddressBuffer:: GetDimensions</span><span class="sxs-lookup"><span data-stu-id="8165d-105">RWByteAddressBuffer::GetDimensions function</span></span>

<span data-ttu-id="8165d-106">Ottiene la lunghezza del buffer.</span><span class="sxs-lookup"><span data-stu-id="8165d-106">Gets the length of the buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="8165d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8165d-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out uint dim
);
```

## <a name="parameters"></a><span data-ttu-id="8165d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="8165d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8165d-109">*Dim* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8165d-109">*dim* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8165d-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="8165d-110">Type: **uint**</span></span>

<span data-ttu-id="8165d-111">Lunghezza, in byte, del buffer.</span><span class="sxs-lookup"><span data-stu-id="8165d-111">The length, in bytes, of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8165d-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8165d-112">Return value</span></span>

<span data-ttu-id="8165d-113">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="8165d-113">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8165d-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="8165d-114">Remarks</span></span>

<span data-ttu-id="8165d-115">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="8165d-115">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="8165d-116">Vertice</span><span class="sxs-lookup"><span data-stu-id="8165d-116">Vertex</span></span> | <span data-ttu-id="8165d-117">Hull</span><span class="sxs-lookup"><span data-stu-id="8165d-117">Hull</span></span> | <span data-ttu-id="8165d-118">Dominio</span><span class="sxs-lookup"><span data-stu-id="8165d-118">Domain</span></span> | <span data-ttu-id="8165d-119">Geometria</span><span class="sxs-lookup"><span data-stu-id="8165d-119">Geometry</span></span> | <span data-ttu-id="8165d-120">Pixel</span><span class="sxs-lookup"><span data-stu-id="8165d-120">Pixel</span></span> | <span data-ttu-id="8165d-121">Calcolo</span><span class="sxs-lookup"><span data-stu-id="8165d-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="8165d-122">x</span><span class="sxs-lookup"><span data-stu-id="8165d-122">x</span></span>     | <span data-ttu-id="8165d-123">x</span><span class="sxs-lookup"><span data-stu-id="8165d-123">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="8165d-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8165d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8165d-125">RWByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="8165d-125">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="8165d-126">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="8165d-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




