---
description: Esempio di filtro synth
ms.assetid: 2d087967-3734-463f-bc5e-9552290ddc0b
title: Esempio di filtro synth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd569091df92eca3fbff4d8cb200150d6e6bfdca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885162"
---
# <a name="synth-filter-sample"></a><span data-ttu-id="af43a-103">Esempio di filtro synth</span><span class="sxs-lookup"><span data-stu-id="af43a-103">Synth Filter Sample</span></span>

## <a name="description"></a><span data-ttu-id="af43a-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="af43a-104">Description</span></span>

<span data-ttu-id="af43a-105">Il filtro synth è un filtro di origine che genera le forme d'onda audio.</span><span class="sxs-lookup"><span data-stu-id="af43a-105">The Synth filter is a source filter that generates audio waveforms.</span></span>

<span data-ttu-id="af43a-106">Questo filtro illustra la compilazione dinamica del grafico.</span><span class="sxs-lookup"><span data-stu-id="af43a-106">This filter illustrates dynamic graph building.</span></span> <span data-ttu-id="af43a-107">Può passare dal formato audio PCM non compresso a quello compresso MS \_ ADPCM (Microsoft Adaptive Delta Pulse Code Modulation).</span><span class="sxs-lookup"><span data-stu-id="af43a-107">It can switch between uncompressed PCM audio and compressed MS\_ADPCM (Microsoft Adaptive Delta Pulse Code Modulation) format.</span></span>

<span data-ttu-id="af43a-108">Questo filtro viene visualizzato in GraphEdit come "filtro del sintetizzatore audio".</span><span class="sxs-lookup"><span data-stu-id="af43a-108">This filter appears in GraphEdit as "Audio Synthesizer Filter."</span></span>

<span data-ttu-id="af43a-109">Per ulteriori informazioni sulla compilazione dinamica dei grafici, vedere [compilazione dinamica dei grafici](dynamic-graph-building.md).</span><span class="sxs-lookup"><span data-stu-id="af43a-109">For more information about dynamic graph building, see [Dynamic Graph Building](dynamic-graph-building.md).</span></span>

## <a name="usage"></a><span data-ttu-id="af43a-110">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="af43a-110">Usage</span></span>

<span data-ttu-id="af43a-111">Il filtro synth consente all'utente di impostare la forma d'onda, la frequenza, il numero di canali e altre proprietà tramite la pagina delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="af43a-111">The Synth filter enables the user to set the waveform, frequency, number of channels, and other properties through the property page.</span></span> <span data-ttu-id="af43a-112">Per impostare l'endpoint superiore o inferiore dell'intervallo di frequenza di sweep, tenere premuto MAIUSC mentre si modifica il dispositivo di scorrimento della frequenza.</span><span class="sxs-lookup"><span data-stu-id="af43a-112">To set either the upper or lower endpoint of the swept frequency range, hold down SHIFT while adjusting the frequency slider.</span></span> <span data-ttu-id="af43a-113">Il filtro supporta inoltre un'interfaccia personalizzata, ISynth2, per l'impostazione di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="af43a-113">The filter also supports a custom interface, ISynth2, for setting these properties.</span></span>

<span data-ttu-id="af43a-114">Per dimostrare la funzionalità di compilazione dinamica dei grafici, procedere come segue:</span><span class="sxs-lookup"><span data-stu-id="af43a-114">To demonstrate the dynamic graph building feature, do the following:</span></span>

1.  <span data-ttu-id="af43a-115">Compilare il filtro e registrarlo con l'utilità regsvr32.</span><span class="sxs-lookup"><span data-stu-id="af43a-115">Build the filter and register it with the Regsvr32 utility.</span></span>
2.  <span data-ttu-id="af43a-116">Avviare GraphEdit.</span><span class="sxs-lookup"><span data-stu-id="af43a-116">Launch GraphEdit.</span></span>
3.  <span data-ttu-id="af43a-117">Inserire il filtro del sintetizzatore audio.</span><span class="sxs-lookup"><span data-stu-id="af43a-117">Insert the Audio Synthesizer filter.</span></span> <span data-ttu-id="af43a-118">Viene visualizzato nella categoria filtri DirectShow.</span><span class="sxs-lookup"><span data-stu-id="af43a-118">It appears in the DirectShow Filters category.</span></span>
4.  <span data-ttu-id="af43a-119">Eseguire il rendering del PIN di output del filtro.</span><span class="sxs-lookup"><span data-stu-id="af43a-119">Render the filter's output pin.</span></span>
5.  <span data-ttu-id="af43a-120">Fare clic sul pulsante **Riproduci** .</span><span class="sxs-lookup"><span data-stu-id="af43a-120">Click the **Play** button.</span></span>
6.  <span data-ttu-id="af43a-121">Aprire la pagina delle proprietà del filtro.</span><span class="sxs-lookup"><span data-stu-id="af43a-121">Open the filter's property page.</span></span>
7.  <span data-ttu-id="af43a-122">Nell'area formato di output Selezionare PCM o Microsoft ADPCM.</span><span class="sxs-lookup"><span data-stu-id="af43a-122">In the Output Format area, select PCM or Microsoft ADPCM.</span></span>

