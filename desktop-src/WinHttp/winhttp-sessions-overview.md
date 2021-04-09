---
description: I servizi HTTP di Microsoft Windows (WinHTTP) espongono un set di funzioni C/C++ che consentono all'applicazione di accedere alle risorse HTTP sul Web. Questo argomento fornisce una panoramica del modo in cui queste funzioni vengono usate per interagire con un server HTTP.
ms.assetid: 66a1616b-0cf3-45c7-880b-e36728b5a9c4
title: Cenni preliminari sulle sessioni WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98dc8116dff75f279b87cb5f5ee6af607034176f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129258"
---
# <a name="winhttp-sessions-overview"></a>Cenni preliminari sulle sessioni WinHTTP

I servizi HTTP di Microsoft Windows (WinHTTP) espongono un set di funzioni C/C++ che consentono all'applicazione di accedere alle risorse HTTP sul Web. Questo argomento fornisce una panoramica del modo in cui queste funzioni vengono usate per interagire con un server HTTP.

-   [Uso dell'API WinHTTP per accedere al Web](#using-the-winhttp-api-to-access-the-web)
-   [Inizializzazione di WinHTTP](#initializing-winhttp)
-   [Apertura di una richiesta](#opening-a-request)
-   [Aggiunta di intestazioni di richiesta](#adding-request-headers)
-   [Invio di una richiesta](#sending-a-request)
-   [Invio di dati al server](#posting-data-to-the-server)
-   [Ottenere informazioni su una richiesta](#getting-information-about-a-request)
-   [Download delle risorse dal Web](#downloading-resources-from-the-web)

## <a name="using-the-winhttp-api-to-access-the-web"></a>Uso dell'API WinHTTP per accedere al Web

Il diagramma seguente illustra l'ordine in cui le funzioni WinHTTP vengono in genere chiamate quando si interagisce con un server HTTP. Le caselle ombreggiate rappresentano le funzioni che generano un handle [HINTERNET](hinternet-handles-in-winhttp.md) , mentre le caselle semplici rappresentano funzioni che usano tali handle.

![funzioni che creano handle](images/art-winhttp3.png)

## <a name="initializing-winhttp"></a>Inizializzazione di WinHTTP

Prima di interagire con un server, è necessario inizializzare WinHTTP chiamando [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen). [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) crea un contesto di sessione per gestire i dettagli relativi alla sessione HTTP e restituisce un handle di sessione. Con questo handle, la funzione [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect) è in grado di specificare un server http di destinazione o Secure HYPERTEXT Transfer Protocol (HTTPS).

> [!Note]  
> Una chiamata a [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect) non comporta una connessione effettiva al server http fino a quando non viene effettuata una richiesta per una risorsa specifica.

 

## <a name="opening-a-request"></a>Apertura di una richiesta

La funzione [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) apre una richiesta HTTP per una determinata risorsa e restituisce un handle [HINTERNET](hinternet-handles-in-winhttp.md) che può essere usato da altre funzioni http. [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) non invia la richiesta al server quando viene chiamata. La funzione [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) stabilisce effettivamente una connessione sulla rete e Invia la richiesta.

Nell'esempio seguente viene illustrata una chiamata di esempio a [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) che utilizza le opzioni predefinite.

`HINTERNET hRequest = WinHttpOpenRequest( hConnect, L"GET", NULL, NULL, NULL, NULL, 0);`

## <a name="adding-request-headers"></a>Aggiunta di intestazioni di richiesta

La funzione [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) consente a un'applicazione di aggiungere intestazioni di richiesta di formato libero aggiuntive all'handle della richiesta HTTP. È progettato per l'uso da parte di applicazioni sofisticate che richiedono un controllo preciso sulle richieste inviate al server HTTP.

La funzione [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) richiede un handle di richiesta HTTP creato da [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest), una stringa che contiene le intestazioni, la lunghezza delle intestazioni e tutti i modificatori.

Con [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)è possibile usare i modificatori seguenti.



| Modificatore                                                                                         | Descrizione                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_aggiunta del \_ flag \_ ADDREQ WinHTTP**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)                       | Aggiunge l'intestazione se non esiste. Usato con [**il \_ flag ADDREQ di WinHTTP \_ \_ Replace**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders).                                                                                                                                                                                                               |
| [**\_flag ADDREQ \_ WinHTTP \_ Aggiungi \_ se \_ nuovo**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)              | Aggiunge l'intestazione solo se non esiste già. in caso contrario, viene restituito un errore.                                                                                                                                                                                                                                                           |
| [**\_ \_ COALESCE flag ADDREQ WinHTTP \_**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)                  | Unisce le intestazioni con lo stesso nome.                                                                                                                                                                                                                                                                                                              |
| [**\_flag ADDREQ \_ WinHTTP \_ COALESCE \_ con \_ virgola**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)     | Unisce le intestazioni con lo stesso nome usando una virgola. Ad esempio, se si aggiunge "Accept: Text/ \* " seguito da "Accept: audio/ \* " con questo flag, viene formata la singola intestazione "Accept: Text/ \* , audio/ \* ", causando il merge della prima intestazione. Spetta all'applicazione chiamante garantire uno schema coeso rispetto a intestazioni unite/separate. |
| [**\_flag ADDREQ \_ WinHTTP \_ COALESCE \_ con \_ punto e virgola**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) | Unisce le intestazioni con lo stesso nome usando un punto e virgola.                                                                                                                                                                                                                                                                                            |
| [**il \_ flag ADDREQ di WinHTTP \_ \_ sostituisce**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)                   | Sostituisce o rimuove un'intestazione. Se il valore dell'intestazione è vuoto e l'intestazione viene trovata, viene rimossa. Se il valore dell'intestazione non è vuoto, il valore dell'intestazione viene sostituito.                                                                                                                                                                            |



 

## <a name="sending-a-request"></a>Invio di una richiesta

La funzione [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) stabilisce una connessione al server e Invia la richiesta al sito specificato. Questa funzione richiede un handle [HINTERNET](hinternet-handles-in-winhttp.md) creato da [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest). [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) può anche inviare intestazioni aggiuntive o informazioni facoltative. Le informazioni facoltative vengono in genere usate per le operazioni che scrivono le informazioni sul server, ad esempio PUT e POST.

Dopo che la funzione [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) ha inviato la richiesta, l'applicazione può usare le funzioni [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata) e [**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) sull'handle [HINTERNET](hinternet-handles-in-winhttp.md) per scaricare le risorse del server.

## <a name="posting-data-to-the-server"></a>Invio di dati al server

Per inserire i dati in un server, il [*verbo http*](glossary.md) nella chiamata a [**WINHTTPOPENREQUEST**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) deve essere post o put. Quando viene chiamato [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) , il parametro *dwTotalLength* deve essere impostato sulla dimensione dei dati in byte. Usare quindi [**WinHttpWriteData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata) per inviare i dati al server.

In alternativa, impostare il parametro *lpOptional* di [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) sull'indirizzo di un buffer che contiene i dati da inviare al server. Quando si utilizza questa tecnica, è necessario impostare i parametri *dwOptionalLength* e *dwTotalLength* di [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) in modo che siano le dimensioni dei dati inviati. La chiamata di [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) in questo modo Elimina la necessità di chiamare [**WinHttpWriteData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata).

## <a name="getting-information-about-a-request"></a>Ottenere informazioni su una richiesta

La funzione [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders) consente a un'applicazione di recuperare informazioni su una richiesta HTTP. La funzione richiede un handle [HINTERNET](hinternet-handles-in-winhttp.md) creato da [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest), un valore del livello di informazioni e una lunghezza del buffer. [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders) accetta anche un buffer che archivia le informazioni e un indice in base zero dell'intestazione che enumera più intestazioni con lo stesso nome.

Usare uno dei valori del livello informazioni disponibili nella pagina [**flag informazioni query**](query-info-flags.md) con un modificatore per controllare il formato in cui le informazioni vengono archiviate nel parametro *lpvBuffer* di [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders).

## <a name="downloading-resources-from-the-web"></a>Download delle risorse dal Web

Dopo l'apertura di una richiesta con la funzione [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) , l'invio al server con [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)e la preparazione dell'handle di richiesta per ricevere una risposta con [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse), l'applicazione può usare le funzioni [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata) e [**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) per scaricare la risorsa dal server http.

Il codice di esempio seguente illustra come scaricare una risorsa con la semantica di transazione sicura. Il codice di esempio Inizializza l'Application Programming Interface WinHTTP (API), seleziona un server HTTPS di destinazione e quindi apre e invia una richiesta per la risorsa protetta. [**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) viene usato con l'handle della richiesta per determinare la quantità di dati disponibili per il download e quindi [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata) viene usato per leggere i dati. Questo processo viene ripetuto fino a quando non viene recuperato e visualizzato l'intero documento.


```C++
  DWORD dwSize = 0;
  DWORD dwDownloaded = 0;
  LPSTR pszOutBuffer;
  BOOL  bResults = FALSE;
  HINTERNET  hSession = NULL, 
             hConnect = NULL,
             hRequest = NULL;

  // Use WinHttpOpen to obtain a session handle.
  hSession = WinHttpOpen( L"WinHTTP Example/1.0",  
                          WINHTTP_ACCESS_TYPE_DEFAULT_PROXY,
                          WINHTTP_NO_PROXY_NAME, 
                          WINHTTP_NO_PROXY_BYPASS, 0 );

  // Specify an HTTP server.
  if( hSession )
    hConnect = WinHttpConnect( hSession, L"www.microsoft.com",
                               INTERNET_DEFAULT_HTTPS_PORT, 0 );

  // Create an HTTP request handle.
  if( hConnect )
    hRequest = WinHttpOpenRequest( hConnect, L"GET", NULL,
                                   NULL, WINHTTP_NO_REFERER, 
                                   WINHTTP_DEFAULT_ACCEPT_TYPES, 
                                   WINHTTP_FLAG_SECURE );

  // Send a request.
  if( hRequest )
    bResults = WinHttpSendRequest( hRequest,
                                   WINHTTP_NO_ADDITIONAL_HEADERS, 0,
                                   WINHTTP_NO_REQUEST_DATA, 0, 
                                   0, 0 );


  // End the request.
  if( bResults )
    bResults = WinHttpReceiveResponse( hRequest, NULL );

  // Keep checking for data until there is nothing left.
  if( bResults )
  {
    do 
    {
      // Check for available data.
      dwSize = 0;
      if( !WinHttpQueryDataAvailable( hRequest, &dwSize ) )
        printf( "Error %u in WinHttpQueryDataAvailable.\n",
                GetLastError( ) );

      // Allocate space for the buffer.
      pszOutBuffer = new char[dwSize+1];
      if( !pszOutBuffer )
      {
        printf( "Out of memory\n" );
        dwSize=0;
      }
      else
      {
        // Read the data.
        ZeroMemory( pszOutBuffer, dwSize+1 );

        if( !WinHttpReadData( hRequest, (LPVOID)pszOutBuffer, 
                              dwSize, &dwDownloaded ) )
          printf( "Error %u in WinHttpReadData.\n", GetLastError( ) );
        else
          printf( "%s", pszOutBuffer );

        // Free the memory allocated to the buffer.
        delete [] pszOutBuffer;
      }
    } while( dwSize > 0 );
  }


  // Report any errors.
  if( !bResults )
    printf( "Error %d has occurred.\n", GetLastError( ) );

  // Close any open handles.
  if( hRequest ) WinHttpCloseHandle( hRequest );
  if( hConnect ) WinHttpCloseHandle( hConnect );
  if( hSession ) WinHttpCloseHandle( hSession );
```



 

 



