---
description: Un URL è una rappresentazione compatta del percorso e del metodo di accesso per una risorsa che si trova su Internet.
ms.assetid: 940c414d-274f-475c-a50e-7a0853c3c26b
title: Uniform Resource Locator (URL) in WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 486ed3b17e2cf205f6ac815e87617a84e0ccc4cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049820"
---
# <a name="uniform-resource-locators-urls-in-winhttp"></a>Uniform Resource Locator (URL) in WinHTTP

Un URL è una rappresentazione compatta del percorso e del metodo di accesso per una risorsa che si trova su Internet. Ogni URL è costituito da uno schema (HTTP, HTTPS, FTP o gopher) e da una stringa specifica dello schema. Questa stringa può includere anche una combinazione di percorso di directory, stringa di ricerca o nome della risorsa. Le funzioni dei servizi HTTP di Microsoft Windows (WinHTTP) offrono la possibilità di creare, combinare, suddividere e Canonicalize URL. Per altre informazioni, vedere [rfc 1738](https://www.ietf.org/rfc/rfc1738.txt), [Uniform Resource Locators](https://www.ietf.org/rfc/rfc1738.txt) e [RFC 2396](https://www.ietf.org/rfc/rfc2396.txt), [Uniform Resource Identifier (URI): sintassi generica](https://www.ietf.org/rfc/rfc1738.txt).

## <a name="what-is-a-canonicalized-url"></a>Che cos'è un URL in formato canonico?

La sintassi e la semantica specificate degli URL lasciano spazio per la variazione e l'errore. La canonizzazione è il processo di normalizzare un URL effettivo in un formato corretto, standard, "canonical".

Questa operazione implica la codifica di alcuni caratteri come sequenze di escape. I caratteri alfanumerici US-ASCII non devono essere codificati (le cifre 0-9, le lettere maiuscole A-Z e le lettere minuscole a-z). La maggior parte degli altri caratteri deve essere preceduto da un carattere di escape, inclusi i caratteri di controllo, lo spazio, il segno di percentuale, "caratteri unsafe" (<, >, ", \# , {,}, \| , \\ , ^, ~, \[ , \] è) e tutti i caratteri con un punto di codice superiore a 127.

## <a name="using-the-winhttp-functions-to-handle-urls"></a>Uso delle funzioni WinHTTP per la gestione degli URL

WinHTTP fornisce due funzioni per la gestione degli URL. [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) separa un URL nelle relative parti componente e [**WINHTTPCREATEURL**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) crea un URL dai componenti.

### <a name="separating-urls"></a>Separazione degli URL

La funzione [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) separa un URL nelle relative parti componente e restituisce i componenti indicati dalla struttura dei [**\_ componenti URL**](/windows/win32/api/winhttp/ns-winhttp-url_components) passati alla funzione.

I componenti che costituiscono la struttura [**dei \_ componenti URL**](/windows/win32/api/winhttp/ns-winhttp-url_components) sono il numero di schema, il nome host, il numero di porta, il nome utente, la password, il percorso URL e altre informazioni, ad esempio i parametri di ricerca. Ogni componente, ad eccezione dello schema e dei numeri di porta, dispone di un membro di stringa che contiene le informazioni e un membro che contiene la lunghezza del membro della stringa. Lo schema e i numeri di porta hanno solo un membro che archivia il valore corrispondente. per tutte le chiamate riuscite a [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl)vengono restituiti sia lo schema che i numeri di porta.

Per recuperare il valore di un particolare componente nella struttura [**dei \_ componenti URL**](/windows/win32/api/winhttp/ns-winhttp-url_components) , il membro che archivia la lunghezza di stringa di tale componente deve essere impostato su un valore diverso da zero. Il membro della stringa può essere un puntatore a un buffer o **null**.

Se il membro del puntatore contiene un puntatore a un buffer, il membro della lunghezza della stringa deve contenere la dimensione del buffer. La funzione [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) restituisce le informazioni sul componente come stringa nel buffer e archivia la lunghezza della stringa nel membro della lunghezza della stringa.

Se il membro del puntatore è impostato su **null**, il membro della lunghezza della stringa può essere impostato su un valore diverso da zero. La funzione [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) archivia un puntatore al primo carattere della stringa dell'URL che contiene le informazioni sul componente e imposta la lunghezza della stringa sul numero di caratteri nella parte rimanente della stringa dell'URL che riguarda il componente.

Tutti i membri del puntatore impostati su **null** con un membro di lunghezza diverso da zero puntano al punto di partenza appropriato nella stringa dell'URL. La lunghezza archiviata nel membro length deve essere utilizzata per determinare la fine delle informazioni del singolo componente.

Per completare l'inizializzazione corretta della struttura dei [**\_ componenti URL**](/windows/win32/api/winhttp/ns-winhttp-url_components) , è necessario impostare il membro **dwStructSize** sulla dimensione della struttura dei [**\_ componenti URL**](/windows/win32/api/winhttp/ns-winhttp-url_components) .

### <a name="creating-urls"></a>Creazione di URL

La funzione [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) usa le informazioni contenute nella struttura dei [**\_ componenti URL**](/windows/win32/api/winhttp/ns-winhttp-url_components) descritti in precedenza per creare un URL.

Per ogni componente richiesto, il membro del puntatore deve contenere un puntatore al buffer che contiene le informazioni. Il membro length deve essere impostato su zero se il membro del puntatore contiene un puntatore a una stringa con terminazione zero. il membro length deve essere impostato sulla lunghezza della stringa se il membro del puntatore contiene un puntatore a una stringa senza terminazione zero. Il membro del puntatore di tutti i componenti non necessari deve essere impostato su **null**.

### <a name="sample-code"></a>Codice di esempio

Il codice di esempio seguente illustra come usare [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) e [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) per disassemblare un URL esistente, modificare uno dei relativi componenti e riassemblarlo in un nuovo URL.


```C++
  URL_COMPONENTS urlComp;
  LPCWSTR pwszUrl1 = 
    L"https://search.msn.com/results.asp?RS=CHECKED&FORM=MSNH&v=1&q=wininet";
  DWORD dwUrlLen = 0;

  // Initialize the URL_COMPONENTS structure.
  ZeroMemory(&urlComp, sizeof(urlComp));
  urlComp.dwStructSize = sizeof(urlComp);

  // Set required component lengths to non-zero so that they are cracked.
  urlComp.dwSchemeLength    = (DWORD)-1;
  urlComp.dwHostNameLength  = (DWORD)-1;
  urlComp.dwUrlPathLength   = (DWORD)-1;
  urlComp.dwExtraInfoLength = (DWORD)-1;

  // Crack the URL.
  if( !WinHttpCrackUrl( pwszUrl1, (DWORD)wcslen(pwszUrl1), 0, &urlComp ) )
      printf( "Error %u in WinHttpCrackUrl.\n", GetLastError( ) );
  else
  {
    // Change the search information.  New info is the same length.
    urlComp.lpszExtraInfo = L"?RS=CHECKED&FORM=MSNH&v=1&q=winhttp";

    // Obtain the size of the new URL and allocate memory.
    WinHttpCreateUrl( &urlComp, 0, NULL, &dwUrlLen );
    LPWSTR pwszUrl2 = new WCHAR[dwUrlLen];

    // Create a new URL.
    if( !WinHttpCreateUrl( &urlComp, 0, pwszUrl2, &dwUrlLen ) )
      printf( "Error %u in WinHttpCreateUrl.\n", GetLastError( ) );
    else
    {
      // Show both URLs.
      printf( "Old URL:  %S\nNew URL:  %S\n", pwszUrl1, pwszUrl2 );
    }

    // Free allocated memory.
    delete [] pwszUrl2;
  }
```



 

 



