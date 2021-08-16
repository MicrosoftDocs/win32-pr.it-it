---
description: Microsoft Windows HTTP Services (WinHTTP) espone un set di funzioni C/C++ che consentono all'applicazione di accedere alle risorse HTTP sul Web. In questo argomento viene fornita una panoramica dell'utilizzo di queste funzioni per interagire con un server HTTP.
ms.assetid: 66a1616b-0cf3-45c7-880b-e36728b5a9c4
title: Panoramica delle sessioni WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 753f7c2a3845b34ac306c1fb8d87441955ab9f4cfe0e1ea250737f62f993cd43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117743906"
---
# <a name="winhttp-sessions-overview"></a>Panoramica delle sessioni WinHTTP

Microsoft Windows HTTP Services (WinHTTP) espone un set di funzioni C/C++ che consentono all'applicazione di accedere alle risorse HTTP sul Web. In questo argomento viene fornita una panoramica dell'utilizzo di queste funzioni per interagire con un server HTTP.

-   [Uso dell'API WinHTTP per accedere al Web](#using-the-winhttp-api-to-access-the-web)
-   [Inizializzazione di WinHTTP](#initializing-winhttp)
-   [Apertura di una richiesta](#opening-a-request)
-   [Aggiunta di intestazioni di richiesta](#adding-request-headers)
-   [Invio di una richiesta](#sending-a-request)
-   [Pubblicazione di dati nel server](#posting-data-to-the-server)
-   [Recupero di informazioni su una richiesta](#getting-information-about-a-request)
-   [Download di risorse dal Web](#downloading-resources-from-the-web)

## <a name="using-the-winhttp-api-to-access-the-web"></a>Uso dell'API WinHTTP per accedere al Web

Il diagramma seguente illustra l'ordine in cui le funzioni WinHTTP vengono in genere chiamate quando si interagisce con un server HTTP. Le caselle ombreggiate rappresentano le funzioni che generano un handle [HINTERNET,](hinternet-handles-in-winhttp.md) mentre le caselle semplici rappresentano le funzioni che usano tali handle.

![Funzioni che creano handle](images/art-winhttp3.png)

## <a name="initializing-winhttp"></a>Inizializzazione di WinHTTP

Prima di interagire con un server, WinHTTP deve essere inizializzato chiamando [**WinHttpOpen.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) [**WinHttpOpen crea**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) un contesto di sessione per mantenere i dettagli sulla sessione HTTP e restituisce un handle di sessione. Usando questo handle, la [**funzione WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect) è quindi in grado di specificare un server HTTP o Secure Hypertext Transfer Protocol (HTTPS) di destinazione.

> [!Note]  
> Una chiamata a [**WinHttpConnect non**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect) comporta una connessione effettiva al server HTTP fino a quando non viene effettuata una richiesta per una risorsa specifica.

 

## <a name="opening-a-request"></a>Apertura di una richiesta

La [**funzione WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) apre una richiesta HTTP per una determinata risorsa e restituisce un handle [HINTERNET](hinternet-handles-in-winhttp.md) che può essere usato dalle altre funzioni HTTP. [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) non invia la richiesta al server quando viene chiamato. La [**funzione WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) stabilisce effettivamente una connessione in rete e invia la richiesta.

L'esempio seguente mostra una chiamata di esempio [**a WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) che usa le opzioni predefinite.

`HINTERNET hRequest = WinHttpOpenRequest( hConnect, L"GET", NULL, NULL, NULL, NULL, 0);`

## <a name="adding-request-headers"></a>Aggiunta di intestazioni di richiesta

La [**funzione WinHttpAddRequestHeaders consente**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) a un'applicazione di aggiungere altre intestazioni di richiesta in formato libero all'handle della richiesta HTTP. È destinato all'uso da parte di applicazioni sofisticate che richiedono un controllo preciso sulle richieste inviate al server HTTP.

La [**funzione WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) richiede un handle di richiesta HTTP creato da [**WinHttpOpenRequest,**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)una stringa che contiene le intestazioni, la lunghezza delle intestazioni ed eventuali modificatori.

I modificatori seguenti possono essere usati con [**WinHttpAddRequestHeaders.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)



| Modificatore                                                                                         | Descrizione                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AGGIUNTA \_ DEL FLAG ADDREQ WINHTTP \_ \_**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)                       | Aggiunge l'intestazione se non esiste. Usato con [**WINHTTP \_ ADDREQ \_ FLAG \_ REPLACE**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders).                                                                                                                                                                                                               |
| [**AGGIUNTA \_ DEL FLAG ADDREQ WINHTTP \_ \_ SE \_ \_ NUOVO**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)              | Aggiunge l'intestazione solo se non esiste già. In caso contrario, viene restituito un errore.                                                                                                                                                                                                                                                           |
| [**WINHTTP \_ ADDREQ \_ FLAG \_ COALESCE**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)                  | Unisce le intestazioni con lo stesso nome.                                                                                                                                                                                                                                                                                                              |
| [**FLAG \_ ADDREQ WINHTTP \_ \_ COALESCE \_ CON \_ VIRGOLA**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)     | Unisce le intestazioni con lo stesso nome usando una virgola. Ad esempio, aggiungendo "Accept: text/ " seguito da "Accept: audio/ " con questo flag forma la singola intestazione \* \* "Accept: text/ \* , audio/ ", causando il merge della prima intestazione \* trovata. È responsabilità dell'applicazione chiamante garantire uno schema coesivo rispetto alle intestazioni unite/separate. |
| [**FLAG \_ ADDREQ WINHTTP \_ \_ COALESCE \_ CON PUNTO E \_ VIRGOLA**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) | Unisce le intestazioni con lo stesso nome usando un punto e virgola.                                                                                                                                                                                                                                                                                            |
| [**SOSTITUZIONE \_ DEL FLAG ADDREQ WINHTTP \_ \_**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)                   | Sostituisce o rimuove un'intestazione. Se il valore dell'intestazione è vuoto e l'intestazione viene trovata, viene rimossa. Se il valore dell'intestazione non è vuoto, il valore dell'intestazione viene sostituito.                                                                                                                                                                            |



 

## <a name="sending-a-request"></a>Invio di una richiesta

La [**funzione WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) stabilisce una connessione al server e invia la richiesta al sito specificato. Questa funzione richiede un handle [HINTERNET](hinternet-handles-in-winhttp.md) creato [**da WinHttpOpenRequest.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) può anche inviare intestazioni aggiuntive o informazioni facoltative. Le informazioni facoltative vengono in genere usate per le operazioni che scrivono informazioni nel server, ad esempio PUT e POST.

Dopo che [**la funzione WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) ha inviato la richiesta, l'applicazione può usare le funzioni [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata) e [**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) nell'handle [HINTERNET](hinternet-handles-in-winhttp.md) per scaricare le risorse del server.

## <a name="posting-data-to-the-server"></a>Pubblicazione di dati nel server

Per inviare dati a un server, il [*verbo HTTP*](glossary.md) nella chiamata [**a WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) deve essere POST o PUT. Quando [**viene chiamato WinHttpSendRequest,**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) il *parametro dwTotalLength* deve essere impostato sulla dimensione dei dati in byte. Usare quindi [**WinHttpWriteData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata) per inviare i dati al server.

In alternativa, impostare *il parametro lpOptional* di [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) sull'indirizzo di un buffer che contiene i dati da pubblicare nel server. Quando si usa questa tecnica, è necessario impostare entrambi i parametri *dwOptionalLength* e *dwTotalLength* di [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) in modo che siano le dimensioni dei dati inviati. La [**chiamata a WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) in questo modo elimina la necessità di [**chiamare WinHttpWriteData.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata)

## <a name="getting-information-about-a-request"></a>Recupero di informazioni su una richiesta

La [**funzione WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders) consente a un'applicazione di recuperare informazioni su una richiesta HTTP. La funzione richiede un handle [HINTERNET](hinternet-handles-in-winhttp.md) creato [**da WinHttpOpenRequest,**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)un valore del livello di informazioni e una lunghezza del buffer. [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders) accetta anche un buffer che archivia le informazioni e un indice di intestazione in base zero che enumera più intestazioni con lo stesso nome.

Usare uno dei valori a livello di informazioni disponibili nella pagina [**Flag**](query-info-flags.md) informazioni query con un modificatore per controllare il formato in cui le informazioni vengono archiviate nel parametro *lpvBuffer* di [**WinHttpQueryHeaders.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders)

## <a name="downloading-resources-from-the-web"></a>Download di risorse dal Web

Dopo l'apertura di una richiesta con la funzione [**WinHttpOpenRequest,**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) l'invio al server con [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)e la preparazione dell'handle di richiesta per ricevere una risposta [**con WinHttpReceiveResponse,**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse)l'applicazione può usare le funzioni [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata) e [**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) per scaricare la risorsa dal server HTTP.

Il codice di esempio seguente illustra come scaricare una risorsa con semantica di transazione sicura. Il codice di esempio inizializza l'API WinHTTP, seleziona un server HTTPS di destinazione e quindi apre e invia una richiesta per questa risorsa protetta. [**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) viene usato con l'handle della richiesta per determinare la quantità di dati disponibili per il download e quindi [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata) viene usato per leggere i dati. Questo processo viene ripetuto fino a quando non viene recuperato e visualizzato l'intero documento.


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



 

 



