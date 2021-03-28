---
title: Funzione interlockedr (riferimento HLSL)
description: Esegue un oggetto atomico garantito o.
ms.assetid: ecbe6b2f-8eff-41d7-9ca3-4487c9ffeaf6
keywords:
- Funzione di interblocco HLSL
topic_type:
- apiref
api_name:
- InterlockedOr
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 36ab900416d6d04e0e47a843aa345c1a01318c50
ms.sourcegitcommit: 12e9b14501d51641b690ee0cf764e2b91eb9a140
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/06/2020
ms.locfileid: "104993328"
---
# <a name="interlockedor-function-hlsl-reference"></a><span data-ttu-id="6bbf2-104">Funzione interlockedr (riferimento HLSL)</span><span class="sxs-lookup"><span data-stu-id="6bbf2-104">InterlockedOr function (HLSL reference)</span></span>

<span data-ttu-id="6bbf2-105">Esegue un oggetto atomico garantito o.</span><span class="sxs-lookup"><span data-stu-id="6bbf2-105">Performs a guaranteed atomic or.</span></span>

## <a name="syntax"></a><span data-ttu-id="6bbf2-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6bbf2-106">Syntax</span></span>

``` syntax
void InterlockedOr(
  in  R dest,
  in  T value,
  out T original_value
);
```

## <a name="parameters"></a><span data-ttu-id="6bbf2-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="6bbf2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6bbf2-108">*dest* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6bbf2-108">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6bbf2-109">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="6bbf2-109">Type: **R**</span></span>

<span data-ttu-id="6bbf2-110">Indirizzo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="6bbf2-110">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="6bbf2-111">*valore* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="6bbf2-111">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6bbf2-112">Tipo: **T**</span><span class="sxs-lookup"><span data-stu-id="6bbf2-112">Type: **T**</span></span>

<span data-ttu-id="6bbf2-113">Valore di input.</span><span class="sxs-lookup"><span data-stu-id="6bbf2-113">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="6bbf2-114">*\_ valore originale* in \[ uscita\]</span><span class="sxs-lookup"><span data-stu-id="6bbf2-114">*original\_value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6bbf2-115">Tipo: **T**</span><span class="sxs-lookup"><span data-stu-id="6bbf2-115">Type: **T**</span></span>

<span data-ttu-id="6bbf2-116">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="6bbf2-116">Optional.</span></span> <span data-ttu-id="6bbf2-117">Valore di input originale.</span><span class="sxs-lookup"><span data-stu-id="6bbf2-117">The original input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6bbf2-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6bbf2-118">Return value</span></span>

<span data-ttu-id="6bbf2-119">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="6bbf2-119">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6bbf2-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="6bbf2-120">Remarks</span></span>

<span data-ttu-id="6bbf2-121">Questa operazione può essere eseguita solo su risorse tipizzate int o uint e variabili di memoria condivisa.</span><span class="sxs-lookup"><span data-stu-id="6bbf2-121">This operation can only be performed on int or uint typed resources and shared memory variables.</span></span> <span data-ttu-id="6bbf2-122">Esistono due possibili usi per questa funzione.</span><span class="sxs-lookup"><span data-stu-id="6bbf2-122">There are two possible uses for this function.</span></span> <span data-ttu-id="6bbf2-123">Il primo è quando R è un tipo di variabile di memoria condivisa.</span><span class="sxs-lookup"><span data-stu-id="6bbf2-123">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="6bbf2-124">In questo caso, la funzione esegue un'operazione atomica o di valore nel registro di memoria condivisa a cui fa riferimento dest.</span><span class="sxs-lookup"><span data-stu-id="6bbf2-124">In this case, the function performs an atomic or of value to the shared memory register referenced by dest.</span></span> <span data-ttu-id="6bbf2-125">Il secondo scenario è quando R è un tipo di variabile di risorsa.</span><span class="sxs-lookup"><span data-stu-id="6bbf2-125">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="6bbf2-126">In questo scenario, la funzione esegue un'operazione atomica o di valore nel percorso della risorsa a cui fa riferimento dest.</span><span class="sxs-lookup"><span data-stu-id="6bbf2-126">In this scenario, the function performs an atomic or of value to the resource location referenced by dest.</span></span> <span data-ttu-id="6bbf2-127">La funzione in overload ha una variabile di output aggiuntiva che verrà impostata sul valore originale di dest.</span><span class="sxs-lookup"><span data-stu-id="6bbf2-127">The overloaded function has an additional output variable which will be set to the original value of dest.</span></span> <span data-ttu-id="6bbf2-128">Questa operazione di overload è disponibile solo quando R è leggibile e scrivibile.</span><span class="sxs-lookup"><span data-stu-id="6bbf2-128">This overloaded operation is only available when R is readable and writable.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="6bbf2-129">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="6bbf2-129">Minimum Shader Model</span></span>

<span data-ttu-id="6bbf2-130">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="6bbf2-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="6bbf2-131">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="6bbf2-131">Shader Model</span></span>                                                                | <span data-ttu-id="6bbf2-132">Supportato</span><span class="sxs-lookup"><span data-stu-id="6bbf2-132">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="6bbf2-133">[Shader Model 5](d3d11-graphics-reference-sm5.md) e versioni successive shader Models</span><span class="sxs-lookup"><span data-stu-id="6bbf2-133">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="6bbf2-134">sì</span><span class="sxs-lookup"><span data-stu-id="6bbf2-134">yes</span></span>       |



 

<span data-ttu-id="6bbf2-135">Questa funzione è supportata nei tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="6bbf2-135">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="6bbf2-136">Vertice</span><span class="sxs-lookup"><span data-stu-id="6bbf2-136">Vertex</span></span> | <span data-ttu-id="6bbf2-137">Hull</span><span class="sxs-lookup"><span data-stu-id="6bbf2-137">Hull</span></span> | <span data-ttu-id="6bbf2-138">Dominio</span><span class="sxs-lookup"><span data-stu-id="6bbf2-138">Domain</span></span> | <span data-ttu-id="6bbf2-139">Geometria</span><span class="sxs-lookup"><span data-stu-id="6bbf2-139">Geometry</span></span> | <span data-ttu-id="6bbf2-140">Pixel</span><span class="sxs-lookup"><span data-stu-id="6bbf2-140">Pixel</span></span> | <span data-ttu-id="6bbf2-141">Calcolo</span><span class="sxs-lookup"><span data-stu-id="6bbf2-141">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="6bbf2-142">x</span><span class="sxs-lookup"><span data-stu-id="6bbf2-142">x</span></span>      |  <span data-ttu-id="6bbf2-143">x</span><span class="sxs-lookup"><span data-stu-id="6bbf2-143">x</span></span>   |  <span data-ttu-id="6bbf2-144">x</span><span class="sxs-lookup"><span data-stu-id="6bbf2-144">x</span></span>     |  <span data-ttu-id="6bbf2-145">x</span><span class="sxs-lookup"><span data-stu-id="6bbf2-145">x</span></span>       | <span data-ttu-id="6bbf2-146">x</span><span class="sxs-lookup"><span data-stu-id="6bbf2-146">x</span></span>     | <span data-ttu-id="6bbf2-147">x</span><span class="sxs-lookup"><span data-stu-id="6bbf2-147">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="6bbf2-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6bbf2-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bbf2-149">Funzioni intrinseche</span><span class="sxs-lookup"><span data-stu-id="6bbf2-149">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="6bbf2-150">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="6bbf2-150">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




