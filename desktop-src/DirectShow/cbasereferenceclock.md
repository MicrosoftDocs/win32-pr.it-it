---
description: La classe CBaseReferenceClock implementa un clock di riferimento.
ms.assetid: 898e1968-a9ab-4bb9-abf0-943bfae502e2
title: Classe CBaseReferenceClock (Refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1da55a57faac201a2dbf0ef4d8a9774157d9215d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329410"
---
# <a name="cbasereferenceclock-class"></a><span data-ttu-id="32322-103">Classe CBaseReferenceClock</span><span class="sxs-lookup"><span data-stu-id="32322-103">CBaseReferenceClock class</span></span>

![gerarchia di classi cbasereferenceclock](images/rclock01.png)

<span data-ttu-id="32322-105">La `CBaseReferenceClock` classe implementa un clock di riferimento.</span><span class="sxs-lookup"><span data-stu-id="32322-105">The `CBaseReferenceClock` class implements a reference clock.</span></span>



| <span data-ttu-id="32322-106">Variabili membro protette</span><span class="sxs-lookup"><span data-stu-id="32322-106">Protected Member Variables</span></span>                                                         | <span data-ttu-id="32322-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="32322-107">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="32322-108">**\_pSchedule m**</span><span class="sxs-lookup"><span data-stu-id="32322-108">**m\_pSchedule**</span></span>](cbasereferenceclock-m-pschedule.md)                            | <span data-ttu-id="32322-109">Oggetto [**CAMSchedule**](camschedule.md) che gestisce le attività di pianificazione del clock.</span><span class="sxs-lookup"><span data-stu-id="32322-109">[**CAMSchedule**](camschedule.md) object that handles scheduling tasks for the clock.</span></span> |
| <span data-ttu-id="32322-110">Metodi protetti</span><span class="sxs-lookup"><span data-stu-id="32322-110">Protected Methods</span></span>                                                                  | <span data-ttu-id="32322-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="32322-111">Description</span></span>                                                                            |
| [<span data-ttu-id="32322-112">**~ CBaseReferenceClock**</span><span class="sxs-lookup"><span data-stu-id="32322-112">**~CBaseReferenceClock**</span></span>](cbasereferenceclock--cbasereferenceclock.md)           | <span data-ttu-id="32322-113">Metodo del distruttore.</span><span class="sxs-lookup"><span data-stu-id="32322-113">Destructor method.</span></span>                                                                     |
| <span data-ttu-id="32322-114">Metodi pubblici</span><span class="sxs-lookup"><span data-stu-id="32322-114">Public Methods</span></span>                                                                     | <span data-ttu-id="32322-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="32322-115">Description</span></span>                                                                            |
| [<span data-ttu-id="32322-116">**CBaseReferenceClock**</span><span class="sxs-lookup"><span data-stu-id="32322-116">**CBaseReferenceClock**</span></span>](cbasereferenceclock-cbasereferenceclock.md)             | <span data-ttu-id="32322-117">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="32322-117">Constructor method.</span></span>                                                                    |
| [<span data-ttu-id="32322-118">**GetPrivateTime**</span><span class="sxs-lookup"><span data-stu-id="32322-118">**GetPrivateTime**</span></span>](cbasereferenceclock-getprivatetime.md)                       | <span data-ttu-id="32322-119">Recupera il tempo reale dal clock.</span><span class="sxs-lookup"><span data-stu-id="32322-119">Retrieves the real time from the clock.</span></span>                                                |
| [<span data-ttu-id="32322-120">**SetTimeDelta**</span><span class="sxs-lookup"><span data-stu-id="32322-120">**SetTimeDelta**</span></span>](cbasereferenceclock-settimedelta.md)                           | <span data-ttu-id="32322-121">Regola l'ora di clock interna.</span><span class="sxs-lookup"><span data-stu-id="32322-121">Adjusts the internal clock time.</span></span>                                                       |
| [<span data-ttu-id="32322-122">**Getschedule**</span><span class="sxs-lookup"><span data-stu-id="32322-122">**GetSchedule**</span></span>](cbasereferenceclock-getschedule.md)                             | <span data-ttu-id="32322-123">Recupera un puntatore all'oggetto di pianificazione del clock.</span><span class="sxs-lookup"><span data-stu-id="32322-123">Retrieves a pointer to the clock's scheduling object.</span></span>                                  |
| [<span data-ttu-id="32322-124">**TriggerThread**</span><span class="sxs-lookup"><span data-stu-id="32322-124">**TriggerThread**</span></span>](cbasereferenceclock-triggerthread.md)                         | <span data-ttu-id="32322-125">Attiva il thread di lavoro che gestisce la pianificazione.</span><span class="sxs-lookup"><span data-stu-id="32322-125">Wakes up the worker thread that handles scheduling.</span></span>                                    |
| <span data-ttu-id="32322-126">Metodi IReferenceClock</span><span class="sxs-lookup"><span data-stu-id="32322-126">IReferenceClock Methods</span></span>                                                            | <span data-ttu-id="32322-127">Descrizione</span><span class="sxs-lookup"><span data-stu-id="32322-127">Description</span></span>                                                                            |
| [<span data-ttu-id="32322-128">**GetTime**</span><span class="sxs-lookup"><span data-stu-id="32322-128">**GetTime**</span></span>](cbasereferenceclock-gettime.md)                                     | <span data-ttu-id="32322-129">Recupera l'ora di riferimento corrente.</span><span class="sxs-lookup"><span data-stu-id="32322-129">Retrieves the current reference time.</span></span>                                                  |
| [<span data-ttu-id="32322-130">**AdviseTime**</span><span class="sxs-lookup"><span data-stu-id="32322-130">**AdviseTime**</span></span>](cbasereferenceclock-advisetime.md)                               | <span data-ttu-id="32322-131">Crea una richiesta di notifica di un unico tentativo.</span><span class="sxs-lookup"><span data-stu-id="32322-131">Creates a one-shot advise request.</span></span>                                                     |
| [<span data-ttu-id="32322-132">**AdvisePeriodic**</span><span class="sxs-lookup"><span data-stu-id="32322-132">**AdvisePeriodic**</span></span>](cbasereferenceclock-adviseperiodic.md)                       | <span data-ttu-id="32322-133">Crea una richiesta di notifica periodica.</span><span class="sxs-lookup"><span data-stu-id="32322-133">Creates a periodic advise request.</span></span>                                                     |
| [<span data-ttu-id="32322-134">**Unadvise**</span><span class="sxs-lookup"><span data-stu-id="32322-134">**Unadvise**</span></span>](cbasereferenceclock-unadvise.md)                                   | <span data-ttu-id="32322-135">Rimuove una richiesta di notifica in sospeso.</span><span class="sxs-lookup"><span data-stu-id="32322-135">Removes a pending advise request.</span></span>                                                      |
| <span data-ttu-id="32322-136">Metodi IReferenceClockTimerControl</span><span class="sxs-lookup"><span data-stu-id="32322-136">IReferenceClockTimerControl Methods</span></span>                                                | <span data-ttu-id="32322-137">Descrizione</span><span class="sxs-lookup"><span data-stu-id="32322-137">Description</span></span>                                                                            |
| [<span data-ttu-id="32322-138">**GetDefaultTimerResolution**</span><span class="sxs-lookup"><span data-stu-id="32322-138">**GetDefaultTimerResolution**</span></span>](cbasereferenceclock-getdefaulttimerresolution.md) | <span data-ttu-id="32322-139">Restituisce la risoluzione corrente del timer del clock di riferimento.</span><span class="sxs-lookup"><span data-stu-id="32322-139">Returns the current resolution of the reference clock's timer.</span></span>                         |
| [<span data-ttu-id="32322-140">**SetDefaultTimerResolution**</span><span class="sxs-lookup"><span data-stu-id="32322-140">**SetDefaultTimerResolution**</span></span>](cbasereferenceclock-setdefaulttimerresolution.md) | <span data-ttu-id="32322-141">Imposta la risoluzione del timer del clock di riferimento.</span><span class="sxs-lookup"><span data-stu-id="32322-141">Sets the resolution of the reference clock's timer.</span></span>                                    |
| <span data-ttu-id="32322-142">Funzioni di supporto</span><span class="sxs-lookup"><span data-stu-id="32322-142">Helper Functions</span></span>                                                                   | <span data-ttu-id="32322-143">Descrizione</span><span class="sxs-lookup"><span data-stu-id="32322-143">Description</span></span>                                                                            |
| [<span data-ttu-id="32322-144">**ConvertToMilliseconds**</span><span class="sxs-lookup"><span data-stu-id="32322-144">**ConvertToMilliseconds**</span></span>](converttomilliseconds.md)                             | <span data-ttu-id="32322-145">Converte un'ora di riferimento in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="32322-145">Converts a reference time to milliseconds.</span></span>                                             |



 

## <a name="remarks"></a><span data-ttu-id="32322-146">Commenti</span><span class="sxs-lookup"><span data-stu-id="32322-146">Remarks</span></span>

<span data-ttu-id="32322-147">Questa classe implementa un clock di riferimento che supporta le interfacce [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) e [**IReferenceClockTimerControl**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclocktimercontrol) .</span><span class="sxs-lookup"><span data-stu-id="32322-147">This class implements a reference clock that supports the [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) and [**IReferenceClockTimerControl**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclocktimercontrol) interfaces.</span></span> <span data-ttu-id="32322-148">Se un filtro può fornire un orologio di riferimento per il grafico di filtro, ad esempio accedendo a un dispositivo hardware, può usare questa classe per implementare l'orologio.</span><span class="sxs-lookup"><span data-stu-id="32322-148">If a filter can provide a reference clock for the filter graph for example, by accessing a hardware device it can use this class to implement the clock.</span></span>

<span data-ttu-id="32322-149">L' `CBaseReferenceClock` oggetto gestisce due valori temporali distinti:</span><span class="sxs-lookup"><span data-stu-id="32322-149">The `CBaseReferenceClock` object maintains two distinct time values:</span></span>

-   <span data-ttu-id="32322-150">Internamente, il metodo [**CBaseReferenceClock:: GetPrivateTime**](cbasereferenceclock-getprivatetime.md) restituisce il tempo effettivo mantenuto dal clock.</span><span class="sxs-lookup"><span data-stu-id="32322-150">Internally, the [**CBaseReferenceClock::GetPrivateTime**](cbasereferenceclock-getprivatetime.md) method returns the actual time kept by the clock.</span></span>
-   <span data-ttu-id="32322-151">Esternamente, il metodo [**CBaseReferenceClock:: GetTime**](cbasereferenceclock-gettime.md) restituisce l'ora di riferimento per il grafico del filtro.</span><span class="sxs-lookup"><span data-stu-id="32322-151">Externally, the [**CBaseReferenceClock::GetTime**](cbasereferenceclock-gettime.md) method returns the reference time for the filter graph.</span></span>

<span data-ttu-id="32322-152">È valido per l'esecuzione del clock interno indietro per brevi periodi.</span><span class="sxs-lookup"><span data-stu-id="32322-152">It is valid for the internal clock to run backward over brief periods.</span></span> <span data-ttu-id="32322-153">Se, ad esempio, il clock si sposta in avanti, il filtro può adattarlo all'indietro.</span><span class="sxs-lookup"><span data-stu-id="32322-153">For example, if the clock drifts forward, the filter can adjust it backward.</span></span> <span data-ttu-id="32322-154">Vedere [**CBaseReferenceClock:: SetTimeDelta**](cbasereferenceclock-settimedelta.md). Il metodo **getTime** usa i valori temporali restituiti da **GetPrivateTime**.</span><span class="sxs-lookup"><span data-stu-id="32322-154">(See [**CBaseReferenceClock::SetTimeDelta**](cbasereferenceclock-settimedelta.md).) The **GetTime** method uses the time values reported by **GetPrivateTime**.</span></span> <span data-ttu-id="32322-155">Tuttavia, l'ora di riferimento è a incremento progressivo costante. in altre parole, non viene mai eseguito all'indietro.</span><span class="sxs-lookup"><span data-stu-id="32322-155">However, the reference time is monotonically increasing; in other words, it never runs backward.</span></span> <span data-ttu-id="32322-156">Di conseguenza, se il clock interno viene eseguito indietro, **getTime** continua a segnalare l'ora precedente fino a quando l'orologio interno non viene ripreso.</span><span class="sxs-lookup"><span data-stu-id="32322-156">Therefore, if the internal clock runs backward, **GetTime** continues to report the old time until the internal clock catches up.</span></span>

<span data-ttu-id="32322-157">Ad esempio, i due metodi potrebbero restituire le sequenze seguenti:</span><span class="sxs-lookup"><span data-stu-id="32322-157">For example, the two methods might return the following sequences:</span></span>

``` syntax
GetPrivateTime: 105, 106, 103, 104, 105, 106, 107, 108
GetTime:        105, 106, 106, 106, 106, 106, 107, 108
```

<span data-ttu-id="32322-158">Al terzo Tick del clock, il clock interno passa indietro a 103.</span><span class="sxs-lookup"><span data-stu-id="32322-158">On the third clock tick, the internal clock jumps backward to 103.</span></span> <span data-ttu-id="32322-159">Il metodo **getTime** continua a segnalare 106 fino a quando l'orologio interno non viene ripreso.</span><span class="sxs-lookup"><span data-stu-id="32322-159">The **GetTime** method continues to report 106 until the internal clock catches up.</span></span>

<span data-ttu-id="32322-160">Per impostazione predefinita, **GetPrivateTime** restituisce l'ora di sistema tramite una chiamata alla funzione **timeGetTime** .</span><span class="sxs-lookup"><span data-stu-id="32322-160">By default, **GetPrivateTime** returns the system time, through a call to the **timeGetTime** function.</span></span> <span data-ttu-id="32322-161">Un filtro che fornisce un orologio di riferimento da un dispositivo esterno può eseguire una delle operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="32322-161">A filter that is providing a reference clock from an external device can do one of the following:</span></span>

-   <span data-ttu-id="32322-162">Eseguire l'override di **GetPrivateTime** per restituire l'ora dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="32322-162">Override **GetPrivateTime** to return the time from the device.</span></span>
-   <span data-ttu-id="32322-163">Monitorare la discrepanza tra l'ora del dispositivo e l'ora di sistema e chiamare **SetTimeDelta** per apportare le correzioni.</span><span class="sxs-lookup"><span data-stu-id="32322-163">Monitor the discrepancy between the device time and the system time, and call **SetTimeDelta** to make corrections.</span></span>

<span data-ttu-id="32322-164">Questa classe usa un oggetto [**CAMSchedule**](camschedule.md) per gestire la pianificazione delle richieste di notifica.</span><span class="sxs-lookup"><span data-stu-id="32322-164">This class uses a [**CAMSchedule**](camschedule.md) object to handle scheduling of advise requests.</span></span> <span data-ttu-id="32322-165">Per informazioni dettagliate, vedere la documentazione per la classe **CAMSchedule** .</span><span class="sxs-lookup"><span data-stu-id="32322-165">For details, see the documentation for the **CAMSchedule** class.</span></span>

## <a name="requirements"></a><span data-ttu-id="32322-166">Requisiti</span><span class="sxs-lookup"><span data-stu-id="32322-166">Requirements</span></span>



| <span data-ttu-id="32322-167">Requisito</span><span class="sxs-lookup"><span data-stu-id="32322-167">Requirement</span></span> | <span data-ttu-id="32322-168">Valore</span><span class="sxs-lookup"><span data-stu-id="32322-168">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32322-169">Intestazione</span><span class="sxs-lookup"><span data-stu-id="32322-169">Header</span></span><br/>  | <dl> <span data-ttu-id="32322-170"><dt>Refclock. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="32322-170"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="32322-171">Libreria</span><span class="sxs-lookup"><span data-stu-id="32322-171">Library</span></span><br/> | <dl> <span data-ttu-id="32322-172"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="32322-172"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




