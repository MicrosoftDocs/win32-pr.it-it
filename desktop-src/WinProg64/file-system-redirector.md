---
title: File System Redirector
description: La directory windir System32 è riservata per le applicazioni a 64 bit in applicazioni a \\ 64 bit Windows.
ms.assetid: b4d36fe8-8bbb-469b-8ad1-650d559a4c75
keywords:
- file system redirector a 64 bit Windows programmazione
- Guida alla programmazione Windows a 64 bit Windows programmazione a 64 bit , file system redirector
- Wow64 64-bit Windows Programming , file system redirector
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 318a04d85309ca6c97c87ae2d6a580a85f1a4ee224e162a008034e731a1ff557
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119569971"
---
# <a name="file-system-redirector"></a>File System Redirector

La directory %windir% System32 è riservata alle applicazioni a \\ 64 bit Windows. La maggior parte dei nomi di file DLL non è stata modificata quando sono state create versioni a 64 bit delle DLL, quindi le versioni a 32 bit delle DLL vengono archiviate in una directory diversa. WOW64 nasconde questa differenza usando un *file system di reindirizzamento.*

Nella maggior parte dei casi, ogni volta che un'applicazione a 32 bit tenta di accedere a %windir% \\ System32, %windir% \\ lastgood \\ system32 o %windir%regedit.exe, l'accesso viene reindirizzato a un percorso specifico \\ dell'architettura.

> [!Note]  
> Questi percorsi vengono forniti solo come riferimento. Per garantire la compatibilità, le applicazioni non devono usare direttamente questi percorsi. Devono invece chiamare le API descritte di seguito.

 



| Percorso originale                | Percorso reindirizzato per processi x86 a 32 bit | Percorso reindirizzato per processi ARM a 32 bit |
|------------------------------|------------------------------------------|------------------------------------------|
| %windir% \\ System32           | %windir% \\ SysWOW64                       | %windir% \\ SysArm32                       |
| %windir% \\ lastgood \\ system32 | %windir% \\ lastgood \\ SysWOW64             | %windir% \\ lastgood \\ SysArm32             |
| %windir% \\regedit.exe        | %windir% \\ SysWOW64 \\regedit.exe          | %windir% \\ SysArm32 \\regedit.exe         |



 

Se l'accesso fa sì che il sistema visualizza il prompt di Controllo dell'account utente, il reindirizzamento non viene eseguito. Viene invece avviata la versione a 64 bit del file richiesto. Per evitare questo problema, specificare la directory SysWOW64 per evitare il reindirizzamento e verificare l'accesso alla versione a 32 bit del file oppure eseguire l'applicazione a 32 bit con privilegi di amministratore in modo che il prompt di Controllo dell'account utente non venga visualizzato.

**Windows Server 2003 e Windows XP: Controllo dell'account utente ** non è supportato.

Alcune sottodirectory sono esenti dal reindirizzamento. L'accesso a queste sottodirectory non viene reindirizzato a %windir% \\ SysWOW64: <dl> %windir% \\ system32 \\ catroot  
%windir% \\ system32 \\ catroot2  
%windir% \\ system32 \\ driverstore  
%windir% \\ driver system32 \\ e così \\ via  
%windir% \\ system32 \\ logfiles  
%windir% \\ system32 \\ spool  
</dl>

**Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP: **%windir% \\ system32 \\ driverstore viene reindirizzato.

Per recuperare il nome della directory di sistema a 32 bit, le applicazioni a 64 bit devono usare la funzione [**GetSystemWow64Directory2**](/windows/desktop/api/wow64apiset/nf-wow64apiset-getsystemwow64directory2a) (Windows 10, versione 1511) o [**la funzione GetSystemWow64Directory.**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath)

Le applicazioni devono usare [**la funzione SHGetKnownFolderPath**](https://www.bing.com/search?q=**SHGetKnownFolderPath**) per determinare il nome di directory %ProgramFiles%.

**Windows Server 2003 e Windows XP:** Le applicazioni devono usare [**la funzione SHGetSpecialFolderPath**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetspecialfolderpatha) per determinare il nome di directory %ProgramFiles%.

Le applicazioni possono controllare il redirector file system WOW64 usando le funzioni [**Wow64DisableWow64FsRedirection**](/windows/desktop/api/wow64apiset/nf-wow64apiset-wow64disablewow64fsredirection), [**Wow64EnableWow64FsRedirection**](/windows/desktop/api/winbase/nf-winbase-wow64enablewow64fsredirection)e [**Wow64RevertWow64FsRedirection.**](/windows/desktop/api/wow64apiset/nf-wow64apiset-wow64revertwow64fsredirection) La disabilitazione file system reindirizzamento dei file influisce su tutte le operazioni sui file eseguite dal thread chiamante, quindi deve essere disabilitata solo quando è necessaria per una singola chiamata [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) e ri abilitata nuovamente immediatamente dopo la fine della funzione. La disabilitazione file system reindirizzamento per periodi più lunghi può impedire alle applicazioni a 32 bit di caricare LE DLL di sistema, causando l'errore delle applicazioni.

Le applicazioni a 32 bit possono accedere alla directory di sistema nativa sostituendo %windir% \\ Sysnative con %windir% \\ System32. WOW64 riconosce Sysnative come alias speciale usato per indicare che il file system non deve reindirizzare l'accesso. Questo meccanismo è flessibile e facile da usare, pertanto è il meccanismo consigliato per ignorare file system reindirizzamento. Si noti che le applicazioni a 64 bit non possono usare l'alias Sysnative perché si tratta di una directory virtuale non reale.

**Windows Server 2003 e Windows XP:** L'alias Sysnative è stato aggiunto a partire da Windows Vista.

 

 