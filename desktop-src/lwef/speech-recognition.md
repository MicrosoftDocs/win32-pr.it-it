---
title: Riconoscimento vocale
description: Riconoscimento vocale
ms.assetid: cb5ac509-12a4-4ca4-8776-424568cf780d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dd36ea5754d53ceda2761635ecb838fdfb0328617827ca90fc969af915b4ea6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119960851"
---
# <a name="speech-recognition"></a>Riconoscimento vocale

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Il riconoscimento vocale offre un'interfaccia molto naturale e familiare per l'interazione con i caratteri. Tuttavia, l'input vocale presenta anche molte sfide. I motori vocali attualmente operano senza parti sostanziali del linguaggio di comunicazione vocale umano, ad esempio movimenti, intonazione ed espressioni facciali. Inoltre, la sintesi vocale naturale è in genere illimitata. È facile che il parlante superi il vocabolario corrente, o *grammatica,* del motore. Analogamente, la formulazione o l'ordine delle parole può variare per qualsiasi richiesta o risposta specificata. Inoltre, i motori di riconoscimento vocale devono spesso gestire grandi variazioni nell'ambiente del parlante. Ad esempio, il rumore di fondo, la qualità del microfono e la posizione possono influire sulla qualità dell'input. Analogamente, diverse pronunce del parlante o anche variazioni dello stesso parlante, ad esempio quando il parlante ha un freddo, rendono difficile convertire i dati acustici in comprensione rappresentativa. Infine, i motori di riconoscimento vocale devono anche gestire parole o frasi simili in una lingua, ad esempio "nuovo", "noto" e "gnu" o "distruggere una buona marea" e "riconoscere il parlato".

Il riconoscimento vocale non è sempre la forma migliore di input per un'attività. A causa della natura del riconoscimento vocale, spesso può essere più lento rispetto ad altre forme di input. Come la tastiera, l'input vocale è un'interfaccia scadente per il puntamento, a meno che non venga fornito un tipo di rappresentazione mnemoica. Pertanto, valutare sempre se la voce è l'input più appropriato per un'attività. È meglio evitare di usare il parlato come interfaccia esclusiva per qualsiasi attività. Fornire altri modi per accedere a qualsiasi funzionalità di base usando metodi come il mouse o la tastiera. Inoltre, sfruttare la natura multimodale dell'uso della voce nell'interfaccia visiva combinando l'input vocale con le informazioni visive che consentono di specificare il contesto e le opzioni.

Infine, l'uso corretto dell'input vocale è dovuto solo in parte alla qualità della tecnologia. Anche il riconoscimento umano, che supera qualsiasi tecnologia di riconoscimento corrente, talvolta non riesce. Tuttavia, nella comunicazione umana vengono usate strategie che migliorano la probabilità di successo e forniscono il ripristino degli errori in caso di problemi. Di conseguenza, l'efficacia dell'input vocale dipende anche dalla qualità dell'interfaccia utente che lo presenta.

Lo studio dei modelli umani di interazione vocale può essere utile quando si progettano interfacce vocali più naturali. La registrazione dei dialoghi vocali umani effettivi per scenari specifici può aiutare a comprendere meglio i costrutti e i modelli usati, nonché le forme efficaci di feedback e ripristino degli errori. Può essere utile per determinare il vocabolario appropriato da usare (per input e output). È meglio progettare un'interfaccia vocale in base al modo in cui le persone parlano piuttosto che derivarla semplicemente dall'interfaccia grafica in cui opera.

Si noti che Microsoft Agent usa Microsoft Speech API (SAPI) per supportare il riconoscimento vocale. In questo modo Microsoft Agent può essere usato con un'ampia gamma di motori compatibili. Anche se Microsoft Agent specifica determinate interfacce di base, i requisiti di prestazioni e la qualità di un motore possono variare.

Il riconoscimento vocale non è l'unico mezzo per supportare le interfacce di conversazione. È anche possibile usare l'elaborazione in linguaggio naturale dell'input da tastiera al posto di o in aggiunta alla voce. In queste situazioni, è comunque possibile applicare in genere linee guida per l'input vocale.

-   [Ascolto, non solo riconoscimento](listen--dont-just-recognize.md)
-   [Chiarire e limitare le scelte](clarify-and-limit-choices.md)
-   [Fornire un buon ripristino degli errori](provide-good-error-recovery.md)

 

 




