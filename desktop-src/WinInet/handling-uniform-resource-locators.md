---
title: Gestione di localizzatori di risorse uniformi
description: Un Uniform Resource Locator (URL) è una rappresentazione compatta del percorso e del metodo di accesso per una risorsa che si trova su Internet.
ms.assetid: bb59ada6-f49f-412c-a32c-4fb9495b1222
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08157738d99e78ff4d458a3bdd1b1e2e661ce538
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/10/2021
ms.locfileid: "104566040"
---
# <a name="handling-uniform-resource-locators"></a>Gestione di localizzatori di risorse uniformi

Un Uniform Resource Locator (URL) è una rappresentazione compatta del percorso e del metodo di accesso per una risorsa che si trova su Internet. Ogni URL è costituito da uno schema (HTTP, HTTPS o FTP) e da una stringa specifica dello schema. Questa stringa può includere anche una combinazione di percorso di directory, stringa di ricerca o nome della risorsa. Le funzioni WinINet offrono la possibilità di creare, combinare, suddividere e Canonicalize URL. Per ulteriori informazioni sugli URL, vedere [RFC-1738](https://www.ietf.org/rfc/rfc1738.txt) su Uniform Resource Locator (URL).

Le funzioni URL operano in modo orientato alle attività. Il contenuto e il formato dell'URL assegnato alla funzione non vengono verificati. L'applicazione chiamante deve tenere traccia dell'utilizzo di queste funzioni per assicurarsi che i dati siano nel formato previsto. La funzione [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) , ad esempio, converte il carattere "%" nella sequenza di escape "%25" quando non si utilizzano flag. Se si utilizza [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) nell'URL canonico, la sequenza di escape "%25" verrebbe convertita nella sequenza di escape "%2525", che non funzionerà correttamente.

-   [Che cos'è un URL in formato canonico?](#what-is-a-canonicalized-url)
-   [Utilizzo delle funzioni WinINet per la gestione degli URL](#using-the-wininet-functions-to-handle-urls)
-   [URL forma canonica](#what-is-a-canonicalized-url)
-   [Combinazione degli URL di base e relativi](#combining-base-and-relative-urls)
-   [URL di cracking](#cracking-urls)
-   [Creazione di URL](#creating-urls)
-   [Accesso diretto agli URL](#accessing-urls-directly)

## <a name="what-is-a-canonicalized-url"></a>Che cos'è un URL in formato canonico?

Il formato di tutti gli URL deve seguire la sintassi e la semantica accettate per accedere alle risorse tramite Internet. La canonizzazione è il processo di formattazione di un URL per seguire la sintassi e la semantica accettate.

I caratteri che devono essere codificati includono qualsiasi carattere senza carattere grafico corrispondente nel set di caratteri US-ASCII codificato (esadecimale 80-FF, che non vengono usati nel set di caratteri US-ASCII codificato, ed esadecimali 00-1F e 7F, che sono caratteri di controllo), spazi vuoti, "%" (usato per codificare altri caratteri) e caratteri unsafe (<, >, ", \# , {,}, \| , \\ , ^, ~, \[ , \] è).

## <a name="using-the-wininet-functions-to-handle-urls"></a>Utilizzo delle funzioni WinINet per la gestione degli URL

Nella tabella seguente sono riepilogate le funzioni URL.



| Funzione                                                   | Descrizione                                        |
|------------------------------------------------------------|----------------------------------------------------|
| [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) | Canonicalizes l'URL.                             |
| [**InternetCombineUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcombineurla)           | Combina gli URL di base e relativi.                   |
| [**InternetCrackUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla)               | Analizza una stringa URL in componenti.               |
| [**InternetCreateUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcreateurla)             | Crea una stringa URL da Components.              |
| [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)                 | Inizia a recuperare una risorsa FTP, HTTP o HTTPS. |



 

## <a name="canonicalizing-urls"></a>URL forma canonica

Forma canonica un URL è il processo che converte un URL, che può contenere caratteri non sicuri, ad esempio spazi vuoti, caratteri riservati e così via, in un formato accettato.

La funzione [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) può essere usata per Canonicalize URL. Questa funzione è molto orientata alle attività, quindi l'applicazione deve tenere traccia del suo utilizzo con attenzione. [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) non verifica che l'URL passato sia già canonico e che l'URL restituito sia valido.

I cinque flag seguenti controllano il modo in cui [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) gestisce un URL specifico. I flag possono essere utilizzati in combinazione. Se non viene usato alcun flag, la funzione codifica l'URL per impostazione predefinita.



| Valore                     | Significato                                                                                                                                                                                                 |
|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_modalità browser \_ ICU        | Non codificare o decodificare i caratteri dopo " \# " o "?" e non rimuovere gli spazi vuoti finali dopo "?". Se questo valore non viene specificato, l'intero URL viene codificato e gli spazi vuoti finali vengono rimossi. |
| DECODIFICA di ICU \_               | Converte tutte le sequenze% XX in caratteri, incluse le sequenze di escape, prima dell'analisi dell'URL.                                                                                                          |
| \_ \_ solo spazi di codifica ICU \_ | Codifica solo gli spazi.                                                                                                                                                                                     |
| \_non \_ codifica ICU           | Non convertire i caratteri non sicuri in sequenze di escape.                                                                                                                                                   |
| ICU \_ No \_ meta             | Non rimuovere le metasequenze (ad esempio "." e "..") dall'URL.                                                                                                                                       |



 

Il \_ flag di decodifica di ICU deve essere usato solo su URL in formato canonico, perché presuppone che tutte le sequenze% XX siano codici di escape e li converte nei caratteri indicati dal codice. Se l'URL contiene un simbolo "%" che non fa parte di un codice di escape, il \_ DEcodificatore di ICU lo considera comunque come uno. Questa caratteristica potrebbe causare la creazione di un URL non valido in [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) .

Per usare [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) per restituire un URL completamente decodificato, \_ è necessario specificare i flag ICU Decode e ICU \_ senza \_ codifica. Questa installazione presuppone che l'URL passato a [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) sia stato precedentemente reso canonico.

## <a name="combining-base-and-relative-urls"></a>Combinazione degli URL di base e relativi

Un URL relativo è una rappresentazione compatta della posizione di una risorsa relativa a un URL di base assoluto. L'URL di base deve essere noto al parser e in genere include lo schema, il percorso di rete e le parti del percorso URL. Un'applicazione può chiamare [**InternetCombineUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcombineurla) per combinare l'URL relativo con l'URL di base. [**InternetCombineUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcombineurla) canonicalizes anche l'URL risultante.

## <a name="cracking-urls"></a>URL di cracking

La funzione [**InternetCrackUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla) separa un URL nelle relative parti componente e restituisce i componenti indicati dalla struttura dei [**\_ componenti URL**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) passati alla funzione.

I componenti che costituiscono la struttura [**dei \_ componenti URL**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) sono il numero di schema, il nome host, il numero di porta, il nome utente, la password, il percorso URL e informazioni aggiuntive, ad esempio i parametri di ricerca. Ogni componente, ad eccezione dello schema e dei numeri di porta, dispone di un membro di stringa che contiene le informazioni e un membro che contiene la lunghezza del membro della stringa. Lo schema e i numeri di porta hanno solo un membro che archivia il valore corrispondente. vengono entrambi restituiti per tutte le chiamate riuscite a [**InternetCrackUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla).

Per ottenere il valore di un particolare componente nella struttura [**dei \_ componenti URL**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) , il membro che archivia la lunghezza di stringa di tale componente deve essere impostato su un valore diverso da zero. Il membro della stringa può essere l'indirizzo di un buffer o **null**.

Se il membro del puntatore contiene l'indirizzo di un buffer, il membro della lunghezza della stringa deve contenere la dimensione del buffer. [**InternetCrackUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla) restituisce le informazioni sul componente come stringa nel buffer e archivia la lunghezza della stringa nel membro della lunghezza della stringa.

Se il membro del puntatore è **null**, il membro della lunghezza della stringa può essere impostato su un valore diverso da zero. [**InternetCrackUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla) archivia l'indirizzo del primo carattere della stringa dell'URL che contiene le informazioni sul componente e imposta la lunghezza della stringa sul numero di caratteri nella parte rimanente della stringa dell'URL relativa al componente.

Tutti i membri del puntatore impostati su **null** con un membro di lunghezza diverso da zero puntano al punto di partenza appropriato nella stringa dell'URL. La lunghezza archiviata nel membro length deve essere utilizzata per determinare la fine delle informazioni del singolo componente.

Per completare l'inizializzazione corretta della struttura dei [**\_ componenti URL**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) , è necessario impostare il membro **dwStructSize** sulla dimensione della struttura dei [**\_ componenti URL**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) , in byte.

Nell'esempio seguente vengono restituiti i componenti dell'URL nella casella di modifica, IDC \_ PreOpen1, e i componenti vengono restituiti alla casella di riepilogo, IDC \_ preopen List. Per visualizzare solo le informazioni per un singolo componente, questa funzione copia il carattere immediatamente dopo le informazioni del componente nella stringa e lo sostituisce temporaneamente con un **valore null**.


```C++
#include <windows.h>
#include <tchar.h>
#include <strsafe.h>
#include <wininet.h>
#include <stdlib.h>

#pragma comment(lib, "wininet.lib")
#pragma comment(lib, "user32.lib")

#define  CRACKER_BUFFER_SIZE           MAX_PATH

// For sample source code implementing the InternetErrorOut( ) 
// function referenced below, see the "Handling Errors" topic  
// under "Using WinInet"
extern BOOL WINAPI InternetErrorOut( HWND hWnd, DWORD dwError,
                                     LPCTSTR szFailingFunctionName );

// Forward declaration of listUrlPart helper functions:
BOOL listURLpart( HWND hDlg, int nListBoxID, 
                  LPTSTR szPartName, LPTSTR part, DWORD partLength );
BOOL listURLpart( HWND hDlg, int nListBoxID, 
                  LPTSTR szPartName, int partValue );

// Static list describing the URL Scheme types 
// enumerated in INTERNET_SCHEME:
TCHAR* schemeType[] =
{
  TEXT( "[Partial URL]" ),                //  0
  TEXT( "[Unknown scheme]" ),             //  1
  TEXT( "[Default scheme]" ),             //  2
  TEXT( "FTP" ),                          //  3
  TEXT( "Gopher" ),                       //  4
  TEXT( "HTTP" ),                         //  5
  TEXT( "HTTPS" ),                        //  6
  TEXT( "File" ),                         //  7
  TEXT( "News" ),                         //  8
  TEXT( "MailTo" ),                       //  9
  TEXT( "Socks" ),                        // 10
  TEXT( "JavaScript" ),                   // 11
  TEXT( "VBScript" )                      // 12
};
#define  CRACKER_SCHEME_TYPE_ARRAY_SIZE      13

BOOL WINAPI Cracker( HWND hDlg, int nURLtextBoxId, int nListBoxId )
{
   int i, j;
   TCHAR* failedFunctionName;
   TCHAR URL_buffer[CRACKER_BUFFER_SIZE];

   URL_COMPONENTS URLparts;

   URLparts.dwStructSize = sizeof( URLparts );

   // The following elements determine which components are displayed
   URLparts.dwSchemeLength    = 1;
   URLparts.dwHostNameLength  = 1;
   URLparts.dwUserNameLength  = 1;
   URLparts.dwPasswordLength  = 1;
   URLparts.dwUrlPathLength   = 1;
   URLparts.dwExtraInfoLength = 1;

   URLparts.lpszScheme     = NULL;
   URLparts.lpszHostName   = NULL;
   URLparts.lpszUserName   = NULL;
   URLparts.lpszPassword   = NULL;
   URLparts.lpszUrlPath    = NULL;
   URLparts.lpszExtraInfo  = NULL;

   SendDlgItemMessage( hDlg, nListBoxId, LB_RESETCONTENT, 0, 0 );
   if( !GetDlgItemText( hDlg, nURLtextBoxId, 
                        URL_buffer, CRACKER_BUFFER_SIZE ) )
   {
       failedFunctionName = TEXT( "GetDlgItemText" );
       goto CrackerError_01;
   }

   if( FAILED( StringCchLength( URL_buffer, CRACKER_BUFFER_SIZE, 
                                (size_t*) &i ) ) )
   {
       failedFunctionName = TEXT( "StringCchLength" );
       goto CrackerError_01;
   }

   if( !InternetCrackUrl( URL_buffer, (DWORD)_tcslen( URL_buffer ), 0, 
                          &URLparts ) )
   {
       failedFunctionName = TEXT( "InternetCrackUrl" );
       goto CrackerError_01;
   }

   failedFunctionName = TEXT( "listURLpart" );

   i = URLparts.nScheme + 2;
   if( ( i >= 0 ) && ( i < CRACKER_SCHEME_TYPE_ARRAY_SIZE ) )
   {
       StringCchLength( schemeType[i], 
                        CRACKER_BUFFER_SIZE, 
                        (size_t*) &j );
       if( !listURLpart( hDlg, nListBoxId, 
                         TEXT("Scheme type"), 
                         schemeType[i], j ))
           goto CrackerError_01;
   }

   if( !listURLpart( hDlg, nListBoxId, TEXT( "Scheme text" ), 
                     URLparts.lpszScheme, 
                     URLparts.dwSchemeLength ) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "Host name" ), 
                     URLparts.lpszHostName, 
                     URLparts.dwHostNameLength) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "Port number" ), 
                     (int) URLparts.nPort ) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "User name" ), 
                     URLparts.lpszUserName, 
                     URLparts.dwUserNameLength) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "Password" ), 
                     URLparts.lpszPassword, 
                     URLparts.dwPasswordLength) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "Path" ), 
                     URLparts.lpszUrlPath, 
                     URLparts.dwUrlPathLength) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "Extra information"), 
                     URLparts.lpszExtraInfo, 
                     URLparts.dwExtraInfoLength))
           goto CrackerError_01;

   return( TRUE );

CrackerError_01:
// For sample source code of the InternetErrorOut( ) function 
// referenced below, see the "Handling Errors" 
// topic under "Using WinInet"
   InternetErrorOut( hDlg, GetLastError( ), failedFunctionName );
   return FALSE;
}

// listURLpart( ) helper function for string parts
BOOL listURLpart( HWND hDlg, int nListBoxId, 
                  LPTSTR szPartName, LPTSTR part, DWORD partLength )
{
  TCHAR outputBuffer[CRACKER_BUFFER_SIZE];
  LPTSTR nextStart;
  size_t nextSize;

  if( partLength == 0 )  // Just skip empty ones
    return( TRUE );

  if( FAILED( StringCchCopyEx( outputBuffer, 
                              (size_t) CRACKER_BUFFER_SIZE,
                               szPartName, &nextStart, 
                               &nextSize, 0 ) ) ||
      FAILED( StringCchCopyEx( nextStart, nextSize, TEXT( ": " ), 
                               &nextStart, &nextSize, 0 ) ) ||
      FAILED( StringCchCopyNEx( nextStart, nextSize, part, 
                                (size_t) partLength,
                                &nextStart, &nextSize, 0 ) ) )
    return( FALSE );

  *nextStart = 0;
  if( SendDlgItemMessage( hDlg, nListBoxId, LB_ADDSTRING, 0, 
                          (LPARAM)outputBuffer ) < 0 )
    return( FALSE );
  return( TRUE );
}

// listURLpart( ) helper function for numeric parts
BOOL listURLpart( HWND hDlg, int nListBoxId, 
                  LPTSTR szPartName, int partValue )
{
  TCHAR outputBuffer[CRACKER_BUFFER_SIZE];

  if( FAILED( StringCchPrintf( outputBuffer, 
                               (size_t) CRACKER_BUFFER_SIZE,
                               TEXT( "%s: %d" ), szPartName, 
                               partValue ) ) ||
      ( SendDlgItemMessage( hDlg, nListBoxId, LB_ADDSTRING, 0, 
                            (LPARAM)outputBuffer ) < 0 ) )
    return( FALSE );
  return( TRUE );
}
```



## <a name="creating-urls"></a>Creazione di URL

La funzione [**InternetCreateUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcreateurla) usa le informazioni contenute nella struttura dei [**\_ componenti URL**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) per creare un Uniform Resource Locator.

I componenti che costituiscono la struttura [**dei \_ componenti URL**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) sono lo schema, il nome host, il numero di porta, il nome utente, la password, il percorso URL e informazioni aggiuntive, ad esempio i parametri di ricerca. Ogni componente, eccetto il numero di porta, dispone di un membro di stringa che contiene le informazioni e un membro che contiene la lunghezza del membro della stringa.

Per ogni componente richiesto, il membro del puntatore deve contenere l'indirizzo del buffer che contiene le informazioni. Il membro length deve essere impostato su zero se il membro del puntatore contiene l'indirizzo di una stringa con terminazione zero. il membro length deve essere impostato sulla lunghezza della stringa se il membro del puntatore contiene l'indirizzo di una stringa senza terminazione zero. Il membro del puntatore di tutti i componenti non necessari deve essere **null**.

## <a name="accessing-urls-directly"></a>Accesso diretto agli URL

È possibile accedere direttamente alle risorse FTP e HTTP su Internet usando le funzioni [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)e [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) . [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) apre una connessione alla risorsa in corrispondenza dell'URL passato alla funzione. Quando si effettua questa connessione, è possibile eseguire due passaggi. Prima di tutto, se la risorsa è un file, [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) può scaricarlo; in secondo luogo, se la risorsa è una directory, [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) può enumerare i file all'interno della directory, tranne quando si usano i proxy CERN. Per ulteriori informazioni su [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), vedere la pagina relativa alla [lettura di file](common-functions.md). Per ulteriori informazioni su [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea), vedere [la pagina relativa alla ricerca del file successivo](common-functions.md).

Per le applicazioni che devono funzionare tramite un proxy CERN, è possibile usare [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) per accedere a directory e file FTP. Le richieste FTP sono incluse in un pacchetto per essere visualizzate come una richiesta HTTP, che verrà accettata dal proxy CERN.

[**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) usa l'handle [**HINTERNET**](appendix-a-hinternet-handles.md) creato dalla funzione [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) e l'URL della risorsa. L'URL deve includere lo schema (http:, FTP:, file: \[ per un file locale \] o https: \[ per il protocollo Hypertext Secure \] ) e il percorso di rete (ad esempio `www.microsoft.com` ). L'URL può includere anche un percorso (ad esempio,/ISAPI/gomscom.asp? TARGET =/Windows/Feature/) e il nome della risorsa (ad esempio, default.htm). Per le richieste HTTP o HTTPS, è possibile includere intestazioni aggiuntive.

[**La InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable), [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea), [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)e [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) (solo URL http o HTTPS) possono usare l'handle creato da [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) per scaricare la risorsa.

Il diagramma seguente illustra gli handle da usare con ogni funzione.

![handle da usare con le funzioni](images/ax-wnt02.png)

L'handle [**HINTERNET**](appendix-a-hinternet-handles.md) radice creato da [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) viene usato da [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla). L'handle **HINTERNET** creato da [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) può essere usato da [**la InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable), [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) (non mostrato qui) e [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) (solo URL http o HTTPS).

Per altre informazioni, vedere [**handle hInternet**](appendix-a-hinternet-handles.md).

> [!Note]  
> WinINet non supporta le implementazioni del server. Inoltre, non deve essere utilizzato da un servizio. Per le implementazioni o i servizi del server, usare i [Servizi http di Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 