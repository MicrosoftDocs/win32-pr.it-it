---
description: Fondamentale per organizzare i file di cui eseguire il backup o il ripristino del writer è il concetto di un componente.
ms.assetid: 5f85bd0e-31bb-45aa-af7c-15299ed31b26
title: Componenti dei metadati VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c913262158d59a69de21a6e0d49e31979c1a0cae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307162"
---
# <a name="vss-metadata-components"></a>Componenti dei metadati VSS

Fondamentale per organizzare i file di cui eseguire il backup o il ripristino del writer è il concetto di un [*componente*](vssgloss-c.md).

I componenti consentono a un writer di indicare a un motore di backup come organizzare i file, le dipendenze tra i file e il tipo di dati che tali file possono contenere. Questo consente a un motore di backup di decidere come archiviare i file per ottenere la massima efficienza.

Inoltre, le applicazioni basate su VSS utilizzano componenti come blocchi predefiniti per i relativi metadati e il supporto per la comunicazione writer/richiedente.

I writer e i richiedenti archiviano le informazioni sui componenti separatamente: nel documento dei metadati del writer e nel documento sui componenti di backup, rispettivamente, e le informazioni sono diverse in ogni rappresentazione.

Le informazioni sui componenti nei documenti di metadati del writer includono quanto segue:

-   Informazioni da un solo Writer in ogni documento
-   Tutti i componenti del writer, che possono essere inclusi in [*modo esplicito*](vssgloss-e.md) o che devono essere inclusi in modo [*implicito*](vssgloss-i.md) in un'operazione di backup o ripristino
-   Informazioni sul [*percorso logico*](vssgloss-l.md) utilizzate per associare un componente selezionabile per il backup con particolare non selezionabile per i componenti di backup, formando così un set di componenti
-   Informazioni sul [*set di file*](vssgloss-f.md) , ovvero percorso, specifica file e flag di ricorsione, gestite per ogni componente

I documenti di metadati del writer contengono anche informazioni sui metadati a livello di writer, ad esempio metodi di ripristino e mapping dei percorsi alternativi per il ripristino. I documenti di metadati del writer sono di sola lettura. L'interfaccia per l'analisi di queste informazioni è [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent).

Le informazioni sul componente nei documenti dei componenti di backup includono quanto segue:

-   Solo informazioni sui componenti inclusi in modo esplicito
-   Informazioni sui metadati a livello di writer, ad esempio mapping di percorsi alternativi e ripristino
-   Informazioni sullo stato che descrivono un'operazione di backup o ripristino

I documenti del componente di backup non contengono informazioni sui [*set di file*](vssgloss-f.md)dei componenti. I documenti dei componenti di backup non sono di sola lettura e possono essere modificati dal writer. L'interfaccia per l'accesso a queste informazioni è [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent).

Il ciclo di vita e la relazione tra le due espressioni di un componente possono essere interpretate nel modo seguente:

-   I writer sono responsabili delle definizioni iniziali dei componenti.
-   Un richiedente esamina i metadati di tutti i writer e i relativi componenti.
-   Dalle informazioni relative a selezione e percorso logico dei componenti, un richiedente determina quali componenti devono essere inclusi in modo esplicito, che possono essere inclusi in modo esplicito, che definiscono i set di componenti e che sono membri dei set di componenti.
-   Un richiedente aggiunge i componenti che richiedono l'inclusione esplicita e include implicitamente sottocomponenti nei [*set di componenti*](/windows) (le cui informazioni non sono presenti nel documento componenti di backup).
-   Quando si gestiscono gli eventi, i writer e i richiedenti possono modificare ed esaminare le informazioni del componente archiviate nel documento componenti di backup per coordinare l'attività.

Per eseguire correttamente le operazioni di backup e ripristino, sono necessarie sia le informazioni sul componente writer che le versioni del richiedente, che devono essere archiviate con tutti i dati di cui è stato eseguito il backup:

-   [Tipi di componenti](component-types.md)
-   [Definizione dei componenti per Writer](definition-of-components-by-writers.md)
-   [Uso dei componenti da parte del richiedente](use-of-components-by-the-requestor.md)

 

 
