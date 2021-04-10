---
description: WinHTTP implementa il protocollo WPAD utilizzando la funzione WinHttpGetProxyForUrl insieme a due funzioni di utilità di supporto, WinHttpDetectAutoProxyConfigUrl e WinHttpGetIEProxyConfigForCurrentUser.
ms.assetid: d941e3c6-c1db-4de1-b640-4f582f86fc54
title: Funzioni proxy AutoProxy WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afd4cf8289add4c72c2266df4bb9025e0b4c1aa0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966691"
---
# <a name="winhttp-autoproxy-functions"></a><span data-ttu-id="595fd-103">Funzioni proxy AutoProxy WinHTTP</span><span class="sxs-lookup"><span data-stu-id="595fd-103">WinHTTP AutoProxy Functions</span></span>

<span data-ttu-id="595fd-104">WinHTTP implementa il protocollo WPAD utilizzando la funzione [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) insieme a due funzioni di utilità di supporto, [**WinHttpDetectAutoProxyConfigUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) e [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser).</span><span class="sxs-lookup"><span data-stu-id="595fd-104">WinHTTP implements the WPAD protocol using the [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) function along with two supporting utility functions, [**WinHttpDetectAutoProxyConfigUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) and [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser).</span></span>

<span data-ttu-id="595fd-105">Il supporto di AutoProxy non è completamente integrato nello stack HTTP in WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="595fd-105">AutoProxy support is not fully integrated into the HTTP stack in WinHTTP.</span></span> <span data-ttu-id="595fd-106">Prima di inviare una richiesta, l'applicazione deve chiamare [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) per ottenere il nome di un server proxy e quindi chiamare [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) usando il **\_ \_ proxy di opzione WinHTTP** per impostare la configurazione del proxy sull'handle di richiesta WinHTTP creato da [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest).</span><span class="sxs-lookup"><span data-stu-id="595fd-106">Before sending a request, the application must call [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) to obtain the name of a proxy server and then call [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) using **WINHTTP\_OPTION\_PROXY** to set the proxy configuration on the WinHTTP request handle created by [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest).</span></span>

<span data-ttu-id="595fd-107">La funzione [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) può eseguire tutti e tre i passaggi del protocollo WPAD descritti nella panoramica precedente: (1) individuare l'URL del PAC, (2) scaricare il file di script PAC (3) eseguire il codice dello script e restituire la configurazione del proxy in una struttura di **\_ \_ informazioni proxy WinHTTP** .</span><span class="sxs-lookup"><span data-stu-id="595fd-107">The [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) function can execute all three steps of the WPAD protocol described in the previous overview: (1) discover the PAC URL, (2) download the PAC script file, (3) execute the script code and return the proxy configuration in a **WINHTTP\_PROXY\_INFO** structure.</span></span> <span data-ttu-id="595fd-108">Facoltativamente, se l'applicazione conosce in anticipo l'URL PAC, può specificarlo a **WinHttpGetProxyForUrl**.</span><span class="sxs-lookup"><span data-stu-id="595fd-108">Optionally, if the application knows in advance the PAC URL it can specify this to **WinHttpGetProxyForUrl**.</span></span>

<span data-ttu-id="595fd-109">Il codice di esempio seguente usa il proxy AutoProxy.</span><span class="sxs-lookup"><span data-stu-id="595fd-109">The following example code uses autoproxy.</span></span> <span data-ttu-id="595fd-110">Imposta una richiesta HTTP GET creando prima gli handle di connessione e di richiesta della sessione WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="595fd-110">It sets up an HTTP GET request by first creating the WinHTTP session connect and request handles.</span></span> <span data-ttu-id="595fd-111">La chiamata [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) specifica il **tipo di accesso WinHTTP \_ \_ \_ nessun \_ proxy** per la configurazione iniziale del proxy, per indicare che le richieste vengono inviate direttamente al server di destinazione per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="595fd-111">The [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) call specifies **WINHTTP\_ACCESS\_TYPE\_NO\_PROXY** for the initial proxy configuration, to indicate that requests are sent directly to the target server by default.</span></span> <span data-ttu-id="595fd-112">Utilizzando AutoProxy, viene quindi impostata la configurazione del proxy direttamente nell'handle della richiesta.</span><span class="sxs-lookup"><span data-stu-id="595fd-112">Using autoproxy, it then sets the proxy configuration directly on the request handle.</span></span>


