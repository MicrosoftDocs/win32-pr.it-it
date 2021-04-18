---
description: Il metodo GetRenderEvent recupera l'evento che pianifica il rendering.
ms.assetid: da0272f6-6a1d-4c07-a907-822227b56305
title: Metodo CBaseRenderer. GetRenderEvent (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetRenderEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9e2fd0b9cd98194129eccd2e24e6ee75577d1eec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324855"
---
# <a name="cbaserenderergetrenderevent-method"></a><span data-ttu-id="aa48d-103">CBaseRenderer. GetRenderEvent, metodo</span><span class="sxs-lookup"><span data-stu-id="aa48d-103">CBaseRenderer.GetRenderEvent method</span></span>

<span data-ttu-id="aa48d-104">Il `GetRenderEvent` metodo recupera l'evento che pianifica il rendering.</span><span class="sxs-lookup"><span data-stu-id="aa48d-104">The `GetRenderEvent` method retrieves the event that schedules rendering.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa48d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="aa48d-105">Syntax</span></span>


```C++
CAMEvent* GetRenderEvent();
```



## <a name="parameters"></a><span data-ttu-id="aa48d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="aa48d-106">Parameters</span></span>

<span data-ttu-id="aa48d-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="aa48d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="aa48d-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="aa48d-108">Return value</span></span>

<span data-ttu-id="aa48d-109">Restituisce un puntatore all'evento [**CBaseRenderer:: m \_ RenderEvent**](cbaserenderer-m-renderevent.md) .</span><span class="sxs-lookup"><span data-stu-id="aa48d-109">Returns a pointer to the [**CBaseRenderer::m\_RenderEvent**](cbaserenderer-m-renderevent.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa48d-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aa48d-110">Requirements</span></span>



| <span data-ttu-id="aa48d-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa48d-111">Requirement</span></span> | <span data-ttu-id="aa48d-112">Valore</span><span class="sxs-lookup"><span data-stu-id="aa48d-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa48d-113">Intestazione</span><span class="sxs-lookup"><span data-stu-id="aa48d-113">Header</span></span><br/>  | <dl> <span data-ttu-id="aa48d-114"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="aa48d-114"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="aa48d-115">Libreria</span><span class="sxs-lookup"><span data-stu-id="aa48d-115">Library</span></span><br/> | <dl> <span data-ttu-id="aa48d-116"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="aa48d-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa48d-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aa48d-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa48d-118">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="aa48d-118">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




