---
title: Memorizzazione nella cache (Windows Internet)
description: Le funzioni WinINet hanno un supporto di memorizzazione nella cache integrato semplice, ma flessibile.
ms.assetid: 44c268c9-a745-432a-8540-60d7e7d2cb2d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e753d826ec3abe580b94158296562208dcbed44
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104118786"
---
# <a name="caching-windows-internet"></a><span data-ttu-id="1ce43-103">Memorizzazione nella cache (Windows Internet)</span><span class="sxs-lookup"><span data-stu-id="1ce43-103">Caching (Windows Internet)</span></span>

<span data-ttu-id="1ce43-104">Le funzioni WinINet hanno un supporto di memorizzazione nella cache integrato semplice, ma flessibile.</span><span class="sxs-lookup"><span data-stu-id="1ce43-104">The WinINet functions have simple, yet flexible, built-in caching support.</span></span> <span data-ttu-id="1ce43-105">Tutti i dati recuperati dalla rete vengono memorizzati nella cache sul disco rigido e recuperati per le richieste successive.</span><span class="sxs-lookup"><span data-stu-id="1ce43-105">Any data retrieved from the network is cached on the hard disk and retrieved for subsequent requests.</span></span> <span data-ttu-id="1ce43-106">L'applicazione può controllare la memorizzazione nella cache per ogni richiesta.</span><span class="sxs-lookup"><span data-stu-id="1ce43-106">The application can control the caching on each request.</span></span> <span data-ttu-id="1ce43-107">Per le richieste HTTP dal server, vengono memorizzate nella cache anche la maggior parte delle intestazioni ricevute.</span><span class="sxs-lookup"><span data-stu-id="1ce43-107">For http requests from the server, most headers received are also cached.</span></span> <span data-ttu-id="1ce43-108">Quando una richiesta HTTP viene soddisfatta dalla cache, anche le intestazioni memorizzate nella cache vengono restituite al chiamante.</span><span class="sxs-lookup"><span data-stu-id="1ce43-108">When an http request is satisfied from the cache, the cached headers are also returned to the caller.</span></span> <span data-ttu-id="1ce43-109">In questo modo, il download dei dati viene semplificato, indipendentemente dal fatto che i dati provengano dalla cache o dalla rete.</span><span class="sxs-lookup"><span data-stu-id="1ce43-109">This makes data download seamless, whether the data is coming from the cache or from the network.</span></span>

