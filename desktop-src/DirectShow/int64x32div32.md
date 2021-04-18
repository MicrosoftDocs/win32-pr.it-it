---
description: La funzione Int64x32Div32 implementa la formula ((a \* b) + Rnd)/c dove a è un valore a 64 bit e b, c e Rnd sono valori a 32 bit.
ms.assetid: 566ac194-5b15-43b7-aa7c-0c18c6f69691
title: Funzione Int64x32Div32 (Wxutil. h)
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
ms.openlocfilehash: de60ca08b262dbf97aa118bd115bd6dc58576a1d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332026"
---
# <a name="int64x32div32-function"></a><span data-ttu-id="a6bfe-103">Int64x32Div32 (funzione)</span><span class="sxs-lookup"><span data-stu-id="a6bfe-103">Int64x32Div32 function</span></span>

<span data-ttu-id="a6bfe-104">La `Int64x32Div32` funzione implementa la formula `((a*b)+rnd)/c` in  cui è un valore a 64 bit e *b*, *c* e *Rnd* sono valori a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="a6bfe-104">The `Int64x32Div32` function implements the formula `((a*b)+rnd)/c` where *a* is a 64-bit value and *b*, *c*, and *rnd* are 32-bit values.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6bfe-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a6bfe-105">Syntax</span></span>


```C++
LONGLONG WINAPI Int64x32Div32(
   LONGLONG a,
   LONG     b,
   LONG     c,
   LONG     rnd
);
```



## <a name="parameters"></a><span data-ttu-id="a6bfe-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a6bfe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6bfe-107">*un*</span><span class="sxs-lookup"><span data-stu-id="a6bfe-107">*a*</span></span> 
</dt> <dd>

<span data-ttu-id="a6bfe-108">Multiplicand.</span><span class="sxs-lookup"><span data-stu-id="a6bfe-108">Multiplicand.</span></span>

</dd> <dt>

<span data-ttu-id="a6bfe-109">*b*</span><span class="sxs-lookup"><span data-stu-id="a6bfe-109">*b*</span></span> 
</dt> <dd>

<span data-ttu-id="a6bfe-110">Moltiplicatore.</span><span class="sxs-lookup"><span data-stu-id="a6bfe-110">Multiplier.</span></span>

</dd> <dt>

<span data-ttu-id="a6bfe-111">*c*</span><span class="sxs-lookup"><span data-stu-id="a6bfe-111">*c*</span></span> 
</dt> <dd>

<span data-ttu-id="a6bfe-112">Divisore.</span><span class="sxs-lookup"><span data-stu-id="a6bfe-112">Divisor.</span></span>

</dd> <dt>

<span data-ttu-id="a6bfe-113">*Rnd*</span><span class="sxs-lookup"><span data-stu-id="a6bfe-113">*rnd*</span></span> 
</dt> <dd>

<span data-ttu-id="a6bfe-114">Fattore di arrotondamento.</span><span class="sxs-lookup"><span data-stu-id="a6bfe-114">Rounding factor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6bfe-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a6bfe-115">Return value</span></span>

<span data-ttu-id="a6bfe-116">Restituisce il `(a * b + rnd)/c` calcolo o uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="a6bfe-116">Returns either the `(a * b + rnd)/c` calculation or one of the following values.</span></span>



| <span data-ttu-id="a6bfe-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="a6bfe-117">Return code</span></span>                                                                                       | <span data-ttu-id="a6bfe-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a6bfe-118">Description</span></span>                                                              |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a6bfe-119"><dt>**0x7FFFFFFFFFFFFFFF**</dt></span><span class="sxs-lookup"><span data-stu-id="a6bfe-119"><dt>**0x7FFFFFFFFFFFFFFF**</dt></span></span> </dl> | <span data-ttu-id="a6bfe-120">Si è verificato un overflow perché il risultato è troppo grande (positivo).</span><span class="sxs-lookup"><span data-stu-id="a6bfe-120">Overflow occurred because the result is too large (positive).</span></span><br/> |
| <dl> <span data-ttu-id="a6bfe-121"><dt>**0x8000000000000000**</dt></span><span class="sxs-lookup"><span data-stu-id="a6bfe-121"><dt>**0x8000000000000000**</dt></span></span> </dl> | <span data-ttu-id="a6bfe-122">Si è verificato un overflow perché il risultato è troppo grande (negativo).</span><span class="sxs-lookup"><span data-stu-id="a6bfe-122">Overflow occurred because the result is too large (negative).</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a6bfe-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="a6bfe-123">Remarks</span></span>

<span data-ttu-id="a6bfe-124">L'arrotondamento alla divisione è verso lo zero.</span><span class="sxs-lookup"><span data-stu-id="a6bfe-124">Rounding on the division is toward zero.</span></span> <span data-ttu-id="a6bfe-125">La divisione per zero viene conteggiata come condizione di overflow.</span><span class="sxs-lookup"><span data-stu-id="a6bfe-125">Division by zero is counted as an overflow condition.</span></span>

<span data-ttu-id="a6bfe-126">I timestamp e i tempi di ricerca sono valori a 64 bit, pertanto questa funzione è utile per l'esecuzione di conversioni su sistemi a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="a6bfe-126">Time stamps and seek times are 64-bit values, so this function is useful for performing conversions on 32-bit systems.</span></span> <span data-ttu-id="a6bfe-127">Ad esempio, in MPEG-1 il riferimento all'orologio di sistema è 90-kHz o 90.000 tick al secondo.</span><span class="sxs-lookup"><span data-stu-id="a6bfe-127">For example, in MPEG-1 the system clock reference is 90-kHz, or 90,000 ticks per second.</span></span> <span data-ttu-id="a6bfe-128">La formula per convertire questo oggetto in ora di riferimento (unità 100-nanosecondo) è</span><span class="sxs-lookup"><span data-stu-id="a6bfe-128">The formula to convert this to reference time (100-nanosecond units) is</span></span>


```C++
(timestamp * 1000) / 9
```



<span data-ttu-id="a6bfe-129">che può essere calcolato come `Int64x32Div32(timestamp, 1000, 9, 0)` .</span><span class="sxs-lookup"><span data-stu-id="a6bfe-129">which can be calculated as `Int64x32Div32(timestamp, 1000, 9, 0)`.</span></span> <span data-ttu-id="a6bfe-130">Usare il parametro *Rnd* come fattore di arrotondamento.</span><span class="sxs-lookup"><span data-stu-id="a6bfe-130">Use the *rnd* parameter as a rounding factor.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6bfe-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a6bfe-131">Requirements</span></span>



| <span data-ttu-id="a6bfe-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6bfe-132">Requirement</span></span> | <span data-ttu-id="a6bfe-133">Valore</span><span class="sxs-lookup"><span data-stu-id="a6bfe-133">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6bfe-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a6bfe-134">Header</span></span><br/>  | <dl> <span data-ttu-id="a6bfe-135"><dt>Wxutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a6bfe-135"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="a6bfe-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="a6bfe-136">Library</span></span><br/> | <dl> <span data-ttu-id="a6bfe-137"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="a6bfe-137"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6bfe-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a6bfe-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6bfe-139">Funzioni helper varie</span><span class="sxs-lookup"><span data-stu-id="a6bfe-139">Miscellaneous Helper Functions</span></span>](miscellaneous-helper-functions.md)
</dt> <dt>

[<span data-ttu-id="a6bfe-140">**llMulDiv**</span><span class="sxs-lookup"><span data-stu-id="a6bfe-140">**llMulDiv**</span></span>](llmuldiv.md)
</dt> </dl>

 

 




