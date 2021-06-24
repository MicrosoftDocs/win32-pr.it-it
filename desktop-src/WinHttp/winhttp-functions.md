---
description: Questo argomento identifica le funzioni fornite da WinHTTP.
ms.assetid: dcb56d5d-ed0d-49bb-95bf-940a49c033f1
title: Funzioni WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf5f9db8fcde5589a86556111bec6df3b2b18c76
ms.sourcegitcommit: 749dea42142dec076d41a8f26cb57ae8db46e848
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/24/2021
ms.locfileid: "112587746"
---
# <a name="winhttp-functions"></a><span data-ttu-id="f5d9e-103">Funzioni WinHTTP</span><span class="sxs-lookup"><span data-stu-id="f5d9e-103">WinHTTP Functions</span></span>

<span data-ttu-id="f5d9e-104">WinHTTP offre le funzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="f5d9e-104">WinHTTP provides the following functions:</span></span>

<dl> <dt>

[<span data-ttu-id="f5d9e-105">**WinHttpAddRequestHeaders**</span><span class="sxs-lookup"><span data-stu-id="f5d9e-105">**WinHttpAddRequestHeaders**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)
</dt> <dd>

<span data-ttu-id="f5d9e-106">Aggiunge una o più intestazioni di richiesta HTTP all'handle della richiesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="f5d9e-106">Adds one or more HTTP request headers to the HTTP request handle.</span></span>

</dd> <dt>

[<span data-ttu-id="f5d9e-107">**WinHttpCheckPlatform**</span><span class="sxs-lookup"><span data-stu-id="f5d9e-107">**WinHttpCheckPlatform**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcheckplatform)
</dt> <dd>

<span data-ttu-id="f5d9e-108">Determina se la piattaforma corrente è supportata da WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="f5d9e-108">Determines whether the current platform is supported by WinHTTP.</span></span>

</dd> <dt>

[<span data-ttu-id="f5d9e-109">**WinHttpCloseHandle**</span><span class="sxs-lookup"><span data-stu-id="f5d9e-109">**WinHttpCloseHandle**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpclosehandle)
</dt> <dd>

<span data-ttu-id="f5d9e-110">Chiude un singolo [handle HINTERNET.](hinternet-handles-in-winhttp.md)</span><span class="sxs-lookup"><span data-stu-id="f5d9e-110">Closes a single [HINTERNET](hinternet-handles-in-winhttp.md) handle.</span></span>

</dd> <dt>

[<span data-ttu-id="f5d9e-111">**WinHttpConnect**</span><span class="sxs-lookup"><span data-stu-id="f5d9e-111">**WinHttpConnect**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect)
</dt> <dd>

<span data-ttu-id="f5d9e-112">Specifica il server di destinazione iniziale di una richiesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="f5d9e-112">Specifies the initial target server of an HTTP request.</span></span>

</dd> <dt>

[<span data-ttu-id="f5d9e-113">**WinHttpCrackUrl**</span><span class="sxs-lookup"><span data-stu-id="f5d9e-113">**WinHttpCrackUrl**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl)
</dt> <dd>

<span data-ttu-id="f5d9e-114">Separa un URL nelle relative parti del componente, ad esempio il nome host e il percorso.</span><span class="sxs-lookup"><span data-stu-id="f5d9e-114">Separates a URL into its component parts, for example, host name and path.</span></span>

</dd> <dt>

[<span data-ttu-id="f5d9e-115">**WinHttpCreateProxyResolver**</span><span class="sxs-lookup"><span data-stu-id="f5d9e-115">**WinHttpCreateProxyResolver**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateproxyresolver)
</dt> <dd>

<span data-ttu-id="f5d9e-116">Crea un handle per l'uso [**da parte di WinHttpGetProxyForUrlEx.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex)</span><span class="sxs-lookup"><span data-stu-id="f5d9e-116">Creates a handle for use by [**WinHttpGetProxyForUrlEx**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex).</span></span>

</dd> <dt>

[<span data-ttu-id="f5d9e-117">**WinHttpCreateUrl**</span><span class="sxs-lookup"><span data-stu-id="f5d9e-117">**WinHttpCreateUrl**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl)
</dt> <dd>

<span data-ttu-id="f5d9e-118">Crea un URL dalle parti del componente, ad esempio il nome host e il percorso.</span><span class="sxs-lookup"><span data-stu-id="f5d9e-118">Creates a URL from component parts, for example, the host name and path.</span></span>

