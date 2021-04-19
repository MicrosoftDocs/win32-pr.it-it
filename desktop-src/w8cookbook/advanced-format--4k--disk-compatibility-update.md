---
title: Aggiornamento della compatibilità del disco con formato avanzato (4K)
description: Aggiornamento della compatibilità del disco con formato avanzato (4K)
ms.assetid: 2C9EB0CF-D27B-457A-8FE6-24824BCC084C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbad505575c4479bd750f09ccd83bc4da4c39667
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314974"
---
# <a name="advanced-format-4k-disk-compatibility-update"></a>Aggiornamento della compatibilità del disco con formato avanzato (4K)

## <a name="platforms"></a>Piattaforme

**Client**   di   Windows XP, Windows Vista, Windows 7, Windows 7 SP1, Windows 8  
**Server**   di   Windows Server 2003, Windows Server 2008, Windows Server 2008 R2, Windows Server 2008 R2 SP1, Windows Server 2012, Windows Server 2012 R2, Windows Server 2016  


## <a name="description"></a>Descrizione

Questo articolo è una versione aggiornata dell'articolo intitolato aggiornamento della compatibilità del disco 512e (512-byte Emulation), rilasciato per Windows 7 SP1 e Windows Server 2008 R2 SP1. Questo aggiornamento contiene informazioni molto nuove, alcune delle quali si applicano solo a Windows 8 e Windows Server 2012.

Le densità di area geospaziale sono sempre più annuali e, con il recente avvento di dischi da 3 TB, i meccanismi di correzione degli errori utilizzati per gestire la riduzione del rapporto tra segnale e rumore sono diventati inefficienti. ovvero, è necessaria una maggiore quantità di overhead per garantire che il supporto sia utilizzabile. Una delle soluzioni del settore di archiviazione per migliorare questo meccanismo di correzione degli errori consiste nell'introdurre un formato multimediale fisico diverso che includa dimensioni del settore fisico più grandi. Questo nuovo formato multimediale fisico è denominato formato avanzato. Pertanto, non è più sicuro creare presupposti relativi alle dimensioni del settore dei dispositivi di archiviazione moderni e gli sviluppatori dovranno studiare i presupposti sottostanti il codice per determinare se vi sia un effetto.

In questo argomento viene illustrato l'effetto dei dispositivi di archiviazione in formato avanzato sul software, vengono illustrate le app che possono essere supportate da questo tipo di supporto e viene illustrata l'infrastruttura introdotta da Microsoft con Windows Vista, Windows 7 e Windows 8 per consentire agli sviluppatori di supportare questi tipi di dispositivi. Sebbene il materiale presentato in questo argomento fornisca linee guida per migliorare la compatibilità con i dischi in formato avanzato, le informazioni si applicano in genere a tutti i sistemi con dischi di formato avanzati che eseguono Windows Vista, Windows 7 e Windows 8.

**Riepilogo delle nuove funzionalità correlate ai settori di grandi dimensioni**

Nell'elenco seguente sono riepilogate le nuove funzionalità fornite come parte di Windows 8 e Windows Server 2012 per migliorare l'esperienza dei clienti e degli sviluppatori con dischi di settore di grandi dimensioni. Seguono una descrizione più dettagliata di ogni elemento.

-   Si basa sul supporto di Windows 7 SP1 per i dischi 4K con emulazione (512e) e offre il supporto completo della posta in arrivo per i dischi con dimensioni di settore 4K senza emulazione (4K nativo). Alcune app e scenari supportati includono:
    -   Possibilità di installare Windows e di eseguire l'avvio da un disco del settore 4K senza emulazione (disco nativo 4K)
    -   VHD e nuovo formato di file VHDX
    -   Supporto completo per HyperV
    -   Windows backup
    -   Supporto completo in NT file system (NTFS)
    -   Supporto completo con nuovi pool e spazi di archiviazione (SSP)
    -   Supporto completo con Windows Defender
-   Fornisce una nuova API per eseguire una query per le dimensioni del settore fisico (FileFsSectorSizeInformation):
    -   Disponibile per i volumi di rete
    -   Può essere emesso per qualsiasi handle di file
    -   Disponibile per le app senza privilegi
    -   Modello di utilizzo più amichevole
