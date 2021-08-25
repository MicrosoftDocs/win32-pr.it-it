---
title: Configurazione dei Flussi video per la ricerca di prestazioni
description: Configurazione dei Flussi video per la ricerca di prestazioni
ms.assetid: 2df507f9-60a5-4489-b3db-7fe15604e625
keywords:
- flussi, configurazione di flussi video
- codec, configurazione di flussi video
- flussi video, configurazione
- flussi video, prestazioni
- prestazioni, flussi video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b7a21e6352d03375b680702a16190b4af9eef24ca7ba9d592adb79ab5794b5c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119840161"
---
# <a name="configuring-video-streams-for-seeking-performance"></a>Configurazione dei Flussi video per la ricerca di prestazioni

Alcune applicazioni di riproduzione eseguono molte operazioni di ricerca su singoli flussi. La ricerca è un'area in cui le prestazioni possono variare notevolmente a seconda delle impostazioni del flusso. Se si sa che il contenuto deve essere ottimizzato per la ricerca rapida, è possibile personalizzare la configurazione del flusso per migliorare le prestazioni.

Il fattore più importante che influisce sulla velocità delle operazioni di ricerca nel video è la spaziatura dei fotogrammi chiave. Poiché ogni fotogramma tra i fotogrammi chiave deve essere ricostruito in base ai fotogrammi precedenti, i fotogrammi chiave con spazi molto spaziati comportano tempi di ricerca più lunghi. Ad esempio, se un flusso video con 30 fotogrammi al secondo ha una spaziatura massima dei fotogrammi chiave di 10 secondi, ci sono potenzialmente 300 fotogrammi tra i fotogrammi chiave. Se si cerca l'ultimo [*frame differenziale,*](wmformat-glossary.md)è necessario ricostruire 299 fotogrammi per decompressire il frame. Se la ricostruzione di ogni fotogramma ha richiesto 0,01 secondi, la ricerca potrebbe richiedere quasi 3 secondi. Se si vuole aumentare l'efficienza della ricerca, ridurre la spaziatura dei fotogrammi chiave può essere utile. Tuttavia, se si impostano i fotogrammi chiave troppo vicini, si può perdere la qualità.

È possibile impostare la spaziatura massima dei fotogrammi chiave chiamando [**IWMVideoMediaProps::SetMaxKeyFrameSpacing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmvideomediaprops-setmaxkeyframespacing). I valori consigliati, in base alla velocità in bit del flusso, sono elencati nella tabella seguente. Questi valori offrono un buon equilibrio tra prestazioni e qualità. L'SDK non applica alcun limite al tempo tra fotogrammi chiave. In generale, tempi più lunghi di 30 secondi possono influire negativamente sui tempi di ricerca sia quando il contenuto viene trasmesso in rete che quando viene riprodotto in locale.



| Velocità in bit             | Spaziatura massima dei fotogrammi chiave suggerita |
|----------------------|-------------------------------------|
| Da 22 Kbps a 300 Kbps  | 8 secondi                           |
| Da 300 Kbps a 600 Kbps | 6 secondi                           |
| Da 600 Kbps a 2 Mbps   | 4 secondi                           |
| 2 Mbps e versioni successive    | 3 secondi                           |



 

Per altre informazioni su come ottenere prestazioni ottimali quando si cercano file video, vedere [Ottenere le migliori prestazioni di ricerca video.](getting-the-best-video-seeking-performance.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Configurazione di Flussi**](configuring-streams.md)
</dt> </dl>

 

 




