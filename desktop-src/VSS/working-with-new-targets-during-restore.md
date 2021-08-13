---
description: Un richiedente potrebbe dover ripristinare i file in un percorso indicato da un percorso diverso dal percorso predefinito di un set di file o dal relativo mapping del percorso alternativo.
ms.assetid: ce11485c-da0e-4c16-962e-eeedc2da3de4
title: Uso di nuove destinazioni durante il ripristino
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9f7b9a614b043a423dd90868b0a66b505ee194ef968daed4952b0ba60fec6b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118590465"
---
# <a name="working-with-new-targets-during-restore"></a>Uso di nuove destinazioni durante il ripristino

Un richiedente potrebbe dover ripristinare i file in un percorso indicato da un percorso diverso dal percorso predefinito di un set di file o dal [*mapping del percorso alternativo.*](vssgloss-a.md) Questo problema può verificarsi per diversi motivi: ad esempio, nessuna destinazione di ripristino era accessibile o un utente richiedente richiede intenzionalmente che i file siano ripristinati in una posizione precedentemente sconosciuta. In questo caso, il richiedente usa il nuovo meccanismo di destinazione per indicare ai writer che è stato ripristinato un file in un'area diversa sul disco.

Non tutti i writer supportano un richiedente che modifica la destinazione di ripristino di un file. Un richiedente deve verificare il supporto del writer controllando la maschera dello schema di backup del writer (restituita da [**IVssExamineWriterMetadata::GetBackupSchema)**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema)e verificando che contenga il \_ flag VSS BS \_ WRITER \_ SUPPORTS NEW \_ \_ TARGET.

Il richiedente indica un ripristino di questo tipo tramite [**il metodo IVssBackupComponents::AddNewTarget.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget) Oltre a specificare una specifica di file e una destinazione di ripristino originale e nuova, il richiedente specifica le informazioni sui componenti, ovvero un percorso logico e un nome di componente.

Le informazioni sul componente usato dipendono dal fatto che il componente che [](vssgloss-e.md) gestisce il file con una nuova destinazione aggiunta sia stato incluso in modo esplicito o [*implicito*](vssgloss-i.md) nel backup.

Se il componente di gestione è stato incluso in modo esplicito, vengono usate le relative informazioni. Se il componente di gestione è stato incluso in modo implicito, è un sottocomponente in un set di componenti. In questo caso, vengono usate le informazioni del componente di definizione del set di componenti.

Durante la gestione [**dell'evento PostRestore,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore) i writer devono verificare se uno dei file è stato ripristinato in una nuova posizione. Questa operazione può essere eseguita usando [**i metodi IVssComponent::GetNewTargetCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtargetcount) e [**IVssComponent::GetNewTarget.**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtarget)

L'istanza [**dell'interfaccia IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) usata dipende dal fatto che il componente di gestione del file sia stato aggiunto in modo esplicito o implicito al backup.

 

 



