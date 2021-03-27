---
title: 'Funzione buffer:: GetDimensions'
description: 'Ottiene la lunghezza del buffer. | Funzione buffer:: GetDimensions'
ms.assetid: 704890e8-43e4-4e72-b7e2-eeef331bef1c
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
ms.openlocfilehash: c7f1ad1da7600e65d7442c1b2431535e2fdcf38c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981090"
---
# <a name="buffergetdimensions-function"></a><span data-ttu-id="2d8d1-105">Funzione buffer:: GetDimensions</span><span class="sxs-lookup"><span data-stu-id="2d8d1-105">Buffer::GetDimensions function</span></span>

<span data-ttu-id="2d8d1-106">Ottiene la lunghezza del buffer.</span><span class="sxs-lookup"><span data-stu-id="2d8d1-106">Gets the length of the buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d8d1-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2d8d1-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out uint dim
);
```

## <a name="parameters"></a><span data-ttu-id="2d8d1-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="2d8d1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d8d1-109">*Dim* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="2d8d1-109">*dim* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2d8d1-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="2d8d1-110">Type: **uint**</span></span>

<span data-ttu-id="2d8d1-111">Lunghezza, in byte, del buffer.</span><span class="sxs-lookup"><span data-stu-id="2d8d1-111">The length, in bytes, of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d8d1-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2d8d1-112">Return value</span></span>

<span data-ttu-id="2d8d1-113">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="2d8d1-113">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d8d1-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="2d8d1-114">Remarks</span></span>

<span data-ttu-id="2d8d1-115">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="2d8d1-115">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="2d8d1-116">Vertice</span><span class="sxs-lookup"><span data-stu-id="2d8d1-116">Vertex</span></span> | <span data-ttu-id="2d8d1-117">Hull</span><span class="sxs-lookup"><span data-stu-id="2d8d1-117">Hull</span></span> | <span data-ttu-id="2d8d1-118">Dominio</span><span class="sxs-lookup"><span data-stu-id="2d8d1-118">Domain</span></span> | <span data-ttu-id="2d8d1-119">Geometria</span><span class="sxs-lookup"><span data-stu-id="2d8d1-119">Geometry</span></span> | <span data-ttu-id="2d8d1-120">Pixel</span><span class="sxs-lookup"><span data-stu-id="2d8d1-120">Pixel</span></span> | <span data-ttu-id="2d8d1-121">Calcolo</span><span class="sxs-lookup"><span data-stu-id="2d8d1-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="2d8d1-122">x</span><span class="sxs-lookup"><span data-stu-id="2d8d1-122">x</span></span>      | <span data-ttu-id="2d8d1-123">x</span><span class="sxs-lookup"><span data-stu-id="2d8d1-123">x</span></span>    | <span data-ttu-id="2d8d1-124">x</span><span class="sxs-lookup"><span data-stu-id="2d8d1-124">x</span></span>      | <span data-ttu-id="2d8d1-125">x</span><span class="sxs-lookup"><span data-stu-id="2d8d1-125">x</span></span>        | <span data-ttu-id="2d8d1-126">x</span><span class="sxs-lookup"><span data-stu-id="2d8d1-126">x</span></span>     | <span data-ttu-id="2d8d1-127">x</span><span class="sxs-lookup"><span data-stu-id="2d8d1-127">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="2d8d1-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2d8d1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d8d1-129">Buffer</span><span class="sxs-lookup"><span data-stu-id="2d8d1-129">Buffer</span></span>](sm5-object-buffer.md)
</dt> <dt>

[<span data-ttu-id="2d8d1-130">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="2d8d1-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




