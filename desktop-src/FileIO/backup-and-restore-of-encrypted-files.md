---
description: Le funzioni di crittografia non elaborata consentono il backup dei file crittografati.
ms.assetid: 00f9b00e-305d-4554-8b43-7061228c92c3
title: Backup e ripristino di file crittografati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34308dbfc0f67a1fcf9a70f1f7a5878434018494fa1450d308fa493af78226ca
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119766181"
---
# <a name="backup-and-restore-of-encrypted-files"></a>Backup e ripristino di file crittografati

Il Encrypting File System (EFS) filtra l'apertura di un file crittografato in modo che l'applicazione che ha aperto il file otterrà l'accesso alle informazioni non crittografate, purché abbia naturalmente le credenziali appropriate per accedere al file e ottenere la chiave necessaria per decrittografare il file. Le successive operazioni di lettura su questo file generano testo non crittografato. Questo è molto utile per l'accesso tipico ai file crittografati e mantiene trasparente la crittografia e la decrittografia dei file. Tuttavia, impedisce il backup dei file crittografati, perché se si tenta di eseguire il backup con le chiamate I/O di file standard come [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea), [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile)e [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile), i file di cui è stato eseguito il backup saranno la versione in testo normale.

Per risolvere questo problema vengono fornite le funzioni di crittografia non elaborata. Le applicazioni di backup sono un utente destinato principalmente a queste funzioni. Le funzioni di crittografia non elaborata si differenziano dalle altre funzioni file system in modo che le funzioni di apertura, lettura e scrittura consentano l'accesso ai flussi di dati crittografati non elaborati e consentono anche la lettura/scrittura del flusso $EFS non elaborato. Pertanto, il chiamante delle funzioni di crittografia non elaborato non deve accedere alle chiavi crittografiche che decrittografano il file. Le API di crittografia non elaborata seguenti sono disponibili per l'uso con le applicazioni di backup e ripristino: 

| API di crittografia non elaborata                                     | Descrizione                                                                                                                                                                                                                                                                   |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**OpenEncryptedFileRaw**](/windows/desktop/api/WinBase/nf-winbase-openencryptedfilerawa)   | Aprire un file crittografato con accesso ai dati in formato crittografato. Se il chiamante non ha accesso alla chiave per il file, il chiamante deve [seBackupPrivilege](/windows/desktop/SecAuthZ/authorization-constants) per esportare i file crittografati o SeRestorePrivilege per importare i file crittografati. |
| [**CloseEncryptedFileRaw**](/windows/desktop/api/WinBase/nf-winbase-closeencryptedfileraw) | Chiudere un file crittografato aperto [ **con OpenEncryptedFileRaw**](/windows/desktop/api/WinBase/nf-winbase-openencryptedfilerawa)                                                                                                                                                                                      |
| [**ReadEncryptedFileRaw**](/windows/desktop/api/WinBase/nf-winbase-readencryptedfileraw)   | Leggere un file crittografato lasciando i dati in formato crittografato                                                                                                                                                                                                                   |
| [**WriteEncryptedFileRaw**](/windows/desktop/api/WinBase/nf-winbase-writeencryptedfileraw) | Scrivere un file crittografato lasciando i dati in formato crittografato                                                                                                                                                                                                                  |
| [**ImportCallback**](/windows/desktop/api/WinBase/nc-winbase-pfe_import_func)               | Callback definito dall'applicazione da usare [ **con WriteEncryptedFileRaw**](/windows/desktop/api/WinBase/nf-winbase-writeencryptedfileraw)                                                                                                                                                                              |
| [**ExportCallback**](/windows/desktop/api/WinBase/nc-winbase-pfe_export_func)               | Callback definito dall'applicazione da usare [ **con ReadEncryptedFileRaw**](/windows/desktop/api/WinBase/nf-winbase-readencryptedfileraw)                                                                                                                                                                                |



 

 

 
