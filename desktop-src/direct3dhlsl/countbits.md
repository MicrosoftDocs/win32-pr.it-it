---
title: countbits (funzione)
description: Conta il numero di bit (per componente) nell'intero di input.
ms.assetid: c4fafbc8-e21c-48cb-b433-8241a989ec85
keywords:
- funzione countbits HLSL
topic_type:
- apiref
api_name:
- countbits
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 60d3cd63502c6217e6fb0b0ff17685b2d2b5bf25
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104045876"
---
# <a name="countbits-function"></a><span data-ttu-id="d2a63-104">countbits (funzione)</span><span class="sxs-lookup"><span data-stu-id="d2a63-104">countbits function</span></span>

<span data-ttu-id="d2a63-105">Conta il numero di bit (per componente) nell'intero di input.</span><span class="sxs-lookup"><span data-stu-id="d2a63-105">Counts the number of bits (per component) in the input integer.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2a63-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d2a63-106">Syntax</span></span>

``` syntax
uint countbits(
  in uint value
);
```

## <a name="parameters"></a><span data-ttu-id="d2a63-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="d2a63-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2a63-108">*valore* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="d2a63-108">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2a63-109">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="d2a63-109">Type: **uint**</span></span>

<span data-ttu-id="d2a63-110">Valore di input.</span><span class="sxs-lookup"><span data-stu-id="d2a63-110">The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2a63-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d2a63-111">Return value</span></span>

<span data-ttu-id="d2a63-112">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="d2a63-112">Type: **uint**</span></span>

<span data-ttu-id="d2a63-113">Numero di bit.</span><span class="sxs-lookup"><span data-stu-id="d2a63-113">The number of bits.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2a63-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="d2a63-114">Remarks</span></span>

<span data-ttu-id="d2a63-115">Sono disponibili anche le seguenti versioni di overload:</span><span class="sxs-lookup"><span data-stu-id="d2a63-115">The following overloaded versions are also available:</span></span>

``` syntax
uint count_bits(uint value);
uint2 count_bits(uint2 value);
uint3 count_bits(uint3 value);
uint4 count_bits(uint4 value);
```

### <a name="minimum-shader-model"></a><span data-ttu-id="d2a63-116">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="d2a63-116">Minimum Shader Model</span></span>

<span data-ttu-id="d2a63-117">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="d2a63-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="d2a63-118">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="d2a63-118">Shader Model</span></span>                                                                | <span data-ttu-id="d2a63-119">Supportato</span><span class="sxs-lookup"><span data-stu-id="d2a63-119">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="d2a63-120">[Shader Model 5](d3d11-graphics-reference-sm5.md) e versioni successive shader Models</span><span class="sxs-lookup"><span data-stu-id="d2a63-120">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="d2a63-121">sì</span><span class="sxs-lookup"><span data-stu-id="d2a63-121">yes</span></span>       |



 

<span data-ttu-id="d2a63-122">Questa funzione è supportata nei tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="d2a63-122">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="d2a63-123">Vertice</span><span class="sxs-lookup"><span data-stu-id="d2a63-123">Vertex</span></span> | <span data-ttu-id="d2a63-124">Hull</span><span class="sxs-lookup"><span data-stu-id="d2a63-124">Hull</span></span> | <span data-ttu-id="d2a63-125">Dominio</span><span class="sxs-lookup"><span data-stu-id="d2a63-125">Domain</span></span> | <span data-ttu-id="d2a63-126">Geometria</span><span class="sxs-lookup"><span data-stu-id="d2a63-126">Geometry</span></span> | <span data-ttu-id="d2a63-127">Pixel</span><span class="sxs-lookup"><span data-stu-id="d2a63-127">Pixel</span></span> | <span data-ttu-id="d2a63-128">Calcolo</span><span class="sxs-lookup"><span data-stu-id="d2a63-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="d2a63-129">x</span><span class="sxs-lookup"><span data-stu-id="d2a63-129">x</span></span>      | <span data-ttu-id="d2a63-130">x</span><span class="sxs-lookup"><span data-stu-id="d2a63-130">x</span></span>    | <span data-ttu-id="d2a63-131">x</span><span class="sxs-lookup"><span data-stu-id="d2a63-131">x</span></span>      | <span data-ttu-id="d2a63-132">x</span><span class="sxs-lookup"><span data-stu-id="d2a63-132">x</span></span>        | <span data-ttu-id="d2a63-133">x</span><span class="sxs-lookup"><span data-stu-id="d2a63-133">x</span></span>     | <span data-ttu-id="d2a63-134">x</span><span class="sxs-lookup"><span data-stu-id="d2a63-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="d2a63-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d2a63-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2a63-136">Funzioni intrinseche</span><span class="sxs-lookup"><span data-stu-id="d2a63-136">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="d2a63-137">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="d2a63-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




