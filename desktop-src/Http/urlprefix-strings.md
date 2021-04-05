---
title: UrlPrefix Strings (Stringhe UrlPrefix)
description: Nell'API del server HTTP, un UrlPrefix è una stringa Unicode a caratteri wide (UTF-16) con una forma canonica che specifica una sezione dello spazio dei nomi URL.
ms.assetid: 4f317bf6-ee6a-47a8-a531-78534217109d
keywords:
- API server HTTP UrlPrefix Strings
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bddc484f26bc1b3de5d20196dadec9201d3ea272
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/20/2020
ms.locfileid: "103734738"
---
# <a name="urlprefix-strings"></a><span data-ttu-id="a4638-104">UrlPrefix Strings (Stringhe UrlPrefix)</span><span class="sxs-lookup"><span data-stu-id="a4638-104">UrlPrefix Strings</span></span>

<span data-ttu-id="a4638-105">Nell'API del server HTTP, un *URLPrefix* è una stringa Unicode a caratteri wide (UTF-16) con una forma canonica che specifica una sezione dello spazio dei nomi URL.</span><span class="sxs-lookup"><span data-stu-id="a4638-105">In the HTTP Server API, a *UrlPrefix* is a wide-character (UTF-16) Unicode string with a canonical form that specifies a section of URL namespace.</span></span> <span data-ttu-id="a4638-106">Viene usato per riservare una sezione dello spazio dei nomi URL per un account utente o per registrare una sezione dello spazio dei nomi URL per un processo.</span><span class="sxs-lookup"><span data-stu-id="a4638-106">It is used to reserve a section of URL namespace for a user account or register a section of URL namespace for a process.</span></span>

## <a name="urlprefix-format"></a><span data-ttu-id="a4638-107">Formato UrlPrefix</span><span class="sxs-lookup"><span data-stu-id="a4638-107">UrlPrefix Format</span></span>

<span data-ttu-id="a4638-108">Un UrlPrefix ha la sintassi seguente:</span><span class="sxs-lookup"><span data-stu-id="a4638-108">A UrlPrefix has the following syntax:</span></span>

<span data-ttu-id="a4638-109">"Scheme://host: Port/relativeURI"</span><span class="sxs-lookup"><span data-stu-id="a4638-109">"scheme://host:port/relativeURI"</span></span>

<span data-ttu-id="a4638-110">Gli elementi schema, host e Port di un UrlPrefix devono essere presenti e non vuoti e devono rispettare le regole seguenti:</span><span class="sxs-lookup"><span data-stu-id="a4638-110">The scheme, host and port elements of a UrlPrefix must be present and non-empty, and must obey the following rules:</span></span>

<dl> <dt>

<span data-ttu-id="a4638-111"><span id="scheme"></span><span id="SCHEME"></span>Schema</span><span class="sxs-lookup"><span data-stu-id="a4638-111"><span id="scheme"></span><span id="SCHEME"></span>scheme</span></span>
</dt> <dd>

<span data-ttu-id="a4638-112">Deve essere http o HTTPS, tutto in minuscolo.</span><span class="sxs-lookup"><span data-stu-id="a4638-112">Must be either http or https, all in lowercase.</span></span>

</dd> <dt>

<span data-ttu-id="a4638-113"><span id="host"></span><span id="HOST"></span>host</span><span class="sxs-lookup"><span data-stu-id="a4638-113"><span id="host"></span><span id="HOST"></span>host</span></span>
</dt> <dd>

