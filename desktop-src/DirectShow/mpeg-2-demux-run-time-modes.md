---
description: MpEG-2 Modalità Run-Time demux
ms.assetid: b0d0c725-9220-43a5-af1c-d3c5c72e1ef3
title: MpEG-2 Modalità Run-Time demux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0bffe5f58a18ae9e935985e8dae8dc340c3895bd2dc1a2a89965355832e701f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072965"
---
# <a name="mpeg-2-demux-run-time-modes"></a>MpEG-2 Modalità Run-Time demux

Il [demultiplexer MPEG-2](mpeg-2-demultiplexer.md) ("demux") può operare in modalità push o pull. In modalità push i dati provengono da un'origine live, ad esempio una trasmissione di rete. In modalità pull, i dati provengono da un file locale.

-   La modalità pull è disponibile in Windows XP e versioni successive, solo per i flussi di programma. Nelle piattaforme di livello inferiore usare il filtro [mpeg-2 splitter.](mpeg-2-splitter.md)
-   La modalità push è disponibile in tutte le piattaforme, sia per i flussi di programma che per i flussi di trasporto.

Il demux supporta quindi tre modalità possibili: flussi di programma in modalità pull, flussi di programma in modalità push e flussi di trasporto in modalità push. Il demux determina la modalità da usare in fase di esecuzione. La modalità viene determinata quando si connette il pin di input o quando viene configurato il primo pin di output, a seconda dell'evento che si verifica per primo:

-   Quando il pin di input si connette: Windows XP e versioni successive, il demux esegue una query sul filtro upstream per [**l'interfaccia IAsyncReader;**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) Se il filtro upstream espone tale interfaccia, il demux si configura per i flussi del programma in modalità pull. In caso contrario, il demux usa la modalità push e il tipo di supporto determina il tipo di flusso (flusso del programma o flusso di trasporto). Per un elenco dei tipi di input, vedere [**MpEG-2 Demultiplexer Media Types (Tipi di supporti demultiplexer MPEG-2).**](mpeg-2-demultiplexer-media-types.md)
-   Quando viene configurato il primo pin di output: se si crea un pin di output ed esegue una query per [**IMPEG2PIDMap,**](/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-impeg2pidmap)il demux si configura per i flussi di trasporto in modalità push. Se si esegue una query sul pin per [**IMPEG2StreamIdMap**](/windows/desktop/api/Strmif/nn-strmif-impeg2streamidmap), il demux si configura per i flussi del programma, anche in modalità push. Le query successive per l'altra interfaccia hanno esito negativo, perché il demux non può operare in due modalità contemporaneamente.

Dopo che il demux si è configurato per una particolare modalità, rimane in tale modalità. Per usare una modalità diversa, è necessario creare una nuova istanza del demux.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso del demultiplexer MPEG-2](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 



