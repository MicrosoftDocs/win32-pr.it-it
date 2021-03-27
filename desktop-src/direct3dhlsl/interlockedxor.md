---
title: Funzione InterlockedXor (riferimento HLSL)
description: Esegue un XOR atomico garantito.
ms.assetid: 844ca31f-d051-4713-b9e1-dd6712ad36ca
keywords:
- Funzione InterlockedXor HLSL
topic_type:
- apiref
api_name:
- InterlockedXor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b8ecaf0aa78a3bd2c1d79d10bea1e97299605398
ms.sourcegitcommit: 12e9b14501d51641b690ee0cf764e2b91eb9a140
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/06/2020
ms.locfileid: "103720070"
---
# <a name="interlockedxor-function-hlsl-reference"></a><span data-ttu-id="d2c83-104">Funzione InterlockedXor (riferimento HLSL)</span><span class="sxs-lookup"><span data-stu-id="d2c83-104">InterlockedXor function (HLSL reference)</span></span>

<span data-ttu-id="d2c83-105">Esegue un XOR atomico garantito.</span><span class="sxs-lookup"><span data-stu-id="d2c83-105">Performs a guaranteed atomic xor.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2c83-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d2c83-106">Syntax</span></span>

``` syntax
void InterlockedXor(
  in  R dest,
  in  T value,
  out T original_value
);
```

## <a name="parameters"></a><span data-ttu-id="d2c83-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="d2c83-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2c83-108">*dest* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d2c83-108">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2c83-109">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="d2c83-109">Type: **R**</span></span>

<span data-ttu-id="d2c83-110">Indirizzo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="d2c83-110">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="d2c83-111">*valore* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="d2c83-111">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2c83-112">Tipo: **T**</span><span class="sxs-lookup"><span data-stu-id="d2c83-112">Type: **T**</span></span>

<span data-ttu-id="d2c83-113">Valore di input.</span><span class="sxs-lookup"><span data-stu-id="d2c83-113">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="d2c83-114">*\_ valore originale* in \[ uscita\]</span><span class="sxs-lookup"><span data-stu-id="d2c83-114">*original\_value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d2c83-115">Tipo: **T**</span><span class="sxs-lookup"><span data-stu-id="d2c83-115">Type: **T**</span></span>

<span data-ttu-id="d2c83-116">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="d2c83-116">Optional.</span></span> <span data-ttu-id="d2c83-117">Valore di input originale.</span><span class="sxs-lookup"><span data-stu-id="d2c83-117">The original input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2c83-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d2c83-118">Return value</span></span>

<span data-ttu-id="d2c83-119">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="d2c83-119">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2c83-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="d2c83-120">Remarks</span></span>

<span data-ttu-id="d2c83-121">Questa operazione può essere eseguita solo su risorse tipizzate int o uint e variabili di memoria condivisa.</span><span class="sxs-lookup"><span data-stu-id="d2c83-121">This operation can only be performed on int or uint typed resources and shared memory variables.</span></span> <span data-ttu-id="d2c83-122">Esistono due possibili usi per questa funzione.</span><span class="sxs-lookup"><span data-stu-id="d2c83-122">There are two possible uses for this function.</span></span> <span data-ttu-id="d2c83-123">Il primo è quando R è un tipo di variabile di memoria condivisa.</span><span class="sxs-lookup"><span data-stu-id="d2c83-123">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="d2c83-124">In questo caso, la funzione esegue un XOR atomico di valore al registro di memoria condiviso a cui fa riferimento dest.</span><span class="sxs-lookup"><span data-stu-id="d2c83-124">In this case, the function performs an atomic XOR of value to the shared memory register referenced by dest.</span></span> <span data-ttu-id="d2c83-125">Il secondo scenario è quando R è un tipo di variabile di risorsa.</span><span class="sxs-lookup"><span data-stu-id="d2c83-125">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="d2c83-126">In questo scenario, la funzione esegue un valore atomico XORof per la posizione della risorsa a cui fa riferimento dest.</span><span class="sxs-lookup"><span data-stu-id="d2c83-126">In this scenario, the function performs an atomic XORof value to the resource location referenced by dest.</span></span> <span data-ttu-id="d2c83-127">La funzione in overload ha una variabile di output aggiuntiva che verrà impostata sul valore originale di dest.</span><span class="sxs-lookup"><span data-stu-id="d2c83-127">The overloaded function has an additional output variable which will be set to the original value of dest.</span></span> <span data-ttu-id="d2c83-128">Questa operazione di overload è disponibile solo quando R è leggibile e scrivibile.</span><span class="sxs-lookup"><span data-stu-id="d2c83-128">This overloaded operation is only available when R is readable and writable.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="d2c83-129">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="d2c83-129">Minimum Shader Model</span></span>

<span data-ttu-id="d2c83-130">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="d2c83-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="d2c83-131">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="d2c83-131">Shader Model</span></span>                                                                | <span data-ttu-id="d2c83-132">Supportato</span><span class="sxs-lookup"><span data-stu-id="d2c83-132">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="d2c83-133">[Shader Model 5](d3d11-graphics-reference-sm5.md) e versioni successive shader Models</span><span class="sxs-lookup"><span data-stu-id="d2c83-133">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="d2c83-134">sì</span><span class="sxs-lookup"><span data-stu-id="d2c83-134">yes</span></span>       |



 

<span data-ttu-id="d2c83-135">Questa funzione è supportata nei tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="d2c83-135">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="d2c83-136">Vertice</span><span class="sxs-lookup"><span data-stu-id="d2c83-136">Vertex</span></span> | <span data-ttu-id="d2c83-137">Hull</span><span class="sxs-lookup"><span data-stu-id="d2c83-137">Hull</span></span> | <span data-ttu-id="d2c83-138">Dominio</span><span class="sxs-lookup"><span data-stu-id="d2c83-138">Domain</span></span> | <span data-ttu-id="d2c83-139">Geometria</span><span class="sxs-lookup"><span data-stu-id="d2c83-139">Geometry</span></span> | <span data-ttu-id="d2c83-140">Pixel</span><span class="sxs-lookup"><span data-stu-id="d2c83-140">Pixel</span></span> | <span data-ttu-id="d2c83-141">Calcolo</span><span class="sxs-lookup"><span data-stu-id="d2c83-141">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|  <span data-ttu-id="d2c83-142">x</span><span class="sxs-lookup"><span data-stu-id="d2c83-142">x</span></span>     |  <span data-ttu-id="d2c83-143">x</span><span class="sxs-lookup"><span data-stu-id="d2c83-143">x</span></span>   | <span data-ttu-id="d2c83-144">x</span><span class="sxs-lookup"><span data-stu-id="d2c83-144">x</span></span>      |  <span data-ttu-id="d2c83-145">x</span><span class="sxs-lookup"><span data-stu-id="d2c83-145">x</span></span>       | <span data-ttu-id="d2c83-146">x</span><span class="sxs-lookup"><span data-stu-id="d2c83-146">x</span></span>     | <span data-ttu-id="d2c83-147">x</span><span class="sxs-lookup"><span data-stu-id="d2c83-147">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="d2c83-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d2c83-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2c83-149">Funzioni intrinseche</span><span class="sxs-lookup"><span data-stu-id="d2c83-149">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="d2c83-150">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="d2c83-150">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




