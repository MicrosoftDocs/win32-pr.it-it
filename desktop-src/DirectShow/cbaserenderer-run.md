---
description: Il metodo run esegue il filtro.
ms.assetid: 83251137-83f8-45a3-b3f2-d7b45f43f7f8
title: Metodo CBaseRenderer. Run (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cc298cbe3f2a0b8063caaa3bdb69fd0d8a88f556
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333329"
---
# <a name="cbaserendererrun-method"></a><span data-ttu-id="cae39-103">Metodo CBaseRenderer. Run</span><span class="sxs-lookup"><span data-stu-id="cae39-103">CBaseRenderer.Run method</span></span>

<span data-ttu-id="cae39-104">Il `Run` metodo esegue il filtro.</span><span class="sxs-lookup"><span data-stu-id="cae39-104">The `Run` method runs the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="cae39-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cae39-105">Syntax</span></span>


```C++
HRESULT Run();
```



## <a name="parameters"></a><span data-ttu-id="cae39-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="cae39-106">Parameters</span></span>

<span data-ttu-id="cae39-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="cae39-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cae39-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cae39-108">Return value</span></span>

<span data-ttu-id="cae39-109">Restituisce \_ OK se ha esito positivo o un valore **HRESULT** che indica la ragione dell'errore.</span><span class="sxs-lookup"><span data-stu-id="cae39-109">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="cae39-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="cae39-110">Remarks</span></span>

<span data-ttu-id="cae39-111">Questo metodo esegue l'override del metodo [**CBaseFilter:: Run**](cbasefilter-run.md) .</span><span class="sxs-lookup"><span data-stu-id="cae39-111">This method overrides the [**CBaseFilter::Run**](cbasefilter-run.md) method.</span></span> <span data-ttu-id="cae39-112">Esegue le azioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="cae39-112">It performs the following actions:</span></span>

-   <span data-ttu-id="cae39-113">Chiama il metodo **CBaseFilter:: Run** .</span><span class="sxs-lookup"><span data-stu-id="cae39-113">Calls the **CBaseFilter::Run** method.</span></span>
-   <span data-ttu-id="cae39-114">Viene eseguito il commit dell'allocatore.</span><span class="sxs-lookup"><span data-stu-id="cae39-114">Commits the allocator.</span></span> <span data-ttu-id="cae39-115">Vedere [**IMemAllocator:: commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit).</span><span class="sxs-lookup"><span data-stu-id="cae39-115">(See [**IMemAllocator::Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit).)</span></span>
-   <span data-ttu-id="cae39-116">Se lo stato precedente è stato interrotto, il filtro rilascia tutti i campioni che contiene.</span><span class="sxs-lookup"><span data-stu-id="cae39-116">If the previous state was stopped, the filter releases any sample it is holding.</span></span> <span data-ttu-id="cae39-117">(L'esempio non è più valido).</span><span class="sxs-lookup"><span data-stu-id="cae39-117">(The sample is no longer valid.)</span></span>
-   <span data-ttu-id="cae39-118">Chiama il metodo [**CBaseRenderer:: StartStreaming**](cbaserenderer-startstreaming.md) e restituisce il risultato.</span><span class="sxs-lookup"><span data-stu-id="cae39-118">Calls the [**CBaseRenderer::StartStreaming**](cbaserenderer-startstreaming.md) method and returns the result.</span></span> <span data-ttu-id="cae39-119">Se un esempio è in sospeso, il metodo **StartStreaming** lo pianifica per il rendering.</span><span class="sxs-lookup"><span data-stu-id="cae39-119">If a sample is pending, the **StartStreaming** method schedules it for rendering.</span></span>

<span data-ttu-id="cae39-120">Se il filtro non è connesso, invia immediatamente un evento [**EC \_ complete**](ec-complete.md) .</span><span class="sxs-lookup"><span data-stu-id="cae39-120">If the filter is not connected, it posts an [**EC\_COMPLETE**](ec-complete.md) event immediately.</span></span>

## <a name="requirements"></a><span data-ttu-id="cae39-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cae39-121">Requirements</span></span>



| <span data-ttu-id="cae39-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="cae39-122">Requirement</span></span> | <span data-ttu-id="cae39-123">Valore</span><span class="sxs-lookup"><span data-stu-id="cae39-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cae39-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cae39-124">Header</span></span><br/>  | <dl> <span data-ttu-id="cae39-125"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cae39-125"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="cae39-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="cae39-126">Library</span></span><br/> | <dl> <span data-ttu-id="cae39-127"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="cae39-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cae39-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cae39-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cae39-129">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="cae39-129">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




