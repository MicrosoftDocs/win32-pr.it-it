---
description: Raccolta di informazioni Fine-Tuning
ms.assetid: 0d9ea896-e0a9-411b-9a10-e366e3686a34
title: Raccolta di informazioni Fine-Tuning
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27d191f677acc9306202bce141ef8f6683b43c61
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303828"
---
# <a name="collecting-fine-tuning-information"></a><span data-ttu-id="109a8-103">Raccolta di informazioni Fine-Tuning</span><span class="sxs-lookup"><span data-stu-id="109a8-103">Collecting Fine-Tuning Information</span></span>

<span data-ttu-id="109a8-104">Sebbene le frequenze dei cavi siano in genere esatte, le frequenze di broadcast possono essere regolate verso l'alto o verso il basso di diversi kHz dalla stazione di trasmissione per ridurre la potenziale interferenza con i canali adiacenti.</span><span class="sxs-lookup"><span data-stu-id="109a8-104">Although cable frequencies are generally expected to be exact, broadcast frequencies may be adjusted up or down several kHz by the broadcast station to reduce potential interference with neighboring channels.</span></span>

<span data-ttu-id="109a8-105">Quando il filtro del sintonizzatore TV si sintonizza su un canale, analizza il segnale più preciso.</span><span class="sxs-lookup"><span data-stu-id="109a8-105">When the TV Tuner filter tunes to a channel, it scans for the most precise signal.</span></span> <span data-ttu-id="109a8-106">Per salvare queste informazioni nel registro di sistema per le successive operazioni di ottimizzazione, procedere come segue:</span><span class="sxs-lookup"><span data-stu-id="109a8-106">To save this information in the registry for subsequent tuning operations, do the following:</span></span>

1.  <span data-ttu-id="109a8-107">Chiamare [**IAMTuner:: ChannelMinMax**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-channelminmax) per determinare l'intervallo di voci di frequenza nella tabella di frequenza corrente.</span><span class="sxs-lookup"><span data-stu-id="109a8-107">Call [**IAMTuner::ChannelMinMax**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-channelminmax) to determine the range of frequency entries in the current frequency table.</span></span>
2.  <span data-ttu-id="109a8-108">Chiamare il metodo [**IAMTuner::p il \_ canale UT**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) una volta per ogni indice di frequenza nell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="109a8-108">Call the [**IAMTuner::put\_Channel**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) method once for each frequency index in the range.</span></span>
3.  <span data-ttu-id="109a8-109">Chiamare [**Impossibile IAMTVTuner:: StoreAutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-storeautotune) per salvare le informazioni di ottimizzazione nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="109a8-109">Call [**IAMTVTuner::StoreAutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-storeautotune) to save the fine-tuning information in the registry.</span></span> <span data-ttu-id="109a8-110">Le informazioni vengono archiviate nella chiave del registro di sistema per lo spazio di ottimizzazione corrente.</span><span class="sxs-lookup"><span data-stu-id="109a8-110">The information is stored under the registry key for the current tuning space.</span></span>

<span data-ttu-id="109a8-111">Il codice seguente illustra questi passaggi:</span><span class="sxs-lookup"><span data-stu-id="109a8-111">The following code shows these steps:</span></span>


```C++
long lMin = 0, lMax = 0;
hr = pTuner->ChannelMinMax(&lMin, &lMax);
if (SUCCEEDED(hr))
{
    for (long i = lMin; i <= lMax; i++)
    {
        pTuner->put_Channel(i, AMTUNER_SUBCHAN_DEFAULT,
            AMTUNER_SUBCHAN_DEFAULT)
    }
    pTuner->StoreAutoTune();
}
```



