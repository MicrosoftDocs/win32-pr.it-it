---
title: 'Funzione RWByteAddressBuffer:: Load4 (uint)'
description: 'Ottiene quattro valori. | Funzione RWByteAddressBuffer:: Load4 (uint)'
ms.assetid: b46cd119-75be-4c2d-82f9-5dcabd7e4400
keywords:
- Funzione Load4 HLSL
topic_type:
- apiref
api_name:
- Load4
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bb2bdc5adf3b3d95c68871a14c9382891a59ad52
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104982049"
---
# <a name="rwbyteaddressbufferload4uint-function"></a><span data-ttu-id="5388c-105">Funzione RWByteAddressBuffer:: Load4 (uint)</span><span class="sxs-lookup"><span data-stu-id="5388c-105">RWByteAddressBuffer::Load4(uint) function</span></span>

<span data-ttu-id="5388c-106">Ottiene quattro valori.</span><span class="sxs-lookup"><span data-stu-id="5388c-106">Gets four values.</span></span>

## <a name="syntax"></a><span data-ttu-id="5388c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5388c-107">Syntax</span></span>

``` syntax
uint4 Load4(
  in uint address
);
```

## <a name="parameters"></a><span data-ttu-id="5388c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="5388c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5388c-109">*Indirizzo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5388c-109">*address* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5388c-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="5388c-110">Type: **uint**</span></span>

<span data-ttu-id="5388c-111">Indirizzo di input in byte, che deve essere un multiplo di 4.</span><span class="sxs-lookup"><span data-stu-id="5388c-111">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5388c-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5388c-112">Return value</span></span>

<span data-ttu-id="5388c-113">Tipo: **uint4**</span><span class="sxs-lookup"><span data-stu-id="5388c-113">Type: **uint4**</span></span>

<span data-ttu-id="5388c-114">Quattro valori.</span><span class="sxs-lookup"><span data-stu-id="5388c-114">Four values.</span></span>

## <a name="remarks"></a><span data-ttu-id="5388c-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="5388c-115">Remarks</span></span>

<span data-ttu-id="5388c-116">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="5388c-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="5388c-117">Vertice</span><span class="sxs-lookup"><span data-stu-id="5388c-117">Vertex</span></span> | <span data-ttu-id="5388c-118">Hull</span><span class="sxs-lookup"><span data-stu-id="5388c-118">Hull</span></span> | <span data-ttu-id="5388c-119">Dominio</span><span class="sxs-lookup"><span data-stu-id="5388c-119">Domain</span></span> | <span data-ttu-id="5388c-120">Geometria</span><span class="sxs-lookup"><span data-stu-id="5388c-120">Geometry</span></span> | <span data-ttu-id="5388c-121">Pixel</span><span class="sxs-lookup"><span data-stu-id="5388c-121">Pixel</span></span> | <span data-ttu-id="5388c-122">Calcolo</span><span class="sxs-lookup"><span data-stu-id="5388c-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="5388c-123">x</span><span class="sxs-lookup"><span data-stu-id="5388c-123">x</span></span>     | <span data-ttu-id="5388c-124">x</span><span class="sxs-lookup"><span data-stu-id="5388c-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="5388c-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5388c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5388c-126">Metodi Load4</span><span class="sxs-lookup"><span data-stu-id="5388c-126">Load4 methods</span></span>](rwbyteaddressbuffer-load4.md)
</dt> <dt>

[<span data-ttu-id="5388c-127">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="5388c-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




