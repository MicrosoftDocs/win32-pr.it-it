---
description: Durante l'inizializzazione di un'operazione di ripristino vss, un richiedente deve recuperare il documento del componente di backup e ogni documento di metadati del writer pertinente creato e salvato durante l'operazione di backup.
ms.assetid: 0a087125-c9d4-460a-8153-3e2e26633ac2
title: Panoramica dell'inizializzazione del ripristino
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c531e4b47c49e5bd5538ea30583a31273bb6645a445ef1b1ea851bac539411c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117751690"
---
# <a name="overview-of-restore-initialization"></a>Panoramica dell'inizializzazione del ripristino

Durante l'inizializzazione di un'operazione di ripristino vss, un richiedente deve recuperare il documento del componente di backup e ogni documento di metadati del writer pertinente creato e salvato durante l'operazione di backup. Lo stato corrente del writer verrà sottoposto a query nella gestione [*dell'evento Identify*](vssgloss-i.md) generato dal richiedente. Per altre informazioni, vedere [Panoramica dell'elaborazione di un ripristino in VSS.](overview-of-processing-a-restore-under-vss.md)

Nella tabella seguente viene illustrata la sequenza di azioni ed eventi necessari per inizializzare un'operazione di ripristino.



| Azione del richiedente                                                                                                                                                                                                                                                                                                       | Evento                                                     | Azione writer                                                                                                                                                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Creare [**un'interfaccia IVssBackupComponents,**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) inizializzarla per gestire un ripristino e caricare i metadati del richiedente archiviati (vedere [**CreateVssBackupComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-createvssbackupcomponents), [**IVssBackupComponents::InitializeForRestore).**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforrestore) | Nessuno                                                      | Nessuno                                                                                                                                                                                                                                                                                                                      |
| Chiamare [**CreateVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-createvssexaminewritermetadata) per creare [**interfacce IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) e caricarle con i metadati del writer archiviati.                                                                                                           | Nessuno                                                      | Nessuno                                                                                                                                                                                                                                                                                                                      |
| Avviare un contatto asincrono con i writer (vedere [**IVssBackupComponents::GatherWriterMetadata).**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)                                                                                                                                                                      | [*Identificare*](vssgloss-i.md) | Il writer inizia la gestione degli eventi a supporto del ripristino. Crea il documento di metadati del writer (vedere [Uso del documento](working-with-the-writer-metadata-document.md)di metadati del writer , [**CVssWriter::OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify), [**IVssCreateWriterMetadata).**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata) |
| Il richiedente attende l'inizializzazione dei writer chiamando [**IVssAsync.**](/windows/desktop/api/Vss/nn-vss-ivssasync)                                                                                                                                                                                                                               | Nessuno                                                      | Nessuno                                                                                                                                                                                                                                                                                                                      |



 

## <a name="requester-actions-during-restore-initialization"></a>Azioni del richiedente durante l'inizializzazione del ripristino

Durante la fase di inizializzazione di un ripristino, il richiedente deve avere accesso al documento dei componenti di backup archiviato e a tutti i documenti di metadati del writer.

A seconda dell'implementazione, ciò significa che il richiedente richiederà che i supporti di backup siano montati e leggibili o che sia disponibile un altro meccanismo per l'accesso ai metadati archiviati.

Il richiedente usa il documento XML archiviato contenente il documento dei componenti di backup del richiedente che ha eseguito il backup per inizializzare il documento dei componenti di backup usando [**IVssBackupComponents::InitializeForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforrestore) per accedere alle informazioni.

Come nel caso del backup, le informazioni del documento dei componenti di backup non sono sufficienti per supportare un ripristino. Pertanto, il richiedente deve accedere ai documenti di metadati del writer archiviati durante il backup (vedere Uso dei [componenti da parte del richiedente).](use-of-components-by-the-requestor.md)

Il richiedente recupera i metadati del writer archiviati chiamando [**CreateVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-createvssexaminewritermetadata) per ogni writer i cui dati sono stati sottoposti a backup e che ora devono essere ripristinati. Questa funzione crea un [**oggetto IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) per ogni writer e carica il documento di metadati del writer nell'oggetto .

Come nel caso del backup, per avviare la collaborazione tra se stesso e i writer del sistema, un richiedente deve generare un evento [*Identify*](vssgloss-i.md) chiamando [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata). Non è necessario chiamare [**IVssBackupComponents::GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) dopo il completamento di [**GatherWriterMetadata.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) I writer che non riescono a elaborare l'evento [*Identify*](vssgloss-i.md) non verranno inclusi nell'elenco di writer che forniscono i metadati che devono essere restituiti da [**IVssBackupComponents::GetWriterMetadataCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadatacount) e [**IVssBackupComponents::GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata) (vedere Determinazione dello stato del [writer).](determining-writer-status.md)

Come per l'operazione di backup, un richiedente dovrà eseguire query e analizzare le informazioni nel documento dei componenti di backup e confrontarlo con i dati nei documenti dei metadati del writer per determinare i componenti di cui è stato eseguito il backup e per scegliere quelli da ripristinare (vedere [Panoramica](overview-of-preparing-for-restore.md)della preparazione per il ripristino). Inoltre, il richiedente dovrà generare un elenco dettagliato contenente informazioni sui file nei supporti di backup selezionati per il ripristino, nonché su come e dove devono essere ripristinati. Vedere [Generazione di un set di ripristino.](generating-a-restore-set.md)

Pertanto, alcune applicazioni di backup possono risultare utili per archiviare nei supporti di backup il proprio elenco (nel proprio formato ottimizzato) dei file e le informazioni relative a scrittura, componente, procedura di ripristino e percorso associate. Questo elenco può essere usato per ridurre al minimo la quantità di analisi e confronto tra i documenti di metadati del writer e i documenti dei componenti di backup necessari per supportare un ripristino.

## <a name="writer-actions-during-restore-initialization"></a>Azioni del writer durante l'inizializzazione del ripristino

Come avviene durante un'operazione di ripristino, in risposta all'evento Identify, VSS chiama il metodo del gestore virtuale di ogni writer [**CVssWriter::OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify).

Si noti che le applicazioni diverse dal richiedente corrente (ad esempio, le applicazioni di sistema) possono generare eventi Di identificazione, che devono essere gestiti dal writer. Inoltre, un writer non può determinare in alcun modo dall'interno di [**CVssWriter::OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) quale applicazione ha generato l'evento Identify.

Dato che un writer può ricevere diversi eventi Identify durante l'elaborazione di un'operazione di ripristino, i writer non devono mai impostare informazioni sullo stato nel gestore [**CVssWriter::OnIdentify.**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) Devono invece usare lo stesso algoritmo per la creazione del documento di metadati del writer eseguito durante le operazioni di backup. Per altre informazioni, vedere Writer [Actions during Backup Initialization](overview-of-backup-initialization.md) (Azioni del writer durante l'inizializzazione del backup).

 

 



