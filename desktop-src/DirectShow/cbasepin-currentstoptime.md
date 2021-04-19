---
description: "Il metodo CurrentStopTime recupera l'ora di arresto del segmento, impostata dal Metodo CBasePin:: NewSegment."
ms.assetid: 2066c4a5-2d39-4a2e-b2d6-48c615862aec
title: Metodo CBasePin. CurrentStopTime (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CurrentStopTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 74fb25184bbcd0778268f74a4c40ccfb0722287f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328171"
---
# <a name="cbasepincurrentstoptime-method"></a><span data-ttu-id="cca96-103">CBasePin. CurrentStopTime, metodo</span><span class="sxs-lookup"><span data-stu-id="cca96-103">CBasePin.CurrentStopTime method</span></span>

<span data-ttu-id="cca96-104">Il `CurrentStopTime` metodo recupera l'ora di arresto del segmento, impostata dal metodo [**CBasePin:: NewSegment**](cbasepin-newsegment.md) .</span><span class="sxs-lookup"><span data-stu-id="cca96-104">The `CurrentStopTime` method retrieves the segment stop time, set by the [**CBasePin::NewSegment**](cbasepin-newsegment.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="cca96-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cca96-105">Syntax</span></span>


```C++
REFERENCE_TIME CurrentStopTime();
```



## <a name="parameters"></a><span data-ttu-id="cca96-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="cca96-106">Parameters</span></span>

<span data-ttu-id="cca96-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="cca96-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cca96-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cca96-108">Return value</span></span>

<span data-ttu-id="cca96-109">Restituisce il valore di [**CBasePin:: m \_ tStop**](cbasepin-m-tstop.md).</span><span class="sxs-lookup"><span data-stu-id="cca96-109">Returns the value of [**CBasePin::m\_tStop**](cbasepin-m-tstop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cca96-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cca96-110">Requirements</span></span>



| <span data-ttu-id="cca96-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="cca96-111">Requirement</span></span> | <span data-ttu-id="cca96-112">Valore</span><span class="sxs-lookup"><span data-stu-id="cca96-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cca96-113">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cca96-113">Header</span></span><br/>  | <dl> <span data-ttu-id="cca96-114"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cca96-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="cca96-115">Libreria</span><span class="sxs-lookup"><span data-stu-id="cca96-115">Library</span></span><br/> | <dl> <span data-ttu-id="cca96-116"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="cca96-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cca96-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cca96-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cca96-118">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="cca96-118">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




