---
description: Alcuni server e proxy HTTP richiedono l'autenticazione prima di consentire l'accesso alle risorse su Internet. Le funzioni dei servizi HTTP di Microsoft Windows (WinHTTP) supportano l'autenticazione server e proxy per le sessioni HTTP.
ms.assetid: 077d6275-8600-4091-b78e-419a41a2101a
title: Autenticazione in WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a75c6703e9d28902c5705f0b8ab8433193c4d085
ms.sourcegitcommit: 59ec383331366f8a62c94bb88468ca03e95c43f8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/13/2021
ms.locfileid: "107380827"
---
# <a name="authentication-in-winhttp"></a>Autenticazione in WinHTTP

Alcuni server e proxy HTTP richiedono l'autenticazione prima di consentire l'accesso alle risorse su Internet. Le funzioni dei servizi HTTP di Microsoft Windows (WinHTTP) supportano l'autenticazione server e proxy per le sessioni HTTP.

## <a name="about-http-authentication"></a>Informazioni sull'autenticazione HTTP

Se è necessaria l'autenticazione, l'applicazione HTTP riceve il codice di stato 401 (il server richiede l'autenticazione) o 407 (il proxy richiede l'autenticazione). Insieme al codice di stato, il proxy o il server invia una o più intestazioni di autenticazione: WWW-Authenticate (per l'autenticazione server) o Proxy-Authenticate (per l'autenticazione proxy).

Ogni intestazione di autenticazione contiene uno schema di autenticazione supportato e, per gli schemi Basic e Digest, un'area di autenticazione. Se sono supportati più schemi di autenticazione, il server restituisce più intestazioni di autenticazione. Il valore dell'area di autenticazione fa distinzione tra maiuscole e minuscole e definisce un set di server o proxy per i quali vengono accettate le stesse credenziali. Ad esempio, l'intestazione "WWW-Authenticate: Basic Realm="example"" potrebbe essere restituita quando è necessaria l'autenticazione del server. Questa intestazione specifica che le credenziali utente devono essere fornite per il dominio "example".

Un'applicazione HTTP può includere un campo di intestazione di autorizzazione con una richiesta inviata al server. L'intestazione dell'autorizzazione contiene lo schema di autenticazione e la risposta appropriata richiesta da tale schema. Ad esempio, l'intestazione "Authorization: Basic " verrebbe aggiunta alla richiesta e inviata al server se il client ricevesse l'intestazione di risposta \<username:password> "WWW-Authenticate: Basic Realm="example"".

> [!Note]  
> Anche se vengono visualizzati come testo normale, il nome utente e la password sono in realtà [*codificati in base 64.*](glossary.md)

 

Esistono due tipi generali di schemi di autenticazione:

-   Schema di autenticazione di base, in cui il nome utente e la password vengono inviati in testo non crittografato al server.

    Lo schema di autenticazione di base si basa sul modello che un client deve identificare con un nome utente e una password per ogni area di autenticazione. Il server servizi la richiesta solo se la richiesta viene inviata con un'intestazione di autorizzazione che include un nome utente e una password validi.

-   Schemi challenge-response, ad esempio Kerberos, in cui il server sfida il client con i [*dati di autenticazione*](glossary.md). Il client trasforma i dati con le credenziali utente e li invia al server per l'autenticazione.

    Gli schemi challenge-response consentono un'autenticazione più sicura. In uno schema challenge-response il nome utente e la password non vengono mai trasmessi in rete. Dopo che il client ha selezionato uno schema challenge-response, il server restituisce un codice di stato appropriato con una richiesta contenente i dati [*di*](glossary.md) autenticazione per tale schema. Il client invia quindi nuovamente la richiesta con la risposta appropriata per ottenere il servizio richiesto. Gli schemi challenge-response possono richiedere più scambi per il completamento.

La tabella seguente contiene gli schemi di autenticazione supportati da WinHTTP, il tipo di autenticazione e una descrizione dello schema.



