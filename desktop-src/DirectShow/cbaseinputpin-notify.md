---
description: 'Metodo CBaseInputPin.Notify: il metodo Notify notifica al pin che è richiesta una modifica di qualità. Questo metodo implementa il metodo IQualityControl::Notify.'
ms.assetid: 76124321-0d2d-4fee-a08a-4db23078e8df
title: Metodo CBaseInputPin.Notify (Amfilter.h)
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
ms.openlocfilehash: 610888193762618d427a0329a27d3019bd625e69
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119999"
---
# <a name="cbaseinputpinnotify-method"></a><span data-ttu-id="d5d4b-104">Metodo CBaseInputPin.Notify</span><span class="sxs-lookup"><span data-stu-id="d5d4b-104">CBaseInputPin.Notify method</span></span>

<span data-ttu-id="d5d4b-105">Il `Notify` metodo notifica al pin che è richiesta una modifica di qualità.</span><span class="sxs-lookup"><span data-stu-id="d5d4b-105">The `Notify` method notifies the pin that a quality change is requested.</span></span> <span data-ttu-id="d5d4b-106">Questo metodo implementa il [**metodo IQualityControl::Notify.**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify)</span><span class="sxs-lookup"><span data-stu-id="d5d4b-106">This method implements the [**IQualityControl::Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5d4b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d5d4b-107">Syntax</span></span>


```C++
HRESULT Notify(
   IBaseFilter *pSelf,
   Quality     q
);
```



## <a name="parameters"></a><span data-ttu-id="d5d4b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d5d4b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5d4b-109">*pSelf*</span><span class="sxs-lookup"><span data-stu-id="d5d4b-109">*pSelf*</span></span> 
</dt> <dd>

<span data-ttu-id="d5d4b-110">Puntatore al filtro che invia il messaggio di controllo qualità.</span><span class="sxs-lookup"><span data-stu-id="d5d4b-110">Pointer to the filter that is sending the quality-control message.</span></span>

</dd> <dt>

<span data-ttu-id="d5d4b-111">*D*</span><span class="sxs-lookup"><span data-stu-id="d5d4b-111">*q*</span></span> 
</dt> <dd>

<span data-ttu-id="d5d4b-112">[**Struttura**](/windows/win32/api/strmif/ns-strmif-quality) di qualità che contiene il messaggio di controllo qualità.</span><span class="sxs-lookup"><span data-stu-id="d5d4b-112">[**Quality**](/windows/win32/api/strmif/ns-strmif-quality) structure that contains the quality-control message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5d4b-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d5d4b-113">Return value</span></span>

<span data-ttu-id="d5d4b-114">Restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d5d4b-114">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5d4b-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="d5d4b-115">Remarks</span></span>

<span data-ttu-id="d5d4b-116">I filtri passano in genere messaggi di controllo della qualità a un pin di output upstream, non a un pin di input.</span><span class="sxs-lookup"><span data-stu-id="d5d4b-116">Filters usually pass quality-control messages to an upstream output pin, not to an input pin.</span></span> <span data-ttu-id="d5d4b-117">Pertanto, questo metodo restituisce S \_ OK senza eseguire alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="d5d4b-117">Therefore, this method returns S\_OK without doing anything.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5d4b-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d5d4b-118">Requirements</span></span>



| <span data-ttu-id="d5d4b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5d4b-119">Requirement</span></span> | <span data-ttu-id="d5d4b-120">Valore</span><span class="sxs-lookup"><span data-stu-id="d5d4b-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5d4b-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d5d4b-121">Header</span></span><br/>  | <dl> <span data-ttu-id="d5d4b-122"><dt>Amfilter.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="d5d4b-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d5d4b-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="d5d4b-123">Library</span></span><br/> | <dl> <span data-ttu-id="d5d4b-124"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d5d4b-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5d4b-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d5d4b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5d4b-126">**Classe CBaseInputPin**</span><span class="sxs-lookup"><span data-stu-id="d5d4b-126">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> <dt>

[<span data-ttu-id="d5d4b-127">Gestione del controllo di qualità</span><span class="sxs-lookup"><span data-stu-id="d5d4b-127">Quality-Control Management</span></span>](quality-control-management.md)
</dt> </dl>

 

 




