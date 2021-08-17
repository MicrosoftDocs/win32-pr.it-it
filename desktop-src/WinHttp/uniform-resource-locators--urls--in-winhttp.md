---
description: Un URL è una rappresentazione compatta del percorso e del metodo di accesso per una risorsa che si trova su Internet.
ms.assetid: 940c414d-274f-475c-a50e-7a0853c3c26b
title: URL (Uniform Resource Locators) in WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 798d18dd2e3d2095e175904fcc2f3a332d618100174f174510c98780b06a57ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133009"
---
# <a name="uniform-resource-locators-urls-in-winhttp"></a>URL (Uniform Resource Locators) in WinHTTP

Un URL è una rappresentazione compatta del percorso e del metodo di accesso per una risorsa che si trova su Internet. Ogni URL è costituito da uno schema (HTTP, HTTPS, FTP o Gopher) e da una stringa specifica dello schema. Questa stringa può includere anche una combinazione di un percorso di directory, una stringa di ricerca o un nome della risorsa. Le funzioni microsoft Windows servizi HTTP (WinHTTP) consentono di creare, combinare, suddividere e canonizzare gli URL. Per altre informazioni, vedere [RFC 1738](https://www.ietf.org/rfc/rfc1738.txt), [Uniform Resource Locators](https://www.ietf.org/rfc/rfc1738.txt) e [RFC 2396](https://www.ietf.org/rfc/rfc2396.txt), [URI (Uniform Resource Identifier): Sintassi generica](https://www.ietf.org/rfc/rfc1738.txt).

## <a name="what-is-a-canonicalized-url"></a>Che cos'è un URL canonico?

La sintassi e la semantica degli URL specificati lasciano spazio alla variazione e all'errore. La canonizzazione è il processo di normalizzazione di un URL effettivo in una forma corretta, standard e "canonica".

Ciò comporta la codifica di alcuni caratteri come "sequenze di escape". I caratteri US-ASCII alfanumerici non devono essere codificati (le cifre da 0 a 9, le lettere maiuscole A-Z e le lettere minuscole a-z). La maggior parte degli altri caratteri deve essere preceduta da caratteri di escape, inclusi i caratteri di controllo, lo spazio, il segno di percentuale, i "caratteri non sicuri" ( <, >, ", {, }, , ^, ~, , e ' ) e tutti i caratteri con un punto di codice superiore \# \| a \\ \[ \] 127.

## <a name="using-the-winhttp-functions-to-handle-urls"></a>Uso delle funzioni WinHTTP per gestire gli URL

WinHTTP offre due funzioni per la gestione degli URL. [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) separa un URL nelle parti del componente e [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) crea un URL dai componenti.

### <a name="separating-urls"></a>Separazione degli URL

La [**funzione WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) separa un URL nelle relative parti del componente e restituisce i componenti indicati dalla struttura [**\_ COMPONENTS dell'URL**](/windows/win32/api/winhttp/ns-winhttp-url_components) passata alla funzione.

I componenti che costituiscono la struttura [**COMPONENTI URL \_**](/windows/win32/api/winhttp/ns-winhttp-url_components) sono il numero dello schema, il nome host, il numero di porta, il nome utente, la password, il percorso URL e informazioni aggiuntive, ad esempio i parametri di ricerca. Ogni componente, ad eccezione dello schema e dei numeri di porta, ha un membro stringa che contiene le informazioni e un membro che contiene la lunghezza del membro stringa. Lo schema e i numeri di porta hanno solo un membro che archivia il valore corrispondente. Sia lo schema che i numeri di porta vengono restituiti in tutte le chiamate riuscite a [**WinHttpCrackUrl.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl)

Per recuperare il valore di un componente specifico nella struttura [**\_ COMPONENTS dell'URL,**](/windows/win32/api/winhttp/ns-winhttp-url_components) il membro che archivia la lunghezza della stringa di tale componente deve essere impostato su un valore diverso da zero. Il membro stringa può essere un puntatore a un buffer o **NULL.**

Se il membro puntatore contiene un puntatore a un buffer, il membro di lunghezza della stringa deve contenere le dimensioni di tale buffer. La [**funzione WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) restituisce le informazioni sul componente come stringa nel buffer e archivia la lunghezza della stringa nel membro di lunghezza della stringa.

Se il membro puntatore è impostato su **NULL,** il membro di lunghezza della stringa può essere impostato su qualsiasi valore diverso da zero. La [**funzione WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) archivia un puntatore al primo carattere della stringa URL che contiene le informazioni sul componente e imposta la lunghezza della stringa sul numero di caratteri nella parte rimanente della stringa URL relativa al componente.

Tutti i membri puntatore impostati su **NULL** con un membro di lunghezza diversa da zero puntano al punto iniziale appropriato nella stringa URL. La lunghezza archiviata nel membro length deve essere usata per determinare la fine delle informazioni del singolo componente.

Per completare correttamente l'inizializzazione della struttura [**\_ COMPONENTS dell'URL,**](/windows/win32/api/winhttp/ns-winhttp-url_components) il membro **dwStructSize** deve essere impostato sulla dimensione della struttura [**COMPONENTS \_ dell'URL.**](/windows/win32/api/winhttp/ns-winhttp-url_components)

### <a name="creating-urls"></a>Creazione di URL

La [**funzione WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) usa le informazioni nella struttura [**\_ COMPONENTI URL**](/windows/win32/api/winhttp/ns-winhttp-url_components) descritta in precedenza per creare un URL.

Per ogni componente richiesto, il membro puntatore deve contenere un puntatore al buffer che contiene le informazioni. Il membro length deve essere impostato su zero se il membro puntatore contiene un puntatore a una stringa con terminazione zero. Il membro length deve essere impostato sulla lunghezza della stringa se il membro puntatore contiene un puntatore a una stringa che non ha terminazione zero. Il membro puntatore di tutti i componenti non necessari deve essere impostato su **NULL.**

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



 

 



