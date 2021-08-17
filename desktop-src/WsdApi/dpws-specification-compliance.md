---
description: Questo argomento descrive in che modo WSDAPI implementa la funzionalità facoltativa nella specifica Devices Profile for Web Services (DPWS). Descrive anche quale funzionalità DPWS è stata omessa dall'implementazione WSDAPI.
ms.assetid: 54d51e56-8022-4696-b488-4b3a226224d8
title: Conformità alle specifiche DPWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce59ba29e8e36fd5030732c0b61a2dfd164d9c887bdd9881a775c8b1ce6ec353
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130828"
---
# <a name="dpws-specification-compliance"></a>Conformità alle specifiche DPWS

Questo argomento descrive in che modo WSDAPI implementa la funzionalità facoltativa nella specifica [Devices Profile for Web Services](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS). Descrive anche quale funzionalità DPWS è stata omessa dall'implementazione WSDAPI.

La specifica DPWS fornisce un modo coerente per inviare messaggi ai dispositivi. Vengono inoltre aggiunte restrizioni e raccomandazioni specifiche che semplificano il processo di supporto dei servizi Web nell'hardware incorporato.

La specifica DPWS descrive la funzionalità elective usando i termini MAY o SHOULD in una specifica raccomandazione o restrizione di implementazione. La funzionalità omessa può essere una funzionalità descritta come REQUIRED nella specifica DPWS che non è stata implementata da WSDAPI oppure può essere una funzionalità implementata da WSDAPI in un metodo diverso da quello specificato nella specifica DPWS.

Questo argomento segue il layout della sezione DPWS per sezione. Ogni sezione descrive il modo in cui restrizioni, requisiti e funzionalità elettrificate specifici vengono gestiti dall'implementazione WSDAPI. Questo argomento è più leggibile in tandem con la specifica DPWS.

## <a name="dpws-30-messaging"></a>Messaggistica DPWS 3.0

### <a name="dpws-31-uri-formats"></a>Formati URI DPWS 3.1

Restrizioni R0025 e R0027 vincolano gli URI agli ottetti MAX \_ URI \_ SIZE. WSDAPI applica entrambe queste restrizioni come specificato.

### <a name="dpws-32-udp-messaging"></a>Messaggistica UDP DPWS 3.2

La raccomandazione R0029 suggerisce che i pacchetti UDP maggiori dell'unità di trasferimento massima (MTU) per UDP non devono essere inviati. WSDAPI non implementa questa raccomandazione e consentirà alle implementazioni di inviare e ricevere messaggi di individuazione maggiori della MTU.

### <a name="dpws-33-http-messaging"></a>Messaggistica HTTP DPWS 3.3

R0001 richiede che i servizi supportino il trasferimento in blocchi. WSDAPI accetta dati in blocchi nei messaggi di richiesta e invierà dati in blocchi nei messaggi di richiesta.

R0012 e R0013 descrivono le parti necessarie dell'associazione HTTP SOAP. Per R0012, WSDAPI implementa l'associazione HTTP SOAP, ma non inizierà a leggere la risposta HTTP fino al termine dell'invio della richiesta HTTP da parte di WSDAPI. WSDAPI implementa il modello di scambio di messaggi richiesto in R0013, implementa il nodo SOAP di risposta facoltativo in R0014 e non implementa la funzionalità facoltativa del metodo Web in R0015. WSDAPI supporta anche i requisiti in R0030 e R0017.

### <a name="dpws-34-soap-envelope"></a>DPWS 3.4 SOAP Envelope

WSDAPI supporta R0034 e applica R0003 e R0026 per impostazione predefinita. In particolare, in conformità con R0003 e R0026, se WSDAPI riceve una soap envelope maggiore di MAX ENVELOPE SIZE su HTTP viene rifiutata e la connessione viene \_ \_ chiusa.

### <a name="dpws-35-ws-addressing"></a>DPWS 3.5 WS-Addressing

R0004 riflette l'uso consigliato dell'API del dispositivo in WSDAPI ed è supportato dall'API client in WSDAPI. Poiché si tratta di una raccomandazione, WSDAPI consentirà a client e dispositivi di usare URI diversi dagli URI per gli endpoint del dispositivo per garantire la massima `urn:uuid` compatibilità. Poiché l'API del dispositivo in WSDAPI non rende persistente lo stato tra le inizializzazioni, gli sviluppatori di applicazioni che usano l'API del dispositivo in WSDAPI garantiscono che R0005 e R0006 siano supportati correttamente. L'API client in WSDAPI presuppone che le identità del dispositivo siano univoche e persistenti e la funzionalità basata sull'API client in WSDAPI (ad esempio PnP-X) lo richiederà per riconoscere correttamente il dispositivo tra i riavvii del dispositivo.