<span data-ttu-id="1ce43-110">Le applicazioni devono allocare correttamente un buffer per ottenere i risultati desiderati quando si utilizzano le funzioni di memorizzazione nella cache degli URL persistenti.</span><span class="sxs-lookup"><span data-stu-id="1ce43-110">Applications must properly allocate a buffer in order to get the desired results when using the persistent URL caching functions.</span></span> <span data-ttu-id="1ce43-111">Per ulteriori informazioni, vedere [utilizzo dei buffer](appendix-b-using-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="1ce43-111">For more information, see [Using Buffers](appendix-b-using-buffers.md).</span></span>

## <a name="cache-behavior-during-response-processing"></a><span data-ttu-id="1ce43-112">Comportamento della cache durante l'elaborazione della risposta</span><span class="sxs-lookup"><span data-stu-id="1ce43-112">Cache Behavior During Response Processing</span></span>

<span data-ttu-id="1ce43-113">La cache di WinINet è conforme alle direttive di controllo della cache HTTP descritte in RFC 2616.</span><span class="sxs-lookup"><span data-stu-id="1ce43-113">The WinINet cache is compliant with the HTTP cache-control directives described in RFC 2616.</span></span> <span data-ttu-id="1ce43-114">Le direttive di controllo della cache e i flag del set di applicazioni determinano ciò che può essere memorizzato nella cache. Tuttavia, WinINet determina ciò che viene effettivamente memorizzato nella cache in base ai criteri seguenti:</span><span class="sxs-lookup"><span data-stu-id="1ce43-114">The cache-control directives and application set flags determine what may be cached; however, WinINet determines what is actually cached based on the following criterion:</span></span>

-   <span data-ttu-id="1ce43-115">WinINet memorizza nella cache solo le risposte HTTP e FTP.</span><span class="sxs-lookup"><span data-stu-id="1ce43-115">WinINet only caches HTTP and FTP responses.</span></span>
-   <span data-ttu-id="1ce43-116">Solo le risposte ben corrette possono essere archiviate da una cache e usate in una risposta a una richiesta successiva.</span><span class="sxs-lookup"><span data-stu-id="1ce43-116">Only well behaved responses may be stored by a cache and used in a reply to a subsequent Request.</span></span> <span data-ttu-id="1ce43-117">Le risposte ben corrette sono definite come risposte che restituiscono correttamente.</span><span class="sxs-lookup"><span data-stu-id="1ce43-117">Well behaved responses are defined as responses that return successfully.</span></span>
-   <span data-ttu-id="1ce43-118">Per impostazione predefinita, WinINet memorizza nella cache le risposte con esito positivo, a meno che una direttiva di controllo della cache dal server o un flag definito dall'applicazione denoti specificamente che la risposta potrebbe non essere memorizzata nella cache.</span><span class="sxs-lookup"><span data-stu-id="1ce43-118">By default, WinINet will cache successful responses unless either a cache-control directive from the server, or an application-defined flag specifically denote that the response may not be cached.</span></span>
-   <span data-ttu-id="1ce43-119">In generale, le risposte al verbo GET vengono memorizzate nella cache se vengono soddisfatti i requisiti elencati in precedenza.</span><span class="sxs-lookup"><span data-stu-id="1ce43-119">In general, responses to the GET verb are cached if the requirements listed above are met.</span></span> <span data-ttu-id="1ce43-120">Le risposte ai verbi PUT e POST non vengono memorizzate nella cache in qualsiasi circostanza.</span><span class="sxs-lookup"><span data-stu-id="1ce43-120">Responses to PUT and POST verbs are not cached under any circumstances.</span></span>
-   <span data-ttu-id="1ce43-121">Gli elementi verranno memorizzati nella cache anche quando la cache è piena.</span><span class="sxs-lookup"><span data-stu-id="1ce43-121">Items will be cached even when the cache is full.</span></span> <span data-ttu-id="1ce43-122">Se un elemento aggiunto inserisce la cache sul limite delle dimensioni, viene pianificato il scavenger della cache.</span><span class="sxs-lookup"><span data-stu-id="1ce43-122">If an added item is puts the cache over the size limit, the cache scavenger is scheduled.</span></span> <span data-ttu-id="1ce43-123">Per impostazione predefinita, nella cache non è garantito che gli elementi rimangano più di 10 minuti.</span><span class="sxs-lookup"><span data-stu-id="1ce43-123">By default, items are not guaranteed to remain more than 10 minutes in the cache.</span></span> <span data-ttu-id="1ce43-124">Per altre informazioni, vedere la sezione [cache Scavenger](#cache-scavenger) riportata di seguito.</span><span class="sxs-lookup"><span data-stu-id="1ce43-124">For more information, see the [Cache Scavenger](#cache-scavenger) section below.</span></span>
-   <span data-ttu-id="1ce43-125">HTTPS viene memorizzato nella cache per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="1ce43-125">Https is cached by default.</span></span> <span data-ttu-id="1ce43-126">Questa operazione viene gestita da un'impostazione globale che non può essere sottoposta a override dalle direttive della cache definite dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="1ce43-126">This is managed by a global setting that cannot be overridden by application-defined cache directives.</span></span> <span data-ttu-id="1ce43-127">Per eseguire l'override dell'impostazione globale, selezionare l'applet Opzioni Internet nel pannello di controllo e passare alla scheda Avanzate. Selezionare la casella "non salvare le pagine crittografate su disco" nella sezione "sicurezza".</span><span class="sxs-lookup"><span data-stu-id="1ce43-127">To override the global setting, select the Internet Options applet in the control panel, and go to the advanced tab. Check the "Do not save encrypted pages to disk" box under the "Security" section.</span></span>

## <a name="cache-scavenger"></a><span data-ttu-id="1ce43-128">Scavenger cache</span><span class="sxs-lookup"><span data-stu-id="1ce43-128">Cache Scavenger</span></span>

<span data-ttu-id="1ce43-129">Il scavenger della cache pulisce periodicamente gli elementi dalla cache.</span><span class="sxs-lookup"><span data-stu-id="1ce43-129">The cache scavenger periodically cleans items from the cache.</span></span> <span data-ttu-id="1ce43-130">Se un elemento viene aggiunto alla cache e la cache è piena, l'elemento viene aggiunto alla cache e il scavenger della cache è pianificato.</span><span class="sxs-lookup"><span data-stu-id="1ce43-130">If an item is added to the cache and the cache is full, the item is added to the cache and the cache scavenger is scheduled.</span></span> <span data-ttu-id="1ce43-131">Se il scavenger della cache completa un ciclo di scavenging e la cache non ha raggiunto il limite della cache, il Scavenger viene pianificato per un altro round quando un altro elemento viene aggiunto alla cache.</span><span class="sxs-lookup"><span data-stu-id="1ce43-131">If the cache scavenger completes a round of scavenging and the cache has not reached the cache limit, the scavenger is scheduled for another round when another item is added to the cache.</span></span> <span data-ttu-id="1ce43-132">In generale, il Scavenger viene pianificato quando un elemento aggiunto inserisce la cache sul limite delle dimensioni.</span><span class="sxs-lookup"><span data-stu-id="1ce43-132">In general, the scavenger is scheduled when an added item puts the cache over its size limit.</span></span> <span data-ttu-id="1ce43-133">Per impostazione predefinita, la durata minima della cache è impostata su 10 minuti, se non diversamente specificato in una direttiva di controllo della cache.</span><span class="sxs-lookup"><span data-stu-id="1ce43-133">By default, the minimum time to live in the cache is set to 10 minutes unless otherwise specified in a cache-control directive.</span></span> <span data-ttu-id="1ce43-134">Quando viene avviato lo scavenger della cache, non c'è alcuna garanzia che gli elementi meno recenti siano i primi a essere eliminati dalla cache.</span><span class="sxs-lookup"><span data-stu-id="1ce43-134">When the cache scavenger is initiated, there is no guarantee that the oldest items are the first to be deleted from the cache.</span></span>

<span data-ttu-id="1ce43-135">La cache è condivisa tra tutte le applicazioni WinINet nel computer per lo stesso utente.</span><span class="sxs-lookup"><span data-stu-id="1ce43-135">The cache is shared across all WinINet applications on the computer for the same user.</span></span> <span data-ttu-id="1ce43-136">A partire da Windows Vista e Windows Server 2008, le dimensioni della cache sono impostate su 1/32A per la dimensione del disco, con una dimensione minima di 8MB e una dimensione massima di 50 MB.</span><span class="sxs-lookup"><span data-stu-id="1ce43-136">Starting with Windows Vista and Windows Server 2008 the cache size is set to 1/32nd the size of the disk, with a minimum size of 8MB and a maximum size of 50MB.</span></span>

## <a name="using-flags-to-control-caching"></a><span data-ttu-id="1ce43-137">Utilizzo di flag per il controllo della memorizzazione nella cache</span><span class="sxs-lookup"><span data-stu-id="1ce43-137">Using Flags to Control Caching</span></span>

<span data-ttu-id="1ce43-138">I flag di memorizzazione nella cache consentono a un'applicazione di controllare quando e come viene utilizzata la cache.</span><span class="sxs-lookup"><span data-stu-id="1ce43-138">The caching flags allow an application to control when and how it uses the cache.</span></span> <span data-ttu-id="1ce43-139">Questi flag possono essere usati singolarmente o in combinazione con il parametro *dwFlags* in funzioni che accedono a informazioni o risorse su Internet.</span><span class="sxs-lookup"><span data-stu-id="1ce43-139">These flags can be used alone or in combination with the *dwFlags* parameter in functions that access information or resources on the Internet.</span></span> <span data-ttu-id="1ce43-140">Per impostazione predefinita, le funzioni archiviano tutti i dati scaricati da Internet.</span><span class="sxs-lookup"><span data-stu-id="1ce43-140">By default, the functions store all data downloaded from the Internet.</span></span>

<span data-ttu-id="1ce43-141">I flag seguenti possono essere utilizzati per controllare la memorizzazione nella cache.</span><span class="sxs-lookup"><span data-stu-id="1ce43-141">The following flags can be used to control caching.</span></span>



| <span data-ttu-id="1ce43-142">Valore</span><span class="sxs-lookup"><span data-stu-id="1ce43-142">Value</span></span>                                                                                                                                                  | <span data-ttu-id="1ce43-143">Significato</span><span class="sxs-lookup"><span data-stu-id="1ce43-143">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1ce43-144">**\_ \_ Async della cache del flag Internet \_**</span><span class="sxs-lookup"><span data-stu-id="1ce43-144">**INTERNET\_FLAG\_CACHE\_ASYNC**</span></span>](api-flags.md)                                                                            | <span data-ttu-id="1ce43-145">Questo flag non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="1ce43-145">This flag has no effect.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="1ce43-146">**\_cache del flag Internet se la rete ha \_ \_ \_ \_ esito negativo**</span><span class="sxs-lookup"><span data-stu-id="1ce43-146">**INTERNET\_FLAG\_CACHE\_IF\_NET\_FAIL**</span></span>](api-flags.md)                                                              | <span data-ttu-id="1ce43-147">Restituisce la risorsa dalla cache se la richiesta di rete per la risorsa ha esito negativo a causa di un [errore di \_ \_ \_ reimpostazione della connessione Internet](wininet-errors.md) o di [errore \_ Internet \_ non è in grado di \_ connettersi](wininet-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="1ce43-147">Returns the resource from the cache if the network request for the resource fails due to an [ERROR\_INTERNET\_CONNECTION\_RESET](wininet-errors.md) or [ERROR\_INTERNET\_CANNOT\_CONNECT](wininet-errors.md) error.</span></span> <span data-ttu-id="1ce43-148">Questo flag viene usato da [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span><span class="sxs-lookup"><span data-stu-id="1ce43-148">This flag is used by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span>                                                                                                              |
| [<span data-ttu-id="1ce43-149">**\_flag Internet \_ dont \_ cache**</span><span class="sxs-lookup"><span data-stu-id="1ce43-149">**INTERNET\_FLAG\_DONT\_CACHE**</span></span>](api-flags.md)                                                                              | <span data-ttu-id="1ce43-150">Non memorizza nella cache i dati, in locale o in qualsiasi gateway.</span><span class="sxs-lookup"><span data-stu-id="1ce43-150">Does not cache the data, either locally or in any gateways.</span></span> <span data-ttu-id="1ce43-151">Identico al valore preferito, [**il \_ flag \_ Internet \_ Nessuna \_ scrittura nella cache**](api-flags.md).</span><span class="sxs-lookup"><span data-stu-id="1ce43-151">Identical to the preferred value, [**INTERNET\_FLAG\_NO\_CACHE\_WRITE**](api-flags.md).</span></span>                                                                                                                                                                                                                                                                                 |
|                                                                                                                                                        | <span data-ttu-id="1ce43-152">Indica che si tratta di un invio di form.</span><span class="sxs-lookup"><span data-stu-id="1ce43-152">Indicates that this is a Forms submission.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="1ce43-153">[**Internet \_ flag inviato dal flag Internet \_ \_ della cache**](api-flags.md)[**\_ \_ \_ Invia form**](api-flags.md)</span><span class="sxs-lookup"><span data-stu-id="1ce43-153">[**INTERNET\_FLAG\_FROM\_CACHE**](api-flags.md)[**INTERNET\_FLAG\_FORMS\_SUBMIT**](api-flags.md)</span></span> | <span data-ttu-id="1ce43-154">Non esegue richieste di rete.</span><span class="sxs-lookup"><span data-stu-id="1ce43-154">Does not make network requests.</span></span> <span data-ttu-id="1ce43-155">Tutte le entità vengono restituite dalla cache.</span><span class="sxs-lookup"><span data-stu-id="1ce43-155">All entities are returned from the cache.</span></span> <span data-ttu-id="1ce43-156">Se l'elemento richiesto non è presente nella cache, viene restituito un errore appropriato, ad esempio file di errore \_ \_ non \_ trovato.</span><span class="sxs-lookup"><span data-stu-id="1ce43-156">If the requested item is not in the cache, a suitable error, such as ERROR\_FILE\_NOT\_FOUND, is returned.</span></span> <span data-ttu-id="1ce43-157">Solo la funzione [**Internetopn**](/windows/desktop/api/Wininet/nf-wininet-internetopena) usa questo flag.</span><span class="sxs-lookup"><span data-stu-id="1ce43-157">Only the [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) function uses this flag.</span></span>                                                                                                                                                                                                       |
| [<span data-ttu-id="1ce43-158">**\_nuovo flag Internet \_ FWD \_**</span><span class="sxs-lookup"><span data-stu-id="1ce43-158">**INTERNET\_FLAG\_FWD\_BACK**</span></span>](api-flags.md)                                                                                  | <span data-ttu-id="1ce43-159">Indica che la funzione deve utilizzare la copia della risorsa attualmente nella cache Internet.</span><span class="sxs-lookup"><span data-stu-id="1ce43-159">Indicates that the function should use the copy of the resource that is currently in the Internet cache.</span></span> <span data-ttu-id="1ce43-160">La data di scadenza e altre informazioni sulla risorsa non sono controllate.</span><span class="sxs-lookup"><span data-stu-id="1ce43-160">The expiration date and other information about the resource is not checked.</span></span> <span data-ttu-id="1ce43-161">Se l'elemento richiesto non viene trovato nella cache Internet, il sistema tenta di individuare la risorsa nella rete.</span><span class="sxs-lookup"><span data-stu-id="1ce43-161">If the requested item is not found in the Internet cache, the system attempts to locate the resource on the network.</span></span> <span data-ttu-id="1ce43-162">Questo valore è stato introdotto in Microsoft Internet Explorer 5 ed è associato alle operazioni dei pulsanti **Avanti** e **indietro** di Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="1ce43-162">This value was introduced in Microsoft Internet Explorer 5 and is associated with the **Forward** and **Back** button operations of Internet Explorer.</span></span> |
| [<span data-ttu-id="1ce43-163">**\_ \_ collegamento ipertestuale flag Internet**</span><span class="sxs-lookup"><span data-stu-id="1ce43-163">**INTERNET\_FLAG\_HYPERLINK**</span></span>](api-flags.md)                                                                                 | <span data-ttu-id="1ce43-164">Impone all'applicazione di ricaricare una risorsa se non è stata restituita alcuna ora di scadenza e se la risorsa è stata archiviata nella cache.</span><span class="sxs-lookup"><span data-stu-id="1ce43-164">Forces the application to reload a resource if no expire time and no last-modified time were returned when the resource was stored in the cache.</span></span>                                                                                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="1ce43-165">**FLAG INTERNET che \_ \_ rende \_ persistente**</span><span class="sxs-lookup"><span data-stu-id="1ce43-165">**INTERNET\_FLAG\_MAKE\_PERSISTENT**</span></span>](api-flags.md)                                                                    | <span data-ttu-id="1ce43-166">Non più supportata.</span><span class="sxs-lookup"><span data-stu-id="1ce43-166">No longer supported.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="1ce43-167">**il \_ flag Internet \_ deve \_ memorizzare nella cache la \_ richiesta**</span><span class="sxs-lookup"><span data-stu-id="1ce43-167">**INTERNET\_FLAG\_MUST\_CACHE\_REQUEST**</span></span>](api-flags.md)                                                             | <span data-ttu-id="1ce43-168">Determina la creazione di un file temporaneo se il file non può essere memorizzato nella cache.</span><span class="sxs-lookup"><span data-stu-id="1ce43-168">Causes a temporary file to be created if the file cannot be cached.</span></span> <span data-ttu-id="1ce43-169">Si tratta di un valore identico a quello preferito, il [**\_ file di \_ richiesta \_ del flag Internet**](api-flags.md).</span><span class="sxs-lookup"><span data-stu-id="1ce43-169">This is identical to the preferred value, [**INTERNET\_FLAG\_NEED\_FILE**](api-flags.md).</span></span>                                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="1ce43-170">**\_file con flag Internet \_ necessario \_**</span><span class="sxs-lookup"><span data-stu-id="1ce43-170">**INTERNET\_FLAG\_NEED\_FILE**</span></span>](api-flags.md)                                                                                | <span data-ttu-id="1ce43-171">Determina la creazione di un file temporaneo se il file non può essere memorizzato nella cache.</span><span class="sxs-lookup"><span data-stu-id="1ce43-171">Causes a temporary file to be created if the file cannot be cached.</span></span>                                                                                                                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="1ce43-172">**\_flag Internet \_ senza \_ \_ scrittura cache**</span><span class="sxs-lookup"><span data-stu-id="1ce43-172">**INTERNET\_FLAG\_NO\_CACHE\_WRITE**</span></span>](api-flags.md)                                                                     | <span data-ttu-id="1ce43-173">Rifiuta qualsiasi tentativo da parte della funzione di archiviare i dati scaricati da Internet nella cache.</span><span class="sxs-lookup"><span data-stu-id="1ce43-173">Rejects any attempt by the function to store data downloaded from the Internet in the cache.</span></span> <span data-ttu-id="1ce43-174">Questo flag è necessario se l'applicazione non desidera che le risorse scaricate vengano archiviate localmente.</span><span class="sxs-lookup"><span data-stu-id="1ce43-174">This flag is necessary if the application does not want any downloaded resources to be stored locally.</span></span>                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="1ce43-175">**\_flag Internet \_ Nessuna \_ interfaccia utente**</span><span class="sxs-lookup"><span data-stu-id="1ce43-175">**INTERNET\_FLAG\_NO\_UI**</span></span>](api-flags.md)                                                                                        | <span data-ttu-id="1ce43-176">Disabilita la finestra di dialogo dei cookie.</span><span class="sxs-lookup"><span data-stu-id="1ce43-176">Disables the cookie dialog box.</span></span> <span data-ttu-id="1ce43-177">Questo flag può essere usato da [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (solo richieste http).</span><span class="sxs-lookup"><span data-stu-id="1ce43-177">This flag can be used by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (HTTP requests only).</span></span>                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="1ce43-178">**\_flag Internet \_ offline**</span><span class="sxs-lookup"><span data-stu-id="1ce43-178">**INTERNET\_FLAG\_OFFLINE**</span></span>](api-flags.md)                                                                                     | <span data-ttu-id="1ce43-179">Impedisce all'applicazione di inviare richieste alla rete.</span><span class="sxs-lookup"><span data-stu-id="1ce43-179">Prevents the application from sending requests to the network.</span></span> <span data-ttu-id="1ce43-180">Tutte le richieste vengono risolte utilizzando le risorse archiviate nella cache.</span><span class="sxs-lookup"><span data-stu-id="1ce43-180">All requests are resolved using the resources stored in the cache.</span></span> <span data-ttu-id="1ce43-181">Se la risorsa non è presente nella cache, viene restituito un errore appropriato, ad esempio file di errore \_ \_ non \_ trovato.</span><span class="sxs-lookup"><span data-stu-id="1ce43-181">If the resource is not in the cache, a suitable error, such as ERROR\_FILE\_NOT\_FOUND, is returned.</span></span>                                                                                                                                                                                                                            |
| [<span data-ttu-id="1ce43-182">**\_flag Internet \_ pragma \_ NoCache**</span><span class="sxs-lookup"><span data-stu-id="1ce43-182">**INTERNET\_FLAG\_PRAGMA\_NOCACHE**</span></span>](api-flags.md)                                                                      | <span data-ttu-id="1ce43-183">Impone la risoluzione della richiesta da parte del server di origine, anche se nel proxy esiste una copia memorizzata nella cache.</span><span class="sxs-lookup"><span data-stu-id="1ce43-183">Forces the request to be resolved by the origin server, even if a cached copy exists on the proxy.</span></span> <span data-ttu-id="1ce43-184">La funzione [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (solo per le richieste HTTP e HTTPS) e la funzione [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) usano questo flag.</span><span class="sxs-lookup"><span data-stu-id="1ce43-184">The [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) function (on HTTP and HTTPS requests only) and [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) function use this flag.</span></span>                                                                                                                                                                                               |
| [<span data-ttu-id="1ce43-185">**\_ricarica del flag Internet \_**</span><span class="sxs-lookup"><span data-stu-id="1ce43-185">**INTERNET\_FLAG\_RELOAD**</span></span>](api-flags.md)                                                                                       | <span data-ttu-id="1ce43-186">Impone la funzione per recuperare la risorsa richiesta direttamente da Internet.</span><span class="sxs-lookup"><span data-stu-id="1ce43-186">Forces the function to retrieve the requested resource directly from the Internet.</span></span> <span data-ttu-id="1ce43-187">Le informazioni scaricate vengono memorizzate nella cache.</span><span class="sxs-lookup"><span data-stu-id="1ce43-187">The information that is downloaded is stored in the cache.</span></span>                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="1ce43-188">**risincronizzazione del \_ flag Internet \_**</span><span class="sxs-lookup"><span data-stu-id="1ce43-188">**INTERNET\_FLAG\_RESYNCHRONIZE**</span></span>](api-flags.md)                                                                         | <span data-ttu-id="1ce43-189">Fa in modo che un'applicazione esegua un download condizionale della risorsa da Internet.</span><span class="sxs-lookup"><span data-stu-id="1ce43-189">Causes an application to perform a conditional download of the resource from the Internet.</span></span> <span data-ttu-id="1ce43-190">Se la versione archiviata nella cache è aggiornata, le informazioni vengono scaricate dalla cache.</span><span class="sxs-lookup"><span data-stu-id="1ce43-190">If the version stored in the cache is current, the information is downloaded from the cache.</span></span> <span data-ttu-id="1ce43-191">In caso contrario, le informazioni vengono ricaricate dal server.</span><span class="sxs-lookup"><span data-stu-id="1ce43-191">Otherwise, the information is reloaded from the server.</span></span>                                                                                                                                                                                                                   |



 

## <a name="persistent-caching-functions"></a><span data-ttu-id="1ce43-192">Funzioni di Caching permanenti</span><span class="sxs-lookup"><span data-stu-id="1ce43-192">Persistent Caching Functions</span></span>

<span data-ttu-id="1ce43-193">I client che necessitano di servizi di memorizzazione nella cache permanenti utilizzano le funzioni di Caching permanenti per consentire alle applicazioni di salvare i dati nella file system locale per un uso successivo, ad esempio in situazioni in cui un collegamento a larghezza di banda ridotta limita l'accesso ai dati o l'accesso non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="1ce43-193">Clients that need persistent caching services use the persistent caching functions to allow their applications to save data in the local file system for subsequent use, such as in situations where a low-bandwidth link limits access to the data, or the access is not available at all.</span></span>

<span data-ttu-id="1ce43-194">Le funzioni della cache forniscono la memorizzazione nella cache persistente e l'esplorazione offline.</span><span class="sxs-lookup"><span data-stu-id="1ce43-194">The cache functions provide persistent caching and offline browsing.</span></span> <span data-ttu-id="1ce43-195">A meno che non venga specificato in modo esplicito nessun flag di [**\_ \_ \_ \_ scrittura**](api-flags.md) nella cache, le funzioni memorizzano nella cache tutti i dati scaricati dalla rete.</span><span class="sxs-lookup"><span data-stu-id="1ce43-195">Unless the [**INTERNET\_FLAG\_NO\_CACHE\_WRITE**](api-flags.md) flag explicitly specifies no caching, the functions cache all data downloaded from the network.</span></span> <span data-ttu-id="1ce43-196">Le risposte ai dati POST non vengono memorizzate nella cache.</span><span class="sxs-lookup"><span data-stu-id="1ce43-196">The responses to POST data are not cached.</span></span>

## <a name="using-the-persistent-url-cache-functions"></a><span data-ttu-id="1ce43-197">Uso delle funzioni di cache URL persistenti</span><span class="sxs-lookup"><span data-stu-id="1ce43-197">Using the Persistent URL Cache Functions</span></span>

<span data-ttu-id="1ce43-198">Le seguenti funzioni di cache URL persistenti consentono a un'applicazione di accedere e modificare le informazioni archiviate nella cache.</span><span class="sxs-lookup"><span data-stu-id="1ce43-198">The following persistent URL cache functions allow an application to access and manipulate information stored in the cache.</span></span>



| <span data-ttu-id="1ce43-199">Funzione</span><span class="sxs-lookup"><span data-stu-id="1ce43-199">Function</span></span>                                                           | <span data-ttu-id="1ce43-200">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1ce43-200">Description</span></span>                                                                                                                                                   |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1ce43-201">**CommitUrlCacheEntryA**</span><span class="sxs-lookup"><span data-stu-id="1ce43-201">**CommitUrlCacheEntryA**</span></span>](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya)               | <span data-ttu-id="1ce43-202">Memorizza nella cache i dati nel file specificato nell'archivio della cache e li associa all'URL specificato.</span><span class="sxs-lookup"><span data-stu-id="1ce43-202">Caches data in the specified file in the cache storage and associates it with the given URL.</span></span>                                                                  |
| [<span data-ttu-id="1ce43-203">**CommitUrlCacheEntryW**</span><span class="sxs-lookup"><span data-stu-id="1ce43-203">**CommitUrlCacheEntryW**</span></span>](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentryw)               | <span data-ttu-id="1ce43-204">Memorizza nella cache i dati nel file specificato nell'archivio della cache e li associa all'URL specificato.</span><span class="sxs-lookup"><span data-stu-id="1ce43-204">Caches data in the specified file in the cache storage and associates it with the given URL.</span></span>                                                                  |
| [<span data-ttu-id="1ce43-205">**CreateUrlCacheEntry**</span><span class="sxs-lookup"><span data-stu-id="1ce43-205">**CreateUrlCacheEntry**</span></span>](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya)                 | <span data-ttu-id="1ce43-206">Alloca l'archiviazione della cache richiesta e crea un nome di file locale per salvare la voce della cache che corrisponde al nome dell'origine.</span><span class="sxs-lookup"><span data-stu-id="1ce43-206">Allocates the requested cache storage and creates a local file name for saving the cache entry that corresponds to the source name.</span></span>                           |
| [<span data-ttu-id="1ce43-207">**CreateUrlCacheGroup**</span><span class="sxs-lookup"><span data-stu-id="1ce43-207">**CreateUrlCacheGroup**</span></span>](/windows/desktop/api/Wininet/nf-wininet-createurlcachegroup)                 | <span data-ttu-id="1ce43-208">Genera un'identificazione del gruppo di cache.</span><span class="sxs-lookup"><span data-stu-id="1ce43-208">Generates a cache group identification.</span></span>                                                                                                                       |
| [<span data-ttu-id="1ce43-209">**DeleteUrlCacheEntry**</span><span class="sxs-lookup"><span data-stu-id="1ce43-209">**DeleteUrlCacheEntry**</span></span>](/windows/desktop/api/Wininet/nf-wininet-deleteurlcacheentry)                 | <span data-ttu-id="1ce43-210">Rimuove il file associato al nome di origine dalla cache, se il file esiste.</span><span class="sxs-lookup"><span data-stu-id="1ce43-210">Removes the file associated with the source name from the cache, if the file exists.</span></span>                                                                          |
| [<span data-ttu-id="1ce43-211">**DeleteUrlCacheGroup**</span><span class="sxs-lookup"><span data-stu-id="1ce43-211">**DeleteUrlCacheGroup**</span></span>](/windows/desktop/api/Wininet/nf-wininet-deleteurlcachegroup)                 | <span data-ttu-id="1ce43-212">Rilascia un **GROUPID** e qualsiasi stato associato nel file di indice della cache.</span><span class="sxs-lookup"><span data-stu-id="1ce43-212">Releases a **GROUPID** and any associated state in the cache index file.</span></span>                                                                                      |
| [<span data-ttu-id="1ce43-213">**FindCloseUrlCache**</span><span class="sxs-lookup"><span data-stu-id="1ce43-213">**FindCloseUrlCache**</span></span>](/windows/desktop/api/Wininet/nf-wininet-findcloseurlcache)                     | <span data-ttu-id="1ce43-214">Chiude l'handle di enumerazione specificato.</span><span class="sxs-lookup"><span data-stu-id="1ce43-214">Closes the specified enumeration handle.</span></span>                                                                                                                      |
| [<span data-ttu-id="1ce43-215">**FindFirstUrlCacheEntry**</span><span class="sxs-lookup"><span data-stu-id="1ce43-215">**FindFirstUrlCacheEntry**</span></span>](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya)           | <span data-ttu-id="1ce43-216">Inizia l'enumerazione della cache.</span><span class="sxs-lookup"><span data-stu-id="1ce43-216">Begins the enumeration of the cache.</span></span>                                                                                                                          |
| [<span data-ttu-id="1ce43-217">**FindFirstUrlCacheEntryEx**</span><span class="sxs-lookup"><span data-stu-id="1ce43-217">**FindFirstUrlCacheEntryEx**</span></span>](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentryexa)       | <span data-ttu-id="1ce43-218">Avvia un'enumerazione filtrata della cache.</span><span class="sxs-lookup"><span data-stu-id="1ce43-218">Begins a filtered enumeration of the cache.</span></span>                                                                                                                   |
| [<span data-ttu-id="1ce43-219">**FindNextUrlCacheEntry**</span><span class="sxs-lookup"><span data-stu-id="1ce43-219">**FindNextUrlCacheEntry**</span></span>](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentrya)             | <span data-ttu-id="1ce43-220">Recupera la voce successiva nella cache.</span><span class="sxs-lookup"><span data-stu-id="1ce43-220">Retrieves the next entry in the cache.</span></span>                                                                                                                        |
| [<span data-ttu-id="1ce43-221">**FindNextUrlCacheEntryEx**</span><span class="sxs-lookup"><span data-stu-id="1ce43-221">**FindNextUrlCacheEntryEx**</span></span>](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentryexa)         | <span data-ttu-id="1ce43-222">Recupera la voce successiva in un'enumerazione della cache filtrata.</span><span class="sxs-lookup"><span data-stu-id="1ce43-222">Retrieves the next entry in a filtered cache enumeration.</span></span>                                                                                                     |
| [<span data-ttu-id="1ce43-223">**GetUrlCacheEntryInfo**</span><span class="sxs-lookup"><span data-stu-id="1ce43-223">**GetUrlCacheEntryInfo**</span></span>](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa)               | <span data-ttu-id="1ce43-224">Recupera le informazioni su una voce della cache.</span><span class="sxs-lookup"><span data-stu-id="1ce43-224">Retrieves information about a cache entry.</span></span>                                                                                                                    |
| [<span data-ttu-id="1ce43-225">**GetUrlCacheEntryInfoEx**</span><span class="sxs-lookup"><span data-stu-id="1ce43-225">**GetUrlCacheEntryInfoEx**</span></span>](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoexa)           | <span data-ttu-id="1ce43-226">Cerca l'URL dopo aver tradotto tutti i reindirizzamenti memorizzati nella cache che verrebbero applicati in modalità offline da [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span><span class="sxs-lookup"><span data-stu-id="1ce43-226">Searches for the URL after translating any cached redirections that would be applied in offline mode by [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span></span>           |
| [<span data-ttu-id="1ce43-227">**ReadUrlCacheEntryStream**</span><span class="sxs-lookup"><span data-stu-id="1ce43-227">**ReadUrlCacheEntryStream**</span></span>](/windows/desktop/api/Wininet/nf-wininet-readurlcacheentrystream)         | <span data-ttu-id="1ce43-228">Legge i dati memorizzati nella cache da un flusso aperto utilizzando [**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama).</span><span class="sxs-lookup"><span data-stu-id="1ce43-228">Reads the cached data from a stream that has been opened using [**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama).</span></span>                            |
| [<span data-ttu-id="1ce43-229">**RetrieveUrlCacheEntryFile**</span><span class="sxs-lookup"><span data-stu-id="1ce43-229">**RetrieveUrlCacheEntryFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea)     | <span data-ttu-id="1ce43-230">Recupera una voce della cache dalla cache sotto forma di file.</span><span class="sxs-lookup"><span data-stu-id="1ce43-230">Retrieves a cache entry from the cache in the form of a file.</span></span>                                                                                                 |
| [<span data-ttu-id="1ce43-231">**RetrieveUrlCacheEntryStream**</span><span class="sxs-lookup"><span data-stu-id="1ce43-231">**RetrieveUrlCacheEntryStream**</span></span>](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama) | <span data-ttu-id="1ce43-232">Fornisce il modo più efficiente e indipendente dall'implementazione per accedere ai dati della cache.</span><span class="sxs-lookup"><span data-stu-id="1ce43-232">Provides the most efficient and implementation-independent way of accessing the cache data.</span></span>                                                                   |
| [<span data-ttu-id="1ce43-233">**SetUrlCacheEntryGroup**</span><span class="sxs-lookup"><span data-stu-id="1ce43-233">**SetUrlCacheEntryGroup**</span></span>](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentrygroup)             | <span data-ttu-id="1ce43-234">Aggiunge o rimuove voci da un gruppo di cache.</span><span class="sxs-lookup"><span data-stu-id="1ce43-234">Adds or removes entries from a cache group.</span></span>                                                                                                                   |
| [<span data-ttu-id="1ce43-235">**SetUrlCacheEntryInfo**</span><span class="sxs-lookup"><span data-stu-id="1ce43-235">**SetUrlCacheEntryInfo**</span></span>](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentryinfoa)               | <span data-ttu-id="1ce43-236">Imposta i membri specificati della struttura [**delle \_ \_ \_ informazioni sulla voce della cache Internet**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) .</span><span class="sxs-lookup"><span data-stu-id="1ce43-236">Sets the specified members of the [**INTERNET\_CACHE\_ENTRY\_INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) structure.</span></span>                                                |
| [<span data-ttu-id="1ce43-237">**UnlockUrlCacheEntryFile**</span><span class="sxs-lookup"><span data-stu-id="1ce43-237">**UnlockUrlCacheEntryFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentryfile)         | <span data-ttu-id="1ce43-238">Sblocca la voce della cache che è stata bloccata quando il file è stato recuperato per l'uso dalla cache da parte di [**RetrieveUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea).</span><span class="sxs-lookup"><span data-stu-id="1ce43-238">Unlocks the cache entry that was locked when the file was retrieved for use from the cache by [**RetrieveUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea).</span></span> |
| [<span data-ttu-id="1ce43-239">**UnlockUrlCacheEntryStream**</span><span class="sxs-lookup"><span data-stu-id="1ce43-239">**UnlockUrlCacheEntryStream**</span></span>](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentrystream)     | <span data-ttu-id="1ce43-240">Chiude il flusso recuperato utilizzando [**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama).</span><span class="sxs-lookup"><span data-stu-id="1ce43-240">Closes the stream that has been retrieved using [**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama).</span></span>                                           |



 

