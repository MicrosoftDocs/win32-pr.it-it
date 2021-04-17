---
description: Override della frequenza
ms.assetid: 0e45d0a6-3c3e-462c-a8dc-c4f25b614b85
title: Override della frequenza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57177e4990cb40be271fc551718964faf1696d2d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520658"
---
# <a name="frequency-overrides"></a>Override della frequenza

È stata impiegata una quantità significativa di lavoro per garantire la correttezza delle frequenze di broadcast e delle assegnazioni standard dei colori per ogni paese/area geografica. Anche in questo caso, si verificano situazioni in cui le tabelle di frequenza non sono sufficienti, contengono errori o diventano obsolete. Per risolvere questo problema, le frequenze elencate nelle tabelle di frequenza del filtro del sintonizzatore TV possono essere sostituite selettivamente, usando la chiave del registro di sistema seguente:

**HKEY \_ \_Computer locale** \\ **software** \\ **Microsoft** \\ **TV System Services** \\ **TVAutoTune** \\ **TS0-1**

> [!Note]  
> A partire da Windows 7, la chiave del registro di sistema reindirizzata seguente viene usata per le applicazioni x86 eseguite in versioni x64 di Windows:

 

**HKEY \_ \_Computer locale** \\ **software** \\ **Wow6432Node** \\ **Microsoft** \\ **TV System Services** \\ **TVAutoTune** \\ **TS0-1**

Gli override di frequenza sono raggruppati in "spazi di ottimizzazione" definiti dall'applicazione, identificati da Number. Nell'esempio seguente viene illustrato un override di esempio:

``` syntax
HKEY_LOCAL_MACHINE\Software\Microsoft\TV System Services\TVAutoTune\TS0-1
"12"=dword:04022750
```

In questo caso, "TS0-1" indica lo spazio di ottimizzazione 0 per le frequenze dei cavi. Il primo numero identifica lo spazio di ottimizzazione. Il secondo numero è 0 per le frequenze di broadcast o 1 per le frequenze dei cavi.

La sottochiave denominata "12" esegue l'override del valore Frequency per la frequenza in corrispondenza dell'indice 12 della tabella Frequency corrente. Il valore della sottochiave è un **DWORD** che specifica la frequenza in Hertz (Hz). In questo esempio, la frequenza è impostata su 67,25 MHz. È possibile definire le sostituzioni per qualsiasi numero di canale nell'intervallo compreso tra 1 e 999, inclusi. Se l'hardware di ottimizzazione non supporta una determinata frequenza, la richiesta di ottimizzazione avrà esito negativo.

Questo meccanismo può essere utilizzato anche per creare nuovi numeri di canale al di fuori dell'intervallo esistente nella tabella Frequency. Il metodo [**IAMTuner:: ChannelMinMax**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-channelminmax) restituirà l'intervallo di canali esteso. Se, ad esempio, l'intervallo di canali originale è compreso tra 1 e 158 e viene aggiunto un override del canale "200" al registro di sistema, il metodo **ChannelMinMax** restituirà 200 come canale massimo. In questo caso, ai numeri di canale compresi tra 159 e 199 non verrà assegnata alcuna frequenza, quindi le richieste di ottimizzazione in tale intervallo avranno automaticamente esito negativo.

Il metodo [**IAMTuner::p UT \_ TuningSpace**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_tuningspace) consente all'applicazione di scegliere il set di sostituzioni e le informazioni di ottimizzazione da usare. I numeri di spazio di ottimizzazione sono arbitrari. È responsabilità dell'applicazione mantenere la relazione tra lo spazio di ottimizzazione e la tabella Frequency. L'approccio più semplice consiste nell'usare il codice paese/area geografica come numero di spazio di ottimizzazione. Quindi, ogni volta che l'applicazione passa a un nuovo codice paese/area geografica, passa anche allo stesso spazio di ottimizzazione (in questo ordine).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Ottimizzazione della TV analoga internazionale](international-analog-tv-tuning.md)
</dt> </dl>

 

 



