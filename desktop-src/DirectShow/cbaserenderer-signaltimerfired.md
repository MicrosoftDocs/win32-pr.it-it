---
description: Il metodo SignalTimerFired cancella l'identificatore del timer utilizzato per pianificare il rendering.
ms.assetid: b8ae362e-fcda-4888-be32-8fb910d0f0db
title: Metodo CBaseRenderer. SignalTimerFired (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SignalTimerFired
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4dd29b37869fc6f07c2d876dfa0d1d306b04b111
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332998"
---
# <a name="cbaserenderersignaltimerfired-method"></a><span data-ttu-id="bf492-103">CBaseRenderer. SignalTimerFired, metodo</span><span class="sxs-lookup"><span data-stu-id="bf492-103">CBaseRenderer.SignalTimerFired method</span></span>

<span data-ttu-id="bf492-104">Il `SignalTimerFired` metodo cancella l'identificatore del timer utilizzato per pianificare il rendering.</span><span class="sxs-lookup"><span data-stu-id="bf492-104">The `SignalTimerFired` method clears the timer identifier used to schedule rendering.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf492-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bf492-105">Syntax</span></span>


```C++
virtual void SignalTimerFired();
```



## <a name="parameters"></a><span data-ttu-id="bf492-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="bf492-106">Parameters</span></span>

<span data-ttu-id="bf492-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="bf492-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bf492-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bf492-108">Return value</span></span>

<span data-ttu-id="bf492-109">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="bf492-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf492-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="bf492-110">Remarks</span></span>

<span data-ttu-id="bf492-111">Il filtro chiama questo metodo quando il timer di rendering viene attivato (vedere [**CBaseRenderer:: WaitForRenderTime**](cbaserenderer-waitforrendertime.md)) o quando il timer viene annullato (vedere [**CBaseRenderer:: CancelNotification**](cbaserenderer-cancelnotification.md)).</span><span class="sxs-lookup"><span data-stu-id="bf492-111">The filter calls this method when the rendering timer activates (see [**CBaseRenderer::WaitForRenderTime**](cbaserenderer-waitforrendertime.md)) or when the timer is canceled (see [**CBaseRenderer::CancelNotification**](cbaserenderer-cancelnotification.md)).</span></span> <span data-ttu-id="bf492-112">Il metodo reimposta la variabile membro [**CBaseRenderer:: m \_ dwAdvise**](cbaserenderer-m-dwadvise.md) su zero.</span><span class="sxs-lookup"><span data-stu-id="bf492-112">The method resets the [**CBaseRenderer::m\_dwAdvise**](cbaserenderer-m-dwadvise.md) member variable to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf492-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bf492-113">Requirements</span></span>



| <span data-ttu-id="bf492-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf492-114">Requirement</span></span> | <span data-ttu-id="bf492-115">Valore</span><span class="sxs-lookup"><span data-stu-id="bf492-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf492-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bf492-116">Header</span></span><br/>  | <dl> <span data-ttu-id="bf492-117"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bf492-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="bf492-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="bf492-118">Library</span></span><br/> | <dl> <span data-ttu-id="bf492-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="bf492-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf492-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bf492-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf492-121">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="bf492-121">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




