---
description: Alcuni server e proxy HTTP richiedono l'autenticazione prima di consentire l'accesso alle risorse su Internet. Le funzioni dei servizi HTTP di Microsoft Windows (WinHTTP) supportano l'autenticazione server e proxy per le sessioni HTTP.
ms.assetid: 077d6275-8600-4091-b78e-419a41a2101a
title: Autenticazione in WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a75c6703e9d28902c5705f0b8ab8433193c4d085
ms.sourcegitcommit: 59ec383331366f8a62c94bb88468ca03e95c43f8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/13/2021
ms.locfileid: "107380827"
---
# <a name="authentication-in-winhttp"></a><span data-ttu-id="fa907-104">Autenticazione in WinHTTP</span><span class="sxs-lookup"><span data-stu-id="fa907-104">Authentication in WinHTTP</span></span>

<span data-ttu-id="fa907-105">Alcuni server e proxy HTTP richiedono l'autenticazione prima di consentire l'accesso alle risorse su Internet.</span><span class="sxs-lookup"><span data-stu-id="fa907-105">Some HTTP servers and proxies require authentication before allowing access to resources on the Internet.</span></span> <span data-ttu-id="fa907-106">Le funzioni dei servizi HTTP di Microsoft Windows (WinHTTP) supportano l'autenticazione server e proxy per le sessioni HTTP.</span><span class="sxs-lookup"><span data-stu-id="fa907-106">The Microsoft Windows HTTP Services (WinHTTP) functions support server and proxy authentication for HTTP sessions.</span></span>

## <a name="about-http-authentication"></a><span data-ttu-id="fa907-107">Informazioni sull'autenticazione HTTP</span><span class="sxs-lookup"><span data-stu-id="fa907-107">About HTTP Authentication</span></span>

<span data-ttu-id="fa907-108">Se è necessaria l'autenticazione, l'applicazione HTTP riceve il codice di stato 401 (il server richiede l'autenticazione) o 407 (il proxy richiede l'autenticazione).</span><span class="sxs-lookup"><span data-stu-id="fa907-108">If authentication is required, the HTTP application receives a status code of 401 (server requires authentication) or 407 (proxy requires authentication).</span></span> <span data-ttu-id="fa907-109">Insieme al codice di stato, il proxy o il server invia una o più intestazioni di autenticazione: WWW-Authenticate (per l'autenticazione server) o Proxy-Authenticate (per l'autenticazione proxy).</span><span class="sxs-lookup"><span data-stu-id="fa907-109">Along with the status code, the proxy or server sends one or more authenticate headers: WWW-Authenticate (for server authentication) or Proxy-Authenticate (for proxy authentication).</span></span>

<span data-ttu-id="fa907-110">Ogni intestazione di autenticazione contiene uno schema di autenticazione supportato e, per gli schemi Basic e Digest, un'area di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="fa907-110">Each authenticate header contains a supported authentication scheme and, for the Basic and Digest schemes, a realm.</span></span> <span data-ttu-id="fa907-111">Se sono supportati più schemi di autenticazione, il server restituisce più intestazioni di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="fa907-111">If multiple authentication schemes are supported, the server returns multiple authenticate headers.</span></span> <span data-ttu-id="fa907-112">Il valore dell'area di autenticazione fa distinzione tra maiuscole e minuscole e definisce un set di server o proxy per i quali vengono accettate le stesse credenziali.</span><span class="sxs-lookup"><span data-stu-id="fa907-112">The realm value is case-sensitive and defines a set of servers or proxies for which the same credentials are accepted.</span></span> <span data-ttu-id="fa907-113">Ad esempio, l'intestazione "WWW-Authenticate: Basic Realm="example"" potrebbe essere restituita quando è necessaria l'autenticazione del server.</span><span class="sxs-lookup"><span data-stu-id="fa907-113">For example, the header "WWW-Authenticate: Basic Realm="example"" might be returned when server authentication is required.</span></span> <span data-ttu-id="fa907-114">Questa intestazione specifica che le credenziali utente devono essere fornite per il dominio "example".</span><span class="sxs-lookup"><span data-stu-id="fa907-114">This header specifies that user credentials must be supplied for the "example" domain.</span></span>

<span data-ttu-id="fa907-115">Un'applicazione HTTP può includere un campo di intestazione di autorizzazione con una richiesta inviata al server.</span><span class="sxs-lookup"><span data-stu-id="fa907-115">An HTTP application can include an authorization header field with a request it sends to the server.</span></span> <span data-ttu-id="fa907-116">L'intestazione dell'autorizzazione contiene lo schema di autenticazione e la risposta appropriata richiesta da tale schema.</span><span class="sxs-lookup"><span data-stu-id="fa907-116">The authorization header contains the authentication scheme and the appropriate response required by that scheme.</span></span> <span data-ttu-id="fa907-117">Ad esempio, l'intestazione "Authorization: Basic " verrebbe aggiunta alla richiesta e inviata al server se il client ricevesse l'intestazione di risposta \<username:password> "WWW-Authenticate: Basic Realm="example"".</span><span class="sxs-lookup"><span data-stu-id="fa907-117">For example, the header "Authorization: Basic \<username:password>" would be added to the request and sent to the server if the client received the response header "WWW-Authenticate: Basic Realm="example"".</span></span>

