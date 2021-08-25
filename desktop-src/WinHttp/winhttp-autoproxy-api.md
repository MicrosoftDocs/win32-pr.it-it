---
description: WinHTTP implementa il protocollo WPAD usando la funzione WinHttpGetProxyForUrl insieme a due funzioni di utilità di supporto, WinHttpDetectAutoProxyConfigUrl e WinHttpGetIEProxyConfigForCurrentUser.
ms.assetid: d941e3c6-c1db-4de1-b640-4f582f86fc54
title: Funzioni del proxy automatico WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8443567e12d7a0f3b75d09fc284dc634315ec635ff8b630821bb84031e39781b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955711"
---
# <a name="winhttp-autoproxy-functions"></a>Funzioni del proxy automatico WinHTTP

WinHTTP implementa il protocollo WPAD usando la [**funzione WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) insieme a due funzioni di utilità di supporto, [**WinHttpDetectAutoProxyConfigUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) e [**WinHttpGetIEProxyConfigForCurrentUser.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser)

Il supporto di AutoProxy non è completamente integrato nello stack HTTP in WinHTTP. Prima di inviare una richiesta, l'applicazione deve chiamare [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) per ottenere il nome di un server proxy e quindi chiamare [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) usando **WINHTTP \_ OPTION \_ PROXY** per impostare la configurazione del proxy nell'handle di richiesta WinHTTP creato da [**WinHttpOpenRequest.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)

La funzione [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) può eseguire tutti e tre i passaggi del protocollo WPAD descritti nella panoramica precedente: (1) individuare l'URL PAC, (2) scaricare il file script PAC, (3) eseguire il codice script e restituire la configurazione del proxy in una struttura **WINHTTP \_ PROXY \_ INFO.** Facoltativamente, se l'applicazione riconosce in anticipo l'URL PAC, può specificare questo valore **in WinHttpGetProxyForUrl.**

Il codice di esempio seguente usa il proxy automatico. Configura una richiesta HTTP GET creando prima la connessione di sessione WinHTTP e gli handle di richiesta. La [**chiamata WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) specifica **WINHTTP ACCESS TYPE NO \_ \_ \_ \_ PROXY** per la configurazione iniziale del proxy, per indicare che le richieste vengono inviate direttamente al server di destinazione per impostazione predefinita. Usando il proxy automatico, imposta quindi la configurazione del proxy direttamente sull'handle della richiesta.


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



Nel codice di esempio fornito, la chiamata a [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) indica alla funzione di individuare automaticamente il file di configurazione automatica del proxy specificando il flag **AUTO \_ \_ \_ DETECT WINHTTP AUTOPROXY** nella struttura [**WINHTTP \_ AUTOPROXY \_ OPTIONS.**](/windows/win32/api/winhttp/ns-winhttp-winhttp_autoproxy_options) L'uso del flag **WINHTTP \_ AUTOPROXY \_ AUTO \_ DETECT** richiede al codice di specificare uno o entrambi i flag di rilevamento automatico (**WINHTTP \_ AUTO DETECT \_ TYPE \_ \_ DHCP,** **WINHTTP AUTO DETECT TYPE \_ \_ DNS \_ \_ \_ A**). Il codice di esempio usa la funzionalità di rilevamento automatico **di WinHttpGetProxyForUrl** perché l'URL PAC non è noto in anticipo. Se non è possibile trovare un URL PAC nella rete in questo scenario, **WinHttpGetProxyForUrl** ha esito negativo ([**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce **ERROR \_ WINHTTP \_ AUTODETECTION \_ FAILED**).

## <a name="if-the-pac-url-is-known-in-advance"></a>Se l'URL pac è noto in anticipo

Se l'applicazione conosce l'URL PAC, può specificarlo nella struttura WINHTTP AUTOPROXY OPTIONS e configurare \_ \_ [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) per ignorare la fase di rilevamento automatico.

Ad esempio, se un file PAC è disponibile nella rete locale all'URL " ", la chiamata a https://InternalSite/proxy-config.pac [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) sarà simile alla seguente.


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



Se la struttura [**WINHTTP \_ AUTOPROXY \_ OPTIONS**](/windows/win32/api/winhttp/ns-winhttp-winhttp_autoproxy_options) specifica entrambi i flag DI URL DI CONFIGURAZIONE **WINHTTP \_ AUTOPROXY \_ AUTO \_ DETECT** e **WINHTTP \_ AUTOPROXY \_ (e \_** specifica i flag di detzione automatica e un URL di configurazione automatica), [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) tenta prima il rilevamento automatico e quindi, se il rilevamento automatico non riesce a individuare un URL PAC, "esegue il fall back" all'URL di configurazione automatica fornito dall'applicazione.

## <a name="the-winhttpdetectautoproxyconfigurl-function"></a>Funzione WinHttpDetectAutoProxyConfigUrl

La funzione [**WinHttpDetectAutoProxyConfigUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) implementa un subset del protocollo WPAD: tenta di rilevare automaticamente l'URL per il file di configurazione automatica del proxy, senza scaricare o eseguire il file PAC. Questa funzione è utile in situazioni speciali in cui un'applicazione client Web deve gestire il download e l'esecuzione del file PAC stesso.

## <a name="the-winhttpgetieproxyconfigforcurrentuser-function"></a>Funzione WinHttpGetIeProxyConfigForCurrentUser

La [**funzione WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) restituisce l'utente corrente Internet Explorer impostazioni proxy per la connessione di rete attiva corrente, senza chiamare in "WinInet.dll". Questa funzione è utile solo quando viene chiamata all'interno di un processo in esecuzione con un'identità dell'account utente interattivo, perché è probabile che nessuna configurazione del proxy Internet Explorer disponibile in caso contrario. Ad esempio, non sarebbe utile chiamare questa funzione da una DLL ISAPI in esecuzione nel processo del servizio IIS. Per altre informazioni e uno scenario in cui un'applicazione basata su WinHTTP userebbe **WinHttpGetIEProxyConfigForCurrentUser,** vedere Individuazione senza un [file di configurazione automatica](discovery-without-an-auto-config-file.md).

 

 
