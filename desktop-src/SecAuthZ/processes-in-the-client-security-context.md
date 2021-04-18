---
description: Un'applicazione server può chiamare la funzione CreateProcessAsUser ha per creare un nuovo processo eseguito in un contesto di sicurezza dei client.
ms.assetid: bd416109-fe76-4d55-bc63-3ebbcf32b92a
title: Processi nel contesto di sicurezza del client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29c9bafb576bd0d195ae762c69be885ac32f1071
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308147"
---
# <a name="processes-in-the-client-security-context"></a>Processi nel contesto di sicurezza del client

Un'applicazione server può chiamare la funzione [**CreateProcessAsUser ha**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) per creare un nuovo processo eseguito nel [*contesto di sicurezza*](/windows/desktop/SecGloss/s-gly)di un client. Quando viene chiamato con il [*token di accesso*](/windows/desktop/SecGloss/a-gly)di un client, **CreateProcessAsUser ha** richiede il \_ \_ nome ASSIGNPRIMARYTOKEN e i \_ privilegi per il nome della quota if increase \_ \_ , che sono conservati dai servizi Windows in esecuzione nell' [account LocalSystem](/windows/desktop/Services/localsystem-account).

La funzione [**CreateProcessAsUser ha**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) richiede anche un [*token di accesso primario*](/windows/desktop/SecGloss/p-gly). Un server può ottenere un token di accesso primario per un client [avviando una sessione di accesso](client-logon-sessions.md) per il client o [rappresentando il client](client-impersonation.md) e duplicando il [*token di rappresentazione*](/windows/desktop/SecGloss/i-gly).

Nelle procedure riportate di seguito vengono descritti due modi per creare un processo client.

**Per creare un processo client accedendo al client**

1.  Accedere al computer locale usando le [*credenziali*](/windows/desktop/SecGloss/c-gly) del client in una chiamata a [**LogonUser**](/windows/desktop/api/winbase/nf-winbase-logonusera). **LogonUser** produce un token primario per la sessione di [*accesso*](/windows/desktop/SecGloss/l-gly)del client.
2.  Se il server deve usare il contesto di sicurezza del client, ottenere l'accesso al file eseguibile per il [*processo*](/windows/desktop/SecGloss/p-gly) client usando il token primario in una chiamata alla funzione [**ImpersonateLoggedOnUser**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser) .
3.  Creare un processo nel contesto di sicurezza del client usando il token primario in una chiamata a [**CreateProcessAsUser ha**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera).

> [!Note]  
> Un processo creato con la tecnica seguente potrebbe non essere in grado di accedere alle risorse di rete a meno che non disponga delle [*credenziali*](/windows/desktop/SecGloss/c-gly)del client.

 

**Per creare un processo client rappresentando il client**

1.  Avviare la rappresentazione utilizzando una funzione di rappresentazione, ad esempio [**ImpersonateNamedPipeClient**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-impersonatenamedpipeclient).
2.  Chiamare la funzione [**OpenThreadToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) per ottenere un token di rappresentazione con il contesto di sicurezza del client.
3.  Chiamare la funzione [**DuplicateTokenEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex) per convertire il token di rappresentazione in un token primario.
4.  Usare il token primario in una chiamata alla funzione [**CreateProcessAsUser ha**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) per creare un processo nel contesto di sicurezza del client.

Per impostazione predefinita, [**CreateProcessAsUser ha**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) crea il [*processo*](/windows/desktop/SecGloss/p-gly) client in una stazione di finestra e un desktop non interattivo. Per creare un processo interattivo, il server deve innanzitutto impostare gli [*elenchi di controllo di accesso discrezionale*](/windows/desktop/SecGloss/d-gly) (DACL) di Interactive Window Station e desktop per assicurarsi che il client sia autorizzato ad accedervi. Il modo migliore per eseguire questa operazione consiste nell'accedere al client, [ottenere l'ID di sicurezza (SID) della sessione di accesso del client](/previous-versions//aa446670(v=vs.85))e quindi usare tale SID nelle voci ACE consentite di accesso sia nella stazione di finestra interattiva che nel desktop. Il server può quindi chiamare **CreateProcessAsUser ha**, specificando la stazione finestra interattiva e il desktop WinSta0 \\ predefinito. Per un esempio in cui viene illustrata questa procedura, vedere [avvio di un processo client interattivo in C++](/previous-versions//aa379608(v=vs.85)).

 

 
