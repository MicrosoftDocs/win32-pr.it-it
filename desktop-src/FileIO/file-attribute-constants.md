---
Description: Gli attributi di file sono valori di metadati archiviati dal file system su disco e usati dal sistema e sono disponibili per gli sviluppatori tramite varie API di I/O di file.
ms.assetid: ed9a73d2-7fb6-4fb7-97f6-4dbf89e2f156
title: Costanti di attributi file (WinNT. h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/23/2020
ms.openlocfilehash: eae376462ae6c633be96e4434fbb782fa41c802f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324254"
---
# <a name="file-attribute-constants"></a>Costanti di attributi file

Gli attributi di file sono valori di metadati archiviati dal file system su disco e usati dal sistema e sono disponibili per gli sviluppatori tramite varie API di I/O di file. Per un elenco di API e argomenti correlati, vedere la sezione vedere anche.

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

Esempio tratto da un [esempio di Windows classico](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/winbase/io/extendedfileapis/ExtendedFileAPIs.cpp) in GitHub.



| Costante/valore                                                                                                                                                                                                                                                                                                 | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FILE_ATTRIBUTE_ARCHIVE"></span><span id="file_attribute_archive"></span><dl> <dt>**File \_ \_Archivio attributi**</dt> <dt>32 (0x20)</dt> </dl>                                                       | Un file o una directory che corrisponde A un file di archivio o A una directory. Le applicazioni in genere usano questo attributo per contrassegnare i file per il backup o la rimozione. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="FILE_ATTRIBUTE_COMPRESSED"></span><span id="file_attribute_compressed"></span><dl> <dt>**File \_ ATTRIBUTO \_ compresso**</dt> <dt>2048 (0x800)</dt> </dl>                                           | Un file o una directory compressa. Per un file, tutti i dati nel file vengono compressi. Per una directory, la compressione è l'impostazione predefinita per i file e le sottodirectory appena creati.<br/>                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="FILE_ATTRIBUTE_DEVICE"></span><span id="file_attribute_device"></span><dl> <dt>**File \_ ATTRIBUTO \_ DEVICE**</dt> <dt>64 (0x40)</dt> </dl>                                                          | Questo valore è riservato per l'utilizzo del sistema.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="FILE_ATTRIBUTE_DIRECTORY"></span><span id="file_attribute_directory"></span><dl> <dt>**File \_ \_Directory degli attributi**</dt> <dt>16 (0x10)</dt> </dl>                                                 | Handle che identifica una directory.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="FILE_ATTRIBUTE_ENCRYPTED"></span><span id="file_attribute_encrypted"></span><dl> <dt>**File \_ ATTRIBUTO \_ crittografato**</dt> <dt>16384 (0x4000)</dt> </dl>                                            | File o directory crittografata. Per un file, tutti i flussi di dati nel file vengono crittografati. Per una directory, la crittografia è l'impostazione predefinita per i file e le sottodirectory appena creati.<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="FILE_ATTRIBUTE_HIDDEN"></span><span id="file_attribute_hidden"></span><dl> <dt>**File \_ ATTRIBUTO \_ nascosto**</dt> <dt>2 (0x2)</dt> </dl>                                                            | Il file o la directory è nascosta. Non è incluso in un elenco di directory ordinarie.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="FILE_ATTRIBUTE_INTEGRITY_STREAM"></span><span id="file_attribute_integrity_stream"></span><dl> <dt>**File \_ \_ \_ Flusso di integrità degli attributi**</dt> <dt>32768 (0x8000)</dt> </dl>                      | Il flusso di dati utente o directory è configurato con l'integrità (supportata solo nei volumi ReFS). Non è incluso in un elenco di directory ordinarie. L'impostazione di integrità viene mantenute con il file se è stato rinominato. Se viene copiato un file, il file di destinazione avrà un set di integrità se il file di origine o la directory di destinazione hanno impostato l'integrità.<br/> **Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Questo flag non è supportato fino a Windows Server 2012.<br/>                              |
| <span id="FILE_ATTRIBUTE_NORMAL"></span><span id="file_attribute_normal"></span><dl> <dt>**File \_ ATTRIBUTO \_ NORMAL**</dt> <dt>128 (0x80)</dt> </dl>                                                         | Un file per il quale non sono impostati altri attributi. Questo attributo è valido solo se usato da solo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="FILE_ATTRIBUTE_NOT_CONTENT_INDEXED"></span><span id="file_attribute_not_content_indexed"></span><dl> <dt>**File \_ ATTRIBUTO \_ non \_ contenuto \_ indicizzato**</dt> <dt>8192 (0x2000)</dt> </dl>             | Il file o la directory non deve essere indicizzata dal servizio di indicizzazione del contenuto.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="FILE_ATTRIBUTE_NO_SCRUB_DATA"></span><span id="file_attribute_no_scrub_data"></span><dl> <dt>**File \_ ATTRIBUTO \_ nessun \_ \_ dato di scrub**</dt> <dt>131072 (0x20000)</dt> </dl>                            | Flusso di dati utente che non deve essere letto dallo scanner di integrità dei dati in background (noto anche come pulitura). Se impostata su una directory, fornisce solo l'ereditarietà. Questo flag è supportato solo nei volumi di spazi di archiviazione e ReFS. Non è incluso in un elenco di directory ordinarie.<br/> **Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Questo flag non è supportato fino a Windows 8 e Windows Server 2012.<br/>                                                                                                    |
| <span id="FILE_ATTRIBUTE_OFFLINE"></span><span id="file_attribute_offline"></span><dl> <dt>**File \_ ATTRIBUTO \_ OFFLINE**</dt> <dt>4096 (0x1000)</dt> </dl>                                                   | I dati di un file non sono immediatamente disponibili. Questo attributo indica che i dati del file vengono spostati fisicamente nell'archivio offline. Questo attributo viene usato dall'archiviazione remota, ovvero il software di gestione dell'archiviazione gerarchica. Le applicazioni non devono modificare arbitrariamente questo attributo.<br/>                                                                                                                                                                                                                                                                         |
| <span id="FILE_ATTRIBUTE_READONLY"></span><span id="file_attribute_readonly"></span><dl> <dt>**File \_ ATTRIBUTO \_ ReadOnly**</dt> <dt>1 (0x1)</dt> </dl>                                                      | File di sola lettura. Le applicazioni sono in grado di leggere il file, ma non di scriverlo o eliminarlo. Questo attributo non viene rispettato nelle directory. Per ulteriori informazioni, vedere [non è possibile visualizzare o modificare gli attributi di sola lettura o di sistema delle cartelle in Windows Server 2003, in Windows XP, in Windows Vista o in Windows 7](https://support.microsoft.com/kb/326549).<br/>                                                                                                                                                                                           |
| <span id="FILE_ATTRIBUTE_RECALL_ON_DATA_ACCESS"></span><span id="file_attribute_recall_on_data_access"></span><dl> <dt>**File \_ \_Richiamo attributi \_ sull' \_ \_ accesso ai dati**</dt> <dt>4194304 (0x400000)</dt> </dl> | Quando questo attributo è impostato, significa che il file o la directory non è completamente presente localmente. Per un file che significa che non tutti i relativi dati si trova nella risorsa di archiviazione locale (ad esempio, può essere di tipo sparse con alcuni dati ancora in archiviazione remota). Per una directory significa che parte del contenuto della directory viene virtualizzata da un'altra posizione. La lettura del file/enumerazione della directory sarà più costosa del normale, ad esempio, verrà recuperato almeno un contenuto di file/directory da un archivio remoto. Solo i chiamanti in modalità kernel possono impostare questo bit.<br/> |
| <span id="FILE_ATTRIBUTE_RECALL_ON_OPEN"></span><span id="file_attribute_recall_on_open"></span><dl> <dt>**File \_ \_Richiamo attributi \_ all' \_ apertura**</dt> <dt>262144 (0x40000)</dt> </dl>                         | Questo attributo viene visualizzato solo nelle classi di enumerazione directory \_ ( \_ informazioni directory FILE, file \_ sia \_ \_ informazioni dir, ecc.). Quando questo attributo è impostato, significa che il file o la directory non dispone di una rappresentazione fisica nel sistema locale; l'elemento è virtuale. L'apertura dell'elemento sarà più costosa del normale, ad esempio ne determinerà il recupero di almeno parte di esso da un archivio remoto.<br/>                                                                                                                                                                 |
| <span id="FILE_ATTRIBUTE_REPARSE_POINT"></span><span id="file_attribute_reparse_point"></span><dl> <dt>**File \_ \_ \_ Punto di analisi degli attributi**</dt> <dt>1024 (0x400)</dt> </dl>                                 | Un file o una directory a cui è associato un reparse point o un file che rappresenta un collegamento simbolico.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="FILE_ATTRIBUTE_SPARSE_FILE"></span><span id="file_attribute_sparse_file"></span><dl> <dt>**File \_ \_ \_ File sparse degli attributi**</dt> <dt>512 (0x200)</dt> </dl>                                        | File di tipo sparse.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="FILE_ATTRIBUTE_SYSTEM"></span><span id="file_attribute_system"></span><dl> <dt>**File \_ \_Sistema di attributi**</dt> <dt>4 (0x4)</dt> </dl>                                                            | Un file o una directory utilizzata dal sistema operativo o esclusivamente.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="FILE_ATTRIBUTE_TEMPORARY"></span><span id="file_attribute_temporary"></span><dl> <dt>**File \_ ATTRIBUTO \_ temporaneo**</dt> <dt>256 (0x100)</dt> </dl>                                               | File utilizzato per l'archiviazione temporanea. I file System evitano di scrivere dati nell'archiviazione di massa se è disponibile memoria sufficiente per la cache, perché in genere un'applicazione elimina un file temporaneo dopo la chiusura dell'handle. In questo scenario, il sistema può evitare completamente di scrivere i dati. In caso contrario, i dati vengono scritti dopo la chiusura dell'handle.<br/>                                                                                                                                                                                                       |
| <span id="FILE_ATTRIBUTE_VIRTUAL"></span><span id="file_attribute_virtual"></span><dl> <dt>**File \_ ATTRIBUTO \_ VIRTUAL**</dt> <dt>65536 (0x10000)</dt> </dl>                                                 | Questo valore è riservato per l'utilizzo del sistema.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                   |
| Intestazione<br/>                   | <dl> <dt>WinNT. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Attributo Compression](compression-attribute.md)
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

[**SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa)
</dt> <dt>

[**SetFileAttributesTransacted**](/windows/desktop/api/WinBase/nf-winbase-setfileattributestransacteda)
</dt> <dt>

[**SetFileInformationByHandle**](/windows/desktop/api/FileAPI/nf-fileapi-setfileinformationbyhandle)
</dt> </dl>

 

 




