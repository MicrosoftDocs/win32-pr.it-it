---
description: Vengono descritti due tipi di archiviazione su disco e vengono descritti gli stili di partizione.
ms.assetid: 5d511654-92e0-4236-80e7-bb2417403186
title: Dischi di base e dinamici
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd3b52767983c7707f619b83c93e987b51879fdd
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "103968984"
---
# <a name="basic-and-dynamic-disks"></a>Dischi di base e dinamici

Prima di partizionare un'unità o ottenere informazioni sul layout della partizione di un'unità, è necessario innanzitutto comprendere le funzionalità e le limitazioni dei tipi di archiviazione su disco di base e dinamica.

Ai fini di questo argomento, il termine *volume* viene usato per fare riferimento al concetto di partizione disco formattato con un file System valido, più comunemente NTFS, usato dal sistema operativo Windows per archiviare i file. Un volume ha un nome di percorso Win32, può essere enumerato dalle funzioni [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew) e [**FindNextVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew) e in genere ha una lettera di unità assegnata, ad esempio C:. Per ulteriori informazioni sui volumi e sui file System, vedere [file System](file-systems.md).

In questo argomento

-   [Dischi di base](#basic-disks)
-   [Dischi dinamici](#dynamic-disks)
-   [Stili partizione](#partition-styles)
    -   [record di avvio principale](#master-boot-record)
    -   [tabella delle partizioni GUID](#guid-partition-table)
-   [Rilevamento del tipo di disco](#detecting-the-type-of-disk)
-   [Argomenti correlati](#related-topics)

Esistono due tipi di dischi quando si fa riferimento ai tipi di archiviazione in questo contesto: *dischi di base* e *dischi dinamici*. Si noti che i tipi di archiviazione descritti in questo articolo non sono gli stessi dei dischi fisici o degli stili di partizione, che sono concetti correlati ma distinti. Il riferimento a un disco di base, ad esempio, non implica un particolare stile di partizione, ma è necessario specificare anche lo stile della partizione usato per il disco in discussione. Per una descrizione semplificata del modo in cui un tipo di archiviazione su disco di base è correlato a un disco rigido fisico, vedere [dispositivi e partizioni disco](disk-devices-and-partitions.md).

## <a name="basic-disks"></a>Dischi di base

I *dischi di base* sono i tipi di archiviazione usati più spesso con Windows. Il termine *disco di base* fa riferimento a un disco che contiene partizioni, come le partizioni primarie e le unità logiche, che a loro volta vengono in genere formattate con un file System per diventare un volume per l'archiviazione di file. I dischi di base forniscono una soluzione di archiviazione semplice in grado di supportare una vasta gamma di scenari di requisiti di archiviazione mutevoli. I dischi di base supportano anche dischi cluster, dischi IEEE (Institute of Electrical and Electronics Engineers) 1394 e unità rimovibili USB (Universal Serial Bus). Per compatibilità con le versioni precedenti, i dischi di base usano in genere lo stesso stile di partizione MBR (master boot record) dei dischi usati dal sistema operativo Microsoft MS-DOS e tutte le versioni di Windows, ma possono anche supportare partizioni GPT ( **GUID** Partition Table) nei sistemi che la supportano. Per altre informazioni sugli stili di partizione MBR e GPT, vedere la sezione [stili di partizione](#partition-styles) .

È possibile aggiungere spazio a unità logiche e partizioni primarie esistenti estendendole nello spazio adiacente, contiguo non allocato sullo stesso disco. Per estendere un volume di base, deve essere formattato con il file system NTFS. È possibile estendere un'unità logica all'interno di spazio libero contiguo nella partizione estesa che lo contiene. Se si estende un'unità logica oltre lo spazio libero disponibile nella partizione estesa, la partizione estesa cresce per contenere l'unità logica, purché la partizione estesa venga seguita da spazio non allocato contiguo. Per altre informazioni, vedere funzionamento di [dischi e volumi di base](/previous-versions/windows/it-pro/windows-server-2003/cc739412(v=ws.10)).

È possibile eseguire le operazioni seguenti solo sui dischi di base:

-   Creare ed eliminare partizioni primarie ed estese.
-   Creare ed eliminare unità logiche all'interno di una partizione estesa.
-   Formattare una partizione e contrassegnarla come attiva.

## <a name="dynamic-disks"></a>Dischi dinamici

> [!NOTE]
> Per tutti gli utilizzi tranne i volumi di avvio speculare (usando un volume mirror per ospitare il sistema operativo), i dischi dinamici sono deprecati. Per i dati che richiedono resilienza in caso di errore dell'unità, usare spazi di archiviazione, una soluzione di virtualizzazione dell'archiviazione resiliente. Per altre informazioni, vedere [Panoramica di spazi di archiviazione](/windows-server/storage/storage-spaces/overview).

I *dischi dinamici* forniscono funzionalità non disponibili per i dischi di base, ad esempio la possibilità di creare volumi che si estendono su più dischi (volumi con spanning e con striping) e la possibilità di creare volumi a tolleranza d'errore (volumi con mirroring e RAID-5). Come i dischi di base, i dischi dinamici possono usare gli stili di partizione MBR o GPT nei sistemi che supportano entrambi. Tutti i volumi sui dischi dinamici sono noti come volumi dinamici. I dischi dinamici offrono maggiore flessibilità per la gestione dei volumi poiché utilizzano un database per tenere traccia delle informazioni sui volumi dinamici sul disco e sugli altri dischi dinamici nel computer. Poiché ogni disco dinamico in un computer archivia una replica del database del disco dinamico, ad esempio, un database del disco dinamico danneggiato può ripristinare un disco dinamico utilizzando il database in un altro disco dinamico. Il percorso del database è determinato dallo stile della partizione del disco. Nelle partizioni MBR il database è contenuto negli ultimi 1 megabyte (MB) del disco. Nelle partizioni GPT il database è contenuto in una partizione riservata (nascosta) da 1 MB.

I dischi dinamici sono una forma separata di gestione dei volumi che consente ai volumi di avere extent non contigui in uno o più dischi fisici. I dischi e i volumi dinamici si basano su Gestione dischi logici (LDM) e sul servizio dischi virtuali (VDS) e sulle relative funzionalità associate. Queste funzionalità consentono di eseguire attività quali la conversione dei dischi di base in dischi dinamici e la creazione di volumi a tolleranza di errore. Per incoraggiare l'uso di dischi dinamici, il supporto del volume multipartizione è stato rimosso dai dischi di base ed è ora supportato esclusivamente su dischi dinamici.

È possibile eseguire le operazioni seguenti solo sui dischi dinamici:

-   Creazione ed eliminazione di volumi semplici, con spanning, con striping, con mirroring e RAID-5.
-   Estendere un volume semplice o con spanning.
-   Rimuovere un mirror da un volume con mirroring o suddividere il volume con mirroring in due volumi.
-   Ripristinare i volumi con mirroring o RAID-5.
-   Riattivare un disco mancante o offline.

Un'altra differenza tra i dischi di base e quelli dinamici è che i volumi di dischi dinamici possono essere composti da un set di extent non contigui in uno o più dischi fisici. Al contrario, un volume su un disco di base è costituito da un set di extent contigui in un singolo disco. A causa della posizione e della dimensione dello spazio su disco necessario per il database LDM, Windows non è in grado di convertire un disco di base in un disco dinamico, a meno che non sia presente almeno 1 MB di spazio inutilizzato sul disco.

Indipendentemente dal fatto che i dischi dinamici in un sistema usino lo stile di partizione MBR o GPT, è possibile creare fino a 2.000 volumi dinamici in un sistema, anche se il numero consigliato di volumi dinamici è 32 o meno. Per informazioni dettagliate e altre considerazioni sull'uso di dischi e volumi dinamici, vedere [dischi e volumi dinamici](/previous-versions/windows/it-pro/windows-server-2003/cc757696(v=ws.10)).

Per altre funzionalità e scenari di utilizzo per i dischi dinamici, vedere [che cosa sono i dischi e i volumi dinamici?](/previous-versions/windows/it-pro/windows-server-2003/cc737048(v=ws.10)).

Le operazioni comuni ai dischi di base e dinamici sono le seguenti:

-   Supportano gli stili di partizione MBR e GPT.
-   Controllare le proprietà del disco, ad esempio capacità, spazio libero disponibile e stato corrente.
-   Visualizzare le proprietà della partizione, ad esempio offset, lunghezza, tipo e se la partizione può essere utilizzata come volume di sistema all'avvio.
-   Visualizzare le proprietà del volume, ad esempio le dimensioni, l'assegnazione di lettere di unità, l'etichetta, il tipo, il nome del percorso Win32, il tipo di partizione e file system.
-   Definire le assegnazioni di lettere di unità per volumi o partizioni disco e per i dispositivi CD-ROM.
-   Convertire un disco di base in un disco dinamico o un disco dinamico in un disco di base.

Se non specificato diversamente, Windows inizialmente partiziona un'unità come disco di base per impostazione predefinita. È necessario convertire in modo esplicito un disco di base in un disco dinamico. Tuttavia, esistono considerazioni sullo spazio su disco che è necessario tenere in considerazione prima di provare a eseguire questa operazione. Per ulteriori informazioni, vedere [How to Convert to Basic and Dynamic disks in Windows XP Professional](https://support.microsoft.com/kb/309044).

## <a name="partition-styles"></a>Stili partizione

Gli *stili di partizione*, detti anche schemi di *partizione*, sono un termine che fa riferimento alla particolare struttura sottostante del layout del disco e al modo in cui il partizionamento è effettivamente disposto, le funzionalità sono e anche le limitazioni. Per avviare Windows, le implementazioni del BIOS nei computer basati su x86 e x64 richiedono un disco di base che deve contenere almeno una partizione MBR (master boot record) contrassegnata come attiva, in cui le informazioni sul sistema operativo Windows (ma non necessariamente sull'intera installazione del sistema operativo) e sulla posizione in cui vengono archiviate le informazioni sulle partizioni sul disco. Queste informazioni vengono inserite in posizioni separate e queste due posizioni possono trovarsi in partizioni separate o in una singola partizione. Tutti gli altri tipi di archiviazione su disco fisico possono essere configurati come diverse combinazioni dei due stili di partizione disponibili, descritti nelle sezioni riportate di seguito. Per ulteriori informazioni su altri tipi di sistema, vedere l'argomento TechNet sugli [stili di partizione](/previous-versions/windows/it-pro/windows-server-2003/cc738081(v=ws.10)).

I dischi dinamici seguono scenari di utilizzo leggermente diversi, come descritto in precedenza, e il modo in cui usano i due stili di partizione è influenzato da tale uso. Poiché i dischi dinamici non vengono in genere usati per contenere volumi di avvio del sistema, questa discussione è semplificata per escludere scenari con casi particolari. Per informazioni più dettagliate sui layout dei blocchi di dati delle partizioni e sugli scenari di utilizzo dei dischi di base o dinamici correlati agli stili di partizione, vedere [come funzionano i dischi](/previous-versions/windows/it-pro/windows-server-2003/cc739412(v=ws.10)) e i volumi di base e [come funzionano i dischi e i volumi dinamici](/previous-versions/windows/it-pro/windows-server-2003/cc758035(v=ws.10)).

### <a name="master-boot-record"></a>record di avvio principale

Tutti i computer basati su x86 e x64 che eseguono Windows possono utilizzare lo stile di partizione noto come MBR ( *master boot record* ). Lo stile di partizione MBR contiene una tabella di partizione che descrive la posizione in cui si trovano le partizioni sul disco. Poiché MBR è l'unico stile di partizione disponibile nei computer basati su x86 precedenti a Windows Server 2003 con Service Pack 1 (SP1), non è necessario scegliere questo stile. Viene usato automaticamente.

È possibile creare fino a quattro partizioni in un disco di base usando lo schema di partizione MBR, ovvero quattro partizioni primarie o tre primarie e una estesa. La partizione estesa può contenere una o più unità logiche. La figura seguente illustra un layout di esempio di tre partizioni primarie e una partizione estesa su un disco di base con MBR. La partizione estesa contiene quattro unità logiche estese al suo interno. La partizione estesa può essere o non trovarsi alla fine del disco, ma è sempre un singolo spazio contiguo per le unità logiche 1-n.

![tre partizioni primarie e una partizione estesa su un disco di base con MBR](images/basic-mbr.png)

Ogni partizione, sia primaria che estesa, può essere formattata come volume di Windows, con una correlazione uno-a-uno tra volume e partizione. In altre parole, una singola partizione non può contenere più di un singolo volume. In questo esempio sarà disponibile un totale di sette volumi per l'archiviazione di file in Windows. Una partizione non formattata non è disponibile per l'archiviazione di file in Windows.

Il layout MBR del disco dinamico ha un aspetto molto simile al layout MBR del disco di base, ad eccezione del fatto che è consentita una sola partizione primaria (definita partizione LDM), non è consentito alcun partizionamento esteso ed è presente una partizione nascosta alla fine del disco per il database LDM. Per ulteriori informazioni su LDM, vedere la sezione relativa ai [dischi dinamici](#basic-and-dynamic-disks) .

### <a name="guid-partition-table"></a>tabella delle partizioni GUID

I sistemi che eseguono Windows Server 2003 con SP1 e versioni successive possono usare uno stile di partizione noto come tabella di partizione **GUID**(Globally Unique Identifier) (GPT), oltre allo stile di partizione MBR. Un disco di base con lo stile di partizione GPT può avere fino a 128 partizioni primarie, mentre i dischi dinamici avranno una singola partizione LDM come con il partizionamento MBR. Poiché i dischi di base che usano il partizionamento GPT non limitano l'utente a quattro partizioni, non è necessario creare partizioni estese o unità logiche.

Lo stile di partizione GPT presenta anche le proprietà seguenti:

-   Consente partizioni di dimensioni superiori a 2 terabyte.
-   Aggiunta dell'affidabilità dalla replica e dalla protezione del controllo di ridondanza ciclico (CRC) della tabella di partizione.
-   Supporto per altri tipi di partizioni **GUID** definiti da OEM (Original Equipment Manufacturer), fornitori di software indipendenti (ISV) e altri sistemi operativi.

Il layout di partizionamento GPT per un disco di base è illustrato nella figura seguente.

![layout GPT](images/basic-gpt.png)

L'area MBR di protezione esiste in un layout di partizione GPT per la compatibilità con le versioni precedenti delle utilità di gestione del disco che operano su MBR. L'intestazione GPT definisce l'intervallo di indirizzi dei blocchi logici utilizzabili dalle voci della partizione. L'intestazione GPT definisce anche la relativa posizione sul disco, il **GUID** e un checksum CRC32 (ciclica di ridondanza) a 32 bit utilizzato per verificare l'integrità dell'intestazione GPT. Ogni voce di partizione **GUID** inizia con un GUID di tipo di partizione. Il **GUID** del tipo di partizione a 16 byte, che è simile a un ID di sistema nella tabella delle partizioni di un disco MBR, identifica il tipo di dati contenuti nella partizione e identifica la modalità di utilizzo della partizione, ad esempio se si tratta di un disco di base o di un disco dinamico. Si noti che ogni voce della partizione **GUID** ha una copia di backup.

I layout di partizione **GPT** del disco dinamico hanno un aspetto simile a questo esempio di disco di base, ma come indicato in precedenza è presente una sola voce di partizione LDM anziché 1-n partizioni primarie come consentito nei dischi di base. Esiste anche una partizione di database LDM nascosta con una corrispondente voce di partizione **GUID** . Per ulteriori informazioni su LDM, vedere la sezione relativa ai [dischi dinamici](#basic-and-dynamic-disks) .

## <a name="detecting-the-type-of-disk"></a>Rilevamento del tipo di disco

Non esiste alcuna funzione specifica per rilevare a livello di codice il tipo di disco su cui si trova un file o una directory specifica. Esiste un metodo indiretto.

* Passare il percorso del file o della directory a [**GetVolumePathName**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumepathnamew) per ottenere il punto di montaggio.
* Passare il punto di montaggio a [**GetVolumeNameForVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) per ottenere il nome del volume.
* Rimuovere la barra rovesciata finale dal nome del volume.
* Passare il nome del volume senza la barra rovesciata finale a [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) per aprire il volume.
* Usare il volume [**IOCTL per \_ ottenere i volumi del \_ \_ \_ disco \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_volume_get_volume_disk_extents) con l'handle del volume per ottenere i numeri di disco.
* Usare i numeri di disco per costruire i percorsi del disco, ad esempio " \\ \\ ? \\ PhysicalDrive *X*".
* Passare ogni percorso del disco a [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) per aprire il disco.
* Per ottenere l'elenco delle partizioni, utilizzare [**IOCTL \_ disk \_ get \_ drive \_ layout \_ ex**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_disk_get_drive_layout_ex) .
* Controllare **PartitionType** per ogni voce nell'elenco delle partizioni.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sulla gestione dei volumi](about-volume-management.md)
</dt> <dt>

[Riferimento tecnico per dischi e volumi di base](/previous-versions/windows/it-pro/windows-server-2003/cc784732(v=ws.10))
</dt> <dt>

[Guida di riferimento tecnico ai dischi e ai volumi dinamici](/previous-versions/windows/it-pro/windows-server-2003/cc785638(v=ws.10))
</dt> <dt>

[Archiviazione di base rispetto all'archiviazione dinamica in Windows XP]( https://support.microsoft.com/kb/314343/)
</dt> </dl>

 

 
