---
description: Alcuni server e proxy HTTP richiedono l'autenticazione prima di consentire l'accesso alle risorse su Internet. Le funzioni dei servizi HTTP di Microsoft Windows (WinHTTP) supportano l'autenticazione del server e del proxy per le sessioni HTTP.
ms.assetid: 077d6275-8600-4091-b78e-419a41a2101a
title: Autenticazione in WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dd40e6da1f455e04e24fa740cf4d83da7e0472e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231676"
---
# <a name="authentication-in-winhttp"></a><span data-ttu-id="0a7e1-104">Autenticazione in WinHTTP</span><span class="sxs-lookup"><span data-stu-id="0a7e1-104">Authentication in WinHTTP</span></span>

<span data-ttu-id="0a7e1-105">Alcuni server e proxy HTTP richiedono l'autenticazione prima di consentire l'accesso alle risorse su Internet.</span><span class="sxs-lookup"><span data-stu-id="0a7e1-105">Some HTTP servers and proxies require authentication before allowing access to resources on the Internet.</span></span> <span data-ttu-id="0a7e1-106">Le funzioni dei servizi HTTP di Microsoft Windows (WinHTTP) supportano l'autenticazione del server e del proxy per le sessioni HTTP.</span><span class="sxs-lookup"><span data-stu-id="0a7e1-106">The Microsoft Windows HTTP Services (WinHTTP) functions support server and proxy authentication for HTTP sessions.</span></span>

## <a name="about-http-authentication"></a><span data-ttu-id="0a7e1-107">Informazioni sull'autenticazione HTTP</span><span class="sxs-lookup"><span data-stu-id="0a7e1-107">About HTTP Authentication</span></span>

<span data-ttu-id="0a7e1-108">Se è richiesta l'autenticazione, l'applicazione HTTP riceve un codice di stato 401 (il server richiede l'autenticazione) o 407 (il proxy richiede l'autenticazione).</span><span class="sxs-lookup"><span data-stu-id="0a7e1-108">If authentication is required, the HTTP application receives a status code of 401 (server requires authentication) or 407 (proxy requires authentication).</span></span> <span data-ttu-id="0a7e1-109">Oltre al codice di stato, il proxy o il server invia una o più intestazioni di autenticazione: WWW-Authenticate (per l'autenticazione del server) o Proxy-Authenticate (per l'autenticazione del proxy).</span><span class="sxs-lookup"><span data-stu-id="0a7e1-109">Along with the status code, the proxy or server sends one or more authenticate headers: WWW-Authenticate (for server authentication) or Proxy-Authenticate (for proxy authentication).</span></span>

<span data-ttu-id="0a7e1-110">Ogni intestazione Authenticate contiene uno schema di autenticazione supportato e, per gli schemi di base e del digest, un'area di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="0a7e1-110">Each authenticate header contains a supported authentication scheme and, for the Basic and Digest schemes, a realm.</span></span> <span data-ttu-id="0a7e1-111">Se sono supportati più schemi di autenticazione, il server restituisce più intestazioni di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="0a7e1-111">If multiple authentication schemes are supported, the server returns multiple authenticate headers.</span></span> <span data-ttu-id="0a7e1-112">Il valore dell'area di autenticazione fa distinzione tra maiuscole e minuscole e definisce un set di server o proxy per i quali vengono accettate le stesse credenziali.</span><span class="sxs-lookup"><span data-stu-id="0a7e1-112">The realm value is case-sensitive and defines a set of servers or proxies for which the same credentials are accepted.</span></span> <span data-ttu-id="0a7e1-113">Ad esempio, è possibile che venga restituita l'intestazione "WWW-Authenticate: Basic realm =" example "" quando è richiesta l'autenticazione server.</span><span class="sxs-lookup"><span data-stu-id="0a7e1-113">For example, the header "WWW-Authenticate: Basic Realm="example"" might be returned when server authentication is required.</span></span> <span data-ttu-id="0a7e1-114">Questa intestazione specifica che è necessario fornire le credenziali utente per il dominio "example".</span><span class="sxs-lookup"><span data-stu-id="0a7e1-114">This header specifies that user credentials must be supplied for the "example" domain.</span></span>