</dd> <dt>

[<span data-ttu-id="f5d9e-119">**WinHttpDetectAutoProxyConfigUrl**</span><span class="sxs-lookup"><span data-stu-id="f5d9e-119">**WinHttpDetectAutoProxyConfigUrl**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl)
</dt> <dd>

<span data-ttu-id="f5d9e-120">Trova l'URL per il file pac (Proxy Auto-Configuration).</span><span class="sxs-lookup"><span data-stu-id="f5d9e-120">Finds the URL for the Proxy Auto-Configuration (PAC) file.</span></span> <span data-ttu-id="f5d9e-121">Questa funzione segnala l'URL del file PAC, ma non scarica il file.</span><span class="sxs-lookup"><span data-stu-id="f5d9e-121">This function reports the URL of the PAC file, but it does not download the file.</span></span>

</dd> <dt>

[<span data-ttu-id="f5d9e-122">**WinHttpFreeProxyResult**</span><span class="sxs-lookup"><span data-stu-id="f5d9e-122">**WinHttpFreeProxyResult**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpfreeproxyresult)
</dt> <dd>

<span data-ttu-id="f5d9e-123">Libera i dati recuperati da una chiamata precedente a [**WinHttpGetProxyResult.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult)</span><span class="sxs-lookup"><span data-stu-id="f5d9e-123">Frees the data retrieved from a previous call to [**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult).</span></span>

</dd> <dt>

[<span data-ttu-id="f5d9e-124">**WinHttpFreeQueryConnectionGroupResult**</span><span class="sxs-lookup"><span data-stu-id="f5d9e-124">**WinHttpFreeQueryConnectionGroupResult**</span></span>](/windows/win32/api/Winhttp/nf-winhttp-winhttpfreequeryconnectiongroupresult)
</dt> <dd>

<span data-ttu-id="f5d9e-125">Libera la memoria allocata da una chiamata precedente a [WinHttpQueryConnectionGroup.](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryconnectiongroup)</span><span class="sxs-lookup"><span data-stu-id="f5d9e-125">Frees the memory allocated by a previous call to [WinHttpQueryConnectionGroup](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryconnectiongroup).</span></span>

</dd> <dt>

[<span data-ttu-id="f5d9e-126">**WinHttpGetDefaultProxyConfiguration**</span><span class="sxs-lookup"><span data-stu-id="f5d9e-126">**WinHttpGetDefaultProxyConfiguration**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetdefaultproxyconfiguration)
</dt> <dd>

<span data-ttu-id="f5d9e-127">Recupera la configurazione del proxy WinHTTP predefinita dal Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="f5d9e-127">Retrieves the default WinHTTP proxy configuration from the registry.</span></span>

</dd> <dt>

[<span data-ttu-id="f5d9e-128">**WinHTTPGetIeProxyConfigForCurrentUser**</span><span class="sxs-lookup"><span data-stu-id="f5d9e-128">**WinHTTPGetIEProxyConfigForCurrentUser**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser)
</dt> <dd>

<span data-ttu-id="f5d9e-129">Ottiene la configurazione Internet Explorer proxy (IE) per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="f5d9e-129">Obtains the Internet Explorer (IE) proxy configuration for the current user.</span></span>

</dd> <dt>

[<span data-ttu-id="f5d9e-130">**WinHttpGetProxyForUrl**</span><span class="sxs-lookup"><span data-stu-id="f5d9e-130">**WinHttpGetProxyForUrl**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl)
</dt> <dd>

<span data-ttu-id="f5d9e-131">Recupera le informazioni proxy per l'URL specificato.</span><span class="sxs-lookup"><span data-stu-id="f5d9e-131">Retrieves the proxy information for the specified URL.</span></span>

</dd> <dt>

[<span data-ttu-id="f5d9e-132">**WinHttpGetProxyForUrlEx**</span><span class="sxs-lookup"><span data-stu-id="f5d9e-132">**WinHttpGetProxyForUrlEx**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex)
</dt> <dd>

<span data-ttu-id="f5d9e-133">Recupera le informazioni proxy per l'URL specificato.</span><span class="sxs-lookup"><span data-stu-id="f5d9e-133">Retrieves the proxy information for the specified URL.</span></span>

