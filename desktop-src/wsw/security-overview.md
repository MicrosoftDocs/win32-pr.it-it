---
title: Cenni preliminari sulla sicurezza
description: Il Framework di sicurezza nell'API per servizi Web Windows (WWSAPI) fornisce integrità dei messaggi, riservatezza, rilevamento riproduzione e autenticazione server tramite la sicurezza del trasporto.
ms.assetid: 2681bffc-ba07-4822-b265-2bf7f95297d4
keywords:
- Panoramica della sicurezza dei servizi Web per Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 741e98ef023c0bae146b5fde582484f2dd133df6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473771"
---
# <a name="security-overview"></a>Cenni preliminari sulla sicurezza

Il Framework di sicurezza nell'API dei servizi Web Windows (WWSAPI) fornisce:

-   Integrità dei messaggi, riservatezza, rilevamento della riproduzione e autenticazione del server mediante la sicurezza del trasporto.
-   Autenticazione client, ad esempio la convalida dei token di sicurezza, l'attendibilità dei certificati e i controlli di revoca e così via utilizzando la sicurezza del messaggio SOAP o del trasporto.

## <a name="the-security-programming-model"></a>Modello di programmazione della sicurezza

La sicurezza è associata ai [canali di comunicazione](channel-layer-overview.md). La protezione di un canale prevede i passaggi seguenti.

-   Creare e inizializzare una o più [**associazioni di sicurezza**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding) appropriate per i requisiti di sicurezza dell'applicazione.
-   Creare una [**Descrizione di sicurezza**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) contenente le associazioni di sicurezza.
-   Creare un [**canale**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannel) o un [**proxy del servizio**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) (sul lato client) oppure creare un [**listener**](/windows/desktop/api/WebServices/nf-webservices-wscreatelistener) o un host del [**servizio**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) (sul lato server) passando la descrizione della sicurezza.
-   Eseguire i normali passaggi di programmazione del canale di apertura, accettazione, trasmissione, ricezione, chiusura e così via.

I messaggi inviati e ricevuti sul canale vengono protetti automaticamente dal runtime in base alla descrizione di sicurezza fornita. Facoltativamente, è possibile ottimizzare questi passaggi specificando una o più impostazioni di [sicurezza a livello di canale](security-channel-settings.md) nella descrizione della sicurezza o nelle [impostazioni di sicurezza a livello di binding](security-binding-settings.md) in un'associazione di sicurezza.

Tutte le autorizzazioni necessarie per le identità del mittente devono essere eseguite dall'applicazione utilizzando i [risultati di elaborazione della sicurezza](security-processing-results.md) associati a ogni messaggio ricevuto. I passaggi di autorizzazione non sono specificati nella descrizione della sicurezza, né vengono eseguiti automaticamente dal runtime.

Gli errori nella descrizione della sicurezza, ad esempio le associazioni non supportate, le proprietà o i campi non applicabili, la mancanza di proprietà/campi richiesti o valori di proprietà/campi non validi, causeranno un errore di creazione del canale o del listener.

## <a name="selecting-security-bindings"></a>Selezione delle associazioni di sicurezza

Quando si progetta la sicurezza per un'applicazione, la decisione principale è la selezione delle associazioni di sicurezza da includere nella descrizione della sicurezza. Di seguito sono riportate alcune linee guida per la scelta delle associazioni di sicurezza adatte allo scenario di sicurezza di un'applicazione. Un'euristica utile consiste nel comprendere innanzitutto quali tipi di credenziali di sicurezza (ad esempio [**certificati X. 509**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_credential), [**nome utente/password del dominio Windows**](/windows/desktop/api/WebServices/ns-webservices-ws_windows_integrated_auth_credential), [**nome utente/password definiti dall'applicazione**](/windows/desktop/api/WebServices/ns-webservices-ws_username_credential)) saranno disponibili per l'applicazione e quindi scegliere un'associazione di sicurezza che può utilizzare tale tipo di credenziale.