R0007 consiglia l'uso di proprietà di riferimento nei riferimenti all'endpoint. WSDAPI riconoscerà e accetterà comunque gli endpoint con proprietà di riferimento e gli sviluppatori possono scegliere di usarli, ma per impostazione predefinita WSDAPI non li popola negli endpoint creati. Analogamente, con R0042, quando WSDAPI crea endpoint di servizio, userà un indirizzo di trasporto HTTP o HTTPS, ma non richiederà che i dispositivi usino indirizzi di trasporto HTTP o HTTPS negli endpoint di servizio. Il comportamento del client quando si tenta di comunicare con un servizio che non usa HTTP o HTTPS non è definito.

In caso di errori, R0031 vincola l'endpoint di risposta e descrive l'errore da inviare se l'errore non è anonimo. WSDAPI forza l'endpoint di risposta a usare il valore corretto durante l'invio di messaggi e avrà un errore corretto se WSDAPI riceve un messaggio di richiesta con l'endpoint di risposta non corretto. R0041 offre alle implementazioni la possibilità di eliminare un errore se l'endpoint di risposta non è valido. Anziché eliminare l'errore, WSDAPI invierà nuovamente l'errore sul canale di richiesta, indirizzato all'endpoint anonimo, come "sforzo migliore" per comunicare con il client.

Infine, esistono due restrizioni sulle intestazioni SOAP, R0019 e R0040, entrambe che WSDAPI è conforme e applica ai messaggi ricevuti.

### <a name="dpws-36-attachments"></a>Allegati DPWS 3.6

WSDAPI supporta gli allegati e è conforme a R0022. WSDAPI è conforme anche a R0037. Quando si inviano allegati, WSDAPI imposta sempre la codifica per il trasferimento del contenuto su "binaria" per tutte le parti MIME. Tuttavia, WSDAPI non applica R0036. Il comportamento di WSDAPI quando si riceve una parte MIME con una codifica di trasferimento del contenuto non impostata su "binary" non è definito.

DPWS definisce anche le clausole di ordinamento delle parti MIME. Per R0038, WSDAPI implicherà l'ordinamento delle parti e rifiuterà un messaggio MIME se la soap envelope non è la prima parte MIME. Per R0039, WSDAPI invierà sempre la soap envelope come prima parte MIME.

## <a name="dpws-40-discovery"></a>Individuazione DPWS 4.0

R1013 e R1001 differenziano l'individuazione dei dispositivi e l'individuazione dei servizi. WSDAPI è conforme a R1013. L'implementazione dell'hosting è conforme a R1001, ma WSDAPI non applica questa raccomandazione al client.

DPWS fornisce anche indicazioni sui tipi e sulle regole di corrispondenza dell'ambito. WSDAPI supporta tutte le regole di corrispondenza dell'ambito definite in [WS-Discovery,](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) ad eccezione di LDAP. WSDAPI fornisce anche un modello estendibile per la definizione di regole di corrispondenza dell'ambito personalizzate, conformemente a R1019. L'API di hosting fornirà sempre il tipo di individuazione `wsdp:Device` per R1020, ma l'API client non lo richiede. Altre applicazioni create su WSDAPI, ad esempio PnP-X, presentano un requisito difficile per il tipo `wsdp:Device` da presentare nell'individuazione.

Per facilitare l'individuazione e l'associazione, WSDAPI supporta R1009 e R1016. Per R1018, WSDAPI ignorerà udp multicast non inviato all'indirizzo anonimo. R1015, R1021 e R1022 definiscono un'associazione HTTP per il messaggio Probe, che WSDAPI supporta come descritto.

## <a name="dpws-50-description"></a>Descrizione di DPWS 5.0

WSDAPI applica R2044 al client. Sul lato hosting, WSDAPI fornirà solo l'elemento `wsx:Metadata` nel corpo della soap envelope. R2045 consente ai dispositivi di supportare un subset della [funzionalità WS-Transfer.](https://specs.xmlsoap.org/ws/2004/09/transfer/WS-Transfer.pdf) L'API di hosting genererà sempre `wsa:ActionNotSupported` l'errore.

### <a name="dpws-51-characteristics"></a>Caratteristiche di DPWS 5.1

DPWS descrive le caratteristiche di base per il dispositivo. Oltre alle restrizioni descritte in questo argomento, i limiti di lunghezza sono definiti per stringhe e URI specifici. WSDAPI applica i limiti di lunghezza in questa sezione DPWS 5.1, prima di inviare il messaggio o dopo l'analisi del contenuto.

