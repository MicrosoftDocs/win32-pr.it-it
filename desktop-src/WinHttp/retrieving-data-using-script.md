---
description: Questo argomento include un esempio di come scrivere uno script che ottiene i dati tramite i servizi HTTP di Microsoft Windows (WinHTTP) in modo sincrono o asincrono.
ms.assetid: 84b847f8-4d9e-4fea-9e87-df4c65b54a02
title: Recupero di dati tramite script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 734516cf75f92cc43ab4cb15f22bd97aa803ec33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966421"
---
# <a name="retrieving-data-using-script"></a><span data-ttu-id="900dd-103">Recupero di dati tramite script</span><span class="sxs-lookup"><span data-stu-id="900dd-103">Retrieving Data Using Script</span></span>

<span data-ttu-id="900dd-104">Questo argomento include un esempio di come scrivere uno script che ottiene i dati tramite i servizi HTTP di Microsoft Windows (WinHTTP) in modo sincrono o asincrono.</span><span class="sxs-lookup"><span data-stu-id="900dd-104">This topic includes an example of how to write a script that obtains data through Microsoft Windows HTTP Services (WinHTTP) either synchronously or asynchronously.</span></span> <span data-ttu-id="900dd-105">I concetti illustrati in questo esempio rappresentano la base per la scrittura di applicazioni server client o di livello intermedio che richiedono l'accesso ai dati tramite il protocollo HTTP.</span><span class="sxs-lookup"><span data-stu-id="900dd-105">The concepts demonstrated in this example provide the basis for writing client or middle-tier server applications that require access to data using the HTTP protocol.</span></span>

