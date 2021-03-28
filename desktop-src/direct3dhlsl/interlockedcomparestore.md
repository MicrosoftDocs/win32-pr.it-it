---
title: Funzione InterlockedCompareStore (riferimento HLSL)
description: Confronta in modo atomico la destinazione con il valore di confronto. Se sono identici, la destinazione viene sovrascritta con il valore di input.
ms.assetid: eaf7e669-5240-40c9-9840-f4e7916e51b4
keywords:
- Funzione InterlockedCompareStore HLSL
topic_type:
- apiref
api_name:
- InterlockedCompareStore
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: df3ffb51bbe8fe8150d19a390e62640e64ded5c9
ms.sourcegitcommit: 12e9b14501d51641b690ee0cf764e2b91eb9a140
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/06/2020
ms.locfileid: "104398469"
---
# <a name="interlockedcomparestore-function-hlsl-reference"></a><span data-ttu-id="a738d-105">Funzione InterlockedCompareStore (riferimento HLSL)</span><span class="sxs-lookup"><span data-stu-id="a738d-105">InterlockedCompareStore function (HLSL reference)</span></span>

<span data-ttu-id="a738d-106">Confronta in modo atomico la destinazione con il valore di confronto.</span><span class="sxs-lookup"><span data-stu-id="a738d-106">Atomically compares the destination to the comparison value.</span></span> <span data-ttu-id="a738d-107">Se sono identici, la destinazione viene sovrascritta con il valore di input.</span><span class="sxs-lookup"><span data-stu-id="a738d-107">If they are identical, the destination is overwritten with the input value.</span></span>

## <a name="syntax"></a><span data-ttu-id="a738d-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a738d-108">Syntax</span></span>

``` syntax
void InterlockedCompareStore(
  in R dest,
  in T compare_value,
  in T value
);
```

## <a name="parameters"></a><span data-ttu-id="a738d-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="a738d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a738d-110">*dest* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a738d-110">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a738d-111">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="a738d-111">Type: **R**</span></span>

<span data-ttu-id="a738d-112">Indirizzo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="a738d-112">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="a738d-113">*Confronta \_ valore* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a738d-113">*compare\_value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a738d-114">Tipo: **T**</span><span class="sxs-lookup"><span data-stu-id="a738d-114">Type: **T**</span></span>

<span data-ttu-id="a738d-115">Valore di confronto.</span><span class="sxs-lookup"><span data-stu-id="a738d-115">The comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="a738d-116">*valore* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="a738d-116">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a738d-117">Tipo: **T**</span><span class="sxs-lookup"><span data-stu-id="a738d-117">Type: **T**</span></span>

<span data-ttu-id="a738d-118">Valore di input.</span><span class="sxs-lookup"><span data-stu-id="a738d-118">The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a738d-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a738d-119">Return value</span></span>

<span data-ttu-id="a738d-120">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="a738d-120">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a738d-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="a738d-121">Remarks</span></span>

<span data-ttu-id="a738d-122">Confronta in modo atomico il valore a cui fa riferimento *dest* con *\_ valore di confronto* e archivia il *valore* nella posizione a cui fa riferimento *dest* se i valori corrispondono.</span><span class="sxs-lookup"><span data-stu-id="a738d-122">Atomically compares the value referenced by *dest* with *compare\_value* and stores *value* in the location referenced by *dest* if the values match.</span></span> <span data-ttu-id="a738d-123">Questa operazione può essere eseguita solo su risorse tipizzate **int** o **uint** e variabili di memoria condivisa.</span><span class="sxs-lookup"><span data-stu-id="a738d-123">This operation can only be performed on **int** or **uint** typed resources and shared memory variables.</span></span> <span data-ttu-id="a738d-124">Esistono due possibili usi per questa funzione.</span><span class="sxs-lookup"><span data-stu-id="a738d-124">There are two possible uses for this function.</span></span> <span data-ttu-id="a738d-125">Il primo è quando R è un tipo di variabile di memoria condivisa.</span><span class="sxs-lookup"><span data-stu-id="a738d-125">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="a738d-126">In questo caso, la funzione esegue l'operazione sul Registro di memoria condiviso a cui fa riferimento *dest*.</span><span class="sxs-lookup"><span data-stu-id="a738d-126">In this case, the function performs the operation on the shared memory register referenced by *dest*.</span></span> <span data-ttu-id="a738d-127">Il secondo scenario è quando R è un tipo di variabile di risorsa.</span><span class="sxs-lookup"><span data-stu-id="a738d-127">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="a738d-128">In questo scenario, la funzione esegue l'operazione sul percorso della risorsa a cui fa riferimento *dest*.</span><span class="sxs-lookup"><span data-stu-id="a738d-128">In this scenario, the function performs the operation on the resource location referenced by *dest*.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="a738d-129">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="a738d-129">Minimum Shader Model</span></span>

<span data-ttu-id="a738d-130">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="a738d-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="a738d-131">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="a738d-131">Shader Model</span></span>                                                                | <span data-ttu-id="a738d-132">Supportato</span><span class="sxs-lookup"><span data-stu-id="a738d-132">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="a738d-133">[Shader Model 5](d3d11-graphics-reference-sm5.md) e versioni successive shader Models</span><span class="sxs-lookup"><span data-stu-id="a738d-133">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="a738d-134">sì</span><span class="sxs-lookup"><span data-stu-id="a738d-134">yes</span></span>       |



 

<span data-ttu-id="a738d-135">Questa funzione è supportata nei tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="a738d-135">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="a738d-136">Vertice</span><span class="sxs-lookup"><span data-stu-id="a738d-136">Vertex</span></span> | <span data-ttu-id="a738d-137">Hull</span><span class="sxs-lookup"><span data-stu-id="a738d-137">Hull</span></span> | <span data-ttu-id="a738d-138">Dominio</span><span class="sxs-lookup"><span data-stu-id="a738d-138">Domain</span></span> | <span data-ttu-id="a738d-139">Geometria</span><span class="sxs-lookup"><span data-stu-id="a738d-139">Geometry</span></span> | <span data-ttu-id="a738d-140">Pixel</span><span class="sxs-lookup"><span data-stu-id="a738d-140">Pixel</span></span> | <span data-ttu-id="a738d-141">Calcolo</span><span class="sxs-lookup"><span data-stu-id="a738d-141">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|  <span data-ttu-id="a738d-142">x</span><span class="sxs-lookup"><span data-stu-id="a738d-142">x</span></span>     | <span data-ttu-id="a738d-143">x</span><span class="sxs-lookup"><span data-stu-id="a738d-143">x</span></span>    |  <span data-ttu-id="a738d-144">x</span><span class="sxs-lookup"><span data-stu-id="a738d-144">x</span></span>     |  <span data-ttu-id="a738d-145">x</span><span class="sxs-lookup"><span data-stu-id="a738d-145">x</span></span>       | <span data-ttu-id="a738d-146">x</span><span class="sxs-lookup"><span data-stu-id="a738d-146">x</span></span>     | <span data-ttu-id="a738d-147">x</span><span class="sxs-lookup"><span data-stu-id="a738d-147">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="a738d-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a738d-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a738d-149">Funzioni intrinseche</span><span class="sxs-lookup"><span data-stu-id="a738d-149">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="a738d-150">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="a738d-150">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




