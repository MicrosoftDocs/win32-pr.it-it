---
title: Federazione
description: La federazione consente la delega dell'autorità di autorizzazione ad altri membri di una relazione.
ms.assetid: 574496df-95dc-45f7-8c42-e646aec12e69
keywords:
- Servizi Web federativi per Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45a02744c9c0a5358da35f4c31c20633c420fee9
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/12/2021
ms.locfileid: "104550121"
---
# <a name="federation"></a>Federazione

La federazione consente la delega dell'autorità di autorizzazione ad altri membri di una relazione. Si consideri, ad esempio, il problema aziendale seguente: l'azienda di produzione di auto parts Contoso Ltd desidera consentire ai dipendenti autorizzati del cliente Fabrikam Inc di accedere in modo sicuro al servizio Web per l'ordine delle parti di contoso. Una soluzione di sicurezza per questo scenario è che Contoso può configurare un meccanismo di attendibilità con Fabrikam per delegare la decisione di autorizzazione di accesso a Fabrikam. Questo processo potrebbe funzionare come segue:

-   Fabrikam, quando diventa un partner di Contoso, configura un accordo di trust con contoso. L'obiettivo di questo passaggio consiste nell'accettare il tipo di token di sicurezza e il contenuto che rappresenterà l'autorizzazione di Fabrikam e sarà accettabile per contoso. Ad esempio, è possibile che un certificato X. 509 attendibile con nome soggetto "CN = Fabrikam Inc Supplier STS" firmi un token SAML per tale SAML affinché venga accettato dal servizio Web di contoso. Inoltre, è possibile che l'attestazione di sicurezza nel token SAML emesso sia ' https://schemas.contoso.com/claims/lookup ' (per l'autorizzazione per la ricerca della parte) o ' https://schemas.contoso.com/claims/order ' (per l'autorizzazione per l'ordinamento delle parti).
-   Quando un dipendente Fabrikam utilizza l'applicazione di ordinamento delle parti interna, innanzitutto Contatta un servizio token di sicurezza (STS) all'interno di Fabrikam. Tale dipendente viene autenticato mediante il meccanismo di sicurezza interno di Fabrikam (ad indicare, nome utente/password di dominio Windows), l'autorizzazione per l'ordine delle parti viene verificata e viene emesso un token SAML di breve durata che contiene le attestazioni appropriate e firmato dal certificato X. 509 deciso in precedenza. L'applicazione di ordinamento parti Contatta quindi il servizio Contoso che presenta il token SAML emesso per autenticare ed eseguire l'attività di ordinamento.

In questo caso, il servizio token di servizio Fabrikam funge da "entità emittente" e il servizio parti di Contoso funge da "relying party". ![Diagramma che mostra un'entità emittente e un relying party in una Federazione.](images/stsmodel.png)

## <a name="federation-features"></a>Funzionalità di Federazione

Di seguito sono riportate le funzionalità di sicurezza supportate per le entità o i ruoli coinvolti in uno scenario di Federazione:

-   Lato client: per ottenere il token di sicurezza dal servizio token di sicurezza, è possibile usare la funzione [**WsRequestSecurityToken**](/windows/desktop/api/WebServices/nf-webservices-wsrequestsecuritytoken) . In alternativa, è possibile usare una libreria del provider di token di sicurezza lato client, ad esempio CardSpace o LiveID, e quindi usare l'output per creare un token di sicurezza in locale usando [**WsCreateXmlSecurityToken**](/windows/desktop/api/WebServices/nf-webservices-wscreatexmlsecuritytoken). In entrambi i casi, una volta che il client dispone di un token di sicurezza, può creare un canale per il servizio specificando l' [**associazione di sicurezza del \_ messaggio del \_ token \_ \_ \_ WS XML**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_token_message_security_binding) per presentare il token, insieme a un'associazione di sicurezza del trasporto, ad esempio l'associazione di sicurezza del [**trasporto di WS \_ SSL \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) , per proteggere il canale.
-   Lato server: in uno scenario di federazione con un servizio token di sicurezza che rilascia token SAML, il server può utilizzare l' [**\_ associazione di \_ \_ sicurezza dei \_ messaggi WS SAML**](/windows/desktop/api/WebServices/ns-webservices-ws_saml_message_security_binding), insieme a un'associazione di sicurezza del trasporto, ad esempio il binding di sicurezza del [**trasporto di WS \_ \_ \_ \_ SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) , per proteggere il canale.
-   STS-Side: si noti che il servizio token di sicurezza è un'applicazione di servizio Web e può specificare i requisiti di sicurezza per quelli che richiedono un token di sicurezza utilizzando una struttura di [**Descrizione della sicurezza**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) in fase di creazione del listener come qualsiasi altro servizio Web protetto. Può quindi analizzare i payload dei messaggi di richiesta in ingresso per convalidare le richieste di token e restituire i token emessi come payload del messaggio di risposta. Attualmente non è disponibile alcuna funzionalità per semplificare le operazioni di analisi e di emissione.

Si noti che il lato client può gestire il token di sicurezza emesso in modo generico come token di sicurezza XML senza conoscere il tipo di token o eseguire un'elaborazione specifica del tipo di token. Tuttavia, il server deve comprendere il tipo di token di sicurezza specifico per comprenderlo ed elaborarlo. I passaggi di richiesta e risposta del token di sicurezza utilizzano i costrutti definiti nella specifica WS-Trust.

## <a name="more-complex-federation-scenarios"></a>Scenari federativi più complessi

Uno scenario federativo può coinvolgere più STSs che formano una catena di Federazione. Si consideri l'esempio seguente:

-   Il client esegue l'autenticazione al servizio token di sicurezza LiveID usando un nome utente/password LiveID e ottiene un token di sicurezza T1.
-   Il client esegue l'autenticazione a STS1 usando T1 e ottiene un token di sicurezza T2.
-   Il client esegue l'autenticazione a STS2 usando T2 e ottiene un T3 del token di sicurezza.
-   Il client esegue l'autenticazione al servizio di destinazione usando T3.

Qui, LiveID STS, STS1, STS2 e S formano la catena di Federazione. Il STSs in una catena di federazione può eseguire vari ruoli per lo scenario di applicazione generale. Esempi di tali ruoli funzionali STS includono provider di identità, Decision Maker di autorizzazione, Anonymizer e Resource Manager.

## <a name="sts-request-parameters-and-metadata-exchange"></a>Parametri della richiesta STS e scambio di metadati

Affinché il client esegua una chiamata [**WsRequestSecurityToken**](/windows/desktop/api/WebServices/nf-webservices-wsrequestsecuritytoken) corretta, è necessario che conosca i parametri della chiamata (ad esempio il tipo di token e i tipi di attestazione richiesti), i requisiti di descrizione della sicurezza del canale di richiesta per il servizio token di sicurezza e l' [indirizzo dell'endpoint](endpoint-address.md) del servizio token di [**sicurezza**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) . Per determinare queste informazioni, l'applicazione client può utilizzare una delle tecniche seguenti:

-   Codificare in modo rigido le informazioni nell'applicazione come parte delle decisioni relative alla fase di progettazione.
-   Leggere queste informazioni da un file di configurazione a livello di applicazione configurato dal deployer dell'applicazione locale.
-   Consente di individuare in modo dinamico queste informazioni in fase di esecuzione utilizzando la funzionalità di [importazione dei metadati](metadata-import.md) con la struttura del [**\_ \_ \_ \_ \_ \_ vincolo di sicurezza del messaggio del token WS emesso**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint) .

Per illustrare l'uso di MEX dinamico con la Federazione, prendere in considerazione l'esempio di 3 STS sopra riportato. Il client eseguirà prima un MEX dinamico con i per ottenere informazioni su T3 (ad esempio, cosa chiedere da STS2), nonché l'indirizzo MEX dinamico STS2 (ad esempio, dove trovare STS2). Utilizzerà quindi tali informazioni per eseguire un MEX dinamico con STS2 per individuare informazioni su T2 e STS1 e così via.

Pertanto, i passaggi dinamici del MEX vengono eseguiti nell'ordine 4, 3, 2, 1 per creare la catena di Federazione e la richiesta di token e i passaggi di presentazione avvengono nell'ordine 1, 2, 3, 4 per la rimozione della catena di Federazione.

> [!Note]  
> Windows 7 e Windows Server 2008 R2: WWSAPI supporta solo [WS-Trust](https://specs.xmlsoap.org/ws/2005/02/trust/WS-Trust.pdf) e [WS-SecureConversation](https://specs.xmlsoap.org/ws/2005/02/sc/WS-SecureConversation.pdf) come definito da [Lightweight Web Services Security Profile (LWSSP)](/openspecs/windows_protocols/ms-lwssp/376af2f8-f4fe-4577-bfd5-370ac12cac2e). Per informazioni dettagliate sull'implementazione di Microsoft, vedere la sezione relativa alla [sintassi dei messaggi](/openspecs/windows_protocols/ms-lwssp/d4f0f509-e14a-47b5-81e8-ade06a51d1ed) di LWSSP.

 

 

 