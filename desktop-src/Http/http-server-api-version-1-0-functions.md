---
title: Funzioni dell'API server HTTP versione 1.0
description: L'API server HTTP fornisce le funzioni seguenti per la scrittura di applicazioni.
ms.assetid: 1da9907d-a09d-41e1-aca1-9a8e2b91296f
keywords:
- Funzioni dell'API server HTTP versione 1.0
- HTTP di Funzioni , API server HTTP versione 1.0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8520753e56e995b5751b55ff71cf49f8e82d414e702b2df255c2901e69c397fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047201"
---
# <a name="http-server-api-version-10-functions"></a>Funzioni dell'API server HTTP versione 1.0

L'API server HTTP fornisce le funzioni seguenti per la scrittura di applicazioni.

## <a name="general"></a>Generale



| Funzione                                             | Descrizione                                                                                                                       |
|------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**HttpCreateHttpHandle**](/windows/desktop/api/Http/nf-http-httpcreatehttphandle) | Crea una coda di richieste HTTP e le restituisce un handle.                                                                         |
| [**HttpInitialize**](/windows/desktop/api/Http/nf-http-httpinitialize)             | Inizializza l'API del server HTTP per l'uso da parte del processo chiamante.                                                                   |
| [**HttpPrepareUrl**](/windows/desktop/api/Http/nf-http-httpprepareurl)             | Analizza, analizza e normalizza un URL Unicode o punycode non normalizzato in modo che sia sicuro e valido da usare in altre funzioni HTTP. |
| [**HttpTerminate**](/windows/desktop/api/Http/nf-http-httpterminate)               | Indica all'API del server HTTP di pulire tutte le risorse associate a un processo specifico.                                       |



 

## <a name="cache-management"></a>Gestione della cache



| Funzione                                                       | Descrizione                                                                                            |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**HttpAddFragmentToCache**](/windows/desktop/api/Http/nf-http-httpaddfragmenttocache)       | Memorizza nella cache un frammento di dati in modo che possa essere usato per comporre una risposta dinamica senza leggere dal disco. |
| [**HttpFlushResponseCache**](/windows/desktop/api/Http/nf-http-httpflushresponsecache)       | Rimuove dalla cache HTTP i frammenti specificati memorizzati nella cache.                                                |
| [**HttpReadFragmentFromCache**](/windows/desktop/api/Http/nf-http-httpreadfragmentfromcache) | Recupera un frammento di risposta memorizzato nella cache specificato.                                                        |



 

## <a name="configuration"></a>Configurazione



| Funzione                                                                 | Descrizione                                                       |
|--------------------------------------------------------------------------|-------------------------------------------------------------------|
| [**HttpDeleteServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpdeleteserviceconfiguration) | Elimina le informazioni specificate dall'archivio di configurazione HTTP.  |
| [**HttpQueryServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpqueryserviceconfiguration)   | Esegue una query sull'archivio di configurazione HTTP per ottenere le informazioni specificate.   |
| [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration)       | Imposta i valori specificati nell'archivio di configurazione dell'API del server HTTP. |



 

## <a name="input-and-output"></a>Input e output



| Funzione                                                             | Descrizione                                                    |
|----------------------------------------------------------------------|----------------------------------------------------------------|
| [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest)             | Recupera una richiesta HTTP da una coda di richieste specificata.      |
| [**HttpReceiveRequestEntityBody**](/windows/desktop/api/Http/nf-http-httpreceiverequestentitybody) | Recupera i dati del corpo dell'entità di una determinata richiesta HTTP.       |
| [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse)                 | Invia una risposta HTTP per una determinata richiesta HTTP.          |
| [**HttpSendResponseEntityBody**](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody)     | Invia i dati del corpo dell'entità di una risposta HTTP.                    |
| [**HttpWaitForDisconnect**](/windows/desktop/api/Http/nf-http-httpwaitfordisconnect)               | Notifica all'applicazione quando un client HTTP si è disconnesso. |



 

## <a name="ssl"></a>SSL



| Funzione                                                             | Descrizione                                             |
|----------------------------------------------------------------------|---------------------------------------------------------|
| [**HttpReceiveClientCertificate**](/windows/desktop/api/Http/nf-http-httpreceiveclientcertificate) | Recupera il certificato client per una connessione SSL. |



 

## <a name="url-registration"></a>Registrazione URL



| Funzione                               | Descrizione                                                                                     |
|----------------------------------------|-------------------------------------------------------------------------------------------------|
| [**HttpAddUrl**](/windows/desktop/api/Http/nf-http-httpaddurl)       | Registra un URL in modo che le relative richieste HTTP siano indirizzate a una coda di richieste specificata.           |
| [**HttpRemoveUrl**](/windows/desktop/api/Http/nf-http-httpremoveurl) | Annulla la registrazione di un URL specificato, in modo che le richieste non siano più indirizzate a una coda specificata. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Strutture dell'API del server HTTP versione 1.0](http-server-api-version-1-0-structures.md)
</dt> </dl>

 

 




