---
title: Autenticazione (API server HTTP)
description: A partire dalla versione 2.0, l'API server HTTP esegue l'autenticazione lato server per l'applicazione.
ms.assetid: e8e41e8e-1b10-4747-b18e-763e0752ade4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4e3c35dc4e244fd51af42bb3c52d225d233364f61fc79a8127ef450e84016fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078361"
---
# <a name="authentication-http-server-api"></a>Autenticazione (API server HTTP)

Alcune applicazioni server richiedono l'autenticazione client per accedere alle risorse e alle richieste HTTP del servizio. A partire dalla versione 2.0, l'API server HTTP esegue l'autenticazione lato server per l'applicazione. Nell'API server HTTP versione 1.0, l'applicazione server doveva implementare la propria autenticazione. Alcuni vantaggi dell'autenticazione eseguita dall'API del server HTTP includono:

-   Le applicazioni possono essere eseguite con privilegi bassi, riducendo così i rischi per la sicurezza.
-   L'autenticazione viene eseguita in modalità kernel, riducendo così le transizioni dalla modalità utente alla modalità kernel durante l'autenticazione.
-   L'autenticazione eseguita in modalità kernel consente l'esecuzione di applicazioni server in account utente diversi. Nella versione 1.0, tutte le applicazioni nel computer devono essere eseguite con lo stesso account utente per l'autenticazione nel nome del principio di servizio (SPN).
-   L'handshake di autenticazione NTLM non viene reimpostato se un processo di lavoro viene riciclato mentre l'handshake è in corso.

Per sfruttare l'autenticazione della versione 2.0, l'applicazione abilita gli schemi di autenticazione che l'API del server HTTP applica agli URL per cui l'applicazione ha registrato. L'autenticazione può essere abilitata nella sessione del server o nel gruppo di URL. Il gruppo di URL eredita gli schemi di autenticazione abilitati dalla sessione del server se non ne è impostato nessuno nel gruppo di URL. L'API server HTTP supporta gli schemi seguenti:

-   Negotiate
-   NTLM
-   Digest
-   Basic

L'applicazione server può anche implementare schemi di autenticazione non supportati dall'API server HTTP. L'API del server HTTP invia richieste all'applicazione per gli schemi di autenticazione non supportati o per gli schemi che non sono stati abilitati dall'applicazione.

### <a name="enabling-authentication"></a>Abilitazione dell'autenticazione

L'applicazione server abilita e configura l'autenticazione nella sessione del server o nel gruppo DI URL con le funzioni [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) [**o HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) come indicato di seguito:

1.  L'applicazione abilita l'autenticazione specificando **HttpServerAuthenticationProperty** nel parametro *Property* di [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) [**o HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty).
2.  L'applicazione specifica i parametri di configurazione nella struttura [**HTTP \_ SERVER AUTHENTICATION \_ \_ INFO**](/windows/desktop/api/Http/ns-http-http_server_authentication_info) nel *parametro pPropertyInformation* di [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) o [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty). L'applicazione specifica gli schemi di autenticazione abilitati, se la memorizzazione nella cache delle credenziali NTLM è disabilitata e fornisce i parametri Basic e Digest nella struttura **HTTP \_ SERVER AUTHENTICATION \_ \_ INFO.**

### <a name="authentication-procedure"></a>Procedura di autenticazione

Per avviare l'autenticazione del server HTTP, l'applicazione abilita la proprietà di autenticazione prima dell'arrivo della prima richiesta nella coda delle richieste. I passaggi seguenti sono il flusso di elaborazione comune per l'autenticazione di una richiesta.

1.  L'applicazione abilita l'autenticazione. Vedere la sezione precedente "Abilitazione dell'autenticazione".
    > [!Note]  
    > Il client invia una richiesta non autenticata. L'API del server HTTP passa la richiesta all'applicazione server e consente di generare la richiesta iniziale 401. L'API del server HTTP include la [**struttura HTTP \_ REQUEST \_ AUTH \_ INFO**](/windows/desktop/api/Http/ns-http-http_request_auth_info) incorporata con la [**struttura HTTP \_ REQUEST.**](/previous-versions/windows/desktop/legacy/aa364545(v=vs.85)) Il **membro AuthStatus** indica **HttpAuthStatusNotAuthenticated**

     

2.  L'applicazione esamina il **membro AuthStatus** della struttura [**HTTP REQUEST \_ \_ AUTH \_ INFO**](/windows/desktop/api/Http/ns-http-http_request_auth_info) per determinare se la richiesta è stata autenticata. Se la richiesta non è stata autenticata, l'applicazione può eseguire la richiesta come anonima o inviare una richiesta di autenticazione 401 iniziale.
3.  Se l'applicazione gestisce la richiesta come anonima, gestisce la richiesta e invia la risposta finale all'applicazione client, proprio come se l'autenticazione non fosse coinvolta.
4.  Se invece l'applicazione richiede l'autenticazione, invia la richiesta iniziale 401 con una o più intestazioni WWW-Authenticate che indicano gli schemi disponibili al client. L'applicazione deve usare la struttura [**HTTP \_ MULTIPLE KNOWN \_ \_ HEADERS**](/windows/desktop/api/Http/ns-http-http_multiple_known_headers) per compilare il set richiesto di intestazioni quando nella risposta vengono inviate più intestazioni di autenticazione.
    > [!Note]
    >
    > Il client invia nuovamente la richiesta con l'intestazione di autorizzazione per uno schema selezionato dal set di schemi disponibili indicato dall'applicazione server nella risposta iniziale 401.
    >
    > L'API server HTTP esamina l'intestazione di autorizzazione della richiesta di autorizzazione per determinare se lo schema è abilitato. In caso contrario, l'API del server HTTP esegue l'autenticazione e gestisce tutti gli scambi di richieste/risposte provvisorie fino a quando l'handshake di autenticazione non viene finalizzato.
    >
    > Quando l'API del server HTTP completa il tentativo di autenticazione, invia la richiesta all'applicazione con i risultati del tentativo di autenticazione nella struttura [**HTTP \_ REQUEST \_ AUTH \_ INFO**](/windows/desktop/api/Http/ns-http-http_request_auth_info) restituita con la richiesta. Se il tentativo di autenticazione non riesce per uno dei motivi seguenti, l'API server HTTP non passa la richiesta all'applicazione:
    >
    > -   Se l'handshake di autenticazione ha esito negativo a causa di un errore interno dell'API del server HTTP, ad esempio un errore di allocazione della memoria, l'API server HTTP genera una risposta 503 (servizio non disponibile) e restituisce al client.
    > -   Se viene rilevata un'intestazione di autorizzazione in formato non valido, ad esempio un'intestazione senza un nome di schema o una codifica Base64 in formato non valido delle credenziali client, l'API del server HTTP genera una risposta 400 (richiesta non valida) e la invia al client.

     