</dd> <dt>

[<span data-ttu-id="f5d9e-134">**WinHttpGetProxyResult**</span><span class="sxs-lookup"><span data-stu-id="f5d9e-134">**WinHttpGetProxyResult**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult)
</dt> <dd>

<span data-ttu-id="f5d9e-135">Recupera i risultati di una chiamata a [**WinHttpGetProxyForUrlEx.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex)</span><span class="sxs-lookup"><span data-stu-id="f5d9e-135">Retrieves the results of a call to [**WinHttpGetProxyForUrlEx**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex).</span></span>

</dd> <dt>

[<span data-ttu-id="f5d9e-136">**WinHttpOpen**</span><span class="sxs-lookup"><span data-stu-id="f5d9e-136">**WinHttpOpen**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen)
</dt> <dd>

<span data-ttu-id="f5d9e-137">Inizializza l'uso delle funzioni WinHTTP da parte di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f5d9e-137">Initializes an application's use of the WinHTTP functions.</span></span>

</dd> <dt>

[<span data-ttu-id="f5d9e-138">**WinHttpOpenRequest**</span><span class="sxs-lookup"><span data-stu-id="f5d9e-138">**WinHttpOpenRequest**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)
</dt> <dd>

<span data-ttu-id="f5d9e-139">Crea un handle di richiesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="f5d9e-139">Creates an HTTP request handle.</span></span>

</dd> <dt>

[<span data-ttu-id="f5d9e-140">**WinHttpQueryAuthSchemes**</span><span class="sxs-lookup"><span data-stu-id="f5d9e-140">**WinHttpQueryAuthSchemes**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes)
</dt> <dd>

<span data-ttu-id="f5d9e-141">Restituisce gli schemi di autorizzazione supportati dal server.</span><span class="sxs-lookup"><span data-stu-id="f5d9e-141">Returns the authorization schemes that the server supports.</span></span>

</dd> <dt>

[<span data-ttu-id="f5d9e-142">**WinHttpQueryConnectionGroup**</span><span class="sxs-lookup"><span data-stu-id="f5d9e-142">**WinHttpQueryConnectionGroup**</span></span>](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryconnectiongroup)
</dt> <dd>

<span data-ttu-id="f5d9e-143">Recupera una descrizione dello stato corrente delle connessioni di WinHttp.</span><span class="sxs-lookup"><span data-stu-id="f5d9e-143">Retrieves a description of the current state of WinHttp's connections.</span></span>

</dd> <dt>

[<span data-ttu-id="f5d9e-144">**WinHttpQueryDataAvailable**</span><span class="sxs-lookup"><span data-stu-id="f5d9e-144">**WinHttpQueryDataAvailable**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable)
</dt> <dd>

<span data-ttu-id="f5d9e-145">Restituisce il numero di byte di dati immediatamente disponibili per la lettura [**con WinHttpReadData.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata)</span><span class="sxs-lookup"><span data-stu-id="f5d9e-145">Returns the number of bytes of data that are available immediately to be read with [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata).</span></span>

</dd> <dt>

[<span data-ttu-id="f5d9e-146">**WinHttpQueryHeaders**</span><span class="sxs-lookup"><span data-stu-id="f5d9e-146">**WinHttpQueryHeaders**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders)
</dt> <dd>

<span data-ttu-id="f5d9e-147">Recupera le informazioni di intestazione associate a una richiesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="f5d9e-147">Retrieves header information associated with an HTTP request.</span></span>

</dd> <dt>

[<span data-ttu-id="f5d9e-148">**WinHttpQueryOption**</span><span class="sxs-lookup"><span data-stu-id="f5d9e-148">**WinHttpQueryOption**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)
</dt> <dd>

<span data-ttu-id="f5d9e-149">Esegue una query su un'opzione Internet sull'handle specificato.</span><span class="sxs-lookup"><span data-stu-id="f5d9e-149">Queries an Internet option on the specified handle.</span></span>

</dd> <dt>

[<span data-ttu-id="f5d9e-150">**WinHttpReadData**</span><span class="sxs-lookup"><span data-stu-id="f5d9e-150">**WinHttpReadData**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata)
</dt> <dd>

<span data-ttu-id="f5d9e-151">Legge i dati da un handle aperto dalla [**funzione WinHttpOpenRequest.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)</span><span class="sxs-lookup"><span data-stu-id="f5d9e-151">Reads data from a handle opened by the [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) function.</span></span>

