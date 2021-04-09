---
description: Le funzioni di crittografia RAW consentono di eseguire il backup dei file crittografati.
ms.assetid: 00f9b00e-305d-4554-8b43-7061228c92c3
title: Backup e ripristino di file crittografati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fbc5d1babbbbb92cef9e78f9a0dade702fd63d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049651"
---
# <a name="backup-and-restore-of-encrypted-files"></a>Backup e ripristino di file crittografati

Il Encrypting File System (EFS) filtra l'apertura di un file crittografato in modo che l'applicazione che ha aperto il file ottenga l'accesso alle informazioni non crittografate, a condizione che disponga delle credenziali appropriate per accedere al file e ottenere la chiave necessaria per decrittografare il file. Le successive operazioni di lettura su questo file produrranno testo non crittografato. Questa operazione è molto utile per l'accesso tipico ai file crittografati e consente di mantenere trasparente la crittografia e la decrittografia dei file. Tuttavia, ostacola il backup dei file crittografati, perché se si tenta di eseguire il backup con le chiamate di I/O di file standard come [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea), [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile)e [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile), i file di cui viene eseguito il backup saranno la versione in formato testo normale.

Per risolvere questo problema, vengono fornite le funzioni di crittografia non elaborate. Le applicazioni di backup sono un utente principale previsto per queste funzioni. Le funzioni di crittografia non elaborate sono diverse da quelle di altre funzioni file system in quanto le funzioni di apertura, lettura e scrittura consentono l'accesso ai flussi di dati crittografati non elaborati e consentono anche la lettura/scrittura del flusso di $EFS. Pertanto, il chiamante delle funzioni di crittografia non elaborate non necessita dell'accesso alle chiavi crittografiche che decrittografano il file. Le API di crittografia raw seguenti sono disponibili per l'uso con le applicazioni di backup e ripristino: 

| API di crittografia non elaborata                                     | Descrizione                                                                                                                                                                                                                                                                   |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**OpenEncryptedFileRaw**](/windows/desktop/api/WinBase/nf-winbase-openencryptedfilerawa)   | Aprire un file crittografato con accesso ai dati in formato crittografato. Se il chiamante non ha accesso alla chiave per il file, il chiamante deve [SeBackupPrivilege](/windows/desktop/SecAuthZ/authorization-constants) per esportare i file crittografati o SeRestorePrivilege per importare i file crittografati. |
| [**CloseEncryptedFileRaw**](/windows/desktop/api/WinBase/nf-winbase-closeencryptedfileraw) | Chiude un file crittografato aperto con [ **OpenEncryptedFileRaw**](/windows/desktop/api/WinBase/nf-winbase-openencryptedfilerawa)                                                                                                                                                                                      |
| [**ReadEncryptedFileRaw**](/windows/desktop/api/WinBase/nf-winbase-readencryptedfileraw)   | Lettura di un file crittografato lasciando i dati in formato crittografato                                                                                                                                                                                                                   |
| [**WriteEncryptedFileRaw**](/windows/desktop/api/WinBase/nf-winbase-writeencryptedfileraw) | Scrivere un file crittografato lasciando i dati in formato crittografato                                                                                                                                                                                                                  |
| [**ImportCallback**](/windows/desktop/api/WinBase/nc-winbase-pfe_import_func)               | Callback definito dall'applicazione per l'uso con [ **WriteEncryptedFileRaw**](/windows/desktop/api/WinBase/nf-winbase-writeencryptedfileraw)                                                                                                                                                                              |
| [**ExportCallback**](/windows/desktop/api/WinBase/nc-winbase-pfe_export_func)               | Callback definito dall'applicazione per l'uso con [ **ReadEncryptedFileRaw**](/windows/desktop/api/WinBase/nf-winbase-readencryptedfileraw)                                                                                                                                                                                |



 

 

 
