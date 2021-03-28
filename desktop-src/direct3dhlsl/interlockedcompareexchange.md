---
title: Funzione InterlockedCompareExchange (riferimento HLSL)
description: Confronta in modo atomico la destinazione con il valore di confronto. Se sono identici, la destinazione viene sovrascritta con il valore di input. Il valore originale è impostato sul valore originale della destinazione.
ms.assetid: 85d1ba58-8e79-41cd-abd6-7ffff59839c7
keywords:
- Funzione InterlockedCompareExchange HLSL
topic_type:
- apiref
api_name:
- InterlockedCompareExchange
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 74bc189996752d754599bf4547e8baa4d9fb74cc
ms.sourcegitcommit: 12e9b14501d51641b690ee0cf764e2b91eb9a140
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/06/2020
ms.locfileid: "104993317"
---
# <a name="interlockedcompareexchange-function-hlsl-reference"></a><span data-ttu-id="fa6af-106">Funzione InterlockedCompareExchange (riferimento HLSL)</span><span class="sxs-lookup"><span data-stu-id="fa6af-106">InterlockedCompareExchange function (HLSL reference)</span></span>

<span data-ttu-id="fa6af-107">Confronta in modo atomico la destinazione con il valore di confronto.</span><span class="sxs-lookup"><span data-stu-id="fa6af-107">Atomically compares the destination with the comparison value.</span></span> <span data-ttu-id="fa6af-108">Se sono identici, la destinazione viene sovrascritta con il valore di input.</span><span class="sxs-lookup"><span data-stu-id="fa6af-108">If they are identical, the destination is overwritten with the input value.</span></span> <span data-ttu-id="fa6af-109">Il valore originale è impostato sul valore originale della destinazione.</span><span class="sxs-lookup"><span data-stu-id="fa6af-109">The original value is set to the destination's original value.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa6af-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fa6af-110">Syntax</span></span>

``` syntax
void InterlockedCompareExchange(
  in  R dest,
  in  T compare_value,
  in  T value,
  out T original_value
);
```

## <a name="parameters"></a><span data-ttu-id="fa6af-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="fa6af-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa6af-112">*dest* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fa6af-112">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa6af-113">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="fa6af-113">Type: **R**</span></span>

<span data-ttu-id="fa6af-114">Indirizzo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="fa6af-114">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="fa6af-115">*Confronta \_ valore* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fa6af-115">*compare\_value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa6af-116">Tipo: **T**</span><span class="sxs-lookup"><span data-stu-id="fa6af-116">Type: **T**</span></span>

<span data-ttu-id="fa6af-117">Valore di confronto.</span><span class="sxs-lookup"><span data-stu-id="fa6af-117">The comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="fa6af-118">*valore* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="fa6af-118">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa6af-119">Tipo: **T**</span><span class="sxs-lookup"><span data-stu-id="fa6af-119">Type: **T**</span></span>

<span data-ttu-id="fa6af-120">Valore di input.</span><span class="sxs-lookup"><span data-stu-id="fa6af-120">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="fa6af-121">*\_ valore originale* in \[ uscita\]</span><span class="sxs-lookup"><span data-stu-id="fa6af-121">*original\_value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fa6af-122">Tipo: **T**</span><span class="sxs-lookup"><span data-stu-id="fa6af-122">Type: **T**</span></span>

<span data-ttu-id="fa6af-123">Valore originale.</span><span class="sxs-lookup"><span data-stu-id="fa6af-123">The original value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa6af-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fa6af-124">Return value</span></span>

<span data-ttu-id="fa6af-125">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="fa6af-125">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa6af-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="fa6af-126">Remarks</span></span>

