---
description: Un file contrassegnato come crittografato viene crittografato dall'file system NTFS usando il driver di crittografia corrente.
ms.assetid: 166bfb8c-b97d-4cc7-bf6b-399837cb8ad0
title: Gestione di file e directory crittografati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2718656a28eb678c10076e228e08a2a95cabd1fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968400"
---
# <a name="handling-encrypted-files-and-directories"></a>Gestione di file e directory crittografati

Un programmatore o un utente può contrassegnare una directory o un file come crittografato. Un file contrassegnato come crittografato viene crittografato dall'file system NTFS usando il driver di crittografia corrente. Se in un secondo momento il file viene contrassegnato come non crittografato, viene decrittografato e lasciato in uno stato di testo normale (non protetto).

Le directory non vengono crittografate. Per impostazione predefinita, invece, in una directory "crittografata" tutti i nuovi file nella directory vengono crittografati al momento della creazione. Un utente deve modificare in modo specifico lo stato di un nuovo file in decrittografato se l'utente non vuole crittografare il file. Una directory crittografata è visibile. Per rendere una directory inaccessibile ad altri utenti, utilizzare i metodi standard di controllo di accesso.

Non è possibile usare le funzioni di crittografia con l' [API di backup](/windows/desktop/Backup/backup).

Per crittografare un nuovo file, utilizzare la funzione [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) con il flag **\_ \_ crittografato dell'attributo file** . Per crittografare un file esistente, usare la funzione [**EncryptFile**](/windows/desktop/api/WinBase/nf-winbase-encryptfilea) . Tutti i flussi di dati nel file sono crittografati. Se il file è già crittografato, **EncryptFile** non esegue alcuna operazione ma restituisce un valore diverso da zero, che indica l'esito positivo. Se il file è compresso, **EncryptFile** decomprime il file prima di crittografarlo.

Per decrittografare un file crittografato, usare la funzione [**DecryptFile**](/windows/desktop/api/WinBase/nf-winbase-decryptfilea) . Se il file non è crittografato, **DecryptFile** non esegue alcuna operazione ma restituisce un valore diverso da zero che indica l'esito positivo.

La funzione [**EncryptionDisable**](/windows/desktop/api/WinEfs/nf-winefs-encryptiondisable) Disabilita o Abilita la crittografia della directory indicata e dei file al suo interno. Non influisce sulla crittografia delle sottodirectory sotto la directory indicata.

Per recuperare lo stato di crittografia di un file, usare la funzione [**FileEncryptionStatus**](/windows/desktop/api/WinBase/nf-winbase-fileencryptionstatusa) . In alternativa, chiamare la funzione [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) ed esaminare il flag di **\_ attributo \_ crittografato del file** nel valore restituito.

[**CopyFile**](/windows/desktop/api/WinBase/nf-winbase-copyfile) e [**CopyFileEx**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa) tentano di crittografare il file di destinazione con le chiavi usate nella crittografia del file di origine. Se non è possibile eseguire questa operazione, entrambe le funzioni tentano di crittografare il file di destinazione con le chiavi predefinite. Se non è possibile eseguire entrambi questi metodi, **CopyFile** e **CopyFileEx** hanno esito negativo e si **\_ \_ è verificato** un errore di crittografia degli errori. Se si vuole che **CopyFileEx** completi l'operazione di copia anche quando il file di destinazione non può essere crittografato, includere il flag di **\_ \_ \_ \_ destinazione Consenti decrittografia del file** nel valore del parametro *dwCopyFlags* nella chiamata a **CopyFileEx**.

 

 
