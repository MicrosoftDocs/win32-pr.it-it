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
# <a name="winhttp-autoproxy-functions"></a>Funzioni proxy AutoProxy WinHTTP

WinHTTP implementa il protocollo WPAD utilizzando la funzione [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) insieme a due funzioni di utilità di supporto, [**WinHttpDetectAutoProxyConfigUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) e [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser).

Il supporto di AutoProxy non è completamente integrato nello stack HTTP in WinHTTP. Prima di inviare una richiesta, l'applicazione deve chiamare [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) per ottenere il nome di un server proxy e quindi chiamare [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) usando il **\_ \_ proxy di opzione WinHTTP** per impostare la configurazione del proxy sull'handle di richiesta WinHTTP creato da [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest).

La funzione [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) può eseguire tutti e tre i passaggi del protocollo WPAD descritti nella panoramica precedente: (1) individuare l'URL del PAC, (2) scaricare il file di script PAC (3) eseguire il codice dello script e restituire la configurazione del proxy in una struttura di **\_ \_ informazioni proxy WinHTTP** . Facoltativamente, se l'applicazione conosce in anticipo l'URL PAC, può specificarlo a **WinHttpGetProxyForUrl**.

Il codice di esempio seguente usa il proxy AutoProxy. Imposta una richiesta HTTP GET creando prima gli handle di connessione e di richiesta della sessione WinHTTP. La chiamata [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) specifica il **tipo di accesso WinHTTP \_ \_ \_ nessun \_ proxy** per la configurazione iniziale del proxy, per indicare che le richieste vengono inviate direttamente al server di destinazione per impostazione predefinita. Utilizzando AutoProxy, viene quindi impostata la configurazione del proxy direttamente nell'handle della richiesta.


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



Nel codice di esempio fornito, la chiamata a [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) indica alla funzione di individuare automaticamente il file di configurazione automatica del proxy specificando il flag di **\_ \_ \_ rilevamento automatico WinHTTP AutoProxy** nella struttura delle [**Opzioni del \_ proxy \_ automatico WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_autoproxy_options) . L'uso del flag di rilevamento **\_ \_ automatico \_ WinHTTP AutoProxy** richiede che il codice specifichi uno o entrambi i flag di rilevamento automatico (tipo di rilevamento automatico **WinHTTP \_ \_ \_ \_ DHCP**, **tipo di \_ rilevamento automatico WinHTTP, \_ \_ \_ DNS \_ A**). Il codice di esempio usa la funzionalità di rilevamento automatico di **WinHttpGetProxyForUrl** perché l'URL PAC non è noto in anticipo. Se non è possibile individuare un URL PAC sulla rete in questo scenario, **WinHttpGetProxyForUrl** ha esito negativo ([**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce l' **errore il \_ \_ rilevamento automatico WinHTTP \_ non è riuscito**).

## <a name="if-the-pac-url-is-known-in-advance"></a>Se l'URL PAC è noto in anticipo

Se l'applicazione conosce l'URL PAC, può specificarla nella struttura delle opzioni del \_ proxy \_ automatico WinHTTP e configurare [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) per ignorare la fase di rilevamento automatico.

Se, ad esempio, un file PAC è disponibile nella rete locale all'URL " https://InternalSite/proxy-config.pac ", la chiamata a [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) avrà un aspetto simile al seguente.


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



Se la struttura di [**\_ \_ Opzioni del proxy automatico WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_autoproxy_options) specifica sia il rilevamento automatico WinHTTP AutoProxy che i flag **\_ \_ \_ URL di configurazione AutoProxy** (e specifica i flag Detction automatici e un URL di configurazione automatica), [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) tenta innanzitutto il rilevamento automatico e quindi, se il rilevamento automatico non riesce a individuare un URL PAC, "esegue il fallback" all'URL di configurazione automatica fornito dall'applicazione. **\_ \_ \_**

## <a name="the-winhttpdetectautoproxyconfigurl-function"></a>Funzione WinHttpDetectAutoProxyConfigUrl

La funzione [**WinHttpDetectAutoProxyConfigUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) implementa un subset del protocollo WPAD: tenta di rilevare automaticamente l'URL per il file di configurazione automatica del proxy, senza scaricare o eseguire il file PAC. Questa funzione è utile in situazioni speciali in cui un'applicazione client Web deve gestire il download e l'esecuzione del file PAC.

## <a name="the-winhttpgetieproxyconfigforcurrentuser-function"></a>Funzione WinHttpGetIEProxyConfigForCurrentUser

La funzione [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) restituisce le impostazioni proxy di Internet Explorer dell'utente corrente per la connessione di rete attiva corrente, senza chiamare "WinInet.dll". Questa funzione è utile solo quando viene chiamata all'interno di un processo in esecuzione con un'identità di account utente interattiva, perché in caso contrario non è possibile che la configurazione del proxy di Internet Explorer sia disponibile. Non sarebbe utile, ad esempio, chiamare questa funzione da una DLL ISAPI in esecuzione nel processo del servizio IIS. Per ulteriori informazioni e uno scenario in cui un'applicazione basata su WinHTTP utilizzerebbe **WinHttpGetIEProxyConfigForCurrentUser**, vedere [individuazione senza un file di configurazione automatica](discovery-without-an-auto-config-file.md).

 

 
