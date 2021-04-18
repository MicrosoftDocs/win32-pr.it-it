---
description: La funzione DbgOutString invia una stringa al percorso di output di debug. Ignorato nelle compilazioni al dettaglio.
ms.assetid: 644bf4f7-ec2d-466e-85c6-690dd44da702
title: Funzione DbgOutString (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgOutString
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bdc12d4b73080f00a3d32c80074a801146ea4a74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327522"
---
# <a name="dbgoutstring-function"></a><span data-ttu-id="68e05-104">DbgOutString (funzione)</span><span class="sxs-lookup"><span data-stu-id="68e05-104">DbgOutString function</span></span>

<span data-ttu-id="68e05-105">La funzione **DbgOutString** invia una stringa al percorso di output di debug.</span><span class="sxs-lookup"><span data-stu-id="68e05-105">The **DbgOutString** function sends a string to the debug output location.</span></span> <span data-ttu-id="68e05-106">Ignorato nelle compilazioni al dettaglio.</span><span class="sxs-lookup"><span data-stu-id="68e05-106">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="68e05-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="68e05-107">Syntax</span></span>


```C++
void DbgOutString(
   LPCTSTR psz
);
```



## <a name="parameters"></a><span data-ttu-id="68e05-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="68e05-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68e05-109">*PSZ*</span><span class="sxs-lookup"><span data-stu-id="68e05-109">*psz*</span></span> 
</dt> <dd>

<span data-ttu-id="68e05-110">Stringa da restituire.</span><span class="sxs-lookup"><span data-stu-id="68e05-110">String to output.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68e05-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="68e05-111">Return value</span></span>

<span data-ttu-id="68e05-112">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="68e05-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="68e05-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="68e05-113">Remarks</span></span>

<span data-ttu-id="68e05-114">Nelle build di debug questa funzione restituisce sempre la stringa, indipendentemente dai livelli di output di debug correnti.</span><span class="sxs-lookup"><span data-stu-id="68e05-114">In debug builds, this function always outputs the string, regardless of the current debug output levels.</span></span> <span data-ttu-id="68e05-115">Per un controllo più preciso sull'output, usare la macro [**DbgLog**](dbglog.md) .</span><span class="sxs-lookup"><span data-stu-id="68e05-115">For finer control over the output, use the [**DbgLog**](dbglog.md) macro.</span></span>

## <a name="examples"></a><span data-ttu-id="68e05-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="68e05-116">Examples</span></span>


```C++
DbgOutString("Creating the filter graph...\n"); 
```



## <a name="requirements"></a><span data-ttu-id="68e05-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="68e05-117">Requirements</span></span>



| <span data-ttu-id="68e05-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="68e05-118">Requirement</span></span> | <span data-ttu-id="68e05-119">Valore</span><span class="sxs-lookup"><span data-stu-id="68e05-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68e05-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="68e05-120">Header</span></span><br/>  | <dl> <span data-ttu-id="68e05-121"><dt>Wxdebug. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="68e05-121"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="68e05-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="68e05-122">Library</span></span><br/> | <dl> <span data-ttu-id="68e05-123"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="68e05-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68e05-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="68e05-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68e05-125">Funzioni di output di debug</span><span class="sxs-lookup"><span data-stu-id="68e05-125">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




