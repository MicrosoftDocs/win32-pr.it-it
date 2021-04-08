---
title: Funzioni di backup
description: Le funzioni seguenti vengono utilizzate con il backup su nastro.
ms.assetid: 8c5f92f7-4918-475c-bc86-2b02291488d5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 312c7477c28f83b7c1c64073234799219346f89a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728919"
---
# <a name="backup-functions"></a>Funzioni di backup

Le funzioni seguenti vengono utilizzate con il [backup su nastro](tape-backup.md).



| Funzione                                           | Descrizione                                                                                            |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**BackupRead**](/windows/desktop/api/Winbase/nf-winbase-backupread)                   | Legge i dati associati a un file o a una directory specificata in un buffer.                                |
| [**BackupSeek**](/windows/desktop/api/Winbase/nf-winbase-backupseek)                   | Cerca in futuro in un flusso di dati.                                                                        |
| [**BackupWrite**](/windows/desktop/api/Winbase/nf-winbase-backupwrite)                 | Scrive un flusso di dati da un buffer a un file o a una directory specificata.                                |
| [**CreateTapePartition**](/windows/desktop/api/Winbase/nf-winbase-createtapepartition) | Riformatta un nastro.                                                                                      |
| [**EraseTape**](/windows/desktop/api/Winbase/nf-winbase-erasetape)                     | Cancella tutto o parte di un nastro.                                                                          |
| [**GetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-gettapeparameters)     | Recupera le informazioni che descrivono il nastro o l'unità nastro.                                       |
| [**GetTapePosition**](/windows/desktop/api/Winbase/nf-winbase-gettapeposition)         | Recupera l'indirizzo corrente del nastro.                                                             |
| [**GetTapeStatus**](/windows/desktop/api/Winbase/nf-winbase-gettapestatus)             | Determina se il dispositivo nastro è pronto per l'elaborazione dei comandi del nastro.                                  |
| [**PrepareTape**](/windows/desktop/api/Winbase/nf-winbase-preparetape)                 | Prepara il nastro per l'accesso o la rimozione.                                                           |
| [**SetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-settapeparameters)     | Specifica la dimensione del blocco di un nastro o la configurazione del dispositivo nastro.                                      |
| [**SetTapePosition**](/windows/desktop/api/Winbase/nf-winbase-settapeposition)         | Imposta la posizione del nastro sul dispositivo specificato.                                                        |
| [**WriteTapemark**](/windows/desktop/api/Winbase/nf-winbase-writetapemark)             | Scrive un numero specificato di filemark, i contrassegni, i filemark brevi o i filemark lunghi in un dispositivo nastro. |



 

Per lavorare con l' [archivio a istanza singola e il backup SIS](single-instance-store-and-sis-backup.md)sono disponibili le funzioni seguenti.



| Funzione                                                          | Descrizione                                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [**SisCreateBackupStructure**](siscreatebackupstructure.md)      | Crea la struttura di backup SIS specificata in base alle informazioni fornite.                      |
| [**SisCreateRestoreStructure**](siscreaterestorestructure.md)    | Crea la struttura di ripristino SIS specificata in base alle informazioni fornite.                     |
| [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md)    | Restituisce informazioni che descrivono i file dell'archivio comune a cui punta il collegamento SIS specificato.            |
| [**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md)          | Libera la memoria allocata dalle funzioni API SIS.                                                       |
| [**SisFreeBackupStructure**](sisfreebackupstructure.md)          | Libera la struttura di backup SIS specificata.                                                          |
| [**SisFreeRestoreStructure**](sisfreerestorestructure.md)        | Libera la struttura di ripristino SIS specificata.                                                         |
| [**StoreFile SisRestoredCommon**](sisrestoredcommonstorefile.md) | Segnala all'architettura SIS che è stato scritto un file di archivio comune.                         |
| [**SisRestoredLink**](sisrestoredlink.md)                        | Restituisce i nomi del file o dei file dell'archivio comune a cui fa riferimento il collegamento SIS ripristinato specificato. |



 

Per lavorare con il [backup e il ripristino di file crittografati](/windows/desktop/FileIO/backup-and-restore-of-encrypted-files)sono disponibili le funzioni seguenti.



| Funzione                                                | Descrizione                                                                                |
|---------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**CloseEncryptedFileRaw**](/windows/desktop/api/winbase/nf-winbase-closeencryptedfileraw) | Chiudere un file crittografato aperto con [**OpenEncryptedFileRaw**](/windows/desktop/api/winbase/nf-winbase-openencryptedfilerawa). |
| [**OpenEncryptedFileRaw**](/windows/desktop/api/winbase/nf-winbase-openencryptedfilerawa)   | Aprire un file crittografato con accesso ai dati in formato crittografato.                            |
| [**ReadEncryptedFileRaw**](/windows/desktop/api/winbase/nf-winbase-readencryptedfileraw)   | Leggere un file crittografato lasciando i dati in formato crittografato.                               |
| [**WriteEncryptedFileRaw**](/windows/desktop/api/winbase/nf-winbase-writeencryptedfileraw) | Scrivere un file crittografato lasciando i dati in formato crittografato.                              |



 

 

 