<span data-ttu-id="109a8-112">Con le versioni precedenti del filtro del sintonizzatore TV, è stato consigliato il metodo [**Impossibile IAMTVTuner:: Autotune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-autotune) per l'ottimizzazione.</span><span class="sxs-lookup"><span data-stu-id="109a8-112">With earlier versions of the TV Tuner filter, the [**IAMTVTuner::AutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-autotune) method was recommended for fine-tuning.</span></span> <span data-ttu-id="109a8-113">Tuttavia, questo metodo ignora gli override di frequenza, quindi il suo utilizzo non è più consigliabile.</span><span class="sxs-lookup"><span data-stu-id="109a8-113">However, this method ignores any frequency overrides, so its use is no longer recommended.</span></span> <span data-ttu-id="109a8-114">Il codice seguente è equivalente al metodo **Autotune** , ma funziona correttamente con gli override di frequenza:</span><span class="sxs-lookup"><span data-stu-id="109a8-114">The following code is equivalent to the **AutoTune** method, but works correctly with frequency overrides:</span></span>


```C++
HRESULT MyAutoTune(IAMTVTuner *pTuner, long lIndex, long *plFoundSignal)
{
    long SignalStrength = AMTUNER_NOSIGNAL;
    HRESULT hr;
    hr = pTuner->put_Channel(lIndex, AMTUNER_SUBCHAN_DEFAULT, AMTUNER_SUBCHAN_DEFAULT);
    if (NOERROR == hr)
        pTuner->SignalPresent(&SignalStrength);
    *plFoundSignal = (SignalStrength != AMTUNER_NOSIGNAL);
        return hr;
}
```



<span data-ttu-id="109a8-115">Con la ricezione broadcast, non è sempre possibile ottenere un blocco orizzontale, anche se l'immagine è visualizzabile.</span><span class="sxs-lookup"><span data-stu-id="109a8-115">With broadcast reception, it is not always possible to get a horizontal lock, although the picture is viewable.</span></span> <span data-ttu-id="109a8-116">In questi casi, l'hardware del sintonizzatore avrà un blocco di frequenza, ma il decodificatore non avrà un blocco orizzontale.</span><span class="sxs-lookup"><span data-stu-id="109a8-116">In these cases, the tuner hardware will have a frequency lock, but the decoder will not have horizontal lock.</span></span> <span data-ttu-id="109a8-117">Questa condizione può essere rilevata quando si usa il [**\_ canale put**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) o l' [**ottimizzazione**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-autotune) automatica esaminando il codice restituito.</span><span class="sxs-lookup"><span data-stu-id="109a8-117">This condition can be detected when using [**put\_Channel**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) or [**AutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-autotune) by examining the return code.</span></span>



| <span data-ttu-id="109a8-118">Valore</span><span class="sxs-lookup"><span data-stu-id="109a8-118">Value</span></span>    | <span data-ttu-id="109a8-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="109a8-119">Description</span></span>                                                                                                                                                                               |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="109a8-120">\_OK</span><span class="sxs-lookup"><span data-stu-id="109a8-120">S\_OK</span></span>    | <span data-ttu-id="109a8-121">L'operazione di ottimizzazione è riuscita e il sintonizzatore ha ottenuto un blocco di frequenza.</span><span class="sxs-lookup"><span data-stu-id="109a8-121">The tune operation succeeded and the tuner got a frequency lock.</span></span>                                                                                                                          |
| <span data-ttu-id="109a8-122">S \_ false</span><span class="sxs-lookup"><span data-stu-id="109a8-122">S\_FALSE</span></span> | <span data-ttu-id="109a8-123">Non si sono verificati errori durante l'operazione di ottimizzazione, ma il sintonizzatore non è stato in grado di ottenere un blocco di frequenza.</span><span class="sxs-lookup"><span data-stu-id="109a8-123">There were no errors during the tune operation, but the tuner was not able to get a frequency lock.</span></span> <span data-ttu-id="109a8-124">È molto improbabile che sia presente un canale visualizzabile risultante da questa operazione.</span><span class="sxs-lookup"><span data-stu-id="109a8-124">It is highly unlikely that there is a viewable channel resulting from this operation.</span></span> |



 

<span data-ttu-id="109a8-125">Qualsiasi altro codice restituito indica che si è verificato un errore.</span><span class="sxs-lookup"><span data-stu-id="109a8-125">Any other return code indicates that some error occurred.</span></span>

