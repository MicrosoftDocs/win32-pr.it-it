---
description: Un IDENTIFICATORE di sicurezza (SID) è un valore univoco di lunghezza variabile usato per identificare un fiduciare.
ms.assetid: 7cb07bcd-70f4-43dd-8382-320fcff151c7
title: Identificatori di sicurezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf6acaaeacfbc77b2dc814062c4254c5f08e58869e0b6d8b2fbb64e8511dc31e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119413491"
---
# <a name="security-identifiers"></a>Identificatori di sicurezza

Un SID (Security [*Identifier)*](/windows/desktop/SecGloss/s-gly) è un valore univoco di lunghezza variabile utilizzato per identificare un [fiduciare.](trustees.md) Ogni account ha un SID univoco emesso da un'autorità, ad esempio un controller di dominio Windows e archiviato in un database di sicurezza. Ogni volta che un utente accede, il sistema recupera il SID per tale utente dal database e lo inserisce nel [*token*](/windows/desktop/SecGloss/a-gly) di accesso per tale utente. Il sistema usa il SID nel token di accesso per identificare l'utente in tutte le interazioni successive con Windows sicurezza. Quando un SID è stato usato come identificatore univoco per un utente o un gruppo, non può mai essere usato di nuovo per identificare un altro utente o gruppo.

Windows sicurezza usa SID negli elementi di sicurezza seguenti:

-   Nei [descrittori di sicurezza per](security-descriptors.md) identificare il proprietario di un oggetto e di un gruppo primario
-   Nelle [voci di controllo di accesso](access-control-entries.md), per identificare il trustee per il quale l'accesso è consentito, negato o controllati
-   Nei [token di accesso](access-tokens.md), per identificare l'utente e i gruppi a cui appartiene l'utente

Oltre ai SID specifici del dominio creati in modo univoco assegnati a utenti e gruppi specifici, sono presenti [SID](well-known-sids.md) noti che identificano gruppi generici e utenti generici. Ad esempio, i SID noti, Everyone e World, identificano un gruppo che include tutti gli utenti.

La maggior parte delle applicazioni non deve mai usare i SID. Poiché i nomi dei [SID](well-known-sids.md) noti possono variare, è consigliabile usare le funzioni per compilare il SID dalle costanti predefinite anziché usare il nome del SID noto. Ad esempio, la versione inglese degli Stati Uniti del sistema operativo Windows ha un SID noto denominato "BUILTIN Administrators" che potrebbe avere un nome diverso nelle versioni internazionali \\ del sistema. Per un esempio che compila un SID noto, vedere Ricerca di un SID in un token di [accesso in C++.](searching-for-a-sid-in-an-access-token-in-c--.md)

Se è necessario usare i SID, non modificarli direttamente. Usare invece le funzioni seguenti.



| Funzione                                                       | Descrizione                                                                                                                                               |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AllocateAndInitializeSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid)   | Alloca e inizializza un SID con il numero specificato di sottoautorità.                                                                              |
| [**ConvertSidToStringSid**](/windows/desktop/api/Sddl/nf-sddl-convertsidtostringsida)         | Converte un SID in un formato stringa adatto per la visualizzazione, l'archiviazione o il trasporto.                                                                            |
| [**ConvertStringSidToSid**](/windows/desktop/api/Sddl/nf-sddl-convertstringsidtosida)         | Converte un SID in formato stringa in un SID funzionale valido.                                                                                                  |
| [**CopySid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-copysid)                                     | Copia un SID di origine in un buffer.                                                                                                                          |
| [**EqualPrefixSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-equalprefixsid)                       | Verifica l'uguaglianza di due valori di prefisso SID. Un prefisso SID è l'intero SID ad eccezione dell'ultimo valore di sottoautorità.                                          |
| [**EqualSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-equalsid)                                   | Verifica l'uguaglianza di due SID. Devono corrispondere esattamente per essere considerate uguali.                                                                              |
| [**FreeSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-freesid)                                     | Libera un SID allocato in precedenza usando la [**funzione AllocateAndInitializeSid.**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid)                                      |
| [**GetLengthSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getlengthsid)                           | Recupera la lunghezza di un SID.                                                                                                                            |
| [**GetSidIdentifierAuthority**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsididentifierauthority) | Recupera un puntatore all'autorità dell'identificatore per un SID.                                                                                                |
| [**GetSidLengthRequired**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsidlengthrequired)           | Recupera le dimensioni del buffer necessarie per archiviare un SID con un numero specificato di sottoautentiche.                                                       |
| [**GetSidSubAuthority**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsidsubauthority)               | Recupera un puntatore a una sottoautorità specificata in un SID.                                                                                                 |
| [**GetSidSubAuthorityCount**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsidsubauthoritycount)     | Recupera il numero di sottoautentiche in un SID.                                                                                                          |
| [**InitializeSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-initializesid)                         | Inizializza una [**struttura SID.**](/windows/desktop/api/Winnt/ns-winnt-sid)                                                                                                               |
| [**IsValidSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-isvalidsid)                               | Verifica la validità di un SID verificando che il numero di revisione sia compreso in un intervallo noto e che il numero di sottoautentiche sia inferiore al massimo. |
| [**Lookupaccountname**](/windows/desktop/api/Winbase/nf-winbase-lookupaccountnamea)                 | Recupera il SID che corrisponde a un nome di account specificato.                                                                                           |
| [**Lookupaccountsid**](/windows/desktop/api/Winbase/nf-winbase-lookupaccountsida)                   | Recupera il nome dell'account che corrisponde a un SID specificato.                                                                                           |



 

 

 
