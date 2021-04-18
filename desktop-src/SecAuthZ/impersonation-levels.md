---
description: L' \_ \_ enumerazione livello di rappresentazione di sicurezza definisce quattro livelli di rappresentazione che determinano le operazioni che un server può eseguire nel contesto dei client.
ms.assetid: ae152dbf-44f0-417f-a85e-09bf60dcfcb0
title: Livelli di rappresentazione (autorizzazione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b91654f42a86e5c47069197bed084df56f5445dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317048"
---
# <a name="impersonation-levels-authorization"></a>Livelli di rappresentazione (autorizzazione)

L' [**enumerazione \_ \_ livello di rappresentazione di sicurezza**](/windows/desktop/api/Winnt/ne-winnt-security_impersonation_level) definisce quattro livelli di rappresentazione che determinano le operazioni che un server può eseguire nel contesto del client.



| Livello di rappresentazione    | Descrizione                                                                                      |
|------------------------|--------------------------------------------------------------------------------------------------|
| SecurityAnonymous      | Il server non può rappresentare o identificare il client.                                            |
| SecurityIdentification | Il server può ottenere l'identità e i privilegi del client, ma non può rappresentare il client. |
| SecurityImpersonation  | Il server può rappresentare il contesto di sicurezza del client nel sistema locale.                    |
| SecurityDelegation     | Il server può rappresentare il contesto di sicurezza del client nei sistemi remoti.                      |



 

Il client di una connessione named pipe, RPC o DDE può controllare il livello di rappresentazione. Ad esempio, un client named pipe può chiamare la funzione [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) per aprire un handle per un named pipe e specificare il livello di rappresentazione del server.

Quando la connessione named pipe, RPC o DDE è remota, i flag passati a [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) per impostare il livello di rappresentazione vengono ignorati. In questo caso, il livello di rappresentazione del client è determinato dai livelli di rappresentazione abilitati dal server, che viene impostato da un flag nell'account del server nel servizio directory. Se, ad esempio, il server è abilitato per la delega, anche il livello di rappresentazione del client verrà impostato sulla delega anche se i flag passati a **CreateFile** specificano il livello di rappresentazione di identificazione.

I client DDE utilizzano la funzione [**DdeSetQualityOfService**](/windows/win32/api/dde/nf-dde-ddesetqualityofservice) con [**la \_ qualità \_ di sicurezza della struttura del \_ servizio**](/windows/desktop/api/Winnt/ns-winnt-security_quality_of_service) per specificare il livello di rappresentazione. Il livello SecurityImpersonation è l'impostazione predefinita per i server named pipe, RPC e DDE. Le funzioni [**ImpersonateSelf**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateself), [**DuplicateToken**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetoken)e [**DuplicateTokenEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex) consentono al chiamante di specificare un livello di rappresentazione. Utilizzare la funzione [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) per recuperare il livello di rappresentazione di un [*token di accesso*](/windows/desktop/SecGloss/a-gly).

A livello di SecurityImpersonation, la maggior parte delle azioni del thread si verifica nel contesto di sicurezza del [*token di rappresentazione*](/windows/desktop/SecGloss/i-gly) del thread invece che nel [*token primario*](/windows/desktop/SecGloss/p-gly) del [*processo*](/windows/desktop/SecGloss/p-gly) che possiede il thread. Se, ad esempio, un thread di rappresentazione apre un [oggetto a protezione diretta](securable-objects.md), il sistema usa il token di rappresentazione per verificare l'accesso del thread. Analogamente, se un thread di rappresentazione crea un nuovo oggetto, ad esempio chiamando la funzione [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) , il proprietario del nuovo oggetto è il proprietario predefinito del [*token di accesso*](/windows/desktop/SecGloss/a-gly)del client.

Tuttavia, il sistema usa il token primario del processo anziché il token di rappresentazione del thread chiamante nelle situazioni seguenti:

-   Se un thread di rappresentazione chiama la funzione [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) , il nuovo processo eredita sempre il token primario del processo.
-   Per le funzioni che richiedono il \_ privilegio se TCB \_ , ad esempio la funzione [**LogonUser**](/windows/desktop/api/winbase/nf-winbase-logonusera) , il sistema verifica sempre il privilegio nel token primario del processo.
-   Per le funzioni che richiedono il \_ privilegio se controlla \_ nome, ad esempio la funzione [**ObjectOpenAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-objectopenauditalarma) , il sistema verifica sempre il privilegio nel token primario del processo.
-   In una chiamata alla funzione [**OpenThreadToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) , un thread può specificare se la funzione usa il token di rappresentazione o il token primario per determinare se concedere l'accesso richiesto.

 

 
