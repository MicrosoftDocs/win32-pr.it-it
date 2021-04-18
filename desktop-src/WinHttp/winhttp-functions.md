---
description: In questo argomento vengono identificate le funzioni fornite da WinHTTP.
ms.assetid: dcb56d5d-ed0d-49bb-95bf-940a49c033f1
title: Funzioni WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6511d2e66acc923072cc7a961aae3cb572b8e466
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307101"
---
# <a name="winhttp-functions"></a><span data-ttu-id="03605-103">Funzioni WinHTTP</span><span class="sxs-lookup"><span data-stu-id="03605-103">WinHTTP Functions</span></span>

<span data-ttu-id="03605-104">WinHTTP fornisce le funzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="03605-104">WinHTTP provides the following functions:</span></span>

<dl> <dt>

[<span data-ttu-id="03605-105">**WinHttpAddRequestHeaders**</span><span class="sxs-lookup"><span data-stu-id="03605-105">**WinHttpAddRequestHeaders**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)
</dt> <dd>

<span data-ttu-id="03605-106">Aggiunge una o più intestazioni di richiesta HTTP all'handle della richiesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="03605-106">Adds one or more HTTP request headers to the HTTP request handle.</span></span>

</dd> <dt>

[<span data-ttu-id="03605-107">**WinHttpCheckPlatform**</span><span class="sxs-lookup"><span data-stu-id="03605-107">**WinHttpCheckPlatform**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcheckplatform)
</dt> <dd>

<span data-ttu-id="03605-108">Determina se la piattaforma corrente è supportata da WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="03605-108">Determines whether the current platform is supported by WinHTTP.</span></span>

</dd> <dt>

[<span data-ttu-id="03605-109">**WinHttpCloseHandle**</span><span class="sxs-lookup"><span data-stu-id="03605-109">**WinHttpCloseHandle**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpclosehandle)
</dt> <dd>

<span data-ttu-id="03605-110">Chiude un singolo handle [HINTERNET](hinternet-handles-in-winhttp.md) .</span><span class="sxs-lookup"><span data-stu-id="03605-110">Closes a single [HINTERNET](hinternet-handles-in-winhttp.md) handle.</span></span>

</dd> <dt>

[<span data-ttu-id="03605-111">**WinHttpConnect**</span><span class="sxs-lookup"><span data-stu-id="03605-111">**WinHttpConnect**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect)
</dt> <dd>

<span data-ttu-id="03605-112">Specifica il server di destinazione iniziale di una richiesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="03605-112">Specifies the initial target server of an HTTP request.</span></span>

</dd> <dt>

[<span data-ttu-id="03605-113">**WinHttpCrackUrl**</span><span class="sxs-lookup"><span data-stu-id="03605-113">**WinHttpCrackUrl**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl)
</dt> <dd>

<span data-ttu-id="03605-114">Separa un URL nelle parti del componente, ad esempio il nome host e il percorso.</span><span class="sxs-lookup"><span data-stu-id="03605-114">Separates a URL into its component parts, for example, host name and path.</span></span>

</dd> <dt>

[<span data-ttu-id="03605-115">**WinHttpCreateProxyResolver**</span><span class="sxs-lookup"><span data-stu-id="03605-115">**WinHttpCreateProxyResolver**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateproxyresolver)
</dt> <dd>

<span data-ttu-id="03605-116">Crea un handle per l'uso da [**WinHttpGetProxyForUrlEx**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex).</span><span class="sxs-lookup"><span data-stu-id="03605-116">Creates a handle for use by [**WinHttpGetProxyForUrlEx**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex).</span></span>

</dd> <dt>

[<span data-ttu-id="03605-117">**WinHttpCreateUrl**</span><span class="sxs-lookup"><span data-stu-id="03605-117">**WinHttpCreateUrl**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl)
</dt> <dd>

<span data-ttu-id="03605-118">Crea un URL dalle parti del componente, ad esempio il nome host e il percorso.</span><span class="sxs-lookup"><span data-stu-id="03605-118">Creates a URL from component parts, for example, the host name and path.</span></span>

</dd> <dt>

[<span data-ttu-id="03605-119">**WinHttpDetectAutoProxyConfigUrl**</span><span class="sxs-lookup"><span data-stu-id="03605-119">**WinHttpDetectAutoProxyConfigUrl**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl)
</dt> <dd>

<span data-ttu-id="03605-120">Trova l'URL per il file di configurazione automatica del proxy (PAC).</span><span class="sxs-lookup"><span data-stu-id="03605-120">Finds the URL for the Proxy Auto-Configuration (PAC) file.</span></span> <span data-ttu-id="03605-121">Questa funzione segnala l'URL del file PAC, ma il file non viene scaricato.</span><span class="sxs-lookup"><span data-stu-id="03605-121">This function reports the URL of the PAC file, but it does not download the file.</span></span>

