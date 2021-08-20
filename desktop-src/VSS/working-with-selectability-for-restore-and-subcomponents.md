---
description: La selezionabilità per il ripristino consente al richiedente di determinare quando un componente può essere ripristinato singolarmente.
ms.assetid: 684dc50f-5d7b-4c95-85dd-77c320d65fff
title: Uso della selezionabilità per il ripristino e i sottocomponenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1186c9517af8e7e7b914b9508e10a2b4c8d1961afdbf6d68c2dadcede58c4c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117937382"
---
# <a name="working-with-selectability-for-restore-and-subcomponents"></a>Uso della selezionabilità per il ripristino e i sottocomponenti

La selezionabilità per il ripristino consente al richiedente di determinare quando un componente può essere ripristinato singolarmente. Un componente incluso per il backup può essere visualizzato in uno dei due modi seguenti:

-   È possibile che un componente sia stato [*incluso*](vssgloss-e.md) in modo esplicito nel backup. Questi componenti hanno [**un'istanza di IVssComponent corrispondente**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) nel documento Backup Components ( Componenti di backup). Questi componenti sono inclusi in un ripristino [**tramite IVssBackupComponents::SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore).
-   È possibile che un componente sia stato incluso in [*modo implicito*](vssgloss-i.md) nel backup. Questi componenti non hanno un'istanza [**di IVssComponent corrispondente**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) nel documento backup components; Tuttavia, nel documento sarà sempre presente **un'istanza di IVssComponent** per un componente predecessore. Questi componenti sono inclusi in un ripristino [**tramite IVssBackupComponents::AddRestoreSubcomponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent).

Qualsiasi componente incluso in modo esplicito nel backup può sempre essere selezionato singolarmente per il ripristino, indipendentemente dal relativo valore di selezionabilità per ripristino. Il richiedente chiama [**IVssBackupComponents::SetSelectedForRestore,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore)passando l'ID writer, il percorso logico e il nome del componente specifico. I componenti inclusi in modo implicito nel backup verranno ripristinati quando viene ripristinato un predecessore incluso in modo esplicito. I componenti inclusi in modo implicito possono essere selezionati singolarmente per il ripristino solo se sono contrassegnati come selezionabili per il ripristino. Il richiedente chiama **prima IVssBackupComponents::SetSelectedForRestore** sul componente predecessore incluso in modo esplicito più vicino e quindi chiama [**IVssBackupComponents::AddRestoreSubcomponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent) sul componente predecessore per selezionare il componente incluso in modo implicito per il ripristino. Al termine, verrà ripristinato solo il componente selezionato in modo implicito. Tutti gli altri componenti nel set di componenti non verranno ripristinati.

A differenza della selezionabilità per il backup, che deve essere sempre impostata in modo esplicito quando un componente viene aggiunto con [**IVssCreateWriterMetadata::AddComponent,**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponent)la selezionabilità per il ripristino ha un valore predefinito false, che può essere sostituito.

Poiché i componenti di primo livello (componenti con un percorso logico vuoto) possono essere inclusi in modo esplicito solo in un backup, la selezionabilità per il ripristino non ha alcun significato per questi componenti.

 

 