### <a name="enumerating-the-cache"></a><span data-ttu-id="1ce43-241">Enumerazione della cache</span><span class="sxs-lookup"><span data-stu-id="1ce43-241">Enumerating the Cache</span></span>

<span data-ttu-id="1ce43-242">Le funzioni [**FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya) e [**FindNextUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentrya) enumerano le informazioni archiviate nella cache.</span><span class="sxs-lookup"><span data-stu-id="1ce43-242">The [**FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya) and [**FindNextUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentrya) functions enumerate the information stored in the cache.</span></span> <span data-ttu-id="1ce43-243">[**FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya) avvia l'enumerazione accettando un criterio di ricerca, un buffer e una dimensione del buffer per creare un handle e restituire la prima voce della cache.</span><span class="sxs-lookup"><span data-stu-id="1ce43-243">[**FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya) starts the enumeration by taking a search pattern, a buffer, and a buffer size to create a handle and return the first cache entry.</span></span> <span data-ttu-id="1ce43-244">[**FindNextUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentrya) accetta l'handle creato da [**FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya), un buffer e una dimensione del buffer per restituire la voce della cache successiva.</span><span class="sxs-lookup"><span data-stu-id="1ce43-244">[**FindNextUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentrya) takes the handle created by [**FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya), a buffer, and a buffer size to return the next cache entry.</span></span>

