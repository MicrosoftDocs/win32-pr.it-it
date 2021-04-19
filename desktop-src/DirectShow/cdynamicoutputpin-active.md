---
description: Il metodo attivo notifica al pin che il filtro è ora attivo.
ms.assetid: c2b8eb54-1bae-4f52-8324-dc70e3cac577
title: Metodo CDynamicOutputPin. Active (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8f1765d0aa524c0dafd03a3fe4133af71e32fa70
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333462"
---
# <a name="cdynamicoutputpinactive-method"></a><span data-ttu-id="21df0-103">Metodo CDynamicOutputPin. Active</span><span class="sxs-lookup"><span data-stu-id="21df0-103">CDynamicOutputPin.Active method</span></span>

<span data-ttu-id="21df0-104">Il `Active` metodo notifica al pin che il filtro è ora attivo.</span><span class="sxs-lookup"><span data-stu-id="21df0-104">The `Active` method notifies the pin that the filter is now active.</span></span>

## <a name="syntax"></a><span data-ttu-id="21df0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="21df0-105">Syntax</span></span>


```C++
HRESULT Active();
```



## <a name="parameters"></a><span data-ttu-id="21df0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="21df0-106">Parameters</span></span>

<span data-ttu-id="21df0-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="21df0-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="21df0-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="21df0-108">Return value</span></span>

<span data-ttu-id="21df0-109">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="21df0-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="21df0-110">I valori possibili includono quelli mostrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="21df0-110">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="21df0-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="21df0-111">Return code</span></span>                                                                            | <span data-ttu-id="21df0-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="21df0-112">Description</span></span>                                                                                                     |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="21df0-113"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="21df0-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="21df0-114">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="21df0-114">Success.</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="21df0-115"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="21df0-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="21df0-116">Esito negativo.</span><span class="sxs-lookup"><span data-stu-id="21df0-116">Failure.</span></span> <span data-ttu-id="21df0-117">[**CDynamicOutputPin:: SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md) non è stato chiamato.</span><span class="sxs-lookup"><span data-stu-id="21df0-117">[**CDynamicOutputPin::SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md) was not called.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="21df0-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="21df0-118">Remarks</span></span>

<span data-ttu-id="21df0-119">Questo metodo esegue l'override del metodo [**CBaseOutputPin:: Active**](cbaseoutputpin-active.md) .</span><span class="sxs-lookup"><span data-stu-id="21df0-119">This method overrides the [**CBaseOutputPin::Active**](cbaseoutputpin-active.md) method.</span></span> <span data-ttu-id="21df0-120">Reimposta l'evento [**CDynamicOutputPin:: m \_ hStopEvent**](cdynamicoutputpin-m-hstopevent.md) .</span><span class="sxs-lookup"><span data-stu-id="21df0-120">It resets the [**CDynamicOutputPin::m\_hStopEvent**](cdynamicoutputpin-m-hstopevent.md) event.</span></span> <span data-ttu-id="21df0-121">Se il filtro proprietario non ha chiamato **SetConfigInfo**, questo metodo restituisce E ha \_ esito negativo.</span><span class="sxs-lookup"><span data-stu-id="21df0-121">If the owning filter has not called **SetConfigInfo**, this method returns E\_FAIL.</span></span>

## <a name="requirements"></a><span data-ttu-id="21df0-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="21df0-122">Requirements</span></span>



| <span data-ttu-id="21df0-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="21df0-123">Requirement</span></span> | <span data-ttu-id="21df0-124">Valore</span><span class="sxs-lookup"><span data-stu-id="21df0-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21df0-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="21df0-125">Header</span></span><br/>  | <dl> <span data-ttu-id="21df0-126"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="21df0-126"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="21df0-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="21df0-127">Library</span></span><br/> | <dl> <span data-ttu-id="21df0-128"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="21df0-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21df0-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="21df0-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21df0-130">**Classe CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="21df0-130">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




