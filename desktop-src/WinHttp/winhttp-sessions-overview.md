---
description: I servizi HTTP di Microsoft Windows (WinHTTP) espongono un set di funzioni C/C++ che consentono all'applicazione di accedere alle risorse HTTP sul Web. Questo argomento fornisce una panoramica del modo in cui queste funzioni vengono usate per interagire con un server HTTP.
ms.assetid: 66a1616b-0cf3-45c7-880b-e36728b5a9c4
title: Cenni preliminari sulle sessioni WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98dc8116dff75f279b87cb5f5ee6af607034176f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129258"
---
# <a name="winhttp-sessions-overview"></a><span data-ttu-id="619aa-104">Cenni preliminari sulle sessioni WinHTTP</span><span class="sxs-lookup"><span data-stu-id="619aa-104">WinHTTP Sessions Overview</span></span>

<span data-ttu-id="619aa-105">I servizi HTTP di Microsoft Windows (WinHTTP) espongono un set di funzioni C/C++ che consentono all'applicazione di accedere alle risorse HTTP sul Web.</span><span class="sxs-lookup"><span data-stu-id="619aa-105">The Microsoft Windows HTTP Services (WinHTTP) exposes a set of C/C++ functions that enable your application to access HTTP resources on the Web.</span></span> <span data-ttu-id="619aa-106">Questo argomento fornisce una panoramica del modo in cui queste funzioni vengono usate per interagire con un server HTTP.</span><span class="sxs-lookup"><span data-stu-id="619aa-106">This topic provides an overview of how these functions are used to interact with an HTTP server.</span></span>

