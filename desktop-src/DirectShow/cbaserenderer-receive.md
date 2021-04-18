---
description: Il metodo Receive riceve il campione multimediale successivo nel flusso.
ms.assetid: b340f76c-2305-444f-bc00-1ef5acdea329
title: Metodo CBaseRenderer. Receive (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 96abb2ee3d44604c23e9943e086a52312a011e92
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333894"
---
# <a name="cbaserendererreceive-method"></a><span data-ttu-id="8e553-103">Metodo CBaseRenderer. Receive</span><span class="sxs-lookup"><span data-stu-id="8e553-103">CBaseRenderer.Receive method</span></span>

<span data-ttu-id="8e553-104">Il `Receive` metodo riceve il campione multimediale successivo nel flusso.</span><span class="sxs-lookup"><span data-stu-id="8e553-104">The `Receive` method receives the next media sample in the stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e553-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8e553-105">Syntax</span></span>


```C++
virtual Receive(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="8e553-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8e553-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e553-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="8e553-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="8e553-108">Puntatore all'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="8e553-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e553-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8e553-109">Return value</span></span>

<span data-ttu-id="8e553-110">Restituisce \_ OK se ha esito positivo o un valore **HRESULT** che indica la ragione dell'errore.</span><span class="sxs-lookup"><span data-stu-id="8e553-110">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e553-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="8e553-111">Remarks</span></span>

<span data-ttu-id="8e553-112">Il pin di input chiama questo metodo quando riceve un esempio dal filtro upstream.</span><span class="sxs-lookup"><span data-stu-id="8e553-112">The input pin calls this method when it receives a sample from the upstream filter.</span></span>

<span data-ttu-id="8e553-113">Se il filtro è in esecuzione, questo metodo esegue i passaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="8e553-113">If the filter is running, this method performs the following steps:</span></span>

1.  <span data-ttu-id="8e553-114">Pianifica l'esempio per il rendering ([**CBaseRenderer::P reparereceive**](cbaserenderer-preparereceive.md)).</span><span class="sxs-lookup"><span data-stu-id="8e553-114">Schedules the sample for rendering ([**CBaseRenderer::PrepareReceive**](cbaserenderer-preparereceive.md)).</span></span>
2.  <span data-ttu-id="8e553-115">Attende l'ora pianificata ([**CBaseRenderer:: WaitForRenderTime**](cbaserenderer-waitforrendertime.md)).</span><span class="sxs-lookup"><span data-stu-id="8e553-115">Waits for the scheduled time ([**CBaseRenderer::WaitForRenderTime**](cbaserenderer-waitforrendertime.md)).</span></span>
3.  <span data-ttu-id="8e553-116">Esegue il rendering dell'esempio ([**CBaseRenderer:: Render**](cbaserenderer-render.md)).</span><span class="sxs-lookup"><span data-stu-id="8e553-116">Renders the sample ([**CBaseRenderer::Render**](cbaserenderer-render.md)).</span></span>
4.  <span data-ttu-id="8e553-117">Rilascia l'esempio ([**CBaseRenderer:: ClearPendingSample**](cbaserenderer-clearpendingsample.md)).</span><span class="sxs-lookup"><span data-stu-id="8e553-117">Releases the sample ([**CBaseRenderer::ClearPendingSample**](cbaserenderer-clearpendingsample.md)).</span></span>

<span data-ttu-id="8e553-118">Se il filtro è sospeso, il metodo esegue i passaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="8e553-118">If the filter is paused, the method performs the following steps:</span></span>

1.  <span data-ttu-id="8e553-119">Notifica alla classe derivata che è disponibile un esempio ([**CBaseRenderer:: OnReceiveFirstSample**](cbaserenderer-onreceivefirstsample.md)).</span><span class="sxs-lookup"><span data-stu-id="8e553-119">Notifies the derived class that a sample is available ([**CBaseRenderer::OnReceiveFirstSample**](cbaserenderer-onreceivefirstsample.md)).</span></span>
2.  <span data-ttu-id="8e553-120">Attende l'ora pianificata.</span><span class="sxs-lookup"><span data-stu-id="8e553-120">Waits for the scheduled time.</span></span>
3.  <span data-ttu-id="8e553-121">Esegue il rendering dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="8e553-121">Renders the sample.</span></span>
4.  <span data-ttu-id="8e553-122">Rilascia l'esempio.</span><span class="sxs-lookup"><span data-stu-id="8e553-122">Releases the sample.</span></span>

<span data-ttu-id="8e553-123">Durante la pausa, il metodo attende nel passaggio 2 fino a quando il filtro passa a uno stato di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="8e553-123">While paused, the method waits in step 2 until the filter switches to a running state.</span></span> <span data-ttu-id="8e553-124">A questo punto, il filtro pianifica l'esempio.</span><span class="sxs-lookup"><span data-stu-id="8e553-124">At that point, the filter schedules the sample.</span></span>

<span data-ttu-id="8e553-125">Nella classe di base, il metodo **OnReceiveFirstSample** non esegue alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="8e553-125">In the base class, the **OnReceiveFirstSample** method does nothing.</span></span> <span data-ttu-id="8e553-126">La classe derivata può eseguire l'override.</span><span class="sxs-lookup"><span data-stu-id="8e553-126">The derived class can override it.</span></span> <span data-ttu-id="8e553-127">Ad esempio, quando un renderer video viene sospeso, viene visualizzato il primo campione come immagine ancora.</span><span class="sxs-lookup"><span data-stu-id="8e553-127">For example, when a video renderer is paused, it displays the first sample as a still image.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e553-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8e553-128">Requirements</span></span>



| <span data-ttu-id="8e553-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e553-129">Requirement</span></span> | <span data-ttu-id="8e553-130">Valore</span><span class="sxs-lookup"><span data-stu-id="8e553-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e553-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8e553-131">Header</span></span><br/>  | <dl> <span data-ttu-id="8e553-132"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8e553-132"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8e553-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="8e553-133">Library</span></span><br/> | <dl> <span data-ttu-id="8e553-134"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="8e553-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e553-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8e553-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e553-136">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="8e553-136">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




