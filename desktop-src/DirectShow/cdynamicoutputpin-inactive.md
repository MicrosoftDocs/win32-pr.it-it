---
description: Il metodo inattivo notifica al pin che il filtro è stato arrestato.
ms.assetid: f7efb67b-cc3f-47c4-a8ba-b2365aef0d96
title: Metodo CDynamicOutputPin. Inactive (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4501025e844056a83be3e20a19f8ad52f935097f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324184"
---
# <a name="cdynamicoutputpininactive-method"></a><span data-ttu-id="9260c-103">Metodo CDynamicOutputPin. Inactive</span><span class="sxs-lookup"><span data-stu-id="9260c-103">CDynamicOutputPin.Inactive method</span></span>

<span data-ttu-id="9260c-104">Il `Inactive` metodo notifica al pin che il filtro è stato arrestato.</span><span class="sxs-lookup"><span data-stu-id="9260c-104">The `Inactive` method notifies the pin that the filter has stopped.</span></span>

## <a name="syntax"></a><span data-ttu-id="9260c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9260c-105">Syntax</span></span>


```C++
HRESULT Inactive();
```



## <a name="parameters"></a><span data-ttu-id="9260c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9260c-106">Parameters</span></span>

<span data-ttu-id="9260c-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="9260c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9260c-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9260c-108">Return value</span></span>

<span data-ttu-id="9260c-109">Restituisce \_ OK se ha esito positivo o un valore **HRESULT** che indica la ragione dell'errore.</span><span class="sxs-lookup"><span data-stu-id="9260c-109">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="9260c-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="9260c-110">Remarks</span></span>

<span data-ttu-id="9260c-111">Questo metodo esegue l'override del metodo [**CBaseOutputPin:: inactive**](cbaseoutputpin-inactive.md) .</span><span class="sxs-lookup"><span data-stu-id="9260c-111">This method overrides the [**CBaseOutputPin::Inactive**](cbaseoutputpin-inactive.md) method.</span></span> <span data-ttu-id="9260c-112">Imposta l'evento [**CDynamicOutputPin:: m \_ hStopEvent**](cdynamicoutputpin-m-hstopevent.md) .</span><span class="sxs-lookup"><span data-stu-id="9260c-112">It sets the [**CDynamicOutputPin::m\_hStopEvent**](cdynamicoutputpin-m-hstopevent.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="9260c-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9260c-113">Requirements</span></span>



| <span data-ttu-id="9260c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="9260c-114">Requirement</span></span> | <span data-ttu-id="9260c-115">Valore</span><span class="sxs-lookup"><span data-stu-id="9260c-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9260c-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9260c-116">Header</span></span><br/>  | <dl> <span data-ttu-id="9260c-117"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9260c-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="9260c-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="9260c-118">Library</span></span><br/> | <dl> <span data-ttu-id="9260c-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="9260c-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9260c-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9260c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9260c-121">**Classe CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="9260c-121">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




