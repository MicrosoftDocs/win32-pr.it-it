---
title: 'Funzione RWByteAddressBuffer:: InterlockedMin'
description: Trova il valore minimo, atomicamente.
ms.assetid: bf650b2e-9c6c-4458-9565-1e9ec76a1472
keywords:
- Funzione InterlockedMin HLSL
topic_type:
- apiref
api_name:
- InterlockedMin
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b818a1fa0897d103e7d609a676212c6db428935f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046766"
---
# <a name="interlockedmin-function"></a><span data-ttu-id="d9597-104">InterlockedMin (funzione)</span><span class="sxs-lookup"><span data-stu-id="d9597-104">InterlockedMin function</span></span>

<span data-ttu-id="d9597-105">Trova il valore minimo, atomicamente.</span><span class="sxs-lookup"><span data-stu-id="d9597-105">Finds the minimum value, atomically.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9597-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d9597-106">Syntax</span></span>

``` syntax
void InterlockedMin(
  in  UINT dest,
  in  UINT value,
  out UINT original_value
);
```

## <a name="parameters"></a><span data-ttu-id="d9597-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="d9597-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9597-108">*dest* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d9597-108">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9597-109">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d9597-109">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d9597-110">Indirizzo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="d9597-110">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="d9597-111">*valore* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="d9597-111">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9597-112">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d9597-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d9597-113">Valore di input.</span><span class="sxs-lookup"><span data-stu-id="d9597-113">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="d9597-114">*\_ valore originale* in \[ uscita\]</span><span class="sxs-lookup"><span data-stu-id="d9597-114">*original\_value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d9597-115">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d9597-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d9597-116">Valore originale.</span><span class="sxs-lookup"><span data-stu-id="d9597-116">The original value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9597-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d9597-117">Return value</span></span>

<span data-ttu-id="d9597-118">Nothing</span><span class="sxs-lookup"><span data-stu-id="d9597-118">Nothing</span></span>

## <a name="remarks"></a><span data-ttu-id="d9597-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="d9597-119">Remarks</span></span>

<span data-ttu-id="d9597-120">Questa operazione può essere eseguita solo su risorse tipizzate int e uint e variabili di memoria condivisa.</span><span class="sxs-lookup"><span data-stu-id="d9597-120">This operation can only be performed on int and uint typed resources and shared memory variables.</span></span> <span data-ttu-id="d9597-121">Per questa funzione sono disponibili tre possibili utilizzi.</span><span class="sxs-lookup"><span data-stu-id="d9597-121">There are three possible uses for this function.</span></span> <span data-ttu-id="d9597-122">Il primo è quando R è un tipo di variabile di memoria condivisa.</span><span class="sxs-lookup"><span data-stu-id="d9597-122">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="d9597-123">In questo caso, la funzione esegue un valore minimo atomico del valore al registro di memoria condiviso a cui fa riferimento dest.</span><span class="sxs-lookup"><span data-stu-id="d9597-123">In this case, the function performs an atomic minimum of the value to the shared memory register referenced by dest.</span></span> <span data-ttu-id="d9597-124">Il secondo scenario è quando R è un tipo di variabile di risorsa.</span><span class="sxs-lookup"><span data-stu-id="d9597-124">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="d9597-125">In questo scenario, la funzione esegue un valore minimo atomico del valore per la posizione della risorsa a cui fa riferimento dest.</span><span class="sxs-lookup"><span data-stu-id="d9597-125">In this scenario, the function performs an atomic minimum of the value to the resource location referenced by dest.</span></span> <span data-ttu-id="d9597-126">Infine, il terzo scenario è quando R è un tipo di variabile locale.</span><span class="sxs-lookup"><span data-stu-id="d9597-126">Finally, the third scenario is when R is a local variable type.</span></span> <span data-ttu-id="d9597-127">In questo scenario, la funzione riduce a un valore minimo del valore di dest e value, archiviato in dest.</span><span class="sxs-lookup"><span data-stu-id="d9597-127">In this scenario, the function reduces to a minimum of the value of dest and value, stored in dest.</span></span> <span data-ttu-id="d9597-128">La funzione in overload ha una variabile di output aggiuntiva che verrà impostata sul valore originale di dest.</span><span class="sxs-lookup"><span data-stu-id="d9597-128">The overloaded function has an additional output variable which will be set to the original value of dest.</span></span> <span data-ttu-id="d9597-129">Questa operazione di overload è disponibile solo quando R è leggibile e scrivibile.</span><span class="sxs-lookup"><span data-stu-id="d9597-129">This overloaded operation is only available when R is readable and writable.</span></span>

<span data-ttu-id="d9597-130">Questa funzione è supportata nei tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="d9597-130">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="d9597-131">VS</span><span class="sxs-lookup"><span data-stu-id="d9597-131">VS</span></span>  | <span data-ttu-id="d9597-132">HS</span><span class="sxs-lookup"><span data-stu-id="d9597-132">HS</span></span>  | <span data-ttu-id="d9597-133">DS</span><span class="sxs-lookup"><span data-stu-id="d9597-133">DS</span></span>  | <span data-ttu-id="d9597-134">GS</span><span class="sxs-lookup"><span data-stu-id="d9597-134">GS</span></span>  | <span data-ttu-id="d9597-135">PS</span><span class="sxs-lookup"><span data-stu-id="d9597-135">PS</span></span>  | <span data-ttu-id="d9597-136">CS</span><span class="sxs-lookup"><span data-stu-id="d9597-136">CS</span></span>  |
|-----|-----|-----|-----|-----|-----|
| <span data-ttu-id="d9597-137">x</span><span class="sxs-lookup"><span data-stu-id="d9597-137">x</span></span>   |  <span data-ttu-id="d9597-138">x</span><span class="sxs-lookup"><span data-stu-id="d9597-138">x</span></span>  | <span data-ttu-id="d9597-139">x</span><span class="sxs-lookup"><span data-stu-id="d9597-139">x</span></span>   | <span data-ttu-id="d9597-140">x</span><span class="sxs-lookup"><span data-stu-id="d9597-140">x</span></span>   | <span data-ttu-id="d9597-141">x</span><span class="sxs-lookup"><span data-stu-id="d9597-141">x</span></span>   | <span data-ttu-id="d9597-142">x</span><span class="sxs-lookup"><span data-stu-id="d9597-142">x</span></span>   |



 

## <a name="see-also"></a><span data-ttu-id="d9597-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d9597-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9597-144">RWByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="d9597-144">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="d9597-145">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="d9597-145">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 