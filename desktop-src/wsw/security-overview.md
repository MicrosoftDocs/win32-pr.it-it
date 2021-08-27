---
title: Cenni preliminari sulla sicurezza
description: Il framework di sicurezza in Windows API dei servizi Web (WWSAPI) fornisce integrità dei messaggi, riservatezza, rilevamento della riproduzione e autenticazione server tramite la sicurezza del trasporto.
ms.assetid: 2681bffc-ba07-4822-b265-2bf7f95297d4
keywords:
- Panoramica della sicurezza web services for Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6928afd51ded7104e909994f8b625b931da6a157e859c890066c73074ae7d16
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089441"
---
# <a name="security-overview"></a>Cenni preliminari sulla sicurezza

Il framework di sicurezza Windows'API dei servizi Web (WWSAPI) offre:

-   Integrità dei messaggi, riservatezza, rilevamento della riproduzione e autenticazione del server tramite la sicurezza del trasporto.
-   Autenticazione client, ad esempio la convalida dei token di sicurezza, i controlli di attendibilità e revoca dei certificati e così via, utilizzando la sicurezza del trasporto o dei messaggi SOAP.

## <a name="the-security-programming-model"></a>Modello di programmazione della sicurezza

La sicurezza è associata ai [canali di comunicazione](channel-layer-overview.md). La protezione di un canale è costituita dai passaggi seguenti.

-   Creare e inizializzare una o [**più associazioni di sicurezza appropriate**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding) per i requisiti di sicurezza dell'applicazione.
-   Creare una [**descrizione di sicurezza**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) contenente tali associazioni di sicurezza.
-   Creare [**un**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannel) [**proxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) del canale o del servizio (sul lato client) oppure creare un [**listener**](/windows/desktop/api/WebServices/nf-webservices-wscreatelistener) o un [**host**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) del servizio (sul lato server) passando tale descrizione di sicurezza.
-   Eseguire i normali passaggi di programmazione del canale di Apertura, Accettazione, Invio, Ricezione, Chiusura e così via.

I messaggi inviati e ricevuti sul canale vengono protetti automaticamente dal runtime in base alla descrizione di sicurezza fornita. Facoltativamente, questi passaggi possono essere ottimizzati specificando [](security-channel-settings.md) una o più impostazioni di sicurezza a livello di canale nella descrizione di sicurezza o nelle impostazioni di sicurezza a livello di associazione [in](security-binding-settings.md) un'associazione di sicurezza.

Qualsiasi autorizzazione necessaria per le identità del mittente deve essere eseguita dall'applicazione usando i risultati dell'elaborazione [della](security-processing-results.md) sicurezza associati a ogni messaggio ricevuto. I passaggi di autorizzazione non vengono specificati nella descrizione della sicurezza, né vengono eseguiti automaticamente dal runtime.

Gli errori nella descrizione della sicurezza, ad esempio associazioni non supportate, proprietà/campi inapplicabili, mancanza di proprietà/campi obbligatori o valori di proprietà/campi non validi, causeranno l'esito negativo della creazione del canale o del listener.

## <a name="selecting-security-bindings"></a>Selezione delle associazioni di sicurezza

Quando si progetta la sicurezza per un'applicazione, la decisione principale è la selezione delle associazioni di sicurezza da includere nella descrizione della sicurezza. Di seguito sono riportate alcune linee guida per la scelta delle associazioni di sicurezza adatte allo scenario di sicurezza di un'applicazione. Un'euristica utile è comprendere prima di tutto quali tipi di credenziali di sicurezza (ad esempio certificati [**X.509,**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_credential)nome [**utente/password**](/windows/desktop/api/WebServices/ns-webservices-ws_windows_integrated_auth_credential)di dominio Windows , nome [**utente/password**](/windows/desktop/api/WebServices/ns-webservices-ws_username_credential)definiti dall'applicazione) saranno disponibili per l'applicazione e quindi scegliere un'associazione di sicurezza che possa usare tale tipo di credenziale.

