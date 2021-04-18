---
description: In generale, la modalità di creazione di una copia shadow dipende dal tipo di copia shadow da creare, dal relativo contesto e dal ruolo associato ai writer nell'operazione di copia shadow.
ms.assetid: eab3b39b-dfa7-43ea-adba-cd0b495c373f
title: Dettagli creazione copia shadow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b9281b899593ca0751f1d549aed60305041b18c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310664"
---
# <a name="shadow-copy-creation-details"></a>Dettagli creazione copia shadow

In generale, la modalità di creazione di una copia shadow dipende dal tipo di copia shadow da creare, dal relativo contesto e dal ruolo associato ai writer nell'operazione di copia shadow. Per ulteriori informazioni, vedere [configurazioni del contesto per copie shadow](shadow-copy-context-configurations.md) .

Il contesto della copia shadow viene impostato chiamando il metodo [**IVssBackupComponents:: secontext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext) . Prima di chiamare il metodo [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) per creare una copia shadow, i richiedenti devono chiamare i metodi [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) nell'ordine specificato nelle sezioni riportate di seguito.

## <a name="prerequisites-for-all-shadow-copies"></a>Prerequisiti per tutte le copie shadow

Indipendentemente dal livello di partecipazione del writer, per la creazione di qualsiasi copia shadow sarà sempre necessario inizializzare il richiedente con le chiamate a [**IVssBackupComponents:: InitializeForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforbackup) e [**IVssBackupComponents:: StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset).

Se questa chiamata non viene eseguita, il metodo [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) restituirà un errore.

## <a name="shadow-copies-with-writer-participation"></a>Copie shadow con partecipazione del writer

Se il contesto della copia shadow specifica la partecipazione del writer (ovvero, [**IVssBackupComponents:: secontext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext) viene chiamato con il **\_ \_ backup VSS CTX** o il **rollback dell' \_ \_ app \_ VSS CTX**):

-   I richiedenti devono chiamare sempre [**IVssBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) quando il contesto della copia shadow supporta la partecipazione del writer. Se il contesto della copia shadow supporta la partecipazione del writer e **IVssBackupComponents:: GatherWriterMetadata** non viene chiamato prima di [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset), viene restituito un errore.
-   Se un richiedente desidera selezionare componenti writer specifici, deve chiamare [**IVssBackupComponents:: AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) prima di chiamare [**StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) per creare il set di copie shadow.
-   È necessario chiamare [**StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) per creare il set di copie shadow.
-   I richiedenti possono aggiungere uno o più volumi al set di copie shadow chiamando [**AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset). Alcuni componenti del writer non possono specificare alcun volume interessato. In questo caso è accettabile che un set di snapshot sia vuoto, ovvero che non contenga volumi.
-   Per garantire la coerenza dei metadati del writer, è necessario che un richiedente chiami sempre [**IVssBackupComponents::P repareforbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) anche se non è selezionato alcun componente. In questo modo VSS genera un evento **PrepareForBackup** , in cui VSS chiama il metodo [**CVssWriter:: OnPrepareBackup**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpreparebackup) per ogni writer partecipante.
-   VSS genera [*PrepareForSnapshot*](vssgloss-p.md) e [*blocca*](vssgloss-f.md) gli eventi prima di creare la copia shadow in risposta a [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset). I writer gestiranno gli eventi con [**CVssWriter:: OnPrepareSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpreparesnapshot) e [**CVssWriter:: OnFreeze**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onfreeze).
-   VSS genera eventi di [*sblocco*](vssgloss-t.md) e post- [*snapshot*](vssgloss-p.md) dopo la creazione di una copia shadow in risposta a [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset). I writer gestiranno gli eventi con [**CVssWriter:: Onscongelate**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onthaw) e [**CVssWriter:: OnPostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot).

## <a name="shadow-copies-without-writer-participation"></a>Copie shadow senza partecipazione del writer

La creazione di copie shadow senza partecipazione del writer è sconsigliata per le applicazioni di backup standard. vedere [backup senza partecipazione al writer](backups-without-writer-participation.md).

Sono disponibili usi, ad esempio backup veloci di un disco per fornire una rete di protezione contro il danneggiamento accidentale dei file, che può essere eseguito senza una partecipazione esplicita del writer. Una copia shadow di questo tipo avrà un contesto di **\_ backup della \_ \_ condivisione file \_ VSS CTX** o del **\_ \_ \_ rollback del Server VSS CTX**.

Per questo tipo di copia shadow, tenere presente quanto segue:

-   I richiedenti devono comunque chiamare i metodi richiesti elencati in [prerequisiti per tutte le copie shadow](#prerequisites-for-all-shadow-copies).
-   I richiedenti possono chiamare [**IVssBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata), ma questa operazione non è obbligatoria.
-   Se i richiedenti chiamano [**IVssBackupComponents:: AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent), [**IVssBackupComponents::P repareforbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup)o [**IVssBackupComponents:: BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete), verrà restituito un errore.
-   I provider non genereranno eventi [*PrepareForSnapshot*](vssgloss-p.md), [*Freeze*](vssgloss-f.md), [*scongelate*](vssgloss-t.md)o [*PostSnapshot*](vssgloss-p.md) per questo tipo di copia shadow.

 

 



