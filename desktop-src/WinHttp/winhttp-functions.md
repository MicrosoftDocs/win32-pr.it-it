---
description: Questo argomento identifica le funzioni fornite da WinHTTP.
ms.assetid: dcb56d5d-ed0d-49bb-95bf-940a49c033f1
title: Funzioni WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41e45289230c1cc22a7f8799dfbbe1dafddccf38
ms.sourcegitcommit: 8e3d8594fa073a9c43eb5dcc7babea03ea30f10f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/01/2021
ms.locfileid: "113174973"
---
# <a name="winhttp-functions"></a><span data-ttu-id="46d36-103">Funzioni WinHTTP</span><span class="sxs-lookup"><span data-stu-id="46d36-103">WinHTTP Functions</span></span>

<span data-ttu-id="46d36-104">WinHTTP offre le funzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="46d36-104">WinHTTP provides the following functions:</span></span>

<dl> <dt>

[<span data-ttu-id="46d36-105">**WinHttpAddRequestHeaders**</span><span class="sxs-lookup"><span data-stu-id="46d36-105">**WinHttpAddRequestHeaders**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)
</dt> <dd>

<span data-ttu-id="46d36-106">Aggiunge una o più intestazioni di richiesta HTTP all'handle della richiesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="46d36-106">Adds one or more HTTP request headers to the HTTP request handle.</span></span>

</dd> <dt>

[<span data-ttu-id="46d36-107">**WinHttpAddRequestHeadersEx**</span><span class="sxs-lookup"><span data-stu-id="46d36-107">**WinHttpAddRequestHeadersEx**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheadersex)
</dt> <dd>

<span data-ttu-id="46d36-108">Aggiunge una o più intestazioni di richiesta HTTP a un handle di richiesta HTTP, consentendo di usare stringhe nome/valore separate.</span><span class="sxs-lookup"><span data-stu-id="46d36-108">Adds one or more HTTP request headers to an HTTP request handle, allowing you to use separate name/value strings.</span></span>

</dd> <dt>

[<span data-ttu-id="46d36-109">**WinHttpCheckPlatform**</span><span class="sxs-lookup"><span data-stu-id="46d36-109">**WinHttpCheckPlatform**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcheckplatform)
</dt> <dd>

<span data-ttu-id="46d36-110">Determina se la piattaforma corrente è supportata da WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="46d36-110">Determines whether the current platform is supported by WinHTTP.</span></span>

</dd> <dt>

[<span data-ttu-id="46d36-111">**WinHttpCloseHandle**</span><span class="sxs-lookup"><span data-stu-id="46d36-111">**WinHttpCloseHandle**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpclosehandle)
</dt> <dd>

<span data-ttu-id="46d36-112">Chiude un singolo handle [HINTERNET.](hinternet-handles-in-winhttp.md)</span><span class="sxs-lookup"><span data-stu-id="46d36-112">Closes a single [HINTERNET](hinternet-handles-in-winhttp.md) handle.</span></span>

</dd> <dt>

[<span data-ttu-id="46d36-113">**WinHttpConnect**</span><span class="sxs-lookup"><span data-stu-id="46d36-113">**WinHttpConnect**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect)
</dt> <dd>

<span data-ttu-id="46d36-114">Specifica il server di destinazione iniziale di una richiesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="46d36-114">Specifies the initial target server of an HTTP request.</span></span>

</dd> <dt>

[<span data-ttu-id="46d36-115">**WinHttpUrl**</span><span class="sxs-lookup"><span data-stu-id="46d36-115">**WinHttpCrackUrl**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl)
</dt> <dd>

<span data-ttu-id="46d36-116">Separa un URL nelle relative parti componenti, ad esempio il nome host e il percorso.</span><span class="sxs-lookup"><span data-stu-id="46d36-116">Separates a URL into its component parts, for example, host name and path.</span></span>

</dd> <dt>

[<span data-ttu-id="46d36-117">**WinHttpCreateProxyResolver**</span><span class="sxs-lookup"><span data-stu-id="46d36-117">**WinHttpCreateProxyResolver**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateproxyresolver)
</dt> <dd>

<span data-ttu-id="46d36-118">Crea un handle per l'uso [**da parte di WinHttpGetProxyForUrlEx.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex)</span><span class="sxs-lookup"><span data-stu-id="46d36-118">Creates a handle for use by [**WinHttpGetProxyForUrlEx**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex).</span></span>

</dd> <dt>

