---
description: Un diritto di accesso è un flag di bit che corrisponde a un particolare set di operazioni che un thread può eseguire su un oggetto a protezione diretta.
ms.assetid: da67c486-d2e7-4632-ac7a-c18aabc3f21d
title: Diritti di accesso e maschere di accesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1238766e2e4c8629b6c3a508b30d1e8832314d2e8ddd5ffdf4a1b93085f3c64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118914358"
---
# <a name="access-rights-and-access-masks"></a>Diritti di accesso e maschere di accesso

Un *diritto di accesso* è un flag di bit che corrisponde a un particolare set di operazioni che un thread può eseguire su un oggetto a protezione diretta. Ad esempio, una chiave del Registro di sistema ha il diritto di accesso KEY SET VALUE, che corrisponde alla possibilità di un thread di \_ impostare un valore sotto la \_ chiave. Se un thread tenta di eseguire un'operazione su un oggetto, ma non dispone del diritto di accesso necessario all'oggetto, il sistema non esegue l'operazione.

Una [*maschera di accesso*](/windows/desktop/SecGloss/a-gly) è un valore a 32 bit i cui bit corrispondono ai diritti di accesso supportati da un oggetto . Tutti Windows a protezione diretta usano un [formato maschera](access-mask-format.md) di accesso che include bit per i tipi di diritti di accesso seguenti:

-   [Diritti di accesso generici](generic-access-rights.md)
-   [Diritti di accesso standard](standard-access-rights.md)
-   [Diritto di accesso SACL](sacl-access-right.md)
-   [Diritti di accesso ai servizi directory](directory-services-access-rights.md)

Quando un thread tenta di aprire un handle per un oggetto , il thread specifica in genere una maschera di accesso per [richiedere un set di diritti di accesso](requesting-access-rights-to-an-object.md). Ad esempio, un'applicazione che deve impostare ed eseguire query sui valori di una chiave del Registro di sistema può aprire la chiave usando una maschera di accesso per richiedere i diritti di accesso KEY SET VALUE e \_ \_ KEY QUERY \_ \_ VALUE.

La tabella seguente illustra le funzioni che modificano le informazioni di sicurezza per ogni tipo di oggetto a protezione diretta.



| Tipo di oggetto                                                                                                                                           | Funzioni del descrittore di sicurezza                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [File o directory](/windows/desktop/FileIO/file-security-and-access-rights) in un file system NTFS                                                                     | [**GetNamedSecurityInfo,**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) [**SetNamedSecurityInfo,**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) [**GetSecurityInfo,**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Named pipe Pipe](/windows/desktop/ipc/named-pipe-security-and-access-rights)[anonime](/windows/desktop/ipc/anonymous-pipe-security-and-access-rights)<br/>                 | [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [ **SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo)                                                                                                             |
| Buffer dello schermo della console                                                                                                                                | Non supportata.                                                                                                                                                                                     |
| [Thread dei](/windows/desktop/ProcThread/process-security-and-access-rights)[processi](/windows/desktop/ProcThread/thread-security-and-access-rights)<br/>                                      | [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [ **SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo)                                                                                                             |
| [Oggetti di mapping dei file](/windows/desktop/Memory/file-mapping-security-and-access-rights)                                                                                  | [**GetNamedSecurityInfo,**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) [**SetNamedSecurityInfo,**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) [**GetSecurityInfo,**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Token di accesso](access-rights-for-access-token-objects.md)                                                                                           | [**SetKernelObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setkernelobjectsecurity), [ **GetKernelObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getkernelobjectsecurity)                                                                             |
| Oggetti di gestione delle finestre ([stazioni di finestra](/windows/desktop/winstation/window-station-security-and-access-rights) [e desktop](/windows/desktop/winstation/desktop-security-and-access-rights)) | [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [ **SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo)                                                                                                             |
| [Chiavi del Registro di sistema](/windows/desktop/SysInfo/registry-key-security-and-access-rights)                                                                                         | [**GetNamedSecurityInfo,**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) [**SetNamedSecurityInfo,**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) [**GetSecurityInfo,**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Windows servizi](/windows/desktop/Services/service-security-and-access-rights)                                                                                           | [**GetNamedSecurityInfo,**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) [**SetNamedSecurityInfo,**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) [**GetSecurityInfo,**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| Stampanti locali o remote                                                                                                                              | [**GetNamedSecurityInfo,**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) [**SetNamedSecurityInfo,**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) [**GetSecurityInfo,**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| Condivisioni di rete                                                                                                                                        | [**GetNamedSecurityInfo,**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) [**SetNamedSecurityInfo,**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) [**GetSecurityInfo,**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Oggetti di sincronizzazione interprocesso](/windows/desktop/Sync/synchronization-object-security-and-access-rights) (eventi, mutex, semafori e timer waitable)     | [**GetNamedSecurityInfo,**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) [**SetNamedSecurityInfo,**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) [**GetSecurityInfo,**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Oggetti processo](/windows/desktop/ProcThread/job-object-security-and-access-rights)                                                                                             | [**GetNamedSecurityInfo,**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) [**SetNamedSecurityInfo,**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) [**GetSecurityInfo,**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |



 

 

