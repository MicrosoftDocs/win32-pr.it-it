---
description: Vengono descritte le considerazioni per il controllo dell'applicazione del buffering dei file, noto anche come input/output (I/O) file non memorizzato nel buffer.
ms.assetid: ae1e5d0f-9b55-4aae-8402-b9c8e33d9363
title: Buffer dei file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a44f6724622b2c3116fa24a6109efb6c0d9f1d9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233518"
---
# <a name="file-buffering"></a>Buffer dei file

In questo argomento vengono illustrate le varie considerazioni per il controllo delle applicazioni del buffering dei file, noto anche come input/output (I/O) file non memorizzato nel buffer. Il buffering dei file viene in genere gestito dal sistema dietro le quinte e viene considerato parte della [memorizzazione nella cache del file](file-caching.md) nel sistema operativo Windows, se non diversamente specificato. Sebbene i termini *caching* e *buffering* vengano talvolta utilizzati in modo intercambiabile, in questo argomento viene utilizzato il termine *buffering* specifico nel contesto di spiegazione della modalità di interazione con i dati che non vengono memorizzati nella cache (memorizzati nel buffer) dal sistema, in modo da evitare il controllo diretto delle applicazioni in modalità utente.

Quando si apre o si crea un file con la funzione [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) , non è possibile specificare il flag del **\_ \_ \_ buffer** per disabilitare la memorizzazione nella cache del sistema dei dati letti o scritti nel file. Sebbene ciò consenta il controllo completo e diretto del buffer di I/O dei dati, nel caso di file e dispositivi simili sono previsti requisiti di allineamento dei dati che devono essere presi in considerazione.

> [!Note]  
> Queste informazioni di allineamento sono valide per I/O nei dispositivi, ad esempio i file che supportano la ricerca e il concetto di puntatori alla posizione dei file (o *offset*). Per i dispositivi che non cercano, ad esempio le named pipe o i dispositivi di comunicazione, la disattivazione del buffer potrebbe non richiedere alcun allineamento particolare. Eventuali limitazioni o efficienze che possono essere ottenute tramite l'allineamento in questo caso dipendono dalla tecnologia sottostante.

 

In un semplice esempio, l'applicazione apre un file per l'accesso in scrittura con **il \_ flag file senza flag di \_ \_ buffering** e quindi esegue una chiamata alla funzione [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) usando un buffer di dati definito nell'applicazione. In queste circostanze, questo buffer locale è effettivamente l'unico buffer di file esistente per questa operazione. A causa del layout del disco fisico, del layout di archiviazione file system e del rilevamento della posizione del puntatore del file a livello di sistema, questa operazione di scrittura avrà esito negativo a meno che i buffer dei dati definiti localmente soddisfino determinati criteri di allineamento, descritti nella sezione seguente.

> [!Note]  
> La discussione sulla memorizzazione nella cache non prende in considerazione la memorizzazione nell'hardware del disco fisico, che non è necessariamente all'interno del controllo diretto del sistema in ogni caso. Questa operazione non ha alcun effetto sui requisiti specificati in questo argomento.

 

Per ulteriori informazioni su come **flag di file \_ \_ nessun \_ buffer** interagisce con altri flag correlati alla cache, vedere [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea).

## <a name="alignment-and-file-access-requirements"></a>Requisiti di allineamento e accesso ai file

Come descritto in precedenza, un'applicazione deve soddisfare determinati requisiti quando si lavora con i file aperti con il **flag di file \_ \_ senza \_ buffering**. Si applicano le seguenti specifiche:

-   Le dimensioni di accesso ai file, incluso l'offset del file facoltativo nella struttura [**sovrapposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) , se specificato, devono essere per un numero di byte che è un multiplo intero della dimensione del settore del volume. Se, ad esempio, le dimensioni del settore sono pari a 512 byte, un'applicazione può richiedere letture e scritture di 512, 1.024, 1.536 o 2.048 byte, ma non di 335, 981 o 7.171 byte.
-   Gli indirizzi del buffer di accesso ai file per le operazioni di lettura e scrittura devono essere allineati al settore fisico, ovvero allineati sugli indirizzi in memoria che sono multipli integer delle dimensioni del settore fisico del volume. A seconda del disco, questo requisito potrebbe non essere applicato.

