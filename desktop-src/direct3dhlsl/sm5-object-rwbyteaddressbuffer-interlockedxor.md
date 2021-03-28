---
title: 'Funzione RWByteAddressBuffer:: InterlockedXor'
description: Esegue un XOR atomico sul valore.
ms.assetid: 692f8b5e-a81e-4700-8a8d-3594aba85671
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
ms.openlocfilehash: 920ae912c599b66a03a25d7bc8ecc9b199036b26
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963104"
---
# <a name="interlockedxor-function"></a><span data-ttu-id="291a0-104">InterlockedXor (funzione)</span><span class="sxs-lookup"><span data-stu-id="291a0-104">InterlockedXor function</span></span>

<span data-ttu-id="291a0-105">Esegue un **Xor** atomico sul valore.</span><span class="sxs-lookup"><span data-stu-id="291a0-105">Performs an atomic **XOR** on the value.</span></span>

## <a name="syntax"></a><span data-ttu-id="291a0-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="291a0-106">Syntax</span></span>

``` syntax
void InterlockedXor(
  in  UINT dest,
  in  UINT value,
  out UINT original_value
);
```

## <a name="parameters"></a><span data-ttu-id="291a0-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="291a0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="291a0-108">*dest* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="291a0-108">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="291a0-109">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="291a0-109">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="291a0-110">Indirizzo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="291a0-110">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="291a0-111">*valore* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="291a0-111">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="291a0-112">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="291a0-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="291a0-113">Valore di input.</span><span class="sxs-lookup"><span data-stu-id="291a0-113">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="291a0-114">*\_ valore originale* in \[ uscita\]</span><span class="sxs-lookup"><span data-stu-id="291a0-114">*original\_value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="291a0-115">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="291a0-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="291a0-116">Valore originale.</span><span class="sxs-lookup"><span data-stu-id="291a0-116">The original value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="291a0-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="291a0-117">Return value</span></span>

<span data-ttu-id="291a0-118">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="291a0-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="291a0-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="291a0-119">Remarks</span></span>

<span data-ttu-id="291a0-120">Questa operazione può essere eseguita solo su risorse tipizzate **int** o **uint** e variabili di memoria condivisa.</span><span class="sxs-lookup"><span data-stu-id="291a0-120">This operation can be performed only on **INT** or **UINT** typed resources and shared memory variables.</span></span> <span data-ttu-id="291a0-121">Per questa funzione sono disponibili tre possibili utilizzi.</span><span class="sxs-lookup"><span data-stu-id="291a0-121">There are three possible uses for this function.</span></span> <span data-ttu-id="291a0-122">Il primo è quando R è un tipo di variabile di memoria condivisa.</span><span class="sxs-lookup"><span data-stu-id="291a0-122">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="291a0-123">In questo caso, la funzione esegue un **Xor** atomico con il valore del registro di memoria condiviso a cui fa riferimento *dest*.</span><span class="sxs-lookup"><span data-stu-id="291a0-123">In this case, the function performs an atomic **XOR** with the value of the shared memory register referenced by *dest*.</span></span> <span data-ttu-id="291a0-124">Il secondo scenario è quando R è un tipo di variabile di risorsa.</span><span class="sxs-lookup"><span data-stu-id="291a0-124">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="291a0-125">In questo scenario, la funzione esegue un **Xor** atomico con il valore della posizione della risorsa a cui fa riferimento *dest*.</span><span class="sxs-lookup"><span data-stu-id="291a0-125">In this scenario, the function performs an atomic **XOR** with the value of the resource location referenced by *dest*.</span></span> <span data-ttu-id="291a0-126">Infine, il terzo scenario è quando R è un tipo di variabile locale.</span><span class="sxs-lookup"><span data-stu-id="291a0-126">Finally, the third scenario is when R is a local variable type.</span></span> <span data-ttu-id="291a0-127">In questo scenario, la funzione riduce a uno **Xor** dei valori di *dest* e *value*.</span><span class="sxs-lookup"><span data-stu-id="291a0-127">In this scenario, the function reduces to an **XOR** of the values of *dest* and *value*.</span></span> <span data-ttu-id="291a0-128">Il risultato dell'operazione sostituisce il valore in *dest*.</span><span class="sxs-lookup"><span data-stu-id="291a0-128">The result of the operation replaces the value in *dest*.</span></span> <span data-ttu-id="291a0-129">La funzione in overload ha una variabile di output aggiuntiva che verrà impostata sul valore originale di *dest*.</span><span class="sxs-lookup"><span data-stu-id="291a0-129">The overloaded function has an additional output variable which will be set to the original value of *dest*.</span></span> <span data-ttu-id="291a0-130">Questa operazione di overload è disponibile solo se R è leggibile e scrivibile.</span><span class="sxs-lookup"><span data-stu-id="291a0-130">This overloaded operation is available only when R is readable and writable.</span></span>

<span data-ttu-id="291a0-131">Questa funzione è supportata nei tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="291a0-131">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="291a0-132">VS</span><span class="sxs-lookup"><span data-stu-id="291a0-132">VS</span></span>  | <span data-ttu-id="291a0-133">HS</span><span class="sxs-lookup"><span data-stu-id="291a0-133">HS</span></span>  | <span data-ttu-id="291a0-134">DS</span><span class="sxs-lookup"><span data-stu-id="291a0-134">DS</span></span>  | <span data-ttu-id="291a0-135">GS</span><span class="sxs-lookup"><span data-stu-id="291a0-135">GS</span></span>  | <span data-ttu-id="291a0-136">PS</span><span class="sxs-lookup"><span data-stu-id="291a0-136">PS</span></span>  | <span data-ttu-id="291a0-137">CS</span><span class="sxs-lookup"><span data-stu-id="291a0-137">CS</span></span>  |
|-----|-----|-----|-----|-----|-----|
| <span data-ttu-id="291a0-138">x</span><span class="sxs-lookup"><span data-stu-id="291a0-138">x</span></span>   |  <span data-ttu-id="291a0-139">x</span><span class="sxs-lookup"><span data-stu-id="291a0-139">x</span></span>  | <span data-ttu-id="291a0-140">x</span><span class="sxs-lookup"><span data-stu-id="291a0-140">x</span></span>   | <span data-ttu-id="291a0-141">x</span><span class="sxs-lookup"><span data-stu-id="291a0-141">x</span></span>   | <span data-ttu-id="291a0-142">x</span><span class="sxs-lookup"><span data-stu-id="291a0-142">x</span></span>   | <span data-ttu-id="291a0-143">x</span><span class="sxs-lookup"><span data-stu-id="291a0-143">x</span></span>   |



 

## <a name="see-also"></a><span data-ttu-id="291a0-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="291a0-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="291a0-145">RWByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="291a0-145">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="291a0-146">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="291a0-146">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 