---
description: In generale, la modalità di creazione di una copia shadow dipende dal tipo di copia shadow da creare, dal relativo contesto e dal ruolo concesso ai writer nell'operazione di copia shadow.
ms.assetid: eab3b39b-dfa7-43ea-adba-cd0b495c373f
title: Dettagli di creazione della copia shadow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b8d8f506ef8d5c7acff86cb6a2fa890b3773423fddf339ea4911a0299963224
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998131"
---
# <a name="shadow-copy-creation-details"></a>Dettagli di creazione della copia shadow

In generale, la modalità di creazione di una copia shadow dipende dal tipo di copia shadow da creare, dal relativo contesto e dal ruolo concesso ai writer nell'operazione di copia shadow. Per altre [informazioni, vedere Configurazioni](shadow-copy-context-configurations.md) del contesto della copia shadow.

Il contesto della copia shadow viene impostato chiamando il [**metodo IVssBackupComponents::SetContext.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext) Prima di chiamare il metodo [**IVssBackupComponents::D oSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) per creare una copia shadow, i richiedenti devono chiamare i metodi [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) nell'ordine specificato nelle sezioni seguenti.

## <a name="prerequisites-for-all-shadow-copies"></a>Prerequisiti per tutte le copie shadow

Indipendentemente dal livello di partecipazione del writer, la creazione di qualsiasi copia shadow richiederà sempre l'inizializzazione del richiedente con chiamate a [**IVssBackupComponents::InitializeForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforbackup) e [**IVssBackupComponents::StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset).

Se questa chiamata non viene effettuata, il [**metodo IVssBackupComponents::D oSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) restituirà un errore.

## <a name="shadow-copies-with-writer-participation"></a>Copie shadow con partecipazione al writer

Se il contesto della copia shadow specifica la partecipazione al writer( ovvero, [**IVssBackupComponents::SetContext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext) viene chiamato con **VSS \_ CTX \_ BACKUP** o **VSS \_ CTX \_ APP \_ ROLLBACK):**

-   I richiedenti devono sempre chiamare [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) quando il contesto della copia shadow supporta la partecipazione al writer. Se il contesto della copia shadow supporta la partecipazione al writer e **IVssBackupComponents::GatherWriterMetadata** non viene chiamato prima di [**IVssBackupComponents::D oSnapshotSet,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)verrà restituito un errore.
-   Se un richiedente vuole selezionare componenti writer specifici, deve chiamare [**IVssBackupComponents::AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) prima di [**chiamare StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) per creare il set di copie shadow.
-   [**È necessario chiamare StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) per creare il set di copie shadow.
-   I richiedenti possono aggiungere uno o più volumi al set di copie shadow chiamando [**AddToSnapshotSet.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset) Alcuni componenti del writer potrebbero non specificare volumi interessati. In questo caso, è accettabile che un set di snapshot sia vuoto, ovvero non contenga volumi.
-   Per garantire la coerenza dei metadati del writer, un richiedente deve sempre chiamare [**IVssBackupComponents::P repareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) anche se non è selezionato alcun componente. In questo modo VSS genera un evento **PrepareForBackup,** in cui VSS chiama il metodo [**CVssWriter::OnPrepareBackup**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpreparebackup) per ogni writer partecipante.
-   VsS genererà gli [*eventi PrepareForSnapshot*](vssgloss-p.md) e [*Freeze*](vssgloss-f.md) prima di creare la copia shadow in risposta a [**IVssBackupComponents::D oSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset). I writer gestiranno gli eventi [**con CVssWriter::OnPrepareSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpreparesnapshot) e [**CVssWriter::OnFreeze**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onfreeze).
-   VsS genererà eventi [*Thaw*](vssgloss-t.md) ed eventi [*PostSnapshot*](vssgloss-p.md) dopo la creazione di una copia shadow in risposta a [**IVssBackupComponents::D oSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset). I writer gestiranno gli eventi con [**CVssWriter::OnThaw**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onthaw) e [**CVssWriter::OnPostSnapshot.**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot)

## <a name="shadow-copies-without-writer-participation"></a>Copie shadow senza partecipazione al writer

La creazione di copie shadow senza partecipazione al writer è sconsigliata per le applicazioni di backup standard (vedere [Backup senza partecipazione al writer).](backups-without-writer-participation.md)

Esistono usi, ad esempio backup rapidi di un disco per fornire una rete di sicurezza contro il danneggiamento accidentale dei file, che può essere eseguito senza partecipazione esplicita al writer. Una copia shadow di questo tipo avrebbe un contesto di BACKUP CONDIVISIONE **FILE VSS \_ CTX o \_ \_ \_ ROLLBACK** **NAS \_ VSS CTX \_ \_**.

Per questo tipo di copia shadow, tenere presente quanto segue:

-   I richiedenti devono comunque chiamare i metodi necessari elencati in [Prerequisiti per tutte le copie shadow.](#prerequisites-for-all-shadow-copies)
-   I richiedenti possono [**chiamare IVssBackupComponents::GatherWriterMetadata,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)ma questa operazione non è necessaria.
-   Se i richiedenti chiamano [**IVssBackupComponents::AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent), [**IVssBackupComponents::P repareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup)o [**IVssBackupComponents::BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete), verrà restituito un errore.
-   I provider non genereranno eventi [*PrepareForSnapshot*](vssgloss-p.md), [*Freeze*](vssgloss-f.md), [*Thaw*](vssgloss-t.md)o [*PostSnapshot*](vssgloss-p.md) per questo tipo di copia shadow.

 

 



