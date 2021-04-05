---
description: Un oggetto a protezione diretta è un oggetto che può disporre di un descrittore di sicurezza.
ms.assetid: 32f2ec06-822f-4d1e-bf51-5ae1d7355e60
title: Oggetti a protezione diretta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 867a40e781d9d7f97302ed6e592a7fc26d61b939
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752751"
---
# <a name="securable-objects"></a>Oggetti a protezione diretta

Un oggetto a protezione diretta è un oggetto che può disporre di un [descrittore di sicurezza](security-descriptors.md). Tutti gli oggetti Windows denominati sono entità a protezione diretta. Alcuni oggetti senza nome, ad esempio gli oggetti [*processo*](/windows/desktop/SecGloss/p-gly) e thread, possono avere anche descrittori di sicurezza. Per la maggior parte degli oggetti a protezione diretta, è possibile specificare un [*descrittore di sicurezza*](/windows/desktop/SecGloss/s-gly) di un oggetto nella chiamata di funzione che crea l'oggetto. È ad esempio possibile specificare un descrittore di sicurezza nelle funzioni [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) e [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) .

Inoltre, le funzioni di sicurezza di Windows consentono di ottenere e impostare le informazioni di sicurezza per gli oggetti a protezione diretta creati in sistemi operativi diversi da Windows. Le funzioni di sicurezza di Windows forniscono inoltre supporto per l'utilizzo di descrittori di sicurezza con oggetti privati definiti dall'applicazione. Per ulteriori informazioni sugli oggetti a protezione diretta privati, vedere [controllo di accesso client/server](client-server-access-control.md).

Ogni tipo di oggetto a protezione diretta definisce il proprio set di [diritti di accesso](access-rights-and-access-masks.md) specifici e il proprio [mapping di diritti di accesso generici](generic-access-rights.md). Per informazioni sui diritti di accesso specifici e generici per ogni tipo di oggetto a protezione diretta, vedere la Panoramica di tale tipo di oggetto.

Nella tabella seguente vengono illustrate le funzioni da utilizzare per modificare le informazioni di sicurezza per alcuni oggetti a protezione diretta comuni.



| Tipo di oggetto                                                                                                                                           | Funzioni descrittore di sicurezza                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [File o directory](/windows/desktop/FileIO/file-security-and-access-rights) in un file system NTFS                                                                     | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Named pipe](/windows/desktop/ipc/named-pipe-security-and-access-rights)<br/> [Pipe anonime](/windows/desktop/ipc/anonymous-pipe-security-and-access-rights)<br/>     | [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [ **SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo)                                                                                                             |
| [Processi](/windows/desktop/ProcThread/process-security-and-access-rights)<br/> [Thread](/windows/desktop/ProcThread/thread-security-and-access-rights)<br/>                          | [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [ **SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo)                                                                                                             |
| [Oggetti di mapping di file](/windows/desktop/Memory/file-mapping-security-and-access-rights)                                                                                  | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Token di accesso](access-rights-for-access-token-objects.md)                                                                                           | [**SetKernelObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setkernelobjectsecurity), [ **GetKernelObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getkernelobjectsecurity)                                                                             |
| Oggetti di gestione della finestra (stazioni e [Desktop](/windows/desktop/winstation/desktop-security-and-access-rights)della[finestra](/windows/desktop/winstation/window-station-security-and-access-rights) ) | [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [ **SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo)                                                                                                             |
| [Chiavi del Registro di sistema](/windows/desktop/SysInfo/registry-key-security-and-access-rights)                                                                                         | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Servizi Windows](/windows/desktop/Services/service-security-and-access-rights)                                                                                           | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| Stampanti locali o remote                                                                                                                              | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| Condivisioni di rete                                                                                                                                        | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Oggetti di sincronizzazione interprocesso](/windows/desktop/Sync/synchronization-object-security-and-access-rights) (eventi, mutex, semafori e timer in attesa)     | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Oggetti processo](/windows/desktop/ProcThread/job-object-security-and-access-rights)                                                                                             | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| Oggetti servizio directory                                                                                                                             | Questi oggetti vengono gestiti da oggetti Active Directory. Per ulteriori informazioni, vedere [Active Directory interfacce del servizio](/windows/desktop/ADSI/active-directory-service-interfaces-adsi).                             |



 

 

