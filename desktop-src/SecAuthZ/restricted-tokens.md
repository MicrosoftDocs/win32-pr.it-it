---
description: Un token con restrizioni è un token di accesso primario o di rappresentazione modificato dalla funzione CreateRestrictedToken.
ms.assetid: 06580ab9-ff58-4aa9-bf88-9536a2e1981d
title: Token con restrizioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fee8e6c89915e3edd0a9206f84a0d3d5697a3cb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129911"
---
# <a name="restricted-tokens"></a>Token con restrizioni

Un token con restrizioni è un [*token di accesso*](/windows/desktop/SecGloss/a-gly) [*primario*](/windows/desktop/SecGloss/p-gly) o di rappresentazione modificato dalla funzione [**CreateRestrictedToken**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken) . Un [*processo*](/windows/desktop/SecGloss/p-gly) o un thread di rappresentazione eseguito nel [*contesto di sicurezza*](/windows/desktop/SecGloss/s-gly) di un token con restrizioni è limitato alla possibilità di accedere agli oggetti a protezione diretta o di eseguire operazioni con privilegi. La funzione **CreateRestrictedToken** può limitare un token nei modi seguenti:

-   Rimuovere i [privilegi](privileges.md) dal token.
-   Applicare l'attributo Deny-only ai SID nel token in modo che non possano essere utilizzati per accedere agli oggetti protetti. Per altre informazioni sull'attributo Deny-only, vedere [attributi SID in un token di accesso](sid-attributes-in-an-access-token.md).
-   Specificare un elenco di SID di restrizione, che possono limitare l'accesso agli oggetti a protezione diretta.

Il sistema utilizza l'elenco dei SID di restrizione quando controlla l'accesso del token a un oggetto a protezione diretta. Quando un processo o un thread con restrizioni tenta di accedere a un oggetto a protezione diretta, il sistema esegue due controlli di accesso: uno usando i SID abilitati del token e un altro usando l'elenco dei SID di restrizione. L'accesso viene concesso solo se entrambi i controlli di accesso consentono i diritti di accesso richiesti. Per ulteriori informazioni sui controlli di accesso, vedere [come gli elenchi DACL controllano l'accesso a un oggetto](how-dacls-control-access-to-an-object.md).

È possibile usare un [*token primario*](/windows/desktop/SecGloss/p-gly) con restrizioni in una chiamata alla funzione [**CreateProcessAsUser ha**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) . In genere, il processo che chiama **CreateProcessAsUser ha** deve avere il \_ privilegio se ASSIGNPRIMARYTOKEN \_ Name, che in genere viene mantenuto solo dal codice di sistema o dai servizi in esecuzione nell'account LocalSystem. Tuttavia, se la chiamata **CreateProcessAsUser ha** specifica una versione limitata del token primario del chiamante, questo privilegio non è obbligatorio. Questo consente alle applicazioni ordinarie di creare processi con restrizioni.

È anche possibile usare un [*token di rappresentazione*](/windows/desktop/SecGloss/i-gly) o primario con restrizioni nella funzione [**ImpersonateLoggedOnUser**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser) .

Per determinare se un token ha un elenco di SID di restrizione, chiamare la funzione [**IsTokenRestricted**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-istokenrestricted) .

> [!Note]  
> Le applicazioni che usano token con restrizioni devono eseguire l'applicazione con restrizioni su desktop diversi dal desktop predefinito. Questa operazione è necessaria per evitare un attacco da parte di un'applicazione con restrizioni, tramite **SendMessage** o **PostMessage**, alle applicazioni senza restrizioni sul desktop predefinito. Se necessario, spostarsi tra i desktop a scopo di applicazione.

 

 

 
