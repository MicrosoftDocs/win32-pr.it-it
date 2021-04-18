---
description: 'Il metodo SetMediaTime imposta i tempi dei supporti per questo esempio. Questo metodo implementa il metodo IMediaSample:: SetMediaTime.'
ms.assetid: 768812f8-c044-4499-9149-7c334c51e539
title: Metodo CMediaSample. SetMediaTime (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0240ef40f4c37f6c5528c979b2e89b43b03b3451
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325308"
---
# <a name="cmediasamplesetmediatime-method"></a><span data-ttu-id="6fef5-104">CMediaSample. SetMediaTime, metodo</span><span class="sxs-lookup"><span data-stu-id="6fef5-104">CMediaSample.SetMediaTime method</span></span>

<span data-ttu-id="6fef5-105">Il `SetMediaTime` metodo imposta i tempi dei supporti per questo esempio.</span><span class="sxs-lookup"><span data-stu-id="6fef5-105">The `SetMediaTime` method sets the media times for this sample.</span></span> <span data-ttu-id="6fef5-106">Questo metodo implementa il metodo [**IMediaSample:: SetMediaTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatime) .</span><span class="sxs-lookup"><span data-stu-id="6fef5-106">This method implements the [**IMediaSample::SetMediaTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatime) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fef5-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6fef5-107">Syntax</span></span>


```C++
HRESULT SetMediaTime(
   LONGLONG *pStart,
   LONGLONG *pEnd
);
```



## <a name="parameters"></a><span data-ttu-id="6fef5-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="6fef5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6fef5-109">*pStart*</span><span class="sxs-lookup"><span data-stu-id="6fef5-109">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="6fef5-110">Puntatore all'ora di inizio del supporto o **null**.</span><span class="sxs-lookup"><span data-stu-id="6fef5-110">Pointer to the media start time, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="6fef5-111">*Sospendere*</span><span class="sxs-lookup"><span data-stu-id="6fef5-111">*pEnd*</span></span> 
</dt> <dd>

<span data-ttu-id="6fef5-112">Puntatore all'ora di arresto del supporto o **null**.</span><span class="sxs-lookup"><span data-stu-id="6fef5-112">Pointer to the media stop time, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6fef5-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6fef5-113">Return value</span></span>

<span data-ttu-id="6fef5-114">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6fef5-114">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="6fef5-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="6fef5-115">Remarks</span></span>

<span data-ttu-id="6fef5-116">L'ora di arresto del supporto deve essere maggiore dell'ora di inizio del supporto.</span><span class="sxs-lookup"><span data-stu-id="6fef5-116">The media stop time must be greater than the media start time.</span></span> <span data-ttu-id="6fef5-117">Usare **null** per invalidare i tempi dei supporti.</span><span class="sxs-lookup"><span data-stu-id="6fef5-117">Use **NULL** to invalidate the media times.</span></span>

<span data-ttu-id="6fef5-118">Il parametro *Pending* specifica un'ora assoluta dei supporti, ma la variabile membro [**CMediaSample:: m \_ MediaEnd**](cmediasample-m-mediaend.md) viene calcolata come offset da *PStart*.</span><span class="sxs-lookup"><span data-stu-id="6fef5-118">The *pEnd* parameter specifies an absolute media time, but the [**CMediaSample::m\_MediaEnd**](cmediasample-m-mediaend.md) member variable is calculated as an offset from *pStart*.</span></span> <span data-ttu-id="6fef5-119">In altre parole, **m \_ MediaEnd**  =  \* *pTimeEnd* \* *pTimeStart*.  </span><span class="sxs-lookup"><span data-stu-id="6fef5-119">In other words, **m\_MediaEnd** = \**pTimeEnd*  \**pTimeStart*.</span></span>

<span data-ttu-id="6fef5-120">Per informazioni sui tempi dei supporti, vedere [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="6fef5-120">For information about media times, see [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6fef5-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6fef5-121">Requirements</span></span>



| <span data-ttu-id="6fef5-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="6fef5-122">Requirement</span></span> | <span data-ttu-id="6fef5-123">Valore</span><span class="sxs-lookup"><span data-stu-id="6fef5-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6fef5-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6fef5-124">Header</span></span><br/>  | <dl> <span data-ttu-id="6fef5-125"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6fef5-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="6fef5-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="6fef5-126">Library</span></span><br/> | <dl> <span data-ttu-id="6fef5-127"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="6fef5-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6fef5-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6fef5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fef5-129">**Classe CMediaSample**</span><span class="sxs-lookup"><span data-stu-id="6fef5-129">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




