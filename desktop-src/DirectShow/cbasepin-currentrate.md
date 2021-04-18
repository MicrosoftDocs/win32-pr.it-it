---
description: 'Il metodo PercentualeCorrente recupera la velocità del segmento, impostata dal Metodo CBasePin:: NewSegment.'
ms.assetid: 19780dd2-2dcf-4e5d-8a70-a46be05e040c
title: Metodo CBasePin. PercentualeCorrente (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CurrentRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: adffcc02aad4c5516a8e92c247e47b7dbf389d73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324686"
---
# <a name="cbasepincurrentrate-method"></a><span data-ttu-id="dfdc0-103">CBasePin. PercentualeCorrente, metodo</span><span class="sxs-lookup"><span data-stu-id="dfdc0-103">CBasePin.CurrentRate method</span></span>

<span data-ttu-id="dfdc0-104">Il `CurrentRate` metodo recupera la velocità del segmento, impostata dal metodo [**CBasePin:: NewSegment**](cbasepin-newsegment.md) .</span><span class="sxs-lookup"><span data-stu-id="dfdc0-104">The `CurrentRate` method retrieves the segment rate, set by the [**CBasePin::NewSegment**](cbasepin-newsegment.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfdc0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dfdc0-105">Syntax</span></span>


```C++
double CurrentRate();
```



## <a name="parameters"></a><span data-ttu-id="dfdc0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="dfdc0-106">Parameters</span></span>

<span data-ttu-id="dfdc0-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="dfdc0-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="dfdc0-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dfdc0-108">Return value</span></span>

<span data-ttu-id="dfdc0-109">Restituisce il valore di [**CBasePin:: m \_ drate**](cbasepin-m-drate.md).</span><span class="sxs-lookup"><span data-stu-id="dfdc0-109">Returns the value of [**CBasePin::m\_dRate**](cbasepin-m-drate.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dfdc0-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dfdc0-110">Requirements</span></span>



| <span data-ttu-id="dfdc0-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="dfdc0-111">Requirement</span></span> | <span data-ttu-id="dfdc0-112">Valore</span><span class="sxs-lookup"><span data-stu-id="dfdc0-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfdc0-113">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dfdc0-113">Header</span></span><br/>  | <dl> <span data-ttu-id="dfdc0-114"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dfdc0-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="dfdc0-115">Libreria</span><span class="sxs-lookup"><span data-stu-id="dfdc0-115">Library</span></span><br/> | <dl> <span data-ttu-id="dfdc0-116"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="dfdc0-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dfdc0-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dfdc0-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfdc0-118">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="dfdc0-118">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




