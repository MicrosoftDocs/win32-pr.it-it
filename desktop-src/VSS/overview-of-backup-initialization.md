---
description: "Questa fase del backup Inizializza sia il writer che il richiedente, compilando le strutture di dati interne, specificando il backup e stabilisce la comunicazione del writer/richiedente tramite la chiamata obbligatoria a IVssBackupComponents:: GatherWriterMetadata. Per ulteriori informazioni, vedere Cenni preliminari sull'elaborazione di un backup in VSS."
ms.assetid: 1fc46062-c4a0-4aa2-ae05-3d7cded18584
title: Panoramica dell'inizializzazione del backup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53fb97b43cf19ca60e3e4601899700e35bdad3aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310691"
---
# <a name="overview-of-backup-initialization"></a>Panoramica dell'inizializzazione del backup

Questa fase del backup Inizializza sia il writer che il richiedente, compilando le strutture di dati interne, specificando il backup e stabilisce la comunicazione del writer/richiedente tramite la chiamata obbligatoria a [**IVssBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata). Per ulteriori informazioni, vedere [Cenni preliminari sull'elaborazione di un backup in VSS](overview-of-processing-a-backup-under-vss.md).

Nella tabella seguente viene illustrata la sequenza di azioni ed eventi necessari per l'inizializzazione del backup.



| Azione del richiedente                                                                                                                                                                                                                                                                                                                            | Evento                                                     | Azione del writer                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Crea un'interfaccia [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) e la inizializza per gestire un backup (vedere [**CreateVssBackupComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-createvssbackupcomponents), [**IVssBackupComponents:: InitializeForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforbackup)) e, facoltativamente, abilitare o disabilitare i writer nel sistema. | nessuno                                                      | nessuno                                                                                                                                                                                                                                                       |
| Facoltativamente, impostare il contesto per le operazioni di copia shadow e, facoltativamente, eseguire una query sul sistema sui provider e sulle copie shadow supportate. vedere [**IVssBackupComponents:: secontext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext), [**IVssBackupComponents:: query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query).                                               | nessuno                                                      | nessuno                                                                                                                                                                                                                                                       |
| Il richiedente può fornire ulteriori informazioni sulla gestione delle operazioni di backup e ripristino (vedere [**IVssBackupComponents:: SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate))                                                                                                                                                        | nessuno                                                      | nessuno                                                                                                                                                                                                                                                       |
| Avvia il contatto asincrono con i writer (vedere [**IVssBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata))                                                                                                                                                                                           | [*Identificare*](vssgloss-i.md) | Crea un documento di metadati del writer (vedere [utilizzo del documento di metadati del writer](working-with-the-writer-metadata-document.md), [**CVssWriter:: onidentifi**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify), [**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata)) |



 

## <a name="requester-actions-during-backup-initialization"></a>Azioni del richiedente durante l'inizializzazione del backup

Un oggetto [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) può essere utilizzato solo per un backup. Pertanto, un richiedente deve procedere fino alla fine del backup, incluso il rilascio dell'interfaccia **IVssBackupComponents** . Se il backup deve terminare in modo anomalo, il richiedente deve chiamare [**IVssBackupComponents:: AbortBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup) e quindi rilasciare l'oggetto **IVssBackupComponents** . per ulteriori informazioni, vedere l' [interruzione delle operazioni VSS](aborting-vss-operations.md) . Non tentare di riprendere l'interfaccia **IVssBackupComponents** .

In genere, il documento dei componenti di backup di un richiedente viene inizializzato come vuoto. Un documento dei componenti di backup archiviato può essere caricato quando viene chiamato [**IVssBackupComponents:: InitializeForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforbackup) , in genere supportato da volumi di copie shadow trasportabili. In questo caso, la comunicazione del richiedente Writer sarà leggermente diversa da quella descritta di seguito. Per ulteriori informazioni, vedere [importazione di volumi di copie shadow trasportabili](importing-transportable-shadow-copied-volumes.md) .

Per aggiungere volumi al set di copie shadow, un richiedente deve innanzitutto impostare il contesto per l'operazione di copia shadow chiamando [**IVssBackupComponents:: secontext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext). Se questo metodo non viene chiamato, viene utilizzato il contesto predefinito per le copie shadow, \_ ovvero il backup VSS CTX \_ . Per informazioni sull'impostazione del contesto della copia shadow, vedere configurazioni del contesto per la [Copia Shadow](shadow-copy-context-configurations.md).

Per iniziare il completamento della configurazione prima del backup, un richiedente deve chiamare [**IVssBackupComponents:: SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate). In questo modo, un richiedente indica ai writer:

-   Tipo di backup (come definito nel [**tipo di \_ backup \_ VSS**](/windows/desktop/api/Vss/ne-vss-vss_backup_type))
-   Indica se il backup include uno stato del sistema di avvio
-   Indica se il richiedente supporta la selezione di singoli componenti o esegue il backup di interi volumi.

Tutti i richiedenti che partecipano alle operazioni di backup e ripristino devono chiamare sempre [**IVssBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata). Questo metodo avvia la comunicazione del richiedente del writer generando un evento di [*Identificazione*](vssgloss-i.md) VSS, in risposta al quale un writer crea il documento di metadati.

Prima di chiamare [**IVssBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata), un richiedente ha la possibilità di abilitare o disabilitare esplicitamente determinati writer e classi writer specifiche usando [**IVssBackupComponents:: EnableWriterClasses**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-enablewriterclasses), [**IVssBackupComponents::D Isablewriterinstances**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-disablewriterinstances)e [**IVssBackupComponents::D isablewriterclasses**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-disablewriterclasses) (per impostazione predefinita, tutte le classi sono abilitate). Dopo la chiamata di **IVssBackupComponents:: GatherWriterMetadata** , queste chiamate non hanno alcun effetto.

Poiché non esiste alcun modo per ottenere un elenco di writer nel sistema prima di chiamare [**IVssBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata), i richiedenti possono prendere in considerazione la creazione e l'eliminazione di una seconda istanza di [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) per ottenere l'elenco.

Non è necessario chiamare [**IVssBackupComponents:: GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) dopo il completamento di [**IVssBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata). I writer che non riescono a elaborare l'evento di [*Identificazione*](vssgloss-i.md) generato dalle chiamate non faranno parte dell'elenco di writer che forniscono i metadati trovati da [**IVssBackupComponents:: GetWriterMetadataCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadatacount) e [**IVssBackupComponents:: GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata) (vedere [determinare lo stato del writer](determining-writer-status.md)).

## <a name="writer-actions-during-backup-initialization"></a>Azioni del writer durante l'inizializzazione del backup

In risposta all'evento di identificazione, VSS chiama il metodo del gestore virtuale di ogni writer, [**CVssWriter:: onidentifi**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify). Un writer crea il documento di metadati del writer eseguendo l'override dell'implementazione predefinita di **CVssWriter:: Onidentificate** e usando l'interfaccia [**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata) .

Si noti che le applicazioni diverse dal richiedente corrente (ad esempio, le applicazioni di sistema) possono generare eventi di identificazione che devono essere gestiti dal writer. Inoltre, non esiste alcun modo che un writer determini dall'interno di [**CVssWriter:: Onidentificate**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) l'applicazione che ha generato l'evento di identificazione.

Questo è il caso, dato che un writer può ricevere diversi eventi di identificazione durante l'elaborazione di un'operazione di backup, un writer non deve mai impostare le informazioni sullo stato nel gestore [**CVssWriter:: onidentifi**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) .

Al contrario, [**CVssWriter:: onidentifi**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) deve eseguire un algoritmo coerente per creare il documento di metadati del writer del writer, in particolare perché, in seguito alla creazione del documento da parte di un writer, il richiedente e il writer non possono modificarlo. Da questo punto in poi, si tratta di un documento di sola lettura.

Ciò significa che il numero e il tipo di [*componenti*](vssgloss-c.md) associati a un writer, i file che fanno parte di ogni componente e l'esclusione esplicita dei file dalle operazioni di backup o ripristino non possono essere modificati dopo che un writer ha restituito l'elaborazione dell'evento di identificazione.

Tutti i writer che partecipano a VSS sono necessari per eseguire le operazioni seguenti:

1.  Indicare un metodo di ripristino per tutti i componenti gestiti dal writer usando [**IVssCreateWriterMetadata:: SetRestoreMethod**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setrestoremethod).
2.  Aggiungere almeno un componente usando [**IVssCreateWriterMetadata:: AddComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponent) (vedere la [definizione di componenti per Writer](definition-of-components-by-writers.md) per ulteriori informazioni sulla specifica del componente).

Un writer indica i file per partecipare a un'operazione di backup o ripristino mediante l'aggiunta di [*set di file*](vssgloss-f.md), ovvero una combinazione di un percorso, una specifica del file e un flag di ricorsione, a un determinato componente usando [**IVssCreateWriterMetadata:: AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup), [**IVssCreateWriterMetadata:: AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)o [**IVssCreateWriterMetadata:: AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles), a seconda del tipo (vedere [aggiunta di file ai componenti](definition-of-components-by-writers.md)).

Un writer può inoltre disporre di uno o più componenti vuoti, componenti a cui non è stato aggiunto alcun file. Sono molto utili per organizzare i componenti del writer. (Vedere il [percorso logico dei componenti](logical-pathing-of-components.md)).

Un writer USA [**IVssCreateWriterMetadata:: AddExcludeFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addexcludefiles) per impedire in modo esplicito l'inclusione di file nel backup. Questa esclusione esplicita è utile perché i caratteri jolly possono essere usati per specificare i file da includere (vedere la [specifica dell'elenco di file esclusi](writer-metadata-document-contents.md)). Si noti che l'elenco di file di esclusione ha la precedenza sugli elenchi di file dei componenti.

[**IVssCreateWriterMetadata:: AddAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addalternatelocationmapping) viene usato per creare [*mapping di percorsi alternativi*](vssgloss-a.md) per i set di file specificati che sono stati aggiunti a uno dei componenti del writer. Questi mapping vengono usati durante il ripristino del file quando il ripristino nel percorso originale di un file non è possibile o auspicabile. Vedere [Panoramica del ripristino di file effettivi e dei](overview-of-actual-file-restoration.md) [percorsi di backup e ripristino non predefiniti](non-default-backup-and-restore-locations.md).

Poiché il set di file di backup viene specificato nel documento di metadati del writer, non può essere modificato in un secondo momento. Pertanto, un writer deve essere codificato in modo che la definizione del set di file includa tutti i file necessari nel backup, in base al nome o tramite caratteri jolly. In teoria, può includere alcuni file che potrebbero essere creati dopo l'evento di identificazione.

 

 