5.  L'applicazione server esamina il membro **AuthStatus** della struttura [**HTTP REQUEST \_ \_ AUTH \_ INFO**](/windows/desktop/api/Http/ns-http-http_request_auth_info) per determinare se l'autenticazione ha avuto esito positivo. Quando l'autenticazione ha esito negativo, l'API del server HTTP include l'errore restituito da [AcceptSecurityContext](/previous-versions/windows/embedded/ms937012(v=msdn.10)) nel membro **SecStatus** della **struttura HTTP REQUEST \_ \_ AUTH \_ INFO.** Se il tentativo di autenticazione non riesce a causa di credenziali non valide, l'applicazione può generare un'altra richiesta 401 con l'intestazione WWW-Authenticate desiderata oppure può decidere di eseguire la richiesta come anonima.
6.  Se l'autenticazione ha esito positivo, l'applicazione usa il token fornito nella struttura [**HTTP \_ REQUEST \_ AUTH \_ INFO**](/windows/desktop/api/Http/ns-http-http_request_auth_info) per rappresentare il client e accedere alle risorse. L'handle del token di accesso restituito all'applicazione è valido purché l'ID richiesta sia valido, ovvero in genere fino a quando l'applicazione non completa la risposta alla richiesta. Il token può tuttavia scadere durante questo periodo e l'applicazione potrebbe dover inviare un'altra richiesta 401 al client.
7.  L'applicazione invia la risposta 200 OK finale e deve chiudere l'handle al token di accesso.
    > [!Note]  
    > L'API del server HTTP aggiunge i dati di autenticazione reciproca alla risposta OK finale 200, se ne è stata generata una durante l'handshake di autenticazione.

     

### <a name="ntlm-null-sessions"></a>Sessioni NTLM NULL

Si noti che una sessione NTLM NULL indicata nel contesto di sicurezza finale non viene considerata autenticata. In questo caso, la richiesta viene inviata all'applicazione con un errore HttpAuthStatusFailure nella struttura [**HTTP \_ REQUEST \_ AUTH \_ INFO**](/windows/desktop/api/Http/ns-http-http_request_auth_info) e l'applicazione può inviare un'altra richiesta 401.

### <a name="preemptive-authentication"></a>Autenticazione preventiva

In base al protocollo HTTP, dopo che il client ha stabilito l'autenticazione per una risorsa, può inviare preventivamente l'intestazione di autorizzazione corrispondente con richieste consecutive successive per la risorsa senza attendere una richiesta 401 dal server. Se lo schema indicato nell'intestazione Authorization è ancora abilitato dall'applicazione e supportato dall'API server HTTP, il server HTTP tenta l'autenticazione senza inviare la richiesta all'applicazione. Quando questo tipo di richiesta autenticata viene ricevuto dall'applicazione, può scegliere di eliminare la richiesta e rigenerare la richiesta iniziale 401 o di eseguire il servizio della richiesta come autenticata.

### <a name="mutual-authentication"></a>Autenticazione reciproca

I dati di autenticazione reciproca vengono generati quando lo schema di negoziazione viene usato durante l'handshake e viene risolto in Kerberos e il client ha richiesto l'autenticazione reciproca. I dati di autenticazione reciproca vengono inseriti automaticamente dall'API del server HTTP nella risposta OK finale 200 inviata dall'applicazione server. Per impostazione predefinita, l'API server HTTP non passa i dati di autenticazione reciproca all'applicazione server, poiché gestisce automaticamente l'invio. Tuttavia, se l'applicazione server abilita il flag ReceiveMutualAuth nella struttura [**HTTP \_ SERVER AUTHENTICATION \_ \_ INFO**](/windows/desktop/api/Http/ns-http-http_server_authentication_info) nella configurazione, i dati di autenticazione reciproca vengono passati all'applicazione nella struttura [**HTTP REQUEST \_ \_ AUTH \_ INFO**](/windows/desktop/api/Http/ns-http-http_request_auth_info) incorporata nella struttura [**HTTP \_ REQUEST autenticata.**](/previous-versions/windows/desktop/legacy/aa364545(v=vs.85)) In questo caso l'applicazione deve inviare i dati di autenticazione reciproca con la risposta 200 OK finale. Nel caso in cui più siti siano serviti da un singolo computer, tutti i siti nel computer usano le credenziali per l'account del computer locale nel dominio per l'autenticazione reciproca.

 

 
