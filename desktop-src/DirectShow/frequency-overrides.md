---
description: Sostituzioni di frequenza
ms.assetid: 0e45d0a6-3c3e-462c-a8dc-c4f25b614b85
title: Sostituzioni di frequenza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79a2c7663e70aa0e975cee52dc630453bea1ad4121a8c91d03564fe7d7a2cb4d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997840"
---
# <a name="frequency-overrides"></a>Sostituzioni di frequenza

È stata spesa una notevole quantità di impegno per garantire che le frequenze di trasmissione e le assegnazioni standard dei colori siano corrette per ogni paese/area geografica. Anche in questo caso, si verificano situazioni in cui le tabelle di frequenza non sono sufficienti, contengono errori o diventano obsolete. Per risolvere questo problema, le frequenze elencate nelle tabelle di frequenza del filtro siner TV possono essere sostituite in modo selettivo usando la chiave del Registro di sistema seguente:

**HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **TV System Services** \\ **TVAutoTune** \\ **TS0-1**

> [!Note]  
> A partire Windows 7, la chiave del Registro di sistema reindirizzata seguente viene usata per le applicazioni x86 in esecuzione in versioni x64 di Windows:

 

**HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Wow6432Node** \\ **Microsoft** \\ **TV System Services** \\ **TVAutoTune** \\ **TS0-1**

Le sostituzioni di frequenza sono raggruppate in "spazi di ottimizzazione" definiti dall'applicazione, identificati in base al numero. L'esempio seguente illustra un override di esempio:

``` syntax
HKEY_LOCAL_MACHINE\Software\Microsoft\TV System Services\TVAutoTune\TS0-1
"12"=dword:04022750
```

In questo caso, "TS0-1" indica lo spazio di ottimizzazione 0 per le frequenze dei cavi. Il primo numero identifica lo spazio di ottimizzazione. Il secondo numero è 0 per le frequenze di trasmissione o 1 per le frequenze dei cavi.

La sottochiave denominata "12" sostituisce il valore di frequenza per la frequenza in corrispondenza dell'indice 12 nella tabella di frequenza corrente. Il valore della sottochiave è un **valore DWORD** che specifica la frequenza in Hertz (Hz). In questo esempio la frequenza è impostata su 67,25 MHz. Le sostituzioni possono essere definite per tutti i numeri di canale compresi nell'intervallo compreso tra 1 e 999, inclusi. Se l'hardware di ottimizzazione non supporta una determinata frequenza, la richiesta di ottimizzazione avrà esito negativo.

Questo meccanismo può essere usato anche per creare nuovi numeri di canale al di fuori dell'intervallo esistente nella tabella delle frequenze. Il [**metodo IAMTuner::ChannelMinMax**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-channelminmax) restituirà l'intervallo di canali esteso. Ad esempio, se l'intervallo di canali originale è compreso tra 1 e 158 e viene aggiunto un override del canale "200" al Registro di sistema, il metodo **ChannelMinMax** restituirà 200 come canale massimo. In questo caso, ai numeri di canale nell'intervallo compreso tra 159 e 199 non saranno assegnate frequenze, quindi le richieste di ottimizzazione in tale intervallo avranno automaticamente esito negativo.

Il [**metodo IAMTuner::p ut \_ TuningSpace**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_tuningspace) consente all'applicazione di scegliere il set di sostituzioni e le informazioni di ottimizzazione da usare. I numeri di spazio di ottimizzazione sono arbitrari. È responsabilità dell'applicazione mantenere la relazione tra lo spazio di ottimizzazione e la tabella di frequenza. L'approccio più semplice consiste nell'usare il codice paese/area geografica come numero di spazio di ottimizzazione. Quindi, ogni volta che l'applicazione passa a un nuovo codice paese/area geografica, passa allo stesso spazio di ottimizzazione (in questo ordine).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Ottimizzazione tv analoga internazionale](international-analog-tv-tuning.md)
</dt> </dl>

 

 



