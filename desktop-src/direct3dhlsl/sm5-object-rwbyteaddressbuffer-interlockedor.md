---
title: 'Funzione RWByteAddressBuffer:: interlockedr'
description: Esegue un oggetto atomico o sul valore.
ms.assetid: 3a05619b-db97-4cf1-af3c-12c376e605a6
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
ms.openlocfilehash: 14b902f70919c79ed3e313671ede709f284a1490
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963105"
---
# <a name="interlockedor-function"></a><span data-ttu-id="d0a2a-104">Funzione di interblocco</span><span class="sxs-lookup"><span data-stu-id="d0a2a-104">InterlockedOr function</span></span>

<span data-ttu-id="d0a2a-105">Esegue un oggetto atomico **o** sul valore.</span><span class="sxs-lookup"><span data-stu-id="d0a2a-105">Performs an atomic **OR** on the value.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0a2a-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d0a2a-106">Syntax</span></span>

``` syntax
void InterlockedOr(
  in  UINT dest,
  in  UINT value,
  out UINT original_value
);
```

## <a name="parameters"></a><span data-ttu-id="d0a2a-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="d0a2a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0a2a-108">*dest* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d0a2a-108">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0a2a-109">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d0a2a-109">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d0a2a-110">Indirizzo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="d0a2a-110">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="d0a2a-111">*valore* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="d0a2a-111">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0a2a-112">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d0a2a-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d0a2a-113">Valore di input.</span><span class="sxs-lookup"><span data-stu-id="d0a2a-113">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="d0a2a-114">*\_ valore originale* in \[ uscita\]</span><span class="sxs-lookup"><span data-stu-id="d0a2a-114">*original\_value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d0a2a-115">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d0a2a-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d0a2a-116">Valore originale.</span><span class="sxs-lookup"><span data-stu-id="d0a2a-116">The original value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0a2a-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d0a2a-117">Return value</span></span>

<span data-ttu-id="d0a2a-118">Nothing</span><span class="sxs-lookup"><span data-stu-id="d0a2a-118">Nothing</span></span>

## <a name="remarks"></a><span data-ttu-id="d0a2a-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="d0a2a-119">Remarks</span></span>

<span data-ttu-id="d0a2a-120">Questa operazione può essere eseguita solo su risorse tipizzate **int** o **uint** e variabili di memoria condivisa.</span><span class="sxs-lookup"><span data-stu-id="d0a2a-120">This operation can be performed only on **INT** or **UINT** typed resources and shared memory variables.</span></span> <span data-ttu-id="d0a2a-121">Per questa funzione sono disponibili tre possibili utilizzi.</span><span class="sxs-lookup"><span data-stu-id="d0a2a-121">There are three possible uses for this function.</span></span> <span data-ttu-id="d0a2a-122">Il primo è quando R è un tipo di variabile di memoria condivisa.</span><span class="sxs-lookup"><span data-stu-id="d0a2a-122">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="d0a2a-123">In questo caso, la funzione esegue un'operazione atomica **o** con il valore del registro di memoria condiviso a cui fa riferimento *dest*.</span><span class="sxs-lookup"><span data-stu-id="d0a2a-123">In this case, the function performs an atomic **OR** with the value of the shared memory register referenced by *dest*.</span></span> <span data-ttu-id="d0a2a-124">Il secondo scenario è quando R è un tipo di variabile di risorsa.</span><span class="sxs-lookup"><span data-stu-id="d0a2a-124">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="d0a2a-125">In questo scenario, la funzione esegue un'operazione atomica **o** con il valore della posizione della risorsa a cui fa riferimento *dest*.</span><span class="sxs-lookup"><span data-stu-id="d0a2a-125">In this scenario, the function performs an atomic **OR** with the value of the resource location referenced by *dest*.</span></span> <span data-ttu-id="d0a2a-126">Infine, il terzo scenario è quando R è un tipo di variabile locale.</span><span class="sxs-lookup"><span data-stu-id="d0a2a-126">Finally, the third scenario is when R is a local variable type.</span></span> <span data-ttu-id="d0a2a-127">In questo scenario, la funzione riduce a **o** con i valori di *dest* e *value*.</span><span class="sxs-lookup"><span data-stu-id="d0a2a-127">In this scenario, the function reduces to an **OR** with the values of *dest* and *value*.</span></span> <span data-ttu-id="d0a2a-128">Il risultato dell'operazione sostituisce il valore di *dest*.</span><span class="sxs-lookup"><span data-stu-id="d0a2a-128">The result of the operation replaces the value of *dest*.</span></span> <span data-ttu-id="d0a2a-129">La funzione in overload ha una variabile di output aggiuntiva, che verrà impostata sul valore originale di *dest*.</span><span class="sxs-lookup"><span data-stu-id="d0a2a-129">The overloaded function has an additional output variable, which will be set to the original value of *dest*.</span></span> <span data-ttu-id="d0a2a-130">Questa operazione di overload è disponibile solo se R è leggibile e scrivibile.</span><span class="sxs-lookup"><span data-stu-id="d0a2a-130">This overloaded operation is available only when R is readable and writable.</span></span>

<span data-ttu-id="d0a2a-131">Questa funzione è supportata nei tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="d0a2a-131">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="d0a2a-132">VS</span><span class="sxs-lookup"><span data-stu-id="d0a2a-132">VS</span></span>  | <span data-ttu-id="d0a2a-133">HS</span><span class="sxs-lookup"><span data-stu-id="d0a2a-133">HS</span></span>  | <span data-ttu-id="d0a2a-134">DS</span><span class="sxs-lookup"><span data-stu-id="d0a2a-134">DS</span></span>  | <span data-ttu-id="d0a2a-135">GS</span><span class="sxs-lookup"><span data-stu-id="d0a2a-135">GS</span></span>  | <span data-ttu-id="d0a2a-136">PS</span><span class="sxs-lookup"><span data-stu-id="d0a2a-136">PS</span></span>  | <span data-ttu-id="d0a2a-137">CS</span><span class="sxs-lookup"><span data-stu-id="d0a2a-137">CS</span></span>  |
|-----|-----|-----|-----|-----|-----|
| <span data-ttu-id="d0a2a-138">x</span><span class="sxs-lookup"><span data-stu-id="d0a2a-138">x</span></span>   |  <span data-ttu-id="d0a2a-139">x</span><span class="sxs-lookup"><span data-stu-id="d0a2a-139">x</span></span>  | <span data-ttu-id="d0a2a-140">x</span><span class="sxs-lookup"><span data-stu-id="d0a2a-140">x</span></span>   | <span data-ttu-id="d0a2a-141">x</span><span class="sxs-lookup"><span data-stu-id="d0a2a-141">x</span></span>   | <span data-ttu-id="d0a2a-142">x</span><span class="sxs-lookup"><span data-stu-id="d0a2a-142">x</span></span>   | <span data-ttu-id="d0a2a-143">x</span><span class="sxs-lookup"><span data-stu-id="d0a2a-143">x</span></span>   |



 

## <a name="see-also"></a><span data-ttu-id="d0a2a-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d0a2a-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0a2a-145">RWByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="d0a2a-145">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="d0a2a-146">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="d0a2a-146">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 