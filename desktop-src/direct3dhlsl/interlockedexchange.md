---
title: Funzione InterlockedExchange (riferimento HLSL)
description: Assegna il valore a dest e restituisce il valore originale.
ms.assetid: 1e7ce7ff-9e23-47fa-8e76-713f6bf57abf
keywords:
- Funzione InterlockedExchange HLSL
topic_type:
- apiref
api_name:
- InterlockedExchange
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7c39dc4f68429fa3f070d446f998fd528a99af01
ms.sourcegitcommit: 12e9b14501d51641b690ee0cf764e2b91eb9a140
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/06/2020
ms.locfileid: "104976583"
---
# <a name="interlockedexchange-function-hlsl-reference"></a><span data-ttu-id="85432-104">Funzione InterlockedExchange (riferimento HLSL)</span><span class="sxs-lookup"><span data-stu-id="85432-104">InterlockedExchange function (HLSL reference)</span></span>

<span data-ttu-id="85432-105">Assegna il valore a dest e restituisce il valore originale.</span><span class="sxs-lookup"><span data-stu-id="85432-105">Assigns value to dest and returns the original value.</span></span>

## <a name="syntax"></a><span data-ttu-id="85432-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="85432-106">Syntax</span></span>

``` syntax
void InterlockedExchange(
  in  R dest,
  in  T value,
  out T original_value
);
```

## <a name="parameters"></a><span data-ttu-id="85432-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="85432-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85432-108">*dest* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="85432-108">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85432-109">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="85432-109">Type: **R**</span></span>

<span data-ttu-id="85432-110">Indirizzo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="85432-110">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="85432-111">*valore* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="85432-111">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85432-112">Tipo: **T**</span><span class="sxs-lookup"><span data-stu-id="85432-112">Type: **T**</span></span>

<span data-ttu-id="85432-113">Valore di input.</span><span class="sxs-lookup"><span data-stu-id="85432-113">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="85432-114">*\_ valore originale* in \[ uscita\]</span><span class="sxs-lookup"><span data-stu-id="85432-114">*original\_value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="85432-115">Tipo: **T**</span><span class="sxs-lookup"><span data-stu-id="85432-115">Type: **T**</span></span>

<span data-ttu-id="85432-116">Valore originale.</span><span class="sxs-lookup"><span data-stu-id="85432-116">The original value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85432-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="85432-117">Return value</span></span>

<span data-ttu-id="85432-118">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="85432-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="85432-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="85432-119">Remarks</span></span>

<span data-ttu-id="85432-120">Questa operazione può essere eseguita solo su risorse con tipizzazione scalare e variabili di memoria condivisa.</span><span class="sxs-lookup"><span data-stu-id="85432-120">This operation can only be performed on scalar-typed resources and shared memory variables.</span></span> <span data-ttu-id="85432-121">Esistono due possibili usi per questa funzione.</span><span class="sxs-lookup"><span data-stu-id="85432-121">There are two possible uses for this function.</span></span> <span data-ttu-id="85432-122">Il primo è quando R è un tipo di variabile di memoria condivisa.</span><span class="sxs-lookup"><span data-stu-id="85432-122">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="85432-123">In questo caso, la funzione esegue l'operazione sul Registro di memoria condiviso a cui fa riferimento dest.</span><span class="sxs-lookup"><span data-stu-id="85432-123">In this case, the function performs the operation on the shared memory register referenced by dest.</span></span> <span data-ttu-id="85432-124">Il secondo scenario è quando R è un tipo di variabile di risorsa.</span><span class="sxs-lookup"><span data-stu-id="85432-124">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="85432-125">In questo scenario, la funzione esegue l'operazione sul percorso della risorsa a cui fa riferimento dest.</span><span class="sxs-lookup"><span data-stu-id="85432-125">In this scenario, the function performs the operation on the resource location referenced by dest.</span></span> <span data-ttu-id="85432-126">Questa operazione è disponibile solo se R è leggibile e scrivibile.</span><span class="sxs-lookup"><span data-stu-id="85432-126">This operation is only available when R is readable and writable.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="85432-127">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="85432-127">Minimum Shader Model</span></span>

<span data-ttu-id="85432-128">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="85432-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="85432-129">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="85432-129">Shader Model</span></span>                                                                | <span data-ttu-id="85432-130">Supportato</span><span class="sxs-lookup"><span data-stu-id="85432-130">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="85432-131">[Shader Model 5](d3d11-graphics-reference-sm5.md) e versioni successive shader Models</span><span class="sxs-lookup"><span data-stu-id="85432-131">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="85432-132">sì</span><span class="sxs-lookup"><span data-stu-id="85432-132">yes</span></span>       |



 

<span data-ttu-id="85432-133">Questa funzione è supportata nei tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="85432-133">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="85432-134">Vertice</span><span class="sxs-lookup"><span data-stu-id="85432-134">Vertex</span></span> | <span data-ttu-id="85432-135">Hull</span><span class="sxs-lookup"><span data-stu-id="85432-135">Hull</span></span> | <span data-ttu-id="85432-136">Dominio</span><span class="sxs-lookup"><span data-stu-id="85432-136">Domain</span></span> | <span data-ttu-id="85432-137">Geometria</span><span class="sxs-lookup"><span data-stu-id="85432-137">Geometry</span></span> | <span data-ttu-id="85432-138">Pixel</span><span class="sxs-lookup"><span data-stu-id="85432-138">Pixel</span></span> | <span data-ttu-id="85432-139">Calcolo</span><span class="sxs-lookup"><span data-stu-id="85432-139">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="85432-140">x</span><span class="sxs-lookup"><span data-stu-id="85432-140">x</span></span>      |  <span data-ttu-id="85432-141">x</span><span class="sxs-lookup"><span data-stu-id="85432-141">x</span></span>   | <span data-ttu-id="85432-142">x</span><span class="sxs-lookup"><span data-stu-id="85432-142">x</span></span>      |  <span data-ttu-id="85432-143">x</span><span class="sxs-lookup"><span data-stu-id="85432-143">x</span></span>       | <span data-ttu-id="85432-144">x</span><span class="sxs-lookup"><span data-stu-id="85432-144">x</span></span>     | <span data-ttu-id="85432-145">x</span><span class="sxs-lookup"><span data-stu-id="85432-145">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="85432-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="85432-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85432-147">Funzioni intrinseche</span><span class="sxs-lookup"><span data-stu-id="85432-147">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="85432-148">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="85432-148">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




