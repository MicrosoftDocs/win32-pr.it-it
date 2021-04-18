---
description: Questa classe implementa l'interfaccia IAMStreamControl per i pin di input e di output.
ms.assetid: a0ddc2d5-8385-4209-b1c5-9822c30f8a02
title: Classe CBaseStreamControl (Strmctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c20a4f08040bdb2c71bdd8f09aa657719228efa5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326937"
---
# <a name="cbasestreamcontrol-class"></a><span data-ttu-id="c935e-103">Classe CBaseStreamControl</span><span class="sxs-lookup"><span data-stu-id="c935e-103">CBaseStreamControl class</span></span>

![gerarchia di classi cbasestreamcontrol](images/strmctl1.png)

<span data-ttu-id="c935e-105">Questa classe implementa l'interfaccia [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) per i pin di input e di output.</span><span class="sxs-lookup"><span data-stu-id="c935e-105">This class implements the [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) interface for input and output pins.</span></span> <span data-ttu-id="c935e-106">Consente di controllare l'avvio e l'arresto di un singolo pin sul filtro.</span><span class="sxs-lookup"><span data-stu-id="c935e-106">It provides control over starting and stopping an individual pin on the filter.</span></span> <span data-ttu-id="c935e-107">Un pin che supporta **IAMStreamControl** deve ereditare da questa classe di base.</span><span class="sxs-lookup"><span data-stu-id="c935e-107">A pin that supports **IAMStreamControl** should inherit from this base class.</span></span> <span data-ttu-id="c935e-108">Di seguito è riportata una dichiarazione tipica per un pin di input:</span><span class="sxs-lookup"><span data-stu-id="c935e-108">The following is a typical declaration for an input pin:</span></span>

``` syntax
class CMyInputPin : public CBaseInputPin, public CBaseStreamControl
```

<span data-ttu-id="c935e-109">Assicurarsi di eseguire l'override di **NonDelegatingQueryInteface** per esporre **IAMStreamControl**.</span><span class="sxs-lookup"><span data-stu-id="c935e-109">Be sure to override **NonDelegatingQueryInteface** to expose **IAMStreamControl**.</span></span> <span data-ttu-id="c935e-110">Per ulteriori informazioni, vedere [How to implement IUnknown](how-to-implement-iunknown.md).</span><span class="sxs-lookup"><span data-stu-id="c935e-110">For more information, see [How to Implement IUnknown](how-to-implement-iunknown.md).</span></span>



| <span data-ttu-id="c935e-111">Metodi pubblici</span><span class="sxs-lookup"><span data-stu-id="c935e-111">Public Methods</span></span>                                                        | <span data-ttu-id="c935e-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c935e-112">Description</span></span>                                                                                          |
|-----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c935e-113">**CBaseStreamControl**</span><span class="sxs-lookup"><span data-stu-id="c935e-113">**CBaseStreamControl**</span></span>](cbasestreamcontrol-cbasestreamcontrol.md)   | <span data-ttu-id="c935e-114">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="c935e-114">Constructor method.</span></span>                                                                                  |
| [<span data-ttu-id="c935e-115">**~ CBaseStreamControl**</span><span class="sxs-lookup"><span data-stu-id="c935e-115">**~CBaseStreamControl**</span></span>](cbasestreamcontrol--cbasestreamcontrol.md) | <span data-ttu-id="c935e-116">Metodo del distruttore.</span><span class="sxs-lookup"><span data-stu-id="c935e-116">Destructor method.</span></span>                                                                                   |
| [<span data-ttu-id="c935e-117">**CheckStreamState**</span><span class="sxs-lookup"><span data-stu-id="c935e-117">**CheckStreamState**</span></span>](cbasestreamcontrol-checkstreamstate.md)       | <span data-ttu-id="c935e-118">Determina se un campione multimediale deve essere recapitato o rimosso.</span><span class="sxs-lookup"><span data-stu-id="c935e-118">Determines whether a media sample should be delivered or discarded.</span></span>                                  |
| [<span data-ttu-id="c935e-119">**Flushing**</span><span class="sxs-lookup"><span data-stu-id="c935e-119">**Flushing**</span></span>](cbasestreamcontrol-flushing.md)                       | <span data-ttu-id="c935e-120">Notifica alla classe di base che il pin ha avviato o interrotto lo svuotamento.</span><span class="sxs-lookup"><span data-stu-id="c935e-120">Notifies the base class that the pin has started or stopped flushing.</span></span>                                |
| [<span data-ttu-id="c935e-121">**NotifyFilterState**</span><span class="sxs-lookup"><span data-stu-id="c935e-121">**NotifyFilterState**</span></span>](cbasestreamcontrol-notifyfilterstate.md)     | <span data-ttu-id="c935e-122">Notifica al pin quando lo stato del filtro viene modificato.</span><span class="sxs-lookup"><span data-stu-id="c935e-122">Notifies the pin when the filter's state changes.</span></span>                                                    |
| [<span data-ttu-id="c935e-123">**SetFilterGraph**</span><span class="sxs-lookup"><span data-stu-id="c935e-123">**SetFilterGraph**</span></span>](cbasestreamcontrol-setfiltergraph.md)           | <span data-ttu-id="c935e-124">Specifica il sink di evento per gli eventi di controllo di flusso.</span><span class="sxs-lookup"><span data-stu-id="c935e-124">Specifies the event sink for stream control events.</span></span>                                                  |
| [<span data-ttu-id="c935e-125">**SetSyncSource**</span><span class="sxs-lookup"><span data-stu-id="c935e-125">**SetSyncSource**</span></span>](cbasestreamcontrol-setsyncsource.md)             | <span data-ttu-id="c935e-126">Notifica alla classe di base l'orologio di riferimento corrente.</span><span class="sxs-lookup"><span data-stu-id="c935e-126">Notifies the base class of the current reference clock.</span></span>                                              |
| <span data-ttu-id="c935e-127">Metodi IAMStreamControl</span><span class="sxs-lookup"><span data-stu-id="c935e-127">IAMStreamControl Methods</span></span>                                              | <span data-ttu-id="c935e-128">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c935e-128">Description</span></span>                                                                                          |
| [<span data-ttu-id="c935e-129">**GetInfo**</span><span class="sxs-lookup"><span data-stu-id="c935e-129">**GetInfo**</span></span>](cbasestreamcontrol-getinfo.md)                         | <span data-ttu-id="c935e-130">Recupera le informazioni sulle impostazioni correnti del controllo del flusso, incluse le ore di inizio e di fine.</span><span class="sxs-lookup"><span data-stu-id="c935e-130">Retrieves information about the current stream-control settings, including the start and stop times.</span></span> |
| [<span data-ttu-id="c935e-131">**StartAt**</span><span class="sxs-lookup"><span data-stu-id="c935e-131">**StartAt**</span></span>](cbasestreamcontrol-startat.md)                         | <span data-ttu-id="c935e-132">Informa il PIN quando iniziare a consegnare i dati.</span><span class="sxs-lookup"><span data-stu-id="c935e-132">Informs the pin when to start delivering data.</span></span>                                                       |
| [<span data-ttu-id="c935e-133">**StopAt**</span><span class="sxs-lookup"><span data-stu-id="c935e-133">**StopAt**</span></span>](cbasestreamcontrol-stopat.md)                           | <span data-ttu-id="c935e-134">Informa il PIN quando interrompere la distribuzione dei dati.</span><span class="sxs-lookup"><span data-stu-id="c935e-134">Informs the pin when to stop delivering data.</span></span>                                                        |



 

## <a name="remarks"></a><span data-ttu-id="c935e-135">Commenti</span><span class="sxs-lookup"><span data-stu-id="c935e-135">Remarks</span></span>

<span data-ttu-id="c935e-136">Questa classe richiede il PIN e il filtro proprietario per notificare alla classe quando si verificano vari eventi, ad esempio il filtro che aggiunge il grafo o riceve un nuovo Clock di riferimento.</span><span class="sxs-lookup"><span data-stu-id="c935e-136">This class requires the pin and the owning filter to notify the class when various events occur, such as the filter joining the graph or receiving a new reference clock.</span></span> <span data-ttu-id="c935e-137">È necessario chiamare i metodi della classe seguenti:</span><span class="sxs-lookup"><span data-stu-id="c935e-137">You should call the following class methods:</span></span>

-   <span data-ttu-id="c935e-138">Nel metodo [**IMediaFilter:: SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) del filtro chiamare il metodo [**CBaseStreamControl:: SetSyncSource**](cbasestreamcontrol-setsyncsource.md) .</span><span class="sxs-lookup"><span data-stu-id="c935e-138">In the filter's [**IMediaFilter::SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) method, call the [**CBaseStreamControl::SetSyncSource**](cbasestreamcontrol-setsyncsource.md) method.</span></span> <span data-ttu-id="c935e-139">Questo metodo notifica alla classe l'orologio di riferimento corrente.</span><span class="sxs-lookup"><span data-stu-id="c935e-139">This method notifies the class of the current reference clock.</span></span>
-   <span data-ttu-id="c935e-140">Nel metodo [**CBaseFilter:: JoinFilterGraph**](cbasefilter-joinfiltergraph.md) del filtro chiamare il metodo [**CBaseStreamControl:: SetFilterGraph**](cbasestreamcontrol-setfiltergraph.md) .</span><span class="sxs-lookup"><span data-stu-id="c935e-140">In the filter's [**CBaseFilter::JoinFilterGraph**](cbasefilter-joinfiltergraph.md) method, call the [**CBaseStreamControl::SetFilterGraph**](cbasestreamcontrol-setfiltergraph.md) method.</span></span> <span data-ttu-id="c935e-141">Questo metodo assegna alla classe un puntatore al gestore del grafico dei filtri, in modo che la classe possa inviare gli eventi di controllo di flusso corretti.</span><span class="sxs-lookup"><span data-stu-id="c935e-141">This method gives the class a pointer to the Filter Graph Manager, so that the class can send the right stream-control events.</span></span>
-   <span data-ttu-id="c935e-142">Ogni volta che il filtro cambia stato (in esecuzione, in pausa o arrestato), chiamare il metodo [**CBaseStreamControl:: NotifyFilterState**](cbasestreamcontrol-notifyfilterstate.md) .</span><span class="sxs-lookup"><span data-stu-id="c935e-142">Whenever the filter changes state (to running, paused, or stopped), call the [**CBaseStreamControl::NotifyFilterState**](cbasestreamcontrol-notifyfilterstate.md) method.</span></span>
-   <span data-ttu-id="c935e-143">Nei metodi [**Ipin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) e [**Ipin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) del pin chiamare il metodo [**CBaseStreamControl:: Flushing**](cbasestreamcontrol-flushing.md) .</span><span class="sxs-lookup"><span data-stu-id="c935e-143">In the pin's [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) and [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) methods, call the [**CBaseStreamControl::Flushing**](cbasestreamcontrol-flushing.md) method.</span></span>

<span data-ttu-id="c935e-144">La `CBaseStreamControl` classe usa l'orologio di riferimento del grafo del filtro per determinare quali campioni devono essere recapitati dal filtro e quali devono essere rimossi.</span><span class="sxs-lookup"><span data-stu-id="c935e-144">The `CBaseStreamControl` class uses the filter graph's reference clock to determine which samples the filter should be deliver, and which it should discard.</span></span> <span data-ttu-id="c935e-145">Nel metodo [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) del pin chiamare il metodo [**CBaseStreamControl:: CheckStreamState**](cbasestreamcontrol-checkstreamstate.md) con un puntatore all'esempio di supporto in entrata.</span><span class="sxs-lookup"><span data-stu-id="c935e-145">In your pin's [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method, call the [**CBaseStreamControl::CheckStreamState**](cbasestreamcontrol-checkstreamstate.md) method with a pointer to the incoming media sample.</span></span> <span data-ttu-id="c935e-146">Se il metodo restituisce il flusso del flusso \_ di valori, fornire l'esempio downstream.</span><span class="sxs-lookup"><span data-stu-id="c935e-146">If the method returns the value STREAM\_FLOWING, deliver the sample downstream.</span></span> <span data-ttu-id="c935e-147">In caso contrario, eliminarlo.</span><span class="sxs-lookup"><span data-stu-id="c935e-147">Otherwise, discard it.</span></span>

## <a name="requirements"></a><span data-ttu-id="c935e-148">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c935e-148">Requirements</span></span>



| <span data-ttu-id="c935e-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="c935e-149">Requirement</span></span> | <span data-ttu-id="c935e-150">Valore</span><span class="sxs-lookup"><span data-stu-id="c935e-150">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c935e-151">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c935e-151">Header</span></span><br/>  | <dl> <span data-ttu-id="c935e-152"><dt>Strmctl. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c935e-152"><dt>Strmctl.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c935e-153">Libreria</span><span class="sxs-lookup"><span data-stu-id="c935e-153">Library</span></span><br/> | <dl> <span data-ttu-id="c935e-154"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="c935e-154"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




