---
description: Creazione della copia shadow per i provider
ms.assetid: d5042945-ba81-40d0-b204-1f08d153a788
title: Creazione della copia shadow per i provider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 953f9b5556b8cf0a35117d8df6756fdd52bdf033d390f0b08a7e018d1eaf5410
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118121849"
---
# <a name="shadow-copy-creation-for-providers"></a>Creazione della copia shadow per i provider

## <a name="the-shadow-copy-creation-process"></a>Processo di creazione della copia shadow

Un richiedente è l'applicazione che avvia la richiesta di creazione di una copia shadow. In genere il richiedente è un'applicazione di backup. Se necessario, vss chiamerà i provider coinvolti. La maggior parte dei provider è interessata a tre richieste specifiche dal richiedente.

1.  Il richiedente avvia l'attività di creazione della copia shadow con una chiamata a [**IVssBackupComponents::StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset). Viene generato un **GUID di** tipo **\_ VSS ID che** identifica in modo univoco questo set di copie shadow specifico, SnapshotSetId. Il provider non è coinvolto in questo passaggio, ma SnapshotSetId viene usato ampiamente in tutti i passaggi successivi.
2.  Per ogni volume da includere in questo set di copie shadow, il richiedente chiama [**IVssBackupComponents::AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset). VSS determina quale provider verrà usato per eseguire la copia shadow del volume.
    -   Più provider possono partecipare a un set di copie shadow. Ad esempio, se il volume di sistema e un volume di dati fanno parte dello stesso set di copie shadow, il provider di sistema può fungere da provider di copie shadow per il volume di sistema, mentre un provider di hardware può fungere da provider di copie shadow per il volume di dati. Entrambi i provider fanno parte dello stesso set di copie shadow e l'utente si aspetta la stessa coerenza tempormente in entrambi i volumi.
    -   Per poter selezionare un provider hardware, il provider di hardware deve essere in grado di supportare tutti i LUN che contribuiscono al volume specificato.
    -   Tutti i provider registrati hanno la possibilità di indicare il supporto per un determinato volume durante la creazione della copia shadow. Se più provider indicano il supporto, il Servizio Copia Copia Inventario software per impostazione predefinita verrà utilizzato per impostazione predefinita per i provider hardware, quindi per i provider di software e infine per il provider di sistema (se nessun altro provider indica il supporto per tale volume).
    -   Un richiedente può eseguire l'override di questo ordine predefinito indicando in modo esplicito il provider necessario per creare la copia shadow.
    -   Se sono presenti più provider di hardware che supportano un determinato volume, non è garantito l'ordine in cui verranno chiamati i provider hardware.
3.  Dopo una o più chiamate ad [**AddToSnapshotSet,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset)il richiedente può richiedere la creazione della copia shadow usando il metodo [**IVssBackupComponents::D oSnapshotSet.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) VSS funziona quindi con il sistema per creare la copia shadow. Il **metodo DoSnapshotSet** esegue questa operazione in modo asincrono e il richiedente può eseguire il polling o attendere il completamento del processo di creazione della copia shadow.

Questo diagramma mostra le interazioni tra il richiedente, il servizio VSS, il supporto del kernel VSS, tutti i vss writer coinvolti ed eventuali provider di hardware VSS. Per [una descrizione dettagliata di queste](the-shadow-copy-creation-process.md) interazioni, vedere Processo di creazione della copia shadow.

![interazioni tra richiedente, componenti di backup, writer e provider](images/vssimpl.png)

Al termine del processo di creazione della copia shadow, il richiedente può determinare se la creazione della copia shadow ha avuto esito positivo e, in caso contrario, determinare l'origine dell'errore.

