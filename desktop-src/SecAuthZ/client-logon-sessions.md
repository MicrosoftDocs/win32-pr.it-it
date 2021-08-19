---
description: Un server con il privilegio edizione Standard TCB NAME, ad esempio un servizio Windows in esecuzione nell'account LocalSystem, può chiamare la funzione LogonUser per autenticare un client nel computer in cui è in esecuzione il \_ \_ server.
ms.assetid: 27328497-8f04-42e8-aadd-4c33b9907b94
title: Sessioni di accesso client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baafdc46800cc5b334a5496be5502b97e18d4702bdf9b839d8431a92110c3d64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783023"
---
# <a name="client-logon-sessions"></a>Sessioni di accesso client

Un server con il privilegio edizione Standard TCB NAME, ad esempio un servizio Windows in esecuzione \_ nell'account \_ [LocalSystem,](/windows/desktop/Services/localsystem-account) [](/windows/desktop/SecGloss/a-gly) può chiamare la funzione [**LogonUser**](/windows/desktop/api/winbase/nf-winbase-logonusera) per autenticare un client nel computer in cui è in esecuzione il server. La **funzione LogonUser** avvia una nuova sessione [*di*](/windows/desktop/SecGloss/s-gly) accesso e restituisce un token di [*accesso*](/windows/desktop/SecGloss/p-gly) primario che contiene le informazioni di sicurezza del client. È possibile usare questo token primario per chiamare la funzione [**ImpersonateLoggedOnUser**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser) per rappresentare il client o chiamare [](/windows/desktop/SecGloss/s-gly) la [**funzione CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) per creare un processo eseguito nel contesto di sicurezza del client.

Il vantaggio di autenticare il client in questo modo è che il server che rappresenta il client autenticato, o un processo creato nel contesto del client autenticato, può connettersi [*alle*](/windows/desktop/SecGloss/p-gly) risorse di rete remote come client. Se questa autenticazione non viene eseguita, il server può connettersi alle risorse di rete solo se ha acquisito il nome account e la password del client da passare alla [**funzione WNetAddConnection2.**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection2a)

Lo svantaggio dell'autenticazione del client in questo modo è che il server deve aver acquisito le credenziali del client [*(nome*](/windows/desktop/SecGloss/c-gly) di dominio, nome utente e password). Se un client remoto fornisce queste credenziali al server, è responsabilità del client e del server assicurarsi che le credenziali siano trasmesse in modo sicuro.

 

 
