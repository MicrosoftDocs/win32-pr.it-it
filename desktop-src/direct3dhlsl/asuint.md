---
title: asuint (funzione)
description: Reinterpreta lo schema di bit di un valore a 64 bit come due interi senza segno a 32 bit.
ms.assetid: 29671661-4fec-46e5-9b6f-56fba8e1d756
keywords:
- funzione asuint HLSL
topic_type:
- apiref
api_name:
- asuint
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c54ed89e112482df4a54f35e24a04694e88fa490
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104045892"
---
# <a name="asuint-function"></a><span data-ttu-id="9f616-104">asuint (funzione)</span><span class="sxs-lookup"><span data-stu-id="9f616-104">asuint function</span></span>

<span data-ttu-id="9f616-105">Reinterpreta lo schema di bit di un valore a 64 bit come due interi senza segno a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="9f616-105">Reinterprets the bit pattern of a 64-bit value as two unsigned 32-bit integers.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f616-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9f616-106">Syntax</span></span>

``` syntax
void asuint(
  in  double value,
  out uint lowbits,
  out uint highbits
);
```

## <a name="parameters"></a><span data-ttu-id="9f616-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="9f616-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f616-108">*valore* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="9f616-108">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f616-109">Tipo: **Double**</span><span class="sxs-lookup"><span data-stu-id="9f616-109">Type: **double**</span></span>

<span data-ttu-id="9f616-110">Valore di input.</span><span class="sxs-lookup"><span data-stu-id="9f616-110">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="9f616-111">*lowbits* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9f616-111">*lowbits* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9f616-112">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="9f616-112">Type: **uint**</span></span>

<span data-ttu-id="9f616-113">Modello a 32 bit basso di *value*.</span><span class="sxs-lookup"><span data-stu-id="9f616-113">The low 32-bit pattern of *value*.</span></span>

</dd> <dt>

<span data-ttu-id="9f616-114">*highbits* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9f616-114">*highbits* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9f616-115">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="9f616-115">Type: **uint**</span></span>

<span data-ttu-id="9f616-116">Modello a 32 bit elevato di *value*.</span><span class="sxs-lookup"><span data-stu-id="9f616-116">The high 32-bit pattern of *value*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f616-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9f616-117">Return value</span></span>

<span data-ttu-id="9f616-118">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="9f616-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f616-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="9f616-119">Remarks</span></span>

<span data-ttu-id="9f616-120">Questa funzione è una versione alternativa della funzione intrinseca [**asuint**](dx-graphics-hlsl-asuint.md) disponibile nei modelli shader precedenti ed è stata introdotta per il modello di shader 5.</span><span class="sxs-lookup"><span data-stu-id="9f616-120">This function is an alternate version of the [**asuint**](dx-graphics-hlsl-asuint.md) intrinsic that has been available in earlier shader models, and was introduced for Shader Model 5.</span></span> <span data-ttu-id="9f616-121">La funzione originale, riconosciuta nel compilatore HLSL con la firma diversa, rimane disponibile per il modello di shader 5.</span><span class="sxs-lookup"><span data-stu-id="9f616-121">The original function (recognized in the HLSL compiler by its different signature) remains available to Shader Model 5.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="9f616-122">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="9f616-122">Minimum Shader Model</span></span>

<span data-ttu-id="9f616-123">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="9f616-123">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="9f616-124">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="9f616-124">Shader Model</span></span>                                                                | <span data-ttu-id="9f616-125">Supportato</span><span class="sxs-lookup"><span data-stu-id="9f616-125">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="9f616-126">[Shader Model 5](d3d11-graphics-reference-sm5.md) e versioni successive shader Models</span><span class="sxs-lookup"><span data-stu-id="9f616-126">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="9f616-127">sì</span><span class="sxs-lookup"><span data-stu-id="9f616-127">yes</span></span>       |



 

<span data-ttu-id="9f616-128">Questa funzione è supportata nei tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="9f616-128">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="9f616-129">Vertice</span><span class="sxs-lookup"><span data-stu-id="9f616-129">Vertex</span></span> | <span data-ttu-id="9f616-130">Hull</span><span class="sxs-lookup"><span data-stu-id="9f616-130">Hull</span></span> | <span data-ttu-id="9f616-131">Dominio</span><span class="sxs-lookup"><span data-stu-id="9f616-131">Domain</span></span> | <span data-ttu-id="9f616-132">Geometria</span><span class="sxs-lookup"><span data-stu-id="9f616-132">Geometry</span></span> | <span data-ttu-id="9f616-133">Pixel</span><span class="sxs-lookup"><span data-stu-id="9f616-133">Pixel</span></span> | <span data-ttu-id="9f616-134">Calcolo</span><span class="sxs-lookup"><span data-stu-id="9f616-134">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="9f616-135">x</span><span class="sxs-lookup"><span data-stu-id="9f616-135">x</span></span>      | <span data-ttu-id="9f616-136">x</span><span class="sxs-lookup"><span data-stu-id="9f616-136">x</span></span>    | <span data-ttu-id="9f616-137">x</span><span class="sxs-lookup"><span data-stu-id="9f616-137">x</span></span>      | <span data-ttu-id="9f616-138">x</span><span class="sxs-lookup"><span data-stu-id="9f616-138">x</span></span>        | <span data-ttu-id="9f616-139">x</span><span class="sxs-lookup"><span data-stu-id="9f616-139">x</span></span>     | <span data-ttu-id="9f616-140">x</span><span class="sxs-lookup"><span data-stu-id="9f616-140">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="9f616-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9f616-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f616-142">Funzioni intrinseche</span><span class="sxs-lookup"><span data-stu-id="9f616-142">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="9f616-143">**asuint (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="9f616-143">**asuint (DirectX HLSL)**</span></span>](dx-graphics-hlsl-asuint.md)
</dt> <dt>

[<span data-ttu-id="9f616-144">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="9f616-144">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




