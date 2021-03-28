---
title: 'Funzione WavePrefixProduct '
description: Restituisce il prodotto di tutti i valori nelle corsie attive in questa Wave con indici inferiori a questa corsia.
ms.assetid: 3A5B271D-EF45-4511-9086-A9AD0D215D9A
keywords:
- Funzione WavePrefixProduct HLSL
topic_type:
- apiref
api_name:
- WavePrefixProduct
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d073d72590951ddbbbb74274d4cd237e0a138c4f
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104399934"
---
# <a name="waveprefixproduct-function"></a><span data-ttu-id="ade4a-104">Funzione WavePrefixProduct </span><span class="sxs-lookup"><span data-stu-id="ade4a-104">WavePrefixProduct function</span></span>

<span data-ttu-id="ade4a-105">Restituisce il prodotto di tutti i valori nelle corsie attive in questa Wave con indici inferiori a questa corsia.</span><span class="sxs-lookup"><span data-stu-id="ade4a-105">Returns the product of all of the values in the active lanes in this wave with indices less than this lane.</span></span>

## <a name="syntax"></a><span data-ttu-id="ade4a-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ade4a-106">Syntax</span></span>

``` syntax
<type> WavePrefixProduct(
   <type> value
);
```

## <a name="parameters"></a><span data-ttu-id="ade4a-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="ade4a-107">Parameters</span></span>

<span data-ttu-id="ade4a-108">*value*</span><span class="sxs-lookup"><span data-stu-id="ade4a-108">*value*</span></span> 

<span data-ttu-id="ade4a-109">Valore da moltiplicare.</span><span class="sxs-lookup"><span data-stu-id="ade4a-109">The value to multiply.</span></span>

## <a name="return-value"></a><span data-ttu-id="ade4a-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ade4a-110">Return value</span></span>

<span data-ttu-id="ade4a-111">Prodotto di tutti i valori.</span><span class="sxs-lookup"><span data-stu-id="ade4a-111">The product of all the values.</span></span>

## <a name="remarks"></a><span data-ttu-id="ade4a-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="ade4a-112">Remarks</span></span>

<span data-ttu-id="ade4a-113">Non è possibile garantire l'ordine delle operazioni su questa routine.</span><span class="sxs-lookup"><span data-stu-id="ade4a-113">The order of operations on this routine cannot be guaranteed.</span></span> <span data-ttu-id="ade4a-114">Quindi, il \[ \] flag esatto viene ignorato al suo interno.</span><span class="sxs-lookup"><span data-stu-id="ade4a-114">So, effectively, the \[precise\] flag is ignored within it.</span></span>

<span data-ttu-id="ade4a-115">Un prodotto suffisso può essere calcolato moltiplicando il prodotto di prefisso per il valore della corsia corrente.</span><span class="sxs-lookup"><span data-stu-id="ade4a-115">A postfix product can be computed by multiplying the prefix product by the current lane's value.</span></span>

<span data-ttu-id="ade4a-116">Si noti che la corsia attiva con l'indice più basso riceve sempre 1 per il prodotto prefisso.</span><span class="sxs-lookup"><span data-stu-id="ade4a-116">Note that the active lane with the lowest index will always receive a 1 for its prefix product.</span></span>

<span data-ttu-id="ade4a-117">Questa funzione è supportata dal modello di shader 6,0 in tutte le fasi dello shader.</span><span class="sxs-lookup"><span data-stu-id="ade4a-117">This function is supported from shader model 6.0 in all shader stages.</span></span> 

## <a name="examples"></a><span data-ttu-id="ade4a-118">Esempio</span><span class="sxs-lookup"><span data-stu-id="ade4a-118">Examples</span></span>

```hlsl
uint numToMultiply = 2;
uint prefixProduct = WavePrefixProduct( numToMultiply );
```

<span data-ttu-id="ade4a-119">In un computer con una dimensione di onda pari a 8 e tutte le corsie attive eccetto le corsie 0 e 4, i valori seguenti verrebbero restituiti da WavePrefixProduct.</span><span class="sxs-lookup"><span data-stu-id="ade4a-119">On a machine with a wave size of 8, and all lanes active except lanes 0 and 4, the following values would be returned from WavePrefixProduct.</span></span>

