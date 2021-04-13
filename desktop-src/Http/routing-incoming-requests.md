---
title: Routing delle richieste in ingresso
description: L'API server HTTP gestisce un database di routing per determinare quale applicazione riceve una richiesta in ingresso.
ms.assetid: 7c613137-66bd-4375-93cb-b5562823bc12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da483030441f3a9239eef153da59212166bce9eb
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/20/2020
ms.locfileid: "104399897"
---
# <a name="routing-incoming-requests"></a><span data-ttu-id="9be4d-103">Routing delle richieste in ingresso</span><span class="sxs-lookup"><span data-stu-id="9be4d-103">Routing Incoming Requests</span></span>

<span data-ttu-id="9be4d-104">L'API server HTTP gestisce un database di routing per determinare quale applicazione riceve una richiesta in ingresso.</span><span class="sxs-lookup"><span data-stu-id="9be4d-104">The HTTP Server API maintains a routing database to determine which application receives an incoming request.</span></span> <span data-ttu-id="9be4d-105">La tabella di routing è compilata dal database di prenotazione e contiene le voci di prenotazione nonché le registrazioni correnti.</span><span class="sxs-lookup"><span data-stu-id="9be4d-105">The routing table is built from the reservation database and contains reservation entries as well as current registrations.</span></span> <span data-ttu-id="9be4d-106">Quando viene effettuata una registrazione o una prenotazione, questa viene inserita nel bucket del database di routing che corrisponde al tipo di host, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="9be4d-106">When a registration or reservation is made, it is placed into the routing database bucket that corresponds to the host type as follows:</span></span>

-   <span data-ttu-id="9be4d-107">\+ : le registrazioni delle porte vengono inserite nel bucket "con carattere jolly sicuro"</span><span class="sxs-lookup"><span data-stu-id="9be4d-107">\+ : port registrations are placed in the "Strong Wildcard" bucket</span></span>

-   <span data-ttu-id="9be4d-108">host: le registrazioni delle porte vengono inserite nel bucket "esplicito"</span><span class="sxs-lookup"><span data-stu-id="9be4d-108">host : port registrations are placed in the "Explicit" bucket</span></span>

-   <span data-ttu-id="9be4d-109">IP: le registrazioni delle porte vengono inserite nel bucket "con carattere jolly vulnerabile associato a IP"</span><span class="sxs-lookup"><span data-stu-id="9be4d-109">IP : port registrations are placed in the "IP-bound Weak Wildcard" bucket</span></span>

-   <span data-ttu-id="9be4d-110">\* : le registrazioni delle porte vengono inserite nel bucket "con carattere jolly debole"</span><span class="sxs-lookup"><span data-stu-id="9be4d-110">\* : port registrations are placed in the "Weak Wildcard" bucket</span></span>

<span data-ttu-id="9be4d-111">Questa procedura si riferisce anche all'elaborazione delle richieste HTTP in ingresso.</span><span class="sxs-lookup"><span data-stu-id="9be4d-111">These steps also refer to the order incoming HTTP requests are processed.</span></span> <span data-ttu-id="9be4d-112">Prima le prenotazioni con caratteri jolly forti, quindi la prenotazione esplicita vengono controllate seguito dal carattere jolly debole associato a IP e dal carattere jolly vulnerabile.</span><span class="sxs-lookup"><span data-stu-id="9be4d-112">The strong wildcard reservations first, then the explicit reservation are checked followed by the IP-bound weak wildcard and weak wildcard.</span></span> <span data-ttu-id="9be4d-113">La ricerca viene arrestata quando viene trovata una corrispondenza in modo che non vengano trovate le registrazioni in uno dei bucket rimanenti.</span><span class="sxs-lookup"><span data-stu-id="9be4d-113">The search stops when a match is found so that registrations in any of the remaining buckets are not found.</span></span>

<span data-ttu-id="9be4d-114">L'algoritmo di routing dell'API del server HTTP individua la migliore corrispondenza per [URLPrefix](urlprefix-strings.md) eseguendo una ricerca nelle voci di registrazione e nelle voci di prenotazione del database di routing, iniziando dal bucket con carattere jolly complesso e terminando con il bucket con carattere jolly vulnerabile.</span><span class="sxs-lookup"><span data-stu-id="9be4d-114">The HTTP Server API routing algorithm locates the best match for the [UrlPrefix](urlprefix-strings.md) by searching both the registration entries and the reservation entries of the routing database, starting with the strong wildcard bucket and ending with the weak wildcard bucket.</span></span> <span data-ttu-id="9be4d-115">La corrispondenza migliore, all'interno di un bucket, è la corrispondenza più estesa nella parte URI relativa di UrlPrefix (presupponendo una corrispondenza esatta per l'host, la porta e le parti dello schema dell'URL).</span><span class="sxs-lookup"><span data-stu-id="9be4d-115">The best match, within a bucket, is the longest match in the relative URI portion of the UrlPrefix (assuming an exact match for the host, port and scheme portions of the URL).</span></span> <span data-ttu-id="9be4d-116">Quando viene trovata una corrispondenza in un bucket, l'algoritmo di routing interrompe la ricerca e ignora tutti i bucket con priorità più bassa.</span><span class="sxs-lookup"><span data-stu-id="9be4d-116">After a match is found in a bucket, the routing algorithm stops its search and skips all lower priority buckets.</span></span>

