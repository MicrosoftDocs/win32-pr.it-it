---
description: La deframmentazione è il processo di trasferimento di parti di file in un disco per deframmentare i file, ovvero il processo di trasferimento dei cluster di file su un disco per renderli contigui.
ms.assetid: 27ccaab7-ec89-489b-80dc-df9beb7969bc
title: Deframmentazione di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b2d079f58ec98f320356a477531616788f84ccb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880529"
---
# <a name="defragmenting-files"></a>Deframmentazione di file

Quando un file viene scritto su un disco, a volte il file non può essere scritto in cluster contigui. I cluster non contigui rallentano il processo di lettura e scrittura di un file. Oltre a un disco i cluster non contigui, il problema è peggiore, a causa del tempo necessario per spostare l'intestazione di lettura/scrittura di un'unità disco rigido. Un file con cluster non contigui è *frammentato*. Per ottimizzare i file per un accesso rapido, è possibile deframmentare un volume.

La *deframmentazione* è il processo di trasferimento di parti di file in un disco per deframmentare i file, ovvero il processo di trasferimento dei cluster di file su un disco per renderli contigui. Per altre informazioni, vedere le sezioni seguenti:

-   [Deframmentazione di un file](#defragmenting-a-file)
-   [Riduzione delle interazioni tra la deframmentazione e le copie shadow](#minimizing-interactions-between-defragmentation-and-shadow-copies)
-   [File, flussi e tipi di flusso supportati per la deframmentazione](#files-streams-and-stream-types-supported-for-defragmentation)

## <a name="defragmenting-a-file"></a>Deframmentazione di un file

In un semplice sistema operativo con singole attività, il software di deframmentazione è l'unica attività e non vi sono altri processi da leggere o scrivere sul disco. Tuttavia, in un sistema operativo multitasking, alcuni processi possono leggere e scrivere su un'unità disco rigido mentre un altro processo sta deframmentare tale unità disco rigido. Il trucco consiste nell'evitare scritture in un file da deframmentare senza arrestare il processo di scrittura per molto tempo. La risoluzione di questo problema non è semplice, ma è possibile.

Per consentire la deframmentazione senza richiedere una conoscenza approfondita di una struttura del disco file system, viene fornito un set di tre codici di controllo. I codici di controllo forniscono le funzionalità seguenti:

-   Consentire alle applicazioni di individuare i cluster vuoti
-   Determinare il percorso del disco dei cluster di file
-   Spostare i cluster in un disco

I codici di controllo gestiscono anche in modo trasparente il problema di inibire e consentire ad altri processi di leggere e scrivere nei file durante lo spostamento.

Queste operazioni possono essere eseguite senza impedire l'esecuzione di altri processi. Tuttavia, gli altri processi hanno tempi di risposta più lenti durante la deframmentazione di un'unità disco.

**Per deframmentare un file**

1.  Usare il codice di controllo [**bitmap di FSCTL \_ get \_ volume \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_volume_bitmap) per trovare una posizione nel volume sufficientemente grande da accettare un intero file.
    > [!Note]  
    > Se necessario, spostare altri file per creare una posizione sufficientemente grande. Idealmente, sono presenti cluster non allocati sufficienti dopo il primo extent del file che è possibile spostare in avanti nello spazio dopo il primo extent.

     

2.  Usare il codice di controllo [**\_ \_ \_ puntatori recupero FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_retrieval_pointers) per ottenere una mappa del layout corrente del file sul disco.
3.  Esaminare la struttura del [**\_ \_ buffer dei puntatori di recupero**](/windows/desktop/api/WinIoCtl/ns-winioctl-retrieval_pointers_buffer) restituita da FSCTL i [**\_ \_ \_ puntatori di recupero Get**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_retrieval_pointers).
4.  Usare il [**FSCTL \_ spostare \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_move_file) il codice di controllo file per spostare ogni cluster mentre si esamina la struttura.
    > [!Note]  
    > Potrebbe essere necessario rinnovare la bitmap o la struttura di recupero oppure entrambe le volte quando altri processi scrivono sul disco.

     

Due delle operazioni utilizzate nel processo di deframmentazione richiedono un handle per un volume. Solo gli amministratori possono ottenere un handle per un volume, in modo che solo gli amministratori possano deframmentare un volume. Un'applicazione deve verificare i diritti di un utente che tenta di eseguire software di deframmentazione e non deve consentire a un utente di deframmentare un volume se l'utente non dispone dei diritti appropriati.

Quando si utilizza [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) per aprire una directory durante la deframmentazione di un volume di file system FAT o FAT32, specificare il valore generico della maschera di accesso in **\_ lettura** . Non specificare il valore **massimo \_ consentito** per la maschera di accesso. L'accesso alla directory viene negato se questa operazione viene eseguita.

Non tentare di spostare i cluster allocati in un file system NTFS che si estendono oltre le dimensioni del file arrotondato del cluster, perché il risultato è un errore.

È possibile deframmentare i punti di analisi, le bitmap e gli elenchi di attributi in NTFS file system volumi, aperti per la lettura e la sincronizzazione, e denominati usando la sintassi *file*:*Name*:*Type* . ad esempio, *dirname*: $i 30: $index \_ allocation, *MRP*:: $DATA, *MRP*:: $REPARSE \_ Point e *MRP*:: $Attribute \_ List.

Quando si deframmentano volumi file system NTFS, la deframmentazione di un cluster virtuale oltre le dimensioni di allocazione di un file è consentita.

## <a name="minimizing-interactions-between-defragmentation-and-shadow-copies"></a>Riduzione delle interazioni tra la deframmentazione e le copie shadow

Quando possibile, spostare i dati in blocchi allineati l'uno rispetto all'altro in incrementi di 16 kilobyte (KB). In questo modo si riduce il sovraccarico di copia su scrittura quando le copie shadow sono abilitate, perché lo spazio della copia shadow aumenta e le prestazioni vengono ridotte quando si verificano le condizioni seguenti:

-   Le dimensioni del blocco della richiesta di spostamento sono inferiori o uguali a 16 KB.
-   Il Delta di spostamento non è in incrementi di 16 KB.

Il Delta di spostamento è il numero di byte tra l'inizio del blocco di origine e l'inizio del blocco di destinazione. In altre parole, un blocco a partire dall'offset X (su disco) può essere spostato in un offset iniziale Y se il valore assoluto di X meno Y è un multiplo pari a 16 KB. Quindi, supponendo che i cluster da 4 KB vengano ottimizzati, il passaggio dal cluster 3 al cluster 27 verrà ottimizzato, ma non sarà possibile passare dal cluster 18 al cluster 24. Si noti che mod (3, 4) = 3 = mod (27, 4). Viene scelto il mod 4 perché quattro cluster a 4 KB ciascuno equivale a 16 KB. Pertanto, un volume formattato in una dimensione del cluster da 16 KB comporterà l'ottimizzazione di tutti i file di spostamento.

Per ulteriori informazioni sulle copie shadow, vedere [servizio Copia Shadow del volume](/windows/desktop/VSS/about-the-volume-shadow-copy-service).

## <a name="files-streams-and-stream-types-supported-for-defragmentation"></a>File, flussi e tipi di flusso supportati per la deframmentazione

Sebbene la maggior parte dei file possa essere spostata usando il codice di controllo del [**\_ \_ file di spostamento FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_move_file) , non è possibile spostarli tutti. Di seguito è riportato l'elenco di file, flussi e tipi di flusso (detti anche codici di tipo di attributo) supportati dal **\_ \_ file di spostamento FSCTL**. Altri file, flussi e tipi di flusso non sono supportati dal **\_ \_ file di spostamento FSCTL**.

Tipi di flusso supportati per qualsiasi file o directory.

-   :: $DATA
-   elenco:: $ATTRIBUTE \_
-   :: \_ punto $REPARSE
-   :: $EA
-   flusso dell'utilità:: $LOGGED \_ \_

* * Windows 7, Windows Server 2008 R2, Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP: * *:: $EA e:: $LOGGED \_ flusso di utilità \_ non sono supportati prima di Windows 8 e windows Server 2012

Tipi di flusso supportati per qualsiasi directory.

-   :: $BITMAP
-   allocazione $INDEX:: \_

Di seguito sono riportati i tipi di file di sistema, di flusso e di flusso supportati dal [**\_ \_ file di spostamento FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_move_file) nel formato "*filename*:*streamName*: $*typeName*".

-   $MFT:: $DATA
-   elenco $MFT:: $ATTRIBUTE \_
-   $MFT:: $BITMAP
-   $AttrDef:: $DATA
-   Elenco $AttrDef:: $ATTRIBUTE \_
-   $Secure: $SDS: $DATA
-   Elenco $Secure:: $ATTRIBUTE \_
-   $Secure: $SDH: \_ allocazione $index
-   $Secure: $SDH: $BITMAP
-   $Secure: $SII: \_ allocazione $index
-   $Secure: $SII: $BITMAP
-   $UpCase:: $DATA
-   Elenco $UpCase:: $ATTRIBUTE \_
-   $Extend: $I 30: \_ allocazione $index
-   Elenco $Extend:: $ATTRIBUTE \_
-   $Extend: $I 30: $BITMAP
-   $Extend \\ $UsnJrnl: $J: $data
-   \\Elenco $Extend $UsnJrnl:: $Attribute \_
-   $Extend \\ $UsnJrnl: $max: $data
-   $Extend \\ $quota: $Q: $index \_ allocazione
-   \\Elenco $Extend $quota:: $Attribute \_
-   $Extend \\ $quota: $Q: $bitmap
-   $Extend \\ $quota: $O: $index \_ allocazione
-   $Extend \\ $quota: $O: $bitmap
-   $Extend \\ $objid: $O: $index \_ allocazione
-   \\Elenco $Extend $ObjId:: $Attribute \_
-   $Extend \\ $objid: $O: $bitmap
-   $Extend \\ $reparse: $R: $index \_ allocazione
-   \\Elenco $Extend $reparse:: $Attribute \_
-   $Extend \\ $reparse: $R: $bitmap
-   $Extend \\ $RmMetadata: $I 30: $index \_ allocazione
-   $Extend \\ $RmMetadata: $I 30: $bitmap
-   \\Elenco $Extend $RmMetadata:: $Attribute \_
-   $Extend \\ $RmMetadata \\ $Repair:: $data
-   $Extend \\ $RmMetadata \\ elenco $Repair:: $Attribute \_
-   $Extend \\ $RmMetadata \\ $Repair: $Config: $data
-   $Extend \\ $RmMetadata \\ $Txf: $I 30: $index \_ allocazione
-   $Extend \\ $RmMetadata \\ elenco $TXF:: $Attribute \_
-   $Extend \\ $RmMetadata \\ $Txf: $I 30: $bitmap
-   $Extend \\ $RmMetadata \\ $TXF: \_ dati $TXF: flusso dell'utilità di $logged \_ \_
-   $Extend \\ $RmMetadata \\ $TxfLog: $I 30: $index \_ allocazione
-   $Extend \\ $RmMetadata \\ elenco $txflog:: $Attribute \_
-   $Extend \\ $RmMetadata \\ $TxfLog: $I 30: $bitmap
-   $Extend \\ $RmMetadata \\ $txflog \\ $Tops:: $data
-   $Extend \\ $RmMetadata \\ $TxfLog \\ elenco $Tops:: $Attribute \_
-   $Extend \\ $RmMetadata \\ $txflog \\ $Tops: $T: $data
-   $Extend \\ $RmMetadata \\ $txflog \\ $txflog. blf:: $data
-   $Extend \\ $RmMetadata \\ $TxfLog \\ elenco $txflog. blf:: $Attribute \_

 

 
