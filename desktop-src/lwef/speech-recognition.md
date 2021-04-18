---
title: Riconoscimento vocale
description: Riconoscimento vocale
ms.assetid: cb5ac509-12a4-4ca4-8776-424568cf780d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d5c037ced96c386a5e0baf18eeba258422e0193
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298956"
---
# <a name="speech-recognition"></a>Riconoscimento vocale

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Il riconoscimento vocale fornisce un'interfaccia molto naturale e familiare per interagire con i caratteri. Tuttavia, l'input vocale presenta anche molti problemi. I motori di riconoscimento vocale attualmente funzionano senza parti sostanziali del repertorio di comunicazione vocale umana, ad esempio movimenti, intonazione ed espressioni facciali. Inoltre, la sintesi vocale naturale è in genere non vincolata. È facile per il relatore superare il vocabolario o la *grammatica* corrente del motore. Analogamente, l'ordine di parole o parole può variare in base a qualsiasi richiesta o risposta. Inoltre, i motori di riconoscimento vocale devono spesso occuparsi di grandi variazioni nell'ambiente del relatore. Ad esempio, i rumori di fondo, la qualità del microfono e la posizione possono influenzare la qualità dell'input. Analogamente, le pronunce del relatore diverse o anche le varianti dello stesso altoparlante, ad esempio quando il relatore è a freddo, rendono difficile la conversione dei dati acustici in informazioni di presentazione. Infine, i motori di riconoscimento vocale devono gestire anche parole o frasi simili in un linguaggio, ad esempio "nuovo", "conoscente" e "GNU" o "relitto di una spiaggia interessante" e "riconoscimento vocale".

Il riconoscimento vocale non è sempre il tipo di input migliore per un'attività. A causa della natura del riconoscimento vocale, spesso può essere più lenta rispetto ad altre forme di input. Analogamente alla tastiera, l'input vocale è un'interfaccia insufficiente per puntare, a meno che non venga fornito un tipo di rappresentazione mnemonico. Pertanto, valutare sempre se la voce è l'input più appropriato per un'attività. È consigliabile evitare di usare il riconoscimento vocale come interfaccia esclusiva per qualsiasi attività. Fornire altri modi per accedere a qualsiasi funzionalità di base utilizzando metodi quali il mouse o la tastiera. Inoltre, è possibile sfruttare la natura multimodale dell'uso del riconoscimento vocale nell'interfaccia visiva combinando l'input vocale con informazioni visive che consentono di specificare il contesto e le opzioni.

Infine, il corretto utilizzo dell'input vocale è dovuto solo in parte alla qualità della tecnologia. Anche il riconoscimento umano, che supera qualsiasi tecnologia di riconoscimento corrente, a volte non riesce. Tuttavia, nella comunicazione umana vengono usate strategie che migliorano la probabilità di successo e che forniscono il ripristino degli errori quando si verifica un problema. Pertanto, l'efficacia dell'input vocale dipende anche dalla qualità dell'interfaccia utente che la presenta.

Studiare i modelli umani di interazione vocale può essere utile quando si progettano interfacce di sintesi vocale più naturali. La registrazione dei dialoghi vocali umani effettivi per determinati scenari può aiutarti a comprendere meglio i costrutti e i modelli usati, oltre a forme efficaci di feedback e ripristino degli errori. Può aiutare a determinare il vocabolario appropriato da usare (per l'input e l'output). È preferibile progettare un'interfaccia vocale basata sul modo in cui le persone parlano effettivamente di derivarlo semplicemente dall'interfaccia grafica in cui opera.

Si noti che Microsoft Agent USA Microsoft Speech API (SAPI) per supportare il riconoscimento vocale. Questo consente l'uso di Microsoft Agent con diversi motori compatibili. Sebbene l'agente Microsoft specifichi determinate interfacce di base, i requisiti di prestazioni e la qualità di un motore possono variare.

Il riconoscimento vocale non è l'unico mezzo per supportare interfacce di conversazione. È anche possibile usare l'elaborazione in linguaggio naturale dell'input da tastiera al posto di o in aggiunta alla voce. In tali situazioni, è comunque possibile applicare in genere linee guida per l'input vocale.

-   [Ascolta, non solo riconosci](listen--dont-just-recognize.md)
-   [Chiarire e limitare le scelte](clarify-and-limit-choices.md)
-   [Fornire un ripristino corretto degli errori](provide-good-error-recovery.md)

 

 




