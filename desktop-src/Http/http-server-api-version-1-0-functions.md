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
# <a name="http-server-api-version-10-functions"></a><span data-ttu-id="1d870-105">Funzioni API server HTTP versione 1,0</span><span class="sxs-lookup"><span data-stu-id="1d870-105">HTTP Server API Version 1.0 Functions</span></span>

<span data-ttu-id="1d870-106">L'API server HTTP fornisce le funzioni seguenti per la scrittura di applicazioni.</span><span class="sxs-lookup"><span data-stu-id="1d870-106">The HTTP Server API provides the following functions for writing applications.</span></span>

## <a name="general"></a><span data-ttu-id="1d870-107">Generale</span><span class="sxs-lookup"><span data-stu-id="1d870-107">General</span></span>



| <span data-ttu-id="1d870-108">Funzione</span><span class="sxs-lookup"><span data-stu-id="1d870-108">Function</span></span>                                             | <span data-ttu-id="1d870-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1d870-109">Description</span></span>                                                                                                                       |
|------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1d870-110">**HttpCreateHttpHandle**</span><span class="sxs-lookup"><span data-stu-id="1d870-110">**HttpCreateHttpHandle**</span></span>](/windows/desktop/api/Http/nf-http-httpcreatehttphandle) | <span data-ttu-id="1d870-111">Crea una coda di richieste HTTP e restituisce un handle.</span><span class="sxs-lookup"><span data-stu-id="1d870-111">Creates an HTTP request queue and returns a handle to it.</span></span>                                                                         |
| [<span data-ttu-id="1d870-112">**HttpInitialize**</span><span class="sxs-lookup"><span data-stu-id="1d870-112">**HttpInitialize**</span></span>](/windows/desktop/api/Http/nf-http-httpinitialize)             | <span data-ttu-id="1d870-113">Inizializza l'API del server HTTP per l'utilizzo da parte del processo chiamante.</span><span class="sxs-lookup"><span data-stu-id="1d870-113">Initializes the HTTP Server API for use by the calling process.</span></span>                                                                   |
| [<span data-ttu-id="1d870-114">**HttpPrepareUrl**</span><span class="sxs-lookup"><span data-stu-id="1d870-114">**HttpPrepareUrl**</span></span>](/windows/desktop/api/Http/nf-http-httpprepareurl)             | <span data-ttu-id="1d870-115">Analizza, analizza e normalizza un URL Unicode o Punycode non normalizzato in modo che sia sicuro e valido per l'uso in altre funzioni HTTP.</span><span class="sxs-lookup"><span data-stu-id="1d870-115">Parses, analyzes, and normalizes a non-normalized Unicode or punycode URL so it is safe and valid to use in other HTTP functions.</span></span> |
| [<span data-ttu-id="1d870-116">**HttpTerminate**</span><span class="sxs-lookup"><span data-stu-id="1d870-116">**HttpTerminate**</span></span>](/windows/desktop/api/Http/nf-http-httpterminate)               | <span data-ttu-id="1d870-117">Indica all'API del server HTTP di eseguire la pulizia di tutte le risorse associate a un determinato processo.</span><span class="sxs-lookup"><span data-stu-id="1d870-117">Directs the HTTP Server API to clean up any resources associated with a particular process.</span></span>                                       |



 

## <a name="cache-management"></a><span data-ttu-id="1d870-118">Gestione della cache</span><span class="sxs-lookup"><span data-stu-id="1d870-118">Cache Management</span></span>



