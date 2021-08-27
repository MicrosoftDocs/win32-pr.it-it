---
description: Vengono descritte diverse considerazioni sulla programmazione per NTFS transazionale.
ms.assetid: a1ef1ce1-42f6-4627-ab64-e7f41fa23e94
title: Considerazioni sulla programmazione per NTFS transazionale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd3150746b1cb34495178cc8318805587f3d08f17e04cb8227e95a9c52ddce3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047941"
---
# <a name="programming-considerations-for-transactional-ntfs"></a>Considerazioni sulla programmazione per NTFS transazionale

Per una descrizione delle varie considerazioni sulla programmazione per TRANSACTIONAL NTFS, vedere le sezioni seguenti:

-   [Quali modifiche ai file vengono transazionate](#which-file-changes-are-transacted)
-   [Compressione](#compression)
-   [Creazione di un file o di una directory](#creating-a-file-or-directory)
-   [Eliminazione di un file](#deleting-a-file)
-   [Eliminazione di una directory](#deleting-a-directory)
-   [Problemi di blocco della directory](#directory-locking-issues)
-   [Enumerazione della directory](#directory-enumeration)
-   [File mappati alla memoria](#memory-mapped-files)
-   [Flussi denominati](#named-streams)
-   [Ridenominazione di un file o di una directory](#renaming-a-file-or-directory)
-   [Punti di analisi](#reparse-points)
-   [Codici errore](#error-codes)
-   [File system crittografato](#encrypted-file-system)
-   [Funzioni di I/O di file e NTFS transazionale](#file-io-functions-and-transactional-ntfs)
    -   [Funzioni transazione](#transacted-functions)
    -   [Funzioni di I/O di file modificate da TxF](#file-io-functions-changed-by-txf)

## <a name="which-file-changes-are-transacted"></a>Quali modifiche ai file vengono transazionate

La maggior parte delle modifiche ai file, ad esempio le modifiche al contenuto del file, ai flussi, ai reparse point, agli attributi e allo spazio dei nomi file system, viene eseguita la transazione. Quando viene apportata una di queste modifiche in un handle di file transazionale, la modifica viene isolata da altre transazioni e la modifica viene annullata se viene eseguito il rollback della transazione.

Le modifiche che non influiscono sul contenuto del file, sui metadati o file system spazio dei nomi, ad esempio le modifiche alla compressione o alla deframmentazione, non vengono transazionate. Queste modifiche non sono isolate da altre transazioni e non vengono annullate se viene eseguito il rollback della transazione.

## <a name="compression"></a>Compressione

Lo stato di compressione di un file aperto in una transazione non può essere modificato.

## <a name="creating-a-file-or-directory"></a>Creazione di un file o di una directory

Un file o una directory creata in una transazione non è visibile a qualsiasi elemento esterno alla transazione corrente. All'esterno di questa transazione, qualsiasi tentativo di creare un file con lo stesso nome ha esito negativo con l'errore **ERROR \_ TRANSACTIONAL \_ CONFLICT,** riservando in modo efficace il nome file per quando viene eseguito il commit o il rollback della transazione.

## <a name="deleting-a-file"></a>Eliminazione di un file

Un file o una directory eliminata chiamando la [**funzione DeleteFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-deletefiletransacteda) rimane visibile a tutti i lettori esterni.

> [!Note]  
> Tutti gli handle transazionale per il file devono essere chiusi prima della fine della transazione. Se gli handle non vengono chiusi correttamente, l'eliminazione non viene eseguita. Tutti gli handle aperti per il file devono essere chiusi prima di eseguire il commit perché l'operazione di eliminazione venga considerata parte della transazione. Ciò è dovuto al fatto che il sistema non elimina effettivamente un file fino alla chiusura dell'ultimo handle, anche quando l'operazione non è transazionata, come parte del sottosistema di I/O di file Windows.

 

## <a name="deleting-a-directory"></a>Eliminazione di una directory

Una directory eliminata chiamando la [**funzione RemoveDirectoryTransacted**](/windows/desktop/api/WinBase/nf-winbase-removedirectorytransacteda) rimane visibile a tutti i lettori esterni.

> [!Note]  
> Gli stessi vincoli esistono per gli handle aperti nelle operazioni di directory transazionate come per i file. Per altre informazioni, vedere [Eliminazione di un file](#deleting-a-file).

 

## <a name="directory-locking-issues"></a>Problemi di blocco della directory

Se un file viene modificato in una transazione, tutti i componenti  della directory del percorso del file vengono definiti aggiunti alla ridenominazione fino al termine della transazione. Ciò significa che il sistema impedisce di rinominarli fino a quando non viene eseguito il commit o il rollback della transazione. Un tentativo di rinominare una directory che è un predecessore di un file modificato in una transazione in corso avrà esito negativo con l'errore **\_ ERRORE CANT BREAK \_ \_ TRANSACTIONAL \_ DEPENDENCY**.

## <a name="directory-enumeration"></a>Enumerazione di directory

Il contenuto di una directory può essere modificato mentre è in corso un'enumerazione in seguito all'uso di API che enumerano, ad esempio le funzioni [**FindFirstFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-findfirstfiletransacteda) e [**FindNextFile.**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea)

Le modifiche apportate a una directory esterna a una transazione non sono isolate dalla transazione e sono immediatamente visibili all'interno della transazione. Ad esempio, se un writer non transazionale aggiunge un file a una directory, il nuovo file è immediatamente visibile all'interno della transazione in modo che la chiamata alla funzione [**FindFirstFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-findfirstfiletransacteda) o [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea) restituirà il nuovo file.

Le modifiche apportate a una directory all'interno di una transazione vengono isolate fino al commit della transazione. Ad esempio, un file creato nella directory come parte della transazione. Un lettore non transazionale che chiama la [**funzione FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) o [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea) non visualizza il file appena creato fino al commit della transazione.

## <a name="memory-mapped-files"></a>File mappati alla memoria

Il client deve chiamare la funzione [**FlushViewOfFile,**](/windows/desktop/api/memoryapi/nf-memoryapi-flushviewoffile) chiudere l'oggetto di mapping dei file e chiudere l'handle di file prima di eseguire il commit della transazione associata in un file mappato alla memoria.

## <a name="named-streams"></a>Flussi denominati

I flussi denominati sono completamente transazionali, ma il blocco viene eseguito a livello di file, non a livello di flusso. I writer esterni a una transazione che tentano di modificare qualsiasi flusso all'interno di un file bloccato ricevono **l'errore ERROR \_ SHARING \_ VIOLATION**.

Non è possibile rinominare un flusso secondario in una transazione.

## <a name="renaming-a-file-or-directory"></a>Ridenominazione di un file o di una directory

Per rinominare un file come operazione transazionata, chiamare [**MoveFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-movefiletransacteda) per spostare il file.

## <a name="reparse-points"></a>Punti di analisi

Le modifiche ai reparse point vengono transazionate, il che significa che se un nuovo reparse point viene assegnato a un file in una transazione, non è visibile alle altre transazioni. Analogamente, le modifiche o la rimozione di un reparse point esistente non sono visibili fino al commit.

## <a name="error-codes"></a>Codici errore

Kernel Transaction Manager (KTM) usa i codici di errore di sistema nell'intervallo compreso tra 6700 e 6799. Transactional NTFS (TxF) usa Windows di errore nell'intervallo compreso tra 6800 e 6899. Per altre informazioni, vedere WinError.h e Codici di errore di sistema (6000-8199).

## <a name="encrypted-file-system"></a>File system crittografato

TxF non supporta le operazioni sui file EFS. Non è possibile aprire un file crittografato con EFS per le transazioni. La chiamata [**della funzione CreateFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda) in un file EFS avrà esito negativo con l'errore **ERROR \_ EFS NOT ALLOWED IN \_ \_ \_ \_ TRANSACTION**. Analogamente, la chiamata della [**funzione EncryptFile**](/windows/desktop/api/WinBase/nf-winbase-encryptfilea) su un file in una transazione avrà esito negativo con l'errore **ERROR \_ EFS NOT ALLOWED IN \_ \_ \_ \_ TRANSACTION**.

## <a name="file-io-functions-and-transactional-ntfs"></a>Funzioni di I/O di file e NTFS transazionale

TxF offre nuove funzioni transazionche che accettano un nome di file e modifica il comportamento delle funzioni API di I/O di file esistenti che accettano un handle di file.

### <a name="transacted-functions"></a>Funzioni transazione

Se non si chiama una delle funzioni transazionate seguenti al posto della versione non transazionata, l'operazione non verrà eseguita:

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

Ad esempio, la [**funzione CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) ha ora una versione transazionata: [**CreateFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda).

### <a name="file-io-functions-changed-by-txf"></a>Funzioni di I/O di file modificate da TxF

Nella tabella seguente sono elencate le funzioni il cui comportamento è interessato da NTFS transazionale. Ad esempio, il comportamento della [**funzione ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) varia a seconda che il *parametro hFile* sia stato creato dalla funzione [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) o [**dalla funzione CreateFileTransacted.**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda)



| Funzione                                                                                                                                                                                                                                                                                                                                                                                                                                             | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CloseHandle"></span><span id="closehandle"></span><span id="CLOSEHANDLE"></span>[**Closehandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle)<br/>                                                                                                                                                                                                                                                                                                             | Le applicazioni devono chiudere tutti gli handle associati a una transazione prima del commit della transazione. Un'applicazione deve chiudere un handle transazionale aperto con **FILE FLAG DELETE ON \_ \_ \_ \_ CLOSE** prima di eseguire il commit della transazione per consentire l'esecuzione dell'operazione di eliminazione.<br/>                                                                                                                                     |
| <span id="CreateFileMapping"></span><span id="createfilemapping"></span><span id="CREATEFILEMAPPING"></span>[**CreateFileMapping**](/windows/desktop/api/winbase/nf-winbase-createfilemappinga)<br/>                                                                                                                                                                                                                                                                                 | Se è presente una transazione associata a *hFile*, l'oggetto di mapping dei file creato da questa funzione verrà associato alla stessa transazione. Le modifiche apportate tramite le visualizzazioni di questo oggetto di mapping dei file vengono transazionate. Le applicazioni devono chiamare [**FlushViewOfFile**](/windows/desktop/api/memoryapi/nf-memoryapi-flushviewoffile), annullare il mapping di tutte le visualizzazioni e chiudere tutti gli handle per l'oggetto di mapping dei file prima di eseguire il commit delle modifiche transazione.<br/> |
| <span id="FindNextFile"></span><span id="findnextfile"></span><span id="FINDNEXTFILE"></span>[**Findnextfile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea)<br/>                                                                                                                                                                                                                                                                                                         | Se è presente una transazione associata all'handle di enumerazione dei file, i file restituiti sono soggetti alle regole di isolamento della transazione.<br/>                                                                                                                                                                                                                                                                    |
| <span id="FSCTL_SET_COMPRESSION"></span><span id="fsctl_set_compression"></span>[**FSCTL \_ SET \_ COMPRESSION**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression)<br/>                                                                                                                                                                                                                                                                                                  | Non è possibile modificare lo stato di compressione di un file aperto da [**CreateFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda).<br/>                                                                                                                                                                                                                                                                                               |
| <span id="GetFileInformationByHandle__________and__________GetFileInformationByHandleEx"></span><span id="getfileinformationbyhandle__________and__________getfileinformationbyhandleex"></span><span id="GETFILEINFORMATIONBYHANDLE__________AND__________GETFILEINFORMATIONBYHANDLEEX"></span>[**GetFileInformationByHandle**](/windows/desktop/api/FileAPI/nf-fileapi-getfileinformationbyhandle) e [ **GetFileInformationByHandleEx**](/windows/desktop/api/WinBase/nf-winbase-getfileinformationbyhandleex)<br/> | Se è presente una transazione associata all'handle di file, la funzione restituisce informazioni per la vista file isolato.<br/>                                                                                                                                                                                                                                                                                           |
| <span id="GetFileSize_and__________GetFileSizeEx"></span><span id="getfilesize_and__________getfilesizeex"></span><span id="GETFILESIZE_AND__________GETFILESIZEEX"></span>[**GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) e [ **GetFileSizeEx**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesizeex)<br/>                                                                                                                                                                                  | Se è presente una transazione associata all'handle di file, la funzione restituisce informazioni per la vista file isolato.<br/>                                                                                                                                                                                                                                                                                           |
| <span id="GetVolumeInformation"></span><span id="getvolumeinformation"></span><span id="GETVOLUMEINFORMATION"></span>[**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa)<br/>                                                                                                                                                                                                                                                                 | Se il volume supporta file system, la funzione restituisce **FILE \_ SUPPORTS \_ TRANSACTIONS** in *lpFileSystemFlags*.<br/>                                                                                                                                                                                                                                                                                  |
| <span id="MapViewOfFile_and__________MapViewOfFileEx"></span><span id="mapviewoffile_and__________mapviewoffileex"></span><span id="MAPVIEWOFFILE_AND__________MAPVIEWOFFILEEX"></span>[**MapViewOfFile e**](/windows/desktop/api/memoryapi/nf-memoryapi-mapviewoffile) [ **MapViewOfFileEx**](/windows/desktop/api/memoryapi/nf-memoryapi-mapviewoffileex)<br/>                                                                                                                                                                | Se è presente una transazione associata all'handle di file usato per creare l'oggetto di mapping dei file di cui viene eseguito il mapping, la vista associata viene transazionata. Se la vista viene usata per apportare modifiche transazionale a un file, l'utente deve chiamare [**FlushViewOfFile**](/windows/desktop/api/memoryapi/nf-memoryapi-flushviewoffile), chiudere l'oggetto mapping file e chiudere l'handle di file prima di eseguire il commit della transazione associata.<br/>              |
| <span id="ReadDirectoryChangesW"></span><span id="readdirectorychangesw"></span><span id="READDIRECTORYCHANGESW"></span>[**ReadDirectoryChangesW**](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw)<br/>                                                                                                                                                                                                                                                            | Se è presente una transazione associata all'handle di directory, le notifiche riflettono la visualizzazione isolata della directory. Le modifiche ai file all'esterno della visualizzazione transazionata della directory non vengono incluse nelle notifiche.<br/>                                                                                                                                                                                |
| <span id="ReadFile___________ReadFileEx__and__________ReadFileScatter"></span><span id="readfile___________readfileex__and__________readfilescatter"></span><span id="READFILE___________READFILEEX__AND__________READFILESCATTER"></span>[**ReadFile,**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex)e [**ReadFileScatter**](/windows/desktop/api/FileAPI/nf-fileapi-readfilescatter)<br/>                                                                                  | Se è presente una transazione associata all'handle di file, la funzione restituisce i dati dalla vista transazionale del file. È garantito che un handle di lettura transazione mostri la stessa visualizzazione di un file per la durata dell'handle.<br/>                                                                                                                                                                                 |
| <span id="SetEndOfFile"></span><span id="setendoffile"></span><span id="SETENDOFFILE"></span>[**SetEndOfFile**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile)<br/>                                                                                                                                                                                                                                                                                                         | Se è presente una transazione associata all'handle, viene eseguita la transazione della modifica nella posizione di fine file.<br/>                                                                                                                                                                                                                                                                                                       |
| <span id="SetFileInformationByHandle"></span><span id="setfileinformationbyhandle"></span><span id="SETFILEINFORMATIONBYHANDLE"></span>[**SetFileInformationByHandle**](/windows/desktop/api/FileAPI/nf-fileapi-setfileinformationbyhandle)<br/>                                                                                                                                                                                                                                   | Se è presente una transazione associata all'handle, le modifiche apportate verranno transazionali per le classi di informazioni **FileBasicInfo**, **FileRenameInfo**, **FileAllocationInfo**, **FileEndOfFileInfo** e **FileDispositionInfo**.<br/>                                                                                                                                                                          |
| <span id="SetFileShortName"></span><span id="setfileshortname"></span><span id="SETFILESHORTNAME"></span>[**SetFileShortName**](/windows/desktop/api/WinBase/nf-winbase-setfileshortnamea)<br/>                                                                                                                                                                                                                                                                                     | Se è presente una transazione associata all'handle, la modifica nel nome breve del file viene eseguita in modo transazionale.<br/>                                                                                                                                                                                                                                                                                                          |
| <span id="SetFileTime"></span><span id="setfiletime"></span><span id="SETFILETIME"></span>[**SetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-setfiletime)<br/>                                                                                                                                                                                                                                                                                                             | Se è presente una transazione associata all'handle, la modifica dell'ora del file viene eseguita in modo transazionale.<br/>                                                                                                                                                                                                                                                                                                                      |
| <span id="WriteFile__________WriteFileEx__and_________WriteFileGather"></span><span id="writefile__________writefileex__and_________writefilegather"></span><span id="WRITEFILE__________WRITEFILEEX__AND_________WRITEFILEGATHER"></span>[**WriteFile,**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex)e [**WriteFileGather**](/windows/desktop/api/FileAPI/nf-fileapi-writefilegather)<br/>                                                                              | Se è presente una transazione associata all'handle di file, la scrittura del file viene eseguita in modo transazionale.<br/>                                                                                                                                                                                                                                                                                                                          |



 

 

