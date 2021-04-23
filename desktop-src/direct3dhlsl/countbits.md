---
title: countbits (funzione)
description: Conta il numero di bit (per componente) impostati nell'intero di input.
ms.assetid: c4fafbc8-e21c-48cb-b433-8241a989ec85
keywords:
- Funzione countbits HLSL
topic_type:
- apiref
api_name:
- countbits
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 357aceca6e2aea261a9e94212b58ff6308c99560
ms.sourcegitcommit: 435ea8f5bf06808ffa7dce39afb0ee6de842ba2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/23/2021
ms.locfileid: "107925624"
---
# <a name="countbits-function"></a><span data-ttu-id="da029-104">countbits (funzione)</span><span class="sxs-lookup"><span data-stu-id="da029-104">countbits function</span></span>

<span data-ttu-id="da029-105">Conta il numero di bit (per componente) impostati nell'intero di input.</span><span class="sxs-lookup"><span data-stu-id="da029-105">Counts the number of bits (per component) set in the input integer.</span></span>

## <a name="syntax"></a><span data-ttu-id="da029-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="da029-106">Syntax</span></span>

``` syntax
uint countbits(
  in uint value
);
```

## <a name="parameters"></a><span data-ttu-id="da029-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="da029-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da029-108">*value* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="da029-108">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da029-109">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="da029-109">Type: **uint**</span></span>

<span data-ttu-id="da029-110">Valore di input.</span><span class="sxs-lookup"><span data-stu-id="da029-110">The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da029-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="da029-111">Return value</span></span>

<span data-ttu-id="da029-112">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="da029-112">Type: **uint**</span></span>

<span data-ttu-id="da029-113">Numero di bit.</span><span class="sxs-lookup"><span data-stu-id="da029-113">The number of bits.</span></span>

## <a name="remarks"></a><span data-ttu-id="da029-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="da029-114">Remarks</span></span>

<span data-ttu-id="da029-115">Sono disponibili anche le versioni di overload seguenti:</span><span class="sxs-lookup"><span data-stu-id="da029-115">The following overloaded versions are also available:</span></span>

``` syntax
uint count_bits(uint value);
uint2 count_bits(uint2 value);
uint3 count_bits(uint3 value);
uint4 count_bits(uint4 value);
```

### <a name="minimum-shader-model"></a><span data-ttu-id="da029-116">Modello di shader minimo</span><span class="sxs-lookup"><span data-stu-id="da029-116">Minimum Shader Model</span></span>

<span data-ttu-id="da029-117">Questa funzione è supportata nei modelli di shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="da029-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="da029-118">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="da029-118">Shader Model</span></span>                                                                | <span data-ttu-id="da029-119">Supportato</span><span class="sxs-lookup"><span data-stu-id="da029-119">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="da029-120">[Modello shader 5 e](d3d11-graphics-reference-sm5.md) modelli di shader superiori</span><span class="sxs-lookup"><span data-stu-id="da029-120">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="da029-121">sì</span><span class="sxs-lookup"><span data-stu-id="da029-121">yes</span></span>       |



 

<span data-ttu-id="da029-122">Questa funzione è supportata nei tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="da029-122">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="da029-123">Vertice</span><span class="sxs-lookup"><span data-stu-id="da029-123">Vertex</span></span> | <span data-ttu-id="da029-124">Scafo</span><span class="sxs-lookup"><span data-stu-id="da029-124">Hull</span></span> | <span data-ttu-id="da029-125">Dominio</span><span class="sxs-lookup"><span data-stu-id="da029-125">Domain</span></span> | <span data-ttu-id="da029-126">Geometria</span><span class="sxs-lookup"><span data-stu-id="da029-126">Geometry</span></span> | <span data-ttu-id="da029-127">Pixel</span><span class="sxs-lookup"><span data-stu-id="da029-127">Pixel</span></span> | <span data-ttu-id="da029-128">Calcolo</span><span class="sxs-lookup"><span data-stu-id="da029-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="da029-129">x</span><span class="sxs-lookup"><span data-stu-id="da029-129">x</span></span>      | <span data-ttu-id="da029-130">x</span><span class="sxs-lookup"><span data-stu-id="da029-130">x</span></span>    | <span data-ttu-id="da029-131">x</span><span class="sxs-lookup"><span data-stu-id="da029-131">x</span></span>      | <span data-ttu-id="da029-132">x</span><span class="sxs-lookup"><span data-stu-id="da029-132">x</span></span>        | <span data-ttu-id="da029-133">x</span><span class="sxs-lookup"><span data-stu-id="da029-133">x</span></span>     | <span data-ttu-id="da029-134">x</span><span class="sxs-lookup"><span data-stu-id="da029-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="da029-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="da029-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da029-136">Funzioni intrinseche</span><span class="sxs-lookup"><span data-stu-id="da029-136">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="da029-137">Modello shader 5</span><span class="sxs-lookup"><span data-stu-id="da029-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




