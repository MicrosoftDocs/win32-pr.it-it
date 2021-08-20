---
description: Un token di accesso è un oggetto che descrive il contesto di sicurezza di un processo o di un thread.
ms.assetid: 350159c9-2399-427a-ba44-c897a9664299
title: Token di accesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f9067df376006f7f7b61dedadc074c23674b2278fb5c311794bbddd12256277
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785391"
---
# <a name="access-tokens"></a>Token di accesso

Un [*token di accesso*](/windows/desktop/SecGloss/a-gly) è un oggetto che descrive il contesto di [*sicurezza*](/windows/desktop/SecGloss/s-gly) di un processo [*o*](/windows/desktop/SecGloss/p-gly) di un thread. Le informazioni in un token includono l'identità e i privilegi dell'account utente associato al processo o al thread. Quando un utente esegue l'accesso, il sistema verifica la password dell'utente confrontandolo con le informazioni archiviate in un database di sicurezza. Se la password è [*autenticata,*](/windows/desktop/SecGloss/a-gly)il sistema produce un token di accesso. Ogni processo eseguito per conto di questo utente dispone di una copia di questo token di accesso.

Il sistema usa un token di accesso per identificare l'utente quando un thread interagisce con un oggetto [a](securable-objects.md) protezione diretta o tenta di eseguire un'attività di sistema che richiede privilegi. I token di accesso contengono le informazioni seguenti:

-   ID [di sicurezza](security-identifiers.md) (SID) per l'account dell'utente
-   SID per i gruppi di cui l'utente è membro
-   SID [*di accesso che*](/windows/desktop/SecGloss/l-gly) identifica la sessione di accesso [*corrente*](/windows/desktop/SecGloss/l-gly)
-   Elenco dei privilegi [dell'utente](privileges.md) o dei gruppi dell'utente
-   SID proprietario
-   SID del gruppo primario
-   DACL [predefinito utilizzato](access-control-lists.md) dal sistema quando l'utente crea un oggetto a protezione diretta senza specificare un [*descrittore di sicurezza*](/windows/desktop/SecGloss/s-gly)
-   Origine del token di accesso
-   Se il token è un [*token primario*](/windows/desktop/SecGloss/p-gly) o [di rappresentazione](client-impersonation.md)
-   Elenco facoltativo di [SID di limitazione](restricted-tokens.md)
-   Livelli di rappresentazione correnti
-   Altre statistiche

Ogni processo ha un [*token*](/windows/desktop/SecGloss/p-gly) primario che descrive il [*contesto di sicurezza*](/windows/desktop/SecGloss/s-gly) dell'account utente associato al processo. Per impostazione predefinita, il sistema usa il token primario quando un thread del processo interagisce con un oggetto a protezione diretta. Inoltre, un thread può rappresentare un account client. La rappresentazione consente al thread di interagire con gli oggetti a protezione diretta usando il contesto di sicurezza del client. Un thread che rappresenta un client dispone sia di un token primario che di [*un token di rappresentazione.*](/windows/desktop/SecGloss/i-gly)

Usare la [**funzione OpenProcessToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken) per recuperare un handle per il token primario di un processo. Usare la [**funzione OpenThreadToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) per recuperare un handle per il token di rappresentazione di un thread. Per altre informazioni, vedere [Rappresentazione.](client-impersonation.md)

È possibile usare le funzioni seguenti per modificare i token di accesso.



| Funzione                                               | Descrizione                                                                                                                                                            |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AdjustTokenGroups**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokengroups)         | Modifica le informazioni sul gruppo in un token di accesso.                                                                                                                      |
| [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) | Abilita o disabilita i privilegi in un token di accesso. Non concede nuovi privilegi né revoca quelli esistenti.                                                       |
| [**CheckTokenMembership**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-checktokenmembership)   | Determina se un SID specificato è abilitato in un token di accesso specificato.                                                                                             |
| [**CreateRestrictedToken**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken) | Crea un nuovo token che è una versione con restrizioni di un token esistente. Il token con restrizioni può avere SID disabilitati, privilegi eliminati e un elenco di SID con restrizioni. |
| [**DuplicateToken**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetoken)               | Crea un nuovo token di rappresentazione che duplica un token esistente.                                                                                                   |
| [**DuplicateTokenEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex)           | Crea un nuovo token primario o token di rappresentazione che duplica un token esistente.                                                                                  |
| [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation)     | Recupera informazioni su un token.                                                                                                                                   |
| [**IsTokenRestricted**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-istokenrestricted)         | Determina se un token dispone di un elenco di SID di limitazione.                                                                                                             |
| [**OpenProcessToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken)           | Recupera un handle per il token di accesso primario per un processo.                                                                                                          |
| [**OpenThreadToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken)             | Recupera un handle per il token di accesso di rappresentazione per un thread.                                                                                                     |
| [**SetThreadToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadtoken)               | Assegna o rimuove un token di rappresentazione per un thread.                                                                                                                |
| [**SetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-settokeninformation)     | Modifica il proprietario, il gruppo primario o l'elenco DACL predefinito di un token.                                                                                                               |



 

