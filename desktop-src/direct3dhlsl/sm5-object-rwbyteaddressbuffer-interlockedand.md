---
title: 'Funzione RWByteAddressBuffer:: InterlockedAnd'
description: Il valore, in modo atomico.
ms.assetid: c4024be0-3884-4af9-8075-76774c7c6178
keywords:
- Funzione InterlockedAnd HLSL
topic_type:
- apiref
api_name:
- InterlockedAnd
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a389da886b193815c7d4b2c1fe0a86db1f068fc7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399206"
---
# <a name="interlockedand-function"></a><span data-ttu-id="c9e43-104">InterlockedAnd (funzione)</span><span class="sxs-lookup"><span data-stu-id="c9e43-104">InterlockedAnd function</span></span>

<span data-ttu-id="c9e43-105">Il valore, in modo atomico.</span><span class="sxs-lookup"><span data-stu-id="c9e43-105">Ands the value, atomically.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9e43-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c9e43-106">Syntax</span></span>

``` syntax
void InterlockedAnd(
  in  UINT dest,
  in  UINT value,
  out UINT original_value
);
```

## <a name="parameters"></a><span data-ttu-id="c9e43-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="c9e43-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9e43-108">*dest* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c9e43-108">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9e43-109">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c9e43-109">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c9e43-110">Indirizzo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="c9e43-110">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="c9e43-111">*valore* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="c9e43-111">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9e43-112">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c9e43-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c9e43-113">Valore di input.</span><span class="sxs-lookup"><span data-stu-id="c9e43-113">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="c9e43-114">*\_ valore originale* in \[ uscita\]</span><span class="sxs-lookup"><span data-stu-id="c9e43-114">*original\_value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c9e43-115">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c9e43-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c9e43-116">Valore originale.</span><span class="sxs-lookup"><span data-stu-id="c9e43-116">The original value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9e43-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c9e43-117">Return value</span></span>

<span data-ttu-id="c9e43-118">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="c9e43-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9e43-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="c9e43-119">Remarks</span></span>

<span data-ttu-id="c9e43-120">Questa operazione può essere eseguita solo su risorse tipizzate int o uint e variabili di memoria condivisa.</span><span class="sxs-lookup"><span data-stu-id="c9e43-120">This operation can only be performed on int or uint typed resources and shared memory variables.</span></span> <span data-ttu-id="c9e43-121">Per questa funzione sono disponibili tre possibili utilizzi.</span><span class="sxs-lookup"><span data-stu-id="c9e43-121">There are three possible uses for this function.</span></span> <span data-ttu-id="c9e43-122">Il primo è quando R è un tipo di variabile di memoria condivisa.</span><span class="sxs-lookup"><span data-stu-id="c9e43-122">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="c9e43-123">In questo caso, la funzione esegue un'operazione atomica e di valore nel registro di memoria condiviso a cui fa riferimento dest.</span><span class="sxs-lookup"><span data-stu-id="c9e43-123">In this case, the function performs an atomic and of value to the shared memory register referenced by dest.</span></span> <span data-ttu-id="c9e43-124">Il secondo scenario è quando R è un tipo di variabile di risorsa.</span><span class="sxs-lookup"><span data-stu-id="c9e43-124">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="c9e43-125">In questo scenario, la funzione esegue un'operazione atomica e di valore nel percorso della risorsa a cui fa riferimento dest.</span><span class="sxs-lookup"><span data-stu-id="c9e43-125">In this scenario, the function performs an atomic and of value to the resource location referenced by dest.</span></span> <span data-ttu-id="c9e43-126">Infine, il terzo scenario è quando R è un tipo di variabile locale.</span><span class="sxs-lookup"><span data-stu-id="c9e43-126">Finally, the third scenario is when R is a local variable type.</span></span> <span data-ttu-id="c9e43-127">In questo scenario, la funzione riduce a e del valore di dest e value, archiviati in dest.</span><span class="sxs-lookup"><span data-stu-id="c9e43-127">In this scenario, the function reduces to an and of the value of dest and value, stored in dest.</span></span> <span data-ttu-id="c9e43-128">La funzione in overload ha una variabile di output aggiuntiva che verrà impostata sul valore originale di dest.</span><span class="sxs-lookup"><span data-stu-id="c9e43-128">The overloaded function has an additional output variable which will be set to the original value of dest.</span></span> <span data-ttu-id="c9e43-129">Questa operazione di overload è disponibile solo quando R è leggibile e scrivibile.</span><span class="sxs-lookup"><span data-stu-id="c9e43-129">This overloaded operation is only available when R is readable and writable.</span></span>

<span data-ttu-id="c9e43-130">Questa funzione è supportata nei tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="c9e43-130">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="c9e43-131">VS</span><span class="sxs-lookup"><span data-stu-id="c9e43-131">VS</span></span>  | <span data-ttu-id="c9e43-132">HS</span><span class="sxs-lookup"><span data-stu-id="c9e43-132">HS</span></span>  | <span data-ttu-id="c9e43-133">DS</span><span class="sxs-lookup"><span data-stu-id="c9e43-133">DS</span></span>  | <span data-ttu-id="c9e43-134">GS</span><span class="sxs-lookup"><span data-stu-id="c9e43-134">GS</span></span>  | <span data-ttu-id="c9e43-135">PS</span><span class="sxs-lookup"><span data-stu-id="c9e43-135">PS</span></span>  | <span data-ttu-id="c9e43-136">CS</span><span class="sxs-lookup"><span data-stu-id="c9e43-136">CS</span></span>  |
|-----|-----|-----|-----|-----|-----|
| <span data-ttu-id="c9e43-137">x</span><span class="sxs-lookup"><span data-stu-id="c9e43-137">x</span></span>   | <span data-ttu-id="c9e43-138">x</span><span class="sxs-lookup"><span data-stu-id="c9e43-138">x</span></span>   |  <span data-ttu-id="c9e43-139">x</span><span class="sxs-lookup"><span data-stu-id="c9e43-139">x</span></span>  | <span data-ttu-id="c9e43-140">x</span><span class="sxs-lookup"><span data-stu-id="c9e43-140">x</span></span>   | <span data-ttu-id="c9e43-141">x</span><span class="sxs-lookup"><span data-stu-id="c9e43-141">x</span></span>   | <span data-ttu-id="c9e43-142">x</span><span class="sxs-lookup"><span data-stu-id="c9e43-142">x</span></span>   |



 

## <a name="see-also"></a><span data-ttu-id="c9e43-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c9e43-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9e43-144">RWByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="c9e43-144">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="c9e43-145">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="c9e43-145">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 