---
description: Le applicazioni distribuite (client/server) utilizzano i pacchetti di sicurezza per ottenere connessioni autenticate e scambiare messaggi.
ms.assetid: 8f28177f-335a-4fa2-bf66-2ec1698bebec
title: Inizializzazione della modalità utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 473b06daf2e1c3612b02583d203ce4cd9afebabd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968084"
---
# <a name="user-mode-initialization"></a>Inizializzazione della modalità utente

Le applicazioni distribuite (client/server) utilizzano i [*pacchetti di sicurezza*](../secgloss/s-gly.md) per ottenere connessioni autenticate e scambiare messaggi. L'applicazione chiama le funzioni SSPI (Security Support Provider Interface) di cui è stato eseguito il mapping a [funzioni implementate da SSP/APS](authentication-functions.md)e [funzioni implementate da SSP/APS in modalità utente](authentication-functions.md). Questo mapping viene eseguito dalla DLL del provider di sicurezza (Secur32.dll o Security.dll), che può essere caricata in modo dinamico nei processi client e server. La DLL può anche essere collegata in modo statico mediante Secur32. lib. Sia la DLL che la libreria LIB sono fornite con Microsoft Windows Software Development Kit (SDK).

Il caricamento del pacchetto di protezione nel processo del client o del server viene gestito dal sistema, se la DLL SSP/AP che contiene il pacchetto di sicurezza è registrata correttamente.

Il server avvia il processo di acquisizione di una connessione protetta con un client monitorando una porta, in attesa che un client invii un messaggio. Il client avvia il processo di recupero di una connessione sicura al server chiamando la funzione SSPI [**InitializeSecurityContext (generale)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta). Questa funzione è mappata alla funzione [**SpInitLsaModeContext**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spinitlsamodecontextfn) del pacchetto di sicurezza personalizzato. **SpInitLsaModeContext** restituisce un token al client, che lo trasmette al server.

Quando riceve il token dal client, il server chiama la funzione SSPI [**AcceptSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext), che viene inviata alla funzione [**SpAcceptLsaModeContext**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spacceptlsamodecontextfn) del pacchetto di sicurezza. Se la funzione **SpAcceptLsaModeContext** ha esito positivo e non è necessaria alcuna elaborazione per stabilire il contesto di sicurezza, la funzione deve restituire lo stato \_ di esito positivo al chiamante. Se è necessaria un'elaborazione aggiuntiva, la funzione deve restituire il secondo \_ \_ e continuare a \_ essere necessario e restituire un token al server. Il server invia il token al client, che chiama di nuovo [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) .

Il ciclo chiamante può essere ripetuto con la frequenza necessaria fino a quando non viene stabilita una connessione autenticata o ha esito negativo. Durante questo processo, se la funzione [**SpAcceptLsaModeContext**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spacceptlsamodecontextfn) o [**SpInitLsaModeContext**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spinitlsamodecontextfn) ha esito positivo e non è necessaria alcuna elaborazione per stabilire il [*contesto di sicurezza*](../secgloss/s-gly.md), la funzione deve restituire lo stato \_ di esito positivo al chiamante. Se è necessaria un'elaborazione aggiuntiva, la funzione deve restituire il secondo \_ \_ e continuare a essere \_ necessario e restituire un token al chiamante, che è responsabile dell'invio.

Il protocollo implementato dal pacchetto di sicurezza determina il numero di volte in cui il ciclo viene ripetuto. Ad esempio, nei pacchetti di sicurezza che supportano l'autenticazione reciproca a tre gambe, la sequenza chiamante è la seguente:

1.  Il client ottiene un token chiamando [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta)e lo invia al server. Il server chiama [**AcceptSecurityContext (generale)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) la prima volta e restituisce un token di risposta inviato al client.
2.  Il client usa il token ricevuto dal server in una seconda chiamata a [**InitializeSecurityContext (generale)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta)e restituisce un token finale. Il client invia questo token al server.
3.  Il server riceve il token generato nel segmento 2 usato nella chiamata finale a [**AcceptSecurityContext (generale)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext).

Quando le funzioni [**SpAcceptLsaModeContext**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spacceptlsamodecontextfn) e [**SpInitLsaModeContext**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spinitlsamodecontextfn) hanno esito positivo e non è necessaria alcuna elaborazione per stabilire il contesto di sicurezza, le funzioni dovrebbero restituire lo stato \_ di esito positivo al chiamante. Inoltre, se il pacchetto di sicurezza personalizzato supporta le [funzioni implementate da SSP/APS in modalità utente](authentication-functions.md), **SpAcceptLsaModeContext** e **SpInitLsaModeContext** devono restituire **true** tramite il parametro *MappedContext* . Il valore *MappedContext* non viene restituito all'applicazione; viene intercettato dall'LSA.

Quando *MappedContext* è **true**, LSA chiama la funzione [**SPUSERMODEINITIALIZE**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spusermodeinitializefn) della dll SSP/AP. Questa funzione fornisce tabelle di puntatori alle funzioni in modalità utente implementate da ogni pacchetto di sicurezza. Viene chiamata la funzione [**SpInstanceInit**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spinstanceinitfn) di ogni pacchetto, usando le tabelle di funzione restituite da **SpUsermodeInitialize**. **SpInstanceInit** riceve una tabella di puntatori alle [funzioni LSA chiamate da SSP/APS in modalità utente](authentication-functions.md).

 

 
