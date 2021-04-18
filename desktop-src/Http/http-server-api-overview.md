---
title: Panoramica dell'API del server HTTP
description: Questo argomento identifica una sequenza tipica di operazioni che usano l'API del server HTTP.
ms.assetid: 1245fd98-8370-4f1b-8c86-de9be5e678bd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c99af3e4914c5496c2adea10b3ac658f75f3018
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299644"
---
# <a name="http-server-api-overview"></a>Panoramica dell'API del server HTTP

L'elenco seguente identifica una sequenza tipica di operazioni che usano l'API del server HTTP:

-   Inizializzare l'API del server HTTP utilizzando la funzione [**HttpInitialize**](/windows/desktop/api/Http/nf-http-httpinitialize) .
-   Creare una coda di richieste usando la funzione [**HttpCreateHttpHandle**](/windows/desktop/api/Http/nf-http-httpcreatehttphandle) .
-   Registrare uno o più URL utilizzando la funzione [**HttpAddUrl**](/windows/desktop/api/Http/nf-http-httpaddurl) .
-   Ricevere le richieste in ingresso indirizzate agli URL registrati tramite la funzione [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest) e inviare risposte http per queste richieste usando la funzione [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) .
-   Opzionale Quando si invia una risposta, inviare un corpo di entità aggiuntivo utilizzando la funzione [**HttpSendResponseEntityBody**](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody) .
-   Eseguire operazioni di pulizia usando le funzioni [**HttpRemoveUrl**](/windows/desktop/api/Http/nf-http-httpremoveurl), [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) e [**HttpTerminate**](/windows/desktop/api/Http/nf-http-httpterminate) .

Nelle operazioni che usano gli URL, si noti che si tratta dell'URL elaborato contenuto nel membro **CookedUrl** della struttura della [**\_ richiesta HTTP \_ V1**](/windows/desktop/api/Http/ns-http-http_request_v1) da usare. Non l'URL non elaborato nel membro **pRawUrl** , che è esclusivamente a scopo di rilevamento e statistica.

Ogni applicazione crea una propria coda di richieste. Un'applicazione ottiene l'handle della coda di richieste da [**HttpCreateHttpHandle**](/windows/desktop/api/Http/nf-http-httpcreatehttphandle). Passa questo handle alla funzione [**HttpAddUrl**](/windows/desktop/api/Http/nf-http-httpaddurl) per aggiungere un URL alla coda di richieste. L'applicazione riceve la notifica di una richiesta in ingresso e la Recupera dalla coda delle richieste chiamando la funzione [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest) con l'handle della coda di richieste. Questa funzione può essere utilizzata per ricevere le intestazioni della richiesta o sia le intestazioni che il corpo dell'entità. [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest) restituisce anche un identificatore di richiesta (RequestId) per la richiesta ricevuta che è univoca per l'handle della richiesta.

> [!Note]  
> È responsabilità dell'applicazione esaminare tutte le intestazioni di richiesta rilevanti, incluse le intestazioni content-negotiation se vengono usate, e le richieste con esito negativo in base al contenuto dell'intestazione. L'API server HTTP garantisce che ogni riga di intestazione sia terminata correttamente e non contenga caratteri non validi.

 

Usare la funzione [**HttpReceiveRequestEntityBody**](/windows/desktop/api/Http/nf-http-httpreceiverequestentitybody) con l'handle della coda di richieste per recuperare le parti successive del corpo dell'entità di una richiesta, se presenti.

> [!Note]  
> L'API del server HTTP decodifica i messaggi in blocchi sul lato di ricezione, ma non esegue la codifica chunked sul lato di trasmissione. Se è richiesta la suddivisione in blocchi sul lato di trasmissione, l'applicazione deve implementarla. Per ulteriori informazioni sulla codifica chunked, vedere [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).

 

Usare la funzione [**HttpReceiveClientCertificate**](/windows/desktop/api/Http/nf-http-httpreceiveclientcertificate) con le applicazioni che forniscono URL usando uno schema sicuro ("**https**") per recuperare facoltativamente le informazioni sul certificato del client.

Le risposte vengono inviate con la funzione [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) . Questa funzione usa il RequestId dal Request to Send corrispondente della risposta. È possibile inviare una risposta in diverse chiamate API nel tempo chiamando la funzione [**HttpSendResponseEntityBody**](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody) con RequestId dalla richiesta originariamente ricevuta.

> [!Note]  
> Per impostazione predefinita, [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) USA "Microsoft-HTTPAPI/1.0" come intestazione "Server:". Se un'applicazione specifica un'intestazione del server in una risposta, il valore viene inserito come prima parte dell'intestazione del server, seguito da uno spazio e quindi da "Microsoft-HTTPAPI/1.0".

 

In generale, l'API server HTTP nasconde i dettagli relativi alla gestione delle connessioni e alla loro creazione e teardown dalle applicazioni. Tuttavia, un'applicazione può facoltativamente rilevare la chiusura di una connessione chiamando [**HttpWaitForDisconnect**](/windows/desktop/api/Http/nf-http-httpwaitfordisconnect).

Le applicazioni devono eseguire la pulizia attenendosi alla procedura seguente:

-   Quando l'applicazione non è in ascolto o risponde a un URL, l'URL viene rimosso tramite la funzione [**HttpRemoveURL**](/windows/desktop/api/Http/nf-http-httpremoveurl) .
-   Al termine dell'applicazione con la coda di richieste, chiudere l'handle della coda di richieste usando la funzione [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) .
-   Al termine dell'applicazione con l'API del server HTTP, chiamare la funzione [**HttpTerminate**](/windows/desktop/api/Http/nf-http-httpterminate) .

 

 