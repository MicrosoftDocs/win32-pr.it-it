---
Description: Gli attributi di file sono valori di metadati archiviati dal file system su disco e vengono usati dal sistema e sono disponibili per gli sviluppatori tramite varie API di I/O di file.
ms.assetid: ed9a73d2-7fb6-4fb7-97f6-4dbf89e2f156
title: Costanti di attributi file (WinNT.h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/23/2020
ms.openlocfilehash: 1dbb3d8e5eb091c47635f78eba9558a0d2262caeb5ce482c7b5bccdc3b237169
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050871"
---
# <a name="file-attribute-constants"></a>Costanti di attributi file

Gli attributi di file sono valori di metadati archiviati dal file system su disco e vengono usati dal sistema e sono disponibili per gli sviluppatori tramite varie API di I/O di file. Per un elenco di API e argomenti correlati, vedere la sezione Vedere anche.

## <a name="example"></a>Esempio
```cpp


FILE_BASIC_INFO basicInfo;
    BOOL result;

    result = GetFileInformationByHandleEx( hFile,
                                               FileBasicInfo,
                                               &basicInfo,
                                               sizeof(basicInfo));

\\...

printf("  File Attributes: ");
    PrintFileAttributes(basicInfo.FileAttributes);

\\...
VOID
PrintFileAttributes(
    ULONG FileAttributes
    )
{
    
    if (FileAttributes & FILE_ATTRIBUTE_ARCHIVE) {
        printf("Archive ");
    }
    if (FileAttributes & FILE_ATTRIBUTE_DIRECTORY) {
        printf("Directory ");
    }
    if (FileAttributes & FILE_ATTRIBUTE_READONLY) {
        printf("Read-Only ");
    }
}
```

Esempio tratto da un [esempio Windows classico](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/winbase/io/extendedfileapis/ExtendedFileAPIs.cpp) in GitHub.



| Costante/valore                                                                                                                                                                                                                                                                                                 | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FILE_ATTRIBUTE_ARCHIVE"></span><span id="file_attribute_archive"></span><dl> <dt>**FILE \_ ATTRIBUTE \_ ARCHIVE**</dt> <dt>32 (0x20)</dt> </dl>                                                       | File o directory che è un file o una directory di archivio. Le applicazioni usano in genere questo attributo per contrassegnare i file per il backup o la rimozione di . <br/>                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="FILE_ATTRIBUTE_COMPRESSED"></span><span id="file_attribute_compressed"></span><dl> <dt>**FILE \_ ATTRIBUTE \_ COMPRESSED**</dt> <dt>2048 (0x800)</dt> </dl>                                           | File o directory compresso. Per un file, tutti i dati nel file vengono compressi. Per una directory, la compressione è l'impostazione predefinita per i file e le sottodirectory appena creati.<br/>                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="FILE_ATTRIBUTE_DEVICE"></span><span id="file_attribute_device"></span><dl> <dt>**FILE \_ ATTRIBUTE \_ DEVICE**</dt> <dt>64 (0x40)</dt> </dl>                                                          | Questo valore è riservato per l'uso da parte del sistema.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="FILE_ATTRIBUTE_DIRECTORY"></span><span id="file_attribute_directory"></span><dl> <dt>**FILE \_ ATTRIBUTE \_ DIRECTORY**</dt> <dt>16 (0x10)</dt> </dl>                                                 | Handle che identifica una directory.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="FILE_ATTRIBUTE_ENCRYPTED"></span><span id="file_attribute_encrypted"></span><dl> <dt>**FILE \_ ATTRIBUTE \_ ENCRYPTED**</dt> <dt>16384 (0x4000)</dt> </dl>                                            | File o directory crittografato. Per un file, tutti i flussi di dati nel file vengono crittografati. Per una directory, la crittografia è l'impostazione predefinita per i file e le sottodirectory appena creati.<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="FILE_ATTRIBUTE_HIDDEN"></span><span id="file_attribute_hidden"></span><dl> <dt>**FILE \_ ATTRIBUTE \_ HIDDEN**</dt> <dt>2 (0x2)</dt> </dl>                                                            | Il file o la directory è nascosta. Non è incluso in un elenco di directory normale.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="FILE_ATTRIBUTE_INTEGRITY_STREAM"></span><span id="file_attribute_integrity_stream"></span><dl> <dt>**FILE \_ FLUSSO \_ DI \_ INTEGRITÀ DEGLI**</dt> ATTRIBUTI <dt>32768 (0x8000)</dt> </dl>                      | Il flusso di dati della directory o dell'utente è configurato con l'integrità (supportata solo nei volumi ReFS). Non è incluso in un elenco di directory normale. L'impostazione di integrità viene mantenuta con il file se viene rinominato. Se un file viene copiato, l'integrità del file di destinazione sarà impostata se per il file di origine o per la directory di destinazione è impostata l'integrità.<br/> **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP:** Questo flag non è supportato fino a Windows Server 2012.<br/>                              |
| <span id="FILE_ATTRIBUTE_NORMAL"></span><span id="file_attribute_normal"></span><dl> <dt>**FILE \_ ATTRIBUTE \_ NORMAL**</dt> <dt>128 (0x80)</dt> </dl>                                                         | File per cui non sono impostati altri attributi. Questo attributo è valido solo se usato da solo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="FILE_ATTRIBUTE_NOT_CONTENT_INDEXED"></span><span id="file_attribute_not_content_indexed"></span><dl> <dt>**FILE \_ ATTRIBUTE \_ NOT \_ CONTENT \_ INDEXED**</dt> <dt>8192 (0x2000)</dt> </dl>             | Il file o la directory non deve essere indicizzato dal servizio di indicizzazione del contenuto.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="FILE_ATTRIBUTE_NO_SCRUB_DATA"></span><span id="file_attribute_no_scrub_data"></span><dl> <dt>**FILE \_ ATTRIBUTO \_ NO \_ SCRUB \_ DATA**</dt> <dt>131072 (0x20000)</dt> </dl>                            | Flusso di dati utente che non deve essere letto dallo strumento di analisi dell'integrità dei dati in background(noto anche come scrubber). Se impostato in una directory, fornisce solo l'ereditarietà. Questo flag è supportato solo nei volumi Spazi di archiviazione e ReFS. Non è incluso in un elenco di directory normale.<br/> **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP:** Questo flag non è supportato fino a Windows 8 e Windows Server 2012.<br/>                                                                                                    |
| <span id="FILE_ATTRIBUTE_OFFLINE"></span><span id="file_attribute_offline"></span><dl> <dt>**FILE \_ ATTRIBUTO \_ OFFLINE**</dt> <dt>4096 (0x1000)</dt> </dl>                                                   | I dati di un file non sono immediatamente disponibili. Questo attributo indica che i dati del file vengono spostati fisicamente nell'archiviazione offline. Questo attributo viene usato da Remote Archiviazione, ovvero il software di gestione dell'archiviazione gerarchico. Le applicazioni non devono modificare arbitrariamente questo attributo.<br/>                                                                                                                                                                                                                                                                         |
| <span id="FILE_ATTRIBUTE_READONLY"></span><span id="file_attribute_readonly"></span><dl> <dt>**FILE \_ ATTRIBUTE \_ READONLY**</dt> <dt>1 (0x1)</dt> </dl>                                                      | File di sola lettura. Le applicazioni possono leggere il file, ma non possono scriverlo o eliminarlo. Questo attributo non viene rispettato nelle directory. Per altre informazioni, vedere Non è possibile visualizzare o modificare gli attributi di sola lettura o di sistema delle cartelle [in Windows Server 2003, in Windows XP, in Windows Vista o in Windows 7.](https://support.microsoft.com/kb/326549)<br/>                                                                                                                                                                                           |
| <span id="FILE_ATTRIBUTE_RECALL_ON_DATA_ACCESS"></span><span id="file_attribute_recall_on_data_access"></span><dl> <dt>**FILE \_ RICHIAMO \_ DEGLI ATTRIBUTI IN DATA \_ \_ \_ ACCESS**</dt> <dt>4194304 (0x400000)</dt> </dl> | Quando questo attributo è impostato, significa che il file o la directory non è completamente presente in locale. Per un file che indica che non tutti i dati si trova nell'archiviazione locale(ad esempio, potrebbe essere di tipo sparse con alcuni dati ancora nell'archiviazione remota). Per una directory significa che parte del contenuto della directory viene virtualizzato da un'altra posizione. La lettura del file o l'enumerazione della directory sarà più costosa del normale, ad esempio causerà il recupero di almeno parte del contenuto di file/directory da un archivio remoto. Solo i chiamanti in modalità kernel possono impostare questo bit.<br/> |
| <span id="FILE_ATTRIBUTE_RECALL_ON_OPEN"></span><span id="file_attribute_recall_on_open"></span><dl> <dt>**FILE \_ RICHIAMO \_ \_ DI ATTRIBUTI IN \_ OPEN**</dt> <dt>262144 (0x40000)</dt> </dl>                         | Questo attributo viene visualizzato solo nelle classi di enumerazione della directory (FILE \_ DIRECTORY \_ INFORMATION, FILE \_ BOTH \_ DIR INFORMATION e così \_ via). Quando questo attributo è impostato, significa che il file o la directory non ha una rappresentazione fisica nel sistema locale; L'elemento è virtuale. L'apertura dell'elemento sarà più costosa del normale, ad esempio ne causerà il recupero di almeno una parte da un archivio remoto.<br/>                                                                                                                                                                 |
| <span id="FILE_ATTRIBUTE_REPARSE_POINT"></span><span id="file_attribute_reparse_point"></span><dl> <dt>**FILE \_ ATTRIBUTE \_ REPARSE \_ POINT**</dt> <dt>1024 (0x400)</dt> </dl>                                 | File o directory a cui è associato un reparse point o un file che rappresenta un collegamento simbolico.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="FILE_ATTRIBUTE_SPARSE_FILE"></span><span id="file_attribute_sparse_file"></span><dl> <dt>**FILE \_ ATTRIBUTE \_ SPARSE \_ FILE**</dt> <dt>512 (0x200)</dt> </dl>                                        | File che è un file sparse.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="FILE_ATTRIBUTE_SYSTEM"></span><span id="file_attribute_system"></span><dl> <dt>**FILE \_ ATTRIBUTE \_ SYSTEM**</dt> <dt>4 (0x4)</dt> </dl>                                                            | File o directory di cui il sistema operativo usa una parte o usa esclusivamente .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="FILE_ATTRIBUTE_TEMPORARY"></span><span id="file_attribute_temporary"></span><dl> <dt>**FILE \_ ATTRIBUTO \_ TEMPORARY**</dt> <dt>256 (0x100)</dt> </dl>                                               | File utilizzato per l'archiviazione temporanea. I file system evitano di scrivere i dati nell'archiviazione di massa se è disponibile memoria cache sufficiente, perché in genere un'applicazione elimina un file temporaneo dopo la chiusura dell'handle. In questo scenario, il sistema può evitare completamente di scrivere i dati. In caso contrario, i dati vengono scritti dopo la chiusura dell'handle.<br/>                                                                                                                                                                                                       |
| <span id="FILE_ATTRIBUTE_VIRTUAL"></span><span id="file_attribute_virtual"></span><dl> <dt>**FILE \_ ATTRIBUTE \_ VIRTUAL**</dt> <dt>65536 (0x10000)</dt> </dl>                                                 | Questo valore è riservato per l'uso da parte del sistema.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                                            |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                   |
| Intestazione<br/>                   | <dl> <dt>WinNT.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Attributo di compressione](compression-attribute.md)
</dt> <dt>

[Creazione e apertura di file](creating-and-opening-files.md)
</dt> <dt>

[**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)
</dt> <dt>

[**CreateFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda)
</dt> <dt>

[**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa)
</dt> <dt>

[**GetFileAttributesEx**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa)
</dt> <dt>

[**GetFileAttributesTransacted**](/windows/desktop/api/WinBase/nf-winbase-getfileattributestransacteda)
</dt> <dt>

[**GetFileInformationByHandle**](/windows/desktop/api/FileAPI/nf-fileapi-getfileinformationbyhandle)
</dt> <dt>

[**GetFileInformationByHandleEx**](/windows/desktop/api/WinBase/nf-winbase-getfileinformationbyhandleex)
</dt> <dt>

[**Attributi SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa)
</dt> <dt>

[**SetFileAttributesTransacted**](/windows/desktop/api/WinBase/nf-winbase-setfileattributestransacteda)
</dt> <dt>

[**SetFileInformationByHandle**](/windows/desktop/api/FileAPI/nf-fileapi-setfileinformationbyhandle)
</dt> </dl>

 

 




