---
title: Funzioni di backup
description: Con il backup su nastro vengono utilizzate le funzioni seguenti.
ms.assetid: 8c5f92f7-4918-475c-bc86-2b02291488d5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2164958d7261c4c22caf1ac5124f524eca2f7ed355b082bede59d66a2e6fe697
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119529611"
---
# <a name="backup-functions"></a>Funzioni di backup

Le funzioni seguenti vengono utilizzate con il [backup su nastro.](tape-backup.md)



| Funzione                                           | Descrizione                                                                                            |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**BackupRead**](/windows/desktop/api/Winbase/nf-winbase-backupread)                   | Legge i dati associati a un file o a una directory specificata in un buffer.                                |
| [**BackupSeek**](/windows/desktop/api/Winbase/nf-winbase-backupseek)                   | Cerca in avanti in un flusso di dati.                                                                        |
| [**BackupWrite**](/windows/desktop/api/Winbase/nf-winbase-backupwrite)                 | Scrive un flusso di dati da un buffer in un file o in una directory specificata.                                |
| [**CreateTapePartition**](/windows/desktop/api/Winbase/nf-winbase-createtapepartition) | Riformatta un nastro.                                                                                      |
| [**EraseTape**](/windows/desktop/api/Winbase/nf-winbase-erasetape)                     | Cancella tutto o parte di un nastro.                                                                          |
| [**GetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-gettapeparameters)     | Recupera informazioni che descrivono il nastro o l'unità nastro.                                       |
| [**GetTapePosition**](/windows/desktop/api/Winbase/nf-winbase-gettapeposition)         | Recupera l'indirizzo corrente del nastro.                                                             |
| [**GetTapeStatus**](/windows/desktop/api/Winbase/nf-winbase-gettapestatus)             | Determina se il dispositivo nastro è pronto per elaborare i comandi del nastro.                                  |
| [**PrepareTape**](/windows/desktop/api/Winbase/nf-winbase-preparetape)                 | Prepara il nastro per l'accesso o la rimozione.                                                           |
| [**SetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-settapeparameters)     | Specifica le dimensioni del blocco di un nastro o configura il dispositivo nastro.                                      |
| [**SetTapePosition**](/windows/desktop/api/Winbase/nf-winbase-settapeposition)         | Imposta la posizione del nastro sul dispositivo specificato.                                                        |
| [**WriteTapemark**](/windows/desktop/api/Winbase/nf-winbase-writetapemark)             | Scrive un numero specificato di contrassegni file, setmark, brevi contrassegni file o lunghi contrassegni file in un dispositivo nastro. |



 

Le funzioni seguenti sono disponibili per l'uso con [l'archivio a istanza singola e il backup SIS](single-instance-store-and-sis-backup.md).



| Funzione                                                          | Descrizione                                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [**SisCreateBackupStructure**](siscreatebackupstructure.md)      | Crea la struttura di backup SIS specificata in base alle informazioni fornite.                      |
| [**SisCreateRestoreStructure**](siscreaterestorestructure.md)    | Crea la struttura di ripristino SIS specificata in base alle informazioni fornite.                     |
| [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md)    | Restituisce informazioni che descrivono i file di archivio comune a cui punta il collegamento SIS specificato.            |
| [**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md)          | Libera la memoria allocata dalle funzioni DELL'API SIS.                                                       |
| [**SisFreeBackupStructure**](sisfreebackupstructure.md)          | Libera la struttura di backup SIS specificata.                                                          |
| [**SisFreeRestoreStructure**](sisfreerestorestructure.md)        | Libera la struttura di ripristino SIS specificata.                                                         |
| [**SisRestoredCommon StoreFile**](sisrestoredcommonstorefile.md) | Segnala all'architettura SIS che è stato scritto un file di archivio comune.                         |
| [**SisRestoredLink**](sisrestoredlink.md)                        | Restituisce i nomi dei file di archivio comune a cui punta il collegamento SIS ripristinato specificato. |



 

Le funzioni seguenti sono disponibili per l'utilizzo del [backup e del ripristino di file crittografati.](/windows/desktop/FileIO/backup-and-restore-of-encrypted-files)



| Funzione                                                | Descrizione                                                                                |
|---------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**CloseEncryptedFileRaw**](/windows/desktop/api/winbase/nf-winbase-closeencryptedfileraw) | Chiudere un file crittografato aperto [**con OpenEncryptedFileRaw.**](/windows/desktop/api/winbase/nf-winbase-openencryptedfilerawa) |
| [**OpenEncryptedFileRaw**](/windows/desktop/api/winbase/nf-winbase-openencryptedfilerawa)   | Aprire un file crittografato con accesso ai dati in formato crittografato.                            |
| [**ReadEncryptedFileRaw**](/windows/desktop/api/winbase/nf-winbase-readencryptedfileraw)   | Leggere un file crittografato lasciando i dati in formato crittografato.                               |
| [**WriteEncryptedFileRaw**](/windows/desktop/api/winbase/nf-winbase-writeencryptedfileraw) | Scrivere un file crittografato lasciando i dati in formato crittografato.                              |



 

 

 