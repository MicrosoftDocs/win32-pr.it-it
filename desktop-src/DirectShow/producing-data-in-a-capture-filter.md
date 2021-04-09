---
description: Questo argomento descrive come un filtro di acquisizione DirectShow personalizzato deve generare dati di output.
ms.assetid: e407e9ed-f1f7-43c4-a048-c27476c910ea
title: Produzione di dati in un filtro di acquisizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d9c9e5bed6fc7e01aa89bf6f495c1bbdf6e42a0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103965721"
---
# <a name="producing-data-in-a-capture-filter"></a><span data-ttu-id="52ca4-103">Produzione di dati in un filtro di acquisizione</span><span class="sxs-lookup"><span data-stu-id="52ca4-103">Producing Data in a Capture Filter</span></span>

<span data-ttu-id="52ca4-104">Questo argomento descrive come un filtro di acquisizione DirectShow personalizzato deve generare dati di output.</span><span class="sxs-lookup"><span data-stu-id="52ca4-104">This topic describes how a custom DirectShow capture filter should generate output data.</span></span>

## <a name="filter-state-changes"></a><span data-ttu-id="52ca4-105">Modifica stato filtro</span><span class="sxs-lookup"><span data-stu-id="52ca4-105">Filter State Changes</span></span>

<span data-ttu-id="52ca4-106">Un filtro di acquisizione deve produrre dati solo quando il filtro è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="52ca4-106">A capture filter should produce data only when the filter is running.</span></span> <span data-ttu-id="52ca4-107">Non inviare dati dai pin quando il filtro è sospeso.</span><span class="sxs-lookup"><span data-stu-id="52ca4-107">Do not send data from your pins when the filter is paused.</span></span> <span data-ttu-id="52ca4-108">Inoltre, quando il filtro viene sospeso, restituisce il **\_ \_ \_ CUE del cant di VFW** dal metodo [**CBaseFilter:: GetState**](cbasefilter-getstate.md) .</span><span class="sxs-lookup"><span data-stu-id="52ca4-108">Also, return **VFW\_S\_CANT\_CUE** from the [**CBaseFilter::GetState**](cbasefilter-getstate.md) method when the filter is paused.</span></span> <span data-ttu-id="52ca4-109">Questo valore restituito informa il gestore del grafico del filtro che non deve attendere i dati dal filtro mentre il filtro è sospeso.</span><span class="sxs-lookup"><span data-stu-id="52ca4-109">This return value informs the Filter Graph Manager that it should not wait for any data from your filter while the filter is paused.</span></span> <span data-ttu-id="52ca4-110">Per altre informazioni, vedere [Stati di filtro](filter-states.md).</span><span class="sxs-lookup"><span data-stu-id="52ca4-110">For more information, see [Filter States](filter-states.md).</span></span>

<span data-ttu-id="52ca4-111">Il codice seguente illustra come implementare il metodo [**IMediaFilter:: GetState**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate) :</span><span class="sxs-lookup"><span data-stu-id="52ca4-111">The following code shows how to implement the [**IMediaFilter::GetState**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate) method:</span></span>


```C++
CMyVidcapFilter::GetState(DWORD dw, FILTER_STATE *pState)
{
    CheckPointer(pState, E_POINTER);
    *pState = m_State;
    if (m_State == State_Paused)
    {
        return VFW_S_CANT_CUE;
    }
    else
    {
        return S_OK;
    }
}
```



## <a name="controlling-individual-streams"></a><span data-ttu-id="52ca4-112">Controllo di singoli flussi</span><span class="sxs-lookup"><span data-stu-id="52ca4-112">Controlling Individual Streams</span></span>

<span data-ttu-id="52ca4-113">I pin di output di un filtro di acquisizione devono supportare l'interfaccia [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) , in modo che un'applicazione possa attivare o disattivare ogni pin singolarmente.</span><span class="sxs-lookup"><span data-stu-id="52ca4-113">A capture filter's output pins should support the [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) interface, so that an application can turn each pin on or off individually.</span></span> <span data-ttu-id="52ca4-114">Un'applicazione, ad esempio, può essere anteprima senza acquisizione, quindi passare alla modalità di acquisizione senza ricompilare il grafico del filtro.</span><span class="sxs-lookup"><span data-stu-id="52ca4-114">For example, an application can preview without capturing, and then switch to capture mode without rebuilding the filter graph.</span></span> <span data-ttu-id="52ca4-115">Per implementare questa interfaccia, è possibile usare la classe [**CBaseStreamControl**](cbasestreamcontrol.md) .</span><span class="sxs-lookup"><span data-stu-id="52ca4-115">You can use the [**CBaseStreamControl**](cbasestreamcontrol.md) class to implement this interface.</span></span>

## <a name="time-stamps"></a><span data-ttu-id="52ca4-116">Timestamp</span><span class="sxs-lookup"><span data-stu-id="52ca4-116">Time Stamps</span></span>

<span data-ttu-id="52ca4-117">Quando il filtro acquisisce un campione, ora contrassegna l'esempio con l'ora corrente del flusso.</span><span class="sxs-lookup"><span data-stu-id="52ca4-117">When the filter captures a sample, time stamp the sample with the current stream time.</span></span> <span data-ttu-id="52ca4-118">L'ora di fine è l'ora di inizio più la durata.</span><span class="sxs-lookup"><span data-stu-id="52ca4-118">The end time is the start time plus the duration.</span></span> <span data-ttu-id="52ca4-119">Se, ad esempio, il filtro sta acquisendo dieci campioni al secondo e il tempo di flusso è di 200 milioni unità quando il filtro acquisisce l'esempio, gli indicatori di data e ora devono essere 200 milioni e 201 milioni.</span><span class="sxs-lookup"><span data-stu-id="52ca4-119">For example, if the filter is capturing at ten samples per second, and the stream time is 200,000,000 units when the filter captures the sample, the time stamps should be 200000000 and 201000000.</span></span> <span data-ttu-id="52ca4-120">(Ci sono 10 milioni unità al secondo).</span><span class="sxs-lookup"><span data-stu-id="52ca4-120">(There are 10,000,000 units per second.)</span></span>

