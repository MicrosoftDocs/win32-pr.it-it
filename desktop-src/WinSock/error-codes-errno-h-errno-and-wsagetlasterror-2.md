---
description: Nelle applicazioni Winsock, i codici di errore vengono recuperati utilizzando la funzione WSAGetLastError, Windows Sockets sostituisce la funzione GetLastError di Windows.
ms.assetid: cb73fc92-74bd-4c8b-a1c0-6daf4d298aa1
title: Codici di errore-errno, h_errno e WSAGetLastError
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31b547e0b580599aaec27a0b77bfad0ffaa8966e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306990"
---
# <a name="error-codes---errno-h_errno-and-wsagetlasterror"></a><span data-ttu-id="c93d0-103">Codici di errore-errno, h \_ errno e WSAGetLastError</span><span class="sxs-lookup"><span data-stu-id="c93d0-103">Error Codes - errno, h\_errno and WSAGetLastError</span></span>

<span data-ttu-id="c93d0-104">Nelle applicazioni Winsock, i codici di errore vengono recuperati utilizzando la funzione [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) , Windows Sockets sostituisce la funzione [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) di Windows.</span><span class="sxs-lookup"><span data-stu-id="c93d0-104">In Winsock applications, error codes are retrieved using the [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) function, the Windows Sockets substitute for the Windows [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span> <span data-ttu-id="c93d0-105">I codici di errore restituiti dai socket di Windows sono simili alle costanti del codice di errore socket UNIX, ma le costanti hanno tutti il prefisso WSA.</span><span class="sxs-lookup"><span data-stu-id="c93d0-105">The error codes returned by Windows Sockets are similar to UNIX socket error code constants, but the constants are all prefixed with WSA.</span></span> <span data-ttu-id="c93d0-106">Pertanto, nelle applicazioni Winsock viene restituito il codice di errore WSAEWOULDBLOCK, mentre nelle applicazioni UNIX viene restituito il codice di errore EWOULDBLOCK.</span><span class="sxs-lookup"><span data-stu-id="c93d0-106">So in Winsock applications the WSAEWOULDBLOCK error code would be returned, while in UNIX applications the EWOULDBLOCK error code would be returned.</span></span>

<span data-ttu-id="c93d0-107">I codici di errore impostati da Windows Sockets non vengono resi disponibili tramite la variabile *errno* .</span><span class="sxs-lookup"><span data-stu-id="c93d0-107">Error codes set by Windows Sockets are not made available through the *errno* variable.</span></span> <span data-ttu-id="c93d0-108">Per la classe **getXbyY** di funzioni, inoltre, i codici di errore non vengono resi disponibili tramite la variabile *h \_ errno* .</span><span class="sxs-lookup"><span data-stu-id="c93d0-108">Additionally, for the **getXbyY** class of functions, error codes are not made available through the *h\_errno* variable.</span></span> <span data-ttu-id="c93d0-109">La funzione [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) è destinata a fornire un modo affidabile per un thread in un processo multithread per ottenere informazioni sugli errori per thread.</span><span class="sxs-lookup"><span data-stu-id="c93d0-109">The [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) function is intended to provide a reliable way for a thread in a multithreaded process to obtain per-thread error information.</span></span>

<span data-ttu-id="c93d0-110">Per la compatibilità con Berkeley UNIX (BSD), le prime versioni di Windows (Windows 95 con Windows Socket 2 Update e Windows 98, ad esempio) costanti di errore Berkeley regolari ridefinite in genere in *errno. h* in BSD come gli equivalenti errori WSA di Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="c93d0-110">For compatibility with Berkeley UNIX (BSD), early versions of Windows (Windows 95 with the Windows Socket 2 Update and Windows 98, for example) redefined regular Berkeley error constants typically found in *errno.h* on BSD as the equivalent Windows Sockets WSA errors.</span></span> <span data-ttu-id="c93d0-111">Ad esempio, ECONNREFUSED è stato definito come **WSAECONNREFUSED** nel file di intestazione *Winsock. h* .</span><span class="sxs-lookup"><span data-stu-id="c93d0-111">So for example, ECONNREFUSED was defined as **WSAECONNREFUSED** in the *Winsock.h* header file.</span></span> <span data-ttu-id="c93d0-112">Nelle versioni successive di Windows (Windows NT 3,1 e versioni successive) queste definizioni sono state impostate come commento per evitare conflitti con *errno. h* utilizzato con Microsoft C/C++ e Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="c93d0-112">In subsequent versions of Windows (Windows NT 3.1 and later) these defines were commented out to avoid conflicts with *errno.h* used with Microsoft C/C++ and Visual Studio.</span></span>

<span data-ttu-id="c93d0-113">Il file di intestazione *Winsock2. h* incluso nel Software Development Kit (SDK) di Microsoft Windows, Platform Software Development Kit (SDK) e Visual Studio contiene ancora un blocco commentato delle definizioni all'interno di un \# blocco ifdef 0 e \# endif che definiscono i codici di errore del socket BSD in modo che corrispondano alle costanti di errore WSA.</span><span class="sxs-lookup"><span data-stu-id="c93d0-113">The *Winsock2.h* header file included with the Microsoft Windows Software Development Kit (SDK), Platform Software Development Kit (SDK), and Visual Studio still contains a commented out block of defines within an \#ifdef 0 and \#endif block that define the BSD socket error codes to be the same as the WSA error constants.</span></span> <span data-ttu-id="c93d0-114">Questi possono essere usati per garantire una certa compatibilità con la programmazione di socket UNIX, BSD e Linux.</span><span class="sxs-lookup"><span data-stu-id="c93d0-114">These can be used to provide some compatibility with UNIX, BSD, and Linux socket programming.</span></span> <span data-ttu-id="c93d0-115">Per la compatibilità con BSD, un'applicazione può scegliere di modificare *Winsock2. h* e rimuovere il commento dal blocco.</span><span class="sxs-lookup"><span data-stu-id="c93d0-115">For compatibility with BSD, an application may choose to change the *Winsock2.h* and uncomment this block.</span></span> <span data-ttu-id="c93d0-116">Tuttavia, gli sviluppatori di applicazioni si sconsigliano vivamente di rimuovere il commento da questo blocco a causa di conflitti inevitabili con *errno. h* nella maggior parte delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="c93d0-116">However, application developers are strongly discouraged from uncommenting this block because of inevitable conflicts with *errno.h* in most applications.</span></span> <span data-ttu-id="c93d0-117">Gli errori di socket BSD sono inoltre definiti con valori molto diversi da quelli usati nei programmi UNIX, BSD e Linux.</span><span class="sxs-lookup"><span data-stu-id="c93d0-117">Also, the BSD socket errors are defined to very different values than are used in UNIX, BSD, and Linux programs.</span></span> <span data-ttu-id="c93d0-118">Gli sviluppatori di applicazioni sono vivamente invitati a usare le costanti di errore WSA nelle applicazioni socket.</span><span class="sxs-lookup"><span data-stu-id="c93d0-118">Application developers are very strongly encouraged to use the WSA error constants in socket applications.</span></span>

<span data-ttu-id="c93d0-119">Queste definizioni restano impostate come commento nell'intestazione *Winsock2. h* all'interno di un \# blocco ifdef 0 e \# endif.</span><span class="sxs-lookup"><span data-stu-id="c93d0-119">These defines remain commented out in the *Winsock2.h* header within an \#ifdef 0 and \#endif block.</span></span> <span data-ttu-id="c93d0-120">Se uno sviluppatore di applicazioni insiste sull'uso dei codici di errore BSD per la compatibilità, un'applicazione può scegliere di includere una riga nel formato:</span><span class="sxs-lookup"><span data-stu-id="c93d0-120">If an application developer insists on using the BSD error codes for compatibility, then an application may choose to include a line of the form:</span></span>


```C++
#include <windows.h>

#define errno WSAGetLastError()
```



<span data-ttu-id="c93d0-121">In questo modo, il codice di rete scritto per l'utilizzo di *errno* globale funziona correttamente in un ambiente a thread singolo.</span><span class="sxs-lookup"><span data-stu-id="c93d0-121">This allows networking code which was written to use the global *errno* to work correctly in a single-threaded environment.</span></span> <span data-ttu-id="c93d0-122">Ci sono alcuni svantaggi molto gravi.</span><span class="sxs-lookup"><span data-stu-id="c93d0-122">There are some very serious drawbacks.</span></span> <span data-ttu-id="c93d0-123">Se un file di origine include codice che controlla *errno* per le funzioni socket e non socket, questo meccanismo non può essere utilizzato.</span><span class="sxs-lookup"><span data-stu-id="c93d0-123">If a source file includes code which inspects *errno* for both socket and non-socket functions, this mechanism cannot be used.</span></span> <span data-ttu-id="c93d0-124">Non è inoltre possibile che un'applicazione assegni un nuovo valore a *errno*.</span><span class="sxs-lookup"><span data-stu-id="c93d0-124">Furthermore, it is not possible for an application to assign a new value to *errno*.</span></span> <span data-ttu-id="c93d0-125">(In Windows Sockets, la funzione [**WSASetLastError**](/windows/desktop/api/winsock/nf-winsock-wsasetlasterror) può essere usata a questo scopo).</span><span class="sxs-lookup"><span data-stu-id="c93d0-125">(In Windows Sockets, the function [**WSASetLastError**](/windows/desktop/api/winsock/nf-winsock-wsasetlasterror) may be used for this purpose.)</span></span>

<span data-ttu-id="c93d0-126">Stile BSD tipico</span><span class="sxs-lookup"><span data-stu-id="c93d0-126">Typical BSD Style</span></span>


```C++
r = recv(...);
if (r == -1
    && errno == EWOULDBLOCK)
    {...}
```



<span data-ttu-id="c93d0-127">Stile preferito</span><span class="sxs-lookup"><span data-stu-id="c93d0-127">Preferred Style</span></span>


```C++
r = recv(...);
if (r == -1       /* (but see below) */
    && WSAGetLastError() == EWOULDBLOCK)
    {...}
```



<span data-ttu-id="c93d0-128">Sebbene le costanti di errore coerenti con i socket Berkeley 4,3 siano fornite a scopo di compatibilità, le applicazioni sono fortemente incoraggiate a usare le definizioni dei codici di errore WSA.</span><span class="sxs-lookup"><span data-stu-id="c93d0-128">Although error constants consistent with Berkeley Sockets 4.3 are provided for compatibility purposes, applications are strongly encouraged to use the WSA error code definitions.</span></span> <span data-ttu-id="c93d0-129">Questo perché i codici di errore restituiti da alcune funzioni di Windows Sockets rientrano nell'intervallo standard di codici di errore definiti da Microsoft C ©.</span><span class="sxs-lookup"><span data-stu-id="c93d0-129">This is because error codes returned by certain Windows Sockets functions fall into the standard range of error codes as defined by Microsoft C©.</span></span> <span data-ttu-id="c93d0-130">Una versione migliore del frammento di codice sorgente precedente è quindi:</span><span class="sxs-lookup"><span data-stu-id="c93d0-130">Thus, a better version of the preceding source code fragment is:</span></span>


```C++
r = recv(...);
if (r == -1       /* (but see below) */
    && WSAGetLastError() == WSAEWOULDBLOCK)
    {...}
```



<span data-ttu-id="c93d0-131">La specifica Winsock 1,1 originale definita in 1995 consiglia un set di codici di errore ed elenca i possibili errori che possono essere restituiti come risultato di ogni funzione.</span><span class="sxs-lookup"><span data-stu-id="c93d0-131">The original Winsock 1.1 specification defined in 1995 recommended a set of error codes, and listed the possible errors that can be returned as a result of each function.</span></span> <span data-ttu-id="c93d0-132">Windows Sockets 2 ha aggiunto funzioni e funzionalità con altri codici di errore di Windows Sockets restituiti oltre a quelli elencati nella specifica Winsock originale.</span><span class="sxs-lookup"><span data-stu-id="c93d0-132">Windows Sockets 2 added functions and features with other Windows Sockets error codes returned in addition to those listed in the original Winsock specification.</span></span> <span data-ttu-id="c93d0-133">Nel tempo sono state aggiunte funzioni aggiuntive per migliorare Winsock per l'uso da parte degli sviluppatori.</span><span class="sxs-lookup"><span data-stu-id="c93d0-133">Additional functions have been added over time to enhance Winsock for use by developers.</span></span> <span data-ttu-id="c93d0-134">Ad esempio, sono state aggiunte nuove funzioni del servizio nome (ad esempio,[**funzione getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) e [**GetNameInfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo)) che supportano sia IPv6 che IPv4 in Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="c93d0-134">For example, new name service functions ([**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) and [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo), for example) were added that support both IPv6 and IPv4 on Windows XP and later.</span></span> <span data-ttu-id="c93d0-135">Alcune delle funzioni del servizio nomi solo IPv4 precedenti (ad esempio la classe **getXbyY** di funzioni) sono state deprecate.</span><span class="sxs-lookup"><span data-stu-id="c93d0-135">Some of the older IPv4-only name service functions (the **getXbyY** class of functions, for example) have been deprecated.</span></span>

<span data-ttu-id="c93d0-136">Un elenco completo dei codici di errore possibili restituiti dalle funzioni Windows Sockets è indicato nella sezione relativa ai [codici di errore di Windows Sockets](windows-sockets-error-codes-2.md).</span><span class="sxs-lookup"><span data-stu-id="c93d0-136">A complete list of possible error codes returned by Windows Sockets functions is given in the section on [Windows Sockets Error Codes](windows-sockets-error-codes-2.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c93d0-137">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c93d0-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c93d0-138">Gestione degli errori Winsock</span><span class="sxs-lookup"><span data-stu-id="c93d0-138">Handling Winsock Errors</span></span>](handling-winsock-errors.md)
</dt> <dt>

[<span data-ttu-id="c93d0-139">Porting delle applicazioni socket in Winsock</span><span class="sxs-lookup"><span data-stu-id="c93d0-139">Porting Socket Applications to Winsock</span></span>](porting-socket-applications-to-winsock.md)
</dt> <dt>

[<span data-ttu-id="c93d0-140">Codici di errore di Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="c93d0-140">Windows Sockets Error Codes</span></span>](windows-sockets-error-codes-2.md)
</dt> <dt>

[<span data-ttu-id="c93d0-141">Considerazioni sulla programmazione Winsock</span><span class="sxs-lookup"><span data-stu-id="c93d0-141">Winsock Programming Considerations</span></span>](winsock-programming-considerations.md)
</dt> </dl>

 

 
