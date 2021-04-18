---
description: Il metodo DoBufferProcessingLoop genera dati multimediali e li recapita al pin di input downstream.
ms.assetid: a8dce761-eed6-402d-9115-e21822d7a853
title: Metodo CSourceStream. DoBufferProcessingLoop (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.DoBufferProcessingLoop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 809694cacf0c30acf88ddf7d14c7f5ea1f654436
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329484"
---
# <a name="csourcestreamdobufferprocessingloop-method"></a><span data-ttu-id="09ef6-103">CSourceStream. DoBufferProcessingLoop, metodo</span><span class="sxs-lookup"><span data-stu-id="09ef6-103">CSourceStream.DoBufferProcessingLoop method</span></span>

<span data-ttu-id="09ef6-104">Il `DoBufferProcessingLoop` metodo genera dati multimediali e li recapita al pin di input downstream.</span><span class="sxs-lookup"><span data-stu-id="09ef6-104">The `DoBufferProcessingLoop` method generates media data and delivers it to the downstream input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="09ef6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="09ef6-105">Syntax</span></span>


```C++
virtual HRESULT DoBufferProcessingLoop();
```



## <a name="parameters"></a><span data-ttu-id="09ef6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="09ef6-106">Parameters</span></span>

<span data-ttu-id="09ef6-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="09ef6-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="09ef6-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="09ef6-108">Return value</span></span>

<span data-ttu-id="09ef6-109">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="09ef6-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="09ef6-110">I valori possibili includono quelli mostrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="09ef6-110">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="09ef6-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="09ef6-111">Return code</span></span>                                                                             | <span data-ttu-id="09ef6-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="09ef6-112">Description</span></span>                                                             |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="09ef6-113"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="09ef6-113"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="09ef6-114">Il thread ha ricevuto una richiesta di arresto.</span><span class="sxs-lookup"><span data-stu-id="09ef6-114">Thread received a stop request.</span></span><br/>                              |
| <dl> <span data-ttu-id="09ef6-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="09ef6-115"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="09ef6-116">Il flusso è terminato oppure il filtro downstream non accetta esempi.</span><span class="sxs-lookup"><span data-stu-id="09ef6-116">Stream ended, or downstream filter is not accepting samples.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="09ef6-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="09ef6-117">Remarks</span></span>

<span data-ttu-id="09ef6-118">Questo metodo implementa il ciclo principale che elabora i dati e li recapita a valle.</span><span class="sxs-lookup"><span data-stu-id="09ef6-118">This method implements the main loop that processes data and delivers it downstream.</span></span> <span data-ttu-id="09ef6-119">Ogni volta che viene attraversato il ciclo, il metodo recupera un esempio di supporto vuoto dall'allocatore.</span><span class="sxs-lookup"><span data-stu-id="09ef6-119">Each time through the loop, the method retrieves an empty media sample from the allocator.</span></span> <span data-ttu-id="09ef6-120">Passa l'esempio al metodo [**CSourceStream:: FillBuffer**](csourcestream-fillbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="09ef6-120">It passes the sample to the [**CSourceStream::FillBuffer**](csourcestream-fillbuffer.md) method.</span></span> <span data-ttu-id="09ef6-121">Il metodo **FillBuffer** , che deve essere implementato dalla classe derivata, genera dati multimediali e li inserisce nel buffer di esempio.</span><span class="sxs-lookup"><span data-stu-id="09ef6-121">The **FillBuffer** method, which the derived class must implement, generates media data and places it in the sample buffer.</span></span>

<span data-ttu-id="09ef6-122">Il ciclo termina quando si verifica una delle condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="09ef6-122">The loop ends when any of the following occurs:</span></span>

-   <span data-ttu-id="09ef6-123">Il metodo [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) del PIN di input rifiuta un campione.</span><span class="sxs-lookup"><span data-stu-id="09ef6-123">The input pin's [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method rejects a sample.</span></span>
-   <span data-ttu-id="09ef6-124">Il metodo **FillBuffer** restituisce \_ false, che indica la fine del flusso o restituisce un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="09ef6-124">The **FillBuffer** method returns S\_FALSE, indicating the end of the stream, or returns an error code.</span></span>
-   <span data-ttu-id="09ef6-125">Il thread riceve una richiesta [**CSourceStream:: Stop**](csourcestream-stop.md) .</span><span class="sxs-lookup"><span data-stu-id="09ef6-125">The thread receives a [**CSourceStream::Stop**](csourcestream-stop.md) request.</span></span>

<span data-ttu-id="09ef6-126">Il `DoBufferProcessingLoop` metodo gestisce la notifica di fine del flusso.</span><span class="sxs-lookup"><span data-stu-id="09ef6-126">The `DoBufferProcessingLoop` method handles the end-of-stream notification.</span></span> <span data-ttu-id="09ef6-127">Se si verifica un errore, viene inviato un evento [**EC \_ ERRORABORT**](ec-errorabort.md) al gestore del grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="09ef6-127">If an error occurs, it sends an [**EC\_ERRORABORT**](ec-errorabort.md) event to the filter graph manager.</span></span>

## <a name="requirements"></a><span data-ttu-id="09ef6-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="09ef6-128">Requirements</span></span>



| <span data-ttu-id="09ef6-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="09ef6-129">Requirement</span></span> | <span data-ttu-id="09ef6-130">Valore</span><span class="sxs-lookup"><span data-stu-id="09ef6-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09ef6-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="09ef6-131">Header</span></span><br/>  | <dl> <span data-ttu-id="09ef6-132"><dt>Source. h (Includi Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="09ef6-132"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="09ef6-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="09ef6-133">Library</span></span><br/> | <dl> <span data-ttu-id="09ef6-134"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="09ef6-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09ef6-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="09ef6-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09ef6-136">**Classe CSourceStream**</span><span class="sxs-lookup"><span data-stu-id="09ef6-136">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




