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
# <a name="error-codes---errno-h_errno-and-wsagetlasterror"></a>Codici di errore-errno, h \_ errno e WSAGetLastError

Nelle applicazioni Winsock, i codici di errore vengono recuperati utilizzando la funzione [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) , Windows Sockets sostituisce la funzione [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) di Windows. I codici di errore restituiti dai socket di Windows sono simili alle costanti del codice di errore socket UNIX, ma le costanti hanno tutti il prefisso WSA. Pertanto, nelle applicazioni Winsock viene restituito il codice di errore WSAEWOULDBLOCK, mentre nelle applicazioni UNIX viene restituito il codice di errore EWOULDBLOCK.

I codici di errore impostati da Windows Sockets non vengono resi disponibili tramite la variabile *errno* . Per la classe **getXbyY** di funzioni, inoltre, i codici di errore non vengono resi disponibili tramite la variabile *h \_ errno* . La funzione [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) è destinata a fornire un modo affidabile per un thread in un processo multithread per ottenere informazioni sugli errori per thread.

Per la compatibilità con Berkeley UNIX (BSD), le prime versioni di Windows (Windows 95 con Windows Socket 2 Update e Windows 98, ad esempio) costanti di errore Berkeley regolari ridefinite in genere in *errno. h* in BSD come gli equivalenti errori WSA di Windows Sockets. Ad esempio, ECONNREFUSED è stato definito come **WSAECONNREFUSED** nel file di intestazione *Winsock. h* . Nelle versioni successive di Windows (Windows NT 3,1 e versioni successive) queste definizioni sono state impostate come commento per evitare conflitti con *errno. h* utilizzato con Microsoft C/C++ e Visual Studio.

Il file di intestazione *Winsock2. h* incluso nel Software Development Kit (SDK) di Microsoft Windows, Platform Software Development Kit (SDK) e Visual Studio contiene ancora un blocco commentato delle definizioni all'interno di un \# blocco ifdef 0 e \# endif che definiscono i codici di errore del socket BSD in modo che corrispondano alle costanti di errore WSA. Questi possono essere usati per garantire una certa compatibilità con la programmazione di socket UNIX, BSD e Linux. Per la compatibilità con BSD, un'applicazione può scegliere di modificare *Winsock2. h* e rimuovere il commento dal blocco. Tuttavia, gli sviluppatori di applicazioni si sconsigliano vivamente di rimuovere il commento da questo blocco a causa di conflitti inevitabili con *errno. h* nella maggior parte delle applicazioni. Gli errori di socket BSD sono inoltre definiti con valori molto diversi da quelli usati nei programmi UNIX, BSD e Linux. Gli sviluppatori di applicazioni sono vivamente invitati a usare le costanti di errore WSA nelle applicazioni socket.

Queste definizioni restano impostate come commento nell'intestazione *Winsock2. h* all'interno di un \# blocco ifdef 0 e \# endif. Se uno sviluppatore di applicazioni insiste sull'uso dei codici di errore BSD per la compatibilità, un'applicazione può scegliere di includere una riga nel formato:


```C++
#include <windows.h>

#define errno WSAGetLastError()
```



In questo modo, il codice di rete scritto per l'utilizzo di *errno* globale funziona correttamente in un ambiente a thread singolo. Ci sono alcuni svantaggi molto gravi. Se un file di origine include codice che controlla *errno* per le funzioni socket e non socket, questo meccanismo non può essere utilizzato. Non è inoltre possibile che un'applicazione assegni un nuovo valore a *errno*. (In Windows Sockets, la funzione [**WSASetLastError**](/windows/desktop/api/winsock/nf-winsock-wsasetlasterror) può essere usata a questo scopo).

Stile BSD tipico


```C++
r = recv(...);
if (r == -1
    && errno == EWOULDBLOCK)
    {...}
```



Stile preferito


```C++
r = recv(...);
if (r == -1       /* (but see below) */
    && WSAGetLastError() == EWOULDBLOCK)
    {...}
```



Sebbene le costanti di errore coerenti con i socket Berkeley 4,3 siano fornite a scopo di compatibilità, le applicazioni sono fortemente incoraggiate a usare le definizioni dei codici di errore WSA. Questo perché i codici di errore restituiti da alcune funzioni di Windows Sockets rientrano nell'intervallo standard di codici di errore definiti da Microsoft C ©. Una versione migliore del frammento di codice sorgente precedente è quindi:


```C++
r = recv(...);
if (r == -1       /* (but see below) */
    && WSAGetLastError() == WSAEWOULDBLOCK)
    {...}
```



La specifica Winsock 1,1 originale definita in 1995 consiglia un set di codici di errore ed elenca i possibili errori che possono essere restituiti come risultato di ogni funzione. Windows Sockets 2 ha aggiunto funzioni e funzionalità con altri codici di errore di Windows Sockets restituiti oltre a quelli elencati nella specifica Winsock originale. Nel tempo sono state aggiunte funzioni aggiuntive per migliorare Winsock per l'uso da parte degli sviluppatori. Ad esempio, sono state aggiunte nuove funzioni del servizio nome (ad esempio,[**funzione getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) e [**GetNameInfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo)) che supportano sia IPv6 che IPv4 in Windows XP e versioni successive. Alcune delle funzioni del servizio nomi solo IPv4 precedenti (ad esempio la classe **getXbyY** di funzioni) sono state deprecate.

Un elenco completo dei codici di errore possibili restituiti dalle funzioni Windows Sockets è indicato nella sezione relativa ai [codici di errore di Windows Sockets](windows-sockets-error-codes-2.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione degli errori Winsock](handling-winsock-errors.md)
</dt> <dt>

[Porting delle applicazioni socket in Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[Codici di errore di Windows Sockets](windows-sockets-error-codes-2.md)
</dt> <dt>

[Considerazioni sulla programmazione Winsock](winsock-programming-considerations.md)
</dt> </dl>

 

 