| Schema            | Tipo               | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Basic (testo non crittografato) | Basic              | Usa una [*stringa con codifica Base64*](glossary.md) che contiene il nome utente e la password.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Digest            | Risposta alla richiesta di richiesta | Problemi relativi all'uso di un valore nonce (una stringa di dati specificata dal server). Una risposta valida contiene un checksum del nome utente, della password, del valore nonce specificato, del [*verbo HTTP*](glossary.md)e del Uniform Resource Identifier (URI).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| NTLM              | Risposta alla richiesta di richiesta | Richiede che [*i dati di autenticazione*](glossary.md) siano trasformati con le credenziali utente per dimostrare l'identità. Per il corretto funzionamento dell'autenticazione NTLM, è necessario eseguire diversi scambi nella stessa connessione. Pertanto, l'autenticazione NTLM non può essere usata se un proxy interviene non supporta le connessioni keep-alive. L'autenticazione NTLM ha esito negativo anche se [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) viene usato con il flag [**WINHTTP \_ DISABLE KEEP \_ \_ ALIVE**](option-flags.md) che disabilita la semantica keep-alive.                                                                                                                                                                                                                                       |
| Passport          | Risposta alla richiesta di sfida | Usa [Microsoft Passport 1.4.](passport-authentication-in-winhttp.md)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Negotiate         | Risposta alla richiesta di richiesta | Se sia il server che il client usano Windows 2000 o versione successiva, viene usata l'autenticazione Kerberos. In caso contrario, viene usata l'autenticazione NTLM. Kerberos è disponibile nei sistemi operativi Windows 2000 e versioni successive ed è considerato più sicuro dell'autenticazione NTLM. Per il corretto funzionamento dell'autenticazione negotiate, è necessario che nella stessa connessione vengano evasi diversi scambi. Pertanto, l'autenticazione Negotiate non può essere utilizzata se un proxy non supporta le connessioni keep-alive. L'autenticazione negotiate ha esito negativo anche se [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) viene usato con il flag [**WINHTTP \_ DISABLE KEEP \_ \_ ALIVE**](option-flags.md) che disabilita la semantica keep-alive. Lo schema di autenticazione Negotiate viene talvolta chiamato integrated autenticazione di Windows. |



 

## <a name="authentication-in-winhttp-applications"></a>Autenticazione nelle applicazioni WinHTTP

L'API (Application Programming Interface) WinHTTP fornisce due funzioni usate per accedere alle risorse Internet nelle situazioni in cui è necessaria l'autenticazione: [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) e [**WinHttpQueryAuthSchemes.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes)

Quando si riceve una risposta con un codice di stato 401 o 407, è possibile usare [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes) per analizzare le intestazioni di autenticazione per determinare gli schemi di autenticazione supportati e la destinazione dell'autenticazione. La destinazione dell'autenticazione è il server o il proxy che richiede l'autenticazione. **WinHttpQueryAuthSchemes** determina anche il primo schema di autenticazione, dagli schemi disponibili, in base alle preferenze dello schema di autenticazione suggerite dal server. Questo metodo per la scelta di uno schema di autenticazione è il comportamento suggerito da [RFC 2616.](https://www.ietf.org/rfc/rfc2616.txt)

[**WinHttpSetCredentials consente**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) a un'applicazione di specificare lo schema di autenticazione usato insieme a un nome utente e una password validi da usare nel server o nel proxy di destinazione. Dopo aver impostato le credenziali e aver reinviato la richiesta, le intestazioni necessarie vengono generate e aggiunte automaticamente alla richiesta. Poiché alcuni schemi di autenticazione richiedono più [**transazioni, WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) potrebbe restituire l'errore ERROR \_ WINHTTP \_ RESEND \_ REQUEST. Quando viene rilevato questo errore, l'applicazione deve continuare a inviare nuovamente la richiesta fino a quando non viene ricevuta una risposta che non contiene un codice di stato 401 o 407. Un codice di stato 200 indica che la risorsa è disponibile e che la richiesta ha esito positivo. Per altri codici di stato che possono essere restituiti, vedere Codici di stato [**HTTP.**](http-status-codes.md)

Se uno schema di autenticazione e credenziali accettabili sono noti prima dell'invio di una richiesta al server, un'applicazione può chiamare [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) prima di [**chiamare WinHttpSendRequest.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) In questo caso, WinHTTP tenta di eseguire la pre-autenticazione con il server fornendo credenziali o dati di [*autenticazione*](glossary.md) nella richiesta iniziale al server. La pre-autenticazione può ridurre il numero di scambi nel processo di autenticazione e quindi migliorare le prestazioni dell'applicazione.

