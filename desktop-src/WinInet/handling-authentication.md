---
title: Gestione dell'autenticazione
description: Alcuni proxy e server richiedono l'autenticazione prima di concedere l'accesso alle risorse su Internet.
ms.assetid: f3752031-30d3-4e35-8eae-1d4971b66bc2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e82d8cd93f1010c71560d856793ad06d8bc5d9d5
ms.sourcegitcommit: 59ec383331366f8a62c94bb88468ca03e95c43f8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/13/2021
ms.locfileid: "107380855"
---
# <a name="handling-authentication"></a><span data-ttu-id="8b16b-103">Gestione dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="8b16b-103">Handling Authentication</span></span>

<span data-ttu-id="8b16b-104">Alcuni proxy e server richiedono l'autenticazione prima di concedere l'accesso alle risorse su Internet.</span><span class="sxs-lookup"><span data-stu-id="8b16b-104">Some proxies and servers require authentication before granting access to resources on the Internet.</span></span> <span data-ttu-id="8b16b-105">Le funzioni WinINet supportano l'autenticazione server e proxy per le sessioni HTTP.</span><span class="sxs-lookup"><span data-stu-id="8b16b-105">The WinINet functions support server and proxy authentication for http sessions.</span></span> <span data-ttu-id="8b16b-106">L'autenticazione dei server ftp deve essere gestita dalla [**funzione InternetConnect.**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)</span><span class="sxs-lookup"><span data-stu-id="8b16b-106">Authentication of ftp servers must be handled by the [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) function.</span></span> <span data-ttu-id="8b16b-107">Attualmente l'autenticazione del gateway FTP non è supportata.</span><span class="sxs-lookup"><span data-stu-id="8b16b-107">Currently, FTP gateway authentication is not supported.</span></span>

## <a name="about-http-authentication"></a><span data-ttu-id="8b16b-108">Informazioni sull'autenticazione HTTP</span><span class="sxs-lookup"><span data-stu-id="8b16b-108">About HTTP Authentication</span></span>

