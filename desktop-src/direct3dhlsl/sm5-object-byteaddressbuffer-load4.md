---
title: 'Funzione ByteAddressBuffer:: Load4 (uint)'
description: 'Ottiene quattro valori. | Funzione ByteAddressBuffer:: Load4 (uint)'
ms.assetid: bc74bf29-1c22-4e47-bafc-ecef194f54b8
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
ms.openlocfilehash: 18ce27e7d02a414165aab169e40a6ab14cdd8c4c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981927"
---
# <a name="byteaddressbufferload4uint-function"></a><span data-ttu-id="e0cd2-105">Funzione ByteAddressBuffer:: Load4 (uint)</span><span class="sxs-lookup"><span data-stu-id="e0cd2-105">ByteAddressBuffer::Load4(uint) function</span></span>

<span data-ttu-id="e0cd2-106">Ottiene quattro valori.</span><span class="sxs-lookup"><span data-stu-id="e0cd2-106">Gets four values.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0cd2-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e0cd2-107">Syntax</span></span>

``` syntax
uint4 Load4(
  in uint address
);
```

## <a name="parameters"></a><span data-ttu-id="e0cd2-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e0cd2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0cd2-109">*Indirizzo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e0cd2-109">*address* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0cd2-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="e0cd2-110">Type: **uint**</span></span>

<span data-ttu-id="e0cd2-111">Indirizzo di input in byte, che deve essere un multiplo di 4.</span><span class="sxs-lookup"><span data-stu-id="e0cd2-111">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0cd2-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e0cd2-112">Return value</span></span>

<span data-ttu-id="e0cd2-113">Tipo: **uint4**</span><span class="sxs-lookup"><span data-stu-id="e0cd2-113">Type: **uint4**</span></span>

<span data-ttu-id="e0cd2-114">Quattro valori.</span><span class="sxs-lookup"><span data-stu-id="e0cd2-114">Four values.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0cd2-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="e0cd2-115">Remarks</span></span>

<span data-ttu-id="e0cd2-116">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="e0cd2-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="e0cd2-117">Vertice</span><span class="sxs-lookup"><span data-stu-id="e0cd2-117">Vertex</span></span> | <span data-ttu-id="e0cd2-118">Hull</span><span class="sxs-lookup"><span data-stu-id="e0cd2-118">Hull</span></span> | <span data-ttu-id="e0cd2-119">Dominio</span><span class="sxs-lookup"><span data-stu-id="e0cd2-119">Domain</span></span> | <span data-ttu-id="e0cd2-120">Geometria</span><span class="sxs-lookup"><span data-stu-id="e0cd2-120">Geometry</span></span> | <span data-ttu-id="e0cd2-121">Pixel</span><span class="sxs-lookup"><span data-stu-id="e0cd2-121">Pixel</span></span> | <span data-ttu-id="e0cd2-122">Calcolo</span><span class="sxs-lookup"><span data-stu-id="e0cd2-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="e0cd2-123">x</span><span class="sxs-lookup"><span data-stu-id="e0cd2-123">x</span></span>      | <span data-ttu-id="e0cd2-124">x</span><span class="sxs-lookup"><span data-stu-id="e0cd2-124">x</span></span>    | <span data-ttu-id="e0cd2-125">x</span><span class="sxs-lookup"><span data-stu-id="e0cd2-125">x</span></span>      | <span data-ttu-id="e0cd2-126">x</span><span class="sxs-lookup"><span data-stu-id="e0cd2-126">x</span></span>        | <span data-ttu-id="e0cd2-127">x</span><span class="sxs-lookup"><span data-stu-id="e0cd2-127">x</span></span>     | <span data-ttu-id="e0cd2-128">x</span><span class="sxs-lookup"><span data-stu-id="e0cd2-128">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="e0cd2-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e0cd2-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0cd2-130">Metodi Load4</span><span class="sxs-lookup"><span data-stu-id="e0cd2-130">Load4 methods</span></span>](byteaddressbuffer-load4.md)
</dt> <dt>

[<span data-ttu-id="e0cd2-131">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="e0cd2-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




