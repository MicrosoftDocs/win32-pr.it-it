---
description: La classe CBaseMediaFilter implementa l'interfaccia IMediaFilter.
ms.assetid: 45c8973b-d0b3-4aeb-96e7-be47f8d7f4a7
title: Classe CBaseMediaFilter (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4e594fd941fffecc836af26bd3d70cced82ddcaa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326433"
---
# <a name="cbasemediafilter-class"></a><span data-ttu-id="aadc9-103">Classe CBaseMediaFilter</span><span class="sxs-lookup"><span data-stu-id="aadc9-103">CBaseMediaFilter class</span></span>

![cbasemediafilter](images/filter05.png)

<span data-ttu-id="aadc9-105">La `CBaseMediaFilter` classe implementa l'interfaccia [**IMediaFilter**](/windows/desktop/api/Strmif/nn-strmif-imediafilter) .</span><span class="sxs-lookup"><span data-stu-id="aadc9-105">The `CBaseMediaFilter` class implements the [**IMediaFilter**](/windows/desktop/api/Strmif/nn-strmif-imediafilter) interface.</span></span> <span data-ttu-id="aadc9-106">Usare questa classe per i distributori di plug-in o altri oggetti che devono supportare **IMediaFilter** senza supportare l'interfaccia [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) .</span><span class="sxs-lookup"><span data-stu-id="aadc9-106">Use this class for plug-in distributors or other objects that need to support **IMediaFilter** without supporting the [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface.</span></span> <span data-ttu-id="aadc9-107">Non usare questa classe per i filtri.</span><span class="sxs-lookup"><span data-stu-id="aadc9-107">Do not use this class for filters.</span></span> <span data-ttu-id="aadc9-108">Usare invece la classe [**CBaseFilter**](cbasefilter.md) o una classe di base derivata da **CBaseFilter**.</span><span class="sxs-lookup"><span data-stu-id="aadc9-108">Instead, use the [**CBaseFilter**](cbasefilter.md) class, or a base class derived from **CBaseFilter**.</span></span>



| <span data-ttu-id="aadc9-109">Variabili membro protette</span><span class="sxs-lookup"><span data-stu-id="aadc9-109">Protected Member Variables</span></span>                                       | <span data-ttu-id="aadc9-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aadc9-110">Description</span></span>                                                  |
|------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="aadc9-111">**m \_ stato**</span><span class="sxs-lookup"><span data-stu-id="aadc9-111">**m\_State**</span></span>](cbasemediafilter-m-state.md)                     | <span data-ttu-id="aadc9-112">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="aadc9-112">Current state of the object.</span></span>                                 |
| [<span data-ttu-id="aadc9-113">**\_pClock m**</span><span class="sxs-lookup"><span data-stu-id="aadc9-113">**m\_pClock**</span></span>](cbasemediafilter-m-pclock.md)                   | <span data-ttu-id="aadc9-114">Puntatore al clock di riferimento dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="aadc9-114">Pointer to the object's reference clock.</span></span>                     |
| [<span data-ttu-id="aadc9-115">**\_tStart m**</span><span class="sxs-lookup"><span data-stu-id="aadc9-115">**m\_tStart**</span></span>](cbasemediafilter-m-tstart.md)                   | <span data-ttu-id="aadc9-116">Tempo di riferimento che corrisponde al tempo di flusso 0.</span><span class="sxs-lookup"><span data-stu-id="aadc9-116">Reference time that corresponds to stream time 0.</span></span>            |
| [<span data-ttu-id="aadc9-117">**\_CLSID m**</span><span class="sxs-lookup"><span data-stu-id="aadc9-117">**m\_clsid**</span></span>](cbasemediafilter-m-clsid.md)                     | <span data-ttu-id="aadc9-118">Identificatore di classe (CLSID) dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="aadc9-118">Class identifier (CLSID) of the object.</span></span>                      |
| [<span data-ttu-id="aadc9-119">**\_pLock m**</span><span class="sxs-lookup"><span data-stu-id="aadc9-119">**m\_pLock**</span></span>](cbasemediafilter-m-plock.md)                     | <span data-ttu-id="aadc9-120">Puntatore a una sezione critica.</span><span class="sxs-lookup"><span data-stu-id="aadc9-120">Pointer to a critical section.</span></span>                               |
| <span data-ttu-id="aadc9-121">Metodi pubblici</span><span class="sxs-lookup"><span data-stu-id="aadc9-121">Public Methods</span></span>                                                   | <span data-ttu-id="aadc9-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aadc9-122">Description</span></span>                                                  |
| [<span data-ttu-id="aadc9-123">**CBaseMediaFilter**</span><span class="sxs-lookup"><span data-stu-id="aadc9-123">**CBaseMediaFilter**</span></span>](cbasemediafilter-cbasemediafilter.md)    | <span data-ttu-id="aadc9-124">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="aadc9-124">Constructor method.</span></span>                                          |
| [<span data-ttu-id="aadc9-125">**~ CBaseMediaFilter**</span><span class="sxs-lookup"><span data-stu-id="aadc9-125">**~ CBaseMediaFilter**</span></span>](cbasemediafilter--cbasemediafilter.md) | <span data-ttu-id="aadc9-126">Metodo del distruttore.</span><span class="sxs-lookup"><span data-stu-id="aadc9-126">Destructor method.</span></span> <span data-ttu-id="aadc9-127">Virtuale.</span><span class="sxs-lookup"><span data-stu-id="aadc9-127">Virtual.</span></span>                                  |
| [<span data-ttu-id="aadc9-128">**StreamTime**</span><span class="sxs-lookup"><span data-stu-id="aadc9-128">**StreamTime**</span></span>](cbasemediafilter-streamtime.md)                | <span data-ttu-id="aadc9-129">Recupera l'ora corrente del flusso.</span><span class="sxs-lookup"><span data-stu-id="aadc9-129">Retrieves the current stream time.</span></span> <span data-ttu-id="aadc9-130">Virtuale.</span><span class="sxs-lookup"><span data-stu-id="aadc9-130">Virtual.</span></span>                  |
| [<span data-ttu-id="aadc9-131">**IsActive**</span><span class="sxs-lookup"><span data-stu-id="aadc9-131">**IsActive**</span></span>](cbasemediafilter-isactive.md)                    | <span data-ttu-id="aadc9-132">Determina se l'oggetto è attivo (in esecuzione o in pausa).</span><span class="sxs-lookup"><span data-stu-id="aadc9-132">Determines whether the object is active (running or paused).</span></span> |
| <span data-ttu-id="aadc9-133">Metodi IPersist</span><span class="sxs-lookup"><span data-stu-id="aadc9-133">IPersist Methods</span></span>                                                 | <span data-ttu-id="aadc9-134">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aadc9-134">Description</span></span>                                                  |
| [<span data-ttu-id="aadc9-135">**GetClassID**</span><span class="sxs-lookup"><span data-stu-id="aadc9-135">**GetClassID**</span></span>](cbasemediafilter-getclassid.md)                | <span data-ttu-id="aadc9-136">Recupera l'identificatore di classe.</span><span class="sxs-lookup"><span data-stu-id="aadc9-136">Retrieves the class identifier.</span></span>                              |
| <span data-ttu-id="aadc9-137">Metodi IMediaFilter</span><span class="sxs-lookup"><span data-stu-id="aadc9-137">IMediaFilter Methods</span></span>                                             | <span data-ttu-id="aadc9-138">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aadc9-138">Description</span></span>                                                  |
| [<span data-ttu-id="aadc9-139">**GetState**</span><span class="sxs-lookup"><span data-stu-id="aadc9-139">**GetState**</span></span>](cbasemediafilter-getstate.md)                    | <span data-ttu-id="aadc9-140">Recupera lo stato dell'oggetto (in esecuzione, arrestato o sospeso).</span><span class="sxs-lookup"><span data-stu-id="aadc9-140">Retrieves the object's state (running, stopped, or paused).</span></span>  |
| [<span data-ttu-id="aadc9-141">**SetSyncSource**</span><span class="sxs-lookup"><span data-stu-id="aadc9-141">**SetSyncSource**</span></span>](cbasemediafilter-setsyncsource.md)          | <span data-ttu-id="aadc9-142">Imposta un clock di riferimento per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="aadc9-142">Sets a reference clock for the object.</span></span>                       |
| [<span data-ttu-id="aadc9-143">**GetSyncSource**</span><span class="sxs-lookup"><span data-stu-id="aadc9-143">**GetSyncSource**</span></span>](cbasemediafilter-getsyncsource.md)          | <span data-ttu-id="aadc9-144">Recupera l'orologio di riferimento usato dall'oggetto.</span><span class="sxs-lookup"><span data-stu-id="aadc9-144">Retrieves the reference clock that the object is using.</span></span>      |
| [<span data-ttu-id="aadc9-145">**Interrompere**</span><span class="sxs-lookup"><span data-stu-id="aadc9-145">**Stop**</span></span>](cbasemediafilter-stop.md)                            | <span data-ttu-id="aadc9-146">Arresta l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="aadc9-146">Stops the object.</span></span>                                            |
| [<span data-ttu-id="aadc9-147">**Sospendere**</span><span class="sxs-lookup"><span data-stu-id="aadc9-147">**Pause**</span></span>](cbasemediafilter-pause.md)                          | <span data-ttu-id="aadc9-148">Sospende l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="aadc9-148">Pauses the object.</span></span>                                           |
| [<span data-ttu-id="aadc9-149">**Correre**</span><span class="sxs-lookup"><span data-stu-id="aadc9-149">**Run**</span></span>](cbasemediafilter-run.md)                              | <span data-ttu-id="aadc9-150">Esegue l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="aadc9-150">Runs the object.</span></span>                                             |



 

## <a name="requirements"></a><span data-ttu-id="aadc9-151">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aadc9-151">Requirements</span></span>



| <span data-ttu-id="aadc9-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="aadc9-152">Requirement</span></span> | <span data-ttu-id="aadc9-153">Valore</span><span class="sxs-lookup"><span data-stu-id="aadc9-153">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aadc9-154">Intestazione</span><span class="sxs-lookup"><span data-stu-id="aadc9-154">Header</span></span><br/>  | <dl> <span data-ttu-id="aadc9-155"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="aadc9-155"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="aadc9-156">Libreria</span><span class="sxs-lookup"><span data-stu-id="aadc9-156">Library</span></span><br/> | <dl> <span data-ttu-id="aadc9-157"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="aadc9-157"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