</dd> <dt>

[<span data-ttu-id="03605-122">**WinHttpFreeProxyResult**</span><span class="sxs-lookup"><span data-stu-id="03605-122">**WinHttpFreeProxyResult**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpfreeproxyresult)
</dt> <dd>

<span data-ttu-id="03605-123">Libera i dati recuperati da una chiamata precedente a [**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult).</span><span class="sxs-lookup"><span data-stu-id="03605-123">Frees the data retrieved from a previous call to [**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult).</span></span>

</dd> <dt>

[<span data-ttu-id="03605-124">**WinHttpGetDefaultProxyConfiguration**</span><span class="sxs-lookup"><span data-stu-id="03605-124">**WinHttpGetDefaultProxyConfiguration**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetdefaultproxyconfiguration)
</dt> <dd>

<span data-ttu-id="03605-125">Recupera la configurazione predefinita del proxy WinHTTP dal registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="03605-125">Retrieves the default WinHTTP proxy configuration from the registry.</span></span>

</dd> <dt>

[<span data-ttu-id="03605-126">**WinHTTPGetIEProxyConfigForCurrentUser**</span><span class="sxs-lookup"><span data-stu-id="03605-126">**WinHTTPGetIEProxyConfigForCurrentUser**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser)
</dt> <dd>

<span data-ttu-id="03605-127">Ottiene la configurazione del proxy Internet Explorer (IE) per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="03605-127">Obtains the Internet Explorer (IE) proxy configuration for the current user.</span></span>

</dd> <dt>

[<span data-ttu-id="03605-128">**WinHttpGetProxyForUrl**</span><span class="sxs-lookup"><span data-stu-id="03605-128">**WinHttpGetProxyForUrl**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl)
</dt> <dd>

<span data-ttu-id="03605-129">Recupera le informazioni sul proxy per l'URL specificato.</span><span class="sxs-lookup"><span data-stu-id="03605-129">Retrieves the proxy information for the specified URL.</span></span>

</dd> <dt>

[<span data-ttu-id="03605-130">**WinHttpGetProxyForUrlEx**</span><span class="sxs-lookup"><span data-stu-id="03605-130">**WinHttpGetProxyForUrlEx**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex)
</dt> <dd>

<span data-ttu-id="03605-131">Recupera le informazioni sul proxy per l'URL specificato.</span><span class="sxs-lookup"><span data-stu-id="03605-131">Retrieves the proxy information for the specified URL.</span></span>

</dd> <dt>

[<span data-ttu-id="03605-132">**WinHttpGetProxyResult**</span><span class="sxs-lookup"><span data-stu-id="03605-132">**WinHttpGetProxyResult**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult)
</dt> <dd>

<span data-ttu-id="03605-133">Recupera i risultati di una chiamata a [**WinHttpGetProxyForUrlEx**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex).</span><span class="sxs-lookup"><span data-stu-id="03605-133">Retrieves the results of a call to [**WinHttpGetProxyForUrlEx**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex).</span></span>

</dd> <dt>

[<span data-ttu-id="03605-134">**WinHttpOpen**</span><span class="sxs-lookup"><span data-stu-id="03605-134">**WinHttpOpen**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen)
</dt> <dd>

<span data-ttu-id="03605-135">Inizializza l'utilizzo delle funzioni WinHTTP da parte di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="03605-135">Initializes an application's use of the WinHTTP functions.</span></span>

</dd> <dt>

[<span data-ttu-id="03605-136">**WinHttpOpenRequest**</span><span class="sxs-lookup"><span data-stu-id="03605-136">**WinHttpOpenRequest**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)
</dt> <dd>

<span data-ttu-id="03605-137">Crea un handle di richiesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="03605-137">Creates an HTTP request handle.</span></span>

</dd> <dt>

[<span data-ttu-id="03605-138">**WinHttpQueryAuthSchemes**</span><span class="sxs-lookup"><span data-stu-id="03605-138">**WinHttpQueryAuthSchemes**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes)
</dt> <dd>

<span data-ttu-id="03605-139">Restituisce gli schemi di autorizzazione supportati dal server.</span><span class="sxs-lookup"><span data-stu-id="03605-139">Returns the authorization schemes that the server supports.</span></span>

</dd> <dt>

[<span data-ttu-id="03605-140">**WinHttpQueryDataAvailable**</span><span class="sxs-lookup"><span data-stu-id="03605-140">**WinHttpQueryDataAvailable**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable)
</dt> <dd>