<span data-ttu-id="a4638-114">Deve essere un nome di dominio completo, una stringa letterale IPv4 o IPv6 o un carattere jolly.</span><span class="sxs-lookup"><span data-stu-id="a4638-114">Must be a fully qualified domain name, an IPv4 or IPv6 literal string, or a wildcard.</span></span> <span data-ttu-id="a4638-115">A differenza dello schema, che deve essere minuscolo, la parte host non fa distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="a4638-115">Unlike the scheme, which must be lowercase, the host portion is case-insensitive.</span></span> <span data-ttu-id="a4638-116">A seconda di come viene specificata la relativa porzione host, un UrlPrefix rientra in una delle quattro categorie di routing seguenti, descritte in modo più dettagliato di seguito:</span><span class="sxs-lookup"><span data-stu-id="a4638-116">Depending on how its host portion is specified, a UrlPrefix falls into one of the following four routing categories, which are described in more detail below:</span></span>

<dl> <dd><span data-ttu-id="a4638-117">Carattere jolly sicuro</span><span class="sxs-lookup"><span data-stu-id="a4638-117">Strong wildcard</span></span></dd> <dd><span data-ttu-id="a4638-118">Esplicita</span><span class="sxs-lookup"><span data-stu-id="a4638-118">Explicit</span></span></dd> <dd><span data-ttu-id="a4638-119">Carattere jolly vulnerabile associato a IP</span><span class="sxs-lookup"><span data-stu-id="a4638-119">IP-bound weak wildcard</span></span></dd> <dd><span data-ttu-id="a4638-120">Carattere jolly vulnerabile</span><span class="sxs-lookup"><span data-stu-id="a4638-120">Weak wildcard</span></span></dd> </dl> </dd> <dt>

<span data-ttu-id="a4638-121"><span id="port"></span><span id="PORT"></span>porta</span><span class="sxs-lookup"><span data-stu-id="a4638-121"><span id="port"></span><span id="PORT"></span>port</span></span>
</dt> <dd>

<span data-ttu-id="a4638-122">Stringa numerica decimale che non inizia con zero e che rappresenta un numero di porta TCP valido (da 1 a 65.535).</span><span class="sxs-lookup"><span data-stu-id="a4638-122">A decimal numeric string that does not start with zero and that represents a valid TCP port number (1 to 65,535).</span></span> <span data-ttu-id="a4638-123">Questo valore non può essere un carattere jolly.</span><span class="sxs-lookup"><span data-stu-id="a4638-123">This value cannot be a wildcard.</span></span>

</dd> <dt>

<span data-ttu-id="a4638-124"><span id="relativeURI"></span><span id="relativeuri"></span><span id="RELATIVEURI"></span>relativeURI</span><span class="sxs-lookup"><span data-stu-id="a4638-124"><span id="relativeURI"></span><span id="relativeuri"></span><span id="RELATIVEURI"></span>relativeURI</span></span>
</dt> <dd>

<span data-ttu-id="a4638-125">L'elemento relativeURI è facoltativo, ma se è presente deve essere sempre seguito da un carattere barra ("/").</span><span class="sxs-lookup"><span data-stu-id="a4638-125">The relativeURI element is optional, but if present must always be followed by a slash character ("/").</span></span> <span data-ttu-id="a4638-126">Si tratta di una stringa di prefisso che indica un sottoalbero nello spazio dei nomi del computer specificato rispetto ai valori di schema, host e porta.</span><span class="sxs-lookup"><span data-stu-id="a4638-126">This is a prefix string that indicates a subtree within the machine's namespace specified relative to the scheme, host and port values.</span></span> <span data-ttu-id="a4638-127">A differenza dello schema, che deve essere minuscolo, la parte relativeURI non fa distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="a4638-127">Unlike the scheme, which must be lowercase, the relativeURI portion is case-insensitive.</span></span>

</dd> </dl>

<span data-ttu-id="a4638-128">Esempi di prefissi URL correttamente formati sono:</span><span class="sxs-lookup"><span data-stu-id="a4638-128">Examples of properly formed UrlPrefixes are:</span></span>

-   `https://www.adatum.com:80/vroot/`
-   `https://adatum.com:443/secure/database/`
-   `https://+:80/vroot/`

