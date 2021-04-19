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
# <a name="analog-television-tuning"></a>Ottimizzazione della televisione analoga

L'ottimizzazione viene controllata dal filtro del sintonizzatore TV tramite l'interfaccia [**Impossibile IAMTVTuner**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner) . L'interfaccia Impossibile IAMTVTuner eredita IAMTuner. Per ottenere un puntatore all'interfaccia, chiamare il metodo [**ICaptureGraphBuilder2:: FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) come indicato di seguito:


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



Il primo parametro indica di cercare upstream dal filtro di acquisizione.

Tabelle Frequency

Internamente, il filtro del sintonizzatore TV mantiene un elenco di tabelle di frequenza. Ogni tabella Frequency corrisponde alle frequenze broadcast o Cable per un determinato paese/area geografica. Esiste anche una tabella di frequenza "Unicable" generica che viene usata quando un paese/area geografica non dispone di un set standard di assegnazioni di frequenza.

Ogni tabella Frequency contiene un elenco di frequenze di ottimizzazione. Per alcuni paesi o aree geografiche, gli indici della tabella corrispondono direttamente ai numeri di canale, ovvero la frequenza per il canale n è la n voce nella tabella. Per alcuni paesi o aree geografiche, tuttavia, non esiste alcuna corrispondenza diretta tra numeri di canale e frequenze. In tal caso, l'applicazione deve contenere un elenco che esegue il mapping dei numeri di canale, in genere scelti dall'utente, alle voci della tabella Frequency. Ad esempio, l'elemento visualizzato dall'utente come "Channel 5" potrebbe essere il numero di porta 12 nella tabella Frequency.

Per informazioni dettagliate, vedere la pagina relativa all' [ottimizzazione della TV analoga internazionale](international-analog-tv-tuning.md).

Operazioni di ottimizzazione di base

Se il sintonizzatore supporta più modalità di ricezione, ad esempio la televisione e la radio FM, chiamare [**IAMTuner::p \_ modalità UT**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_mode) per selezionare la modalità. Il metodo [**IAMTuner:: GetAvailableModes**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-getavailablemodes) restituisce tutte le modalità supportate dal sintonizzatore. Il codice seguente, ad esempio, controlla se il Tuner supporta FM radio e, in tal caso, passa a tale modalità.


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



Per impostare il paese/area geografica, chiamare il metodo [**IAMTuner::p UT \_ CountryCode**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_countrycode) . Il sintonizzatore utilizza questo valore per selezionare la tabella di frequenza appropriata. Per ulteriori informazioni, vedere [assegnazioni di paese/area geografica](country-region-assignments.md) .

Per impostare il canale, chiamare il metodo [**IAMTuner::p UT \_ Channel**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) . L'argomento di questo metodo non è in realtà un numero di canale, bensì un indice nella tabella della frequenza corrente. Come descritto in precedenza, il numero di indice può corrispondere o meno a un numero di canale. Il metodo [**IAMTuner:: ChannelMinMax**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-channelminmax) restituisce i valori di indice minimo e massimo per la tabella di frequenza corrente.

Sostituzione di voci di frequenza

È possibile che alcune voci nelle tabelle di frequenza potrebbero non essere corrette o diventare obsolete. Viene pertanto fornito un meccanismo per eseguire l'override delle singole voci utilizzando le chiavi del registro di sistema.

Le specifiche sono illustrate nell'argomento [ottimizzazione della TV analoga internazionale](international-analog-tv-tuning.md). Ogni chiave del registro di sistema definisce uno spazio di ottimizzazione che contiene una o più sottochiavi. Ogni sottochiave esegue l'override di una voce di frequenza. Per impostare lo spazio di ottimizzazione corrente, usare il metodo [**IAMTuner::p UT \_ TuningSpace**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_tuningspace) . L'attivazione dello spazio di ottimizzazione sostituisce le voci di frequenza nella tabella di frequenza corrente. Pertanto, l'applicazione deve mantenere una corrispondenza tra gli spazi di ottimizzazione e i paesi/aree geografiche. L'approccio migliore consiste semplicemente nell'usare l'identificatore Country/Region come nome dello spazio di ottimizzazione.

Ottimizzazione delle voci di frequenza

Le frequenze di broadcast possono essere regolate in base a diversi kHz dalla stazione di broadcast per ridurre la potenziale interferenza con i canali adiacenti. Data la frequenza nominale, la scheda Tuner può analizzare la frequenza esatta. Il filtro del sintonizzatore TV dispone di un meccanismo per il salvataggio delle frequenze modificate nel registro di sistema.

Per ogni voce nella tabella Frequency, chiamare il metodo Put \_ Channel per ottimizzare la frequenza. Il sintonizzatore analizzerà la frequenza più precisa. È possibile verificare se il sintonizzatore ha eseguito un blocco orizzontale chiamando [**IAMTuner:: SignalPresent**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-signalpresent). Il filtro del sintonizzatore TV archivia anche il risultato internamente.

Dopo aver analizzato tutte le frequenze, chiamare il metodo [**Impossibile IAMTVTuner:: StoreAutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-storeautotune) per scrivere i valori aggiornati nel registro di sistema. I valori aggiornati vengono archiviati nella voce del registro di sistema per lo spazio di ottimizzazione corrente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Televisione analoga](analog-television.md)
</dt> </dl>

 

 



