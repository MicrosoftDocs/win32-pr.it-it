---
title: Attività del server HTTP
description: In genere, le attività del server HTTP vengono eseguite in un ordine specifico. in altri, un'attività deve essere completata e l'output ottenuto prima dell'inizio dell'attività successiva.
ms.assetid: 08f8e7e9-23b9-403f-b00c-8912919d65b1
keywords:
- Attività del server HTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d89f72074ba870981421e228b0ff271505b3fce1e30cd49e79d58463570c0b3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119830061"
---
# <a name="http-server-tasks"></a>Attività del server HTTP

In genere, le attività del server HTTP vengono eseguite in un ordine specifico. in altri, un'attività deve essere completata e l'output ottenuto prima dell'inizio dell'attività successiva.

Viene creata una pagina attività per presentare il codice di esempio sulle attività specifiche eseguite da un'applicazione server HTTP. Una pagina attività è collegata al file di estensione C dell'esempio di server HTTP. Quando si installa PSDK nell'unità C: di un computer locale, l'applicazione di esempio server completa viene installata in \\ C: \\ Programmi Microsoft SDK \\ Samples \\ \\ netds http \\ \\ server.

L'elenco seguente identifica le attività del server HTTP:

-   [Inizializzare il servizio HTTP](#initialize-the-http-service)
-   [Registrare gli URL per l'ascolto](#register-the-urls-to-listen-on)
-   [Chiamare la routine per ricevere una richiesta](#call-the-routine-to-receive-a-request)
-   [Ricevere la richiesta](#receive-the-request)
-   [Gestire la richiesta HTTP](#handle-the-http-request)
-   [Inviare la risposta HTTP](#send-the-http-response)
-   [Inviare la risposta HTTP POST](#send-the-http-post-response)
-   [Pulire l'API server HTTP](#clean-up-the-http-server-api)

## <a name="initialize-the-http-service"></a>Inizializzare il servizio HTTP

Il servizio HTTP viene inizializzato usando la [**funzione HttpInitialize**](/windows/desktop/api/Http/nf-http-httpinitialize) e l'handle per la coda di richieste viene creato tramite [**HttpCreateHttpHandle**](/windows/desktop/api/Http/nf-http-httpcreatehttphandle). Il server deve essere inizializzato prima di poter chiamare qualsiasi altra funzione del server. La coda di richieste deve essere creata prima che il servizio possa registrare gli URL per restare in ascolto delle richieste HTTP in ingresso.

Per altre informazioni e un esempio di codice, vedere [Inizializzare il servizio HTTP](http-server-sample-application.md).

## <a name="register-the-urls-to-listen-on"></a>Registrare gli URL per l'ascolto

Perché l'API del server HTTP sia in ascolto delle richieste in ingresso, url specifici vengono registrati con l'API chiamando la [**funzione HttpAddUrl.**](/windows/desktop/api/Http/nf-http-httpaddurl) Le richieste in ingresso che corrispondono a questi URL vengono indirizzate alla coda di richieste specificata in questa chiamata.

Per altre informazioni e un esempio di codice, vedere [Registrare gli URL per l'ascolto su](http-server-sample-application.md).

## <a name="call-the-routine-to-receive-a-request"></a>Chiamare la routine per ricevere una richiesta

La funzione DoReceiveRequest alloca il buffer delle richieste, inizializza l'ID richiesta e avvia il ciclo per ricevere le richieste.

Per altre informazioni e un esempio di codice, vedere [Chiamare la routine per ricevere una richiesta](http-server-sample-application.md).

## <a name="receive-the-request"></a>Ricevere la richiesta

L'API del server HTTP fornisce una struttura di richiesta per archiviare la richiesta in ingresso analizzata. Questa struttura viene allocata dall'applicazione e inizializzata quando viene ricevuta una richiesta in ingresso. L'applicazione chiama [**la funzione HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest) per ricevere la richiesta. Se il buffer delle richieste è troppo piccolo per ricevere la richiesta, l'applicazione può aumentare le dimensioni del buffer e chiamare di nuovo **HttpReceiveHttpRequest** per ricevere l'intera richiesta.

Per altre informazioni e un esempio di codice, vedere [Ricevere una richiesta](http-server-sample-application.md).

## <a name="handle-the-http-request"></a>Gestire la richiesta HTTP

L'applicazione di esempio illustra come gestire i verbi di richiesta HTTP GET e POST. L'applicazione invia un errore 503 (**NOT \_ IMPLEMENTED**) se nella richiesta sono presenti verbi non gestiti dall'applicazione.

Si noti che l'URL da usare per la gestione delle richieste è l'URL elaborato contenuto nel membro **CookedUrl** della [**struttura HTTP REQUEST \_ \_ V1.**](/windows/desktop/api/Http/ns-http-http_request_v1) Non l'URL non elaborato nel membro **pRawUrl,** che è esclusivamente a scopo statistico e di rilevamento.

Per altre informazioni e un esempio di codice, vedere [Gestire la richiesta HTTP](http-server-sample-application.md).

## <a name="send-the-http-response"></a>Inviare la risposta HTTP

La struttura della risposta viene allocata e inizializzata con il codice di stato e una frase di motivo nella macro INITIALIZE \_ HTTP \_ RESPONSE. Nella struttura della risposta della macro ADD KNOWN HEADER viene aggiunta un'intestazione HTTP nota e il corpo dell'entità viene aggiunto alla risposta da un blocco di dati \_ \_ dalla memoria. La [**funzione HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) viene chiamata per inviare la risposta. In questo esempio l'applicazione invia una semplice risposta 200 OK alla richiesta GET.

Per altre informazioni e un esempio di codice, vedere [Inviare una risposta HTTP.](http-server-sample-application.md)

## <a name="send-the-http-post-response"></a>Inviare la risposta HTTP POST

La richiesta POST richiede più elaborazione rispetto alla richiesta GET. Il corpo dell'entità richiesta viene ricevuto chiamando la [**funzione HttpReceiveRequestEntityBody.**](/windows/desktop/api/Http/nf-http-httpreceiverequestentitybody) L'applicazione invia la risposta e il corpo dell'entità di risposta in chiamate separate all'API del server HTTP. Le intestazioni di risposta vengono inviate con [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse). Il corpo dell'entità viene inviato in un blocco di dati da un handle di file con la [**funzione HttpSendResponseEntityBody.**](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody)

Per altre informazioni e un esempio di codice, vedere [Inviare una risposta HTTP POST](http-server-sample-application.md).

## <a name="clean-up-the-http-server-api"></a>Pulire l'API server HTTP

Le operazioni di pulizia per l'API server HTTP includono:

-   Rimozione di tutti gli URL registrati.
-   Chiusura dell'handle alla coda delle richieste.
-   Terminazione delle risorse create dall'API del server HTTP.

L'applicazione chiama [**la funzione HttpRemoveUrl**](/windows/desktop/api/Http/nf-http-httpremoveurl) per annullare la registrazione degli URL registrati dalla funzione [**HttpAddUrl**](/windows/desktop/api/Http/nf-http-httpaddurl) iniziale. L'applicazione chiama anche [**HttpTerminate**](/windows/desktop/api/Http/nf-http-httpterminate) per ogni chiamata a [**HttpInitialize con**](/windows/desktop/api/Http/nf-http-httpinitialize) le impostazioni del flag corrispondenti. Questa chiamata termina tutte le risorse create dalla chiamata a **HttpInitialize.**

Per altre informazioni e un esempio di codice, vedere [Pulizia dell'API server HTTP](http-server-sample-application.md).

 

 