<span data-ttu-id="1ce43-245">Entrambe le funzioni archiviano una struttura di [**\_ \_ \_ informazioni sulla voce della cache Internet**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) nel buffer.</span><span class="sxs-lookup"><span data-stu-id="1ce43-245">Both functions store an [**INTERNET\_CACHE\_ENTRY\_INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) structure in the buffer.</span></span> <span data-ttu-id="1ce43-246">La dimensione di questa struttura varia per ogni voce.</span><span class="sxs-lookup"><span data-stu-id="1ce43-246">The size of this structure varies for each entry.</span></span> <span data-ttu-id="1ce43-247">Se la dimensione del buffer passata a una delle due funzioni è insufficiente, la funzione ha esito negativo e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce un errore di \_ buffer insufficiente \_ .</span><span class="sxs-lookup"><span data-stu-id="1ce43-247">If the buffer size passed to either function is insufficient, the function fails and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INSUFFICIENT\_BUFFER.</span></span> <span data-ttu-id="1ce43-248">La variabile della dimensione del buffer contiene la dimensione del buffer necessaria per recuperare la voce della cache.</span><span class="sxs-lookup"><span data-stu-id="1ce43-248">The buffer size variable contains the buffer size that was needed to retrieve that cache entry.</span></span> <span data-ttu-id="1ce43-249">È necessario allocare un buffer della dimensione indicata dalla variabile della dimensione del buffer e la funzione deve essere chiamata nuovamente con il nuovo buffer.</span><span class="sxs-lookup"><span data-stu-id="1ce43-249">A buffer of the size indicated by the buffer size variable should be allocated, and the function should be called again with the new buffer.</span></span>

