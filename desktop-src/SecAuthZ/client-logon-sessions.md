---
description: Un server con \_ \_ privilegi per il nome se TCB, ad esempio un servizio Windows in esecuzione nell'account LocalSystem, può chiamare la funzione LogonUser per autenticare un client nel computer in cui è in esecuzione il server.
ms.assetid: 27328497-8f04-42e8-aadd-4c33b9907b94
title: Sessioni di accesso client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1439b27637b0e46df3b468b42cb9c45ac8f759f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527642"
---
# <a name="client-logon-sessions"></a>Sessioni di accesso client

Un server con \_ \_ privilegi per il nome se TCB, ad esempio un servizio Windows in esecuzione nell' [account LocalSystem](/windows/desktop/Services/localsystem-account), può chiamare la funzione [**LogonUser**](/windows/desktop/api/winbase/nf-winbase-logonusera) per [*autenticare*](/windows/desktop/SecGloss/a-gly) un client nel computer in cui è in esecuzione il server. La funzione **LogonUser** avvia una nuova [*sessione*](/windows/desktop/SecGloss/s-gly) di accesso e restituisce un [*token di accesso primario*](/windows/desktop/SecGloss/p-gly) che contiene le informazioni di sicurezza del client. È possibile usare questo token primario per chiamare la funzione [**ImpersonateLoggedOnUser**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser) per rappresentare il client o per chiamare la funzione [**CreateProcessAsUser ha**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) per creare un processo che viene eseguito nel contesto di [*sicurezza*](/windows/desktop/SecGloss/s-gly) del client.

Il vantaggio di autenticare il client in questo modo è che il server che rappresenta il client autenticato o un [*processo*](/windows/desktop/SecGloss/p-gly) creato nel contesto del client autenticato può connettersi alle risorse di rete remote come client. Se l'autenticazione non viene eseguita, il server può connettersi alle risorse di rete solo se ha acquisito il nome e la password dell'account del client da passare alla funzione [**WNetAddConnection2**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection2a) .

Lo svantaggio dell'autenticazione del client in questo modo è che il server deve avere acquisito le [*credenziali*](/windows/desktop/SecGloss/c-gly) del client (nome di dominio, nome utente e password). Se un client remoto fornisce queste credenziali al server, è responsabilità del client e del server garantire che le credenziali vengano trasmesse in modo sicuro.

 

 