La preautenticazione può essere usata con gli schemi di autenticazione seguenti:

-   Di base: sempre possibile.
-   Negoziazione della risoluzione in Kerberos- molto probabilmente possibile; l'unica eccezione si verifica quando le differenze di tempo sono disattivate tra il client e il controller di dominio.
-   (Negoziazione della risoluzione in NTLM) - mai possibile.
-   NTLM: possibile solo in Windows Server 2008 R2.
-   Digest: mai possibile.
-   Passport: mai possibile; dopo la richiesta di verifica iniziale, WinHTTP usa i cookie per eseguire la pre-autenticazione in Passport.

Una tipica applicazione WinHTTP completa i passaggi seguenti per gestire l'autenticazione.

-   Richiedere una risorsa con [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) e [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).
-   Controllare le intestazioni della risposta [**con WinHttpQueryHeaders.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders)
-   Se viene restituito un codice di stato 401 o 407 che indica che l'autenticazione è necessaria, chiamare [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes) per trovare uno schema accettabile.
-   Impostare lo schema di autenticazione, il nome utente e la password [**con WinHttpSetCredentials.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials)
-   Inviare nuovamente la richiesta con lo stesso handle di richiesta chiamando [**WinHttpSendRequest.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)

Le credenziali impostate da [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) vengono usate solo per una richiesta. WinHTTP non memorizza nella cache le credenziali da usare in altre richieste, il che significa che è necessario scrivere applicazioni in grado di rispondere a più richieste. Se una connessione autenticata viene usata di nuovo, è possibile che non venga inviata una richiesta ad altre richieste, ma il codice dovrebbe essere in grado di rispondere a una richiesta in qualsiasi momento.

### <a name="example-retrieving-a-document"></a>Esempio: Recupero di un documento

Il codice di esempio seguente tenta di recuperare un documento specificato da un server HTTP. Il codice di stato viene recuperato dalla risposta per determinare se è necessaria l'autenticazione. Se viene trovato un codice di stato 200, il documento è disponibile. Se viene trovato un codice di stato 401 o 407, l'autenticazione è necessaria prima di poter recuperare il documento. Per qualsiasi altro codice di stato, viene visualizzato un messaggio di errore. Per un elenco dei possibili codici di stato, vedere Codici di stato [**HTTP.**](http-status-codes.md)


