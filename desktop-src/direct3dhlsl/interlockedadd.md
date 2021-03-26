---
title: Funzione InterlockedAdd (riferimento HLSL)
description: Esegue un aggiunta atomico garantita del valore alla variabile di risorsa dest.
ms.assetid: b3b9cf5c-0da0-4c72-a83f-a0d96f1cac32
keywords:
- Funzione InterlockedAdd HLSL
topic_type:
- apiref
api_name:
- InterlockedAdd
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1d58965ea47fcad8452979a8c8ffe5b289392850
ms.sourcegitcommit: 12e9b14501d51641b690ee0cf764e2b91eb9a140
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/06/2020
ms.locfileid: "104398465"
---
# <a name="interlockedadd-function-hlsl-reference"></a><span data-ttu-id="bbc0d-104">Funzione InterlockedAdd (riferimento HLSL)</span><span class="sxs-lookup"><span data-stu-id="bbc0d-104">InterlockedAdd function (HLSL reference)</span></span>

<span data-ttu-id="bbc0d-105">Esegue un aggiunta atomico garantita del valore alla variabile di risorsa dest.</span><span class="sxs-lookup"><span data-stu-id="bbc0d-105">Performs a guaranteed atomic add of value to the dest resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbc0d-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bbc0d-106">Syntax</span></span>

``` syntax
void InterlockedAdd(
  in  R dest,
  in  T value,
  out T original_value
);
```

## <a name="parameters"></a><span data-ttu-id="bbc0d-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="bbc0d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bbc0d-108">*dest* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bbc0d-108">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bbc0d-109">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="bbc0d-109">Type: **R**</span></span>

<span data-ttu-id="bbc0d-110">Indirizzo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="bbc0d-110">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="bbc0d-111">*valore* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="bbc0d-111">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bbc0d-112">Tipo: **T**</span><span class="sxs-lookup"><span data-stu-id="bbc0d-112">Type: **T**</span></span>

<span data-ttu-id="bbc0d-113">Valore di input.</span><span class="sxs-lookup"><span data-stu-id="bbc0d-113">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="bbc0d-114">*\_ valore originale* in \[ uscita\]</span><span class="sxs-lookup"><span data-stu-id="bbc0d-114">*original\_value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bbc0d-115">Tipo: **T**</span><span class="sxs-lookup"><span data-stu-id="bbc0d-115">Type: **T**</span></span>

<span data-ttu-id="bbc0d-116">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="bbc0d-116">Optional.</span></span> <span data-ttu-id="bbc0d-117">Valore di input originale.</span><span class="sxs-lookup"><span data-stu-id="bbc0d-117">The original input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bbc0d-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bbc0d-118">Return value</span></span>

<span data-ttu-id="bbc0d-119">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="bbc0d-119">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bbc0d-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="bbc0d-120">Remarks</span></span>

<span data-ttu-id="bbc0d-121">Questa operazione può essere eseguita solo su risorse tipizzate int o uint e variabili di memoria condivisa.</span><span class="sxs-lookup"><span data-stu-id="bbc0d-121">This operation can only be performed on int or uint typed resources and shared memory variables.</span></span> <span data-ttu-id="bbc0d-122">Esistono due possibili usi per questa funzione.</span><span class="sxs-lookup"><span data-stu-id="bbc0d-122">There are two possible uses for this function.</span></span> <span data-ttu-id="bbc0d-123">Il primo è quando R è un tipo di variabile di memoria condivisa.</span><span class="sxs-lookup"><span data-stu-id="bbc0d-123">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="bbc0d-124">In questo caso, la funzione esegue un aggiunta atomico del valore al registro della memoria condivisa a cui fa riferimento dest.</span><span class="sxs-lookup"><span data-stu-id="bbc0d-124">In this case, the function performs an atomic add of value to the shared memory register referenced by dest.</span></span> <span data-ttu-id="bbc0d-125">Il secondo scenario è quando R è un tipo di variabile di risorsa.</span><span class="sxs-lookup"><span data-stu-id="bbc0d-125">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="bbc0d-126">In questo scenario, la funzione esegue un aggiunta atomica di valore al percorso della risorsa a cui fa riferimento dest.</span><span class="sxs-lookup"><span data-stu-id="bbc0d-126">In this scenario, the function performs an atomic add of value to the resource location referenced by dest.</span></span> <span data-ttu-id="bbc0d-127">La funzione in overload ha una variabile di output aggiuntiva che verrà impostata sul valore originale di dest.</span><span class="sxs-lookup"><span data-stu-id="bbc0d-127">The overloaded function has an additional output variable which will be set to the original value of dest.</span></span> <span data-ttu-id="bbc0d-128">Questa operazione di overload è disponibile solo quando R è leggibile e scrivibile.</span><span class="sxs-lookup"><span data-stu-id="bbc0d-128">This overloaded operation is only available when R is readable and writable.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="bbc0d-129">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="bbc0d-129">Minimum Shader Model</span></span>

<span data-ttu-id="bbc0d-130">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="bbc0d-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="bbc0d-131">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="bbc0d-131">Shader Model</span></span>                                                                | <span data-ttu-id="bbc0d-132">Supportato</span><span class="sxs-lookup"><span data-stu-id="bbc0d-132">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="bbc0d-133">[Shader Model 5](d3d11-graphics-reference-sm5.md) e versioni successive shader Models</span><span class="sxs-lookup"><span data-stu-id="bbc0d-133">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="bbc0d-134">sì</span><span class="sxs-lookup"><span data-stu-id="bbc0d-134">yes</span></span>       |



 

<span data-ttu-id="bbc0d-135">Questa funzione è supportata nei tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="bbc0d-135">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="bbc0d-136">Vertice</span><span class="sxs-lookup"><span data-stu-id="bbc0d-136">Vertex</span></span> | <span data-ttu-id="bbc0d-137">Hull</span><span class="sxs-lookup"><span data-stu-id="bbc0d-137">Hull</span></span> | <span data-ttu-id="bbc0d-138">Dominio</span><span class="sxs-lookup"><span data-stu-id="bbc0d-138">Domain</span></span> | <span data-ttu-id="bbc0d-139">Geometria</span><span class="sxs-lookup"><span data-stu-id="bbc0d-139">Geometry</span></span> | <span data-ttu-id="bbc0d-140">Pixel</span><span class="sxs-lookup"><span data-stu-id="bbc0d-140">Pixel</span></span> | <span data-ttu-id="bbc0d-141">Calcolo</span><span class="sxs-lookup"><span data-stu-id="bbc0d-141">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="bbc0d-142">x</span><span class="sxs-lookup"><span data-stu-id="bbc0d-142">x</span></span>      | <span data-ttu-id="bbc0d-143">x</span><span class="sxs-lookup"><span data-stu-id="bbc0d-143">x</span></span>    | <span data-ttu-id="bbc0d-144">x</span><span class="sxs-lookup"><span data-stu-id="bbc0d-144">x</span></span>      | <span data-ttu-id="bbc0d-145">x</span><span class="sxs-lookup"><span data-stu-id="bbc0d-145">x</span></span>        | <span data-ttu-id="bbc0d-146">x</span><span class="sxs-lookup"><span data-stu-id="bbc0d-146">x</span></span>     | <span data-ttu-id="bbc0d-147">x</span><span class="sxs-lookup"><span data-stu-id="bbc0d-147">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="bbc0d-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bbc0d-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbc0d-149">Funzioni intrinseche</span><span class="sxs-lookup"><span data-stu-id="bbc0d-149">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="bbc0d-150">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="bbc0d-150">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