## <a name="host-specifier-categories"></a><span data-ttu-id="a4638-129">Categorie di Host-Specifier</span><span class="sxs-lookup"><span data-stu-id="a4638-129">Host-Specifier Categories</span></span>

<span data-ttu-id="a4638-130">Per flessibilità e semplicità d'uso, l'API server HTTP supporta quattro diversi modi per specificare gli host.</span><span class="sxs-lookup"><span data-stu-id="a4638-130">For flexibility and ease of use, the HTTP Server API supports four different ways to specify hosts.</span></span> <span data-ttu-id="a4638-131">Le quattro categorie host-specifier sono elencate di seguito in ordine di precedenza:</span><span class="sxs-lookup"><span data-stu-id="a4638-131">The four host-specifier categories are listed below in order of precedence:</span></span>

<dl> <dt>

<span data-ttu-id="a4638-132"><span id="Strong_wildcard__Plus_Sign_"></span><span id="strong_wildcard__plus_sign_"></span><span id="STRONG_WILDCARD__PLUS_SIGN_"></span>Carattere jolly forte (segno più)</span><span class="sxs-lookup"><span data-stu-id="a4638-132"><span id="Strong_wildcard__Plus_Sign_"></span><span id="strong_wildcard__plus_sign_"></span><span id="STRONG_WILDCARD__PLUS_SIGN_"></span>Strong wildcard (Plus Sign)</span></span>
</dt> <dd>

<span data-ttu-id="a4638-133">Quando l'elemento host di un UrlPrefix è costituito da un singolo segno più (+), il UrlPrefix corrisponde a tutti i nomi host possibili nel contesto dello schema, della porta e degli elementi relativeURI e rientra nella categoria con caratteri jolly forti.</span><span class="sxs-lookup"><span data-stu-id="a4638-133">When the host element of a UrlPrefix consists of a single plus sign (+), the UrlPrefix matches all possible host names in the context of its scheme, port and relativeURI elements, and falls into the strong wildcard category.</span></span>

<span data-ttu-id="a4638-134">Un carattere jolly complesso è utile quando un'applicazione deve gestire le richieste destinate a uno o più relativeURIs, indipendentemente dal modo in cui tali richieste vengono ricevute nel computer o nel sito specificato nelle rispettive intestazioni host.</span><span class="sxs-lookup"><span data-stu-id="a4638-134">A strong wildcard is useful when an application needs to serve requests addressed to one or more relativeURIs, regardless of how those requests arrive on the machine or what site they specify in their Host headers.</span></span> <span data-ttu-id="a4638-135">In questa situazione, l'utilizzo di un carattere jolly complesso evita la necessità di specificare un elenco completo di indirizzi IP e/o host.</span><span class="sxs-lookup"><span data-stu-id="a4638-135">Use of a strong wildcard in this situation avoids the need to specify an exhaustive list of host and/or IP-addresses.</span></span>

</dd> <dt>

<span data-ttu-id="a4638-136"><span id="Explicit"></span><span id="explicit"></span><span id="EXPLICIT"></span>Esplicita</span><span class="sxs-lookup"><span data-stu-id="a4638-136"><span id="Explicit"></span><span id="explicit"></span><span id="EXPLICIT"></span>Explicit</span></span>
</dt> <dd>

<span data-ttu-id="a4638-137">Un nome host esplicito, ad esempio un nome di dominio completo nell'elemento host, inserisce un UrlPrefix nella categoria Explicit.</span><span class="sxs-lookup"><span data-stu-id="a4638-137">An explicit host name such as a fully qualified domain name in the host element places a UrlPrefix in the explicit category.</span></span> <span data-ttu-id="a4638-138">Questo tipo di elemento host viene associato direttamente alle intestazioni host delle richieste in ingresso.</span><span class="sxs-lookup"><span data-stu-id="a4638-138">This kind of host element is matched directly against the Host headers of incoming requests.</span></span>

