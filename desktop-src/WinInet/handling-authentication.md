---
title: Gestione dell'autenticazione
description: Alcuni proxy e server richiedono l'autenticazione prima di concedere l'accesso alle risorse su Internet.
ms.assetid: f3752031-30d3-4e35-8eae-1d4971b66bc2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36a8eaa38f61f0d97f1f543e0623313aa196aab7
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "104047526"
---
# <a name="handling-authentication"></a><span data-ttu-id="3d43f-103">Gestione dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="3d43f-103">Handling Authentication</span></span>

<span data-ttu-id="3d43f-104">Alcuni proxy e server richiedono l'autenticazione prima di concedere l'accesso alle risorse su Internet.</span><span class="sxs-lookup"><span data-stu-id="3d43f-104">Some proxies and servers require authentication before granting access to resources on the Internet.</span></span> <span data-ttu-id="3d43f-105">Le funzioni WinINet supportano l'autenticazione server e proxy per le sessioni HTTP.</span><span class="sxs-lookup"><span data-stu-id="3d43f-105">The WinINet functions support server and proxy authentication for http sessions.</span></span> <span data-ttu-id="3d43f-106">L'autenticazione dei server FTP deve essere gestita dalla funzione [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) .</span><span class="sxs-lookup"><span data-stu-id="3d43f-106">Authentication of ftp servers must be handled by the [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) function.</span></span> <span data-ttu-id="3d43f-107">Attualmente, l'autenticazione del gateway FTP non è supportata.</span><span class="sxs-lookup"><span data-stu-id="3d43f-107">Currently, FTP gateway authentication is not supported.</span></span>

## <a name="about-http-authentication"></a><span data-ttu-id="3d43f-108">Informazioni sull'autenticazione HTTP</span><span class="sxs-lookup"><span data-stu-id="3d43f-108">About HTTP Authentication</span></span>