<span data-ttu-id="0a7e1-115">Un'applicazione HTTP può includere un campo di intestazione dell'autorizzazione con una richiesta inviata al server.</span><span class="sxs-lookup"><span data-stu-id="0a7e1-115">An HTTP application can include an authorization header field with a request it sends to the server.</span></span> <span data-ttu-id="0a7e1-116">L'intestazione Authorization contiene lo schema di autenticazione e la risposta appropriata richiesta da tale schema.</span><span class="sxs-lookup"><span data-stu-id="0a7e1-116">The authorization header contains the authentication scheme and the appropriate response required by that scheme.</span></span> <span data-ttu-id="0a7e1-117">Ad esempio, l'intestazione "Authorization: Basic <username: password>" viene aggiunta alla richiesta e inviata al server se il client ha ricevuto l'intestazione della risposta "WWW-Authenticate: Basic realm =" example "".</span><span class="sxs-lookup"><span data-stu-id="0a7e1-117">For example, the header "Authorization: Basic <username:password>" would be added to the request and sent to the server if the client received the response header "WWW-Authenticate: Basic Realm="example"".</span></span>

> [!Note]  
> <span data-ttu-id="0a7e1-118">Sebbene siano visualizzati come testo normale, il nome utente e la password sono in realtà [*codificati con Base64*](glossary.md).</span><span class="sxs-lookup"><span data-stu-id="0a7e1-118">Although they are shown here as plain text, the username and password are actually [*base64 encoded*](glossary.md).</span></span>

 

<span data-ttu-id="0a7e1-119">Esistono due tipi generali di schemi di autenticazione:</span><span class="sxs-lookup"><span data-stu-id="0a7e1-119">There are two general types of authentication schemes:</span></span>

-   <span data-ttu-id="0a7e1-120">Schema di autenticazione di base, in cui il nome utente e la password vengono inviati in testo non crittografato al server.</span><span class="sxs-lookup"><span data-stu-id="0a7e1-120">Basic authentication scheme, in which the user name and password are sent in clear text to the server.</span></span>

    <span data-ttu-id="0a7e1-121">Lo schema di autenticazione di base è basato sul modello che deve essere identificato da un client con un nome utente e una password per ogni area di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="0a7e1-121">The Basic authentication scheme is based on the model that a client must identify itself with a user name and password for each realm.</span></span> <span data-ttu-id="0a7e1-122">Il server Servizi la richiesta solo se la richiesta viene inviata con un'intestazione di autorizzazione che include un nome utente e una password validi.</span><span class="sxs-lookup"><span data-stu-id="0a7e1-122">The server services the request only if the request is sent with an authorization header that includes a valid user name and password.</span></span>

-   <span data-ttu-id="0a7e1-123">Schemi di richiesta-risposta, ad esempio Kerberos, in cui il server sfida il client con i [*dati di autenticazione*](glossary.md).</span><span class="sxs-lookup"><span data-stu-id="0a7e1-123">Challenge-response schemes, such as Kerberos, in which the server challenges the client with [*authentication data*](glossary.md).</span></span> <span data-ttu-id="0a7e1-124">Il client trasforma i dati con le credenziali utente e invia di nuovo i dati trasformati al server per l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="0a7e1-124">The client transforms the data with the user credentials and sends the transformed data back to the server for authentication.</span></span>

    <span data-ttu-id="0a7e1-125">Gli schemi di richiesta-risposta consentono un'autenticazione più sicura.</span><span class="sxs-lookup"><span data-stu-id="0a7e1-125">Challenge-response schemes enable a more secure authentication.</span></span> <span data-ttu-id="0a7e1-126">In uno schema di richiesta-risposta, il nome utente e la password non vengono mai trasmessi in rete.</span><span class="sxs-lookup"><span data-stu-id="0a7e1-126">In a challenge-response scheme, the username and password are never transmitted over the network.</span></span> <span data-ttu-id="0a7e1-127">Quando il client seleziona uno schema di richiesta-risposta, il server restituisce un codice di stato appropriato con una richiesta di verifica che contiene i [*dati di autenticazione*](glossary.md) per tale schema.</span><span class="sxs-lookup"><span data-stu-id="0a7e1-127">After the client selects a challenge-response scheme, the server returns an appropriate status code with a challenge that contains the [*authentication data*](glossary.md) for that scheme.</span></span> <span data-ttu-id="0a7e1-128">Il client invia nuovamente la richiesta con la risposta appropriata per ottenere il servizio richiesto.</span><span class="sxs-lookup"><span data-stu-id="0a7e1-128">The client then resends the request with the proper response to obtain the requested service.</span></span> <span data-ttu-id="0a7e1-129">Gli schemi di richiesta-risposta possono richiedere più scambi per il completamento.</span><span class="sxs-lookup"><span data-stu-id="0a7e1-129">Challenge-response schemes can take multiple exchanges to complete.</span></span>

