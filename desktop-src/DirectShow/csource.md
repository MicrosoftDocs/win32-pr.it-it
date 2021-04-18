---
description: La classe CSource è una classe di base per l'implementazione dei filtri di origine. Un filtro derivato da CSource contiene uno o più pin di output derivati dalla classe CSourceStream. Ogni pin di output crea un thread di lavoro che esegue il push degli esempi di supporti downstream.
ms.assetid: 25bd0334-4ad1-48ed-93f9-b36c13a280a3
title: Classe CSource (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a4fcecbd1973c54e30c9bf1251bed174aa4a469f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329362"
---
# <a name="csource-class"></a><span data-ttu-id="654f9-105">Classe CSource</span><span class="sxs-lookup"><span data-stu-id="654f9-105">CSource class</span></span>

![gerarchia di classi CSource](images/source01.png)

<span data-ttu-id="654f9-107">La classe **CSource** è una classe di base per l'implementazione dei filtri di origine.</span><span class="sxs-lookup"><span data-stu-id="654f9-107">The **CSource** class is a base class for implementing source filters.</span></span> <span data-ttu-id="654f9-108">Un filtro derivato da **CSource** contiene uno o più pin di output derivati dalla classe [**CSourceStream**](csourcestream.md) .</span><span class="sxs-lookup"><span data-stu-id="654f9-108">A filter derived from **CSource** contains one or more output pins derived from the [**CSourceStream**](csourcestream.md) class.</span></span> <span data-ttu-id="654f9-109">Ogni pin di output crea un thread di lavoro che esegue il push degli esempi di supporti downstream.</span><span class="sxs-lookup"><span data-stu-id="654f9-109">Each output pin creates a worker thread that pushes media samples downstream.</span></span>

> [!Note]  
> <span data-ttu-id="654f9-110">La classe **CSource** è progettata per supportare il modello push per il flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="654f9-110">The **CSource** class is designed to support the push model for data flow.</span></span> <span data-ttu-id="654f9-111">Questa classe non è consigliata per la creazione di filtri di lettura file.</span><span class="sxs-lookup"><span data-stu-id="654f9-111">This class is not recommended for creating file-reader filters.</span></span> <span data-ttu-id="654f9-112">I lettori di file devono supportare il modello pull tramite l'interfaccia [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) .</span><span class="sxs-lookup"><span data-stu-id="654f9-112">File readers should support the pull model, through the [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) interface.</span></span> <span data-ttu-id="654f9-113">Per ulteriori informazioni, vedere [flusso di dati per gli sviluppatori di filtri](data-flow-for-filter-developers.md).</span><span class="sxs-lookup"><span data-stu-id="654f9-113">For more information, see [Data Flow for Filter Developers](data-flow-for-filter-developers.md).</span></span>

 



| <span data-ttu-id="654f9-114">Variabili membro protette</span><span class="sxs-lookup"><span data-stu-id="654f9-114">Protected Member Variables</span></span>                     | <span data-ttu-id="654f9-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="654f9-115">Description</span></span>                                                  |
|------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="654f9-116">**\_iPins m**</span><span class="sxs-lookup"><span data-stu-id="654f9-116">**m\_iPins**</span></span>](csource-m-ipins.md)            | <span data-ttu-id="654f9-117">Numero di pin sul filtro.</span><span class="sxs-lookup"><span data-stu-id="654f9-117">Number of pins on the filter.</span></span>                                |
| [<span data-ttu-id="654f9-118">**\_paStreams m**</span><span class="sxs-lookup"><span data-stu-id="654f9-118">**m\_paStreams**</span></span>](csource-m-pastreams.md)    | <span data-ttu-id="654f9-119">Matrice di pin.</span><span class="sxs-lookup"><span data-stu-id="654f9-119">Array of pins.</span></span>                                               |
| [<span data-ttu-id="654f9-120">**\_cStateLock m**</span><span class="sxs-lookup"><span data-stu-id="654f9-120">**m\_cStateLock**</span></span>](csource-m-cstatelock.md)  | <span data-ttu-id="654f9-121">Oggetto sezione critica che protegge lo stato del filtro.</span><span class="sxs-lookup"><span data-stu-id="654f9-121">Critical section object that protects the filter state.</span></span>      |
| <span data-ttu-id="654f9-122">Metodi pubblici</span><span class="sxs-lookup"><span data-stu-id="654f9-122">Public Methods</span></span>                                 | <span data-ttu-id="654f9-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="654f9-123">Description</span></span>                                                  |
| [<span data-ttu-id="654f9-124">**CSource**</span><span class="sxs-lookup"><span data-stu-id="654f9-124">**CSource**</span></span>](csource-csource.md)             | <span data-ttu-id="654f9-125">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="654f9-125">Constructor method.</span></span>                                          |
| [<span data-ttu-id="654f9-126">**~ CSource**</span><span class="sxs-lookup"><span data-stu-id="654f9-126">**~CSource**</span></span>](csource--csource.md)           | <span data-ttu-id="654f9-127">Metodo del distruttore.</span><span class="sxs-lookup"><span data-stu-id="654f9-127">Destructor method.</span></span>                                           |
| [<span data-ttu-id="654f9-128">**GetPinCount**</span><span class="sxs-lookup"><span data-stu-id="654f9-128">**GetPinCount**</span></span>](csource-getpincount.md)     | <span data-ttu-id="654f9-129">Recupera il numero di pin sul filtro.</span><span class="sxs-lookup"><span data-stu-id="654f9-129">Retrieves the number of pins on the filter.</span></span>                  |
| [<span data-ttu-id="654f9-130">**GetPin**</span><span class="sxs-lookup"><span data-stu-id="654f9-130">**GetPin**</span></span>](csource-getpin.md)               | <span data-ttu-id="654f9-131">Recupera un PIN.</span><span class="sxs-lookup"><span data-stu-id="654f9-131">Retrieves a pin.</span></span>                                             |
| [<span data-ttu-id="654f9-132">**pStateLock**</span><span class="sxs-lookup"><span data-stu-id="654f9-132">**pStateLock**</span></span>](csource--pstatelock.md)      | <span data-ttu-id="654f9-133">Recupera un puntatore all'oggetto sezione critica del filtro.</span><span class="sxs-lookup"><span data-stu-id="654f9-133">Retrieves a pointer to the filter's critical section object.</span></span> |
| [<span data-ttu-id="654f9-134">**AddPin**</span><span class="sxs-lookup"><span data-stu-id="654f9-134">**AddPin**</span></span>](csource-addpin.md)               | <span data-ttu-id="654f9-135">Aggiunge un nuovo PIN di output al filtro.</span><span class="sxs-lookup"><span data-stu-id="654f9-135">Adds a new output pin to the filter.</span></span>                         |
| [<span data-ttu-id="654f9-136">**RemovePin**</span><span class="sxs-lookup"><span data-stu-id="654f9-136">**RemovePin**</span></span>](csource-removepin.md)         | <span data-ttu-id="654f9-137">Rimuove un PIN specificato dal filtro.</span><span class="sxs-lookup"><span data-stu-id="654f9-137">Removes a specified pin from the filter.</span></span>                     |
| [<span data-ttu-id="654f9-138">**FindPinNumber**</span><span class="sxs-lookup"><span data-stu-id="654f9-138">**FindPinNumber**</span></span>](csource-findpinnumber.md) | <span data-ttu-id="654f9-139">Recupera il numero di un PIN specificato sul filtro.</span><span class="sxs-lookup"><span data-stu-id="654f9-139">Retrieves the number of a specified pin on the filter.</span></span>       |
| <span data-ttu-id="654f9-140">Metodi IBaseFilter</span><span class="sxs-lookup"><span data-stu-id="654f9-140">IBaseFilter Methods</span></span>                            | <span data-ttu-id="654f9-141">Descrizione</span><span class="sxs-lookup"><span data-stu-id="654f9-141">Description</span></span>                                                  |
| [<span data-ttu-id="654f9-142">**FindPin**</span><span class="sxs-lookup"><span data-stu-id="654f9-142">**FindPin**</span></span>](csource-findpin.md)             | <span data-ttu-id="654f9-143">Recupera il pin con l'identificatore specificato.</span><span class="sxs-lookup"><span data-stu-id="654f9-143">Retrieves the pin with the specified identifier.</span></span>             |



 

