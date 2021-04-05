---
description: Il documento componenti di backup viene mantenuto dalle istanze dell'interfaccia IVssBackupComponents.
ms.assetid: 8c7ebba8-58c4-4733-ba59-802abf902c5e
title: Contenuto del documento dei componenti di backup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e12c88ebffa0037702e1f30dd818d4fd23fe4e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885414"
---
# <a name="backup-components-document-contents"></a>Contenuto del documento dei componenti di backup

Il documento componenti di backup viene mantenuto dalle istanze dell'interfaccia [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) . Questa interfaccia contiene inoltre numerosi metodi per il controllo delle operazioni di backup, la modifica delle copie shadow e l'esecuzione di query sullo stato del sistema. Tuttavia, non tutte le informazioni del documento sono direttamente accessibili tramite questa interfaccia.

Il documento componenti di backup è costituito da diversi set di dati:

-   Informazioni sui componenti inclusi in modo esplicito in un'operazione di backup o ripristino
-   Rappresentazione delle informazioni sul componente e sul writer archiviati
-   Informazioni sullo stato relative all'operazione di backup/ripristino

Sebbene le informazioni sul componente siano disponibili sia per il richiedente che per il writer, solo il writer ha accesso alle informazioni sullo stato.

## <a name="component-inclusion-information"></a>Informazioni sull'inclusione di componenti

Il documento componenti di backup contiene un elenco dei componenti inclusi in modo esplicito nel backup e nel ripristino dal richiedente. L'elenco contiene gli elementi seguenti:

-   Inclusi in modo esplicito i [*componenti selezionabili*](vssgloss-s.md).

    L'inclusione di questi file nelle operazioni di backup è indicata da [**IVssBackupComponents:: AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) e dalle operazioni di ripristino di [**IVssBackupComponents:: SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore).

-   Non selezionabile per i sottocomponenti di backup senza un predecessore selezionabile per il componente di backup.

    Tutti questi componenti devono essere inclusi se nell'operazione sono inclusi componenti del writer. L'inclusione di questi file nelle operazioni di backup è indicata da [**IVssBackupComponents:: AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) e dalle operazioni di ripristino di [**IVssBackupComponents:: SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore).

-   Componenti aggiunti in modo implicito al backup ([*sottocomponenti*](vssgloss-s.md)) [*selezionabili per il ripristino*](vssgloss-s.md) e aggiunti esplicitamente al ripristino.

    Questi componenti possono essere selezionabili o non selezionabili, ma hanno un predecessore selezionabile che è stato usato per selezionarli in modo implicito per il backup. Vengono aggiunti al documento componenti di backup di [**IVssBackupComponents:: AddRestoreSubcomponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent).

Le identità dei componenti inclusi in modo implicito nel ripristino non vengono archiviate nel documento componenti di backup.

VSS ha accesso alle informazioni sull'inclusione dei componenti: i writer senza componenti inclusi in modo esplicito in un ripristino o un backup non ricevono eventi VSS dopo la generazione degli eventi [*PrepareForBackup*](vssgloss-p.md) o di [*preripristino*](vssgloss-p.md) .

I writer non possono eseguire query direttamente su queste informazioni. Non si tratta di una limitazione significativa perché, per impostazione predefinita, i singoli writer del servizio Copia Shadow del volume non devono richiedere informazioni dettagliate sullo stato di altri writer del sistema e, come indicato in precedenza, quelli senza componenti inclusi non dovranno partecipare all'operazione VSS.

Un richiedente può determinare quali componenti sono stati inclusi in modo esplicito in un'operazione.

Il metodo [**IVssBackupComponents:: GetWriterComponentsCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponentscount) restituisce il numero di writer con le informazioni sul componente archiviate nel documento dei componenti di backup (e non il numero di componenti nel documento).

Il richiedente indicizza le informazioni del writer archiviato usando [**IVssBackupComponents:: GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents), che restituisce le istanze dell'interfaccia [**IVssWriterComponentsExt**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext) . L'interfaccia **IVssWriterComponentsExt** consente al richiedente di ottenere la [*classe Writer*](vssgloss-w.md) e l' [*istanza writer*](vssgloss-w.md) dei writer partecipanti, nonché di accedere alle informazioni relative ai componenti archiviati nel documento componenti di backup.

## <a name="information-on-included-components"></a>Informazioni sui componenti inclusi

