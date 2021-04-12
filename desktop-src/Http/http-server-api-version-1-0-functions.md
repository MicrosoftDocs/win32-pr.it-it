---
title: Funzioni API server HTTP versione 1,0
description: L'API server HTTP fornisce le funzioni seguenti per la scrittura di applicazioni.
ms.assetid: 1da9907d-a09d-41e1-aca1-9a8e2b91296f
keywords:
- Funzioni API server HTTP versione 1,0
- Funzioni HTTP, API server HTTP versione 1,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 050821e40695268d6e3fa2c946d2e8859748db2b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221869"
---
# <a name="http-server-api-version-10-functions"></a>Funzioni API server HTTP versione 1,0

L'API server HTTP fornisce le funzioni seguenti per la scrittura di applicazioni.

## <a name="general"></a>Generale



| Funzione                                             | Descrizione                                                                                                                       |
|------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**HttpCreateHttpHandle**](/windows/desktop/api/Http/nf-http-httpcreatehttphandle) | Crea una coda di richieste HTTP e restituisce un handle.                                                                         |
| [**HttpInitialize**](/windows/desktop/api/Http/nf-http-httpinitialize)             | Inizializza l'API del server HTTP per l'utilizzo da parte del processo chiamante.                                                                   |
| [**HttpPrepareUrl**](/windows/desktop/api/Http/nf-http-httpprepareurl)             | Analizza, analizza e normalizza un URL Unicode o Punycode non normalizzato in modo che sia sicuro e valido per l'uso in altre funzioni HTTP. |
| [**HttpTerminate**](/windows/desktop/api/Http/nf-http-httpterminate)               | Indica all'API del server HTTP di eseguire la pulizia di tutte le risorse associate a un determinato processo.                                       |



 

## <a name="cache-management"></a>Gestione della cache



| Funzione                                                       | Descrizione                                                                                            |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**HttpAddFragmentToCache**](/windows/desktop/api/Http/nf-http-httpaddfragmenttocache)       | Memorizza nella cache un frammento di dati in modo che possa essere usato per comporre una risposta dinamica senza leggere dal disco. |
| [**HttpFlushResponseCache**](/windows/desktop/api/Http/nf-http-httpflushresponsecache)       | Rimuove i frammenti specificati memorizzati dalla cache HTTP.                                                |
| [**HttpReadFragmentFromCache**](/windows/desktop/api/Http/nf-http-httpreadfragmentfromcache) | Recupera un frammento di risposta memorizzato nella cache specificato.                                                        |



 

## <a name="configuration"></a>Configurazione



| Funzione                                                                 | Descrizione                                                       |
|--------------------------------------------------------------------------|-------------------------------------------------------------------|
| [**HttpDeleteServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpdeleteserviceconfiguration) | Elimina le informazioni specificate dall'archivio di configurazione HTTP.  |
| [**HttpQueryServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpqueryserviceconfiguration)   | Esegue una query sull'archivio di configurazione HTTP per le informazioni specificate.   |
| [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration)       | Imposta i valori specificati nell'archivio di configurazione dell'API del server HTTP. |



 

## <a name="input-and-output"></a>Input e output



| Funzione                                                             | Descrizione                                                    |
|----------------------------------------------------------------------|----------------------------------------------------------------|
| [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest)             | Recupera una richiesta HTTP da una coda di richieste specificata.      |
| [**HttpReceiveRequestEntityBody**](/windows/desktop/api/Http/nf-http-httpreceiverequestentitybody) | Recupera i dati del corpo dell'entità di una determinata richiesta HTTP.       |
| [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse)                 | Invia una risposta HTTP per una determinata richiesta HTTP.          |
| [**HttpSendResponseEntityBody**](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody)     | Invia dati del corpo dell'entità di una risposta HTTP.                    |
| [**HttpWaitForDisconnect**](/windows/desktop/api/Http/nf-http-httpwaitfordisconnect)               | Notifica all'applicazione la disconnessione di un client HTTP. |



 

## <a name="ssl"></a>SSL



| Funzione                                                             | Descrizione                                             |
|----------------------------------------------------------------------|---------------------------------------------------------|
| [**HttpReceiveClientCertificate**](/windows/desktop/api/Http/nf-http-httpreceiveclientcertificate) | Recupera il certificato client per una connessione SSL. |



 

## <a name="url-registration"></a>Registrazione URL



| Funzione                               | Descrizione                                                                                     |
|----------------------------------------|-------------------------------------------------------------------------------------------------|
| [**HttpAddUrl**](/windows/desktop/api/Http/nf-http-httpaddurl)       | Registra un URL in modo che le richieste HTTP vengano indirizzate a una coda di richieste specificata.           |
| [**HttpRemoveUrl**](/windows/desktop/api/Http/nf-http-httpremoveurl) | Annulla la registrazione di un URL specificato, in modo che le richieste non vengano più indirizzate a una coda specificata. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Strutture API server HTTP versione 1,0](http-server-api-version-1-0-structures.md)
</dt> </dl>

 

 




