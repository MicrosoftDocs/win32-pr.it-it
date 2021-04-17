---
title: Gestione dei cookie
description: Con il protocollo http, un server o uno script usa i cookie per mantenere le informazioni sullo stato nella workstation client.
ms.assetid: c00279cf-9cdc-4caf-8549-af1851edfa25
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed0418442e961f6f4d3d2bcddb2c607ac9cf7928
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300166"
---
# <a name="managing-cookies"></a>Gestione dei cookie

Con il protocollo http, un server o uno script usa i cookie per mantenere le informazioni sullo stato nella workstation client. Per questo scopo, le funzioni WinINet hanno implementato un database di cookie permanente. Possono essere usati per impostare i cookie in e accedere ai cookie dal database dei cookie. Per ulteriori informazioni, vedere [http cookies](http-cookies.md).

Le funzioni [**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) e [**InternetGetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea) possono essere utilizzate per gestire i cookie.

## <a name="using-cookie-functions"></a>Uso delle funzioni cookie

Le funzioni seguenti consentono a un'applicazione di creare o recuperare cookie nel database dei cookie.



| Funzione                                       | Descrizione                                                      |
|------------------------------------------------|------------------------------------------------------------------|
| [**InternetGetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea) | Recupera i cookie per l'URL specificato e per tutti i relativi URL padre. |
| [**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) | Imposta un cookie sull'URL specificato.                              |



 

Si noti che queste funzioni non richiedono una chiamata a [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena). I cookie con una data di scadenza vengono archiviati nell'account degli utenti locali sotto la \\ directory "username" \\ AppData \\ roaming di \\ Microsoft \\ Windows \\ cookies e il \\ nome utente "username" \\ AppData \\ roaming \\ Microsoft \\ Windows \\ cookies \\ low directory per le applicazioni in esecuzione con privilegi limitati. I cookie che non dispongono di una data di scadenza vengono archiviati in memoria e sono disponibili solo per il processo in cui sono stati creati.

Come indicato nell'argomento [http cookies](http-cookies.md) , la funzione [**InternetGetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea) non restituisce i cookie contrassegnati dal server come non configurabili tramite script con l'attributo "HttpOnly" nell'intestazione Set-Cookie.

### <a name="getting-a-cookie"></a>Recupero di un cookie

[**InternetGetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea) restituisce i cookie per l'URL specificato e per tutti i relativi URL padre.

Nell'esempio seguente viene illustrata una chiamata a [**InternetGetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea).


```C++
TCHAR szURL[256];         // buffer to hold the URL
LPTSTR lpszData = NULL;   // buffer to hold the cookie data
DWORD dwSize=0;           // variable to get the buffer size needed

// Insert code to retrieve the URL.

retry:

// The first call to InternetGetCookie will get the required
// buffer size needed to download the cookie data.
if (!InternetGetCookie(szURL, NULL, lpszData, &dwSize))
{
    // Check for an insufficient buffer error.
    if (GetLastError()== ERROR_INSUFFICIENT_BUFFER)
    {
        // Allocate the necessary buffer.
        lpszData = new TCHAR[dwSize];

        // Try the call again.
        goto retry;
    }
    else
    {
        // Insert error handling code.
    }
}
else
{
    // Insert code to display the cookie data.

    // Release the memory allocated for the buffer.
    delete[]lpszData;
}
```



### <a name="setting-a-cookie"></a>Impostazione di un cookie

[**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) viene usato per impostare un cookie nell'URL specificato. [**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) può creare cookie di sessione e permanenti.

I cookie permanenti hanno una data di scadenza. Questi cookie vengono archiviati nell'account degli utenti locali sotto la \\ directory "username" di \\ AppData \\ roaming di \\ Microsoft \\ Windows \\ cookies e il \\ nome utente "username" \\ AppData \\ roaming \\ \\ di Microsoft Windows \\ cookies \\ low directory per le applicazioni in esecuzione con privilegi limitati.

I cookie di sessione vengono archiviati in memoria ed è possibile accedervi solo dal processo che li ha creati.

Il formato dei dati per il cookie deve essere il seguente:

``` syntax
NAME=VALUE
```

Per la data di scadenza, il formato deve essere:

``` syntax
DAY, DD-MMM-YYYY HH:MM:SS GMT
```

DAY è l'abbreviazione di tre lettere per il giorno della settimana, GG è il giorno del mese, MMM è l'abbreviazione di tre lettere per il mese, AAAA è l'anno e HH: MM: SS è l'ora del giorno in tempo militare.

Nell'esempio seguente vengono illustrate due chiamate a [**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea). La prima chiamata crea un cookie di sessione e il secondo crea un cookie permanente.


```C++
BOOL bReturn;

// Create a session cookie.
bReturn = InternetSetCookie(TEXT("https://www.adventure_works.com"), NULL,
            TEXT("TestData = Test"));

// Create a persistent cookie.
bReturn = InternetSetCookie(TEXT("https://www.adventure_works.com"), NULL,
           TEXT("TestData = Test; expires = Sat,01-Jan-2000 00:00:00 GMT"));

```



> [!Note]  
> WinINet non supporta le implementazioni del server. Inoltre, non deve essere utilizzato da un servizio. Per le implementazioni o i servizi del server, usare i [Servizi http di Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 