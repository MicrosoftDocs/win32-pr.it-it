---
description: Il metodo StreamTime recupera l'ora del flusso corrente.
ms.assetid: 88a2939d-fb51-49fd-af71-21c99511de43
title: Metodo CBaseFilter. StreamTime (Amfilter. h)
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
ms.openlocfilehash: f4370758eb4ab15a9e53a5157550ee2129783c7f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331654"
---
# <a name="cbasefilterstreamtime-method"></a><span data-ttu-id="b4a61-103">CBaseFilter. StreamTime, metodo</span><span class="sxs-lookup"><span data-stu-id="b4a61-103">CBaseFilter.StreamTime method</span></span>

<span data-ttu-id="b4a61-104">Il metodo **StreamTime** recupera l'ora del flusso corrente.</span><span class="sxs-lookup"><span data-stu-id="b4a61-104">The **StreamTime** method retrieves the current stream time.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4a61-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b4a61-105">Syntax</span></span>


```C++
virtual HRESULT StreamTime(
  [ref] CRefTime &rtStream
);
```



## <a name="parameters"></a><span data-ttu-id="b4a61-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b4a61-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4a61-107">*rtStream* \[ Ref\]</span><span class="sxs-lookup"><span data-stu-id="b4a61-107">*rtStream* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="b4a61-108">Riferimento a un oggetto [**CRefTime**](creftime.md) che riceve l'ora del flusso corrente.</span><span class="sxs-lookup"><span data-stu-id="b4a61-108">Reference to a [**CRefTime**](creftime.md) object that receives the current stream time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4a61-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b4a61-109">Return value</span></span>

<span data-ttu-id="b4a61-110">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b4a61-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="b4a61-111">I valori possibili includono quelli elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="b4a61-111">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="b4a61-112">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="b4a61-112">Return code</span></span>                                                                                      | <span data-ttu-id="b4a61-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b4a61-113">Description</span></span>                                 |
|--------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="b4a61-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b4a61-114"><dt>**S\_OK**</dt></span></span> </dl>             | <span data-ttu-id="b4a61-115">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="b4a61-115">Success.</span></span><br/>                         |
| <dl> <span data-ttu-id="b4a61-116"><dt>**VFW \_ E \_ nessun \_ Clock**</dt></span><span class="sxs-lookup"><span data-stu-id="b4a61-116"><dt>**VFW\_E\_NO\_CLOCK**</dt></span></span> </dl> | <span data-ttu-id="b4a61-117">Nessun clock di riferimento disponibile.</span><span class="sxs-lookup"><span data-stu-id="b4a61-117">No reference clock is available.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b4a61-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="b4a61-118">Remarks</span></span>

<span data-ttu-id="b4a61-119">Il tempo di flusso viene definito come ora di riferimento corrente (come indicato dall'orologio di riferimento) meno l'ora di inizio (specificata da [**CBaseFilter:: m \_ tStart**](cbasefilter-m-tstart.md)).</span><span class="sxs-lookup"><span data-stu-id="b4a61-119">Stream time is defined as the current reference time (as given by the reference clock) minus the start time (specified by [**CBaseFilter::m\_tStart**](cbasefilter-m-tstart.md)).</span></span> <span data-ttu-id="b4a61-120">Il *timestamp* di un campione multimediale specifica l'ora del flusso in cui deve essere eseguito il rendering.</span><span class="sxs-lookup"><span data-stu-id="b4a61-120">A media sample's *time stamp* specifies the stream time when it should be rendered.</span></span> <span data-ttu-id="b4a61-121">Se non è ancora stato eseguito il rendering di un campione con un timestamp inferiore al tempo di flusso corrente, è in ritardo.</span><span class="sxs-lookup"><span data-stu-id="b4a61-121">If a sample with a time stamp less than the current stream time has not yet been rendered, it is late.</span></span>

<span data-ttu-id="b4a61-122">Questo metodo ottiene l'ora del flusso chiamando [**IReferenceClock:: GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) per ottenere l'ora di riferimento corrente e quindi sottraendo l'ora di inizio iniziale.</span><span class="sxs-lookup"><span data-stu-id="b4a61-122">This method gets the stream time by calling [**IReferenceClock::GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) to get the current reference time, and then subtracting the initial start time.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4a61-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b4a61-123">Requirements</span></span>



| <span data-ttu-id="b4a61-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4a61-124">Requirement</span></span> | <span data-ttu-id="b4a61-125">Valore</span><span class="sxs-lookup"><span data-stu-id="b4a61-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4a61-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b4a61-126">Header</span></span><br/>  | <dl> <span data-ttu-id="b4a61-127"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b4a61-127"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="b4a61-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="b4a61-128">Library</span></span><br/> | <dl> <span data-ttu-id="b4a61-129"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b4a61-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4a61-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b4a61-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4a61-131">Time and Clocks in DirectShow</span><span class="sxs-lookup"><span data-stu-id="b4a61-131">Time and Clocks in DirectShow</span></span>](time-and-clocks-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="b4a61-132">**Classe CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="b4a61-132">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