## <a name="remarks"></a><span data-ttu-id="654f9-144">Commenti</span><span class="sxs-lookup"><span data-stu-id="654f9-144">Remarks</span></span>

<span data-ttu-id="654f9-145">Per implementare un pin di output, procedere come segue:</span><span class="sxs-lookup"><span data-stu-id="654f9-145">To implement an output pin, do the following:</span></span>

-   <span data-ttu-id="654f9-146">Derivare una classe da [**CSourceStream**](csourcestream.md).</span><span class="sxs-lookup"><span data-stu-id="654f9-146">Derive a class from [**CSourceStream**](csourcestream.md).</span></span>
-   <span data-ttu-id="654f9-147">Eseguire l'override del metodo [**CSourceStream:: GetMediaType**](csourcestream-getmediatype.md) ed eventualmente del metodo [**CSourceStream:: CheckMediaType**](csourcestream-checkmediatype.md) , che convalida i tipi di supporto per il PIN.</span><span class="sxs-lookup"><span data-stu-id="654f9-147">Override the [**CSourceStream::GetMediaType**](csourcestream-getmediatype.md) method and possibly the [**CSourceStream::CheckMediaType**](csourcestream-checkmediatype.md) method, which validate media types for the pin.</span></span>
-   <span data-ttu-id="654f9-148">Implementare il metodo [**CBaseOutputPin::D ecidebuffersize**](cbaseoutputpin-decidebuffersize.md) , che restituisce i requisiti del buffer del PIN.</span><span class="sxs-lookup"><span data-stu-id="654f9-148">Implement the [**CBaseOutputPin::DecideBufferSize**](cbaseoutputpin-decidebuffersize.md) method, which returns the pin's buffer requirements.</span></span>
-   <span data-ttu-id="654f9-149">Implementare il metodo [**CSourceStream:: FillBuffer**](csourcestream-fillbuffer.md) , che compila un buffer di esempio multimediale con i dati.</span><span class="sxs-lookup"><span data-stu-id="654f9-149">Implement the [**CSourceStream::FillBuffer**](csourcestream-fillbuffer.md) method, which fills a media sample buffer with data.</span></span>