<span data-ttu-id="a4638-139">Le specifiche host esplicite sono utili per le applicazioni multisito, ad esempio i server Web che forniscono contenuti diversi a seconda del sito a cui è stata indirizzata la richiesta.</span><span class="sxs-lookup"><span data-stu-id="a4638-139">Explicit host specifications are useful for multi-site applications such as Web servers that deliver different content depending on the site to which the request was directed.</span></span>

</dd> <dt>

<span data-ttu-id="a4638-140"><span id="IP-bound_weak_wildcard"></span><span id="ip-bound_weak_wildcard"></span><span id="IP-BOUND_WEAK_WILDCARD"></span>Carattere jolly vulnerabile associato a IP</span><span class="sxs-lookup"><span data-stu-id="a4638-140"><span id="IP-bound_weak_wildcard"></span><span id="ip-bound_weak_wildcard"></span><span id="IP-BOUND_WEAK_WILDCARD"></span>IP-bound weak wildcard</span></span>
</dt> <dd>

<span data-ttu-id="a4638-141">Quando un indirizzo IP viene visualizzato come elemento host, il UrlPrefix rientra nella categoria con carattere jolly vulnerabile associato a IP.</span><span class="sxs-lookup"><span data-stu-id="a4638-141">When an IP address appears as the host element, then the UrlPrefix falls into the IP-bound Weak Wildcard category.</span></span> <span data-ttu-id="a4638-142">Questo tipo di UrlPrefix corrisponde a qualsiasi nome host per l'interfaccia IP specificata con lo schema, la porta e il relativeURI specificati e che non è già stato trovato come corrispondenza con un carattere jolly sicuro o un UrlPrefix esplicito.</span><span class="sxs-lookup"><span data-stu-id="a4638-142">This kind of UrlPrefix matches any host name for the specified IP interface with the specified scheme, port and relativeURI, and that has not already been matched by a strong-wildcard or explicit UrlPrefix.</span></span> <span data-ttu-id="a4638-143">L'indirizzo IP accetta uno dei due formati seguenti nell'elemento host:</span><span class="sxs-lookup"><span data-stu-id="a4638-143">The IP address takes one of two forms in the host element:</span></span>

<dl> <dt>

<span data-ttu-id="a4638-144"><span id="IPv4_Literal_String"></span><span id="ipv4_literal_string"></span><span id="IPV4_LITERAL_STRING"></span>Stringa letterale IPv4</span><span class="sxs-lookup"><span data-stu-id="a4638-144"><span id="IPv4_Literal_String"></span><span id="ipv4_literal_string"></span><span id="IPV4_LITERAL_STRING"></span>IPv4 Literal String</span></span>
</dt> <dd>

<span data-ttu-id="a4638-145">Un valore letterale IPv4 è costituito da quattro numeri decimali punteggiati, ognuno nell'intervallo 0-255, ad esempio 192.168.0.0.</span><span class="sxs-lookup"><span data-stu-id="a4638-145">An IPv4 literal consists of four dotted decimal numbers, each in the range 0-255, such as 192.168.0.0.</span></span>

</dd> <dt>

<span data-ttu-id="a4638-146"><span id="IPv6_Literal_String"></span><span id="ipv6_literal_string"></span><span id="IPV6_LITERAL_STRING"></span>Stringa letterale IPv6</span><span class="sxs-lookup"><span data-stu-id="a4638-146"><span id="IPv6_Literal_String"></span><span id="ipv6_literal_string"></span><span id="IPV6_LITERAL_STRING"></span>IPv6 Literal String</span></span>
</dt> <dd>

<span data-ttu-id="a4638-147">Una stringa letterale IPv6 è racchiusa tra parentesi quadre e contiene numeri esadecimali separati da due punti; ad esempio::: \[ 1 \] o \[ 3FFE: ffff:: 6ECB: 0101 \] .</span><span class="sxs-lookup"><span data-stu-id="a4638-147">An IPv6 literal string is enclosed in square brackets and contains hex numbers separated by colons; for example: \[::1\] or \[3ffe:ffff::6ECB:0101\].</span></span>

