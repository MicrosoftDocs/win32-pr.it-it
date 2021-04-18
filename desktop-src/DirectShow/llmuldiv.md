---
description: La funzione llMulDiv implementa la formula ((a \* b) + Rnd)/c, dove ogni termine è un valore a 64 bit.
ms.assetid: cd5073b9-27c7-42ee-8487-2d4ea29f77d4
title: funzione llMulDiv (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Int64x32Div32
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e45d22eec1536517bd2b57d875dd596e4a1e28db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327421"
---
# <a name="llmuldiv-function"></a><span data-ttu-id="60d32-103">llMulDiv (funzione)</span><span class="sxs-lookup"><span data-stu-id="60d32-103">llMulDiv function</span></span>

<span data-ttu-id="60d32-104">La `llMulDiv` funzione implementa la formula in `((a*b)+rnd)/c` cui ogni termine è un valore a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="60d32-104">The `llMulDiv` function implements the formula `((a*b)+rnd)/c` where each term is a 64-bit value.</span></span>

<span data-ttu-id="60d32-105">I timestamp e i tempi di ricerca sono valori a 64 bit, pertanto questa funzione è utile per l'esecuzione di conversioni su sistemi a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="60d32-105">Time stamps and seek times are 64-bit values, so this function is useful for performing conversions on 32-bit systems.</span></span> <span data-ttu-id="60d32-106">Ad esempio, la formula per byte al secondo è</span><span class="sxs-lookup"><span data-stu-id="60d32-106">For example, the formula for bytes-per-second is</span></span>


```C++
(Number of Bytes * Reference Time) / 10,000,000
```



<span data-ttu-id="60d32-107">che può essere calcolato come `llMulDiv(nBytes, rtTime, 10000000, 0)` .</span><span class="sxs-lookup"><span data-stu-id="60d32-107">which can be calculated as `llMulDiv(nBytes, rtTime, 10000000, 0)`.</span></span> <span data-ttu-id="60d32-108">Usare il parametro *Rnd* come fattore di arrotondamento.</span><span class="sxs-lookup"><span data-stu-id="60d32-108">Use the *rnd* parameter as a rounding factor.</span></span>

## <a name="syntax"></a><span data-ttu-id="60d32-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="60d32-109">Syntax</span></span>


```C++
LONGLONG WINAPI Int64x32Div32(
   LONGLONG a,
   LONGLONG b,
   LONGLONG c,
   LONGLONG rnd
);
```



## <a name="parameters"></a><span data-ttu-id="60d32-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="60d32-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60d32-111">*un*</span><span class="sxs-lookup"><span data-stu-id="60d32-111">*a*</span></span> 
</dt> <dd>

<span data-ttu-id="60d32-112">Multiplicand.</span><span class="sxs-lookup"><span data-stu-id="60d32-112">Multiplicand.</span></span>

</dd> <dt>

<span data-ttu-id="60d32-113">*b*</span><span class="sxs-lookup"><span data-stu-id="60d32-113">*b*</span></span> 
</dt> <dd>

<span data-ttu-id="60d32-114">Moltiplicatore.</span><span class="sxs-lookup"><span data-stu-id="60d32-114">Multiplier.</span></span>

</dd> <dt>

<span data-ttu-id="60d32-115">*c*</span><span class="sxs-lookup"><span data-stu-id="60d32-115">*c*</span></span> 
</dt> <dd>

<span data-ttu-id="60d32-116">Divisore.</span><span class="sxs-lookup"><span data-stu-id="60d32-116">Divisor.</span></span>

</dd> <dt>

<span data-ttu-id="60d32-117">*Rnd*</span><span class="sxs-lookup"><span data-stu-id="60d32-117">*rnd*</span></span> 
</dt> <dd>

<span data-ttu-id="60d32-118">Fattore di arrotondamento.</span><span class="sxs-lookup"><span data-stu-id="60d32-118">Rounding factor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60d32-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="60d32-119">Return value</span></span>

<span data-ttu-id="60d32-120">Restituisce il `(a * b + rnd)/c` calcolo o uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="60d32-120">Returns either the `(a * b + rnd)/c` calculation or one of the following values.</span></span>



| <span data-ttu-id="60d32-121">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="60d32-121">Return code</span></span>                                                                                       | <span data-ttu-id="60d32-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="60d32-122">Description</span></span>                                                              |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="60d32-123"><dt>**0x7FFFFFFFFFFFFFFF**</dt></span><span class="sxs-lookup"><span data-stu-id="60d32-123"><dt>**0x7FFFFFFFFFFFFFFF**</dt></span></span> </dl> | <span data-ttu-id="60d32-124">Si è verificato un overflow perché il risultato è troppo grande (positivo).</span><span class="sxs-lookup"><span data-stu-id="60d32-124">Overflow occurred because the result is too large (positive).</span></span><br/> |
| <dl> <span data-ttu-id="60d32-125"><dt>**0x8000000000000000**</dt></span><span class="sxs-lookup"><span data-stu-id="60d32-125"><dt>**0x8000000000000000**</dt></span></span> </dl> | <span data-ttu-id="60d32-126">Si è verificato un overflow perché il risultato è troppo grande (negativo).</span><span class="sxs-lookup"><span data-stu-id="60d32-126">Overflow occurred because the result is too large (negative).</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="60d32-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="60d32-127">Remarks</span></span>

<span data-ttu-id="60d32-128">L'arrotondamento alla divisione è verso lo zero.</span><span class="sxs-lookup"><span data-stu-id="60d32-128">Rounding on the division is toward zero.</span></span> <span data-ttu-id="60d32-129">La divisione per zero viene conteggiata come condizione di overflow.</span><span class="sxs-lookup"><span data-stu-id="60d32-129">Division by zero is counted as an overflow condition.</span></span>

## <a name="requirements"></a><span data-ttu-id="60d32-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="60d32-130">Requirements</span></span>



| <span data-ttu-id="60d32-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="60d32-131">Requirement</span></span> | <span data-ttu-id="60d32-132">Valore</span><span class="sxs-lookup"><span data-stu-id="60d32-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60d32-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="60d32-133">Header</span></span><br/>  | <dl> <span data-ttu-id="60d32-134"><dt>Wxutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="60d32-134"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="60d32-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="60d32-135">Library</span></span><br/> | <dl> <span data-ttu-id="60d32-136"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="60d32-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60d32-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="60d32-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60d32-138">Funzioni helper varie</span><span class="sxs-lookup"><span data-stu-id="60d32-138">Miscellaneous Helper Functions</span></span>](miscellaneous-helper-functions.md)
</dt> <dt>

[<span data-ttu-id="60d32-139">**Int64x32Div32**</span><span class="sxs-lookup"><span data-stu-id="60d32-139">**Int64x32Div32**</span></span>](int64x32div32.md)
</dt> </dl>

 

 




