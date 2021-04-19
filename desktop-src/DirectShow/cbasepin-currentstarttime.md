---
description: "Il metodo CurrentStartTime recupera l'ora di inizio del segmento, impostata dal Metodo CBasePin:: NewSegment."
ms.assetid: 6bf7407e-0b23-47cf-925e-3fed183c76fa
title: Metodo CBasePin. CurrentStartTime (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CurrentStartTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5f413419992d66f8de3a28bb7e39368564ce0803
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333489"
---
# <a name="cbasepincurrentstarttime-method"></a><span data-ttu-id="c315a-103">CBasePin. CurrentStartTime, metodo</span><span class="sxs-lookup"><span data-stu-id="c315a-103">CBasePin.CurrentStartTime method</span></span>

<span data-ttu-id="c315a-104">Il `CurrentStartTime` metodo recupera l'ora di inizio del segmento, impostata dal metodo [**CBasePin:: NewSegment**](cbasepin-newsegment.md) .</span><span class="sxs-lookup"><span data-stu-id="c315a-104">The `CurrentStartTime` method retrieves the segment start time, set by the [**CBasePin::NewSegment**](cbasepin-newsegment.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c315a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c315a-105">Syntax</span></span>


```C++
REFERENCE_TIME CurrentStartTime();
```



## <a name="parameters"></a><span data-ttu-id="c315a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c315a-106">Parameters</span></span>

<span data-ttu-id="c315a-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="c315a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c315a-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c315a-108">Return value</span></span>

<span data-ttu-id="c315a-109">Restituisce il valore di [**CBasePin:: m \_ tStart**](cbasepin-m-tstart.md).</span><span class="sxs-lookup"><span data-stu-id="c315a-109">Returns the value of [**CBasePin::m\_tStart**](cbasepin-m-tstart.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c315a-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c315a-110">Requirements</span></span>



| <span data-ttu-id="c315a-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="c315a-111">Requirement</span></span> | <span data-ttu-id="c315a-112">Valore</span><span class="sxs-lookup"><span data-stu-id="c315a-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c315a-113">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c315a-113">Header</span></span><br/>  | <dl> <span data-ttu-id="c315a-114"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c315a-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c315a-115">Libreria</span><span class="sxs-lookup"><span data-stu-id="c315a-115">Library</span></span><br/> | <dl> <span data-ttu-id="c315a-116"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="c315a-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c315a-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c315a-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c315a-118">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="c315a-118">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