<span data-ttu-id="654f9-150">Per implementare il filtro, eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="654f9-150">To implement the filter, do the following:</span></span>

-   <span data-ttu-id="654f9-151">Derivare una classe da **CSource**.</span><span class="sxs-lookup"><span data-stu-id="654f9-151">Derive a class from **CSource**.</span></span>
-   <span data-ttu-id="654f9-152">Nel costruttore creare uno o più pin di output derivati da [**CSourceStream**](csourcestream.md).</span><span class="sxs-lookup"><span data-stu-id="654f9-152">In the constructor, create one or more output pins derived from [**CSourceStream**](csourcestream.md).</span></span> <span data-ttu-id="654f9-153">I pin si aggiungono automaticamente al filtro nei metodi del costruttore e si rimuovono nei metodi del distruttore.</span><span class="sxs-lookup"><span data-stu-id="654f9-153">The pins automatically add themselves to the filter in their constructor methods, and remove themselves in their destructor methods.</span></span>

<span data-ttu-id="654f9-154">Per sincronizzare lo stato del filtro tra più thread, chiamare il metodo [**CSource::P stateLock**](csource--pstatelock.md) .</span><span class="sxs-lookup"><span data-stu-id="654f9-154">To synchronize the filter state among multiple threads, call the [**CSource::pStateLock**](csource--pstatelock.md) method.</span></span> <span data-ttu-id="654f9-155">Questo metodo restituisce un puntatore alla sezione critica dello stato del filtro.</span><span class="sxs-lookup"><span data-stu-id="654f9-155">This method returns a pointer to the filter-state critical section.</span></span> <span data-ttu-id="654f9-156">Usare la classe [**CAutoLock**](cautolock.md) per mantenere la sezione critica.</span><span class="sxs-lookup"><span data-stu-id="654f9-156">Use the [**CAutoLock**](cautolock.md) class to hold the critical section.</span></span> <span data-ttu-id="654f9-157">Da un PIN è possibile accedere a **pStateLock** dalla variabile membro [**CBasePin:: m \_ pFilter**](cbasepin-m-pfilter.md) del PIN, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="654f9-157">From a pin, you can access **pStateLock** from the pin's [**CBasePin::m\_pFilter**](cbasepin-m-pfilter.md) member variable, as follows:</span></span>


```
CAutoLock lock(m_pFilter->pStateLock());
```



## <a name="requirements"></a><span data-ttu-id="654f9-158">Requisiti</span><span class="sxs-lookup"><span data-stu-id="654f9-158">Requirements</span></span>



| <span data-ttu-id="654f9-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="654f9-159">Requirement</span></span> | <span data-ttu-id="654f9-160">Valore</span><span class="sxs-lookup"><span data-stu-id="654f9-160">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="654f9-161">Intestazione</span><span class="sxs-lookup"><span data-stu-id="654f9-161">Header</span></span><br/>  | <dl> <span data-ttu-id="654f9-162"><dt>Source. h (Includi Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="654f9-162"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="654f9-163">Libreria</span><span class="sxs-lookup"><span data-stu-id="654f9-163">Library</span></span><br/> | <dl> <span data-ttu-id="654f9-164"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="654f9-164"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="654f9-165">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="654f9-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="654f9-166">Scrittura di filtri di origine</span><span class="sxs-lookup"><span data-stu-id="654f9-166">Writing Source Filters</span></span>](writing-source-filters.md)
</dt> </dl>

 

 




