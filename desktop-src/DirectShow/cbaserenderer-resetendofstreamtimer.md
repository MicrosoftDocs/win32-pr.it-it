---
description: Il metodo ResetEndOfStreamTimer Annulla il timer che pianifica le \_ notifiche complete di EC.
ms.assetid: 9d423241-1401-4181-8fbf-c409a1e8abdd
title: Metodo CBaseRenderer. ResetEndOfStreamTimer (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.ResetEndOfStreamTimer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 734673c4e2bd6719179eca00f03a6c2f41061132
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333330"
---
# <a name="cbaserendererresetendofstreamtimer-method"></a><span data-ttu-id="d4b6b-103">CBaseRenderer. ResetEndOfStreamTimer, metodo</span><span class="sxs-lookup"><span data-stu-id="d4b6b-103">CBaseRenderer.ResetEndOfStreamTimer method</span></span>

<span data-ttu-id="d4b6b-104">Il `ResetEndOfStreamTimer` metodo annulla il timer che pianifica le notifiche [**\_ complete di EC**](ec-complete.md) .</span><span class="sxs-lookup"><span data-stu-id="d4b6b-104">The `ResetEndOfStreamTimer` method cancels the timer that schedules [**EC\_COMPLETE**](ec-complete.md) notifications.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4b6b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d4b6b-105">Syntax</span></span>


```C++
void ResetEndOfStreamTimer();
```



## <a name="parameters"></a><span data-ttu-id="d4b6b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d4b6b-106">Parameters</span></span>

<span data-ttu-id="d4b6b-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="d4b6b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d4b6b-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d4b6b-108">Return value</span></span>

<span data-ttu-id="d4b6b-109">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="d4b6b-109">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4b6b-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d4b6b-110">Requirements</span></span>



| <span data-ttu-id="d4b6b-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4b6b-111">Requirement</span></span> | <span data-ttu-id="d4b6b-112">Valore</span><span class="sxs-lookup"><span data-stu-id="d4b6b-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4b6b-113">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d4b6b-113">Header</span></span><br/>  | <dl> <span data-ttu-id="d4b6b-114"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d4b6b-114"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d4b6b-115">Libreria</span><span class="sxs-lookup"><span data-stu-id="d4b6b-115">Library</span></span><br/> | <dl> <span data-ttu-id="d4b6b-116"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d4b6b-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4b6b-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d4b6b-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4b6b-118">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="d4b6b-118">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> <dt>

[<span data-ttu-id="d4b6b-119">**CBaseRenderer::SendEndOfStream**</span><span class="sxs-lookup"><span data-stu-id="d4b6b-119">**CBaseRenderer::SendEndOfStream**</span></span>](cbaserenderer-sendendofstream.md)
</dt> <dt>

[<span data-ttu-id="d4b6b-120">**CBaseRenderer:: TimerCallback**</span><span class="sxs-lookup"><span data-stu-id="d4b6b-120">**CBaseRenderer::TimerCallback**</span></span>](cbaserenderer-timercallback.md)
</dt> </dl>

 

 