-   La sicurezza del trasporto, in cui viene applicata la sicurezza a livello di flusso di byte di trasporto (al di sotto dei limiti del messaggio SOAP), è la prima opzione da considerare.
    -   Per gli scenari Internet e per gli scenari Intranet in cui è possibile distribuire un certificato X. 509 nel server, l'applicazione può utilizzare [**l' \_ \_ associazione di \_ sicurezza \_ del trasporto WS SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding). Nell'esempio seguente viene illustrata questa opzione. Client: server [HttpClientWithSslExample](httpclientwithsslexample.md) : [HttpServerWithSslExample](httpserverwithsslexample.md).

        Se si desidera eseguire l'autenticazione client tramite l'autenticazione dell'intestazione HTTP, è possibile aggiungere un'associazione di sicurezza di autenticazione dell' [**\_ \_ intestazione \_ \_ \_ WS http**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding) per fornire tale funzionalità.

    -   Per gli scenari Intranet in cui sono appropriati i protocolli di autenticazione integrata di Windows, ad esempio Kerberos, NTLM e SPNEGO, l'applicazione può utilizzare l' [**\_ associazione di \_ \_ \_ sicurezza \_ del trasporto SSPI WS TCP**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding). Nell'esempio seguente viene illustrata questa opzione: client: [RequestReplyTcpClientWithWindowsTransportSecurityExample](requestreplytcpclientwithwindowstransportsecurityexample.md) server: [RequestReplyTcpServerWithWindowsTransportSecurityExample](requestreplytcpserverwithwindowstransportsecurityexample.md).

        Client su named pipe: [RequestReplyNamedPipesClientWithWindowsTransportSecurityExample](requestreplynamedpipesclientwithwindowstransportsecurityexample.md)

        Server su named pipe: [RequestReplyNamedPipesServerWithWindowsTransportSecurityExample](requestreplynamedpipesserverwithwindowstransportsecurityexample.md)

    -   Per gli scenari di computer locali in cui sono appropriati protocolli di autenticazione integrata di Windows, ad esempio Kerberos, NTLM e SPNEGO, l'applicazione può utilizzare l' [**\_ associazione di \_ \_ sicurezza del trasporto \_ \_ SSPI di WS TCP**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding) o l' [**associazione di sicurezza del trasporto di WS \_ NAMEDPIPE \_ SSPI \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_namedpipe_sspi_transport_security_binding). L'[**\_ associazione di \_ canale \_ WS NAMEDPIPE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) è preferibile in questi scenari perché garantisce che il traffico non lasci il computer (questa è la proprietà dell' **\_ \_ \_ associazione di canale WS NAMEDPIPE**).

-   Sicurezza in modalità mista, in cui la sicurezza del trasporto protegge la connessione e un'intestazione WS-Security nel messaggio SOAP fornisce l'autenticazione client, è l'opzione successiva da considerare. Le associazioni seguenti vengono utilizzate insieme a una delle associazioni di sicurezza del trasporto descritte nella sezione precedente.
    -   Quando il client viene autenticato da una coppia nome utente/password a livello di applicazione, l'applicazione può usare un' [**\_ associazione di sicurezza del \_ messaggio \_ \_ WS nomeutente**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding) per fornire i dati di autenticazione. Negli esempi seguenti viene illustrato l'utilizzo di questa associazione insieme a un' [**associazione di \_ \_ \_ sicurezza \_ del trasporto di WS SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding):
        -   Client: [HttpClientWithUsernameOverSslExample](httpclientwithusernameoversslexample.md)
        -   Server: [HttpServerWithUsernameOverSslExample](httpserverwithusernameoversslexample.md)
    -   Quando il client viene autenticato da un ticket Kerberos, l'applicazione può utilizzare un' [**\_ associazione di \_ \_ sicurezza del \_ \_ messaggio WS Kerberos APREQ**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) per fornire i dati di autenticazione.
    -   Quando si utilizza un [contesto di sicurezza](security-context.md), il client stabilisce innanzitutto un contesto di sicurezza con il server e quindi utilizza tale contesto per autenticare i messaggi. Per abilitare questa funzionalità, la descrizione di sicurezza deve contenere [**un' \_ \_ associazione di \_ \_ sicurezza del \_ messaggio del contesto di sicurezza WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding). Una volta stabiliti, i contesti di sicurezza possono essere trasmessi tramite token leggeri, evitando di dover inviare le credenziali client potenzialmente grandi e dispendiose in termini di calcolo con ogni messaggio.
    -   In uno scenario di [sicurezza federata](federation.md) , il client ottiene innanzitutto un token di sicurezza emesso da un servizio token di sicurezza (STS), quindi presenta il token emesso a un servizio. Lato client: per ottenere il token di sicurezza dal servizio token di sicurezza, l'applicazione può usare [**WsRequestSecurityToken**](/windows/desktop/api/WebServices/nf-webservices-wsrequestsecuritytoken). In alternativa, l'applicazione può usare una libreria del provider di token di sicurezza lato client, ad esempio CardSpace o LiveID, e quindi usare l'output per creare un token di sicurezza in locale usando [**WsCreateXmlSecurityToken**](/windows/desktop/api/WebServices/nf-webservices-wscreatexmlsecuritytoken). In entrambi i casi, una volta che il token di sicurezza è disponibile per il client, è possibile che venga presentato al servizio utilizzando una descrizione di sicurezza contenente un' [**associazione di sicurezza del \_ messaggio del \_ token \_ \_ \_ WS XML**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_token_message_security_binding). Lato server: se il token di sicurezza emesso dal servizio token di sicurezza è un token SAML, il server può usare una descrizione di sicurezza con un' [**\_ associazione di sicurezza del \_ messaggio \_ \_ WS SAML**](/windows/desktop/api/WebServices/ns-webservices-ws_saml_message_security_binding).
        > [!Note]  
        > Windows 7 e Windows Server 2008 R2: WWSAPI supporta solo [WS-Trust](http://specs.xmlsoap.org/ws/2005/02/trust/WS-Trust.pdf) e [WS-SecureConversation](http://specs.xmlsoap.org/ws/2005/02/sc/WS-SecureConversation.pdf) come definito da [Lightweight Web Services Security Profile (LWSSP)](/openspecs/windows_protocols/ms-lwssp/376af2f8-f4fe-4577-bfd5-370ac12cac2e). Per informazioni dettagliate sull'implementazione di Microsoft, vedere la sezione relativa alla [sintassi dei messaggi](/openspecs/windows_protocols/ms-lwssp/d4f0f509-e14a-47b5-81e8-ade06a51d1ed) di LWSSP.

         
-   L'ultima opzione da considerare è l'utilizzo delle associazioni di autenticazione senza l'utilizzo di un'associazione di protezione, ad esempio l' [**associazione di sicurezza del trasporto di WS \_ SSL \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding). Questo comporterà la trasmissione delle credenziali in testo non crittografato e può avere implicazioni di sicurezza. L'uso di questa opzione deve essere valutato attentamente per assicurarsi che non vi siano vulnerabilità di conseguenza. Un esempio di utilizzo potenziale consiste nello scambio di messaggi tra server back-end tramite una rete privata sicura. Le configurazioni seguenti supportano questa opzione.

    -   [**WS \_ L' \_ \_ associazione di \_ sicurezza \_ AUTH header http**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding) supporta questa opzione in tutte le configurazioni.
    -   [**WS \_ L' \_ \_ \_ associazione di sicurezza dei messaggi nomeutente**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding) supporta questa opzione nel server quando si usa http come trasporto.
    -   [**WS \_ L' \_ \_ associazione di \_ sicurezza \_ dei messaggi APREQ Kerberos**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) supporta questa opzione nel server quando si usa http come trasporto.
    -   [**WS \_ L' \_ \_ associazione di \_ sicurezza \_ del messaggio del contesto di sicurezza**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) supporta questa opzione nel server quando si usa http come trasporto.
    -   [**WS \_ L' \_ \_ \_ associazione di sicurezza dei messaggi SAML**](/windows/desktop/api/WebServices/ns-webservices-ws_saml_message_security_binding) supporta questa opzione nel server quando si usa http come trasporto.

    Per abilitare questa opzione, è necessario impostare in modo esplicito il [**\_ \_ livello di protezione WS**](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level) su un valore diverso da **WS \_ Protection \_ level \_ Sign \_ e \_ Encrypt**.

## <a name="channels-and-security"></a>Canali e sicurezza

Come indicato in precedenza, l'ambito della sicurezza è limitato ai canali. Inoltre, le operazioni sui canali vengono mappate ai passaggi di sicurezza in modo coerente in tutte le associazioni di sicurezza.

-   Channel create: il set di associazioni di sicurezza specificato nella descrizione della sicurezza viene convalidato e rimane fisso per il canale in seguito. Viene anche determinata la forma dello stack dei canali, inclusi i canali laterali da usare per le negoziazioni basate su WS-Trust.
-   Canale aperto: vengono caricate tutte le credenziali fornite come parte delle associazioni di sicurezza e vengono stabilite le sessioni di sicurezza. In generale, un canale aperto contiene lo stato di sicurezza "Live". L'apertura di un canale client specifica anche l'indirizzo endpoint del server in cui verrà eseguita l'autenticazione del server da parte del runtime.
-   Tra canale aperto e Chiudi: i messaggi possono essere inviati e ricevuti in modo sicuro durante questa fase.
-   Messaggio inviato: i token del contesto di sicurezza vengono ottenuti o rinnovati in base alle esigenze e la sicurezza viene applicata a ogni messaggio trasmesso in base alla descrizione della sicurezza. Gli errori rilevati durante l'applicazione della sicurezza vengono restituiti all'applicazione come errori di invio.
-   Ricezione di messaggi: la sicurezza viene verificata per ogni messaggio ricevuto in base alla descrizione della sicurezza. Gli eventuali errori di verifica della sicurezza dei messaggi vengono restituiti all'applicazione come errori di ricezione. Questi errori per messaggio non influiscono sullo stato del canale o sulle ricevute successive. L'applicazione può rimuovere una ricezione non riuscita e riavviare una ricezione per un altro messaggio.
-   Interruzione canale: il canale può essere interrotto in qualsiasi momento per arrestare tutte le operazioni di I/O sul canale. In caso di interruzione, il canale passerà a uno stato di errore e non consentirà ulteriori invii o riceventi. Tuttavia, il canale può comunque mantenere uno stato di sicurezza ' Live ', pertanto sarà necessario eseguire una chiusura del canale successiva per eliminare tutti gli Stati.
-   Chiusura canale: lo stato di sicurezza creato al momento dell'apertura è eliminato e le sessioni vengono disattivate. I token del contesto di sicurezza vengono annullati. Lo stack dei canali rimane, ma non contiene lo stato di sicurezza ' Live ' o le credenziali caricate.
-   Canale gratuito: lo stack dei canali creato in fase di creazione, insieme a tutte le risorse di sicurezza, viene liberato.

## <a name="security-apis"></a>API di sicurezza

La documentazione dell'API per la sicurezza è raggruppata negli argomenti seguenti.

-   [Descrizione della sicurezza](security-description.md)
    -   [Impostazioni del canale di sicurezza](security-channel-settings.md)
    -   [Associazioni di sicurezza](security-bindings.md)
        -   [Credenziali di protezione](security-credentials.md)
        -   [Impostazioni di associazione di sicurezza](security-binding-settings.md)
-   [Federazione](federation.md)
-   [Contesto di sicurezza](security-context.md)
-   [Identità endpoint](endpoint-identity.md)
-   [Risultati dell'elaborazione della sicurezza](security-processing-results.md)

## <a name="security"></a>Sicurezza

Quando si usa l'API di sicurezza WWSAPI, le applicazioni presentano diversi rischi per la sicurezza:

<dl> <dt>

<span id="Accidental_misconfiguration"></span><span id="accidental_misconfiguration"></span><span id="ACCIDENTAL_MISCONFIGURATION"></span>Errata configurazione accidentale
</dt> <dd>

WWSAPI supporta una gamma di opzioni di configurazione correlate alla sicurezza. Vedere ad esempio [**\_ \_ \_ \_ ID Proprietà associazione di sicurezza WS**](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_property_id). Alcune di queste opzioni, ad esempio la **proprietà di associazione di sicurezza WS, consentono ai \_ \_ \_ \_ \_ \_ client anonimi** di ridurre il livello predefinito di sicurezza fornito dalle diverse associazioni di sicurezza. È consigliabile valutare attentamente l'uso di tali opzioni per assicurarsi che non esistano vettori di attacco risultanti.

Inoltre, come descritto in precedenza, WWSAPI consente a un'applicazione di disabilitare intenzionalmente alcuni passaggi necessari per proteggere completamente uno scambio di messaggi, ad esempio consentendo di disabilitare la crittografia anche se le credenziali di sicurezza vengono trasmesse. Questa operazione è consentita per determinati scenari specifici e non deve essere usata per la comunicazione generale. Il [**\_ \_ livello di protezione WS**](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level) deve essere specificamente ridotto per consentire questo scenario e le applicazioni non devono modificare tale valore, a meno che non sia assolutamente necessario, in quanto in questo modo verranno disabilitati molti controlli progettati per garantire una configurazione sicura.

</dd> <dt>

<span id="Storing_confidential_information_in_memory"></span><span id="storing_confidential_information_in_memory"></span><span id="STORING_CONFIDENTIAL_INFORMATION_IN_MEMORY"></span>Archiviazione di informazioni riservate in memoria
</dt> <dd>

Le informazioni riservate, ad esempio le password, archiviate in memoria sono vulnerabili ad essere estratte da un utente malintenzionato con privilegi per mezzo, ad esempio, il file di paging. WWSAPI esegue una copia delle credenziali fornite e crittografa tale copia, lasciando i dati originali non protetti. È responsabilità dell'applicazione proteggere l'istanza originale. Inoltre, la copia crittografata viene brevemente decrittografata durante l'utilizzo, aprendo una finestra per estrarla.

</dd> <dt>

<span id="Denial_of_service"></span><span id="denial_of_service"></span><span id="DENIAL_OF_SERVICE"></span>Attacco Denial of Service
</dt> <dd>

L'elaborazione della sicurezza può utilizzare risorse significative. Ogni ulteriore binding di sicurezza aumenta tali costi. WWSAPI interrompe l'elaborazione della sicurezza non appena viene rilevato un errore di verifica della sicurezza, ma alcuni controlli, ad esempio le decisioni di autorizzazione, potrebbero non avvenire finché non vengono eseguite operazioni significative.

Mentre un messaggio viene elaborato sul server, lo stato di sicurezza viene archiviato nell'heap dei messaggi. L'applicazione può limitare il consumo di memoria durante l'elaborazione della sicurezza, riducendo le dimensioni dell'heap tramite le \_ proprietà dell'heap delle proprietà del messaggio WS \_ \_ \_ . Inoltre, alcune associazioni di sicurezza, ad esempio l' \_ associazione di sicurezza del messaggio del contesto di sicurezza WS, \_ \_ \_ \_ possono causare l'allocazione delle risorse per conto del client da parte del server. I limiti per tali risorse possono essere configurati tramite i seguenti [**valori \_ \_ ID della \_ proprietà \_ di binding di sicurezza WS**](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_property_id) :

-   il contesto di sicurezza della proprietà del binding di sicurezza di WS \_ \_ \_ \_ \_ \_ massimo \_ \_ contesti in sospeso
-   \_contesto di sicurezza della proprietà Binding di sicurezza di WS \_ \_ \_ \_ \_ Max \_ \_ contesti attivi
-   \_intervallo di \_ \_ rinnovo del \_ contesto di sicurezza della proprietà associazione \_ \_ di sicurezza \_ WS
-   \_intervallo di \_ \_ rollover del \_ contesto di sicurezza della proprietà associazione \_ \_ di sicurezza \_ WS

L'impostazione di tali limiti su valori bassi riduce il consumo di memoria massimo, ma può causare il rifiuto dei client legittimi quando viene raggiunta la quota.

</dd> </dl>

 

 