</dd> </dl>

<span data-ttu-id="a4638-148">Gli identificatori host con caratteri jolly vulnerabili con binding IP sono destinati ad applicazioni che variano il contenuto che viene utilizzato in base alla route eseguita dalle richieste in ingresso.</span><span class="sxs-lookup"><span data-stu-id="a4638-148">IP-bound weak-wildcard host specifiers are intended for applications that vary the content they serve based on the route taken by incoming requests.</span></span> <span data-ttu-id="a4638-149">Non fare affidamento sugli identificatori host con caratteri jolly vulnerabili con binding IP per applicare la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="a4638-149">Do not rely on IP-bound weak-wildcard host specifiers to enforce security.</span></span>

</dd> <dt>

<span data-ttu-id="a4638-150"><span id="Weak_wildcard__asterisk_"></span><span id="weak_wildcard__asterisk_"></span><span id="WEAK_WILDCARD__ASTERISK_"></span>Carattere jolly debole (asterisco)</span><span class="sxs-lookup"><span data-stu-id="a4638-150"><span id="Weak_wildcard__asterisk_"></span><span id="weak_wildcard__asterisk_"></span><span id="WEAK_WILDCARD__ASTERISK_"></span>Weak wildcard (asterisk)</span></span>
</dt> <dd>

<span data-ttu-id="a4638-151">Quando un asterisco ( \* ) viene visualizzato come elemento host, il URLPrefix rientra nella categoria con carattere jolly debole.</span><span class="sxs-lookup"><span data-stu-id="a4638-151">When an asterisk (\*) appears as the host element, then the UrlPrefix falls into the weak wildcard category.</span></span> <span data-ttu-id="a4638-152">Questo tipo di UrlPrefix corrisponde a qualsiasi nome host associato allo schema, alla porta e al relativeURI specificati che non sono già stati confrontati da un carattere jolly sicuro, esplicito o con carattere jolly debole associato a IP.</span><span class="sxs-lookup"><span data-stu-id="a4638-152">This kind of UrlPrefix matches any host name associated with the specified scheme, port and relativeURI that has not already been matched by a strong-wildcard, explicit, or IP-bound weak-wildcard UrlPrefix.</span></span>

<span data-ttu-id="a4638-153">Questa specifica host può essere usata come catch-all predefinito in alcune circostanze oppure può essere usata per specificare una sezione di grandi dimensioni dello spazio dei nomi URL senza dover usare molti prefissi URL.</span><span class="sxs-lookup"><span data-stu-id="a4638-153">This host specification can be used as a default catch-all in some circumstances, or can be used to specify a large section of URL namespace without having to use many UrlPrefixes.</span></span>

</dd> </dl>

## <a name="urlprefix-conflict-detection-during-reservation-and-registration"></a><span data-ttu-id="a4638-154">Rilevamento dei conflitti di UrlPrefix durante la prenotazione e la registrazione</span><span class="sxs-lookup"><span data-stu-id="a4638-154">UrlPrefix Conflict Detection During Reservation and Registration</span></span>

<span data-ttu-id="a4638-155">Ai fini della prenotazione e della registrazione, le quattro categorie diverse di UrlPrefix vengono gestite separatamente, senza riferimento l'una all'altra.</span><span class="sxs-lookup"><span data-stu-id="a4638-155">For reservation and registration purposes, the four different categories of UrlPrefix are treated separately, without reference to one another.</span></span> <span data-ttu-id="a4638-156">È possibile registrare prefissi URL in conflitto, purché si trovino in categorie diverse.</span><span class="sxs-lookup"><span data-stu-id="a4638-156">It is possible to register conflicting UrlPrefixes as long as they are in different categories.</span></span> <span data-ttu-id="a4638-157">Solo all'interno della stessa categoria si verifica un conflitto perché un tentativo di prenotazione non riesce.</span><span class="sxs-lookup"><span data-stu-id="a4638-157">Only within the same category does a conflict cause a reservation attempt to fail.</span></span>

