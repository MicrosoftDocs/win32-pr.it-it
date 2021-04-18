---
description: Un ID di sicurezza (SID) è un valore univoco di lunghezza variabile usato per identificare un trustee.
ms.assetid: 7cb07bcd-70f4-43dd-8382-320fcff151c7
title: ID di sicurezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0368b2484cd8766aa7fa74c24679e82b10854e9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308132"
---
# <a name="security-identifiers"></a>ID di sicurezza

Un [*ID di sicurezza*](/windows/desktop/SecGloss/s-gly) (SID) è un valore univoco di lunghezza variabile usato per identificare un [trustee](trustees.md). Ogni account dispone di un SID univoco emesso da un'autorità, ad esempio un controller di dominio Windows, e archiviato in un database di sicurezza. Ogni volta che un utente esegue l'accesso, il sistema Recupera il SID per tale utente dal database e lo inserisce nel [*token di accesso*](/windows/desktop/SecGloss/a-gly) per tale utente. Il sistema usa il SID nel token di accesso per identificare l'utente in tutte le interazioni successive con la sicurezza di Windows. Quando un SID è stato usato come identificatore univoco per un utente o un gruppo, non può mai essere usato di nuovo per identificare un altro utente o gruppo.

La sicurezza di Windows usa i SID negli elementi di sicurezza seguenti:

-   Nei [descrittori di sicurezza](security-descriptors.md) per identificare il proprietario di un oggetto e di un gruppo primario
-   In [voci di controllo di accesso](access-control-entries.md), per identificare il trustee per il quale l'accesso è consentito, negato o controllato
-   In [token di accesso](access-tokens.md), per identificare l'utente e i gruppi a cui appartiene l'utente

Oltre ai SID specifici del dominio creati in modo univoco assegnati a utenti e gruppi specifici, sono disponibili [SID noti](well-known-sids.md) che identificano i gruppi e gli utenti generici. Ad esempio, i SID noti, Everyone e World, identificano un gruppo che include tutti gli utenti.

La maggior parte delle applicazioni non deve mai usare i SID. Poiché i nomi dei [SID noti](well-known-sids.md) possono variare, è necessario utilizzare le funzioni per compilare il SID dalle costanti predefinite anziché utilizzare il nome del SID noto. La versione inglese (Stati Uniti) del sistema operativo Windows, ad esempio, dispone di un SID noto denominato "BUILTin \\ Administrators", che potrebbe avere un nome diverso nelle versioni internazionali del sistema. Per un esempio in cui viene compilato un SID noto, vedere [ricerca di un SID in un token di accesso in C++](searching-for-a-sid-in-an-access-token-in-c--.md).

Se è necessario usare i SID, non modificarli direttamente. Usare invece le funzioni seguenti.



| Funzione                                                       | Descrizione                                                                                                                                               |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AllocateAndInitializeSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid)   | Alloca e Inizializza un SID con il numero di sottoscrittori specificato.                                                                              |
| [**ConvertSidToStringSid**](/windows/desktop/api/Sddl/nf-sddl-convertsidtostringsida)         | Converte un SID in un formato stringa adatto per la visualizzazione, l'archiviazione o il trasporto.                                                                            |
| [**ConvertStringSidToSid**](/windows/desktop/api/Sddl/nf-sddl-convertstringsidtosida)         | Converte un SID in formato stringa in un SID funzionale valido.                                                                                                  |
| [**Copysid ha**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-copysid)                                     | Copia un SID di origine in un buffer.                                                                                                                          |
| [**EqualPrefixSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-equalprefixsid)                       | Verifica l'uguaglianza di due valori di prefisso SID. Un prefisso SID è l'intero SID, ad eccezione dell'ultimo valore di sottoautorizzazione.                                          |
| [**EqualSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-equalsid)                                   | Verifica l'uguaglianza di due SID. Devono corrispondere esattamente per essere considerati uguali.                                                                              |
| [**FreeSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-freesid)                                     | Libera un SID allocato in precedenza tramite la funzione [**AllocateAndInitializeSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid) .                                      |
| [**GetLengthSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getlengthsid)                           | Recupera la lunghezza di un SID.                                                                                                                            |
| [**GetSidIdentifierAuthority**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsididentifierauthority) | Recupera un puntatore all'autorità di identificazione per un SID.                                                                                                |
| [**GetSidLengthRequired**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsidlengthrequired)           | Recupera la dimensione del buffer necessaria per archiviare un SID con un numero specificato di sottoscritte.                                                       |
| [**GetSidSubAuthority**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsidsubauthority)               | Recupera un puntatore a una sottoautorizzazione specificata in un SID.                                                                                                 |
| [**GetSidSubAuthorityCount**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsidsubauthoritycount)     | Recupera il numero di sottoscrittori in un SID.                                                                                                          |
| [**InitializeSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-initializesid)                         | Inizializza una struttura [**SID**](/windows/desktop/api/Winnt/ns-winnt-sid) .                                                                                                               |
| [**IsValidSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-isvalidsid)                               | Verifica la validità di un SID verificando che il numero di revisione si trovi all'interno di un intervallo noto e che il numero di sottoautori è inferiore al valore massimo. |
| [**LookupAccountName**](/windows/desktop/api/Winbase/nf-winbase-lookupaccountnamea)                 | Recupera il SID che corrisponde a un nome di account specificato.                                                                                           |
| [**LookupAccountSid**](/windows/desktop/api/Winbase/nf-winbase-lookupaccountsida)                   | Recupera il nome dell'account che corrisponde a un SID specificato.                                                                                           |



 

 

 