[<span data-ttu-id="46d36-119">**WinHttpCreateUrl**</span><span class="sxs-lookup"><span data-stu-id="46d36-119">**WinHttpCreateUrl**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl)
</dt> <dd>

<span data-ttu-id="46d36-120">Crea un URL dalle parti del componente, ad esempio il nome host e il percorso.</span><span class="sxs-lookup"><span data-stu-id="46d36-120">Creates a URL from component parts, for example, the host name and path.</span></span>

</dd> <dt>

[<span data-ttu-id="46d36-121">**WinHttpDetectAutoProxyConfigUrl**</span><span class="sxs-lookup"><span data-stu-id="46d36-121">**WinHttpDetectAutoProxyConfigUrl**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl)
</dt> <dd>

<span data-ttu-id="46d36-122">Trova l'URL per il file di configurazione automatica del proxy (PAC).</span><span class="sxs-lookup"><span data-stu-id="46d36-122">Finds the URL for the Proxy Auto-Configuration (PAC) file.</span></span> <span data-ttu-id="46d36-123">Questa funzione segnala l'URL del file PAC, ma non scarica il file.</span><span class="sxs-lookup"><span data-stu-id="46d36-123">This function reports the URL of the PAC file, but it does not download the file.</span></span>

</dd> <dt>

[<span data-ttu-id="46d36-124">**WinHttpFreeProxyResult**</span><span class="sxs-lookup"><span data-stu-id="46d36-124">**WinHttpFreeProxyResult**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpfreeproxyresult)
</dt> <dd>

<span data-ttu-id="46d36-125">Libera i dati recuperati da una chiamata precedente a [**WinHttpGetProxyResult.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult)</span><span class="sxs-lookup"><span data-stu-id="46d36-125">Frees the data retrieved from a previous call to [**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult).</span></span>

</dd> <dt>

[<span data-ttu-id="46d36-126">**WinHttpFreeQueryConnectionGroupResult**</span><span class="sxs-lookup"><span data-stu-id="46d36-126">**WinHttpFreeQueryConnectionGroupResult**</span></span>](/windows/win32/api/Winhttp/nf-winhttp-winhttpfreequeryconnectiongroupresult)
</dt> <dd>

<span data-ttu-id="46d36-127">Libera la memoria allocata da una chiamata precedente a [WinHttpQueryConnectionGroup.](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryconnectiongroup)</span><span class="sxs-lookup"><span data-stu-id="46d36-127">Frees the memory allocated by a previous call to [WinHttpQueryConnectionGroup](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryconnectiongroup).</span></span>

</dd> <dt>

[<span data-ttu-id="46d36-128">**WinHttpGetDefaultProxyConfiguration**</span><span class="sxs-lookup"><span data-stu-id="46d36-128">**WinHttpGetDefaultProxyConfiguration**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetdefaultproxyconfiguration)
</dt> <dd>

<span data-ttu-id="46d36-129">Recupera la configurazione del proxy WinHTTP predefinita dal Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="46d36-129">Retrieves the default WinHTTP proxy configuration from the registry.</span></span>

</dd> <dt>

[<span data-ttu-id="46d36-130">**WinHTTPGetIEProxyConfigForCurrentUser**</span><span class="sxs-lookup"><span data-stu-id="46d36-130">**WinHTTPGetIEProxyConfigForCurrentUser**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser)
</dt> <dd>

<span data-ttu-id="46d36-131">Ottiene la configurazione Internet Explorer proxy per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="46d36-131">Obtains the Internet Explorer (IE) proxy configuration for the current user.</span></span>

</dd> <dt>

[<span data-ttu-id="46d36-132">**WinHttpGetProxyForUrl**</span><span class="sxs-lookup"><span data-stu-id="46d36-132">**WinHttpGetProxyForUrl**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl)
</dt> <dd>

<span data-ttu-id="46d36-133">Recupera le informazioni proxy per l'URL specificato.</span><span class="sxs-lookup"><span data-stu-id="46d36-133">Retrieves the proxy information for the specified URL.</span></span>

</dd> <dt>

[<span data-ttu-id="46d36-134">**WinHttpGetProxyForUrlEx**</span><span class="sxs-lookup"><span data-stu-id="46d36-134">**WinHttpGetProxyForUrlEx**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex)
</dt> <dd>

<span data-ttu-id="46d36-135">Recupera le informazioni proxy per l'URL specificato.</span><span class="sxs-lookup"><span data-stu-id="46d36-135">Retrieves the proxy information for the specified URL.</span></span>

</dd> <dt>