```C++
  HINTERNET hHttpSession = NULL;
  HINTERNET hConnect     = NULL;
  HINTERNET hRequest     = NULL;
  
  WINHTTP_AUTOPROXY_OPTIONS  AutoProxyOptions;
  WINHTTP_PROXY_INFO         ProxyInfo;
  DWORD                      cbProxyInfoSize = sizeof(ProxyInfo);
  
  ZeroMemory( &AutoProxyOptions, sizeof(AutoProxyOptions) );
  ZeroMemory( &ProxyInfo, sizeof(ProxyInfo) );
  
//
// Create the WinHTTP session.
//
  hHttpSession = WinHttpOpen( L"WinHTTP AutoProxy Sample/1.0",
                              WINHTTP_ACCESS_TYPE_NO_PROXY,
                              WINHTTP_NO_PROXY_NAME,
                              WINHTTP_NO_PROXY_BYPASS,
                              0 );
  
// Exit if WinHttpOpen failed.
  if( !hHttpSession )
    goto Exit;
  
//
// Create the WinHTTP connect handle.
//
  hConnect = WinHttpConnect( hHttpSession,
                             L"www.microsoft.com",
                             INTERNET_DEFAULT_HTTP_PORT,
                             0 );
  
// Exit if WinHttpConnect failed.
  if( !hConnect )
    goto Exit;
  
//
// Create the HTTP request handle.
//
  hRequest = WinHttpOpenRequest( hConnect,
                                 L"GET",
                                 L"ms.htm",
                                 L"HTTP/1.1",
                                 WINHTTP_NO_REFERER,
                                 WINHTTP_DEFAULT_ACCEPT_TYPES,
                                 0 );
  
// Exit if WinHttpOpenRequest failed.
  if( !hRequest )
    goto Exit;
  
//
// Set up the autoproxy call.
//

// Use auto-detection because the Proxy 
// Auto-Config URL is not known.
  AutoProxyOptions.dwFlags = WINHTTP_AUTOPROXY_AUTO_DETECT;

// Use DHCP and DNS-based auto-detection.
  AutoProxyOptions.dwAutoDetectFlags = 
                             WINHTTP_AUTO_DETECT_TYPE_DHCP |
                             WINHTTP_AUTO_DETECT_TYPE_DNS_A;

// If obtaining the PAC script requires NTLM/Negotiate
// authentication, then automatically supply the client
// domain credentials.
  AutoProxyOptions.fAutoLogonIfChallenged = TRUE;

//
// Call WinHttpGetProxyForUrl with our target URL. If 
// auto-proxy succeeds, then set the proxy info on the 
// request handle. If auto-proxy fails, ignore the error 
// and attempt to send the HTTP request directly to the 
// target server (using the default WINHTTP_ACCESS_TYPE_NO_PROXY 
// configuration, which the requesthandle will inherit 
// from the session).
//
  if( WinHttpGetProxyForUrl( hHttpSession,
                             L"https://www.microsoft.com/ms.htm",
                             &AutoProxyOptions,
                             &ProxyInfo))
  {
  // A proxy configuration was found, set it on the
  // request handle.
    
    if( !WinHttpSetOption( hRequest, 
                           WINHTTP_OPTION_PROXY,
                           &ProxyInfo,
                           cbProxyInfoSize ) )
    {
      // Exit if setting the proxy info failed.
      goto Exit;
    }
  }

//
// Send the request.
//
  if( !WinHttpSendRequest( hRequest,
                           WINHTTP_NO_ADDITIONAL_HEADERS,
                           0,
                           WINHTTP_NO_REQUEST_DATA,
                           0,
                           0,
                           NULL ) )
  {
    // Exit if WinHttpSendRequest failed.
    goto Exit;
  }

//
// Wait for the response.
//

  if( !WinHttpReceiveResponse( hRequest, NULL ) )
    goto Exit;

//
// A response has been received, then process it.
// (omitted)
//


  Exit:
  //
  // Clean up the WINHTTP_PROXY_INFO structure.
  //
    if( ProxyInfo.lpszProxy != NULL )
      GlobalFree(ProxyInfo.lpszProxy);

    if( ProxyInfo.lpszProxyBypass != NULL )
      GlobalFree( ProxyInfo.lpszProxyBypass );

  //
  // Close the WinHTTP handles.
  //
    if( hRequest != NULL )
      WinHttpCloseHandle( hRequest );
  
    if( hConnect != NULL )
      WinHttpCloseHandle( hConnect );
  
    if( hHttpSession != NULL )
      WinHttpCloseHandle( hHttpSession );

```