L'intervallo di tempo tra il blocco e lo s thaw delle applicazioni writer deve essere ridotto al minimo. Il provider deve avviare in modo asincrono tutte le operazioni di preparazione correlate alla copia shadow, ad esempio un provider hardware che usa plex che avviano la sincronizzazione, nel metodo [**IVssHardwareSnapshotProvider::BeginPrepareSnapshot**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotprovider-beginpreparesnapshot) e quindi attendere i completamenti nel metodo [**IVssProviderCreateSnapshotSet::EndPrepareSnapshots.**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-endpreparesnapshots)

Esistono più intervalli di tempo che i provider devono seguire. Di conseguenza, i provider ben comportati eseguiranno tutte le elaborazioni non necessarie prima di [**IVssProviderCreateSnapshotSet::P reCommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-precommitsnapshots) e dopo [**IVssProviderCreateSnapshotSet::P ostCommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-postcommitsnapshots).

Il set di copie shadow è fisso quando [**viene chiamato DoSnapshotSet.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) Non è possibile aggiungere volumi aggiuntivi in un secondo momento perché i volumi aggiuntivi non condividono lo stesso punto nel tempo.

È previsto un limite di 64 volumi nel set di copie shadow. Un volume specifico può essere mappato a un intero LUN, a una parte di un LUN o a parti di più LUN. La maggior parte delle configurazioni avrà un volume per LUN, anche se sono possibili mapping arbitrari.

Non esiste alcun limite al numero di set di copie shadow o al numero di set di copie shadow di un volume originale. Un provider può definire limiti specifici o limitare dinamicamente in base alle risorse hardware disponibili.

### <a name="point-in-time-for-writerless-applications"></a>Tempor per le applicazioni senza scrittura

