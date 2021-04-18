---
description: 'Il metodo Notify notifica al pin che è richiesta una modifica di qualità. Questo metodo implementa il metodo IQualityControl:: Notify.'
ms.assetid: 76124321-0d2d-4fee-a08a-4db23078e8df
title: Metodo CBaseInputPin. Notify (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.Notify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a5ae7ca47c5adc11c87a739e8736ba327dc0b65f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330939"
---
# <a name="cbaseinputpinnotify-method"></a><span data-ttu-id="8e4b2-104">Metodo CBaseInputPin. Notify</span><span class="sxs-lookup"><span data-stu-id="8e4b2-104">CBaseInputPin.Notify method</span></span>

<span data-ttu-id="8e4b2-105">Il `Notify` metodo notifica al pin che è richiesta una modifica di qualità.</span><span class="sxs-lookup"><span data-stu-id="8e4b2-105">The `Notify` method notifies the pin that a quality change is requested.</span></span> <span data-ttu-id="8e4b2-106">Questo metodo implementa il metodo [**IQualityControl:: Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) .</span><span class="sxs-lookup"><span data-stu-id="8e4b2-106">This method implements the [**IQualityControl::Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e4b2-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8e4b2-107">Syntax</span></span>


```C++
HRESULT Notify(
   IBaseFilter *pSelf,
   Quality     q
);
```



## <a name="parameters"></a><span data-ttu-id="8e4b2-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="8e4b2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e4b2-109">*pSelf*</span><span class="sxs-lookup"><span data-stu-id="8e4b2-109">*pSelf*</span></span> 
</dt> <dd>

<span data-ttu-id="8e4b2-110">Puntatore al filtro che sta inviando il messaggio di controllo di qualità.</span><span class="sxs-lookup"><span data-stu-id="8e4b2-110">Pointer to the filter that is sending the quality-control message.</span></span>

</dd> <dt>

<span data-ttu-id="8e4b2-111">*d*</span><span class="sxs-lookup"><span data-stu-id="8e4b2-111">*q*</span></span> 
</dt> <dd>

<span data-ttu-id="8e4b2-112">Struttura di [**qualità**](/windows/win32/api/strmif/ns-strmif-quality) che contiene il messaggio di controllo della qualità.</span><span class="sxs-lookup"><span data-stu-id="8e4b2-112">[**Quality**](/windows/win32/api/strmif/ns-strmif-quality) structure that contains the quality-control message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e4b2-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8e4b2-113">Return value</span></span>

<span data-ttu-id="8e4b2-114">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8e4b2-114">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e4b2-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="8e4b2-115">Remarks</span></span>

<span data-ttu-id="8e4b2-116">I filtri di solito passano messaggi di controllo della qualità a un pin di output upstream, non a un pin di input.</span><span class="sxs-lookup"><span data-stu-id="8e4b2-116">Filters usually pass quality-control messages to an upstream output pin, not to an input pin.</span></span> <span data-ttu-id="8e4b2-117">Pertanto, questo metodo restituisce \_ OK senza eseguire alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="8e4b2-117">Therefore, this method returns S\_OK without doing anything.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e4b2-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8e4b2-118">Requirements</span></span>



| <span data-ttu-id="8e4b2-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e4b2-119">Requirement</span></span> | <span data-ttu-id="8e4b2-120">Valore</span><span class="sxs-lookup"><span data-stu-id="8e4b2-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e4b2-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8e4b2-121">Header</span></span><br/>  | <dl> <span data-ttu-id="8e4b2-122"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8e4b2-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="8e4b2-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="8e4b2-123">Library</span></span><br/> | <dl> <span data-ttu-id="8e4b2-124"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="8e4b2-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e4b2-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8e4b2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e4b2-126">**Classe CBaseInputPin**</span><span class="sxs-lookup"><span data-stu-id="8e4b2-126">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> <dt>

[<span data-ttu-id="8e4b2-127">Gestione controllo qualità</span><span class="sxs-lookup"><span data-stu-id="8e4b2-127">Quality-Control Management</span></span>](quality-control-management.md)
</dt> </dl>

 

 




