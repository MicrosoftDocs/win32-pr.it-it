---
description: Imposta il valore di timeout del debug. Ignorato nelle compilazioni al dettaglio.
ms.assetid: d0f60d8b-34f2-44b2-bdd6-5e8e6f7806d8
title: Funzione DbgSetWaitTimeout (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgSetWaitTimeout
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5805112b19132045e0245ef7baf29cb5c844e290
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326660"
---
# <a name="dbgsetwaittimeout-function"></a><span data-ttu-id="fc8bc-104">DbgSetWaitTimeout (funzione)</span><span class="sxs-lookup"><span data-stu-id="fc8bc-104">DbgSetWaitTimeout function</span></span>

<span data-ttu-id="fc8bc-105">Imposta il valore di timeout del debug.</span><span class="sxs-lookup"><span data-stu-id="fc8bc-105">Sets the debugging time-out value.</span></span> <span data-ttu-id="fc8bc-106">Ignorato nelle compilazioni al dettaglio.</span><span class="sxs-lookup"><span data-stu-id="fc8bc-106">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc8bc-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fc8bc-107">Syntax</span></span>


```C++
void DbgSetWaitTimeout(
   DWORD dwTimeout
);
```



## <a name="parameters"></a><span data-ttu-id="fc8bc-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="fc8bc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc8bc-109">*dwTimeout*</span><span class="sxs-lookup"><span data-stu-id="fc8bc-109">*dwTimeout*</span></span> 
</dt> <dd>

<span data-ttu-id="fc8bc-110">Valore di timeout in millisecondi o infinito per un'attesa indefinita.</span><span class="sxs-lookup"><span data-stu-id="fc8bc-110">Time-out value in milliseconds, or INFINITE to wait indefinitely.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc8bc-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fc8bc-111">Return value</span></span>

<span data-ttu-id="fc8bc-112">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="fc8bc-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc8bc-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="fc8bc-113">Remarks</span></span>

<span data-ttu-id="fc8bc-114">Nelle build di debug, le funzioni [**DbgWaitForMultipleObjects**](dbgwaitformultipleobjects.md) e [**DbgWaitForSingleObject**](dbgwaitforsingleobject.md) usano questo valore come intervallo di timeout.</span><span class="sxs-lookup"><span data-stu-id="fc8bc-114">In debug builds, the [**DbgWaitForMultipleObjects**](dbgwaitformultipleobjects.md) and [**DbgWaitForSingleObject**](dbgwaitforsingleobject.md) functions use this value as the time-out interval.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc8bc-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fc8bc-115">Requirements</span></span>



| <span data-ttu-id="fc8bc-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc8bc-116">Requirement</span></span> | <span data-ttu-id="fc8bc-117">Valore</span><span class="sxs-lookup"><span data-stu-id="fc8bc-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc8bc-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fc8bc-118">Header</span></span><br/>  | <dl> <span data-ttu-id="fc8bc-119"><dt>Wxdebug. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fc8bc-119"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="fc8bc-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="fc8bc-120">Library</span></span><br/> | <dl> <span data-ttu-id="fc8bc-121"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="fc8bc-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc8bc-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fc8bc-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc8bc-123">Funzioni di debug di attesa</span><span class="sxs-lookup"><span data-stu-id="fc8bc-123">Wait Debugging Functions</span></span>](wait-debugging-functions.md)
</dt> </dl>

 

 




