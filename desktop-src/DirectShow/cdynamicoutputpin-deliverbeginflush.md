---
description: "Metodo CDynamicOutputPin.DeliverBeginFlush: il metodo DeliverBeginFlush richiede al pin di input connesso di iniziare un'operazione di scaricamento."
ms.assetid: eafc3835-7696-480b-abc8-154938e19b15
title: Metodo CDynamicOutputPin.DeliverBeginFlush (Amfilter.h)
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
ms.openlocfilehash: e4158a3d6191325e8b647e4551133952d623f795
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099319"
---
# <a name="cdynamicoutputpindeliverbeginflush-method"></a><span data-ttu-id="c6720-103">Metodo CDynamicOutputPin.DeliverBeginFlush</span><span class="sxs-lookup"><span data-stu-id="c6720-103">CDynamicOutputPin.DeliverBeginFlush method</span></span>

<span data-ttu-id="c6720-104">Il `DeliverBeginFlush` metodo richiede al pin di input connesso di iniziare un'operazione di scaricamento.</span><span class="sxs-lookup"><span data-stu-id="c6720-104">The `DeliverBeginFlush` method requests the connected input pin to begin a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6720-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c6720-105">Syntax</span></span>


```C++
HRESULT DeliverBeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="c6720-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c6720-106">Parameters</span></span>

<span data-ttu-id="c6720-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="c6720-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c6720-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c6720-108">Return value</span></span>

<span data-ttu-id="c6720-109">Restituisce S OK in caso di esito positivo o un \_ **valore HRESULT** che indica la causa dell'errore.</span><span class="sxs-lookup"><span data-stu-id="c6720-109">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6720-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="c6720-110">Remarks</span></span>

<span data-ttu-id="c6720-111">Questo metodo esegue l'override [**del metodo CBaseOutputPin::D eliverBeginFlush.**](cbaseoutputpin-deliverbeginflush.md)</span><span class="sxs-lookup"><span data-stu-id="c6720-111">This method overrides the [**CBaseOutputPin::DeliverBeginFlush**](cbaseoutputpin-deliverbeginflush.md) method.</span></span> <span data-ttu-id="c6720-112">Imposta [**l'evento \_ HStopEvent CDynamicOutputPin::m.**](cdynamicoutputpin-m-hstopevent.md)</span><span class="sxs-lookup"><span data-stu-id="c6720-112">It sets the [**CDynamicOutputPin::m\_hStopEvent**](cdynamicoutputpin-m-hstopevent.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6720-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c6720-113">Requirements</span></span>



| <span data-ttu-id="c6720-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6720-114">Requirement</span></span> | <span data-ttu-id="c6720-115">Valore</span><span class="sxs-lookup"><span data-stu-id="c6720-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6720-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c6720-116">Header</span></span><br/>  | <dl> <span data-ttu-id="c6720-117"><dt>Amfilter.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="c6720-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c6720-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="c6720-118">Library</span></span><br/> | <dl> <span data-ttu-id="c6720-119"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="c6720-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6720-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c6720-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6720-121">**Classe CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="c6720-121">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




