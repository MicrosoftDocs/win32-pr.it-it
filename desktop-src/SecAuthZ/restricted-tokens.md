---
description: Un token con restrizioni è un token di accesso primario o di rappresentazione modificato dalla funzione CreateRestrictedToken.
ms.assetid: 06580ab9-ff58-4aa9-bf88-9536a2e1981d
title: Token con restrizioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53f63402997d9e1304ca75ca117554ce52c3aa727f44b3b8316c28e1ecfcea45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118912009"
---
# <a name="restricted-tokens"></a>Token con restrizioni

Un token con restrizioni è un [*token*](/windows/desktop/SecGloss/a-gly) [*di*](/windows/desktop/SecGloss/p-gly) accesso primario o di rappresentazione modificato dalla [**funzione CreateRestrictedToken.**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken) Un [*processo*](/windows/desktop/SecGloss/p-gly) o un thread [](/windows/desktop/SecGloss/s-gly) di rappresentazione in esecuzione nel contesto di sicurezza di un token con restrizioni è limitato nella possibilità di accedere a oggetti a protezione diretta o di eseguire operazioni con privilegi. La **funzione CreateRestrictedToken** può limitare un token nei modi seguenti:

-   Rimuovere [i privilegi](privileges.md) dal token.
-   Applicare l'attributo di sola negazione ai SID nel token in modo che non possa essere usato per accedere agli oggetti protetti. Per altre informazioni sull'attributo di sola negazione, vedere [Attributi SID in un token di accesso](sid-attributes-in-an-access-token.md).
-   Specificare un elenco di SID di limitazione, che possono limitare l'accesso agli oggetti a protezione diretta.

Il sistema usa l'elenco di SID di limitazione quando controlla l'accesso del token a un oggetto a protezione diretta. Quando un processo o un thread con restrizioni tenta di accedere a un oggetto a protezione diretta, il sistema esegue due controlli di accesso: uno usando i SID abilitati del token e l'altro usando l'elenco di SID di limitazione. L'accesso viene concesso solo se entrambi i controlli di accesso consentono i diritti di accesso richiesti. Per altre informazioni sui controlli di accesso, vedere Controllo dell'accesso a un oggetto da parte degli [daCL](how-dacls-control-access-to-an-object.md).

È possibile usare un [*token primario*](/windows/desktop/SecGloss/p-gly) con restrizioni in una chiamata alla [**funzione CreateProcessAsUser.**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) In genere, il processo che chiama **CreateProcessAsUser** deve avere il privilegio edizione Standard ASSIGNPRIMARYTOKEN NAME, che in genere viene mantenuto solo dal codice di sistema o dai servizi in esecuzione \_ \_ nell'account LocalSystem. Tuttavia, se la **chiamata CreateProcessAsUser** specifica una versione limitata del token primario del chiamante, questo privilegio non è necessario. Ciò consente alle applicazioni comuni di creare processi con restrizioni.

È anche possibile usare un token primario o [*di rappresentazione*](/windows/desktop/SecGloss/i-gly) con restrizioni nella [**funzione ImpersonateLoggedOnUser.**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser)

Per determinare se un token include un elenco di SID limitati, chiamare la [**funzione IsTokenRestricted.**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-istokenrestricted)

> [!Note]  
> Le applicazioni che usano token con restrizioni devono eseguire l'applicazione con restrizioni su desktop diversi dal desktop predefinito. Questa operazione è necessaria per impedire un attacco da parte di un'applicazione con restrizioni, tramite **SendMessage** o **PostMessage**, ad applicazioni senza restrizioni sul desktop predefinito. Se necessario, passare da un desktop all'altro per l'applicazione.

 

 

 
