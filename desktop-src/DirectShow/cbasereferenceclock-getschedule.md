---
description: Il metodo getschedule recupera un puntatore all'oggetto di pianificazione del clock.
ms.assetid: ae509f16-d85f-4365-8cf2-c6585cbbdc3d
title: Metodo CBaseReferenceClock. getschedule (Refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.GetSchedule
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a37cdb3e18f3ab71b144af071233aee5a6a3a93d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326576"
---
# <a name="cbasereferenceclockgetschedule-method"></a><span data-ttu-id="7128e-103">Metodo CBaseReferenceClock. getschedule</span><span class="sxs-lookup"><span data-stu-id="7128e-103">CBaseReferenceClock.GetSchedule method</span></span>

<span data-ttu-id="7128e-104">Il `GetSchedule` metodo recupera un puntatore all'oggetto di pianificazione del clock.</span><span class="sxs-lookup"><span data-stu-id="7128e-104">The `GetSchedule` method retrieves a pointer to the clock's scheduling object.</span></span>

## <a name="syntax"></a><span data-ttu-id="7128e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7128e-105">Syntax</span></span>


```C++
CAMSchedule* GetSchedule();
```



## <a name="parameters"></a><span data-ttu-id="7128e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7128e-106">Parameters</span></span>

<span data-ttu-id="7128e-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="7128e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7128e-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7128e-108">Return value</span></span>

<span data-ttu-id="7128e-109">Restituisce la variabile membro [**CBaseReferenceClock:: m \_ pSchedule**](cbasereferenceclock-m-pschedule.md) .</span><span class="sxs-lookup"><span data-stu-id="7128e-109">Returns the [**CBaseReferenceClock::m\_pSchedule**](cbasereferenceclock-m-pschedule.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="7128e-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7128e-110">Requirements</span></span>



| <span data-ttu-id="7128e-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="7128e-111">Requirement</span></span> | <span data-ttu-id="7128e-112">Valore</span><span class="sxs-lookup"><span data-stu-id="7128e-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7128e-113">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7128e-113">Header</span></span><br/>  | <dl> <span data-ttu-id="7128e-114"><dt>Refclock. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7128e-114"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="7128e-115">Libreria</span><span class="sxs-lookup"><span data-stu-id="7128e-115">Library</span></span><br/> | <dl> <span data-ttu-id="7128e-116"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="7128e-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7128e-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7128e-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7128e-118">**Classe CBaseReferenceClock**</span><span class="sxs-lookup"><span data-stu-id="7128e-118">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