<span data-ttu-id="fa6af-127">Confronta in modo atomico il valore a cui fa *riferimento dest* con *\_ valore di confronto*, archivia il *valore* nella posizione a cui fa riferimento *dest* se i valori corrispondono, restituisce il valore originale di *dest* nel *\_ valore originale*.</span><span class="sxs-lookup"><span data-stu-id="fa6af-127">Atomically compares the value referenced by *dest* with *compare\_value*, stores *value* in the location referenced by *dest* if the values match, returns the original value of *dest* in *original\_value*.</span></span> <span data-ttu-id="fa6af-128">Questa operazione può essere eseguita solo su risorse tipizzate **int** o **uint** e variabili di memoria condivisa.</span><span class="sxs-lookup"><span data-stu-id="fa6af-128">This operation can only be performed on **int** or **uint** typed resources and shared memory variables.</span></span> <span data-ttu-id="fa6af-129">Esistono due possibili usi per questa funzione.</span><span class="sxs-lookup"><span data-stu-id="fa6af-129">There are two possible uses for this function.</span></span> <span data-ttu-id="fa6af-130">Il primo è quando R è un tipo di variabile di memoria condivisa.</span><span class="sxs-lookup"><span data-stu-id="fa6af-130">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="fa6af-131">In questo caso, la funzione esegue l'operazione sul Registro di memoria condiviso a cui fa riferimento *dest*.</span><span class="sxs-lookup"><span data-stu-id="fa6af-131">In this case, the function performs the operation on the shared memory register referenced by *dest*.</span></span> <span data-ttu-id="fa6af-132">Il secondo scenario è quando R è un tipo di variabile di risorsa.</span><span class="sxs-lookup"><span data-stu-id="fa6af-132">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="fa6af-133">In questo scenario, la funzione esegue l'operazione sul percorso della risorsa a cui fa riferimento *dest*.</span><span class="sxs-lookup"><span data-stu-id="fa6af-133">In this scenario, the function performs the operation on the resource location referenced by *dest*.</span></span> <span data-ttu-id="fa6af-134">Questa operazione è disponibile solo se R è leggibile e scrivibile.</span><span class="sxs-lookup"><span data-stu-id="fa6af-134">This operation is only available when R is readable and writable.</span></span>

> [!Note]  
> <span data-ttu-id="fa6af-135">Se si chiama **InterlockedCompareExchange** in un ciclo [**for**](dx-graphics-hlsl-for.md) o [**while**](dx-graphics-hlsl-while.md) compute shader, per la corretta compilazione è necessario usare l'attributo **\[ allow \_ \_ Condition \] UAV** in quel ciclo.</span><span class="sxs-lookup"><span data-stu-id="fa6af-135">If you call **InterlockedCompareExchange** in a [**for**](dx-graphics-hlsl-for.md) or [**while**](dx-graphics-hlsl-while.md) compute shader loop, to properly compile, you must use the **\[allow\_uav\_condition\]** attribute on that loop.</span></span>

 

### <a name="minimum-shader-model"></a><span data-ttu-id="fa6af-136">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="fa6af-136">Minimum Shader Model</span></span>

<span data-ttu-id="fa6af-137">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="fa6af-137">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="fa6af-138">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="fa6af-138">Shader Model</span></span>                                                                | <span data-ttu-id="fa6af-139">Supportato</span><span class="sxs-lookup"><span data-stu-id="fa6af-139">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="fa6af-140">[Shader Model 5](d3d11-graphics-reference-sm5.md) e versioni successive shader Models</span><span class="sxs-lookup"><span data-stu-id="fa6af-140">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="fa6af-141">sì</span><span class="sxs-lookup"><span data-stu-id="fa6af-141">yes</span></span>       |



 

<span data-ttu-id="fa6af-142">Questa funzione è supportata nei tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="fa6af-142">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="fa6af-143">Vertice</span><span class="sxs-lookup"><span data-stu-id="fa6af-143">Vertex</span></span> | <span data-ttu-id="fa6af-144">Hull</span><span class="sxs-lookup"><span data-stu-id="fa6af-144">Hull</span></span> | <span data-ttu-id="fa6af-145">Dominio</span><span class="sxs-lookup"><span data-stu-id="fa6af-145">Domain</span></span> | <span data-ttu-id="fa6af-146">Geometria</span><span class="sxs-lookup"><span data-stu-id="fa6af-146">Geometry</span></span> | <span data-ttu-id="fa6af-147">Pixel</span><span class="sxs-lookup"><span data-stu-id="fa6af-147">Pixel</span></span> | <span data-ttu-id="fa6af-148">Calcolo</span><span class="sxs-lookup"><span data-stu-id="fa6af-148">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="fa6af-149">x</span><span class="sxs-lookup"><span data-stu-id="fa6af-149">x</span></span>      |  <span data-ttu-id="fa6af-150">x</span><span class="sxs-lookup"><span data-stu-id="fa6af-150">x</span></span>   |  <span data-ttu-id="fa6af-151">x</span><span class="sxs-lookup"><span data-stu-id="fa6af-151">x</span></span>     |  <span data-ttu-id="fa6af-152">x</span><span class="sxs-lookup"><span data-stu-id="fa6af-152">x</span></span>       | <span data-ttu-id="fa6af-153">x</span><span class="sxs-lookup"><span data-stu-id="fa6af-153">x</span></span>     | <span data-ttu-id="fa6af-154">x</span><span class="sxs-lookup"><span data-stu-id="fa6af-154">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="fa6af-155">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fa6af-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa6af-156">Funzioni intrinseche</span><span class="sxs-lookup"><span data-stu-id="fa6af-156">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="fa6af-157">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="fa6af-157">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




