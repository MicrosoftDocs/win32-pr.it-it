---
description: In genere, la sincronizzazione non è necessaria quando si dispone di un apartment a thread singolo (STA), perché l'apartment fornisce la sincronizzazione automaticamente.
ms.assetid: a05de040-0115-44aa-80e2-55eff2ec894d
title: Concetti relativi alla sincronizzazione COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4153c02a5fcd9a0990459e360d239396e7de30cff22316da70f73002e73d6e0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129003"
---
# <a name="com-synchronization-concepts"></a>Concetti relativi alla sincronizzazione COM+

In genere, la sincronizzazione non è necessaria quando si dispone di un apartment a thread singolo (STA), perché l'apartment fornisce la sincronizzazione automaticamente. La sincronizzazione diventa importante quando si dispone di un apartment multithreading (MTA) e di un oggetto a thread libero. In passato, gli oggetti a thread libero dovevano gestire il blocco. È possibile eliminare la necessità di usare il blocco impostando l'attributo di sincronizzazione per un componente.

La sincronizzazione ha le proprietà seguenti:

-   Consente a un chiamante di immettere il componente alla volta.
-   Impedisce il flusso tra processi o tra computer.
-   Scorre da un componente a un componente all'interno di un processo.
-   Consente la reentrancy dallo stesso chiamante.

A differenza degli apartment, le attività si estendono su contesti di più processi e host. La sincronizzazione determina quale attività conterrà un oggetto . Gli oggetti possono risiedere in una delle attività seguenti:

-   Attività del creatore
-   Nuova attività
-   Nessuna attività

COM+ garantisce la concorrenza tramite una serie di blocchi per ogni attività. Se un chiamante tenta di immettere un componente sincronizzato COM+ già usato da un altro chiamante, la chiamata viene bloccata fino al rilascio del blocco. Questo comportamento di blocco non si verifica e non può essere configurato per il timeout. Se il blocco non è in uso, il blocco viene acquisito e la chiamata viene elaborata. Al termine, il blocco viene rilasciato per il chiamante successivo. Per evitare un deadlock, COM+ gestisce l'accesso a tutti gli oggetti tra le attività tramite una serie annidata di chiamate concatenate in tutta la rete.

COM+ fornisce le impostazioni di sincronizzazione seguenti:

-   Disabled
-   Non supportato
-   Supportato
-   Necessario
-   RequiresNew

> [!Note]  
> Alcune impostazioni di sincronizzazione funzionano in combinazione con altre impostazioni del componente COM+. Ad esempio, la sincronizzazione è necessaria se è abilitato il servizio di attivazione [JIT COM+.](com--just-in-time-activation.md) JIT è obbligatorio se si abilitano le transazioni. Di conseguenza, anche l'elaborazione [delle transazioni](com--transactions.md) COM+ richiede la sincronizzazione. Pertanto, anche le classi con l'impostazione JIT=True devono avere l'impostazione Synchronization=Required o Synchronization=RequiresNew.

 

Per istruzioni sull'impostazione delle opzioni di sincronizzazione tramite lo strumento amministrativo Servizi componenti, vedere [Impostazione dell'attributo di sincronizzazione](setting-the-synchronization-attribute.md).

Per altre informazioni sull'uso della libreria di amministrazione COM+ per impostare le opzioni di sincronizzazione, vedere [Automazione dell'amministrazione COM+.](automating-com--administration.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attività di sincronizzazione COM+](com--synchronization-tasks.md)
</dt> </dl>

 

 



