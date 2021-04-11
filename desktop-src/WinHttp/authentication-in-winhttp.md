---
description: Alcuni server e proxy HTTP richiedono l'autenticazione prima di consentire l'accesso alle risorse su Internet. Le funzioni dei servizi HTTP di Microsoft Windows (WinHTTP) supportano l'autenticazione del server e del proxy per le sessioni HTTP.
ms.assetid: 077d6275-8600-4091-b78e-419a41a2101a
title: Autenticazione in WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dd40e6da1f455e04e24fa740cf4d83da7e0472e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231676"
---
# <a name="authentication-in-winhttp"></a>Autenticazione in WinHTTP

Alcuni server e proxy HTTP richiedono l'autenticazione prima di consentire l'accesso alle risorse su Internet. Le funzioni dei servizi HTTP di Microsoft Windows (WinHTTP) supportano l'autenticazione del server e del proxy per le sessioni HTTP.

## <a name="about-http-authentication"></a>Informazioni sull'autenticazione HTTP

Se è richiesta l'autenticazione, l'applicazione HTTP riceve un codice di stato 401 (il server richiede l'autenticazione) o 407 (il proxy richiede l'autenticazione). Oltre al codice di stato, il proxy o il server invia una o più intestazioni di autenticazione: WWW-Authenticate (per l'autenticazione del server) o Proxy-Authenticate (per l'autenticazione del proxy).

Ogni intestazione Authenticate contiene uno schema di autenticazione supportato e, per gli schemi di base e del digest, un'area di autenticazione. Se sono supportati più schemi di autenticazione, il server restituisce più intestazioni di autenticazione. Il valore dell'area di autenticazione fa distinzione tra maiuscole e minuscole e definisce un set di server o proxy per i quali vengono accettate le stesse credenziali. Ad esempio, è possibile che venga restituita l'intestazione "WWW-Authenticate: Basic realm =" example "" quando è richiesta l'autenticazione server. Questa intestazione specifica che è necessario fornire le credenziali utente per il dominio "example".

Un'applicazione HTTP può includere un campo di intestazione dell'autorizzazione con una richiesta inviata al server. L'intestazione Authorization contiene lo schema di autenticazione e la risposta appropriata richiesta da tale schema. Ad esempio, l'intestazione "Authorization: Basic <username: password>" viene aggiunta alla richiesta e inviata al server se il client ha ricevuto l'intestazione della risposta "WWW-Authenticate: Basic realm =" example "".

> [!Note]  
> Sebbene siano visualizzati come testo normale, il nome utente e la password sono in realtà [*codificati con Base64*](glossary.md).

 

Esistono due tipi generali di schemi di autenticazione:

-   Schema di autenticazione di base, in cui il nome utente e la password vengono inviati in testo non crittografato al server.

    Lo schema di autenticazione di base è basato sul modello che deve essere identificato da un client con un nome utente e una password per ogni area di autenticazione. Il server Servizi la richiesta solo se la richiesta viene inviata con un'intestazione di autorizzazione che include un nome utente e una password validi.

-   Schemi di richiesta-risposta, ad esempio Kerberos, in cui il server sfida il client con i [*dati di autenticazione*](glossary.md). Il client trasforma i dati con le credenziali utente e invia di nuovo i dati trasformati al server per l'autenticazione.

    Gli schemi di richiesta-risposta consentono un'autenticazione più sicura. In uno schema di richiesta-risposta, il nome utente e la password non vengono mai trasmessi in rete. Quando il client seleziona uno schema di richiesta-risposta, il server restituisce un codice di stato appropriato con una richiesta di verifica che contiene i [*dati di autenticazione*](glossary.md) per tale schema. Il client invia nuovamente la richiesta con la risposta appropriata per ottenere il servizio richiesto. Gli schemi di richiesta-risposta possono richiedere più scambi per il completamento.

Nella tabella seguente sono inclusi gli schemi di autenticazione supportati da WinHTTP, il tipo di autenticazione e una descrizione dello schema.