<span data-ttu-id="109a8-126">Un valore restituito di S \_ OK non garantisce che il decodificatore abbia un blocco orizzontale.</span><span class="sxs-lookup"><span data-stu-id="109a8-126">A return value of S\_OK does not guarantee that the decoder has a horizontal lock.</span></span> <span data-ttu-id="109a8-127">Il metodo [**Autotune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-autotune) aggiorna il parametro *FoundSignal* per indicare se è stato eseguito o meno il blocco orizzontale.</span><span class="sxs-lookup"><span data-stu-id="109a8-127">The [**AutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-autotune) method updates the *FoundSignal* parameter to indicate whether or not horizontal lock was achieved.</span></span> <span data-ttu-id="109a8-128">Il metodo [**IAMTuner:: SignalPresent**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-signalpresent) restituisce le stesse informazioni.</span><span class="sxs-lookup"><span data-stu-id="109a8-128">The [**IAMTuner::SignalPresent**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-signalpresent) method returns the same information.</span></span>

<span data-ttu-id="109a8-129">Se il valore restituito è \_ OK, tuttavia, l'applicazione ha la possibilità di ignorare il parametro *FoundSignal* , perché il sintonizzatore segnala un blocco di frequenza.</span><span class="sxs-lookup"><span data-stu-id="109a8-129">When the return value is S\_OK, however, the application has the option of ignoring the *FoundSignal* parameter, because the tuner is reporting a frequency lock.</span></span> <span data-ttu-id="109a8-130">È possibile che si verifichi un blocco di frequenza sul rumore, ma è opportuno valutare la possibilità di ignorare i canali visualizzabili.</span><span class="sxs-lookup"><span data-stu-id="109a8-130">There is the possibility of a frequency lock on noise, but this possibility should be weighed against the possibility of skipping viewable channels.</span></span>

## <a name="registry-conversion"></a><span data-ttu-id="109a8-131">Conversione del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="109a8-131">Registry Conversion</span></span>

<span data-ttu-id="109a8-132">Per supportare le sostituzioni di frequenza, è stato modificato il formato interno della chiave del registro di sistema che contiene le informazioni di ottimizzazione.</span><span class="sxs-lookup"><span data-stu-id="109a8-132">To support frequency overrides, the internal format of the registry key that holds fine-tuning information has changed.</span></span> <span data-ttu-id="109a8-133">Il formato originale è ancora supportato per la compatibilità con le versioni precedenti, ma non supporta le sostituzioni di frequenza.</span><span class="sxs-lookup"><span data-stu-id="109a8-133">The original format is still supported for backward compatibility, but it does not support frequency overrides.</span></span>

<span data-ttu-id="109a8-134">Il formato del registro di sistema precedente viene convertito nel nuovo formato ogni volta che viene chiamato il metodo [**Impossibile IAMTVTuner:: StoreAutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-storeautotune) .</span><span class="sxs-lookup"><span data-stu-id="109a8-134">The old registry format is converted to the new format whenever the [**IAMTVTuner::StoreAutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-storeautotune) method is called.</span></span> <span data-ttu-id="109a8-135">Se l'applicazione aggiunge sostituzioni di frequenza, deve chiamare il metodo **StoreAutoTune** per eseguire la conversione nel nuovo formato del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="109a8-135">If your application adds frequency overrides, it should call the **StoreAutoTune** method to convert to the new registry format.</span></span> <span data-ttu-id="109a8-136">Non è necessario raccogliere informazioni di ottimizzazione prima di chiamare **StoreAutoTune**.</span><span class="sxs-lookup"><span data-stu-id="109a8-136">It is not necessary to collect any fine-tuning information before calling **StoreAutoTune**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="109a8-137">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="109a8-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="109a8-138">Ottimizzazione della TV analoga internazionale</span><span class="sxs-lookup"><span data-stu-id="109a8-138">International Analog TV Tuning</span></span>](international-analog-tv-tuning.md)
</dt> </dl>

 

 



