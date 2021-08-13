---
description: Questa fase del backup inizializza sia il writer che il richiedente, compilando le strutture di dati interne, specificando il backup e stabilendo la comunicazione tra writer e richiedente tramite la chiamata richiesta a IVssBackupComponents::GatherWriterMetadata. Per altre informazioni, vedere Panoramica dell'elaborazione di un backup in VSS.
ms.assetid: 1fc46062-c4a0-4aa2-ae05-3d7cded18584
title: Panoramica dell'inizializzazione del backup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4054dc644056100a4db28ea11b6dcaf9c358084a1b01b9ad28c13e14133fc5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118591355"
---
# <a name="overview-of-backup-initialization"></a>Panoramica dell'inizializzazione del backup

Questa fase del backup inizializza sia il writer che il richiedente, compilando le strutture di dati interne, specificando il backup e stabilendo la comunicazione tra writer e richiedente tramite la chiamata richiesta a [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata). Per altre informazioni, vedere [Panoramica dell'elaborazione di un backup in VSS.](overview-of-processing-a-backup-under-vss.md)

Nella tabella seguente viene illustrata la sequenza di azioni ed eventi necessari per l'inizializzazione del backup.



| Azione del richiedente                                                                                                                                                                                                                                                                                                                            | Evento                                                     | Azione writer                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Crea [**un'interfaccia IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) e la inizializza per gestire un backup (vedere [**CreateVssBackupComponents,**](/windows/desktop/api/VsBackup/nf-vsbackup-createvssbackupcomponents) [**IVssBackupComponents::InitializeForBackup)**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforbackup)e facoltativamente abilitare o disabilitare i writer nel sistema. | Nessuno                                                      | Nessuno                                                                                                                                                                                                                                                       |
| Facoltativamente, impostare il contesto per le operazioni di copia shadow ed eventualmente eseguire una query sul sistema sui provider e sulle copie shadow supportate (vedere [**IVssBackupComponents::SetContext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext), [**IVssBackupComponents::Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query)).                                               | Nessuno                                                      | Nessuno                                                                                                                                                                                                                                                       |
| Il richiedente può fornire informazioni aggiuntive sulla gestione delle operazioni di backup e ripristino (vedere [**IVssBackupComponents::SetBackupState)**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate)                                                                                                                                                        | Nessuno                                                      | Nessuno                                                                                                                                                                                                                                                       |
| Avvia un contatto asincrono con i writer (vedere [**IVssBackupComponents::GatherWriterMetadata)**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)                                                                                                                                                                                           | [*Identificare*](vssgloss-i.md) | Crea un documento di metadati del writer (vedere Uso del documento di metadati del [writer](working-with-the-writer-metadata-document.md), [**CVssWriter::OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify), [**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata)) |



 

## <a name="requester-actions-during-backup-initialization"></a>Azioni del richiedente durante l'inizializzazione del backup

Un [**oggetto IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) può essere usato per un solo backup. Pertanto, un richiedente deve procedere fino alla fine del backup, incluso il rilascio **dell'interfaccia IVssBackupComponents.** Se il backup deve terminare prematuramente, il richiedente deve chiamare [**IVssBackupComponents::AbortBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup) e quindi rilasciare l'oggetto **IVssBackupComponents.** Per altre informazioni, vedere Interruzione delle operazioni [VSS.](aborting-vss-operations.md) Non tentare di riprendere **l'interfaccia IVssBackupComponents.**

In genere, il documento dei componenti di backup del richiedente viene inizializzato come vuoto. Un documento dei componenti di backup archiviato può essere caricato quando viene chiamato [**IVssBackupComponents::InitializeForBackup,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforbackup) in genere a supporto di volumi copiati shadow trasportabili. In questo caso, la comunicazione tra writer e richiedente sarà leggermente diversa da quella descritta di seguito. Per altre [informazioni, vedere Importazione di volumi copiati shadow](importing-transportable-shadow-copied-volumes.md) trasportabili.

Per aggiungere volumi al set di copie shadow, un richiedente deve innanzitutto impostare il contesto per l'operazione di copia shadow chiamando [**IVssBackupComponents::SetContext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext). Se questo metodo non viene chiamato, viene usato il contesto predefinito per le copie shadow, VSS \_ CTX \_ BACKUP. Per informazioni sull'impostazione del contesto della copia shadow, vedere [Configurazioni del contesto della copia shadow.](shadow-copy-context-configurations.md)

Per iniziare il completamento della configurazione prima del backup, un richiedente deve chiamare [**IVssBackupComponents::SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate). In questo modo, un richiedente indica agli autori:

-   Tipo di backup (come definito in [**VSS \_ BACKUP \_ TYPE)**](/windows/desktop/api/Vss/ne-vss-vss_backup_type)
-   Se il backup include uno stato del sistema di avvio
-   Indica se il richiedente supporta la selezione di singoli componenti o il backup di interi volumi.

Tutti i richiedenti che partecipano alle operazioni di backup e ripristino devono sempre chiamare [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata). Questo metodo avvia la comunicazione tra writer e richiedente generando un evento VsS [*Identify,*](vssgloss-i.md) in risposta al quale un writer crea il documento di metadati.

Prima di chiamare [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata), un richiedente ha la possibilità di abilitare o disabilitare in modo esplicito determinati writer e classi writer specifici usando [**IVssBackupComponents::EnableWriterClasses**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-enablewriterclasses), [**IVssBackupComponents::D isableWriterInstances**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-disablewriterinstances)e [**IVssBackupComponents::D isableWriterClasses**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-disablewriterclasses) (per impostazione predefinita, tutte le classi sono abilitate). Dopo **la chiamata di IVssBackupComponents::GatherWriterMetadata,** queste chiamate non hanno alcun effetto.

Poiché non è possibile ottenere un elenco di writer nel sistema prima di chiamare [**IVssBackupComponents::GatherWriterMetadata,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)i richiedenti possono prendere in considerazione la creazione e l'eliminazione di una seconda istanza di [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) per ottenere l'elenco.

Non è necessario chiamare [**IVssBackupComponents::GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) dopo il completamento di [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata). I writer che non riescono a elaborare l'evento [*Identify*](vssgloss-i.md) generato dalle chiamate non fanno parte dell'elenco di writer che forniscono metadati trovati da [**IVssBackupComponents::GetWriterMetadataCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadatacount) e [**IVssBackupComponents::GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata) (vedere Determinazione dello stato [del writer).](determining-writer-status.md)

## <a name="writer-actions-during-backup-initialization"></a>Azioni del writer durante l'inizializzazione del backup

In risposta all'evento Identify, VSS chiama il metodo del gestore virtuale di ogni writer, [**CVssWriter::OnIdentify.**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) Un writer crea il documento di metadati del writer eseguendo l'override dell'implementazione predefinita di **CVssWriter::OnIdentify** e usando [**l'interfaccia IVssCreateWriterMetadata.**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata)

Si noti che le applicazioni diverse dal richiedente corrente (ad esempio, le applicazioni di sistema) possono generare eventi Di identificazione che devono essere gestiti dal writer. Inoltre, un writer non può determinare in alcun modo dall'interno di [**CVssWriter::OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) quale applicazione ha generato l'evento Identify.

In questo caso, dato che un writer può ricevere diversi eventi Identify durante l'elaborazione di un'operazione di backup, un writer non deve mai impostare le informazioni sullo stato nel gestore [**CVssWriter::OnIdentify.**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify)

[**CVssWriter::OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) deve invece eseguire un algoritmo coerente per creare il documento di metadati del writer, in particolare perché dopo che un writer ha creato il documento, né il richiedente né il writer possono modificarlo. Da questo punto in poi, si tratta di un documento di sola lettura.

Ciò significa che il [](vssgloss-c.md) numero e il tipo di componenti associati a un writer, i file che fanno parte di ogni componente e l'esclusione esplicita di file dalle operazioni di backup o ripristino non può essere modificata dopo che un writer torna a elaborare l'evento Identify.

Tutti i writer che partecipano al Servizio Copia Microsoft devono eseguire le operazioni seguenti:

1.  Indicare un metodo di ripristino per tutti i componenti gestiti dal writer usando [**IVssCreateWriterMetadata::SetRestoreMethod**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setrestoremethod).
2.  Aggiungere almeno un componente usando [**IVssCreateWriterMetadata::AddComponent.**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponent) Per altre informazioni sulla specifica del componente, vedere [Definizione](definition-of-components-by-writers.md) dei componenti in base ai writer.

Un writer indica i file da partecipare a un'operazione di backup o ripristino aggiungendo set di [*file,*](vssgloss-f.md)ovvero una combinazione di un percorso, una specifica di file e un flag di ricorsione, a un determinato componente usando [**IVssCreateWriterMetadata::AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup), [**IVssCreateWriterMetadata::AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)o [](definition-of-components-by-writers.md) [**IVssCreateWriterMetadata::AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles), a seconda del tipo .)

Un writer può anche avere uno o più componenti vuoti, componenti a cui non è stato aggiunto alcun file. Sono molto utili per organizzare i componenti del writer. Vedere [Percorso logico dei componenti.](logical-pathing-of-components.md)

Un writer usa [**IVssCreateWriterMetadata::AddExcludeFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addexcludefiles) per impedire in modo esplicito l'inserimento di file nel backup. Questa esclusione esplicita è utile perché è possibile usare caratteri jolly per specificare i file da includere (vedere [Escludi specifica elenco file).](writer-metadata-document-contents.md) Si noti che l'elenco di file di esclusione ha la precedenza rispetto all'elenco dei file dei componenti.

[**IVssCreateWriterMetadata::AddAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addalternatelocationmapping) viene usato per creare [*mapping*](vssgloss-a.md) di percorsi alternativi per i set di file specificati aggiunti a uno dei componenti del writer. Questi mapping vengono usati durante il ripristino dei file quando il ripristino nel percorso originale di un file non è possibile o auspicabile. Vedere [Panoramica del ripristino effettivo dei file e](overview-of-actual-file-restoration.md) dei percorsi di backup e ripristino non [predefiniti.](non-default-backup-and-restore-locations.md)

Poiché il set di file di backup è specificato nel documento di metadati del writer, non può essere modificato in un secondo momento. Pertanto, un writer deve essere codificato in modo che la definizione del set di file includa tutti i file necessari nel backup, in base al nome o tramite caratteri jolly. È possibile che siano inclusi alcuni file che potrebbero essere creati dopo l'evento Identify.

 

 