-   La sicurezza del trasporto, in cui la sicurezza viene applicata a livello di flusso di byte del trasporto (al di sotto dei limiti dei messaggi SOAP), è la prima opzione da considerare.
    -   Per gli scenari Internet e per gli scenari Intranet in cui un certificato X.509 può essere distribuito nel server, l'applicazione può utilizzare [**WS \_ SSL TRANSPORT SECURITY \_ \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding). Nell'esempio seguente viene illustrata questa opzione. Client: [HttpClientWithSslExample](httpclientwithsslexample.md) Server: [HttpServerWithSslExample](httpserverwithsslexample.md).

        Se si desidera l'autenticazione client tramite l'autenticazione dell'intestazione HTTP, è possibile aggiungere [**WS \_ HTTP HEADER \_ \_ AUTH SECURITY \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding) per fornire tale funzionalità.

    -   Per gli scenari Intranet Windows protocolli di autenticazione integrata, ad esempio Kerberos, NTLM e SPNEGO, l'applicazione può utilizzare [**WS \_ TCP \_ SSPI \_ TRANSPORT SECURITY \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding). L'esempio seguente illustra questa opzione: Client: [RequestReplyTcpClientWithWindowsTransportSecurityExample](requestreplytcpclientwithwindowstransportsecurityexample.md) Server: [RequestReplyTcpServerWithWindowsTransportSecurityExample](requestreplytcpserverwithwindowstransportsecurityexample.md).

        Client su named pipe: [RequestReplyNamedPipesClientWithWindowsTransportSecurityExample](requestreplynamedpipesclientwithwindowstransportsecurityexample.md)

        Server su named pipe: [RequestReplyNamedPipesServerWithWindowsTransportSecurityExample](requestreplynamedpipesserverwithwindowstransportsecurityexample.md)

    -   Per gli scenari di computer locali Windows cui sono appropriati protocolli di autenticazione integrata come Kerberos, NTLM e SPNEGO, l'applicazione può utilizzare [**WS \_ TCP \_ SSPI \_ TRANSPORT SECURITY \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding) o [**WS \_ NAMEDPIPE \_ SSPI TRANSPORT SECURITY \_ \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_namedpipe_sspi_transport_security_binding). [**WS \_ NAMEDPIPE \_ CHANNEL \_ BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) è preferibile in questi scenari perché garantisce che il traffico non lasci il computer (questa è la proprietà di **WS \_ NAMEDPIPE \_ CHANNEL \_ BINDING).**

