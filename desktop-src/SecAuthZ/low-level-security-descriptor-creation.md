---
description: Funzioni per la creazione di un descrittore di sicurezza e per ottenere e impostare i componenti di un descrittore di sicurezza.
ms.assetid: d07dab5a-7c06-40c4-aa59-fa0baaaa77e7
title: Creazione del descrittore di sicurezza di basso livello
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdafc99fe4d01c24e68a076aecc035843452205b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317040"
---
# <a name="low-level-security-descriptor-creation"></a>Creazione del descrittore di sicurezza di basso livello

Il controllo di accesso di basso livello fornisce un set di funzioni per la creazione di un [*descrittore di sicurezza*](/windows/desktop/SecGloss/s-gly) e per ottenere e impostare i componenti di un descrittore di sicurezza. Le funzioni di basso livello per l'inizializzazione e l'impostazione dei componenti di un descrittore di sicurezza funzionano solo con i descrittori di sicurezza in formato assoluto. Le funzioni di basso livello per ottenere i componenti di un descrittore di sicurezza funzionano con i [descrittori di sicurezza sia assoluti che autonomi](absolute-and-self-relative-security-descriptors.md).

La funzione [**InitializeSecurityDescriptor**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-initializesecuritydescriptor) Inizializza un buffer del [**\_ descrittore di sicurezza**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) . Il descrittore di sicurezza inizializzato è in formato [*assoluto*](/windows/desktop/SecGloss/a-gly) e non ha proprietario, gruppo primario, [*elenco di controllo di accesso discrezionale*](/windows/desktop/SecGloss/d-gly) (DACL) o [*elenco di controllo di accesso di sistema*](/windows/desktop/SecGloss/s-gly) (SACL). È possibile utilizzare le funzioni di basso livello seguenti per ottenere o impostare componenti specifici di un descrittore di sicurezza specificato.



| Funzione                                                             | Descrizione                                                                                                                                                               |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol) | Recupera le informazioni di revisione e controllo da un descrittore di sicurezza.                                                                                                    |
| [**GetSecurityDescriptorDacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptordacl)       | Recupera l'elenco DACL da un descrittore di sicurezza.                                                                                                                            |
| [**GetSecurityDescriptorGroup**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorgroup)     | Recupera l'ID di [*sicurezza*](/windows/desktop/SecGloss/s-gly) (SID) del gruppo primario da un descrittore di sicurezza. |
| [**GetSecurityDescriptorLength**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorlength)   | Restituisce la lunghezza di un descrittore di sicurezza.                                                                                                                              |
| [**GetSecurityDescriptorOwner**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorowner)     | Recupera il SID del proprietario da un descrittore di sicurezza.                                                                                                                       |
| [**GetSecurityDescriptorSacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorsacl)       | Recupera l'elenco SACL da un descrittore di sicurezza.                                                                                                                            |
| [**SetSecurityDescriptorDacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptordacl)       | Inserisce un DACL in un descrittore di sicurezza, sostituendo qualsiasi DACL esistente.                                                                                                    |
| [**SetSecurityDescriptorGroup**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorgroup)     | Imposta il SID del gruppo primario di un descrittore di sicurezza.                                                                                                                      |
| [**SetSecurityDescriptorOwner**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorowner)     | Imposta il SID del proprietario di un descrittore di sicurezza.                                                                                                                              |
| [**SetSecurityDescriptorSacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorsacl)       | Inserisce un SACL in un descrittore di sicurezza, sostituendo qualsiasi SACL esistente.                                                                                                    |



 

Per controllare il livello di revisione e l' [*integrità*](/windows/desktop/SecGloss/i-gly) strutturale di un descrittore di sicurezza, chiamare la funzione [**IsValidSecurityDescriptor**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-isvalidsecuritydescriptor) .

 

 
