---
title: Configurazione dei flussi video per le prestazioni di ricerca
description: Configurazione dei flussi video per le prestazioni di ricerca
ms.assetid: 2df507f9-60a5-4489-b3db-7fe15604e625
keywords:
- flussi, configurazione di flussi video
- codec, configurazione dei flussi video
- flussi video, configurazione
- flussi video, prestazioni
- prestazioni, flussi video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33b4fc68e0b3a91cf135d29dc7123d5af88db84c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723438"
---
# <a name="configuring-video-streams-for-seeking-performance"></a>Configurazione dei flussi video per le prestazioni di ricerca

Alcune applicazioni di riproduzione eseguono molte ricerche nei singoli flussi. La ricerca è un'area in cui le prestazioni possono variare significativamente a seconda delle impostazioni del flusso. Se si sa che il contenuto deve essere ottimizzato per la ricerca rapida, è possibile personalizzare la configurazione del flusso per migliorare le prestazioni.

Il fattore più importante che influisce sulla velocità delle operazioni di ricerca nel video è la spaziatura dei fotogrammi chiave. Poiché ogni frame tra fotogrammi chiave deve essere ricostruito in base ai frame che lo precedono, i fotogrammi chiave con spazi ampi risultano più lunghi. Se, ad esempio, un flusso video con 30 fotogrammi al secondo ha una spaziatura massima con fotogrammi chiave di 10 secondi, esistono potenzialmente 300 di frame tra fotogrammi chiave. Se si cerca l'ultimo [*frame Delta*](wmformat-glossary.md), è necessario ricostruire i frame 299 per la decompressione del fotogramma. Se ogni ricostruzione di frame ha richiesto .01 secondi, la ricerca richiederebbe circa 3 secondi. Se si desidera aumentare l'efficienza della ricerca, è possibile ridurre la spaziatura dei fotogrammi chiave. Tuttavia, se si impostano i fotogrammi chiave troppo vicini, è possibile perdere la qualità.

È possibile impostare la spaziatura massima del fotogramma chiave chiamando [**IWMVideoMediaProps:: SetMaxKeyFrameSpacing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmvideomediaprops-setmaxkeyframespacing). I valori consigliati, in base alla velocità in bit del flusso, sono elencati nella tabella seguente. Questi valori rappresentano un equilibrio efficace tra la ricerca di prestazioni e qualità. L'SDK non impone alcun limite per il tempo tra i fotogrammi chiave. In generale, i tempi più lunghi di 30 secondi possono influire negativamente sui tempi di ricerca sia quando il contenuto viene trasmesso su una rete che quando viene riprodotto localmente.



| Velocità in bit             | Spaziatura massima consigliata per i fotogrammi chiave |
|----------------------|-------------------------------------|
| da 22 kbps a 300 kbps  | 8 secondi                           |
| 300 kbps a 600 Kbps | 6 secondi                           |
| da 600 kbps a 2 Mbps   | 4 secondi                           |
| 2 Mbps e versioni successive    | 3 secondi                           |



 

Per ulteriori informazioni su come ottenere prestazioni ottimali durante la ricerca di file video, vedere [ottenere le migliori prestazioni di ricerca dei video](getting-the-best-video-seeking-performance.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Configurazione di flussi**](configuring-streams.md)
</dt> </dl>

 

 