<span data-ttu-id="9be4d-117">Si considerino, ad esempio, le registrazioni seguenti (elencate in ordine decrescente di priorità in base ai tipi di bucket:</span><span class="sxs-lookup"><span data-stu-id="9be4d-117">For example, consider the following registrations (listed in descending order of priority based on bucket types:</span></span>

-   <span data-ttu-id="9be4d-118">Registrazione: `https://+:80/vroot/` è registrata dall'applicazione 1</span><span class="sxs-lookup"><span data-stu-id="9be4d-118">Registration: `https://+:80/vroot/` is registered by application 1</span></span>

-   <span data-ttu-id="9be4d-119">Registrazione: `https://adatum.com:80/` è registrata dall'applicazione 2</span><span class="sxs-lookup"><span data-stu-id="9be4d-119">Registration: `https://adatum.com:80/` is registered by application 2</span></span>

-   <span data-ttu-id="9be4d-120">Registrazione: `https://\*:80/` è registrata dall'applicazione 3</span><span class="sxs-lookup"><span data-stu-id="9be4d-120">Registration: `https://\*:80/` is registered by application 3</span></span>

<span data-ttu-id="9be4d-121">Una richiesta in ingresso per `https://adatum.com:80/vroot/subdir/file.htm/` viene inviata all'applicazione 1.</span><span class="sxs-lookup"><span data-stu-id="9be4d-121">An incoming request for `https://adatum.com:80/vroot/subdir/file.htm/` is delivered to application 1.</span></span> <span data-ttu-id="9be4d-122">Una richiesta in ingresso per `https://adatum.com:80/default.htm/` viene inviata all'applicazione 2.</span><span class="sxs-lookup"><span data-stu-id="9be4d-122">An incoming request for `https://adatum.com:80/default.htm/` is delivered to application 2.</span></span> <span data-ttu-id="9be4d-123">Una richiesta in ingresso per `https://otheradatum.com:80/file.htm/` viene inviata all'applicazione 3.</span><span class="sxs-lookup"><span data-stu-id="9be4d-123">An incoming request for `https://otheradatum.com:80/file.htm/` is delivered to application 3.</span></span>

<span data-ttu-id="9be4d-124">Se la corrispondenza migliore è una voce di prenotazione, significa che l'applicazione che deve ricevere la richiesta non è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="9be4d-124">If the best match is a reservation entry, this means that the application that should receive the request is not running.</span></span> <span data-ttu-id="9be4d-125">Si consideri, ad esempio, la registrazione e la prenotazione seguenti:</span><span class="sxs-lookup"><span data-stu-id="9be4d-125">For example, consider the following registration and reservation:</span></span>

-   <span data-ttu-id="9be4d-126">Registrazione: `https://\*:80/vroot/` è registrata dall'applicazione 1, dall'utente A</span><span class="sxs-lookup"><span data-stu-id="9be4d-126">Registration: `https://\*:80/vroot/` is registered by application 1, user A</span></span>

-   <span data-ttu-id="9be4d-127">Prenotazione: `https://adatum.com:80/` è stata riservata all'utente B</span><span class="sxs-lookup"><span data-stu-id="9be4d-127">Reservation: `https://adatum.com:80/` has been reserved for user B</span></span>

<span data-ttu-id="9be4d-128">Una richiesta in ingresso per `https://adatum.com:80/vroot/file.htm/` non viene recapitata all'applicazione 1 perché la corrispondenza migliore porta alla voce di prenotazione per l'utente B. Le regole di precedenza vengono applicate in questo caso alla prenotazione con una priorità più alta.</span><span class="sxs-lookup"><span data-stu-id="9be4d-128">An incoming request for `https://adatum.com:80/vroot/file.htm/` is not delivered to application 1 because the best match leads to the reservation entry for user B. The precedence rules are applied in this case to the reservation which has a higher priority.</span></span> <span data-ttu-id="9be4d-129">Se non è attivo alcun processo autorizzato e registrato per richieste di assistenza per l'URL ricevuto, la richiesta viene rifiutata con un codice di stato 400 (richiesta non valida).</span><span class="sxs-lookup"><span data-stu-id="9be4d-129">If no process is active that is authorized and registered to service requests for the URL received, the request is rejected with a 400 status code (Bad Request).</span></span>

 

 




