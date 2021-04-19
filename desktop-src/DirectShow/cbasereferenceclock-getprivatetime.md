---
description: Il metodo GetPrivateTime recupera l'ora reale dal clock.
ms.assetid: ce9832cb-4b5a-49a1-9a69-d2fb90b3ed2e
title: Metodo CBaseReferenceClock. GetPrivateTime (Refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.GetPrivateTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 387df10472e4913d33722492bf07601faf08e3ba
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332228"
---
# <a name="cbasereferenceclockgetprivatetime-method"></a><span data-ttu-id="e336e-103">CBaseReferenceClock. GetPrivateTime, metodo</span><span class="sxs-lookup"><span data-stu-id="e336e-103">CBaseReferenceClock.GetPrivateTime method</span></span>

<span data-ttu-id="e336e-104">Il `GetPrivateTime` metodo recupera il tempo reale dal clock.</span><span class="sxs-lookup"><span data-stu-id="e336e-104">The `GetPrivateTime` method retrieves the real time from the clock.</span></span>

## <a name="syntax"></a><span data-ttu-id="e336e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e336e-105">Syntax</span></span>


```C++
virtual REFERENCE_TIME GetPrivateTime();
```



## <a name="parameters"></a><span data-ttu-id="e336e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e336e-106">Parameters</span></span>

<span data-ttu-id="e336e-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="e336e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e336e-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e336e-108">Return value</span></span>

<span data-ttu-id="e336e-109">Restituisce l'ora dell'orologio corrente, in unità di 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="e336e-109">Returns the current clock time, in 100-nanosecond units.</span></span>

## <a name="remarks"></a><span data-ttu-id="e336e-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="e336e-110">Remarks</span></span>

<span data-ttu-id="e336e-111">Questo metodo restituisce il tempo reale segnalato dall'orologio.</span><span class="sxs-lookup"><span data-stu-id="e336e-111">This method returns the real time reported by the clock.</span></span> <span data-ttu-id="e336e-112">I chiamanti esterni usano il metodo [**CBaseReferenceClock:: GetTime**](cbasereferenceclock-gettime.md) , che chiama questo metodo.</span><span class="sxs-lookup"><span data-stu-id="e336e-112">External callers use the [**CBaseReferenceClock::GetTime**](cbasereferenceclock-gettime.md) method, which calls this method.</span></span> <span data-ttu-id="e336e-113">A differenza del metodo **getTime** , il clock interno può tornare indietro.</span><span class="sxs-lookup"><span data-stu-id="e336e-113">Unlike the **GetTime** method, the internal clock is allowed to go backward.</span></span> <span data-ttu-id="e336e-114">In tal caso, il metodo **getTime** continua a restituire l'ultima volta che ha segnalato, fino a quando il metodo non viene `GetPrivateTime` aggiornato.</span><span class="sxs-lookup"><span data-stu-id="e336e-114">If that happens, the **GetTime** method continues to return the last time that it reported, until the `GetPrivateTime` method catches up.</span></span>

<span data-ttu-id="e336e-115">Questo metodo restituisce l'ora di sistema.</span><span class="sxs-lookup"><span data-stu-id="e336e-115">This method returns the system time.</span></span> <span data-ttu-id="e336e-116">Eseguire l'override di questo metodo se l'orologio ottiene l'ora da un'altra origine.</span><span class="sxs-lookup"><span data-stu-id="e336e-116">Override this method if your clock gets the time from another source.</span></span>

## <a name="requirements"></a><span data-ttu-id="e336e-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e336e-117">Requirements</span></span>



| <span data-ttu-id="e336e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e336e-118">Requirement</span></span> | <span data-ttu-id="e336e-119">Valore</span><span class="sxs-lookup"><span data-stu-id="e336e-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e336e-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e336e-120">Header</span></span><br/>  | <dl> <span data-ttu-id="e336e-121"><dt>Refclock. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e336e-121"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e336e-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="e336e-122">Library</span></span><br/> | <dl> <span data-ttu-id="e336e-123"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e336e-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e336e-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e336e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e336e-125">**Classe CBaseReferenceClock**</span><span class="sxs-lookup"><span data-stu-id="e336e-125">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