| Schema            | Tipo               | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Di base (testo non crittografato) | Basic              | Usa una stringa [*con codifica Base64*](glossary.md) che contiene il nome utente e la password.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Digest            | Richiesta-risposta | Problemi di utilizzo di un valore nonce (una stringa di dati specificata dal server). Una risposta valida contiene un checksum del nome utente, la password, il valore nonce specificato, il [*verbo http*](glossary.md)e l'URI (Uniform Resource Identifier richiesto).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| NTLM              | Richiesta-risposta | Richiede la trasformazione [*dei dati di autenticazione*](glossary.md) con le credenziali utente per dimostrare l'identità. Per il corretto funzionamento dell'autenticazione NTLM, è necessario eseguire diversi scambi nella stessa connessione. Pertanto, non è possibile usare l'autenticazione NTLM se un proxy corrispondente non supporta le connessioni keep-alive. L'autenticazione NTLM ha esito negativo anche se [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) viene usato con il flag di [**\_ disabilitazione \_ Keep \_**](option-flags.md) -Alive WinHTTP che disabilita la semantica Keep-Alive.                                                                                                                                                                                                                                       |
| Passport          | Richiesta-risposta | USA [Microsoft Passport 1,4](passport-authentication-in-winhttp.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Negotiate         | Richiesta-risposta | Se il server e il client utilizzano Windows 2000 o versione successiva, viene utilizzata l'autenticazione Kerberos. In caso contrario, viene utilizzata l'autenticazione NTLM. Kerberos è disponibile in Windows 2000 e nei sistemi operativi successivi ed è considerato più sicuro rispetto all'autenticazione NTLM. Per il corretto funzionamento dell'autenticazione Negotiate, è necessario eseguire diversi scambi nella stessa connessione. Di conseguenza, non è possibile usare l'autenticazione Negotiate se un proxy corrispondente non supporta le connessioni keep-alive. L'autenticazione Negotiate ha esito negativo anche se [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) viene usato con il flag di [**\_ disabilitazione \_ Keep \_ Alive di WinHTTP**](option-flags.md) che disabilita la semantica Keep-Alive. Lo schema di autenticazione Negotiate viene talvolta definito autenticazione integrata di Windows. |



 

## <a name="authentication-in-winhttp-applications"></a>Autenticazione nelle applicazioni WinHTTP

Il Application Programming Interface WinHTTP (API) fornisce due funzioni usate per accedere alle risorse Internet nelle situazioni in cui è richiesta l'autenticazione: [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) e [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes).

Quando viene ricevuta una risposta con un codice di stato 401 o 407, è possibile usare [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes) per analizzare le intestazioni di autenticazione per determinare gli schemi di autenticazione supportati e la destinazione di autenticazione. La destinazione di autenticazione è il server o il proxy che richiede l'autenticazione. **WinHttpQueryAuthSchemes** determina anche il primo schema di autenticazione, dagli schemi disponibili, in base alle preferenze dello schema di autenticazione suggerite dal server. Questo metodo per la scelta di uno schema di autenticazione è il comportamento suggerito da [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).

[**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) consente a un'applicazione di specificare lo schema di autenticazione utilizzato insieme a un nome utente e una password validi per l'utilizzo nel server o nel proxy di destinazione. Dopo aver impostato le credenziali e inviato nuovamente la richiesta, le intestazioni necessarie vengono generate e aggiunte automaticamente alla richiesta. Poiché alcuni schemi di autenticazione richiedono più transazioni, [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) potrebbe restituire l'errore \_ . errore WinHTTP: \_ Invia nuovamente la \_ richiesta. Quando si verifica questo errore, l'applicazione deve continuare a inviare nuovamente la richiesta fino a quando non viene ricevuta una risposta che non contiene un codice di stato 401 o 407. Un codice di stato 200 indica che la risorsa è disponibile e che la richiesta ha avuto esito positivo. Per ulteriori codici di stato che possono essere restituiti, vedere [**codici di stato http**](http-status-codes.md) .

Se uno schema di autenticazione accettabile e le credenziali sono note prima dell'invio di una richiesta al server, un'applicazione può chiamare [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) prima di chiamare [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest). In questo caso, WinHTTP tenta di pre-eseguire l'autenticazione con il server fornendo le credenziali o i [*dati di autenticazione*](glossary.md) nella richiesta iniziale al server. La pre-autenticazione può ridurre il numero di scambi nel processo di autenticazione e quindi migliorare le prestazioni dell'applicazione.

La preautenticazione può essere utilizzata con gli schemi di autenticazione seguenti:

-   Basic: sempre possibile.
-   Negoziare la risoluzione in Kerberos: molto probabilmente possibile; l'unica eccezione è rappresentata dal caso in cui le sfasamento temporali siano disattivate tra il client e il controller di dominio.
-   (Negoziazione della risoluzione in NTLM): mai possibile.
-   NTLM: possibile solo in Windows Server 2008 R2.
-   Digest: mai possibile.
-   Passport: mai possibile; Dopo la richiesta di risposta iniziale, WinHTTP usa i cookie per eseguire la pre-autenticazione a Passport.

Una tipica applicazione WinHTTP completa i passaggi seguenti per gestire l'autenticazione.

-   Richiedere una risorsa con [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) e [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).
-   Controllare le intestazioni della risposta con [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders).
-   Se viene restituito un codice di stato 401 o 407 che indica che è richiesta l'autenticazione, chiamare [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes) per trovare uno schema accettabile.
-   Impostare lo schema di autenticazione, il nome utente e la password con [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials).
-   Inviare di nuovo la richiesta con lo stesso handle di richiesta chiamando [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).

Le credenziali impostate da [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) vengono usate solo per una richiesta. WinHTTP non memorizza nella cache le credenziali da usare in altre richieste, il che significa che le applicazioni devono essere scritte in grado di rispondere a più richieste. Se viene riutilizzata una connessione autenticata, altre richieste potrebbero non essere richieste, ma il codice deve essere in grado di rispondere a una richiesta in qualsiasi momento.

### <a name="example-retrieving-a-document"></a>Esempio: recupero di un documento

Il codice di esempio seguente tenta di recuperare un documento specificato da un server HTTP. Il codice di stato viene recuperato dalla risposta per determinare se l'autenticazione è obbligatoria. Se viene trovato un codice di stato 200, il documento sarà disponibile. Se viene trovato un codice di stato 401 o 407, è necessaria l'autenticazione prima di poter recuperare il documento. Per qualsiasi altro codice di stato, viene visualizzato un messaggio di errore. Per un elenco di possibili codici di stato, vedere [**codici di stato http**](http-status-codes.md) .


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



## <a name="automatic-logon-policy"></a>Criteri di accesso automatici

Il criterio di accesso automatico (accesso automatico) determina quando è accettabile che WinHTTP includa le credenziali predefinite in una richiesta. Le credenziali predefinite sono il token del thread corrente o il token di sessione, a seconda che WinHTTP venga utilizzato in modalità sincrona o asincrona. Il token del thread viene usato in modalità sincrona e il token di sessione viene usato in modalità asincrona. Queste credenziali predefinite sono spesso il nome utente e la password utilizzati per accedere a Microsoft Windows.

Il criterio di accesso automatico è stato implementato per impedire che queste credenziali vengano usate in modo casuale per l'autenticazione in un server non attendibile. Per impostazione predefinita, il livello di sicurezza è impostato su WINHTTP \_ AUTOlogod \_ Security \_ level \_ media, che consente di utilizzare le credenziali predefinite solo per le richieste Intranet. Il criterio di accesso automatico si applica solo agli schemi di autenticazione NTLM e Negotiate. Le credenziali non vengono mai trasmesse automaticamente con altri schemi.

È possibile impostare i criteri di accesso automatico usando la funzione [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) con il flag di [**\_ \_ \_ criteri AutoLogon dell'opzione WinHTTP**](option-flags.md) . Questo flag si applica solo all'handle della richiesta. Quando il criterio è impostato sul livello di sicurezza con accesso \_ automatico WinHTTP \_ \_ \_ basso, le credenziali predefinite possono essere inviate a tutti i server. Quando il criterio è impostato sul \_ livello di sicurezza automatico WinHTTP- \_ \_ \_ alto, le credenziali predefinite non possono essere usate per l'autenticazione. Si consiglia vivamente di utilizzare l'accesso automatico a livello medio.

## <a name="stored-user-names-and-passwords"></a>Gestione nomi utente e password archiviati

In Windows XP è stato introdotto il concetto di nomi utente e password archiviati. Se le credenziali Passport di un utente vengono salvate tramite la **registrazione guidata Passport** o la **finestra di dialogo credenziali** standard, vengono salvate in nomi utente e password archiviati. Quando si usa WinHTTP in Windows XP o versioni successive, WinHTTP usa automaticamente le credenziali nei nomi utente e nelle password archiviati se le credenziali non sono impostate in modo esplicito. Questa operazione è simile a quella del supporto per le credenziali di accesso predefinite per NTLM/Kerberos. Tuttavia, l'utilizzo delle credenziali Passport predefinite non è soggetto alle impostazioni dei criteri di accesso automatico.

 

 



