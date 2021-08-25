---
description: La deframmentazione è il processo di spostamento di parti di file su un disco per deframmentare i file, cio' il processo di spostamento dei cluster di file su un disco per renderli contigui.
ms.assetid: 27ccaab7-ec89-489b-80dc-df9beb7969bc
title: Deframmentazione di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f04c0a3c961854b7e3ecab50d67db608178393113ca259b916db9623058e2f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119696291"
---
# <a name="defragmenting-files"></a>Deframmentazione di file

Quando un file viene scritto su disco, talvolta il file non può essere scritto in cluster contigui. I cluster non contigui rallentano il processo di lettura e scrittura di un file. Più a parte su un disco, i cluster non contigui sono, peggiorando il problema, a causa del tempo necessario per spostare l'head di lettura/scrittura di un'unità disco rigido. Un file con cluster non contigui è *frammentato.* Per ottimizzare i file per l'accesso rapido, è possibile deframmentare un volume.

*La deframmentazione* è il processo di spostamento di parti di file su un disco per deframmentare i file, cio' il processo di spostamento dei cluster di file su un disco per renderli contigui. Per altre informazioni, vedere le sezioni seguenti:

-   [Deframmentazione di un file](#defragmenting-a-file)
-   [Riduzione al minimo delle interazioni tra deframmentazione e copie shadow](#minimizing-interactions-between-defragmentation-and-shadow-copies)
-   [File, flussi e tipi di flusso supportati per la deframmentazione](#files-streams-and-stream-types-supported-for-defragmentation)

## <a name="defragmenting-a-file"></a>Deframmentazione di un file

In un sistema operativo con un'unica attività semplice, il software di deframmentazione è l'unica attività e non esistono altri processi da leggere o scrivere sul disco. In un sistema operativo multitasking, tuttavia, alcuni processi possono leggere e scrivere in un'unità disco rigido mentre un altro processo deframmenta tale unità disco rigido. Il problema è evitare di scrivere in un file deframmentato senza interrompere il processo di scrittura per molto tempo. La risoluzione di questo problema non è semplice, ma è possibile.

Per consentire la deframmentazione senza richiedere una conoscenza dettagliata di una struttura file system disco, viene fornito un set di tre codici di controllo. I codici di controllo forniscono le funzionalità seguenti:

-   Consentire alle applicazioni di individuare cluster vuoti
-   Determinare il percorso del disco dei cluster di file
-   Spostare i cluster in un disco

I codici di controllo gestiscono anche in modo trasparente il problema di impedire e consentire ad altri processi di leggere e scrivere nei file durante gli spostamenti.

Queste operazioni possono essere eseguite senza impedire l'esecuzione di altri processi. Tuttavia, gli altri processi hanno tempi di risposta più lenti durante la deframmentazione di un'unità disco.

**Per deframmentare un file**

1.  Usare il [**codice di controllo \_ \_ \_ FSCTL GET VOLUME BITMAP**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_volume_bitmap) per trovare una posizione nel volume sufficientemente grande da accettare un intero file.
    > [!Note]  
    > Se necessario, spostare altri file per creare una posizione sufficientemente grande. Idealmente, dopo il primo extent del file è disponibile un numero sufficiente di cluster non allocati che è possibile spostare gli extent successivi nello spazio dopo il primo extent.

     

2.  Usare il [**codice di controllo \_ FSCTL GET RETRIEVAL \_ \_ POINTERS**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_retrieval_pointers) per ottenere una mappa del layout corrente del file sul disco.
3.  Illustra la [**struttura \_ BUFFER DEI \_ PUNTATORI DI**](/windows/desktop/api/WinIoCtl/ns-winioctl-retrieval_pointers_buffer) RECUPERO restituita da [**FSCTL \_ GET RETRIEVAL \_ \_ POINTERS**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_retrieval_pointers).
4.  Usare il [**codice di controllo \_ FSCTL MOVE \_ FILE**](/windows/win32/api/winioctl/ni-winioctl-fsctl_move_file) per spostare ogni cluster mentre si esplora la struttura.
    > [!Note]  
    > Potrebbe essere necessario rinnovare la bitmap o la struttura di recupero oppure entrambe le volte mentre altri processi scrivono sul disco.

     

Due delle operazioni utilizzate nel processo di deframmentazione richiedono un handle per un volume. Solo gli amministratori possono ottenere un handle per un volume, pertanto solo gli amministratori possono deframmentare un volume. Un'applicazione deve controllare i diritti di un utente che tenta di eseguire il software di deframmentazione e non deve consentire a un utente di deframmentare un volume se l'utente non dispone dei diritti appropriati.

Quando si [**usa CreateFile per**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) aprire una directory durante la deframmentazione di un volume di file system FAT o FAT32, specificare il valore **GENERIC \_ READ** access mask. Non specificare il valore **della maschera di accesso MAXIMUM \_ ALLOWED.** In questo caso, l'accesso alla directory viene negato.

Non tentare di spostare i cluster allocati in un file system NTFS che si estendono oltre le dimensioni del file arrotondato del cluster, perché il risultato è un errore.

I punti di analisi, le bitmap e gli elenchi di attributi nei volumi file system NTFS possono essere deframmentati, aperti per la lettura e la sincronizzazione e denominati usando il *file*:*nome**:* sintassi del tipo; ad esempio *dirname*:$i 30:$INDEX \_ ALLOCATION, *mrp*::$DATA, *mrp*::$REPARSE POINT e \_ *mrp*::$ATTRIBUTE \_ LIST.

Quando si deframmenta ntfs file system volumi, è consentita la deframmentazione di un cluster virtuale oltre le dimensioni di allocazione di un file.

## <a name="minimizing-interactions-between-defragmentation-and-shadow-copies"></a>Riduzione al minimo delle interazioni tra deframmentazione e copie shadow

Quando possibile, spostare i dati in blocchi allineati l'uno rispetto all'altro in incrementi di 16 kilobyte (KB). In questo modo si riduce il sovraccarico di copia su scrittura quando sono abilitate le copie shadow, perché lo spazio delle copie shadow aumenta e le prestazioni si riducono quando si verificano le condizioni seguenti:

-   La dimensione del blocco della richiesta di spostamento è minore o uguale a 16 KB.
-   Il delta di spostamento non è in incrementi di 16 KB.

Il delta di spostamento è il numero di byte tra l'inizio del blocco di origine e l'inizio del blocco di destinazione. In altre parole, un blocco che inizia in corrispondenza dell'offset X (su disco) può essere spostato in un offset iniziale Y se il valore assoluto di X meno Y è un multiplo pari di 16 KB. Pertanto, presupponendo cluster di 4 KB, verrà ottimizzato lo spostamento dal cluster 3 al cluster 27, ma non dal cluster 18 al cluster 24. Si noti che mod(3,4) = 3 = mod(27,4). Viene scelto mod 4 perché quattro cluster a 4 KB, ognuno dei quali equivale a 16 KB. Di conseguenza, un volume formattato con dimensioni del cluster di 16 KB comporta l'ottimizzazione di tutti i file di spostamento.

Per altre informazioni sulle copie shadow, vedere [Servizio Copia Shadow del volume](/windows/desktop/VSS/about-the-volume-shadow-copy-service).

## <a name="files-streams-and-stream-types-supported-for-defragmentation"></a>File, flussi e tipi di flusso supportati per la deframmentazione

Anche se la maggior parte dei file può essere spostata usando il codice di controllo [**FSCTL \_ MOVE \_ FILE,**](/windows/win32/api/winioctl/ni-winioctl-fsctl_move_file) non tutti possono essere spostati. Di seguito è riportato l'elenco di file, flussi e tipi di flusso (detti anche codici di tipo attributo) supportati da **FSCTL \_ MOVE \_ FILE.** Altri file, flussi e tipi di flusso non sono supportati da **FSCTL \_ MOVE \_ FILE.**

Tipi di flusso supportati per qualsiasi file o directory.

-   ::$DATA
-   ::$ATTRIBUTE \_ LIST
-   ::$REPARSE \_ POINT
-   ::$EA
-   ::$LOGGED UTILITY \_ \_ STREAM

**Windows 7, Windows Server 2008 R2, Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP: **::$EA e ::$LOGGED UTILITY STREAM non sono supportati prima di \_ \_ Windows 8 e Windows Server 2012

Tipi di flusso supportati per qualsiasi directory.

-   ::$BITMAP
-   ::$INDEX \_ ALLOCATION

Di seguito sono riportati i tipi di file di sistema, flusso e flusso supportati da [**FSCTL \_ MOVE \_ FILE**](/windows/win32/api/winioctl/ni-winioctl-fsctl_move_file) nel formato "*filename*:*streamname*:$*typename*".

-   $MFT::$DATA
-   $MFT::$ATTRIBUTE \_ LIST
-   $MFT::$BITMAP
-   $AttrDef::$DATA
-   $AttrDef::$ATTRIBUTE \_ LIST
-   $Secure:$SDS:$DATA
-   $Secure::$ATTRIBUTE \_ LIST
-   $Secure:$SDH:$INDEX ALLOCAZIONE \_
-   $Secure:$SDH:$BITMAP
-   $Secure:$SII:$INDEX \_ ALLOCATION
-   $Secure:$SII:$BITMAP
-   $UpCase::$DATA
-   $UpCase::$ATTRIBUTE \_ LIST
-   $Extend:$I 30:$INDEX \_ ALLOCATION
-   $Extend::$ATTRIBUTE \_ LIST
-   $Extend:$I 30:$BITMAP
-   $Extend \\ $UsnJrnl:$J:$DATA
-   $Extend \\ $UsnJrnl::$ATTRIBUTE \_ LIST
-   $Extend \\ $UsnJrnl:$Max:$DATA
-   $Extend \\ $Quota:$Q:$INDEX \_ ALLOCATION
-   $Extend \\ $Quota::$ATTRIBUTE \_ LIST
-   $Extend \\ $Quota:$Q:$BITMAP
-   $Extend \\ $Quota:$O:$INDEX \_ ALLOCATION
-   $Extend \\ $Quota:$O:$BITMAP
-   $Extend \\ $ObjId:$O:$INDEX \_ ALLOCATION
-   $Extend \\ $ObjId::$ATTRIBUTE \_ LIST
-   $Extend \\ $ObjId:$O:$BITMAP
-   $Extend \\ $Reparse:$R:$INDEX \_ ALLOCATION
-   $Extend \\ $Reparse::$ATTRIBUTE \_ LIST
-   $Extend \\ $Reparse:$R:$BITMAP
-   $Extend \\ $RmMetadata:$I 30:$INDEX \_ ALLOCATION
-   $Extend \\ $RmMetadata:$I 30:$BITMAP
-   $Extend \\ $RmMetadata::$ATTRIBUTE \_ LIST
-   $Extend $RmMetadata \\ \\ $Repair::$DATA
-   $Extend $RmMetadata \\ \\ $Repair::$ATTRIBUTE \_ LIST
-   $Extend \\ $RmMetadata \\ $Repair:$Config:$DATA
-   $Extend $RmMetadata \\ \\ $Txf:$I 30:$INDEX \_ ALLOCATION
-   $Extend \\ $RmMetadata \\ $Txf::$ATTRIBUTE \_ LIST
-   $Extend $RmMetadata \\ \\ $Txf:$I 30:$BITMAP
-   $Extend $RmMetadata \\ \\ $Txf:$TXF \_ DATA:$LOGGED \_ UTILITY \_ STREAM
-   $Extend $RmMetadata \\ \\ $TxfLog:$I 30:$INDEX \_ ALLOCATION
-   $Extend $RmMetadata \\ \\ $TxfLog::$ATTRIBUTE \_ LIST
-   $Extend \\ $RmMetadata \\ $TxfLog:$I 30:$BITMAP
-   $Extend \\ $RmMetadata \\ $TxfLog \\ $Tops::$DATA
-   $Extend $RmMetadata \\ \\ $TxfLog \\ $Tops::$ATTRIBUTE \_ LIST
-   $Extend \\ $RmMetadata \\ $TxfLog \\ $Tops:$T:$DATA
-   $Extend $RmMetadata \\ \\ $TxfLog \\ $TxfLog.blf::$DATA
-   $Extend $RmMetadata \\ \\ $TxfLog \\ $TxfLog.blf::$ATTRIBUTE \_ LIST

 

 
