---
description: Il metodo DeliverBeginFlush richiede al pin di input connesso di iniziare un'operazione di svuotamento.
ms.assetid: eafc3835-7696-480b-abc8-154938e19b15
title: Metodo CDynamicOutputPin. DeliverBeginFlush (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.DeliverBeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 242394a327b63fcc901b08f572096bf2f42238b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328255"
---
# <a name="cdynamicoutputpindeliverbeginflush-method"></a><span data-ttu-id="c8e87-103">CDynamicOutputPin. DeliverBeginFlush, metodo</span><span class="sxs-lookup"><span data-stu-id="c8e87-103">CDynamicOutputPin.DeliverBeginFlush method</span></span>

<span data-ttu-id="c8e87-104">Il `DeliverBeginFlush` metodo richiede al pin di input connesso di iniziare un'operazione di svuotamento.</span><span class="sxs-lookup"><span data-stu-id="c8e87-104">The `DeliverBeginFlush` method requests the connected input pin to begin a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8e87-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c8e87-105">Syntax</span></span>


```C++
HRESULT DeliverBeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="c8e87-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c8e87-106">Parameters</span></span>

<span data-ttu-id="c8e87-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="c8e87-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c8e87-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c8e87-108">Return value</span></span>

<span data-ttu-id="c8e87-109">Restituisce \_ OK se ha esito positivo o un valore **HRESULT** che indica la ragione dell'errore.</span><span class="sxs-lookup"><span data-stu-id="c8e87-109">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8e87-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="c8e87-110">Remarks</span></span>

<span data-ttu-id="c8e87-111">Questo metodo esegue l'override del metodo [**CBaseOutputPin::D eliverbeginflush**](cbaseoutputpin-deliverbeginflush.md) .</span><span class="sxs-lookup"><span data-stu-id="c8e87-111">This method overrides the [**CBaseOutputPin::DeliverBeginFlush**](cbaseoutputpin-deliverbeginflush.md) method.</span></span> <span data-ttu-id="c8e87-112">Imposta l'evento [**CDynamicOutputPin:: m \_ hStopEvent**](cdynamicoutputpin-m-hstopevent.md) .</span><span class="sxs-lookup"><span data-stu-id="c8e87-112">It sets the [**CDynamicOutputPin::m\_hStopEvent**](cdynamicoutputpin-m-hstopevent.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8e87-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c8e87-113">Requirements</span></span>



| <span data-ttu-id="c8e87-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8e87-114">Requirement</span></span> | <span data-ttu-id="c8e87-115">Valore</span><span class="sxs-lookup"><span data-stu-id="c8e87-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8e87-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c8e87-116">Header</span></span><br/>  | <dl> <span data-ttu-id="c8e87-117"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c8e87-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c8e87-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="c8e87-118">Library</span></span><br/> | <dl> <span data-ttu-id="c8e87-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="c8e87-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8e87-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c8e87-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8e87-121">**Classe CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="c8e87-121">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