<span data-ttu-id="3d43f-109">Se è richiesta l'autenticazione, l'applicazione client riceve un codice di stato 401, se il server richiede l'autenticazione, o 407, se il proxy richiede l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="3d43f-109">If authentication is required, the client application receives a status code 401, if the server requires authentication, or 407, if the proxy requires authentication.</span></span> <span data-ttu-id="3d43f-110">Con il codice di stato, il proxy o il server invia uno o più, autenticare le intestazioni di risposta: proxy-Authenticate (per l'autenticazione proxy) o WWW-Authenticate (per l'autenticazione server).</span><span class="sxs-lookup"><span data-stu-id="3d43f-110">With the status code, the proxy or server sends one, or more, authenticate response headers—Proxy-Authenticate (for proxy authentication) or WWW-Authenticate (for server authentication).</span></span>

<span data-ttu-id="3d43f-111">Ogni intestazione della risposta di autenticazione contiene uno schema di autenticazione disponibile e un'area di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="3d43f-111">Each authenticate response header contains an available authentication scheme and a realm.</span></span> <span data-ttu-id="3d43f-112">Se sono supportati più schemi di autenticazione, il server restituisce più intestazioni di risposta di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="3d43f-112">If multiple authentication schemes are supported, the server returns multiple authenticate response headers.</span></span> <span data-ttu-id="3d43f-113">Il valore dell'area di autenticazione fa distinzione tra maiuscole e minuscole e definisce uno spazio di protezione sul proxy o sul server.</span><span class="sxs-lookup"><span data-stu-id="3d43f-113">The realm value is case-sensitive and defines a protection space on the proxy or server.</span></span> <span data-ttu-id="3d43f-114">Ad esempio, l'intestazione "WWW-Authenticate: Basic realm =" example "" è un esempio di un'intestazione restituita quando è richiesta l'autenticazione server.</span><span class="sxs-lookup"><span data-stu-id="3d43f-114">For example, the header "WWW-Authenticate: Basic Realm="example"" would be an example of a header returned when server authentication is required.</span></span>

<span data-ttu-id="3d43f-115">L'applicazione client che ha inviato la richiesta può autenticarsi con l'inclusione di un campo di intestazione dell'autorizzazione con la richiesta.</span><span class="sxs-lookup"><span data-stu-id="3d43f-115">The client application that sent the request can authenticate itself by including an Authorization header field with the request.</span></span> <span data-ttu-id="3d43f-116">L'intestazione di autorizzazione conterrà lo schema di autenticazione e la risposta appropriata richiesta da tale schema.</span><span class="sxs-lookup"><span data-stu-id="3d43f-116">The Authorization header would contain the authentication scheme and the appropriate response required by that scheme.</span></span> <span data-ttu-id="3d43f-117">Ad esempio, l'intestazione "Authorization: Basic <username: password>" viene aggiunta alla richiesta e inviata nuovamente al server se il client ha ricevuto l'intestazione di risposta di autenticazione "WWW-Authenticate: Basic realm =" example "".</span><span class="sxs-lookup"><span data-stu-id="3d43f-117">For example, the header "Authorization: Basic <username:password>" would be added to the request and re-sent to the server if the client received the authenticate response header "WWW-Authenticate: Basic Realm="example"".</span></span>

<span data-ttu-id="3d43f-118">Esistono due tipi generali di schemi di autenticazione:</span><span class="sxs-lookup"><span data-stu-id="3d43f-118">There are two general types of authentication schemes:</span></span>

-   <span data-ttu-id="3d43f-119">Schema di autenticazione di base, in cui il nome utente e la password vengono inviati in testo non crittografato al server.</span><span class="sxs-lookup"><span data-stu-id="3d43f-119">Basic authentication scheme, where the user name and password are sent in cleartext to the server.</span></span>
-   <span data-ttu-id="3d43f-120">Schemi di richiesta-risposta che consentono un formato di richiesta-risposta.</span><span class="sxs-lookup"><span data-stu-id="3d43f-120">Challenge-response schemes, which allow for a challenge-response format.</span></span>

<span data-ttu-id="3d43f-121">Lo schema di autenticazione di base è basato sul modello che un client deve autenticarsi con un nome utente e una password per ogni area di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="3d43f-121">The Basic authentication scheme is based on the model that a client must authenticate itself with a user name and password for each realm.</span></span> <span data-ttu-id="3d43f-122">Il server di Invia la richiesta se viene inviato nuovamente con un'intestazione di autorizzazione che include un nome utente e una password validi.</span><span class="sxs-lookup"><span data-stu-id="3d43f-122">The server services the request if it is resent with an Authorization header that includes a valid user name and password.</span></span>

<span data-ttu-id="3d43f-123">Gli schemi di richiesta-risposta consentono un'autenticazione più sicura.</span><span class="sxs-lookup"><span data-stu-id="3d43f-123">Challenge-response schemes enable more secure authentication.</span></span> <span data-ttu-id="3d43f-124">Se per una richiesta è necessaria l'autenticazione tramite uno schema di verifica della risposta, il codice di stato appropriato e le intestazioni di autenticazione vengono restituiti al client.</span><span class="sxs-lookup"><span data-stu-id="3d43f-124">If a request requires authentication using a challenge-response scheme, the appropriate status code and Authenticate headers are returned to the client.</span></span> <span data-ttu-id="3d43f-125">Il client deve quindi inviare nuovamente la richiesta con una negoziazione.</span><span class="sxs-lookup"><span data-stu-id="3d43f-125">The client must then to resend the request with a negotiate.</span></span> <span data-ttu-id="3d43f-126">Il server restituirà un codice di stato appropriato con una richiesta di verifica e il client dovrà quindi inviare nuovamente la richiesta con la risposta appropriata per ottenere il servizio richiesto.</span><span class="sxs-lookup"><span data-stu-id="3d43f-126">The server would return an appropriate status code with a challenge, and the client would then require to resend the request with the proper response to get the requested service.</span></span>

<span data-ttu-id="3d43f-127">Nella tabella seguente sono elencati gli schemi di autenticazione, il tipo di autenticazione, la DLL che li supporta e una descrizione dello schema.</span><span class="sxs-lookup"><span data-stu-id="3d43f-127">The following table lists authentication schemes, the authentication type, the DLL that supports them, and a description of the scheme.</span></span>



| <span data-ttu-id="3d43f-128">Schema</span><span class="sxs-lookup"><span data-stu-id="3d43f-128">Scheme</span></span>                                    | <span data-ttu-id="3d43f-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="3d43f-129">Type</span></span>               | <span data-ttu-id="3d43f-130">DLL</span><span class="sxs-lookup"><span data-stu-id="3d43f-130">DLL</span></span>                  | <span data-ttu-id="3d43f-131">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3d43f-131">Description</span></span>                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------------|--------------------|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d43f-132">Di base (testo non crittografato)</span><span class="sxs-lookup"><span data-stu-id="3d43f-132">Basic (cleartext)</span></span>                         | <span data-ttu-id="3d43f-133">basic</span><span class="sxs-lookup"><span data-stu-id="3d43f-133">basic</span></span>              | <span data-ttu-id="3d43f-134">Wininet.dll</span><span class="sxs-lookup"><span data-stu-id="3d43f-134">Wininet.dll</span></span>          | <span data-ttu-id="3d43f-135">Usa una stringa con codifica Base64 che contiene il nome utente e la password.</span><span class="sxs-lookup"><span data-stu-id="3d43f-135">Uses a base64 encoded string that contains the user name and password.</span></span>                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="3d43f-136">Digest</span><span class="sxs-lookup"><span data-stu-id="3d43f-136">Digest</span></span>                                    | <span data-ttu-id="3d43f-137">richiesta-risposta</span><span class="sxs-lookup"><span data-stu-id="3d43f-137">challenge-response</span></span> | <span data-ttu-id="3d43f-138">Digest.dll</span><span class="sxs-lookup"><span data-stu-id="3d43f-138">Digest.dll</span></span>           | <span data-ttu-id="3d43f-139">Schema di richiesta-risposta che richiede l'uso di un valore nonce, ovvero una stringa di dati specificata dal server.</span><span class="sxs-lookup"><span data-stu-id="3d43f-139">A challenge-response scheme that challenges using a nonce (a server-specified data string) value.</span></span> <span data-ttu-id="3d43f-140">Una risposta valida contiene un checksum del nome utente, la password, il valore nonce specificato, il metodo HTTP e la Uniform Resource Identifier richiesta (URI).</span><span class="sxs-lookup"><span data-stu-id="3d43f-140">A valid response contains a checksum of the user name, the password, the given nonce value, the HTTP method, and the requested Uniform Resource Identifier (URI).</span></span> <span data-ttu-id="3d43f-141">Il supporto per l'autenticazione del digest è stato introdotto in Microsoft Internet Explorer 5.</span><span class="sxs-lookup"><span data-stu-id="3d43f-141">Digest authentication support was introduced in Microsoft Internet Explorer 5.</span></span> |
| <span data-ttu-id="3d43f-142">NT LAN Manager (NTLM)</span><span class="sxs-lookup"><span data-stu-id="3d43f-142">NT LAN Manager (NTLM)</span></span>                     | <span data-ttu-id="3d43f-143">richiesta-risposta</span><span class="sxs-lookup"><span data-stu-id="3d43f-143">challenge-response</span></span> | <span data-ttu-id="3d43f-144">Winsspi.dll</span><span class="sxs-lookup"><span data-stu-id="3d43f-144">Winsspi.dll</span></span>          | <span data-ttu-id="3d43f-145">Uno schema di richiesta-risposta che basa la richiesta sul nome utente.</span><span class="sxs-lookup"><span data-stu-id="3d43f-145">A challenge-response scheme that bases the challenge on the user name.</span></span>                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="3d43f-146">Rete Microsoft (MSN)</span><span class="sxs-lookup"><span data-stu-id="3d43f-146">Microsoft Network (MSN)</span></span>                   | <span data-ttu-id="3d43f-147">richiesta-risposta</span><span class="sxs-lookup"><span data-stu-id="3d43f-147">challenge-response</span></span> | <span data-ttu-id="3d43f-148">Msnsspc.dll</span><span class="sxs-lookup"><span data-stu-id="3d43f-148">Msnsspc.dll</span></span>          | <span data-ttu-id="3d43f-149">Schema di autenticazione di The Microsoft Network.</span><span class="sxs-lookup"><span data-stu-id="3d43f-149">The Microsoft Network's authentication scheme.</span></span>                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="3d43f-150">Autenticazione della password distribuita</span><span class="sxs-lookup"><span data-stu-id="3d43f-150">Distributed Password Authentication (DPA)</span></span> | <span data-ttu-id="3d43f-151">richiesta-risposta</span><span class="sxs-lookup"><span data-stu-id="3d43f-151">challenge-response</span></span> | <span data-ttu-id="3d43f-152">Msapsspc.dll</span><span class="sxs-lookup"><span data-stu-id="3d43f-152">Msapsspc.dll</span></span>         | <span data-ttu-id="3d43f-153">Simile all'autenticazione MSN e viene usato anche dalla rete Microsoft.</span><span class="sxs-lookup"><span data-stu-id="3d43f-153">Similar to MSN authentication and is also used by the Microsoft Network.</span></span>                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="3d43f-154">Autenticazione passphrase remota (RPA)</span><span class="sxs-lookup"><span data-stu-id="3d43f-154">Remote Passphrase Authentication (RPA)</span></span>    | <span data-ttu-id="3d43f-155">CompuServe</span><span class="sxs-lookup"><span data-stu-id="3d43f-155">CompuServe</span></span>         | <span data-ttu-id="3d43f-156">Rpawinet.dll, da.dll</span><span class="sxs-lookup"><span data-stu-id="3d43f-156">Rpawinet.dll, da.dll</span></span> | <span data-ttu-id="3d43f-157">Schema di autenticazione CompuServe.</span><span class="sxs-lookup"><span data-stu-id="3d43f-157">CompuServe authentication scheme.</span></span> <span data-ttu-id="3d43f-158">Per ulteriori informazioni, vedere le [specifiche del meccanismo RPA](https://www.compuserve.com/).</span><span class="sxs-lookup"><span data-stu-id="3d43f-158">For more information, see the [RPA Mechanism Specifications](https://www.compuserve.com/).</span></span>                                                                                                                                                                                                    |



 

<span data-ttu-id="3d43f-159">Per qualsiasi elemento diverso dall'autenticazione di base, è necessario configurare le chiavi del registro di sistema oltre all'installazione della DLL appropriata.</span><span class="sxs-lookup"><span data-stu-id="3d43f-159">For anything other than Basic authentication, the registry keys must be set up in addition to installing the appropriate DLL.</span></span>

<span data-ttu-id="3d43f-160">Se è necessaria l'autenticazione, nella chiamata a [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)è necessario usare il flag [Internet \_ \_ Keep \_ Connection](api-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="3d43f-160">If authentication is required, the [INTERNET\_FLAG\_KEEP\_CONNECTION](api-flags.md) flag should be used in the call to [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span> <span data-ttu-id="3d43f-161">Il \_ contrassegno Internet flag \_ Keep \_ Connection è necessario per NTLM e altri tipi di autenticazione per mantenere la connessione durante il completamento del processo di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="3d43f-161">The INTERNET\_FLAG\_KEEP\_CONNECTION flag is required for NTLM and other types of authentication in order to maintain the connection while completing the authentication process.</span></span> <span data-ttu-id="3d43f-162">Se la connessione non viene mantenuta, il processo di autenticazione deve essere riavviato con il proxy o il server.</span><span class="sxs-lookup"><span data-stu-id="3d43f-162">If the connection is not maintained, the authentication process must be restarted with the proxy or server.</span></span>

<span data-ttu-id="3d43f-163">Le funzioni [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) e [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) vengono completate correttamente anche quando è richiesta l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="3d43f-163">The [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) and [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) functions complete successfully even when authentication is required.</span></span> <span data-ttu-id="3d43f-164">La differenza è che i dati restituiti nei file di intestazione e [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) riceveranno una pagina HTML che informa l'utente del codice di stato.</span><span class="sxs-lookup"><span data-stu-id="3d43f-164">The difference is, the data returned in the header files and [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) would receive an HTML page informing the user of the status code.</span></span>

### <a name="registering-authentication-keys"></a><span data-ttu-id="3d43f-165">Registrazione delle chiavi di autenticazione</span><span class="sxs-lookup"><span data-stu-id="3d43f-165">Registering Authentication Keys</span></span>

<span data-ttu-id="3d43f-166">\_ \_ La preconfigurazione di Internet Open Type \_ esamina i valori del registro di sistema **ProxyEnable**, **ProxyServer** e **ProxyOverride**.</span><span class="sxs-lookup"><span data-stu-id="3d43f-166">INTERNET\_OPEN\_TYPE\_PRECONFIG looks at the registry values **ProxyEnable**, **ProxyServer**, and **ProxyOverride**.</span></span> <span data-ttu-id="3d43f-167">Questi valori si trovano in **HKEY \_ Current \_ User** \\ **software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Internet Settings**.</span><span class="sxs-lookup"><span data-stu-id="3d43f-167">These values are located under **HKEY\_CURRENT\_USER**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Internet Settings**.</span></span>

<span data-ttu-id="3d43f-168">Per gli schemi di autenticazione diversi da Basic è necessario aggiungere una chiave al registro di sistema in **HKEY \_ Local \_ Machine** \\ **software** \\ **Microsoft** \\ **Internet Explorer** \\ **Security**.</span><span class="sxs-lookup"><span data-stu-id="3d43f-168">For authentication schemes other than Basic, a key must be added to the registry under **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Internet Explorer**\\**Security**.</span></span> <span data-ttu-id="3d43f-169">È necessario impostare un valore **DWORD** , **Flags**, con il valore appropriato.</span><span class="sxs-lookup"><span data-stu-id="3d43f-169">A **DWORD** value, **Flags**, should be set with the appropriate value.</span></span> <span data-ttu-id="3d43f-170">Nell'elenco seguente sono indicati i valori possibili per il valore dei **flag** .</span><span class="sxs-lookup"><span data-stu-id="3d43f-170">The following list shows the possible values for the **Flags** value.</span></span>

-   <span data-ttu-id="3d43f-171">Flag di autenticazione plug-in il \_ \_ \_ \_ contesto univoco \_ per \_ Tcpip (value = 0x01)</span><span class="sxs-lookup"><span data-stu-id="3d43f-171">PLUGIN\_AUTH\_FLAGS\_UNIQUE\_CONTEXT\_PER\_TCPIP (value=0x01)</span></span>

    <span data-ttu-id="3d43f-172">Ogni socket TCP/IP (Transmission Control Protocol/Internet Protocol) contiene un contesto diverso.</span><span class="sxs-lookup"><span data-stu-id="3d43f-172">Each Transmission Control Protocol/Internet Protocol (TCP/IP) socket contains a different context.</span></span> <span data-ttu-id="3d43f-173">In caso contrario, viene passato un nuovo contesto per ogni modello di area di autenticazione o di URL di blocco.</span><span class="sxs-lookup"><span data-stu-id="3d43f-173">Otherwise, a new context is passed for each realm or block URL template.</span></span>

-   <span data-ttu-id="3d43f-174">I flag di autenticazione plug-in \_ \_ \_ possono \_ gestire l' \_ interfaccia utente (value = 0x02)</span><span class="sxs-lookup"><span data-stu-id="3d43f-174">PLUGIN\_AUTH\_FLAGS\_CAN\_HANDLE\_UI (value=0x02)</span></span>

    <span data-ttu-id="3d43f-175">Questa DLL può gestire il proprio input utente.</span><span class="sxs-lookup"><span data-stu-id="3d43f-175">This DLL can handle its own user input.</span></span>

-   <span data-ttu-id="3d43f-176">I flag di autenticazione plug-in \_ \_ \_ possono \_ gestire \_ Nessuna \_ password (valore = 0x04)</span><span class="sxs-lookup"><span data-stu-id="3d43f-176">PLUGIN\_AUTH\_FLAGS\_CAN\_HANDLE\_NO\_PASSWD (value=0x04)</span></span>

    <span data-ttu-id="3d43f-177">Questa DLL può essere in grado di eseguire un'autenticazione senza richiedere una password all'utente.</span><span class="sxs-lookup"><span data-stu-id="3d43f-177">This DLL might be capable of doing an authentication without prompting the user for a password.</span></span>

-   <span data-ttu-id="3d43f-178">Flag di autenticazione plug-in \_ \_ \_ senza \_ area di autenticazione (valore = 0x08)</span><span class="sxs-lookup"><span data-stu-id="3d43f-178">PLUGIN\_AUTH\_FLAGS\_NO\_REALM (value=0x08)</span></span>

    <span data-ttu-id="3d43f-179">Questa DLL non usa una stringa dell'area di autenticazione HTTP standard.</span><span class="sxs-lookup"><span data-stu-id="3d43f-179">This DLL does not use a standard http realm string.</span></span> <span data-ttu-id="3d43f-180">Qualsiasi dato che sembra essere un'area di autenticazione è costituito da dati specifici dello schema.</span><span class="sxs-lookup"><span data-stu-id="3d43f-180">Any data that appears to be a realm is scheme-specific data.</span></span>

-   <span data-ttu-id="3d43f-181">I flag di autenticazione plug-in \_ \_ \_ Keep \_ Alive \_ non sono \_ necessari (valore = 0x10)</span><span class="sxs-lookup"><span data-stu-id="3d43f-181">PLUGIN\_AUTH\_FLAGS\_KEEP\_ALIVE\_NOT\_REQUIRED (value=0x10)</span></span>

    <span data-ttu-id="3d43f-182">Questa DLL non richiede una connessione permanente per la relativa sequenza di richiesta-risposta.</span><span class="sxs-lookup"><span data-stu-id="3d43f-182">This DLL does not require a persistent connection for its challenge-response sequence.</span></span>

<span data-ttu-id="3d43f-183">Ad esempio, per aggiungere l'autenticazione NTLM, è necessario aggiungere la chiave NTLM a **HKEY \_ Local \_ Machine** \\ **software** \\ **Microsoft** \\ **Internet Explorer** \\ **Security**.</span><span class="sxs-lookup"><span data-stu-id="3d43f-183">For example, to add NTLM authentication, the key NTLM must be added to **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Internet Explorer**\\**Security**.</span></span> <span data-ttu-id="3d43f-184">In **HKEY \_ Local \_ Machine** \\ **software** \\ **Microsoft** \\ **Internet Explorer** \\ **Security** \\ **NTLM**, è necessario aggiungere il valore stringa **DLLFile** e un valore **DWORD** , **Flags**.</span><span class="sxs-lookup"><span data-stu-id="3d43f-184">Under **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Internet Explorer**\\**Security**\\**NTLM**, the string value, **DLLFile**, and a **DWORD** value, **Flags**, must be added.</span></span> <span data-ttu-id="3d43f-185">**DLLFile** deve essere impostato su Winsspi.dll e i **flag** devono essere impostati su 0x08.</span><span class="sxs-lookup"><span data-stu-id="3d43f-185">**DLLFile** must be set to Winsspi.dll, and **Flags** must be set to 0x08.</span></span>

### <a name="server-authentication"></a><span data-ttu-id="3d43f-186">Autenticazione del server</span><span class="sxs-lookup"><span data-stu-id="3d43f-186">Server Authentication</span></span>

<span data-ttu-id="3d43f-187">Quando un server riceve una richiesta che richiede l'autenticazione, il server restituisce un messaggio di codice di stato 401.</span><span class="sxs-lookup"><span data-stu-id="3d43f-187">When a server receives a request that requires authentication, the server returns a 401 status code message.</span></span> <span data-ttu-id="3d43f-188">Nel messaggio, il server deve includere una o più intestazioni di risposta WWW-Authenticate.</span><span class="sxs-lookup"><span data-stu-id="3d43f-188">In that message, the server should include one or more WWW-Authenticate response headers.</span></span> <span data-ttu-id="3d43f-189">Queste intestazioni includono i metodi di autenticazione disponibili per il server.</span><span class="sxs-lookup"><span data-stu-id="3d43f-189">These headers include the authentication methods the server has available.</span></span> <span data-ttu-id="3d43f-190">WinINet sceglie il primo metodo che riconosce.</span><span class="sxs-lookup"><span data-stu-id="3d43f-190">WinINet chooses the first method it recognizes.</span></span>

<span data-ttu-id="3d43f-191">L'autenticazione di base garantisce una sicurezza debole, a meno che il canale non sia stato crittografato per la prima volta con SSL o PCT.</span><span class="sxs-lookup"><span data-stu-id="3d43f-191">Basic authentication provides weak security unless the channel is first link-encrypted with SSL or PCT.</span></span>

<span data-ttu-id="3d43f-192">La funzione [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) può essere utilizzata per ottenere i dati del nome utente e della password dall'utente oppure un'interfaccia utente personalizzata può essere progettata per ottenere i dati.</span><span class="sxs-lookup"><span data-stu-id="3d43f-192">The [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) function can be used to obtain the user name and password data from the user, or a customized user interface can be designed to obtain the data.</span></span>

<span data-ttu-id="3d43f-193">Un'interfaccia personalizzata può usare la funzione [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) per impostare la [ \_ \_ password dell'opzione Internet](option-flags.md) e i valori del [ \_ \_ nome utente dell'opzione Internet](option-flags.md) , quindi inviare nuovamente la richiesta al server.</span><span class="sxs-lookup"><span data-stu-id="3d43f-193">A custom interface can use the [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) function to set the [INTERNET\_OPTION\_PASSWORD](option-flags.md) and [INTERNET\_OPTION\_USERNAME](option-flags.md) values and then resend the request to the server.</span></span>

### <a name="proxy-authentication"></a><span data-ttu-id="3d43f-194">Autenticazione proxy</span><span class="sxs-lookup"><span data-stu-id="3d43f-194">Proxy Authentication</span></span>

<span data-ttu-id="3d43f-195">Quando un client tenta di usare un proxy che richiede l'autenticazione, il proxy restituisce un messaggio di codice di stato 407 al client.</span><span class="sxs-lookup"><span data-stu-id="3d43f-195">When a client attempts to use a proxy that requires authentication, the proxy returns a 407 status code message to the client.</span></span> <span data-ttu-id="3d43f-196">Nel messaggio, il proxy deve includere una o più intestazioni di risposta Proxy-Authenticate.</span><span class="sxs-lookup"><span data-stu-id="3d43f-196">In that message, the proxy should include one or more Proxy-Authenticate response headers.</span></span> <span data-ttu-id="3d43f-197">Queste intestazioni includono i metodi di autenticazione disponibili dal proxy.</span><span class="sxs-lookup"><span data-stu-id="3d43f-197">These headers include the authentication methods available from the proxy.</span></span> <span data-ttu-id="3d43f-198">WinINet sceglie il primo metodo che riconosce.</span><span class="sxs-lookup"><span data-stu-id="3d43f-198">WinINet chooses the first method it recognizes.</span></span>

<span data-ttu-id="3d43f-199">La funzione [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) può essere usata per ottenere i dati relativi a nome utente e password dall'utente oppure è possibile progettare un'interfaccia utente personalizzata.</span><span class="sxs-lookup"><span data-stu-id="3d43f-199">The [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) function can be used to obtain the user name and password data from the user, or a customized user interface can be designed.</span></span>

<span data-ttu-id="3d43f-200">Un'interfaccia personalizzata può usare la funzione [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) per impostare la [ \_ \_ \_ password del proxy dell'opzione Internet](option-flags.md) e il [ \_ \_ \_ nome utente del proxy di opzione Internet](option-flags.md) e quindi inviare nuovamente la richiesta al proxy.</span><span class="sxs-lookup"><span data-stu-id="3d43f-200">A custom interface can use the [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) function to set the [INTERNET\_OPTION\_PROXY\_PASSWORD](option-flags.md) and [INTERNET\_OPTION\_PROXY\_USERNAME](option-flags.md) values and then resend the request to the proxy.</span></span>

<span data-ttu-id="3d43f-201">Se non è impostato alcun nome utente e password proxy, WinINet tenta di utilizzare il nome utente e la password per il server.</span><span class="sxs-lookup"><span data-stu-id="3d43f-201">If no proxy user name and password are set, WinINet attempts to use the user name and password for the server.</span></span> <span data-ttu-id="3d43f-202">Questo comportamento consente ai client di implementare la stessa interfaccia utente personalizzata utilizzata per gestire l'autenticazione del server.</span><span class="sxs-lookup"><span data-stu-id="3d43f-202">This behavior enables clients to implement the same customized user interface used to handle server authentication.</span></span>

## <a name="handling-http-authentication"></a><span data-ttu-id="3d43f-203">Gestione dell'autenticazione HTTP</span><span class="sxs-lookup"><span data-stu-id="3d43f-203">Handling HTTP Authentication</span></span>

<span data-ttu-id="3d43f-204">L'autenticazione HTTP può essere gestita con [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) o con una funzione personalizzata che usa [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) o aggiunge le proprie intestazioni di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="3d43f-204">HTTP authentication can be handled with either [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) or a customized function that uses [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) or adds its own authentication headers.</span></span> <span data-ttu-id="3d43f-205">[**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) può esaminare le intestazioni associate a un handle [**HINTERNET**](appendix-a-hinternet-handles.md) per trovare errori nascosti, ad esempio codici di stato da un proxy o un server.</span><span class="sxs-lookup"><span data-stu-id="3d43f-205">[**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) can examine the headers associated with an [**HINTERNET**](appendix-a-hinternet-handles.md) handle to find hidden errors, such as status codes from a proxy or server.</span></span> <span data-ttu-id="3d43f-206">[**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) può essere utilizzato per impostare il nome utente e la password per il proxy e il server.</span><span class="sxs-lookup"><span data-stu-id="3d43f-206">[**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) can be used to set the user name and password for the proxy and server.</span></span> <span data-ttu-id="3d43f-207">Per l'autenticazione MSN e DPA, è necessario usare [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) per impostare il nome utente e la password.</span><span class="sxs-lookup"><span data-stu-id="3d43f-207">For MSN and DPA authentication, [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) must be used to set the user name and password.</span></span>

<span data-ttu-id="3d43f-208">Per qualsiasi funzione personalizzata che aggiunge le proprie intestazioni WWW-Authenticate o Proxy-Authenticate, il [ \_ flag Internet \_ nessun \_ ](api-flags.md) flag di autenticazione deve essere impostato per disabilitare l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="3d43f-208">For any customized function that adds its own WWW-Authenticate or Proxy-Authenticate headers, the [INTERNET\_FLAG\_NO\_AUTH](api-flags.md) flag should be set to disable authentication.</span></span>

<span data-ttu-id="3d43f-209">Nell'esempio seguente viene illustrato come utilizzare [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) per gestire l'autenticazione HTTP.</span><span class="sxs-lookup"><span data-stu-id="3d43f-209">The following example shows how [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) can be used to handle HTTP authentication.</span></span>


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



<span data-ttu-id="3d43f-210">Nell'esempio, dwErrorCode viene usato per archiviare gli eventuali errori associati alla chiamata a [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span><span class="sxs-lookup"><span data-stu-id="3d43f-210">In the example, dwErrorCode is used to store any errors associated with the call to [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span></span> <span data-ttu-id="3d43f-211">[**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) viene completato correttamente, anche se il proxy o il server richiede l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="3d43f-211">[**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) completes successfully, even if the proxy or server requires authentication.</span></span> <span data-ttu-id="3d43f-212">Quando il \_ flag del \_ filtro dell'interfaccia utente per i flag Error \_ per gli \_ \_ errori viene passato a [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg), la funzione controlla le intestazioni per individuare eventuali errori nascosti.</span><span class="sxs-lookup"><span data-stu-id="3d43f-212">When the FLAGS\_ERROR\_UI\_FILTER\_FOR\_ERRORS flag is passed to [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg), the function checks the headers for any hidden errors.</span></span> <span data-ttu-id="3d43f-213">Questi errori nascosti includono qualsiasi richiesta di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="3d43f-213">These hidden errors would include any requests for authentication.</span></span> <span data-ttu-id="3d43f-214">[**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) Visualizza la finestra di dialogo appropriata per richiedere all'utente i dati necessari.</span><span class="sxs-lookup"><span data-stu-id="3d43f-214">[**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) displays the appropriate dialog box to prompt the user for the necessary data.</span></span> <span data-ttu-id="3d43f-215">I flag \_ dell' \_ interfaccia utente degli errori \_ di flag \_ generano \_ dati e flag \_ errore flag interfaccia utente i flag \_ \_ \_ \_ delle opzioni di modifica devono essere passati anche a [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg), in modo che la funzione costruisca la struttura dei dati appropriata per l'errore e archivia i risultati della finestra di dialogo nell'handle [**HINTERNET**](appendix-a-hinternet-handles.md) .</span><span class="sxs-lookup"><span data-stu-id="3d43f-215">The FLAGS\_ERROR\_UI\_FLAGS\_GENERATE\_DATA and FLAGS\_ERROR\_UI\_FLAGS\_CHANGE\_OPTIONS flags should also be passed to [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg), so that the function constructs the appropriate data structure for the error and stores the results of the dialog box in the [**HINTERNET**](appendix-a-hinternet-handles.md) handle.</span></span>

<span data-ttu-id="3d43f-216">Nell'esempio di codice riportato di seguito viene illustrato il modo in cui l'autenticazione può essere gestita utilizzando [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="3d43f-216">The following example code shows how authentication could be handled using [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


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
> <span data-ttu-id="3d43f-217">WinINet non supporta le implementazioni del server.</span><span class="sxs-lookup"><span data-stu-id="3d43f-217">WinINet does not support server implementations.</span></span> <span data-ttu-id="3d43f-218">Inoltre, non deve essere utilizzato da un servizio.</span><span class="sxs-lookup"><span data-stu-id="3d43f-218">In addition, it should not be used from a service.</span></span> <span data-ttu-id="3d43f-219">Per le implementazioni o i servizi del server, usare i [Servizi http di Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="3d43f-219">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 