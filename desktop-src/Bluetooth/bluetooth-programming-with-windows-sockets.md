---
title: Programmazione Bluetooth con Windows Sockets
description: Questa sezione descrive come usare le funzioni e le strutture di Windows Sockets per programmare un'applicazione Bluetooth.
ms.assetid: 0f15cb84-1d7a-4b64-86e8-b1b23c956c64
keywords:
- Bluetooth, attività
- Windows Sockets
- programmazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca797121696af8eb36549bf596ad51ee8189c3cd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299876"
---
# <a name="bluetooth-programming-with-windows-sockets"></a>Programmazione Bluetooth con Windows Sockets

Questa sezione descrive come usare le funzioni e le strutture di Windows Sockets per programmare un'applicazione Bluetooth. Le informazioni di riferimento complete per gli elementi dell'API Windows Sockets sono disponibili in [Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2). in questa sezione vengono fornite solo le informazioni specifiche del Bluetooth per ogni elemento di programmazione Windows Sockets.

Per un esempio completo, è anche possibile scaricare l' [esempio di connessione Bluetooth](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Bluetooth%20connection%20sample) .

Come per tutte le applicazioni Windows Sockets Programming, la funzione [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) deve essere chiamata per avviare la funzionalità Windows Sockets e abilitare Bluetooth.

Negli argomenti seguenti vengono fornite informazioni aggiuntive sull'utilizzo di funzioni e strutture Windows Sockets con l'API Bluetooth Microsoft:



| Argomento                                                                                            | Descrizione                                                                                                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Bluetooth e accetta](bluetooth-and-accept.md)                                                 | Bluetooth usa la funzione [**Accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) per abilitare i tentativi di connessione in ingresso in un socket.<br/>                                                                                                                                                                                                  |
| [Bluetooth e binding](bluetooth-and-bind.md)                                                     | Bluetooth usa la funzione di [**Binding**](/windows/desktop/api/winsock/nf-winsock-bind) per eseguire il binding a un socket.<br/>                                                                                                                                                                                                                                     |
| [Bluetooth e BLOB](bluetooth-and-blob.md)                                                     | Bluetooth usa la struttura [**BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob) per passare o ricevere dati specifici del trasporto alla struttura [**WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md) durante le chiamate alle funzioni [**WSASetService**](bluetooth-and-wsasetservice.md) o **WSALookupService** \* . <br/>             |
| [Bluetooth e Connetti](bluetooth-and-connect.md)                                               | Bluetooth usa la funzione [**Connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) per connettersi a un dispositivo Bluetooth di destinazione usando un Socket Bluetooth creato in precedenza.<br/>                                                                                                                                                              |
| [Bluetooth e funzione getaddrinfo](bluetooth-and-getaddrinfo.md)                                       | La funzione [**funzione getaddrinfo**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo) fornisce la conversione dal nome host all'indirizzo per i trasporti basati su IP.<br/>                                                                                                                                                                                   |
| [Bluetooth e getpeername](bluetooth-and-getpeername.md)                                       | Utilizzato per recuperare l'indirizzo Bluetooth del dispositivo Bluetooth peer.<br/>                                                                                                                                                                                                                                            |
| [Bluetooth e getsockname](bluetooth-and-getsockname.md)                                       | Bluetooth usa la funzione [**getsockname**](/windows/desktop/api/winsock/nf-winsock-getsockname) per recuperare l'indirizzo del dispositivo server e il numero di porta allocato a un socket tramite una chiamata precedente alla funzione di [**Binding**](/windows/desktop/api/winsock/nf-winsock-bind) .<br/>                                                                                            |
| [Bluetooth e getsockopt](bluetooth-and-getsockopt.md)                                         | Bluetooth usa la funzione [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) per eseguire una query sui diversi parametri associati al canale server o alla connessione. <br/>                                                                                                                                                           |
| [Bluetooth e ascolto, selezione e chiamata closesocket](bluetooth-and-listen-select-and-closesocket.md) | Bluetooth usa le funzioni [**Listen**](/windows/desktop/api/winsock2/nf-winsock2-listen), [**SELECT**](/windows/desktop/api/winsock2/nf-winsock2-select)e [**chiamata closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) senza alcuna modifica dalla programmazione standard di Windows Sockets.<br/>                                                                                                   |
| [Bluetooth e operazioni di lettura o scrittura](bluetooth-and-read-or-write-operations.md)             | Descrive le operazioni di lettura e scrittura Winsock supportate.<br/>                                                                                                                                                                                                                                                        |
| [Bluetooth e setsockopt](bluetooth-and-setsockopt.md)                                         | Bluetooth usa la funzione [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) per impostare vari parametri associati al canale server o alla connessione.<br/>                                                                                                                                                              |
| [Bluetooth e spegnimento](bluetooth-and-shutdown.md)                                             | Bluetooth usa la funzione [**Shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) per disconnettersi dalla radio remota.<br/>                                                                                                                                                                                                             |
| [Bluetooth e socket](bluetooth-and-socket.md)                                                 | Bluetooth usa la funzione [**socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) crea un socket per le connessioni in ingresso o in uscita.<br/>                                                                                                                                                                                               |
| [Opzioni Bluetooth e socket](bluetooth-and-socket-options.md)                                 | Informazioni dettagliate sulle opzioni di socket supportate da Microsoft Bluetooth.<br/>                                                                                                                                                                                                                                                    |
| [Bluetooth e WSAAddressToString](bluetooth-and-wsaaddresstostring.md)                         | Usato per convertire un indirizzo del dispositivo Bluetooth in una stringa, che a sua volta viene fornita alla funzione [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) tramite la struttura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) durante il recupero delle informazioni sul servizio del dispositivo.<br/>                                           |
| [Bluetooth e WSALookupServiceBegin](bluetooth-and-wsalookupservicebegin.md)                   | Bluetooth usa la funzione [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) per eseguire una query per i dispositivi e per individuare i servizi.<br/>                                                                                                                                                                         |
| [Bluetooth e WSALookupServiceNext](bluetooth-and-wsalookupservicenext.md)                     | Bluetooth usa la funzione [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) per trovare la corrispondenza con le query specificate in una precedente chiamata a [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina).<br/>                                                                                                           |
| [Bluetooth e WSALookupServiceEnd](bluetooth-and-wsalookupserviceend.md)                       | Bluetooth usa la funzione [**WSALookupServiceEnd**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend) per terminare una query avviata in una precedente chiamata a [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)ed eventualmente estesa nelle chiamate successive a [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta).<br/> |
| [Bluetooth e WSAQUERYSET](bluetooth-and-wsaqueryset.md)                                       | La struttura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) viene usata nelle operazioni di, tra cui richiesta di dispositivi, richiesta di assistenza e impostazione del servizio.<br/>                                                                                                                                                                |
| [Bluetooth e WSASetService](bluetooth-and-wsasetservice.md)                                   | Bluetooth usa la funzione [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) per registrare o rimuovere un'istanza del servizio nello spazio dei nomi Bluetooth (NS \_ BTH) dal registro di sistema.<br/>                                                                                                                                   |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

