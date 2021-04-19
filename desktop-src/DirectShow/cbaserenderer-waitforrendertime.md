---
description: Il metodo WaitForRenderTime attende l'ora di presentazione dell'esempio corrente.
ms.assetid: a6acb780-48df-4f73-adcb-cfa4e54b19ac
title: Metodo CBaseRenderer. WaitForRenderTime (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.WaitForRenderTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 43a537728ca0874fa1dfd69b4712bcc97cf23850
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324193"
---
# <a name="cbaserendererwaitforrendertime-method"></a><span data-ttu-id="3696b-103">CBaseRenderer. WaitForRenderTime, metodo</span><span class="sxs-lookup"><span data-stu-id="3696b-103">CBaseRenderer.WaitForRenderTime method</span></span>

<span data-ttu-id="3696b-104">Il `WaitForRenderTime` metodo attende l'ora di presentazione dell'esempio corrente.</span><span class="sxs-lookup"><span data-stu-id="3696b-104">The `WaitForRenderTime` method waits for the current sample's presentation time.</span></span>

## <a name="syntax"></a><span data-ttu-id="3696b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3696b-105">Syntax</span></span>


```C++
virtual HRESULT WaitForRenderTime();
```



## <a name="parameters"></a><span data-ttu-id="3696b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3696b-106">Parameters</span></span>

<span data-ttu-id="3696b-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="3696b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3696b-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3696b-108">Return value</span></span>

<span data-ttu-id="3696b-109">Restituisce uno dei seguenti valori **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3696b-109">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="3696b-110">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="3696b-110">Return code</span></span>                                                                                           | <span data-ttu-id="3696b-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3696b-111">Description</span></span>                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3696b-112"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3696b-112"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="3696b-113">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="3696b-113">Success.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="3696b-114"><dt>**stato di VFW \_ E \_ \_ modificato**</dt></span><span class="sxs-lookup"><span data-stu-id="3696b-114"><dt>**VFW\_E\_STATE\_CHANGED**</dt></span></span> </dl> | <span data-ttu-id="3696b-115">Lo stato del filtro è stato modificato prima dell'arrivo dell'ora di presentazione.</span><span class="sxs-lookup"><span data-stu-id="3696b-115">The filter state changed before the presentation time arrived.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3696b-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="3696b-116">Remarks</span></span>

<span data-ttu-id="3696b-117">Questo metodo attende fino a quando si verifica una delle condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="3696b-117">This method waits until one of the following occurs:</span></span>

-   <span data-ttu-id="3696b-118">Il tempo di presentazione dell'esempio arriva, a quel punto è possibile eseguire il rendering dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="3696b-118">The sample's presentation time arrives, at which point the sample can be rendered.</span></span>
-   <span data-ttu-id="3696b-119">Il filtro interrompe o inizia a scaricare i dati.</span><span class="sxs-lookup"><span data-stu-id="3696b-119">The filter stops or begins flushing data.</span></span>

<span data-ttu-id="3696b-120">Se l'ora di presentazione arriva, viene segnalato l'evento [**CBaseRenderer:: m \_ RenderEvent**](cbaserenderer-m-renderevent.md) .</span><span class="sxs-lookup"><span data-stu-id="3696b-120">If the presentation time arrives, the [**CBaseRenderer::m\_RenderEvent**](cbaserenderer-m-renderevent.md) event is signaled.</span></span> <span data-ttu-id="3696b-121">Se lo stato viene modificato, viene segnalato l'evento [**CBaseRenderer:: m \_ ThreadSignal**](cbaserenderer-m-threadsignal.md) .</span><span class="sxs-lookup"><span data-stu-id="3696b-121">If the state changes, the [**CBaseRenderer::m\_ThreadSignal**](cbaserenderer-m-threadsignal.md) event is signaled.</span></span> <span data-ttu-id="3696b-122">Questo metodo attende entrambi gli eventi.</span><span class="sxs-lookup"><span data-stu-id="3696b-122">This method waits on both events.</span></span> <span data-ttu-id="3696b-123">La classe derivata può eseguire l'override di questo metodo per attendere eventi aggiuntivi, se necessario.</span><span class="sxs-lookup"><span data-stu-id="3696b-123">The derived class can override this method to wait on additional events, if necessary.</span></span>

<span data-ttu-id="3696b-124">Questo metodo chiama il metodo [**CBaseRenderer:: OnWaitStart**](cbaserenderer-onwaitstart.md) all'inizio dell'attesa e il metodo [**CBaseRenderer:: OnWaitEnd**](cbaserenderer-onwaitend.md) al termine dell'attesa.</span><span class="sxs-lookup"><span data-stu-id="3696b-124">This method calls the [**CBaseRenderer::OnWaitStart**](cbaserenderer-onwaitstart.md) method when the wait begins, and the [**CBaseRenderer::OnWaitEnd**](cbaserenderer-onwaitend.md) method when the wait is done.</span></span> <span data-ttu-id="3696b-125">Nessuno dei due metodi esegue alcuna operazione nella classe di base, ma la classe derivata può eseguirne l'override.</span><span class="sxs-lookup"><span data-stu-id="3696b-125">Neither method does anything in the base class, but the derived class can override them.</span></span>

## <a name="requirements"></a><span data-ttu-id="3696b-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3696b-126">Requirements</span></span>



| <span data-ttu-id="3696b-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="3696b-127">Requirement</span></span> | <span data-ttu-id="3696b-128">Valore</span><span class="sxs-lookup"><span data-stu-id="3696b-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3696b-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3696b-129">Header</span></span><br/>  | <dl> <span data-ttu-id="3696b-130"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3696b-130"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3696b-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="3696b-131">Library</span></span><br/> | <dl> <span data-ttu-id="3696b-132"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="3696b-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3696b-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3696b-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3696b-134">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="3696b-134">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




