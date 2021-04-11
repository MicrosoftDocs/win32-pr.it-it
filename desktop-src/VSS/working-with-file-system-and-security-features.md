---
description: Di seguito sono riportati alcuni suggerimenti per l'interoperabilità corretta con diverse funzionalità di file system e sicurezza introdotte in Windows Vista e Windows Server 2008.
ms.assetid: 3e8a1fd2-59e5-4f18-aafc-0ce5ac1e1cfa
title: Utilizzo delle funzionalità di sicurezza e file System
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12903599beb7ed153965f4b803ad8147fd32067a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129271"
---
# <a name="working-with-file-system-and-security-features"></a>Utilizzo delle funzionalità di sicurezza e file System

Di seguito sono riportati alcuni suggerimenti per l'interoperabilità corretta con diverse funzionalità di file system e sicurezza introdotte in Windows Vista e Windows Server 2008.

## <a name="interoperability-with-transactions"></a>Interoperabilità con transazioni

Per supportare le transazioni, VSS garantisce che sia la gestione transazioni kernel (KTM) che la Distributed Transaction Coordinator (DTC) siano bloccate prima della creazione delle copie shadow del volume. Se il sistema non riesce a bloccare o scongelare KTM o DTC, il metodo [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) può restituire gli errori di timeout seguenti:

<dl> \_ \_ \_ timeout blocco transazioni VSS \_ E  
\_timeout di \_ \_ sblocco transazione VSS E \_  
</dl>

Se il richiedente riceve uno di questi codici di errore, deve ritentare la creazione della copia shadow.

Anche le operazioni di registro e file system possono essere transazionali. Nel caso del registro di sistema, il writer del registro di sistema è responsabile di garantire la coerenza delle transazioni. Nel caso di operazioni di file system transazionale NTFS (TxF), il provider di sistema è responsabile di garantire la coerenza delle transazioni. Questa operazione viene eseguita montando la copia shadow come di lettura/scrittura dopo che è stata creata per consentire il ripristino automatico. Durante la fase di recupero automatico, KTM esegue il rollback di tutte le transazioni incomplete.

## <a name="identifying-and-creating-hard-links"></a>Identificazione e creazione di collegamenti reali

Quando si esegue il backup dei file, un'applicazione di backup deve identificare tutti i collegamenti reali a ogni file per evitare di eseguire il backup dello stesso file più di una volta. Per l'enumerazione dei collegamenti reali sono disponibili due nuove funzioni: [**FindFirstFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findfirstfilenamew) e [**FindNextFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findnextfilenamew).

Analogamente, quando si ripristinano i file, l'applicazione di backup deve ripristinare i collegamenti reali utilizzando la funzione [**CreateHardLink**](/windows/win32/api/winbase/nf-winbase-createhardlinka) .

Le applicazioni di backup devono anche dichiarare \_ il \_ privilegio di nome backup se durante la fase di backup e il \_ nome del ripristino se \_ durante la fase di ripristino.

## <a name="permissions-and-privileges-required-by-backup-applications"></a>Autorizzazioni e privilegi richiesti dalle applicazioni di backup

Per le applicazioni di backup che ripristinano i file di sistema sono necessari i privilegi seguenti:

<dl> \_nome backup \_ se  
\_nome ripristino \_ se  
\_nome sicurezza \_ se  
\_nome del \_ proprietario \_  
</dl>

Anche le applicazioni di backup devono richiedere \_ i diritti di accesso del proprietario della scrittura durante la fase di ripristino.

## <a name="windows-media-digital-rights-management"></a>Windows Media Digital Rights Management

Il client Windows Media Digital Rights Management (DRM) gestisce una directory di file di licenza e di stato sensibili nella directory% ProgramData% \\ Microsoft \\ Windows \\ DRM. I file in questa directory devono essere eliminati contemporaneamente ai file temporanei e di cache. Per assicurarsi che il client DRM di Windows rimanga in uno stato coerente, è necessario evitare di eseguire il backup o il ripristino di questi file. Questa directory è elencata nella chiave del registro di sistema FilesNotToBackup. Per ulteriori informazioni sulla chiave FilesNotToBackup, vedere [generazione di un set di backup](generating-a-backup-set.md).

## <a name="user-account-control"></a>Controllo dell'account utente

L'introduzione di controllo dell'account utente in Windows Vista indica che, se non specificato diversamente, le applicazioni devono essere eseguite con un account utente standard. Inoltre, la funzionalità di virtualizzazione di file e registro di sistema di controllo dell'account utente modifica i percorsi in cui vengono archiviati i dati utente. Per altre informazioni su come usare UAC e la virtualizzazione di file e registro di sistema, vedere i riferimenti seguenti:

<dl>

[Windows Vista e Windows Server 2008 Developer Story: requisiti per lo sviluppo di applicazioni Windows Vista per il controllo dell'account utente (UAC)](/previous-versions/aa905330(v=msdn.10))  
[Requisiti per lo sviluppo di applicazioni Windows Vista per la compatibilità con controllo dell'account utente](/previous-versions/dotnet/articles/bb530410(v=msdn.10))  
[Applicazione di patch al controllo dell'account utente (UAC)](../msi/user-account-control--uac--patching.md)  
</dl>

## <a name="bitlocker-drive-encryption"></a>Crittografia unità BitLocker

Crittografia unità BitLocker è una nuova funzionalità di Windows Vista Enterprise, Windows Vista Ultimate e Windows Server 2008 che offre avvio sicuro e crittografia completa del volume. La comprensione di questa funzionalità è importante per gli sviluppatori di applicazioni di backup che eseguono ripristini offline in cui potrebbe essere necessario ripristinare i dati in un'unità crittografata.

Per ripristinare i dati in un'unità crittografata, seguire questa procedura:

1.  Sbloccare l'unità.
2.  Disattivare Crittografia unità BitLocker.
3.  Eseguire il ripristino.
4.  Avviare il sistema operativo ripristinato e attivare Crittografia unità BitLocker.

Per informazioni dettagliate sui Crittografia unità BitLocker, inclusa una guida dettagliata, vedere [crittografia unità BitLocker](https://www.microsoft.com/technet/windowsvista/security/bitlockr.mspx) sul sito Web Microsoft TechNet per Windows Vista. Per informazioni sul provider WMI Crittografia unità BitLocker, vedere [provider di crittografia unità BitLocker](../secprov/bitlocker-drive-encryption-provider.md).

 

 