| <span data-ttu-id="ade4a-120">Indice della corsia</span><span class="sxs-lookup"><span data-stu-id="ade4a-120">lane index</span></span> | <span data-ttu-id="ade4a-121">status</span><span class="sxs-lookup"><span data-stu-id="ade4a-121">status</span></span>   | <span data-ttu-id="ade4a-122">prefixProduct</span><span class="sxs-lookup"><span data-stu-id="ade4a-122">prefixProduct</span></span> | 
|------------|----------|---------------|
| <span data-ttu-id="ade4a-123">0</span><span class="sxs-lookup"><span data-stu-id="ade4a-123">0</span></span>          | <span data-ttu-id="ade4a-124">inactive</span><span class="sxs-lookup"><span data-stu-id="ade4a-124">inactive</span></span> | <span data-ttu-id="ade4a-125">n/d</span><span class="sxs-lookup"><span data-stu-id="ade4a-125">n/a</span></span>           |
| <span data-ttu-id="ade4a-126">1</span><span class="sxs-lookup"><span data-stu-id="ade4a-126">1</span></span>          | <span data-ttu-id="ade4a-127">active</span><span class="sxs-lookup"><span data-stu-id="ade4a-127">active</span></span>   | <span data-ttu-id="ade4a-128">= 1</span><span class="sxs-lookup"><span data-stu-id="ade4a-128">= 1</span></span>           |
| <span data-ttu-id="ade4a-129">2</span><span class="sxs-lookup"><span data-stu-id="ade4a-129">2</span></span>          | <span data-ttu-id="ade4a-130">active</span><span class="sxs-lookup"><span data-stu-id="ade4a-130">active</span></span>   | <span data-ttu-id="ade4a-131">= 1 \* 2</span><span class="sxs-lookup"><span data-stu-id="ade4a-131">= 1\*2</span></span>        |
| <span data-ttu-id="ade4a-132">3</span><span class="sxs-lookup"><span data-stu-id="ade4a-132">3</span></span>          | <span data-ttu-id="ade4a-133">active</span><span class="sxs-lookup"><span data-stu-id="ade4a-133">active</span></span>   | <span data-ttu-id="ade4a-134">= 1 \* 2 \* 2</span><span class="sxs-lookup"><span data-stu-id="ade4a-134">= 1\*2\*2</span></span>     |
| <span data-ttu-id="ade4a-135">4</span><span class="sxs-lookup"><span data-stu-id="ade4a-135">4</span></span>          | <span data-ttu-id="ade4a-136">inactive</span><span class="sxs-lookup"><span data-stu-id="ade4a-136">inactive</span></span> | <span data-ttu-id="ade4a-137">n/d</span><span class="sxs-lookup"><span data-stu-id="ade4a-137">n/a</span></span>           |
| <span data-ttu-id="ade4a-138">5</span><span class="sxs-lookup"><span data-stu-id="ade4a-138">5</span></span>          | <span data-ttu-id="ade4a-139">active</span><span class="sxs-lookup"><span data-stu-id="ade4a-139">active</span></span>   | <span data-ttu-id="ade4a-140">= 1 \* 2 \* 2 2 \*</span><span class="sxs-lookup"><span data-stu-id="ade4a-140">= 1\*2\*2\*2</span></span>       |
| <span data-ttu-id="ade4a-141">6</span><span class="sxs-lookup"><span data-stu-id="ade4a-141">6</span></span>          | <span data-ttu-id="ade4a-142">active</span><span class="sxs-lookup"><span data-stu-id="ade4a-142">active</span></span>   | <span data-ttu-id="ade4a-143">= 1 \* 2 \* 2 \* 2 \* 2</span><span class="sxs-lookup"><span data-stu-id="ade4a-143">= 1\*2\*2\*2\*2</span></span>    |
| <span data-ttu-id="ade4a-144">7</span><span class="sxs-lookup"><span data-stu-id="ade4a-144">7</span></span>          | <span data-ttu-id="ade4a-145">active</span><span class="sxs-lookup"><span data-stu-id="ade4a-145">active</span></span>   | <span data-ttu-id="ade4a-146">= 1 \* 2 \* 2 \* 2 \* 2 \* 2</span><span class="sxs-lookup"><span data-stu-id="ade4a-146">= 1\*2\*2\*2\*2\*2</span></span> |

## <a name="see-also"></a><span data-ttu-id="ade4a-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ade4a-147">See also</span></span>

[<span data-ttu-id="ade4a-148">Panoramica del modello di shader 6</span><span class="sxs-lookup"><span data-stu-id="ade4a-148">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)

[<span data-ttu-id="ade4a-149">Modello shader 6</span><span class="sxs-lookup"><span data-stu-id="ade4a-149">Shader Model 6</span></span>](shader-model-6-0.md)