[<span data-ttu-id="46d36-136">**WinHttpGetProxyResult**</span><span class="sxs-lookup"><span data-stu-id="46d36-136">**WinHttpGetProxyResult**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult)
</dt> <dd>

<span data-ttu-id="46d36-137">Recupera i risultati di una chiamata a [**WinHttpGetProxyForUrlEx.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex)</span><span class="sxs-lookup"><span data-stu-id="46d36-137">Retrieves the results of a call to [**WinHttpGetProxyForUrlEx**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex).</span></span>

</dd> <dt>

[<span data-ttu-id="46d36-138">**WinHttpOpen**</span><span class="sxs-lookup"><span data-stu-id="46d36-138">**WinHttpOpen**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen)
</dt> <dd>

<span data-ttu-id="46d36-139">Inizializza l'uso delle funzioni WinHTTP da parte di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="46d36-139">Initializes an application's use of the WinHTTP functions.</span></span>

</dd> <dt>

[<span data-ttu-id="46d36-140">**WinHttpOpenRequest**</span><span class="sxs-lookup"><span data-stu-id="46d36-140">**WinHttpOpenRequest**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)
</dt> <dd>

<span data-ttu-id="46d36-141">Crea un handle di richiesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="46d36-141">Creates an HTTP request handle.</span></span>

</dd> <dt>

[<span data-ttu-id="46d36-142">**WinHttpQueryAuthSchemes**</span><span class="sxs-lookup"><span data-stu-id="46d36-142">**WinHttpQueryAuthSchemes**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes)
</dt> <dd>

<span data-ttu-id="46d36-143">Restituisce gli schemi di autorizzazione supportati dal server.</span><span class="sxs-lookup"><span data-stu-id="46d36-143">Returns the authorization schemes that the server supports.</span></span>

</dd> <dt>

[<span data-ttu-id="46d36-144">**WinHttpQueryConnectionGroup**</span><span class="sxs-lookup"><span data-stu-id="46d36-144">**WinHttpQueryConnectionGroup**</span></span>](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryconnectiongroup)
</dt> <dd>

<span data-ttu-id="46d36-145">Recupera una descrizione dello stato corrente delle connessioni di WinHttp.</span><span class="sxs-lookup"><span data-stu-id="46d36-145">Retrieves a description of the current state of WinHttp's connections.</span></span>

</dd> <dt>

[<span data-ttu-id="46d36-146">**WinHttpQueryDataAvailable**</span><span class="sxs-lookup"><span data-stu-id="46d36-146">**WinHttpQueryDataAvailable**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable)
</dt> <dd>

<span data-ttu-id="46d36-147">Restituisce il numero di byte di dati immediatamente disponibili per la lettura con [**WinHttpReadData.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata)</span><span class="sxs-lookup"><span data-stu-id="46d36-147">Returns the number of bytes of data that are available immediately to be read with [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata).</span></span>

</dd> <dt>

[<span data-ttu-id="46d36-148">**WinHttpQueryHeaders**</span><span class="sxs-lookup"><span data-stu-id="46d36-148">**WinHttpQueryHeaders**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders)
</dt> <dd>

<span data-ttu-id="46d36-149">Recupera le informazioni di intestazione associate a una richiesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="46d36-149">Retrieves header information associated with an HTTP request.</span></span>

</dd> <dt>

[<span data-ttu-id="46d36-150">**WinHttpQueryHeadersEx**</span><span class="sxs-lookup"><span data-stu-id="46d36-150">**WinHttpQueryHeadersEx**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheadersex)
</dt> <dd>

<span data-ttu-id="46d36-151">Recupera le informazioni di intestazione associate a una richiesta HTTP. offre un modo per recuperare le stringhe di nome e valore dell'intestazione analizzata.</span><span class="sxs-lookup"><span data-stu-id="46d36-151">Retrieves header information associated with an HTTP request; offers a way to retrieve parsed header name and value strings.</span></span>

</dd> <dt>

[<span data-ttu-id="46d36-152">**WinHttpQueryOption**</span><span class="sxs-lookup"><span data-stu-id="46d36-152">**WinHttpQueryOption**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)
</dt> <dd>

<span data-ttu-id="46d36-153">Esegue una query su un'opzione Internet sull'handle specificato.</span><span class="sxs-lookup"><span data-stu-id="46d36-153">Queries an Internet option on the specified handle.</span></span>

</dd> <dt>

[<span data-ttu-id="46d36-154">**WinHttpReadData**</span><span class="sxs-lookup"><span data-stu-id="46d36-154">**WinHttpReadData**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata)
</dt> <dd>

