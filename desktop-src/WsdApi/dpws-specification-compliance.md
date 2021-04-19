---
description: Questo argomento descrive il modo in cui WSDAPI implementa la funzionalità elettiva nella specifica Device Profile for Web Services (DPWS). Viene inoltre descritta la funzionalità DPWS omessa dall'implementazione di WSDAPI.
ms.assetid: 54d51e56-8022-4696-b488-4b3a226224d8
title: Conformità della specifica DPWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ed26e57a0f7a94069e802f96f346a3a5eca67b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313670"
---
# <a name="dpws-specification-compliance"></a>Conformità della specifica DPWS

Questo argomento descrive il modo in cui WSDAPI implementa la funzionalità elettiva nella specifica [Device Profile for Web Services](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS). Viene inoltre descritta la funzionalità DPWS omessa dall'implementazione di WSDAPI.

La specifica DPWS fornisce un modo coerente per i messaggi con i dispositivi. Vengono inoltre aggiunte limitazioni e raccomandazioni specifiche che semplificano il processo di supporto dei servizi Web nell'hardware incorporato.

La specifica DPWS descrive la funzionalità elettiva usando i termini che possono o devono essere inclusi in una raccomandazione o una restrizione di implementazione specificata. La funzionalità omessa può essere una funzionalità descritta come obbligatoria nella specifica DPWS, che non è stata implementata da WSDAPI, oppure può essere una funzionalità che WSDAPI implementata in un metodo diverso da quello specificato nella specifica DPWS.

Questo argomento segue il layout della sezione DPWS per sezione. Ogni sezione descrive il modo in cui le restrizioni, i requisiti e le funzionalità elettive specifiche vengono gestiti dall'implementazione di WSDAPI. Questo argomento viene letto meglio in tandem con la specifica DPWS.

## <a name="dpws-30-messaging"></a>Messaggistica DPWS 3,0

### <a name="dpws-31-uri-formats"></a>Formati URI DPWS 3,1

Restrizioni R0025 e R0027 vincolano gli URI al numero massimo di \_ \_ ottetti. WSDAPI impone entrambe le restrizioni come specificato.

### <a name="dpws-32-udp-messaging"></a>Messaggistica UDP DPWS 3,2

Recommendation R0029 suggerisce che i pacchetti UDP di dimensioni maggiori di Maximum Transfer Unit (MTU) per UDP non devono essere inviati. WSDAPI non implementa questa raccomandazione e consente alle implementazioni di inviare e ricevere messaggi di individuazione maggiori del MTU.

### <a name="dpws-33-http-messaging"></a>Messaggistica HTTP DPWS 3,3

R0001 richiede che i servizi supportino il trasferimento in blocchi. WSDAPI accetta i dati in blocchi nei messaggi di richiesta e invierà i dati Chunked nei messaggi di richiesta.

R0012 e R0013 descrivono le parti obbligatorie dell'associazione HTTP SOAP. Per R0012, WSDAPI implementa l'associazione HTTP SOAP, ma non inizierà a leggere la risposta HTTP fino a quando WSDAPI non avrà terminato l'invio della richiesta HTTP. WSDAPI implementa il modello di scambio dei messaggi richiesto in R0013, implementa il nodo SOAP di risposta facoltativo in R0014 e non implementa la funzionalità del metodo Web facoltativo in R0015. WSDAPI supporta anche i requisiti in R0030 e R0017.

### <a name="dpws-34-soap-envelope"></a>Busta SOAP DPWS 3,4

WSDAPI supporta R0034 e impone R0003 e R0026 per impostazione predefinita. In modo più specifico, in base a R0003 e R0026, se WSDAPI riceve una busta SOAP superiore \_ alla dimensione massima della busta \_ su http, viene rifiutata e la connessione viene chiusa.

### <a name="dpws-35-ws-addressing"></a>DPWS 3,5 WS-Addressing

R0004 riflette l'uso consigliato dell'API del dispositivo in WSDAPI ed è supportato dall'API client in WSDAPI. Poiché si tratta di una raccomandazione, WSDAPI consentirà ai client e ai dispositivi di usare URI diversi dagli `urn:uuid` URI per gli endpoint del dispositivo per garantire la massima compatibilità. Poiché l'API del dispositivo in WSDAPI non rende persistente lo stato tra le inizializzazioni, spetta agli sviluppatori di applicazioni che usano l'API del dispositivo in WSDAPI per assicurarsi che R0005 e R0006 siano supportati correttamente. L'API client in WSDAPI presuppone che le identità dei dispositivi siano univoche e rese permanente e che la funzionalità di compilazione nell'API client in WSDAPI (ad esempio, PnP-X) lo richieda per poter riconoscere correttamente il dispositivo tra i riavvii del dispositivo.