<span data-ttu-id="03605-141">Restituisce il numero di byte di dati disponibili immediatamente per la lettura con [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata).</span><span class="sxs-lookup"><span data-stu-id="03605-141">Returns the number of bytes of data that are available immediately to be read with [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata).</span></span>

</dd> <dt>

[<span data-ttu-id="03605-142">**WinHttpQueryHeaders**</span><span class="sxs-lookup"><span data-stu-id="03605-142">**WinHttpQueryHeaders**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders)
</dt> <dd>

<span data-ttu-id="03605-143">Recupera le informazioni di intestazione associate a una richiesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="03605-143">Retrieves header information associated with an HTTP request.</span></span>

</dd> <dt>

[<span data-ttu-id="03605-144">**WinHttpQueryOption**</span><span class="sxs-lookup"><span data-stu-id="03605-144">**WinHttpQueryOption**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)
</dt> <dd>

<span data-ttu-id="03605-145">Esegue una query su un'opzione Internet nell'handle specificato.</span><span class="sxs-lookup"><span data-stu-id="03605-145">Queries an Internet option on the specified handle.</span></span>

</dd> <dt>

[<span data-ttu-id="03605-146">**WinHttpReadData**</span><span class="sxs-lookup"><span data-stu-id="03605-146">**WinHttpReadData**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata)
</dt> <dd>

<span data-ttu-id="03605-147">Legge i dati da un handle aperto dalla funzione [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) .</span><span class="sxs-lookup"><span data-stu-id="03605-147">Reads data from a handle opened by the [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) function.</span></span>

</dd> <dt>

[<span data-ttu-id="03605-148">**WinHttpReceiveResponse**</span><span class="sxs-lookup"><span data-stu-id="03605-148">**WinHttpReceiveResponse**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse)
</dt> <dd>

