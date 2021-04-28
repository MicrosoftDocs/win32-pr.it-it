---
description: "Metodo CBaseFilter.StreamTime: il metodo StreamTime recupera l'ora corrente del flusso."
ms.assetid: 88a2939d-fb51-49fd-af71-21c99511de43
title: Metodo CBaseFilter.StreamTime (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.StreamTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f3334ac273a733c3f0591b76af7e76460997a199
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108120069"
---
# <a name="cbasefilterstreamtime-method"></a><span data-ttu-id="16106-103">Metodo CBaseFilter.StreamTime</span><span class="sxs-lookup"><span data-stu-id="16106-103">CBaseFilter.StreamTime method</span></span>

<span data-ttu-id="16106-104">Il **metodo StreamTime** recupera l'ora corrente del flusso.</span><span class="sxs-lookup"><span data-stu-id="16106-104">The **StreamTime** method retrieves the current stream time.</span></span>

## <a name="syntax"></a><span data-ttu-id="16106-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="16106-105">Syntax</span></span>


```C++
virtual HRESULT StreamTime(
  [ref] CRefTime &rtStream
);
```



## <a name="parameters"></a><span data-ttu-id="16106-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="16106-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16106-107">*rtStream* \[ Ref\]</span><span class="sxs-lookup"><span data-stu-id="16106-107">*rtStream* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="16106-108">Riferimento a un [**oggetto CRefTime**](creftime.md) che riceve l'ora corrente del flusso.</span><span class="sxs-lookup"><span data-stu-id="16106-108">Reference to a [**CRefTime**](creftime.md) object that receives the current stream time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16106-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="16106-109">Return value</span></span>

<span data-ttu-id="16106-110">Restituisce un **valore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="16106-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="16106-111">I valori possibili includono quelli elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="16106-111">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="16106-112">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="16106-112">Return code</span></span>                                                                                      | <span data-ttu-id="16106-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="16106-113">Description</span></span>                                 |
|--------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="16106-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="16106-114"><dt>**S\_OK**</dt></span></span> </dl>             | <span data-ttu-id="16106-115">Operazione completata.</span><span class="sxs-lookup"><span data-stu-id="16106-115">Success.</span></span><br/>                         |
| <dl> <span data-ttu-id="16106-116"><dt>**VFW \_ E \_ NO \_ CLOCK**</dt></span><span class="sxs-lookup"><span data-stu-id="16106-116"><dt>**VFW\_E\_NO\_CLOCK**</dt></span></span> </dl> | <span data-ttu-id="16106-117">Non è disponibile alcun orologio di riferimento.</span><span class="sxs-lookup"><span data-stu-id="16106-117">No reference clock is available.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="16106-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="16106-118">Remarks</span></span>

<span data-ttu-id="16106-119">L'ora di flusso è definita come ora di riferimento corrente (come specificato dall'orologio di riferimento) meno l'ora di inizio (specificata da [**CBaseFilter::m \_ tStart**](cbasefilter-m-tstart.md)).</span><span class="sxs-lookup"><span data-stu-id="16106-119">Stream time is defined as the current reference time (as given by the reference clock) minus the start time (specified by [**CBaseFilter::m\_tStart**](cbasefilter-m-tstart.md)).</span></span> <span data-ttu-id="16106-120">Il timestamp di un campione *multimediale* specifica l'ora del flusso in cui deve essere eseguito il rendering.</span><span class="sxs-lookup"><span data-stu-id="16106-120">A media sample's *time stamp* specifies the stream time when it should be rendered.</span></span> <span data-ttu-id="16106-121">Se non è ancora stato eseguito il rendering di un esempio con timestamp inferiore all'ora corrente del flusso, è in ritardo.</span><span class="sxs-lookup"><span data-stu-id="16106-121">If a sample with a time stamp less than the current stream time has not yet been rendered, it is late.</span></span>

<span data-ttu-id="16106-122">Questo metodo ottiene l'ora del flusso chiamando [**IReferenceClock::GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) per ottenere l'ora di riferimento corrente e quindi sottraendo l'ora di inizio iniziale.</span><span class="sxs-lookup"><span data-stu-id="16106-122">This method gets the stream time by calling [**IReferenceClock::GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) to get the current reference time, and then subtracting the initial start time.</span></span>

## <a name="requirements"></a><span data-ttu-id="16106-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="16106-123">Requirements</span></span>



| <span data-ttu-id="16106-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="16106-124">Requirement</span></span> | <span data-ttu-id="16106-125">Valore</span><span class="sxs-lookup"><span data-stu-id="16106-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16106-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="16106-126">Header</span></span><br/>  | <dl> <span data-ttu-id="16106-127"><dt>Amfilter.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="16106-127"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="16106-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="16106-128">Library</span></span><br/> | <dl> <span data-ttu-id="16106-129"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="16106-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16106-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="16106-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16106-131">Ora e orologi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="16106-131">Time and Clocks in DirectShow</span></span>](time-and-clocks-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="16106-132">**Classe CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="16106-132">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




