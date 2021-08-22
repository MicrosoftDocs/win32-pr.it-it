---
description: Inizializzazione del contesto client
ms.assetid: 0c8aad3e-e726-49ce-8fc9-94dbd60cc5cb
title: Inizializzazione del contesto client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0c0f2912de57487c1f30fdac1ef40740553947b993ef6f5179a028625f132af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141184"
---
# <a name="client-context-initialization"></a>Inizializzazione del contesto client

Per stabilire una connessione protetta, il client acquisisce un handle di credenziali [*in*](/windows/desktop/SecGloss/c-gly) uscita prima di inviare una richiesta di autenticazione al server. Il server crea un contesto di sicurezza per il client dalla richiesta di autenticazione. Nella configurazione dell'autenticazione sono coinvolte due funzioni SSPI sul lato client:

-   [**AcquireCredentialsHandle ottiene**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) un riferimento alle credenziali di accesso ottenute [*in precedenza.*](/windows/desktop/SecGloss/c-gly)
-   [**InitializeSecurityContext (Generale) crea**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) i token di sicurezza della richiesta di autenticazione iniziale.

Il codice per questo processo può essere visualizzato nella funzione **GenClientContext** in [Using SSPI with a Windows Sockets Client](using-sspi-with-a-windows-sockets-client.md).

Se un programma client deve usare le credenziali oltre alle proprie credenziali di accesso, ad esempio un nome utente, un nome di dominio e una password diversi, li fornisce nella chiamata [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) con una struttura [**SEC \_ WINNT \_ AUTH \_ IDENTITY**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) che specifica le credenziali aggiuntive. Per altre informazioni sulle funzioni delle credenziali, vedere [Gestione delle credenziali](authentication-functions.md).

> [!Note]  
> Il **membro Flags** della struttura SEC [**\_ WINNT \_ AUTH \_ IDENTITY**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) può essere impostato su SEC WINNT AUTH IDENTITY ANSI quando le stringhe nella struttura sono \_ \_ \_ \_ ASCI o OEM. Le stringhe ANSI possono essere usate con il membro **Flags** della struttura **SEC \_ WINNT \_ AUTH \_ IDENTITY** impostata su SEC WINNT AUTH IDENTITY UNICODE se vengono prima convertite in Unicode usando la funzione \_ \_ \_ \_ [**MultiByteToWideChar.**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) [](/windows/desktop/SecGloss/u-gly)

 

Per avviare la prima parte dell'autenticazione, il client chiama [**InitializeSecurityContext (Generale)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) per ottenere un token di sicurezza iniziale da inviare in un messaggio di richiesta di connessione al server.

Il client usa le informazioni sul token di sicurezza ricevute nel descrittore del buffer di output per generare un messaggio da inviare al server. La costruzione del messaggio, in termini di posizionamento di vari [](/windows/desktop/SecGloss/a-gly) buffer e così via, fa parte del protocollo dell'applicazione e deve essere compresa da entrambe le parti.

Il client controlla lo stato restituito da [**InitializeSecurityContext (Generale)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) per verificare se l'autenticazione verrà completata in una singola chiamata. Lo stato restituito sec \_ I CONTINUE NEEDED indica che il protocollo di sicurezza richiede più messaggi di \_ \_ autenticazione. Per altre informazioni sulle funzioni di contesto, vedere [Gestione del contesto](authentication-functions.md).

 

 
