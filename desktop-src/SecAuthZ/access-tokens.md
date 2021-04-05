---
description: Un token di accesso è un oggetto che descrive il contesto di sicurezza di un processo o di un thread.
ms.assetid: 350159c9-2399-427a-ba44-c897a9664299
title: Token di accesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0993c1f5aebab797ab28e61b36f59507e4d2f1ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882646"
---
# <a name="access-tokens"></a>Token di accesso

Un [*token di accesso*](/windows/desktop/SecGloss/a-gly) è un oggetto che descrive il [*contesto di sicurezza*](/windows/desktop/SecGloss/s-gly) di un [*processo*](/windows/desktop/SecGloss/p-gly) o di un thread. Le informazioni contenute in un token includono l'identità e i privilegi dell'account utente associato al processo o al thread. Quando un utente esegue l'accesso, il sistema verifica la password dell'utente confrontandolo con le informazioni archiviate in un database di sicurezza. Se la password viene [*autenticata*](/windows/desktop/SecGloss/a-gly), il sistema produce un token di accesso. Ogni processo eseguito per conto di questo utente ha una copia di questo token di accesso.

Il sistema utilizza un token di accesso per identificare l'utente quando un thread interagisce con un [oggetto a protezione diretta](securable-objects.md) o tenta di eseguire un'attività di sistema che richiede privilegi. I token di accesso contengono le informazioni seguenti:

-   [ID di sicurezza](security-identifiers.md) (SID) per l'account dell'utente
-   SID per i gruppi di cui l'utente è membro
-   [*SID di accesso*](/windows/desktop/SecGloss/l-gly) che identifica la [*sessione di accesso*](/windows/desktop/SecGloss/l-gly) corrente
-   Elenco dei [privilegi](privileges.md) utilizzati dall'utente o dai gruppi dell'utente
-   SID proprietario
-   SID del gruppo primario
-   [DACL](access-control-lists.md) predefinito utilizzato dal sistema quando l'utente crea un oggetto a protezione diretta senza specificare un [*descrittore di sicurezza*](/windows/desktop/SecGloss/s-gly) .
-   Origine del token di accesso
-   Indica se il token è un token [*primario*](/windows/desktop/SecGloss/p-gly) o di [rappresentazione](client-impersonation.md)
-   Elenco facoltativo dei [SID di restrizione](restricted-tokens.md)
-   Livelli di rappresentazione correnti
-   Altre statistiche

Ogni processo dispone di un [*token primario*](/windows/desktop/SecGloss/p-gly) che descrive il [*contesto di sicurezza*](/windows/desktop/SecGloss/s-gly) dell'account utente associato al processo. Per impostazione predefinita, il sistema usa il token primario quando un thread del processo interagisce con un oggetto a protezione diretta. Un thread può inoltre rappresentare un account client. La rappresentazione consente al thread di interagire con gli oggetti a protezione diretta usando il contesto di sicurezza del client. Un thread che rappresenta un client dispone di un token primario e di un [*token di rappresentazione*](/windows/desktop/SecGloss/i-gly).

Usare la funzione [**OpenProcessToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken) per recuperare un handle per il token primario di un processo. Utilizzare la funzione [**OpenThreadToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) per recuperare un handle per il token di rappresentazione di un thread. Per ulteriori informazioni, vedere [rappresentazione](client-impersonation.md).

Per modificare i token di accesso, è possibile usare le funzioni seguenti.



| Funzione                                               | Descrizione                                                                                                                                                            |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AdjustTokenGroups**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokengroups)         | Modifica le informazioni sul gruppo in un token di accesso.                                                                                                                      |
| [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) | Abilita o Disabilita i privilegi in un token di accesso. Non concede nuovi privilegi o revoca quelli esistenti.                                                       |
| [**CheckTokenMembership**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-checktokenmembership)   | Determina se un SID specificato è abilitato in un token di accesso specificato.                                                                                             |
| [**CreateRestrictedToken**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken) | Crea un nuovo token che è una versione con restrizioni di un token esistente. Il token con restrizioni può avere SID disabilitati, privilegi eliminati e un elenco di SID con restrizioni. |
| [**DuplicateToken**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetoken)               | Crea un nuovo token di rappresentazione che duplica un token esistente.                                                                                                   |
| [**DuplicateTokenEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex)           | Crea un nuovo token primario o un token di rappresentazione che duplica un token esistente.                                                                                  |
| [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation)     | Recupera le informazioni su un token.                                                                                                                                   |
| [**IsTokenRestricted**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-istokenrestricted)         | Determina se un token ha un elenco di SID di restrizione.                                                                                                             |
| [**OpenProcessToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken)           | Recupera un handle per il token di accesso primario per un processo.                                                                                                          |
| [**OpenThreadToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken)             | Recupera un handle per il token di accesso di rappresentazione per un thread.                                                                                                     |
| [**SetThreadToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadtoken)               | Assegna o rimuove un token di rappresentazione per un thread.                                                                                                                |
| [**SetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-settokeninformation)     | Modifica il proprietario, il gruppo primario o l'elenco DACL predefinito di un token.                                                                                                               |



 

Le funzioni del token di accesso utilizzano le strutture seguenti per descrivere le parti di un token di accesso.



| Struttura                                            | Descrizione                                                                                           |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**\_controllo token**](/windows/desktop/api/Winnt/ns-winnt-token_control)              | Informazioni che identificano un token di accesso.                                                          |
| [**\_DACL predefinito del token \_**](/windows/desktop/api/Winnt/ns-winnt-token_default_dacl)   | DACL predefinito utilizzato dal sistema nei descrittori di sicurezza dei nuovi oggetti creati da un thread. |
| [**gruppi di TOKEN \_**](/windows/desktop/api/Winnt/ns-winnt-token_groups)                | Specifica i SID e gli attributi dei SID di gruppo in un token di accesso.                               |
| [**proprietario del TOKEN \_**](/windows/desktop/api/Winnt/ns-winnt-token_owner)                  | SID predefinito del proprietario per i descrittori di sicurezza dei nuovi oggetti.                                    |
| [**\_gruppo primario \_ token**](/windows/desktop/api/Winnt/ns-winnt-token_primary_group) | SID del gruppo primario predefinito per i descrittori di sicurezza dei nuovi oggetti.                            |
| [**privilegi di TOKEN \_**](/windows/desktop/api/Winnt/ns-winnt-token_privileges)        | Privilegi associati a un token di accesso. Determina inoltre se i privilegi sono abilitati.   |
| [**\_origine token**](/windows/desktop/api/Winnt/ns-winnt-token_source)                | Origine di un token di accesso.                                                                        |
| [**\_statistiche token**](/windows/desktop/api/Winnt/ns-winnt-token_statistics)        | Statistiche associate a un token di accesso.                                                           |
| [**\_utente token**](/windows/desktop/api/Winnt/ns-winnt-token_user)                    | SID dell'utente associato a un token di accesso.                                                  |



 

Le funzioni del token di accesso usano i seguenti tipi di enumerazione.



| Tipo di enumerazione                                             | Specifica                                                                       |
|--------------------------------------------------------------|---------------------------------------------------------------------------------|
| [**\_classe di informazioni sui token \_**](/windows/desktop/api/Winnt/ne-winnt-token_information_class) | Identifica il tipo di informazioni da impostare o recuperare da un token di accesso. |
| [**tipo di TOKEN \_**](/windows/desktop/api/Winnt/ne-winnt-token_type)                            | Identifica un token di accesso come token primario o di rappresentazione.                 |



 

 

 