<span data-ttu-id="0a7e1-130">Nella tabella seguente sono inclusi gli schemi di autenticazione supportati da WinHTTP, il tipo di autenticazione e una descrizione dello schema.</span><span class="sxs-lookup"><span data-stu-id="0a7e1-130">The following table contains the authentication schemes that are supported by WinHTTP, the authentication type, and a description of the scheme.</span></span>



| <span data-ttu-id="0a7e1-131">Schema</span><span class="sxs-lookup"><span data-stu-id="0a7e1-131">Scheme</span></span>            | <span data-ttu-id="0a7e1-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="0a7e1-132">Type</span></span>               | <span data-ttu-id="0a7e1-133">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0a7e1-133">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a7e1-134">Di base (testo non crittografato)</span><span class="sxs-lookup"><span data-stu-id="0a7e1-134">Basic (plaintext)</span></span> | <span data-ttu-id="0a7e1-135">Basic</span><span class="sxs-lookup"><span data-stu-id="0a7e1-135">Basic</span></span>              | <span data-ttu-id="0a7e1-136">Usa una stringa [*con codifica Base64*](glossary.md) che contiene il nome utente e la password.</span><span class="sxs-lookup"><span data-stu-id="0a7e1-136">Uses a [*base64 encoded*](glossary.md) string that contains the user name and password.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="0a7e1-137">Digest</span><span class="sxs-lookup"><span data-stu-id="0a7e1-137">Digest</span></span>            | <span data-ttu-id="0a7e1-138">Richiesta-risposta</span><span class="sxs-lookup"><span data-stu-id="0a7e1-138">Challenge-response</span></span> | <span data-ttu-id="0a7e1-139">Problemi di utilizzo di un valore nonce (una stringa di dati specificata dal server).</span><span class="sxs-lookup"><span data-stu-id="0a7e1-139">Challenges using a nonce (a server-specified data string) value.</span></span> <span data-ttu-id="0a7e1-140">Una risposta valida contiene un checksum del nome utente, la password, il valore nonce specificato, il [*verbo http*](glossary.md)e l'URI (Uniform Resource Identifier richiesto).</span><span class="sxs-lookup"><span data-stu-id="0a7e1-140">A valid response contains a checksum of the user name, the password, the given nonce value, the [*HTTP verb*](glossary.md), and the requested Uniform Resource Identifier (URI).</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="0a7e1-141">NTLM</span><span class="sxs-lookup"><span data-stu-id="0a7e1-141">NTLM</span></span>              | <span data-ttu-id="0a7e1-142">Richiesta-risposta</span><span class="sxs-lookup"><span data-stu-id="0a7e1-142">Challenge-response</span></span> | <span data-ttu-id="0a7e1-143">Richiede la trasformazione [*dei dati di autenticazione*](glossary.md) con le credenziali utente per dimostrare l'identità.</span><span class="sxs-lookup"><span data-stu-id="0a7e1-143">Requires the [*authentication data*](glossary.md) to be transformed with the user credentials to prove identity.</span></span> <span data-ttu-id="0a7e1-144">Per il corretto funzionamento dell'autenticazione NTLM, è necessario eseguire diversi scambi nella stessa connessione.</span><span class="sxs-lookup"><span data-stu-id="0a7e1-144">For NTLM authentication to function correctly, several exchanges must take place on the same connection.</span></span> <span data-ttu-id="0a7e1-145">Pertanto, non è possibile usare l'autenticazione NTLM se un proxy corrispondente non supporta le connessioni keep-alive.</span><span class="sxs-lookup"><span data-stu-id="0a7e1-145">Therefore, NTLM authentication cannot be used if an intervening proxy does not support keep-alive connections.</span></span> <span data-ttu-id="0a7e1-146">L'autenticazione NTLM ha esito negativo anche se [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) viene usato con il flag di [**\_ disabilitazione \_ Keep \_**](option-flags.md) -Alive WinHTTP che disabilita la semantica Keep-Alive.</span><span class="sxs-lookup"><span data-stu-id="0a7e1-146">NTLM authentication also fails if [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) is used with the [**WINHTTP\_DISABLE\_KEEP\_ALIVE**](option-flags.md) flag that disables keep-alive semantics.</span></span>                                                                                                                                                                                                                                       |
| <span data-ttu-id="0a7e1-147">Passport</span><span class="sxs-lookup"><span data-stu-id="0a7e1-147">Passport</span></span>          | <span data-ttu-id="0a7e1-148">Richiesta-risposta</span><span class="sxs-lookup"><span data-stu-id="0a7e1-148">Challenge-response</span></span> | <span data-ttu-id="0a7e1-149">USA [Microsoft Passport 1,4](passport-authentication-in-winhttp.md).</span><span class="sxs-lookup"><span data-stu-id="0a7e1-149">Uses [Microsoft Passport 1.4](passport-authentication-in-winhttp.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="0a7e1-150">Negotiate</span><span class="sxs-lookup"><span data-stu-id="0a7e1-150">Negotiate</span></span>         | <span data-ttu-id="0a7e1-151">Richiesta-risposta</span><span class="sxs-lookup"><span data-stu-id="0a7e1-151">Challenge-response</span></span> | <span data-ttu-id="0a7e1-152">Se il server e il client utilizzano Windows 2000 o versione successiva, viene utilizzata l'autenticazione Kerberos.</span><span class="sxs-lookup"><span data-stu-id="0a7e1-152">If both the server and client are using Windows 2000 or later, Kerberos authentication is used.</span></span> <span data-ttu-id="0a7e1-153">In caso contrario, viene utilizzata l'autenticazione NTLM.</span><span class="sxs-lookup"><span data-stu-id="0a7e1-153">Otherwise NTLM authentication is used.</span></span> <span data-ttu-id="0a7e1-154">Kerberos è disponibile in Windows 2000 e nei sistemi operativi successivi ed è considerato più sicuro rispetto all'autenticazione NTLM.</span><span class="sxs-lookup"><span data-stu-id="0a7e1-154">Kerberos is available in Windows 2000 and later operating systems and is considered to be more secure than NTLM authentication.</span></span> <span data-ttu-id="0a7e1-155">Per il corretto funzionamento dell'autenticazione Negotiate, è necessario eseguire diversi scambi nella stessa connessione.</span><span class="sxs-lookup"><span data-stu-id="0a7e1-155">For Negotiate authentication to function correctly, several exchanges must take place on the same connection.</span></span> <span data-ttu-id="0a7e1-156">Di conseguenza, non è possibile usare l'autenticazione Negotiate se un proxy corrispondente non supporta le connessioni keep-alive.</span><span class="sxs-lookup"><span data-stu-id="0a7e1-156">Therefore, Negotiate authentication cannot be used if an intervening proxy does not support keep-alive connections.</span></span> <span data-ttu-id="0a7e1-157">L'autenticazione Negotiate ha esito negativo anche se [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) viene usato con il flag di [**\_ disabilitazione \_ Keep \_ Alive di WinHTTP**](option-flags.md) che disabilita la semantica Keep-Alive.</span><span class="sxs-lookup"><span data-stu-id="0a7e1-157">Negotiate authentication also fails if [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) is used with the [**WINHTTP\_DISABLE\_KEEP\_ALIVE**](option-flags.md) flag that disables keep-alive semantics.</span></span> <span data-ttu-id="0a7e1-158">Lo schema di autenticazione Negotiate viene talvolta definito autenticazione integrata di Windows.</span><span class="sxs-lookup"><span data-stu-id="0a7e1-158">The Negotiate authentication scheme is sometimes called Integrated Windows authentication.</span></span> |



 

## <a name="authentication-in-winhttp-applications"></a><span data-ttu-id="0a7e1-159">Autenticazione nelle applicazioni WinHTTP</span><span class="sxs-lookup"><span data-stu-id="0a7e1-159">Authentication in WinHTTP Applications</span></span>

<span data-ttu-id="0a7e1-160">Il Application Programming Interface WinHTTP (API) fornisce due funzioni usate per accedere alle risorse Internet nelle situazioni in cui è richiesta l'autenticazione: [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) e [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes).</span><span class="sxs-lookup"><span data-stu-id="0a7e1-160">The WinHTTP application programming interface (API) provides two functions used to access Internet resources in situations where authentication is required: [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) and [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes).</span></span>

<span data-ttu-id="0a7e1-161">Quando viene ricevuta una risposta con un codice di stato 401 o 407, è possibile usare [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes) per analizzare le intestazioni di autenticazione per determinare gli schemi di autenticazione supportati e la destinazione di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="0a7e1-161">When a response is received with a 401 or 407 status code, [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes) can be used to parse the authentication headers to determine the supported authentication schemes and the authentication target.</span></span> <span data-ttu-id="0a7e1-162">La destinazione di autenticazione è il server o il proxy che richiede l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="0a7e1-162">The authentication target is the server or proxy that requests authentication.</span></span> <span data-ttu-id="0a7e1-163">**WinHttpQueryAuthSchemes** determina anche il primo schema di autenticazione, dagli schemi disponibili, in base alle preferenze dello schema di autenticazione suggerite dal server.</span><span class="sxs-lookup"><span data-stu-id="0a7e1-163">**WinHttpQueryAuthSchemes** also determines the first authentication scheme, from the available schemes, based on the authentication scheme preferences suggested by the server.</span></span> <span data-ttu-id="0a7e1-164">Questo metodo per la scelta di uno schema di autenticazione è il comportamento suggerito da [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span><span class="sxs-lookup"><span data-stu-id="0a7e1-164">This method for choosing an authentication scheme is the behavior suggested by [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span></span>

<span data-ttu-id="0a7e1-165">[**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) consente a un'applicazione di specificare lo schema di autenticazione utilizzato insieme a un nome utente e una password validi per l'utilizzo nel server o nel proxy di destinazione.</span><span class="sxs-lookup"><span data-stu-id="0a7e1-165">[**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) enables an application to specify the authentication scheme that is used along with a valid username and password for use on the target server or proxy.</span></span> <span data-ttu-id="0a7e1-166">Dopo aver impostato le credenziali e inviato nuovamente la richiesta, le intestazioni necessarie vengono generate e aggiunte automaticamente alla richiesta.</span><span class="sxs-lookup"><span data-stu-id="0a7e1-166">After setting the credentials and resending the request, the necessary headers are generated and added to the request automatically.</span></span> <span data-ttu-id="0a7e1-167">Poiché alcuni schemi di autenticazione richiedono più transazioni, [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) potrebbe restituire l'errore \_ . errore WinHTTP: \_ Invia nuovamente la \_ richiesta.</span><span class="sxs-lookup"><span data-stu-id="0a7e1-167">Because some authentication schemes require multiple transactions [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) could return the error, ERROR\_WINHTTP\_RESEND\_REQUEST.</span></span> <span data-ttu-id="0a7e1-168">Quando si verifica questo errore, l'applicazione deve continuare a inviare nuovamente la richiesta fino a quando non viene ricevuta una risposta che non contiene un codice di stato 401 o 407.</span><span class="sxs-lookup"><span data-stu-id="0a7e1-168">When this error is encountered, the application should continue to resend the request until a response is received that does not contain a 401 or 407 status code.</span></span> <span data-ttu-id="0a7e1-169">Un codice di stato 200 indica che la risorsa è disponibile e che la richiesta ha avuto esito positivo.</span><span class="sxs-lookup"><span data-stu-id="0a7e1-169">A 200 status code indicates that the resource is available and the request is successful.</span></span> <span data-ttu-id="0a7e1-170">Per ulteriori codici di stato che possono essere restituiti, vedere [**codici di stato http**](http-status-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="0a7e1-170">See [**HTTP Status Codes**](http-status-codes.md) for additional status codes that can be returned.</span></span>

<span data-ttu-id="0a7e1-171">Se uno schema di autenticazione accettabile e le credenziali sono note prima dell'invio di una richiesta al server, un'applicazione può chiamare [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) prima di chiamare [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span><span class="sxs-lookup"><span data-stu-id="0a7e1-171">If an acceptable authentication scheme and credentials are known before a request is sent to the server, an application can call [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) before calling [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span> <span data-ttu-id="0a7e1-172">In questo caso, WinHTTP tenta di pre-eseguire l'autenticazione con il server fornendo le credenziali o i [*dati di autenticazione*](glossary.md) nella richiesta iniziale al server.</span><span class="sxs-lookup"><span data-stu-id="0a7e1-172">In this case, WinHTTP attempts pre-authentication with the server by providing credentials or [*authentication data*](glossary.md) in the initial request to the server.</span></span> <span data-ttu-id="0a7e1-173">La pre-autenticazione può ridurre il numero di scambi nel processo di autenticazione e quindi migliorare le prestazioni dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0a7e1-173">Pre-authentication can decrease the number of exchanges in the authentication process and therefore improve application performance.</span></span>

<span data-ttu-id="0a7e1-174">La preautenticazione può essere utilizzata con gli schemi di autenticazione seguenti:</span><span class="sxs-lookup"><span data-stu-id="0a7e1-174">Preauthentication can be used with the following authentication schemes:</span></span>

-   <span data-ttu-id="0a7e1-175">Basic: sempre possibile.</span><span class="sxs-lookup"><span data-stu-id="0a7e1-175">Basic - always possible.</span></span>
-   <span data-ttu-id="0a7e1-176">Negoziare la risoluzione in Kerberos: molto probabilmente possibile; l'unica eccezione è rappresentata dal caso in cui le sfasamento temporali siano disattivate tra il client e il controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="0a7e1-176">Negotiate resolving into Kerberos - very likely possible; the only exception is when the time-skews are off between the client and the domain controller.</span></span>
-   <span data-ttu-id="0a7e1-177">(Negoziazione della risoluzione in NTLM): mai possibile.</span><span class="sxs-lookup"><span data-stu-id="0a7e1-177">(Negotiate resolving into NTLM) - never possible.</span></span>
-   <span data-ttu-id="0a7e1-178">NTLM: possibile solo in Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="0a7e1-178">NTLM - possible in Windows Server 2008 R2 only.</span></span>
-   <span data-ttu-id="0a7e1-179">Digest: mai possibile.</span><span class="sxs-lookup"><span data-stu-id="0a7e1-179">Digest - never possible.</span></span>
-   <span data-ttu-id="0a7e1-180">Passport: mai possibile; Dopo la richiesta di risposta iniziale, WinHTTP usa i cookie per eseguire la pre-autenticazione a Passport.</span><span class="sxs-lookup"><span data-stu-id="0a7e1-180">Passport - never possible; after the initial challenge-response, WinHTTP uses cookies to pre-authenticate to Passport.</span></span>

<span data-ttu-id="0a7e1-181">Una tipica applicazione WinHTTP completa i passaggi seguenti per gestire l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="0a7e1-181">A typical WinHTTP application completes the following steps in order to handle authentication.</span></span>

-   <span data-ttu-id="0a7e1-182">Richiedere una risorsa con [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) e [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span><span class="sxs-lookup"><span data-stu-id="0a7e1-182">Request a resource with [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) and [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span>
-   <span data-ttu-id="0a7e1-183">Controllare le intestazioni della risposta con [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders).</span><span class="sxs-lookup"><span data-stu-id="0a7e1-183">Check the response headers with [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders).</span></span>
-   <span data-ttu-id="0a7e1-184">Se viene restituito un codice di stato 401 o 407 che indica che è richiesta l'autenticazione, chiamare [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes) per trovare uno schema accettabile.</span><span class="sxs-lookup"><span data-stu-id="0a7e1-184">If a 401 or 407 status code is returned indicating that authentication is required, call [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes) to find an acceptable scheme.</span></span>
-   <span data-ttu-id="0a7e1-185">Impostare lo schema di autenticazione, il nome utente e la password con [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials).</span><span class="sxs-lookup"><span data-stu-id="0a7e1-185">Set the authentication scheme, username, and password with [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials).</span></span>
-   <span data-ttu-id="0a7e1-186">Inviare di nuovo la richiesta con lo stesso handle di richiesta chiamando [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span><span class="sxs-lookup"><span data-stu-id="0a7e1-186">Resend the request with the same request handle by calling [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span>

<span data-ttu-id="0a7e1-187">Le credenziali impostate da [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) vengono usate solo per una richiesta.</span><span class="sxs-lookup"><span data-stu-id="0a7e1-187">The credentials set by [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) are only used for one request.</span></span> <span data-ttu-id="0a7e1-188">WinHTTP non memorizza nella cache le credenziali da usare in altre richieste, il che significa che le applicazioni devono essere scritte in grado di rispondere a più richieste.</span><span class="sxs-lookup"><span data-stu-id="0a7e1-188">WinHTTP does not cache the credentials to use in other requests, which means that applications must be written that can respond to multiple requests.</span></span> <span data-ttu-id="0a7e1-189">Se viene riutilizzata una connessione autenticata, altre richieste potrebbero non essere richieste, ma il codice deve essere in grado di rispondere a una richiesta in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="0a7e1-189">If an authenticated connection is re-used, other requests may not be challenged, but your code should be able to respond to a request at any time.</span></span>

### <a name="example-retrieving-a-document"></a><span data-ttu-id="0a7e1-190">Esempio: recupero di un documento</span><span class="sxs-lookup"><span data-stu-id="0a7e1-190">Example: Retrieving a Document</span></span>

<span data-ttu-id="0a7e1-191">Il codice di esempio seguente tenta di recuperare un documento specificato da un server HTTP.</span><span class="sxs-lookup"><span data-stu-id="0a7e1-191">The following sample code attempts to retrieve a specified document from an HTTP server.</span></span> <span data-ttu-id="0a7e1-192">Il codice di stato viene recuperato dalla risposta per determinare se l'autenticazione è obbligatoria.</span><span class="sxs-lookup"><span data-stu-id="0a7e1-192">The status code is retrieved from the response to determine if authentication is required.</span></span> <span data-ttu-id="0a7e1-193">Se viene trovato un codice di stato 200, il documento sarà disponibile.</span><span class="sxs-lookup"><span data-stu-id="0a7e1-193">If a 200 status code is found, the document is available.</span></span> <span data-ttu-id="0a7e1-194">Se viene trovato un codice di stato 401 o 407, è necessaria l'autenticazione prima di poter recuperare il documento.</span><span class="sxs-lookup"><span data-stu-id="0a7e1-194">If a status code of 401 or 407 is found, authentication is required before the document can be retrieved.</span></span> <span data-ttu-id="0a7e1-195">Per qualsiasi altro codice di stato, viene visualizzato un messaggio di errore.</span><span class="sxs-lookup"><span data-stu-id="0a7e1-195">For any other status code, an error message is displayed.</span></span> <span data-ttu-id="0a7e1-196">Per un elenco di possibili codici di stato, vedere [**codici di stato http**](http-status-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="0a7e1-196">See [**HTTP Status Codes**](http-status-codes.md) for a list of possible status codes.</span></span>


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



## <a name="automatic-logon-policy"></a><span data-ttu-id="0a7e1-197">Criteri di accesso automatici</span><span class="sxs-lookup"><span data-stu-id="0a7e1-197">Automatic Logon Policy</span></span>

<span data-ttu-id="0a7e1-198">Il criterio di accesso automatico (accesso automatico) determina quando è accettabile che WinHTTP includa le credenziali predefinite in una richiesta.</span><span class="sxs-lookup"><span data-stu-id="0a7e1-198">The automatic logon (auto-logon) policy determines when it is acceptable for WinHTTP to include the default credentials in a request.</span></span> <span data-ttu-id="0a7e1-199">Le credenziali predefinite sono il token del thread corrente o il token di sessione, a seconda che WinHTTP venga utilizzato in modalità sincrona o asincrona.</span><span class="sxs-lookup"><span data-stu-id="0a7e1-199">The default credentials are either the current thread token or the session token depending on whether WinHTTP is used in synchronous or asynchronous mode.</span></span> <span data-ttu-id="0a7e1-200">Il token del thread viene usato in modalità sincrona e il token di sessione viene usato in modalità asincrona.</span><span class="sxs-lookup"><span data-stu-id="0a7e1-200">The thread token is used in synchronous mode, and the session token is used in asynchronous mode.</span></span> <span data-ttu-id="0a7e1-201">Queste credenziali predefinite sono spesso il nome utente e la password utilizzati per accedere a Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="0a7e1-201">These default credentials are often the username and password used to log on to Microsoft Windows.</span></span>

<span data-ttu-id="0a7e1-202">Il criterio di accesso automatico è stato implementato per impedire che queste credenziali vengano usate in modo casuale per l'autenticazione in un server non attendibile.</span><span class="sxs-lookup"><span data-stu-id="0a7e1-202">The auto-logon policy was implemented to prevent these credentials from being casually used to authenticate against an untrusted server.</span></span> <span data-ttu-id="0a7e1-203">Per impostazione predefinita, il livello di sicurezza è impostato su WINHTTP \_ AUTOlogod \_ Security \_ level \_ media, che consente di utilizzare le credenziali predefinite solo per le richieste Intranet.</span><span class="sxs-lookup"><span data-stu-id="0a7e1-203">By default, the security level is set to WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_MEDIUM, which allows the default credentials to be used only for Intranet requests.</span></span> <span data-ttu-id="0a7e1-204">Il criterio di accesso automatico si applica solo agli schemi di autenticazione NTLM e Negotiate.</span><span class="sxs-lookup"><span data-stu-id="0a7e1-204">The auto-logon policy only applies to the NTLM and Negotiate authentication schemes.</span></span> <span data-ttu-id="0a7e1-205">Le credenziali non vengono mai trasmesse automaticamente con altri schemi.</span><span class="sxs-lookup"><span data-stu-id="0a7e1-205">Credentials are never automatically transmitted with other schemes.</span></span>

<span data-ttu-id="0a7e1-206">È possibile impostare i criteri di accesso automatico usando la funzione [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) con il flag di [**\_ \_ \_ criteri AutoLogon dell'opzione WinHTTP**](option-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="0a7e1-206">The auto-logon policy can be set using the [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) function with the [**WINHTTP\_OPTION\_AUTOLOGON\_POLICY**](option-flags.md) flag.</span></span> <span data-ttu-id="0a7e1-207">Questo flag si applica solo all'handle della richiesta.</span><span class="sxs-lookup"><span data-stu-id="0a7e1-207">This flag applies only to the request handle.</span></span> <span data-ttu-id="0a7e1-208">Quando il criterio è impostato sul livello di sicurezza con accesso \_ automatico WinHTTP \_ \_ \_ basso, le credenziali predefinite possono essere inviate a tutti i server.</span><span class="sxs-lookup"><span data-stu-id="0a7e1-208">When the policy is set to WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_LOW, default credentials can be sent to all servers.</span></span> <span data-ttu-id="0a7e1-209">Quando il criterio è impostato sul \_ livello di sicurezza automatico WinHTTP- \_ \_ \_ alto, le credenziali predefinite non possono essere usate per l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="0a7e1-209">When the policy is set to WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_HIGH, default credentials cannot be used for authentication.</span></span> <span data-ttu-id="0a7e1-210">Si consiglia vivamente di utilizzare l'accesso automatico a livello medio.</span><span class="sxs-lookup"><span data-stu-id="0a7e1-210">It is strongly recommended that you use the auto-logon at the MEDIUM level.</span></span>

## <a name="stored-user-names-and-passwords"></a><span data-ttu-id="0a7e1-211">Gestione nomi utente e password archiviati</span><span class="sxs-lookup"><span data-stu-id="0a7e1-211">Stored User Names and Passwords</span></span>

<span data-ttu-id="0a7e1-212">In Windows XP è stato introdotto il concetto di nomi utente e password archiviati.</span><span class="sxs-lookup"><span data-stu-id="0a7e1-212">Windows XP introduced the concept of Stored User Names and Passwords.</span></span> <span data-ttu-id="0a7e1-213">Se le credenziali Passport di un utente vengono salvate tramite la **registrazione guidata Passport** o la **finestra di dialogo credenziali** standard, vengono salvate in nomi utente e password archiviati.</span><span class="sxs-lookup"><span data-stu-id="0a7e1-213">If a user's Passport credentials are saved through the **Passport Registration Wizard** or the standard **Credential Dialog**, it is saved in the Stored User Names and Passwords.</span></span> <span data-ttu-id="0a7e1-214">Quando si usa WinHTTP in Windows XP o versioni successive, WinHTTP usa automaticamente le credenziali nei nomi utente e nelle password archiviati se le credenziali non sono impostate in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="0a7e1-214">When using WinHTTP on Windows XP or later, WinHTTP automatically uses the credentials in the Stored User Names and Passwords if credentials are not explicitly set.</span></span> <span data-ttu-id="0a7e1-215">Questa operazione è simile a quella del supporto per le credenziali di accesso predefinite per NTLM/Kerberos.</span><span class="sxs-lookup"><span data-stu-id="0a7e1-215">This is similar to the support of default logon credentials for NTLM/Kerberos.</span></span> <span data-ttu-id="0a7e1-216">Tuttavia, l'utilizzo delle credenziali Passport predefinite non è soggetto alle impostazioni dei criteri di accesso automatico.</span><span class="sxs-lookup"><span data-stu-id="0a7e1-216">However, use of default Passport credentials is not subject to the automatic logon policy settings.</span></span>

 

 



