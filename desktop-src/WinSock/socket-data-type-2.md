---
description: Nelle applicazioni Winsock, un descrittore di socket non è un descrittore di file e deve essere usato con le funzioni Winsock.
ms.assetid: bc434b35-9231-4b03-bc8f-cf59aaeb821e
title: Tipo di dati socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea031032e0d05abc02f7c3c948477c7fe9a1d1de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347066"
---
# <a name="socket-data-type"></a>Tipo di dati socket

Nelle applicazioni Winsock, un descrittore di socket non è un descrittore di file e deve essere usato con le funzioni Winsock.

In UNIX, un descrittore di socket è rappresentato da un descrittore di file standard. Di conseguenza, un descrittore di socket in UNIX può essere passato a una delle funzioni standard di I/O dei file (ad esempio, lettura e scrittura).

Inoltre, tutti gli handle in UNIX, inclusi gli handle di socket, sono numeri interi non negativi e alcune applicazioni si basano su presupposti che questa operazione sarà vera.

Gli handle di Windows Sockets non hanno restrizioni, a parte il valore \_ socket non valido non è un socket valido. Gli handle di socket possono avere un valore compreso nell'intervallo da 0 a socket non valido \_ -1.

Poiché il tipo di **socket** non è firmato, la compilazione del codice sorgente esistente da, ad esempio, un ambiente UNIX può causare avvisi del compilatore sulle mancate corrispondenze tra tipi di dati firmati e non firmati.

Ciò significa, ad esempio, che il controllo degli errori quando le funzioni [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) e [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) restituite non deve essere eseguito confrontando il valore restituito con-1 o verificando se il valore è negativo (approcci comuni e validi in UNIX). Al contrario, un'applicazione deve usare il socket costante manifesto non valido \_ come definito nel file di intestazione *Winsock2. h* . Ad esempio:

Tipico stile BSD UNIX


```C++
s = socket(...);
if (s == -1)    /* or s < 0 */
    {/*...*/}
```



Stile preferito


```C++
s = socket(...);
if (s == INVALID_SOCKET)
    {/*...*/}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Porting delle applicazioni socket in Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[Considerazioni sulla programmazione Winsock](winsock-programming-considerations.md)
</dt> </dl>

 

 



