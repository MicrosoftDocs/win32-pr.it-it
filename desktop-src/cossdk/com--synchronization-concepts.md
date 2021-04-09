---
description: In genere, la sincronizzazione non è necessaria quando si ha un Apartment a thread singolo (STA) perché l'Apartment fornisce la sincronizzazione.
ms.assetid: a05de040-0115-44aa-80e2-55eff2ec894d
title: Concetti relativi alla sincronizzazione COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eaca81050e67c76e3de6ad4845543b9230d2a24
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748879"
---
# <a name="com-synchronization-concepts"></a>Concetti relativi alla sincronizzazione COM+

In genere, la sincronizzazione non è necessaria quando si ha un Apartment a thread singolo (STA) perché l'Apartment fornisce la sincronizzazione. La sincronizzazione diventa importante quando si dispone di un Apartment a thread multipli (MTA) e di un oggetto a thread libero. In passato, gli oggetti a thread libero hanno dovuto gestire il blocco. È possibile eliminare la necessità di utilizzare il blocco impostando l'attributo di sincronizzazione per un componente.

La sincronizzazione presenta le proprietà seguenti:

-   Consente a un chiamante di immettere il componente alla volta.
-   Impedisce il flusso attraverso il processo o tra computer.
-   Flussi da componente a componente all'interno di un processo.
-   Consente la rientranza dallo stesso chiamante.

Diversamente dagli Apartment, le attività estendono i contesti di più processi e host. La sincronizzazione determina quale attività conterrà un oggetto. Gli oggetti possono risiedere in una delle attività seguenti:

-   Attività del creatore
-   Nuova attività
-   Nessuna attività

COM+ garantisce la concorrenza in base a una serie di blocchi per ogni attività. Se un chiamante tenta di immettere un componente COM+ Synchronized già utilizzato da un altro chiamante, la chiamata viene bloccata fino a quando il blocco non viene rilasciato. Questo comportamento di blocco non si timeout e non può essere configurato per il timeout. Se il blocco non è in uso, il blocco viene acquisito e la chiamata viene elaborata. Al termine, il blocco viene rilasciato per il chiamante successivo. Per evitare deadlock, COM+ gestisce l'accesso a tutti gli oggetti tra le attività da parte di una serie annidata di chiamate concatenate in tutta la rete.

COM+ fornisce le seguenti impostazioni di sincronizzazione:

-   Disabled
-   Non supportato
-   Supportato
-   Necessario
-   RequiresNew

> [!Note]  
> Alcune impostazioni di sincronizzazione funzionano insieme ad altre impostazioni del componente COM+. La sincronizzazione è ad esempio necessaria se il servizio [di attivazione JIT (just-in-Time) com+](com--just-in-time-activation.md) è abilitato. JIT è obbligatorio se si abilitano le transazioni. Pertanto, l' [elaborazione delle transazioni](com--transactions.md) com+ richiede anche la sincronizzazione. Pertanto, le classi con l'impostazione JIT = true devono avere anche l'impostazione Synchronization = Required o Synchronization = RequiresNew.

 

Per istruzioni sull'impostazione delle opzioni di sincronizzazione tramite lo strumento di amministrazione Servizi componenti, vedere [impostazione dell'attributo di sincronizzazione](setting-the-synchronization-attribute.md).

Per ulteriori informazioni sull'utilizzo della libreria di amministrazione COM+ per impostare le opzioni di sincronizzazione, vedere [automazione di com+ Administration](automating-com--administration.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attività di sincronizzazione COM+](com--synchronization-tasks.md)
</dt> </dl>

 

 