| <span data-ttu-id="1d870-119">Funzione</span><span class="sxs-lookup"><span data-stu-id="1d870-119">Function</span></span>                                                       | <span data-ttu-id="1d870-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1d870-120">Description</span></span>                                                                                            |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1d870-121">**HttpAddFragmentToCache**</span><span class="sxs-lookup"><span data-stu-id="1d870-121">**HttpAddFragmentToCache**</span></span>](/windows/desktop/api/Http/nf-http-httpaddfragmenttocache)       | <span data-ttu-id="1d870-122">Memorizza nella cache un frammento di dati in modo che possa essere usato per comporre una risposta dinamica senza leggere dal disco.</span><span class="sxs-lookup"><span data-stu-id="1d870-122">Caches a data fragment so that it can be used to compose a dynamic response without reading from disk.</span></span> |
| [<span data-ttu-id="1d870-123">**HttpFlushResponseCache**</span><span class="sxs-lookup"><span data-stu-id="1d870-123">**HttpFlushResponseCache**</span></span>](/windows/desktop/api/Http/nf-http-httpflushresponsecache)       | <span data-ttu-id="1d870-124">Rimuove i frammenti specificati memorizzati dalla cache HTTP.</span><span class="sxs-lookup"><span data-stu-id="1d870-124">Removes specified cached fragments from the HTTP cache.</span></span>                                                |
| [<span data-ttu-id="1d870-125">**HttpReadFragmentFromCache**</span><span class="sxs-lookup"><span data-stu-id="1d870-125">**HttpReadFragmentFromCache**</span></span>](/windows/desktop/api/Http/nf-http-httpreadfragmentfromcache) | <span data-ttu-id="1d870-126">Recupera un frammento di risposta memorizzato nella cache specificato.</span><span class="sxs-lookup"><span data-stu-id="1d870-126">Retrieves a specified cached response fragment.</span></span>                                                        |



 

## <a name="configuration"></a><span data-ttu-id="1d870-127">Configurazione</span><span class="sxs-lookup"><span data-stu-id="1d870-127">Configuration</span></span>



| <span data-ttu-id="1d870-128">Funzione</span><span class="sxs-lookup"><span data-stu-id="1d870-128">Function</span></span>                                                                 | <span data-ttu-id="1d870-129">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1d870-129">Description</span></span>                                                       |
|--------------------------------------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="1d870-130">**HttpDeleteServiceConfiguration**</span><span class="sxs-lookup"><span data-stu-id="1d870-130">**HttpDeleteServiceConfiguration**</span></span>](/windows/desktop/api/Http/nf-http-httpdeleteserviceconfiguration) | <span data-ttu-id="1d870-131">Elimina le informazioni specificate dall'archivio di configurazione HTTP.</span><span class="sxs-lookup"><span data-stu-id="1d870-131">Deletes specified information from the HTTP configuration store.</span></span>  |
| [<span data-ttu-id="1d870-132">**HttpQueryServiceConfiguration**</span><span class="sxs-lookup"><span data-stu-id="1d870-132">**HttpQueryServiceConfiguration**</span></span>](/windows/desktop/api/Http/nf-http-httpqueryserviceconfiguration)   | <span data-ttu-id="1d870-133">Esegue una query sull'archivio di configurazione HTTP per le informazioni specificate.</span><span class="sxs-lookup"><span data-stu-id="1d870-133">Queries the HTTP configuration store for specified information.</span></span>   |
| [<span data-ttu-id="1d870-134">**HttpSetServiceConfiguration**</span><span class="sxs-lookup"><span data-stu-id="1d870-134">**HttpSetServiceConfiguration**</span></span>](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration)       | <span data-ttu-id="1d870-135">Imposta i valori specificati nell'archivio di configurazione dell'API del server HTTP.</span><span class="sxs-lookup"><span data-stu-id="1d870-135">Sets specified values in the HTTP Server API configuration store.</span></span> |



 

## <a name="input-and-output"></a><span data-ttu-id="1d870-136">Input e output</span><span class="sxs-lookup"><span data-stu-id="1d870-136">Input and Output</span></span>



