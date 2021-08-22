---
description: Nelle applicazioni Winsock i codici di errore vengono recuperati usando la funzione WSAGetLastError, che sostituisce Windows Sockets con la Windows GetLastError.
ms.assetid: cb73fc92-74bd-4c8b-a1c0-6daf4d298aa1
title: 'Codici di errore : errno, h_errno e WSAGetLastError'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2e9c4372bd479ee4b94bd3226128737dae3d5637be94046eb013716590ac285
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132634"
---
# <a name="error-codes---errno-h_errno-and-wsagetlasterror"></a>Codici di errore : errno, h \_ errno e WSAGetLastError

Nelle applicazioni Winsock i codici di errore vengono recuperati usando la funzione [**WSAGetLastError,**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) che sostituisce Windows Sockets con la Windows [**GetLastError.**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) I codici di errore restituiti da Windows Socket sono simili UNIX costanti del codice di errore socket, ma tutte le costanti sono precedute da WSA. Nelle applicazioni Winsock viene quindi restituito il codice di errore WSAEWOULDBLOCK, mentre nelle applicazioni UNIX viene restituito il codice di errore EWOULDBLOCK.

I codici di errore impostati Windows socket non vengono resi disponibili tramite la *variabile errno.* Inoltre, per la classe di funzioni **getXbyY,** i codici di errore non vengono resi disponibili tramite la *variabile h \_ errno.* La [**funzione WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) è progettata per fornire a un thread in un processo multithreading un modo affidabile per ottenere informazioni sugli errori per thread.

Per compatibilità con Berkeley UNIX (BSD), le prime versioni di Windows (Windows 95 con Windows Socket 2 Update e Windows 98, ad esempio) ridefinirono le normali costanti di errore Berkeley generalmente presenti in *errno.h* in BSD come errori WSA Windows Sockets equivalenti. Quindi, ad esempio, ECONNREFUSED è stato definito **come WSAECONNREFUSED nel** file *di intestazione Winsock.h.* Nelle versioni successive di Windows (Windows NT 3.1 e versioni successive) queste definizioni sono state commentate per evitare conflitti con *errno.h* usati con Microsoft C/C++ e Visual Studio.

Il file di intestazione *Winsock2.h* incluso in Microsoft Windows Software Development Kit (SDK), Platform Software Development Kit (SDK) e Visual Studio contiene ancora un blocco commentato di defines all'interno di un blocco ifdef 0 ed endif che definiscono i codici di errore del socket BSD in modo che siano gli stessi delle costanti di errore \# \# WSA. Questi possono essere usati per garantire una certa compatibilità con UNIX, BSD e programmazione di socket Linux. Per compatibilità con BSD, un'applicazione può scegliere di modificare *Winsock2.h* e rimuovere il commento da questo blocco. Tuttavia, gli sviluppatori di applicazioni sono fortemente sconsigliati di rimuovere il commento da questo blocco a causa di conflitti inevitabili *con errno.h* nella maggior parte delle applicazioni. Inoltre, gli errori del socket BSD sono definiti con valori molto diversi rispetto a quelli usati nei programmi UNIX, BSD e Linux. Gli sviluppatori di applicazioni sono vivamente invitati a usare le costanti di errore WSA nelle applicazioni socket.

Queste definisce rimangono commentate nell'intestazione *Winsock2.h* all'interno di \# un blocco ifdef 0 \# ed endif. Se uno sviluppatore di applicazioni si indotta a usare i codici di errore BSD per la compatibilità, un'applicazione può scegliere di includere una riga del modulo:


```C++
#include <windows.h>

#define errno WSAGetLastError()
```



In questo modo il codice di rete scritto per usare *l'errno globale* può funzionare correttamente in un ambiente a thread singolo. Esistono alcuni svantaggi molto gravi. Se un file di origine include codice che controlla *errno* per le funzioni socket e non socket, questo meccanismo non può essere usato. Inoltre, non è possibile che un'applicazione assegni un nuovo valore *a errno*. In Windows socket, a questo scopo può essere usata la funzione [**WSASetLastError.**](/windows/desktop/api/winsock/nf-winsock-wsasetlasterror)

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



Sebbene le costanti di errore coerenti con Berkeley Sockets 4.3 siano fornite per motivi di compatibilità, è consigliabile che le applicazioni usino le definizioni del codice di errore WSA. Ciò è dovuto al fatto che i codici di errore restituiti da alcune funzioni Windows Sockets rientrano nell'intervallo standard di codici di errore definito da Microsoft C©. Di conseguenza, una versione migliore del frammento di codice sorgente precedente è:


```C++
r = recv(...);
if (r == -1       /* (but see below) */
    && WSAGetLastError() == WSAEWOULDBLOCK)
    {...}
```



La specifica winsock 1.1 originale definita nel 1995 consiglia un set di codici di errore ed elencati i possibili errori che possono essere restituiti come risultato di ogni funzione. Windows Sockets 2 ha aggiunto funzioni e funzionalità con altri codici di errore Windows Sockets restituiti oltre a quelli elencati nella specifica Winsock originale. Nel corso del tempo sono state aggiunte funzioni aggiuntive per migliorare Winsock per l'uso da parte degli sviluppatori. Ad esempio, sono state aggiunte nuove funzioni del servizio dei nomi ([**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) e [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo), ad esempio) che supportano sia IPv6 che IPv4 in Windows XP e versioni successive. Alcune delle funzioni precedenti del servizio dei nomi solo IPv4 (ad esempio la classe di funzioni **getXbyY)** sono state deprecate.

Un elenco completo dei possibili codici di errore restituiti dalle Windows Sockets è disponibile nella sezione relativa ai codici di errore [Windows Sockets](windows-sockets-error-codes-2.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione degli errori di Winsock](handling-winsock-errors.md)
</dt> <dt>

[Porting di applicazioni socket in Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[Windows Codici di errore dei socket](windows-sockets-error-codes-2.md)
</dt> <dt>

[Considerazioni sulla programmazione winsock](winsock-programming-considerations.md)
</dt> </dl>

 

 
