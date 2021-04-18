---
description: La funzione ConvertToMilliseconds converte un tempo di riferimento in millisecondi.
ms.assetid: fae3baa4-9344-4197-b375-4abe2656e1b7
title: Funzione ConvertToMilliseconds (Refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConvertToMilliseconds
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 066f50856824a9bc7b5bbb8c4918c7cbfe5b9da5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327442"
---
# <a name="converttomilliseconds-function"></a><span data-ttu-id="f4a1a-103">ConvertToMilliseconds (funzione)</span><span class="sxs-lookup"><span data-stu-id="f4a1a-103">ConvertToMilliseconds function</span></span>

<span data-ttu-id="f4a1a-104">La `ConvertToMilliseconds` funzione converte un'ora di riferimento in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="f4a1a-104">The `ConvertToMilliseconds` function converts a reference time to milliseconds.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4a1a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f4a1a-105">Syntax</span></span>


```C++
LONGLONG ConvertToMilliseconds(
   const REFERENCE_TIME &RT
);
```



## <a name="parameters"></a><span data-ttu-id="f4a1a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f4a1a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4a1a-107">*RT* \[ Ref\]</span><span class="sxs-lookup"><span data-stu-id="f4a1a-107">*RT* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="f4a1a-108">Tempo di riferimento, in unità di 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="f4a1a-108">Reference time, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4a1a-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f4a1a-109">Return value</span></span>

<span data-ttu-id="f4a1a-110">Restituisce l'ora di riferimento convertita in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="f4a1a-110">Returns the reference time converted to milliseconds.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4a1a-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f4a1a-111">Requirements</span></span>



| <span data-ttu-id="f4a1a-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4a1a-112">Requirement</span></span> | <span data-ttu-id="f4a1a-113">Valore</span><span class="sxs-lookup"><span data-stu-id="f4a1a-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4a1a-114">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f4a1a-114">Header</span></span><br/>  | <dl> <span data-ttu-id="f4a1a-115"><dt>Refclock. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f4a1a-115"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f4a1a-116">Libreria</span><span class="sxs-lookup"><span data-stu-id="f4a1a-116">Library</span></span><br/> | <dl> <span data-ttu-id="f4a1a-117"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f4a1a-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4a1a-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f4a1a-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4a1a-119">**Classe CBaseReferenceClock**</span><span class="sxs-lookup"><span data-stu-id="f4a1a-119">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