-   Include l'utilità della riga di comando fsutil avanzata per eseguire query per le dimensioni logiche e fisiche del volume con le informazioni di allineamento (la versione di base dell'utilità senza informazioni di allineamento è disponibile per Windows 7 con Microsoft KB 982018 e Windows Server 2008 R2 con Microsoft KB 982018)

**Introduzione ai dischi con formato avanzato (4K)**

Uno dei problemi relativi all'introduzione di questa modifica nel formato multimediale è il rischio di introdurre problemi di compatibilità con il software e l'hardware esistenti. Come soluzione di compatibilità temporanea, il settore dell'archiviazione introduce inizialmente i dischi che emulano un normale disco del settore a 512 byte, ma che rendono disponibili informazioni sulle reali dimensioni del settore mediante i comandi ATA e SCSI standard. In seguito a questa emulazione, in pratica sono presenti due dimensioni di settore:

**Settore logico:** Unità utilizzata per l'indirizzamento dei blocchi logici per il supporto. Possiamo anche considerarlo come la più piccola unità di scrittura che la risorsa di archiviazione può accettare. Si tratta dell'emulazione.   
**Settore fisico:** Unità per la quale vengono completate le operazioni di lettura e scrittura nel dispositivo in un'unica operazione. Si tratta dell'unità di scrittura atomica.  
 La maggior parte delle API Windows correnti, ad esempio la \_ geometria del disco IOCTL \_ Get Drive, \_ \_ restituirà le dimensioni del settore logico, ma le dimensioni del settore fisico possono essere recuperate tramite il codice di controllo della proprietà della <a href="/windows-hardware/drivers/ddi/content/ntddstor/ni-ntddstor-ioctl_storage_query_property"> \_ query di archiviazione \_ \_ IOCTL</a> , con le informazioni rilevanti contenute nel campo BytesPerPhysicalSector della struttura del <a href="/windows/desktop/api/winioctl/ns-winioctl-storage_access_alignment_descriptor"> \_ \_ \_ descrittore di allineamento dell'accesso di archiviazione</a> . Questo argomento verrà descritto più dettagliatamente più avanti in questo articolo.

**Tipi iniziali di supporti per settori di grandi dimensioni**

Il settore dell'archiviazione sta dilagando rapidamente nel tentativo di passare a questo nuovo tipo di archiviazione avanzata per i supporti con dimensioni di settore fisico di 4 KB. Due tipi di supporti verranno rilasciati sul mercato:

**4 KB nativi:** Questo supporto non dispone di un livello di emulazione ed espone direttamente 4 KB come dimensioni del settore logico e fisico. Il problema generale del nuovo tipo di supporto è che la maggior parte delle applicazioni e dei sistemi operativi non eseguono query e allineano le operazioni di I/o alle dimensioni del settore fisico, causando operazioni di I/o non riuscite impreviste.  
**emulazione a 512 byte (512e):** Questo supporto ha un livello di emulazione, come illustrato nella sezione precedente, ed espone 512 byte come dimensioni del settore logico (analogamente a un normale disco), ma rende disponibili le informazioni sulle dimensioni del settore fisico (4 KB). Il problema generale del nuovo tipo di supporto è che la maggior parte dei sistemi operativi e delle app non comprende l'esistenza delle dimensioni del settore fisico, il che può comportare un certo numero di problemi, come verrà illustrato di seguito.  
**Supporto generale di Windows per supporti di settore di grandi dimensioni**

