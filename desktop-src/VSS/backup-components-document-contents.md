---
description: Il documento Componenti di backup viene gestito dalle istanze dell'interfaccia IVssBackupComponents.
ms.assetid: 8c7ebba8-58c4-4733-ba59-802abf902c5e
title: Contenuto del documento componenti di backup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c844f2e9e106817c8201822d000c2f6cb94c0fa272bb5b165d98e4cc48b1c21
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119248341"
---
# <a name="backup-components-document-contents"></a>Contenuto del documento componenti di backup

Il documento Componenti di backup viene gestito dalle istanze [**dell'interfaccia IVssBackupComponents.**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) Questa interfaccia contiene anche numerosi metodi per controllare le operazioni di backup, modificare le copie shadow ed eseguire query sullo stato del sistema. Tuttavia, non tutte le informazioni del documento sono direttamente accessibili tramite questa interfaccia.

Il documento Componenti di backup è costituito da diversi set di dati:

-   Informazioni sui componenti inclusi in modo esplicito in un'operazione di backup o ripristino
-   Rappresentazione del componente archiviato e delle informazioni sul writer
-   Informazioni sullo stato dell'operazione di backup/ripristino

Mentre le informazioni sul componente sono disponibili sia per il richiedente che per il writer, solo il writer può accedere alle informazioni sullo stato.

## <a name="component-inclusion-information"></a>Informazioni sull'inclusione di componenti

Il documento Componenti di backup contiene un elenco di tali componenti inclusi in modo esplicito nel backup e nel ripristino da parte del richiedente. L'elenco contiene gli elementi seguenti:

-   Componenti [*selezionabili inclusi in modo esplicito.*](vssgloss-s.md)

    L'inclusione di questi file nelle operazioni di backup è indicata da [**IVssBackupComponents::AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) e nelle operazioni di ripristino da [**IVssBackupComponents::SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore).

-   Non selezionabile per i sottocomponenti di backup senza un predecessore del componente di backup selezionabile.

    Tutti questi componenti devono essere inclusi se i componenti del writer devono essere inclusi nell'operazione. L'inclusione di questi file nelle operazioni di backup è indicata da [**IVssBackupComponents::AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) e nelle operazioni di ripristino da [**IVssBackupComponents::SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore).

-   Componenti aggiunti in modo implicito al backup [](vssgloss-s.md) ([*sottocomponenti*](vssgloss-s.md)) selezionabili per il ripristino e aggiunti in modo esplicito al ripristino.

    Questi componenti possono essere selezionabili o non selezionabili, ma hanno un predecessore selezionabile usato per selezionarli in modo implicito per il backup. Vengono aggiunti al documento Componenti di backup da [**IVssBackupComponents::AddRestoreSubcomponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent).

Le identità dei componenti incluse in modo implicito nel ripristino non vengono archiviate nel documento Componenti di backup.

VSS ha accesso alle informazioni sull'inclusione dei componenti: i writer senza componenti inclusi in modo esplicito in un ripristino o in un backup non ricevono eventi VSS dopo la generazione degli eventi [*PrepareForBackup*](vssgloss-p.md) [*o PreRestore.*](vssgloss-p.md)

I writer non possono eseguire direttamente query su queste informazioni. Non si tratta di una limitazione significativa perché, in base alla progettazione, i singoli writer VSS non devono richiedere informazioni dettagliate sullo stato di altri writer nel sistema e, come indicato in precedenza, quelli senza componenti inclusi non dovranno partecipare all'operazione VSS.

Un richiedente può determinare quali componenti sono stati inclusi in modo esplicito in un'operazione.

Il [**metodo IVssBackupComponents::GetWriterComponentsCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponentscount) restituisce il numero di writer con informazioni sui componenti archiviate nel documento componenti di backup (e non il numero di componenti nel documento).

Il richiedente indicizza le informazioni del writer archiviate [**usando IVssBackupComponents::GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents), che restituisce istanze dell'interfaccia [**IVssWriterComponentsExt.**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext) **L'interfaccia IVssWriterComponentsExt** consente al richiedente di ottenere la classe [*writer*](vssgloss-w.md) e l'istanza del [*writer*](vssgloss-w.md) dei writer partecipanti, nonché di accedere alle informazioni sui componenti archiviati nel documento Componenti di backup.

## <a name="information-on-included-components"></a>Informazioni sui componenti inclusi

Rappresentazione del documento dei componenti di backup dei dati del componente (che non include informazioni sul percorso e sulla specifica del file), a cui si accede tramite istanze [**dell'interfaccia IVssComponent.**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent)

I richiedenti e i writer ottengono l'accesso alle istanze [**dell'interfaccia IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) in modi diversi.

Un richiedente esamina i dati dei componenti in un writer in base al writer usando istanze dell'interfaccia [**IVssWriterComponentsExt**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext) restituita da [**IVssBackupComponents::GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents).

Oltre alle informazioni di identificazione del writer, [**l'interfaccia IVssWriterComponentsExt**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext) fornisce una matrice di istanze dell'interfaccia [**IVssComponent,**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) una per ognuno dei componenti inclusi tra i writer selezionati.

Come illustrato in Ciclo di vita del documento dei componenti di [backup,](backup-components-document-life-cycle.md)i writer possono accedere alle stesse informazioni tramite l'interfaccia [**IVssWriterComponents**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswritercomponents) quando si gestisce l'evento PrepareForBackup, PrepareForSnapshot, PostSnapshot, BackupComplete, PreRestore o PostRestore.

[**IVssComponent consente**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) sia al writer che ai richiedenti di ottenere le informazioni seguenti:

-   Nome, tipo e percorso logico di un componente [*(*](vssgloss-l.md) [**GetComponentName,**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getcomponentname) [**GetComponentType,**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getcomponenttype) [**GetLogicalPath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getlogicalpath))
-   Come ripristinare un componente come indicato dalla destinazione [*di*](vssgloss-r.md) ripristino ([**IVssComponent::GetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoretarget))
-   Se è stato usato un percorso alternativo per il ripristino di un file ([**GetAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmapping), [**GetAlternateLocationMappingCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmappingcount))
-   Nuove informazioni di destinazione, se presenti ([**GetNewTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtarget), [**GetNewTargetCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtargetcount))
-   Messaggi di errore pre e post-ripristino ([**GetPreRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getprerestorefailuremsg), [**GetPostRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpostrestorefailuremsg))
-   Se è [*stato selezionato un elemento selezionabile*](vssgloss-s.md) per il componente di backup che definisce un set di componenti per il ripristino ([**IsSelectedForRestore**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-isselectedforrestore))
-   Esito positivo di un backup o di un ripristino ([**GetBackupSucceeded**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupsucceeded), [**GetFileRestoreStatus**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getfilerestorestatus))
-   Qualsiasi opzione di backup o ripristino specifica del writer che potrebbe essere stata impostata da [**IVssBackupComponents::SetBackupOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupoptions) o [**IVssBackupComponents::SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) ([**GetBackupOptions**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupoptions), [**GetRestoreOptions**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoreoptions))
-   Tutti i metadati di backup o ripristino specifici del writer ([**GetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata)), [**GetRestoreMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoremetadata))
-   Informazioni sul timestamp ([**GetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupstamp), [**GetPreviousBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpreviousbackupstamp))
-   Informazioni sui sottocomponenti di backup inclusi in modo esplicito in un ripristino ([**GetRestoreSubcomponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoresubcomponent), [**GetRestoreSubcomponentCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoresubcomponentcount))

A differenza dei richiedenti, i writer possono modificare determinate informazioni nel documento Componenti di backup tramite [**l'interfaccia IVssComponent:**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent)

-   Come ripristinare un componente come indicato dalla destinazione di ripristino ([**IVssComponent::SetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoretarget))
-   Metadati di backup e ripristino specifici del writer ([**IVssComponent::SetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupmetadata), [**IVssComponent::SetRestoreMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoremetadata))
-   Informazioni sul timestamp ([**SetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp))
-   Messaggi di errore pre-ripristino e post-ripristino ([**SetPreRestoreFailureMsg,**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setprerestorefailuremsg) [**SetPostRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setpostrestorefailuremsg))

## <a name="requester-state-information"></a>Informazioni sullo stato del richiedente

I richiedenti inseriscono informazioni sullo stato di un'operazione di backup o ripristino nel documento Componenti di backup usando [**l'interfaccia IVssBackupComponents.**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) Le applicazioni writer sono in grado di eseguire query per ottenere queste informazioni tramite [**la classe CVssWriter.**](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriter)

Le informazioni sullo stato archiviate nel documento Componenti di backup includono quanto segue:

Informazioni generali sul backup

-   Tipo di backup complessivo (incrementale, differenziale o completo)<dl> <dt>

Impostazione da parte dei richiedenti [ **tramite IVssBackupComponents::SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate)
</dt> <dt>

Recuperato dai writer tramite [ **CVssWriter::GetBackupType**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getbackuptype)
</dt> </dl>
-   Whether component operations are supported<dl> <dt>

Impostazione da parte dei richiedenti [ **tramite IVssBackupComponents::SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate)
</dt> <dt>

Recuperato dai writer con [ **CVssWriter::AreComponentsSelected**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-arecomponentsselected)
</dt> </dl>
-   Whether the bootable system state is backed up<dl> <dt>

Impostazione da parte dei richiedenti [ **tramite IVssBackupComponents::SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate)
</dt> <dt>

Recuperato dai writer con [ **CVssWriter::IsBootableStateBackedUp**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-isbootablesystemstatebackedup)
</dt> </dl>
-   Whether partial file operations are supported<dl> <dt>

Impostazione da parte dei richiedenti [ **tramite IVssBackupComponents::SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate)
</dt> <dt>

Recuperato dai writer con [ **CVssWriter::IsPartialFileSupportEnabled**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-ispartialfilesupportenabled)
</dt> </dl>

Informazioni generali sul ripristino

-   Tipo di ripristino complessivo (se il ripristino è tramite copia o importazione)<dl> <dt>

Impostazione da parte dei richiedenti [ **tramite IVssBackupComponents::SetRestoreState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestorestate)
</dt> <dt>

Recuperato dai writer tramite [ **CVssWriter::GetRestoreType**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getrestoretype)
</dt> </dl>

Informazioni sul supporto dei file

-   Percorso dei file di intervalli usati da un componente specifico nelle operazioni sui file parziali<dl> <dt>

Impostazione da parte dei richiedenti [ **tramite IVssBackupComponents::SetRangesFilePath**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrangesfilepath)
</dt> <dt>

Recuperato da writer (o richiedenti) tramite [ **IVssComponent::GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile)
</dt> </dl>

Stato delle informazioni

-   Indicare se è stato eseguito correttamente il backup di uno dei componenti di un writer specificato<dl> <dt>

Impostazione da parte dei richiedenti [ **tramite IVssBackupComponents::SetBackupSucceeded**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded)
</dt> <dt>

Recuperato da writer e richiedenti usando [ **IVssComponent::GetBackupSucceeded**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupsucceeded)
</dt> </dl>
-   Indicate whether one of a given writer's components was successfully restored<dl> <dt>

Impostata dai richiedenti [ **tramite IVssBackupComponents::SetFileRestoreStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setfilerestorestatus)
</dt> <dt>

Recuperato da writer e richiedenti tramite [ **IVssComponent::GetFileRestoreStatus**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getfilerestorestatus)
</dt> </dl>

Writer-Settable informazioni

-   Specifica di backup aggiuntiva per uno dei componenti di un writer specificato<dl> <dt>

Impostazione da parte di writer [ **tramite IVssComponent::SetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupmetadata)
</dt> <dt>

Recuperato da writer e richiedenti usando [ **IVssComponent::GetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata)
</dt> </dl>
-   Additional restore specification for one of a given writer's components<dl> <dt>

Impostazione da parte di writer [ **tramite IVssComponent::SetRestoreMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoremetadata)
</dt> <dt>

Recuperato da writer e richiedenti usando [ **IVssComponent::GetRestoreMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoremetadata)
</dt> </dl>
-   A backup stamp that indicates, in a writer's own specific format, the time of the current backup of one of its component's backups<dl> <dt>

Impostazione da parte di writer [ **tramite IVssComponent::SetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp)
</dt> <dt>

Recuperato da writer e richiedenti tramite [ **IVssComponent::GetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupstamp)
</dt> </dl>
-   A backup stamp that indicates, in a writer's own specific format, the time of the last backup of one of its components' backups using a backup stamp initially set by <a href="/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp">IVssComponent::SetBackupStamp</a><dl> <dt>

Archiviati e impostati dai richiedenti per un componente specifico [ **usando IVssBackupComponents::SetPreviousBackupStamp**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setpreviousbackupstamp)
</dt> <dt>

Recuperato da writer e richiedenti tramite [ **IVssComponent::GetPreviousBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpreviousbackupstamp)
</dt> </dl>
-   Error messages for failure before and after restore operations<dl> <dt>

Impostare i writer usando [**IVssComponent::SetPreRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setprerestorefailuremsg) o [**IVssComponent::SetPostRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setpostrestorefailuremsg)
</dt> <dt>

Recuperato da writer e richiedenti usando [**IVssComponent::GetPreRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getprerestorefailuremsg) o [**IVssComponent::GetPostRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpostrestorefailuremsg)
</dt> </dl>

 

 
