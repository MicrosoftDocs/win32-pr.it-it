---
description: Un file contrassegnato come crittografato viene crittografato dal file system NTFS usando il driver di crittografia corrente.
ms.assetid: 166bfb8c-b97d-4cc7-bf6b-399837cb8ad0
title: Gestione di file e directory crittografati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf1a3a7b4a2d38aa2f4e012ccb96d01712f280879ff578afdb5c69392ab826a5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119927791"
---
# <a name="handling-encrypted-files-and-directories"></a>Gestione di file e directory crittografati

Un programmatore o un utente può contrassegnare una directory o un file come crittografato. Un file contrassegnato come crittografato viene crittografato dal file system NTFS usando il driver di crittografia corrente. Se in un secondo momento il file viene contrassegnato come non crittografato, viene decrittografato e lasciato in uno stato di testo normale (non protetto).

Le directory non vengono crittografate. Per impostazione predefinita, invece, in una directory "crittografata" tutti i nuovi file nella directory vengono crittografati al momento della creazione. Un utente deve modificare in modo specifico lo stato di un nuovo file in decrittografato se l'utente non vuole che il file sia crittografato. È visibile una directory crittografata. Per rendere una directory inaccessibile ad altri utenti, usare i metodi standard di controllo di accesso.

Le funzioni di crittografia non possono essere usate con [l'API backup](/windows/desktop/Backup/backup).

Per crittografare un nuovo file, usare [**la funzione CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) con il flag **FILE ATTRIBUTE \_ \_ ENCRYPTED.** Per crittografare un file esistente, usare la [**funzione EncryptFile.**](/windows/desktop/api/WinBase/nf-winbase-encryptfilea) Tutti i flussi di dati nel file vengono crittografati. Se il file è già crittografato, **EncryptFile** non esegue alcuna operazione, ma restituisce un valore diverso da zero, che indica l'esito positivo. Se il file è compresso, **EncryptFile** decomprime il file prima di crittografarlo.

Per decrittografare un file crittografato, usare la [**funzione DecryptFile.**](/windows/desktop/api/WinBase/nf-winbase-decryptfilea) Se il file non è crittografato, **DecryptFile** non esegue alcuna operazione, ma restituisce un valore diverso da zero che indica l'esito positivo.

La [**funzione EncryptionDisable**](/windows/desktop/api/WinEfs/nf-winefs-encryptiondisable) disabilita o abilita la crittografia della directory indicata e dei file in essa presenti. Non influisce sulla crittografia delle sottodirectory sotto la directory indicata.

Per recuperare lo stato di crittografia di un file, usare la [**funzione FileEncryptionStatus.**](/windows/desktop/api/WinBase/nf-winbase-fileencryptionstatusa) In alternativa, chiamare la [**funzione GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) ed esaminare il flag **FILE ATTRIBUTE \_ \_ ENCRYPTED** nel valore restituito.

[**CopyFile**](/windows/desktop/api/WinBase/nf-winbase-copyfile) e [**CopyFileEx**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa) tentano di crittografare il file di destinazione con le chiavi usate nella crittografia del file di origine. Se non è possibile eseguire questa operazione, entrambe le funzioni tentano di crittografare il file di destinazione con chiavi predefinite. Se non è possibile eseguire entrambi questi metodi, **CopyFile** e **CopyFileEx** hanno esito negativo con un **errore ERROR ENCRYPTION \_ \_ FAILED.** Se si desidera che **CopyFileEx** completi l'operazione di copia anche quando non è possibile crittografare il file di destinazione, includere il flag **COPY FILE ALLOW \_ \_ \_ DECRYPTED \_ DESTINATION** nel valore del *parametro dwCopyFlags* nella chiamata a **CopyFileEx**.

 

 