R0007 consiglia di usare le proprietà di riferimento nei riferimenti agli endpoint. WSDAPI rileverà e accetterà gli endpoint con proprietà di riferimento e gli sviluppatori potranno scegliere di usarli, ma per impostazione predefinita WSDAPI non li popola negli endpoint creati. Analogamente, con R0042, quando WSDAPI crea endpoint di servizio utilizzerà un indirizzo di trasporto HTTP o HTTPS, ma non richiederà che i dispositivi usino indirizzi di trasporto HTTP o HTTPS nei propri endpoint di servizio. Il comportamento del client durante il tentativo di comunicare con un servizio che non usa HTTP o HTTPS non è definito.

In caso di errori, R0031 vincola l'endpoint di risposta e descrive l'errore da inviare se l'errore non è anonimo. WSDAPI impone all'endpoint di risposta di usare il valore corretto quando si inviano messaggi e si verifica un errore in modo corretto se WSDAPI riceve un messaggio di richiesta con l'endpoint di risposta errato. R0041 fornisce alle implementazioni l'opzione per eliminare un errore se l'endpoint di risposta non è valido. Anziché eliminare l'errore, WSDAPI invierà di nuovo l'errore sul canale di richiesta, indirizzato all'endpoint Anonimo, come "Best Effort" per comunicare con il client.

Infine, esistono due restrizioni sulle intestazioni SOAP, R0019 e R0040, entrambe WSDAPI sono conformi a e impongono i messaggi ricevuti.

### <a name="dpws-36-attachments"></a>DPWS 3,6 allegati

WSDAPI supporta gli allegati ed è conforme a R0022. WSDAPI è conforme anche a R0037. Quando si inviano allegati, WSDAPI imposta sempre la codifica di trasferimento del contenuto su "binary" per tutte le parti MIME. Tuttavia, WSDAPI non impone R0036. Il comportamento di WSDAPI quando si riceve una parte MIME con una codifica di trasferimento del contenuto non impostato su "binary" non è definito.

DPWS definisce anche le clausole di ordinamento della parte MIME. Per R0038, WSDAPI imporrà l'ordinamento delle parti e rifiuterà un messaggio MIME se la busta SOAP non è la prima parte MIME. Per R0039, WSDAPI invierà sempre la busta SOAP come prima parte MIME.

## <a name="dpws-40-discovery"></a>Individuazione DPWS 4,0

R1013 e R1001 differenziano l'individuazione dei dispositivi e l'individuazione dei servizi. WSDAPI è conforme a R1013. L'implementazione host è conforme a R1001, ma WSDAPI non impone questa raccomandazione nel client.

DPWS fornisce anche indicazioni sui tipi e sulle regole di corrispondenza degli ambiti. WSDAPI supporta tutte le regole di corrispondenza degli ambiti definite in [WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) eccetto LDAP. WSDAPI fornisce anche un modello estensibile per la definizione di regole di corrispondenza degli ambiti personalizzate, in modo da conforme a R1019. L'API di hosting fornirà sempre il `wsdp:Device` tipo di individuazione per ogni R1020, ma l'API client non richiede che sia presente. Altre applicazioni compilate in WSDAPI, ad esempio PnP-X, hanno un requisito difficile per il `wsdp:Device` tipo da presentare nell'individuazione.

Per facilitare l'individuazione e l'associazione, WSDAPI supporta R1009 e R1016. Per R1018, WSDAPI ignorerà UDP multicast non inviato all'indirizzo anonimo. R1015, R1021 e R1022 definiscono un binding HTTP per il messaggio Probe, supportato da WSDAPI come descritto.

## <a name="dpws-50-description"></a>Descrizione di DPWS 5,0

WSDAPI impone R2044 sul client. Sul lato host, WSDAPI fornirà l' `wsx:Metadata` elemento solo nel corpo della busta SOAP. R2045 consente ai dispositivi di supportare un subset della funzionalità [WS-Transfer](https://specs.xmlsoap.org/ws/2004/09/transfer/WS-Transfer.pdf) . L'API di hosting genererà sempre l' `wsa:ActionNotSupported` errore.

### <a name="dpws-51-characteristics"></a>Caratteristiche di DPWS 5,1

DPWS descrive le caratteristiche di base del dispositivo. Oltre alle limitazioni descritte in questo argomento, i limiti di lunghezza vengono definiti per stringhe e URI specifici. WSDAPI applica i limiti di lunghezza in questa DPWS sezione 5,1, prima di inviare il messaggio o dopo averne analizzato il contenuto.

