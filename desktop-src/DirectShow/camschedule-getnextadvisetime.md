---
description: Il metodo GetNextAdviseTime recupera l'ora della successiva richiesta di notifica.
ms.assetid: 2a376250-fb39-46d7-a5a8-e3a3143cd209
title: Metodo CAMSchedule. GetNextAdviseTime (Dsschedule. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule.GetNextAdviseTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5894ae98666c9134abd4bce96922a5f28d5919b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329562"
---
# <a name="camschedulegetnextadvisetime-method"></a><span data-ttu-id="76ce9-103">CAMSchedule. GetNextAdviseTime, metodo</span><span class="sxs-lookup"><span data-stu-id="76ce9-103">CAMSchedule.GetNextAdviseTime method</span></span>

<span data-ttu-id="76ce9-104">Il `GetNextAdviseTime` metodo recupera l'ora della successiva richiesta di notifica.</span><span class="sxs-lookup"><span data-stu-id="76ce9-104">The `GetNextAdviseTime` method retrieves the time of the next advise request.</span></span>

## <a name="syntax"></a><span data-ttu-id="76ce9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="76ce9-105">Syntax</span></span>


```C++
REFERENCE_TIME GetNextAdviseTime();
```



## <a name="parameters"></a><span data-ttu-id="76ce9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="76ce9-106">Parameters</span></span>

<span data-ttu-id="76ce9-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="76ce9-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="76ce9-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="76ce9-108">Return value</span></span>

<span data-ttu-id="76ce9-109">Restituisce l'ora di riferimento della richiesta di notifica successiva o il tempo massimo in cui \_ non è pianificata alcuna richiesta.</span><span class="sxs-lookup"><span data-stu-id="76ce9-109">Returns the reference time of the next advise request, or MAX\_TIME no requests are scheduled.</span></span>

## <a name="requirements"></a><span data-ttu-id="76ce9-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="76ce9-110">Requirements</span></span>



| <span data-ttu-id="76ce9-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="76ce9-111">Requirement</span></span> | <span data-ttu-id="76ce9-112">Valore</span><span class="sxs-lookup"><span data-stu-id="76ce9-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76ce9-113">Intestazione</span><span class="sxs-lookup"><span data-stu-id="76ce9-113">Header</span></span><br/>  | <dl> <span data-ttu-id="76ce9-114"><dt>Dsschedule. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="76ce9-114"><dt>Dsschedule.h (include Streams.h)</dt></span></span> </dl>                                                                                |
| <span data-ttu-id="76ce9-115">Libreria</span><span class="sxs-lookup"><span data-stu-id="76ce9-115">Library</span></span><br/> | <dl> <span data-ttu-id="76ce9-116"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="76ce9-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76ce9-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="76ce9-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76ce9-118">**Classe CAMSchedule**</span><span class="sxs-lookup"><span data-stu-id="76ce9-118">**CAMSchedule Class**</span></span>](camschedule.md)
</dt> </dl>

 

 




