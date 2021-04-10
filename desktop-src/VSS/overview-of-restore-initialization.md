---
description: Durante l'inizializzazione di un'operazione di ripristino VSS, un richiedente deve recuperare il documento del componente di backup e ogni documento di metadati del writer pertinente creato e salvato durante l'operazione di backup.
ms.assetid: 0a087125-c9d4-460a-8153-3e2e26633ac2
title: Panoramica dell'inizializzazione del ripristino
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eb62e5282a74e38cd53d36c8ba004f4b8069746
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131270"
---
# <a name="overview-of-restore-initialization"></a>Panoramica dell'inizializzazione del ripristino

Durante l'inizializzazione di un'operazione di ripristino VSS, un richiedente deve recuperare il documento del componente di backup e ogni documento di metadati del writer pertinente creato e salvato durante l'operazione di backup. Lo stato corrente del writer verrà sottoposto a query durante la gestione dell' [*evento di identificazione*](vssgloss-i.md) generato dal richiedente. Per ulteriori informazioni, vedere [Cenni preliminari sull'elaborazione di un ripristino in VSS](overview-of-processing-a-restore-under-vss.md).

Nella tabella seguente viene illustrata la sequenza di azioni ed eventi necessari per inizializzare un'operazione di ripristino.



| Azione del richiedente                                                                                                                                                                                                                                                                                                       | Evento                                                     | Azione del writer                                                                                                                                                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Creare un'interfaccia [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) , inizializzarla per gestire un ripristino e caricare i metadati del richiedente archiviato. vedere [**CreateVssBackupComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-createvssbackupcomponents), [**IVssBackupComponents:: InitializeForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforrestore). | nessuno                                                      | nessuno                                                                                                                                                                                                                                                                                                                      |
| Chiamare [**CreateVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-createvssexaminewritermetadata) per creare interfacce [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) e caricarle con i metadati del writer archiviati.                                                                                                           | nessuno                                                      | nessuno                                                                                                                                                                                                                                                                                                                      |
| Avviare il contatto asincrono con i writer (vedere [**IVssBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata).)                                                                                                                                                                      | [*Identificare*](vssgloss-i.md) | Il writer avvia la gestione degli eventi a supporto del ripristino. Crea il documento di metadati del writer (vedere [utilizzo del documento di metadati del writer](working-with-the-writer-metadata-document.md), [**CVssWriter:: onidentificate**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify), [**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata)). |
| Il richiedente è in attesa dell'inizializzazione dei writer chiamando [**IVssAsync**](/windows/desktop/api/Vss/nn-vss-ivssasync).                                                                                                                                                                                                                               | nessuno                                                      | nessuno                                                                                                                                                                                                                                                                                                                      |



 

## <a name="requester-actions-during-restore-initialization"></a>Azioni del richiedente durante l'inizializzazione del ripristino

Durante la fase di inizializzazione di un ripristino, il richiedente deve avere accesso al documento dei componenti di backup archiviati e a tutti i documenti di metadati del writer.

A seconda dell'implementazione di, ciò significa che il richiedente richiede che i supporti di backup siano montati e leggibili oppure che sia disponibile un altro meccanismo per accedere ai metadati archiviati.

Il richiedente usa il documento XML archiviato contenente il documento componenti di backup del richiedente che ha eseguito il backup per inizializzare il documento relativo ai componenti di backup usando [**IVssBackupComponents:: InitializeForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforrestore) può accedere alle informazioni.

Come nel caso del backup, il documento componenti di backup non contiene informazioni sufficienti per supportare un ripristino. per questo motivo, il richiedente deve accedere ai documenti dei metadati del writer archiviati durante il backup (vedere [uso dei componenti da parte del richiedente](use-of-components-by-the-requestor.md)).

Il richiedente recupera i metadati del writer archiviati chiamando [**CreateVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-createvssexaminewritermetadata) per ogni writer di cui è stato eseguito il backup dei dati e che ora deve essere ripristinato. Questa funzione crea un oggetto [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) per ogni writer e carica il documento di metadati del writer del writer nell'oggetto.

Come nel caso del backup, per avviare la collaborazione tra se stesso e i writer del sistema, un richiedente deve generare un evento di [*Identificazione*](vssgloss-i.md) chiamando [**IVssBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata). Non è necessario chiamare [**IVssBackupComponents:: GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) dopo il completamento di [**GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata). I writer che non riescono a elaborare l'evento di [*Identificazione*](vssgloss-i.md) non verranno inclusi nell'elenco di writer che forniscono i metadati che devono essere restituiti da [**IVssBackupComponents:: GetWriterMetadataCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadatacount) e [**IVssBackupComponents:: GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata) (vedere [determinare lo stato del writer](determining-writer-status.md)).

Come per l'operazione di backup, un richiedente dovrà eseguire una query e analizzare le informazioni nel documento sui componenti di backup e confrontarlo con i dati nei documenti dei metadati del writer per individuare i componenti di cui è stato eseguito il backup e scegliere quelli da ripristinare. vedere [Panoramica della preparazione per il ripristino](overview-of-preparing-for-restore.md). Inoltre, il richiedente dovrà generare un elenco dettagliato contenente le informazioni sui file nel supporto di backup selezionato per il ripristino, nonché le modalità e la posizione in cui devono essere ripristinati. (Vedere [generazione di un set di ripristino](generating-a-restore-set.md)).

È pertanto possibile che alcune applicazioni di backup richiedano di archiviare nei supporti di backup il proprio elenco (in un formato ottimizzato) dei file e le informazioni relative a writer, componenti, procedure di ripristino e percorso. Questo elenco può essere utilizzato per ridurre al minimo la quantità di analisi e di confronto dei documenti di metadati del writer e dei documenti del componente di backup necessari per supportare un ripristino.

## <a name="writer-actions-during-restore-initialization"></a>Azioni del writer durante l'inizializzazione del ripristino

Analogamente a quanto avviene durante un'operazione di ripristino, in risposta all'evento di identificazione, VSS chiama il metodo del gestore virtuale di ogni writer [**CVssWriter:: onidentifi**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify).

Si noti che le applicazioni diverse dal richiedente corrente (ad esempio, le applicazioni di sistema) possono generare eventi di identificazione, che devono essere gestiti dal writer. Inoltre, non esiste alcun modo che un writer determini dall'interno di [**CVssWriter:: Onidentificate**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) l'applicazione che ha generato l'evento di identificazione.

Dato che un writer può ricevere diversi eventi di identificazione durante l'elaborazione di un'operazione di ripristino, i writer non devono mai impostare le informazioni sullo stato nel gestore [**CVssWriter:: onidentifi**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) . Devono invece usare lo stesso algoritmo per la creazione del documento di metadati del writer come è stato fatto durante le operazioni di backup. per altre informazioni, vedere [azioni del writer durante l'inizializzazione del backup](overview-of-backup-initialization.md) .

 

 



