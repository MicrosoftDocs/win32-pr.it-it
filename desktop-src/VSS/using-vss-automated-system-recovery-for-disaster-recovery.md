---
description: Un'applicazione di backup e ripristino VSS che esegue il ripristino di emergenza (detto anche ripristino bare metal) può utilizzare il writer di ripristino automatico del sistema (ASR) insieme a Ambiente preinstallazione di Windows (Windows PE) per eseguire il backup e il ripristino di volumi critici e di altri componenti dello stato del sistema di avvio. L'applicazione di backup viene implementata come richiedente VSS.
ms.assetid: 13adfd79-f26a-4385-9b59-129d06fa72eb
title: Uso del ripristino automatico del sistema VSS per il ripristino di emergenza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e31ef8ba223f40928e2422fa92240656f94592d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307181"
---
# <a name="using-vss-automated-system-recovery-for-disaster-recovery"></a>Uso del ripristino automatico del sistema VSS per il ripristino di emergenza

Un'applicazione di backup e ripristino VSS che esegue il ripristino di emergenza (detto anche ripristino bare metal) può utilizzare il writer di ripristino automatico del sistema (ASR) insieme a Ambiente preinstallazione di Windows (Windows PE) per eseguire il backup e il ripristino di volumi critici e di altri componenti dello stato del sistema di avvio. L'applicazione di backup viene implementata come richiedente VSS.

**Nota**  Per le applicazioni che usano ASR è necessario concedere in licenza Windows PE.

**Windows Server 2003 e Windows XP:** ASR non è implementato come VSS writer.

Per informazioni sugli strumenti di traccia che è possibile usare con ASR, vedere [uso degli strumenti di traccia con le applicazioni VSS ASR](using-tracing-tools-with-vss-asr-applications.md).

**Contenuto dell'articolo:**