La rappresentazione del documento dei componenti di backup dei dati del componente, che non include informazioni sulle specifiche di percorso e file, a cui si accede tramite istanze dell'interfaccia [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) .

I richiedenti e i writer ottengono l'accesso alle istanze dell'interfaccia [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) in modi diversi.

Un richiedente esamina i dati del componente in un writer in base al writer usando le istanze dell'interfaccia [**IVssWriterComponentsExt**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext) restituite da [**IVssBackupComponents:: GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents).

Oltre alle informazioni di identificazione del writer, l'interfaccia [**IVssWriterComponentsExt**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext) fornisce una matrice di istanze dell'interfaccia [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) , una per ogni componente dei writer selezionati inclusi.

Come indicato nel [ciclo di vita del documento dei componenti di backup](backup-components-document-life-cycle.md), i writer possono accedere alle stesse informazioni tramite l'interfaccia [**IVssWriterComponents**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswritercomponents) durante la gestione dell'evento PrepareForBackup, PrepareForSnapshot, PostSnapshot, BackupComplete, PreRestore o PostRestore.

[**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) consente a writer e richiedenti di ottenere le informazioni seguenti:

-   Nome, tipo e [*percorso logico*](vssgloss-l.md) di un componente ([**GetComponentName**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getcomponentname), [**GetComponentType**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getcomponenttype), [**GetLogicalPath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getlogicalpath))
-   Come deve essere ripristinato un componente come indicato dalla [*destinazione di ripristino*](vssgloss-r.md) ([**IVssComponent:: GetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoretarget))
-   Se è stato usato un percorso alternativo per il ripristino di un file ([**GetAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmapping), [**GetAlternateLocationMappingCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmappingcount))
-   Nuove informazioni di destinazione, se presenti ([**GetNewTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtarget), [**GetNewTargetCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtargetcount))
-   Messaggi di errore pre-e post-ripristino ([**GetPreRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getprerestorefailuremsg), [**GetPostRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpostrestorefailuremsg))
-   Se è stato selezionato un componente [*selezionabile per il backup*](vssgloss-s.md) che definisce un set di componenti per il ripristino ([**IsSelectedForRestore**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-isselectedforrestore))
-   Indica se il backup o il ripristino è riuscito ([**GetBackupSucceeded**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupsucceeded), [**GetFileRestoreStatus**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getfilerestorestatus))
-   Eventuali opzioni di backup o ripristino specifiche del writer che potrebbero essere state impostate da [**IVssBackupComponents:: SetBackupOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupoptions) o [**IVssBackupComponents:: SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) ([**GetBackupOptions**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupoptions), [**GetRestoreOptions**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoreoptions))
-   Tutti i metadati specifici del writer per il backup o il ripristino ([**GetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata)), [**GetRestoreMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoremetadata))
-   Informazioni timestamp ([**GetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupstamp), [**GetPreviousBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpreviousbackupstamp))
-   Informazioni sui sottocomponenti di backup inclusi in modo esplicito in un ripristino ([**GetRestoreSubcomponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoresubcomponent), [**GetRestoreSubcomponentCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoresubcomponentcount))

A differenza dei richiedenti, i writer possono modificare determinate informazioni nel documento componenti di backup tramite l'interfaccia [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) :

-   Come deve essere ripristinato un componente come indicato dalla destinazione di ripristino ([**IVssComponent:: SetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoretarget))
-   Metadati di backup e ripristino specifici del writer ([**IVssComponent:: SetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupmetadata), [**IVssComponent:: SetRestoreMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoremetadata))
-   Informazioni timestamp ([**SetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp))
-   Messaggi di errore pre-e post-ripristino ([**SetPreRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setprerestorefailuremsg), [**SetPostRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setpostrestorefailuremsg))

## <a name="requester-state-information"></a>Informazioni sullo stato del richiedente

I richiedenti inseriscono informazioni sullo stato di un'operazione di backup o ripristino nel documento componenti di backup usando l'interfaccia [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) . Le applicazioni writer sono in grado di eseguire query per queste informazioni tramite la classe [**CVssWriter**](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriter) .

Le informazioni sullo stato archiviate nel documento componenti di backup includono quanto segue:

Informazioni generali sul backup

-   Il tipo di backup complessivo (incrementale, differenziale o completo)<dl> <dt>

Impostato dai richiedenti con [ **IVssBackupComponents:: SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate)
</dt> <dt>

Recuperato dai writer con [ **CVssWriter:: GetBackupType**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getbackuptype)
</dt> </dl>
-   Whether component operations are supported<dl> <dt>

