---
title: Redirector del file System
description: La \\ directory di windir system32 è riservata alle applicazioni a 64 bit in Windows a 64 bit.
ms.assetid: b4d36fe8-8bbb-469b-8ad1-650d559a4c75
keywords:
- Programmazione Windows a 64 bit per redirector file system
- Guida per programmatori Windows a 64 bit-programmazione Windows a 64 bit, redirector file system
- Programmazione Windows WOW64 a 64 bit, redirector file system
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 561d03c8da51bd37a2d97746296bc74e24e43154
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047074"
---
# <a name="file-system-redirector"></a>Redirector del file System

La directory% windir% \\ system32 è riservata alle applicazioni a 64 bit in Windows a 64 bit. La maggior parte dei nomi di file DLL non è stata modificata quando sono state create versioni a 64 bit delle dll, quindi le versioni a 32 bit delle dll vengono archiviate in una directory diversa. WOW64 nasconde questa differenza usando un *redirector file System*.

Nella maggior parte dei casi, ogni volta che un'applicazione a 32 bit tenta di accedere a% windir% \\ system32,% windir% \\ LastGood \\ System32 o% windir% \\regedit.exe, l'accesso viene reindirizzato a un percorso specifico dell'architettura.

> [!Note]  
> Questi percorsi vengono forniti solo per riferimento. Per compatibilità, le applicazioni non devono utilizzare direttamente questi percorsi. Devono invece chiamare le API descritte di seguito.

 



|                              |                                          |                                          |
|------------------------------|------------------------------------------|------------------------------------------|
| Percorso originale                | Percorso reindirizzato per i processi x86 a 32 bit | Percorso reindirizzato per processi ARM a 32 bit |
| % WINDIR% \\ system32           | % WINDIR% \\ SysWow64                       | % WINDIR% \\ SysArm32                       |
| % WINDIR% \\ LastGood \\ system32 | % WINDIR% \\ LastGood \\ SysWow64             | % WINDIR% \\ LastGood \\ SysArm32             |
| % WINDIR% \\regedit.exe        | % WINDIR% \\ SysWOW64 \\regedit.exe          | % WINDIR% \\ SysArm32 \\regedit.exe         |



 

Se l'accesso fa in modo che il sistema visualizzi la richiesta di controllo dell'account utente, il reindirizzamento non viene eseguito. Viene invece avviata la versione a 64 bit del file richiesto. Per evitare questo problema, specificare la directory SysWOW64 per evitare il reindirizzamento e garantire l'accesso alla versione a 32 bit del file oppure eseguire l'applicazione a 32 bit con privilegi di amministratore, in modo che la richiesta di controllo dell'account utente non venga visualizzata.

**Windows Server 2003 e Windows XP:  ** Il controllo dell'account utente non è supportato.

Alcune sottodirectory sono esentate dal reindirizzamento. L'accesso a queste sottodirectory non viene reindirizzato a% windir% \\ SysWow64: <dl> % WINDIR% \\ system32 \\ Catroot  
% WINDIR% \\ system32 \\ Catroot2  
% WINDIR% \\ system32 \\ DriverStore  
% WINDIR% \\ system32 \\ drivers e \\ così via  
% WINDIR% \\ system32 \\ LogFiles  
% WINDIR% \\ system32 \\ spool  
</dl>

**Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:  **% windir% \\ system32 \\ DriverStore è stato reindirizzato.

Per recuperare il nome della directory di sistema a 32 bit, le applicazioni a 64 bit devono usare la funzione [**GetSystemWow64Directory2**](/windows/desktop/api/wow64apiset/nf-wow64apiset-getsystemwow64directory2a) (Windows 10, versione 1511) o la funzione [**GetSystemWow64Directory**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) .

Le applicazioni devono utilizzare la funzione [**SHGetKnownFolderPath**](https://www.bing.com/search?q=**SHGetKnownFolderPath**) per determinare il nome di directory% ProgramFiles%.

**Windows Server 2003 e Windows XP:** Le applicazioni devono utilizzare la funzione [**SHGetSpecialFolderPath**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetspecialfolderpatha) per determinare il nome di directory% ProgramFiles%.

Le applicazioni possono controllare il redirector file system WOW64 usando le funzioni [**Wow64DisableWow64FsRedirection**](/windows/desktop/api/wow64apiset/nf-wow64apiset-wow64disablewow64fsredirection), [**Wow64EnableWow64FsRedirection**](/windows/desktop/api/winbase/nf-winbase-wow64enablewow64fsredirection)e [**Wow64RevertWow64FsRedirection**](/windows/desktop/api/wow64apiset/nf-wow64apiset-wow64revertwow64fsredirection) . La disabilitazione del reindirizzamento file system influiscono su tutte le operazioni sui file eseguite dal thread chiamante, quindi deve essere disabilitata solo quando è necessario per una singola chiamata a [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) e nuovamente riabilitata immediatamente dopo la restituzione della funzione. La disabilitazione del reindirizzamento file system per periodi più lunghi può impedire il caricamento di dll di sistema da parte delle applicazioni a 32 bit, causando l'esito negativo delle applicazioni.

le applicazioni a 32 bit possono accedere alla directory di sistema nativa sostituendo% windir% \\ SysNative per% windir% \\ system32. WOW64 riconosce SysNative come un alias speciale usato per indicare che l'file system non deve reindirizzare l'accesso. Questo meccanismo è flessibile e facile da usare, pertanto è il meccanismo consigliato per ignorare il reindirizzamento file system. Si noti che le applicazioni a 64 bit non possono usare l'alias SysNative perché si tratta di una directory virtuale non reale.

**Windows Server 2003 e Windows XP:** L'alias SysNative è stato aggiunto a partire da Windows Vista.

 

 