-   [<span data-ttu-id="619aa-107">Uso dell'API WinHTTP per accedere al Web</span><span class="sxs-lookup"><span data-stu-id="619aa-107">Using the WinHTTP API to Access the Web</span></span>](#using-the-winhttp-api-to-access-the-web)
-   [<span data-ttu-id="619aa-108">Inizializzazione di WinHTTP</span><span class="sxs-lookup"><span data-stu-id="619aa-108">Initializing WinHTTP</span></span>](#initializing-winhttp)
-   [<span data-ttu-id="619aa-109">Apertura di una richiesta</span><span class="sxs-lookup"><span data-stu-id="619aa-109">Opening a Request</span></span>](#opening-a-request)
-   [<span data-ttu-id="619aa-110">Aggiunta di intestazioni di richiesta</span><span class="sxs-lookup"><span data-stu-id="619aa-110">Adding Request Headers</span></span>](#adding-request-headers)
-   [<span data-ttu-id="619aa-111">Invio di una richiesta</span><span class="sxs-lookup"><span data-stu-id="619aa-111">Sending a Request</span></span>](#sending-a-request)
-   [<span data-ttu-id="619aa-112">Invio di dati al server</span><span class="sxs-lookup"><span data-stu-id="619aa-112">Posting Data to the Server</span></span>](#posting-data-to-the-server)
-   [<span data-ttu-id="619aa-113">Ottenere informazioni su una richiesta</span><span class="sxs-lookup"><span data-stu-id="619aa-113">Getting Information About a Request</span></span>](#getting-information-about-a-request)
-   [<span data-ttu-id="619aa-114">Download delle risorse dal Web</span><span class="sxs-lookup"><span data-stu-id="619aa-114">Downloading Resources from the Web</span></span>](#downloading-resources-from-the-web)

## <a name="using-the-winhttp-api-to-access-the-web"></a><span data-ttu-id="619aa-115">Uso dell'API WinHTTP per accedere al Web</span><span class="sxs-lookup"><span data-stu-id="619aa-115">Using the WinHTTP API to Access the Web</span></span>

<span data-ttu-id="619aa-116">Il diagramma seguente illustra l'ordine in cui le funzioni WinHTTP vengono in genere chiamate quando si interagisce con un server HTTP.</span><span class="sxs-lookup"><span data-stu-id="619aa-116">The following diagram shows the order in which WinHTTP functions are typically called when interacting with an HTTP server.</span></span> <span data-ttu-id="619aa-117">Le caselle ombreggiate rappresentano le funzioni che generano un handle [HINTERNET](hinternet-handles-in-winhttp.md) , mentre le caselle semplici rappresentano funzioni che usano tali handle.</span><span class="sxs-lookup"><span data-stu-id="619aa-117">The shaded boxes represent functions that generate an [HINTERNET](hinternet-handles-in-winhttp.md) handle, while the plain boxes represent functions that use those handles.</span></span>

![funzioni che creano handle](images/art-winhttp3.png)

## <a name="initializing-winhttp"></a><span data-ttu-id="619aa-119">Inizializzazione di WinHTTP</span><span class="sxs-lookup"><span data-stu-id="619aa-119">Initializing WinHTTP</span></span>

<span data-ttu-id="619aa-120">Prima di interagire con un server, è necessario inizializzare WinHTTP chiamando [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen).</span><span class="sxs-lookup"><span data-stu-id="619aa-120">Before interacting with a server, WinHTTP must be initialized by calling [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen).</span></span> <span data-ttu-id="619aa-121">[**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) crea un contesto di sessione per gestire i dettagli relativi alla sessione HTTP e restituisce un handle di sessione.</span><span class="sxs-lookup"><span data-stu-id="619aa-121">[**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) creates a session context to maintain details about the HTTP session, and returns a session handle.</span></span> <span data-ttu-id="619aa-122">Con questo handle, la funzione [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect) è in grado di specificare un server http di destinazione o Secure HYPERTEXT Transfer Protocol (HTTPS).</span><span class="sxs-lookup"><span data-stu-id="619aa-122">Using this handle, the [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect) function is then able to specify a target HTTP or Secure Hypertext Transfer Protocol (HTTPS) server.</span></span>

> [!Note]  
> <span data-ttu-id="619aa-123">Una chiamata a [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect) non comporta una connessione effettiva al server http fino a quando non viene effettuata una richiesta per una risorsa specifica.</span><span class="sxs-lookup"><span data-stu-id="619aa-123">A call to [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect) does not result in an actual connection to the HTTP server until a request is made for a specific resource.</span></span>

 

## <a name="opening-a-request"></a><span data-ttu-id="619aa-124">Apertura di una richiesta</span><span class="sxs-lookup"><span data-stu-id="619aa-124">Opening a Request</span></span>

<span data-ttu-id="619aa-125">La funzione [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) apre una richiesta HTTP per una determinata risorsa e restituisce un handle [HINTERNET](hinternet-handles-in-winhttp.md) che può essere usato da altre funzioni http.</span><span class="sxs-lookup"><span data-stu-id="619aa-125">The [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) function opens an HTTP request for a particular resource and returns an [HINTERNET](hinternet-handles-in-winhttp.md) handle that can be used by the other HTTP functions.</span></span> <span data-ttu-id="619aa-126">[**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) non invia la richiesta al server quando viene chiamata.</span><span class="sxs-lookup"><span data-stu-id="619aa-126">[**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) does not send the request to the server when called.</span></span> <span data-ttu-id="619aa-127">La funzione [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) stabilisce effettivamente una connessione sulla rete e Invia la richiesta.</span><span class="sxs-lookup"><span data-stu-id="619aa-127">The [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) function actually establishes a connection over the network and sends the request.</span></span>

<span data-ttu-id="619aa-128">Nell'esempio seguente viene illustrata una chiamata di esempio a [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) che utilizza le opzioni predefinite.</span><span class="sxs-lookup"><span data-stu-id="619aa-128">The following example shows a sample call to [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) that uses the default options.</span></span>

`HINTERNET hRequest = WinHttpOpenRequest( hConnect, L"GET", NULL, NULL, NULL, NULL, 0);`

## <a name="adding-request-headers"></a><span data-ttu-id="619aa-129">Aggiunta di intestazioni di richiesta</span><span class="sxs-lookup"><span data-stu-id="619aa-129">Adding Request Headers</span></span>

<span data-ttu-id="619aa-130">La funzione [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) consente a un'applicazione di aggiungere intestazioni di richiesta di formato libero aggiuntive all'handle della richiesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="619aa-130">The [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) function allows an application to append additional free-format request headers to the HTTP request handle.</span></span> <span data-ttu-id="619aa-131">È progettato per l'uso da parte di applicazioni sofisticate che richiedono un controllo preciso sulle richieste inviate al server HTTP.</span><span class="sxs-lookup"><span data-stu-id="619aa-131">It is intended for use by sophisticated applications that require precise control over the requests sent to the HTTP server.</span></span>

<span data-ttu-id="619aa-132">La funzione [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) richiede un handle di richiesta HTTP creato da [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest), una stringa che contiene le intestazioni, la lunghezza delle intestazioni e tutti i modificatori.</span><span class="sxs-lookup"><span data-stu-id="619aa-132">The [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) function requires an HTTP request handle created by [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest), a string that contains the headers, the length of the headers, and any modifiers.</span></span>

<span data-ttu-id="619aa-133">Con [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)è possibile usare i modificatori seguenti.</span><span class="sxs-lookup"><span data-stu-id="619aa-133">The following modifiers can be used with [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders).</span></span>



| <span data-ttu-id="619aa-134">Modificatore</span><span class="sxs-lookup"><span data-stu-id="619aa-134">Modifier</span></span>                                                                                         | <span data-ttu-id="619aa-135">Descrizione</span><span class="sxs-lookup"><span data-stu-id="619aa-135">Description</span></span>                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="619aa-136">**\_aggiunta del \_ flag \_ ADDREQ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="619aa-136">**WINHTTP\_ADDREQ\_FLAG\_ADD**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)                       | <span data-ttu-id="619aa-137">Aggiunge l'intestazione se non esiste.</span><span class="sxs-lookup"><span data-stu-id="619aa-137">Adds the header if it does not exist.</span></span> <span data-ttu-id="619aa-138">Usato con [**il \_ flag ADDREQ di WinHTTP \_ \_ Replace**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders).</span><span class="sxs-lookup"><span data-stu-id="619aa-138">Used with [**WINHTTP\_ADDREQ\_FLAG\_REPLACE**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders).</span></span>                                                                                                                                                                                                               |
| [<span data-ttu-id="619aa-139">**\_flag ADDREQ \_ WinHTTP \_ Aggiungi \_ se \_ nuovo**</span><span class="sxs-lookup"><span data-stu-id="619aa-139">**WINHTTP\_ADDREQ\_FLAG\_ADD\_IF\_NEW**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)              | <span data-ttu-id="619aa-140">Aggiunge l'intestazione solo se non esiste già. in caso contrario, viene restituito un errore.</span><span class="sxs-lookup"><span data-stu-id="619aa-140">Adds the header only if it does not already exist; otherwise, an error is returned.</span></span>                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="619aa-141">**\_ \_ COALESCE flag ADDREQ WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="619aa-141">**WINHTTP\_ADDREQ\_FLAG\_COALESCE**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)                  | <span data-ttu-id="619aa-142">Unisce le intestazioni con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="619aa-142">Merges headers of the same name.</span></span>                                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="619aa-143">**\_flag ADDREQ \_ WinHTTP \_ COALESCE \_ con \_ virgola**</span><span class="sxs-lookup"><span data-stu-id="619aa-143">**WINHTTP\_ADDREQ\_FLAG\_COALESCE\_WITH\_COMMA**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)     | <span data-ttu-id="619aa-144">Unisce le intestazioni con lo stesso nome usando una virgola.</span><span class="sxs-lookup"><span data-stu-id="619aa-144">Merges headers of the same name using a comma.</span></span> <span data-ttu-id="619aa-145">Ad esempio, se si aggiunge "Accept: Text/ \* " seguito da "Accept: audio/ \* " con questo flag, viene formata la singola intestazione "Accept: Text/ \* , audio/ \* ", causando il merge della prima intestazione.</span><span class="sxs-lookup"><span data-stu-id="619aa-145">For example, adding "Accept: text/\*" followed by "Accept: audio/\*" with this flag forms the single header "Accept: text/\*, audio/\*", causing the first header found to be merged.</span></span> <span data-ttu-id="619aa-146">Spetta all'applicazione chiamante garantire uno schema coeso rispetto a intestazioni unite/separate.</span><span class="sxs-lookup"><span data-stu-id="619aa-146">It is up to the calling application to ensure a cohesive scheme with respect to merged/separate headers.</span></span> |
| [<span data-ttu-id="619aa-147">**\_flag ADDREQ \_ WinHTTP \_ COALESCE \_ con \_ punto e virgola**</span><span class="sxs-lookup"><span data-stu-id="619aa-147">**WINHTTP\_ADDREQ\_FLAG\_COALESCE\_WITH\_SEMICOLON**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) | <span data-ttu-id="619aa-148">Unisce le intestazioni con lo stesso nome usando un punto e virgola.</span><span class="sxs-lookup"><span data-stu-id="619aa-148">Merges headers of the same name using a semicolon.</span></span>                                                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="619aa-149">**il \_ flag ADDREQ di WinHTTP \_ \_ sostituisce**</span><span class="sxs-lookup"><span data-stu-id="619aa-149">**WINHTTP\_ADDREQ\_FLAG\_REPLACE**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)                   | <span data-ttu-id="619aa-150">Sostituisce o rimuove un'intestazione.</span><span class="sxs-lookup"><span data-stu-id="619aa-150">Replaces or removes a header.</span></span> <span data-ttu-id="619aa-151">Se il valore dell'intestazione è vuoto e l'intestazione viene trovata, viene rimossa.</span><span class="sxs-lookup"><span data-stu-id="619aa-151">If the header value is empty and the header is found, it is removed.</span></span> <span data-ttu-id="619aa-152">Se il valore dell'intestazione non è vuoto, il valore dell'intestazione viene sostituito.</span><span class="sxs-lookup"><span data-stu-id="619aa-152">If the header value is not empty, the header value is replaced.</span></span>                                                                                                                                                                            |



 

## <a name="sending-a-request"></a><span data-ttu-id="619aa-153">Invio di una richiesta</span><span class="sxs-lookup"><span data-stu-id="619aa-153">Sending a Request</span></span>

<span data-ttu-id="619aa-154">La funzione [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) stabilisce una connessione al server e Invia la richiesta al sito specificato.</span><span class="sxs-lookup"><span data-stu-id="619aa-154">The [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) function establishes a connection to the server and sends the request to the specified site.</span></span> <span data-ttu-id="619aa-155">Questa funzione richiede un handle [HINTERNET](hinternet-handles-in-winhttp.md) creato da [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest).</span><span class="sxs-lookup"><span data-stu-id="619aa-155">This function requires an [HINTERNET](hinternet-handles-in-winhttp.md) handle created by [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest).</span></span> <span data-ttu-id="619aa-156">[**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) può anche inviare intestazioni aggiuntive o informazioni facoltative.</span><span class="sxs-lookup"><span data-stu-id="619aa-156">[**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) can also send additional headers or optional information.</span></span> <span data-ttu-id="619aa-157">Le informazioni facoltative vengono in genere usate per le operazioni che scrivono le informazioni sul server, ad esempio PUT e POST.</span><span class="sxs-lookup"><span data-stu-id="619aa-157">The optional information is generally used for operations that write information to the server, such as PUT and POST.</span></span>

<span data-ttu-id="619aa-158">Dopo che la funzione [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) ha inviato la richiesta, l'applicazione può usare le funzioni [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata) e [**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) sull'handle [HINTERNET](hinternet-handles-in-winhttp.md) per scaricare le risorse del server.</span><span class="sxs-lookup"><span data-stu-id="619aa-158">After the [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) function sends the request, the application can use the [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata) and [**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) functions on the [HINTERNET](hinternet-handles-in-winhttp.md) handle to download the server's resources.</span></span>

## <a name="posting-data-to-the-server"></a><span data-ttu-id="619aa-159">Invio di dati al server</span><span class="sxs-lookup"><span data-stu-id="619aa-159">Posting Data to the Server</span></span>

<span data-ttu-id="619aa-160">Per inserire i dati in un server, il [*verbo http*](glossary.md) nella chiamata a [**WINHTTPOPENREQUEST**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) deve essere post o put.</span><span class="sxs-lookup"><span data-stu-id="619aa-160">To post data to a server, the [*HTTP verb*](glossary.md) in the call to [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) must be either POST or PUT.</span></span> <span data-ttu-id="619aa-161">Quando viene chiamato [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) , il parametro *dwTotalLength* deve essere impostato sulla dimensione dei dati in byte.</span><span class="sxs-lookup"><span data-stu-id="619aa-161">When [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) is called, the *dwTotalLength* parameter should be set to the size of the data in bytes.</span></span> <span data-ttu-id="619aa-162">Usare quindi [**WinHttpWriteData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata) per inviare i dati al server.</span><span class="sxs-lookup"><span data-stu-id="619aa-162">Then use [**WinHttpWriteData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata) to post the data to the server.</span></span>

<span data-ttu-id="619aa-163">In alternativa, impostare il parametro *lpOptional* di [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) sull'indirizzo di un buffer che contiene i dati da inviare al server.</span><span class="sxs-lookup"><span data-stu-id="619aa-163">Alternatively, set the *lpOptional* parameter of [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) to the address of a buffer that contains data to post to the server.</span></span> <span data-ttu-id="619aa-164">Quando si utilizza questa tecnica, è necessario impostare i parametri *dwOptionalLength* e *dwTotalLength* di [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) in modo che siano le dimensioni dei dati inviati.</span><span class="sxs-lookup"><span data-stu-id="619aa-164">When using this technique, you must set both the *dwOptionalLength* and *dwTotalLength* parameters of [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) to be the size of the data being posted.</span></span> <span data-ttu-id="619aa-165">La chiamata di [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) in questo modo Elimina la necessità di chiamare [**WinHttpWriteData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata).</span><span class="sxs-lookup"><span data-stu-id="619aa-165">Calling [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) in this manner eliminates the need to call [**WinHttpWriteData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata).</span></span>

## <a name="getting-information-about-a-request"></a><span data-ttu-id="619aa-166">Ottenere informazioni su una richiesta</span><span class="sxs-lookup"><span data-stu-id="619aa-166">Getting Information About a Request</span></span>

<span data-ttu-id="619aa-167">La funzione [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders) consente a un'applicazione di recuperare informazioni su una richiesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="619aa-167">The [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders) function allows an application to retrieve information about an HTTP request.</span></span> <span data-ttu-id="619aa-168">La funzione richiede un handle [HINTERNET](hinternet-handles-in-winhttp.md) creato da [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest), un valore del livello di informazioni e una lunghezza del buffer.</span><span class="sxs-lookup"><span data-stu-id="619aa-168">The function requires an [HINTERNET](hinternet-handles-in-winhttp.md) handle created by [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest), an information level value, and a buffer length.</span></span> <span data-ttu-id="619aa-169">[**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders) accetta anche un buffer che archivia le informazioni e un indice in base zero dell'intestazione che enumera più intestazioni con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="619aa-169">[**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders) also accepts a buffer that stores the information and a zero-based header index that enumerates multiple headers with the same name.</span></span>

<span data-ttu-id="619aa-170">Usare uno dei valori del livello informazioni disponibili nella pagina [**flag informazioni query**](query-info-flags.md) con un modificatore per controllare il formato in cui le informazioni vengono archiviate nel parametro *lpvBuffer* di [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders).</span><span class="sxs-lookup"><span data-stu-id="619aa-170">Use any of the information level values found on the [**Query Info Flags**](query-info-flags.md) page with a modifier to control the format in which the information is stored in the *lpvBuffer* parameter of [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders).</span></span>

## <a name="downloading-resources-from-the-web"></a><span data-ttu-id="619aa-171">Download delle risorse dal Web</span><span class="sxs-lookup"><span data-stu-id="619aa-171">Downloading Resources from the Web</span></span>

<span data-ttu-id="619aa-172">Dopo l'apertura di una richiesta con la funzione [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) , l'invio al server con [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)e la preparazione dell'handle di richiesta per ricevere una risposta con [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse), l'applicazione può usare le funzioni [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata) e [**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) per scaricare la risorsa dal server http.</span><span class="sxs-lookup"><span data-stu-id="619aa-172">After opening a request with the [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) function, sending it to the server with [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest), and preparing the request handle to receive a response with [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse), the application can use the [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata) and [**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) functions to download the resource from the HTTP server.</span></span>

<span data-ttu-id="619aa-173">Il codice di esempio seguente illustra come scaricare una risorsa con la semantica di transazione sicura.</span><span class="sxs-lookup"><span data-stu-id="619aa-173">The following sample code shows how to download a resource with secure transaction semantics.</span></span> <span data-ttu-id="619aa-174">Il codice di esempio Inizializza l'Application Programming Interface WinHTTP (API), seleziona un server HTTPS di destinazione e quindi apre e invia una richiesta per la risorsa protetta.</span><span class="sxs-lookup"><span data-stu-id="619aa-174">The sample code initializes the WinHTTP application programming interface (API), selects a target HTTPS server, and then opens and sends a request for this secure resource.</span></span> <span data-ttu-id="619aa-175">[**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) viene usato con l'handle della richiesta per determinare la quantità di dati disponibili per il download e quindi [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata) viene usato per leggere i dati.</span><span class="sxs-lookup"><span data-stu-id="619aa-175">[**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) is used with the request handle to determine how much data is available for download, and then [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata) is used to read that data.</span></span> <span data-ttu-id="619aa-176">Questo processo viene ripetuto fino a quando non viene recuperato e visualizzato l'intero documento.</span><span class="sxs-lookup"><span data-stu-id="619aa-176">This process is repeated until the entire document has been retrieved and displayed.</span></span>


```C++
  DWORD dwSize = 0;
  DWORD dwDownloaded = 0;
  LPSTR pszOutBuffer;
  BOOL  bResults = FALSE;
  HINTERNET  hSession = NULL, 
             hConnect = NULL,
             hRequest = NULL;

  // Use WinHttpOpen to obtain a session handle.
  hSession = WinHttpOpen( L"WinHTTP Example/1.0",  
                          WINHTTP_ACCESS_TYPE_DEFAULT_PROXY,
                          WINHTTP_NO_PROXY_NAME, 
                          WINHTTP_NO_PROXY_BYPASS, 0 );

  // Specify an HTTP server.
  if( hSession )
    hConnect = WinHttpConnect( hSession, L"www.microsoft.com",
                               INTERNET_DEFAULT_HTTPS_PORT, 0 );

  // Create an HTTP request handle.
  if( hConnect )
    hRequest = WinHttpOpenRequest( hConnect, L"GET", NULL,
                                   NULL, WINHTTP_NO_REFERER, 
                                   WINHTTP_DEFAULT_ACCEPT_TYPES, 
                                   WINHTTP_FLAG_SECURE );

  // Send a request.
  if( hRequest )
    bResults = WinHttpSendRequest( hRequest,
                                   WINHTTP_NO_ADDITIONAL_HEADERS, 0,
                                   WINHTTP_NO_REQUEST_DATA, 0, 
                                   0, 0 );


  // End the request.
  if( bResults )
    bResults = WinHttpReceiveResponse( hRequest, NULL );

  // Keep checking for data until there is nothing left.
  if( bResults )
  {
    do 
    {
      // Check for available data.
      dwSize = 0;
      if( !WinHttpQueryDataAvailable( hRequest, &dwSize ) )
        printf( "Error %u in WinHttpQueryDataAvailable.\n",
                GetLastError( ) );

      // Allocate space for the buffer.
      pszOutBuffer = new char[dwSize+1];
      if( !pszOutBuffer )
      {
        printf( "Out of memory\n" );
        dwSize=0;
      }
      else
      {
        // Read the data.
        ZeroMemory( pszOutBuffer, dwSize+1 );

        if( !WinHttpReadData( hRequest, (LPVOID)pszOutBuffer, 
                              dwSize, &dwDownloaded ) )
          printf( "Error %u in WinHttpReadData.\n", GetLastError( ) );
        else
          printf( "%s", pszOutBuffer );

        // Free the memory allocated to the buffer.
        delete [] pszOutBuffer;
      }
    } while( dwSize > 0 );
  }


  // Report any errors.
  if( !bResults )
    printf( "Error %d has occurred.\n", GetLastError( ) );

  // Close any open handles.
  if( hRequest ) WinHttpCloseHandle( hRequest );
  if( hConnect ) WinHttpCloseHandle( hConnect );
  if( hSession ) WinHttpCloseHandle( hSession );
```



 

 



