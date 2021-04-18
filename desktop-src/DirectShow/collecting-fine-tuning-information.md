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
# <a name="collecting-fine-tuning-information"></a>Raccolta di informazioni Fine-Tuning

Sebbene le frequenze dei cavi siano in genere esatte, le frequenze di broadcast possono essere regolate verso l'alto o verso il basso di diversi kHz dalla stazione di trasmissione per ridurre la potenziale interferenza con i canali adiacenti.

Quando il filtro del sintonizzatore TV si sintonizza su un canale, analizza il segnale più preciso. Per salvare queste informazioni nel registro di sistema per le successive operazioni di ottimizzazione, procedere come segue:

1.  Chiamare [**IAMTuner:: ChannelMinMax**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-channelminmax) per determinare l'intervallo di voci di frequenza nella tabella di frequenza corrente.
2.  Chiamare il metodo [**IAMTuner::p il \_ canale UT**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) una volta per ogni indice di frequenza nell'intervallo.
3.  Chiamare [**Impossibile IAMTVTuner:: StoreAutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-storeautotune) per salvare le informazioni di ottimizzazione nel registro di sistema. Le informazioni vengono archiviate nella chiave del registro di sistema per lo spazio di ottimizzazione corrente.

Il codice seguente illustra questi passaggi:


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



Con le versioni precedenti del filtro del sintonizzatore TV, è stato consigliato il metodo [**Impossibile IAMTVTuner:: Autotune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-autotune) per l'ottimizzazione. Tuttavia, questo metodo ignora gli override di frequenza, quindi il suo utilizzo non è più consigliabile. Il codice seguente è equivalente al metodo **Autotune** , ma funziona correttamente con gli override di frequenza:


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



Con la ricezione broadcast, non è sempre possibile ottenere un blocco orizzontale, anche se l'immagine è visualizzabile. In questi casi, l'hardware del sintonizzatore avrà un blocco di frequenza, ma il decodificatore non avrà un blocco orizzontale. Questa condizione può essere rilevata quando si usa il [**\_ canale put**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) o l' [**ottimizzazione**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-autotune) automatica esaminando il codice restituito.



| Valore    | Descrizione                                                                                                                                                                               |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_OK    | L'operazione di ottimizzazione è riuscita e il sintonizzatore ha ottenuto un blocco di frequenza.                                                                                                                          |
| S \_ false | Non si sono verificati errori durante l'operazione di ottimizzazione, ma il sintonizzatore non è stato in grado di ottenere un blocco di frequenza. È molto improbabile che sia presente un canale visualizzabile risultante da questa operazione. |



 

Qualsiasi altro codice restituito indica che si è verificato un errore.

Un valore restituito di S \_ OK non garantisce che il decodificatore abbia un blocco orizzontale. Il metodo [**Autotune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-autotune) aggiorna il parametro *FoundSignal* per indicare se è stato eseguito o meno il blocco orizzontale. Il metodo [**IAMTuner:: SignalPresent**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-signalpresent) restituisce le stesse informazioni.

Se il valore restituito è \_ OK, tuttavia, l'applicazione ha la possibilità di ignorare il parametro *FoundSignal* , perché il sintonizzatore segnala un blocco di frequenza. È possibile che si verifichi un blocco di frequenza sul rumore, ma è opportuno valutare la possibilità di ignorare i canali visualizzabili.

## <a name="registry-conversion"></a>Conversione del registro di sistema

Per supportare le sostituzioni di frequenza, è stato modificato il formato interno della chiave del registro di sistema che contiene le informazioni di ottimizzazione. Il formato originale è ancora supportato per la compatibilità con le versioni precedenti, ma non supporta le sostituzioni di frequenza.

Il formato del registro di sistema precedente viene convertito nel nuovo formato ogni volta che viene chiamato il metodo [**Impossibile IAMTVTuner:: StoreAutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-storeautotune) . Se l'applicazione aggiunge sostituzioni di frequenza, deve chiamare il metodo **StoreAutoTune** per eseguire la conversione nel nuovo formato del registro di sistema. Non è necessario raccogliere informazioni di ottimizzazione prima di chiamare **StoreAutoTune**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Ottimizzazione della TV analoga internazionale](international-analog-tv-tuning.md)
</dt> </dl>

 

 



