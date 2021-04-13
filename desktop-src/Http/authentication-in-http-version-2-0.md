---
title: Autenticazione (API del server HTTP)
description: A partire dalla versione 2,0, l'API del server HTTP esegue l'autenticazione lato server per l'applicazione.
ms.assetid: e8e41e8e-1b10-4747-b18e-763e0752ade4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16d523df90861c83a45f67811edad243ceee5165
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104400116"
---
# <a name="authentication-http-server-api"></a>Autenticazione (API del server HTTP)

Alcune applicazioni server richiedono l'autenticazione client per accedere alle risorse e alle richieste HTTP del servizio. A partire dalla versione 2,0, l'API del server HTTP esegue l'autenticazione lato server per l'applicazione. Nell'API del server HTTP versione 1,0, l'applicazione server doveva implementare una propria autenticazione. Di seguito sono riportati alcuni vantaggi dell'autenticazione eseguita dall'API del server HTTP:

-   Le applicazioni possono essere eseguite con privilegi limitati, riducendo così i rischi per la sicurezza.
-   L'autenticazione viene eseguita in modalità kernel, riducendo così le transizioni dalla modalità utente alla modalità kernel durante l'autenticazione.
-   L'autenticazione eseguita in modalità kernel consente l'esecuzione delle applicazioni server su account utente diversi. Nella versione 1,0, tutte le applicazioni nel computer devono essere eseguite con lo stesso account utente per l'autenticazione in base al nome SPN (Service Principal Name).
-   L'handshake di autenticazione NTLM non viene reimpostato se un processo di lavoro viene riciclato durante il processo di handshake.

Per sfruttare i vantaggi dell'autenticazione della versione 2,0, l'applicazione Abilita gli schemi di autenticazione che l'API del server HTTP applica agli URL per i quali l'applicazione è stata registrata. È possibile abilitare l'autenticazione per la sessione del server o il gruppo di URL. Il gruppo URL eredita gli schemi di autenticazione abilitati dalla sessione del server se non è impostato alcun valore per il gruppo di URL. L'API server HTTP supporta gli schemi seguenti:

-   Negotiate
-   NTLM
-   Digest
-   Basic

L'applicazione server può inoltre implementare schemi di autenticazione non supportati dall'API del server HTTP. L'API server HTTP invia le richieste all'applicazione per gli schemi di autenticazione non supportati o per gli schemi che non sono stati abilitati dall'applicazione.

### <a name="enabling-authentication"></a>Abilitazione dell'autenticazione

L'applicazione server consente di abilitare e configurare l'autenticazione per la sessione del server o il gruppo di URL con le funzioni [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) o [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) come indicato di seguito:

1.  L'applicazione Abilita l'autenticazione specificando **HttpServerAuthenticationProperty** nel parametro *Property* di [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) o [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty).
2.  L'applicazione specifica i parametri di configurazione nella struttura di [**informazioni di \_ autenticazione del server \_ \_ http**](/windows/desktop/api/Http/ns-http-http_server_authentication_info) nel parametro *pPropertyInformation* di [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) o [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty). L'applicazione specifica gli schemi di autenticazione abilitati, se la memorizzazione nella cache delle credenziali NTLM è disabilitata e fornisce i parametri di base e digest nella struttura delle **\_ informazioni di \_ autenticazione \_ del server http** .

### <a name="authentication-procedure"></a>Procedura di autenticazione

Per avviare l'autenticazione del server HTTP, l'applicazione Abilita la proprietà di autenticazione prima che la prima richiesta arrivi nella coda di richieste. I passaggi seguenti sono il flusso di elaborazione comune per l'autenticazione di una richiesta.

1.  L'applicazione Abilita l'autenticazione. Vedere la sezione precedente "Abilitazione dell'autenticazione".
    > [!Note]  
    > Il client invia una richiesta non autenticata. L'API server HTTP passa la richiesta all'applicazione server e consente di generare la richiesta iniziale 401. L'API server HTTP include la struttura delle [**\_ informazioni di \_ autenticazione \_ della richiesta http**](/windows/desktop/api/Http/ns-http-http_request_auth_info) incorporata con la struttura della [**\_ richiesta http**](/previous-versions/windows/desktop/legacy/aa364545(v=vs.85)) . Il membro **AuthStatus** indica **HttpAuthStatusNotAuthenticated**

     

2.  L'applicazione esamina il membro **AuthStatus** della struttura di [**\_ informazioni di \_ autenticazione \_ della richiesta http**](/windows/desktop/api/Http/ns-http-http_request_auth_info) per determinare se la richiesta è stata autenticata. Se la richiesta non è stata autenticata, l'applicazione può servire la richiesta come anonima o inviare una richiesta di autenticazione 401 iniziale.
3.  Se l'applicazione invia la richiesta come anonima, gestisce la richiesta e Invia la risposta finale all'applicazione client, proprio come se l'autenticazione non fosse stata interrotta.
4.  Se invece l'applicazione richiede l'autenticazione, Invia la richiesta iniziale 401 con una o più intestazioni di WWW-Authenticate che indicano gli schemi disponibili per il client. L'applicazione deve usare la struttura di [**\_ \_ \_ intestazioni note multiple http**](/windows/desktop/api/Http/ns-http-http_multiple_known_headers) per compilare il set di intestazioni necessario quando nella risposta viene inviata più di un'intestazione di autenticazione.
    > [!Note]
    >
    > Il client invia nuovamente la richiesta con l'intestazione di autorizzazione per uno schema selezionato dal set di schemi disponibili indicato dall'applicazione server nella risposta iniziale 401.
    >
    > L'API server HTTP esamina l'intestazione di autorizzazione della richiesta di autorizzazione per determinare se lo schema è abilitato. In caso contrario, l'API del server HTTP esegue l'autenticazione e gestisce tutti gli scambi di richieste/401-risposte provvisori, fino alla finalizzazione dell'handshake di autenticazione.
    >
    > Quando l'API del server HTTP completa il tentativo di autenticazione, Invia la richiesta all'applicazione con i risultati del tentativo di autenticazione nella struttura delle [**\_ \_ \_ informazioni**](/windows/desktop/api/Http/ns-http-http_request_auth_info) di autenticazione della richiesta HTTP restituita con la richiesta. Se il tentativo di autenticazione ha esito negativo per uno dei motivi seguenti, l'API server HTTP non passa la richiesta all'applicazione:
    >
    > -   Se l'handshake di autenticazione ha esito negativo a causa di un errore interno dell'API del server HTTP, ad esempio un errore di allocazione della memoria, l'API del server HTTP genera una risposta 503 (servizio non disponibile) e invia nuovamente al client.
    > -   Se è stata rilevata un'intestazione di autorizzazione non valida, ad esempio un'intestazione priva di nome di schema o di una codifica Base64 con formato non valido di credenziali client, l'API del server HTTP genera una risposta 400 (richiesta non valida) e la invia nuovamente al client.

     

