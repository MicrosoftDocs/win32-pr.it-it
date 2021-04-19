---
description: 'Il metodo setime imposta il flusso di tempo quando questo esempio deve iniziare e terminare. Questo metodo implementa il metodo IMediaSample:: setime.'
ms.assetid: cab4907f-eb6f-4444-9b41-1f95a6ecffed
title: Metodo CMediaSample. setime (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 935c4f3aa565b291e459d36e067805944b4fd6b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324024"
---
# <a name="cmediasamplesettime-method"></a><span data-ttu-id="e1058-104">CMediaSample. setime (metodo)</span><span class="sxs-lookup"><span data-stu-id="e1058-104">CMediaSample.SetTime method</span></span>

<span data-ttu-id="e1058-105">Il `SetTime` metodo imposta il flusso di tempo quando questo esempio deve iniziare e terminare.</span><span class="sxs-lookup"><span data-stu-id="e1058-105">The `SetTime` method sets the stream times when this sample should begin and finish.</span></span> <span data-ttu-id="e1058-106">Questo metodo implementa il metodo [**IMediaSample:: setime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) .</span><span class="sxs-lookup"><span data-stu-id="e1058-106">This method implements the [**IMediaSample::SetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1058-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e1058-107">Syntax</span></span>


```C++
HRESULT SetTime(
   REFERENCE_TIME *pTimeStart,
   REFERENCE_TIME *pTimeEnd
);
```



## <a name="parameters"></a><span data-ttu-id="e1058-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e1058-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1058-109">*pTimeStart*</span><span class="sxs-lookup"><span data-stu-id="e1058-109">*pTimeStart*</span></span> 
</dt> <dd>

<span data-ttu-id="e1058-110">Puntatore all'ora del flusso in cui inizia l'esempio, in unità di 100 nanosecondi o **null**.</span><span class="sxs-lookup"><span data-stu-id="e1058-110">Pointer to the stream time at which the sample begins, in 100-nanosecond units, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e1058-111">*pTimeEnd*</span><span class="sxs-lookup"><span data-stu-id="e1058-111">*pTimeEnd*</span></span> 
</dt> <dd>

<span data-ttu-id="e1058-112">Puntatore all'ora del flusso in cui termina il campione, in unità di 100 nanosecondi o **null**.</span><span class="sxs-lookup"><span data-stu-id="e1058-112">Pointer to the stream time at which the sample ends, in 100-nanosecond units, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1058-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e1058-113">Return value</span></span>

<span data-ttu-id="e1058-114">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e1058-114">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1058-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="e1058-115">Remarks</span></span>

<span data-ttu-id="e1058-116">Questo metodo imposta le variabili membro End [**CMediaSample:: m \_ Start**](cmediasample-m-start.md) e [**CMediaSample \_ :: m**](cmediasample-m-end.md) , che specificano i timestamp.</span><span class="sxs-lookup"><span data-stu-id="e1058-116">This method sets the [**CMediaSample::m\_Start**](cmediasample-m-start.md) and [**CMediaSample::m\_End**](cmediasample-m-end.md) member variables, which specify the time stamps.</span></span> <span data-ttu-id="e1058-117">Viene inoltre aggiornata la variabile membro [**\_ dwFlags CMediaSample:: m**](cmediasample-m-dwflags.md) , che specifica se i timestamp sono validi.</span><span class="sxs-lookup"><span data-stu-id="e1058-117">It also updates the [**CMediaSample::m\_dwFlags**](cmediasample-m-dwflags.md) member variable, which specifies whether the time stamps are valid.</span></span>

<span data-ttu-id="e1058-118">Per informazioni sui timestamp, vedere [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="e1058-118">For information about time stamps, see [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e1058-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e1058-119">Requirements</span></span>



| <span data-ttu-id="e1058-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1058-120">Requirement</span></span> | <span data-ttu-id="e1058-121">Valore</span><span class="sxs-lookup"><span data-stu-id="e1058-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1058-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e1058-122">Header</span></span><br/>  | <dl> <span data-ttu-id="e1058-123"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e1058-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e1058-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="e1058-124">Library</span></span><br/> | <dl> <span data-ttu-id="e1058-125"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e1058-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1058-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e1058-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1058-127">**Classe CMediaSample**</span><span class="sxs-lookup"><span data-stu-id="e1058-127">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




