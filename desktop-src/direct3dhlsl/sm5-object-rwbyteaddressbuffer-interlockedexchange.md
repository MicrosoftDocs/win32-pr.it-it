---
title: 'Funzione RWByteAddressBuffer:: InterlockedExchange'
description: Scambia un valore in modo atomico.
ms.assetid: a50f4cba-a7a2-44b0-9de7-003b4c7a947f
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
ms.openlocfilehash: 47c51374b7dcd62ac208e0aa8811a8d693ce0ac6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993352"
---
# <a name="interlockedexchange-function"></a><span data-ttu-id="496f6-104">InterlockedExchange (funzione)</span><span class="sxs-lookup"><span data-stu-id="496f6-104">InterlockedExchange function</span></span>

<span data-ttu-id="496f6-105">Scambia un valore in modo atomico.</span><span class="sxs-lookup"><span data-stu-id="496f6-105">Exchanges a value, atomically.</span></span>

## <a name="syntax"></a><span data-ttu-id="496f6-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="496f6-106">Syntax</span></span>

``` syntax
void InterlockedExchange(
  in  UINT dest,
  in  UINT value,
  out UINT original_value
);
```

## <a name="parameters"></a><span data-ttu-id="496f6-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="496f6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="496f6-108">*dest* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="496f6-108">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="496f6-109">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="496f6-109">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="496f6-110">Indirizzo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="496f6-110">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="496f6-111">*valore* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="496f6-111">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="496f6-112">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="496f6-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="496f6-113">Valore di input.</span><span class="sxs-lookup"><span data-stu-id="496f6-113">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="496f6-114">*\_ valore originale* in \[ uscita\]</span><span class="sxs-lookup"><span data-stu-id="496f6-114">*original\_value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="496f6-115">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="496f6-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="496f6-116">Valore originale.</span><span class="sxs-lookup"><span data-stu-id="496f6-116">The original value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="496f6-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="496f6-117">Return value</span></span>

<span data-ttu-id="496f6-118">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="496f6-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="496f6-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="496f6-119">Remarks</span></span>

<span data-ttu-id="496f6-120">Questa operazione può essere eseguita solo su risorse con tipizzazione scalare e variabili di memoria condivisa.</span><span class="sxs-lookup"><span data-stu-id="496f6-120">This operation can only be performed on scalar-typed resources and shared memory variables.</span></span> <span data-ttu-id="496f6-121">Per questa funzione sono disponibili tre possibili utilizzi.</span><span class="sxs-lookup"><span data-stu-id="496f6-121">There are three possible uses for this function.</span></span> <span data-ttu-id="496f6-122">Il primo è quando R è un tipo di variabile di memoria condivisa.</span><span class="sxs-lookup"><span data-stu-id="496f6-122">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="496f6-123">In questo caso, la funzione esegue l'operazione sul Registro di memoria condiviso a cui fa riferimento dest.</span><span class="sxs-lookup"><span data-stu-id="496f6-123">In this case, the function performs the operation on the shared memory register referenced by dest.</span></span> <span data-ttu-id="496f6-124">Il secondo scenario è quando R è un tipo di variabile di risorsa.</span><span class="sxs-lookup"><span data-stu-id="496f6-124">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="496f6-125">In questo scenario, la funzione esegue l'operazione sul percorso della risorsa a cui fa riferimento dest.</span><span class="sxs-lookup"><span data-stu-id="496f6-125">In this scenario, the function performs the operation on the resource location referenced by dest.</span></span> <span data-ttu-id="496f6-126">Infine, il terzo scenario è quando R è un tipo di variabile locale.</span><span class="sxs-lookup"><span data-stu-id="496f6-126">Finally, the third scenario is when R is a local variable type.</span></span> <span data-ttu-id="496f6-127">In questo scenario, la funzione riduce l'operazione eseguita usando le operazioni locali.</span><span class="sxs-lookup"><span data-stu-id="496f6-127">In this scenario, the function reduces to the operation performed using local operations.</span></span> <span data-ttu-id="496f6-128">Questa operazione è disponibile solo se R è leggibile e scrivibile.</span><span class="sxs-lookup"><span data-stu-id="496f6-128">This operation is only available when R is readable and writable.</span></span>

<span data-ttu-id="496f6-129">Questa funzione è supportata nei tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="496f6-129">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="496f6-130">VS</span><span class="sxs-lookup"><span data-stu-id="496f6-130">VS</span></span>  | <span data-ttu-id="496f6-131">HS</span><span class="sxs-lookup"><span data-stu-id="496f6-131">HS</span></span>  | <span data-ttu-id="496f6-132">DS</span><span class="sxs-lookup"><span data-stu-id="496f6-132">DS</span></span>  | <span data-ttu-id="496f6-133">GS</span><span class="sxs-lookup"><span data-stu-id="496f6-133">GS</span></span>  | <span data-ttu-id="496f6-134">PS</span><span class="sxs-lookup"><span data-stu-id="496f6-134">PS</span></span>  | <span data-ttu-id="496f6-135">CS</span><span class="sxs-lookup"><span data-stu-id="496f6-135">CS</span></span>  |
|-----|-----|-----|-----|-----|-----|
|  <span data-ttu-id="496f6-136">x</span><span class="sxs-lookup"><span data-stu-id="496f6-136">x</span></span>  |  <span data-ttu-id="496f6-137">x</span><span class="sxs-lookup"><span data-stu-id="496f6-137">x</span></span>  |  <span data-ttu-id="496f6-138">x</span><span class="sxs-lookup"><span data-stu-id="496f6-138">x</span></span>  |  <span data-ttu-id="496f6-139">x</span><span class="sxs-lookup"><span data-stu-id="496f6-139">x</span></span>  | <span data-ttu-id="496f6-140">x</span><span class="sxs-lookup"><span data-stu-id="496f6-140">x</span></span>   | <span data-ttu-id="496f6-141">x</span><span class="sxs-lookup"><span data-stu-id="496f6-141">x</span></span>   |



 

## <a name="see-also"></a><span data-ttu-id="496f6-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="496f6-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="496f6-143">RWByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="496f6-143">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="496f6-144">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="496f6-144">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 