<span data-ttu-id="1ce43-250">La struttura delle [**\_ \_ \_ informazioni sulla voce della cache Internet**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) contiene le dimensioni della struttura, l'URL delle informazioni memorizzate nella cache, il nome del file locale, il tipo di voce della cache, il conteggio di utilizzo, la frequenza di riscontri, le dimensioni, l'ora dell'Ultima modifica, la scadenza, l'ultimo accesso, l'ora dell'ultima sincronizzazione, le informazioni di intestazione,</span><span class="sxs-lookup"><span data-stu-id="1ce43-250">The [**INTERNET\_CACHE\_ENTRY\_INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) structure contains the structure size, URL of the cached information, local file name, cache entry type, use count, hit rate, size, last modified time, expiration, last access, last synchronized time, header information, header information size, and file name extension.</span></span>

<span data-ttu-id="1ce43-251">La funzione [**FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya) accetta un criterio di ricerca, un buffer che archivia la struttura delle [**\_ \_ \_ informazioni sulla voce della cache Internet**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) e le dimensioni del buffer.</span><span class="sxs-lookup"><span data-stu-id="1ce43-251">The [**FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya) function takes a search pattern, a buffer that stores the [**INTERNET\_CACHE\_ENTRY\_INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) structure, and the buffer size.</span></span> <span data-ttu-id="1ce43-252">Attualmente, viene implementato solo il criterio di ricerca predefinito, che restituisce tutte le voci della cache.</span><span class="sxs-lookup"><span data-stu-id="1ce43-252">Currently, only the default search pattern, which returns all cache entries, is implemented.</span></span>

<span data-ttu-id="1ce43-253">Dopo che la cache è stata enumerata, l'applicazione deve chiamare [**FindCloseUrlCache**](/windows/desktop/api/Wininet/nf-wininet-findcloseurlcache) per chiudere l'handle di enumerazione della cache.</span><span class="sxs-lookup"><span data-stu-id="1ce43-253">After the cache is enumerated, the application should call [**FindCloseUrlCache**](/windows/desktop/api/Wininet/nf-wininet-findcloseurlcache) to close the cache enumeration handle.</span></span>

<span data-ttu-id="1ce43-254">Nell'esempio seguente viene visualizzato l'URL di ogni voce della cache in una casella di riepilogo, ovvero **IDC \_**.</span><span class="sxs-lookup"><span data-stu-id="1ce43-254">The following example displays each cache entry's URL in a list box, **IDC\_CacheList**.</span></span> <span data-ttu-id="1ce43-255">USA \_ \_ \_ la dimensione massima delle informazioni sulla voce della cache \_ per allocare inizialmente un buffer, perché le versioni precedenti dell'API WinInet non enumerano la cache in modo corretto.</span><span class="sxs-lookup"><span data-stu-id="1ce43-255">It uses MAX\_CACHE\_ENTRY\_INFO\_SIZE to initially allocate a buffer, since early versions of the WinINet API do not enumerate the cache properly otherwise.</span></span> <span data-ttu-id="1ce43-256">Le versioni successive enumerano correttamente la cache e non è previsto alcun limite per le dimensioni della cache.</span><span class="sxs-lookup"><span data-stu-id="1ce43-256">Later versions do enumerate the cache properly and there is no cache size limit.</span></span> <span data-ttu-id="1ce43-257">Tutte le applicazioni in esecuzione su computer con la versione dell'API WinINet da Internet Explorer 4,0 devono allocare un buffer con le dimensioni richieste.</span><span class="sxs-lookup"><span data-stu-id="1ce43-257">All applications that run on computers with the version of the WinINet API from Internet Explorer 4.0 must allocate a buffer of the required size.</span></span> <span data-ttu-id="1ce43-258">Per ulteriori informazioni, vedere [utilizzo dei buffer](appendix-b-using-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="1ce43-258">For more information, see [Using Buffers](appendix-b-using-buffers.md).</span></span>


