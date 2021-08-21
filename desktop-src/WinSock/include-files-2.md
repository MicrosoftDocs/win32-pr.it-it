---
description: Il file di inclusione originale da usare con Windows Sockets 1.1 era il file di intestazione Winsock.h.
ms.assetid: 0536abcc-4277-4bd8-927c-3bf429bc65bb
title: File di inclusione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 740bde9fae96aa3088a4317c66479bcc75176ee3b9ca9f5e390365c5ef481109
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051529"
---
# <a name="include-files"></a>File di inclusione

Il file di inclusione originale da usare con Windows Sockets 1.1 era il file di *intestazione Winsock.h.* Per semplificare il porting del codice sorgente esistente basato su socket di berkeley UNIX a socket Windows, i kit di sviluppo Windows Sockets per Winsock 1.1 sono stati invitati a essere forniti con diversi file di inclusione con gli stessi nomi dei file di inclusione UNIX standard (ad esempio i file di intestazione *sys/socket.h* e arpa/inet.h). Tuttavia, questi file di intestazione Winsock simili contenevano semplicemente una direttiva per includere il file di intestazione *Winsock2.h.*

Quando Windows socket 2 è stato rilasciato, il file di inclusione primario da usare con Windows Sockets è stato *rinominato in Winsock2.h.* Anche il file di *intestazione Winsock.h* originale precedente per Winsock 1.1 è stato mantenuto per garantire la compatibilità con le applicazioni precedenti. Lo sviluppo di applicazioni compatibili con Winsock 1.1 è stato deprecato Windows 2000. Tutte le applicazioni devono ora usare la direttiva include *Winsock2.h* nei file di origine dell'applicazione Winsock.

Il file *di intestazione Winsock2.h* contiene la maggior parte delle funzioni, delle strutture e delle definizioni di Winsock. Il file di intestazione *Ws2tcpip.h* contiene le definizioni introdotte nel documento Annex di WinSock 2 Protocol-Specific per TCP/IP che include le funzioni e le strutture più recenti usate per recuperare gli indirizzi IP. tra cui la famiglia di funzioni [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) e [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) che forniscono la risoluzione dei nomi per gli indirizzi IPv4 o IPv6. Il file di intestazione *Ws2tcpip.h* è necessario solo se queste funzioni di denominazione indipendenti da IP sono richieste dall'applicazione.

Il file di intestazione *Mswsock.h* contiene le definizioni per le estensioni specifiche di Microsoft per Windows Sockets 2 ([**TransmitFile**](/windows/win32/api/mswsock/nf-mswsock-transmitfile), [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex)e [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex), ad esempio). Il file *di intestazione Mswsock.h* non è normalmente necessario a meno che queste estensioni specifiche di Microsoft non vengano usate dall'applicazione.

Il file di *intestazione Winsock2.h* include internamente elementi di base del file di intestazione *Windows.h,* pertanto non è in genere presente una riga di inclusione per il file di intestazione \# *Windows.h* nelle applicazioni Winsock. Se è necessaria una riga di inclusione per il file di intestazione \# *Windows.h,* deve essere preceduta dalla \# macro DEFINE WIN32 \_ LEAN AND \_ \_ MEAN. Per motivi cronologici, *l'intestazione Windows.h* include per impostazione predefinita il file di *intestazione Winsock.h* per Windows Sockets 1.1. Le dichiarazioni nel file di intestazione *Winsock.h* saranno in conflitto con le dichiarazioni nel file di intestazione *Winsock2.h* richieste da Windows Sockets 2. La macro WIN32 LEAN AND MEAN impedisce \_ \_ che \_ *Winsock.h* venga incluso *dall'intestazione Windows.h.* Di seguito è riportato un esempio che illustra questa operazione.


```C++
#include <winsock2.h>
#include <ws2tcpip.h>
#include <stdio.h>

#pragma comment(lib, "Ws2_32.lib")

int main() {
  return 0;
}

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di un'applicazione Winsock di base](creating-a-basic-winsock-application.md)
</dt> <dt>

[Attività iniziali con Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Porting di applicazioni socket in Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[Considerazioni sulla programmazione di Winsock](winsock-programming-considerations.md)
</dt> </dl>

 

 