```C++
#include <windows.h>
#include <winhttp.h>
#include <stdio.h>

#pragma comment(lib, "winhttp.lib")

DWORD ChooseAuthScheme( DWORD dwSupportedSchemes )
{
  //  It is the server's responsibility only to accept 
  //  authentication schemes that provide a sufficient
  //  level of security to protect the servers resources.
  //
  //  The client is also obligated only to use an authentication
  //  scheme that adequately protects its username and password.
  //
  //  Thus, this sample code does not use Basic authentication  
  //  becaus Basic authentication exposes the client's username
  //  and password to anyone monitoring the connection.
  
  if( dwSupportedSchemes & WINHTTP_AUTH_SCHEME_NEGOTIATE )
    return WINHTTP_AUTH_SCHEME_NEGOTIATE;
  else if( dwSupportedSchemes & WINHTTP_AUTH_SCHEME_NTLM )
    return WINHTTP_AUTH_SCHEME_NTLM;
  else if( dwSupportedSchemes & WINHTTP_AUTH_SCHEME_PASSPORT )
    return WINHTTP_AUTH_SCHEME_PASSPORT;
  else if( dwSupportedSchemes & WINHTTP_AUTH_SCHEME_DIGEST )
    return WINHTTP_AUTH_SCHEME_DIGEST;
  else
    return 0;
}

struct SWinHttpSampleGet
{
  LPCWSTR szServer;
  LPCWSTR szPath;
  BOOL fUseSSL;
  LPCWSTR szServerUsername;
  LPCWSTR szServerPassword;
  LPCWSTR szProxyUsername;
  LPCWSTR szProxyPassword;
};

void WinHttpAuthSample( IN SWinHttpSampleGet *pGetRequest )
{
  DWORD dwStatusCode = 0;
  DWORD dwSupportedSchemes;
  DWORD dwFirstScheme;
  DWORD dwSelectedScheme;
  DWORD dwTarget;
  DWORD dwLastStatus = 0;
  DWORD dwSize = sizeof(DWORD);
  BOOL  bResults = FALSE;
  BOOL  bDone = FALSE;

  DWORD dwProxyAuthScheme = 0;
  HINTERNET  hSession = NULL, 
             hConnect = NULL,
             hRequest = NULL;

  // Use WinHttpOpen to obtain a session handle.
  hSession = WinHttpOpen( L"WinHTTP Example/1.0",  
                          WINHTTP_ACCESS_TYPE_DEFAULT_PROXY,
                          WINHTTP_NO_PROXY_NAME, 
                          WINHTTP_NO_PROXY_BYPASS, 0 );

  INTERNET_PORT nPort = ( pGetRequest->fUseSSL ) ? 
                        INTERNET_DEFAULT_HTTPS_PORT  :
                        INTERNET_DEFAULT_HTTP_PORT;

  // Specify an HTTP server.
  if( hSession )
    hConnect = WinHttpConnect( hSession, 
                               pGetRequest->szServer, 
                               nPort, 0 );

  // Create an HTTP request handle.
  if( hConnect )
    hRequest = WinHttpOpenRequest( hConnect, 
                                   L"GET", 
                                   pGetRequest->szPath,
                                   NULL, 
                                   WINHTTP_NO_REFERER, 
                                   WINHTTP_DEFAULT_ACCEPT_TYPES,
                                   ( pGetRequest->fUseSSL ) ? 
                                       WINHTTP_FLAG_SECURE : 0 );

  // Continue to send a request until status code 
  // is not 401 or 407.
  if( hRequest == NULL )
    bDone = TRUE;

  while( !bDone )
  {
    //  If a proxy authentication challenge was responded to, reset
    //  those credentials before each SendRequest, because the proxy  
    //  may require re-authentication after responding to a 401 or  
    //  to a redirect. If you don't, you can get into a 
    //  407-401-407-401- loop.
    if( dwProxyAuthScheme != 0 )
      bResults = WinHttpSetCredentials( hRequest, 
                                        WINHTTP_AUTH_TARGET_PROXY, 
                                        dwProxyAuthScheme, 
                                        pGetRequest->szProxyUsername,
                                        pGetRequest->szProxyPassword,
                                        NULL );
    // Send a request.
    bResults = WinHttpSendRequest( hRequest,
                                   WINHTTP_NO_ADDITIONAL_HEADERS,
                                   0,
                                   WINHTTP_NO_REQUEST_DATA,
                                   0, 
                                   0, 
                                   0 );

    // End the request.
    if( bResults )
      bResults = WinHttpReceiveResponse( hRequest, NULL );

    // Resend the request in case of 
    // ERROR_WINHTTP_RESEND_REQUEST error.
    if( !bResults && GetLastError( ) == ERROR_WINHTTP_RESEND_REQUEST)
        continue;

    // Check the status code.
    if( bResults ) 
      bResults = WinHttpQueryHeaders( hRequest, 
                                      WINHTTP_QUERY_STATUS_CODE |
                                      WINHTTP_QUERY_FLAG_NUMBER,
                                      NULL, 
                                      &dwStatusCode, 
                                      &dwSize, 
                                      NULL );

    if( bResults )
    {
      switch( dwStatusCode )
      {
        case 200: 
          // The resource was successfully retrieved.
          // You can use WinHttpReadData to read the 
          // contents of the server's response.
          printf( "The resource was successfully retrieved.\n" );
          bDone = TRUE;
          break;

        case 401:
          // The server requires authentication.
          printf(" The server requires authentication. Sending credentials...\n" );

          // Obtain the supported and preferred schemes.
          bResults = WinHttpQueryAuthSchemes( hRequest, 
                                              &dwSupportedSchemes, 
                                              &dwFirstScheme, 
                                              &dwTarget );

          // Set the credentials before resending the request.
          if( bResults )
          {
            dwSelectedScheme = ChooseAuthScheme( dwSupportedSchemes);

            if( dwSelectedScheme == 0 )
              bDone = TRUE;
            else
              bResults = WinHttpSetCredentials( hRequest, 
                                        dwTarget, 
                                        dwSelectedScheme,
                                        pGetRequest->szServerUsername,
                                        pGetRequest->szServerPassword,
                                        NULL );
          }

          // If the same credentials are requested twice, abort the
          // request.  For simplicity, this sample does not check
          // for a repeated sequence of status codes.
          if( dwLastStatus == 401 )
            bDone = TRUE;

          break;

        case 407:
          // The proxy requires authentication.
          printf( "The proxy requires authentication.  Sending credentials...\n" );

          // Obtain the supported and preferred schemes.
          bResults = WinHttpQueryAuthSchemes( hRequest, 
                                              &dwSupportedSchemes, 
                                              &dwFirstScheme, 
                                              &dwTarget );

          // Set the credentials before resending the request.
          if( bResults )
            dwProxyAuthScheme = ChooseAuthScheme(dwSupportedSchemes);

          // If the same credentials are requested twice, abort the
          // request.  For simplicity, this sample does not check 
          // for a repeated sequence of status codes.
          if( dwLastStatus == 407 )
            bDone = TRUE;
          break;

        default:
          // The status code does not indicate success.
          printf("Error. Status code %d returned.\n", dwStatusCode);
          bDone = TRUE;
      }
    }

    // Keep track of the last status code.
    dwLastStatus = dwStatusCode;

    // If there are any errors, break out of the loop.
    if( !bResults ) 
        bDone = TRUE;
  }

  // Report any errors.
  if( !bResults )
  {
    DWORD dwLastError = GetLastError( );
    printf( "Error %d has occurred.\n", dwLastError );
  }

  // Close any open handles.
  if( hRequest ) WinHttpCloseHandle( hRequest );
  if( hConnect ) WinHttpCloseHandle( hConnect );
  if( hSession ) WinHttpCloseHandle( hSession );
}

```



