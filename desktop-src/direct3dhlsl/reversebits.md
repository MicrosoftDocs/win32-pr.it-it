---
title: reversebits (funzione)
description: Inverte l'ordine dei bit, per componente.
ms.assetid: dad46e25-9980-4645-98eb-d834db704fc8
keywords:
- funzione reversebits HLSL
topic_type:
- apiref
api_name:
- reversebits
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d98b824883ddc4f06e6c11d30c2759bb0fc2be26
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104471958"
---
# <a name="reversebits-function"></a><span data-ttu-id="8267e-104">reversebits (funzione)</span><span class="sxs-lookup"><span data-stu-id="8267e-104">reversebits function</span></span>

<span data-ttu-id="8267e-105">Inverte l'ordine dei bit, per componente.</span><span class="sxs-lookup"><span data-stu-id="8267e-105">Reverses the order of the bits, per component.</span></span>

## <a name="syntax"></a><span data-ttu-id="8267e-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8267e-106">Syntax</span></span>

``` syntax
uint reversebits(
  in uint value
);
```

## <a name="parameters"></a><span data-ttu-id="8267e-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="8267e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8267e-108">*valore* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="8267e-108">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8267e-109">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="8267e-109">Type: **uint**</span></span>

<span data-ttu-id="8267e-110">Valore di input.</span><span class="sxs-lookup"><span data-stu-id="8267e-110">The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8267e-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8267e-111">Return value</span></span>

<span data-ttu-id="8267e-112">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="8267e-112">Type: **uint**</span></span>

<span data-ttu-id="8267e-113">Valore di input, con l'ordine dei bit invertito.</span><span class="sxs-lookup"><span data-stu-id="8267e-113">The input value, with the bit order reversed.</span></span>

## <a name="remarks"></a><span data-ttu-id="8267e-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="8267e-114">Remarks</span></span>

<span data-ttu-id="8267e-115">Sono disponibili anche le seguenti versioni di overload:</span><span class="sxs-lookup"><span data-stu-id="8267e-115">The following overloaded versions are also available:</span></span>

``` syntax
uint2 reversebits(uint2 value);
uint3 reversebits(uint3 value);
uint4 reversebits(uint4 value);
```

### <a name="minimum-shader-model"></a><span data-ttu-id="8267e-116">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="8267e-116">Minimum Shader Model</span></span>

<span data-ttu-id="8267e-117">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="8267e-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="8267e-118">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="8267e-118">Shader Model</span></span>                                                                | <span data-ttu-id="8267e-119">Supportato</span><span class="sxs-lookup"><span data-stu-id="8267e-119">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="8267e-120">[Shader Model 5](d3d11-graphics-reference-sm5.md) e versioni successive shader Models</span><span class="sxs-lookup"><span data-stu-id="8267e-120">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="8267e-121">sì</span><span class="sxs-lookup"><span data-stu-id="8267e-121">yes</span></span>       |



 

<span data-ttu-id="8267e-122">Questa funzione è supportata nei tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="8267e-122">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="8267e-123">Vertice</span><span class="sxs-lookup"><span data-stu-id="8267e-123">Vertex</span></span> | <span data-ttu-id="8267e-124">Hull</span><span class="sxs-lookup"><span data-stu-id="8267e-124">Hull</span></span> | <span data-ttu-id="8267e-125">Dominio</span><span class="sxs-lookup"><span data-stu-id="8267e-125">Domain</span></span> | <span data-ttu-id="8267e-126">Geometria</span><span class="sxs-lookup"><span data-stu-id="8267e-126">Geometry</span></span> | <span data-ttu-id="8267e-127">Pixel</span><span class="sxs-lookup"><span data-stu-id="8267e-127">Pixel</span></span> | <span data-ttu-id="8267e-128">Calcolo</span><span class="sxs-lookup"><span data-stu-id="8267e-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="8267e-129">x</span><span class="sxs-lookup"><span data-stu-id="8267e-129">x</span></span>      | <span data-ttu-id="8267e-130">x</span><span class="sxs-lookup"><span data-stu-id="8267e-130">x</span></span>    | <span data-ttu-id="8267e-131">x</span><span class="sxs-lookup"><span data-stu-id="8267e-131">x</span></span>      | <span data-ttu-id="8267e-132">x</span><span class="sxs-lookup"><span data-stu-id="8267e-132">x</span></span>        | <span data-ttu-id="8267e-133">x</span><span class="sxs-lookup"><span data-stu-id="8267e-133">x</span></span>     | <span data-ttu-id="8267e-134">x</span><span class="sxs-lookup"><span data-stu-id="8267e-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="8267e-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8267e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8267e-136">Funzioni intrinseche</span><span class="sxs-lookup"><span data-stu-id="8267e-136">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="8267e-137">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="8267e-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




