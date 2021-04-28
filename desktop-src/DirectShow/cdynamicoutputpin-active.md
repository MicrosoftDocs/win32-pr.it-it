---
description: 'Metodo CDynamicOutputPin.Active: il metodo Active notifica al segnaposto che il filtro è ora attivo.'
ms.assetid: c2b8eb54-1bae-4f52-8324-dc70e3cac577
title: Metodo CDynamicOutputPin.Active (Amfilter.h)
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
ms.openlocfilehash: 1d9544c0fd125146b10f008565fcfbe330d18de1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099329"
---
# <a name="cdynamicoutputpinactive-method"></a><span data-ttu-id="c9e76-103">Metodo CDynamicOutputPin.Active</span><span class="sxs-lookup"><span data-stu-id="c9e76-103">CDynamicOutputPin.Active method</span></span>

<span data-ttu-id="c9e76-104">Il `Active` metodo notifica al segnaposto che il filtro è ora attivo.</span><span class="sxs-lookup"><span data-stu-id="c9e76-104">The `Active` method notifies the pin that the filter is now active.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9e76-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c9e76-105">Syntax</span></span>


```C++
HRESULT Active();
```



## <a name="parameters"></a><span data-ttu-id="c9e76-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c9e76-106">Parameters</span></span>

<span data-ttu-id="c9e76-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="c9e76-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c9e76-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c9e76-108">Return value</span></span>

<span data-ttu-id="c9e76-109">Restituisce un **valore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="c9e76-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="c9e76-110">I valori possibili includono quelli illustrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="c9e76-110">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="c9e76-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="c9e76-111">Return code</span></span>                                                                            | <span data-ttu-id="c9e76-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c9e76-112">Description</span></span>                                                                                                     |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c9e76-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c9e76-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="c9e76-114">Operazione completata.</span><span class="sxs-lookup"><span data-stu-id="c9e76-114">Success.</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="c9e76-115"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="c9e76-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="c9e76-116">Esito negativo.</span><span class="sxs-lookup"><span data-stu-id="c9e76-116">Failure.</span></span> <span data-ttu-id="c9e76-117">[**CDynamicOutputPin::SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md) non è stato chiamato.</span><span class="sxs-lookup"><span data-stu-id="c9e76-117">[**CDynamicOutputPin::SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md) was not called.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c9e76-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="c9e76-118">Remarks</span></span>

<span data-ttu-id="c9e76-119">Questo metodo esegue l'override [**del metodo CBaseOutputPin::Active.**](cbaseoutputpin-active.md)</span><span class="sxs-lookup"><span data-stu-id="c9e76-119">This method overrides the [**CBaseOutputPin::Active**](cbaseoutputpin-active.md) method.</span></span> <span data-ttu-id="c9e76-120">Reimposta l'evento [**\_ HStopEvent CDynamicOutputPin::m.**](cdynamicoutputpin-m-hstopevent.md)</span><span class="sxs-lookup"><span data-stu-id="c9e76-120">It resets the [**CDynamicOutputPin::m\_hStopEvent**](cdynamicoutputpin-m-hstopevent.md) event.</span></span> <span data-ttu-id="c9e76-121">Se il filtro proprietario non ha chiamato **SetConfigInfo,** questo metodo restituisce E \_ FAIL.</span><span class="sxs-lookup"><span data-stu-id="c9e76-121">If the owning filter has not called **SetConfigInfo**, this method returns E\_FAIL.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9e76-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c9e76-122">Requirements</span></span>



| <span data-ttu-id="c9e76-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9e76-123">Requirement</span></span> | <span data-ttu-id="c9e76-124">Valore</span><span class="sxs-lookup"><span data-stu-id="c9e76-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9e76-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c9e76-125">Header</span></span><br/>  | <dl> <span data-ttu-id="c9e76-126"><dt>Amfilter.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="c9e76-126"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c9e76-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="c9e76-127">Library</span></span><br/> | <dl> <span data-ttu-id="c9e76-128"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="c9e76-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9e76-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c9e76-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9e76-130">**Classe CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="c9e76-130">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




