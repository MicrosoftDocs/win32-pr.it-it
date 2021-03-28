---
title: 'Funzione RWByteAddressBuffer:: InterlockedAdd'
description: Aggiunge il valore, atomicamente.
ms.assetid: 27274aae-1e75-4626-9997-57c4e9393000
keywords:
- Funzione InterlockedAdd HLSL
topic_type:
- apiref
api_name:
- InterlockedAdd
api_location:
- winnt.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d352ed97df15ce076c10950c6da94aaeaff0f2d0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993413"
---
# <a name="interlockedadd-function"></a><span data-ttu-id="c57a3-104">InterlockedAdd (funzione)</span><span class="sxs-lookup"><span data-stu-id="c57a3-104">InterlockedAdd function</span></span>

<span data-ttu-id="c57a3-105">Aggiunge il valore, atomicamente.</span><span class="sxs-lookup"><span data-stu-id="c57a3-105">Adds the value, atomically.</span></span>

## <a name="syntax"></a><span data-ttu-id="c57a3-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c57a3-106">Syntax</span></span>

``` syntax
void InterlockedAdd(
  in  UINT dest,
  in  UINT value,
  out UINT original_value
);
```

## <a name="parameters"></a><span data-ttu-id="c57a3-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="c57a3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c57a3-108">*dest* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c57a3-108">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c57a3-109">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c57a3-109">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c57a3-110">Indirizzo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="c57a3-110">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="c57a3-111">*valore* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="c57a3-111">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c57a3-112">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c57a3-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c57a3-113">Valore di input.</span><span class="sxs-lookup"><span data-stu-id="c57a3-113">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="c57a3-114">*\_ valore originale* in \[ uscita\]</span><span class="sxs-lookup"><span data-stu-id="c57a3-114">*original\_value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c57a3-115">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c57a3-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c57a3-116">Valore originale.</span><span class="sxs-lookup"><span data-stu-id="c57a3-116">The original value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c57a3-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c57a3-117">Return value</span></span>

<span data-ttu-id="c57a3-118">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="c57a3-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c57a3-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="c57a3-119">Remarks</span></span>

<span data-ttu-id="c57a3-120">Questa operazione può essere eseguita solo su risorse tipizzate int o uint e variabili di memoria condivisa.</span><span class="sxs-lookup"><span data-stu-id="c57a3-120">This operation can be performed only on int or uint typed resources and shared memory variables.</span></span> <span data-ttu-id="c57a3-121">Per questa funzione sono disponibili tre possibili utilizzi.</span><span class="sxs-lookup"><span data-stu-id="c57a3-121">There are three possible uses for this function.</span></span> <span data-ttu-id="c57a3-122">Il primo è quando R è un tipo di variabile di memoria condivisa.</span><span class="sxs-lookup"><span data-stu-id="c57a3-122">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="c57a3-123">In questo caso, la funzione esegue un aggiunta atomico del valore al registro della memoria condivisa a cui fa riferimento dest.</span><span class="sxs-lookup"><span data-stu-id="c57a3-123">In this case, the function performs an atomic add of value to the shared memory register referenced by dest.</span></span> <span data-ttu-id="c57a3-124">Il secondo scenario è quando R è un tipo di variabile di risorsa.</span><span class="sxs-lookup"><span data-stu-id="c57a3-124">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="c57a3-125">In questo scenario, la funzione esegue un aggiunta atomica del valore al percorso della risorsa a cui fa riferimento dest.</span><span class="sxs-lookup"><span data-stu-id="c57a3-125">In this scenario, the function performs an atomic add of the value to the resource location referenced by dest.</span></span> <span data-ttu-id="c57a3-126">Infine, il terzo scenario è quando R è un tipo di variabile locale.</span><span class="sxs-lookup"><span data-stu-id="c57a3-126">Finally, the third scenario is when R is a local variable type.</span></span> <span data-ttu-id="c57a3-127">In questo scenario, la funzione riduce a una somma del valore di dest e value, archiviati in dest.</span><span class="sxs-lookup"><span data-stu-id="c57a3-127">In this scenario, the function reduces to a sum of the value of dest and value, stored in dest.</span></span> <span data-ttu-id="c57a3-128">La funzione in overload ha una variabile di output aggiuntiva che verrà impostata sul valore originale di dest.</span><span class="sxs-lookup"><span data-stu-id="c57a3-128">The overloaded function has an additional output variable which will be set to the original value of dest.</span></span> <span data-ttu-id="c57a3-129">Questa operazione di overload è disponibile solo quando R è leggibile e scrivibile.</span><span class="sxs-lookup"><span data-stu-id="c57a3-129">This overloaded operation is only available when R is readable and writable.</span></span>

<span data-ttu-id="c57a3-130">Questa funzione è supportata nei tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="c57a3-130">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="c57a3-131">VS</span><span class="sxs-lookup"><span data-stu-id="c57a3-131">VS</span></span>  | <span data-ttu-id="c57a3-132">HS</span><span class="sxs-lookup"><span data-stu-id="c57a3-132">HS</span></span>  | <span data-ttu-id="c57a3-133">DS</span><span class="sxs-lookup"><span data-stu-id="c57a3-133">DS</span></span>  | <span data-ttu-id="c57a3-134">GS</span><span class="sxs-lookup"><span data-stu-id="c57a3-134">GS</span></span>  | <span data-ttu-id="c57a3-135">PS</span><span class="sxs-lookup"><span data-stu-id="c57a3-135">PS</span></span>  | <span data-ttu-id="c57a3-136">CS</span><span class="sxs-lookup"><span data-stu-id="c57a3-136">CS</span></span>  |
|-----|-----|-----|-----|-----|-----|
| <span data-ttu-id="c57a3-137">x</span><span class="sxs-lookup"><span data-stu-id="c57a3-137">x</span></span>   | <span data-ttu-id="c57a3-138">x</span><span class="sxs-lookup"><span data-stu-id="c57a3-138">x</span></span>   | <span data-ttu-id="c57a3-139">x</span><span class="sxs-lookup"><span data-stu-id="c57a3-139">x</span></span>   | <span data-ttu-id="c57a3-140">x</span><span class="sxs-lookup"><span data-stu-id="c57a3-140">x</span></span>   | <span data-ttu-id="c57a3-141">x</span><span class="sxs-lookup"><span data-stu-id="c57a3-141">x</span></span>   | <span data-ttu-id="c57a3-142">x</span><span class="sxs-lookup"><span data-stu-id="c57a3-142">x</span></span>   |



 

## <a name="requirements"></a><span data-ttu-id="c57a3-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c57a3-143">Requirements</span></span>




## <a name="see-also"></a><span data-ttu-id="c57a3-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c57a3-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c57a3-145">RWByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="c57a3-145">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="c57a3-146">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="c57a3-146">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