<span data-ttu-id="595fd-113">Nel codice di esempio fornito, la chiamata a [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) indica alla funzione di individuare automaticamente il file di configurazione automatica del proxy specificando il flag di **\_ \_ \_ rilevamento automatico WinHTTP AutoProxy** nella struttura delle [**Opzioni del \_ proxy \_ automatico WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_autoproxy_options) .</span><span class="sxs-lookup"><span data-stu-id="595fd-113">In the provided example code, the call to [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) instructs the function to discover the proxy auto-config file automatically by specifying the **WINHTTP\_AUTOPROXY\_AUTO\_DETECT** flag in the [**WINHTTP\_AUTOPROXY\_OPTIONS**](/windows/win32/api/winhttp/ns-winhttp-winhttp_autoproxy_options) structure.</span></span> <span data-ttu-id="595fd-114">L'uso del flag di rilevamento **\_ \_ automatico \_ WinHTTP AutoProxy** richiede che il codice specifichi uno o entrambi i flag di rilevamento automatico (tipo di rilevamento automatico **WinHTTP \_ \_ \_ \_ DHCP**, **tipo di \_ rilevamento automatico WinHTTP, \_ \_ \_ DNS \_ A**).</span><span class="sxs-lookup"><span data-stu-id="595fd-114">Use of the **WINHTTP\_AUTOPROXY\_AUTO\_DETECT** flag requires the code to specify one or both of the auto-detection flags (**WINHTTP\_AUTO\_DETECT\_TYPE\_DHCP**, **WINHTTP\_AUTO\_DETECT\_TYPE\_DNS\_A**).</span></span> <span data-ttu-id="595fd-115">Il codice di esempio usa la funzionalità di rilevamento automatico di **WinHttpGetProxyForUrl** perché l'URL PAC non è noto in anticipo.</span><span class="sxs-lookup"><span data-stu-id="595fd-115">The example code uses the auto-detection feature of **WinHttpGetProxyForUrl** because the PAC URL is not known in advance.</span></span> <span data-ttu-id="595fd-116">Se non è possibile individuare un URL PAC sulla rete in questo scenario, **WinHttpGetProxyForUrl** ha esito negativo ([**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce l' **errore il \_ \_ rilevamento automatico WinHTTP \_ non è riuscito**).</span><span class="sxs-lookup"><span data-stu-id="595fd-116">If a PAC URL cannot be located on the network in this scenario, **WinHttpGetProxyForUrl** fails ([**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns **ERROR\_WINHTTP\_AUTODETECTION\_FAILED**).</span></span>

## <a name="if-the-pac-url-is-known-in-advance"></a><span data-ttu-id="595fd-117">Se l'URL PAC è noto in anticipo</span><span class="sxs-lookup"><span data-stu-id="595fd-117">If the PAC URL is Known in Advance</span></span>

<span data-ttu-id="595fd-118">Se l'applicazione conosce l'URL PAC, può specificarla nella struttura delle opzioni del \_ proxy \_ automatico WinHTTP e configurare [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) per ignorare la fase di rilevamento automatico.</span><span class="sxs-lookup"><span data-stu-id="595fd-118">If the application does know the PAC URL, it can specify it in the WINHTTP\_AUTOPROXY\_OPTIONS structure and configure [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) to skip the auto-detection phase.</span></span>

<span data-ttu-id="595fd-119">Se, ad esempio, un file PAC è disponibile nella rete locale all'URL " https://InternalSite/proxy-config.pac ", la chiamata a [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) avrà un aspetto simile al seguente.</span><span class="sxs-lookup"><span data-stu-id="595fd-119">For example, if a PAC file is available on the local network at the URL, "https://InternalSite/proxy-config.pac", the call to [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) would look the following.</span></span>


```C++
//
// Set up the autoproxy call.
//

// The proxy auto-config URL is known. Auto-detection
// is not required.
  AutoProxyOptions.dwFlags = WINHTTP_AUTOPROXY_CONFIG_URL;

// Set the proxy auto-config URL.
  AutoProxyOptions. lpszAutoConfigUrl =  L"https://InternalSite/proxy-config.pac";

// If obtaining the PAC script requires NTLM/Negotiate
// authentication, then automatically supply the client
// domain credentials.
  AutoProxyOptions.fAutoLogonIfChallenged = TRUE;

//
// Call WinHttpGetProxyForUrl with our target URL. If auto-proxy
// succeeds, then set the proxy info on the request handle.
// If auto-proxy fails, ignore the error and attempt to send the
// HTTP request directly to the target server (using the default
// WINHTTP_ACCESS_TYPE_NO_PROXY configuration, which the request
// handle will inherit from the session).
//
  if( WinHttpGetProxyForUrl( hHttpSession,
                             L"https://www.microsoft.com/ms.htm",
                             &AutoProxyOptions,
                             &ProxyInfo ) )
{
  //...

```



<span data-ttu-id="595fd-120">Se la struttura di [**\_ \_ Opzioni del proxy automatico WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_autoproxy_options) specifica sia il rilevamento automatico WinHTTP AutoProxy che i flag **\_ \_ \_ URL di configurazione AutoProxy** (e specifica i flag Detction automatici e un URL di configurazione automatica), [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) tenta innanzitutto il rilevamento automatico e quindi, se il rilevamento automatico non riesce a individuare un URL PAC, "esegue il fallback" all'URL di configurazione automatica fornito dall'applicazione. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="595fd-120">If the [**WINHTTP\_AUTOPROXY\_OPTIONS**](/windows/win32/api/winhttp/ns-winhttp-winhttp_autoproxy_options) structure specifies both **WINHTTP\_AUTOPROXY\_AUTO\_DETECT** and **WINHTTP\_AUTOPROXY\_CONFIG\_URL** flags (and specifies auto-detction flags and an auto-config URL), [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) first attempts auto-detection, and then, if auto-detection fails to locate a PAC URL, "falls back" to the auto-config URL supplied by the application.</span></span>

## <a name="the-winhttpdetectautoproxyconfigurl-function"></a><span data-ttu-id="595fd-121">Funzione WinHttpDetectAutoProxyConfigUrl</span><span class="sxs-lookup"><span data-stu-id="595fd-121">The WinHttpDetectAutoProxyConfigUrl Function</span></span>

<span data-ttu-id="595fd-122">La funzione [**WinHttpDetectAutoProxyConfigUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) implementa un subset del protocollo WPAD: tenta di rilevare automaticamente l'URL per il file di configurazione automatica del proxy, senza scaricare o eseguire il file PAC.</span><span class="sxs-lookup"><span data-stu-id="595fd-122">The [**WinHttpDetectAutoProxyConfigUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) function implements a subset of the WPAD protocol: it attempts to auto-detect the URL for the proxy auto-config file, without downloading or executing the PAC file.</span></span> <span data-ttu-id="595fd-123">Questa funzione è utile in situazioni speciali in cui un'applicazione client Web deve gestire il download e l'esecuzione del file PAC.</span><span class="sxs-lookup"><span data-stu-id="595fd-123">This function is useful in special situations where a Web client application must handle the download and execution of the PAC file itself.</span></span>

## <a name="the-winhttpgetieproxyconfigforcurrentuser-function"></a><span data-ttu-id="595fd-124">Funzione WinHttpGetIEProxyConfigForCurrentUser</span><span class="sxs-lookup"><span data-stu-id="595fd-124">The WinHttpGetIEProxyConfigForCurrentUser Function</span></span>

<span data-ttu-id="595fd-125">La funzione [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) restituisce le impostazioni proxy di Internet Explorer dell'utente corrente per la connessione di rete attiva corrente, senza chiamare "WinInet.dll".</span><span class="sxs-lookup"><span data-stu-id="595fd-125">The [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) function returns the current user Internet Explorer proxy settings for the current active network connection, without calling into "WinInet.dll".</span></span> <span data-ttu-id="595fd-126">Questa funzione è utile solo quando viene chiamata all'interno di un processo in esecuzione con un'identità di account utente interattiva, perché in caso contrario non è possibile che la configurazione del proxy di Internet Explorer sia disponibile.</span><span class="sxs-lookup"><span data-stu-id="595fd-126">This function is only useful when called within a process that is running under an interactive user account identity, because no Internet Explorer proxy configuration is likely to be available otherwise.</span></span> <span data-ttu-id="595fd-127">Non sarebbe utile, ad esempio, chiamare questa funzione da una DLL ISAPI in esecuzione nel processo del servizio IIS.</span><span class="sxs-lookup"><span data-stu-id="595fd-127">For example, it would not be useful to call this function from an ISAPI DLL running in the IIS service process.</span></span> <span data-ttu-id="595fd-128">Per ulteriori informazioni e uno scenario in cui un'applicazione basata su WinHTTP utilizzerebbe **WinHttpGetIEProxyConfigForCurrentUser**, vedere [individuazione senza un file di configurazione automatica](discovery-without-an-auto-config-file.md).</span><span class="sxs-lookup"><span data-stu-id="595fd-128">For more information and a scenario in which a WinHTTP-based application would use **WinHttpGetIEProxyConfigForCurrentUser**, see [Discovery Without an Auto-Config File](discovery-without-an-auto-config-file.md).</span></span>

 

 
