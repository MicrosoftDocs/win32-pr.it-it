---
title: 'Funzione RWByteAddressBuffer:: InterlockedMax'
description: Trova il valore massimo, atomicamente.
ms.assetid: 2e78065f-c1ee-47ac-a826-c8a46c730c4a
keywords:
- Funzione InterlockedMax HLSL
topic_type:
- apiref
api_name:
- InterlockedMax
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e77f925a0950d3731af58c2c6835867640760371
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993464"
---
# <a name="interlockedmax-function"></a><span data-ttu-id="200e8-104">InterlockedMax (funzione)</span><span class="sxs-lookup"><span data-stu-id="200e8-104">InterlockedMax function</span></span>

<span data-ttu-id="200e8-105">Trova il valore massimo, atomicamente.</span><span class="sxs-lookup"><span data-stu-id="200e8-105">Finds the maximum value, atomically.</span></span>

## <a name="syntax"></a><span data-ttu-id="200e8-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="200e8-106">Syntax</span></span>

``` syntax
void InterlockedMax(
  in  UINT dest,
  in  UINT value,
  out UINT original_value
);
```

## <a name="parameters"></a><span data-ttu-id="200e8-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="200e8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="200e8-108">*dest* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="200e8-108">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="200e8-109">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="200e8-109">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="200e8-110">Indirizzo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="200e8-110">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="200e8-111">*valore* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="200e8-111">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="200e8-112">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="200e8-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="200e8-113">Valore di input.</span><span class="sxs-lookup"><span data-stu-id="200e8-113">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="200e8-114">*\_ valore originale* in \[ uscita\]</span><span class="sxs-lookup"><span data-stu-id="200e8-114">*original\_value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="200e8-115">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="200e8-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="200e8-116">Valore originale.</span><span class="sxs-lookup"><span data-stu-id="200e8-116">The original value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="200e8-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="200e8-117">Return value</span></span>

<span data-ttu-id="200e8-118">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="200e8-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="200e8-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="200e8-119">Remarks</span></span>

<span data-ttu-id="200e8-120">Questa operazione può essere eseguita solo su risorse tipizzate int e uint e variabili di memoria condivisa.</span><span class="sxs-lookup"><span data-stu-id="200e8-120">This operation can only be performed on int and uint typed resources and shared memory variables.</span></span> <span data-ttu-id="200e8-121">Per questa funzione sono disponibili tre possibili utilizzi.</span><span class="sxs-lookup"><span data-stu-id="200e8-121">There are three possible uses for this function.</span></span> <span data-ttu-id="200e8-122">Il primo è quando R è un tipo di variabile di memoria condivisa.</span><span class="sxs-lookup"><span data-stu-id="200e8-122">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="200e8-123">In questo caso, la funzione esegue un valore massimo atomico del valore al registro di memoria condiviso a cui fa riferimento dest.</span><span class="sxs-lookup"><span data-stu-id="200e8-123">In this case, the function performs an atomic maximum of the value to the shared memory register referenced by dest.</span></span> <span data-ttu-id="200e8-124">Il secondo scenario è quando R è un tipo di variabile di risorsa.</span><span class="sxs-lookup"><span data-stu-id="200e8-124">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="200e8-125">In questo scenario, la funzione esegue un valore massimo atomico del valore nel percorso della risorsa a cui fa riferimento dest.</span><span class="sxs-lookup"><span data-stu-id="200e8-125">In this scenario, the function performs an atomic maximum of the value to the resource location referenced by dest.</span></span> <span data-ttu-id="200e8-126">Infine, il terzo scenario è quando R è un tipo di variabile locale.</span><span class="sxs-lookup"><span data-stu-id="200e8-126">Finally, the third scenario is when R is a local variable type.</span></span> <span data-ttu-id="200e8-127">In questo scenario, la funzione riduce a un massimo del valore di dest e value, archiviati in dest.</span><span class="sxs-lookup"><span data-stu-id="200e8-127">In this scenario, the function reduces to a maximum of the value of dest and value, stored in dest.</span></span> <span data-ttu-id="200e8-128">La funzione in overload ha una variabile di output aggiuntiva che verrà impostata sul valore originale di dest.</span><span class="sxs-lookup"><span data-stu-id="200e8-128">The overloaded function has an additional output variable which will be set to the original value of dest.</span></span> <span data-ttu-id="200e8-129">Questa operazione di overload è disponibile solo quando R è leggibile e scrivibile.</span><span class="sxs-lookup"><span data-stu-id="200e8-129">This overloaded operation is only available when R is readable and writable.</span></span>

<span data-ttu-id="200e8-130">Questa funzione è supportata nei tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="200e8-130">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="200e8-131">VS</span><span class="sxs-lookup"><span data-stu-id="200e8-131">VS</span></span>  | <span data-ttu-id="200e8-132">HS</span><span class="sxs-lookup"><span data-stu-id="200e8-132">HS</span></span>  | <span data-ttu-id="200e8-133">DS</span><span class="sxs-lookup"><span data-stu-id="200e8-133">DS</span></span>  | <span data-ttu-id="200e8-134">GS</span><span class="sxs-lookup"><span data-stu-id="200e8-134">GS</span></span>  | <span data-ttu-id="200e8-135">PS</span><span class="sxs-lookup"><span data-stu-id="200e8-135">PS</span></span>  | <span data-ttu-id="200e8-136">CS</span><span class="sxs-lookup"><span data-stu-id="200e8-136">CS</span></span>  |
|-----|-----|-----|-----|-----|-----|
| <span data-ttu-id="200e8-137">x</span><span class="sxs-lookup"><span data-stu-id="200e8-137">x</span></span>   | <span data-ttu-id="200e8-138">x</span><span class="sxs-lookup"><span data-stu-id="200e8-138">x</span></span>   | <span data-ttu-id="200e8-139">x</span><span class="sxs-lookup"><span data-stu-id="200e8-139">x</span></span>   | <span data-ttu-id="200e8-140">x</span><span class="sxs-lookup"><span data-stu-id="200e8-140">x</span></span>   | <span data-ttu-id="200e8-141">x</span><span class="sxs-lookup"><span data-stu-id="200e8-141">x</span></span>   | <span data-ttu-id="200e8-142">x</span><span class="sxs-lookup"><span data-stu-id="200e8-142">x</span></span>   |



 

## <a name="see-also"></a><span data-ttu-id="200e8-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="200e8-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="200e8-144">RWByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="200e8-144">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="200e8-145">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="200e8-145">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 