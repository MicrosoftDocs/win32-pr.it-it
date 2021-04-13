---
description: Un diritto di accesso è un flag di bit che corrisponde a un determinato set di operazioni che un thread può eseguire su un oggetto a protezione diretta.
ms.assetid: da67c486-d2e7-4632-ac7a-c18aabc3f21d
title: Maschere di accesso e diritti di accesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32f06cdf447f9d91c1553ea5fb6b3b7d1f324dc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104401727"
---
# <a name="access-rights-and-access-masks"></a>Maschere di accesso e diritti di accesso

Un *diritto di accesso* è un flag di bit che corrisponde a un determinato set di operazioni che un thread può eseguire su un oggetto a protezione diretta. Una chiave del registro di sistema, ad esempio, ha il diritto di accesso al valore di KEY \_ set \_ , che corrisponde alla capacità di un thread di impostare un valore sotto la chiave. Se un thread tenta di eseguire un'operazione su un oggetto, ma non dispone del diritto di accesso necessario all'oggetto, il sistema non esegue l'operazione.

Una [*maschera di accesso*](/windows/desktop/SecGloss/a-gly) è un valore a 32 bit i cui bit corrispondono ai diritti di accesso supportati da un oggetto. Tutti gli oggetti a protezione diretta di Windows usano un [formato di maschera di accesso](access-mask-format.md) che include BITS per i tipi di diritti di accesso seguenti:

-   [Diritti di accesso generici](generic-access-rights.md)
-   [Diritti di accesso standard](standard-access-rights.md)
-   [Accesso SACL a destra](sacl-access-right.md)
-   [Diritti di accesso ai servizi directory](directory-services-access-rights.md)

Quando un thread tenta di aprire un handle per un oggetto, il thread specifica in genere una maschera di accesso per [richiedere un set di diritti di accesso](requesting-access-rights-to-an-object.md). Ad esempio, un'applicazione che deve impostare ed eseguire una query sui valori di una chiave del registro di sistema può aprire la chiave utilizzando una maschera di accesso per richiedere il valore del set di chiavi \_ \_ e \_ i diritti di accesso ai valori della query della chiave \_ .

Nella tabella seguente vengono illustrate le funzioni che modificano le informazioni di sicurezza per ogni tipo di oggetto a protezione diretta.



| Tipo di oggetto                                                                                                                                           | Funzioni descrittore di sicurezza                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [File o directory](/windows/desktop/FileIO/file-security-and-access-rights) in un file system NTFS                                                                     | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Pipe anonime](/windows/desktop/ipc/anonymous-pipe-security-and-access-rights) [named pipe](/windows/desktop/ipc/named-pipe-security-and-access-rights)<br/>                 | [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [ **SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo)                                                                                                             |
| Buffer dello schermo della console                                                                                                                                | Non supportata.                                                                                                                                                                                     |
| [Elabora](/windows/desktop/ProcThread/process-security-and-access-rights)[thread](/windows/desktop/ProcThread/thread-security-and-access-rights)<br/>                                      | [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [ **SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo)                                                                                                             |
| [Oggetti di mapping di file](/windows/desktop/Memory/file-mapping-security-and-access-rights)                                                                                  | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Token di accesso](access-rights-for-access-token-objects.md)                                                                                           | [**SetKernelObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setkernelobjectsecurity), [ **GetKernelObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getkernelobjectsecurity)                                                                             |
| Oggetti di gestione della finestra (stazioni e [Desktop](/windows/desktop/winstation/desktop-security-and-access-rights)della[finestra](/windows/desktop/winstation/window-station-security-and-access-rights) ) | [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [ **SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo)                                                                                                             |
| [Chiavi del Registro di sistema](/windows/desktop/SysInfo/registry-key-security-and-access-rights)                                                                                         | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Servizi Windows](/windows/desktop/Services/service-security-and-access-rights)                                                                                           | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| Stampanti locali o remote                                                                                                                              | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| Condivisioni di rete                                                                                                                                        | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Oggetti di sincronizzazione interprocesso](/windows/desktop/Sync/synchronization-object-security-and-access-rights) (eventi, mutex, semafori e timer in attesa)     | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Oggetti processo](/windows/desktop/ProcThread/job-object-security-and-access-rights)                                                                                             | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |



 

 

