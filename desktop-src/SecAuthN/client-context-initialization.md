---
description: Inizializzazione del contesto client
ms.assetid: 0c8aad3e-e726-49ce-8fc9-94dbd60cc5cb
title: Inizializzazione del contesto client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 615ce5c157371f1ebfec685d6227bd11a1d76531
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131063"
---
# <a name="client-context-initialization"></a>Inizializzazione del contesto client

Per stabilire una connessione protetta, il client acquisisce un handle delle [*credenziali*](/windows/desktop/SecGloss/c-gly) in uscita prima di inviare una richiesta di autenticazione al server. Il server crea un contesto di sicurezza per il client dalla richiesta di autenticazione. La configurazione dell'autenticazione prevede due funzioni SSPI sul lato client:

-   [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) ottiene un riferimento alle [*credenziali*](/windows/desktop/SecGloss/c-gly)di accesso ottenute in precedenza.
-   [**InitializeSecurityContext (generale)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) crea i token di sicurezza della richiesta di autenticazione iniziale.

Il codice per questo processo può essere visualizzato nella funzione **GenClientContext** nell' [uso di SSPI con un client Windows Sockets](using-sspi-with-a-windows-sockets-client.md).

Se un programma client deve usare le credenziali in aggiunta alle proprie credenziali di accesso, ad esempio un nome utente, un nome di dominio e una password diversi, li fornisce nella chiamata [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) con una struttura di [**\_ \_ \_ identità di autenticazione WinNT sec**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) che specifica le credenziali aggiuntive. Per ulteriori informazioni sulle funzioni di credenziali, vedere [gestione delle](authentication-functions.md)credenziali.

> [!Note]  
> Il membro dei **flag** della struttura di [**\_ \_ \_ identità di autenticazione WinNT sec**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) può essere impostato su sec \_ WinNT \_ auth \_ Identity \_ ANSI quando le stringhe nella struttura sono asci o OEM. Le stringhe ANSI possono essere utilizzate con il membro dei **flag** della struttura di **\_ \_ \_ identità di autenticazione WinNT sec** impostata su sec \_ WinNT \_ auth \_ Identity \_ Unicode se vengono prima convertite in [*Unicode*](/windows/desktop/SecGloss/u-gly) tramite la funzione [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) .

 

Per avviare la prima parte dell'autenticazione, il client chiama [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) per ottenere un token di sicurezza iniziale da inviare in un messaggio di richiesta di connessione al server.

Il client utilizza le informazioni sul token di sicurezza ricevute nel descrittore del buffer di output per generare un messaggio da inviare al server. La costruzione del messaggio, in termini di posizionamento di diversi buffer e così via, fa parte del [*protocollo dell'applicazione*](/windows/desktop/SecGloss/a-gly) e deve essere riconosciuta da entrambe le parti.

Il client controlla lo stato di restituzione da [**InitializeSecurityContext (generale)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) per verificare se l'autenticazione viene completata in un'unica chiamata. Lo stato di restituzione di SEC \_ \_ continua \_ necessario indica che il protocollo di sicurezza richiede più messaggi di autenticazione. Per ulteriori informazioni sulle funzioni di contesto, vedere [gestione del contesto](authentication-functions.md).

 

 
