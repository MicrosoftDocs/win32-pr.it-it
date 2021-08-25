---
title: Bluetooth Programmazione con Windows Socket
description: In questa sezione viene descritto come usare le Windows e le strutture socket per programmare un'Bluetooth applicazione.
ms.assetid: 0f15cb84-1d7a-4b64-86e8-b1b23c956c64
keywords:
- Bluetooth, attività
- Windows Sockets
- programmazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a20cebe459f17601c1c0cbb916be8844b1edbf3b36f974b47ce0d9b28d301d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004091"
---
# <a name="bluetooth-programming-with-windows-sockets"></a>Bluetooth Programmazione con Windows Socket

In questa sezione viene descritto come usare le Windows e le strutture socket per programmare un'Bluetooth applicazione. Informazioni di riferimento complete per gli Windows dell'API Sockets sono disponibili in [Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2); In questa sezione vengono fornite Bluetooth specifiche specifiche per ogni Windows di programmazione Sockets.

È anche possibile scaricare [l'esempio Bluetooth di connessione](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Bluetooth%20connection%20sample) per un esempio completo.

Come per tutte le Windows di applicazioni Sockets, la funzione [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) deve essere chiamata per avviare la funzionalità Windows Sockets e abilitare Bluetooth.

Gli argomenti seguenti forniscono indicazioni sull'uso di funzioni e Windows Sockets con l'API Bluetooth Microsoft:



| Argomento                                                                                            | Descrizione                                                                                                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Bluetooth e accettare](bluetooth-and-accept.md)                                                 | Bluetooth usa la [**funzione accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) per abilitare i tentativi di connessione in ingresso su un socket.<br/>                                                                                                                                                                                                  |
| [Bluetooth e binding](bluetooth-and-bind.md)                                                     | Bluetooth usa la [**funzione bind**](/windows/desktop/api/winsock/nf-winsock-bind) per l'associazione a un socket.<br/>                                                                                                                                                                                                                                     |
| [Bluetooth e BLOB](bluetooth-and-blob.md)                                                     | Bluetooth usa la struttura [**BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob) per passare o ricevere dati specifici del trasporto alla struttura [**WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md) durante le chiamate alle funzioni [**WSASetService**](bluetooth-and-wsasetservice.md) **o WSALookupService.** \* <br/>             |
| [Bluetooth e connettersi](bluetooth-and-connect.md)                                               | Bluetooth usa la funzione [**connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) per connettersi a un dispositivo Bluetooth destinazione, usando un socket Bluetooth creato in precedenza.<br/>                                                                                                                                                              |
| [Bluetooth e getaddrinfo](bluetooth-and-getaddrinfo.md)                                       | La [**funzione getaddrinfo**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo) fornisce la conversione dal nome host all'indirizzo per i trasporti basati su IP.<br/>                                                                                                                                                                                   |
| [Bluetooth e getpeername](bluetooth-and-getpeername.md)                                       | Usato per recuperare l'Bluetooth del peer Bluetooth dispositivo.<br/>                                                                                                                                                                                                                                            |
| [Bluetooth e getsockname](bluetooth-and-getsockname.md)                                       | Bluetooth usa la [**funzione getsockname**](/windows/desktop/api/winsock/nf-winsock-getsockname) per recuperare l'indirizzo del dispositivo server e il numero di porta allocati a un socket tramite una chiamata precedente alla [**funzione bind.**](/windows/desktop/api/winsock/nf-winsock-bind)<br/>                                                                                            |
| [Bluetooth e getsockopt](bluetooth-and-getsockopt.md)                                         | Bluetooth usa la [**funzione getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) per eseguire query su vari parametri associati al canale del server o alla connessione. <br/>                                                                                                                                                           |
| [Bluetooth e ascoltare, selezionare e chiuderesocket](bluetooth-and-listen-select-and-closesocket.md) | Bluetooth usa le funzioni [**listen**](/windows/desktop/api/winsock2/nf-winsock2-listen), [**select**](/windows/desktop/api/winsock2/nf-winsock2-select)e [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) senza alcuna modifica dalla programmazione standard Windows Sockets.<br/>                                                                                                   |
| [Bluetooth operazioni di lettura o scrittura](bluetooth-and-read-or-write-operations.md)             | Informazioni dettagliate sulle operazioni di lettura e scrittura di Winsock supportate.<br/>                                                                                                                                                                                                                                                        |
| [Bluetooth e setsockopt](bluetooth-and-setsockopt.md)                                         | Bluetooth usa la [**funzione setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) per impostare vari parametri associati al canale del server o alla connessione.<br/>                                                                                                                                                              |
| [Bluetooth e arresto](bluetooth-and-shutdown.md)                                             | Bluetooth usa la [**funzione di**](/windows/desktop/api/winsock/nf-winsock-shutdown) arresto per disconnettersi dalla radio remota.<br/>                                                                                                                                                                                                             |
| [Bluetooth e socket](bluetooth-and-socket.md)                                                 | Bluetooth usa la funzione [**socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) crea un socket per le connessioni in ingresso o in uscita.<br/>                                                                                                                                                                                               |
| [Bluetooth e socket](bluetooth-and-socket-options.md)                                 | Informazioni dettagliate sulle opzioni socket supportate da Microsoft Bluetooth.<br/>                                                                                                                                                                                                                                                    |
| [Bluetooth e WSAAddressToString](bluetooth-and-wsaaddresstostring.md)                         | Usato per convertire un indirizzo Bluetooth in una stringa, che viene a sua volta fornita alla funzione [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) tramite la struttura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) durante il recupero delle informazioni sul servizio del dispositivo.<br/>                                           |
| [Bluetooth e WSALookupServiceBegin](bluetooth-and-wsalookupservicebegin.md)                   | Bluetooth usa la [**funzione WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) per eseguire query per i dispositivi e individuare i servizi.<br/>                                                                                                                                                                         |
| [Bluetooth e WSALookupServiceNext](bluetooth-and-wsalookupservicenext.md)                     | Bluetooth usa la [**funzione WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) per trovare la corrispondenza con le query specificate in una chiamata precedente a [**WSALookupServiceBegin.**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)<br/>                                                                                                           |
| [Bluetooth e WSALookupServiceEnd](bluetooth-and-wsalookupserviceend.md)                       | Bluetooth usa la funzione [**WSALookupServiceEnd**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend) per terminare una query avviata in una chiamata precedente a [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)e forse estesa nelle chiamate successive a [**WSALookupServiceNext.**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)<br/> |
| [Bluetooth e WSAQUERYSET](bluetooth-and-wsaqueryset.md)                                       | La [**struttura WSAQUERYSET viene**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) utilizzata nelle operazioni che includono la richiesta del dispositivo, la richiesta di assistenza e l'impostazione del servizio.<br/>                                                                                                                                                                |
| [Bluetooth e WSASetService](bluetooth-and-wsasetservice.md)                                   | Bluetooth usa la funzione [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) per registrare o rimuovere un'istanza del servizio all'interno dello spazio dei nomi Bluetooth (NS \_ BTH) dal Registro di sistema.<br/>                                                                                                                                   |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

