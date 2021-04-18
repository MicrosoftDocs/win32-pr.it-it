---
description: Un richiedente potrebbe dover ripristinare i file in una posizione indicata da un percorso predefinito di un set di file o dal mapping del percorso alternativo.
ms.assetid: ce11485c-da0e-4c16-962e-eeedc2da3de4
title: Utilizzo di nuove destinazioni durante il ripristino
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31f20a6e8c27c186648d0f662921160ab5c76988
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307127"
---
# <a name="working-with-new-targets-during-restore"></a>Utilizzo di nuove destinazioni durante il ripristino

Un richiedente potrebbe dover ripristinare i file in una posizione indicata da un percorso predefinito di un set di file o dal [*mapping del percorso alternativo*](vssgloss-a.md). Esistono molti motivi per cui questa situazione potrebbe verificarsi, ad esempio, nessuna destinazione di ripristino è accessibile o un utente richiedente richiede intenzionalmente che i file vengano ripristinati in un percorso precedentemente sconosciuto. In questo caso, il richiedente usa il nuovo meccanismo di destinazione per indicare ai writer che ha ripristinato un file in un'area diversa sul disco.

Non tutti i writer supportano un richiedente che modifica la destinazione di ripristino di un file. Un richiedente deve verificare il supporto del writer controllando la maschera dello schema di backup del writer (restituita da [**IVssExamineWriterMetadata:: GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema)) e verificando che contenga il writer del servizio Copia Shadow del volume che \_ supporta il \_ \_ \_ nuovo \_ flag di destinazione.

Il richiedente indica un ripristino di questo tipo tramite il metodo [**IVssBackupComponents:: AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget) . Oltre a specificare una specifica del file e una destinazione di ripristino originale e una nuova, il richiedente specifica le informazioni sul componente, ovvero un percorso logico e un nome di componente.

Le informazioni sul componente utilizzate variano a seconda che il componente che gestisce il file con una nuova destinazione aggiunta sia incluso in [*modo esplicito*](vssgloss-e.md) o [*implicito*](vssgloss-i.md) nel backup.

Se il componente di gestione è stato incluso in modo esplicito, vengono utilizzate le relative informazioni. Se il componente di gestione è incluso in modo implicito, si tratta di un sottocomponente di un set di componenti. In questo caso vengono usate le informazioni del componente di definizione del set di componenti.

Durante la gestione dell'evento [**PostRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore) , i writer devono verificare se uno dei file è stato ripristinato in una nuova posizione. A tale scopo, è possibile usare i metodi [**IVssComponent:: GetNewTargetCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtargetcount) e [**IVssComponent:: GetNewTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtarget) .

L'istanza dell'interfaccia [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) utilizzata varia a seconda che il componente di gestione del file sia stato aggiunto in modo esplicito o implicito al backup.

 

 



