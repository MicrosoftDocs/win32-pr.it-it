---
description: "Il metodo getTime recupera l'ora di riferimento corrente. Questo metodo implementa il metodo IReferenceClock:: GetTime."
ms.assetid: 4e4e5954-b899-4741-8b7c-7bc98a3f0404
title: Metodo CBaseReferenceClock. getTime (Refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.GetTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a91f0015756d2ccfb545c4039d67434eb6d3c403
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332227"
---
# <a name="cbasereferenceclockgettime-method"></a><span data-ttu-id="053c1-104">CBaseReferenceClock. getTime, metodo</span><span class="sxs-lookup"><span data-stu-id="053c1-104">CBaseReferenceClock.GetTime method</span></span>

<span data-ttu-id="053c1-105">Il `GetTime` metodo recupera l'ora di riferimento corrente.</span><span class="sxs-lookup"><span data-stu-id="053c1-105">The `GetTime` method retrieves the current reference time.</span></span> <span data-ttu-id="053c1-106">Questo metodo implementa il metodo [**IReferenceClock:: GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) .</span><span class="sxs-lookup"><span data-stu-id="053c1-106">This method implements the [**IReferenceClock::GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="053c1-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="053c1-107">Syntax</span></span>


```C++
HRESULT GetTime(
   REFERENCE_TIME *pTime
);
```



## <a name="parameters"></a><span data-ttu-id="053c1-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="053c1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="053c1-109">*pTime*</span><span class="sxs-lookup"><span data-stu-id="053c1-109">*pTime*</span></span> 
</dt> <dd>

<span data-ttu-id="053c1-110">Puntatore a una variabile che riceve l'ora corrente, in unità di 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="053c1-110">Pointer to a variable that receives the current time, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="053c1-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="053c1-111">Return value</span></span>

<span data-ttu-id="053c1-112">Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="053c1-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="053c1-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="053c1-113">Return code</span></span>                                                                               | <span data-ttu-id="053c1-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="053c1-114">Description</span></span>                                                 |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="053c1-115"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="053c1-115"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="053c1-116">Argomento puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="053c1-116">**NULL** pointer argument.</span></span><br/>                       |
| <dl> <span data-ttu-id="053c1-117"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="053c1-117"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="053c1-118">L'ora restituita è uguale a quella del valore precedente.</span><span class="sxs-lookup"><span data-stu-id="053c1-118">Returned time is the same as the previous value.</span></span><br/> |
| <dl> <span data-ttu-id="053c1-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="053c1-119"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="053c1-120">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="053c1-120">Success.</span></span><br/>                                         |



 

## <a name="remarks"></a><span data-ttu-id="053c1-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="053c1-121">Remarks</span></span>

<span data-ttu-id="053c1-122">Questo metodo chiama il metodo [**CBaseReferenceClock:: GetPrivateTime**](cbasereferenceclock-getprivatetime.md) per determinare l'ora reale del clock.</span><span class="sxs-lookup"><span data-stu-id="053c1-122">This method calls the [**CBaseReferenceClock::GetPrivateTime**](cbasereferenceclock-getprivatetime.md) method to determine the real clock time.</span></span> <span data-ttu-id="053c1-123">Se l'ora dell'orologio è rigorosamente maggiore del valore precedente, `GetTime` Usa l'ora di clock e restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="053c1-123">If the clock time is strictly greater than the previous value, `GetTime` uses the clock time and returns S\_OK.</span></span> <span data-ttu-id="053c1-124">In caso contrario, `GetTime` Usa il valore precedente e restituisce \_ false.</span><span class="sxs-lookup"><span data-stu-id="053c1-124">Otherwise, `GetTime` uses the previous value and returns S\_FALSE.</span></span> <span data-ttu-id="053c1-125">Pertanto, il clock interno può essere eseguito all'indietro per un breve periodo di tempo, senza comportare l'esecuzione precedente dell'ora di riferimento.</span><span class="sxs-lookup"><span data-stu-id="053c1-125">Therefore, the internal clock can run backward for a short period, without causing the reference time to run backward.</span></span> <span data-ttu-id="053c1-126">Al contrario, l'ora di riferimento si "blocca" con lo stesso valore fino a quando l'orologio interno non viene ripreso.</span><span class="sxs-lookup"><span data-stu-id="053c1-126">Instead, the reference time will "stall" at the same value until the internal clock catches up.</span></span>

## <a name="requirements"></a><span data-ttu-id="053c1-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="053c1-127">Requirements</span></span>



| <span data-ttu-id="053c1-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="053c1-128">Requirement</span></span> | <span data-ttu-id="053c1-129">Valore</span><span class="sxs-lookup"><span data-stu-id="053c1-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="053c1-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="053c1-130">Header</span></span><br/>  | <dl> <span data-ttu-id="053c1-131"><dt>Refclock. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="053c1-131"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="053c1-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="053c1-132">Library</span></span><br/> | <dl> <span data-ttu-id="053c1-133"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="053c1-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="053c1-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="053c1-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="053c1-135">**Classe CBaseReferenceClock**</span><span class="sxs-lookup"><span data-stu-id="053c1-135">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




