---
title: 'Funzione WavePrefixSum '
description: Restituisce la somma di tutti i valori nelle corsie attive con indici più piccoli rispetto a questo.
ms.assetid: F51B90AB-3E85-4521-8A2C-7C16A4ECB1F9
keywords:
- Funzione WavePrefixSum HLSL
topic_type:
- apiref
api_name:
- WavePrefixSum
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b133aa37b522156df73914eef66c4d3695a70ed7
ms.sourcegitcommit: 41c742c88f7d9ce05e107008f186b6e872ff9288
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/31/2021
ms.locfileid: "104980983"
---
# <a name="waveprefixsum-function"></a><span data-ttu-id="f9e7f-104">Funzione WavePrefixSum </span><span class="sxs-lookup"><span data-stu-id="f9e7f-104">WavePrefixSum function</span></span>

<span data-ttu-id="f9e7f-105">Restituisce la somma di tutti i valori nelle corsie attive con indici più piccoli rispetto a questo.</span><span class="sxs-lookup"><span data-stu-id="f9e7f-105">Returns the sum of all of the values in the active lanes with smaller indices than this one.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9e7f-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f9e7f-106">Syntax</span></span>

``` syntax
<type> WavePrefixSum(
   <type> value
);
```

## <a name="parameters"></a><span data-ttu-id="f9e7f-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="f9e7f-107">Parameters</span></span>

<span data-ttu-id="f9e7f-108">*value*</span><span class="sxs-lookup"><span data-stu-id="f9e7f-108">*value*</span></span> 

<span data-ttu-id="f9e7f-109">Valore da sommare.</span><span class="sxs-lookup"><span data-stu-id="f9e7f-109">The value to sum up.</span></span>

## <a name="return-value"></a><span data-ttu-id="f9e7f-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f9e7f-110">Return value</span></span>

<span data-ttu-id="f9e7f-111">Somma dei valori.</span><span class="sxs-lookup"><span data-stu-id="f9e7f-111">The sum of the values.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9e7f-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="f9e7f-112">Remarks</span></span>

<span data-ttu-id="f9e7f-113">Non è possibile garantire l'ordine delle operazioni su questa routine.</span><span class="sxs-lookup"><span data-stu-id="f9e7f-113">The order of operations on this routine cannot be guaranteed.</span></span> <span data-ttu-id="f9e7f-114">Quindi, il \[ \] flag esatto viene ignorato al suo interno.</span><span class="sxs-lookup"><span data-stu-id="f9e7f-114">So, effectively, the \[precise\] flag is ignored within it.</span></span>

<span data-ttu-id="f9e7f-115">Una somma suffissa può essere calcolata aggiungendo il prefisso Sum al valore della corsia corrente.</span><span class="sxs-lookup"><span data-stu-id="f9e7f-115">A postfix sum can be computed by adding the prefix sum to the current lane's value.</span></span>

<span data-ttu-id="f9e7f-116">Si noti che la corsia attiva con l'indice più basso riceve sempre un valore 0 per la somma del prefisso.</span><span class="sxs-lookup"><span data-stu-id="f9e7f-116">Note that the active lane with the lowest index will always receive a 0 for its prefix sum.</span></span>

<span data-ttu-id="f9e7f-117">Questa funzione è supportata dal modello di shader 6,0 in tutte le fasi dello shader.</span><span class="sxs-lookup"><span data-stu-id="f9e7f-117">This function is supported from shader model 6.0 in all shader stages.</span></span> 

## <a name="examples"></a><span data-ttu-id="f9e7f-118">Esempio</span><span class="sxs-lookup"><span data-stu-id="f9e7f-118">Examples</span></span>

```hlsl
uint numToSum = 2;
uint prefixSum = WavePrefixSum( numToSum );
```

<span data-ttu-id="f9e7f-119">In un computer con una dimensione di onda pari a 8 e tutte le corsie attive eccetto le corsie 0 e 4, i valori seguenti verrebbero restituiti da WavePrefixSum.</span><span class="sxs-lookup"><span data-stu-id="f9e7f-119">On a machine with a wave size of 8, and all lanes active except lanes 0 and 4, the following values would be returned from WavePrefixSum.</span></span>

