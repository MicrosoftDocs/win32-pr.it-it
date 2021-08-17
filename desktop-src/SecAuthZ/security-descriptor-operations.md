---
description: Usare le funzioni GetSecurityInfo e GetNamedSecurityInfo per recuperare un puntatore a un descrittore di sicurezza degli oggetti.
ms.assetid: 834f1b58-d403-4899-865e-5721a37587e9
title: Operazioni sui descrittori di sicurezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53b9c7a7d1dab22f27bad785c6e1394403588a1719b2cc29932aba909aec89ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117780133"
---
# <a name="security-descriptor-operations"></a>Operazioni sui descrittori di sicurezza

L Windows API fornisce funzioni per ottenere e impostare i componenti del descrittore di [*sicurezza*](/windows/desktop/SecGloss/s-gly) associato a un oggetto a protezione diretta. Usare le [**funzioni GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) e [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) per recuperare un puntatore al descrittore di sicurezza di un oggetto. Queste funzioni possono anche recuperare puntatori ai singoli componenti del descrittore di sicurezza: DACL, SACL, SID proprietario e SID gruppo primario. Usare le [**funzioni SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) [**e SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) per impostare i componenti del descrittore di sicurezza di un oggetto.

In generale, è consigliabile usare [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) e [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) con oggetti identificati da un handle e [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) e [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) con oggetti identificati da un nome. Per altre informazioni sulle funzioni specifiche da usare quando si usano i vari tipi di oggetti, vedere [Oggetti a protezione diretta.](securable-objects.md)

L Windows API fornisce funzioni aggiuntive per la modifica dei componenti di un descrittore di sicurezza. Per informazioni sull'uso degli elenchi di controllo di accesso (DACL o ACL), vedere Recupero di informazioni da un [ACL](getting-information-from-an-acl.md) e Creazione o [modifica di un ACL.](creating-or-modifying-an-acl.md) Per informazioni sui SID, vedere [Id di sicurezza](security-identifiers.md) (SID).

Per ottenere le informazioni sul controllo in un descrittore di sicurezza, chiamare la [**funzione GetSecurityDescriptorControl.**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol) Per impostare i bit di controllo correlati all'ereditarietà ACE automatica, chiamare la [**funzione SetSecurityDescriptorControl.**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorcontrol) Altri bit di controllo vengono impostati dalle varie funzioni che impostano un componente descrittore di sicurezza. Ad esempio, se si usa [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) per modificare l'elenco DACL di un oggetto, la funzione imposta o cancella i bit in base alle esigenze per indicare se il descrittore di sicurezza dispone di un DACL, se si tratta di un DACL predefinito e così via. Un altro esempio sono [*i bit*](/windows/desktop/SecGloss/r-gly) di controllo di Resource Manager (RM) contenuti nel descrittore di sicurezza. Questi bit vengono usati in base all'implementazione di Gestione risorse e sono accessibili tramite le funzioni [**GetSecurityDescriptorRMControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorrmcontrol) [**e SetSecurityDescriptorRMControl.**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorrmcontrol)

 

 