> [!Note]  
> <span data-ttu-id="fa907-118">Anche se vengono visualizzati come testo normale, il nome utente e la password sono in realtà [*codificati in base 64.*](glossary.md)</span><span class="sxs-lookup"><span data-stu-id="fa907-118">Although they are shown here as plain text, the username and password are actually [*base64 encoded*](glossary.md).</span></span>

 

<span data-ttu-id="fa907-119">Esistono due tipi generali di schemi di autenticazione:</span><span class="sxs-lookup"><span data-stu-id="fa907-119">There are two general types of authentication schemes:</span></span>

-   <span data-ttu-id="fa907-120">Schema di autenticazione di base, in cui il nome utente e la password vengono inviati in testo non crittografato al server.</span><span class="sxs-lookup"><span data-stu-id="fa907-120">Basic authentication scheme, in which the user name and password are sent in clear text to the server.</span></span>

    <span data-ttu-id="fa907-121">Lo schema di autenticazione di base si basa sul modello che un client deve identificare con un nome utente e una password per ogni area di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="fa907-121">The Basic authentication scheme is based on the model that a client must identify itself with a user name and password for each realm.</span></span> <span data-ttu-id="fa907-122">Il server servizi la richiesta solo se la richiesta viene inviata con un'intestazione di autorizzazione che include un nome utente e una password validi.</span><span class="sxs-lookup"><span data-stu-id="fa907-122">The server services the request only if the request is sent with an authorization header that includes a valid user name and password.</span></span>

-   <span data-ttu-id="fa907-123">Schemi challenge-response, ad esempio Kerberos, in cui il server sfida il client con i [*dati di autenticazione*](glossary.md).</span><span class="sxs-lookup"><span data-stu-id="fa907-123">Challenge-response schemes, such as Kerberos, in which the server challenges the client with [*authentication data*](glossary.md).</span></span> <span data-ttu-id="fa907-124">Il client trasforma i dati con le credenziali utente e li invia al server per l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="fa907-124">The client transforms the data with the user credentials and sends the transformed data back to the server for authentication.</span></span>

    <span data-ttu-id="fa907-125">Gli schemi challenge-response consentono un'autenticazione più sicura.</span><span class="sxs-lookup"><span data-stu-id="fa907-125">Challenge-response schemes enable a more secure authentication.</span></span> <span data-ttu-id="fa907-126">In uno schema challenge-response il nome utente e la password non vengono mai trasmessi in rete.</span><span class="sxs-lookup"><span data-stu-id="fa907-126">In a challenge-response scheme, the username and password are never transmitted over the network.</span></span> <span data-ttu-id="fa907-127">Dopo che il client ha selezionato uno schema challenge-response, il server restituisce un codice di stato appropriato con una richiesta contenente i dati [*di*](glossary.md) autenticazione per tale schema.</span><span class="sxs-lookup"><span data-stu-id="fa907-127">After the client selects a challenge-response scheme, the server returns an appropriate status code with a challenge that contains the [*authentication data*](glossary.md) for that scheme.</span></span> <span data-ttu-id="fa907-128">Il client invia quindi nuovamente la richiesta con la risposta appropriata per ottenere il servizio richiesto.</span><span class="sxs-lookup"><span data-stu-id="fa907-128">The client then resends the request with the proper response to obtain the requested service.</span></span> <span data-ttu-id="fa907-129">Gli schemi challenge-response possono richiedere più scambi per il completamento.</span><span class="sxs-lookup"><span data-stu-id="fa907-129">Challenge-response schemes can take multiple exchanges to complete.</span></span>

<span data-ttu-id="fa907-130">La tabella seguente contiene gli schemi di autenticazione supportati da WinHTTP, il tipo di autenticazione e una descrizione dello schema.</span><span class="sxs-lookup"><span data-stu-id="fa907-130">The following table contains the authentication schemes that are supported by WinHTTP, the authentication type, and a description of the scheme.</span></span>



