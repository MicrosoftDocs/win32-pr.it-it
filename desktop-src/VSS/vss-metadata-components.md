---
description: Fondamentale per organizzare i file di cui eseguire il backup o il ripristino del writer è il concetto di componente.
ms.assetid: 5f85bd0e-31bb-45aa-af7c-15299ed31b26
title: Componenti dei metadati di VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac121ae62798d0318233dba48e6d0b56c36e2065a71fe8e12af9c963893dd027
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117751434"
---
# <a name="vss-metadata-components"></a>Componenti dei metadati di VSS

Fondamentale per organizzare i file di cui eseguire il backup o il ripristino del writer è il concetto di [*componente*](vssgloss-c.md).

I componenti consentono a un writer di indicare a un motore di backup come devono essere organizzati i file, le dipendenze tra i file e il tipo di dati che tali file possono contenere. Ciò consente a un motore di backup di decidere come archiviare i file per ottenere la massima efficienza.

Inoltre, le applicazioni basate su VSS usano i componenti come blocchi predefiniti per i metadati e il supporto per la comunicazione tra writer e richiedenti.

I writer e i richiedenti archiviano le informazioni sui componenti separatamente, rispettivamente nel documento dei metadati del writer e nel documento dei componenti di backup, e le informazioni differiscono in ogni rappresentazione.

Le informazioni sui componenti nei documenti dei metadati del writer includono quanto segue:

-   Informazioni di un solo writer in ogni documento
-   Tutti i componenti del writer, che [](vssgloss-e.md) possono essere inclusi in modo esplicito o devono essere [*inclusi in modo implicito*](vssgloss-i.md) in un'operazione di backup o ripristino
-   [*Informazioni sul percorso*](vssgloss-l.md) logico usate per associare un componente selezionabile per il backup a particolari componenti non selezionabili per il backup, formando così un set di componenti
-   Informazioni [*sul set*](vssgloss-f.md) di file, ovvero percorso, specifica del file e flag di ricorsione, gestite per ogni componente

I documenti dei metadati del writer contengono anche informazioni sui metadati a livello di writer, ad esempio metodi di ripristino e mapping di percorsi alternativi per il ripristino. I documenti dei metadati del writer sono di sola lettura. L'interfaccia per esaminare queste informazioni è [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent).

Le informazioni sui componenti nei documenti dei componenti di backup includono quanto segue:

-   Solo informazioni sui componenti inclusi in modo esplicito
-   Informazioni sui metadati a livello di writer, ad esempio mapping di percorsi alternativi e ripristino
-   Informazioni sullo stato che descrivono un'operazione di backup o ripristino

I documenti dei componenti di backup non contengono informazioni sui set [*di file dei componenti.*](vssgloss-f.md) I documenti dei componenti di backup non sono di sola lettura e possono essere modificati dal writer. L'interfaccia per accedere a queste informazioni è [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent).

Il ciclo di vita e la relazione tra le due espressioni di un componente possono essere compresi come segue:

-   I writer sono responsabili delle definizioni iniziali dei componenti.
-   Un richiedente esamina i metadati di tutti i writer e dei relativi componenti.
-   Dalle informazioni sulla selezionabilità e sul percorso logico dei componenti, un richiedente determina quali componenti devono essere inclusi in modo esplicito, che possono essere inclusi in modo esplicito, che definiscono i set di componenti e quali sono membri dei set di componenti.
-   Un richiedente aggiunge i componenti che richiedono l'inclusione esplicita e include implicitamente i sottocomponenti [*nei*](/windows) set di componenti (le cui informazioni non sono presenti nel documento Componenti di backup).
-   Durante la gestione degli eventi, writer e richiedenti possono modificare ed esaminare le informazioni sui componenti archiviate nel documento Componenti di backup per coordinarne l'attività.

Per eseguire correttamente le operazioni di backup e ripristino, sia il writer che il componente delle versioni richiedenti devono essere archiviate con tutti i dati di cui è stato eseguito il backup:

-   [Tipi di componenti](component-types.md)
-   [Definizione di componenti di writer](definition-of-components-by-writers.md)
-   [Uso dei componenti da parte del richiedente](use-of-components-by-the-requestor.md)

 

 
