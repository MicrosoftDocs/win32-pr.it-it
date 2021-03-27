---
title: 'Funzione ByteAddressBuffer:: Load (int)'
description: 'Ottiene un valore. | Funzione ByteAddressBuffer:: Load (int)'
ms.assetid: a63f4099-2c3b-4d37-9135-b8c63df30824
keywords:
- Funzione Load HLSL
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e0de7d1a8ef8a7fe3173016fe07a433a930c3d59
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995384"
---
# <a name="byteaddressbufferloadint-function"></a><span data-ttu-id="4cf36-105">Funzione ByteAddressBuffer:: Load (int)</span><span class="sxs-lookup"><span data-stu-id="4cf36-105">ByteAddressBuffer::Load(int) function</span></span>

<span data-ttu-id="4cf36-106">Ottiene un valore.</span><span class="sxs-lookup"><span data-stu-id="4cf36-106">Gets one value.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cf36-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4cf36-107">Syntax</span></span>

``` syntax
uint Load(
  in int address
);
```

## <a name="parameters"></a><span data-ttu-id="4cf36-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="4cf36-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cf36-109">*Indirizzo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4cf36-109">*address* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cf36-110">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="4cf36-110">Type: **int**</span></span>

<span data-ttu-id="4cf36-111">Indirizzo di input in byte, che deve essere un multiplo di 4.</span><span class="sxs-lookup"><span data-stu-id="4cf36-111">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4cf36-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4cf36-112">Return value</span></span>

<span data-ttu-id="4cf36-113">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="4cf36-113">Type: **uint**</span></span>

<span data-ttu-id="4cf36-114">Un valore.</span><span class="sxs-lookup"><span data-stu-id="4cf36-114">One value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4cf36-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="4cf36-115">Remarks</span></span>

<span data-ttu-id="4cf36-116">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="4cf36-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="4cf36-117">Vertice</span><span class="sxs-lookup"><span data-stu-id="4cf36-117">Vertex</span></span> | <span data-ttu-id="4cf36-118">Hull</span><span class="sxs-lookup"><span data-stu-id="4cf36-118">Hull</span></span> | <span data-ttu-id="4cf36-119">Dominio</span><span class="sxs-lookup"><span data-stu-id="4cf36-119">Domain</span></span> | <span data-ttu-id="4cf36-120">Geometria</span><span class="sxs-lookup"><span data-stu-id="4cf36-120">Geometry</span></span> | <span data-ttu-id="4cf36-121">Pixel</span><span class="sxs-lookup"><span data-stu-id="4cf36-121">Pixel</span></span> | <span data-ttu-id="4cf36-122">Calcolo</span><span class="sxs-lookup"><span data-stu-id="4cf36-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="4cf36-123">x</span><span class="sxs-lookup"><span data-stu-id="4cf36-123">x</span></span>      | <span data-ttu-id="4cf36-124">x</span><span class="sxs-lookup"><span data-stu-id="4cf36-124">x</span></span>    | <span data-ttu-id="4cf36-125">x</span><span class="sxs-lookup"><span data-stu-id="4cf36-125">x</span></span>      | <span data-ttu-id="4cf36-126">x</span><span class="sxs-lookup"><span data-stu-id="4cf36-126">x</span></span>        | <span data-ttu-id="4cf36-127">x</span><span class="sxs-lookup"><span data-stu-id="4cf36-127">x</span></span>     | <span data-ttu-id="4cf36-128">x</span><span class="sxs-lookup"><span data-stu-id="4cf36-128">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="4cf36-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4cf36-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cf36-130">Metodi Load</span><span class="sxs-lookup"><span data-stu-id="4cf36-130">Load methods</span></span>](byteaddressbuffer-load.md)
</dt> <dt>

[<span data-ttu-id="4cf36-131">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="4cf36-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