Gli sviluppatori di applicazioni devono prendere nota dei nuovi tipi di dispositivi di archiviazione introdotti sul mercato con una dimensione di settore multimediale fisica di 4.096 byte. Il nome del settore per questi dispositivi è "formato avanzato". Poiché è possibile che si verifichino problemi di compatibilità con l'introduzione diretta di 4.096 byte come unità di indirizzamento per i supporti, una soluzione di compatibilità temporanea prevede l'introduzione di dispositivi che emulano un normale dispositivo di archiviazione settore a 512 byte, ma che rendono disponibili informazioni sulle reali dimensioni del settore tramite comandi ATA e SCSI standard.

In seguito a questa emulazione, esistono essenzialmente due dimensioni di settore che gli sviluppatori dovranno comprendere:

-   Settore logico: unità utilizzata per l'indirizzamento dei blocchi logici per il supporto. Possiamo anche considerarlo come la più piccola unità di scrittura che la risorsa di archiviazione può accettare. Si tratta dell'emulazione.
-   Settore fisico: unità per cui vengono completate le operazioni di lettura e scrittura nel dispositivo in un'unica operazione. Si tratta dell'unità di scrittura atomica e di quali elementi I/O non memorizzati nel buffer dovranno essere allineati per avere caratteristiche ottimali di prestazioni e affidabilità.

La maggior parte delle API Windows correnti, ad esempio [**IOCTL \_ disk \_ get \_ drive \_ Geometry**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_disk_get_drive_geometry) e [**GetDiskFreeSpace**](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespacea), restituirà le dimensioni del settore logico, ma le dimensioni del settore fisico possono essere recuperate tramite il codice di controllo della [**\_ proprietà della query di archiviazione \_ \_ IOCTL**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) , con le informazioni rilevanti contenute nel membro **BytesPerPhysicalSector** nella struttura del [**\_ \_ \_ descrittore di allineamento dell'accesso di archiviazione**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_access_alignment_descriptor) . Per un esempio, vedere il codice di esempio [**al \_ \_ \_ descrittore di allineamento dell'accesso di archiviazione**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_access_alignment_descriptor). Microsoft consiglia agli sviluppatori di allineare i/O senza buffer alle dimensioni del settore fisico come riportato dal codice di controllo **delle \_ \_ \_ proprietà di query di archiviazione IOCTL** per garantire la preparazione delle applicazioni per la transizione delle dimensioni del settore.

**Windows Server 2003 e Windows XP:** La struttura del [**\_ \_ \_ descrittore di allineamento dell'accesso di archiviazione**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_access_alignment_descriptor) non è disponibile. È stata introdotta con Windows Vista e Windows Server 2008.

Poiché gli indirizzi del buffer per le operazioni di lettura e scrittura devono essere allineati al settore, l'applicazione deve avere il controllo diretto del modo in cui vengono allocati i buffer. Un modo per allineare i buffer al settore consiste nell'utilizzare la funzione [**VirtualAlloc**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc) per allocare i buffer. Considerare quanto segue:

-   [**VirtualAlloc**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc) alloca memoria allineata agli indirizzi che sono multipli integer delle dimensioni di pagina del sistema. Le dimensioni della pagina sono di 4.096 byte in x64 e x86 o 8.192 byte per sistemi basati su Itanium. Per ulteriori informazioni, vedere la funzione [**GetSystemInfo**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) .
-   Le dimensioni del settore sono in genere da 512 a 4.096 byte per i dispositivi di archiviazione con accesso diretto (unità disco rigido) e 2.048 byte per CD-ROM.
-   Le dimensioni della pagina e del settore sono le potenze di 2.

Pertanto, nella maggior parte dei casi, la memoria allineata alla pagina sarà anche allineata a livello di settore, perché il caso in cui le dimensioni del settore sono maggiori delle dimensioni della pagina sono rare.

Un altro modo per ottenere buffer di memoria allineati manualmente consiste nell'usare la funzione di [ \_ \_ malloc allineata](/cpp/c-runtime-library/reference/aligned-malloc?view=vs-2019) dalla libreria Run-Time C. Per un esempio di come controllare manualmente l'allineamento del buffer, vedere l'esempio di codice del linguaggio C++ nella sezione di codice di esempio di [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile).

 

 
