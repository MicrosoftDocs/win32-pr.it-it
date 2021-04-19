---
description: In questo argomento viene illustrato l'effetto dei dispositivi di archiviazione in formato avanzato sul software, vengono illustrate le applicazioni che è possibile eseguire per supportare questo tipo di supporto e viene illustrata l'infrastruttura introdotta da Microsoft con Windows 7 SP1 e Windows Server 2008 R2 SP1 per consentire agli sviluppatori di supportare questi tipi di dispositivi.
ms.assetid: 1D2847A7-15E9-42E0-90EB-7F43E76D3E44
title: Aggiornamento della compatibilità dei dischi 512e (512-byte Emulation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74b654473fa8be5fbea997bd063df2c1f898a7d1
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/13/2021
ms.locfileid: "107315004"
---
# <a name="512-byte-emulation-512e-disk-compatibility-update"></a>Aggiornamento della compatibilità dei dischi 512e (512-byte Emulation)

## <a name="platform"></a>Piattaforma

 **Client** -Windows Vista, Windows 7, Windows 7 SP1  
**Server** : windows Server 2008, windows Server 2008 R2, windows Server 2008 R2 SP1  

## <a name="feature-impact"></a>Effetto sulle funzionalità

**Gravità** -alta  
**Frequenza** -alta  









## <a name="description"></a>Descrizione

Le densità di area geospaziale aumentano annualmente e, con il recente avvento di dischi da 3 TB, i meccanismi di correzione degli errori utilizzati per gestire il rapporto tra segnale e rumore diminuiscono lo spazio in modo inefficiente, ovvero è necessaria una maggiore quantità di overhead per garantire che i supporti siano utilizzabili. Una delle soluzioni del settore di archiviazione per migliorare questo meccanismo di correzione degli errori consiste nell'introdurre un formato multimediale fisico diverso che includa dimensioni del settore fisico più grandi. Questo nuovo formato multimediale fisico è denominato *formato avanzato*. Pertanto, non è più sicuro creare presupposti relativi alle dimensioni del settore dei dispositivi di archiviazione moderni e gli sviluppatori dovranno studiare i presupposti sottostanti il codice per determinare se vi sia un effetto.

In questo argomento viene illustrato l'effetto dei dispositivi di archiviazione in formato avanzato sul software, vengono illustrate le applicazioni che è possibile eseguire per supportare questo tipo di supporto e viene illustrata l'infrastruttura per consentire agli sviluppatori di supportare questi tipi di dispositivi. Sebbene il materiale presentato in questo argomento fornisca linee guida per migliorare la compatibilità con i dischi in formato avanzato, le informazioni si applicano in genere a tutti i sistemi con dischi di formato avanzati. Le seguenti versioni di Windows forniscono supporto per l'esecuzione di query sulle dimensioni del settore fisico:

-   Windows 7 con Microsoft KB 982018
-   Windows 7 SP1
-   Windows Server 2008 R2 con Microsoft KB 982018
-   Windows Server 2008 R2 SP1
-   Windows Vista con Microsoft KB 2553708
-   Windows Server 2008 con Microsoft KB 2553708

Per ulteriori informazioni, vedere [le informazioni sui criteri di supporto Microsoft per le unità di settore di grandi dimensioni in Windows](https://support.microsoft.com/kb/2510009).

Per ulteriori informazioni sui dischi con formato avanzato, rivolgersi al fornitore del sistema di archiviazione.

## <a name="logical-vs-physical-sector-size"></a>Dimensioni logiche e dimensioni del settore fisico

Uno dei problemi relativi all'introduzione di questa modifica nel formato multimediale è la compatibilità con il software e l'hardware attualmente disponibili sul mercato. Come soluzione temporanea, il settore dell'archiviazione introduce inizialmente i dischi che emulano un normale disco del settore a 512 byte, ma che rendono disponibili informazioni sulle reali dimensioni del settore mediante i comandi ATA e SCSI standard. In seguito a questa emulazione, esistono due dimensioni di settore:

-   **Settore logico**: unità utilizzata per l'indirizzamento dei blocchi logici per il supporto. Possiamo anche considerarlo come la più piccola unità di scrittura che la risorsa di archiviazione può accettare. Si tratta dell'emulazione.

-   **Settore fisico**: unità per cui vengono completate le operazioni di lettura e scrittura nel dispositivo in un'unica operazione. Si tratta dell'unità di scrittura atomica.

La maggior parte delle API Windows correnti, ad esempio la **\_ geometria del disco IOCTL \_ get \_ drive \_** , restituirà le dimensioni del settore logico, ma le dimensioni del settore fisico possono essere recuperate tramite il codice di controllo delle [ \_ \_ \_ proprietà della query di archiviazione IOCTL](/windows-hardware/drivers/ddi/content/ntddstor/ni-ntddstor-ioctl_storage_query_property) , con le informazioni rilevanti contenute nel campo **BytesPerPhysicalSector** della struttura del [ \_ \_ \_ descrittore di allineamento dell'accesso di archiviazione](/windows/desktop/api/winioctl/ns-winioctl-storage_access_alignment_descriptor) . Questo argomento verrà descritto più dettagliatamente più avanti in questo articolo.

## <a name="initial-types-of-large-sector-media"></a>Tipi iniziali di supporti per settori di grandi dimensioni

Il settore dell'archiviazione sta dilagando rapidamente le attività di transizione al nuovo tipo di archiviazione in formato avanzato per i supporti con dimensioni del settore fisico da 4 KB. Due tipi di supporti verranno rilasciati sul mercato:

-   **4 KB nativi**: questo supporto non ha un livello di emulazione ed espone direttamente 4 KB come dimensione del settore logico e fisico. Questo supporto non è attualmente supportato da Windows e dalla maggior parte degli altri sistemi operativi. Tuttavia, Microsoft sta effettuando un'indagine sulla fattibilità del supporto di questo tipo di supporto in una versione futura di Windows ed emetterà un articolo della Knowledge base quando appropriato.
-   **emulazione a 512 byte (512e)**: questo supporto ha un livello di emulazione, come illustrato nella sezione precedente, ed espone 512-byte come dimensione del settore logico (simile a un normale disco), ma rende disponibili le informazioni sulle dimensioni del settore fisico (4 KB). Questo è ciò che molti fornitori di archiviazione stanno attualmente introducendo al mercato. Questo problema generale con questo nuovo tipo di supporto è che la maggior parte dei sistemi operativi e delle applicazioni non comprende l'esistenza delle dimensioni del settore fisico, il che può comportare un certo numero di problemi, come verrà illustrato di seguito.

## <a name="how-emulation-works-read-modify-write-rmw"></a>Funzionamento dell'emulazione: lettura-modifica-scrittura (RMW)

Un supporto di archiviazione ha una determinata unità all'interno della quale è possibile modificare il supporto fisico. Ovvero, i supporti possono essere scritti o riscritti solo in unità delle dimensioni del settore fisico. Pertanto, le Scritture non eseguite a questo livello di unità richiederebbero passaggi aggiuntivi, che verranno esaminati nell'esempio seguente.

In questo scenario, un'applicazione deve aggiornare il contenuto di un record Datastor situato all'interno di un settore logico a 512 byte. Il diagramma seguente illustra i passaggi necessari per completare la scrittura del dispositivo di archiviazione:

![passaggi necessari per aggiornare il record datastort in un settore logico a 512 byte](images/512ermwsteps.png)

Come illustrato sopra, questo processo implica alcune operazioni eseguite dal dispositivo di archiviazione che possono causare una perdita di prestazioni. Per evitare questo lavoro aggiuntivo, è necessario aggiornare le applicazioni per eseguire le operazioni seguenti:

-   Eseguire una query per le dimensioni del settore fisico.
-   Verificare che le Scritture siano allineate alle dimensioni del settore fisico indicate.

## <a name="the-resiliency-impact-of-read-modify-write"></a>Effetto della resilienza di read-modify-write

La resilienza esprime la possibilità per un'applicazione di ripristinare lo stato tra le sessioni. Sono stati esaminati gli elementi necessari per un dispositivo di archiviazione 512e per l'esecuzione di una scrittura nel settore a 512 byte, ovvero il ciclo di lettura-modifica-scrittura. Si osservi che cosa accadrebbe se il processo di sovrascrittura del precedente settore fisico sul supporto venisse interrotto. Quali sono le conseguenze?

-   Poiché la maggior parte delle unità disco rigido si aggiorna sul posto, il settore fisico, ovvero la parte del supporto in cui si trovava il settore fisico, potrebbe essere stato danneggiato con informazioni incomplete a causa di una sovrascrittura parziale. In altre parole, è possibile considerarlo come potenzialmente perso per tutti gli 8 settori logici (che il settore fisico contiene logicamente).

-   Sebbene la maggior parte delle applicazioni con un archivio dati sia progettata con la possibilità di eseguire il recupero da errori dei supporti, la perdita di otto settori o un altro modo, la perdita di otto record di commit, può potenzialmente rendere impossibile il ripristino normale dell'archivio dati. Un amministratore potrebbe dover ripristinare manualmente il database da un backup o potrebbe anche dover eseguire una ricompilazione lunga.

-   Un altro aspetto importante è che l'azione di un'altra applicazione che causa un ciclo di lettura/modifica-scrittura può causare la perdita dei dati, anche se l'applicazione non è in esecuzione. Questo è semplicemente dovuto al fatto che i dati e i dati dell'altra applicazione potrebbero trovarsi all'interno dello stesso settore fisico.

Tenendo presente questo aspetto, è importante che il software applicativo rivaluti le ipotesi prese nel codice e sia a conoscenza della distinzione delle dimensioni del settore fisico logico, insieme ad alcuni scenari di clienti interessanti illustrati più avanti in questo articolo.

Questo problema è più probabile che si verifichi se l'applicazione si basa su un archivio dati della struttura di log.

## <a name="avoiding-read-modify-write"></a>Evitare la lettura, la modifica e la scrittura

Sebbene alcuni fornitori di archiviazione possano introdurre alcuni livelli di mitigazione all'interno di determinati dispositivi di archiviazione 512e per provare a semplificare i problemi di prestazioni e resilienza del ciclo di lettura-modifica-scrittura, è possibile che la mitigazione sia gestita in termini di carico di lavoro. Di conseguenza, le applicazioni non devono basarsi su questa mitigazione come soluzione a lungo termine.

La soluzione non è mitigazione nell'unità, ma per fare in modo che le applicazioni eseguano il giusto set di elementi per evitare il ciclo di lettura-modifica-scrittura. In questa sezione vengono illustrati gli scenari comuni in cui le applicazioni possono presentare problemi con dischi di settore di grandi dimensioni e viene suggerito un viale di analisi per provare a risolvere ogni problema.

### <a name="issue-1-the-partition-is-not-aligned-to-a-physical-sector-boundary"></a>Problema 1: la partizione non è allineata a un limite di settore fisico

Quando l'amministratore o l'utente partiziona il disco, è possibile che la prima partizione non sia stata creata in un limite allineato. In questo modo tutte le scritture successive diventeranno non allineate ai limiti del settore fisico. A partire da Windows Vista SP1 e Windows Server 2008, la prima partizione viene posizionata al primo 1024 KB del disco (per i dischi da 4 GB o più grandi, in caso contrario l'allineamento è 64 KB) allineato a un limite di settore fisico da 4 KB. Tuttavia, dato il partizionamento predefinito in Windows XP, un'utilità di partizionamento di terze parti o un utilizzo errato delle API Windows, le partizioni create potrebbero non essere allineate a un limite di settore fisico. Gli sviluppatori dovranno assicurarsi che vengano usate le API corrette per garantire l'allineamento. Le API consigliate per garantire l'allineamento della partizione sono descritte di seguito.

Le API **IVdsPack:: CreateVolume** e **IVdsPack2:: CreateVolume2** non utilizzano il parametro di allineamento specificato quando viene creato un nuovo volume e utilizzano invece il valore di allineamento predefinito per il sistema operativo (precedente a Windows vista SP1 utilizzerà 63 byte e post Windows Vista SP1 utilizzerà i valori predefiniti indicati in precedenza). Pertanto, è consigliabile che le applicazioni che devono creare partizioni usino invece le API **IVdsCreatePartitionEx:: CreatePartitionEx** o **IVdsAdvancedDisk:: CreatePartition** , che usano il parametro di allineamento specificato.

Il modo migliore per garantire che l'allineamento sia corretto consiste nell'eseguire questa operazione direttamente quando si crea inizialmente la partizione. In caso contrario, l'applicazione deve tenere conto dell'allineamento quando si eseguono Scritture o in fase di inizializzazione, che può essere molto complessa. A partire da Windows Vista SP1, non si tratta in genere di un problema; Tuttavia, le versioni precedenti di Windows possono creare partizioni non allineate che potrebbero causare problemi di prestazioni con alcuni dischi di formato avanzati.

### <a name="issue-2-unbuffered-writes-not-aligned-to-physical-sector-size"></a>Problema 2: le scritture senza buffer non sono allineate alle dimensioni del settore fisico

Il problema di base è che le Scritture non memorizzate nel buffer non sono allineate alle dimensioni del settore fisico segnalato del supporto di archiviazione, che attiva un'operazione di lettura-modifica-scrittura nell'unità che può causare problemi di prestazioni. Le scritture memorizzate nel buffer, d'altra parte, sono allineate alla dimensione della pagina, ovvero 4 KB, che è il settore fisico della prima generazione di supporti di settore di grandi dimensioni. Tuttavia, la maggior parte delle applicazioni con un archivio dati esegue scritture senza buffer e pertanto dovrà assicurarsi che tali scritture vengano eseguite in unità della dimensione del settore fisico.

Per determinare se l'applicazione esegue l'I/O senza buffer, verificare di includere il **flag di file nessun flag \_ di \_ \_ buffer** nel parametro *DwFlagsAndAttributes* quando si chiama la funzione **CreateFile** .

Inoltre, se si stanno attualmente allineando le Scritture alle dimensioni del settore, le dimensioni del settore sono molto probabilmente solo le dimensioni del settore *logico* , perché la maggior parte delle API esistenti che eseguono query per le dimensioni del settore del supporto effettivamente eseguono una query solo sull'unità di indirizzamento, ovvero le dimensioni del settore logico. Le dimensioni di settore di interesse sono le dimensioni del settore fisico, ovvero l'unità reale di atomicità. Di seguito sono riportati alcuni esempi di API che recuperano le dimensioni del settore logico:

-   **GetDiskFreeSpace**, **GetDiskFreeSpaceEx**
-   **FileFsVolumeInformation**
-   **IOCTL \_ \_ \_ \_ geometria unità disco**, disco **IOCTL \_ \_ ottenere \_ unità \_ Geometry \_ es**
-   **IVdsDisk:: GetProperties**, **IVdsDisk3:: GetProperties2**

**Come eseguire una query per le dimensioni del settore fisico**

Microsoft ha fornito un esempio di codice su MSDN con informazioni dettagliate su come un'applicazione può eseguire una query per le dimensioni del settore fisico del volume. L'esempio di codice si trova in <https://msdn.microsoft.com/library/ff800831.aspx> .

Mentre l'esempio di codice precedente consente di ottenere le dimensioni del settore fisico del volume, è necessario eseguire un controllo di integrità di base sulle dimensioni del settore fisico segnalato prima di utilizzarlo, in quanto è stato rilevato che alcuni driver non restituiscono dati formattati correttamente:

-   Verificare che le dimensioni del settore fisico indicate siano >= le dimensioni del settore logico indicate. In caso contrario, l'applicazione deve utilizzare una dimensione di settore fisico uguale alla dimensione del settore logico indicata.
-   Assicurarsi che le dimensioni del settore fisico segnalato siano una potenza di due. In caso contrario, l'applicazione deve utilizzare una dimensione di settore fisico uguale alla dimensione del settore logico indicata.
-   Se le dimensioni del settore fisico sono un valore di potenza di due tra 512 byte e 4 KB, è consigliabile utilizzare una dimensione di settore fisico arrotondata per difetto alle dimensioni del settore logico indicate.
-   Se le dimensioni del settore fisico sono un valore di potenza di due maggiore di 4 KB, è necessario valutare la capacità dell'applicazione di gestire questo scenario prima di usare tale valore. In caso contrario, è consigliabile utilizzare una dimensione di settore fisico arrotondata a 4 KB.

L'uso di questo IOCTL per ottenere le dimensioni del settore fisico presenta diverse limitazioni:

-   Richiede privilegi elevati. Se l'applicazione non è in esecuzione con privilegi, potrebbe essere necessario scrivere un'applicazione di servizio Windows come indicato in precedenza.

-   Non supporta i volumi SMB. Potrebbe anche essere necessario scrivere un'applicazione di servizio Windows per supportare le query sulle dimensioni del settore fisico su questi volumi.

-   Non può essere emesso per alcun handle di file (il IOCTL deve essere emesso a un handle del volume).

-   Supportato solo nelle versioni di Windows elencate in prossimità dell'inizio di questo articolo.

**I record di commit vengono riempiti in settori a 512 byte**

Le applicazioni con un archivio dati in genere hanno una forma di record di commit che mantiene le informazioni sulle modifiche dei metadati o gestisce la struttura dell'archivio dati. Per garantire che la perdita di un settore non influisca su più record, questo record di commit viene in genere rivestito a dimensioni di settore. Con un disco con dimensioni di settore fisico maggiori, l'applicazione dovrà eseguire una query per le dimensioni del settore fisico, come illustrato nella sezione precedente, e assicurarsi che ogni record di commit venga riempito con tale dimensione. Questa operazione non solo consente di evitare il ciclo di lettura-modifica-scrittura, ma garantisce che, in caso di perdita di un settore fisico, venga perso un solo record di commit.

**I file di log vengono scritti in blocchi non allineati**

Le operazioni di I/O senza buffer vengono in genere utilizzate per l'aggiornamento o l'aggiunta a un file di log. Esistono diversi modi per garantire che questi aggiornamenti siano allineati correttamente:

-   Eseguire internamente il buffer degli aggiornamenti dei log alla dimensione del settore fisico segnalata del supporto operativo e inviare le Scritture del log solo quando un'unità di settore fisico è piena
-   USA I/O memorizzato nel buffer

### <a name="issue-3-file-formats-relying-on-512-byte-sectors"></a>Problema 3: formati di file basati su settori a 512 byte

Per alcune applicazioni con formati di file standard, ad esempio VHD 1,0, questi file possono essere hardcoded per presupporre una dimensione di settore a 512 byte. Pertanto, gli aggiornamenti e le Scritture in questo file comportano un ciclo di lettura-modifica-scrittura sul dispositivo, che potrebbe causare problemi di prestazioni e resilienza per i clienti. Esistono tuttavia modi per consentire a un'applicazione di fornire supporto per l'utilizzo di questo tipo di supporto, ad esempio:

-   Usare la memorizzazione nel buffer per assicurarsi che le Scritture vengano eseguite in unità della dimensione del settore fisico
-   Implementare una lettura-modifica-scrittura interna che consente di garantire che gli aggiornamenti vengano eseguiti in unità della dimensione del settore fisico indicata.
-   Se possibile, riempie i record in un settore fisico, in modo che la spaziatura interna venga interpretata come spazio vuoto
-   Provare a riprogettare una nuova versione della struttura di dati dell'applicazione con supporto per settori di grandi dimensioni

### <a name="issue-4-the-reported-physical-sector-size-can-change-between-sessions"></a>Problema 4: le dimensioni del settore fisico indicate possono cambiare tra le sessioni

Esistono molti scenari in cui le dimensioni del settore fisico segnalato dell'archiviazione sottostante che ospita Datastor possono cambiare. Il più comune di questi si verifica quando si esegue la migrazione di Datastor a un altro volume o anche attraverso la rete. Una modifica nelle dimensioni del settore fisico segnalato può essere un evento imprevisto per molte applicazioni e può comportare la reinizializzazione anche di alcune applicazioni.

Questo non è lo scenario più semplice da supportare ed è indicato come consultivo. È necessario considerare i requisiti di mobilità dei clienti e modificare di conseguenza il supporto per garantire che i clienti non vengano compromessi con i supporti 512e.

## <a name="4-kb-native-media"></a>Supporti nativi da 4 KB

il supporto per l'emulazione a 512 byte viene considerato un passaggio di transizione tra i supporti nativi a 512 byte e i supporti nativi da 4 KB e si prevede di visualizzare i supporti nativi di 4 KB rilasciati subito dopo che 512e è disponibile. Questo supporto presenta diverse implicazioni importanti, che devono essere indicate:

-   Le dimensioni del settore logico e fisico sono entrambe 4 KB
-   Poiché non esiste alcun livello di emulazione, le Scritture non allineate non verranno eseguite dall'archiviazione
-   Nessuna resilienza nascosta: le applicazioni funzionano o non funzionano

Sebbene Microsoft stia attualmente analizzando il supporto per questi tipi di supporti in una versione futura di Windows e rilascerà un articolo della Knowledge base quando appropriato, gli sviluppatori di applicazioni devono considerare preventivamente la fornitura del supporto per questi tipi di supporti.

## <a name="closing"></a>Chiusura

In questo articolo è stato illustrato il problema che introduce i supporti di grandi settori con molti scenari di distribuzione comuni. Abbiamo visto l'impatto sulle prestazioni e sulla resilienza di lettura-modifica-scrittura, alcuni degli scenari interessanti che questo supporto può presentare e il set di problemi che possono causare potenzialmente con il software, che influiscono infine sull'utente finale. Il settore dell'archiviazione viene rapidamente sottoposto a transizione a supporti con dimensioni di settore maggiori e molto presto i clienti non saranno in grado di acquistare dischi con dimensioni tradizionali di settore a 512 byte.

Si tratta di un documento vivente ed è concepito come supporto per gli sviluppatori per aiutare a comprendere questa transizione. È necessario iniziare una conversazione con le rispettive organizzazioni, con i clienti, i professionisti IT e i fornitori di hardware per parlare della transizione di settore di grandi dimensioni e del modo in cui influiscono sugli scenari importanti.

## <a name="links-to-other-resources"></a>Collegamenti ad altre risorse

-   **Dichiarazione del supporto generale di Windows**: <https://support.microsoft.com/kb/2510009>
-   **Hotfix per Windows 7 e Windows Server 2008 R2**: <https://support.microsoft.com/kb/982018>
-   **Hotfix per Windows Vista e Windows Server 2008**: <https://support.microsoft.com/kb/2470478>
-   **Istruzione di supporto HyperV**: <https://support.microsoft.com/kb/2515143>
-   **Informazioni generali sul comando IOCTL \_ \_ \_ Codice controllo proprietà query di archiviazione**: [https://msdn.microsoft.com/library/ff560590.aspx](/windows-hardware/drivers/ddi/ntddstor/ni-ntddstor-ioctl_storage_query_property)
-   **IOCTL \_ \_ \_ Codice controllo proprietà query di archiviazione**: [https://msdn.microsoft.com/library/ff800830.aspx](/windows/win32/api/winioctl/ni-winioctl-ioctl_storage_query_property)
-   **Informazioni generali sull'archiviazione \_ \_Struttura del \_ descrittore di allineamento di accesso**: [https://msdn.microsoft.com/library/ff566344.aspx](/windows-hardware/drivers/ddi/ntddstor/ns-ntddstor-_storage_access_alignment_descriptor)
-   **Descrizione della terminologia standard utilizzata per descrivere gli aggiornamenti software Microsoft**: <https://support.microsoft.com/kb/824684/>
-   **Esempio di codice WDK** con informazioni dettagliate su come estrarre le informazioni di allineamento dell'accesso di archiviazione segnalate dalla struttura del **\_ \_ \_ descrittore dell'allineamento di accesso** alla risorsa di archiviazione quando si effettua una chiamata al codice di controllo della **\_ \_ \_ proprietà query di archiviazione IOCTL** : [/Windows/Desktop/API/WinIoCtl/NS-WinIoCtl-STORAGE_ACCESS_ALIGNMENT_DESCRIPTOR](/windows/desktop/api/winioctl/ns-winioctl-storage_access_alignment_descriptor)
-   **Informazioni generali sulle opzioni di Command-Line di ImageX**: <https://technet.microsoft.com/library/dd799302(WS.10).aspx>
-   **Requisiti del driver del chipset Intel per supportare unità di settore da 4 KB**: <https://www.intel.com/support/chipsets/imsm/sb/CS-031502.htm>
-   Per altre informazioni sui dischi con formati avanzati, visitare i siti Web IDEMa seguenti:
    -   <http://idema.org/?page_id=2172>
    -   <http://idema.org/?download=7926>

 

 