<span data-ttu-id="8b16b-109">Se è necessaria l'autenticazione, l'applicazione client riceve un codice di stato 401, se il server richiede l'autenticazione o 407, se il proxy richiede l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="8b16b-109">If authentication is required, the client application receives a status code 401, if the server requires authentication, or 407, if the proxy requires authentication.</span></span> <span data-ttu-id="8b16b-110">Con il codice di stato, il proxy o il server invia una o più intestazioni di risposta di autenticazione: Proxy-Authenticate (per l'autenticazione proxy) o WWW-Authenticate (per l'autenticazione del server).</span><span class="sxs-lookup"><span data-stu-id="8b16b-110">With the status code, the proxy or server sends one, or more, authenticate response headers—Proxy-Authenticate (for proxy authentication) or WWW-Authenticate (for server authentication).</span></span>

<span data-ttu-id="8b16b-111">Ogni intestazione di risposta di autenticazione contiene uno schema di autenticazione disponibile e un'area di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="8b16b-111">Each authenticate response header contains an available authentication scheme and a realm.</span></span> <span data-ttu-id="8b16b-112">Se sono supportati più schemi di autenticazione, il server restituisce più intestazioni di risposta di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="8b16b-112">If multiple authentication schemes are supported, the server returns multiple authenticate response headers.</span></span> <span data-ttu-id="8b16b-113">Il valore dell'area di autenticazione fa distinzione tra maiuscole e minuscole e definisce uno spazio di protezione nel proxy o nel server.</span><span class="sxs-lookup"><span data-stu-id="8b16b-113">The realm value is case-sensitive and defines a protection space on the proxy or server.</span></span> <span data-ttu-id="8b16b-114">Ad esempio, l'intestazione "WWW-Authenticate: Basic Realm="example"" è un esempio di intestazione restituita quando è necessaria l'autenticazione del server.</span><span class="sxs-lookup"><span data-stu-id="8b16b-114">For example, the header "WWW-Authenticate: Basic Realm="example"" would be an example of a header returned when server authentication is required.</span></span>

<span data-ttu-id="8b16b-115">L'applicazione client che ha inviato la richiesta può autenticarsi includendo un campo di intestazione Authorization con la richiesta.</span><span class="sxs-lookup"><span data-stu-id="8b16b-115">The client application that sent the request can authenticate itself by including an Authorization header field with the request.</span></span> <span data-ttu-id="8b16b-116">L'intestazione Authorization conterrà lo schema di autenticazione e la risposta appropriata richiesta da tale schema.</span><span class="sxs-lookup"><span data-stu-id="8b16b-116">The Authorization header would contain the authentication scheme and the appropriate response required by that scheme.</span></span> <span data-ttu-id="8b16b-117">Ad esempio, l'intestazione "Authorization: Basic" verrà aggiunta alla richiesta e inviata nuovamente al server se il client ha ricevuto l'intestazione di risposta di autenticazione \<username:password> "WWW-Authenticate: Basic Realm="example"".</span><span class="sxs-lookup"><span data-stu-id="8b16b-117">For example, the header "Authorization: Basic \<username:password>" would be added to the request and re-sent to the server if the client received the authenticate response header "WWW-Authenticate: Basic Realm="example"".</span></span>

<span data-ttu-id="8b16b-118">Esistono due tipi generali di schemi di autenticazione:</span><span class="sxs-lookup"><span data-stu-id="8b16b-118">There are two general types of authentication schemes:</span></span>

-   <span data-ttu-id="8b16b-119">Schema di autenticazione di base, in cui il nome utente e la password vengono inviati in testo non crittografato al server.</span><span class="sxs-lookup"><span data-stu-id="8b16b-119">Basic authentication scheme, where the user name and password are sent in cleartext to the server.</span></span>
-   <span data-ttu-id="8b16b-120">Schemi challenge-response, che consentono un formato challenge-response.</span><span class="sxs-lookup"><span data-stu-id="8b16b-120">Challenge-response schemes, which allow for a challenge-response format.</span></span>

<span data-ttu-id="8b16b-121">Lo schema di autenticazione di base è basato sul modello che un client deve autenticare con un nome utente e una password per ogni area di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="8b16b-121">The Basic authentication scheme is based on the model that a client must authenticate itself with a user name and password for each realm.</span></span> <span data-ttu-id="8b16b-122">Il server invia nuovamente la richiesta con un'intestazione Authorization che include un nome utente e una password validi.</span><span class="sxs-lookup"><span data-stu-id="8b16b-122">The server services the request if it is resent with an Authorization header that includes a valid user name and password.</span></span>

<span data-ttu-id="8b16b-123">Gli schemi challenge-response consentono un'autenticazione più sicura.</span><span class="sxs-lookup"><span data-stu-id="8b16b-123">Challenge-response schemes enable more secure authentication.</span></span> <span data-ttu-id="8b16b-124">Se una richiesta richiede l'autenticazione usando uno schema challenge-response, al client vengono restituiti il codice di stato appropriato e le intestazioni Authenticate.</span><span class="sxs-lookup"><span data-stu-id="8b16b-124">If a request requires authentication using a challenge-response scheme, the appropriate status code and Authenticate headers are returned to the client.</span></span> <span data-ttu-id="8b16b-125">Il client deve quindi inviare nuovamente la richiesta con una negoziazione.</span><span class="sxs-lookup"><span data-stu-id="8b16b-125">The client must then to resend the request with a negotiate.</span></span> <span data-ttu-id="8b16b-126">Il server restituirebbe un codice di stato appropriato con una richiesta di verifica e il client richiederebbe quindi di inviare nuovamente la richiesta con la risposta appropriata per ottenere il servizio richiesto.</span><span class="sxs-lookup"><span data-stu-id="8b16b-126">The server would return an appropriate status code with a challenge, and the client would then require to resend the request with the proper response to get the requested service.</span></span>

<span data-ttu-id="8b16b-127">Nella tabella seguente sono elencati gli schemi di autenticazione, il tipo di autenticazione, la DLL che li supporta e una descrizione dello schema.</span><span class="sxs-lookup"><span data-stu-id="8b16b-127">The following table lists authentication schemes, the authentication type, the DLL that supports them, and a description of the scheme.</span></span>



| <span data-ttu-id="8b16b-128">Schema</span><span class="sxs-lookup"><span data-stu-id="8b16b-128">Scheme</span></span>                                    | <span data-ttu-id="8b16b-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="8b16b-129">Type</span></span>               | <span data-ttu-id="8b16b-130">DLL</span><span class="sxs-lookup"><span data-stu-id="8b16b-130">DLL</span></span>                  | <span data-ttu-id="8b16b-131">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8b16b-131">Description</span></span>                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------------|--------------------|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b16b-132">Base (testo non crittografato)</span><span class="sxs-lookup"><span data-stu-id="8b16b-132">Basic (cleartext)</span></span>                         | <span data-ttu-id="8b16b-133">basic</span><span class="sxs-lookup"><span data-stu-id="8b16b-133">basic</span></span>              | <span data-ttu-id="8b16b-134">Wininet.dll</span><span class="sxs-lookup"><span data-stu-id="8b16b-134">Wininet.dll</span></span>          | <span data-ttu-id="8b16b-135">Usa una stringa con codifica Base64 che contiene il nome utente e la password.</span><span class="sxs-lookup"><span data-stu-id="8b16b-135">Uses a base64 encoded string that contains the user name and password.</span></span>                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="8b16b-136">Digest</span><span class="sxs-lookup"><span data-stu-id="8b16b-136">Digest</span></span>                                    | <span data-ttu-id="8b16b-137">challenge-response</span><span class="sxs-lookup"><span data-stu-id="8b16b-137">challenge-response</span></span> | <span data-ttu-id="8b16b-138">Digest.dll</span><span class="sxs-lookup"><span data-stu-id="8b16b-138">Digest.dll</span></span>           | <span data-ttu-id="8b16b-139">Schema challenge-response che sfida l'uso di un valore nonce (una stringa di dati specificata dal server).</span><span class="sxs-lookup"><span data-stu-id="8b16b-139">A challenge-response scheme that challenges using a nonce (a server-specified data string) value.</span></span> <span data-ttu-id="8b16b-140">Una risposta valida contiene un checksum del nome utente, della password, del valore nonce specificato, del metodo HTTP e dell'URI Uniform Resource Identifier richiesta.</span><span class="sxs-lookup"><span data-stu-id="8b16b-140">A valid response contains a checksum of the user name, the password, the given nonce value, the HTTP method, and the requested Uniform Resource Identifier (URI).</span></span> <span data-ttu-id="8b16b-141">Il supporto per l'autenticazione del digest è stato introdotto in Microsoft Internet Explorer 5.</span><span class="sxs-lookup"><span data-stu-id="8b16b-141">Digest authentication support was introduced in Microsoft Internet Explorer 5.</span></span> |
| <span data-ttu-id="8b16b-142">NT LAN Manager (NTLM)</span><span class="sxs-lookup"><span data-stu-id="8b16b-142">NT LAN Manager (NTLM)</span></span>                     | <span data-ttu-id="8b16b-143">challenge-response</span><span class="sxs-lookup"><span data-stu-id="8b16b-143">challenge-response</span></span> | <span data-ttu-id="8b16b-144">Winsspi.dll</span><span class="sxs-lookup"><span data-stu-id="8b16b-144">Winsspi.dll</span></span>          | <span data-ttu-id="8b16b-145">Schema challenge-response che basa la richiesta sul nome utente.</span><span class="sxs-lookup"><span data-stu-id="8b16b-145">A challenge-response scheme that bases the challenge on the user name.</span></span>                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="8b16b-146">Microsoft Network (MSN)</span><span class="sxs-lookup"><span data-stu-id="8b16b-146">Microsoft Network (MSN)</span></span>                   | <span data-ttu-id="8b16b-147">challenge-response</span><span class="sxs-lookup"><span data-stu-id="8b16b-147">challenge-response</span></span> | <span data-ttu-id="8b16b-148">Msnsspc.dll</span><span class="sxs-lookup"><span data-stu-id="8b16b-148">Msnsspc.dll</span></span>          | <span data-ttu-id="8b16b-149">The Microsoft Network di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="8b16b-149">The Microsoft Network's authentication scheme.</span></span>                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="8b16b-150">Distributed Password Authentication (DPA)</span><span class="sxs-lookup"><span data-stu-id="8b16b-150">Distributed Password Authentication (DPA)</span></span> | <span data-ttu-id="8b16b-151">challenge-response</span><span class="sxs-lookup"><span data-stu-id="8b16b-151">challenge-response</span></span> | <span data-ttu-id="8b16b-152">Msapsspc.dll</span><span class="sxs-lookup"><span data-stu-id="8b16b-152">Msapsspc.dll</span></span>         | <span data-ttu-id="8b16b-153">Analogamente all'autenticazione MSN, viene usato anche da Microsoft Network.</span><span class="sxs-lookup"><span data-stu-id="8b16b-153">Similar to MSN authentication and is also used by the Microsoft Network.</span></span>                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="8b16b-154">Autenticazione della passphrase remota (RPA)</span><span class="sxs-lookup"><span data-stu-id="8b16b-154">Remote Passphrase Authentication (RPA)</span></span>    | <span data-ttu-id="8b16b-155">Compuserve</span><span class="sxs-lookup"><span data-stu-id="8b16b-155">CompuServe</span></span>         | <span data-ttu-id="8b16b-156">Rpawinet.dll, da.dll</span><span class="sxs-lookup"><span data-stu-id="8b16b-156">Rpawinet.dll, da.dll</span></span> | <span data-ttu-id="8b16b-157">Schema di autenticazione CompuServe.</span><span class="sxs-lookup"><span data-stu-id="8b16b-157">CompuServe authentication scheme.</span></span> <span data-ttu-id="8b16b-158">Per altre informazioni, vedere Specifiche [del meccanismo RPA.](https://www.compuserve.com/)</span><span class="sxs-lookup"><span data-stu-id="8b16b-158">For more information, see the [RPA Mechanism Specifications](https://www.compuserve.com/).</span></span>                                                                                                                                                                                                    |



 

<span data-ttu-id="8b16b-159">Per qualsiasi elemento diverso dall'autenticazione di base, le chiavi del Registro di sistema devono essere impostate oltre all'installazione della DLL appropriata.</span><span class="sxs-lookup"><span data-stu-id="8b16b-159">For anything other than Basic authentication, the registry keys must be set up in addition to installing the appropriate DLL.</span></span>

<span data-ttu-id="8b16b-160">Se è necessaria l'autenticazione, nella chiamata a [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)deve essere usato il flag [ \_ KEEP \_ \_ CONNECTION](api-flags.md) di INTERNET FLAG .</span><span class="sxs-lookup"><span data-stu-id="8b16b-160">If authentication is required, the [INTERNET\_FLAG\_KEEP\_CONNECTION](api-flags.md) flag should be used in the call to [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span> <span data-ttu-id="8b16b-161">Il flag INTERNET FLAG KEEP CONNECTION è necessario per NTLM e altri tipi di autenticazione per mantenere la connessione durante \_ il completamento del processo di \_ \_ autenticazione.</span><span class="sxs-lookup"><span data-stu-id="8b16b-161">The INTERNET\_FLAG\_KEEP\_CONNECTION flag is required for NTLM and other types of authentication in order to maintain the connection while completing the authentication process.</span></span> <span data-ttu-id="8b16b-162">Se la connessione non viene mantenuta, il processo di autenticazione deve essere riavviato con il proxy o il server.</span><span class="sxs-lookup"><span data-stu-id="8b16b-162">If the connection is not maintained, the authentication process must be restarted with the proxy or server.</span></span>

<span data-ttu-id="8b16b-163">Le [**funzioni InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) [**e HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) vengono completate correttamente anche quando è necessaria l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="8b16b-163">The [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) and [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) functions complete successfully even when authentication is required.</span></span> <span data-ttu-id="8b16b-164">La differenza è che i dati restituiti nei file di intestazione e [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) riceveranno una pagina HTML che informa l'utente del codice di stato.</span><span class="sxs-lookup"><span data-stu-id="8b16b-164">The difference is, the data returned in the header files and [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) would receive an HTML page informing the user of the status code.</span></span>

### <a name="registering-authentication-keys"></a><span data-ttu-id="8b16b-165">Registrazione delle chiavi di autenticazione</span><span class="sxs-lookup"><span data-stu-id="8b16b-165">Registering Authentication Keys</span></span>

<span data-ttu-id="8b16b-166">INTERNET OPEN TYPE PRECONFIG esamina i valori del Registro \_ \_ di sistema \_ **ProxyEnable,** **ProxyServer** e **ProxyOverride.**</span><span class="sxs-lookup"><span data-stu-id="8b16b-166">INTERNET\_OPEN\_TYPE\_PRECONFIG looks at the registry values **ProxyEnable**, **ProxyServer**, and **ProxyOverride**.</span></span> <span data-ttu-id="8b16b-167">Questi valori si trovano in **HKEY \_ CURRENT \_ USER** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** Internet \\ **Settings**.</span><span class="sxs-lookup"><span data-stu-id="8b16b-167">These values are located under **HKEY\_CURRENT\_USER**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Internet Settings**.</span></span>

<span data-ttu-id="8b16b-168">Per gli schemi di autenticazione diversi da Basic, è necessario aggiungere una chiave al Registro di sistema in **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Internet Explorer** \\ **Security**.</span><span class="sxs-lookup"><span data-stu-id="8b16b-168">For authentication schemes other than Basic, a key must be added to the registry under **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Internet Explorer**\\**Security**.</span></span> <span data-ttu-id="8b16b-169">Un **valore DWORD,** **Flags,** deve essere impostato con il valore appropriato.</span><span class="sxs-lookup"><span data-stu-id="8b16b-169">A **DWORD** value, **Flags**, should be set with the appropriate value.</span></span> <span data-ttu-id="8b16b-170">L'elenco seguente mostra i valori possibili per il **valore Flags.**</span><span class="sxs-lookup"><span data-stu-id="8b16b-170">The following list shows the possible values for the **Flags** value.</span></span>

-   <span data-ttu-id="8b16b-171">PLUGIN \_ AUTH \_ FLAGS UNIQUE CONTEXT PER \_ \_ \_ \_ TCPIP (value=0x01)</span><span class="sxs-lookup"><span data-stu-id="8b16b-171">PLUGIN\_AUTH\_FLAGS\_UNIQUE\_CONTEXT\_PER\_TCPIP (value=0x01)</span></span>

    <span data-ttu-id="8b16b-172">Ogni Transmission Control Protocol/Internet Protocol (TCP/IP) contiene un contesto diverso.</span><span class="sxs-lookup"><span data-stu-id="8b16b-172">Each Transmission Control Protocol/Internet Protocol (TCP/IP) socket contains a different context.</span></span> <span data-ttu-id="8b16b-173">In caso contrario, viene passato un nuovo contesto per ogni area di autenticazione o modello di URL di blocco.</span><span class="sxs-lookup"><span data-stu-id="8b16b-173">Otherwise, a new context is passed for each realm or block URL template.</span></span>

-   <span data-ttu-id="8b16b-174">I \_ FLAG DI AUTENTICAZIONE DEL \_ \_ PLUG-IN \_ POSSONO GESTIRE \_ L'INTERFACCIA UTENTE (value=0x02)</span><span class="sxs-lookup"><span data-stu-id="8b16b-174">PLUGIN\_AUTH\_FLAGS\_CAN\_HANDLE\_UI (value=0x02)</span></span>

    <span data-ttu-id="8b16b-175">Questa DLL può gestire il proprio input utente.</span><span class="sxs-lookup"><span data-stu-id="8b16b-175">This DLL can handle its own user input.</span></span>

-   <span data-ttu-id="8b16b-176">I \_ FLAG DI AUTENTICAZIONE DEL \_ \_ PLUG-IN POSSONO GESTIRE NESSUN \_ \_ \_ PASSWD (value=0x04)</span><span class="sxs-lookup"><span data-stu-id="8b16b-176">PLUGIN\_AUTH\_FLAGS\_CAN\_HANDLE\_NO\_PASSWD (value=0x04)</span></span>

    <span data-ttu-id="8b16b-177">Questa DLL potrebbe essere in grado di eseguire un'autenticazione senza richiedere all'utente una password.</span><span class="sxs-lookup"><span data-stu-id="8b16b-177">This DLL might be capable of doing an authentication without prompting the user for a password.</span></span>

-   <span data-ttu-id="8b16b-178">PLUGIN \_ AUTH \_ FLAGS NO REALM \_ \_ (value=0x08)</span><span class="sxs-lookup"><span data-stu-id="8b16b-178">PLUGIN\_AUTH\_FLAGS\_NO\_REALM (value=0x08)</span></span>

    <span data-ttu-id="8b16b-179">Questa DLL non usa una stringa dell'area di autenticazione HTTP standard.</span><span class="sxs-lookup"><span data-stu-id="8b16b-179">This DLL does not use a standard http realm string.</span></span> <span data-ttu-id="8b16b-180">Tutti i dati che sembra essere un'area di autenticazione sono dati specifici dello schema.</span><span class="sxs-lookup"><span data-stu-id="8b16b-180">Any data that appears to be a realm is scheme-specific data.</span></span>

-   <span data-ttu-id="8b16b-181">I \_ FLAG DI AUTENTICAZIONE DEL \_ \_ \_ PLUG-IN \_ KEEP-ALIVE NON SONO OBBLIGATORI \_ (value=0x10)</span><span class="sxs-lookup"><span data-stu-id="8b16b-181">PLUGIN\_AUTH\_FLAGS\_KEEP\_ALIVE\_NOT\_REQUIRED (value=0x10)</span></span>

    <span data-ttu-id="8b16b-182">Questa DLL non richiede una connessione permanente per la sequenza challenge-response.</span><span class="sxs-lookup"><span data-stu-id="8b16b-182">This DLL does not require a persistent connection for its challenge-response sequence.</span></span>

<span data-ttu-id="8b16b-183">Ad esempio, per aggiungere l'autenticazione NTLM, la chiave NTLM deve essere aggiunta a **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Internet Explorer** \\ **Security**.</span><span class="sxs-lookup"><span data-stu-id="8b16b-183">For example, to add NTLM authentication, the key NTLM must be added to **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Internet Explorer**\\**Security**.</span></span> <span data-ttu-id="8b16b-184">In **HKEY \_ LOCAL \_ MACHINE** SOFTWARE Microsoft Internet Explorer Security NTLM è necessario aggiungere il valore stringa DLLFile e un \\  \\  \\  \\  \\  **valore DWORD,** **Flags.** </span><span class="sxs-lookup"><span data-stu-id="8b16b-184">Under **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Internet Explorer**\\**Security**\\**NTLM**, the string value, **DLLFile**, and a **DWORD** value, **Flags**, must be added.</span></span> <span data-ttu-id="8b16b-185">**DLLFile** deve essere impostato su Winsspi.dll **e Flags** deve essere impostato su 0x08.</span><span class="sxs-lookup"><span data-stu-id="8b16b-185">**DLLFile** must be set to Winsspi.dll, and **Flags** must be set to 0x08.</span></span>

### <a name="server-authentication"></a><span data-ttu-id="8b16b-186">Autenticazione del server</span><span class="sxs-lookup"><span data-stu-id="8b16b-186">Server Authentication</span></span>

<span data-ttu-id="8b16b-187">Quando un server riceve una richiesta che richiede l'autenticazione, il server restituisce un messaggio di codice di stato 401.</span><span class="sxs-lookup"><span data-stu-id="8b16b-187">When a server receives a request that requires authentication, the server returns a 401 status code message.</span></span> <span data-ttu-id="8b16b-188">In tale messaggio, il server deve includere una o più intestazioni WWW-Authenticate risposta.</span><span class="sxs-lookup"><span data-stu-id="8b16b-188">In that message, the server should include one or more WWW-Authenticate response headers.</span></span> <span data-ttu-id="8b16b-189">Queste intestazioni includono i metodi di autenticazione disponibili per il server.</span><span class="sxs-lookup"><span data-stu-id="8b16b-189">These headers include the authentication methods the server has available.</span></span> <span data-ttu-id="8b16b-190">WinINet sceglie il primo metodo che riconosce.</span><span class="sxs-lookup"><span data-stu-id="8b16b-190">WinINet chooses the first method it recognizes.</span></span>

<span data-ttu-id="8b16b-191">L'autenticazione di base offre una sicurezza debole a meno che il canale non sia prima crittografato con SSL o PCT.</span><span class="sxs-lookup"><span data-stu-id="8b16b-191">Basic authentication provides weak security unless the channel is first link-encrypted with SSL or PCT.</span></span>

<span data-ttu-id="8b16b-192">La [**funzione InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) può essere usata per ottenere i dati del nome utente e della password dall'utente oppure un'interfaccia utente personalizzata può essere progettata per ottenere i dati.</span><span class="sxs-lookup"><span data-stu-id="8b16b-192">The [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) function can be used to obtain the user name and password data from the user, or a customized user interface can be designed to obtain the data.</span></span>

<span data-ttu-id="8b16b-193">Un'interfaccia personalizzata può usare la [**funzione InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) per impostare i valori [INTERNET OPTION \_ \_ PASSWORD](option-flags.md) e [INTERNET OPTION \_ \_ USERNAME](option-flags.md) e quindi inviare nuovamente la richiesta al server.</span><span class="sxs-lookup"><span data-stu-id="8b16b-193">A custom interface can use the [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) function to set the [INTERNET\_OPTION\_PASSWORD](option-flags.md) and [INTERNET\_OPTION\_USERNAME](option-flags.md) values and then resend the request to the server.</span></span>

### <a name="proxy-authentication"></a><span data-ttu-id="8b16b-194">Autenticazione proxy</span><span class="sxs-lookup"><span data-stu-id="8b16b-194">Proxy Authentication</span></span>

<span data-ttu-id="8b16b-195">Quando un client tenta di usare un proxy che richiede l'autenticazione, il proxy restituisce un messaggio di codice di stato 407 al client.</span><span class="sxs-lookup"><span data-stu-id="8b16b-195">When a client attempts to use a proxy that requires authentication, the proxy returns a 407 status code message to the client.</span></span> <span data-ttu-id="8b16b-196">In questo messaggio, il proxy deve includere una o più intestazioni Proxy-Authenticate risposta.</span><span class="sxs-lookup"><span data-stu-id="8b16b-196">In that message, the proxy should include one or more Proxy-Authenticate response headers.</span></span> <span data-ttu-id="8b16b-197">Queste intestazioni includono i metodi di autenticazione disponibili dal proxy.</span><span class="sxs-lookup"><span data-stu-id="8b16b-197">These headers include the authentication methods available from the proxy.</span></span> <span data-ttu-id="8b16b-198">WinINet sceglie il primo metodo che riconosce.</span><span class="sxs-lookup"><span data-stu-id="8b16b-198">WinINet chooses the first method it recognizes.</span></span>

<span data-ttu-id="8b16b-199">La [**funzione InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) può essere usata per ottenere i dati relativi a nome utente e password dall'utente oppure è possibile creare un'interfaccia utente personalizzata.</span><span class="sxs-lookup"><span data-stu-id="8b16b-199">The [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) function can be used to obtain the user name and password data from the user, or a customized user interface can be designed.</span></span>

<span data-ttu-id="8b16b-200">Un'interfaccia personalizzata può usare la [**funzione InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) per impostare i valori [INTERNET OPTION PROXY \_ \_ \_ PASSWORD](option-flags.md) e [INTERNET OPTION PROXY \_ \_ \_ USERNAME](option-flags.md) e quindi inviare nuovamente la richiesta al proxy.</span><span class="sxs-lookup"><span data-stu-id="8b16b-200">A custom interface can use the [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) function to set the [INTERNET\_OPTION\_PROXY\_PASSWORD](option-flags.md) and [INTERNET\_OPTION\_PROXY\_USERNAME](option-flags.md) values and then resend the request to the proxy.</span></span>

<span data-ttu-id="8b16b-201">Se non sono impostati nome utente e password del proxy, WinINet tenta di usare il nome utente e la password per il server.</span><span class="sxs-lookup"><span data-stu-id="8b16b-201">If no proxy user name and password are set, WinINet attempts to use the user name and password for the server.</span></span> <span data-ttu-id="8b16b-202">Questo comportamento consente ai client di implementare la stessa interfaccia utente personalizzata usata per gestire l'autenticazione del server.</span><span class="sxs-lookup"><span data-stu-id="8b16b-202">This behavior enables clients to implement the same customized user interface used to handle server authentication.</span></span>

## <a name="handling-http-authentication"></a><span data-ttu-id="8b16b-203">Gestione dell'autenticazione HTTP</span><span class="sxs-lookup"><span data-stu-id="8b16b-203">Handling HTTP Authentication</span></span>

<span data-ttu-id="8b16b-204">L'autenticazione HTTP può essere gestita con [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) o con una funzione personalizzata che usa [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) o aggiunge le proprie intestazioni di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="8b16b-204">HTTP authentication can be handled with either [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) or a customized function that uses [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) or adds its own authentication headers.</span></span> <span data-ttu-id="8b16b-205">[**InternetErrorDlg può**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) esaminare le intestazioni associate a un handle [**HINTERNET**](appendix-a-hinternet-handles.md) per trovare gli errori nascosti, ad esempio i codici di stato da un proxy o un server.</span><span class="sxs-lookup"><span data-stu-id="8b16b-205">[**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) can examine the headers associated with an [**HINTERNET**](appendix-a-hinternet-handles.md) handle to find hidden errors, such as status codes from a proxy or server.</span></span> <span data-ttu-id="8b16b-206">[**InternetSetOption può**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) essere usato per impostare il nome utente e la password per il proxy e il server.</span><span class="sxs-lookup"><span data-stu-id="8b16b-206">[**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) can be used to set the user name and password for the proxy and server.</span></span> <span data-ttu-id="8b16b-207">Per l'autenticazione MSN e DPA, è necessario usare [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) per impostare il nome utente e la password.</span><span class="sxs-lookup"><span data-stu-id="8b16b-207">For MSN and DPA authentication, [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) must be used to set the user name and password.</span></span>

<span data-ttu-id="8b16b-208">Per qualsiasi funzione personalizzata che aggiunge intestazioni WWW-Authenticate o Proxy-Authenticate, il flag [INTERNET \_ FLAG NO \_ \_ AUTH](api-flags.md) deve essere impostato per disabilitare l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="8b16b-208">For any customized function that adds its own WWW-Authenticate or Proxy-Authenticate headers, the [INTERNET\_FLAG\_NO\_AUTH](api-flags.md) flag should be set to disable authentication.</span></span>

<span data-ttu-id="8b16b-209">L'esempio seguente illustra come [**usare InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) per gestire l'autenticazione HTTP.</span><span class="sxs-lookup"><span data-stu-id="8b16b-209">The following example shows how [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) can be used to handle HTTP authentication.</span></span>


```C++
HINTERNET hOpenHandle,  hConnectHandle, hResourceHandle;
DWORD dwError, dwErrorCode;
HWND hwnd = GetConsoleWindow();

hOpenHandle = InternetOpen(TEXT("Example"),
                           INTERNET_OPEN_TYPE_PRECONFIG, 
                           NULL, NULL, 0);

hConnectHandle = InternetConnect(hOpenHandle,
                                 TEXT("www.server.com"), 
                                 INTERNET_INVALID_PORT_NUMBER,
                                 NULL,
                                 NULL, 
                                 INTERNET_SERVICE_HTTP,
                                 0,0);

hResourceHandle = HttpOpenRequest(hConnectHandle, TEXT("GET"),
                                  TEXT("/premium/default.htm"),
                                  NULL, NULL, NULL, 
                                  INTERNET_FLAG_KEEP_CONNECTION, 0);

resend:

HttpSendRequest(hResourceHandle, NULL, 0, NULL, 0);

// dwErrorCode stores the error code associated with the call to
// HttpSendRequest.  

dwErrorCode = hResourceHandle ? ERROR_SUCCESS : GetLastError();

dwError = InternetErrorDlg(hwnd, hResourceHandle, dwErrorCode, 
                           FLAGS_ERROR_UI_FILTER_FOR_ERRORS | 
                           FLAGS_ERROR_UI_FLAGS_CHANGE_OPTIONS |
                           FLAGS_ERROR_UI_FLAGS_GENERATE_DATA,
                           NULL);

if (dwError == ERROR_INTERNET_FORCE_RETRY)
    goto resend;

// Insert code to read the data from the hResourceHandle
// at this point.

```



<span data-ttu-id="8b16b-210">Nell'esempio dwErrorCode viene usato per archiviare eventuali errori associati alla chiamata a [**HttpSendRequest.**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)</span><span class="sxs-lookup"><span data-stu-id="8b16b-210">In the example, dwErrorCode is used to store any errors associated with the call to [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span></span> <span data-ttu-id="8b16b-211">[**HttpSendRequest viene**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) completato correttamente, anche se il proxy o il server richiede l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="8b16b-211">[**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) completes successfully, even if the proxy or server requires authentication.</span></span> <span data-ttu-id="8b16b-212">Quando il flag FLAGS ERROR UI FILTER FOR ERRORS viene passato a \_ \_ \_ \_ \_ [**InternetErrorDlg,**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg)la funzione verifica la presenza di eventuali errori nascosti nelle intestazioni.</span><span class="sxs-lookup"><span data-stu-id="8b16b-212">When the FLAGS\_ERROR\_UI\_FILTER\_FOR\_ERRORS flag is passed to [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg), the function checks the headers for any hidden errors.</span></span> <span data-ttu-id="8b16b-213">Questi errori nascosti includono tutte le richieste di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="8b16b-213">These hidden errors would include any requests for authentication.</span></span> <span data-ttu-id="8b16b-214">[**InternetErrorDlg visualizza**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) la finestra di dialogo appropriata per richiedere all'utente i dati necessari.</span><span class="sxs-lookup"><span data-stu-id="8b16b-214">[**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) displays the appropriate dialog box to prompt the user for the necessary data.</span></span> <span data-ttu-id="8b16b-215">I flag FLAGS ERROR UI FLAGS GENERATE DATA e FLAGS ERROR UI FLAGS CHANGE OPTIONS devono essere passati anche a InternetErrorDlg, in modo che la funzione costruisca la struttura dei dati appropriata per l'errore e archivi i risultati della finestra di dialogo \_ \_ \_ \_ \_ \_ \_ \_ \_ nell'handle \_ [**HINTERNET.**](appendix-a-hinternet-handles.md) [](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg)</span><span class="sxs-lookup"><span data-stu-id="8b16b-215">The FLAGS\_ERROR\_UI\_FLAGS\_GENERATE\_DATA and FLAGS\_ERROR\_UI\_FLAGS\_CHANGE\_OPTIONS flags should also be passed to [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg), so that the function constructs the appropriate data structure for the error and stores the results of the dialog box in the [**HINTERNET**](appendix-a-hinternet-handles.md) handle.</span></span>

<span data-ttu-id="8b16b-216">Nell'esempio di codice seguente viene illustrato come gestire l'autenticazione [**tramite InternetSetOption.**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)</span><span class="sxs-lookup"><span data-stu-id="8b16b-216">The following example code shows how authentication could be handled using [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


```C++
HINTERNET hOpenHandle,  hResourceHandle, hConnectHandle;
DWORD dwStatus;
DWORD dwStatusSize = sizeof(dwStatus);
char strUsername[64], strPassword[64];

// Normally, hOpenHandle, hResourceHandle,
// and hConnectHandle need to be properly assigned.

hOpenHandle = InternetOpen(TEXT("Example"),
                           INTERNET_OPEN_TYPE_PRECONFIG,
                           NULL, NULL, 0);
hConnectHandle = InternetConnect(hOpenHandle,
                                 TEXT("www.server.com"),
                                 INTERNET_INVALID_PORT_NUMBER,
                                 NULL,
                                 NULL,
                                 INTERNET_SERVICE_HTTP,
                                 0,0);

hResourceHandle = HttpOpenRequest(hConnectHandle, TEXT("GET"),
                                  TEXT("/premium/default.htm"),
                                  NULL, NULL, NULL,
                                  INTERNET_FLAG_KEEP_CONNECTION,
                                  0);

resend:

HttpSendRequest(hResourceHandle, NULL, 0, NULL, 0);

HttpQueryInfo(hResourceHandle, HTTP_QUERY_FLAG_NUMBER |
              HTTP_QUERY_STATUS_CODE, &dwStatus, &dwStatusSize, NULL);

switch (dwStatus)
{
    // cchUserLength is the length of strUsername and
    // cchPasswordLength is the length of strPassword.
    DWORD cchUserLength, cchPasswordLength;

    case HTTP_STATUS_PROXY_AUTH_REQ: // Proxy Authentication Required
        // Insert code to set strUsername and strPassword.

        // Insert code to safely determine cchUserLength and
        // cchPasswordLength. Insert appropriate error handling code.
        InternetSetOption(hResourceHandle,
                          INTERNET_OPTION_PROXY_USERNAME,
                          strUsername,
                          cchUserLength+1);

        InternetSetOption(hResourceHandle,
                          INTERNET_OPTION_PROXY_PASSWORD,
                          strPassword,
                          cchPasswordLength+1);
        goto resend;
        break;

    case HTTP_STATUS_DENIED:     // Server Authentication Required.
        // Insert code to set strUsername and strPassword.

        // Insert code to safely determine cchUserLength and
        // cchPasswordLength. Insert error handling code as
        // appropriate.
        InternetSetOption(hResourceHandle, INTERNET_OPTION_USERNAME,
                          strUsername, cchUserLength+1);
        InternetSetOption(hResourceHandle, INTERNET_OPTION_PASSWORD,
                          strPassword, cchPasswordLength+1);
        goto resend;
        break;
}

// Insert code to read the data from the hResourceHandle
// at this point.

```



> [!Note]  
> <span data-ttu-id="8b16b-217">WinINet non supporta le implementazioni del server.</span><span class="sxs-lookup"><span data-stu-id="8b16b-217">WinINet does not support server implementations.</span></span> <span data-ttu-id="8b16b-218">Inoltre, non deve essere usato da un servizio.</span><span class="sxs-lookup"><span data-stu-id="8b16b-218">In addition, it should not be used from a service.</span></span> <span data-ttu-id="8b16b-219">Per le implementazioni o i servizi del server usare [i servizi HTTP di Microsoft Windows (WinHTTP).](/windows/desktop/WinHttp/winhttp-start-page)</span><span class="sxs-lookup"><span data-stu-id="8b16b-219">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 