---
description: Ottimizzazione della televisione analoga
ms.assetid: f4ae76e3-0f61-4a33-8ea4-ef14a117df6a
title: Ottimizzazione della televisione analoga
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b85d0826340b913df88cb20dc538bc85943949b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304259"
---
# <a name="analog-television-tuning"></a><span data-ttu-id="06a3c-103">Ottimizzazione della televisione analoga</span><span class="sxs-lookup"><span data-stu-id="06a3c-103">Analog Television Tuning</span></span>

<span data-ttu-id="06a3c-104">L'ottimizzazione viene controllata dal filtro del sintonizzatore TV tramite l'interfaccia [**Impossibile IAMTVTuner**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner) .</span><span class="sxs-lookup"><span data-stu-id="06a3c-104">Tuning is controlled by the TV Tuner filter, through the [**IAMTVTuner**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner) interface.</span></span> <span data-ttu-id="06a3c-105">L'interfaccia Impossibile IAMTVTuner eredita IAMTuner.</span><span class="sxs-lookup"><span data-stu-id="06a3c-105">The IAMTVTuner interface inherits IAMTuner.</span></span> <span data-ttu-id="06a3c-106">Per ottenere un puntatore all'interfaccia, chiamare il metodo [**ICaptureGraphBuilder2:: FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="06a3c-106">To obtain a pointer to the interface, call the [**ICaptureGraphBuilder2::FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) method as follows:</span></span>


```C++
IAMTVTuner *pTuner = NULL;
hr = pBuild->FindInterface(
    &LOOK_UPSTREAM_ONLY,  // Look upstream from pCap.
    NULL,                 // No particular media type.
    pCap,                 // Pointer to the capture filter.
    IID_IAMTVTuner, (void**)&pTuner);
if (SUCCEEDED(hr))
{
    // Use pTuner ...
    pTuner->Release();
}
```



<span data-ttu-id="06a3c-107">Il primo parametro indica di cercare upstream dal filtro di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="06a3c-107">The first parameter indicates to search upstream from the capture filter.</span></span>

<span data-ttu-id="06a3c-108">Tabelle Frequency</span><span class="sxs-lookup"><span data-stu-id="06a3c-108">Frequency Tables</span></span>

<span data-ttu-id="06a3c-109">Internamente, il filtro del sintonizzatore TV mantiene un elenco di tabelle di frequenza.</span><span class="sxs-lookup"><span data-stu-id="06a3c-109">Internally, the TV Tuner filter keeps a list of frequency tables.</span></span> <span data-ttu-id="06a3c-110">Ogni tabella Frequency corrisponde alle frequenze broadcast o Cable per un determinato paese/area geografica.</span><span class="sxs-lookup"><span data-stu-id="06a3c-110">Each frequency table corresponds to the broadcast or cable frequencies for a given country/region.</span></span> <span data-ttu-id="06a3c-111">Esiste anche una tabella di frequenza "Unicable" generica che viene usata quando un paese/area geografica non dispone di un set standard di assegnazioni di frequenza.</span><span class="sxs-lookup"><span data-stu-id="06a3c-111">There is also a generic "Unicable" frequency table, which is used when a country/region does not have a standard set of frequency assignments.</span></span>

<span data-ttu-id="06a3c-112">Ogni tabella Frequency contiene un elenco di frequenze di ottimizzazione.</span><span class="sxs-lookup"><span data-stu-id="06a3c-112">Each frequency table contains a list of tuning frequencies.</span></span> <span data-ttu-id="06a3c-113">Per alcuni paesi o aree geografiche, gli indici della tabella corrispondono direttamente ai numeri di canale, ovvero la frequenza per il canale n è la n voce nella tabella.</span><span class="sxs-lookup"><span data-stu-id="06a3c-113">For some countries/regions, the indexes in the table correspond directly to channel numbers — in other words, the frequency for channel n is the n th entry in the table.</span></span> <span data-ttu-id="06a3c-114">Per alcuni paesi o aree geografiche, tuttavia, non esiste alcuna corrispondenza diretta tra numeri di canale e frequenze.</span><span class="sxs-lookup"><span data-stu-id="06a3c-114">For some countries/regions, however, there is no direct correspondence between channel numbers and frequencies.</span></span> <span data-ttu-id="06a3c-115">In tal caso, l'applicazione deve contenere un elenco che esegue il mapping dei numeri di canale, in genere scelti dall'utente, alle voci della tabella Frequency.</span><span class="sxs-lookup"><span data-stu-id="06a3c-115">In that case, the application must keep a list that maps channel numbers (typically chosen by the user) to frequency table entries.</span></span> <span data-ttu-id="06a3c-116">Ad esempio, l'elemento visualizzato dall'utente come "Channel 5" potrebbe essere il numero di porta 12 nella tabella Frequency.</span><span class="sxs-lookup"><span data-stu-id="06a3c-116">For example, what the user sees as "channel 5" might be entry number 12 in the frequency table.</span></span>

<span data-ttu-id="06a3c-117">Per informazioni dettagliate, vedere la pagina relativa all' [ottimizzazione della TV analoga internazionale](international-analog-tv-tuning.md).</span><span class="sxs-lookup"><span data-stu-id="06a3c-117">For details, see [International Analog TV Tuning](international-analog-tv-tuning.md).</span></span>

<span data-ttu-id="06a3c-118">Operazioni di ottimizzazione di base</span><span class="sxs-lookup"><span data-stu-id="06a3c-118">Basic Tuning Operations</span></span>

<span data-ttu-id="06a3c-119">Se il sintonizzatore supporta più modalità di ricezione, ad esempio la televisione e la radio FM, chiamare [**IAMTuner::p \_ modalità UT**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_mode) per selezionare la modalità.</span><span class="sxs-lookup"><span data-stu-id="06a3c-119">If the tuner supports multiple reception modes, such as television and FM radio, call [**IAMTuner::put\_Mode**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_mode) to select the mode.</span></span> <span data-ttu-id="06a3c-120">Il metodo [**IAMTuner:: GetAvailableModes**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-getavailablemodes) restituisce tutte le modalità supportate dal sintonizzatore.</span><span class="sxs-lookup"><span data-stu-id="06a3c-120">The [**IAMTuner::GetAvailableModes**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-getavailablemodes) method returns all of the modes that the tuner supports.</span></span> <span data-ttu-id="06a3c-121">Il codice seguente, ad esempio, controlla se il Tuner supporta FM radio e, in tal caso, passa a tale modalità.</span><span class="sxs-lookup"><span data-stu-id="06a3c-121">For example, the following code checks whether the tuner supports FM radio, and if so, switches to that mode.</span></span>


```C++
// Check whether the mode is supported.
long lModes = 0;
hr = m_pTuner->GetAvailableModes(&lModes);
if (SUCCEEDED(hr) && (lModes & AMTUNER_MODE_FM_RADIO))
{
    // Set the mode.
    hr = pTuner->put_Mode(AMTUNER_MODE_FM_RADIO);
}
```



<span data-ttu-id="06a3c-122">Per impostare il paese/area geografica, chiamare il metodo [**IAMTuner::p UT \_ CountryCode**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_countrycode) .</span><span class="sxs-lookup"><span data-stu-id="06a3c-122">To set the country/region, call the [**IAMTuner::put\_CountryCode**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_countrycode) method.</span></span> <span data-ttu-id="06a3c-123">Il sintonizzatore utilizza questo valore per selezionare la tabella di frequenza appropriata.</span><span class="sxs-lookup"><span data-stu-id="06a3c-123">The tuner uses this value to select the appropriate frequency table.</span></span> <span data-ttu-id="06a3c-124">Per ulteriori informazioni, vedere [assegnazioni di paese/area geografica](country-region-assignments.md) .</span><span class="sxs-lookup"><span data-stu-id="06a3c-124">See [Country/Region Assignments](country-region-assignments.md) for more information.</span></span>

<span data-ttu-id="06a3c-125">Per impostare il canale, chiamare il metodo [**IAMTuner::p UT \_ Channel**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) .</span><span class="sxs-lookup"><span data-stu-id="06a3c-125">To set the channel, call the [**IAMTuner::put\_Channel**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) method.</span></span> <span data-ttu-id="06a3c-126">L'argomento di questo metodo non è in realtà un numero di canale, bensì un indice nella tabella della frequenza corrente.</span><span class="sxs-lookup"><span data-stu-id="06a3c-126">The argument to this method is actually not a channel number, but rather an index into the current frequency table.</span></span> <span data-ttu-id="06a3c-127">Come descritto in precedenza, il numero di indice può corrispondere o meno a un numero di canale.</span><span class="sxs-lookup"><span data-stu-id="06a3c-127">As described previously, the index number may or may not correspond to a channel number.</span></span> <span data-ttu-id="06a3c-128">Il metodo [**IAMTuner:: ChannelMinMax**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-channelminmax) restituisce i valori di indice minimo e massimo per la tabella di frequenza corrente.</span><span class="sxs-lookup"><span data-stu-id="06a3c-128">The [**IAMTuner::ChannelMinMax**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-channelminmax) method returns the minimum and maximum index values for the current frequency table.</span></span>

<span data-ttu-id="06a3c-129">Sostituzione di voci di frequenza</span><span class="sxs-lookup"><span data-stu-id="06a3c-129">Overriding Frequency Entries</span></span>

<span data-ttu-id="06a3c-130">È possibile che alcune voci nelle tabelle di frequenza potrebbero non essere corrette o diventare obsolete.</span><span class="sxs-lookup"><span data-stu-id="06a3c-130">It is possible that some entries in the frequency tables might be incorrect or become obsolete.</span></span> <span data-ttu-id="06a3c-131">Viene pertanto fornito un meccanismo per eseguire l'override delle singole voci utilizzando le chiavi del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="06a3c-131">Therefore, a mechanism is provided for overriding individual entries using registry keys.</span></span>

<span data-ttu-id="06a3c-132">Le specifiche sono illustrate nell'argomento [ottimizzazione della TV analoga internazionale](international-analog-tv-tuning.md).</span><span class="sxs-lookup"><span data-stu-id="06a3c-132">The specifics are explained in the topic [International Analog TV Tuning](international-analog-tv-tuning.md).</span></span> <span data-ttu-id="06a3c-133">Ogni chiave del registro di sistema definisce uno spazio di ottimizzazione che contiene una o più sottochiavi.</span><span class="sxs-lookup"><span data-stu-id="06a3c-133">Each registry key defines a "tuning space" which contains one or more subkeys.</span></span> <span data-ttu-id="06a3c-134">Ogni sottochiave esegue l'override di una voce di frequenza.</span><span class="sxs-lookup"><span data-stu-id="06a3c-134">Each subkey overrides one frequency entry.</span></span> <span data-ttu-id="06a3c-135">Per impostare lo spazio di ottimizzazione corrente, usare il metodo [**IAMTuner::p UT \_ TuningSpace**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_tuningspace) .</span><span class="sxs-lookup"><span data-stu-id="06a3c-135">To set the current tuning space, use the [**IAMTuner::put\_TuningSpace**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_tuningspace) method.</span></span> <span data-ttu-id="06a3c-136">L'attivazione dello spazio di ottimizzazione sostituisce le voci di frequenza nella tabella di frequenza corrente.</span><span class="sxs-lookup"><span data-stu-id="06a3c-136">Activating the tuning space overrides the frequency entries in the current frequency table.</span></span> <span data-ttu-id="06a3c-137">Pertanto, l'applicazione deve mantenere una corrispondenza tra gli spazi di ottimizzazione e i paesi/aree geografiche.</span><span class="sxs-lookup"><span data-stu-id="06a3c-137">Therefore, it is up to the application to maintain a correspondence between tuning spaces and countries/regions.</span></span> <span data-ttu-id="06a3c-138">L'approccio migliore consiste semplicemente nell'usare l'identificatore Country/Region come nome dello spazio di ottimizzazione.</span><span class="sxs-lookup"><span data-stu-id="06a3c-138">The best approach is simply to use the country/region identifier as the name of the tuning space.</span></span>

<span data-ttu-id="06a3c-139">Ottimizzazione delle voci di frequenza</span><span class="sxs-lookup"><span data-stu-id="06a3c-139">Fine Tuning the Frequency Entries</span></span>

<span data-ttu-id="06a3c-140">Le frequenze di broadcast possono essere regolate in base a diversi kHz dalla stazione di broadcast per ridurre la potenziale interferenza con i canali adiacenti.</span><span class="sxs-lookup"><span data-stu-id="06a3c-140">Broadcast frequencies may be adjusted up or down several kHz by the broadcast station to reduce potential interference with neighboring channels.</span></span> <span data-ttu-id="06a3c-141">Data la frequenza nominale, la scheda Tuner può analizzare la frequenza esatta.</span><span class="sxs-lookup"><span data-stu-id="06a3c-141">Given the nominal frequency, the tuner card can scan for the exact frequency.</span></span> <span data-ttu-id="06a3c-142">Il filtro del sintonizzatore TV dispone di un meccanismo per il salvataggio delle frequenze modificate nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="06a3c-142">The TV Tuner filter has a mechanism for saving the adjusted frequencies in the registry.</span></span>

<span data-ttu-id="06a3c-143">Per ogni voce nella tabella Frequency, chiamare il metodo Put \_ Channel per ottimizzare la frequenza.</span><span class="sxs-lookup"><span data-stu-id="06a3c-143">For each entry in the frequency table, call the put\_Channel method to tune to that frequency.</span></span> <span data-ttu-id="06a3c-144">Il sintonizzatore analizzerà la frequenza più precisa.</span><span class="sxs-lookup"><span data-stu-id="06a3c-144">The tuner will scan for the most precise frequency.</span></span> <span data-ttu-id="06a3c-145">È possibile verificare se il sintonizzatore ha eseguito un blocco orizzontale chiamando [**IAMTuner:: SignalPresent**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-signalpresent).</span><span class="sxs-lookup"><span data-stu-id="06a3c-145">You can check whether the tuner achieved a horizontal lock by calling [**IAMTuner::SignalPresent**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-signalpresent).</span></span> <span data-ttu-id="06a3c-146">Il filtro del sintonizzatore TV archivia anche il risultato internamente.</span><span class="sxs-lookup"><span data-stu-id="06a3c-146">The TV Tuner filter also stores the result internally.</span></span>

<span data-ttu-id="06a3c-147">Dopo aver analizzato tutte le frequenze, chiamare il metodo [**Impossibile IAMTVTuner:: StoreAutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-storeautotune) per scrivere i valori aggiornati nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="06a3c-147">After scanning all of the frequencies, call the [**IAMTVTuner::StoreAutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-storeautotune) method to write the updated values into the registry.</span></span> <span data-ttu-id="06a3c-148">I valori aggiornati vengono archiviati nella voce del registro di sistema per lo spazio di ottimizzazione corrente.</span><span class="sxs-lookup"><span data-stu-id="06a3c-148">The updated values are stored under the registry entry for the current tuning space.</span></span>

## <a name="related-topics"></a><span data-ttu-id="06a3c-149">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="06a3c-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06a3c-150">Televisione analoga</span><span class="sxs-lookup"><span data-stu-id="06a3c-150">Analog Television</span></span>](analog-television.md)
</dt> </dl>

 

 



