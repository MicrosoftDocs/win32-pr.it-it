---
description: Usare le funzioni GetSecurityInfo e GetNamedSecurityInfo per recuperare un puntatore a un descrittore di sicurezza degli oggetti.
ms.assetid: 834f1b58-d403-4899-865e-5721a37587e9
title: Operazioni del descrittore di sicurezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5574a504468a4f4bb7dc14effe1f4717d695846
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129906"
---
# <a name="security-descriptor-operations"></a>Operazioni del descrittore di sicurezza

L'API Windows fornisce funzioni per ottenere e impostare i componenti del [*descrittore di sicurezza*](/windows/desktop/SecGloss/s-gly) associato a un oggetto a protezione diretta. Usare le funzioni [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) e [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) per recuperare un puntatore al descrittore di sicurezza di un oggetto. Queste funzioni possono anche recuperare i puntatori ai singoli componenti del descrittore di sicurezza: DACL, SACL, SID del proprietario e SID del gruppo primario. Usare le funzioni [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) e [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) per impostare i componenti del descrittore di sicurezza di un oggetto.

In generale, è consigliabile usare [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) e [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) con gli oggetti identificati da un handle e [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) e [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) con oggetti identificati da un nome. Per ulteriori informazioni sulle funzioni specifiche da utilizzare quando si utilizzano i vari tipi di oggetti, vedere [oggetti a protezione diretta](securable-objects.md).

L'API Windows fornisce funzioni aggiuntive per la modifica dei componenti di un descrittore di sicurezza. Per informazioni sull'utilizzo degli elenchi di controllo di accesso (DACL o SACL), vedere [recupero di informazioni da un ACL](getting-information-from-an-acl.md) e [creazione o modifica di un ACL](creating-or-modifying-an-acl.md). Per informazioni sui SID, vedere [ID di sicurezza](security-identifiers.md) (SID).

Per ottenere le informazioni di controllo in un descrittore di sicurezza, chiamare la funzione [**GetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol) . Per impostare i bit di controllo correlati all'ereditarietà automatica della voce ACE, chiamare la funzione [**SetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorcontrol) . Altri bit di controllo vengono impostati dalle varie funzioni che impostano un componente del descrittore di sicurezza. Se, ad esempio, si utilizza [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) per modificare l'elenco DACL di un oggetto, la funzione imposta o cancella i bit in modo appropriato per indicare se il descrittore di sicurezza dispone di un DACL, se è un DACL predefinito e così via. Un altro esempio è il bit di controllo di [*Resource Manager*](/windows/desktop/SecGloss/r-gly) (RM) contenuto nel descrittore di sicurezza. Questi bit vengono usati in base all'implementazione di Resource Manager ed è possibile accedervi tramite le funzioni [**GetSecurityDescriptorRMControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorrmcontrol) e [**SetSecurityDescriptorRMControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorrmcontrol) .

 

 