-   [<span data-ttu-id="900dd-106">Prerequisiti e requisiti</span><span class="sxs-lookup"><span data-stu-id="900dd-106">Prerequisites and Requirements</span></span>](#prerequisites-and-requirements)
-   [<span data-ttu-id="900dd-107">Recupero dei dati in modo sincrono</span><span class="sxs-lookup"><span data-stu-id="900dd-107">Retrieving Data Synchronously</span></span>](#retrieving-data-synchronously)
-   [<span data-ttu-id="900dd-108">Recupero dei dati in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="900dd-108">Retrieving Data Asynchronously</span></span>](#retrieving-data-asynchronously)
-   [<span data-ttu-id="900dd-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="900dd-109">Related topics</span></span>](#related-topics)

## <a name="prerequisites-and-requirements"></a><span data-ttu-id="900dd-110">Prerequisiti e requisiti</span><span class="sxs-lookup"><span data-stu-id="900dd-110">Prerequisites and Requirements</span></span>

<span data-ttu-id="900dd-111">Oltre a una conoscenza approfondita di Microsoft JScript, questo esempio richiede quanto segue:</span><span class="sxs-lookup"><span data-stu-id="900dd-111">In addition to a working knowledge of Microsoft JScript, this example requires the following:</span></span>

-   <span data-ttu-id="900dd-112">Versione corrente del Software Development Kit (SDK) di Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="900dd-112">The current version of the Microsoft Windows Software Development Kit (SDK).</span></span>
-   <span data-ttu-id="900dd-113">Lo strumento di configurazione proxy per stabilire le impostazioni proxy per i servizi HTTP di Microsoft Windows (WinHTTP), se la connessione a Internet avviene tramite un server proxy.</span><span class="sxs-lookup"><span data-stu-id="900dd-113">The proxy configuration tool to establish the proxy settings for Microsoft Windows HTTP Services (WinHTTP), if your connection to the Internet is through a proxy server.</span></span> <span data-ttu-id="900dd-114">Per ulteriori informazioni, vedere [ProxyCfg.exe, uno strumento di configurazione proxy](proxycfg-exe--a-proxy-configuration-tool.md).</span><span class="sxs-lookup"><span data-stu-id="900dd-114">For more information, see [ProxyCfg.exe, a Proxy Configuration Tool](proxycfg-exe--a-proxy-configuration-tool.md).</span></span>
-   <span data-ttu-id="900dd-115">Una certa familiarità con i concetti e la [terminologia di rete](network-terminology.md) .</span><span class="sxs-lookup"><span data-stu-id="900dd-115">A familiarity with [network terminology](network-terminology.md) and concepts.</span></span>

## <a name="retrieving-data-synchronously"></a><span data-ttu-id="900dd-116">Recupero dei dati in modo sincrono</span><span class="sxs-lookup"><span data-stu-id="900dd-116">Retrieving Data Synchronously</span></span>

<span data-ttu-id="900dd-117">**Per creare uno script che ottenga il testo da una pagina Web in modo sincrono, eseguire le operazioni seguenti:**</span><span class="sxs-lookup"><span data-stu-id="900dd-117">**To create a script that obtains the text from a Web page synchronously, do the following:**</span></span>

1.  <span data-ttu-id="900dd-118">Aprire un editor di testo.</span><span class="sxs-lookup"><span data-stu-id="900dd-118">Open a text editor.</span></span>
2.  <span data-ttu-id="900dd-119">Copiare il codice seguente nell'editor di testo.</span><span class="sxs-lookup"><span data-stu-id="900dd-119">Copy the following code into the text editor.</span></span>

    ```JScript
    function getText(strURL)
    {
        var strResult;
        
        try
        {
            // Create the WinHTTPRequest ActiveX Object.
            var WinHttpReq = new ActiveXObject(
                                      "WinHttp.WinHttpRequest.5.1");
            
            //  Create an HTTP request.
            var temp = WinHttpReq.Open("GET", strURL, false);

            //  Send the HTTP request.
            WinHttpReq.Send();
            
            //  Retrieve the response text.
            strResult = WinHttpReq.ResponseText;
        }
        catch (objError)
        {
            strResult = objError + "\n"
            strResult += "WinHTTP returned error: " + 
                (objError.number & 0xFFFF).toString() + "\n\n";
            strResult += objError.description;
        }
        
        //  Return the response text.
        return strResult;
    }

    WScript.Echo(getText("https://www.microsoft.com/default.htm"));
    ```

    

3.  <span data-ttu-id="900dd-120">Salvare il file con il nome "Retrieve.js".</span><span class="sxs-lookup"><span data-stu-id="900dd-120">Save the file as "Retrieve.js".</span></span>
4.  <span data-ttu-id="900dd-121">Al prompt dei comandi digitare "cscript Retrieve.js" e premere INVIO.</span><span class="sxs-lookup"><span data-stu-id="900dd-121">From a command prompt, type "cscript Retrieve.js" and press ENTER.</span></span>

<span data-ttu-id="900dd-122">A questo punto si dispone di uno script che usa un oggetto [**WinHttpRequest**](winhttprequest.md) per ottenere il codice sorgente HTML per la pagina Web in https://www.microsoft.com .</span><span class="sxs-lookup"><span data-stu-id="900dd-122">You now have a script that uses a [**WinHttpRequest**](winhttprequest.md) object to obtain the HTML source code for the Web page at https://www.microsoft.com.</span></span> <span data-ttu-id="900dd-123">Potrebbe essere necessario attendere alcuni secondi prima che il codice venga visualizzato.</span><span class="sxs-lookup"><span data-stu-id="900dd-123">You might have to wait several seconds for the code to appear.</span></span>

<span data-ttu-id="900dd-124">L'applicazione contiene una sola funzione, "gettext".</span><span class="sxs-lookup"><span data-stu-id="900dd-124">The application contains only one function, "getText".</span></span> <span data-ttu-id="900dd-125">La prima riga dello script crea l'oggetto [**WinHttpRequest**](winhttprequest.md) .</span><span class="sxs-lookup"><span data-stu-id="900dd-125">The first line of the script creates the [**WinHttpRequest**](winhttprequest.md) object.</span></span>


```JScript
    // Create the WinHTTPRequest ActiveX Object.
    var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");
```



<span data-ttu-id="900dd-126">Quando il motore JScript rileva questa riga, crea un'istanza di questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="900dd-126">When the JScript engine encounters this line, it creates an instance of this object.</span></span> <span data-ttu-id="900dd-127">Se viene visualizzato il messaggio di errore "componente ActiveX non è in grado di creare l'oggetto", in questa riga, probabilmente il WinHttp.dll non è stato registrato correttamente o non è presente nel sistema.</span><span class="sxs-lookup"><span data-stu-id="900dd-127">If you get the error message, "ActiveX component can't create object", on this line, most likely the WinHttp.dll was not properly registered or is not present on the system.</span></span>

<span data-ttu-id="900dd-128">La riga successiva dello script chiama il metodo [**Open**](iwinhttprequest-open.md) .</span><span class="sxs-lookup"><span data-stu-id="900dd-128">The next line of the script calls the [**Open**](iwinhttprequest-open.md) method.</span></span>


```JScript
    //  Create an HTTP request.
    WinHttpReq.Open("GET", "https://www.microsoft.com", false);
```



<span data-ttu-id="900dd-129">Tre parametri specificano il [*verbo http*](glossary.md) da usare, il nome della risorsa e se usare WinHTTP in modo sincrono o asincrono.</span><span class="sxs-lookup"><span data-stu-id="900dd-129">Three parameters specify which [*HTTP verb*](glossary.md) to use, the name of the resource, and whether to use WinHTTP synchronously or asynchronously.</span></span> <span data-ttu-id="900dd-130">In questo esempio, il metodo usa il *verbo http*"Get" per ottenere i dati da https://www.microsoft.com .</span><span class="sxs-lookup"><span data-stu-id="900dd-130">In this example, the method is using the *HTTP verb*"GET" to obtain data from https://www.microsoft.com.</span></span> <span data-ttu-id="900dd-131">Se si specifica **false** per l'ultimo parametro, viene determinato che la transazione viene eseguita in modo sincrono.</span><span class="sxs-lookup"><span data-stu-id="900dd-131">Specifying **FALSE** for the last parameter determines that the transaction occurs synchronously.</span></span> <span data-ttu-id="900dd-132">Il metodo [**Open**](iwinhttprequest-open.md) non stabilisce una connessione alla risorsa come potrebbe implicare il nome.</span><span class="sxs-lookup"><span data-stu-id="900dd-132">The [**Open**](iwinhttprequest-open.md) method does not establish a connection to the resource as the name might imply.</span></span> <span data-ttu-id="900dd-133">Ma Inizializza le strutture di dati interne che conservano le informazioni sulla sessione, sulla connessione e sulla richiesta.</span><span class="sxs-lookup"><span data-stu-id="900dd-133">Rather, it initializes the internal data structures that maintain information about the session, connection, and request.</span></span>

<span data-ttu-id="900dd-134">Il metodo [**Send**](iwinhttprequest-send.md) assembla le intestazioni della richiesta e Invia la richiesta.</span><span class="sxs-lookup"><span data-stu-id="900dd-134">The [**Send**](iwinhttprequest-send.md) method assembles the request headers and sends the request.</span></span> <span data-ttu-id="900dd-135">Quando viene chiamato in modalità sincrona, il metodo [**Send**](iwinhttprequest-send.md) attende anche una risposta prima di consentire all'applicazione di continuare.</span><span class="sxs-lookup"><span data-stu-id="900dd-135">When called in synchronous mode, the [**Send**](iwinhttprequest-send.md) method also waits for a response before allowing the application to continue.</span></span>


```JScript
    // Send the HTTP request.
    WinHttpReq.Send();
```



<span data-ttu-id="900dd-136">Dopo l'invio della richiesta, lo script restituisce il valore della proprietà [**ResponseText**](iwinhttprequest-responsetext.md) dell'oggetto [**WinHttpRequest**](winhttprequest.md) .</span><span class="sxs-lookup"><span data-stu-id="900dd-136">After sending the request, the script returns the value of the [**ResponseText**](iwinhttprequest-responsetext.md) property of the [**WinHttpRequest**](winhttprequest.md) object.</span></span> <span data-ttu-id="900dd-137">Questa proprietà contiene il corpo dell'entità della risposta, in questo caso, l'origine di un documento.</span><span class="sxs-lookup"><span data-stu-id="900dd-137">This property contains the entity body of the response, in this case, the source of a document.</span></span>


```JScript
    // Get the response text.
    return WinHttpReq.ResponseText;
```



<span data-ttu-id="900dd-138">L'esecuzione dello script viene sospesa mentre viene recuperato l'intero testo della risorsa.</span><span class="sxs-lookup"><span data-stu-id="900dd-138">Execution of the script pauses while the entire text of the resource is retrieved.</span></span> <span data-ttu-id="900dd-139">Il testo della risorsa viene restituito dalla funzione e visualizzato.</span><span class="sxs-lookup"><span data-stu-id="900dd-139">The resource text is returned from the function and displayed.</span></span>

<span data-ttu-id="900dd-140">L'oggetto [**WinHttpRequest**](winhttprequest.md) garantisce che tutte le risorse interne allocate per la transazione HTTP vengano rilasciate.</span><span class="sxs-lookup"><span data-stu-id="900dd-140">The [**WinHttpRequest**](winhttprequest.md) object ensures that any internal resources that are allocated for the HTTP transaction are released.</span></span>

## <a name="retrieving-data-asynchronously"></a><span data-ttu-id="900dd-141">Recupero dei dati in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="900dd-141">Retrieving Data Asynchronously</span></span>

<span data-ttu-id="900dd-142">Il recupero dei dati in modo asincrono tramite WinHTTP è molto simile al recupero sincrono dei dati.</span><span class="sxs-lookup"><span data-stu-id="900dd-142">Retrieving data asynchronously using WinHTTP is very similar to retrieving data synchronously.</span></span> <span data-ttu-id="900dd-143">Modificare lo script della sezione precedente facendo due piccole modifiche.</span><span class="sxs-lookup"><span data-stu-id="900dd-143">Modify the script from the previous section by making two small changes.</span></span>

1.  <span data-ttu-id="900dd-144">Impostare il terzo parametro del metodo [**Open**](iwinhttprequest-open.md) su "true" invece di "false" per specificare che i metodi WinHTTP devono essere eseguiti in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="900dd-144">Set the third parameter of the [**Open**](iwinhttprequest-open.md) method to "true" instead of "false" to specify that WinHTTP methods should be performed asynchronously.</span></span>
    ```JScript
       //  Create a HTTP request.
        var temp = WinHttpReq.Open("GET", strURL, true);
    ```

    

2.  <span data-ttu-id="900dd-145">Richiamare il metodo [**waitForResponse**](iwinhttprequest-waitforresponse.md) prima di accedere alla proprietà [**ResponseText**](iwinhttprequest-responsetext.md) per assicurarsi che sia stata ricevuta l'intera risposta.</span><span class="sxs-lookup"><span data-stu-id="900dd-145">Invoke the [**WaitForResponse**](iwinhttprequest-waitforresponse.md) method before accessing the [**ResponseText**](iwinhttprequest-responsetext.md) property to ensure that the entire response has been received.</span></span>
    ```JScript
        //  Send the HTTP request.
        WinHttpReq.Send();
            
        // Wait for the entire response.
        WinHttpReq.WaitForResponse();
            
        //  Retrieve the response text.
        strResult = WinHttpReq.ResponseText;
    ```

    

<span data-ttu-id="900dd-146">Il vantaggio principale dell'uso di WinHTTP in modo asincrono nello script è che il metodo [**Send**](iwinhttprequest-send.md) restituisce immediatamente un risultato.</span><span class="sxs-lookup"><span data-stu-id="900dd-146">The main advantage to using WinHTTP asynchronously in script is that the [**Send**](iwinhttprequest-send.md) method returns immediately.</span></span> <span data-ttu-id="900dd-147">La richiesta viene preparata e inviata da un thread di lavoro.</span><span class="sxs-lookup"><span data-stu-id="900dd-147">The request is prepared and sent by a worker thread.</span></span> <span data-ttu-id="900dd-148">Ciò consente all'applicazione di eseguire altre operazioni mentre è in attesa della risposta.</span><span class="sxs-lookup"><span data-stu-id="900dd-148">This enables your application to do other things while it is waiting for the response.</span></span> <span data-ttu-id="900dd-149">Prima di tentare di accedere alla risposta, verificare che l'intera risposta sia stata ricevuta chiamando il metodo [**waitForResponse**](iwinhttprequest-waitforresponse.md) .</span><span class="sxs-lookup"><span data-stu-id="900dd-149">Before attempting to access the response, ensure that the entire response has been received by calling the [**WaitForResponse**](iwinhttprequest-waitforresponse.md) method.</span></span> <span data-ttu-id="900dd-150">In caso contrario, può verificarsi un errore.</span><span class="sxs-lookup"><span data-stu-id="900dd-150">Otherwise an error can occur.</span></span>

<span data-ttu-id="900dd-151">Il metodo [**waitForResponse**](iwinhttprequest-waitforresponse.md) può essere utilizzato anche per specificare un valore di timeout per la transazione.</span><span class="sxs-lookup"><span data-stu-id="900dd-151">The [**WaitForResponse**](iwinhttprequest-waitforresponse.md) method can also be used to specify a time-out value for the transaction.</span></span> <span data-ttu-id="900dd-152">Un parametro facoltativo consente di specificare il valore di timeout in secondi.</span><span class="sxs-lookup"><span data-stu-id="900dd-152">An optional parameter enables you to specify the time-out value in seconds.</span></span>

## <a name="related-topics"></a><span data-ttu-id="900dd-153">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="900dd-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="900dd-154">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="900dd-154">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="900dd-155">Richiesta di commenti HTTP/1.1 (RFC 2616)</span><span class="sxs-lookup"><span data-stu-id="900dd-155">HTTP/1.1 Request for Comments (RFC 2616)</span></span>](https://www.ietf.org/rfc/rfc2616.txt)
</dt> </dl>

 

 



