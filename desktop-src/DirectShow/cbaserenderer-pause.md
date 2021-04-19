---
description: Il metodo pause sospende il filtro.
ms.assetid: 9dfd23d1-bf07-424b-9952-13719358d0a5
title: Metodo CBaseRenderer. pause (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Pause
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e0b422882c07808f560f5256f67d01054d097726
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333344"
---
# <a name="cbaserendererpause-method"></a><span data-ttu-id="95a1f-103">CBaseRenderer. pause (metodo)</span><span class="sxs-lookup"><span data-stu-id="95a1f-103">CBaseRenderer.Pause method</span></span>

<span data-ttu-id="95a1f-104">Il `Pause` metodo sospende il filtro.</span><span class="sxs-lookup"><span data-stu-id="95a1f-104">The `Pause` method pauses the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="95a1f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="95a1f-105">Syntax</span></span>


```C++
HRESULT Pause();
```



## <a name="parameters"></a><span data-ttu-id="95a1f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="95a1f-106">Parameters</span></span>

<span data-ttu-id="95a1f-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="95a1f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="95a1f-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="95a1f-108">Return value</span></span>

<span data-ttu-id="95a1f-109">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="95a1f-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="95a1f-110">I valori possibili includono quelli nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="95a1f-110">Possible values include those in the following table.</span></span>



| <span data-ttu-id="95a1f-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="95a1f-111">Return code</span></span>                                                                             | <span data-ttu-id="95a1f-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="95a1f-112">Description</span></span>                            |
|-----------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <span data-ttu-id="95a1f-113"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="95a1f-113"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="95a1f-114">La transizione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="95a1f-114">The transition is complete.</span></span><br/> |
| <dl> <span data-ttu-id="95a1f-115"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="95a1f-115"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="95a1f-116">La transizione non è completa.</span><span class="sxs-lookup"><span data-stu-id="95a1f-116">Transition is not complete.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="95a1f-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="95a1f-117">Remarks</span></span>

<span data-ttu-id="95a1f-118">Questo metodo esegue l'override del metodo [**CBaseFilter::P ause**](cbasefilter-pause.md) .</span><span class="sxs-lookup"><span data-stu-id="95a1f-118">This method overrides the [**CBaseFilter::Pause**](cbasefilter-pause.md) method.</span></span> <span data-ttu-id="95a1f-119">Esegue i passaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="95a1f-119">It performs the following steps:</span></span>

-   <span data-ttu-id="95a1f-120">Chiama il metodo **CBaseFilter::P ause** .</span><span class="sxs-lookup"><span data-stu-id="95a1f-120">Calls the **CBaseFilter::Pause** method.</span></span>
-   <span data-ttu-id="95a1f-121">Viene eseguito il commit dell'allocatore.</span><span class="sxs-lookup"><span data-stu-id="95a1f-121">Commits the allocator.</span></span> <span data-ttu-id="95a1f-122">Vedere [**IMemAllocator:: commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit).</span><span class="sxs-lookup"><span data-stu-id="95a1f-122">(See [**IMemAllocator::Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit).)</span></span>
-   <span data-ttu-id="95a1f-123">Se lo stato precedente è stato interrotto, il filtro rilascia tutti i campioni che contiene.</span><span class="sxs-lookup"><span data-stu-id="95a1f-123">If the previous state was stopped, the filter releases any sample it is holding.</span></span> <span data-ttu-id="95a1f-124">(L'esempio non è più valido).</span><span class="sxs-lookup"><span data-stu-id="95a1f-124">(The sample is no longer valid.)</span></span>
-   <span data-ttu-id="95a1f-125">Chiama il metodo [**CBaseRenderer:: CompleteStateChange**](cbaserenderer-completestatechange.md) e restituisce il valore.</span><span class="sxs-lookup"><span data-stu-id="95a1f-125">Calls the [**CBaseRenderer::CompleteStateChange**](cbaserenderer-completestatechange.md) method and returns the value.</span></span>

## <a name="requirements"></a><span data-ttu-id="95a1f-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="95a1f-126">Requirements</span></span>



| <span data-ttu-id="95a1f-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="95a1f-127">Requirement</span></span> | <span data-ttu-id="95a1f-128">Valore</span><span class="sxs-lookup"><span data-stu-id="95a1f-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95a1f-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="95a1f-129">Header</span></span><br/>  | <dl> <span data-ttu-id="95a1f-130"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="95a1f-130"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="95a1f-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="95a1f-131">Library</span></span><br/> | <dl> <span data-ttu-id="95a1f-132"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="95a1f-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95a1f-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="95a1f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95a1f-134">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="95a1f-134">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




