---
description: Questa sezione illustra come scrivere script che usa l'oggetto WinHttpRequest per accedere ai dati da un server che richiede l'autenticazione HTTP.
ms.assetid: 9e46777c-4d79-4f9b-9b31-1280ed1e3289
title: Autenticazione tramite script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 81e2dec50ccf765239bbbd1d6a71c8f8fb2be0e4f70f2db5717b0072f0b62d6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052099"
---
# <a name="authentication-using-script"></a>Autenticazione tramite script

Questa sezione illustra come scrivere script che usa [**l'oggetto WinHttpRequest**](winhttprequest.md) per accedere ai dati da un server che richiede l'autenticazione HTTP.

-   [Prerequisiti e requisiti](#prerequisites-and-requirements)
-   [Accesso a un sito Web con autenticazione](#accessing-a-web-site-with-authentication)
-   [Controllo dei codici di stato](#checking-the-status-codes)
-   [Argomenti correlati](#related-topics)

## <a name="prerequisites-and-requirements"></a>Prerequisiti e requisiti

Oltre a una conoscenza funzionante di Microsoft JScript, questo esempio richiede quanto segue:

-   Versione corrente di Microsoft Windows Software Development Kit (SDK).
-   Strumento di configurazione proxy per stabilire le impostazioni proxy per i servizi HTTP di Microsoft Windows (WinHTTP), se la connessione a Internet viene stabilita tramite un server proxy. Per [altre informazioni, vedereProxycfg.exe, uno strumento di configurazione proxy.](proxycfg-exe--a-proxy-configuration-tool.md)
-   Familiarità con la [terminologia e i concetti](network-terminology.md) della rete.

## <a name="accessing-a-web-site-with-authentication"></a>Accesso a un sito Web con autenticazione

**Per creare uno script che illustri l'autenticazione, eseguire le operazioni seguenti:**

1.  Aprire un editor di testo, ad esempio Microsoft Blocco note.
2.  Copiare il codice seguente nell'editor di testo dopo aver sostituito " authenticationSite " con il testo appropriato per specificare l'URL di un sito che \[ \] richiede l'autenticazione HTTP.

    ```VB
    // Load the WinHttpRequest object.
    var WinHttpReq = 
              new ActiveXObject("WinHttp.WinHttpRequest.5.1");

    function getText1( )
    {
      // Specify the target resource.
      WinHttpReq.open( "GET", 
                       "https://[authenticationSite]", 
                       false;

      // Send a request to the server and wait for a response.
      WinHttpReq.send( );

      // Display the results of the request.
      WScript.Echo( "No Credentials: " );
      WScript.Echo( WinHttpReq.Status + "   " + WinHttpReq.StatusText);
      WScript.Echo( WinHttpReq.GetAllResponseHeaders);
      WScript.Echo( );
    };

    function getText2( )
    {
      // HttpRequest SetCredentials flags
      HTTPREQUEST_SETCREDENTIALS_FOR_SERVER = 0;

      // Specify the target resource.
      WinHttpReq.open( "GET", 
                       "https://[authenticationSite]", 
                       false );

      // Set credentials for server.
      WinHttpReq.SetCredentials( "User Name", 
                                 "Password",
                                 HTTPREQUEST_SETCREDENTIALS_FOR_SERVER);

      // It might also be necessary to supply credentials 
      // to the proxy if you connect to the Internet 
      // through a proxy that requires authentication.

      // Send a request to the server and wait for 
      // a response.
      WinHttpReq.send( );

      // Display the results of the request.
      WScript.Echo( "Credentials: " );
      WScript.Echo( WinHttpReq.Status + "   " + WinHttpReq.StatusText );
      WScript.Echo( WinHttpReq.GetAllResponseHeaders( ) );
      WScript.Echo( );
    };

    getText1( );
    getText2( );
    ```

    

3.  Salvare il file come "Auth.js".
4.  Da un prompt dei comandi digitare "cscript Auth.js" e premere INVIO.

È ora disponibile un programma che richiede una risorsa in due modi diversi. Il primo metodo richiede la risorsa senza fornire credenziali. Viene restituito un codice di stato 401 per indicare che il server richiede l'autenticazione. Vengono visualizzate anche le intestazioni della risposta e dovrebbero essere simili alle seguenti:

``` syntax
Connection: Keep-Alive
Content-Length: 0
Date: Fri, 27 Apr 2001 01:47:18 GMT
Content-Type: text/html
Server: Microsoft-IIS/5.0
WWW-Authenticate: NTLM
WWW-Authenticate: Negotiate
Cache-control: private
```

Anche se la risposta indica che l'accesso alla risorsa è stato negato, restituisce comunque diverse intestazioni che forniscono alcune informazioni sulla risorsa. L'intestazione denominata "WWW-Authenticate" indica che il server richiede l'autenticazione per questa risorsa. Se fosse presente un'intestazione denominata "Proxy-Authenticate", indicherà che il server proxy richiede l'autenticazione. Ogni intestazione di autenticazione contiene uno schema di autenticazione disponibile e talvolta un'area di autenticazione. Il valore dell'area di autenticazione fa distinzione tra maiuscole e minuscole e definisce un set di server o proxy per cui devono essere accettate le stesse credenziali.

Sono disponibili due intestazioni denominate "WWW-Authenticate", che indicano che sono supportati più schemi di autenticazione. Se si chiama il [**metodo GetResponseHeader**](iwinhttprequest-getresponseheader.md) per trovare le intestazioni "WWW-Authenticate", il metodo restituisce solo il contenuto della prima intestazione di tale nome. In questo caso, restituisce il valore "NTLM". Per assicurarsi che tutte le occorrenze di un'intestazione vengano elaborate, usare invece il [**metodo GetAllResponseHeaders.**](iwinhttprequest-getallresponseheaders.md)

La seconda chiamata al metodo richiede la stessa risorsa, ma prima fornisce le credenziali di autenticazione chiamando il [**metodo SetCredentials.**](iwinhttprequest-setcredentials.md) La sezione di codice seguente illustra come viene usato questo metodo.


```VB
WinHttpReq.SetCredentials( "User Name", "Password",
                               HTTPREQUEST_SETCREDENTIALS_FOR_SERVER);
```



Questo metodo imposta il nome utente su "UserName", la password su "Password" e indica che le credenziali di autorizzazione si applicano al server di risorse. Le credenziali di autenticazione possono anche essere inviate a un proxy.

Quando vengono fornite le credenziali, il server restituisce un codice di stato 200 che indica che il documento può essere recuperato.

## <a name="checking-the-status-codes"></a>Controllo dei codici di stato

L'esempio precedente è informativo, ma richiede che l'utente fornisci in modo esplicito le credenziali. Un'applicazione che fornisce le credenziali quando è necessaria e non fornisce le credenziali quando non è necessaria è più utile. Per implementare una funzionalità che esegue questa operazione, è necessario modificare l'esempio per esaminare il codice di stato restituito con la risposta.

Per un elenco completo dei possibili codici di stato, insieme alle descrizioni, vedere [**Codici di stato HTTP**](http-status-codes.md). Per questo esempio, tuttavia, è necessario che si verifichi solo uno dei tre codici. Un codice di stato 200 indica che una risorsa è disponibile e viene inviata con la risposta. Il codice di stato 401 indica che il server richiede l'autenticazione. Un codice di stato 407 indica che il proxy richiede l'autenticazione.

Modificare l'esempio creato nell'ultima sezione sostituendo la funzione "getText2" con il codice seguente (sostituire " authenticationSite " con il proprio testo per specificare l'URL di un sito che richiede \[ \] l'autenticazione HTTP):


```VB
function getText2() {
  WScript.Echo( "Credentials: " );

  // HttpRequest SetCredentials flags.
  HTTPREQUEST_SETCREDENTIALS_FOR_SERVER = 0;
  HTTPREQUEST_SETCREDENTIALS_FOR_PROXY = 1;

  // Specify the target resource.
  var targURL = "https://[authenticationSite]";
  WinHttpReq.open( "GET", targURL, false );

  var Done = false;
  var Attempts = 0;
  do
  {
    // Keep track of the number of request attempts.
    Attempts++;

    // Send a request to the server and wait for a response.
    WinHttpReq.send( );

    // Obtain the status code from the response.
    var Status = WinHttpReq.Status;

    switch (Status)
    {
      // A 200 status indicates that the resource was retrieved.
      case 200:
        Done = true;
        break;

      // A 401 status indicates that the server 
      // requires authentication.
      case 401:
        WScript.Echo( "Requires Server UserName and Password." );

        // Specify the target resource.
        WinHttpReq.open( "GET", targURL, false );

        // Set credentials for the server.
        WinHttpReq.SetCredentials( "User Name", 
                             "Password",
                              HTTPREQUEST_SETCREDENTIALS_FOR_SERVER);
        break;

      // A 407 status indicates that the proxy 
      // requires authentication.
      case 407:
        WScript.Echo( "Requires Proxy UserName and Password." );

        // Specify the target resource.
        WinHttpReq.open( "GET", targURL, false );

        // Set credentials for the proxy.
        WinHttpReq.SetCredentials( "User Name", 
                              "Password",
                              HTTPREQUEST_SETCREDENTIALS_FOR_PROXY );
        break;
    }
  } while( ( !Done ) && ( Attempts < 3 ) );

  // Display the results of the request.
  WScript.Echo( WinHttpReq.Status + "   " + WinHttpReq.StatusText );
  WScript.Echo( WinHttpReq.GetAllResponseHeaders( ) );
  WScript.Echo( );
};
```



Salvare ed eseguire nuovamente il file. Il secondo metodo recupera comunque il documento, ma fornisce le credenziali solo quando necessario. La funzione "getText2" esegue i [**metodi Open**](iwinhttprequest-open.md) e [**Send**](iwinhttprequest-send.md) come se l'autenticazione non fosse necessaria. Lo stato viene recuperato con la [**proprietà Status**](iwinhttprequest-status.md) e un'istruzione switch risponde al codice di stato risultante. Se lo stato è 401 (il server richiede l'autenticazione) o 407 (il proxy richiede l'autenticazione), il [**metodo Open**](iwinhttprequest-open.md) viene eseguito di nuovo. Questo è seguito dal [**metodo SetCredentials,**](iwinhttprequest-setcredentials.md) che imposta il nome utente e la password. Il codice torna quindi al [**metodo Send.**](iwinhttprequest-send.md) Se, dopo tre tentativi, la risorsa non può essere recuperata correttamente, la funzione arresta l'esecuzione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Autenticazione in WinHTTP](authentication-in-winhttp.md)
</dt> <dt>

[WinHttpRequest](winhttprequest.md)
</dt> <dt>

[**SetCredentials**](iwinhttprequest-setcredentials.md)
</dt> <dt>

[Richiesta di commenti HTTP/1.1 (RFC 2616)](https://www.ietf.org/rfc/rfc2616.txt)
</dt> </dl>

 

 



