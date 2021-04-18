---
description: "Il metodo SetClockDelta regola l'ora dell'orologio. Questo metodo implementa il metodo IAMClockAdjust:: SetClockDelta."
ms.assetid: 2bb9266f-3866-4b2e-92a8-cde31a501047
title: Metodo CSystemClock. SetClockDelta (Sysclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSystemClock.SetClockDelta
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cc1027081cc8713cffd2979e20627c037d0799f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324467"
---
# <a name="csystemclocksetclockdelta-method"></a><span data-ttu-id="be511-104">CSystemClock. SetClockDelta, metodo</span><span class="sxs-lookup"><span data-stu-id="be511-104">CSystemClock.SetClockDelta method</span></span>

<span data-ttu-id="be511-105">Il `SetClockDelta` metodo regola l'ora dell'orologio.</span><span class="sxs-lookup"><span data-stu-id="be511-105">The `SetClockDelta` method adjusts the clock time.</span></span> <span data-ttu-id="be511-106">Questo metodo implementa il metodo [**IAMClockAdjust:: SetClockDelta**](/windows/desktop/api/Strmif/nf-strmif-iamclockadjust-setclockdelta) .</span><span class="sxs-lookup"><span data-stu-id="be511-106">This method implements the [**IAMClockAdjust::SetClockDelta**](/windows/desktop/api/Strmif/nf-strmif-iamclockadjust-setclockdelta) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="be511-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="be511-107">Syntax</span></span>


```C++
HRESULT SetClockDelta(
   REFERENCE_TIME rtDelta
);
```



## <a name="parameters"></a><span data-ttu-id="be511-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="be511-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be511-109">*rtDelta*</span><span class="sxs-lookup"><span data-stu-id="be511-109">*rtDelta*</span></span> 
</dt> <dd>

<span data-ttu-id="be511-110">Specifica la quantità in base alla quale impostare l'orologio come valore [**di \_ ora di riferimento**](reference-time.md) .</span><span class="sxs-lookup"><span data-stu-id="be511-110">Specifies the amount by which to adjust the clock, as a [**REFERENCE\_TIME**](reference-time.md) value.</span></span> <span data-ttu-id="be511-111">Un valore positivo consente di spostare l'orologio avanti e un valore negativo consente di spostare l'orologio indietro.</span><span class="sxs-lookup"><span data-stu-id="be511-111">A positive value moves the clock forward, and a negative value moves the clock backward.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be511-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="be511-112">Return value</span></span>

<span data-ttu-id="be511-113">Restituisce \_ OK o un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="be511-113">Returns S\_OK or an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="be511-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="be511-114">Remarks</span></span>

<span data-ttu-id="be511-115">Questo metodo chiama semplicemente [**CBaseReferenceClock:: SetTimeDelta**](cbasereferenceclock-settimedelta.md).</span><span class="sxs-lookup"><span data-stu-id="be511-115">This method simply calls [**CBaseReferenceClock::SetTimeDelta**](cbasereferenceclock-settimedelta.md).</span></span>

<span data-ttu-id="be511-116">I valori dell'ora restituiti da [**IReferenceClock:: GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) sono a incremento progressivo costante.</span><span class="sxs-lookup"><span data-stu-id="be511-116">The time values returned by [**IReferenceClock::GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) are monotonically increasing.</span></span> <span data-ttu-id="be511-117">Se si imposta il clock indietro, **getTime** continua a segnalare l'ora precedente fino a quando l'orologio interno non viene aggiornato.</span><span class="sxs-lookup"><span data-stu-id="be511-117">If you set the clock back, **GetTime** continues to report the old time until the internal clock catches up.</span></span>

## <a name="requirements"></a><span data-ttu-id="be511-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="be511-118">Requirements</span></span>



| <span data-ttu-id="be511-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="be511-119">Requirement</span></span> | <span data-ttu-id="be511-120">Valore</span><span class="sxs-lookup"><span data-stu-id="be511-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be511-121">Versione</span><span class="sxs-lookup"><span data-stu-id="be511-121">Version</span></span><br/> | <span data-ttu-id="be511-122">Classe CSystemClock</span><span class="sxs-lookup"><span data-stu-id="be511-122">CSystemClock Class</span></span><br/>                                                                                                                                                              |
| <span data-ttu-id="be511-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="be511-123">Header</span></span><br/>  | <dl> <span data-ttu-id="be511-124"><dt>Sysclock. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="be511-124"><dt>Sysclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="be511-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="be511-125">Library</span></span><br/> | <dl> <span data-ttu-id="be511-126"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="be511-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




