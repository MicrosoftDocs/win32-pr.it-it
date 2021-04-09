---
description: Creazione di copie shadow per i provider
ms.assetid: d5042945-ba81-40d0-b204-1f08d153a788
title: Creazione di copie shadow per i provider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91cc7306e7a13ef8e96ab032016a922411a70f95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049844"
---
# <a name="shadow-copy-creation-for-providers"></a>Creazione di copie shadow per i provider

## <a name="the-shadow-copy-creation-process"></a>Processo di creazione della copia shadow

Un richiedente è l'applicazione che avvia la richiesta di creazione di una copia shadow. In genere, il richiedente è un'applicazione di backup. Se necessario, il servizio Copia Shadow del volume chiamerà i provider necessari. La maggior parte dei provider è interessata a tre richieste specifiche del richiedente.

1.  Il richiedente avvia l'attività di creazione copia shadow con una chiamata a [**IVssBackupComponents:: StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset). Viene generato un **GUID** di tipo **VSS \_ ID** che identifica in modo univoco il set di copie shadow specifico, ovvero SnapshotSetId. Il provider non è associato a questo passaggio, ma la SnapshotSetId viene utilizzata estensivamente in tutti i passaggi successivi.
2.  Per ogni volume che si desidera includere in questo set di copie shadow, il richiedente chiama [**IVssBackupComponents:: AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset). VSS determina quale provider verrà utilizzato per eseguire la copia shadow del volume.
    -   Più provider possono partecipare a un set di copie shadow. Se, ad esempio, il volume di sistema e un volume di dati fanno parte dello stesso set di copie shadow, il provider di sistema può fungere da provider di copia shadow per il volume di sistema, mentre un provider hardware può fungere da provider di copia shadow per il volume di dati. Entrambi i provider fanno parte dello stesso set di copie shadow e l'utente si aspetta la stessa coerenza temporizzata in entrambi i volumi.
    -   Per selezionare un provider hardware, il provider hardware deve essere in grado di supportare tutti i LUN che contribuiscono al volume specificato.
    -   A tutti i provider registrati viene data la possibilità di indicare il supporto per un determinato volume durante la creazione della copia shadow. Se più provider indicano il supporto, il servizio Copia Shadow del volume utilizzerà per impostazione predefinita i provider hardware, i provider software e infine il provider di sistema (se nessun altro provider indica il supporto per tale volume).
    -   Un richiedente può eseguire l'override di questo ordine predefinito indicando in modo esplicito il provider necessario per creare la copia shadow.
    -   Se sono presenti più provider hardware che supportano un determinato volume, non vi è alcuna garanzia sull'ordine in cui verranno chiamati i provider hardware.
3.  Dopo una o più chiamate a [**AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset), il richiedente può richiedere la creazione della copia shadow usando il metodo [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) . VSS usa quindi il sistema per creare la copia shadow. Il metodo **DoSnapshotSet** esegue questa operazione in modo asincrono e il richiedente può eseguire il polling o attendere il completamento del processo di creazione della copia shadow.

Questo diagramma illustra le interazioni tra il richiedente, il servizio VSS, il supporto del kernel VSS, gli eventuali writer VSS interessati ed eventuali provider hardware VSS. Per una descrizione dettagliata di queste interazioni, vedere [il processo di creazione della copia shadow](the-shadow-copy-creation-process.md) .

![interazioni tra richiedente, componenti di backup, writer e provider](images/vssimpl.png)

Al termine del processo di creazione della copia shadow, il richiedente può determinare se la creazione della copia shadow ha avuto esito positivo e, in caso contrario, determinare l'origine dell'errore.

L'intervallo di tempo tra il blocco e lo sblocco delle applicazioni writer deve essere ridotto a icona. Il provider deve avviare in modo asincrono tutte le operazioni di preparazione correlate alla copia shadow, ad esempio un provider hardware che usa Plex a partire dalla sincronizzazione, nel metodo [**IVssHardwareSnapshotProvider:: BeginPrepareSnapshot**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotprovider-beginpreparesnapshot) e quindi attendere i completamenti nel metodo [**IVssProviderCreateSnapshotSet:: EndPrepareSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-endpreparesnapshots) .

Sono presenti più finestre di limite di tempo che i provider devono seguire. Di conseguenza, i provider correttamente eseguiranno tutte le operazioni di elaborazione non necessarie prima di [**IVssProviderCreateSnapshotSet::P recommitsnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-precommitsnapshots) e dopo [**IVssProviderCreateSnapshotSet::P ostcommitsnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-postcommitsnapshots).

Il set di copie shadow viene corretto quando viene chiamato [**DoSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) . Non è possibile aggiungere volumi aggiuntivi in un secondo momento perché i volumi aggiuntivi non condividono lo stesso punto nel tempo.

È previsto un limite di 64 volumi nel set di copie shadow. Un volume specifico può essere mappato a un intero LUN, una parte di un LUN o parti di più lun. La maggior parte delle configurazioni avrà un volume per LUN, sebbene sia possibile un mapping arbitrario.

Non esiste alcun limite al numero di set di copie shadow o al numero di set di copie shadow di un volume originale. Un provider può definire limiti specifici o limitare dinamicamente in base alle risorse hardware disponibili.

### <a name="point-in-time-for-writerless-applications"></a>Temporizzazione per le applicazioni con Writer

