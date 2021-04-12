---
description: Il file di inclusione originale per l'uso con Windows Sockets 1,1 è il file di intestazione Winsock. h.
ms.assetid: 0536abcc-4277-4bd8-927c-3bf429bc65bb
title: File di inclusione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adf7a4edcd70e6a6280b26f7b6ab9f0f1dab674e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343501"
---
# <a name="include-files"></a>File di inclusione

Il file di inclusione originale per l'uso con Windows Sockets 1,1 è il file di intestazione *Winsock. h* . Per semplificare il porting di codice sorgente esistente basato su socket UNIX Berkeley in Windows Sockets, è stato consigliato di fornire i kit di sviluppo di Windows Sockets per Winsock 1,1 con diversi file di inclusione con gli stessi nomi dei file di inclusione UNIX standard (ad esempio, i file di intestazione *sys/socket. h* e arpa/inet. h). Tuttavia, questi file di intestazione Winsock con nome analogo contengono semplicemente una direttiva per includere il file di intestazione *Winsock2. h* .

Quando Windows Sockets 2 è stato rilasciato, il file di inclusione primario per l'uso con Windows Sockets è stato rinominato in *Winsock2. h*. Il file di intestazione *Winsock. h* precedente per Winsock 1,1 è stato mantenuto anche per la compatibilità con le applicazioni precedenti. Lo sviluppo di applicazioni compatibili con Winsock 1,1 è stato deprecato poiché Windows 2000 è stato rilasciato. Tutte le applicazioni dovrebbero ora usare la direttiva include *Winsock2. h* nei file di origine dell'applicazione Winsock.

Il file di intestazione *Winsock2. h* contiene la maggior parte delle funzioni, delle strutture e delle definizioni Winsock. Il file di intestazione *Ws2tcpip. h* contiene le definizioni introdotte nel documento di allegato WinSock 2 Protocol-Specific per TCP/IP che include funzioni e strutture più recenti utilizzate per recuperare gli indirizzi IP. Sono incluse la famiglia di funzioni [**funzione getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) e [**GetNameInfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) che forniscono la risoluzione dei nomi per gli indirizzi IPv4 o IPv6. Il file di intestazione *Ws2tcpip. h* è necessario solo se le funzioni di denominazione indipendenti dall'IP sono richieste dall'applicazione.

Il file di intestazione *mswsock. h* contiene le definizioni per le estensioni specifiche di Microsoft per Windows Sockets 2 (ad esempio,[**TransmitFile**](/windows/win32/api/mswsock/nf-mswsock-transmitfile), [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex)e [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex)). Il file di intestazione *mswsock. h* non è in genere necessario, a meno che le estensioni specifiche di Microsoft non vengano utilizzate dall'applicazione.

Il file di intestazione *Winsock2. h* include internamente gli elementi di base del file di intestazione di *Windows. h* , quindi non esiste in genere una \# riga di inclusione per il file di intestazione di *Windows. h* nelle applicazioni Winsock. Se \# è necessaria una riga di inclusione per il file di intestazione di *Windows. h* , questa operazione deve essere preceduta dalla macro per la \# definizione e la media di Win32 \_ \_ \_ . Per motivi cronologici, per impostazione predefinita l'intestazione *Windows. h* include il file di intestazione *Winsock. h* per Windows Sockets 1,1. Le dichiarazioni nel file di intestazione *Winsock. h* sono in conflitto con le dichiarazioni nel file di intestazione *Winsock2. h* richiesto da Windows Sockets 2. La \_ macro Win32 snello \_ e \_ media impedisce che *Winsock. h* venga incluso nell'intestazione *Windows. h* . Di seguito è riportato un esempio che illustra questo problema.


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

[Introduzione con Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Porting delle applicazioni socket in Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[Considerazioni sulla programmazione Winsock](winsock-programming-considerations.md)
</dt> </dl>

 

 