<span data-ttu-id="52ca4-121">Per calcolare l'ora del flusso, chiamare il metodo [**IReferenceClock:: GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) per ottenere l'ora di riferimento corrente, quindi sottrarre l'ora di inizio originale.</span><span class="sxs-lookup"><span data-stu-id="52ca4-121">To calculate the stream time, call the [**IReferenceClock::GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) method to get the current reference time, and then substract the original start time.</span></span> <span data-ttu-id="52ca4-122">In alternativa, chiamare il metodo [**CBaseFilter:: StreamTime**](cbasefilter-streamtime.md) , che esegue lo stesso calcolo.</span><span class="sxs-lookup"><span data-stu-id="52ca4-122">Alternatively, call the [**CBaseFilter::StreamTime**](cbasefilter-streamtime.md) method, which performs the same calculation.</span></span> <span data-ttu-id="52ca4-123">Per impostare il timestamp per un esempio, chiamare il metodo [**IMediaSample:: setime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) .</span><span class="sxs-lookup"><span data-stu-id="52ca4-123">To set the time stamp on a sample, call the [**IMediaSample::SetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) method.</span></span>

<span data-ttu-id="52ca4-124">Se il filtro ha un pin di anteprima, tuttavia, gli esempi del PIN di anteprima non devono avere timestamp.</span><span class="sxs-lookup"><span data-stu-id="52ca4-124">If the filter has a preview pin, however, samples from the preview pin should not have time stamps.</span></span> <span data-ttu-id="52ca4-125">Il motivo è che gli esempi raggiungeranno sempre il renderer leggermente dopo il momento dell'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="52ca4-125">The reason is that samples will always reach the renderer slightly after the time of capture.</span></span> <span data-ttu-id="52ca4-126">Se gli esempi sono contrassegnati con un timestamp, il renderer li considererà come in ritardo e potrebbe provare ad aggiornarli eliminando gli esempi.</span><span class="sxs-lookup"><span data-stu-id="52ca4-126">If the samples are time stamped, the renderer will treat them as late, and it may try to catch up by dropping samples.</span></span> <span data-ttu-id="52ca4-127">Per ulteriori informazioni, vedere [filtri di acquisizione video DirectShow](directshow-video-capture-filters.md). Si noti che l'interfaccia [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) richiede il pin per tenere traccia dei tempi di campionamento.</span><span class="sxs-lookup"><span data-stu-id="52ca4-127">(For more information, see [DirectShow Video Capture Filters](directshow-video-capture-filters.md).) Note that the [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) interface requires the pin to keep track of sample times.</span></span> <span data-ttu-id="52ca4-128">Per un pin di anteprima, potrebbe essere necessario modificare l'implementazione in modo che non si basi sugli indicatori temporali.</span><span class="sxs-lookup"><span data-stu-id="52ca4-128">For a preview pin, you might need to modify the implementation so that it does not rely on time stamps.</span></span>

<span data-ttu-id="52ca4-129">Gli indicatori temporali devono sempre aumentare da un campione a quello successivo.</span><span class="sxs-lookup"><span data-stu-id="52ca4-129">Time stamps must always increase from one sample to the next.</span></span> <span data-ttu-id="52ca4-130">Questo vale anche quando il filtro viene sospeso.</span><span class="sxs-lookup"><span data-stu-id="52ca4-130">This is true even when the filter pauses.</span></span> <span data-ttu-id="52ca4-131">Se il filtro viene eseguito, viene sospesa e quindi nuovamente eseguito, il primo campione dopo la pausa deve avere un timestamp maggiore dell'ultimo campione prima della sospensione.</span><span class="sxs-lookup"><span data-stu-id="52ca4-131">If the filter runs, pauses, and then runs again, the first sample after the pause must have a larger time stamp than the last sample before the pause.</span></span>

<span data-ttu-id="52ca4-132">A seconda dei dati che si stanno acquisendo, potrebbe essere opportuno impostare il tempo dei supporti per gli esempi.</span><span class="sxs-lookup"><span data-stu-id="52ca4-132">Depending on the data you are capturing, it might be appropriate to set the media time on the samples.</span></span>

<span data-ttu-id="52ca4-133">Per altre informazioni, vedere [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="52ca4-133">For more information, see [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="52ca4-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="52ca4-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52ca4-135">Filtri di acquisizione video DirectShow</span><span class="sxs-lookup"><span data-stu-id="52ca4-135">DirectShow Video Capture Filters</span></span>](directshow-video-capture-filters.md)
</dt> <dt>

[<span data-ttu-id="52ca4-136">Time and Clocks in DirectShow</span><span class="sxs-lookup"><span data-stu-id="52ca4-136">Time and Clocks in DirectShow</span></span>](time-and-clocks-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="52ca4-137">Scrittura dei filtri di acquisizione</span><span class="sxs-lookup"><span data-stu-id="52ca4-137">Writing Capture Filters</span></span>](writing-capture-filters.md)
</dt> </dl>

 

 



