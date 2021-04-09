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
# <a name="uniform-resource-locators-urls-in-winhttp"></a><span data-ttu-id="42f3b-103">Uniform Resource Locator (URL) in WinHTTP</span><span class="sxs-lookup"><span data-stu-id="42f3b-103">Uniform Resource Locators (URLs) in WinHTTP</span></span>

<span data-ttu-id="42f3b-104">Un URL è una rappresentazione compatta del percorso e del metodo di accesso per una risorsa che si trova su Internet.</span><span class="sxs-lookup"><span data-stu-id="42f3b-104">A URL is a compact representation of the location and access method for a resource located on the Internet.</span></span> <span data-ttu-id="42f3b-105">Ogni URL è costituito da uno schema (HTTP, HTTPS, FTP o gopher) e da una stringa specifica dello schema.</span><span class="sxs-lookup"><span data-stu-id="42f3b-105">Each URL consists of a scheme (HTTP, HTTPS, FTP, or Gopher) and a scheme-specific string.</span></span> <span data-ttu-id="42f3b-106">Questa stringa può includere anche una combinazione di percorso di directory, stringa di ricerca o nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="42f3b-106">This string can also include a combination of a directory path, search string, or name of the resource.</span></span> <span data-ttu-id="42f3b-107">Le funzioni dei servizi HTTP di Microsoft Windows (WinHTTP) offrono la possibilità di creare, combinare, suddividere e Canonicalize URL.</span><span class="sxs-lookup"><span data-stu-id="42f3b-107">The Microsoft Windows HTTP Services (WinHTTP) functions provide the ability to create, combine, break down, and canonicalize URLs.</span></span> <span data-ttu-id="42f3b-108">Per altre informazioni, vedere [rfc 1738](https://www.ietf.org/rfc/rfc1738.txt), [Uniform Resource Locators](https://www.ietf.org/rfc/rfc1738.txt) e [RFC 2396](https://www.ietf.org/rfc/rfc2396.txt), [Uniform Resource Identifier (URI): sintassi generica](https://www.ietf.org/rfc/rfc1738.txt).</span><span class="sxs-lookup"><span data-stu-id="42f3b-108">For more information, see [RFC 1738](https://www.ietf.org/rfc/rfc1738.txt), [Uniform Resource Locators](https://www.ietf.org/rfc/rfc1738.txt) and [RFC 2396](https://www.ietf.org/rfc/rfc2396.txt), [Uniform Resource Identifiers (URI): Generic Syntax](https://www.ietf.org/rfc/rfc1738.txt).</span></span>

## <a name="what-is-a-canonicalized-url"></a><span data-ttu-id="42f3b-109">Che cos'è un URL in formato canonico?</span><span class="sxs-lookup"><span data-stu-id="42f3b-109">What Is a Canonicalized URL?</span></span>

<span data-ttu-id="42f3b-110">La sintassi e la semantica specificate degli URL lasciano spazio per la variazione e l'errore.</span><span class="sxs-lookup"><span data-stu-id="42f3b-110">The specified syntax and semantics of URLs leaves room for variation and error.</span></span> <span data-ttu-id="42f3b-111">La canonizzazione è il processo di normalizzare un URL effettivo in un formato corretto, standard, "canonical".</span><span class="sxs-lookup"><span data-stu-id="42f3b-111">Canonicalization is the process of normalizing an actual URL into a correct, standard, "canonical" form.</span></span>

<span data-ttu-id="42f3b-112">Questa operazione implica la codifica di alcuni caratteri come sequenze di escape.</span><span class="sxs-lookup"><span data-stu-id="42f3b-112">This involves coding some characters as "escape sequences."</span></span> <span data-ttu-id="42f3b-113">I caratteri alfanumerici US-ASCII non devono essere codificati (le cifre 0-9, le lettere maiuscole A-Z e le lettere minuscole a-z).</span><span class="sxs-lookup"><span data-stu-id="42f3b-113">Alphanumeric US-ASCII characters need not be encoded (the digits 0-9, the capital letters A-Z, and the lowercase letters a-z).</span></span> <span data-ttu-id="42f3b-114">La maggior parte degli altri caratteri deve essere preceduto da un carattere di escape, inclusi i caratteri di controllo, lo spazio, il segno di percentuale, "caratteri unsafe" (<, >, ", \# , {,}, \| , \\ , ^, ~, \[ , \] è) e tutti i caratteri con un punto di codice superiore a 127.</span><span class="sxs-lookup"><span data-stu-id="42f3b-114">Most other characters must be escaped, including control characters, the space character, the percent sign, "unsafe characters" ( <, >, ", \#, {, }, \|, \\, ^, ~, \[, \], and ' ), and all characters with a code point above 127.</span></span>

## <a name="using-the-winhttp-functions-to-handle-urls"></a><span data-ttu-id="42f3b-115">Uso delle funzioni WinHTTP per la gestione degli URL</span><span class="sxs-lookup"><span data-stu-id="42f3b-115">Using the WinHTTP Functions to Handle URLs</span></span>

<span data-ttu-id="42f3b-116">WinHTTP fornisce due funzioni per la gestione degli URL.</span><span class="sxs-lookup"><span data-stu-id="42f3b-116">WinHTTP provides two functions for handling URLs.</span></span> <span data-ttu-id="42f3b-117">[**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) separa un URL nelle relative parti componente e [**WINHTTPCREATEURL**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) crea un URL dai componenti.</span><span class="sxs-lookup"><span data-stu-id="42f3b-117">[**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) separates a URL into its component parts, and [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) creates a URL from components.</span></span>

### <a name="separating-urls"></a><span data-ttu-id="42f3b-118">Separazione degli URL</span><span class="sxs-lookup"><span data-stu-id="42f3b-118">Separating URLs</span></span>

<span data-ttu-id="42f3b-119">La funzione [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) separa un URL nelle relative parti componente e restituisce i componenti indicati dalla struttura dei [**\_ componenti URL**](/windows/win32/api/winhttp/ns-winhttp-url_components) passati alla funzione.</span><span class="sxs-lookup"><span data-stu-id="42f3b-119">The [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) function separates a URL into its component parts and returns the components indicated by the [**URL\_COMPONENTS**](/windows/win32/api/winhttp/ns-winhttp-url_components) structure that is passed to the function.</span></span>

<span data-ttu-id="42f3b-120">I componenti che costituiscono la struttura [**dei \_ componenti URL**](/windows/win32/api/winhttp/ns-winhttp-url_components) sono il numero di schema, il nome host, il numero di porta, il nome utente, la password, il percorso URL e altre informazioni, ad esempio i parametri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="42f3b-120">The components that make up the [**URL\_COMPONENTS**](/windows/win32/api/winhttp/ns-winhttp-url_components) structure are the scheme number, host name, port number, user name, password, URL path, and additional information such as search parameters.</span></span> <span data-ttu-id="42f3b-121">Ogni componente, ad eccezione dello schema e dei numeri di porta, dispone di un membro di stringa che contiene le informazioni e un membro che contiene la lunghezza del membro della stringa.</span><span class="sxs-lookup"><span data-stu-id="42f3b-121">Each component, except the scheme and port numbers, has a string member that holds the information and a member that holds the length of the string member.</span></span> <span data-ttu-id="42f3b-122">Lo schema e i numeri di porta hanno solo un membro che archivia il valore corrispondente. per tutte le chiamate riuscite a [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl)vengono restituiti sia lo schema che i numeri di porta.</span><span class="sxs-lookup"><span data-stu-id="42f3b-122">The scheme and port numbers have only a member that stores the corresponding value; both the scheme and port numbers are returned on all successful calls to [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl).</span></span>

<span data-ttu-id="42f3b-123">Per recuperare il valore di un particolare componente nella struttura [**dei \_ componenti URL**](/windows/win32/api/winhttp/ns-winhttp-url_components) , il membro che archivia la lunghezza di stringa di tale componente deve essere impostato su un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="42f3b-123">To retrieve the value of a particular component in the [**URL\_COMPONENTS**](/windows/win32/api/winhttp/ns-winhttp-url_components) structure, the member that stores the string length of that component must be set to a nonzero value.</span></span> <span data-ttu-id="42f3b-124">Il membro della stringa può essere un puntatore a un buffer o **null**.</span><span class="sxs-lookup"><span data-stu-id="42f3b-124">The string member can be either a pointer to a buffer or **NULL**.</span></span>

<span data-ttu-id="42f3b-125">Se il membro del puntatore contiene un puntatore a un buffer, il membro della lunghezza della stringa deve contenere la dimensione del buffer.</span><span class="sxs-lookup"><span data-stu-id="42f3b-125">If the pointer member contains a pointer to a buffer, the string length member must contain the size of that buffer.</span></span> <span data-ttu-id="42f3b-126">La funzione [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) restituisce le informazioni sul componente come stringa nel buffer e archivia la lunghezza della stringa nel membro della lunghezza della stringa.</span><span class="sxs-lookup"><span data-stu-id="42f3b-126">The [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) function returns the component information as a string in the buffer and stores the string length in the string length member.</span></span>

<span data-ttu-id="42f3b-127">Se il membro del puntatore è impostato su **null**, il membro della lunghezza della stringa può essere impostato su un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="42f3b-127">If the pointer member is set to **NULL**, the string length member can be set to any nonzero value.</span></span> <span data-ttu-id="42f3b-128">La funzione [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) archivia un puntatore al primo carattere della stringa dell'URL che contiene le informazioni sul componente e imposta la lunghezza della stringa sul numero di caratteri nella parte rimanente della stringa dell'URL che riguarda il componente.</span><span class="sxs-lookup"><span data-stu-id="42f3b-128">The [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) function stores a pointer to the first character of the URL string that contains the component information and sets the string length to the number of characters in the remaining part of the URL string that pertains to the component.</span></span>

<span data-ttu-id="42f3b-129">Tutti i membri del puntatore impostati su **null** con un membro di lunghezza diverso da zero puntano al punto di partenza appropriato nella stringa dell'URL.</span><span class="sxs-lookup"><span data-stu-id="42f3b-129">All pointer members set to **NULL** with a nonzero length member point to the appropriate starting point in the URL string.</span></span> <span data-ttu-id="42f3b-130">La lunghezza archiviata nel membro length deve essere utilizzata per determinare la fine delle informazioni del singolo componente.</span><span class="sxs-lookup"><span data-stu-id="42f3b-130">The length stored in the length member must be used to determine the end of the individual component's information.</span></span>

<span data-ttu-id="42f3b-131">Per completare l'inizializzazione corretta della struttura dei [**\_ componenti URL**](/windows/win32/api/winhttp/ns-winhttp-url_components) , è necessario impostare il membro **dwStructSize** sulla dimensione della struttura dei [**\_ componenti URL**](/windows/win32/api/winhttp/ns-winhttp-url_components) .</span><span class="sxs-lookup"><span data-stu-id="42f3b-131">To finish initializing the [**URL\_COMPONENTS**](/windows/win32/api/winhttp/ns-winhttp-url_components) structure properly, the **dwStructSize** member must be set to the size of the [**URL\_COMPONENTS**](/windows/win32/api/winhttp/ns-winhttp-url_components) structure.</span></span>

### <a name="creating-urls"></a><span data-ttu-id="42f3b-132">Creazione di URL</span><span class="sxs-lookup"><span data-stu-id="42f3b-132">Creating URLs</span></span>

<span data-ttu-id="42f3b-133">La funzione [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) usa le informazioni contenute nella struttura dei [**\_ componenti URL**](/windows/win32/api/winhttp/ns-winhttp-url_components) descritti in precedenza per creare un URL.</span><span class="sxs-lookup"><span data-stu-id="42f3b-133">The [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) function uses the information in the previously described [**URL\_COMPONENTS**](/windows/win32/api/winhttp/ns-winhttp-url_components) structure to create a URL.</span></span>

<span data-ttu-id="42f3b-134">Per ogni componente richiesto, il membro del puntatore deve contenere un puntatore al buffer che contiene le informazioni.</span><span class="sxs-lookup"><span data-stu-id="42f3b-134">For each required component, the pointer member should contain a pointer to the buffer that holds the information.</span></span> <span data-ttu-id="42f3b-135">Il membro length deve essere impostato su zero se il membro del puntatore contiene un puntatore a una stringa con terminazione zero. il membro length deve essere impostato sulla lunghezza della stringa se il membro del puntatore contiene un puntatore a una stringa senza terminazione zero.</span><span class="sxs-lookup"><span data-stu-id="42f3b-135">The length member should be set to zero if the pointer member contains a pointer to a zero-terminated string; the length member should be set to the string length if the pointer member contains a pointer to a string that is not zero-terminated.</span></span> <span data-ttu-id="42f3b-136">Il membro del puntatore di tutti i componenti non necessari deve essere impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="42f3b-136">The pointer member of any components that are not required must be set to **NULL**.</span></span>

### <a name="sample-code"></a><span data-ttu-id="42f3b-137">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="42f3b-137">Sample code</span></span>

<span data-ttu-id="42f3b-138">Il codice di esempio seguente illustra come usare [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) e [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) per disassemblare un URL esistente, modificare uno dei relativi componenti e riassemblarlo in un nuovo URL.</span><span class="sxs-lookup"><span data-stu-id="42f3b-138">The following sample code shows how to use the [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) and [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) to disassemble an existing URL, modify one of its components, and reassemble it into a new URL.</span></span>


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



 

 



