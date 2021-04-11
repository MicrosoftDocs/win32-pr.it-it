---
title: Sessioni HTTP
description: È possibile accedere alle risorse nel sito Web tramite http.
ms.assetid: 0f307e28-9c38-41e7-9795-7eef08e99a3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85b0b4d30bc86c588495a55ed4867a4084c43a09
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104117975"
---
# <a name="http-sessions"></a><span data-ttu-id="726fd-103">Sessioni HTTP</span><span class="sxs-lookup"><span data-stu-id="726fd-103">HTTP Sessions</span></span>

<span data-ttu-id="726fd-104">WinINet consente di accedere alle risorse nel World Wide Web (WWW).</span><span class="sxs-lookup"><span data-stu-id="726fd-104">WinINet enables you to access resources on the World Wide Web (WWW).</span></span> <span data-ttu-id="726fd-105">È possibile accedere a queste risorse direttamente usando [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) . per altre informazioni, vedere [accesso diretto agli URL](handling-uniform-resource-locators.md).</span><span class="sxs-lookup"><span data-stu-id="726fd-105">These resources can be accessed directly by using [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (for more information, see [Accessing URLs Directly](handling-uniform-resource-locators.md)).</span></span>

<span data-ttu-id="726fd-106">È possibile accedere alle risorse nel sito Web tramite http.</span><span class="sxs-lookup"><span data-stu-id="726fd-106">Resources on the WWW are accessed by using http.</span></span> <span data-ttu-id="726fd-107">Le funzioni HTTP gestiscono i protocolli sottostanti, consentendo allo stesso tempo all'applicazione di accedere alle informazioni sul sito Web.</span><span class="sxs-lookup"><span data-stu-id="726fd-107">The HTTP functions handle the underlying protocols, while allowing your application to access information on the WWW.</span></span> <span data-ttu-id="726fd-108">Con l'evolversi del protocollo HTTP, i protocolli sottostanti vengono aggiornati per mantenere il comportamento della funzione.</span><span class="sxs-lookup"><span data-stu-id="726fd-108">As the HTTP protocol evolves, the underlying protocols are updated to maintain function behavior.</span></span>

<span data-ttu-id="726fd-109">Nel diagramma seguente vengono illustrate le relazioni delle funzioni utilizzate con il protocollo HTTP.</span><span class="sxs-lookup"><span data-stu-id="726fd-109">The following diagram shows the relationships of the functions that are used with the HTTP protocol.</span></span> <span data-ttu-id="726fd-110">Le caselle ombreggiate rappresentano funzioni che restituiscono handle [**HINTERNET**](appendix-a-hinternet-handles.md) , mentre le caselle semplici rappresentano funzioni che usano l'handle **HINTERNET** creato dalla funzione da cui dipendono.</span><span class="sxs-lookup"><span data-stu-id="726fd-110">The shaded boxes represent functions that return [**HINTERNET**](appendix-a-hinternet-handles.md) handles, while the plain boxes represent functions that use the **HINTERNET** handle created by the function on which they depend.</span></span>

![funzioni WinInet usate per http](images/ax-wnt05.png)

<span data-ttu-id="726fd-112">Per altre informazioni, vedere [handle hInternet](appendix-a-hinternet-handles.md).</span><span class="sxs-lookup"><span data-stu-id="726fd-112">For more information, see [HINTERNET Handles](appendix-a-hinternet-handles.md).</span></span>

## <a name="using-the-wininet-functions-to-access-the-www"></a><span data-ttu-id="726fd-113">Uso delle funzioni WinINet per accedere al sito Web</span><span class="sxs-lookup"><span data-stu-id="726fd-113">Using the WinINet Functions to Access the WWW</span></span>

-   [<span data-ttu-id="726fd-114">Avvio di una connessione a WWW</span><span class="sxs-lookup"><span data-stu-id="726fd-114">Initiating a Connection to the WWW</span></span>](#initiating-a-connection-to-the-www)
-   [<span data-ttu-id="726fd-115">Apertura di una richiesta</span><span class="sxs-lookup"><span data-stu-id="726fd-115">Opening a Request</span></span>](#opening-a-request)
-   [<span data-ttu-id="726fd-116">Aggiunta di intestazioni di richiesta</span><span class="sxs-lookup"><span data-stu-id="726fd-116">Adding Request Headers</span></span>](#adding-request-headers)
-   [<span data-ttu-id="726fd-117">Invio di una richiesta</span><span class="sxs-lookup"><span data-stu-id="726fd-117">Sending a Request</span></span>](#sending-a-request)
-   [<span data-ttu-id="726fd-118">Invio di dati al server</span><span class="sxs-lookup"><span data-stu-id="726fd-118">Posting Data to the Server</span></span>](#posting-data-to-the-server)
-   [<span data-ttu-id="726fd-119">Ottenere informazioni su una richiesta</span><span class="sxs-lookup"><span data-stu-id="726fd-119">Getting Information About a Request</span></span>](#getting-information-about-a-request)
-   [<span data-ttu-id="726fd-120">Download delle risorse dal sito Web</span><span class="sxs-lookup"><span data-stu-id="726fd-120">Downloading Resources from the WWW</span></span>](#downloading-resources-from-the-www)

<span data-ttu-id="726fd-121">Le funzioni seguenti vengono usate durante le sessioni HTTP per accedere a WWW.</span><span class="sxs-lookup"><span data-stu-id="726fd-121">The following functions are used during HTTP sessions to access the WWW.</span></span>



| <span data-ttu-id="726fd-122">Funzione</span><span class="sxs-lookup"><span data-stu-id="726fd-122">Function</span></span>                                               | <span data-ttu-id="726fd-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="726fd-123">Description</span></span>                                                                                                                                                                                  |
|--------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="726fd-124">**HttpAddRequestHeaders**</span><span class="sxs-lookup"><span data-stu-id="726fd-124">**HttpAddRequestHeaders**</span></span>](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa) | <span data-ttu-id="726fd-125">Aggiunge intestazioni di richiesta HTTP all'handle della richiesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="726fd-125">Adds HTTP request headers to the HTTP request handle.</span></span> <span data-ttu-id="726fd-126">Questa funzione richiede un handle creato da [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span><span class="sxs-lookup"><span data-stu-id="726fd-126">This function requires a handle created by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span>                                                 |
| [<span data-ttu-id="726fd-127">**HttpOpenRequest**</span><span class="sxs-lookup"><span data-stu-id="726fd-127">**HttpOpenRequest**</span></span>](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)             | <span data-ttu-id="726fd-128">Apre un handle di richiesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="726fd-128">Opens an HTTP request handle.</span></span> <span data-ttu-id="726fd-129">Questa funzione richiede un handle creato da [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="726fd-129">This function requires a handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span>                                                                         |
| [<span data-ttu-id="726fd-130">**HttpQueryInfo**</span><span class="sxs-lookup"><span data-stu-id="726fd-130">**HttpQueryInfo**</span></span>](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa)                 | <span data-ttu-id="726fd-131">Esegue una query sulle informazioni relative a una richiesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="726fd-131">Queries information about an HTTP request.</span></span> <span data-ttu-id="726fd-132">Questa funzione richiede un handle creato dalla funzione [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) o [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) .</span><span class="sxs-lookup"><span data-stu-id="726fd-132">This function requires a handle created by the [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) or [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) function.</span></span> |
| [<span data-ttu-id="726fd-133">**HttpSendRequest**</span><span class="sxs-lookup"><span data-stu-id="726fd-133">**HttpSendRequest**</span></span>](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)             | <span data-ttu-id="726fd-134">Invia la richiesta HTTP specificata al server HTTP.</span><span class="sxs-lookup"><span data-stu-id="726fd-134">Sends the specified HTTP request to the HTTP server.</span></span> <span data-ttu-id="726fd-135">Questa funzione richiede un handle creato da [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span><span class="sxs-lookup"><span data-stu-id="726fd-135">This function requires a handle created by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span>                                                  |
| [<span data-ttu-id="726fd-136">**InternetErrorDlg**</span><span class="sxs-lookup"><span data-stu-id="726fd-136">**InternetErrorDlg**</span></span>](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg)           | <span data-ttu-id="726fd-137">Consente di visualizzare le finestre di dialogo predefinite per le condizioni di errore Internet comuni.</span><span class="sxs-lookup"><span data-stu-id="726fd-137">Displays predefined dialog boxes for common Internet error conditions.</span></span> <span data-ttu-id="726fd-138">Questa funzione richiede l'handle usato nella chiamata a [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span><span class="sxs-lookup"><span data-stu-id="726fd-138">This function requires the handle used in the call to [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span></span>                     |



 

### <a name="initiating-a-connection-to-the-www"></a><span data-ttu-id="726fd-139">Avvio di una connessione a WWW</span><span class="sxs-lookup"><span data-stu-id="726fd-139">Initiating a Connection to the WWW</span></span>

<span data-ttu-id="726fd-140">Per avviare una connessione a WWW, l'applicazione deve chiamare la funzione [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) sulla [**HINTERNET**](appendix-a-hinternet-handles.md) radice restituita da [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span><span class="sxs-lookup"><span data-stu-id="726fd-140">To start a connection to the WWW, the application must call the [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) function on the root [**HINTERNET**](appendix-a-hinternet-handles.md) returned by [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span></span> <span data-ttu-id="726fd-141">[**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) deve stabilire una sessione HTTP dichiarando il \_ tipo di \_ servizio http del servizio Internet.</span><span class="sxs-lookup"><span data-stu-id="726fd-141">[**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) must establish an HTTP session by declaring the INTERNET\_SERVICE\_HTTP service type.</span></span> <span data-ttu-id="726fd-142">Per altre informazioni sull'uso di [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta), vedere [uso di InternetConnect](enabling-internet-functionality.md).</span><span class="sxs-lookup"><span data-stu-id="726fd-142">For more information on using [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta), see [Using InternetConnect](enabling-internet-functionality.md).</span></span>

### <a name="opening-a-request"></a><span data-ttu-id="726fd-143">Apertura di una richiesta</span><span class="sxs-lookup"><span data-stu-id="726fd-143">Opening a Request</span></span>

<span data-ttu-id="726fd-144">La funzione [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) apre una richiesta HTTP e restituisce un handle [**HINTERNET**](appendix-a-hinternet-handles.md) che può essere usato da altre funzioni http.</span><span class="sxs-lookup"><span data-stu-id="726fd-144">The [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) function opens an HTTP request and returns an [**HINTERNET**](appendix-a-hinternet-handles.md) handle that can be used by the other HTTP functions.</span></span> <span data-ttu-id="726fd-145">Diversamente dalle altre funzioni aperte, ad esempio [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) non invia la richiesta a Internet quando viene chiamata.</span><span class="sxs-lookup"><span data-stu-id="726fd-145">Unlike the other open functions (such as [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) does not send the request to the Internet when called.</span></span> <span data-ttu-id="726fd-146">La funzione [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) Invia la richiesta e stabilisce una connessione sulla rete.</span><span class="sxs-lookup"><span data-stu-id="726fd-146">The [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) function sends the request and establishes a connection over the network.</span></span>

<span data-ttu-id="726fd-147">[**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) accetta un handle di sessione HTTP creato da [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) e un verbo HTTP, un nome di oggetto, una stringa di versione, un referrer, i tipi Accept, i flag e il valore di contesto.</span><span class="sxs-lookup"><span data-stu-id="726fd-147">[**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) takes an HTTP session handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) and an HTTP verb, object name, version string, referrer, accept types, flags, and context value.</span></span>

<span data-ttu-id="726fd-148">Il verbo HTTP è una stringa da utilizzare nella richiesta.</span><span class="sxs-lookup"><span data-stu-id="726fd-148">The HTTP verb is a string to be used in the request.</span></span> <span data-ttu-id="726fd-149">I verbi HTTP comuni usati nelle richieste includono GET, PUT e POST.</span><span class="sxs-lookup"><span data-stu-id="726fd-149">Common HTTP verbs used in requests include GET, PUT, and POST.</span></span> <span data-ttu-id="726fd-150">Se questo valore è impostato su **null**, [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) usa il valore predefinito Get.</span><span class="sxs-lookup"><span data-stu-id="726fd-150">If this value is set to **NULL**, [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) uses the default value GET.</span></span>

<span data-ttu-id="726fd-151">Il nome dell'oggetto è una stringa che contiene il nome dell'oggetto di destinazione del verbo HTTP specificato.</span><span class="sxs-lookup"><span data-stu-id="726fd-151">The object name is a string that contains the name of the specified HTTP verb's target object.</span></span> <span data-ttu-id="726fd-152">Si tratta in genere di un nome file, un modulo eseguibile o un identificatore di ricerca.</span><span class="sxs-lookup"><span data-stu-id="726fd-152">This is generally a file name, an executable module, or a search specifier.</span></span> <span data-ttu-id="726fd-153">Se il nome dell'oggetto specificato è una stringa vuota, [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) cerca la pagina predefinita.</span><span class="sxs-lookup"><span data-stu-id="726fd-153">If the object name supplied is an empty string, [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) looks for the default page.</span></span>

<span data-ttu-id="726fd-154">La stringa di versione deve contenere la versione HTTP.</span><span class="sxs-lookup"><span data-stu-id="726fd-154">The version string should contain the HTTP version.</span></span> <span data-ttu-id="726fd-155">Se questo parametro è **null**, la funzione userà "" http/1.1 "".</span><span class="sxs-lookup"><span data-stu-id="726fd-155">If this parameter is **NULL**, the function uses ""HTTP/1.1"".</span></span>

<span data-ttu-id="726fd-156">Il referrer specifica l'indirizzo del documento da cui è stato ottenuto il nome dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="726fd-156">The referrer specifies the address of the document from which the object name was obtained.</span></span> <span data-ttu-id="726fd-157">Se questo parametro è **null**, non viene specificato alcun referrer.</span><span class="sxs-lookup"><span data-stu-id="726fd-157">If this parameter is **NULL**, no referrer is specified.</span></span>

<span data-ttu-id="726fd-158">La stringa con terminazione **null** che contiene i tipi Accept indica i tipi di contenuto accettati dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="726fd-158">The **null**-terminated string that contains the accept types indicates the content types accepted by the application.</span></span> <span data-ttu-id="726fd-159">L'impostazione di questo parametro su **null** indica che l'applicazione non accetta tipi di contenuto.</span><span class="sxs-lookup"><span data-stu-id="726fd-159">Setting this parameter to **NULL** indicates that no content types are accepted by the application.</span></span> <span data-ttu-id="726fd-160">Se viene fornita una stringa vuota, l'applicazione indica che accetta solo documenti di tipo "" Text/ \* "".</span><span class="sxs-lookup"><span data-stu-id="726fd-160">If an empty string is supplied, the application indicates it accepts only documents of type ""text/\*"".</span></span> <span data-ttu-id="726fd-161">Il valore "" Text/ \* "" indica solo i documenti di testo, non le immagini o altri file binari.</span><span class="sxs-lookup"><span data-stu-id="726fd-161">The value ""text/\*"" indicates text-only documents—not pictures or other binary files.</span></span>

<span data-ttu-id="726fd-162">I valori dei flag controllano la memorizzazione nella cache, i cookie e i problemi di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="726fd-162">The flag values control caching, cookies, and security issues.</span></span> <span data-ttu-id="726fd-163">Per Microsoft Network (MSN), NTLM e altri tipi di autenticazione, impostare il contrassegno [Internet \_ flag \_ Keep \_ Connection](api-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="726fd-163">For Microsoft Network (MSN), NTLM, and other types of authentication, set the [INTERNET\_FLAG\_KEEP\_CONNECTION](api-flags.md) flag.</span></span>

<span data-ttu-id="726fd-164">Se il flag di [ \_ flag \_ asincrono Internet](api-flags.md) è stato impostato nella chiamata a [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena), è necessario impostare un valore di contesto diverso da zero per un'operazione asincrona corretta.</span><span class="sxs-lookup"><span data-stu-id="726fd-164">If the [INTERNET\_FLAG\_ASYNC](api-flags.md) flag was set in the call to [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena), a nonzero context value should be set for proper asynchronous operation.</span></span>

<span data-ttu-id="726fd-165">Nell'esempio seguente viene illustrata una chiamata di esempio a [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span><span class="sxs-lookup"><span data-stu-id="726fd-165">The following example is a sample call to [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span>

`hHttpRequest = HttpOpenRequest( hHttpSession, "GET", "", NULL, "", NULL, 0, 0);`

### <a name="adding-request-headers"></a><span data-ttu-id="726fd-166">Aggiunta di intestazioni di richiesta</span><span class="sxs-lookup"><span data-stu-id="726fd-166">Adding Request Headers</span></span>

<span data-ttu-id="726fd-167">La funzione [**HttpAddRequestHeaders**](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa) consente alle applicazioni di aggiungere una o più intestazioni di richiesta alla richiesta iniziale.</span><span class="sxs-lookup"><span data-stu-id="726fd-167">The [**HttpAddRequestHeaders**](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa) function enables applications to add one or more request headers to the initial request.</span></span> <span data-ttu-id="726fd-168">Questa funzione consente a un'applicazione di aggiungere intestazioni di formato libero aggiuntive all'handle di richiesta HTTP; è progettato per l'uso da parte di applicazioni sofisticate che richiedono un controllo preciso sulla richiesta inviata al server HTTP.</span><span class="sxs-lookup"><span data-stu-id="726fd-168">This function allows an application to append additional free-format headers to the HTTP request handle; it is intended for use by sophisticated applications that require precise control over the request sent to the HTTP server.</span></span>

<span data-ttu-id="726fd-169">[**HttpAddRequestHeaders**](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa) richiede un handle di richiesta HTTP creato da [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta), una stringa che contiene le intestazioni, la lunghezza delle intestazioni e i modificatori.</span><span class="sxs-lookup"><span data-stu-id="726fd-169">[**HttpAddRequestHeaders**](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa) needs an HTTP request handle created by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta), a string that contains the headers, the length of the headers, and modifiers.</span></span>

### <a name="sending-a-request"></a><span data-ttu-id="726fd-170">Invio di una richiesta</span><span class="sxs-lookup"><span data-stu-id="726fd-170">Sending a Request</span></span>

<span data-ttu-id="726fd-171">[**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) stabilisce una connessione a Internet e Invia la richiesta al sito specificato.</span><span class="sxs-lookup"><span data-stu-id="726fd-171">[**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) establishes a connection to the Internet and sends the request to the specified site.</span></span> <span data-ttu-id="726fd-172">Questa funzione richiede un handle [**HINTERNET**](appendix-a-hinternet-handles.md) creato da [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span><span class="sxs-lookup"><span data-stu-id="726fd-172">This function requires an [**HINTERNET**](appendix-a-hinternet-handles.md) handle created by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span> <span data-ttu-id="726fd-173">[**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) può anche inviare intestazioni aggiuntive o informazioni facoltative.</span><span class="sxs-lookup"><span data-stu-id="726fd-173">[**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) can also send additional headers or optional information.</span></span> <span data-ttu-id="726fd-174">Le informazioni facoltative vengono in genere usate per le operazioni che scrivono le informazioni sul server, ad esempio PUT e POST.</span><span class="sxs-lookup"><span data-stu-id="726fd-174">The optional information is generally used for operations that write information to the server, such as PUT and POST.</span></span>

<span data-ttu-id="726fd-175">Dopo che [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) ha inviato la richiesta, l'applicazione può usare le funzioni [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), [**la InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable)e [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) sull'handle [**HINTERNET**](appendix-a-hinternet-handles.md) creato da [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) per scaricare le risorse del server.</span><span class="sxs-lookup"><span data-stu-id="726fd-175">After [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) sends the request, the application can use the [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable), and [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) functions on the [**HINTERNET**](appendix-a-hinternet-handles.md) handle created by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) to download the server's resources.</span></span>

### <a name="posting-data-to-the-server"></a><span data-ttu-id="726fd-176">Invio di dati al server</span><span class="sxs-lookup"><span data-stu-id="726fd-176">Posting Data to the Server</span></span>

<span data-ttu-id="726fd-177">Per inserire i dati in un server, il verbo HTTP nella chiamata a [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) deve essere post o put.</span><span class="sxs-lookup"><span data-stu-id="726fd-177">To post data to a server, the HTTP verb in the call to [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) must be either POST or PUT.</span></span> <span data-ttu-id="726fd-178">L'indirizzo del buffer che contiene i dati POST deve quindi essere passato al parametro *lpOptional* in [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span><span class="sxs-lookup"><span data-stu-id="726fd-178">The address of the buffer that contains the POST data should then be passed to the *lpOptional* parameter in [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span></span> <span data-ttu-id="726fd-179">Il parametro *dwOptionalLength* deve essere impostato sulla dimensione dei dati.</span><span class="sxs-lookup"><span data-stu-id="726fd-179">The *dwOptionalLength* parameter should be set to the size of the data.</span></span>

<span data-ttu-id="726fd-180">È anche possibile usare la funzione [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile) per pubblicare dati in un handle [**HINTERNET**](appendix-a-hinternet-handles.md) inviato usando [**HttpSendRequestEx**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequestexa).</span><span class="sxs-lookup"><span data-stu-id="726fd-180">You can also use the [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile) function to post data on an [**HINTERNET**](appendix-a-hinternet-handles.md) handle sent using [**HttpSendRequestEx**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequestexa).</span></span>

### <a name="getting-information-about-a-request"></a><span data-ttu-id="726fd-181">Ottenere informazioni su una richiesta</span><span class="sxs-lookup"><span data-stu-id="726fd-181">Getting Information About a Request</span></span>

<span data-ttu-id="726fd-182">[**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) consente a un'applicazione di recuperare informazioni su una richiesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="726fd-182">[**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) allows an application to retrieve information about an HTTP request.</span></span> <span data-ttu-id="726fd-183">La funzione richiede un handle [**HINTERNET**](appendix-a-hinternet-handles.md) creato da [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) o [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), un valore a livello di informazioni e una lunghezza del buffer.</span><span class="sxs-lookup"><span data-stu-id="726fd-183">The function requires an [**HINTERNET**](appendix-a-hinternet-handles.md) handle created by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) or [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), an information level value, and a buffer length.</span></span> <span data-ttu-id="726fd-184">[**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) accetta anche un buffer che archivia le informazioni e un indice in base zero dell'intestazione che enumera più intestazioni con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="726fd-184">[**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) also accepts a buffer that stores the information and a zero-based header index that enumerates multiple headers with the same name.</span></span>

### <a name="downloading-resources-from-the-www"></a><span data-ttu-id="726fd-185">Download delle risorse dal sito Web</span><span class="sxs-lookup"><span data-stu-id="726fd-185">Downloading Resources from the WWW</span></span>

<span data-ttu-id="726fd-186">Dopo l'apertura di una richiesta con [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) e l'invio al server con [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta), l'applicazione può usare le funzioni [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), [**la InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable)e [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) per scaricare la risorsa dal server http.</span><span class="sxs-lookup"><span data-stu-id="726fd-186">After opening a request with [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) and sending it to the server with [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta), the application can use the [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable), and [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) functions to download the resource from the HTTP server.</span></span>

<span data-ttu-id="726fd-187">Nell'esempio seguente viene scaricata una risorsa.</span><span class="sxs-lookup"><span data-stu-id="726fd-187">The following example downloads a resource.</span></span> <span data-ttu-id="726fd-188">La funzione accetta l'handle per la finestra corrente, il numero di identificazione di una casella di modifica e un handle [**HINTERNET**](appendix-a-hinternet-handles.md) creato da [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) e inviato da [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span><span class="sxs-lookup"><span data-stu-id="726fd-188">The function accepts the handle to the current window, the identification number of an edit box, and an [**HINTERNET**](appendix-a-hinternet-handles.md) handle created by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) and sent by [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span></span> <span data-ttu-id="726fd-189">USA [**la InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) per determinare le dimensioni della risorsa e quindi lo Scarica usando [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).</span><span class="sxs-lookup"><span data-stu-id="726fd-189">It uses [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) to determine the size of the resource and then downloads it using [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).</span></span> <span data-ttu-id="726fd-190">Il contenuto viene quindi visualizzato nella casella di modifica.</span><span class="sxs-lookup"><span data-stu-id="726fd-190">The contents are then displayed in the edit box.</span></span>


```C++
int WINAPI Dumper(HWND hX, int intCtrlID, HINTERNET hResource)
{
    LPTSTR lpszData;    // buffer for the data
    DWORD  dwSize;       // size of the data available
    DWORD  dwDownloaded; // size of the downloaded data
    DWORD  dwSizeSum=0;  // size of the data in the textbox
    LPTSTR lpszHolding;  // buffer to merge the textbox data and buffer

    // Set the cursor to an hourglass.
    SetCursor(LoadCursor(NULL,IDC_WAIT));

    // This loop handles reading the data.
    do
    {
        // The call to InternetQueryDataAvailable determines the
        // amount of data available to download.
        if (!InternetQueryDataAvailable(hResource,&dwSize,0,0))
        {
            printf("InternetQueryDataAvailable failed (%d)\n", GetLastError());
            SetCursor(LoadCursor(NULL,IDC_ARROW));
            return FALSE;
        }
        else
        {
            // Allocate a buffer of the size returned by
            // InternetQueryDataAvailable.
            lpszData = new TCHAR[dwSize+1];

            // Read the data from the HINTERNET handle.
            if(!InternetReadFile(hResource,
                                 (LPVOID)lpszData,
                                 dwSize,
                                 &dwDownloaded))
            {
                printf("InternetReadFile failed (%d)\n", GetLastError());
                delete[] lpszData;
                break;
            }
            else
            {
                // Add a null terminator to the end of the data buffer
                lpszData[dwDownloaded]='\0';

                // Allocate the holding buffer.
                lpszHolding = new TCHAR[dwSizeSum + dwDownloaded + 1];

                // Check if there has been any data written
                // to the textbox.
                if (dwSizeSum != 0)
                {
                    // Retrieve the data stored in the textbox if any
                    GetDlgItemText(hX,intCtrlID,
                                   (LPTSTR)lpszHolding,
                                   dwSizeSum);

                    // Add a null terminator at the end of the
                    // textbox data.
                    lpszHolding[dwSizeSum]='\0';
                }
                else
                {
                    // Make the holding buffer an empty string.
                    lpszHolding[0]='\0';
                }

                size_t cchDest = dwSizeSum + dwDownloaded + dwDownloaded + 1;
                LPTSTR* ppszDestEnd = 0;
                size_t* pcchRemaining = 0;

                // Add the new data to the holding buffer
                HRESULT hr = StringCchCatEx(lpszHolding,
                                            cchDest,
                                            lpszData,
                                            ppszDestEnd,
                                            pcchRemaining,
                                            STRSAFE_NO_TRUNCATION);

                if(SUCCEEDED(hr))
                {
                    // Write the holding buffer to the textbox.
                    SetDlgItemText(hX,intCtrlID,(LPTSTR)lpszHolding);

                    // Delete the two buffers.
                    delete[] lpszHolding;
                    delete[] lpszData;

                    // Add the size of the downloaded data to the
                    // textbox data size.
                    dwSizeSum = dwSizeSum + dwDownloaded + 1;

                    // Check the size of the remaining data.
                    // If it is zero, break.
                    if (dwDownloaded == 0)
                        break;
                    else
                    {
                    //  TODO: Insert error handling code here.
                    }
                }
            }
        }
    }
    while(TRUE);

    // Close the HINTERNET handle.
    InternetCloseHandle(hResource);

    // Set the cursor back to an arrow.
    SetCursor(LoadCursor(NULL,IDC_ARROW));

    return TRUE;
}
```



> [!Note]  
> <span data-ttu-id="726fd-191">WinINet non supporta le implementazioni del server.</span><span class="sxs-lookup"><span data-stu-id="726fd-191">WinINet does not support server implementations.</span></span> <span data-ttu-id="726fd-192">Inoltre, non deve essere utilizzato da un servizio.</span><span class="sxs-lookup"><span data-stu-id="726fd-192">In addition, it should not be used from a service.</span></span> <span data-ttu-id="726fd-193">Per le implementazioni o i servizi del server, usare i [Servizi http di Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="726fd-193">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 