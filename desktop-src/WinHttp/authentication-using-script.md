---
description: In questa sezione viene illustrato come scrivere script che usa l'oggetto WinHttpRequest per accedere ai dati da un server che richiede l'autenticazione HTTP.
ms.assetid: 9e46777c-4d79-4f9b-9b31-1280ed1e3289
title: Autenticazione tramite script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1d33b8042cd1fd15d46e15dfb3624e0d3b4a885b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312698"
---
# <a name="authentication-using-script"></a><span data-ttu-id="fcd19-103">Autenticazione tramite script</span><span class="sxs-lookup"><span data-stu-id="fcd19-103">Authentication Using Script</span></span>

<span data-ttu-id="fcd19-104">In questa sezione viene illustrato come scrivere script che usa l'oggetto [**WinHttpRequest**](winhttprequest.md) per accedere ai dati da un server che richiede l'autenticazione HTTP.</span><span class="sxs-lookup"><span data-stu-id="fcd19-104">This section demonstrates how to write script that uses the [**WinHttpRequest**](winhttprequest.md) object to access data from a server that requires HTTP authentication.</span></span>

-   [<span data-ttu-id="fcd19-105">Prerequisiti e requisiti</span><span class="sxs-lookup"><span data-stu-id="fcd19-105">Prerequisites and Requirements</span></span>](#prerequisites-and-requirements)
-   [<span data-ttu-id="fcd19-106">Accesso a un sito Web con autenticazione</span><span class="sxs-lookup"><span data-stu-id="fcd19-106">Accessing a Web Site With Authentication</span></span>](#accessing-a-web-site-with-authentication)
-   [<span data-ttu-id="fcd19-107">Controllo dei codici di stato</span><span class="sxs-lookup"><span data-stu-id="fcd19-107">Checking the Status Codes</span></span>](#checking-the-status-codes)
-   [<span data-ttu-id="fcd19-108">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fcd19-108">Related topics</span></span>](#related-topics)

## <a name="prerequisites-and-requirements"></a><span data-ttu-id="fcd19-109">Prerequisiti e requisiti</span><span class="sxs-lookup"><span data-stu-id="fcd19-109">Prerequisites and Requirements</span></span>

<span data-ttu-id="fcd19-110">Oltre a una conoscenza approfondita di Microsoft JScript, questo esempio richiede quanto segue:</span><span class="sxs-lookup"><span data-stu-id="fcd19-110">In addition to a working knowledge of Microsoft JScript, this example requires the following:</span></span>

-   <span data-ttu-id="fcd19-111">Versione corrente del Software Development Kit (SDK) di Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="fcd19-111">The current version of the Microsoft Windows Software Development Kit (SDK).</span></span>
-   <span data-ttu-id="fcd19-112">Lo strumento di configurazione proxy per stabilire le impostazioni proxy per i servizi HTTP di Microsoft Windows (WinHTTP), se la connessione a Internet avviene tramite un server proxy.</span><span class="sxs-lookup"><span data-stu-id="fcd19-112">The proxy configuration tool to establish the proxy settings for Microsoft Windows HTTP Services (WinHTTP), if your connection to the Internet is through a proxy server.</span></span> <span data-ttu-id="fcd19-113">Per ulteriori informazioni [ , vedereProxycfg.exe, uno strumento di configurazione del proxy](proxycfg-exe--a-proxy-configuration-tool.md) .</span><span class="sxs-lookup"><span data-stu-id="fcd19-113">See [Proxycfg.exe, a Proxy Configuration Tool](proxycfg-exe--a-proxy-configuration-tool.md) for more information.</span></span>
-   <span data-ttu-id="fcd19-114">Una certa familiarità con i concetti e la [terminologia di rete](network-terminology.md) .</span><span class="sxs-lookup"><span data-stu-id="fcd19-114">A familiarity with [network terminology](network-terminology.md) and concepts.</span></span>

## <a name="accessing-a-web-site-with-authentication"></a><span data-ttu-id="fcd19-115">Accesso a un sito Web con autenticazione</span><span class="sxs-lookup"><span data-stu-id="fcd19-115">Accessing a Web Site With Authentication</span></span>

<span data-ttu-id="fcd19-116">**Per creare uno script che illustri l'autenticazione, eseguire le operazioni seguenti:**</span><span class="sxs-lookup"><span data-stu-id="fcd19-116">**To create a script that demonstrates authentication, do the following:**</span></span>

1.  <span data-ttu-id="fcd19-117">Aprire un editor di testo, ad esempio Blocco note di Microsoft.</span><span class="sxs-lookup"><span data-stu-id="fcd19-117">Open a text editor such as Microsoft Notepad.</span></span>
2.  <span data-ttu-id="fcd19-118">Copiare il codice seguente nell'editor di testo dopo aver sostituito " \[ authenticationSite \] " con il testo appropriato per specificare l'URL di un sito che richiede l'autenticazione HTTP.</span><span class="sxs-lookup"><span data-stu-id="fcd19-118">Copy the following code into the text editor after replacing "\[authenticationSite\]" with the appropriate text to specify the URL of a site that requires HTTP authentication.</span></span>

    ```VB
    // Load the WinHttpRequest object.
    var WinHttpReq = 
              new ActiveXObject("WinHttp.WinHttpRequest.5.1");

    function getText1( )
    {
      // Specify the target resource.
      WinHttpReq.open( "GET", 
                       "https://[authenticationSite]", 
                       false;

      // Send a request to the server and wait for a response.
      WinHttpReq.send( );

      // Display the results of the request.
      WScript.Echo( "No Credentials: " );
      WScript.Echo( WinHttpReq.Status + "   " + WinHttpReq.StatusText);
      WScript.Echo( WinHttpReq.GetAllResponseHeaders);
      WScript.Echo( );
    };

    function getText2( )
    {
      // HttpRequest SetCredentials flags
      HTTPREQUEST_SETCREDENTIALS_FOR_SERVER = 0;

      // Specify the target resource.
      WinHttpReq.open( "GET", 
                       "https://[authenticationSite]", 
                       false );

      // Set credentials for server.
      WinHttpReq.SetCredentials( "User Name", 
                                 "Password",
                                 HTTPREQUEST_SETCREDENTIALS_FOR_SERVER);

      // It might also be necessary to supply credentials 
      // to the proxy if you connect to the Internet 
      // through a proxy that requires authentication.

      // Send a request to the server and wait for 
      // a response.
      WinHttpReq.send( );

      // Display the results of the request.
      WScript.Echo( "Credentials: " );
      WScript.Echo( WinHttpReq.Status + "   " + WinHttpReq.StatusText );
      WScript.Echo( WinHttpReq.GetAllResponseHeaders( ) );
      WScript.Echo( );
    };

    getText1( );
    getText2( );
    ```

    

3.  <span data-ttu-id="fcd19-119">Salvare il file con il nome "Auth.js".</span><span class="sxs-lookup"><span data-stu-id="fcd19-119">Save the file as "Auth.js".</span></span>
4.  <span data-ttu-id="fcd19-120">Al prompt dei comandi digitare "cscript Auth.js" e premere INVIO.</span><span class="sxs-lookup"><span data-stu-id="fcd19-120">From a command prompt, type "cscript Auth.js" and press ENTER.</span></span>

<span data-ttu-id="fcd19-121">A questo punto è disponibile un programma che richiede una risorsa in due modi diversi.</span><span class="sxs-lookup"><span data-stu-id="fcd19-121">You now have a program that requests a resource two different ways.</span></span> <span data-ttu-id="fcd19-122">Il primo metodo richiede la risorsa senza fornire le credenziali.</span><span class="sxs-lookup"><span data-stu-id="fcd19-122">The first method requests the resource without supplying credentials.</span></span> <span data-ttu-id="fcd19-123">Viene restituito un codice di stato 401 per indicare che il server richiede l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="fcd19-123">A 401 status code is returned to indicate that the server requires authentication.</span></span> <span data-ttu-id="fcd19-124">Vengono inoltre visualizzate le intestazioni di risposta e dovrebbero essere simili alle seguenti:</span><span class="sxs-lookup"><span data-stu-id="fcd19-124">The response headers are also displayed and should look similar to the following:</span></span>

``` syntax
Connection: Keep-Alive
Content-Length: 0
Date: Fri, 27 Apr 2001 01:47:18 GMT
Content-Type: text/html
Server: Microsoft-IIS/5.0
WWW-Authenticate: NTLM
WWW-Authenticate: Negotiate
Cache-control: private
```

<span data-ttu-id="fcd19-125">Sebbene la risposta indichi che l'accesso alla risorsa è stato negato, restituisce comunque diverse intestazioni che forniscono alcune informazioni sulla risorsa.</span><span class="sxs-lookup"><span data-stu-id="fcd19-125">Although the response indicates that access to the resource was denied, it still returns several headers that provide some information about the resource.</span></span> <span data-ttu-id="fcd19-126">L'intestazione denominata "WWW-Authenticate" indica che il server richiede l'autenticazione per questa risorsa.</span><span class="sxs-lookup"><span data-stu-id="fcd19-126">The header named "WWW-Authenticate" indicates that the server requires authentication for this resource.</span></span> <span data-ttu-id="fcd19-127">Se è presente un'intestazione denominata "proxy-Authenticate", indica che il server proxy richiede l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="fcd19-127">If there was a header named "Proxy-Authenticate", it would indicate that the proxy server requires authentication.</span></span> <span data-ttu-id="fcd19-128">Ogni intestazione Authenticate contiene uno schema di autenticazione disponibile e talvolta un'area di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="fcd19-128">Each authenticate header contains an available authentication scheme and sometimes a realm.</span></span> <span data-ttu-id="fcd19-129">Il valore dell'area di autenticazione fa distinzione tra maiuscole e minuscole e definisce un set di server o proxy per i quali devono essere accettate le stesse credenziali.</span><span class="sxs-lookup"><span data-stu-id="fcd19-129">The realm value is case-sensitive and defines a set of servers or proxies for which the same credentials should be accepted.</span></span>

<span data-ttu-id="fcd19-130">Sono disponibili due intestazioni denominate "WWW-Authenticate", che indicano che sono supportati più schemi di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="fcd19-130">There are two headers named "WWW-Authenticate", which indicate that multiple authentication schemes are supported.</span></span> <span data-ttu-id="fcd19-131">Se si chiama il metodo [**getResponseHeader**](iwinhttprequest-getresponseheader.md) per trovare le intestazioni "www-Authenticate", il metodo restituisce solo il contenuto della prima intestazione del nome.</span><span class="sxs-lookup"><span data-stu-id="fcd19-131">If you call the [**GetResponseHeader**](iwinhttprequest-getresponseheader.md) method to find "WWW-Authenticate" headers, the method only returns the contents of the first header of that name.</span></span> <span data-ttu-id="fcd19-132">In questo caso, restituisce un valore "NTLM".</span><span class="sxs-lookup"><span data-stu-id="fcd19-132">In this case, it returns a value of "NTLM".</span></span> <span data-ttu-id="fcd19-133">Per assicurarsi che tutte le occorrenze di un'intestazione vengano elaborate, usare invece il metodo [**GetAllResponseHeaders**](iwinhttprequest-getallresponseheaders.md) .</span><span class="sxs-lookup"><span data-stu-id="fcd19-133">To ensure that all occurrences of a header are processed, use the [**GetAllResponseHeaders**](iwinhttprequest-getallresponseheaders.md) method instead.</span></span>

<span data-ttu-id="fcd19-134">La seconda chiamata al metodo richiede la stessa risorsa, ma per prima cosa fornisce le credenziali di autenticazione chiamando il metodo [**Secredentials**](iwinhttprequest-setcredentials.md) .</span><span class="sxs-lookup"><span data-stu-id="fcd19-134">The second method call requests the same resource, but first supplies authentication credentials by calling the [**SetCredentials**](iwinhttprequest-setcredentials.md) method.</span></span> <span data-ttu-id="fcd19-135">Nella sezione seguente del codice viene illustrato come utilizzare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="fcd19-135">The following section of code shows how this method is used.</span></span>


```VB
WinHttpReq.SetCredentials( "User Name", "Password",
                               HTTPREQUEST_SETCREDENTIALS_FOR_SERVER);
```



<span data-ttu-id="fcd19-136">Questo metodo imposta il nome utente su "UserName", la password su "password" e indica che le credenziali di autorizzazione si applicano al server di risorse.</span><span class="sxs-lookup"><span data-stu-id="fcd19-136">This method sets the user name to "UserName", the password to "Password", and indicates that the authorization credentials apply to the resource server.</span></span> <span data-ttu-id="fcd19-137">Le credenziali di autenticazione possono essere inviate anche a un proxy.</span><span class="sxs-lookup"><span data-stu-id="fcd19-137">Authentication credentials can also be sent to a proxy.</span></span>

<span data-ttu-id="fcd19-138">Quando vengono fornite le credenziali, il server restituisce un codice di stato 200 che indica che è possibile recuperare il documento.</span><span class="sxs-lookup"><span data-stu-id="fcd19-138">When credentials are supplied, the server returns a 200 status code that indicates that the document can be retrieved.</span></span>

## <a name="checking-the-status-codes"></a><span data-ttu-id="fcd19-139">Controllo dei codici di stato</span><span class="sxs-lookup"><span data-stu-id="fcd19-139">Checking the Status Codes</span></span>

<span data-ttu-id="fcd19-140">L'esempio precedente è di istruzione, ma richiede che l'utente fornisca esplicitamente le credenziali.</span><span class="sxs-lookup"><span data-stu-id="fcd19-140">The previous example is instructional, but it requires that the user explicitly supply credentials.</span></span> <span data-ttu-id="fcd19-141">Un'applicazione che fornisce le credenziali quando è necessario e non fornisce le credenziali quando non è necessario è più utile.</span><span class="sxs-lookup"><span data-stu-id="fcd19-141">An application that supplies credentials when it is necessary and does not supply credentials when it is not necessary is more useful.</span></span> <span data-ttu-id="fcd19-142">Per implementare una funzionalità che consente di eseguire questa operazione, è necessario modificare l'esempio per esaminare il codice di stato restituito con la risposta.</span><span class="sxs-lookup"><span data-stu-id="fcd19-142">To implement a feature that does this, you must modify your example to examine the status code returned with the response.</span></span>

<span data-ttu-id="fcd19-143">Per un elenco completo dei possibili codici di stato, insieme alle descrizioni, vedere [**codici di stato http**](http-status-codes.md).</span><span class="sxs-lookup"><span data-stu-id="fcd19-143">For a complete list of possible status codes, along with descriptions, see [**HTTP Status Codes**](http-status-codes.md).</span></span> <span data-ttu-id="fcd19-144">Per questo esempio, tuttavia, è necessario trovare solo uno dei tre codici.</span><span class="sxs-lookup"><span data-stu-id="fcd19-144">For this example, however, you should encounter only one of three codes.</span></span> <span data-ttu-id="fcd19-145">Un codice di stato 200 indica che una risorsa è disponibile e viene inviata con la risposta.</span><span class="sxs-lookup"><span data-stu-id="fcd19-145">A status code of 200 indicates that a resource is available and is being sent with the response.</span></span> <span data-ttu-id="fcd19-146">Un codice di stato 401 indica che il server richiede l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="fcd19-146">A status code of 401 indicates that the server requires authentication.</span></span> <span data-ttu-id="fcd19-147">Un codice di stato 407 indica che il proxy richiede l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="fcd19-147">A status code of 407 indicates that the proxy requires authentication.</span></span>

<span data-ttu-id="fcd19-148">Modificare l'esempio creato nell'ultima sezione sostituendo la funzione "getText2" con il codice seguente (sostituire " \[ authenticationSite \] " con il proprio testo per specificare l'URL di un sito che richiede l'autenticazione HTTP):</span><span class="sxs-lookup"><span data-stu-id="fcd19-148">Modify the example you created in the last section by replacing the "getText2" function with the following code (replace "\[authenticationSite\]" with your own text to specifies the URL of a site that requires HTTP authentication):</span></span>


```VB
function getText2() {
  WScript.Echo( "Credentials: " );

  // HttpRequest SetCredentials flags.
  HTTPREQUEST_SETCREDENTIALS_FOR_SERVER = 0;
  HTTPREQUEST_SETCREDENTIALS_FOR_PROXY = 1;

  // Specify the target resource.
  var targURL = "https://[authenticationSite]";
  WinHttpReq.open( "GET", targURL, false );

  var Done = false;
  var Attempts = 0;
  do
  {
    // Keep track of the number of request attempts.
    Attempts++;

    // Send a request to the server and wait for a response.
    WinHttpReq.send( );

    // Obtain the status code from the response.
    var Status = WinHttpReq.Status;

    switch (Status)
    {
      // A 200 status indicates that the resource was retrieved.
      case 200:
        Done = true;
        break;

      // A 401 status indicates that the server 
      // requires authentication.
      case 401:
        WScript.Echo( "Requires Server UserName and Password." );

        // Specify the target resource.
        WinHttpReq.open( "GET", targURL, false );

        // Set credentials for the server.
        WinHttpReq.SetCredentials( "User Name", 
                             "Password",
                              HTTPREQUEST_SETCREDENTIALS_FOR_SERVER);
        break;

      // A 407 status indicates that the proxy 
      // requires authentication.
      case 407:
        WScript.Echo( "Requires Proxy UserName and Password." );

        // Specify the target resource.
        WinHttpReq.open( "GET", targURL, false );

        // Set credentials for the proxy.
        WinHttpReq.SetCredentials( "User Name", 
                              "Password",
                              HTTPREQUEST_SETCREDENTIALS_FOR_PROXY );
        break;
    }
  } while( ( !Done ) && ( Attempts < 3 ) );

  // Display the results of the request.
  WScript.Echo( WinHttpReq.Status + "   " + WinHttpReq.StatusText );
  WScript.Echo( WinHttpReq.GetAllResponseHeaders( ) );
  WScript.Echo( );
};
```



<span data-ttu-id="fcd19-149">Anche in questo caso, salvare ed eseguire il file.</span><span class="sxs-lookup"><span data-stu-id="fcd19-149">Again, save and run the file.</span></span> <span data-ttu-id="fcd19-150">Il secondo metodo recupera comunque il documento, ma fornisce solo le credenziali quando è necessario.</span><span class="sxs-lookup"><span data-stu-id="fcd19-150">The second method still retrieves the document, but it only provides credentials when required.</span></span> <span data-ttu-id="fcd19-151">La funzione "getText2" esegue i metodi [**Open**](iwinhttprequest-open.md) e [**Send**](iwinhttprequest-send.md) come se l'autenticazione non fosse richiesta.</span><span class="sxs-lookup"><span data-stu-id="fcd19-151">The "getText2" function executes the [**Open**](iwinhttprequest-open.md) and [**Send**](iwinhttprequest-send.md) methods as if authentication was not required.</span></span> <span data-ttu-id="fcd19-152">Lo stato viene recuperato con la proprietà [**status**](iwinhttprequest-status.md) e un'istruzione switch risponde al codice di stato risultante.</span><span class="sxs-lookup"><span data-stu-id="fcd19-152">The status is retrieved with the [**Status**](iwinhttprequest-status.md) property and a switch statement responds to the resulting status code.</span></span> <span data-ttu-id="fcd19-153">Se lo stato è 401 (il server richiede l'autenticazione) o 407 (il proxy richiede l'autenticazione), il metodo [**Open**](iwinhttprequest-open.md) viene eseguito nuovamente.</span><span class="sxs-lookup"><span data-stu-id="fcd19-153">If the status is 401 (server requires authentication) or 407 (proxy requires authentication), the [**Open**](iwinhttprequest-open.md) method is executed again.</span></span> <span data-ttu-id="fcd19-154">Questa operazione è seguita dal metodo [**Secredentials**](iwinhttprequest-setcredentials.md) , che imposta il nome utente e la password.</span><span class="sxs-lookup"><span data-stu-id="fcd19-154">This is followed by the [**SetCredentials**](iwinhttprequest-setcredentials.md) method, which sets the user name and password.</span></span> <span data-ttu-id="fcd19-155">Il codice esegue quindi il loopback al metodo [**Send**](iwinhttprequest-send.md) .</span><span class="sxs-lookup"><span data-stu-id="fcd19-155">The code then loops back to the [**Send**](iwinhttprequest-send.md) method.</span></span> <span data-ttu-id="fcd19-156">Se, dopo tre tentativi, la risorsa non può essere recuperata correttamente, la funzione interrompe l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="fcd19-156">If, after three attempts, the resource cannot be successfully retrieved, then the function stops execution.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fcd19-157">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fcd19-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fcd19-158">Autenticazione in WinHTTP</span><span class="sxs-lookup"><span data-stu-id="fcd19-158">Authentication in WinHTTP</span></span>](authentication-in-winhttp.md)
</dt> <dt>

[<span data-ttu-id="fcd19-159">WinHttpRequest</span><span class="sxs-lookup"><span data-stu-id="fcd19-159">WinHttpRequest</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="fcd19-160">**SetCredentials**</span><span class="sxs-lookup"><span data-stu-id="fcd19-160">**SetCredentials**</span></span>](iwinhttprequest-setcredentials.md)
</dt> <dt>

[<span data-ttu-id="fcd19-161">Richiesta di commenti HTTP/1.1 (RFC 2616)</span><span class="sxs-lookup"><span data-stu-id="fcd19-161">HTTP/1.1 Request for Comments (RFC 2616)</span></span>](https://www.ietf.org/rfc/rfc2616.txt)
</dt> </dl>

 

 