## <a name="programming-notes"></a><span data-ttu-id="af43a-123">Note sulla programmazione</span><span class="sxs-lookup"><span data-stu-id="af43a-123">Programming Notes</span></span>

<span data-ttu-id="af43a-124">Questo esempio contiene i file seguenti:</span><span class="sxs-lookup"><span data-stu-id="af43a-124">This sample contains the following files:</span></span>

-   <span data-ttu-id="af43a-125">DYNSRC. h, DYNSRC. cpp: contiene due classi di base per i filtri di origine che supportano la compilazione dinamica dei grafici, CDynamicSource e CDynamicSourceStream.</span><span class="sxs-lookup"><span data-stu-id="af43a-125">Dynsrc.h, Dynsrc.cpp: Contains two base classes for source filters that support dynamic graph building, CDynamicSource and CDynamicSourceStream.</span></span>
-   <span data-ttu-id="af43a-126">ISynth. h: dichiara l'interfaccia ISynth2 personalizzata per l'impostazione delle proprietà nel filtro.</span><span class="sxs-lookup"><span data-stu-id="af43a-126">ISynth.h: Declares the custom ISynth2 interface for setting properties on the filter.</span></span>
-   <span data-ttu-id="af43a-127">Resource. h: contiene costanti di risorsa.</span><span class="sxs-lookup"><span data-stu-id="af43a-127">Resource.h: Contains resource constants.</span></span>
-   <span data-ttu-id="af43a-128">Synth. def: Esporta le funzioni DLL richieste dalla libreria COM.</span><span class="sxs-lookup"><span data-stu-id="af43a-128">Synth.def: Exports the DLL functions needed by the COM library.</span></span>
-   <span data-ttu-id="af43a-129">Synth. h, synth. cpp: contiene la classe CAudioSynth, che genera i dati audio e la classe CSynthFilter, che implementa il filtro.</span><span class="sxs-lookup"><span data-stu-id="af43a-129">Synth.h, Synth.cpp: Contains the CAudioSynth class, which generates the audio data, and the CSynthFilter class, which implements the filter.</span></span>
-   <span data-ttu-id="af43a-130">Synth. RC: contiene le risorse usate dal filtro.</span><span class="sxs-lookup"><span data-stu-id="af43a-130">Synth.rc: Contains resources used by the filter.</span></span>
-   <span data-ttu-id="af43a-131">Synthprp. h, Synthprp. cpp: implementa la pagina delle proprietà del filtro.</span><span class="sxs-lookup"><span data-stu-id="af43a-131">Synthprp.h, Synthprp.cpp: Implements the filter's property page.</span></span>

<span data-ttu-id="af43a-132">La classe CDynamicSource è adattata dalla classe di base [**CSource**](csource.md) .</span><span class="sxs-lookup"><span data-stu-id="af43a-132">The CDynamicSource class is adapted from the [**CSource**](csource.md) base class.</span></span> <span data-ttu-id="af43a-133">Usa uno o più pin di output derivati dalla classe CDynamicSourceStream.</span><span class="sxs-lookup"><span data-stu-id="af43a-133">It uses one or more output pins derived from the CDynamicSourceStream class.</span></span> <span data-ttu-id="af43a-134">La classe CDynamicSourceStream è adattata dalla classe [**CSourceStream**](csourcestream.md) , ma deriva dalla classe [**CDynamicOutputPin**](cdynamicoutputpin.md) anziché dalla classe [**CBaseOutputPin**](cbaseoutputpin.md) .</span><span class="sxs-lookup"><span data-stu-id="af43a-134">The CDynamicSourceStream class is adapted from the [**CSourceStream**](csourcestream.md) class, but derives from the [**CDynamicOutputPin**](cdynamicoutputpin.md) class rather than the [**CBaseOutputPin**](cbaseoutputpin.md) class.</span></span>