-   La sicurezza in modalità mista, in cui la sicurezza del trasporto protegge la connessione e un'intestazione WS-Security nel messaggio SOAP fornisce l'autenticazione client, è l'opzione successiva da considerare. Le associazioni seguenti vengono utilizzate insieme a una delle associazioni di sicurezza del trasporto descritte nella sezione precedente.
    -   Quando il client viene autenticato da una coppia nome utente/password a livello di applicazione, l'applicazione può utilizzare un'associazione [**WS \_ USERNAME MESSAGE SECURITY \_ \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding) per fornire i dati di autenticazione. Negli esempi seguenti viene illustrato l'utilizzo di questa associazione in combinazione con un'associazione [**WS \_ SSL TRANSPORT \_ SECURITY \_ \_ BINDING:**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding)
        -   Client: [HttpClientWithUsernameOverSslExample](httpclientwithusernameoversslexample.md)
        -   Server: [HttpServerWithUsernameOverSslExample](httpserverwithusernameoversslexample.md)
    -   Quando il client viene autenticato da un ticket Kerberos, l'applicazione può utilizzare un'associazione [**WS \_ KERBEROS \_ APREQ \_ MESSAGE SECURITY \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) per fornire i dati di autenticazione.
    -   Quando si usa [un contesto di](security-context.md)sicurezza , il client stabilisce innanzitutto un contesto di sicurezza con il server e quindi usa tale contesto per autenticare i messaggi. Per abilitare questa funzionalità, la descrizione di sicurezza deve contenere un'associazione [**WS \_ SECURITY CONTEXT MESSAGE SECURITY \_ \_ \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding). Una volta stabiliti, i contesti di sicurezza possono essere trasmessi tramite token leggeri, evitando così di dover inviare le credenziali client potenzialmente grandi e costose dal punto di vista del calcolo con ogni messaggio.
    -   In uno scenario [di sicurezza federata,](federation.md) il client ottiene innanzitutto un token di sicurezza emesso da un servizio token di sicurezza e quindi presenta il token emesso a un servizio. Lato client: per ottenere il token di sicurezza dal servizio token di sicurezza, l'applicazione può [**usare WsRequestSecurityToken.**](/windows/desktop/api/WebServices/nf-webservices-wsrequestsecuritytoken) In alternativa, l'applicazione può usare una libreria del provider di token di sicurezza lato client, ad esempio CardSpace o LiveID, e quindi usare il relativo output per creare in locale un token di sicurezza [**usando WsCreateXmlSecurityToken**](/windows/desktop/api/WebServices/nf-webservices-wscreatexmlsecuritytoken). In entrambi i modi, quando il token di sicurezza è disponibile per il client, può essere presentato al servizio utilizzando una descrizione di sicurezza contenente un [**WS \_ XML TOKEN MESSAGE SECURITY \_ \_ \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_token_message_security_binding). Lato server: se il token di sicurezza emesso dal servizio token di sicurezza è un token SAML, il server può usare una descrizione di sicurezza con [**un'associazione WS \_ SAML MESSAGE SECURITY \_ \_ \_ BINDING.**](/windows/desktop/api/WebServices/ns-webservices-ws_saml_message_security_binding)
        > [!Note]  
        > Windows 7 e Windows Server 2008 R2: WWSAPI supporta solo [Ws-Trust](http://specs.xmlsoap.org/ws/2005/02/trust/WS-Trust.pdf) e [Ws-SecureConversation](http://specs.xmlsoap.org/ws/2005/02/sc/WS-SecureConversation.pdf) come definito da [Lightweight Web Services Security Profile (LWSSP).](/openspecs/windows_protocols/ms-lwssp/376af2f8-f4fe-4577-bfd5-370ac12cac2e) Per informazioni dettagliate sull'implementazione di Microsoft, vedere la [sezione message syntax (Sintassi dei](/openspecs/windows_protocols/ms-lwssp/d4f0f509-e14a-47b5-81e8-ade06a51d1ed) messaggi) di LWSSP.

         
-   L'opzione finale da considerare è l'uso di associazioni di autenticazione senza usare un'associazione di protezione, ad esempio [**WS \_ SSL TRANSPORT SECURITY \_ \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding). Ciò comporta la trasmissione delle credenziali in testo non crittografato e può avere implicazioni per la sicurezza. L'uso di questa opzione deve essere valutato attentamente per assicurarsi che non siano presenti vulnerabilità. Un esempio di utilizzo potenziale è lo scambio di messaggi tra server back-end su una rete privata protetta. Le configurazioni seguenti supportano questa opzione.

    -   [**WS \_ HTTP \_ HEADER \_ AUTH SECURITY \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding) supporta questa opzione in tutte le configurazioni.
    -   [**WS \_ USERNAME \_ MESSAGE \_ SECURITY \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding) supporta questa opzione nel server quando si utilizza HTTP come trasporto.
    -   [**WS \_ KERBEROS \_ APREQ \_ MESSAGE SECURITY \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) supporta questa opzione nel server quando si utilizza HTTP come trasporto.
    -   [**WS \_ SECURITY \_ CONTEXT MESSAGE SECURITY \_ \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) supporta questa opzione nel server quando si utilizza HTTP come trasporto.
    -   [**WS \_ SAML \_ MESSAGE \_ SECURITY \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_saml_message_security_binding) supporta questa opzione nel server quando si usa HTTP come trasporto.

    L'abilitazione di questa opzione richiede l'impostazione esplicita di [**WS \_ PROTECTION \_ LEVEL**](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level) su un valore diverso da **WS \_ PROTECTION LEVEL SIGN \_ AND \_ \_ \_ ENCRYPT.**

## <a name="channels-and-security"></a>Canali e sicurezza

Come indicato in precedenza, la sicurezza ha come ambito i canali. Inoltre, le operazioni del canale vengono mappate ai passaggi di sicurezza in modo coerente in tutte le associazioni di sicurezza.

-   Creazione del canale: il set di associazioni di sicurezza specificato nella descrizione di sicurezza viene convalidato e successivamente rimane fisso per il canale. Viene determinata anche la forma dello stack di canali, inclusi eventuali canali laterali da usare per WS-Trust negoziazioni basate su .
-   Channel open: vengono caricate tutte le credenziali fornite come parte delle associazioni di sicurezza e vengono stabilite sessioni di sicurezza. In generale, un canale aperto contiene lo stato di sicurezza "live". L'apertura di un canale client specifica anche l'indirizzo endpoint del server rispetto al quale verrà eseguita l'autenticazione server dal runtime.
-   Tra l'apertura e la chiusura del canale: i messaggi possono essere inviati e ricevuti in modo sicuro durante questa fase.
-   Invio di messaggi: i token del contesto di sicurezza vengono ottenuti o rinnovati in base alle esigenze e la sicurezza viene applicata a ogni messaggio trasmesso in base alla descrizione di sicurezza. Gli errori rilevati durante l'applicazione della sicurezza vengono restituiti all'applicazione come errori di invio.
-   Ricezione del messaggio: la sicurezza viene verificata in ogni messaggio ricevuto in base alla descrizione della sicurezza. Eventuali errori di verifica della sicurezza dei messaggi vengono restituiti all'applicazione come errori di ricezione. Questi errori per messaggio non influiscono sullo stato del canale o sulle successive ricevute. L'applicazione può rimuovere una ricezione non riuscita e riavviare una ricezione per un altro messaggio.
-   Interruzione del canale: il canale può essere interrotto in qualsiasi momento per interrompere tutte le attività di I/O nel canale. In caso di interruzione, il canale passa a uno stato di errore e non consente altri invii o ricevimenti. Tuttavia, il canale può comunque mantenere uno stato di sicurezza "attivo", quindi sarà necessaria una chiusura successiva del canale per eliminare tutti gli stati in modo pulito.
-   Chiusura del canale: lo stato di sicurezza creato all'apertura viene eliminato e le sessioni vengono disattese. I token del contesto di sicurezza vengono annullati. Lo stack dei canali rimane, ma non contiene lo stato di sicurezza "attivo" o le credenziali caricate.
-   Channel free :lo stack di canali creato al momento della creazione, insieme a tutte le risorse di sicurezza, viene liberato.

## <a name="security-apis"></a>API di sicurezza

La documentazione dell'API per la sicurezza è raggruppata negli argomenti seguenti.

-   [Descrizione della sicurezza](security-description.md)
    -   [Canale di sicurezza Impostazioni](security-channel-settings.md)
    -   [Associazioni di sicurezza](security-bindings.md)
        -   [Credenziali di protezione](security-credentials.md)
        -   [Impostazioni di associazione di sicurezza](security-binding-settings.md)
-   [Federazione](federation.md)
-   [Contesto di sicurezza](security-context.md)
-   [Identità endpoint](endpoint-identity.md)
-   [Risultati dell'elaborazione della sicurezza](security-processing-results.md)

## <a name="security"></a>Sicurezza

Quando si usa l'API Sicurezza WWSAPI, le applicazioni devono affrontare diversi rischi per la sicurezza:

<dl> <dt>

<span id="Accidental_misconfiguration"></span><span id="accidental_misconfiguration"></span><span id="ACCIDENTAL_MISCONFIGURATION"></span>Configurazione errata accidentale
</dt> <dd>

WWSAPI supporta una gamma di opzioni di configurazione relative alla sicurezza. Vedere per l'esempio [**WS \_ SECURITY BINDING PROPERTY \_ \_ \_ ID**](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_property_id). Alcune di queste opzioni, ad esempio **WS \_ SECURITY BINDING PROPERTY ALLOW ANONYMOUS \_ \_ \_ \_ \_ CLIENTS** consentono all'applicazione di ridurre il livello di sicurezza predefinito fornito dalle varie associazioni di sicurezza. L'uso di tali opzioni deve essere valutato attentamente per assicurarsi che non siano presenti vettori di attacco risultanti.

Inoltre, come descritto in precedenza, WWSAPI consente a un'applicazione di disabilitare deliberatamente alcuni passaggi necessari per proteggere completamente uno scambio di messaggi, ad esempio consentire la disabilitazione della crittografia anche se le credenziali di sicurezza vengono trasmesse. Ciò consente di abilitare determinati scenari specifici e non deve essere usato per la comunicazione generale. [**WS \_ PROTECTION \_ LEVEL**](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level) deve essere abbassato in modo specifico per abilitare questo scenario e le applicazioni non devono modificare tale valore a meno che non sia assolutamente necessario, perché in questo modo verranno disabilitati molti controlli progettati per garantire una configurazione sicura.

</dd> <dt>

<span id="Storing_confidential_information_in_memory"></span><span id="storing_confidential_information_in_memory"></span><span id="STORING_CONFIDENTIAL_INFORMATION_IN_MEMORY"></span>Archiviazione di informazioni riservate in memoria
</dt> <dd>

Le informazioni riservate, ad esempio le password, archiviate in memoria sono vulnerabili all'estrazione da parte di un utente malintenzionato con privilegi tramite, ad esempio, il file di pagina. WWSAPI crea una copia delle credenziali fornite e crittografa tale copia, lasciando i dati originali non protetti. È responsabilità dell'applicazione proteggere l'istanza originale. Inoltre, la copia crittografata viene brevemente decrittografata durante l'uso, aprendo una finestra per estrarla.

</dd> <dt>

<span id="Denial_of_service"></span><span id="denial_of_service"></span><span id="DENIAL_OF_SERVICE"></span>Denial of Service
</dt> <dd>

L'elaborazione della sicurezza può utilizzare risorse significative. Ogni associazione di sicurezza aggiuntiva aumenta tali costi. WWSAPI interrompe l'elaborazione della sicurezza non appena viene rilevato un errore di verifica della sicurezza, ma alcuni controlli, ad esempio le decisioni relative all'autorizzazione, possono essere eseguiti solo dopo che sono state eseguite operazioni significative.

Durante l'elaborazione di un messaggio nel server, lo stato di sicurezza viene archiviato nell'heap dei messaggi. L'applicazione può limitare l'utilizzo di memoria durante l'elaborazione della sicurezza riducendo le dimensioni dell'heap tramite WS \_ MESSAGE \_ PROPERTY HEAP \_ \_ PROPERTIES. Inoltre, alcune associazioni di sicurezza, ad esempio WS SECURITY CONTEXT MESSAGE SECURITY BINDING, possono causare l'allocazione delle risorse da parte del \_ server per conto del \_ \_ \_ \_ client. I limiti per tali risorse possono essere configurati tramite i seguenti valori di ID proprietà [**\_ WS SECURITY \_ BINDING: \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_property_id)

-   WS \_ SECURITY \_ BINDING \_ PROPERTY \_ SECURITY \_ CONTEXT \_ MAX \_ PENDING \_ CONTEXTS
-   WS \_ SECURITY \_ BINDING \_ PROPERTY \_ SECURITY \_ CONTEXT \_ MAX \_ ACTIVE \_ CONTEXTS
-   INTERVALLO DI \_ RINNOVO DEL CONTESTO DI SICUREZZA DELLE PROPRIETÀ \_ \_ \_ \_ DELL'ASSOCIAZIONE \_ DI \_ SICUREZZA WS
-   INTERVALLO DI \_ \_ ROLLOVER DEL CONTESTO \_ DI SICUREZZA DELLE PROPRIETÀ \_ \_ \_ DELL'ASSOCIAZIONE DI \_ SICUREZZA WS

L'impostazione di questi limiti su valori bassi riduce il consumo massimo di memoria, ma può causare il rifiuto di client legittimi quando viene raggiunta la quota.

</dd> </dl>

 

 