---
description: Il metodo ScheduleSample pianifica un esempio per il rendering.
ms.assetid: 08c218d1-6d0a-4c66-bbde-a39e5d31561c
title: Metodo CBaseRenderer. ScheduleSample (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.ScheduleSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c340e54f35b353820b128681cfbc0c5798d38849
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331930"
---
# <a name="cbaserendererschedulesample-method"></a><span data-ttu-id="ce5bc-103">CBaseRenderer. ScheduleSample, metodo</span><span class="sxs-lookup"><span data-stu-id="ce5bc-103">CBaseRenderer.ScheduleSample method</span></span>

<span data-ttu-id="ce5bc-104">Il `ScheduleSample` metodo pianifica un esempio per il rendering.</span><span class="sxs-lookup"><span data-stu-id="ce5bc-104">The `ScheduleSample` method schedules a sample for rendering.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce5bc-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ce5bc-105">Syntax</span></span>


```C++
virtual BOOL ScheduleSample(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="ce5bc-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ce5bc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce5bc-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="ce5bc-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="ce5bc-108">Puntatore all'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="ce5bc-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce5bc-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ce5bc-109">Return value</span></span>

<span data-ttu-id="ce5bc-110">Restituisce **true** se l'esempio è stato pianificato oppure **false** se l'esempio è stato eliminato.</span><span class="sxs-lookup"><span data-stu-id="ce5bc-110">Returns **TRUE** if the sample was scheduled, or **FALSE** if the sample was dropped.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce5bc-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="ce5bc-111">Remarks</span></span>

<span data-ttu-id="ce5bc-112">Questo metodo determina innanzitutto se il rendering dell'esempio deve essere eseguito immediatamente, sottoposto a rendering in futuro o eliminato.</span><span class="sxs-lookup"><span data-stu-id="ce5bc-112">This method first determines whether the sample should be rendered immediately, rendered in the future, or dropped.</span></span> <span data-ttu-id="ce5bc-113">A tale scopo, viene chiamato il metodo [**CBaseRenderer:: GetSampleTimes**](cbaserenderer-getsampletimes.md) . Se l'esempio deve essere sottoposto a rendering immediatamente, il metodo segnala l'evento [**CBaseRenderer:: m \_ RenderEvent**](cbaserenderer-m-renderevent.md) .</span><span class="sxs-lookup"><span data-stu-id="ce5bc-113">(To do so, it calls the [**CBaseRenderer::GetSampleTimes**](cbaserenderer-getsampletimes.md) method.) If the sample should be rendered immediately, the method signals the [**CBaseRenderer::m\_RenderEvent**](cbaserenderer-m-renderevent.md) event.</span></span> <span data-ttu-id="ce5bc-114">Se l'esempio deve essere sottoposto a rendering in futuro, il metodo chiama il metodo [**IReferenceClock:: AdviseTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) per la pianificazione.</span><span class="sxs-lookup"><span data-stu-id="ce5bc-114">If the sample should be rendered in the future, the method calls the [**IReferenceClock::AdviseTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) method for scheduling.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce5bc-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ce5bc-115">Requirements</span></span>



| <span data-ttu-id="ce5bc-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce5bc-116">Requirement</span></span> | <span data-ttu-id="ce5bc-117">Valore</span><span class="sxs-lookup"><span data-stu-id="ce5bc-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce5bc-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ce5bc-118">Header</span></span><br/>  | <dl> <span data-ttu-id="ce5bc-119"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ce5bc-119"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ce5bc-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="ce5bc-120">Library</span></span><br/> | <dl> <span data-ttu-id="ce5bc-121"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ce5bc-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce5bc-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ce5bc-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce5bc-123">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="ce5bc-123">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




