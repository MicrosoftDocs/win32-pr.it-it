---
description: L'enumerazione SECURITY IMPERSONATION LEVEL definisce quattro livelli di rappresentazione che determinano le operazioni \_ che un server può eseguire nel contesto dei \_ client.
ms.assetid: ae152dbf-44f0-417f-a85e-09bf60dcfcb0
title: Livelli di rappresentazione (autorizzazione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdf80f4f6b84499a94659c137c629d66a041752e5171cb3fa7220506586f36e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119414591"
---
# <a name="impersonation-levels-authorization"></a>Livelli di rappresentazione (autorizzazione)

[**L'enumerazione SECURITY \_ IMPERSONATION \_ LEVEL**](/windows/desktop/api/Winnt/ne-winnt-security_impersonation_level) definisce quattro livelli di rappresentazione che determinano le operazioni che un server può eseguire nel contesto del client.



| Livello di rappresentazione    | Descrizione                                                                                      |
|------------------------|--------------------------------------------------------------------------------------------------|
| SecurityAnonymous      | Il server non è in grado di rappresentare o identificare il client.                                            |
| SecurityIdentification | Il server può ottenere l'identità e i privilegi del client, ma non può rappresentare il client. |
| SecurityImpersonation  | Il server può rappresentare il contesto di sicurezza del client nel sistema locale.                    |
| SecurityDelegation     | Il server può rappresentare il contesto di sicurezza del client nei sistemi remoti.                      |



 

Il client di una named pipe, RPC o DDE può controllare il livello di rappresentazione. Ad esempio, un client named pipe può chiamare la funzione [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) per aprire un handle a un named pipe e specificare il livello di rappresentazione del server.

Quando la named pipe, RPC o DDE è remota, i flag passati a [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) per impostare il livello di rappresentazione vengono ignorati. In questo caso, il livello di rappresentazione del client è determinato dai livelli di rappresentazione abilitati dal server, impostati da un flag sull'account del server nel servizio directory. Ad esempio, se il server è abilitato per la delega, anche il livello di rappresentazione del client verrà impostato sulla delega anche se i flag passati a **CreateFile** specificano il livello di rappresentazione di identificazione.

I client DDE usano [**la funzione DdeSetQualityOfService**](/windows/win32/api/dde/nf-dde-ddesetqualityofservice) con la [**struttura SECURITY QUALITY OF \_ \_ \_ SERVICE**](/windows/desktop/api/Winnt/ns-winnt-security_quality_of_service) per specificare il livello di rappresentazione. Il livello SecurityImpersonation è l'impostazione predefinita per i named pipe, RPC e DDE. Le [**funzioni ImpersonateSelf**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateself), [**DuplicateToken**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetoken)e [**DuplicateTokenEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex) consentono al chiamante di specificare un livello di rappresentazione. Usare la [**funzione GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) per recuperare il livello di rappresentazione di un [*token di accesso*](/windows/desktop/SecGloss/a-gly).

A livello di SecurityImpersonation, la maggior parte delle azioni del thread si verifica nel contesto di [](/windows/desktop/SecGloss/p-gly) sicurezza del token di rappresentazione del thread anziché nel [*token*](/windows/desktop/SecGloss/i-gly) primario del processo proprietario del thread. [](/windows/desktop/SecGloss/p-gly) Ad esempio, se un thread di rappresentazione apre un oggetto [a](securable-objects.md)protezione diretta, il sistema usa il token di rappresentazione per controllare l'accesso del thread. Analogamente, se un thread di rappresentazione crea un nuovo oggetto, ad esempio chiamando la funzione [**CreateFile,**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) il proprietario del nuovo oggetto è il proprietario predefinito dal [*token*](/windows/desktop/SecGloss/a-gly)di accesso del client.

Tuttavia, il sistema usa il token primario del processo anziché il token di rappresentazione del thread chiamante nelle situazioni seguenti:

-   Se un thread di rappresentazione chiama [**la funzione CreateProcess,**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) il nuovo processo eredita sempre il token primario del processo.
-   Per le funzioni che richiedono edizione Standard il privilegio TCB NAME, ad esempio la funzione \_ \_ [**LogonUser,**](/windows/desktop/api/winbase/nf-winbase-logonusera) il sistema verifica sempre il privilegio nel token primario del processo.
-   Per le funzioni che richiedono il privilegio edizione Standard AUDIT NAME, ad esempio la funzione \_ \_ [**ObjectOpenAuditAlarm,**](/windows/desktop/api/Winbase/nf-winbase-objectopenauditalarma) il sistema verifica sempre la presenza del privilegio nel token primario del processo.
-   In una chiamata alla funzione [**OpenThreadToken,**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) un thread può specificare se la funzione usa il token di rappresentazione o il token primario per determinare se concedere l'accesso richiesto.

 

 