Il Servizio Copia Shadow del volume include un supporto speciale che definisce il punto nel tempo comune per tutti i volumi in un set di copie shadow. I provider hardware non devono interfacciarsi direttamente con queste tecnologie del kernel, perché vengono richiamati come parte della normale elaborazione del commit della copia shadow. Tuttavia, è utile comprendere i meccanismi usati perché illustra la definizione di "temporizzazione" per le applicazioni senza writer (applicazioni che non hanno esposto un'interfaccia VSS Writer e pertanto non partecipano al processo di creazione della copia shadow del volume).

Questo supporto del kernel VSS per il punto nel tempo comune viene distribuito tra il driver VolSnap.sys, i file system e vss.

1.  Prima che venga richiamato il supporto del kernel vss, vss ha già:
    1.  Determinare quali volumi devono essere coinvolti nella copia shadow.
    2.  Determinare il provider da usare in ogni volume.
    3.  Applicazioni bloccate che accettano messaggi di blocco/disagi.
    4.  Preparare i provider per la copia shadow chiamando i [**metodi PreCommitSnapshots.**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-precommitsnapshots) Tutti i provider sono ora in attesa di eseguire la creazione effettiva della copia shadow.
2.  Viene quindi creato il punto nel tempo. VsS scarica contemporaneamente i file system in tutti i volumi di cui eseguire la copia shadow.
    1.  VSS esempe un comando di controllo \_ IOCTL VOLSNAP FLUSH AND HOLD WRITES in ogni \_ volume che scarica i \_ file \_ \_ system. Tale IOCTL viene passato verso il basso nello stack di archiviazione per VolSnap.sys. VolSnap.sys quindi tutti gli ISP di scrittura fino al passaggio 4 riportato di seguito. Qualsiasi file system (ad esempio RAW) senza supporto per questo nuovo IOCTL passa l'IOCTL sconosciuto verso il basso, dove viene nuovamente mantenuto da VolSnap.sys. Nei volumi NTFS, lo scaricamento esegue anche il commit del log NTFS.
    2.  In questo modo vengono sospese tutte le attività dei metadati NTFS/FAT. viene eseguito file system commit dei metadati.
    3.  L'istante della copia shadow: VolSnap.sys tutti gli IRP di scrittura successivi vengono accodati in tutti i volumi di cui eseguire la copia shadow.
    4.  VolSnap.sys attesa del completamento di tutte le scritture in sospeso nei volumi copiati shadow. I volumi sono ora inesacienti per quanto riguarda le scritture e sono stati in stato di inesaserenza esattamente nello stesso momento in ogni volume. Non sono garantite operazioni di scrittura in sezioni mappate dall'utente o scritture rilasciate tra (a) e (b) nei file system che non implementano lo scaricamento IOCTL (ad esempio RAW).
3.  VSS indica a ogni provider di eseguire la copia shadow chiamando i metodi [**IVssProviderCreateSnapshotSet::CommitSnapshots.**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots) I provider devono avere tutte le operazioni di preparazione eseguite in modo che si tratta di un'operazione rapida.

    Si noti che il sistema di I/O è in stato inesatto solo durante l'esecuzione di questi metodi [**CommitSnapshots.**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots) Se un provider esegue una sincronizzazione dei LUN di origine e copia shadow, questa sincronizzazione deve essere completata prima che il metodo **CommitSnapshots** del provider restituisca un risultato. Non può essere eseguita in modo asincrono.

4.  Immediatamente dopo la fine del metodo [**CommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots) dell'ultimo provider, vss rilascia tutti gli IRP di scrittura in sospeso (inclusi gli IRP che bloccavano i file system al termine dei percorsi di commit) richiamando un altro IRP passato a VolSnap.sys.
5.  Se il processo di copia shadow ha avuto esito positivo, il Servizio Copia Shadow del volume ora:
    1.  Chiama [**PostCommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-postcommitsnapshots) per i provider coinvolti.
    2.  Chiama [**CVssWriter::OnThaw**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onthaw) per gli autori coinvolti.
    3.  Informa il richiedente che il processo di copia shadow è stato completato.

[**PreCommitSnapshots,**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-precommitsnapshots) [**CommitSnapshots,**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots)to [**PostCommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-postcommitsnapshots) sono tutti time critical. Tutte le operazioni di I/O dalle applicazioni con writer vengono bloccate da **PreCommitSnapshots** a **PostCommitSnapshots**; eventuali ritardi influiscono sulla disponibilità dell'applicazione. Tutti gli I/O di file, incluso l'I/O dell'applicazione senza writer, vengono sospesi **durante CommitSnapshots**.

I provider devono completare tutte le operazioni critiche prima di restituire [**da EndPrepareSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-endpreparesnapshots).

-   [**CommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots) deve essere restituito entro pochi secondi. La **fase CommitSnapshots** si trova all'interno della finestra Scarica e tieni premuto. Il supporto del kernel VSS annulla lo scaricamento e il blocco che contiene l'I/O se la versione successiva non viene ricevuta entro 10 secondi e il Servizio Copia Shadow del volume non riuscirà a completare il processo di creazione della copia shadow. Altre attività verranno svolte nel sistema, quindi un provider non deve basarsi sull'intera 10 secondi. Il provider non deve chiamare le API Win32 durante il commit, perché molte di queste comporteranno scritture e blocchi imprevisti. Se il provider impiega più di pochi secondi per completare la chiamata, esiste una probabilità elevata che questa operazione non riesca.
-   La sequenza completa da [**PreCommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-precommitsnapshots) alla restituzione di [**PostCommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-postcommitsnapshots) viene mappata alla finestra tra i writer che ricevono gli eventi Freeze e Thaw. Il valore predefinito del writer per questa finestra è 60 secondi, ma un writer può eseguire l'override di questo valore con un timeout inferiore. Il writer di Microsoft Exchange Server, ad esempio, imposta il timeout su 20 secondi. I provider non devono impiegare più di un secondo o due in questo metodo.

Durante [**CommitSnapshot il**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots) provider deve evitare qualsiasi I/O di file non di paging. Tale I/O ha una probabilità molto elevata di deadlock. In particolare, il provider non deve scrivere in modo sincrono alcun log di debug o di traccia.

 

 