```C++
int WINAPI EnumerateCacheOld(HWND hX)
{
    DWORD dwEntrySize;
    LPINTERNET_CACHE_ENTRY_INFO lpCacheEntry;
    DWORD MAX_CACHE_ENTRY_INFO_SIZE = 4096;
    HANDLE hCacheDir;
    int nCount=0;

    SendDlgItemMessage(hX,IDC_CacheList,LB_RESETCONTENT,0,0);
    
    SetCursor(LoadCursor(NULL,IDC_WAIT));

    dwEntrySize = MAX_CACHE_ENTRY_INFO_SIZE;
    lpCacheEntry = (LPINTERNET_CACHE_ENTRY_INFO) new char[dwEntrySize];
    lpCacheEntry->dwStructSize = dwEntrySize;

again:

    hCacheDir = FindFirstUrlCacheEntry(NULL,
                                       lpCacheEntry,
                                       &dwEntrySize);
    if (!hCacheDir)                                             
    {
        delete[]lpCacheEntry;
        switch(GetLastError())
        {
            case ERROR_NO_MORE_ITEMS: 
                TCHAR tempout[80];
                _stprintf_s(tempout, 
                            80,   
                            TEXT("The number of cache entries = %d \n"),
                            nCount);
                MessageBox(hX,tempout,TEXT("Cache Enumeration"),MB_OK);
                FindCloseUrlCache(hCacheDir);
                SetCursor(LoadCursor(NULL,IDC_ARROW));
                return TRUE;
                break;
            case ERROR_INSUFFICIENT_BUFFER:
                lpCacheEntry = (LPINTERNET_CACHE_ENTRY_INFO) 
                                new char[dwEntrySize];
                lpCacheEntry->dwStructSize = dwEntrySize;
                goto again;
                break;
            default:
                ErrorOut( hX,GetLastError(),
                          TEXT("FindNextUrlCacheEntry Init"));
                FindCloseUrlCache(hCacheDir);
                SetCursor(LoadCursor(NULL,IDC_ARROW));
                return FALSE;
        }
    }

    SendDlgItemMessage(hX,IDC_CacheList,LB_ADDSTRING,
                       0,(LPARAM)(lpCacheEntry->lpszSourceUrlName));
    nCount++;
    delete (lpCacheEntry);

    do 
    {
        dwEntrySize = MAX_CACHE_ENTRY_INFO_SIZE;
        lpCacheEntry = (LPINTERNET_CACHE_ENTRY_INFO) new char[dwEntrySize];
        lpCacheEntry->dwStructSize = dwEntrySize;

retry:
        if (!FindNextUrlCacheEntry(hCacheDir,
                                   lpCacheEntry, 
                                   &dwEntrySize))
        {
            delete[]lpCacheEntry;
            switch(GetLastError())
            {
                case ERROR_NO_MORE_ITEMS: 
                    TCHAR tempout[80];
                    _stprintf_s(tempout,
                                80,
                                TEXT("The number of cache entries = %d \n"),nCount);
                    MessageBox(hX,
                               tempout,
                               TEXT("Cache Enumeration"),MB_OK);
                    FindCloseUrlCache(hCacheDir);
                    return TRUE;
                    break;
                case ERROR_INSUFFICIENT_BUFFER:
                    lpCacheEntry = 
                             (LPINTERNET_CACHE_ENTRY_INFO) 
                              new char[dwEntrySize];
                    lpCacheEntry->dwStructSize = dwEntrySize;
                    goto retry;
                    break;
                default:
                    ErrorOut(hX,
                             GetLastError(),
                             TEXT("FindNextUrlCacheEntry Init"));
                    FindCloseUrlCache(hCacheDir);
                    return FALSE;
            }
        }

        SendDlgItemMessage(hX,
                           IDC_CacheList,LB_ADDSTRING,
                           0,
                          (LPARAM)(lpCacheEntry->lpszSourceUrlName));
        nCount++;
        delete[] lpCacheEntry;        
    }  while (TRUE);

    SetCursor(LoadCursor(NULL,IDC_ARROW));
    return TRUE;        
}
```



### <a name="retrieving-cache-entry-information"></a><span data-ttu-id="1ce43-259">Recupero delle informazioni sulla voce della cache</span><span class="sxs-lookup"><span data-stu-id="1ce43-259">Retrieving Cache Entry Information</span></span>

<span data-ttu-id="1ce43-260">La funzione [**GetUrlCacheEntryInfo**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa) consente di recuperare la struttura delle [**\_ \_ \_ informazioni sulla voce della cache Internet**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) per l'URL specificato.</span><span class="sxs-lookup"><span data-stu-id="1ce43-260">The [**GetUrlCacheEntryInfo**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa) function lets you retrieve the [**INTERNET\_CACHE\_ENTRY\_INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) structure for the specified URL.</span></span> <span data-ttu-id="1ce43-261">Questa struttura contiene le dimensioni della struttura, l'URL delle informazioni memorizzate nella cache, il nome del file locale, il tipo di voce della cache, il conteggio di utilizzo, la velocità di hit, le dimensioni, l'ora dell'Ultima modifica, la scadenza, l'ultimo accesso, l'ora dell'ultima sincronizzazione, le informazioni di intestazione, le dimensioni delle informazioni</span><span class="sxs-lookup"><span data-stu-id="1ce43-261">This structure contains the structure size, URL of the cached information, local file name, cache entry type, use count, hit rate, size, last modified time, expiration, last access, last synchronized time, header information, header information size, and file name extension.</span></span>

<span data-ttu-id="1ce43-262">[**GetUrlCacheEntryInfo**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa) accetta un URL, un buffer per la struttura delle [**\_ \_ \_ informazioni sulla voce della cache Internet**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) e le dimensioni del buffer.</span><span class="sxs-lookup"><span data-stu-id="1ce43-262">[**GetUrlCacheEntryInfo**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa) accepts a URL, a buffer for an [**INTERNET\_CACHE\_ENTRY\_INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) structure, and the buffer size.</span></span> <span data-ttu-id="1ce43-263">Se l'URL viene trovato, le informazioni vengono copiate nel buffer.</span><span class="sxs-lookup"><span data-stu-id="1ce43-263">If the URL is found, the information is copied into the buffer.</span></span> <span data-ttu-id="1ce43-264">In caso contrario, la funzione ha esito negativo e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce il file di errore \_ \_ non \_ trovato.</span><span class="sxs-lookup"><span data-stu-id="1ce43-264">Otherwise, the function fails and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_FILE\_NOT\_FOUND.</span></span> <span data-ttu-id="1ce43-265">Se la dimensione del buffer non è sufficiente per archiviare le informazioni sulla voce della cache, la funzione ha esito negativo e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce un errore di \_ buffer insufficiente \_ .</span><span class="sxs-lookup"><span data-stu-id="1ce43-265">If the buffer size is insufficient to store the cache entry information, the function fails and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INSUFFICIENT\_BUFFER.</span></span> <span data-ttu-id="1ce43-266">Le dimensioni necessarie per recuperare le informazioni vengono archiviate nella variabile di dimensione del buffer.</span><span class="sxs-lookup"><span data-stu-id="1ce43-266">The size required to retrieve the information is stored in the buffer size variable.</span></span>