Impostato dai richiedenti con [ **IVssBackupComponents:: SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate)
</dt> <dt>

Recuperato dai writer con [ **CVssWriter:: AreComponentsSelected**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-arecomponentsselected)
</dt> </dl>
-   Whether the bootable system state is backed up<dl> <dt>

Impostato dai richiedenti con [ **IVssBackupComponents:: SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate)
</dt> <dt>

Recuperato dai writer con [ **CVssWriter:: IsBootableStateBackedUp**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-isbootablesystemstatebackedup)
</dt> </dl>
-   Whether partial file operations are supported<dl> <dt>

Impostato dai richiedenti con [ **IVssBackupComponents:: SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate)
</dt> <dt>

Recuperato dai writer con [ **CVssWriter:: IsPartialFileSupportEnabled**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-ispartialfilesupportenabled)
</dt> </dl>

Informazioni generali sul ripristino

-   Tipo di ripristino generale (se il ripristino è da copia o importazione)<dl> <dt>

Impostato dai richiedenti con [ **IVssBackupComponents:: SetRestoreState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestorestate)
</dt> <dt>

Recuperato dai writer con [ **CVssWriter:: GetRestoreType**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getrestoretype)
</dt> </dl>

Informazioni sui file di supporto

-   Percorso dei file degli intervalli utilizzati da un componente specifico in operazioni di file parziali<dl> <dt>

Impostato dai richiedenti con [ **IVssBackupComponents:: SetRangesFilePath**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrangesfilepath)
</dt> <dt>

Recuperato da Writer (o richiedenti) con [ **IVssComponent:: GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile)
</dt> </dl>

Stato delle informazioni

-   Indica se è stato eseguito il backup di uno dei componenti del writer specificato<dl> <dt>

Impostato dai richiedenti con [ **IVssBackupComponents:: SetBackupSucceeded**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded)
</dt> <dt>

Recuperato da writer e richiedenti con [ **IVssComponent:: GetBackupSucceeded**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupsucceeded)
</dt> </dl>
-   Indicate whether one of a given writer's components was successfully restored<dl> <dt>

Impostato dai richiedenti con [ **IVssBackupComponents:: SetFileRestoreStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setfilerestorestatus)
</dt> <dt>

Recuperato da writer e richiedente usando [ **IVssComponent:: GetFileRestoreStatus**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getfilerestorestatus)
</dt> </dl>

Informazioni Writer-Settable

-   Specifica di backup aggiuntiva per uno dei componenti del writer specificato<dl> <dt>

Impostato dai writer con [ **IVssComponent:: SetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupmetadata)
</dt> <dt>

Recuperato da writer e richiedenti con [ **IVssComponent:: GetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata)
</dt> </dl>
-   Additional restore specification for one of a given writer's components<dl> <dt>

Impostato dai writer con [ **IVssComponent:: SetRestoreMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoremetadata)
</dt> <dt>

Recuperato da writer e richiedenti con [ **IVssComponent:: GetRestoreMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoremetadata)
</dt> </dl>
-   A backup stamp that indicates, in a writer's own specific format, the time of the current backup of one of its component's backups<dl> <dt>

Impostato dai writer con [ **IVssComponent:: SetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp)
</dt> <dt>

Recuperato da writer e richiedenti con [ **IVssComponent:: GetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupstamp)
</dt> </dl>
-   A backup stamp that indicates, in a writer's own specific format, the time of the last backup of one of its components' backups using a backup stamp initially set by <a href="/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp">IVssComponent:: SetBackupStamp</a><dl> <dt>

Archiviato e impostato dai richiedenti per un componente specifico usando [ **IVssBackupComponents:: SetPreviousBackupStamp**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setpreviousbackupstamp)
</dt> <dt>

Recuperato da writer e richiedenti con [ **IVssComponent:: GetPreviousBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpreviousbackupstamp)
</dt> </dl>
-   Error messages for failure before and after restore operations<dl> <dt>

Impostato dai writer con [**IVssComponent:: SetPreRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setprerestorefailuremsg) o [**IVssComponent:: SetPostRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setpostrestorefailuremsg)
</dt> <dt>

Recuperato da writer e richiedenti con [**IVssComponent:: GetPreRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getprerestorefailuremsg) o [**IVssComponent:: GetPostRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpostrestorefailuremsg)
</dt> </dl>

 

 
