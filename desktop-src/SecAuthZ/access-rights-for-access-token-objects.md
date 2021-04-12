---
description: Un'applicazione non può modificare l'elenco di controllo di accesso di un oggetto a meno che l'applicazione non disponga dei diritti necessari.
ms.assetid: 5f710fd8-33de-47c0-a8b2-baf3008c4ed7
title: Diritti di accesso per oggetti Access-Token
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bb6a62a8c1518dca30f2abbc4481fa5e11cf081
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345151"
---
# <a name="access-rights-for-access-token-objects"></a>Diritti di accesso per oggetti Access-Token

Un'applicazione non può modificare l'elenco di controllo di accesso di un oggetto a meno che l'applicazione non disponga dei diritti necessari. Questi diritti sono controllati da un descrittore di sicurezza nel token di accesso per l'oggetto. Per altre informazioni sulla sicurezza, vedere [modello di controllo di accesso](access-control-model.md).

Per ottenere o impostare il [descrittore di sicurezza](security-descriptors.md) per un [*token di accesso*](/windows/desktop/SecGloss/a-gly), chiamare le funzioni [**GetKernelObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getkernelobjectsecurity) e [**SetKernelObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setkernelobjectsecurity) .

Quando si chiama la funzione [**OpenProcessToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken) o [**OpenThreadToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) per ottenere un handle per un token di accesso, il sistema controlla i [diritti di accesso](access-rights-and-access-masks.md) richiesti rispetto a DACL nel descrittore di sicurezza del token.

Di seguito sono riportati i diritti di accesso validi per gli oggetti token di accesso:

-   Diritti di accesso di tipo DELETE, READ \_ Control, Write \_ DAC e Write \_ owner. [](standard-access-rights.md) I token di accesso non supportano il diritto di sincronizzazione dell'accesso standard.
-   [Diritto di \_ \_ sicurezza del sistema di accesso](sacl-access-right.md) per ottenere o impostare l'elenco SACL nel descrittore di sicurezza dell'oggetto.
-   Diritti di accesso specifici per i token di accesso, elencati nella tabella seguente.

    | Valore                     | Significato                                                                                                                                                                                                                                                                           |
    |---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | \_ \_ impostazione predefinita del token    | Obbligatorio per modificare il proprietario predefinito, il gruppo primario o l'elenco DACL di un token di accesso.                                                                                                                                                                                                  |
    | \_gruppi di modifica del token \_     | Obbligatorio per modificare gli attributi dei gruppi in un token di accesso.                                                                                                                                                                                                               |
    | \_privilegi di regolazione del token \_ | Necessario per abilitare o disabilitare i privilegi in un token di accesso.                                                                                                                                                                                                                  |
    | \_regola token \_ SESSIONID  | Obbligatorio per modificare l'ID di sessione di un token di accesso. Il \_ privilegio del \_ nome TCB se è obbligatorio.                                                                                                                                                                                    |
    | \_assegnazione token \_ primaria    | Obbligatorio per alleghi un [*token primario*](/windows/desktop/SecGloss/p-gly) a un [*processo*](/windows/desktop/SecGloss/p-gly). \_ \_ Per eseguire questa attività, è necessario anche il privilegio per il nome ASSIGNPRIMARYTOKEN. |
    | TOKEN \_ duplicato          | Obbligatorio per duplicare un token di accesso.                                                                                                                                                                                                                                            |
    | esecuzione del TOKEN \_            | Combina \_ i diritti standard \_ Execute e \_ rappresenta il token.                                                                                                                                                                                                                        |
    | RAPPRESENTAZIONE del TOKEN \_        | Obbligatorio per alleghi un token di accesso di rappresentazione a un processo.                                                                                                                                                                                                                    |
    | \_query token              | Obbligatorio per eseguire una query su un token di accesso.                                                                                                                                                                                                                                                |
    | \_origine query \_ token      | Obbligatorio per eseguire una query sull'origine di un token di accesso.                                                                                                                                                                                                                                  |
    | \_lettura token               | Combina la \_ lettura dei diritti standard \_ e la query del token \_ .                                                                                                                                                                                                                                 |
    | \_scrittura token              | Combina \_ i diritti di scrittura standard, i privilegi di regolazione del token \_ , i \_ \_ \_ gruppi di modifica del token e l' \_ \_ \_ impostazione predefinita del token.                                                                                                                                                                   |
    | \_accesso a tutti i token \_        | Combina tutti i diritti di accesso possibili per un token.                                                                                                                                                                                                                                  |

    

     

 

 