DPWS descrive anche le sezioni di metadati obbligatorie e il ciclo della versione dei metadati. L'implementazione client impone la presenza di metadati ThisModel e ThisDevice. L'implementazione host gestisce anche correttamente la versione dei metadati e fornisce sempre queste sezioni, conforme a R2038, R2012, R2001, R2039, R2014 e R2002.

### <a name="dpws-52-hosting"></a>Hosting di DPWS 5,2

In questa sezione viene descritta la gerarchia dei servizi e dei metadati delle relazioni. WSDAPI non impone l'univocità di ServiceId come descritto in questa sezione sul lato client o sul lato dispositivo.

WSDAPI è conforme a R2040 ed è possibile che l'implementazione di hosting invii una risposta dei metadati senza alcuna sezione di relazione se non sono presenti servizi ospitati. L'implementazione client accetta correttamente la risposta dei metadati.

R2029 consente la presenza di più sezioni di relazione in una risposta ai metadati che WSDAPI accetterà correttamente. R2030 e R2042 descrivono la gestione della versione dei metadati, implementata correttamente nell'API di hosting.

### <a name="dpws-53-wsdl"></a>DPWS 5,3 WSDL

Se un servizio fornisce dati di Web Services Description Language (WSDL), le implementazioni client possono ottenere la definizione del servizio e modificare il servizio in tempo reale. Viene usato dai client ad associazione tardiva. L'implementazione del client WSDAPI accetterà WSDL fornito da un servizio, ma il client non lo convaliderà e il client non fornirà un modello di programmazione ad associazione tardiva. L'implementazione host può essere utilizzata per fornire WSDL, ma non è necessario che l'host esegua tale operazione perché i metadati del livello di servizio non sono gestiti dall'host stesso.

### <a name="dpws-54-ws-policy"></a>DPWS 5,4 WS-Policy

DPWS descrive le asserzioni di criteri da usare per i dispositivi. Poiché WSDAPI non fornisce e non interpreta WSDL, non è in grado di riconoscere e applicare i criteri incorporati nei dati WSDL.

## <a name="dpws-60-eventing"></a>Evento DPWS 6,0

### <a name="dpws-61-subscription"></a>Sottoscrizione di DPWS 6,1

DPWS richiede il supporto per il recapito push. WSDAPI implementa il recapito push sul lato del servizio, rispettando quindi R3009 e R3010 e accetterà solo la modalità di recapito push sul lato client. R3017 e R3018 richiedono errori specifici dal servizio se non riconoscono gli `NotifyTo` `EndTo` indirizzi o. WSDAPI non convalida questi indirizzi in anticipo e non genererà tali errori. Tuttavia, l'implementazione client rileverà correttamente questi errori. Analogamente, R3019 è facoltativo e WSDAPI non implementa questa raccomandazione, ma l'implementazione client riconoscerà correttamente il `SubscriptionEnd` messaggio e invierà una notifica all'applicazione di un errore di recapito.

### <a name="dpws-611-filtering"></a>Filtro DPWS 6.1.1

WSDAPI è conforme a R3008 e implementa il `Action` filtro. In conformità con r3011 e R3012, WSDAPI non genererà gli errori nelle condizioni indicate. WSDAPI implementa anche l'errore descritto R3020 se non riconosce le azioni sulle quali viene richiesto di filtrare.

### <a name="dpws-62-subscription-duration-and-renewal"></a>Durata e rinnovo della sottoscrizione DPWS 6,2

WSDAPI è conforme a R3005, R3006 e R3016. WSDAPI utilizzerà sempre `xs:duration` , ma accetterà `xs:dateTime` , se specificato, e quindi non emetterà l'errore facoltativo in R3013. WSDAPI supporta `GetStatus` e non emette l' `wsa:ActionNotSupported` errore per ogni R3015. WSDAPI accetta l' `wsa:ActionNotSupported` errore se un servizio risponde a una `GetStatus` richiesta.

## <a name="dpws-70-security"></a>Sicurezza di DPWS 7,0

DPWS descrive un modello di sicurezza consigliato per i dispositivi. WSDAPI non implementa tali raccomandazioni come descritto e non applica le restrizioni descritte in questa sezione, come descritto in.

## <a name="dpws-appendix-i"></a>DPWS appendice I

DPWS modifica le costanti globali da altre specifiche per adattarsi ai dispositivi. WSDAPI utilizza le costanti di questa sezione ed esegue l'override delle costanti predefinite nell'implementazione [WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) con queste costanti. Le applicazioni che utilizzano WSDAPI per WS-Discovery verranno associato alle costanti definite in DPWS e non alle costanti definite in [WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf).

 

 