<span data-ttu-id="a4638-158">Ad esempio, è possibile riservare sia il UrlPrefix esplicito `https://www.adatum.com:80/vroot/` che il carattere jolly URLPrefix `https://+:80/vroot/` in conflitto, perché appartengono a categorie diverse.</span><span class="sxs-lookup"><span data-stu-id="a4638-158">For example, it would be possible to reserve both the explicit UrlPrefix `https://www.adatum.com:80/vroot/` and the conflicting strong wildcard UrlPrefix `https://+:80/vroot/`, since they belong to different categories.</span></span> <span data-ttu-id="a4638-159">Tuttavia, un tentativo successivo di riservare https://+:80/vroot/ a un utente diverso avrà esito negativo perché potrebbe essere in conflitto con una prenotazione esistente nella relativa categoria.</span><span class="sxs-lookup"><span data-stu-id="a4638-159">However, a subsequent attempt to reserve https://+:80/vroot/ to a different user would fail because it would conflict with an existing reservation in its own category.</span></span>

## <a name="routing-behavior"></a><span data-ttu-id="a4638-160">Comportamento del routing</span><span class="sxs-lookup"><span data-stu-id="a4638-160">Routing Behavior</span></span>

<span data-ttu-id="a4638-161">Quando si esegue il routing di una richiesta HTTP in ingresso, l'API del server HTTP inizia con la categoria con carattere jolly sicuro e confronta l'URL in ingresso con prefissi URL registrati e riservati in tale categoria.</span><span class="sxs-lookup"><span data-stu-id="a4638-161">When routing an incoming HTTP request, the HTTP Server API starts with the strong wildcard category and compares the incoming URL with both registered and reserved UrlPrefixes in that category.</span></span>

<span data-ttu-id="a4638-162">Se l'URL in ingresso corrisponde a una prenotazione ma non a una registrazione, l'API del server HTTP ha esito negativo per la richiesta.</span><span class="sxs-lookup"><span data-stu-id="a4638-162">If the incoming URL matches a reservation but not a registration, the HTTP Server API fails the request.</span></span> <span data-ttu-id="a4638-163">In questo modo si impedisce che le registrazioni con priorità inferiore siano in grado di prelevare richieste non desiderate.</span><span class="sxs-lookup"><span data-stu-id="a4638-163">This prevents a lower-priority registrations from being able to pick up requests not intended for it.</span></span> <span data-ttu-id="a4638-164">Lo stato in caso di errore è 400 ("richiesta non valida") anziché 503 ("servizio non disponibile"), perché un ritorno 503 viene talvolta interpretato erroneamente dai gateway di bilanciamento del carico come indicato che il server è stato sottoposto a overload.</span><span class="sxs-lookup"><span data-stu-id="a4638-164">The status on failure is 400 ("Bad Request") rather than 503 ("Service not available"), because a 503 return is sometimes mistakenly interpreted by load-balancing gateways as indicating that the server was overloaded.</span></span>

<span data-ttu-id="a4638-165">Se viene rilevata una registrazione corrispondente all'interno della categoria, la richiesta viene instradata alla coda di richieste associata a tale registrazione.</span><span class="sxs-lookup"><span data-stu-id="a4638-165">If a matching registration is found within the category, the request is routed to the request queue associated with that registration.</span></span> <span data-ttu-id="a4638-166">La richiesta viene sempre indirizzata alla coda associata alla UrlPrefix corrispondente più estesa all'interno di una categoria.</span><span class="sxs-lookup"><span data-stu-id="a4638-166">The request is always routed to the queue associated with the longest matching UrlPrefix within a category.</span></span>