| <span data-ttu-id="1d870-137">Funzione</span><span class="sxs-lookup"><span data-stu-id="1d870-137">Function</span></span>                                                             | <span data-ttu-id="1d870-138">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1d870-138">Description</span></span>                                                    |
|----------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="1d870-139">**HttpReceiveHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="1d870-139">**HttpReceiveHttpRequest**</span></span>](/windows/desktop/api/Http/nf-http-httpreceivehttprequest)             | <span data-ttu-id="1d870-140">Recupera una richiesta HTTP da una coda di richieste specificata.</span><span class="sxs-lookup"><span data-stu-id="1d870-140">Retrieves an HTTP request from a specified request queue.</span></span>      |
| [<span data-ttu-id="1d870-141">**HttpReceiveRequestEntityBody**</span><span class="sxs-lookup"><span data-stu-id="1d870-141">**HttpReceiveRequestEntityBody**</span></span>](/windows/desktop/api/Http/nf-http-httpreceiverequestentitybody) | <span data-ttu-id="1d870-142">Recupera i dati del corpo dell'entità di una determinata richiesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="1d870-142">Retrieves entity-body data of a particular HTTP request.</span></span>       |
| [<span data-ttu-id="1d870-143">**HttpSendHttpResponse**</span><span class="sxs-lookup"><span data-stu-id="1d870-143">**HttpSendHttpResponse**</span></span>](/windows/desktop/api/Http/nf-http-httpsendhttpresponse)                 | <span data-ttu-id="1d870-144">Invia una risposta HTTP per una determinata richiesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="1d870-144">Sends an HTTP response for a particular HTTP request.</span></span>          |
| [<span data-ttu-id="1d870-145">**HttpSendResponseEntityBody**</span><span class="sxs-lookup"><span data-stu-id="1d870-145">**HttpSendResponseEntityBody**</span></span>](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody)     | <span data-ttu-id="1d870-146">Invia dati del corpo dell'entità di una risposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="1d870-146">Sends entity-body data of an HTTP response.</span></span>                    |
| [<span data-ttu-id="1d870-147">**HttpWaitForDisconnect**</span><span class="sxs-lookup"><span data-stu-id="1d870-147">**HttpWaitForDisconnect**</span></span>](/windows/desktop/api/Http/nf-http-httpwaitfordisconnect)               | <span data-ttu-id="1d870-148">Notifica all'applicazione la disconnessione di un client HTTP.</span><span class="sxs-lookup"><span data-stu-id="1d870-148">Notifies the application when an HTTP client has disconnected.</span></span> |



 

## <a name="ssl"></a><span data-ttu-id="1d870-149">SSL</span><span class="sxs-lookup"><span data-stu-id="1d870-149">SSL</span></span>



| <span data-ttu-id="1d870-150">Funzione</span><span class="sxs-lookup"><span data-stu-id="1d870-150">Function</span></span>                                                             | <span data-ttu-id="1d870-151">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1d870-151">Description</span></span>                                             |
|----------------------------------------------------------------------|---------------------------------------------------------|
| [<span data-ttu-id="1d870-152">**HttpReceiveClientCertificate**</span><span class="sxs-lookup"><span data-stu-id="1d870-152">**HttpReceiveClientCertificate**</span></span>](/windows/desktop/api/Http/nf-http-httpreceiveclientcertificate) | <span data-ttu-id="1d870-153">Recupera il certificato client per una connessione SSL.</span><span class="sxs-lookup"><span data-stu-id="1d870-153">Retrieves the client certificate for an SSL connection.</span></span> |



 

## <a name="url-registration"></a><span data-ttu-id="1d870-154">Registrazione URL</span><span class="sxs-lookup"><span data-stu-id="1d870-154">URL Registration</span></span>



| <span data-ttu-id="1d870-155">Funzione</span><span class="sxs-lookup"><span data-stu-id="1d870-155">Function</span></span>                               | <span data-ttu-id="1d870-156">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1d870-156">Description</span></span>                                                                                     |
|----------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1d870-157">**HttpAddUrl**</span><span class="sxs-lookup"><span data-stu-id="1d870-157">**HttpAddUrl**</span></span>](/windows/desktop/api/Http/nf-http-httpaddurl)       | <span data-ttu-id="1d870-158">Registra un URL in modo che le richieste HTTP vengano indirizzate a una coda di richieste specificata.</span><span class="sxs-lookup"><span data-stu-id="1d870-158">Registers a URL so that HTTP requests for it are routed to a specified request queue.</span></span>           |
| [<span data-ttu-id="1d870-159">**HttpRemoveUrl**</span><span class="sxs-lookup"><span data-stu-id="1d870-159">**HttpRemoveUrl**</span></span>](/windows/desktop/api/Http/nf-http-httpremoveurl) | <span data-ttu-id="1d870-160">Annulla la registrazione di un URL specificato, in modo che le richieste non vengano più indirizzate a una coda specificata.</span><span class="sxs-lookup"><span data-stu-id="1d870-160">Unregisters a specified URL, so that requests for it are no longer routed to a specified queue.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="1d870-161">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1d870-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d870-162">Strutture API server HTTP versione 1,0</span><span class="sxs-lookup"><span data-stu-id="1d870-162">HTTP Server API Version 1.0 Structures</span></span>](http-server-api-version-1-0-structures.md)
</dt> </dl>

 

 