<span data-ttu-id="1ce43-267">[**GetUrlCacheEntryInfo**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa) non esegue l'analisi dell'URL, quindi un URL che contiene un ancoraggio ( \# ) non verrà trovato nella cache, anche se la risorsa è memorizzata nella cache.</span><span class="sxs-lookup"><span data-stu-id="1ce43-267">[**GetUrlCacheEntryInfo**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa) does not do any URL parsing, so a URL that contains an anchor (\#) will not be found in the cache, even if the resource is cached.</span></span> <span data-ttu-id="1ce43-268">Se, ad esempio, viene passato l'URL " https://example.com/example.htm\#sample ", la funzione restituisce il \_ file \_ di errore non \_ trovato anche se " https://example.com/example.htm " si trova nella cache.</span><span class="sxs-lookup"><span data-stu-id="1ce43-268">For example, if the URL "https://example.com/example.htm\#sample" is passed, the function returns ERROR\_FILE\_NOT\_FOUND even if "https://example.com/example.htm" is in the cache.</span></span>

<span data-ttu-id="1ce43-269">Nell'esempio seguente vengono recuperate le informazioni relative alla voce della cache per l'URL specificato.</span><span class="sxs-lookup"><span data-stu-id="1ce43-269">The following example retrieves the cache entry information for the specified URL.</span></span> <span data-ttu-id="1ce43-270">La funzione Visualizza quindi le informazioni di intestazione nella casella di modifica **IDC \_ CacheDump** .</span><span class="sxs-lookup"><span data-stu-id="1ce43-270">The function then displays the header information in the **IDC\_CacheDump** edit box.</span></span>


```C++
int WINAPI GetCacheEntryInfo(HWND hX,LPTSTR lpszUrl)
{
    DWORD dwEntrySize=0;
    LPINTERNET_CACHE_ENTRY_INFO lpCacheEntry;

    SetCursor(LoadCursor(NULL,IDC_WAIT));
    if (!GetUrlCacheEntryInfo(lpszUrl,NULL,&dwEntrySize))
    {
        if (GetLastError()!=ERROR_INSUFFICIENT_BUFFER)
        {
            ErrorOut(hX,GetLastError(),TEXT("GetUrlCacheEntryInfo"));
            SetCursor(LoadCursor(NULL,IDC_ARROW));
            return FALSE;
        }
        else
            lpCacheEntry = (LPINTERNET_CACHE_ENTRY_INFO) 
                            new char[dwEntrySize];
    }
    else
        return FALSE; // should not be successful w/ NULL buffer
                      // and 0 size

    if (!GetUrlCacheEntryInfo(lpszUrl,lpCacheEntry,&dwEntrySize))
    {
        ErrorOut(hX,GetLastError(),TEXT("GetUrlCacheEntryInfo"));
        SetCursor(LoadCursor(NULL,IDC_ARROW));
        return FALSE;
    }
    else
    {
        if ((lpCacheEntry->dwHeaderInfoSize)!=0)
        {
            LPSTR(lpCacheEntry->lpHeaderInfo)
                                [lpCacheEntry->dwHeaderInfoSize]=TEXT('\0');
            SetDlgItemText(hX,IDC_Headers,
                           lpCacheEntry->lpHeaderInfo);
        }
        else
        {
            SetDlgItemText(hX,IDC_Headers,TEXT("None"));
        }

        SetCursor(LoadCursor(NULL,IDC_ARROW));
        return TRUE;
    }
        
}
```



### <a name="creating-a-cache-entry"></a><span data-ttu-id="1ce43-271">Creazione di una voce della cache</span><span class="sxs-lookup"><span data-stu-id="1ce43-271">Creating a Cache Entry</span></span>

<span data-ttu-id="1ce43-272">Un'applicazione usa le funzioni [**CreateUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya) e [**CommitUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya) per creare una voce della cache.</span><span class="sxs-lookup"><span data-stu-id="1ce43-272">An application uses the [**CreateUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya) and [**CommitUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya) functions to create a cache entry.</span></span>

<span data-ttu-id="1ce43-273">[**CreateUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya) accetta l'URL, le dimensioni del file previsto e l'estensione del nome file.</span><span class="sxs-lookup"><span data-stu-id="1ce43-273">[**CreateUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya) accepts the URL, expected file size, and file name extension.</span></span> <span data-ttu-id="1ce43-274">La funzione crea quindi un nome file locale per salvare la voce della cache che corrisponde all'URL e all'estensione del nome di file.</span><span class="sxs-lookup"><span data-stu-id="1ce43-274">The function then creates a local file name for saving the cache entry that corresponds to the URL and file name extension.</span></span>

<span data-ttu-id="1ce43-275">Utilizzando il nome file locale, scrivere i dati nel file locale.</span><span class="sxs-lookup"><span data-stu-id="1ce43-275">Using the local file name, write the data into the local file.</span></span> <span data-ttu-id="1ce43-276">Dopo che i dati sono stati scritti nel file locale, l'applicazione deve chiamare [**CommitUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya).</span><span class="sxs-lookup"><span data-stu-id="1ce43-276">After the data has been written to the local file, the application should call [**CommitUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya).</span></span>

<span data-ttu-id="1ce43-277">[**CommitUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya) accetta l'URL, il nome file locale, la scadenza, l'ora dell'Ultima modifica, il tipo di voce della cache, le informazioni di intestazione, le dimensioni delle informazioni di intestazione e l'estensione del nome file.</span><span class="sxs-lookup"><span data-stu-id="1ce43-277">[**CommitUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya) accepts the URL, local file name, expiration, last modified time, cache entry type, header information, header information size, and file name extension.</span></span> <span data-ttu-id="1ce43-278">La funzione memorizza quindi nella cache i dati nel file specificato nell'archiviazione della cache e li associa all'URL specificato.</span><span class="sxs-lookup"><span data-stu-id="1ce43-278">The function then caches data in the file specified in the cache storage and associates it with the given URL.</span></span>

<span data-ttu-id="1ce43-279">Nell'esempio seguente viene usato il nome file locale, creato da una precedente chiamata a [**CreateUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya), archiviato nella casella di testo **IDC \_ LocalFile**, per archiviare il testo dalla casella di testo, **IDC \_ CacheDump**, nella voce della cache.</span><span class="sxs-lookup"><span data-stu-id="1ce43-279">The following example uses the local file name, created by a previous call to [**CreateUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya), stored in the text box, **IDC\_LocalFile**, to store the text from the text box, **IDC\_CacheDump**, in the cache entry.</span></span> <span data-ttu-id="1ce43-280">Dopo che i dati sono stati scritti nel file usando **fopen**, **fprintf** e **fclose**, viene eseguito il commit della voce usando [**CommitUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya).</span><span class="sxs-lookup"><span data-stu-id="1ce43-280">After the data has been written to the file using **fopen**, **fprintf**, and **fclose**, the entry is committed using [**CommitUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya).</span></span>


```C++
int WINAPI CommitEntry(HWND hX)
{
    LPTSTR lpszUrl, lpszExt, lpszFileName;
    LPTSTR lpszData,lpszSize;
    DWORD dwSize;
    DWORD dwEntryType=0;
    FILE *lpfCacheEntry;
    LPFILETIME lpdtmExpire, lpdtmLastModified;
    LPSYSTEMTIME lpdtmSysTime;
    errno_t err;

    if( SendDlgItemMessage(hX,IDC_RBNormal,BM_GETCHECK,0,0) )
    {
        dwEntryType = dwEntryType + NORMAL_CACHE_ENTRY;
    }
    else if( SendDlgItemMessage(hX,IDC_RBSticky, BM_GETCHECK,0,0) )
    {
        dwEntryType = dwEntryType + STICKY_CACHE_ENTRY;
    }
    else if(SendDlgItemMessage( hX,IDC_RBSparse, BM_GETCHECK,0,0) )
    {
        dwEntryType = dwEntryType + SPARSE_CACHE_ENTRY;
    }
 

    if( SendDlgItemMessage(hX,IDC_RBCookie, BM_GETCHECK,0,0))
    {
            dwEntryType = dwEntryType + COOKIE_CACHE_ENTRY;
    }
    else if( SendDlgItemMessage(hX,IDC_RBUrl, BM_GETCHECK,0,0) )
    {
        dwEntryType = dwEntryType + URLHISTORY_CACHE_ENTRY;
    }


    if( SendDlgItemMessage(hX,IDC_RBNone, BM_GETCHECK,0,0) )
    {
        dwEntryType=0;
    }
        
    lpdtmSysTime = new SYSTEMTIME;
    lpdtmExpire = new FILETIME;
    lpdtmLastModified = new FILETIME;

    GetLocalTime(lpdtmSysTime);
    SystemTimeToFileTime(lpdtmSysTime,lpdtmExpire);
    SystemTimeToFileTime(lpdtmSysTime,lpdtmLastModified);
    delete(lpdtmSysTime);

    lpszUrl = new TCHAR[MAX_PATH];
    lpszFileName = new TCHAR[MAX_PATH];
    lpszExt = new TCHAR[5];
    lpszSize = new TCHAR[10];

    GetDlgItemText(hX,IDC_SourceURL,lpszUrl,MAX_PATH);
    GetDlgItemText(hX,IDC_LocalFile,lpszFileName,MAX_PATH);
    GetDlgItemText(hX,IDC_FileExt,lpszExt,5);

    GetDlgItemText(hX,IDC_SizeLow,lpszSize,10);
    dwSize = (DWORD)_ttol(lpszSize);
    delete(lpszSize);

    if (dwSize==0)
    {
        if((MessageBox(hX,
                       TEXT("Incorrect File Size.\nUsing 8000 characters, Okay?\n"),
                       TEXT("Commit Entry"),MB_YESNO))
                        ==IDYES)
        {
            dwSize = 8000;
        }
        else
        {
            return FALSE;
        }
    }

    lpszData = new TCHAR[dwSize];
    GetDlgItemText(hX,IDC_CacheDump,lpszData,dwSize);
        
     err = _tfopen_s(&lpfCacheEntry,lpszFileName,_T("w"));
     if (err)
        return FALSE;
    fprintf(lpfCacheEntry,"%s",lpszData);
    fclose(lpfCacheEntry);
    delete(lpszData);

    if ( !CommitUrlCacheEntry( lpszUrl, 
                               lpszFileName, 
                               *lpdtmExpire,
                               *lpdtmLastModified, 
                               dwEntryType,
                               NULL,
                               0,
                               lpszExt,
                               0) )
    {
        ErrorOut(hX,GetLastError(),TEXT("Commit Cache Entry"));
        delete(lpszUrl);
        delete(lpszFileName);
        delete(lpszExt);
        delete(lpdtmExpire);
        delete(lpdtmLastModified);
        return FALSE;
    }
    else
    {
        delete(lpszUrl);
        delete(lpszFileName);
        delete(lpszExt);
        delete(lpdtmExpire);
        delete(lpdtmLastModified);
        return TRUE;
    }
}
```



### <a name="deleting-a-cache-entry"></a><span data-ttu-id="1ce43-281">Eliminazione di una voce della cache</span><span class="sxs-lookup"><span data-stu-id="1ce43-281">Deleting a Cache Entry</span></span>

<span data-ttu-id="1ce43-282">La funzione [**DeleteUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-deleteurlcacheentry) accetta un URL e rimuove il file di cache associato.</span><span class="sxs-lookup"><span data-stu-id="1ce43-282">The [**DeleteUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-deleteurlcacheentry) function takes a URL and removes the cache file associated with it.</span></span> <span data-ttu-id="1ce43-283">Se il file di cache non esiste, la funzione ha esito negativo e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce il file di errore \_ \_ non \_ trovato.</span><span class="sxs-lookup"><span data-stu-id="1ce43-283">If the cache file does not exist, the function fails and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_FILE\_NOT\_FOUND.</span></span> <span data-ttu-id="1ce43-284">Se il file di cache è attualmente bloccato o in uso, la funzione ha esito negativo e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce un errore di \_ accesso \_ negato.</span><span class="sxs-lookup"><span data-stu-id="1ce43-284">If the cache file is currently locked or in use, the function fails and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_ACCESS\_DENIED.</span></span> <span data-ttu-id="1ce43-285">Il file viene eliminato quando è sbloccato.</span><span class="sxs-lookup"><span data-stu-id="1ce43-285">The file is deleted when unlocked.</span></span>

### <a name="retrieving-cache-entry-files"></a><span data-ttu-id="1ce43-286">Recupero dei file di voce della cache</span><span class="sxs-lookup"><span data-stu-id="1ce43-286">Retrieving Cache Entry Files</span></span>

<span data-ttu-id="1ce43-287">Per le applicazioni che richiedono il nome file di una risorsa, usare le funzioni [**RetrieveUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea) e [**UnlockUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentryfile) .</span><span class="sxs-lookup"><span data-stu-id="1ce43-287">For applications that require the file name of a resource, use the [**RetrieveUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea) and [**UnlockUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentryfile) functions.</span></span> <span data-ttu-id="1ce43-288">Le applicazioni che non richiedono il nome file devono usare le funzioni [**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama), [**ReadUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-readurlcacheentrystream)e [**UnlockUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentrystream) per recuperare le informazioni nella cache.</span><span class="sxs-lookup"><span data-stu-id="1ce43-288">Applications that do not require the file name should use the [**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama), [**ReadUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-readurlcacheentrystream), and [**UnlockUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentrystream) functions to retrieve the information in the cache.</span></span>

<span data-ttu-id="1ce43-289">[**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama) non esegue l'analisi dell'URL, quindi un URL che contiene un ancoraggio ( \# ) non verrà trovato nella cache, anche se la risorsa è memorizzata nella cache.</span><span class="sxs-lookup"><span data-stu-id="1ce43-289">[**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama) does not do any URL parsing, so a URL that contains an anchor (\#) will not be found in the cache, even if the resource is cached.</span></span> <span data-ttu-id="1ce43-290">Se, ad esempio, viene passato l'URL " https://example.com/example.htm\#sample ", la funzione restituisce il \_ file \_ di errore non \_ trovato anche se " https://example.com/example.htm " si trova nella cache.</span><span class="sxs-lookup"><span data-stu-id="1ce43-290">For example, if the URL "https://example.com/example.htm\#sample" is passed, the function returns ERROR\_FILE\_NOT\_FOUND even if "https://example.com/example.htm" is in the cache.</span></span>

<span data-ttu-id="1ce43-291">[**RetrieveUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea) accetta un URL, un buffer che archivia la struttura delle [**\_ \_ \_ informazioni sulla voce della cache Internet**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) e le dimensioni del buffer.</span><span class="sxs-lookup"><span data-stu-id="1ce43-291">[**RetrieveUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea) accepts a URL, a buffer that stores the [**INTERNET\_CACHE\_ENTRY\_INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) structure, and the buffer size.</span></span> <span data-ttu-id="1ce43-292">La funzione viene recuperata e bloccata per il chiamante.</span><span class="sxs-lookup"><span data-stu-id="1ce43-292">The function is retrieved and locked for the caller.</span></span>

<span data-ttu-id="1ce43-293">Una volta utilizzate le informazioni nel file, l'applicazione deve chiamare [**UnlockUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentryfile) per sbloccare il file.</span><span class="sxs-lookup"><span data-stu-id="1ce43-293">After the information in the file has been used, the application should call [**UnlockUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentryfile) to unlock the file.</span></span>

### <a name="cache-groups"></a><span data-ttu-id="1ce43-294">Gruppi di cache</span><span class="sxs-lookup"><span data-stu-id="1ce43-294">Cache Groups</span></span>

<span data-ttu-id="1ce43-295">Per creare un gruppo di cache, è necessario chiamare la funzione [**CreateUrlCacheGroup**](/windows/desktop/api/Wininet/nf-wininet-createurlcachegroup) per generare un **GROUPID** per il gruppo di cache.</span><span class="sxs-lookup"><span data-stu-id="1ce43-295">To create a cache group, the [**CreateUrlCacheGroup**](/windows/desktop/api/Wininet/nf-wininet-createurlcachegroup) function must be called to generate a **GROUPID** for the cache group.</span></span> <span data-ttu-id="1ce43-296">È possibile aggiungere voci al gruppo di cache specificando l'URL della voce della cache e il \_ flag di aggiunta del gruppo della cache Internet \_ \_ alla funzione [**SetUrlCacheEntryGroup**](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentrygroup) .</span><span class="sxs-lookup"><span data-stu-id="1ce43-296">Entries can be added to the cache group by supplying the cache entry's URL and the INTERNET\_CACHE\_GROUP\_ADD flag to the [**SetUrlCacheEntryGroup**](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentrygroup) function.</span></span> <span data-ttu-id="1ce43-297">Per rimuovere una voce della cache da un gruppo, passare l'URL della voce della cache e \_ il \_ flag di rimozione del gruppo della cache Internet \_ a [**SetUrlCacheEntryGroup**](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentrygroup).</span><span class="sxs-lookup"><span data-stu-id="1ce43-297">To remove a cache entry from a group, pass the cache entry's URL and the INTERNET\_CACHE\_GROUP\_REMOVE flag to [**SetUrlCacheEntryGroup**](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentrygroup).</span></span>

<span data-ttu-id="1ce43-298">Le funzioni [**FindFirstUrlCacheEntryEx**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentryexa) e [**FindNextUrlCacheEntryEx**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentryexa) possono essere utilizzate per enumerare le voci in un gruppo di cache specificato.</span><span class="sxs-lookup"><span data-stu-id="1ce43-298">The [**FindFirstUrlCacheEntryEx**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentryexa) and [**FindNextUrlCacheEntryEx**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentryexa) functions can be used to enumerate the entries in a specified cache group.</span></span> <span data-ttu-id="1ce43-299">Al termine dell'enumerazione, la funzione deve chiamare [**FindCloseUrlCache**](/windows/desktop/api/Wininet/nf-wininet-findcloseurlcache).</span><span class="sxs-lookup"><span data-stu-id="1ce43-299">After the enumeration is complete, the function should call [**FindCloseUrlCache**](/windows/desktop/api/Wininet/nf-wininet-findcloseurlcache).</span></span>

## <a name="handling-structures-with-variable-size-information"></a><span data-ttu-id="1ce43-300">Gestione di strutture con informazioni sulle dimensioni delle variabili</span><span class="sxs-lookup"><span data-stu-id="1ce43-300">Handling Structures with Variable Size Information</span></span>

<span data-ttu-id="1ce43-301">La cache può contenere informazioni sulle dimensioni variabili per ogni URL archiviato.</span><span class="sxs-lookup"><span data-stu-id="1ce43-301">The cache can contain variable size information for each URL stored.</span></span> <span data-ttu-id="1ce43-302">Questo si riflette nella struttura [**delle \_ \_ \_ informazioni sulla voce della cache Internet**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) .</span><span class="sxs-lookup"><span data-stu-id="1ce43-302">This is reflected in the [**INTERNET\_CACHE\_ENTRY\_INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) structure.</span></span> <span data-ttu-id="1ce43-303">Quando le funzioni della cache restituiscono questa struttura, creano un buffer che corrisponde sempre alle dimensioni [**delle \_ \_ \_ informazioni sulla voce della cache Internet**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) più tutte le informazioni sulle dimensioni delle variabili.</span><span class="sxs-lookup"><span data-stu-id="1ce43-303">When the cache functions return this structure, they create a buffer that is always the size of [**INTERNET\_CACHE\_ENTRY\_INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) plus any variable size information.</span></span> <span data-ttu-id="1ce43-304">Se un membro del puntatore non è **null**, fa riferimento all'area di memoria immediatamente dopo la struttura.</span><span class="sxs-lookup"><span data-stu-id="1ce43-304">If a pointer member is not **NULL**, it points to the memory area immediately after the structure.</span></span> <span data-ttu-id="1ce43-305">Durante la copia del buffer restituito da una funzione in un altro buffer, i membri del puntatore devono essere corretti in modo che puntino alla posizione appropriata nel nuovo buffer, come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="1ce43-305">While copying the buffer returned by a function into another buffer, the pointer members should be fixed to point to the appropriate place in the new buffer, as the following example shows.</span></span>

``` syntax
lpDstCEInfo->lpszSourceUrlName = 
    (LPINTERNET_CACHE_ENTRY_INFO) ((LPBYTE) lpSrcCEInfo + 
       ((DWORD)(lpOldCEInfo->lpszSourceUrlName) - (DWORD)lpOldCEInfo));
```

<span data-ttu-id="1ce43-306">Alcune funzioni della cache hanno esito negativo e il \_ \_ messaggio di errore buffer insufficiente se si specifica un buffer troppo piccolo per contenere le informazioni relative alla voce della cache recuperate dalla funzione.</span><span class="sxs-lookup"><span data-stu-id="1ce43-306">Some cache functions fail with the ERROR\_INSUFFICIENT\_BUFFER error message if you specify a buffer that is too small to contain the cache entry information retrieved by the function.</span></span> <span data-ttu-id="1ce43-307">In questo caso, la funzione restituisce anche la dimensione richiesta del buffer.</span><span class="sxs-lookup"><span data-stu-id="1ce43-307">In this case, the function also returns the required size of the buffer.</span></span> <span data-ttu-id="1ce43-308">È quindi possibile allocare un buffer di dimensioni appropriate e chiamare di nuovo la funzione.</span><span class="sxs-lookup"><span data-stu-id="1ce43-308">You can then allocate a buffer of the appropriate size and call the function again.</span></span>

> [!Note]  
> <span data-ttu-id="1ce43-309">WinINet non supporta le implementazioni del server.</span><span class="sxs-lookup"><span data-stu-id="1ce43-309">WinINet does not support server implementations.</span></span> <span data-ttu-id="1ce43-310">Inoltre, non deve essere utilizzato da un servizio.</span><span class="sxs-lookup"><span data-stu-id="1ce43-310">In addition, it should not be used from a service.</span></span> <span data-ttu-id="1ce43-311">Per le implementazioni o i servizi del server, usare i [Servizi http di Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="1ce43-311">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 
