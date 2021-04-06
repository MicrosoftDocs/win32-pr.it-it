---
title: Attività server HTTP
description: In genere, le attività del server HTTP vengono eseguite in un ordine specifico. ovvero, è necessario completare un'attività e l'output ottenuto prima dell'inizio dell'attività successiva.
ms.assetid: 08f8e7e9-23b9-403f-b00c-8912919d65b1
keywords:
- Attività server HTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22455dbda21aca32b26f586eed6e51cef7509af2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714584"
---
# <a name="http-server-tasks"></a>Attività server HTTP

In genere, le attività del server HTTP vengono eseguite in un ordine specifico. ovvero, è necessario completare un'attività e l'output ottenuto prima dell'inizio dell'attività successiva.

Viene creata una pagina attività per presentare il codice di esempio sulle attività specifiche eseguite da un'applicazione server HTTP. Una pagina attività è collegata al file di estensione C dell'esempio HTTP Server. Quando si installa PSDK nell'unità C: \\ di un computer locale, l'applicazione di esempio server completa viene installata in c: \\ programmi \\ Microsoft SDK \\ Samples \\ netds \\ http \\ Server.

L'elenco seguente identifica le attività del server HTTP:

-   [Inizializzare il servizio HTTP](#initialize-the-http-service)
-   [Registrare gli URL per l'ascolto](#register-the-urls-to-listen-on)
-   [Chiamare la routine per ricevere una richiesta](#call-the-routine-to-receive-a-request)
-   [Ricevi la richiesta](#receive-the-request)
-   [Gestire la richiesta HTTP](#handle-the-http-request)
-   [Invia la risposta HTTP](#send-the-http-response)
-   [Invia la risposta HTTP POST](#send-the-http-post-response)
-   [Pulire l'API del server HTTP](#clean-up-the-http-server-api)

## <a name="initialize-the-http-service"></a>Inizializzare il servizio HTTP

Il servizio HTTP viene inizializzato tramite la funzione [**HttpInitialize**](/windows/desktop/api/Http/nf-http-httpinitialize) e l'handle per la coda di richieste viene creato usando [**HttpCreateHttpHandle**](/windows/desktop/api/Http/nf-http-httpcreatehttphandle). Il server deve essere inizializzato prima di poter chiamare altre funzioni server. È necessario creare la coda di richieste prima che il servizio possa registrare gli URL per l'ascolto delle richieste HTTP in ingresso.

Per ulteriori informazioni e un esempio di codice, vedere [Initialize the http Service](http-server-sample-application.md).

## <a name="register-the-urls-to-listen-on"></a>Registrare gli URL per l'ascolto

Per l'ascolto delle richieste in ingresso da parte dell'API server HTTP, URL specifici vengono registrati con l'API chiamando la funzione [**HttpAddUrl**](/windows/desktop/api/Http/nf-http-httpaddurl) . Le richieste in ingresso che corrispondono a questi URL vengono indirizzate alla coda di richieste specificata in questa chiamata.

Per ulteriori informazioni e un esempio di codice, vedere la pagina relativa alla [registrazione degli URL per l'ascolto](http-server-sample-application.md).

## <a name="call-the-routine-to-receive-a-request"></a>Chiamare la routine per ricevere una richiesta

La funzione DoReceiveRequest alloca il buffer della richiesta, Inizializza l'ID della richiesta e avvia il ciclo per ricevere le richieste.

Per ulteriori informazioni e un esempio di codice, vedere [chiamare la routine per ricevere una richiesta](http-server-sample-application.md).

## <a name="receive-the-request"></a>Ricevi la richiesta

L'API server HTTP fornisce una struttura di richiesta per archiviare la richiesta in ingresso analizzata. Questa struttura viene allocata dall'applicazione e inizializzata quando viene ricevuta una richiesta in ingresso. L'applicazione chiama la funzione [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest) per ricevere la richiesta. Se il buffer di richiesta è troppo piccolo per ricevere la richiesta, l'applicazione può aumentare le dimensioni del buffer e chiamare di nuovo **HttpReceiveHttpRequest** per ricevere l'intera richiesta.

Per ulteriori informazioni e un esempio di codice, vedere [ricezione di una richiesta](http-server-sample-application.md).

## <a name="handle-the-http-request"></a>Gestire la richiesta HTTP

Nell'applicazione di esempio viene illustrato come gestire i verbi HTTP GET e POST Request. L'applicazione invia un errore 503 (**non \_ implementato**) se i verbi sono presenti nella richiesta che l'applicazione non gestisce.

Si noti che l'URL da utilizzare per la gestione delle richieste è l'URL elaborato contenuto nel membro **CookedUrl** della struttura della [**\_ richiesta HTTP \_ V1**](/windows/desktop/api/Http/ns-http-http_request_v1) . Non l'URL non elaborato nel membro **pRawUrl** , che è esclusivamente a scopo di rilevamento e statistica.

Per ulteriori informazioni e un esempio di codice, vedere [gestire la richiesta http](http-server-sample-application.md).

## <a name="send-the-http-response"></a>Invia la risposta HTTP

La struttura della risposta viene allocata e inizializzata con il codice di stato e una frase di motivo nella macro di risposta http di INIZIALIZZAzione \_ \_ . Un'intestazione HTTP nota viene aggiunta nella struttura della risposta nella macro dell' \_ intestazione nota Add \_ e il corpo dell'entità viene aggiunto alla risposta da un blocco di dati dalla memoria. La funzione [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) viene chiamata per inviare la risposta. In questo esempio, l'applicazione invia una semplice risposta 200 OK alla richiesta GET.

Per ulteriori informazioni e un esempio di codice, vedere [inviare una risposta http](http-server-sample-application.md).

## <a name="send-the-http-post-response"></a>Invia la risposta HTTP POST

Per la richiesta POST è necessaria una maggiore elaborazione rispetto alla richiesta GET. Il corpo dell'entità della richiesta viene ricevuto chiamando la funzione [**HttpReceiveRequestEntityBody**](/windows/desktop/api/Http/nf-http-httpreceiverequestentitybody) . L'applicazione invia la risposta e il corpo dell'entità della risposta in chiamate separate all'API del server HTTP. Le intestazioni della risposta vengono inviate con [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse). Il corpo dell'entità viene inviato in un blocco di dati da un handle di file con la funzione [**HttpSendResponseEntityBody**](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody) .

Per altre informazioni e un esempio di codice, vedere [inviare una risposta HTTP post](http-server-sample-application.md).

## <a name="clean-up-the-http-server-api"></a>Pulire l'API del server HTTP

Le operazioni di pulizia per l'API del server HTTP includono:

-   Rimozione di tutti gli URL registrati.
-   Chiusura dell'handle per la coda delle richieste.
-   Terminazione delle risorse create dall'API del server HTTP.

L'applicazione chiama la funzione [**HttpRemoveUrl**](/windows/desktop/api/Http/nf-http-httpremoveurl) per annullare la registrazione degli URL registrati dalla funzione [**HttpAddUrl**](/windows/desktop/api/Http/nf-http-httpaddurl) iniziale. L'applicazione chiama anche [**HttpTerminate**](/windows/desktop/api/Http/nf-http-httpterminate) per ogni chiamata a [**HttpInitialize**](/windows/desktop/api/Http/nf-http-httpinitialize) con le impostazioni dei flag corrispondenti. Questa chiamata termina tutte le risorse create dalla chiamata a **HttpInitialize**.

Per altre informazioni e un esempio di codice, vedere [Cleanup the HTTP Server API](http-server-sample-application.md).

 

 