| <span data-ttu-id="f9e7f-120">Indice della corsia</span><span class="sxs-lookup"><span data-stu-id="f9e7f-120">lane index</span></span> | <span data-ttu-id="f9e7f-121">status</span><span class="sxs-lookup"><span data-stu-id="f9e7f-121">status</span></span>   | <span data-ttu-id="f9e7f-122">prefixSum</span><span class="sxs-lookup"><span data-stu-id="f9e7f-122">prefixSum</span></span>     | 
|------------|----------|---------------|
| <span data-ttu-id="f9e7f-123">0</span><span class="sxs-lookup"><span data-stu-id="f9e7f-123">0</span></span>          | <span data-ttu-id="f9e7f-124">inactive</span><span class="sxs-lookup"><span data-stu-id="f9e7f-124">inactive</span></span> | <span data-ttu-id="f9e7f-125">n/d</span><span class="sxs-lookup"><span data-stu-id="f9e7f-125">n/a</span></span>           |
| <span data-ttu-id="f9e7f-126">1</span><span class="sxs-lookup"><span data-stu-id="f9e7f-126">1</span></span>          | <span data-ttu-id="f9e7f-127">active</span><span class="sxs-lookup"><span data-stu-id="f9e7f-127">active</span></span>   | <span data-ttu-id="f9e7f-128">= 0</span><span class="sxs-lookup"><span data-stu-id="f9e7f-128">= 0</span></span>           |
| <span data-ttu-id="f9e7f-129">2</span><span class="sxs-lookup"><span data-stu-id="f9e7f-129">2</span></span>          | <span data-ttu-id="f9e7f-130">active</span><span class="sxs-lookup"><span data-stu-id="f9e7f-130">active</span></span>   | <span data-ttu-id="f9e7f-131">= 0 + 2</span><span class="sxs-lookup"><span data-stu-id="f9e7f-131">= 0+2</span></span>         |
| <span data-ttu-id="f9e7f-132">3</span><span class="sxs-lookup"><span data-stu-id="f9e7f-132">3</span></span>          | <span data-ttu-id="f9e7f-133">active</span><span class="sxs-lookup"><span data-stu-id="f9e7f-133">active</span></span>   | <span data-ttu-id="f9e7f-134">= 0 + 2 + 2</span><span class="sxs-lookup"><span data-stu-id="f9e7f-134">= 0+2+2</span></span>       |
| <span data-ttu-id="f9e7f-135">4</span><span class="sxs-lookup"><span data-stu-id="f9e7f-135">4</span></span>          | <span data-ttu-id="f9e7f-136">inactive</span><span class="sxs-lookup"><span data-stu-id="f9e7f-136">inactive</span></span> | <span data-ttu-id="f9e7f-137">n/d</span><span class="sxs-lookup"><span data-stu-id="f9e7f-137">n/a</span></span>           |
| <span data-ttu-id="f9e7f-138">5</span><span class="sxs-lookup"><span data-stu-id="f9e7f-138">5</span></span>          | <span data-ttu-id="f9e7f-139">active</span><span class="sxs-lookup"><span data-stu-id="f9e7f-139">active</span></span>   | <span data-ttu-id="f9e7f-140">= 0 + 2 + 2 + 2</span><span class="sxs-lookup"><span data-stu-id="f9e7f-140">= 0+2+2+2</span></span>     |
| <span data-ttu-id="f9e7f-141">6</span><span class="sxs-lookup"><span data-stu-id="f9e7f-141">6</span></span>          | <span data-ttu-id="f9e7f-142">active</span><span class="sxs-lookup"><span data-stu-id="f9e7f-142">active</span></span>   | <span data-ttu-id="f9e7f-143">= 0 + 2 + 2 + 2 + 2</span><span class="sxs-lookup"><span data-stu-id="f9e7f-143">= 0+2+2+2+2</span></span>   |
| <span data-ttu-id="f9e7f-144">7</span><span class="sxs-lookup"><span data-stu-id="f9e7f-144">7</span></span>          | <span data-ttu-id="f9e7f-145">active</span><span class="sxs-lookup"><span data-stu-id="f9e7f-145">active</span></span>   | <span data-ttu-id="f9e7f-146">= 0 + 2 + 2 + 2 + 2 + 2</span><span class="sxs-lookup"><span data-stu-id="f9e7f-146">= 0+2+2+2+2+2</span></span> |

## <a name="see-also"></a><span data-ttu-id="f9e7f-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f9e7f-147">See also</span></span>

[<span data-ttu-id="f9e7f-148">Panoramica del modello di shader 6</span><span class="sxs-lookup"><span data-stu-id="f9e7f-148">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)

[<span data-ttu-id="f9e7f-149">Modello shader 6</span><span class="sxs-lookup"><span data-stu-id="f9e7f-149">Shader Model 6</span></span>](shader-model-6-0.md)
