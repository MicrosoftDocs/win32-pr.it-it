---
description: Modalità Run-Time MPEG-2 demux
ms.assetid: b0d0c725-9220-43a5-af1c-d3c5c72e1ef3
title: Modalità Run-Time MPEG-2 demux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6e4e7a1dea0bfeccd60d8680a31b99cc10271ee
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125217"
---
# <a name="mpeg-2-demux-run-time-modes"></a>Modalità Run-Time MPEG-2 demux

Il [Demultiplexer MPEG-2](mpeg-2-demultiplexer.md) ("demux") può funzionare in modalità push o pull. In modalità push, i dati provengono da un'origine live, ad esempio una trasmissione di rete. In modalità pull i dati provengono da un file locale.

-   La modalità pull è disponibile in Windows XP e versioni successive per solo i flussi di programma. Nelle piattaforme di livello inferiore, usare il filtro con [separatore MPEG-2](mpeg-2-splitter.md) .
-   La modalità push è disponibile in tutte le piattaforme, sia per i flussi di programma che per i flussi di trasporto.

Il demux supporta pertanto tre modalità possibili: i flussi di programma in modalità pull, i flussi di programma in modalità push e i flussi di trasporto in modalità push. Il demux determina la modalità da usare in fase di esecuzione. La modalità viene determinata quando il pin di input si connette o quando viene configurato il primo pin di output, a seconda di quale evento si verifica per primo:

-   Quando il pin di input si connette: in Windows XP e versioni successive, demux esegue una query sul filtro upstream per l'interfaccia [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) . Se il filtro upstream espone tale interfaccia, demux si configura per i flussi di programma in modalità pull. In caso contrario, demux usa la modalità push e il tipo di supporto determina il tipo di flusso (flusso del programma o flusso di trasporto). Per un elenco di tipi di input, vedere [**tipi di supporti Demultiplexer MPEG-2**](mpeg-2-demultiplexer-media-types.md) .
-   Quando viene configurato il primo pin di output: se si crea un pin di output e lo si esegue una query per [**IMPEG2PIDMap**](/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-impeg2pidmap), demux si configura per i flussi di trasporto in modalità push. Se si esegue una query sul pin per [**IMPEG2StreamIdMap**](/windows/desktop/api/Strmif/nn-strmif-impeg2streamidmap), demux si configura per i flussi di programma, anche in modalità push. Tutte le query successive per l'altra interfaccia hanno esito negativo, perché demux non può funzionare contemporaneamente in due modalità.

Una volta che il demux è stato configurato per una particolare modalità, rimane in tale modalità. Per utilizzare una modalità diversa, è necessario creare una nuova istanza di demux.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso del Demultiplexer MPEG-2](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 



