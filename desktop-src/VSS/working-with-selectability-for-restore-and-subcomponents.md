---
description: La selezione per il ripristino consente al richiedente di determinare quando un componente può essere ripristinato singolarmente.
ms.assetid: 684dc50f-5d7b-4c95-85dd-77c320d65fff
title: Utilizzo della selezione per il ripristino e i sottocomponenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d988f4c4e029c7dd8623ad22fcaee7662d33e82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526262"
---
# <a name="working-with-selectability-for-restore-and-subcomponents"></a>Utilizzo della selezione per il ripristino e i sottocomponenti

La selezione per il ripristino consente al richiedente di determinare quando un componente può essere ripristinato singolarmente. Un componente incluso per il backup può essere visualizzato in uno dei due modi seguenti:

-   È possibile che un componente sia stato [*incluso in modo esplicito*](vssgloss-e.md) nel backup. Questi componenti hanno un'istanza di [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) corrispondente nel documento componenti di backup. Questi componenti sono inclusi in un ripristino con [**IVssBackupComponents:: SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore).
-   È possibile che un componente sia stato [*incluso in modo implicito*](vssgloss-i.md) nel backup. Questi componenti non hanno un'istanza di [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) corrispondente nel documento dei componenti di backup; Tuttavia, nel documento sarà sempre presente un'istanza di **IVssComponent** per un componente predecessore. Questi componenti sono inclusi in un ripristino con [**IVssBackupComponents:: AddRestoreSubcomponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent).

Tutti i componenti inclusi in modo esplicito nel backup possono essere sempre selezionati singolarmente per il ripristino, indipendentemente dal valore di selezione per il ripristino. Il richiedente chiama [**IVssBackupComponents:: SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore), passando l'ID del writer, il percorso logico e il nome del componente specifico. I componenti che sono stati inclusi in modo implicito nel backup verranno ripristinati quando viene ripristinato un predecessore incluso in modo esplicito. I componenti inclusi in modo implicito possono essere selezionati singolarmente per il ripristino solo se sono contrassegnati come selezionabili per il ripristino. Il richiedente chiama prima **IVssBackupComponents:: SetSelectedForRestore** sul componente predecessore incluso in modo esplicito più vicino, quindi chiama [**IVssBackupComponents:: AddRestoreSubcomponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent) sul componente predecessore per selezionare il componente incluso in modo implicito per il ripristino. Al termine, verrà ripristinato solo il componente selezionato in modo implicito; tutti gli altri componenti del set di componenti non verranno ripristinati.

A differenza della selezione per il backup, che deve sempre essere impostata in modo esplicito quando un componente viene aggiunto con [**IVssCreateWriterMetadata:: AddComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponent), la selezione per il ripristino ha un valore predefinito false, che può essere sottoposto a override.

Poiché i componenti di primo livello, ovvero i componenti con un percorso logico vuoto, possono essere inclusi in modo esplicito solo in un backup, la selezione per il ripristino non ha alcun significato per questi componenti.

 

 