-   [Panoramica delle attività della fase di backup](#overview-of-backup-phase-tasks)
-   [Scelta dei componenti critici di cui eseguire il backup](#choosing-which-critical-components-to-back-up)
-   [Panoramica delle attività della fase di ripristino](#overview-of-restore-phase-tasks)
-   [Esclusione di tutti i dischi per un volume](#excluding-all-disks-for-a-volume)

## <a name="overview-of-backup-phase-tasks"></a>Panoramica delle attività della fase di backup

Al momento del backup, il richiedente esegue i passaggi seguenti.

> [!Note]  
> Tutti i passaggi sono necessari se non diversamente specificato.

 

1.  Chiamare la funzione [**CreateVssBackupComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-createvssbackupcomponents) per creare un'istanza dell'interfaccia [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) e chiamare il metodo [**IVssBackupComponents:: InitializeForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforbackup) per inizializzare l'istanza di per la gestione di un backup.
2.  Chiamare [**IVssBackupComponents:: secontext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext) per impostare il contesto per l'operazione di copia shadow.
3.  Chiamare [**IVssBackupComponents:: SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate) per configurare il backup. Impostare il parametro *bBackupBootableSystemState* su **true** per indicare che il backup includerà uno stato del sistema di avvio.
4.  Scegliere i componenti critici nel documento di metadati del writer di ASR writer per eseguire il backup e chiamare [**IVssBackupComponents:: AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) per ognuno di essi.
5.  Chiamare [**IVssBackupComponents:: StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) per creare un nuovo set di copie shadow vuoto.
6.  Chiamare [**IVssBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) per avviare il contatto asincrono con i writer.
7.  Chiamare [**IVssBackupComponents:: GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata) per recuperare il documento di metadati writer del writer ASR. L'ID writer per il writer ASR è BE000CBE-11FE-4426-9C58-531AA6355FC4 e la stringa del nome writer è "ASR writer".
8.  Chiamare [**IVssExamineWriterMetadata:: saveasxml**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-saveasxml) per salvare una copia del documento di metadati del writer del writer ASR.
9.  Chiamare [**IVssBackupComponents:: AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset) per ogni volume che può partecipare alle copie shadow per aggiungere il volume al set di copie shadow.
10. Chiamare [**IVssBackupComponents::P repareforbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) per notificare ai writer la preparazione per un'operazione di backup.
11. Chiamare [**IVssBackupComponents:: GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) e [**IVssBackupComponents:: GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) (o [**IVssBackupComponentsEx3:: GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex3-getwriterstatusex)) per verificare lo stato del writer ASR.
12. A questo punto, è possibile eseguire una query per i messaggi di errore impostati dal writer nel metodo [**CVssWriter:: OnPrepareBackup**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpreparebackup) . Per un esempio di codice in cui viene illustrato come visualizzare questi messaggi, vedere [**IVssComponentEx:: GetPrepareForBackupFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponentex-getprepareforbackupfailuremsg).
13. Chiamare [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) per creare una copia shadow del volume.
14. Chiamare [**IVssBackupComponents:: GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) e [**IVssBackupComponents:: GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) per verificare lo stato del writer ASR.
15. Eseguire il backup dei dati.
16. Indica se l'operazione di backup ha avuto esito positivo chiamando [**IVssBackupComponents:: SetBackupSucceeded**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded).
17. Chiamare [**IVssBackupComponents:: BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) per indicare che l'operazione di backup è stata completata.
18. Chiamare [**IVssBackupComponents:: GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) e [**IVssBackupComponents:: GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus). La memoria dello stato della sessione del writer è una risorsa limitata e i writer devono riutilizzare gli Stati della sessione. Questo passaggio contrassegna lo stato della sessione di backup del writer come completato e notifica a VSS che questo slot della sessione di backup può essere riutilizzato da un'operazione di backup successiva.
    > [!Note]  
    > Questa operazione è necessaria solo in Windows Server 2008 con Service Pack 2 (SP2) e versioni precedenti.

     

19. Chiamare [**IVssBackupComponents:: saveasxml**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-saveasxml) per salvare una copia del documento dei componenti di backup del richiedente. Le informazioni nel documento componenti di backup vengono utilizzate in fase di ripristino quando il richiedente chiama il metodo [**IVssBackupComponents:: InitializeForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforrestore) .

## <a name="choosing-which-critical-components-to-back-up"></a>Scelta dei componenti critici di cui eseguire il backup

Nella fase di inizializzazione del backup, il writer ASR segnala i tipi di componenti seguenti nel documento di metadati del writer:

-   Volumi critici, ad esempio i volumi di avvio, di sistema e di ambiente ripristino Windows (Windows RE) e la partizione RE di Windows associata all'istanza di Windows Vista o Windows Server 2008 attualmente in esecuzione. Un volume è un *volume critico* se contiene informazioni sullo stato del sistema. I volumi di avvio e di sistema vengono inclusi automaticamente. Il richiedente deve includere tutti i volumi contenenti componenti critici del sistema segnalati da writer, ad esempio i volumi che contengono la Active Directory. I componenti critici del sistema sono contrassegnati come "non selezionabili per il backup". In VSS "non selezionabile" significa "non facoltativo". Pertanto, il richiedente deve eseguire il backup come parte dello stato del sistema. Per ulteriori informazioni, vedere [backup e ripristino dello stato del sistema](locating-additional-system-files.md). I componenti per i quali \_ \_ non è impostato il flag di stato del sistema VSS CF non \_ sono critici per il \_ sistema.
    > [!Note]  
    > Il componente ASR è un componente critico del sistema segnalato dal writer di ASR.

     

-   Dischi. Ogni disco fisso del computer viene esposto come componente in ASR. Se un disco non è stato escluso durante il backup, verrà assegnato durante il ripristino e potrà essere ricreato e formattato nuovamente. Si noti che durante il ripristino, il richiedente può comunque creare nuovamente un disco che è stato escluso durante il backup chiamando il metodo [**IVssBackupComponents:: SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) . Se si seleziona un disco in un pacchetto di disco dinamico, è necessario selezionare anche tutti gli altri dischi del pacchetto. Se viene selezionato un volume perché è un volume critico, ovvero un volume che contiene informazioni sullo stato del sistema, è necessario selezionare anche ogni disco che contiene un extent per tale volume. Per trovare gli extent per un volume, usare il codice IOCTL volume del volume del disco di controllo degli [**\_ \_ \_ \_ \_ extent**](/windows/win32/api/winioctl/ni-winioctl-ioctl_volume_get_volume_disk_extents) .

    > [!Note]  
    > Durante il backup, il richiedente deve includere tutti i dischi fissi. Se il disco che contiene il set di backup del richiedente è un disco locale, questo disco deve essere incluso. Durante il ripristino, il richiedente deve escludere il disco che contiene il set di backup del richiedente per impedirne la sovrascrittura.

     

    In un ambiente di clustering, ASR non ricrea il layout dei dischi condivisi del cluster. I dischi devono essere ripristinati online dopo il ripristino del sistema operativo nel ripristino di Windows.

-   Archivio dati configurazione di avvio (BCD). Questo componente specifica il percorso della directory che contiene l'archivio BCD. Il richiedente deve specificare questo componente ed eseguire il backup di tutti i file nella directory dell'archivio BCD. Per ulteriori informazioni sull'archivio BCD, vedere [About BCD](/previous-versions/windows/desktop/bcd/about-bcd).
    > [!Note]  
    > Nei computer che utilizzano l'interfaccia EFI (Extended Firmware Interface), la partizione di sistema EFI (ESP) è sempre nascosta e non può essere inclusa in una copia shadow del volume. Il richiedente deve eseguire il backup del contenuto di questa partizione. Poiché questa partizione non può essere inclusa in una copia shadow del volume, il backup può essere eseguito solo dal volume Live, non dalla copia shadow. Per ulteriori informazioni su EFI e ESP, vedere [la](/windows-hardware/drivers/bringup/)pagina relativa alla guida.

I nomi dei componenti utilizzano i formati seguenti:

-   Per i componenti del disco, il formato è

    <COMPONENT logicalPath="Disks" componentName="harddisk*n*" componentType="filegroup" />

    dove *n* è il numero del disco. Viene registrato solo il numero del disco. Per ottenere il numero del disco, usare il codice di controllo del [**\_ numero di dispositivo IOCTL storage \_ get \_ \_**](/windows/win32/api/winioctl/ni-winioctl-ioctl_storage_get_device_number) .

-   Per i componenti del volume, il formato è

    <COMPONENT logicalPath="Volumes" componentName="Volume{*GUID*}" componentType="filegroup" />

    dove *GUID* è il GUID del volume.

-   Per il componente archivio BCD, il formato è

    <COMPONENT logicalPath="BCD" componentName="BCD" componentType="filegroup" componentCaption = "This is the path to the boot BCD store and the boot managers...All the files in this directory need to be backed up...">

    Se la partizione di sistema ha un nome di GUID del volume, questo componente è selezionabile. In caso contrario, non è selezionabile.

    > [!Note]  
    > ASR aggiunge i file al gruppo di file del componente archivio BCD come indicato di seguito:
    >
    > -   Per i dischi EFI, ASR aggiunge
    >
    >     *SystemPartitionPath* \\ \\Avvio Microsoft \\ EFI \\ \* .\*
    >
    >     dove *SystemPartitionPath* è il percorso della partizione di sistema.
    >
    > -   Per i dischi GPT, ASR aggiunge
    >
    >     *SystemPartitionPath* \\ Eseguire l'avvio \\ \* .\*
    >
    >     dove *SystemPartitionPath* è il percorso della partizione di sistema.
    >
    > -   Il percorso della partizione di sistema si trova nella seguente chiave del registro di sistema: **HKEY \_ Local \_ computer** \\ **System** \\ **Setup** \\ **SYSTEMPARTITION**

     

Durante il ripristino, è necessario ripristinare tutti i componenti contrassegnati come volumi critici. Se non è possibile ripristinare uno o più volumi critici, l'operazione di ripristino avrà esito negativo.

Nella fase di [**preripristino**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) della sequenza di ripristino i dischi che non sono stati esclusi durante il backup vengono creati nuovamente e riformattati per impostazione predefinita. Tuttavia, non vengono ricreate o riformattate se soddisfano le condizioni seguenti:

-   Un disco di base non viene ricreato se il layout del disco è intatto o se sono state apportate modifiche aggiuntive. Il layout del disco è intatto se vengono soddisfatte le condizioni seguenti:
    -   La firma del disco, lo stile del disco (GPT o MBR), le dimensioni del settore logico e l'offset iniziale del volume non vengono modificati.
    -   La dimensione del volume non viene ridotta.
    -   Per i dischi GPT, l'identificatore di partizione non viene modificato.
-   Se il layout del disco è intatto o se sono state apportate modifiche aggiuntive, un disco dinamico non viene ricreato. Affinché un disco dinamico sia intatto, è necessario che siano soddisfatte tutte le condizioni per un disco di base. Inoltre, l'intera struttura del volume del pacchetto del disco deve essere intatta. La struttura del volume del pacchetto del disco è intatta se soddisfa le condizioni seguenti, che si applicano ai dischi MBR e GPT:
    -   Il numero di volumi disponibili nel pacchetto fisico durante il ripristino deve essere maggiore o uguale al numero di volumi specificati nei metadati del writer ASR durante il backup.
    -   Il numero di [*Plex*](../vds/virtual-disk-service-glossary-all.md) per volume deve essere invariato.
    -   Il numero di [*membri*](../vds/virtual-disk-service-glossary-all.md) deve essere invariato.
    -   Il numero di extent del disco fisico deve essere maggiore del numero di extent del disco specificati nei metadati del writer ASR.
    -   Un pacchetto intatto rimane intatto quando vengono aggiunti volumi aggiuntivi o se un volume nel pacchetto viene esteso, ad esempio da un volume semplice a un volume con spanning.
        > [!Note]  
        > Se viene eseguito il mirroring di un volume semplice, il pacchetto non è intatto e verrà ricreato per garantire che il BCD e lo stato del volume di avvio rimangano coerenti dopo il ripristino. Se i volumi vengono eliminati, il pacchetto viene ricreato.

         
-   Se la struttura del volume del pacchetto del disco dinamico è intatta ed è stata apportata solo una modifica aggiuntiva, i dischi nel pacchetto non vengono ricreati.

    **Windows Vista:** I dischi dinamici vengono sempre ricreati. Si noti che questo comportamento è stato modificato con Windows Server 2008 e Windows Vista con Service Pack 1 (SP1).

In qualsiasi momento prima dell'inizio della fase di ripristino, il richiedente può specificare che i dischi devono essere formattati in modo rapido impostando la chiave del registro di sistema **HKEY \_ Local \_ Machine** \\ **software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **ASR** \\ **RestoreSession** . In questa chiave è presente un valore denominato **QuickFormat** con il tipo di dati reg \_ DWORD. Se questo valore non esiste, è necessario crearlo. Impostare i dati del valore **QuickFormat** su 1 per la formattazione rapida oppure su 0 per la formattazione lenta.

Se il valore **QuickFormat** non esiste, i dischi verranno formattati lentamente.

La formattazione rapida è notevolmente più veloce rispetto alla formattazione lenta (detta anche formattazione completa). Tuttavia, la formattazione rapida non verifica ogni settore nel volume.

## <a name="overview-of-restore-phase-tasks"></a>Panoramica delle attività della fase di ripristino

Al momento del ripristino, il richiedente esegue i passaggi seguenti:

> [!Note]  
> Tutti i passaggi sono necessari se non diversamente specificato.

 

1.  Chiamare la funzione [**CreateVssBackupComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-createvssbackupcomponents) per creare un'istanza dell'interfaccia [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) e chiamare il metodo [**IVssBackupComponents:: InitializeForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforrestore) per inizializzare l'istanza per il ripristino caricando il documento relativo ai componenti di backup del richiedente nell'istanza di.
2.  \[Questo passaggio è necessario solo se il richiedente deve modificare se è specificato "IncludeDisk" o "ExcludeDisk" per uno o più dischi. \] Chiamare [**IVssBackupComponents:: SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) per impostare le opzioni di ripristino per i componenti del writer ASR. Il writer di ASR supporta le opzioni seguenti: "IncludeDisk" consente al richiedente di includere un disco nel sistema di destinazione da considerare per il ripristino, anche se non è stato selezionato durante la fase di backup. "ExcludeDisk" consente al richiedente di impedire la nuova creazione di un disco nel sistema di destinazione. Si noti che se si specifica "ExcludeDisk" per un disco che contiene un volume critico, la chiamata successiva a [**IVssBackupComponents::P il ripristino**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) avrà esito negativo.

    Nell'esempio seguente viene illustrato come utilizzare [**SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) per impedire la ricreazione del disco 0 e del disco 1 e l'inserimento di driver di terze parti nel volume di avvio ripristinato.

    **Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** L'inserimento di driver di terze parti non è supportato.

    Nell'esempio si presuppone che il puntatore [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) , m \_ pBackupComponents, sia valido.

    ```C++
        m_pBackupComponents->SetRestoreOptions(
            AsrWriterId,
            VSS_CT_FILEGROUP,
            NULL,
            TEXT("ASR"),
            TEXT("\"ExcludeDisk\"=\"0\", \"ExcludeDisk\"=\"1\" "),
            TEXT("\"InjectDrivers\"=\"1\" ")
            );
    ```

    

    Per escludere tutti i dischi per un volume specificato, vedere gli argomenti seguenti "esclusione di tutti i dischi per un volume".

3.  Chiamare [**IVssBackupComponents::P Rerestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) per notificare al writer di ASR di prepararsi per un'operazione di ripristino. Chiamare [**IVssAsync:: QueryStatus**](/windows/desktop/api/Vss/nf-vss-ivssasync-querystatus) il numero di volte necessario fino a quando il valore di stato restituito nel parametro *pHrResult* non è un oggetto asincrono di VSS in \_ \_ \_ sospeso.
4.  Ripristinare i dati. Nella fase di ripristino, ASR riconfigura il percorso GUID del volume ( \\ \\ ? \\ Volume {GUID}) per ogni volume in modo che corrisponda al percorso GUID del volume utilizzato durante la fase di backup. Tuttavia, le lettere di unità non vengono mantenute, perché ciò provocherebbe conflitti con le lettere di unità assegnate automaticamente nell'ambiente di ripristino. Pertanto, quando si ripristinano i dati, il richiedente deve usare i percorsi GUID del volume, non le lettere di unità, per accedere ai volumi.
5.  Impostare la  \\  \\ chiave del registro di sistema HKLM Software **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **ASR** \\ **RestoreSession** per indicare il set di volumi che sono stati ripristinati o riformattati.

    In questa chiave è presente un valore denominato **RestoredVolumes** con il tipo di dati reg \_ \_ multisz. Se questo valore non esiste, è necessario crearlo. Con questo valore, il richiedente deve creare una voce del GUID del volume per ogni volume che è stato ripristinato. Il formato di questa voce deve essere il seguente: \\ \\ ? \\ Volume {78618c8f-aefd-11da-a898-806e6f6e6963}. Ogni volta che viene eseguito un ripristino bare metal, ASR imposta il valore **RestoredVolumes** sul set di volumi ripristinati da ASR. Se il richiedente ha ripristinato volumi aggiuntivi, deve impostare questo valore sull'Unione del set di volumi che il richiedente ha ripristinato e il set di volumi ripristinati da ASR. Se il richiedente non ha usato ASR, deve sostituire l'elenco di volumi.

    È inoltre necessario creare un valore denominato **LastInstance** con il tipo di dati reg \_ SZ. Questa chiave deve contenere un cookie casuale che identifica in modo univoco l'operazione di ripristino corrente. Un cookie di questo tipo può essere creato usando le funzioni [**UuidCreate**](/windows/win32/api/rpcdce/nf-rpcdce-uuidcreate) e [**UuidToString**](/windows/win32/api/rpcdce/nf-rpcdce-uuidtostring) . Ogni volta che viene eseguito un ripristino bare metal, ASR Reimposta questo valore del registro di sistema per notificare ai richiedenti e alle applicazioni di backup non VSS che si è verificato il ripristino.

6.  Chiamare [**IVssBackupComponents::P ostrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore) per indicare la fine dell'operazione di ripristino. Chiamare [**IVssAsync:: QueryStatus**](/windows/desktop/api/Vss/nf-vss-ivssasync-querystatus) il numero di volte necessario fino a quando il valore di stato restituito nel parametro *pHrResult* non è un oggetto asincrono di VSS in \_ \_ \_ sospeso.

Nella fase di ripristino, ASR può creare o rimuovere partizioni per ripristinare lo stato precedente del computer. I richiedenti non devono tentare di eseguire il mapping dei numeri di disco dalla fase di backup alla fase di ripristino.

Durante il ripristino, il richiedente deve escludere il disco che contiene il set di backup del richiedente. In caso contrario, il set di backup può essere sovrascritto dall'operazione di ripristino.

Durante il ripristino, un disco viene escluso se non è stato selezionato come componente durante il backup o se è esplicitamente escluso chiamando [**IVssBackupComponents:: SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) con l'opzione "ExcludeDisk" durante il ripristino.

È importante tenere presente che durante il ripristino di emergenza di WinPE è presente la funzionalità del writer ASR, ma non sono disponibili altri writer e il servizio VSS non è in esecuzione. Al termine del ripristino di emergenza di WinPE, il computer è stato riavviato e il sistema operativo Windows è in esecuzione normalmente, il servizio VSS può essere avviato e il richiedente può eseguire qualsiasi operazione di ripristino aggiuntiva che richiede la partecipazione di writer diversi dal writer di ASR.

Se durante la sessione di ripristino l'applicazione di backup rileva che gli ID univoci del volume rimangono invariati e pertanto tutti i volumi dal momento del backup sono presenti e intatti in WinPE, l'applicazione di backup può continuare a ripristinare solo il contenuto dei volumi, senza coinvolgere ASR. In questo caso, l'applicazione di backup deve indicare che il computer è stato ripristinato impostando la seguente chiave del registro di sistema nel sistema operativo ripristinato: **HKEY \_ Local \_ Machine** \\ **software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **ASR** \\ **RestoreSession**

In questa chiave specificare **LastInstance** per il nome del valore, reg \_ SZ per il tipo di valore e un cookie casuale, ad esempio un GUID creato dalla funzione [**UuidCreate**](/windows/win32/api/rpcdce/nf-rpcdce-uuidcreate) , per i dati del valore.

Se durante la sessione di ripristino l'applicazione di backup rileva che uno o più volumi sono stati modificati o mancanti, l'applicazione di backup deve usare ASR per eseguire il ripristino. ASR ricreerà i volumi esattamente come si trovavano al momento del backup e imposterà la chiave del registro di sistema **RestoreSession** .

## <a name="excluding-all-disks-for-a-volume"></a>Esclusione di tutti i dischi per un volume

Nell'esempio seguente viene illustrato come escludere tutti i dischi per un volume specificato.


```C++
HRESULT BuildRestoreOptionString
(
    const WCHAR             *pwszVolumeNamePath,
    CMyString               *pstrExclusionList
)
{
    HANDLE                  hVolume           = INVALID_HANDLE_VALUE;
    DWORD                   cbSize            = 0;
    VOLUME_DISK_EXTENTS     * pExtents        = NULL;
    DISK_EXTENT             * pExtent         = NULL;
    ULONG                   i                 = 0;
    BOOL                    fIoRet            = FALSE;
    WCHAR                   wszDest[MAX_PATH] = L"";
    CMyString               strVolumeName;
    CMyString               strRestoreOption;

    // Open a handle to the volume device.
    strVolumeName.Set( pwszVolumeNamePath );
    // If the volume name contains a trailing backslash, remove it.
    strVolumeName.UnTrailing( L'\\' );
    hVolume = ::CreateFile(strVolumeName, 0, FILE_SHARE_READ | FILE_SHARE_WRITE, NULL, OPEN_EXISTING, NULL, 0);
    // Check whether the call to CreateFile succeeded.

    // Get the list of disks used by this volume.
    cbSize = sizeof(VOLUME_DISK_EXTENTS);
    pExtents = (VOLUME_DISK_EXTENTS *)::CoTaskMemAlloc(cbSize);

    ::ZeroMemory(pExtents, cbSize);

    fIoRet = ::DeviceIoControl(hVolume, IOCTL_VOLUME_GET_VOLUME_DISK_EXTENTS, NULL, 0, pExtents, cbSize, &cbSize, 0);
    if ( !fIoRet && GetLastError() == ERROR_MORE_DATA )
    {
        // Allocate more memory.
        cbSize = FIELD_OFFSET(VOLUME_DISK_EXTENTS, Extents) + pExtents->NumberOfDiskExtents * sizeof(DISK_EXTENT);
        ::CoTaskMemFree(pExtents);
        pExtents = NULL;

        pExtents = (VOLUME_DISK_EXTENTS *) ::CoTaskMemAlloc(cbSize);
        // Check whether CoTaskMemAlloc returned an out-of-memory error.
        ::ZeroMemory(pExtents, cbSize);

        // Now the buffer should be big enough.
        ::DeviceIoControl(hVolume, IOCTL_VOLUME_GET_VOLUME_DISK_EXTENTS, NULL, 0, pExtents, cbSize, &cbSize, 0);
        // Check whether the IOCTL succeeded.
    }
    // Check for errors; note that the IOCTL can fail for a reason other than insufficient memory.

    // For each disk, mark it to be excluded in the Restore Option string.
    for (i = 0; i < pExtents->NumberOfDiskExtents; i++)
    {
        pExtent = &pExtents->Extents[i];

        *wszDest = L'\0';
        StringCchPrintf(wszDest, MAX_PATH, L"\"ExcludeDisk\"=\"%d\", ", pExtent->DiskNumber); // check errors

        strRestoreOption.Append(wszDest);
        // Check for an out-of-memory error.
    }

    // Remove the trailing comma.
    strRestoreOption.TrimRight();
    strRestoreOption.UnTrailing(',');

    // Set the output parameter.
    strRestoreOption.Transfer( pstrExclusionList );

Exit:
    if( pExtents )
    {
        ::CoTaskMemFree(pExtents);
        pExtents = NULL;
    }

    if( hVolume != INVALID_HANDLE_VALUE )
    {
        ::CloseHandle(hVolume);
        hVolume = INVALID_HANDLE_VALUE;
    }

    return ( hr );
}

```



 

 
