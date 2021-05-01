---
description: Un'applicazione non può modificare l'elenco di controllo di accesso di un oggetto a meno che l'applicazione non abbia i diritti necessari.
ms.assetid: 5f710fd8-33de-47c0-a8b2-baf3008c4ed7
title: Diritti di accesso per Access-Token oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 469081d2caa4e5ff7c9b7c55b4c09c31cff1acac
ms.sourcegitcommit: dc2f43e0f23f4a4ce239118cf9a5180f3ff0dd1d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/30/2021
ms.locfileid: "108327196"
---
# <a name="access-rights-for-access-token-objects"></a>Diritti di accesso per Access-Token oggetti

Un'applicazione non può modificare l'elenco di controllo di accesso di un oggetto a meno che l'applicazione non abbia i diritti necessari. Questi diritti sono controllati da un descrittore di sicurezza nel token di accesso per l'oggetto. Per altre informazioni sulla sicurezza, vedere Modello [di controllo di accesso.](access-control-model.md)

Per ottenere o impostare il [descrittore di sicurezza](security-descriptors.md) per un token di [*accesso,*](/windows/desktop/SecGloss/a-gly)chiamare le [**funzioni GetKernelObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getkernelobjectsecurity) [**e SetKernelObjectSecurity.**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setkernelobjectsecurity)

Quando si chiama la funzione [**OpenProcessToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken) o [**OpenThreadToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) per ottenere un [](access-rights-and-access-masks.md) handle a un token di accesso, il sistema controlla i diritti di accesso richiesti rispetto all'elenco DACL nel descrittore di sicurezza del token.

Di seguito sono riportati i diritti di accesso validi per gli oggetti token di accesso:

-   Diritti di accesso standard DELETE, READ \_ CONTROL, WRITE DAC e \_ WRITE \_ [](standard-access-rights.md)OWNER. I token di accesso non supportano il diritto di accesso standard SYNCHRONIZE.
-   Diritto [ACCESS SYSTEM SECURITY \_ \_ per](sacl-access-right.md) ottenere o impostare l'elenco SACL nel descrittore di sicurezza dell'oggetto.
-   Diritti di accesso specifici per i token di accesso, elencati nella tabella seguente.

    | Valore                     | Significato                                                                                                                                                                                                                                                                           |
    |---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | MODIFICA \_ DEL \_ TOKEN PREDEFINITA    | Obbligatorio per modificare il proprietario predefinito, il gruppo primario o l'elenco DACL di un token di accesso.                                                                                                                                                                                                  |
    | GRUPPI \_ DI REGOLAZIONE \_ DEI TOKEN     | Obbligatorio per modificare gli attributi dei gruppi in un token di accesso.                                                                                                                                                                                                               |
    | MODIFICA \_ DEI PRIVILEGI PER I \_ TOKEN | Obbligatorio per abilitare o disabilitare i privilegi in un token di accesso.                                                                                                                                                                                                                  |
    | REGOLAZIONE \_ \_ DEL TOKEN SESSIONID  | Obbligatorio per modificare l'ID sessione di un token di accesso. Il \_ privilegio SE TCB \_ NAME è obbligatorio.                                                                                                                                                                                    |
    | TOKEN \_ ASSIGN \_ PRIMARY    | Obbligatorio per collegare [*un token primario*](/windows/desktop/SecGloss/p-gly) a un [*processo*](/windows/desktop/SecGloss/p-gly). Per eseguire questa attività è necessario anche il privilegio SE \_ ASSIGNPRIMARYTOKEN \_ NAME. |
    | TOKEN \_ DUPLICATO          | Obbligatorio per duplicare un token di accesso.                                                                                                                                                                                                                                            |
    | TOKEN \_ EXECUTE            | Uguale a STANDARD \_ RIGHTS \_ EXECUTE.                                                                                                                                                                                                                                                |
    | TOKEN \_ IMPERSONATE        | Obbligatorio per collegare un token di accesso di rappresentazione a un processo.                                                                                                                                                                                                                    |
    | TOKEN \_ QUERY              | Obbligatorio per eseguire query su un token di accesso.                                                                                                                                                                                                                                                |
    | ORIGINE \_ QUERY \_ TOKEN      | Obbligatorio per eseguire query sull'origine di un token di accesso.                                                                                                                                                                                                                                  |
    | TOKEN \_ READ               | Combina STANDARD \_ RIGHTS READ e TOKEN \_ \_ QUERY.                                                                                                                                                                                                                                 |
    | SCRITTURA \_ DI TOKEN              | Combina I PRIVILEGI STANDARD \_ RIGHTS \_ WRITE, TOKEN \_ ADJUST \_ PRIVILEGES, TOKEN \_ ADJUST GROUPS e TOKEN ADJUST \_ \_ \_ DEFAULT.                                                                                                                                                                   |
    | TOKEN \_ ALL \_ ACCESS        | Combina tutti i diritti di accesso possibili per un token.                                                                                                                                                                                                                                  |

    

     

 

 
