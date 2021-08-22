---
description: Questo argomento illustra l'effetto dei dispositivi di archiviazione in formato avanzato sul software, illustra le operazioni che le applicazioni possono eseguire per supportare questo tipo di supporti e illustra l'infrastruttura introdotta da Microsoft con Windows 7 SP1 e Windows Server 2008 R2 SP1 per consentire agli sviluppatori di supportare questi tipi di dispositivi.
ms.assetid: 1D2847A7-15E9-42E0-90EB-7F43E76D3E44
title: Aggiornamento della compatibilità dei dischi 512e (512-byte Emulation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fd26cfe1b5417af75906431291a51650757c08464f0c1dc6966ef7f58223423
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134179"
---
# <a name="512-byte-emulation-512e-disk-compatibility-update"></a>Aggiornamento della compatibilità dei dischi 512e (512-byte Emulation)

## <a name="platform"></a>Piattaforma

 **Client** - Windows Vista, Windows 7, Windows 7 SP1  
**Server** - Windows Server 2008, Windows Server 2008 R2, Windows Server 2008 R2 SP1  

## <a name="feature-impact"></a>Impatto sulle funzionalità

**Gravità** - Alta  
**Frequenza** - Alta  









## <a name="description"></a>Descrizione

Le densità areali aumentano ogni anno e con l'avvento recente di dischi da 3 TB, i meccanismi di correzione degli errori usati per gestire la riduzione del rapporto segnale-rumore (SNR) stanno diventando inefficienti a livello di spazio, ovvero è necessario un aumento del sovraccarico per garantire che il supporto sia utilizzabile. Una delle soluzioni del settore dell'archiviazione per migliorare questo meccanismo di correzione degli errori è l'introduzione di un formato multimediale fisico diverso che includa dimensioni di settore fisico maggiori. Questo nuovo formato multimediale fisico è denominato *Formato avanzato.* Pertanto, non è più sicuro fare ipotesi relative alle dimensioni del settore dei dispositivi di archiviazione moderni e gli sviluppatori dovranno studiare i presupposti sottostanti al codice per determinare se c'è un impatto.

In questo argomento viene illustrato l'effetto dei dispositivi di archiviazione in formato avanzato sul software, vengono illustrate le operazioni che le applicazioni possono eseguire per supportare questo tipo di supporti e viene illustrata l'infrastruttura per consentire agli sviluppatori di supportare questi tipi di dispositivi. Anche se il materiale presentato in questo argomento fornisce linee guida per migliorare la compatibilità con i dischi in formato avanzato, le informazioni si applicano in genere a tutti i sistemi con dischi in formato avanzato. Le versioni seguenti di Windows il supporto per l'esecuzione di query sulla dimensione del settore fisico:

-   Windows 7 con Microsoft KB 982018
-   Windows 7 SP1
-   Windows Server 2008 R2 con Microsoft KB 982018
-   Windows Server 2008 R2 SP1
-   Windows Vista con Microsoft KB 2553708
-   Windows Server 2008 con Microsoft KB 2553708

Per altri dettagli, vedere [Informazioni sui criteri di supporto Microsoft per le unità di settore di grandi dimensioni in Windows](https://support.microsoft.com/kb/2510009).

Per altre informazioni sui dischi in formato avanzato, contattare il fornitore dell'archiviazione.

## <a name="logical-vs-physical-sector-size"></a>Dimensioni del settore logico e fisico

Uno dei problemi dell'introduzione di questa modifica nel formato multimediale è la compatibilità con il software e l'hardware attualmente disponibili sul mercato. Come soluzione temporanea, il settore dell'archiviazione sta introducendo inizialmente dischi che emulano un normale disco di settore da 512 byte, ma rendono disponibili informazioni sulle dimensioni del settore reale tramite i comandi standard ATA e SCSI. In seguito a questa emulazione, esistono due dimensioni di settore:

-   **Logical Sector:** unità usata per l'indirizzamento logico dei blocchi per il supporto. È anche possibile pensare a questo come all'unità di scrittura più piccola che l'archiviazione può accettare. Questa è l'emulazione.

-   **Settore fisico:** unità per cui le operazioni di lettura e scrittura nel dispositivo vengono completate in un'unica operazione. Questa è l'unità di scrittura atomica.

La maggior parte delle API Windows correnti, ad esempio **IOCTL \_ DISK GET \_ DRIVE \_ \_ GEOMETRY** restituirà le dimensioni del settore logico, ma le dimensioni del settore fisico possono essere recuperate tramite il codice di controllo [IOCTL \_ STORAGE QUERY \_ \_ PROPERTY,](/windows-hardware/drivers/ddi/content/ntddstor/ni-ntddstor-ioctl_storage_query_property) con le informazioni rilevanti contenute nel campo **BytesPerPhysicalSector** nella struttura [ \_ \_ \_ DESCRIPTOR STORAGE ACCESS ALIGNMENT.](/windows/desktop/api/winioctl/ns-winioctl-storage_access_alignment_descriptor) Questo argomento viene illustrato in modo più dettagliato più avanti nell'articolo.

## <a name="initial-types-of-large-sector-media"></a>Tipi iniziali di supporti per settori di grandi dimensioni

Il settore dell'archiviazione sta rapidamente cercando di passare a questo nuovo tipo di formato avanzato di archiviazione per supporti con dimensioni di settore fisico di 4 KB. Due tipi di supporti verranno rilasciati sul mercato:

-   **4 KB nativo:** questo supporto non ha un livello di emulazione ed espone direttamente 4 KB come dimensione di settore logico e fisico. Questo supporto non è attualmente supportato da Windows e dalla maggior parte degli altri sistemi operativi. Tuttavia, Microsoft sta svolgendo un'indagine sulla fattibilità del supporto di questo tipo di supporti in una versione futura di Windows e riemettere un articolo Knowledge Base quando appropriato.
-   Emulazione a **512 byte (512e):** questo supporto ha un livello di emulazione come illustrato nella sezione precedente ed espone 512 byte come dimensione di settore logica (simile a un disco normale attualmente), ma rende disponibili le informazioni sulle dimensioni del settore fisico (4 KB). Questo è ciò che diversi fornitori di risorse di archiviazione stanno introducendo sul mercato. Questo problema generale con questo nuovo tipo di supporto è che la maggior parte delle applicazioni e dei sistemi operativi non è in grado di comprendere l'esistenza delle dimensioni del settore fisico, il che può causare una serie di problemi, come verrà illustrato di seguito.

## <a name="how-emulation-works-read-modify-write-rmw"></a>Funzionamento dell'emulazione: Lettura-Modifica-Scrittura (RMW)

Un supporto di archiviazione ha una determinata unità all'interno della quale è possibile modificare il supporto fisico. Ciò significa che i supporti possono essere scritti o riscritti solo in unità delle dimensioni del settore fisico. Pertanto, le scritture che non vengono eseguite a questo livello di unità richiedono passaggi aggiuntivi, che verranno descritti nell'esempio seguente.

In questo scenario, un'applicazione deve aggiornare il contenuto di un record Datastor che si trova all'interno di un settore logico a 512 byte. Il diagramma seguente illustra i passaggi necessari al dispositivo di archiviazione per completare la scrittura:

![passaggi necessari per aggiornare il record del datastor all'interno di un settore logico a 512 byte](images/512ermwsteps.png)

Come illustrato in precedenza, questo processo comporta alcune operazioni da parte del dispositivo di archiviazione che possono comportare una perdita di prestazioni. Per evitare questo lavoro aggiuntivo, è necessario aggiornare le applicazioni per eseguire le operazioni seguenti:

-   Eseguire una query per le dimensioni del settore fisico.
-   Assicurarsi che le scritture siano allineate alle dimensioni del settore fisico segnalate.

## <a name="the-resiliency-impact-of-read-modify-write"></a>Impatto sulla resilienza di lettura-modifica-scrittura

La resilienza indica la capacità di un'applicazione di ripristinare lo stato tra le sessioni. È stato visto ciò che è necessario per un dispositivo di archiviazione 512e per eseguire una scrittura di settore a 512 byte, il ciclo lettura-modifica-scrittura. Si esamini ora cosa accadrebbe se il processo di sovrascrittura del settore fisico precedente sui supporti fosse stato interrotto. Quali sono le conseguenze?

-   Poiché la maggior parte delle unità disco rigido viene aggiornato sul posto, il settore fisico, ci esempio la parte del supporto in cui si trova il settore fisico, potrebbe essere danneggiato con informazioni incomplete a causa di una sovrascrittura parziale. In altre parole, è possibile pensare che potrebbe avere perso tutti gli 8 settori logici (contenuti logicamente dal settore fisico).

-   Anche se la maggior parte delle applicazioni con un archivio dati è progettata con la possibilità di eseguire il ripristino da errori dei supporti, la perdita di otto settori o, in altri modi, la perdita di otto record di commit, può potenzialmente rendere impossibile il ripristino normalmente da parte dell'archivio dati. Un amministratore potrebbe dover ripristinare manualmente il database da un backup o anche eseguire una lunga ricompilazione.

-   Un impatto ancora più importante è che l'azione di un'altra applicazione che causa un ciclo lettura-modifica-scrittura può potenzialmente causare la perdita dei dati, anche se l'applicazione non è in esecuzione. Ciò è dovuto semplicemente al fatto che i dati e i dati dell'altra applicazione potrebbero trovarsi all'interno dello stesso settore fisico.

A questo punto, è importante che il software applicativo rivaluta eventuali presupposti presi nel codice e tenga presente la distinzione logica-fisica delle dimensioni del settore, insieme ad alcuni scenari interessanti per i clienti illustrati più avanti in questo articolo.

Questo problema si verifica più probabilmente se l'applicazione si basa su un archivio dati della struttura di log.

## <a name="avoiding-read-modify-write"></a>Evitare operazioni di lettura/modifica/scrittura

Anche se alcuni fornitori di risorse di archiviazione potrebbero introdurre alcuni livelli di mitigazione all'interno di determinati dispositivi di archiviazione 512e per tentare di semplificare i problemi di prestazioni e resilienza del ciclo lettura-modifica-scrittura, esiste solo una mitigazione che può essere gestita in termini di carico di lavoro. Di conseguenza, le applicazioni non devono basarsi su questa mitigazione come soluzione a lungo termine.

La soluzione a questo problema non è la mitigazione dell'unità, ma fare in modo che le applicazioni eseeggono il set di operazioni più efficace per evitare il ciclo lettura-modifica-scrittura. Questa sezione illustra gli scenari comuni in cui le applicazioni possono avere problemi con dischi di settore di grandi dimensioni e suggerisce una via di analisi per provare a risolvere ogni problema.

### <a name="issue-1-the-partition-is-not-aligned-to-a-physical-sector-boundary"></a>Problema 1: La partizione non è allineata a un limite di settore fisico

Quando l'amministratore o l'utente partiziona il disco, è possibile che la prima partizione non sia stata creata su un limite allineato. In questo modo, tutte le scritture successive potrebbero diventare non allineate ai limiti del settore fisico. A Windows Vista SP1 e Windows Server 2008, la prima partizione viene posizionata in corrispondenza dei primi 1024 KB del disco (per i dischi da 4 GB o superiori, in caso contrario l'allineamento è di 64 KB) allineata a un limite di settore fisico di 4 KB. Tuttavia, dato il partizionamento predefinito in Windows XP, un'utilità di partizionamento di terze parti o un utilizzo errato delle API Windows, le partizioni create potrebbero non essere allineate a un limite di settore fisico. Gli sviluppatori dovranno assicurarsi che le API corrette siano usate per garantire l'allineamento. Le API consigliate per garantire l'allineamento delle partizioni sono descritte di seguito.

Le API **IVdsPack::CreateVolume** e **IVdsPack2::CreateVolume2** non usano il parametro di allineamento specificato quando viene creato un nuovo volume e usano invece il valore di allineamento predefinito per il sistema operativo (Pre-Windows Vista SP1 userà 63 byte e dopo Windows Vista SP1 verranno usate le impostazioni predefinite indicate in precedenza). È quindi consigliabile che le applicazioni che devono creare partizioni usino invece le API **IVdsCreatePartitionEx::CreatePartitionEx** o **IVdsAdvancedDisk::CreatePartition,** che usano il parametro di allineamento specificato.

Il modo migliore per garantire che l'allineamento sia corretto è quello di farlo correttamente durante la creazione iniziale della partizione. In caso contrario, l'applicazione dovrà prendere in considerazione l'allineamento durante l'esecuzione di operazioni di scrittura o in fase di inizializzazione, operazione che può essere molto complessa. A Windows Vista SP1, questo non è in genere un problema. Tuttavia, le versioni precedenti Windows possono creare partizioni non allineate che possono potenzialmente causare problemi di prestazioni con alcuni dischi in formato avanzato.

### <a name="issue-2-unbuffered-writes-not-aligned-to-physical-sector-size"></a>Problema 2: Scritture senza buffer non allineate alle dimensioni fisiche del settore

Il problema di base è che le scritture senza buffer non sono allineate alle dimensioni del settore fisico segnalate del supporto di archiviazione, che attiva una lettura-modifica-scrittura nell'unità che può causare problemi di prestazioni. Le scritture memorizzate nel buffer, d'altra parte, sono allineate alle dimensioni della pagina, ovvero a 4 KB, che corrispondono in modo coincidente alle dimensioni del settore fisico della prima generazione di supporti di settore di grandi dimensioni. Tuttavia, la maggior parte delle applicazioni con un archivio dati esegue operazioni di scrittura senza buffer e pertanto dovrà garantire che queste operazioni di scrittura siano eseguite in unità delle dimensioni del settore fisico.

Per determinare se l'applicazione esegue I/O senza buffer, verificare di includere il flag **FILE \_ FLAG NO \_ \_ BUFFERING** nel *parametro dwFlagsAndAttributes* quando si chiama la funzione **CreateFile.**

Inoltre, se attualmente si allineano le scritture alle dimensioni del settore, è molto probabile che queste dimensioni del settore siano solo le dimensioni del settore logico, perché la maggior parte delle API esistenti che ese esegue query per ottenere le dimensioni del settore dei supporti in realtà si limiterà a eseguire una query sull'unità di indirizzamento, cio' le dimensioni del settore logico.  Le dimensioni del settore di interesse in questo caso sono le dimensioni del settore fisico, ovvero l'unità reale di atomicità. Di seguito sono riportati alcuni esempi di API che recuperano le dimensioni del settore logico:

-   **GetDiskFreeSpace**, **GetDiskFreeSpaceEx**
-   **FileFsVolumeInformation**
-   **IOCTL \_ DISK \_ GET \_ DRIVE \_ GEOMETRY**, **IOCTL \_ DISK GET DRIVE \_ \_ \_ GEOMETRY \_ EX**
-   **IVdsDisk::GetProperties**, **IVdsDisk3::GetProperties2**

**Come eseguire una query per le dimensioni del settore fisico**

Microsoft ha fornito un esempio di codice in MSDN che illustra in dettaglio come un'applicazione può eseguire query sulle dimensioni del settore fisico del volume. L'esempio di codice si trova in <https://msdn.microsoft.com/library/ff800831.aspx> .

Anche se l'esempio di codice precedente consente di ottenere le dimensioni del settore fisico del volume, è necessario eseguire alcuni controlli di base sulla sanità fisica segnalata prima di usarlo, perché è stato osservato che alcuni driver potrebbero non restituire dati formattati correttamente:

-   Assicurarsi che le dimensioni del settore fisico segnalate siano >= le dimensioni del settore logico segnalate. In caso contrario, l'applicazione deve usare dimensioni di settore fisiche uguali alle dimensioni del settore logico segnalate.
-   Assicurarsi che le dimensioni del settore fisico segnalate siano una potenza di due. In caso contrario, l'applicazione deve usare dimensioni di settore fisiche uguali alle dimensioni del settore logico segnalate.
-   Se le dimensioni del settore fisico sono un valore di potenza di due tra 512 byte e 4 KB, è consigliabile usare una dimensione di settore fisica arrotondata per estinzione alle dimensioni del settore logico segnalate.
-   Se le dimensioni del settore fisico sono un valore di potenza di due maggiori di 4 KB, è necessario valutare la capacità dell'applicazione di gestire questo scenario prima di usare tale valore. In caso contrario, è consigliabile usare una dimensione di settore fisica arrotondata per esere a 4 KB.

L'uso di questo IOCTL per ottenere le dimensioni del settore fisico presenta diverse limitazioni:

-   Richiede privilegi elevati. Se l'applicazione non è in esecuzione con privilegi, potrebbe essere necessario scrivere un'Windows di servizio come indicato in precedenza.

-   Non supporta i volumi SMB. Potrebbe anche essere necessario scrivere un'applicazione di Windows per supportare l'esecuzione di query sulle dimensioni dei settori fisici su questi volumi.

-   Non può essere rilasciato a un handle di file (l'ioCTL deve essere rilasciato a un handle di volume).

-   Supportato solo nelle Windows elencate all'inizio di questo articolo.

**I record di commit vengono riempiti in settori a 512 byte**

Le applicazioni con un archivio dati hanno in genere una forma di record di commit che gestisce le informazioni sulle modifiche ai metadati o la struttura dell'archivio dati. Per garantire che la perdita di un settore non influisca su più record, questo record di commit viene in genere riempito fino a una dimensione di settore. Con un disco con un settore fisico di dimensioni maggiori, l'applicazione dovrà eseguire una query per le dimensioni del settore fisico, come illustrato nella sezione precedente, e assicurarsi che ogni record di commit sia riempito fino a tale dimensione. Non solo evita il ciclo lettura-modifica-scrittura, ma garantisce che, in caso di perdita di un settore fisico, andrebbe perso un solo record di commit.

**I file di log vengono scritti in blocchi non allineati**

L'I/O senza buffer viene in genere usato durante l'aggiornamento o l'aggiunta a un file di log. Esistono diversi modi per garantire che questi aggiornamenti siano allineati correttamente:

-   Eseguire internamente il buffer degli aggiornamenti del log per le dimensioni del settore fisico segnalate dei supporti operativi e mettere le scritture del log solo quando un'unità di settore fisica è piena
-   Usare I/O memorizzato nel buffer

### <a name="issue-3-file-formats-relying-on-512-byte-sectors"></a>Problema 3: Formati di file basati su settori a 512 byte

In alcune applicazioni con formati di file standard ,ad esempio VHD 1.0, questi file potrebbero essere hard coded per presupporre una dimensione di settore di 512 byte. Di conseguenza, gli aggiornamenti e le scritture in questo file comportano un ciclo di lettura-modifica-scrittura nel dispositivo, che potrebbe causare problemi di prestazioni e resilienza per i clienti. Esistono tuttavia modi per un'applicazione di fornire supporto per il funzionamento su questo tipo di supporti, ad esempio:

-   Usare la memorizzazione nel buffer per assicurarsi che le operazioni di scrittura siano eseguite in unità delle dimensioni del settore fisico
-   Implementare una lettura/modifica-scrittura interna che consente di garantire che gli aggiornamenti siano eseguiti in unità delle dimensioni del settore fisico segnalate
-   Se possibile, riempire i record in un settore fisico, in modo che la spaziatura interna venga interpretata come spazio vuoto
-   Provare a riprogettare una nuova versione della struttura dei dati dell'applicazione con supporto per settori più grandi

### <a name="issue-4-the-reported-physical-sector-size-can-change-between-sessions"></a>Problema 4: le dimensioni del settore fisico segnalate possono cambiare tra le sessioni

Esistono molti scenari in cui le dimensioni del settore fisico segnalate dell'archiviazione sottostante che ospita il datastor possono cambiare. La più comune è quando si esegue la migrazione del datastor a un altro volume o anche in rete. Una modifica delle dimensioni del settore fisico segnalate può essere un evento imprevisto per molte applicazioni e può causare la mancata inizializzazione di alcune applicazioni.

Questo non è lo scenario più semplice da supportare ed è indicato qui come avviso. È consigliabile prendere in considerazione i requisiti di mobilità dei clienti e modificare il supporto di conseguenza per assicurarsi che i clienti non siano influenzati negativamente dall'uso di supporti 512e.

## <a name="4-kb-native-media"></a>Supporti nativi da 4 KB

I supporti di emulazione a 512 byte sono concepiti come passaggio di transizione tra supporti nativi da 512 byte e nativi a 4 KB e si prevede che i supporti nativi di 4 KB saranno rilasciati subito dopo la disponibilità di 512e. Esistono diverse implicazioni importanti per questi supporti che devono essere notati:

-   Le dimensioni del settore logico e fisico sono entrambe di 4 KB
-   Poiché non esiste alcun livello di emulazione, le scritture non allineate non verranno completate dall'archiviazione
-   Nessun hit di resilienza nascosto: le applicazioni funzionano o non funzionano

Anche se Microsoft sta attualmente esaminando il supporto per questi tipi di supporti in una versione futura di Windows e rilaserà un articolo della Knowledge Base quando appropriato, gli sviluppatori di applicazioni devono prendere in considerazione la possibilità di fornire supporto preventivamente per questi tipi di supporti.

## <a name="closing"></a>Chiusura

In questo articolo sono stati illustrati gli effetti che i supporti di settore di grandi dimensioni introducono con molti scenari di distribuzione comuni. Sono stati osservati l'impatto sulle prestazioni e sulla resilienza di Lettura-Modifica-Scrittura, alcuni degli scenari interessanti che questi supporti possono introdurre e il set di problemi che possono potenzialmente causare con il software, che in definitiva influisce sull'utente finale. Il settore dell'archiviazione è in rapida transizione ai supporti con dimensioni di settore maggiori e molto presto i clienti non saranno in grado di acquistare dischi con dimensioni tradizionali di settore a 512 byte.

Si tratta di un documento in vita ed è pensato per aiutare gli sviluppatori a comprendere questa transizione. È consigliabile avviare una conversazione con le rispettive organizzazioni, con i clienti, i professionisti IT e i fornitori di hardware per parlare della transizione di settore di grandi dimensioni e del modo in cui influisce sugli scenari che sono importanti per l'utente.

## <a name="links-to-other-resources"></a>Collegamenti ad altre risorse

-   **Windows supporto generale:**<https://support.microsoft.com/kb/2510009>
-   **Hotfix per Windows 7 e Windows Server 2008 R2:**<https://support.microsoft.com/kb/982018>
-   **Hotfix per Windows Vista e Windows Server 2008:**<https://support.microsoft.com/kb/2470478>
-   **Dichiarazione di supporto HyperV:**<https://support.microsoft.com/kb/2515143>
-   **Informazioni generali su IOCTL \_ Codice di \_ controllo DELLA PROPRIETÀ QUERY DI \_ ARCHIVIAZIONE:**[https://msdn.microsoft.com/library/ff560590.aspx](/windows-hardware/drivers/ddi/ntddstor/ni-ntddstor-ioctl_storage_query_property)
-   **IOCTL \_ Codice di \_ controllo DELLA PROPRIETÀ QUERY DI \_ ARCHIVIAZIONE:**[https://msdn.microsoft.com/library/ff800830.aspx](/windows/win32/api/winioctl/ni-winioctl-ioctl_storage_query_property)
-   **Informazioni generali sull'archiviazione \_ STRUTTURA DEL \_ \_ DESCRITTORE DI ALLINEAMENTO DI ACCESSO**: [https://msdn.microsoft.com/library/ff566344.aspx](/windows-hardware/drivers/ddi/ntddstor/ns-ntddstor-_storage_access_alignment_descriptor)
-   **Descrizione della terminologia standard usata per descrivere gli aggiornamenti software Microsoft:**<https://support.microsoft.com/kb/824684/>
-   Codice di esempio **WDK** con informazioni dettagliate su come estrarre le informazioni di allineamento dell'accesso alle risorse di archiviazione segnalate dalla struttura STORAGE **ACCESS ALIGNMENT \_ \_ \_ DESCRIPTOR** quando si effettua una chiamata al codice di controllo **IOCTL \_ STORAGE QUERY \_ \_ PROPERTY:** [/windows/desktop/api/winioctl/ns-winioctl-storage_access_alignment_descriptor](/windows/desktop/api/winioctl/ns-winioctl-storage_access_alignment_descriptor)
-   **Informazioni generali sulle ImageX Command-Line seguenti:**<https://technet.microsoft.com/library/dd799302(WS.10).aspx>
-   **Requisiti del driver Intel Chipset per supportare unità di settore da 4 KB:**<https://www.intel.com/support/chipsets/imsm/sb/CS-031502.htm>
-   Per altre informazioni sui dischi in formato avanzato, visitare i siti Web IDEMA seguenti:
    -   <http://idema.org/?page_id=2172>
    -   <http://idema.org/?download=7926>

 

 
