---
description: Il metodo ThrottleWait inserisce un periodo di attesa dopo ciascun frame.
ms.assetid: 69306093-f5db-4170-b30f-e33cfa448e9f
title: Metodo CBaseVideoRenderer. ThrottleWait (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.ThrottleWait
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7408cfb011fa0fbbb223b6757ddb10ff9cbd357b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325344"
---
# <a name="cbasevideorendererthrottlewait-method"></a><span data-ttu-id="e75fc-103">CBaseVideoRenderer. ThrottleWait, metodo</span><span class="sxs-lookup"><span data-stu-id="e75fc-103">CBaseVideoRenderer.ThrottleWait method</span></span>

<span data-ttu-id="e75fc-104">Il `ThrottleWait` metodo inserisce un periodo di attesa dopo ciascun frame.</span><span class="sxs-lookup"><span data-stu-id="e75fc-104">The `ThrottleWait` method inserts a wait period after each frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="e75fc-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e75fc-105">Syntax</span></span>


```C++
void ThrottleWait();
```



## <a name="parameters"></a><span data-ttu-id="e75fc-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e75fc-106">Parameters</span></span>

<span data-ttu-id="e75fc-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="e75fc-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e75fc-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e75fc-108">Return value</span></span>

<span data-ttu-id="e75fc-109">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="e75fc-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e75fc-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="e75fc-110">Remarks</span></span>

<span data-ttu-id="e75fc-111">Questa funzione membro attende un periodo di tempo ottenuto dal membro dati **m \_ trThrottle** .</span><span class="sxs-lookup"><span data-stu-id="e75fc-111">This member function waits for a time period obtained from the **m\_trThrottle** data member.</span></span>

## <a name="requirements"></a><span data-ttu-id="e75fc-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e75fc-112">Requirements</span></span>



| <span data-ttu-id="e75fc-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="e75fc-113">Requirement</span></span> | <span data-ttu-id="e75fc-114">Valore</span><span class="sxs-lookup"><span data-stu-id="e75fc-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e75fc-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e75fc-115">Header</span></span><br/>  | <dl> <span data-ttu-id="e75fc-116"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e75fc-116"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e75fc-117">Libreria</span><span class="sxs-lookup"><span data-stu-id="e75fc-117">Library</span></span><br/> | <dl> <span data-ttu-id="e75fc-118"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e75fc-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e75fc-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e75fc-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e75fc-120">**Classe CBaseVideoRenderer**</span><span class="sxs-lookup"><span data-stu-id="e75fc-120">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