Le funzioni del token di accesso usano le strutture seguenti per descrivere le parti di un token di accesso.



| Struttura                                            | Descrizione                                                                                           |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**CONTROLLO \_ TOKEN**](/windows/desktop/api/Winnt/ns-winnt-token_control)              | Informazioni che identificano un token di accesso.                                                          |
| [**TOKEN \_ DEFAULT \_ DACL**](/windows/desktop/api/Winnt/ns-winnt-token_default_dacl)   | DACL predefinito utilizzato dal sistema nei descrittori di sicurezza dei nuovi oggetti creati da un thread. |
| [**GRUPPI DI \_ TOKEN**](/windows/desktop/api/Winnt/ns-winnt-token_groups)                | Specifica i SID e gli attributi dei SID di gruppo in un token di accesso.                               |
| [**PROPRIETARIO DEL \_ TOKEN**](/windows/desktop/api/Winnt/ns-winnt-token_owner)                  | SID del proprietario predefinito per i descrittori di sicurezza dei nuovi oggetti.                                    |
| [**TOKEN \_ PRIMARY \_ GROUP**](/windows/desktop/api/Winnt/ns-winnt-token_primary_group) | SID del gruppo primario predefinito per i descrittori di sicurezza dei nuovi oggetti.                            |
| [**PRIVILEGI \_ DI TOKEN**](/windows/desktop/api/Winnt/ns-winnt-token_privileges)        | Privilegi associati a un token di accesso. Determina inoltre se i privilegi sono abilitati.   |
| [**ORIGINE \_ TOKEN**](/windows/desktop/api/Winnt/ns-winnt-token_source)                | Origine di un token di accesso.                                                                        |
| [**TOKEN \_ STATISTICS**](/windows/desktop/api/Winnt/ns-winnt-token_statistics)        | Statistiche associate a un token di accesso.                                                           |
| [**UTENTE \_ TOKEN**](/windows/desktop/api/Winnt/ns-winnt-token_user)                    | SID dell'utente associato a un token di accesso.                                                  |



 

Le funzioni del token di accesso usano i tipi di enumerazione seguenti.



| Tipo di enumerazione                                             | Specifica                                                                       |
|--------------------------------------------------------------|---------------------------------------------------------------------------------|
| [**CLASSE \_ DI INFORMAZIONI SUI \_ TOKEN**](/windows/desktop/api/Winnt/ne-winnt-token_information_class) | Identifica il tipo di informazioni impostate o recuperate da un token di accesso. |
| [**TIPO DI \_ TOKEN**](/windows/desktop/api/Winnt/ne-winnt-token_type)                            | Identifica un token di accesso come token primario o di rappresentazione.                 |



 

 

 
