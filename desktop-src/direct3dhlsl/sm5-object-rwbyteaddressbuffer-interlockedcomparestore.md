---
title: 'Funzione RWByteAddressBuffer:: InterlockedCompareStore'
description: Ccompares l'input al valore di confronto in modo atomico.
ms.assetid: d82a73b6-24a5-4eb3-9f20-15ba263c93d0
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
ms.openlocfilehash: abaa390ba74657e42b54a5147a7bc4006564a5fb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872786"
---
# <a name="interlockedcomparestore-function"></a><span data-ttu-id="2c736-104">InterlockedCompareStore (funzione)</span><span class="sxs-lookup"><span data-stu-id="2c736-104">InterlockedCompareStore function</span></span>

<span data-ttu-id="2c736-105">Ccompares l'input al valore di confronto in modo atomico.</span><span class="sxs-lookup"><span data-stu-id="2c736-105">Ccompares the input to the comparison value, atomically.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c736-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2c736-106">Syntax</span></span>

``` syntax
void InterlockedCompareStore(
  in UINT dest,
  in UINT compare_value,
  in UINT value
);
```

## <a name="parameters"></a><span data-ttu-id="2c736-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="2c736-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c736-108">*dest* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2c736-108">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c736-109">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="2c736-109">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="2c736-110">Indirizzo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="2c736-110">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="2c736-111">*Confronta \_ valore* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2c736-111">*compare\_value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c736-112">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="2c736-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="2c736-113">Valore di confronto.</span><span class="sxs-lookup"><span data-stu-id="2c736-113">The comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="2c736-114">*valore* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="2c736-114">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c736-115">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="2c736-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="2c736-116">Valore di input.</span><span class="sxs-lookup"><span data-stu-id="2c736-116">The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c736-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2c736-117">Return value</span></span>

<span data-ttu-id="2c736-118">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="2c736-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c736-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="2c736-119">Remarks</span></span>

<span data-ttu-id="2c736-120">Questa operazione può essere eseguita solo su risorse tipizzate int o uint e variabili di memoria condivisa.</span><span class="sxs-lookup"><span data-stu-id="2c736-120">This operation can only be performed on int or uint typed resources and shared memory variables.</span></span> <span data-ttu-id="2c736-121">Per questa funzione sono disponibili tre possibili utilizzi.</span><span class="sxs-lookup"><span data-stu-id="2c736-121">There are three possible uses for this function.</span></span> <span data-ttu-id="2c736-122">Il primo è quando R è un tipo di variabile di memoria condivisa.</span><span class="sxs-lookup"><span data-stu-id="2c736-122">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="2c736-123">In questo caso, la funzione esegue l'operazione sul Registro di memoria condiviso a cui fa riferimento dest.</span><span class="sxs-lookup"><span data-stu-id="2c736-123">In this case, the function performs the operation on the shared memory register referenced by dest.</span></span> <span data-ttu-id="2c736-124">Il secondo scenario è quando R è un tipo di variabile di risorsa.</span><span class="sxs-lookup"><span data-stu-id="2c736-124">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="2c736-125">In questo scenario, la funzione esegue l'operazione sul percorso della risorsa a cui fa riferimento dest.</span><span class="sxs-lookup"><span data-stu-id="2c736-125">In this scenario, the function performs the operation on the resource location referenced by dest.</span></span> <span data-ttu-id="2c736-126">Infine, il terzo scenario è quando R è un tipo di variabile locale.</span><span class="sxs-lookup"><span data-stu-id="2c736-126">Finally, the third scenario is when R is a local variable type.</span></span> <span data-ttu-id="2c736-127">In questo scenario, la funzione riduce l'operazione eseguita usando le operazioni locali.</span><span class="sxs-lookup"><span data-stu-id="2c736-127">In this scenario, the function reduces to the operation performed using local operations.</span></span>

<span data-ttu-id="2c736-128">Questa funzione è supportata nei tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="2c736-128">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="2c736-129">VS</span><span class="sxs-lookup"><span data-stu-id="2c736-129">VS</span></span>  | <span data-ttu-id="2c736-130">HS</span><span class="sxs-lookup"><span data-stu-id="2c736-130">HS</span></span>  | <span data-ttu-id="2c736-131">DS</span><span class="sxs-lookup"><span data-stu-id="2c736-131">DS</span></span>  | <span data-ttu-id="2c736-132">GS</span><span class="sxs-lookup"><span data-stu-id="2c736-132">GS</span></span>  | <span data-ttu-id="2c736-133">PS</span><span class="sxs-lookup"><span data-stu-id="2c736-133">PS</span></span>  | <span data-ttu-id="2c736-134">CS</span><span class="sxs-lookup"><span data-stu-id="2c736-134">CS</span></span>  |
|-----|-----|-----|-----|-----|-----|
| <span data-ttu-id="2c736-135">x</span><span class="sxs-lookup"><span data-stu-id="2c736-135">x</span></span>   | <span data-ttu-id="2c736-136">x</span><span class="sxs-lookup"><span data-stu-id="2c736-136">x</span></span>   | <span data-ttu-id="2c736-137">x</span><span class="sxs-lookup"><span data-stu-id="2c736-137">x</span></span>   | <span data-ttu-id="2c736-138">x</span><span class="sxs-lookup"><span data-stu-id="2c736-138">x</span></span>   | <span data-ttu-id="2c736-139">x</span><span class="sxs-lookup"><span data-stu-id="2c736-139">x</span></span>   | <span data-ttu-id="2c736-140">x</span><span class="sxs-lookup"><span data-stu-id="2c736-140">x</span></span>   |



 

## <a name="see-also"></a><span data-ttu-id="2c736-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2c736-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c736-142">RWByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="2c736-142">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="2c736-143">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="2c736-143">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 