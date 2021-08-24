---
title: Federazione
description: La federazione consente la delega dell'autorità di autorizzazione ad altri membri di un oggetto interprise.
ms.assetid: 574496df-95dc-45f7-8c42-e646aec12e69
keywords:
- Servizi Web federativi per Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9a902eb9469ad75e8c3c5a283284a009af11bb59b42470c91c39b1f16f83c61
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119703657"
---
# <a name="federation"></a>Federazione

La federazione consente la delega dell'autorità di autorizzazione ad altri membri di un oggetto interprise. Si consideri ad esempio il problema aziendale seguente: la società di produzione di parti auto Contoso Ltd vuole consentire ai dipendenti autorizzati del cliente Fabrikam Inc di accedere in modo sicuro al servizio Web dell'ordine delle parti di Contoso. Una soluzione di sicurezza per questo scenario è che Contoso configura un meccanismo di attendibilità con Fabrikam per delegare la decisione di autorizzazione di accesso a Fabrikam. Questo processo potrebbe funzionare come segue:

-   Fabrikam, quando diventa partner di Contoso, configura un contratto di attendibilità con Contoso. L'obiettivo di questo passaggio è concordare il tipo di token di sicurezza e il contenuto che rappresenteranno l'autorizzazione di Fabrikam e saranno accettabili per Contoso. Ad esempio, si può decidere che un certificato X.509 attendibile con nome soggetto "CN=Fabrikam Inc Supplier STS" deve firmare un token SAML per tale SAML che deve essere accettato dal servizio Web Contoso. Si può anche decidere che l'attestazione di sicurezza nel token SAML emesso deve essere ' (per l'autorizzazione di ricerca di parte) o ' ' (per l'autorizzazione https://schemas.contoso.com/claims/lookup https://schemas.contoso.com/claims/order di ordinamento in parte).
-   Quando un dipendente di Fabrikam usa l'applicazione di ordinamento delle parti interne, contatta prima un servizio token di sicurezza (STS) all'interno di Fabrikam. Tale dipendente viene autenticato usando il meccanismo di sicurezza interno di Fabrikam (ad esempio, nome utente/password del dominio Windows), viene verificata l'autorizzazione per ordinare le parti e viene emesso un token SAML di breve durata contenente le attestazioni appropriate e firmato dal certificato X.509 deciso in precedenza. L'applicazione di ordinamento delle parti contatta quindi il servizio Contoso presentando il token SAML emesso per autenticare ed eseguire l'attività di ordinamento.

In questo caso, il servizio token di sicurezza fabrikam funge da "entità emittente" e il servizio di parti di Contoso funge da "relying party". ![Diagramma che mostra una parte emittente e una relying party in una federazione.](images/stsmodel.png)

## <a name="federation-features"></a>Funzionalità di federazione

Di seguito sono riportate le funzionalità di sicurezza supportate per le parti o i ruoli coinvolti in uno scenario di federazione:

-   Lato client: per ottenere il token di sicurezza dal servizio token di sicurezza, è possibile usare la [**funzione WsRequestSecurityToken.**](/windows/desktop/api/WebServices/nf-webservices-wsrequestsecuritytoken) In alternativa, è possibile usare una libreria del provider di token di sicurezza lato client, ad esempio CardSpace o LiveID, e quindi usare il relativo output per creare in locale un token di sicurezza [**usando WsCreateXmlSecurityToken**](/windows/desktop/api/WebServices/nf-webservices-wscreatexmlsecuritytoken). In entrambi i casi, quando il client ha il token di sicurezza, può quindi creare un canale al servizio specificando [**WS \_ XML TOKEN MESSAGE SECURITY \_ \_ \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_token_message_security_binding) per presentare il token, insieme a un'associazione di sicurezza del trasporto, ad esempio [**WS SSL TRANSPORT SECURITY \_ \_ \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) per proteggere il canale.
-   Lato server: in uno scenario di federazione con un servizio token di sicurezza che eserciti token SAML, il server può usare [**WS \_ SAML MESSAGE SECURITY \_ \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_saml_message_security_binding), insieme a un'associazione di sicurezza del trasporto, ad esempio [**WS SSL TRANSPORT SECURITY \_ \_ \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) per proteggere il canale.
-   Lato STS: si noti che il servizio token di sicurezza è un'applicazione del servizio Web [](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) e può specificare i requisiti di sicurezza per coloro che richiedono un token di sicurezza tramite una struttura di descrizione della sicurezza al momento della creazione del listener come farebbe qualsiasi altro servizio Web protetto. Può quindi analizzare i payload dei messaggi di richiesta in ingresso per convalidare le richieste di token e inviare nuovamente i token rilasciati come payload dei messaggi di risposta. Attualmente non sono disponibili funzionalità che consentono di eseguire questa operazione di analisi e rilascio.

Si noti che il lato client può gestire il token di sicurezza emesso in modo generico come token di sicurezza XML senza conoscere il tipo di token o eseguire un'elaborazione specifica del tipo di token. Tuttavia, il server deve comprendere il tipo di token di sicurezza specifico per comprenderlo ed elaborarlo. I passaggi di richiesta e risposta del token di sicurezza usano i costrutti definiti nella WS-Trust specifica.

## <a name="more-complex-federation-scenarios"></a>Scenari di federazione più complessi

Uno scenario di federazione può coinvolgere più token di sicurezza che formano una catena di federazione. Si consideri l'esempio seguente:

-   Il client esegue l'autenticazione al servizio token di sicurezza LiveID usando un nome utente/password LiveID e ottiene un token di sicurezza T1.
-   Il client esegue l'autenticazione a STS1 usando T1 e ottiene un token di sicurezza T2.
-   Il client esegue l'autenticazione a STS2 usando T2 e ottiene un token di sicurezza T3.
-   Il client esegue l'autenticazione al servizio di destinazione S usando T3.

In questo caso, il servizio token di sicurezza LiveID, STS1, STS2 e S formano la catena di federazione. I servizi token di sicurezza in una catena di federazione possono eseguire vari ruoli per lo scenario generale dell'applicazione. Esempi di questi ruoli funzionali del servizio token di sicurezza includono il provider di identità, il decision maker di autorizzazione, l'anonimo e il gestore delle risorse.

## <a name="sts-request-parameters-and-metadata-exchange"></a>Parametri di richiesta e metadati del servizio token di sicurezza Exchange

Per eseguire correttamente una chiamata [**WsRequestSecurityToken,**](/windows/desktop/api/WebServices/nf-webservices-wsrequestsecuritytoken) il client deve conoscere i parametri della chiamata (ad [](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) esempio il tipo di token e i tipi di attestazione necessari), i requisiti di descrizione della sicurezza del canale della richiesta al servizio token di sicurezza e l'indirizzo [endpoint](endpoint-address.md) del servizio token di sicurezza. L'applicazione client può usare una delle tecniche seguenti per determinare queste informazioni:

-   Codificare le informazioni nell'applicazione come parte delle decisioni in fase di progettazione.
-   Leggere queste informazioni da un file di configurazione a livello di applicazione configurato dal deployer dell'applicazione locale.
-   Individuare dinamicamente queste informazioni in fase di esecuzione usando la funzionalità [di importazione](metadata-import.md) dei metadati con la [**struttura WS ISSUED TOKEN \_ MESSAGE SECURITY BINDING \_ \_ \_ \_ \_ CONSTRAINT.**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint)

Per illustrare l'uso di MEX dinamico con la federazione, si consideri l'esempio 3 STS precedente. Il client farà prima un MEX dinamico con S per ottenere informazioni su T3 (ad esempio, cosa chiedere da STS2) e l'indirizzo MEX dinamico STS2 (ad esempio, dove trovare STS2). Userà quindi queste informazioni per eseguire un MEX dinamico con STS2 per individuare informazioni su T2 e STS1 e così via.

Di conseguenza, i passaggi MEX dinamici vengono esempe nell'ordine 4, 3, 2, 1 per creare la catena di federazione e i passaggi di richiesta e presentazione del token vengono esempe nell'ordine 1, 2, 3, 4 per rimuovere la catena di federazione.

> [!Note]  
> Windows 7 e Windows Server 2008 R2: WWSAPI supporta solo [Ws-Trust](https://specs.xmlsoap.org/ws/2005/02/trust/WS-Trust.pdf) e [Ws-SecureConversation](https://specs.xmlsoap.org/ws/2005/02/sc/WS-SecureConversation.pdf) come definito da [Lightweight Web Services Security Profile (LWSSP).](/openspecs/windows_protocols/ms-lwssp/376af2f8-f4fe-4577-bfd5-370ac12cac2e) Per informazioni dettagliate sull'implementazione di Microsoft, vedere la [sezione Sintassi MESSAGE](/openspecs/windows_protocols/ms-lwssp/d4f0f509-e14a-47b5-81e8-ade06a51d1ed) di LWSSP.

 

 

 