<span data-ttu-id="46d36-155">Legge i dati da un handle aperto dalla [**funzione WinHttpOpenRequest.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)</span><span class="sxs-lookup"><span data-stu-id="46d36-155">Reads data from a handle opened by the [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) function.</span></span>

</dd> <dt>

[<span data-ttu-id="46d36-156">**WinHttpReadDataEx**</span><span class="sxs-lookup"><span data-stu-id="46d36-156">**WinHttpReadDataEx**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddataex)
</dt> <dd>

<span data-ttu-id="46d36-157">Legge i dati da un handle aperto dalla [**funzione WinHttpOpenRequest.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)</span><span class="sxs-lookup"><span data-stu-id="46d36-157">Reads data from a handle opened by the [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) function.</span></span>

</dd> <dt>

[<span data-ttu-id="46d36-158">**WinHttpReceiveResponse**</span><span class="sxs-lookup"><span data-stu-id="46d36-158">**WinHttpReceiveResponse**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse)
</dt> <dd>

<span data-ttu-id="46d36-159">Termina una richiesta HTTP avviata da [**WinHttpSendRequest.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)</span><span class="sxs-lookup"><span data-stu-id="46d36-159">Ends an HTTP request that is initiated by [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span>

</dd> <dt>

[<span data-ttu-id="46d36-160">**WinHttpResetAutoProxy**</span><span class="sxs-lookup"><span data-stu-id="46d36-160">**WinHttpResetAutoProxy**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpresetautoproxy)
</dt> <dd>

<span data-ttu-id="46d36-161">Reimposta il proxy automatico.</span><span class="sxs-lookup"><span data-stu-id="46d36-161">Resets the auto-proxy.</span></span>

</dd> <dt>

[<span data-ttu-id="46d36-162">**WinHttpSendRequest**</span><span class="sxs-lookup"><span data-stu-id="46d36-162">**WinHttpSendRequest**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)
</dt> <dd>

<span data-ttu-id="46d36-163">Invia la richiesta specificata al server HTTP.</span><span class="sxs-lookup"><span data-stu-id="46d36-163">Sends the specified request to the HTTP server.</span></span>

</dd> <dt>

[<span data-ttu-id="46d36-164">**WinHttpSetCredentials**</span><span class="sxs-lookup"><span data-stu-id="46d36-164">**WinHttpSetCredentials**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials)
</dt> <dd>

<span data-ttu-id="46d36-165">Passa le credenziali di autorizzazione necessarie al server.</span><span class="sxs-lookup"><span data-stu-id="46d36-165">Passes the required authorization credentials to the server.</span></span>

</dd> <dt>

[<span data-ttu-id="46d36-166">**WinHttpSetDefaultProxyConfiguration**</span><span class="sxs-lookup"><span data-stu-id="46d36-166">**WinHttpSetDefaultProxyConfiguration**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetdefaultproxyconfiguration)
</dt> <dd>

<span data-ttu-id="46d36-167">Imposta la configurazione predefinita del proxy WinHTTP nel Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="46d36-167">Sets the default WinHTTP proxy configuration in the registry.</span></span>

</dd> <dt>

[<span data-ttu-id="46d36-168">**WinHttpSetOption**</span><span class="sxs-lookup"><span data-stu-id="46d36-168">**WinHttpSetOption**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)
</dt> <dd>

<span data-ttu-id="46d36-169">Imposta un'opzione Internet.</span><span class="sxs-lookup"><span data-stu-id="46d36-169">Sets an Internet option.</span></span>

</dd> <dt>

[<span data-ttu-id="46d36-170">**WinHttpSetStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="46d36-170">**WinHttpSetStatusCallback**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback)
</dt> <dd>

<span data-ttu-id="46d36-171">Configura una funzione di callback che WinHTTP può chiamare quando viene eseguito lo stato di avanzamento durante un'operazione.</span><span class="sxs-lookup"><span data-stu-id="46d36-171">Sets up a callback function that WinHTTP can call as progress is made during an operation.</span></span>

</dd> <dt>

[<span data-ttu-id="46d36-172">**WinHttpSetTimeouts**</span><span class="sxs-lookup"><span data-stu-id="46d36-172">**WinHttpSetTimeouts**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts)
</dt> <dd>

<span data-ttu-id="46d36-173">Imposta i vari timeout coinvolti nelle transazioni HTTP.</span><span class="sxs-lookup"><span data-stu-id="46d36-173">Sets the various time-outs that are involved with HTTP transactions.</span></span>

</dd> <dt>

[<span data-ttu-id="46d36-174">**WinHttpTimeFromSystemTime**</span><span class="sxs-lookup"><span data-stu-id="46d36-174">**WinHttpTimeFromSystemTime**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttptimefromsystemtime)
</dt> <dd>

<span data-ttu-id="46d36-175">Formatta una data e un'ora in base alla specifica HTTP versione 1.0.</span><span class="sxs-lookup"><span data-stu-id="46d36-175">Formats a date and time according to the HTTP version 1.0 specification.</span></span>

</dd> <dt>

[<span data-ttu-id="46d36-176">**WinHttpTimeToSystemTime**</span><span class="sxs-lookup"><span data-stu-id="46d36-176">**WinHttpTimeToSystemTime**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttptimetosystemtime)
</dt> <dd>

<span data-ttu-id="46d36-177">Accetta una stringa di data/ora HTTP e la converte in [**una struttura SYSTEMTIME.**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)</span><span class="sxs-lookup"><span data-stu-id="46d36-177">Takes an HTTP time/date string and converts it to a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure.</span></span>

</dd> <dt>

[<span data-ttu-id="46d36-178">**WinHttpWriteData**</span><span class="sxs-lookup"><span data-stu-id="46d36-178">**WinHttpWriteData**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata)
</dt> <dd>

<span data-ttu-id="46d36-179">Scrive i dati della richiesta in un server HTTP.</span><span class="sxs-lookup"><span data-stu-id="46d36-179">Writes request data to an HTTP server.</span></span>

</dd> <dt>

[<span data-ttu-id="46d36-180">**WinHttpWebSocketClose**</span><span class="sxs-lookup"><span data-stu-id="46d36-180">**WinHttpWebSocketClose**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketclose)
</dt> <dd>

<span data-ttu-id="46d36-181">Chiude una connessione WebSocket.</span><span class="sxs-lookup"><span data-stu-id="46d36-181">Closes a WebSocket connection.</span></span>

</dd> <dt>

[<span data-ttu-id="46d36-182">**WinHttpWebSocketCompleteUpgrade**</span><span class="sxs-lookup"><span data-stu-id="46d36-182">**WinHttpWebSocketCompleteUpgrade**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketcompleteupgrade)
</dt> <dd>

<span data-ttu-id="46d36-183">Completa un handshake WebSocket avviato da [**WinHttpSendRequest.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)</span><span class="sxs-lookup"><span data-stu-id="46d36-183">Completes a WebSocket handshake started by [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span>

</dd> <dt>

[<span data-ttu-id="46d36-184">**WinHttpWebSocketQueryCloseStatus**</span><span class="sxs-lookup"><span data-stu-id="46d36-184">**WinHttpWebSocketQueryCloseStatus**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketqueryclosestatus)
</dt> <dd>

<span data-ttu-id="46d36-185">Ottiene lo stato di chiusura inviato da un server.</span><span class="sxs-lookup"><span data-stu-id="46d36-185">Gets the close status sent by a server.</span></span>

</dd> <dt>

[<span data-ttu-id="46d36-186">**WinHttpWebSocketReceive**</span><span class="sxs-lookup"><span data-stu-id="46d36-186">**WinHttpWebSocketReceive**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketreceive)
</dt> <dd>

<span data-ttu-id="46d36-187">Riceve dati da una connessione WebSocket.</span><span class="sxs-lookup"><span data-stu-id="46d36-187">Receives data from a WebSocket connection.</span></span>

</dd> <dt>

[<span data-ttu-id="46d36-188">**WinHttpWebSocketSend**</span><span class="sxs-lookup"><span data-stu-id="46d36-188">**WinHttpWebSocketSend**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketsend)
</dt> <dd>

<span data-ttu-id="46d36-189">Invia dati tramite una connessione WebSocket.</span><span class="sxs-lookup"><span data-stu-id="46d36-189">Sends data over a WebSocket connection.</span></span>

</dd> <dt>

[<span data-ttu-id="46d36-190">**WinHttpWebSocketShutdown**</span><span class="sxs-lookup"><span data-stu-id="46d36-190">**WinHttpWebSocketShutdown**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketshutdown)
</dt> <dd>

<span data-ttu-id="46d36-191">Invia un frame vicino a una connessione WebSocket.</span><span class="sxs-lookup"><span data-stu-id="46d36-191">Sends a close frame to a WebSocket connection.</span></span>

</dd> </dl>