Questa tabella documenta i criteri ufficiali di supporto Microsoft per diversi supporti e le relative dimensioni di settore segnalate. Per informazioni dettagliate, vedere questo [articolo della Knowledge Knowledge](https://support.microsoft.com/kb/2510009) .



| Nomi comuni                                  | Dimensioni del settore logico segnalate | Dimensioni del settore fisico segnalate | Versione di Windows con supporto                                                                                                                                                                                                                                                                             |
|-----------------------------------------------|------------------------------|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 512 byte nativi, 512N                         | 512 byte                    | 512 byte                     | Tutte le versioni di Windows                                                                                                                                                                                                                                                                                     |
| Formato avanzato, 512e, AF, emulazione a 512 byte | 512 byte                    | 4 KB                          | Windows Vista w/MS KB 2553708 <br/> Windows Server 2008 \* w/MS KB 2553708 <br/> Windows 7 w/MS KB 982018 <br/> Windows Server 2008 R2 * w/MS KB 982018 <br/> Tutte le versioni di Windows da Windows 7 SP1 e versioni successive. <br/> Tutte le versioni del server da Server 2008 R2 SP1 e versioni successive. <br/> <br/> \*Ad eccezione di Hyper-V. Vedere la sezione ["requisiti di supporto dell'applicazione per unità di grandi dimensioni"](https://support.microsoft.com/help/2510009/microsoft-support-policy-for-4k-sector-hard-drives-in-windows) . |
| Formato avanzato, AF, 4K nativo, 4Kn            | 4 KB                         | 4 KB                          | Tutte le versioni di Windows da Windows 8 e versioni successive <br/> Tutte le versioni server di Windows Server 2012 e versioni successive <br/>                                                                                                                                                                                                                                                      |
| Altro                                         | Non 4 KB o 512 byte        | Non 4 KB o 512 byte         | Non supportato                                                                                                                                                                                                                                                                                            |



 

> [!Note]  
> Sebbene non venga sottolineato nella tabella precedente, Windows XP, Windows Server 2003 e Windows Server 2003 R2 non supportano i supporti 512e o 4Kn. Sebbene il sistema possa avviarsi e funzionare in modo minimo, potrebbero verificarsi scenari sconosciuti di problemi di funzionalità, perdita di dati o prestazioni ottimali. Pertanto, Microsoft consiglia vivamente di utilizzare i supporti 512e con Windows XP o altri prodotti basati sulla codebase di Windows XP (ad esempio Windows Home Server 1,0, Windows Server 2003, Windows Server 2003 R2, Windows XP 64-bit Edition, Windows XP Embedded, Windows Small Business Server 2003 e Windows Small Business Server 2003 R2).

 

## <a name="how-emulation-works-read-modify-write-rmw"></a>Funzionamento dell'emulazione: lettura-modifica-scrittura (RMW)

Un supporto di archiviazione ha una determinata unità all'interno della quale è possibile modificare il supporto fisico. Ovvero, i supporti possono essere scritti o riscritti solo in unità delle dimensioni del settore fisico. Pertanto, le Scritture non eseguite a questo livello di unità richiederebbero passaggi aggiuntivi, che verranno esaminati nell'esempio riportato di seguito.

In questo scenario, un'app deve aggiornare il contenuto di un record Datastor che si trova all'interno di un settore logico a 512 byte. Questo diagramma illustra i passaggi necessari per completare la scrittura del dispositivo di archiviazione:

![passaggi per un dispositivo di archiviazione per completare una scrittura](images/512ermwsteps.png)

Come illustrato sopra, questo processo implica alcune operazioni eseguite dal dispositivo di archiviazione che possono causare una perdita di prestazioni. Per evitare questo lavoro aggiuntivo, è necessario aggiornare le app a:

-   Query per le dimensioni del settore fisico
-   Verificare che le Scritture siano allineate alle dimensioni del settore fisico indicate

Sebbene sia inizialmente possibile che si verifichi un problema di prestazioni, è possibile che si verifichino problemi più gravi. Questa operazione verrà illustrata nella sezione successiva.

**Resilienza: il costo nascosto di lettura-modifica-scrittura**

La resilienza esprime la capacità di un'app di ripristinare lo stato tra le sessioni. Abbiamo visto cosa è necessario affinché un dispositivo di archiviazione 512e esegua un settore a 512 byte per scrivere il ciclo di lettura-modifica-scrittura. Si osservi che cosa accadrebbe se il processo di sovrascrittura del precedente settore fisico sul supporto venisse interrotto. Quali sono le conseguenze?

-   Poiché la maggior parte delle unità disco rigido si aggiorna sul posto, il settore fisico, ovvero la parte del supporto in cui si trovava il settore fisico, potrebbe essere stato danneggiato con informazioni incomplete a causa di una sovrascrittura parziale. In altre parole, è possibile considerarlo come potenzialmente perso per tutti gli 8 settori logici (che il settore fisico contiene logicamente).
-   Sebbene la maggior parte delle app con un archivio dati sia progettata con la possibilità di eseguire il recupero da errori dei supporti, la perdita di otto settori o un altro modo, la perdita di otto record di commit, può potenzialmente rendere impossibile il ripristino normale dell'archivio dati. Un amministratore potrebbe dover ripristinare manualmente il database da un backup o potrebbe anche dover eseguire una ricompilazione lunga.
-   Un altro aspetto importante è che l'azione di un'altra app che causa un ciclo di lettura/modifica-scrittura può causare la perdita dei dati anche se l'app non è in esecuzione. Questo è semplicemente dovuto al fatto che i dati e gli altri dati dell'app potrebbero trovarsi all'interno dello stesso settore fisico.

Tenendo presente questo aspetto, è importante che il software dell'app rivaluti le ipotesi prese nel codice e sia a conoscenza della distinzione delle dimensioni del settore fisico logico, insieme ad alcuni scenari di clienti interessanti illustrati più avanti in questo articolo.

**Operazione corretta (evitando la lettura-modifica-scrittura)**

Sebbene alcuni fornitori di archiviazione possano introdurre alcuni livelli di mitigazione all'interno di determinati dispositivi di archiviazione 512e per provare a semplificare i problemi di prestazioni e resilienza del ciclo di lettura-modifica-scrittura, è possibile che la mitigazione sia sufficiente per la gestione in termini di carico di lavoro. Di conseguenza, le app non devono basarsi su questa mitigazione come soluzione a lungo termine. Inoltre, non vi è alcuna garanzia che tutte le classi di dischi rilevino questa mitigazione, né la garanzia che la mitigazione sia ben progettata.

La soluzione non è la mitigazione nell'unità, ma per progettare le app in modo da eseguire il set corretto di elementi per supportare questo tipo di supporto. Questa sezione illustra gli scenari comuni in cui le app possono avere problemi con dischi di settore di grandi dimensioni e suggerisce un viale di analisi per provare a risolvere ogni problema.

**Problema 1: la partizione non è allineata a un limite di settore fisico**

Quando l'amministratore o l'utente partiziona il disco, è possibile che la prima partizione non sia stata creata in un limite allineato. In questo modo tutte le scritture successive diventeranno non allineate ai limiti del settore fisico. A partire da Windows Vista SP1 e Windows Server 2008, la prima partizione viene posizionata al primo 1024 KB del disco (per i dischi da 4 GB o più grandi, in caso contrario l'allineamento è 64 KB) allineato a un limite del settore fisico da 4 KB. Tuttavia, dato il partizionamento predefinito in Windows XP, un'utilità di partizionamento di terze parti o un utilizzo errato delle API Windows, le partizioni create potrebbero non essere allineate a un limite di settore fisico. Gli sviluppatori dovranno assicurarsi che vengano usate le API corrette per garantire l'allineamento. Le API consigliate per garantire l'allineamento della partizione sono descritte di seguito.

Le API IVdsPack:: CreateVolume e IVdsPack2:: CreateVolume2 non utilizzano il parametro di allineamento specificato quando viene creato un nuovo volume, ma utilizzano invece il valore predefinito di allineamento per il sistema operativo (precedente a Windows Vista SP1 utilizzerà 63 byte e post Windows Vista SP1 utilizzerà i valori predefiniti indicati in precedenza). Usare invece le API IVdsCreatePartitionEx:: CreatePartitionEx o IVdsAdvancedDisk:: CreatePartition che usano il parametro di allineamento specificato per le app che devono creare partizioni.

Il modo migliore per garantire che l'allineamento sia corretto consiste nell'eseguire questa operazione direttamente quando si crea inizialmente la partizione. In caso contrario, l'applicazione deve tenere conto dell'allineamento quando si eseguono le Scritture o all'inizializzazione, che può essere un processo molto complesso.

**Problema 2: le scritture senza buffer non sono allineate alle dimensioni del settore fisico**

Il problema più semplice è che le scritture senza buffer non sono allineate alle dimensioni del settore fisico del supporto di archiviazione indicato. Le scritture memorizzate nel buffer, d'altra parte, sono allineate alle dimensioni della pagina 4 KB, ovvero le dimensioni del settore fisico della prima generazione di supporti di settore di grandi dimensioni. Tuttavia, la maggior parte delle app con un archivio dati eseguono scritture senza buffer e pertanto dovranno assicurarsi che tali scritture vengano eseguite in unità di dimensioni del settore fisico.

Alcuni esempi di scenari in cui l'I/O dell'app risultante non è allineato:

**I record di commit vengono riempiti in settori a 512 byte:** Le app con un archivio dati in genere hanno una forma di record di commit che mantiene le informazioni sulle modifiche dei metadati o gestisce la struttura dell'archivio dati. Per garantire che la perdita di un settore non influisca su più record, questo record di commit viene in genere rivestito a dimensioni di settore. Con un disco con una dimensione di settore fisico più grande, l'app dovrà eseguire una query per le dimensioni del settore fisico, come illustrato nella sezione precedente, e verificare che ogni record di commit venga riempito a tale dimensione. Con un disco 4K, questo assicura che le operazioni di I/o non abbiano esito negativo. Con un disco 512e, non solo questa operazione consente di evitare il ciclo di lettura-modifica-scrittura, per garantire che in caso di perdita di un settore fisico venga perso solo un record di commit.  
**I file di log vengono scritti in blocchi non allineati:** Le operazioni di I/O senza buffer vengono in genere utilizzate per l'aggiornamento o l'aggiunta a un file di log. Le app possono passare all'I/O memorizzato nel buffer oppure inserire internamente gli aggiornamenti dei log in unità di dimensioni del settore fisico per evitare I/o non riusciti o attivare una lettura-modifica-scrittura.  
 Per determinare se l'app emette I/O senza buffer, assicurarsi di includere il flag di FILE \_ \_ nessun \_ flag di buffer nel parametro *dwFlagsAndAttributes* quando si chiama la funzione CreateFile.

Inoltre, se si stanno attualmente allineando le Scritture alle dimensioni del settore, le dimensioni del settore sono molto probabilmente solo le dimensioni del settore logico, perché la maggior parte delle API esistenti che eseguono query per le dimensioni del settore del supporto eseguono solo query sull'unità di indirizzamento, ovvero le dimensioni del settore logico. Le dimensioni di settore di interesse sono le dimensioni del settore fisico, ovvero l'unità reale di atomicità. Di seguito sono riportati alcuni esempi di API che recuperano le dimensioni del settore logico:

-   GetDiskFreeSpace, GetDiskFreeSpaceEx
-   FileFsVolumeInformation
-   \_geometria del disco IOCTL ottenere l' \_ \_ unità \_ geometrica, il \_ disco IOCTL \_ get \_ drive \_ Geometry \_ es
-   IVdsDisk:: GetProperties, IVdsDisk3:: GetProperties2

Ecco come è possibile eseguire una query per le dimensioni del settore fisico:

**Metodo preferito per Windows 8**

Con Windows 8, Microsoft ha introdotto una nuova API che consente agli sviluppatori di integrare facilmente il supporto 4K all'interno delle proprie app. Questa nuova API supporta un numero ancora maggiore di scenari rispetto al metodo legacy per Windows Vista e Windows 7 descritto di seguito. Questa API Abilita questi scenari di chiamata:

-   Chiamata da un'app senza privilegi
-   Chiamata a qualsiasi handle di file valido
-   Chiamata a un handle di file su un volume remoto tramite SMB2
-   Modello di programmazione semplificato

L'API è sotto forma di una nuova classe info, FileFsSectorSizeInformation, con le informazioni relative alle dimensioni del settore FS del FILE di struttura associate \_ \_ \_ \_ , definite come segue:


```
typedef struct _FILE_FS_SECTOR_SIZE_INFORMATION {  
    ULONG LogicalBytesPerSector;  
    ULONG PhysicalBytesPerSectorForAtomicity;  
    ULONG PhysicalBytesPerSectorForPerformance;  
    ULONG FileSystemEffectivePhysicalBytesPerSectorForAtomicity;  
    ULONG Flags;  
    ULONG ByteOffsetForSectorAlignment;  
    ULONG ByteOffsetForPartitionAlignment;  
} FILE_FS_SECTOR_SIZE_INFORMATION, *PFILE_FS_SECTOR_SIZE_INFORMATION;
```



**Metodo legacy per Windows 7 e Windows Vista**

Windows Vista e Windows Server 2008 hanno introdotto le API per eseguire una query per le dimensioni del settore fisico del dispositivo di archiviazione collegato per i controller di archiviazione basati su AHCI. Con Windows 7 e Windows Server 2008 R2, a partire da SP1 (o Microsoft Knowledge Base 982018), questo supporto viene esteso ai controller di archiviazione basati su Storport. Microsoft ha fornito un [esempio di codice](/windows/desktop/api/winioctl/ns-winioctl-storage_access_alignment_descriptor) su MSDN con informazioni dettagliate sul modo in cui un'app può eseguire query per le dimensioni del settore fisico del volume.

Mentre l'esempio di codice precedente consente di ottenere le dimensioni del settore fisico del volume, è necessario eseguire un controllo di integrità di base delle dimensioni del settore fisico segnalato prima di utilizzarlo, in quanto è stato rilevato che alcuni driver non restituiscono dati formattati correttamente:

-   Verificare che le dimensioni del settore fisico segnalato siano >= le dimensioni del settore logico indicate. in caso contrario, l'app deve usare una dimensione del settore fisico uguale alla dimensione del settore logico indicata.
-   Assicurarsi che le dimensioni del settore fisico segnalato siano una potenza di due; in caso contrario, l'app deve usare una dimensione del settore fisico uguale alla dimensione del settore logico indicata.
-   Se le dimensioni del settore fisico sono un valore di potenza di due tra 512 byte e 4 KB, è consigliabile utilizzare una dimensione di settore fisico arrotondata per difetto alle dimensioni del settore logico indicate.
-   Se le dimensioni del settore fisico sono un valore di potenza di due maggiore di 4 KB, è necessario valutare la capacità dell'app di gestire questo scenario prima di usare tale valore. in caso contrario, è consigliabile utilizzare una dimensione di settore fisico arrotondata a 4 KB

L'uso di questo IOCTL per ottenere le dimensioni del settore fisico presenta diverse limitazioni. È

-   Richiede privilegi elevati. Se l'app non è in esecuzione con privilegi, potrebbe essere necessario scrivere un'applicazione di servizio Windows come indicato in precedenza
-   Non supporta i volumi SMB; potrebbe anche essere necessario scrivere un'applicazione di servizio Windows per supportare le query sulle dimensioni del settore fisico su questi volumi
-   Non può essere emesso per alcun handle di file (è necessario emettere IOCTL per un handle del volume)

**Problema 3: formati di file basati su settori a 512 byte**

Per alcune app con formati di file standard, ad esempio VHD 1,0, questi file possono essere hardcoded per presupporre una dimensione di settore a 512 byte. Pertanto, gli aggiornamenti e le Scritture in questo file comporteranno un ciclo di lettura-modifica-scrittura sul dispositivo che potrebbe causare problemi di prestazioni e resilienza per i clienti. Esistono tuttavia modi per consentire a un'app di fornire supporto per l'utilizzo di questo tipo di supporto, ad esempio:

-   Usare la memorizzazione nel buffer per assicurarsi che le Scritture vengano eseguite in unità della dimensione del settore fisico
-   Implementare una lettura-modifica-scrittura interna che consente di garantire che gli aggiornamenti vengano eseguiti in unità della dimensione del settore fisico indicata.
-   Se possibile, riempie i record in un settore fisico, in modo che la spaziatura interna venga interpretata come spazio vuoto
-   Provare a riprogettare una versione della struttura di dati dell'app con supporto per settori di grandi dimensioni

**Problema 4: le dimensioni del settore fisico indicate possono cambiare tra le sessioni**

Esistono molti scenari in cui le dimensioni del settore fisico segnalato dell'archiviazione sottostante che ospita Datastor possono cambiare. Il più comune di questi si verifica quando si esegue la migrazione di Datastor a un altro volume o anche attraverso la rete. Una modifica nelle dimensioni del settore fisico segnalate può essere un evento imprevisto per molte app e potenzialmente può causare la mancata inizializzazione di alcune app.

Questo non è lo scenario più semplice da supportare ed è indicato come consultivo. È necessario prendere in considerazione i requisiti di mobilità dei clienti e modificare di conseguenza il supporto per garantire che i clienti non vengano compromessi con i supporti di 4K nativi o 512e.

**Come un utente può recuperare le dimensioni del settore logico e fisico per un volume**

In-box con Windows è un'utilità che consente di visualizzare le informazioni sulle dimensioni del settore per un volume. Le versioni di Windows con fsutil supportato sono:

-   Windows 8
-   Windows Server 2012
-   Windows 7 SP1 con Microsoft KB 982018
-   Windows 7 con Microsoft KB 982018
-   Windows Server 2008 R2 SP1 con Microsoft KB 982018 (v3)
-   Windows Server 2008 R2 con Microsoft KB 982018 (v3)
-   Windows Vista con Microsoft KB 2553708
-   Windows Server 2008 con Microsoft KB 2553708

Per ottenere le informazioni sulle dimensioni del settore, chiamare l'utilità come indicato di seguito da un prompt dei comandi con privilegi elevati:


```
fsutil fsinfo ntfsinfo <drive letter>
```



Un disco di settore 4K con emulazione a 512 byte ha il campo byte per settore impostato su 512 e il campo byte per settore fisico è impostato su 4096 come indicato di seguito:

![byte per settore e per settore fisico di un disco del settore 4K con emulazione a 512 byte](images/4ksectordiskwith512emulation.png)

Un disco nativo 4K presenta i byte per settore e i byte per ogni campo di settore fisico entrambi impostati su 4096 come indicato di seguito:

![byte per settore e per settore fisico di un disco nativo 4K](images/4knativedisk.png)

> [!Note]  
> Se il campo byte per settore fisico non è supportato, il driver di archiviazione non supporta la \_ \_ proprietà query di archiviazione IOCTL \_ oppure si è verificato un errore durante il recupero delle informazioni.

 

## <a name="resources"></a>Risorse

-   [Dichiarazione del supporto generale di Windows](https://support.microsoft.com/kb/2510009)
-   [Microsoft KB 982018](https://support.microsoft.com/kb/982018)
-   [Microsoft KB 2553708](https://support.microsoft.com/kb/2553708)
-   [Hotfix per Windows 7 e Windows Server 2008 R2](https://support.microsoft.com/kb/982018)
-   [Hotfix per Windows Vista e Windows Server 2008](https://support.microsoft.com/kb/2553708)
-   [Istruzione di supporto HyperV](https://support.microsoft.com/kb/2515143)
-   [Informazioni generali sul codice di \_ \_ controllo delle proprietà di query di archiviazione IOCTL \_](/windows-hardware/drivers/ddi/ntddstor/ni-ntddstor-ioctl_storage_query_property)
-   [\_ \_ \_ Codice controllo proprietà query archiviazione IOCTL](/windows/win32/api/winioctl/ni-winioctl-ioctl_storage_query_property)
-   [Informazioni generali sulla struttura del \_ \_ descrittore di allineamento dell'accesso di archiviazione \_](/windows-hardware/drivers/ddi/ntddstor/ns-ntddstor-_storage_access_alignment_descriptor)
-   [Descrizione della terminologia standard utilizzata per descrivere gli aggiornamenti software Microsoft](https://support.microsoft.com/kb/824684/)
-   [Esempio di codice WDK con informazioni dettagliate su come estrarre le informazioni di allineamento dell'accesso di archiviazione segnalate dalla struttura del descrittore di accesso alla risorsa di archiviazione \_ \_ \_ quando si effettua una chiamata al \_ codice di controllo delle proprietà della query di archiviazione IOCTL \_ \_](/windows/win32/api/winioctl/ns-winioctl-storage_access_alignment_descriptor)
-   [Informazioni generali sulle opzioni di Command-Line di ImageX](/previous-versions/windows/it-pro/windows-7/dd799302(v=ws.10))
-   [Requisiti del driver del chipset Intel per supportare unità di settore a 4 KB](https://www.intel.com/support/chipsets/imsm/sb/CS-031502.htm)

 

