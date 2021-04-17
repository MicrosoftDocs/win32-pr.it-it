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
# <a name="managing-cookies"></a><span data-ttu-id="5ce22-103">Gestione dei cookie</span><span class="sxs-lookup"><span data-stu-id="5ce22-103">Managing Cookies</span></span>

<span data-ttu-id="5ce22-104">Con il protocollo http, un server o uno script usa i cookie per mantenere le informazioni sullo stato nella workstation client.</span><span class="sxs-lookup"><span data-stu-id="5ce22-104">Under the http protocol, a server or a script uses cookies to maintain state information on the client workstation.</span></span> <span data-ttu-id="5ce22-105">Per questo scopo, le funzioni WinINet hanno implementato un database di cookie permanente.</span><span class="sxs-lookup"><span data-stu-id="5ce22-105">The WinINet functions have implemented a persistent cookie database for this purpose.</span></span> <span data-ttu-id="5ce22-106">Possono essere usati per impostare i cookie in e accedere ai cookie dal database dei cookie.</span><span class="sxs-lookup"><span data-stu-id="5ce22-106">They can be used to set cookies in and access cookies from the cookie database.</span></span> <span data-ttu-id="5ce22-107">Per ulteriori informazioni, vedere [http cookies](http-cookies.md).</span><span class="sxs-lookup"><span data-stu-id="5ce22-107">For more information, see [HTTP Cookies](http-cookies.md).</span></span>

<span data-ttu-id="5ce22-108">Le funzioni [**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) e [**InternetGetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea) possono essere utilizzate per gestire i cookie.</span><span class="sxs-lookup"><span data-stu-id="5ce22-108">The [**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) and [**InternetGetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea) functions can be used to manage cookies.</span></span>

## <a name="using-cookie-functions"></a><span data-ttu-id="5ce22-109">Uso delle funzioni cookie</span><span class="sxs-lookup"><span data-stu-id="5ce22-109">Using Cookie Functions</span></span>

<span data-ttu-id="5ce22-110">Le funzioni seguenti consentono a un'applicazione di creare o recuperare cookie nel database dei cookie.</span><span class="sxs-lookup"><span data-stu-id="5ce22-110">The following functions allow an application to create or retrieve cookies in the cookie database.</span></span>



| <span data-ttu-id="5ce22-111">Funzione</span><span class="sxs-lookup"><span data-stu-id="5ce22-111">Function</span></span>                                       | <span data-ttu-id="5ce22-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5ce22-112">Description</span></span>                                                      |
|------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="5ce22-113">**InternetGetCookie**</span><span class="sxs-lookup"><span data-stu-id="5ce22-113">**InternetGetCookie**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea) | <span data-ttu-id="5ce22-114">Recupera i cookie per l'URL specificato e per tutti i relativi URL padre.</span><span class="sxs-lookup"><span data-stu-id="5ce22-114">Retrieves cookies for the specified URL and all its parent URLs.</span></span> |
| [<span data-ttu-id="5ce22-115">**InternetSetCookie**</span><span class="sxs-lookup"><span data-stu-id="5ce22-115">**InternetSetCookie**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) | <span data-ttu-id="5ce22-116">Imposta un cookie sull'URL specificato.</span><span class="sxs-lookup"><span data-stu-id="5ce22-116">Sets a cookie on the specified URL.</span></span>                              |



 

