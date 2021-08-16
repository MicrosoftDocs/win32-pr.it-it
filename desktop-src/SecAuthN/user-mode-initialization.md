---
description: Le applicazioni distribuite (client/server) usano pacchetti di sicurezza per ottenere connessioni autenticate e scambiare messaggi.
ms.assetid: 8f28177f-335a-4fa2-bf66-2ec1698bebec
title: Inizializzazione in modalità utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09be7c4c00937473e2ecc3d6b01bb7c59a2842085a133f381b5a8a10bd9b215f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118915583"
---
# <a name="user-mode-initialization"></a>Inizializzazione in modalità utente

Le applicazioni distribuite (client/server) usano [*pacchetti di sicurezza*](../secgloss/s-gly.md) per ottenere connessioni autenticate e scambiare messaggi. L'applicazione chiama funzioni SSPI (Security Support Provider Interface) mappate a funzioni implementate da [SSP/APs](authentication-functions.md)e funzioni implementate da provider di servizi [condivisi/provider di](authentication-functions.md)servizi di accesso in modalità utente. Questo mapping viene eseguito dalla DLL del provider di sicurezza (Secur32.dll o Security.dll), che può essere caricata dinamicamente nei processi client e server. La DLL può anche essere collegata in modo statico usando Secur32.lib. Sia la DLL che lib vengono forniti con Microsoft Windows Software Development Kit (SDK).

Il caricamento del pacchetto di sicurezza nel processo del client o del server viene gestito dal sistema, se la DLL SSP/AP che contiene il pacchetto di sicurezza è registrata correttamente.

Il server avvia il processo di ottenimento di una connessione sicura con un client monitorando una porta, in attesa che un client invii un messaggio. Il client avvia il processo di ottenimento di una connessione sicura al server chiamando la funzione SSPI [**InitializeSecurityContext (Generale).**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) Questa funzione viene mappata alla funzione [**SpInitLsaModeContext**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spinitlsamodecontextfn) del pacchetto di sicurezza personalizzato. **SpInitLsaModeContext** restituisce un token al client, che lo inoltra al server.

Alla ricezione del token dal client, il server chiama la funzione SSPI [**AcceptSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext), che viene inviata alla funzione [**SpAcceptLsaModeContext**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spacceptlsamodecontextfn) del pacchetto di sicurezza. Se la **funzione SpAcceptLsaModeContext** ha esito positivo e non sono necessarie altre elaborazioni per stabilire il contesto di sicurezza, la funzione deve restituire STATUS \_ SUCCESS al chiamante. Se è necessaria un'ulteriore elaborazione, la funzione deve restituire SEC \_ I CONTINUE NEEDED e restituire un token al \_ \_ server. Il server inoltra il token al client, che chiama [**nuovamente InitializeSecurityContext (Generale).**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta)

Questo ciclo di chiamata può essere ripetuto con la frequenza necessaria fino a quando non viene stabilita o non viene stabilita una connessione autenticata. Durante questo processo, se la [**funzione SpAcceptLsaModeContext**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spacceptlsamodecontextfn) o [**SpInitLsaModeContext**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spinitlsamodecontextfn) ha esito positivo e non sono necessarie altre elaborazioni per stabilire il contesto di [*sicurezza,*](../secgloss/s-gly.md)la funzione deve restituire STATUS SUCCESS al \_ chiamante. Se è necessaria un'ulteriore elaborazione, la funzione deve restituire SEC I CONTINUE NEEDED e restituire un token al \_ \_ chiamante, responsabile \_ dell'inoltro.

Il protocollo implementato dal pacchetto di sicurezza determina il numero di volte in cui questo ciclo viene ripetuto. Ad esempio, nei pacchetti di sicurezza che supportano l'autenticazione reciproca a tre parti, la sequenza di chiamata è la seguente:

1.  Il client ottiene un token chiamando [**InitializeSecurityContext (Generale)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta)e lo invia al server. Il server chiama [**AcceptSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) la prima volta e ottiene un token di risposta inviato al client.
2.  Il client usa il token ricevuto dal server in una seconda chiamata a [**InitializeSecurityContext (Generale)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta)e ottiene un token finale. Il client invia questo token al server.
3.  Il server riceve il token generato nella parte 2 che usa nella chiamata finale ad [**AcceptSecurityContext (Generale).**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext)

Quando le [**funzioni SpAcceptLsaModeContext**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spacceptlsamodecontextfn) e [**SpInitLsaModeContext**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spinitlsamodecontextfn) hanno esito positivo e non sono necessarie altre elaborazioni per stabilire il contesto di sicurezza, le funzioni devono restituire STATUS SUCCESS al \_ chiamante. Inoltre, se il pacchetto di sicurezza personalizzato supporta le funzioni implementate da [SSP/APs](authentication-functions.md)in modalità utente, **SpAcceptLsaModeContext** e **SpInitLsaModeContext** devono restituire **TRUE** tramite il *parametro MappedContext.* Il *valore MappedContext* non viene passato all'applicazione. viene intercettato dall'LSA.

Quando *MappedContext è* **true,** l'LSA chiama la funzione [**SpUsermodeInitialize**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spusermodeinitializefn) della DLL SSP/AP. Questa funzione fornisce tabelle di puntatori alle funzioni in modalità utente implementate da ogni pacchetto di sicurezza. Viene chiamata la [**funzione SpInstanceInit**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spinstanceinitfn) di ogni pacchetto, usando le tabelle di funzioni restituite da **SpUsermodeInitialize**. **SpInstanceInit riceve** una tabella di puntatori alle funzioni [LSA chiamate da SSP/APs in modalità utente.](authentication-functions.md)

 

 
