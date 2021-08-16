---
description: Un oggetto a protezione diretta è un oggetto che può avere un descrittore di sicurezza.
ms.assetid: 32f2ec06-822f-4d1e-bf51-5ae1d7355e60
title: Oggetti a protezione diretta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93af0153082a5e94577e96e3b3f85c30ced8775aa8617bff84db37c96904d814
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117780506"
---
# <a name="securable-objects"></a>Oggetti a protezione diretta

Un oggetto a protezione diretta è un oggetto che può avere un [descrittore di sicurezza](security-descriptors.md). Tutti gli oggetti Windows sono entità a protezione diretta. Alcuni oggetti senza nome, ad esempio gli [*oggetti processo*](/windows/desktop/SecGloss/p-gly) e thread, possono avere anche descrittori di sicurezza. Per la maggior parte degli oggetti a [](/windows/desktop/SecGloss/s-gly) protezione diretta, è possibile specificare il descrittore di sicurezza di un oggetto nella chiamata di funzione che crea l'oggetto. Ad esempio, è possibile specificare un descrittore di sicurezza nelle [**funzioni CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) [**e CreateProcess.**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa)

Le funzioni di sicurezza Windows consentono inoltre di ottenere e impostare le informazioni di sicurezza per gli oggetti a protezione diretta creati in sistemi operativi diversi da Windows. Le Windows di sicurezza forniscono anche il supporto per l'uso di descrittori di sicurezza con oggetti privati definiti dall'applicazione. Per altre informazioni sugli oggetti a protezione diretta privati, vedere [Controllo di accesso client/server.](client-server-access-control.md)

Ogni tipo di oggetto a protezione diretta definisce il proprio set di diritti di accesso [specifici](access-rights-and-access-masks.md) e il [proprio mapping dei diritti di accesso generici](generic-access-rights.md). Per informazioni sui diritti di accesso specifici e generici per ogni tipo di oggetto a protezione diretta, vedere la panoramica per tale tipo di oggetto.

Nella tabella seguente vengono illustrate le funzioni da utilizzare per modificare le informazioni di sicurezza per alcuni oggetti a protezione diretta comuni.



| Tipo di oggetto                                                                                                                                           | Funzioni del descrittore di sicurezza                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [File o directory in](/windows/desktop/FileIO/file-security-and-access-rights) un file system NTFS                                                                     | [**GetNamedSecurityInfo,**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) [**SetNamedSecurityInfo,**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) [**GetSecurityInfo,**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Named pipe](/windows/desktop/ipc/named-pipe-security-and-access-rights)<br/> [Pipe anonime](/windows/desktop/ipc/anonymous-pipe-security-and-access-rights)<br/>     | [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [ **SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo)                                                                                                             |
| [Processi](/windows/desktop/ProcThread/process-security-and-access-rights)<br/> [Thread](/windows/desktop/ProcThread/thread-security-and-access-rights)<br/>                          | [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [ **SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo)                                                                                                             |
| [Oggetti di mapping di file](/windows/desktop/Memory/file-mapping-security-and-access-rights)                                                                                  | [**GetNamedSecurityInfo,**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) [**SetNamedSecurityInfo,**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) [**GetSecurityInfo,**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Token di accesso](access-rights-for-access-token-objects.md)                                                                                           | [**SetKernelObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setkernelobjectsecurity), [ **GetKernelObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getkernelobjectsecurity)                                                                             |
| Oggetti di gestione delle finestre[(finestre stazioni](/windows/desktop/winstation/window-station-security-and-access-rights) [e desktop)](/windows/desktop/winstation/desktop-security-and-access-rights) | [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [ **SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo)                                                                                                             |
| [Chiavi del Registro di sistema](/windows/desktop/SysInfo/registry-key-security-and-access-rights)                                                                                         | [**GetNamedSecurityInfo,**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) [**SetNamedSecurityInfo,**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) [**GetSecurityInfo,**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Windows servizi](/windows/desktop/Services/service-security-and-access-rights)                                                                                           | [**GetNamedSecurityInfo,**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) [**SetNamedSecurityInfo,**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) [**GetSecurityInfo,**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| Stampanti locali o remote                                                                                                                              | [**GetNamedSecurityInfo,**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) [**SetNamedSecurityInfo,**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) [**GetSecurityInfo,**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| Condivisioni di rete                                                                                                                                        | [**GetNamedSecurityInfo,**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) [**SetNamedSecurityInfo,**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) [**GetSecurityInfo,**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Oggetti di sincronizzazione interprocesso](/windows/desktop/Sync/synchronization-object-security-and-access-rights) (eventi, mutex, semafori e timer attese)     | [**GetNamedSecurityInfo,**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) [**SetNamedSecurityInfo,**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) [**GetSecurityInfo,**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Oggetti processo](/windows/desktop/ProcThread/job-object-security-and-access-rights)                                                                                             | [**GetNamedSecurityInfo,**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) [**SetNamedSecurityInfo,**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) [**GetSecurityInfo,**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| Oggetti del servizio directory                                                                                                                             | Questi oggetti vengono gestiti dagli oggetti di Active Directory. Per altre informazioni, vedere [Interfacce del servizio Active Directory.](/windows/desktop/ADSI/active-directory-service-interfaces-adsi)                             |



 

 

