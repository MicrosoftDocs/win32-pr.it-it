---
description: Vengono descritte le varie considerazioni di programmazione per Transactional NTFS.
ms.assetid: a1ef1ce1-42f6-4627-ab64-e7f41fa23e94
title: Considerazioni sulla programmazione per Transactional NTFS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e79dc7eba4de1258c294d3e41f8042f3cb01dc87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315932"
---
# <a name="programming-considerations-for-transactional-ntfs"></a>Considerazioni sulla programmazione per Transactional NTFS

Per una descrizione delle diverse considerazioni di programmazione per la funzionalità NTFS transazionale, vedere le sezioni seguenti:

-   [Modifiche dei file sottoposte a transazione](#which-file-changes-are-transacted)
-   [Compressione](#compression)
-   [Creazione di un file o di una directory](#creating-a-file-or-directory)
-   [Eliminazione di un file](#deleting-a-file)
-   [Eliminazione di una directory](#deleting-a-directory)
-   [Problemi di blocco della directory](#directory-locking-issues)
-   [Enumerazione directory](#directory-enumeration)
-   [File mappati alla memoria](#memory-mapped-files)
-   [Flussi denominati](#named-streams)
-   [Ridenominazione di un file o di una directory](#renaming-a-file-or-directory)
-   [Punti di analisi](#reparse-points)
-   [Codici errore](#error-codes)
-   [File system crittografato](#encrypted-file-system)
-   [Funzioni di I/O di file e NTFS transazionale](#file-io-functions-and-transactional-ntfs)
    -   [Funzioni transazionali](#transacted-functions)
    -   [Funzioni di I/O dei file modificate da TxF](#file-io-functions-changed-by-txf)

## <a name="which-file-changes-are-transacted"></a>Modifiche dei file sottoposte a transazione

La maggior parte delle modifiche apportate ai file, ad esempio modifiche al contenuto del file, ai flussi, ai reparse point, agli attributi e allo spazio dei nomi file system, vengono sottoposte Quando una di queste modifiche viene apportata a un handle di file transazionale, la modifica viene isolata dalle altre transazioni e la modifica viene annullata se viene eseguito il rollback della transazione.

Le modifiche che non influiscono sul contenuto del file, sui metadati o sullo spazio dei nomi file system, ad esempio le modifiche alla compressione o alla deframmentazione, non vengono sottoposte a transazione. Queste modifiche non sono isolate da altre transazioni e non vengono annullate se viene eseguito il rollback della transazione.

## <a name="compression"></a>Compressione

Impossibile modificare lo stato di compressione di un file aperto in una transazione.

## <a name="creating-a-file-or-directory"></a>Creazione di un file o di una directory

Un file o una directory creata in una transazione non è visibile a qualsiasi elemento esterno alla transazione corrente. Al di fuori di questa transazione, qualsiasi tentativo di creare un file con lo stesso nome ha esito negativo con errore di errore **\_ transazionale \_**, riservando in modo efficace il nome del file quando viene eseguito il commit o il rollback della transazione.

## <a name="deleting-a-file"></a>Eliminazione di un file

Un file o una directory eliminata chiamando la funzione [**DeleteFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-deletefiletransacteda) rimane visibile a tutti i lettori esterni.

> [!Note]  
> Tutti gli handle transazionali del file devono essere chiusi prima della fine della transazione. Se gli handle non sono chiusi correttamente, l'eliminazione non viene eseguita. Tutti gli handle aperti per il file devono essere chiusi prima di eseguire il commit affinché l'operazione di eliminazione venga considerata parte della transazione. Questo perché il sistema non elimina effettivamente un file fino a quando non viene chiuso l'ultimo handle, anche quando l'operazione non è transazionale, come parte del sottosistema di I/O dei file di Windows.

 

## <a name="deleting-a-directory"></a>Eliminazione di una directory

Una directory eliminata chiamando la funzione [**RemoveDirectoryTransacted**](/windows/desktop/api/WinBase/nf-winbase-removedirectorytransacteda) rimane visibile a tutti i lettori esterni.

> [!Note]  
> Gli stessi vincoli sono disponibili per gli handle aperti sulle operazioni di directory transazionali come nei file. Per ulteriori informazioni, vedere [eliminazione di un file](#deleting-a-file).

 

## <a name="directory-locking-issues"></a>Problemi di blocco della directory

Se un file viene modificato in una transazione, tutti i componenti di directory del percorso del file vengono indicati come *bloccati rispetto alla ridenominazione* fino alla fine della transazione. Ovvero, il sistema impedisce di rinominarli fino a quando non viene eseguito il commit o il rollback della transazione. Il tentativo di rinominare una directory che è un predecessore di un file che è stato modificato in una transazione in corso avrà esito negativo e si verificherà un errore durante la **\_ \_ \_ \_ dipendenza transazionale**.

## <a name="directory-enumeration"></a>Enumerazione directory

Il contenuto di una directory può essere modificato mentre è in corso un'enumerazione in seguito all'utilizzo di API che enumerano, ad esempio, le funzioni [**FindFirstFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-findfirstfiletransacteda) e [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea) .

Le modifiche apportate a una directory al di fuori di una transazione non sono isolate dalla transazione e sono immediatamente visibili all'interno della transazione. Se, ad esempio, un writer non transazionale aggiunge un file a una directory, il nuovo file sarà immediatamente visibile all'interno della transazione, in modo che la chiamata della funzione [**FindFirstFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-findfirstfiletransacteda) o [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea) restituirà il nuovo file.

Le modifiche apportate a una directory all'interno di una transazione vengono isolate fino al commit della transazione. Ad esempio, un file creato nella directory come parte della transazione. Un lettore non transazionale che chiama la funzione [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) o [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea) non vedrà il file appena creato fino a quando non viene eseguito il commit della transazione.

## <a name="memory-mapped-files"></a>File mappati alla memoria

Il client deve chiamare la funzione [**FlushViewOfFile**](/windows/desktop/api/memoryapi/nf-memoryapi-flushviewoffile) , chiudere l'oggetto mapping di file e chiudere l'handle di file prima di eseguire il commit della transazione associata in un file mappato alla memoria.

## <a name="named-streams"></a>Flussi denominati

I flussi denominati sono completamente transazionali, ma il blocco viene eseguito a livello di file, non a livello di flusso. I writer esterni a una transazione che tentano di modificare qualsiasi flusso all'interno di un file bloccato ricevono la **\_ \_ violazione di condivisione degli errori**.

Non è possibile rinominare un flusso secondario in una transazione.

## <a name="renaming-a-file-or-directory"></a>Ridenominazione di un file o di una directory

Per rinominare un file come operazione transazionale, chiamare [**MoveFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-movefiletransacteda) per spostare il file.

## <a name="reparse-points"></a>Punti di analisi

Le modifiche apportate ai reparse point vengono sottoposte a transazione, il che significa che se un nuovo punto di analisi viene assegnato a un file in una transazione, non è visibile alle altre transazioni. Analogamente, le modifiche o la rimozione di un punto di analisi esistente non sono visibili fino al commit.

## <a name="error-codes"></a>Codici errore

Gestione transazioni kernel usa i codici di errore di sistema nell'intervallo compreso tra 6700 e 6799. Transactional NTFS (TxF) USA i codici di errore di Windows nell'intervallo compreso tra 6800 e 6899. Per ulteriori informazioni, vedere WinError. h e codici di errore di sistema (6000-8199).

## <a name="encrypted-file-system"></a>File system crittografato

TxF non supporta operazioni sui file EFS. Non è possibile aprire un file crittografato EFS per le transazioni. La chiamata della funzione [**CreateFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda) in un file EFS avrà esito negativo e si verificherà l' **errore \_ EFS \_ non \_ consentito \_ nella \_ transazione**. Analogamente, la chiamata della funzione [**EncryptFile**](/windows/desktop/api/WinBase/nf-winbase-encryptfilea) su un file in una transazione avrà esito negativo e si verificherà l' **errore \_ EFS \_ non \_ consentito \_ nella \_ transazione**.

## <a name="file-io-functions-and-transactional-ntfs"></a>Funzioni di I/O di file e NTFS transazionale

TxF fornisce nuove funzioni transazionali che accettano un nome file e modifica il comportamento delle funzioni API di I/O dei file esistenti che accettano un handle di file.

### <a name="transacted-functions"></a>Funzioni transazionali

Se non si chiama una delle funzioni transazionali seguenti al posto della relativa versione non transazionale, l'operazione non verrà sottoposta a transazione:

-   [**CopyFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-copyfiletransacteda)
-   [**CreateDirectoryTransacted**](/windows/desktop/api/WinBase/nf-winbase-createdirectorytransacteda)
-   [**CreateFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda)
-   [**CreateHardLinkTransacted**](/windows/desktop/api/WinBase/nf-winbase-createhardlinktransacteda)
-   [**CreateSymbolicLinkTransacted**](/windows/desktop/api/WinBase/nf-winbase-createsymboliclinktransacteda)
-   [**DeleteFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-deletefiletransacteda)
-   [**FindFirstFileNameTransactedW**](/windows/desktop/api/WinBase/nf-winbase-findfirstfilenametransactedw)
-   [**FindFirstFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-findfirstfiletransacteda)
-   [**FindFirstStreamTransactedW**](/windows/desktop/api/WinBase/nf-winbase-findfirststreamtransactedw)
-   [**GetCompressedFileSizeTransacted**](/windows/desktop/api/WinBase/nf-winbase-getcompressedfilesizetransacteda)
-   [**GetFileAttributesTransacted**](/windows/desktop/api/WinBase/nf-winbase-getfileattributestransacteda)
-   [**GetFullPathNameTransacted**](/windows/desktop/api/WinBase/nf-winbase-getfullpathnametransacteda)
-   [**GetLongPathNameTransacted**](/windows/desktop/api/WinBase/nf-winbase-getlongpathnametransacteda)
-   [**MoveFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-movefiletransacteda)
-   [**RemoveDirectoryTransacted**](/windows/desktop/api/WinBase/nf-winbase-removedirectorytransacteda)
-   [**SetFileAttributesTransacted**](/windows/desktop/api/WinBase/nf-winbase-setfileattributestransacteda)

Ad esempio, la funzione [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) dispone ora di una versione transazionale: [**CreateFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda).

### <a name="file-io-functions-changed-by-txf"></a>Funzioni di I/O dei file modificate da TxF

Nella tabella seguente sono elencate le funzioni il cui comportamento è influenzato da Transactional NTFS. Il comportamento della funzione [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) , ad esempio, può variare a seconda che il parametro *hFile* sia stato creato dalla funzione [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) o dalla funzione [**CreateFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda) .



| Funzione                                                                                                                                                                                                                                                                                                                                                                                                                                             | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CloseHandle"></span><span id="closehandle"></span><span id="CLOSEHANDLE"></span>[**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle)<br/>                                                                                                                                                                                                                                                                                                             | Prima di eseguire il commit della transazione, è necessario che le applicazioni chiudano tutti gli handle associati a una transazione. Prima di eseguire il commit della transazione, è necessario che un'applicazione chiuda un handle transazionale aperto con **flag di file \_ \_ Delete \_ \_** prima di eseguire l'operazione di eliminazione.<br/>                                                                                                                                     |
| <span id="CreateFileMapping"></span><span id="createfilemapping"></span><span id="CREATEFILEMAPPING"></span>[**CreateFileMapping**](/windows/desktop/api/winbase/nf-winbase-createfilemappinga)<br/>                                                                                                                                                                                                                                                                                 | Se è presente una transazione associata a *hFile*, l'oggetto di mapping dei file creato da questa funzione verrà associato alla stessa transazione. Le modifiche apportate tramite viste di questo oggetto mapping di file vengono sottoposte a transazione. Per eseguire il commit delle modifiche transazionali, è necessario che le applicazioni chiamino [**FlushViewOfFile**](/windows/desktop/api/memoryapi/nf-memoryapi-flushviewoffile), annullare tutte le visualizzazioni e chiudano tutti gli handle nell'oggetto mapping di file.<br/> |
| <span id="FindNextFile"></span><span id="findnextfile"></span><span id="FINDNEXTFILE"></span>[**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea)<br/>                                                                                                                                                                                                                                                                                                         | Se è presente una transazione associata all'handle di enumerazione dei file, i file restituiti sono soggetti alle regole di isolamento delle transazioni.<br/>                                                                                                                                                                                                                                                                    |
| <span id="FSCTL_SET_COMPRESSION"></span><span id="fsctl_set_compression"></span>[**\_compressione FSCTL set \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression)<br/>                                                                                                                                                                                                                                                                                                  | Non è possibile modificare lo stato di compressione di un file aperto da [**CreateFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda).<br/>                                                                                                                                                                                                                                                                                               |
| <span id="GetFileInformationByHandle__________and__________GetFileInformationByHandleEx"></span><span id="getfileinformationbyhandle__________and__________getfileinformationbyhandleex"></span><span id="GETFILEINFORMATIONBYHANDLE__________AND__________GETFILEINFORMATIONBYHANDLEEX"></span>[**GetFileInformationByHandle**](/windows/desktop/api/FileAPI/nf-fileapi-getfileinformationbyhandle) e [ **GetFileInformationByHandleEx**](/windows/desktop/api/WinBase/nf-winbase-getfileinformationbyhandleex)<br/> | Se è presente una transazione associata all'handle di file, la funzione restituisce informazioni per la visualizzazione di file isolati.<br/>                                                                                                                                                                                                                                                                                           |
| <span id="GetFileSize_and__________GetFileSizeEx"></span><span id="getfilesize_and__________getfilesizeex"></span><span id="GETFILESIZE_AND__________GETFILESIZEEX"></span>[**Filesize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) e [ **GetFileSizeEx**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesizeex)<br/>                                                                                                                                                                                  | Se è presente una transazione associata all'handle di file, la funzione restituisce informazioni per la visualizzazione di file isolati.<br/>                                                                                                                                                                                                                                                                                           |
| <span id="GetVolumeInformation"></span><span id="getvolumeinformation"></span><span id="GETVOLUMEINFORMATION"></span>[**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa)<br/>                                                                                                                                                                                                                                                                 | Se il volume supporta file system transazioni, la funzione restituisce il **file \_ supporta \_ le transazioni** in *lpFileSystemFlags*.<br/>                                                                                                                                                                                                                                                                                  |
| <span id="MapViewOfFile_and__________MapViewOfFileEx"></span><span id="mapviewoffile_and__________mapviewoffileex"></span><span id="MAPVIEWOFFILE_AND__________MAPVIEWOFFILEEX"></span>[**MapViewOfFile**](/windows/desktop/api/memoryapi/nf-memoryapi-mapviewoffile) e [ **MapViewOfFileEx**](/windows/desktop/api/memoryapi/nf-memoryapi-mapviewoffileex)<br/>                                                                                                                                                                | Se è presente una transazione associata all'handle di file usato per creare l'oggetto di mapping dei file di cui è in corso il mapping, la vista associata viene sottoposta a transazione. Se la vista viene utilizzata per eseguire modifiche transazionali in un file, l'utente deve chiamare [**FlushViewOfFile**](/windows/desktop/api/memoryapi/nf-memoryapi-flushviewoffile), chiudere l'oggetto mapping di file e chiudere l'handle di file prima di eseguire il commit della transazione associata.<br/>              |
| <span id="ReadDirectoryChangesW"></span><span id="readdirectorychangesw"></span><span id="READDIRECTORYCHANGESW"></span>[**ReadDirectoryChangesW**](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw)<br/>                                                                                                                                                                                                                                                            | Se è presente una transazione associata all'handle di directory, le notifiche riflettono la vista isolata della directory. Le modifiche apportate ai file all'esterno della vista transazionale della directory non sono incluse nelle notifiche.<br/>                                                                                                                                                                                |
| <span id="ReadFile___________ReadFileEx__and__________ReadFileScatter"></span><span id="readfile___________readfileex__and__________readfilescatter"></span><span id="READFILE___________READFILEEX__AND__________READFILESCATTER"></span>[**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile), [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex)e [**ReadFileScatter**](/windows/desktop/api/FileAPI/nf-fileapi-readfilescatter)<br/>                                                                                  | Se è presente una transazione associata all'handle di file, la funzione restituisce i dati dalla vista transazionale del file. Un handle di lettura transazionale è garantito che mostri la stessa visualizzazione di un file per la durata dell'handle.<br/>                                                                                                                                                                                 |
| <span id="SetEndOfFile"></span><span id="setendoffile"></span><span id="SETENDOFFILE"></span>[**SetEndOfFile**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile)<br/>                                                                                                                                                                                                                                                                                                         | Se è presente una transazione associata all'handle, la modifica alla fine del file viene sottoposta a transazione.<br/>                                                                                                                                                                                                                                                                                                       |
| <span id="SetFileInformationByHandle"></span><span id="setfileinformationbyhandle"></span><span id="SETFILEINFORMATIONBYHANDLE"></span>[**SetFileInformationByHandle**](/windows/desktop/api/FileAPI/nf-fileapi-setfileinformationbyhandle)<br/>                                                                                                                                                                                                                                   | Se è presente una transazione associata all'handle, le modifiche apportate verranno sottoposte a transazione per le classi di informazioni **FileBasicInfo**, **FileRenameInfo**, **FileAllocationInfo**, **FileEndOfFileInfo** e **FileDispositionInfo**.<br/>                                                                                                                                                                          |
| <span id="SetFileShortName"></span><span id="setfileshortname"></span><span id="SETFILESHORTNAME"></span>[**SetFileShortName**](/windows/desktop/api/WinBase/nf-winbase-setfileshortnamea)<br/>                                                                                                                                                                                                                                                                                     | Se è presente una transazione associata all'handle, la modifica nel nome breve del file viene sottoposta a transazione.<br/>                                                                                                                                                                                                                                                                                                          |
| <span id="SetFileTime"></span><span id="setfiletime"></span><span id="SETFILETIME"></span>[**SetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-setfiletime)<br/>                                                                                                                                                                                                                                                                                                             | Se è presente una transazione associata all'handle, la modifica dell'ora del file viene sottoposta a transazione.<br/>                                                                                                                                                                                                                                                                                                                      |
| <span id="WriteFile__________WriteFileEx__and_________WriteFileGather"></span><span id="writefile__________writefileex__and_________writefilegather"></span><span id="WRITEFILE__________WRITEFILEEX__AND_________WRITEFILEGATHER"></span>[**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile), [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex)e [**WriteFileGather**](/windows/desktop/api/FileAPI/nf-fileapi-writefilegather)<br/>                                                                              | Se è presente una transazione associata all'handle di file, il file Write viene sottoposto a transazione.<br/>                                                                                                                                                                                                                                                                                                                          |



 

 

