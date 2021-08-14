---
description: Funzioni per la creazione di un descrittore di sicurezza e il recupero e l'impostazione dei componenti di un descrittore di sicurezza.
ms.assetid: d07dab5a-7c06-40c4-aa59-fa0baaaa77e7
title: Creazione di descrittori di sicurezza di basso livello
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a6462dcd7672836df5f2c1f6b368723bc3a9488eff290dc22a071ce40279def
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117781484"
---
# <a name="low-level-security-descriptor-creation"></a>Creazione di descrittori di sicurezza di basso livello

Il controllo di accesso di basso livello fornisce un set di funzioni per la creazione di un descrittore di [*sicurezza*](/windows/desktop/SecGloss/s-gly) e per il recupero e l'impostazione dei componenti di un descrittore di sicurezza. Le funzioni di basso livello per l'inizializzazione e l'impostazione dei componenti di un descrittore di sicurezza funzionano solo con i descrittori di sicurezza in formato assoluto. Le funzioni di basso livello per ottenere i componenti di un descrittore di sicurezza funzionano sia con i descrittori di sicurezza assoluti che con i [descrittori di sicurezza auto-relativi.](absolute-and-self-relative-security-descriptors.md)

La [**funzione InitializeSecurityDescriptor**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-initializesecuritydescriptor) inizializza un buffer [**SECURITY \_ DESCRIPTOR.**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) Il descrittore di sicurezza inizializzato è [*in*](/windows/desktop/SecGloss/a-gly) formato assoluto e non dispone di proprietario, gruppo [*primario,*](/windows/desktop/SecGloss/d-gly) elenco di controllo di accesso discrezionale (DACL) o elenco di controllo di accesso [*di*](/windows/desktop/SecGloss/s-gly) sistema (SACL). È possibile usare le funzioni di basso livello seguenti per ottenere o impostare componenti specifici di un descrittore di sicurezza specificato.



| Funzione                                                             | Descrizione                                                                                                                                                               |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol) | Recupera le informazioni di revisione e controllo da un descrittore di sicurezza.                                                                                                    |
| [**GetSecurityDescriptorDacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptordacl)       | Recupera l'elenco DACL da un descrittore di sicurezza.                                                                                                                            |
| [**GetSecurityDescriptorGroup**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorgroup)     | Recupera l'ID di [*sicurezza*](/windows/desktop/SecGloss/s-gly) (SID) del gruppo primario da un descrittore di sicurezza. |
| [**GetSecurityDescriptorLength**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorlength)   | Restituisce la lunghezza di un descrittore di sicurezza.                                                                                                                              |
| [**GetSecurityDescriptorOwner**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorowner)     | Recupera il SID del proprietario da un descrittore di sicurezza.                                                                                                                       |
| [**GetSecurityDescriptorSacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorsacl)       | Recupera l'elenco sacl da un descrittore di sicurezza.                                                                                                                            |
| [**SetSecurityDescriptorDacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptordacl)       | Inserisce un elenco DACL in un descrittore di sicurezza, sostituisce qualsiasi dacl esistente.                                                                                                    |
| [**SetSecurityDescriptorGroup**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorgroup)     | Imposta il SID del gruppo primario di un descrittore di sicurezza.                                                                                                                      |
| [**SetSecurityDescriptorOwner**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorowner)     | Imposta il SID proprietario di un descrittore di sicurezza.                                                                                                                              |
| [**SetSecurityDescriptorSacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorsacl)       | Inserisce un SACL in un descrittore di sicurezza, sostituisce qualsiasi SACL esistente.                                                                                                    |



 

Per controllare il livello di revisione e [*l'integrità*](/windows/desktop/SecGloss/i-gly) strutturale di un descrittore di sicurezza, chiamare la [**funzione IsValidSecurityDescriptor.**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-isvalidsecuritydescriptor)

 

 