<span data-ttu-id="5ce22-117">Si noti che queste funzioni non richiedono una chiamata a [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span><span class="sxs-lookup"><span data-stu-id="5ce22-117">Note that these functions do not require a call to [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span></span> <span data-ttu-id="5ce22-118">I cookie con una data di scadenza vengono archiviati nell'account degli utenti locali sotto la \\ directory "username" \\ AppData \\ roaming di \\ Microsoft \\ Windows \\ cookies e il \\ nome utente "username" \\ AppData \\ roaming \\ Microsoft \\ Windows \\ cookies \\ low directory per le applicazioni in esecuzione con privilegi limitati.</span><span class="sxs-lookup"><span data-stu-id="5ce22-118">Cookies that have an expiration date are stored in the local users account under Users\\"username"\\AppData\\Roaming\\Microsoft\\Windows\\Cookies directory, and the Users\\"username"\\AppData\\Roaming\\Microsoft\\Windows\\Cookies\\Low directory for applications running under low privileges.</span></span> <span data-ttu-id="5ce22-119">I cookie che non dispongono di una data di scadenza vengono archiviati in memoria e sono disponibili solo per il processo in cui sono stati creati.</span><span class="sxs-lookup"><span data-stu-id="5ce22-119">Cookies that do not have an expiration date are stored in memory and are available only to the process in which they were created.</span></span>

<span data-ttu-id="5ce22-120">Come indicato nell'argomento [http cookies](http-cookies.md) , la funzione [**InternetGetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea) non restituisce i cookie contrassegnati dal server come non configurabili tramite script con l'attributo "HttpOnly" nell'intestazione Set-Cookie.</span><span class="sxs-lookup"><span data-stu-id="5ce22-120">As noted in the [HTTP Cookies](http-cookies.md) topic, the [**InternetGetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea) function does not return cookies that have been marked by the server as non-scriptable with the "HttpOnly" attribute in the Set-Cookie header.</span></span>

### <a name="getting-a-cookie"></a><span data-ttu-id="5ce22-121">Recupero di un cookie</span><span class="sxs-lookup"><span data-stu-id="5ce22-121">Getting a Cookie</span></span>

<span data-ttu-id="5ce22-122">[**InternetGetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea) restituisce i cookie per l'URL specificato e per tutti i relativi URL padre.</span><span class="sxs-lookup"><span data-stu-id="5ce22-122">[**InternetGetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea) returns the cookies for the specified URL and all its parent URLs.</span></span>

<span data-ttu-id="5ce22-123">Nell'esempio seguente viene illustrata una chiamata a [**InternetGetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea).</span><span class="sxs-lookup"><span data-stu-id="5ce22-123">The following example demonstrates a call to [**InternetGetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea).</span></span>


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



### <a name="setting-a-cookie"></a><span data-ttu-id="5ce22-124">Impostazione di un cookie</span><span class="sxs-lookup"><span data-stu-id="5ce22-124">Setting a Cookie</span></span>

<span data-ttu-id="5ce22-125">[**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) viene usato per impostare un cookie nell'URL specificato.</span><span class="sxs-lookup"><span data-stu-id="5ce22-125">[**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) is used to set a cookie on the specified URL.</span></span> <span data-ttu-id="5ce22-126">[**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) può creare cookie di sessione e permanenti.</span><span class="sxs-lookup"><span data-stu-id="5ce22-126">[**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) can create both persistent and session cookies.</span></span>

<span data-ttu-id="5ce22-127">I cookie permanenti hanno una data di scadenza.</span><span class="sxs-lookup"><span data-stu-id="5ce22-127">Persistent cookies have an expiration date.</span></span> <span data-ttu-id="5ce22-128">Questi cookie vengono archiviati nell'account degli utenti locali sotto la \\ directory "username" di \\ AppData \\ roaming di \\ Microsoft \\ Windows \\ cookies e il \\ nome utente "username" \\ AppData \\ roaming \\ \\ di Microsoft Windows \\ cookies \\ low directory per le applicazioni in esecuzione con privilegi limitati.</span><span class="sxs-lookup"><span data-stu-id="5ce22-128">These cookies are stored in the local users account under Users\\"username"\\AppData\\Roaming\\Microsoft\\Windows\\Cookies directory, and the Users\\"username"\\AppData\\Roaming\\Microsoft\\Windows\\Cookies\\Low directory for applications running under low privileges.</span></span>

<span data-ttu-id="5ce22-129">I cookie di sessione vengono archiviati in memoria ed è possibile accedervi solo dal processo che li ha creati.</span><span class="sxs-lookup"><span data-stu-id="5ce22-129">Session cookies are stored in memory and can be accessed only by the process that created them.</span></span>

<span data-ttu-id="5ce22-130">Il formato dei dati per il cookie deve essere il seguente:</span><span class="sxs-lookup"><span data-stu-id="5ce22-130">The data for the cookie should be in the format:</span></span>

``` syntax
NAME=VALUE
```

<span data-ttu-id="5ce22-131">Per la data di scadenza, il formato deve essere:</span><span class="sxs-lookup"><span data-stu-id="5ce22-131">For the expiration date, the format must be:</span></span>

``` syntax
DAY, DD-MMM-YYYY HH:MM:SS GMT
```

<span data-ttu-id="5ce22-132">DAY è l'abbreviazione di tre lettere per il giorno della settimana, GG è il giorno del mese, MMM è l'abbreviazione di tre lettere per il mese, AAAA è l'anno e HH: MM: SS è l'ora del giorno in tempo militare.</span><span class="sxs-lookup"><span data-stu-id="5ce22-132">DAY is the three-letter abbreviation for the day of the week, DD is the day of the month, MMM is the three-letter abbreviation for the month, YYYY is the year, and HH:MM:SS is the time of the day in military time.</span></span>

<span data-ttu-id="5ce22-133">Nell'esempio seguente vengono illustrate due chiamate a [**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea).</span><span class="sxs-lookup"><span data-stu-id="5ce22-133">The following example demonstrates two calls to [**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea).</span></span> <span data-ttu-id="5ce22-134">La prima chiamata crea un cookie di sessione e il secondo crea un cookie permanente.</span><span class="sxs-lookup"><span data-stu-id="5ce22-134">The first call creates a session cookie and the second creates a persistent cookie.</span></span>


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
> <span data-ttu-id="5ce22-135">WinINet non supporta le implementazioni del server.</span><span class="sxs-lookup"><span data-stu-id="5ce22-135">WinINet does not support server implementations.</span></span> <span data-ttu-id="5ce22-136">Inoltre, non deve essere utilizzato da un servizio.</span><span class="sxs-lookup"><span data-stu-id="5ce22-136">In addition, it should not be used from a service.</span></span> <span data-ttu-id="5ce22-137">Per le implementazioni o i servizi del server, usare i [Servizi http di Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="5ce22-137">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 