<span data-ttu-id="03605-149">Termina una richiesta HTTP avviata da [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span><span class="sxs-lookup"><span data-stu-id="03605-149">Ends an HTTP request that is initiated by [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span>

</dd> <dt>

[<span data-ttu-id="03605-150">**WinHttpResetAutoProxy**</span><span class="sxs-lookup"><span data-stu-id="03605-150">**WinHttpResetAutoProxy**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpresetautoproxy)
</dt> <dd>

<span data-ttu-id="03605-151">Reimposta il proxy automatico.</span><span class="sxs-lookup"><span data-stu-id="03605-151">Resets the auto-proxy.</span></span>

</dd> <dt>

[<span data-ttu-id="03605-152">**WinHttpSendRequest**</span><span class="sxs-lookup"><span data-stu-id="03605-152">**WinHttpSendRequest**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)
</dt> <dd>

<span data-ttu-id="03605-153">Invia la richiesta specificata al server HTTP.</span><span class="sxs-lookup"><span data-stu-id="03605-153">Sends the specified request to the HTTP server.</span></span>

</dd> <dt>

[<span data-ttu-id="03605-154">**WinHttpSetCredentials**</span><span class="sxs-lookup"><span data-stu-id="03605-154">**WinHttpSetCredentials**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials)
</dt> <dd>

<span data-ttu-id="03605-155">Passa le credenziali di autorizzazione necessarie al server.</span><span class="sxs-lookup"><span data-stu-id="03605-155">Passes the required authorization credentials to the server.</span></span>

</dd> <dt>

[<span data-ttu-id="03605-156">**WinHttpSetDefaultProxyConfiguration**</span><span class="sxs-lookup"><span data-stu-id="03605-156">**WinHttpSetDefaultProxyConfiguration**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetdefaultproxyconfiguration)
</dt> <dd>

<span data-ttu-id="03605-157">Imposta la configurazione predefinita del proxy WinHTTP nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="03605-157">Sets the default WinHTTP proxy configuration in the registry.</span></span>

</dd> <dt>

[<span data-ttu-id="03605-158">**WinHttpSetOption**</span><span class="sxs-lookup"><span data-stu-id="03605-158">**WinHttpSetOption**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)
</dt> <dd>

<span data-ttu-id="03605-159">Imposta un'opzione Internet.</span><span class="sxs-lookup"><span data-stu-id="03605-159">Sets an Internet option.</span></span>

</dd> <dt>

[<span data-ttu-id="03605-160">**WinHttpSetStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="03605-160">**WinHttpSetStatusCallback**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback)
</dt> <dd>

<span data-ttu-id="03605-161">Imposta una funzione di callback che può essere chiamata da WinHTTP come avanzamento durante un'operazione.</span><span class="sxs-lookup"><span data-stu-id="03605-161">Sets up a callback function that WinHTTP can call as progress is made during an operation.</span></span>

</dd> <dt>

[<span data-ttu-id="03605-162">**WinHttpSetTimeouts**</span><span class="sxs-lookup"><span data-stu-id="03605-162">**WinHttpSetTimeouts**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts)
</dt> <dd>

<span data-ttu-id="03605-163">Imposta i diversi timeout che interessano le transazioni HTTP.</span><span class="sxs-lookup"><span data-stu-id="03605-163">Sets the various time-outs that are involved with HTTP transactions.</span></span>

</dd> <dt>

[<span data-ttu-id="03605-164">**WinHttpTimeFromSystemTime**</span><span class="sxs-lookup"><span data-stu-id="03605-164">**WinHttpTimeFromSystemTime**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttptimefromsystemtime)
</dt> <dd>

<span data-ttu-id="03605-165">Formatta una data e un'ora in base alla specifica HTTP versione 1,0.</span><span class="sxs-lookup"><span data-stu-id="03605-165">Formats a date and time according to the HTTP version 1.0 specification.</span></span>

</dd> <dt>

[<span data-ttu-id="03605-166">**WinHttpTimeToSystemTime**</span><span class="sxs-lookup"><span data-stu-id="03605-166">**WinHttpTimeToSystemTime**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttptimetosystemtime)
</dt> <dd>

<span data-ttu-id="03605-167">Accetta una stringa di data/ora HTTP e la converte in una struttura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) .</span><span class="sxs-lookup"><span data-stu-id="03605-167">Takes an HTTP time/date string and converts it to a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure.</span></span>

</dd> <dt>

[<span data-ttu-id="03605-168">**WinHttpWriteData**</span><span class="sxs-lookup"><span data-stu-id="03605-168">**WinHttpWriteData**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata)
</dt> <dd>

<span data-ttu-id="03605-169">Scrive i dati della richiesta in un server HTTP.</span><span class="sxs-lookup"><span data-stu-id="03605-169">Writes request data to an HTTP server.</span></span>

</dd> <dt>

[<span data-ttu-id="03605-170">**WinHttpWebSocketClose**</span><span class="sxs-lookup"><span data-stu-id="03605-170">**WinHttpWebSocketClose**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketclose)
</dt> <dd>

<span data-ttu-id="03605-171">Chiude una connessione WebSocket.</span><span class="sxs-lookup"><span data-stu-id="03605-171">Closes a WebSocket connection.</span></span>

</dd> <dt>

[<span data-ttu-id="03605-172">**WinHttpWebSocketCompleteUpgrade**</span><span class="sxs-lookup"><span data-stu-id="03605-172">**WinHttpWebSocketCompleteUpgrade**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketcompleteupgrade)
</dt> <dd>

<span data-ttu-id="03605-173">Completa un handshake WebSocket avviato da [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span><span class="sxs-lookup"><span data-stu-id="03605-173">Completes a WebSocket handshake started by [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span>

</dd> <dt>

[<span data-ttu-id="03605-174">**WinHttpWebSocketQueryCloseStatus**</span><span class="sxs-lookup"><span data-stu-id="03605-174">**WinHttpWebSocketQueryCloseStatus**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketqueryclosestatus)
</dt> <dd>

<span data-ttu-id="03605-175">Ottiene lo stato di chiusura inviato da un server.</span><span class="sxs-lookup"><span data-stu-id="03605-175">Gets the close status sent by a server.</span></span>

</dd> <dt>

[<span data-ttu-id="03605-176">**WinHttpWebSocketReceive**</span><span class="sxs-lookup"><span data-stu-id="03605-176">**WinHttpWebSocketReceive**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketreceive)
</dt> <dd>

<span data-ttu-id="03605-177">Riceve i dati da una connessione WebSocket.</span><span class="sxs-lookup"><span data-stu-id="03605-177">Receives data from a WebSocket connection.</span></span>

</dd> <dt>

[<span data-ttu-id="03605-178">**WinHttpWebSocketSend**</span><span class="sxs-lookup"><span data-stu-id="03605-178">**WinHttpWebSocketSend**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketsend)
</dt> <dd>

<span data-ttu-id="03605-179">Invia dati tramite una connessione WebSocket.</span><span class="sxs-lookup"><span data-stu-id="03605-179">Sends data over a WebSocket connection.</span></span>

</dd> <dt>

[<span data-ttu-id="03605-180">**WinHttpWebSocketShutdown**</span><span class="sxs-lookup"><span data-stu-id="03605-180">**WinHttpWebSocketShutdown**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketshutdown)
</dt> <dd>

<span data-ttu-id="03605-181">Invia un frame di chiusura a una connessione WebSocket.</span><span class="sxs-lookup"><span data-stu-id="03605-181">Sends a close frame to a WebSocket connection.</span></span>

</dd> </dl>

 

 