</dd> <dt>

[<span data-ttu-id="f5d9e-152">**WinHttpReceiveResponse**</span><span class="sxs-lookup"><span data-stu-id="f5d9e-152">**WinHttpReceiveResponse**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse)
</dt> <dd>

<span data-ttu-id="f5d9e-153">Termina una richiesta HTTP avviata da [**WinHttpSendRequest.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)</span><span class="sxs-lookup"><span data-stu-id="f5d9e-153">Ends an HTTP request that is initiated by [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span>

</dd> <dt>

[<span data-ttu-id="f5d9e-154">**WinHttpResetAutoProxy**</span><span class="sxs-lookup"><span data-stu-id="f5d9e-154">**WinHttpResetAutoProxy**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpresetautoproxy)
</dt> <dd>

<span data-ttu-id="f5d9e-155">Reimposta il proxy automatico.</span><span class="sxs-lookup"><span data-stu-id="f5d9e-155">Resets the auto-proxy.</span></span>

</dd> <dt>

[<span data-ttu-id="f5d9e-156">**WinHttpSendRequest**</span><span class="sxs-lookup"><span data-stu-id="f5d9e-156">**WinHttpSendRequest**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)
</dt> <dd>

<span data-ttu-id="f5d9e-157">Invia la richiesta specificata al server HTTP.</span><span class="sxs-lookup"><span data-stu-id="f5d9e-157">Sends the specified request to the HTTP server.</span></span>

</dd> <dt>

[<span data-ttu-id="f5d9e-158">**WinHttpSetCredentials**</span><span class="sxs-lookup"><span data-stu-id="f5d9e-158">**WinHttpSetCredentials**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials)
</dt> <dd>

<span data-ttu-id="f5d9e-159">Passa le credenziali di autorizzazione necessarie al server.</span><span class="sxs-lookup"><span data-stu-id="f5d9e-159">Passes the required authorization credentials to the server.</span></span>

</dd> <dt>

[<span data-ttu-id="f5d9e-160">**WinHttpSetDefaultProxyConfiguration**</span><span class="sxs-lookup"><span data-stu-id="f5d9e-160">**WinHttpSetDefaultProxyConfiguration**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetdefaultproxyconfiguration)
</dt> <dd>

<span data-ttu-id="f5d9e-161">Imposta la configurazione predefinita del proxy WinHTTP nel Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="f5d9e-161">Sets the default WinHTTP proxy configuration in the registry.</span></span>

</dd> <dt>

[<span data-ttu-id="f5d9e-162">**WinHttpSetOption**</span><span class="sxs-lookup"><span data-stu-id="f5d9e-162">**WinHttpSetOption**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)
</dt> <dd>

<span data-ttu-id="f5d9e-163">Imposta un'opzione Internet.</span><span class="sxs-lookup"><span data-stu-id="f5d9e-163">Sets an Internet option.</span></span>

</dd> <dt>

[<span data-ttu-id="f5d9e-164">**WinHttpSetStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="f5d9e-164">**WinHttpSetStatusCallback**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback)
</dt> <dd>

<span data-ttu-id="f5d9e-165">Configura una funzione di callback che WinHTTP può chiamare quando viene effettuato lo stato di avanzamento durante un'operazione.</span><span class="sxs-lookup"><span data-stu-id="f5d9e-165">Sets up a callback function that WinHTTP can call as progress is made during an operation.</span></span>

</dd> <dt>

[<span data-ttu-id="f5d9e-166">**WinHttpSetTimeouts**</span><span class="sxs-lookup"><span data-stu-id="f5d9e-166">**WinHttpSetTimeouts**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts)
</dt> <dd>

<span data-ttu-id="f5d9e-167">Imposta i vari timeout coinvolti nelle transazioni HTTP.</span><span class="sxs-lookup"><span data-stu-id="f5d9e-167">Sets the various time-outs that are involved with HTTP transactions.</span></span>

</dd> <dt>

[<span data-ttu-id="f5d9e-168">**WinHttpTimeFromSystemTime**</span><span class="sxs-lookup"><span data-stu-id="f5d9e-168">**WinHttpTimeFromSystemTime**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttptimefromsystemtime)
</dt> <dd>

<span data-ttu-id="f5d9e-169">Formatta una data e un'ora in base alla specifica HTTP versione 1.0.</span><span class="sxs-lookup"><span data-stu-id="f5d9e-169">Formats a date and time according to the HTTP version 1.0 specification.</span></span>

</dd> <dt>

[<span data-ttu-id="f5d9e-170">**WinHttpTimeToSystemTime**</span><span class="sxs-lookup"><span data-stu-id="f5d9e-170">**WinHttpTimeToSystemTime**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttptimetosystemtime)
</dt> <dd>

<span data-ttu-id="f5d9e-171">Accetta una stringa di data/ora HTTP e la converte in [**una struttura SYSTEMTIME.**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)</span><span class="sxs-lookup"><span data-stu-id="f5d9e-171">Takes an HTTP time/date string and converts it to a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure.</span></span>

</dd> <dt>

[<span data-ttu-id="f5d9e-172">**WinHttpWriteData**</span><span class="sxs-lookup"><span data-stu-id="f5d9e-172">**WinHttpWriteData**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata)
</dt> <dd>

<span data-ttu-id="f5d9e-173">Scrive i dati della richiesta in un server HTTP.</span><span class="sxs-lookup"><span data-stu-id="f5d9e-173">Writes request data to an HTTP server.</span></span>

</dd> <dt>

[<span data-ttu-id="f5d9e-174">**WinHttpWebSocketClose**</span><span class="sxs-lookup"><span data-stu-id="f5d9e-174">**WinHttpWebSocketClose**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketclose)
</dt> <dd>

<span data-ttu-id="f5d9e-175">Chiude una connessione WebSocket.</span><span class="sxs-lookup"><span data-stu-id="f5d9e-175">Closes a WebSocket connection.</span></span>

</dd> <dt>

[<span data-ttu-id="f5d9e-176">**WinHttpWebSocketCompleteUpgrade**</span><span class="sxs-lookup"><span data-stu-id="f5d9e-176">**WinHttpWebSocketCompleteUpgrade**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketcompleteupgrade)
</dt> <dd>

<span data-ttu-id="f5d9e-177">Completa un handshake WebSocket avviato da [**WinHttpSendRequest.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)</span><span class="sxs-lookup"><span data-stu-id="f5d9e-177">Completes a WebSocket handshake started by [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span>

</dd> <dt>

[<span data-ttu-id="f5d9e-178">**WinHttpWebSocketQueryCloseStatus**</span><span class="sxs-lookup"><span data-stu-id="f5d9e-178">**WinHttpWebSocketQueryCloseStatus**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketqueryclosestatus)
</dt> <dd>

<span data-ttu-id="f5d9e-179">Ottiene lo stato di chiusura inviato da un server.</span><span class="sxs-lookup"><span data-stu-id="f5d9e-179">Gets the close status sent by a server.</span></span>

</dd> <dt>

[<span data-ttu-id="f5d9e-180">**WinHttpWebSocketReceive**</span><span class="sxs-lookup"><span data-stu-id="f5d9e-180">**WinHttpWebSocketReceive**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketreceive)
</dt> <dd>

<span data-ttu-id="f5d9e-181">Riceve dati da una connessione WebSocket.</span><span class="sxs-lookup"><span data-stu-id="f5d9e-181">Receives data from a WebSocket connection.</span></span>

</dd> <dt>

[<span data-ttu-id="f5d9e-182">**WinHttpWebSocketSend**</span><span class="sxs-lookup"><span data-stu-id="f5d9e-182">**WinHttpWebSocketSend**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketsend)
</dt> <dd>

<span data-ttu-id="f5d9e-183">Invia dati tramite una connessione WebSocket.</span><span class="sxs-lookup"><span data-stu-id="f5d9e-183">Sends data over a WebSocket connection.</span></span>

</dd> <dt>

[<span data-ttu-id="f5d9e-184">**WinHttpWebSocketShutdown**</span><span class="sxs-lookup"><span data-stu-id="f5d9e-184">**WinHttpWebSocketShutdown**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketshutdown)
</dt> <dd>

<span data-ttu-id="f5d9e-185">Invia un frame di chiusura a una connessione WebSocket.</span><span class="sxs-lookup"><span data-stu-id="f5d9e-185">Sends a close frame to a WebSocket connection.</span></span>

</dd> </dl>

 

 
