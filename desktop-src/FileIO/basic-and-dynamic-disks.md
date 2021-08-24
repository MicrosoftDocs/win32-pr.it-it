---
description: Vengono descritti due tipi di archiviazione su disco e vengono illustrati gli stili di partizione.
ms.assetid: 5d511654-92e0-4236-80e7-bb2417403186
title: Dischi di base e dinamici
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f134f0dd7c8d81522733d26a6c5efb433d0e425978e1cbffd7edf3b0937b949
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119582632"
---
# <a name="basic-and-dynamic-disks"></a>Dischi di base e dinamici

Prima di partizionare un'unità o ottenere informazioni sul layout di partizione di un'unità, è necessario comprendere le funzionalità e le limitazioni dei tipi di archiviazione su disco di base e dinamico.

Ai fini di questo argomento, il termine *volume* viene usato per fare riferimento al concetto di partizione del disco formattata con un file system valido, in genere NTFS, usato dal sistema operativo Windows per archiviare i file. Un volume ha un nome di percorso Win32, può essere enumerato dalle funzioni [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew) e [**FindNextVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew) e in genere ha una lettera di unità assegnata, ad esempio C:. Per altre informazioni sui volumi e sui file system, vedere [File system](file-systems.md).

In questo argomento

-   [Dischi di base](#basic-disks)
-   [Dischi dinamici](#dynamic-disks)
-   [Stili di partizione](#partition-styles)
    -   [record di avvio principale](#master-boot-record)
    -   [tabella delle partizioni GUID](#guid-partition-table)
-   [Rilevamento del tipo di disco](#detecting-the-type-of-disk)
-   [Argomenti correlati](#related-topics)

Esistono due tipi di dischi quando si fa riferimento ai tipi di archiviazione in questo contesto: dischi *di base* e *dischi dinamici*. Si noti che i tipi di archiviazione illustrati qui non sono gli stessi dei dischi fisici o degli stili di partizione, che sono concetti correlati ma separati. Ad esempio, fare riferimento a un disco di base non implica uno stile di partizione specifico. È necessario specificare anche lo stile di partizione usato per il disco in corso di discussione. Per una descrizione semplificata della relazione tra un tipo di archiviazione su disco di base e un disco rigido fisico, vedere Dispositivi [e partizioni del disco](disk-devices-and-partitions.md).

## <a name="basic-disks"></a>Dischi di base

*I dischi di base* sono i tipi di archiviazione più usati con Windows. Il termine *disco* di base si riferisce a un disco che contiene partizioni, ad esempio partizioni primarie e unità logiche, che a loro volta sono in genere formattati con un file system per diventare un volume per l'archiviazione file. I dischi di base offrono una semplice soluzione di archiviazione in grado di supportare un'utile gamma di scenari di requisiti di archiviazione che cambiano. I dischi di base supportano anche dischi in cluster, dischi IEEE (Institute of Electrical and Electronics Engineers) 1394 e unità rimovibili USB (Universal Serial Bus). Per la compatibilità con le versioni precedenti, i dischi di base usano in genere lo stesso stile di partizione MBR (Master Boot Record) dei dischi usati dal sistema operativo Microsoft MS-DOS e tutte le versioni di Windows, ma possono anche supportare partizioni GPT **(GUID** Partition Table) nei sistemi che lo supportano. Per altre informazioni sugli stili di partizione MBR e GPT, vedere la sezione [Stili di](#partition-styles) partizione.

È possibile aggiungere spazio a unità logiche e partizioni primarie esistenti estendendole nello spazio adiacente, contiguo non allocato sullo stesso disco. Per estendere un volume di base, deve essere formattato con il file system NTFS. È possibile estendere un'unità logica all'interno di spazio libero contiguo nella partizione estesa che lo contiene. Se si estende un'unità logica oltre lo spazio libero disponibile nella partizione estesa, la partizione estesa cresce per contenere l'unità logica, purché la partizione estesa venga seguita da spazio non allocato contiguo. Per altre informazioni, vedere [Funzionamento di dischi e volumi di base.](/previous-versions/windows/it-pro/windows-server-2003/cc739412(v=ws.10))

Le operazioni seguenti possono essere eseguite solo su dischi di base:

-   Creare ed eliminare partizioni primarie ed estese.
-   Creare ed eliminare unità logiche all'interno di una partizione estesa.
-   Formattare una partizione e contrassegnarla come attiva.

## <a name="dynamic-disks"></a>Dischi dinamici

> [!NOTE]
> Per tutti gli utilizzi, ad eccezione dei volumi di avvio mirror (che usano un volume mirror per ospitare il sistema operativo), i dischi dinamici sono deprecati. Per i dati che richiedono resilienza in caso di errore dell'unità, usare Spazi di archiviazione, una soluzione di virtualizzazione dell'archiviazione resiliente. Per altre informazioni, vedere panoramica [Spazi di archiviazione.](/windows-server/storage/storage-spaces/overview)

 I dischi dinamici offrono funzionalità non supportate dai dischi di base, ad esempio la possibilità di creare volumi che si estendono su più dischi (volumi con spanning e con striping) e la possibilità di creare volumi a tolleranza di errore (volumi con mirroring e RAID-5). Analogamente ai dischi di base, i dischi dinamici possono usare gli stili di partizione MBR o GPT nei sistemi che supportano entrambi. Tutti i volumi nei dischi dinamici sono noti come volumi dinamici. I dischi dinamici offrono una maggiore flessibilità per la gestione dei volumi perché usano un database per tenere traccia delle informazioni sui volumi dinamici sul disco e su altri dischi dinamici nel computer. Poiché ogni disco dinamico in un computer archivia una replica del database del disco dinamico, ad esempio, un database su disco dinamico danneggiato può ripristinare un disco dinamico usando il database in un altro disco dinamico. Il percorso del database è determinato dallo stile di partizione del disco. Nelle partizioni MBR il database è contenuto negli ultimi 1 MEGABYTE (MB) del disco. Nelle partizioni GPT il database è contenuto in una partizione riservata (nascosta) da 1 MB.

I dischi dinamici sono una forma separata di gestione dei volumi che consente ai volumi di avere extent non contigui in uno o più dischi fisici. I dischi dinamici e i volumi si basano su Logical Disk Manager (LDM) e virtual disk service (VDS) e sulle relative funzionalità associate. Queste funzionalità consentono di eseguire attività quali la conversione di dischi di base in dischi dinamici e la creazione di volumi a tolleranza di errore. Per favorire l'uso di dischi dinamici, il supporto di volumi multi-partizione è stato rimosso dai dischi di base ed è ora supportato esclusivamente sui dischi dinamici.

Le operazioni seguenti possono essere eseguite solo su dischi dinamici:

-   Creare ed eliminare volumi semplici, con spanning, con striping, con mirroring e RAID-5.
-   Estendere un volume semplice o con spanning.
-   Rimuovere un mirror da un volume con mirroring o suddividere il volume con mirroring in due volumi.
-   Ripristinare volumi con mirroring o RAID-5.
-   Riattivare un disco mancante o offline.

Un'altra differenza tra dischi di base e dinamici è che i volumi di dischi dinamici possono essere costituiti da un set di extent non contigui in uno o più dischi fisici. Al contrario, un volume in un disco di base è costituito da un set di extent contigui in un singolo disco. A causa della posizione e delle dimensioni dello spazio su disco necessario per il database LDM, Windows non può convertire un disco di base in un disco dinamico a meno che non ci siano almeno 1 MB di spazio inutilizzato sul disco.

Indipendentemente dal fatto che i dischi dinamici in un sistema usino lo stile di partizione MBR o GPT, è possibile creare fino a 2.000 volumi dinamici in un sistema, anche se il numero consigliato di volumi dinamici è 32 o inferiore. Per informazioni dettagliate e altre considerazioni sull'uso di dischi e volumi dinamici, vedere [Dischi e volumi dinamici](/previous-versions/windows/it-pro/windows-server-2003/cc757696(v=ws.10)).

Per altre funzionalità e scenari di utilizzo per i dischi dinamici, vedere [Che cosa sono i dischi dinamici e i volumi?](/previous-versions/windows/it-pro/windows-server-2003/cc737048(v=ws.10)).

Le operazioni comuni ai dischi di base e dinamici sono le seguenti:

-   Supporta gli stili di partizione MBR e GPT.
-   Controllare le proprietà del disco, ad esempio la capacità, lo spazio disponibile e lo stato corrente.
-   Visualizzare le proprietà della partizione, ad esempio offset, lunghezza, tipo e se la partizione può essere usata come volume di sistema all'avvio.
-   Visualizzare le proprietà del volume, ad esempio dimensioni, assegnazione lettera di unità, etichetta, tipo, nome percorso Win32, tipo di partizione e file system.
-   Stabilire assegnazioni di lettere di unità per volumi o partizioni del disco e per i dispositivi CD-ROM.
-   Convertire un disco di base in un disco dinamico o un disco dinamico in un disco di base.

Se non diversamente specificato, Windows partiziona inizialmente un'unità come disco di base per impostazione predefinita. È necessario convertire in modo esplicito un disco di base in un disco dinamico. Tuttavia, è necessario tenere conto dello spazio su disco prima di provare a eseguire questa operazione. Per altre informazioni, vedere [How to Convert to Basic and Dynamic Disks in Windows XP Professional](https://support.microsoft.com/kb/309044).

## <a name="partition-styles"></a>Stili di partizione

Gli stili di *partizione,* chiamati anche schemi di *partizione,* sono un termine che fa riferimento alla particolare struttura sottostante del layout del disco e al modo in cui il partizionamento viene effettivamente organizzato, quali sono le funzionalità e quali sono le limitazioni. Per avviare Windows, le implementazioni del BIOS nei computer basati su x86 e x64 richiedono un disco di base che deve contenere almeno una partizione MBR (Master Boot Record) contrassegnata come attiva in cui vengono archiviate le informazioni sul sistema operativo Windows (ma non necessariamente l'intera installazione del sistema operativo) e le informazioni sulle partizioni del disco. Queste informazioni vengono inserite in posizioni separate e queste due posizioni possono trovarsi in partizioni separate o in una singola partizione. Tutte le altre risorse di archiviazione su disco fisico possono essere impostate come varie combinazioni dei due stili di partizione disponibili, descritte nelle sezioni seguenti. Per altre informazioni su altri tipi di sistema, vedere l'argomento TechNet sugli [stili di partizione](/previous-versions/windows/it-pro/windows-server-2003/cc738081(v=ws.10)).

I dischi dinamici seguono scenari di utilizzo leggermente diversi, come descritto in precedenza, e il modo in cui utilizzano i due stili di partizione è influenzato da tale utilizzo. Poiché i dischi dinamici non vengono in genere usati per contenere volumi di avvio del sistema, questa discussione viene semplificata per escludere scenari specifici. Per informazioni più dettagliate sui layout dei blocchi di dati di partizione [](/previous-versions/windows/it-pro/windows-server-2003/cc739412(v=ws.10)) e sugli scenari di utilizzo di dischi di base o dinamici correlati agli stili di partizione, vedere Funzionamento di dischi e volumi di base e Funzionamento di dischi e volumi [dinamici](/previous-versions/windows/it-pro/windows-server-2003/cc758035(v=ws.10)).

### <a name="master-boot-record"></a>record di avvio principale

Tutti i computer basati su x86 e x64 che eseguono Windows possono usare lo stile di partizione noto come record di avvio *master* (MBR). Lo stile di partizione MBR contiene una tabella di partizione che descrive dove si trovano le partizioni sul disco. Poiché MBR è l'unico stile di partizione disponibile nei computer basati su x86 prima di Windows Server 2003 con Service Pack 1 (SP1), non è necessario scegliere questo stile. Viene usato automaticamente.

È possibile creare fino a quattro partizioni in un disco di base usando lo schema di partizione MBR: quattro partizioni primarie o tre partizioni primarie e una estesa. La partizione estesa può contenere una o più unità logiche. La figura seguente illustra un layout di esempio di tre partizioni primarie e di una partizione estesa in un disco di base tramite MBR. La partizione estesa contiene quattro unità logiche estese al suo interno. La partizione estesa può trovarsi o meno alla fine del disco, ma è sempre un singolo spazio contiguo per le unità logiche da 1 a n.

![tre partizioni primarie e una partizione estesa in un disco di base usando mbr](images/basic-mbr.png)

Ogni partizione, primaria o estesa, può essere formattata come volume Windows, con una correlazione uno-a-uno tra volume e partizione. In altre parole, una singola partizione non può contenere più di un singolo volume. In questo esempio sono disponibili in totale sette volumi per l Windows per l'archiviazione di file. Una partizione non formattata non è disponibile per l'archiviazione file in Windows.

Il layout MBR del disco dinamico è molto simile al layout MBR del disco di base, ad eccezione del fatto che è consentita una sola partizione primaria (denominata partizione LDM), non è consentito il partizionamento esteso e alla fine del disco è presente una partizione nascosta per il database LDM. Per altre informazioni su LDM, vedere la [sezione Dischi](#basic-and-dynamic-disks) dinamici.

### <a name="guid-partition-table"></a>tabella delle partizioni GUID

I sistemi che eseguono Windows Server 2003 con SP1 e versioni successivepossono usare uno stile di partizione noto come gpt (globally unique identifier) partition table (GPT) oltre allo stile di partizione MBR. Un disco di base che usa lo stile di partizione GPT può avere fino a 128 partizioni primarie, mentre i dischi dinamici avranno una singola partizione LDM come con il partizionamento MBR. Poiché i dischi di base che usano il partizionamento GPT non si limitano a quattro partizioni, non è necessario creare partizioni estese o unità logiche.

Lo stile di partizione GPT ha anche le proprietà seguenti:

-   Consente partizioni di dimensioni superiori a 2 terabyte.
-   Maggiore affidabilità dalla replica e dalla protezione CRC (cyclic redundancy check) della tabella di partizione.
-   Supporto per guid di tipo di **partizione** aggiuntivi definiti da original equipment manufacturers (OEM), fornitori di software indipendenti (ISV) e altri sistemi operativi.

Il layout di partizionamento GPT per un disco di base è illustrato nella figura seguente.

![layout gpt](images/basic-gpt.png)

L'area MBR protetta esiste in un layout di partizione GPT per la compatibilità con le versioni precedenti delle utilità di gestione del disco che operano su MBR. L'intestazione GPT definisce l'intervallo di indirizzi di blocchi logici utilizzabili dalle voci di partizione. L'intestazione GPT definisce anche la posizione sul disco, il **GUID** e un controllo di ridondanza ciclico a 32 bit (CRC32) usato per verificare l'integrità dell'intestazione GPT. Ogni **voce di** partizione GUID inizia con un GUID del tipo di partizione. Il GUID del tipo di partizione a 16 byte, simile a un **ID** di sistema nella tabella delle partizioni di un disco MBR, identifica il tipo di dati contenuti nella partizione e identifica la modalità di utilizzo della partizione, ad esempio se si tratta di un disco di base o dinamico. Si noti che ogni **voce di** partizione GUID ha una copia di backup.

I layout delle **partizioni GPT** dei dischi dinamici sono simili a questo esempio di disco di base, ma come indicato in precedenza hanno una sola voce di partizione LDM anziché 1-n partizioni primarie consentite nei dischi di base. Esiste anche una partizione di database LDM nascosta con una voce di **partizione GUID** corrispondente. Per altre informazioni sul modello LDM, vedere la [sezione Dischi](#basic-and-dynamic-disks) dinamici.

## <a name="detecting-the-type-of-disk"></a>Rilevamento del tipo di disco

Non esiste alcuna funzione specifica per rilevare a livello di codice il tipo di disco in cui si trova un determinato file o directory. Esiste un metodo indiretto.

* Passare il percorso del file o della directory [**a GetVolumePathName per**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumepathnamew) ottenere il punto di montaggio.
* Passare il punto di montaggio [**a GetVolumeNameForVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) per ottenere il nome del volume.
* Rimuovere la barra rovesciata finale dal nome del volume.
* Passare il nome del volume senza la barra rovesciata finale a [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) per aprire il volume.
* Usare [**IOCTL \_ VOLUME GET VOLUME DISK \_ \_ \_ \_ EXTENTS con**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_volume_get_volume_disk_extents) l'handle di volume per ottenere i numeri di disco.
* Usare i numeri di disco per costruire i percorsi del disco, ad esempio " \\ \\ ? \\ PhysicalDrive *X*".
* Passare ogni percorso del disco [**a CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) per aprire il disco.
* Usare [**IOCTL \_ DISK GET DRIVE LAYOUT \_ \_ \_ \_ EX**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_disk_get_drive_layout_ex) per ottenere l'elenco delle partizioni.
* Controllare **PartitionType per** ogni voce nell'elenco delle partizioni.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sulla gestione dei volumi](about-volume-management.md)
</dt> <dt>

[Riferimento tecnico per dischi e volumi di base](/previous-versions/windows/it-pro/windows-server-2003/cc784732(v=ws.10))
</dt> <dt>

[Riferimento tecnico per dischi e volumi dinamici](/previous-versions/windows/it-pro/windows-server-2003/cc785638(v=ws.10))
</dt> <dt>

[Confronto tra Archiviazione base e Archiviazione dinamico in Windows XP]( https://support.microsoft.com/kb/314343/)
</dt> </dl>

 

 
