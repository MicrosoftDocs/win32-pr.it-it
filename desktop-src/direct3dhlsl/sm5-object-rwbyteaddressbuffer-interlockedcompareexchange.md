---
title: 'Funzione RWByteAddressBuffer:: InterlockedCompareExchange'
description: Confronta l'input con il valore di confronto e scambia il risultato in modo atomico.
ms.assetid: 9d6e8d95-5157-49a7-8a79-f3ca6ba87ebb
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
ms.openlocfilehash: 18c7e5d58fe926d09e7ec48ee12a2336627d5db2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729143"
---
# <a name="interlockedcompareexchange-function"></a><span data-ttu-id="fc903-104">InterlockedCompareExchange (funzione)</span><span class="sxs-lookup"><span data-stu-id="fc903-104">InterlockedCompareExchange function</span></span>

<span data-ttu-id="fc903-105">Confronta l'input con il valore di confronto e scambia il risultato in modo atomico.</span><span class="sxs-lookup"><span data-stu-id="fc903-105">Compares the input to the comparison value and exchanges the result, atomically.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc903-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fc903-106">Syntax</span></span>

``` syntax
void InterlockedCompareExchange(
  in  UINT dest,
  in  UINT compare_value,
  in  UINT value,
  out UINT original_value
);
```

## <a name="parameters"></a><span data-ttu-id="fc903-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="fc903-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc903-108">*dest* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fc903-108">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc903-109">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="fc903-109">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="fc903-110">Indirizzo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="fc903-110">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="fc903-111">*Confronta \_ valore* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fc903-111">*compare\_value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc903-112">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="fc903-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="fc903-113">Valore di confronto.</span><span class="sxs-lookup"><span data-stu-id="fc903-113">The comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="fc903-114">*valore* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="fc903-114">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc903-115">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="fc903-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="fc903-116">Valore di input.</span><span class="sxs-lookup"><span data-stu-id="fc903-116">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="fc903-117">*\_ valore originale* in \[ uscita\]</span><span class="sxs-lookup"><span data-stu-id="fc903-117">*original\_value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fc903-118">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="fc903-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="fc903-119">Valore originale.</span><span class="sxs-lookup"><span data-stu-id="fc903-119">The original value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc903-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fc903-120">Return value</span></span>

<span data-ttu-id="fc903-121">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="fc903-121">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc903-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="fc903-122">Remarks</span></span>

<span data-ttu-id="fc903-123">Confronta in modo atomico il valore in *dest* per *confrontare \_ value*, archivia il valore in *dest* se i valori corrispondono, restituisce il valore originale di *dest* nel *\_ valore originale*.</span><span class="sxs-lookup"><span data-stu-id="fc903-123">Atomically compares the value in *dest* to *compare\_value*, stores value in *dest* if the values match, returns the original value of *dest* in *original\_value*.</span></span> <span data-ttu-id="fc903-124">Questa operazione può essere eseguita solo su risorse tipizzate **int** o *uint* e variabili di memoria condivisa.</span><span class="sxs-lookup"><span data-stu-id="fc903-124">This operation can only be performed on **int** or *uint* typed resources and shared memory variables.</span></span> <span data-ttu-id="fc903-125">Per questa funzione sono disponibili tre possibili utilizzi.</span><span class="sxs-lookup"><span data-stu-id="fc903-125">There are three possible uses for this function.</span></span> <span data-ttu-id="fc903-126">Il primo è quando R è un tipo di variabile di memoria condivisa.</span><span class="sxs-lookup"><span data-stu-id="fc903-126">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="fc903-127">In questo caso, la funzione esegue l'operazione sul Registro di memoria condiviso a cui fa riferimento *dest*.</span><span class="sxs-lookup"><span data-stu-id="fc903-127">In this case, the function performs the operation on the shared memory register referenced by *dest*.</span></span> <span data-ttu-id="fc903-128">Il secondo scenario è quando R è un tipo di variabile di risorsa.</span><span class="sxs-lookup"><span data-stu-id="fc903-128">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="fc903-129">In questo scenario, la funzione esegue l'operazione sul percorso della risorsa a cui fa riferimento *dest*.</span><span class="sxs-lookup"><span data-stu-id="fc903-129">In this scenario, the function performs the operation on the resource location referenced by *dest*.</span></span> <span data-ttu-id="fc903-130">Infine, il terzo scenario è quando R è un tipo di variabile locale.</span><span class="sxs-lookup"><span data-stu-id="fc903-130">Finally, the third scenario is when R is a local variable type.</span></span> <span data-ttu-id="fc903-131">In questo scenario, la funzione riduce l'operazione eseguita usando le operazioni locali.</span><span class="sxs-lookup"><span data-stu-id="fc903-131">In this scenario, the function reduces to the operation performed using local operations.</span></span> <span data-ttu-id="fc903-132">Questa operazione è disponibile solo se R è leggibile e scrivibile.</span><span class="sxs-lookup"><span data-stu-id="fc903-132">This operation is only available when R is readable and writable.</span></span>

> [!Note]  
> <span data-ttu-id="fc903-133">Se si chiama **InterlockedCompareExchange** in un ciclo [**for**](dx-graphics-hlsl-for.md) o [**while**](dx-graphics-hlsl-while.md) compute shader, per la corretta compilazione è necessario usare l'attributo **\[ allow \_ \_ Condition \] UAV** in quel ciclo.</span><span class="sxs-lookup"><span data-stu-id="fc903-133">If you call **InterlockedCompareExchange** in a [**for**](dx-graphics-hlsl-for.md) or [**while**](dx-graphics-hlsl-while.md) compute shader loop, to properly compile, you must use the **\[allow\_uav\_condition\]** attribute on that loop.</span></span>

 

<span data-ttu-id="fc903-134">Questa funzione è supportata nei tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="fc903-134">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="fc903-135">VS</span><span class="sxs-lookup"><span data-stu-id="fc903-135">VS</span></span>  | <span data-ttu-id="fc903-136">HS</span><span class="sxs-lookup"><span data-stu-id="fc903-136">HS</span></span>  | <span data-ttu-id="fc903-137">DS</span><span class="sxs-lookup"><span data-stu-id="fc903-137">DS</span></span>  | <span data-ttu-id="fc903-138">GS</span><span class="sxs-lookup"><span data-stu-id="fc903-138">GS</span></span>  | <span data-ttu-id="fc903-139">PS</span><span class="sxs-lookup"><span data-stu-id="fc903-139">PS</span></span>  | <span data-ttu-id="fc903-140">CS</span><span class="sxs-lookup"><span data-stu-id="fc903-140">CS</span></span>  |
|-----|-----|-----|-----|-----|-----|
| <span data-ttu-id="fc903-141">x</span><span class="sxs-lookup"><span data-stu-id="fc903-141">x</span></span>   | <span data-ttu-id="fc903-142">x</span><span class="sxs-lookup"><span data-stu-id="fc903-142">x</span></span>   | <span data-ttu-id="fc903-143">x</span><span class="sxs-lookup"><span data-stu-id="fc903-143">x</span></span>   | <span data-ttu-id="fc903-144">x</span><span class="sxs-lookup"><span data-stu-id="fc903-144">x</span></span>   | <span data-ttu-id="fc903-145">x</span><span class="sxs-lookup"><span data-stu-id="fc903-145">x</span></span>   | <span data-ttu-id="fc903-146">x</span><span class="sxs-lookup"><span data-stu-id="fc903-146">x</span></span>   |



 

## <a name="see-also"></a><span data-ttu-id="fc903-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fc903-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc903-148">RWByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="fc903-148">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="fc903-149">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="fc903-149">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 