## <a name="automatic-logon-policy"></a>Criteri di accesso automatico

I criteri di accesso automatico (accesso automatico) determinano quando è accettabile che WinHTTP includa le credenziali predefinite in una richiesta. Le credenziali predefinite sono il token del thread corrente o il token di sessione a seconda che WinHTTP sia usato in modalità sincrona o asincrona. Il token del thread viene usato in modalità sincrona e il token di sessione viene usato in modalità asincrona. Queste credenziali predefinite sono spesso il nome utente e la password usati per accedere a Microsoft Windows.

I criteri di accesso automatico sono stati implementati per impedire l'uso casuale di queste credenziali per l'autenticazione in un server non attendibile. Per impostazione predefinita, il livello di sicurezza è impostato su WINHTTP \_ AUTOLOGON SECURITY LEVEL MEDIUM, che consente l'uso delle credenziali predefinite solo per \_ \_ le richieste \_ Intranet. I criteri di accesso automatico si applicano solo agli schemi di autenticazione NTLM e Negotiate. Le credenziali non vengono mai trasmesse automaticamente con altri schemi.

I criteri di accesso automatico possono essere impostati usando la [**funzione WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) con il flag [**WINHTTP \_ OPTION \_ AUTOLOGON \_ POLICY.**](option-flags.md) Questo flag si applica solo all'handle della richiesta. Quando il criterio è impostato su WINHTTP AUTOLOGON SECURITY LEVEL LOW, le credenziali predefinite \_ possono essere inviate a tutti i \_ \_ \_ server. Quando il criterio è impostato su WINHTTP \_ AUTOLOGON \_ SECURITY \_ LEVEL \_ HIGH, le credenziali predefinite non possono essere usate per l'autenticazione. È consigliabile usare l'accesso automatico a livello MEDIUM.

## <a name="stored-user-names-and-passwords"></a>Gestione nomi utente e password archiviati

Windows XP ha introdotto il concetto di nomi utente e password archiviati. Se le credenziali Passport di un utente vengono salvate tramite la **Registrazione** guidata passport o la finestra di dialogo delle credenziali **standard,** vengono salvate in Nomi utente e password archiviati. Quando si usa WinHTTP in Windows XP o versioni successive, WinHTTP usa automaticamente le credenziali in Nomi utente e password archiviati se le credenziali non sono impostate in modo esplicito. È simile al supporto delle credenziali di accesso predefinite per NTLM/Kerberos. Tuttavia, l'uso delle credenziali Passport predefinite non è soggetto alle impostazioni dei criteri di accesso automatico.

 

 