<span data-ttu-id="af43a-135">Per la classe CDynamicSource non sono stati trovati i metodi seguenti in [**CSource**](csource.md):</span><span class="sxs-lookup"><span data-stu-id="af43a-135">The CDynamicSource class has the following methods not found in [**CSource**](csource.md):</span></span>

-   <span data-ttu-id="af43a-136">Stop: segnala l'evento Stop ([**CDynamicOutputPin:: m \_ hStopEvent**](cdynamicoutputpin-m-hstopevent.md)) e arresta il thread di lavoro per tutti i pin non connessi.</span><span class="sxs-lookup"><span data-stu-id="af43a-136">Stop: Signals the stop event ([**CDynamicOutputPin::m\_hStopEvent**](cdynamicoutputpin-m-hstopevent.md)), and shuts down the worker thread for all unconnected pins.</span></span> <span data-ttu-id="af43a-137">Su un pin connesso, il metodo inattivo del pin arresterà il thread di lavoro.</span><span class="sxs-lookup"><span data-stu-id="af43a-137">On a connected pin, the pin's Inactive method will shut down the worker thread.</span></span>
-   <span data-ttu-id="af43a-138">Pause: Reimposta l'evento Stop.</span><span class="sxs-lookup"><span data-stu-id="af43a-138">Pause: Resets the stop event.</span></span>
-   <span data-ttu-id="af43a-139">JoinFilterGraph: chiama il metodo [**CDynamicOutputPin:: SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md) per ogni pin.</span><span class="sxs-lookup"><span data-stu-id="af43a-139">JoinFilterGraph: Calls the [**CDynamicOutputPin::SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md) method on each pin.</span></span>

<span data-ttu-id="af43a-140">Per la classe CDynamicSourceStream non sono stati trovati i metodi seguenti in [**CSourceStream**](csourcestream.md):</span><span class="sxs-lookup"><span data-stu-id="af43a-140">The CDynamicSourceStream class has the following methods not found in [**CSourceStream**](csourcestream.md):</span></span>

-   <span data-ttu-id="af43a-141">DestroySourceThread: arresta il thread di lavoro.</span><span class="sxs-lookup"><span data-stu-id="af43a-141">DestroySourceThread: Shuts down the worker thread.</span></span>
-   <span data-ttu-id="af43a-142">FatalError: segnala un errore al gestore del grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="af43a-142">FatalError: Signals an error to the filter graph manager.</span></span>
-   <span data-ttu-id="af43a-143">OutputPinNeedsToBeReconnected: segnala che è necessario riconnettere il pin di output.</span><span class="sxs-lookup"><span data-stu-id="af43a-143">OutputPinNeedsToBeReconnected: Signals that the output pin should be reconnected.</span></span> <span data-ttu-id="af43a-144">Quando viene chiamato questo metodo, il thread di lavoro chiama il metodo [**CDynamicOutputPin::D ynamicreconnect**](cdynamicoutputpin-dynamicreconnect.md) per riconnettere il PIN.</span><span class="sxs-lookup"><span data-stu-id="af43a-144">When this method is called, the worker thread calls the [**CDynamicOutputPin::DynamicReconnect**](cdynamicoutputpin-dynamicreconnect.md) method to reconnect the pin.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="af43a-145">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="af43a-145">Downloading the Sample</span></span>

<span data-ttu-id="af43a-146">Per scaricare gli esempi di DirectShow SDK, installare la versione più recente del [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="af43a-146">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

<span data-ttu-id="af43a-147">Questo esempio viene installato nel seguente percorso: *\[ SDK \] radice* \\ esempi di \\ \\ filtri DirectShow \\ Multimedia \\ synth.</span><span class="sxs-lookup"><span data-stu-id="af43a-147">This sample is installed under the following path: *\[SDK Root\]*\\Samples\\Multimedia\\DirectShow\\Filters\\Synth.</span></span>

## <a name="related-topics"></a><span data-ttu-id="af43a-148">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="af43a-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af43a-149">Esempi di DirectShow</span><span class="sxs-lookup"><span data-stu-id="af43a-149">DirectShow Samples</span></span>](directshow-samples.md)
</dt> </dl>

 

 



