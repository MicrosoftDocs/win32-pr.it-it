---
description: Il metodo SourceThreadCanWait include o rilascia il thread di streaming.
ms.assetid: f68f5f0b-ef5b-49a9-a768-c4cc065c0cb3
title: Metodo CBaseRenderer. SourceThreadCanWait (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SourceThreadCanWait
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f01be304ec2b5f845ea61c9609808c6e2f39fca9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332996"
---
# <a name="cbaserenderersourcethreadcanwait-method"></a><span data-ttu-id="f5b00-103">CBaseRenderer. SourceThreadCanWait, metodo</span><span class="sxs-lookup"><span data-stu-id="f5b00-103">CBaseRenderer.SourceThreadCanWait method</span></span>

<span data-ttu-id="f5b00-104">Il `SourceThreadCanWait` metodo include o rilascia il thread di streaming.</span><span class="sxs-lookup"><span data-stu-id="f5b00-104">The `SourceThreadCanWait` method holds or releases the streaming thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5b00-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f5b00-105">Syntax</span></span>


```C++
virtual HRESULT SourceThreadCanWait(
   BOOL bCanWait
);
```



## <a name="parameters"></a><span data-ttu-id="f5b00-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f5b00-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5b00-107">*bCanWait*</span><span class="sxs-lookup"><span data-stu-id="f5b00-107">*bCanWait*</span></span> 
</dt> <dd>

<span data-ttu-id="f5b00-108">Valore booleano che indica se mantenere il thread di streaming.</span><span class="sxs-lookup"><span data-stu-id="f5b00-108">Boolean value indicating whether to hold the streaming thread.</span></span> <span data-ttu-id="f5b00-109">Se **true**, il thread di streaming viene bloccato mentre il filtro attende il rendering degli esempi successivi.</span><span class="sxs-lookup"><span data-stu-id="f5b00-109">If **TRUE**, the streaming thread is blocked while the filter waits to render the next samples.</span></span> <span data-ttu-id="f5b00-110">Se **false**, il thread di streaming viene rilasciato.</span><span class="sxs-lookup"><span data-stu-id="f5b00-110">If **FALSE**, the streaming thread is released.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5b00-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f5b00-111">Return value</span></span>

<span data-ttu-id="f5b00-112">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f5b00-112">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5b00-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="f5b00-113">Remarks</span></span>

<span data-ttu-id="f5b00-114">La chiamata al `SourceThreadCanWait` metodo con il valore **false** impone il ritorno del filtro da una chiamata [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) bloccata.</span><span class="sxs-lookup"><span data-stu-id="f5b00-114">Calling the `SourceThreadCanWait` method with the value **FALSE** forces the filter to return from a blocked [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) call.</span></span> <span data-ttu-id="f5b00-115">Quando il filtro è in esecuzione, blocca le chiamate di **ricezione** fino al momento della presentazione del campione corrente.</span><span class="sxs-lookup"><span data-stu-id="f5b00-115">When the filter is running, it blocks **Receive** calls until the current sample's presentation time.</span></span> <span data-ttu-id="f5b00-116">Quando il filtro è sospeso, blocca la **ricezione** delle chiamate a tempo indefinito.</span><span class="sxs-lookup"><span data-stu-id="f5b00-116">When the filter is paused, it blocks **Receive** calls indefinitely.</span></span> <span data-ttu-id="f5b00-117">Questo comportamento regola il flusso di dati nel flusso.</span><span class="sxs-lookup"><span data-stu-id="f5b00-117">This behavior regulates the flow of data in the stream.</span></span> <span data-ttu-id="f5b00-118">Quando il filtro viene arrestato o scaricato, tuttavia, non deve essere bloccato.</span><span class="sxs-lookup"><span data-stu-id="f5b00-118">When the filter is stopped or flushing, however, it should not block.</span></span>

<span data-ttu-id="f5b00-119">Il blocco è controllato dal metodo [**CBaseRenderer:: WaitForRenderTime**](cbaserenderer-waitforrendertime.md) , che attende due eventi: [**CBaseRenderer:: m \_ RenderEvent**](cbaserenderer-m-renderevent.md) e [**CBaseRenderer:: m \_ ThreadSignal**](cbaserenderer-m-threadsignal.md).</span><span class="sxs-lookup"><span data-stu-id="f5b00-119">The blocking is controlled by the [**CBaseRenderer::WaitForRenderTime**](cbaserenderer-waitforrendertime.md) method, which waits on two events: [**CBaseRenderer::m\_RenderEvent**](cbaserenderer-m-renderevent.md) and [**CBaseRenderer::m\_ThreadSignal**](cbaserenderer-m-threadsignal.md).</span></span> <span data-ttu-id="f5b00-120">L' **evento \_ RenderEvent m** viene segnalato all'arrivo dell'ora di presentazione.</span><span class="sxs-lookup"><span data-stu-id="f5b00-120">The **m\_RenderEvent** event is signaled when the presentation time arrives.</span></span> <span data-ttu-id="f5b00-121">L' **evento \_ ThreadSignal m** viene segnalato quando `SourceThreadCanWait` viene chiamato con il valore **false**.</span><span class="sxs-lookup"><span data-stu-id="f5b00-121">The **m\_ThreadSignal** event is signaled when `SourceThreadCanWait` is called with the value **FALSE**.</span></span> <span data-ttu-id="f5b00-122">Se viene chiamato `SourceThreadCanWait` con il valore **true** , viene reimpostato l'evento.</span><span class="sxs-lookup"><span data-stu-id="f5b00-122">Calling `SourceThreadCanWait` with the value **TRUE** resets the event.</span></span>

<span data-ttu-id="f5b00-123">I metodi [**CBaseRenderer:: Stop**](cbaserenderer-stop.md) e [**CBaseRenderer:: BeginFlush**](cbaserenderer-beginflush.md) chiamano `SourceThreadCanWait` con il valore **false** (che rilascia il thread di streaming).</span><span class="sxs-lookup"><span data-stu-id="f5b00-123">The [**CBaseRenderer::Stop**](cbaserenderer-stop.md) and [**CBaseRenderer::BeginFlush**](cbaserenderer-beginflush.md) methods call `SourceThreadCanWait` with the value **FALSE** (releasing the streaming thread).</span></span> <span data-ttu-id="f5b00-124">I metodi [**CBaseRenderer::P ause**](cbaserenderer-pause.md), [**CBaseRenderer:: Run**](cbaserenderer-run.md)e [**CBaseRenderer:: EndFlush**](cbaserenderer-endflush.md) chiamano `SourceThreadCanWait` con il valore **true**.</span><span class="sxs-lookup"><span data-stu-id="f5b00-124">The [**CBaseRenderer::Pause**](cbaserenderer-pause.md), [**CBaseRenderer::Run**](cbaserenderer-run.md), and [**CBaseRenderer::EndFlush**](cbaserenderer-endflush.md) methods call `SourceThreadCanWait` with the value **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5b00-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f5b00-125">Requirements</span></span>



| <span data-ttu-id="f5b00-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5b00-126">Requirement</span></span> | <span data-ttu-id="f5b00-127">Valore</span><span class="sxs-lookup"><span data-stu-id="f5b00-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5b00-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f5b00-128">Header</span></span><br/>  | <dl> <span data-ttu-id="f5b00-129"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f5b00-129"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f5b00-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="f5b00-130">Library</span></span><br/> | <dl> <span data-ttu-id="f5b00-131"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f5b00-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5b00-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f5b00-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5b00-133">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="f5b00-133">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