DPWS descrive anche le sezioni dei metadati necessarie e il ciclo della versione dei metadati. L'implementazione client impone la presenza dei metadati ThisModel e ThisDevice. L'implementazione dell'hosting gestisce anche correttamente la versione dei metadati e fornisce sempre queste sezioni, conformi a R2038, R2012, R2001, R2039, R2014 e R2002.

### <a name="dpws-52-hosting"></a>DPWS 5.2 Hosting

In questa sezione viene descritta la gerarchia dei servizi e dei metadati delle relazioni. WSDAPI non applica l'univocità di ServiceId come descritto in questa sezione sul lato client o dispositivo.

WSDAPI è conforme a R2040 ed è possibile che l'implementazione dell'hosting invii una risposta ai metadati senza alcuna sezione di relazione se non sono presenti servizi ospitati. L'implementazione client accetta correttamente la risposta dei metadati.

R2029 consente più sezioni di relazione in una risposta ai metadati, che WSDAPI accetterà correttamente. R2030 e R2042 descrivono la gestione della versione dei metadati, implementata correttamente nell'API di hosting.

### <a name="dpws-53-wsdl"></a>DPWS 5.3 WSDL

Se un servizio fornisce Web Services Description Language (WSDL), le implementazioni client possono ottenere la definizione del servizio e modificare il servizio in tempo reale. Viene usato dai client ad associazione tardiva. L'implementazione del client WSDAPI accetterà WSDL fornito da un servizio, ma il client non lo convalida e il client non fornisce un modello di programmazione ad associazione tardiva. L'implementazione dell'hosting può essere usata per fornire WSDL, ma l'host non è necessario perché i metadati del livello di servizio non sono gestiti dall'host stesso.

### <a name="dpws-54-ws-policy"></a>DPWS 5.4 WS-Policy

DPWS descrive le asserzioni di criteri da usare per i dispositivi. Poiché WSDAPI non fornisce e non interpreta WSDL, non può riconoscere e applicare i criteri incorporati nei dati WSDL.

## <a name="dpws-60-eventing"></a>Eventi DPWS 6.0

### <a name="dpws-61-subscription"></a>Sottoscrizione di DPWS 6.1

DPWS richiede il supporto per il recapito push. WSDAPI implementa il recapito push sul lato servizio, rispettando in tal modo R3009 e R3010, e accetterà solo la modalità di recapito push sul lato client. R3017 e R3018 richiedono errori specifici dal servizio se non riconosce gli `NotifyTo` indirizzi o `EndTo` . WSDAPI non convalida questi indirizzi in anticipo e non genera questi errori. Tuttavia, l'implementazione del client riconoscerà correttamente questi errori. Analogamente, R3019 è facoltativo e WSDAPI non implementa questa raccomandazione, ma l'implementazione del client riconoscerà correttamente il messaggio e comunicherà all'applicazione un errore `SubscriptionEnd` di recapito.

### <a name="dpws-611-filtering"></a>Filtro DPWS 6.1.1

WSDAPI è conforme a R3008 e implementa il `Action` filtro. In conformità con R3011 e R3012, WSDAPI non genererà gli errori nelle condizioni dichiarate. WSDAPI implementa anche l'errore R3020 descritto se non riconosce le azioni in base alle quali viene richiesto di filtrare.

### <a name="dpws-62-subscription-duration-and-renewal"></a>Durata e rinnovo della sottoscrizione di DPWS 6.2

WSDAPI è conforme a R3005, R3006 e R3016. WSDAPI userà sempre , ma accetterà se specificato e pertanto non riemettere l'errore `xs:duration` `xs:dateTime` facoltativo in R3013. WSDAPI supporta `GetStatus` e non emettere `wsa:ActionNotSupported` l'errore per R3015. WSDAPI accetta `wsa:ActionNotSupported` l'errore se un servizio risponde a `GetStatus` una richiesta con esso.

## <a name="dpws-70-security"></a>Sicurezza di DPWS 7.0

DPWS descrive un modello di sicurezza consigliato per i dispositivi. WSDAPI non implementa queste raccomandazioni come descritto e non applica le restrizioni descritte in questa sezione.

## <a name="dpws-appendix-i"></a>Appendice I di DPWS

DPWS modifica le costanti globali di altre specifiche per adattare i dispositivi. WSDAPI usa le costanti di questa sezione ed esegue l'override delle costanti predefinite nell'implementazione [di WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) con queste costanti. Le applicazioni che usano WSDAPI per WS-Discovery verranno associate alle costanti definite in DPWS, non alle costanti definite in [WS-Discovery.](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf)

 

 



