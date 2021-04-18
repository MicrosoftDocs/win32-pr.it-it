---
description: "Il metodo getTime recupera le ore del flusso in cui l'esempio deve iniziare e terminare. Questo metodo implementa il metodo IMediaSample:: GetTime."
ms.assetid: ddb0df1c-707d-405d-9e73-0d5a59f487b6
title: Metodo CMediaSample. getTime (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8ff2035ede3e49feb2bc14a7aa31cfc18f2e7d23
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324958"
---
# <a name="cmediasamplegettime-method"></a><span data-ttu-id="ce7f0-104">CMediaSample. getTime, metodo</span><span class="sxs-lookup"><span data-stu-id="ce7f0-104">CMediaSample.GetTime method</span></span>

<span data-ttu-id="ce7f0-105">Il `GetTime` metodo recupera l'ora del flusso in cui l'esempio deve iniziare e terminare.</span><span class="sxs-lookup"><span data-stu-id="ce7f0-105">The `GetTime` method retrieves the stream times at which this sample should begin and finish.</span></span> <span data-ttu-id="ce7f0-106">Questo metodo implementa il metodo [**IMediaSample:: GetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-gettime) .</span><span class="sxs-lookup"><span data-stu-id="ce7f0-106">This method implements the [**IMediaSample::GetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-gettime) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce7f0-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ce7f0-107">Syntax</span></span>


```C++
HRESULT GetTime(
   REFERENCE_TIME *pTimeStart,
   REFERENCE_TIME *pTimeEnd
);
```



## <a name="parameters"></a><span data-ttu-id="ce7f0-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ce7f0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce7f0-109">*pTimeStart*</span><span class="sxs-lookup"><span data-stu-id="ce7f0-109">*pTimeStart*</span></span> 
</dt> <dd>

<span data-ttu-id="ce7f0-110">Puntatore a una variabile che riceve l'ora di inizio del flusso, in unità di 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="ce7f0-110">Pointer to a variable that receives the beginning stream time, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="ce7f0-111">*pTimeEnd*</span><span class="sxs-lookup"><span data-stu-id="ce7f0-111">*pTimeEnd*</span></span> 
</dt> <dd>

<span data-ttu-id="ce7f0-112">Puntatore a una variabile che riceve l'ora del flusso finale, in unità di 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="ce7f0-112">Pointer to a variable that receives the ending stream time, in 100-nanosecond units.</span></span> <span data-ttu-id="ce7f0-113">Se l'esempio non ha tempo di arresto, il valore viene impostato sull'ora di inizio più uno.</span><span class="sxs-lookup"><span data-stu-id="ce7f0-113">If the sample has no stop time, the value is set to the start time plus one.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce7f0-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ce7f0-114">Return value</span></span>

<span data-ttu-id="ce7f0-115">Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="ce7f0-115">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="ce7f0-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="ce7f0-116">Return code</span></span>                                                                                                   | <span data-ttu-id="ce7f0-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ce7f0-117">Description</span></span>                                                 |
|---------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="ce7f0-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ce7f0-118"><dt>**S\_OK**</dt></span></span> </dl>                          | <span data-ttu-id="ce7f0-119">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="ce7f0-119">Success.</span></span><br/>                                         |
| <dl> <span data-ttu-id="ce7f0-120"><dt>**\_ \_ nessun tempo di \_ arresto \_ per il VFW**</dt></span><span class="sxs-lookup"><span data-stu-id="ce7f0-120"><dt>**VFW\_S\_NO\_STOP\_TIME**</dt></span></span> </dl>         | <span data-ttu-id="ce7f0-121">L'esempio ha un'ora di inizio valida, ma nessuna ora di arresto.</span><span class="sxs-lookup"><span data-stu-id="ce7f0-121">Sample has a valid start time, but no stop time.</span></span><br/> |
| <dl> <span data-ttu-id="ce7f0-122"><dt>**tempo di esempio di VFW \_ E \_ \_ \_ non \_ impostato**</dt></span><span class="sxs-lookup"><span data-stu-id="ce7f0-122"><dt>**VFW\_E\_SAMPLE\_TIME\_NOT\_SET**</dt></span></span> </dl> | <span data-ttu-id="ce7f0-123">L'esempio non dispone di timestamp validi.</span><span class="sxs-lookup"><span data-stu-id="ce7f0-123">Sample does not have valid time stamps.</span></span><br/>          |



 

## <a name="remarks"></a><span data-ttu-id="ce7f0-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="ce7f0-124">Remarks</span></span>

<span data-ttu-id="ce7f0-125">Le variabili membro End [**CMediaSample:: m \_ Start**](cmediasample-m-start.md) e [**CMediaSample \_ :: m**](cmediasample-m-end.md) specificano i timestamp.</span><span class="sxs-lookup"><span data-stu-id="ce7f0-125">The [**CMediaSample::m\_Start**](cmediasample-m-start.md) and [**CMediaSample::m\_End**](cmediasample-m-end.md) member variables specify the time stamps.</span></span> <span data-ttu-id="ce7f0-126">La variabile membro [**\_ dwFlags CMediaSample:: m**](cmediasample-m-dwflags.md) specifica se i timestamp sono validi.</span><span class="sxs-lookup"><span data-stu-id="ce7f0-126">The [**CMediaSample::m\_dwFlags**](cmediasample-m-dwflags.md) member variable specifies whether the time stamps are valid.</span></span>

<span data-ttu-id="ce7f0-127">Per informazioni sui timestamp, vedere [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="ce7f0-127">For information about time stamps, see [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ce7f0-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ce7f0-128">Requirements</span></span>



| <span data-ttu-id="ce7f0-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce7f0-129">Requirement</span></span> | <span data-ttu-id="ce7f0-130">Valore</span><span class="sxs-lookup"><span data-stu-id="ce7f0-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce7f0-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ce7f0-131">Header</span></span><br/>  | <dl> <span data-ttu-id="ce7f0-132"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ce7f0-132"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ce7f0-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="ce7f0-133">Library</span></span><br/> | <dl> <span data-ttu-id="ce7f0-134"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ce7f0-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce7f0-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ce7f0-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce7f0-136">**Classe CMediaSample**</span><span class="sxs-lookup"><span data-stu-id="ce7f0-136">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