<span data-ttu-id="a4638-167">Se non viene trovata alcuna corrispondenza nella categoria, l'API server HTTP passa alla categoria esplicita e ripete la stessa procedura.</span><span class="sxs-lookup"><span data-stu-id="a4638-167">If no match is found in the category, then the HTTP Server API proceeds to the explicit category and repeats the same procedure.</span></span> <span data-ttu-id="a4638-168">Per riepilogare, l'ordine in cui vengono esaminate le categorie è il seguente:</span><span class="sxs-lookup"><span data-stu-id="a4638-168">To summarize, the order in which the categories are examined is as follows:</span></span>

1.  <span data-ttu-id="a4638-169">Carattere jolly sicuro</span><span class="sxs-lookup"><span data-stu-id="a4638-169">Strong wildcard</span></span>
2.  <span data-ttu-id="a4638-170">Esplicita</span><span class="sxs-lookup"><span data-stu-id="a4638-170">Explicit</span></span>
3.  <span data-ttu-id="a4638-171">Carattere jolly IP-Bound vulnerabile</span><span class="sxs-lookup"><span data-stu-id="a4638-171">IP-Bound weak wildcard</span></span>
4.  <span data-ttu-id="a4638-172">Carattere jolly vulnerabile</span><span class="sxs-lookup"><span data-stu-id="a4638-172">Weak wildcard</span></span>

<span data-ttu-id="a4638-173">Se non viene trovata alcuna corrispondenza in nessuna delle categorie, l'API del server HTTP invia una risposta con un codice di stato 400 per indicare che non è possibile indirizzare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="a4638-173">If no match is found in any of the categories, the HTTP Server API sends a response with a status code of 400 to indicate that the request cannot be routed.</span></span>

## <a name="longest-match-rule"></a><span data-ttu-id="a4638-174">Regola di corrispondenza più lungo</span><span class="sxs-lookup"><span data-stu-id="a4638-174">Longest Match Rule</span></span>

<span data-ttu-id="a4638-175">All'interno di ogni categoria UrlPrefix, l'API server HTTP instrada una richiesta alla coda associata al UrlPrefix più lungo corrispondente.</span><span class="sxs-lookup"><span data-stu-id="a4638-175">Within each UrlPrefix category, HTTP Server API routes a request to the queue associated with the longest matching UrlPrefix.</span></span> <span data-ttu-id="a4638-176">Si supponga, ad esempio, che i due prefissi URL seguenti siano registrati in code diverse:</span><span class="sxs-lookup"><span data-stu-id="a4638-176">For example, suppose the following two UrlPrefixes are registered to different queues:</span></span>

- `Queue1 https://www.adatum.com:80/`
- `Queue2 https://www.adatum.com:80/dir/sna/`

<span data-ttu-id="a4638-177">L'API server HTTP instrada una richiesta di `https://www.adatum.com:80/default.htm` a Queue1 e una richiesta di `https://www.adatum.com:80/dir/sna/snadefault.htm` a Queue2.</span><span class="sxs-lookup"><span data-stu-id="a4638-177">The HTTP Server API routes a request for `https://www.adatum.com:80/default.htm` to Queue1, and a request for `https://www.adatum.com:80/dir/sna/snadefault.htm` to Queue2.</span></span> <span data-ttu-id="a4638-178">Instrada una richiesta di `https://www.adatum.com:80/dir/app.htm` a Queue1 poiché la corrispondenza completa più estesa è con `https://www.adatum.com:80/` URLPrefix, non con `https://www.adatum.com:80/dir/sna` URLPrefix.</span><span class="sxs-lookup"><span data-stu-id="a4638-178">It routes a request for `https://www.adatum.com:80/dir/app.htm` to Queue1 because the longest complete match is with the `https://www.adatum.com:80/` UrlPrefix, not with the `https://www.adatum.com:80/dir/sna` UrlPrefix.</span></span>

 

 