| <span data-ttu-id="fa907-131">Schema</span><span class="sxs-lookup"><span data-stu-id="fa907-131">Scheme</span></span>            | <span data-ttu-id="fa907-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="fa907-132">Type</span></span>               | <span data-ttu-id="fa907-133">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fa907-133">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa907-134">Basic (testo non crittografato)</span><span class="sxs-lookup"><span data-stu-id="fa907-134">Basic (plaintext)</span></span> | <span data-ttu-id="fa907-135">Basic</span><span class="sxs-lookup"><span data-stu-id="fa907-135">Basic</span></span>              | <span data-ttu-id="fa907-136">Usa una [*stringa con codifica Base64*](glossary.md) che contiene il nome utente e la password.</span><span class="sxs-lookup"><span data-stu-id="fa907-136">Uses a [*base64 encoded*](glossary.md) string that contains the user name and password.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="fa907-137">Digest</span><span class="sxs-lookup"><span data-stu-id="fa907-137">Digest</span></span>            | <span data-ttu-id="fa907-138">Risposta alla richiesta di richiesta</span><span class="sxs-lookup"><span data-stu-id="fa907-138">Challenge-response</span></span> | <span data-ttu-id="fa907-139">Problemi relativi all'uso di un valore nonce (una stringa di dati specificata dal server).</span><span class="sxs-lookup"><span data-stu-id="fa907-139">Challenges using a nonce (a server-specified data string) value.</span></span> <span data-ttu-id="fa907-140">Una risposta valida contiene un checksum del nome utente, della password, del valore nonce specificato, del [*verbo HTTP*](glossary.md)e del Uniform Resource Identifier (URI).</span><span class="sxs-lookup"><span data-stu-id="fa907-140">A valid response contains a checksum of the user name, the password, the given nonce value, the [*HTTP verb*](glossary.md), and the requested Uniform Resource Identifier (URI).</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="fa907-141">NTLM</span><span class="sxs-lookup"><span data-stu-id="fa907-141">NTLM</span></span>              | <span data-ttu-id="fa907-142">Risposta alla richiesta di richiesta</span><span class="sxs-lookup"><span data-stu-id="fa907-142">Challenge-response</span></span> | <span data-ttu-id="fa907-143">Richiede che [*i dati di autenticazione*](glossary.md) siano trasformati con le credenziali utente per dimostrare l'identità.</span><span class="sxs-lookup"><span data-stu-id="fa907-143">Requires the [*authentication data*](glossary.md) to be transformed with the user credentials to prove identity.</span></span> <span data-ttu-id="fa907-144">Per il corretto funzionamento dell'autenticazione NTLM, è necessario eseguire diversi scambi nella stessa connessione.</span><span class="sxs-lookup"><span data-stu-id="fa907-144">For NTLM authentication to function correctly, several exchanges must take place on the same connection.</span></span> <span data-ttu-id="fa907-145">Pertanto, l'autenticazione NTLM non può essere usata se un proxy interviene non supporta le connessioni keep-alive.</span><span class="sxs-lookup"><span data-stu-id="fa907-145">Therefore, NTLM authentication cannot be used if an intervening proxy does not support keep-alive connections.</span></span> <span data-ttu-id="fa907-146">L'autenticazione NTLM ha esito negativo anche se [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) viene usato con il flag [**WINHTTP \_ DISABLE KEEP \_ \_ ALIVE**](option-flags.md) che disabilita la semantica keep-alive.</span><span class="sxs-lookup"><span data-stu-id="fa907-146">NTLM authentication also fails if [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) is used with the [**WINHTTP\_DISABLE\_KEEP\_ALIVE**](option-flags.md) flag that disables keep-alive semantics.</span></span>                                                                                                                                                                                                                                       |
| <span data-ttu-id="fa907-147">Passport</span><span class="sxs-lookup"><span data-stu-id="fa907-147">Passport</span></span>          | <span data-ttu-id="fa907-148">Risposta alla richiesta di sfida</span><span class="sxs-lookup"><span data-stu-id="fa907-148">Challenge-response</span></span> | <span data-ttu-id="fa907-149">Usa [Microsoft Passport 1.4.](passport-authentication-in-winhttp.md)</span><span class="sxs-lookup"><span data-stu-id="fa907-149">Uses [Microsoft Passport 1.4](passport-authentication-in-winhttp.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="fa907-150">Negotiate</span><span class="sxs-lookup"><span data-stu-id="fa907-150">Negotiate</span></span>         | <span data-ttu-id="fa907-151">Risposta alla richiesta di richiesta</span><span class="sxs-lookup"><span data-stu-id="fa907-151">Challenge-response</span></span> | <span data-ttu-id="fa907-152">Se sia il server che il client usano Windows 2000 o versione successiva, viene usata l'autenticazione Kerberos.</span><span class="sxs-lookup"><span data-stu-id="fa907-152">If both the server and client are using Windows 2000 or later, Kerberos authentication is used.</span></span> <span data-ttu-id="fa907-153">In caso contrario, viene usata l'autenticazione NTLM.</span><span class="sxs-lookup"><span data-stu-id="fa907-153">Otherwise NTLM authentication is used.</span></span> <span data-ttu-id="fa907-154">Kerberos è disponibile nei sistemi operativi Windows 2000 e versioni successive ed è considerato più sicuro dell'autenticazione NTLM.</span><span class="sxs-lookup"><span data-stu-id="fa907-154">Kerberos is available in Windows 2000 and later operating systems and is considered to be more secure than NTLM authentication.</span></span> <span data-ttu-id="fa907-155">Per il corretto funzionamento dell'autenticazione negotiate, è necessario che nella stessa connessione vengano evasi diversi scambi.</span><span class="sxs-lookup"><span data-stu-id="fa907-155">For Negotiate authentication to function correctly, several exchanges must take place on the same connection.</span></span> <span data-ttu-id="fa907-156">Pertanto, l'autenticazione Negotiate non può essere utilizzata se un proxy non supporta le connessioni keep-alive.</span><span class="sxs-lookup"><span data-stu-id="fa907-156">Therefore, Negotiate authentication cannot be used if an intervening proxy does not support keep-alive connections.</span></span> <span data-ttu-id="fa907-157">L'autenticazione negotiate ha esito negativo anche se [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) viene usato con il flag [**WINHTTP \_ DISABLE KEEP \_ \_ ALIVE**](option-flags.md) che disabilita la semantica keep-alive.</span><span class="sxs-lookup"><span data-stu-id="fa907-157">Negotiate authentication also fails if [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) is used with the [**WINHTTP\_DISABLE\_KEEP\_ALIVE**](option-flags.md) flag that disables keep-alive semantics.</span></span> <span data-ttu-id="fa907-158">Lo schema di autenticazione Negotiate viene talvolta chiamato integrated autenticazione di Windows.</span><span class="sxs-lookup"><span data-stu-id="fa907-158">The Negotiate authentication scheme is sometimes called Integrated Windows authentication.</span></span> |



 

## <a name="authentication-in-winhttp-applications"></a><span data-ttu-id="fa907-159">Autenticazione nelle applicazioni WinHTTP</span><span class="sxs-lookup"><span data-stu-id="fa907-159">Authentication in WinHTTP Applications</span></span>

<span data-ttu-id="fa907-160">L'API (Application Programming Interface) WinHTTP fornisce due funzioni usate per accedere alle risorse Internet nelle situazioni in cui è necessaria l'autenticazione: [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) e [**WinHttpQueryAuthSchemes.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes)</span><span class="sxs-lookup"><span data-stu-id="fa907-160">The WinHTTP application programming interface (API) provides two functions used to access Internet resources in situations where authentication is required: [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) and [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes).</span></span>

<span data-ttu-id="fa907-161">Quando si riceve una risposta con un codice di stato 401 o 407, è possibile usare [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes) per analizzare le intestazioni di autenticazione per determinare gli schemi di autenticazione supportati e la destinazione dell'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="fa907-161">When a response is received with a 401 or 407 status code, [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes) can be used to parse the authentication headers to determine the supported authentication schemes and the authentication target.</span></span> <span data-ttu-id="fa907-162">La destinazione dell'autenticazione è il server o il proxy che richiede l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="fa907-162">The authentication target is the server or proxy that requests authentication.</span></span> <span data-ttu-id="fa907-163">**WinHttpQueryAuthSchemes** determina anche il primo schema di autenticazione, dagli schemi disponibili, in base alle preferenze dello schema di autenticazione suggerite dal server.</span><span class="sxs-lookup"><span data-stu-id="fa907-163">**WinHttpQueryAuthSchemes** also determines the first authentication scheme, from the available schemes, based on the authentication scheme preferences suggested by the server.</span></span> <span data-ttu-id="fa907-164">Questo metodo per la scelta di uno schema di autenticazione è il comportamento suggerito da [RFC 2616.](https://www.ietf.org/rfc/rfc2616.txt)</span><span class="sxs-lookup"><span data-stu-id="fa907-164">This method for choosing an authentication scheme is the behavior suggested by [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span></span>

<span data-ttu-id="fa907-165">[**WinHttpSetCredentials consente**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) a un'applicazione di specificare lo schema di autenticazione usato insieme a un nome utente e una password validi da usare nel server o nel proxy di destinazione.</span><span class="sxs-lookup"><span data-stu-id="fa907-165">[**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) enables an application to specify the authentication scheme that is used along with a valid username and password for use on the target server or proxy.</span></span> <span data-ttu-id="fa907-166">Dopo aver impostato le credenziali e aver reinviato la richiesta, le intestazioni necessarie vengono generate e aggiunte automaticamente alla richiesta.</span><span class="sxs-lookup"><span data-stu-id="fa907-166">After setting the credentials and resending the request, the necessary headers are generated and added to the request automatically.</span></span> <span data-ttu-id="fa907-167">Poiché alcuni schemi di autenticazione richiedono più [**transazioni, WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) potrebbe restituire l'errore ERROR \_ WINHTTP \_ RESEND \_ REQUEST.</span><span class="sxs-lookup"><span data-stu-id="fa907-167">Because some authentication schemes require multiple transactions [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) could return the error, ERROR\_WINHTTP\_RESEND\_REQUEST.</span></span> <span data-ttu-id="fa907-168">Quando viene rilevato questo errore, l'applicazione deve continuare a inviare nuovamente la richiesta fino a quando non viene ricevuta una risposta che non contiene un codice di stato 401 o 407.</span><span class="sxs-lookup"><span data-stu-id="fa907-168">When this error is encountered, the application should continue to resend the request until a response is received that does not contain a 401 or 407 status code.</span></span> <span data-ttu-id="fa907-169">Un codice di stato 200 indica che la risorsa è disponibile e che la richiesta ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="fa907-169">A 200 status code indicates that the resource is available and the request is successful.</span></span> <span data-ttu-id="fa907-170">Per altri codici di stato che possono essere restituiti, vedere Codici di stato [**HTTP.**](http-status-codes.md)</span><span class="sxs-lookup"><span data-stu-id="fa907-170">See [**HTTP Status Codes**](http-status-codes.md) for additional status codes that can be returned.</span></span>

<span data-ttu-id="fa907-171">Se uno schema di autenticazione e credenziali accettabili sono noti prima dell'invio di una richiesta al server, un'applicazione può chiamare [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) prima di [**chiamare WinHttpSendRequest.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)</span><span class="sxs-lookup"><span data-stu-id="fa907-171">If an acceptable authentication scheme and credentials are known before a request is sent to the server, an application can call [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) before calling [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span> <span data-ttu-id="fa907-172">In questo caso, WinHTTP tenta di eseguire la pre-autenticazione con il server fornendo credenziali o dati di [*autenticazione*](glossary.md) nella richiesta iniziale al server.</span><span class="sxs-lookup"><span data-stu-id="fa907-172">In this case, WinHTTP attempts pre-authentication with the server by providing credentials or [*authentication data*](glossary.md) in the initial request to the server.</span></span> <span data-ttu-id="fa907-173">La pre-autenticazione può ridurre il numero di scambi nel processo di autenticazione e quindi migliorare le prestazioni dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="fa907-173">Pre-authentication can decrease the number of exchanges in the authentication process and therefore improve application performance.</span></span>

<span data-ttu-id="fa907-174">La preautenticazione può essere usata con gli schemi di autenticazione seguenti:</span><span class="sxs-lookup"><span data-stu-id="fa907-174">Preauthentication can be used with the following authentication schemes:</span></span>

-   <span data-ttu-id="fa907-175">Di base: sempre possibile.</span><span class="sxs-lookup"><span data-stu-id="fa907-175">Basic - always possible.</span></span>
-   <span data-ttu-id="fa907-176">Negoziazione della risoluzione in Kerberos- molto probabilmente possibile; l'unica eccezione si verifica quando le differenze di tempo sono disattivate tra il client e il controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="fa907-176">Negotiate resolving into Kerberos - very likely possible; the only exception is when the time-skews are off between the client and the domain controller.</span></span>
-   <span data-ttu-id="fa907-177">(Negoziazione della risoluzione in NTLM) - mai possibile.</span><span class="sxs-lookup"><span data-stu-id="fa907-177">(Negotiate resolving into NTLM) - never possible.</span></span>
-   <span data-ttu-id="fa907-178">NTLM: possibile solo in Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="fa907-178">NTLM - possible in Windows Server 2008 R2 only.</span></span>
-   <span data-ttu-id="fa907-179">Digest: mai possibile.</span><span class="sxs-lookup"><span data-stu-id="fa907-179">Digest - never possible.</span></span>
-   <span data-ttu-id="fa907-180">Passport: mai possibile; dopo la richiesta di verifica iniziale, WinHTTP usa i cookie per eseguire la pre-autenticazione in Passport.</span><span class="sxs-lookup"><span data-stu-id="fa907-180">Passport - never possible; after the initial challenge-response, WinHTTP uses cookies to pre-authenticate to Passport.</span></span>

<span data-ttu-id="fa907-181">Una tipica applicazione WinHTTP completa i passaggi seguenti per gestire l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="fa907-181">A typical WinHTTP application completes the following steps in order to handle authentication.</span></span>

-   <span data-ttu-id="fa907-182">Richiedere una risorsa con [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) e [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span><span class="sxs-lookup"><span data-stu-id="fa907-182">Request a resource with [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) and [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span>
-   <span data-ttu-id="fa907-183">Controllare le intestazioni della risposta [**con WinHttpQueryHeaders.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders)</span><span class="sxs-lookup"><span data-stu-id="fa907-183">Check the response headers with [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders).</span></span>
-   <span data-ttu-id="fa907-184">Se viene restituito un codice di stato 401 o 407 che indica che l'autenticazione è necessaria, chiamare [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes) per trovare uno schema accettabile.</span><span class="sxs-lookup"><span data-stu-id="fa907-184">If a 401 or 407 status code is returned indicating that authentication is required, call [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes) to find an acceptable scheme.</span></span>
-   <span data-ttu-id="fa907-185">Impostare lo schema di autenticazione, il nome utente e la password [**con WinHttpSetCredentials.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials)</span><span class="sxs-lookup"><span data-stu-id="fa907-185">Set the authentication scheme, username, and password with [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials).</span></span>
-   <span data-ttu-id="fa907-186">Inviare nuovamente la richiesta con lo stesso handle di richiesta chiamando [**WinHttpSendRequest.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)</span><span class="sxs-lookup"><span data-stu-id="fa907-186">Resend the request with the same request handle by calling [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span>

<span data-ttu-id="fa907-187">Le credenziali impostate da [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) vengono usate solo per una richiesta.</span><span class="sxs-lookup"><span data-stu-id="fa907-187">The credentials set by [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) are only used for one request.</span></span> <span data-ttu-id="fa907-188">WinHTTP non memorizza nella cache le credenziali da usare in altre richieste, il che significa che è necessario scrivere applicazioni in grado di rispondere a più richieste.</span><span class="sxs-lookup"><span data-stu-id="fa907-188">WinHTTP does not cache the credentials to use in other requests, which means that applications must be written that can respond to multiple requests.</span></span> <span data-ttu-id="fa907-189">Se una connessione autenticata viene usata di nuovo, è possibile che non venga inviata una richiesta ad altre richieste, ma il codice dovrebbe essere in grado di rispondere a una richiesta in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="fa907-189">If an authenticated connection is re-used, other requests may not be challenged, but your code should be able to respond to a request at any time.</span></span>

### <a name="example-retrieving-a-document"></a><span data-ttu-id="fa907-190">Esempio: Recupero di un documento</span><span class="sxs-lookup"><span data-stu-id="fa907-190">Example: Retrieving a Document</span></span>

<span data-ttu-id="fa907-191">Il codice di esempio seguente tenta di recuperare un documento specificato da un server HTTP.</span><span class="sxs-lookup"><span data-stu-id="fa907-191">The following sample code attempts to retrieve a specified document from an HTTP server.</span></span> <span data-ttu-id="fa907-192">Il codice di stato viene recuperato dalla risposta per determinare se è necessaria l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="fa907-192">The status code is retrieved from the response to determine if authentication is required.</span></span> <span data-ttu-id="fa907-193">Se viene trovato un codice di stato 200, il documento è disponibile.</span><span class="sxs-lookup"><span data-stu-id="fa907-193">If a 200 status code is found, the document is available.</span></span> <span data-ttu-id="fa907-194">Se viene trovato un codice di stato 401 o 407, l'autenticazione è necessaria prima di poter recuperare il documento.</span><span class="sxs-lookup"><span data-stu-id="fa907-194">If a status code of 401 or 407 is found, authentication is required before the document can be retrieved.</span></span> <span data-ttu-id="fa907-195">Per qualsiasi altro codice di stato, viene visualizzato un messaggio di errore.</span><span class="sxs-lookup"><span data-stu-id="fa907-195">For any other status code, an error message is displayed.</span></span> <span data-ttu-id="fa907-196">Per un elenco dei possibili codici di stato, vedere Codici di stato [**HTTP.**](http-status-codes.md)</span><span class="sxs-lookup"><span data-stu-id="fa907-196">See [**HTTP Status Codes**](http-status-codes.md) for a list of possible status codes.</span></span>


```C++
#include <windows.h>
#include <winhttp.h>
#include <stdio.h>

#pragma comment(lib, "winhttp.lib")

DWORD ChooseAuthScheme( DWORD dwSupportedSchemes )
{
  //  It is the server's responsibility only to accept 
  //  authentication schemes that provide a sufficient
  //  level of security to protect the servers resources.
  //
  //  The client is also obligated only to use an authentication
  //  scheme that adequately protects its username and password.
  //
  //  Thus, this sample code does not use Basic authentication  
  //  becaus Basic authentication exposes the client's username
  //  and password to anyone monitoring the connection.
  
  if( dwSupportedSchemes & WINHTTP_AUTH_SCHEME_NEGOTIATE )
    return WINHTTP_AUTH_SCHEME_NEGOTIATE;
  else if( dwSupportedSchemes & WINHTTP_AUTH_SCHEME_NTLM )
    return WINHTTP_AUTH_SCHEME_NTLM;
  else if( dwSupportedSchemes & WINHTTP_AUTH_SCHEME_PASSPORT )
    return WINHTTP_AUTH_SCHEME_PASSPORT;
  else if( dwSupportedSchemes & WINHTTP_AUTH_SCHEME_DIGEST )
    return WINHTTP_AUTH_SCHEME_DIGEST;
  else
    return 0;
}

struct SWinHttpSampleGet
{
  LPCWSTR szServer;
  LPCWSTR szPath;
  BOOL fUseSSL;
  LPCWSTR szServerUsername;
  LPCWSTR szServerPassword;
  LPCWSTR szProxyUsername;
  LPCWSTR szProxyPassword;
};

void WinHttpAuthSample( IN SWinHttpSampleGet *pGetRequest )
{
  DWORD dwStatusCode = 0;
  DWORD dwSupportedSchemes;
  DWORD dwFirstScheme;
  DWORD dwSelectedScheme;
  DWORD dwTarget;
  DWORD dwLastStatus = 0;
  DWORD dwSize = sizeof(DWORD);
  BOOL  bResults = FALSE;
  BOOL  bDone = FALSE;

  DWORD dwProxyAuthScheme = 0;
  HINTERNET  hSession = NULL, 
             hConnect = NULL,
             hRequest = NULL;

  // Use WinHttpOpen to obtain a session handle.
  hSession = WinHttpOpen( L"WinHTTP Example/1.0",  
                          WINHTTP_ACCESS_TYPE_DEFAULT_PROXY,
                          WINHTTP_NO_PROXY_NAME, 
                          WINHTTP_NO_PROXY_BYPASS, 0 );

  INTERNET_PORT nPort = ( pGetRequest->fUseSSL ) ? 
                        INTERNET_DEFAULT_HTTPS_PORT  :
                        INTERNET_DEFAULT_HTTP_PORT;

  // Specify an HTTP server.
  if( hSession )
    hConnect = WinHttpConnect( hSession, 
                               pGetRequest->szServer, 
                               nPort, 0 );

  // Create an HTTP request handle.
  if( hConnect )
    hRequest = WinHttpOpenRequest( hConnect, 
                                   L"GET", 
                                   pGetRequest->szPath,
                                   NULL, 
                                   WINHTTP_NO_REFERER, 
                                   WINHTTP_DEFAULT_ACCEPT_TYPES,
                                   ( pGetRequest->fUseSSL ) ? 
                                       WINHTTP_FLAG_SECURE : 0 );

  // Continue to send a request until status code 
  // is not 401 or 407.
  if( hRequest == NULL )
    bDone = TRUE;

  while( !bDone )
  {
    //  If a proxy authentication challenge was responded to, reset
    //  those credentials before each SendRequest, because the proxy  
    //  may require re-authentication after responding to a 401 or  
    //  to a redirect. If you don't, you can get into a 
    //  407-401-407-401- loop.
    if( dwProxyAuthScheme != 0 )
      bResults = WinHttpSetCredentials( hRequest, 
                                        WINHTTP_AUTH_TARGET_PROXY, 
                                        dwProxyAuthScheme, 
                                        pGetRequest->szProxyUsername,
                                        pGetRequest->szProxyPassword,
                                        NULL );
    // Send a request.
    bResults = WinHttpSendRequest( hRequest,
                                   WINHTTP_NO_ADDITIONAL_HEADERS,
                                   0,
                                   WINHTTP_NO_REQUEST_DATA,
                                   0, 
                                   0, 
                                   0 );

    // End the request.
    if( bResults )
      bResults = WinHttpReceiveResponse( hRequest, NULL );

    // Resend the request in case of 
    // ERROR_WINHTTP_RESEND_REQUEST error.
    if( !bResults && GetLastError( ) == ERROR_WINHTTP_RESEND_REQUEST)
        continue;

    // Check the status code.
    if( bResults ) 
      bResults = WinHttpQueryHeaders( hRequest, 
                                      WINHTTP_QUERY_STATUS_CODE |
                                      WINHTTP_QUERY_FLAG_NUMBER,
                                      NULL, 
                                      &dwStatusCode, 
                                      &dwSize, 
                                      NULL );

    if( bResults )
    {
      switch( dwStatusCode )
      {
        case 200: 
          // The resource was successfully retrieved.
          // You can use WinHttpReadData to read the 
          // contents of the server's response.
          printf( "The resource was successfully retrieved.\n" );
          bDone = TRUE;
          break;

        case 401:
          // The server requires authentication.
          printf(" The server requires authentication. Sending credentials...\n" );

          // Obtain the supported and preferred schemes.
          bResults = WinHttpQueryAuthSchemes( hRequest, 
                                              &dwSupportedSchemes, 
                                              &dwFirstScheme, 
                                              &dwTarget );

          // Set the credentials before resending the request.
          if( bResults )
          {
            dwSelectedScheme = ChooseAuthScheme( dwSupportedSchemes);

            if( dwSelectedScheme == 0 )
              bDone = TRUE;
            else
              bResults = WinHttpSetCredentials( hRequest, 
                                        dwTarget, 
                                        dwSelectedScheme,
                                        pGetRequest->szServerUsername,
                                        pGetRequest->szServerPassword,
                                        NULL );
          }

          // If the same credentials are requested twice, abort the
          // request.  For simplicity, this sample does not check
          // for a repeated sequence of status codes.
          if( dwLastStatus == 401 )
            bDone = TRUE;

          break;

        case 407:
          // The proxy requires authentication.
          printf( "The proxy requires authentication.  Sending credentials...\n" );

          // Obtain the supported and preferred schemes.
          bResults = WinHttpQueryAuthSchemes( hRequest, 
                                              &dwSupportedSchemes, 
                                              &dwFirstScheme, 
                                              &dwTarget );

          // Set the credentials before resending the request.
          if( bResults )
            dwProxyAuthScheme = ChooseAuthScheme(dwSupportedSchemes);

          // If the same credentials are requested twice, abort the
          // request.  For simplicity, this sample does not check 
          // for a repeated sequence of status codes.
          if( dwLastStatus == 407 )
            bDone = TRUE;
          break;

        default:
          // The status code does not indicate success.
          printf("Error. Status code %d returned.\n", dwStatusCode);
          bDone = TRUE;
      }
    }

    // Keep track of the last status code.
    dwLastStatus = dwStatusCode;

    // If there are any errors, break out of the loop.
    if( !bResults ) 
        bDone = TRUE;
  }

  // Report any errors.
  if( !bResults )
  {
    DWORD dwLastError = GetLastError( );
    printf( "Error %d has occurred.\n", dwLastError );
  }

  // Close any open handles.
  if( hRequest ) WinHttpCloseHandle( hRequest );
  if( hConnect ) WinHttpCloseHandle( hConnect );
  if( hSession ) WinHttpCloseHandle( hSession );
}

```



## <a name="automatic-logon-policy"></a><span data-ttu-id="fa907-197">Criteri di accesso automatico</span><span class="sxs-lookup"><span data-stu-id="fa907-197">Automatic Logon Policy</span></span>

<span data-ttu-id="fa907-198">I criteri di accesso automatico (accesso automatico) determinano quando è accettabile che WinHTTP includa le credenziali predefinite in una richiesta.</span><span class="sxs-lookup"><span data-stu-id="fa907-198">The automatic logon (auto-logon) policy determines when it is acceptable for WinHTTP to include the default credentials in a request.</span></span> <span data-ttu-id="fa907-199">Le credenziali predefinite sono il token del thread corrente o il token di sessione a seconda che WinHTTP sia usato in modalità sincrona o asincrona.</span><span class="sxs-lookup"><span data-stu-id="fa907-199">The default credentials are either the current thread token or the session token depending on whether WinHTTP is used in synchronous or asynchronous mode.</span></span> <span data-ttu-id="fa907-200">Il token del thread viene usato in modalità sincrona e il token di sessione viene usato in modalità asincrona.</span><span class="sxs-lookup"><span data-stu-id="fa907-200">The thread token is used in synchronous mode, and the session token is used in asynchronous mode.</span></span> <span data-ttu-id="fa907-201">Queste credenziali predefinite sono spesso il nome utente e la password usati per accedere a Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="fa907-201">These default credentials are often the username and password used to log on to Microsoft Windows.</span></span>

<span data-ttu-id="fa907-202">I criteri di accesso automatico sono stati implementati per impedire l'uso casuale di queste credenziali per l'autenticazione in un server non attendibile.</span><span class="sxs-lookup"><span data-stu-id="fa907-202">The auto-logon policy was implemented to prevent these credentials from being casually used to authenticate against an untrusted server.</span></span> <span data-ttu-id="fa907-203">Per impostazione predefinita, il livello di sicurezza è impostato su WINHTTP \_ AUTOLOGON SECURITY LEVEL MEDIUM, che consente l'uso delle credenziali predefinite solo per \_ \_ le richieste \_ Intranet.</span><span class="sxs-lookup"><span data-stu-id="fa907-203">By default, the security level is set to WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_MEDIUM, which allows the default credentials to be used only for Intranet requests.</span></span> <span data-ttu-id="fa907-204">I criteri di accesso automatico si applicano solo agli schemi di autenticazione NTLM e Negotiate.</span><span class="sxs-lookup"><span data-stu-id="fa907-204">The auto-logon policy only applies to the NTLM and Negotiate authentication schemes.</span></span> <span data-ttu-id="fa907-205">Le credenziali non vengono mai trasmesse automaticamente con altri schemi.</span><span class="sxs-lookup"><span data-stu-id="fa907-205">Credentials are never automatically transmitted with other schemes.</span></span>

<span data-ttu-id="fa907-206">I criteri di accesso automatico possono essere impostati usando la [**funzione WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) con il flag [**WINHTTP \_ OPTION \_ AUTOLOGON \_ POLICY.**](option-flags.md)</span><span class="sxs-lookup"><span data-stu-id="fa907-206">The auto-logon policy can be set using the [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) function with the [**WINHTTP\_OPTION\_AUTOLOGON\_POLICY**](option-flags.md) flag.</span></span> <span data-ttu-id="fa907-207">Questo flag si applica solo all'handle della richiesta.</span><span class="sxs-lookup"><span data-stu-id="fa907-207">This flag applies only to the request handle.</span></span> <span data-ttu-id="fa907-208">Quando il criterio è impostato su WINHTTP AUTOLOGON SECURITY LEVEL LOW, le credenziali predefinite \_ possono essere inviate a tutti i \_ \_ \_ server.</span><span class="sxs-lookup"><span data-stu-id="fa907-208">When the policy is set to WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_LOW, default credentials can be sent to all servers.</span></span> <span data-ttu-id="fa907-209">Quando il criterio è impostato su WINHTTP \_ AUTOLOGON \_ SECURITY \_ LEVEL \_ HIGH, le credenziali predefinite non possono essere usate per l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="fa907-209">When the policy is set to WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_HIGH, default credentials cannot be used for authentication.</span></span> <span data-ttu-id="fa907-210">È consigliabile usare l'accesso automatico a livello MEDIUM.</span><span class="sxs-lookup"><span data-stu-id="fa907-210">It is strongly recommended that you use the auto-logon at the MEDIUM level.</span></span>

## <a name="stored-user-names-and-passwords"></a><span data-ttu-id="fa907-211">Gestione nomi utente e password archiviati</span><span class="sxs-lookup"><span data-stu-id="fa907-211">Stored User Names and Passwords</span></span>

<span data-ttu-id="fa907-212">Windows XP ha introdotto il concetto di nomi utente e password archiviati.</span><span class="sxs-lookup"><span data-stu-id="fa907-212">Windows XP introduced the concept of Stored User Names and Passwords.</span></span> <span data-ttu-id="fa907-213">Se le credenziali Passport di un utente vengono salvate tramite la **Registrazione** guidata passport o la finestra di dialogo delle credenziali **standard,** vengono salvate in Nomi utente e password archiviati.</span><span class="sxs-lookup"><span data-stu-id="fa907-213">If a user's Passport credentials are saved through the **Passport Registration Wizard** or the standard **Credential Dialog**, it is saved in the Stored User Names and Passwords.</span></span> <span data-ttu-id="fa907-214">Quando si usa WinHTTP in Windows XP o versioni successive, WinHTTP usa automaticamente le credenziali in Nomi utente e password archiviati se le credenziali non sono impostate in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="fa907-214">When using WinHTTP on Windows XP or later, WinHTTP automatically uses the credentials in the Stored User Names and Passwords if credentials are not explicitly set.</span></span> <span data-ttu-id="fa907-215">È simile al supporto delle credenziali di accesso predefinite per NTLM/Kerberos.</span><span class="sxs-lookup"><span data-stu-id="fa907-215">This is similar to the support of default logon credentials for NTLM/Kerberos.</span></span> <span data-ttu-id="fa907-216">Tuttavia, l'uso delle credenziali Passport predefinite non è soggetto alle impostazioni dei criteri di accesso automatico.</span><span class="sxs-lookup"><span data-stu-id="fa907-216">However, use of default Passport credentials is not subject to the automatic logon policy settings.</span></span>

 

 