5.  L'applicazione server esamina il membro **AuthStatus** della struttura di [**\_ informazioni di \_ autenticazione \_ della richiesta http**](/windows/desktop/api/Http/ns-http-http_request_auth_info) per determinare se l'autenticazione è stata eseguita correttamente. Quando l'autenticazione ha esito negativo, l'API del server HTTP include l'errore restituito da [AcceptSecurityContext](/previous-versions/windows/embedded/ms937012(v=msdn.10)) nel membro **SecStatus** della struttura di **informazioni di \_ \_ autenticazione \_ della richiesta http** . Se il tentativo di autenticazione ha esito negativo a causa di credenziali non valide, l'applicazione può generare un'altra richiesta 401 con l'intestazione WWW-Authenticate desiderata oppure può decidere di servire la richiesta come anonima.
6.  Se l'autenticazione ha avuto esito positivo, l'applicazione usa il token fornito nella struttura delle [**\_ informazioni di \_ autenticazione \_ della richiesta http**](/windows/desktop/api/Http/ns-http-http_request_auth_info) per rappresentare il client e accedere alle risorse. L'handle del token di accesso restituito all'applicazione è valido purché l'ID richiesta sia valido, in genere fino a quando l'applicazione non completa la risposta alla richiesta. Il token può tuttavia scadere durante questo periodo e potrebbe essere necessario che l'applicazione invii un'altra richiesta 401 al client.
7.  L'applicazione invia la risposta finale 200 OK ed è necessario chiudere l'handle per il token di accesso.
    > [!Note]  
    > L'API server HTTP aggiunge i dati di autenticazione reciproca alla risposta finale 200 OK, se ne è stata generata una durante l'handshake di autenticazione.

     

### <a name="ntlm-null-sessions"></a>Sessioni NULL NTLM

Si noti che una sessione NTLM NULL indicata nel contesto di sicurezza finale non viene trattata come autenticata. In questo caso, la richiesta viene inviata all'applicazione con un errore HttpAuthStatusFailure nella struttura di [**\_ informazioni di \_ autenticazione \_ della richiesta http**](/windows/desktop/api/Http/ns-http-http_request_auth_info) e l'applicazione può inviare un'altra richiesta di 401.

### <a name="preemptive-authentication"></a>Autenticazione PreEmptive

Secondo il protocollo HTTP, dopo che il client ha stabilito l'autenticazione per una risorsa, può inviare preventivamente l'intestazione di autorizzazione corrispondente con le successive richieste consecutive per la risorsa senza attendere una richiesta di 401 dal server. Se lo schema indicato nell'intestazione dell'autorizzazione è ancora abilitato dall'applicazione e supportato dall'API del server HTTP, il server HTTP tenta l'autenticazione senza inviare la richiesta all'applicazione. Quando l'applicazione riceve questo tipo di richiesta autenticata, può scegliere di rimuovere la richiesta e di rigenerare la richiesta iniziale di 401 o di servizio la richiesta come autenticata.

### <a name="mutual-authentication"></a>Autenticazione reciproca

I dati di autenticazione reciproca vengono generati quando lo schema di negoziazione viene utilizzato durante l'handshake e vengono risolti in Kerberos e il client ha richiesto l'autenticazione reciproca. I dati di autenticazione reciproca vengono inseriti automaticamente dall'API del server HTTP nella risposta finale 200 OK inviata dall'applicazione server. Per impostazione predefinita, l'API server HTTP non passa i dati di autenticazione reciproca all'applicazione server, perché gestisce automaticamente l'invio. Tuttavia, se l'applicazione server Abilita il flag ReceiveMutualAuth nella struttura delle [**\_ informazioni di \_ autenticazione \_ del server http**](/windows/desktop/api/Http/ns-http-http_server_authentication_info) nella configurazione, i dati di autenticazione reciproca vengono passati all'applicazione nella struttura di informazioni di autenticazione della [**\_ richiesta \_ \_ http**](/windows/desktop/api/Http/ns-http-http_request_auth_info) incorporata con la [**\_ richiesta http**](/previous-versions/windows/desktop/legacy/aa364545(v=vs.85))autenticata. In questo caso l'applicazione deve inviare i dati di autenticazione reciproca con la risposta finale 200 OK. Nel caso in cui più siti vengono serviti da un singolo computer, tutti i siti del computer utilizzano le credenziali per l'account del computer locale nel dominio per l'autenticazione reciproca.

 

 