VSS include un supporto speciale che definisce il punto nel tempo comune per tutti i volumi in un set di copie shadow. I provider hardware non devono direttamente interfacciarsi con queste tecnologie kernel, perché vengono richiamati come parte della normale elaborazione del commit della copia shadow. Tuttavia, è utile comprendere i meccanismi utilizzati perché spiega la definizione di "temporizzazione" per le applicazioni senza Writer (applicazioni che non hanno esposto un'interfaccia VSS Writer e pertanto non partecipano al processo di creazione della copia shadow del volume).

Questo supporto del kernel VSS per il punto nel tempo comune viene distribuito tra il driver VolSnap.sys, i file System e VSS.

1.  Prima che venga richiamato il supporto del kernel VSS, VSS ha già:
    1.  Determinare quali volumi devono essere interessati nella copia shadow.
    2.  Determinazione del provider da utilizzare per ogni volume.
    3.  Applicazioni bloccate che accettano messaggi di blocco/sblocco.
    4.  Preparare i provider per la copia shadow chiamando i metodi [**PreCommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-precommitsnapshots) . Tutti i provider sono ora in attesa di eseguire la creazione effettiva della copia shadow.
2.  Viene quindi creato il punto nel tempo. VSS Scarica contemporaneamente i file System in tutti i volumi di cui viene eseguita la copia shadow.
    1.  VSS emette un \_ comando IOCTL \_ VolSnap \_ per lo scaricamento e \_ \_ il controllo delle Scritture in ogni volume che Scarica i file System. Che IOCTL viene passato allo stack di archiviazione per VolSnap.sys. VolSnap.sys quindi include tutti i IRP di scrittura fino al passaggio 4 seguente. Qualsiasi file system (ad esempio RAW) senza supporto per questo nuovo comando IOCTL passa il comando IOCTL sconosciuto, dove viene nuovamente mantenuto da VolSnap.sys. Nei volumi NTFS viene eseguito il commit anche del log NTFS.
    2.  Questa operazione sospende tutte le attività dei metadati NTFS/FAT; il commit dei metadati del file system è stato eseguito in modo corretto.
    3.  Istante copia shadow: VolSnap.sys causa la coda di tutti i IRP di scrittura successivi in tutti i volumi che devono essere replicati.
    4.  VolSnap.sys attende il completamento di tutte le Scritture in sospeso sui volumi copiati Shadow. I volumi sono ora tranquilli per quanto riguarda le Scritture e sono stati tranquilli esattamente nello stesso momento in ogni volume. Non sono previste garanzie per le Scritture nelle sezioni con mapping utente o nelle scritture eseguite tra (a) e (b) nei file System che non implementano il IOCTL di scaricamento (ad esempio, RAW).
3.  VSS indica a ogni provider di eseguire la copia shadow chiamando il metodo [**IVssProviderCreateSnapshotSet:: CommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots) . I provider devono disporre di tutti i preparativi, in modo che si tratta di un'operazione rapida.

    Si noti che il sistema di I/O è insufficiente solo durante l'esecuzione di questi metodi [**CommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots) . Se un provider esegue una sincronizzazione dei LUN di origine e copia shadow, è necessario completare la sincronizzazione prima di restituire il metodo **CommitSnapshots** del provider. Non può essere eseguita in modo asincrono.

4.  Subito dopo la restituzione del metodo [**CommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots) dell'ultimo provider, VSS rilascia tutti i IRP di scrittura in sospeso (inclusi i IRP che bloccavano i file System al termine dei percorsi di commit) richiamando un altro oggetto IRP passato a VolSnap.sys.
5.  Se il processo di copia shadow ha avuto esito positivo, VSS Now:
    1.  Chiama [**PostCommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-postcommitsnapshots) per i provider necessari.
    2.  Chiama [**CVssWriter:: Onscongelate**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onthaw) per i writer necessari.
    3.  Informa il richiedente che il processo di copia shadow è stato completato.

[**PreCommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-precommitsnapshots), [**CommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots), [**PostCommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-postcommitsnapshots) sono tutti critici per il tempo. Tutte le I/O dalle applicazioni con Writer sono bloccate da **PreCommitSnapshots** a **PostCommitSnapshots**; eventuali ritardi influiscono sulla disponibilità dell'applicazione. Tutte le I/o di file, incluse le I/O dell'applicazione non writer, vengono sospese durante **CommitSnapshots**.

I provider devono completare tutto il lavoro critico per il tempo prima di tornare da [**EndPrepareSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-endpreparesnapshots).

-   [**CommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots) deve essere restituito entro pochi secondi. La fase **CommitSnapshots** si trova all'interno della finestra di svuotamento e di attesa. Il supporto del kernel VSS Annulla lo scaricamento e la conservazione che contiene l'i/O se la versione successiva non viene ricevuta entro 10 secondi e il processo di creazione della copia shadow non riuscirà. Altre attività verranno eseguite nel sistema, pertanto un provider non deve basarsi su un totale di 10 secondi. Il provider non deve chiamare le API Win32 durante il commit. il numero di Scritture e il blocco imprevisto. Se il provider richiede più di alcuni secondi per completare la chiamata, esiste una probabilità elevata che questa operazione avrà esito negativo.
-   La sequenza completa da [**PreCommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-precommitsnapshots) al ritorno di [**PostCommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-postcommitsnapshots) viene mappata alla finestra tra i writer che ricevono gli eventi di blocco e di sblocco. Il valore predefinito del writer per questa finestra è 60 secondi, ma un writer può eseguire l'override di questo valore con un timeout minore. Ad esempio, il writer di Microsoft Exchange Server imposta il timeout su 20 secondi. I provider non devono spendere più di un secondo o due in questo metodo.

Durante [**CommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots) il provider deve evitare i/O di file non di paging; tali I/O hanno una probabilità molto elevata di deadlock. In particolare, il provider non deve scrivere in modo sincrono alcun registro di traccia o di debug.

 

 



