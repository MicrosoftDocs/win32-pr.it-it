---
description: 'Il metodo GetMediaTime recupera i tempi dei supporti per questo esempio. Questo metodo implementa il metodo IMediaSample:: GetMediaTime.'
ms.assetid: f58a2162-5764-48f2-8984-ee4bba1229ab
title: Metodo CMediaSample. GetMediaTime (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f9a41d29e46d29cff9023421a661cc90731d4c06
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326406"
---
# <a name="cmediasamplegetmediatime-method"></a><span data-ttu-id="bd9f8-104">CMediaSample. GetMediaTime, metodo</span><span class="sxs-lookup"><span data-stu-id="bd9f8-104">CMediaSample.GetMediaTime method</span></span>

<span data-ttu-id="bd9f8-105">Il `GetMediaTime` metodo recupera i tempi di supporto per questo esempio.</span><span class="sxs-lookup"><span data-stu-id="bd9f8-105">The `GetMediaTime` method retrieves the media times for this sample.</span></span> <span data-ttu-id="bd9f8-106">Questo metodo implementa il metodo [**IMediaSample:: GetMediaTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatime) .</span><span class="sxs-lookup"><span data-stu-id="bd9f8-106">This method implements the [**IMediaSample::GetMediaTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatime) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd9f8-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bd9f8-107">Syntax</span></span>


```C++
HRESULT GetMediaTime(
   LONGLONG *pStart,
   LONGLONG *pEnd
);
```



## <a name="parameters"></a><span data-ttu-id="bd9f8-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="bd9f8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd9f8-109">*pStart*</span><span class="sxs-lookup"><span data-stu-id="bd9f8-109">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="bd9f8-110">Puntatore a una variabile che riceve l'ora di inizio del supporto.</span><span class="sxs-lookup"><span data-stu-id="bd9f8-110">Pointer to a variable that receives the media start time.</span></span>

</dd> <dt>

<span data-ttu-id="bd9f8-111">*Sospendere*</span><span class="sxs-lookup"><span data-stu-id="bd9f8-111">*pEnd*</span></span> 
</dt> <dd>

<span data-ttu-id="bd9f8-112">Puntatore a una variabile che riceve l'ora di arresto del supporto.</span><span class="sxs-lookup"><span data-stu-id="bd9f8-112">Pointer to a variable that receives the media stop time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd9f8-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bd9f8-113">Return value</span></span>

<span data-ttu-id="bd9f8-114">Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="bd9f8-114">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="bd9f8-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="bd9f8-115">Return code</span></span>                                                                                                  | <span data-ttu-id="bd9f8-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bd9f8-116">Description</span></span>                                         |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="bd9f8-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="bd9f8-117"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="bd9f8-118">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="bd9f8-118">Success.</span></span><br/>                                 |
| <dl> <span data-ttu-id="bd9f8-119"><dt>**\_ \_ tempo medio E \_ \_ non \_ impostato per VFW**</dt></span><span class="sxs-lookup"><span data-stu-id="bd9f8-119"><dt>**VFW\_E\_MEDIA\_TIME\_NOT\_SET**</dt></span></span> </dl> | <span data-ttu-id="bd9f8-120">Non sono stati impostati tempi multimediali per questo esempio.</span><span class="sxs-lookup"><span data-stu-id="bd9f8-120">No media times were set for this sample.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="bd9f8-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="bd9f8-121">Remarks</span></span>

<span data-ttu-id="bd9f8-122">La variabile membro [**CMediaSample:: m \_ MediaEnd**](cmediasample-m-mediaend.md) specifica un offset da [**CMediaSample:: m \_ MediaStart**](cmediasample-m-mediastart.md), ma il valore ricevuto dal parametro *Pending* è un tempo di supporto assoluto, calcolato come **m \_ MediaStart**  +  **m \_ MediaEnd**.</span><span class="sxs-lookup"><span data-stu-id="bd9f8-122">The [**CMediaSample::m\_MediaEnd**](cmediasample-m-mediaend.md) member variable specifies an offset from [**CMediaSample::m\_MediaStart**](cmediasample-m-mediastart.md), but the value received by the *pEnd* parameter is an absolute media time, calculated as **m\_MediaStart** + **m\_MediaEnd**.</span></span>

<span data-ttu-id="bd9f8-123">Per informazioni sui tempi dei supporti, vedere [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="bd9f8-123">For information about media times, see [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bd9f8-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bd9f8-124">Requirements</span></span>



| <span data-ttu-id="bd9f8-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd9f8-125">Requirement</span></span> | <span data-ttu-id="bd9f8-126">Valore</span><span class="sxs-lookup"><span data-stu-id="bd9f8-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd9f8-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bd9f8-127">Header</span></span><br/>  | <dl> <span data-ttu-id="bd9f8-128"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bd9f8-128"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="bd9f8-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="bd9f8-129">Library</span></span><br/> | <dl> <span data-ttu-id="bd9f8-130"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="bd9f8-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd9f8-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bd9f8-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd9f8-132">**Classe CMediaSample**</span><span class="sxs-lookup"><span data-stu-id="bd9f8-132">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




