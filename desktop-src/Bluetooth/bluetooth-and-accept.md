---
title: Bluetooth e accetta
description: Bluetooth usa la funzione Accept per abilitare i tentativi di connessione in ingresso in un socket.
ms.assetid: 79708118-2f70-4759-b5d6-cf5cfc33c27e
keywords:
- accettare
- Bluetooth
- Bluetooth
- Bluetooth e accetta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28dff84ec05429411614e64a08ab159a5ee134b6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300343"
---
# <a name="bluetooth-and-accept"></a>Bluetooth e accetta

Bluetooth usa la funzione [**Accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) per abilitare i tentativi di connessione in ingresso in un socket. Il \_ valore addr BTH dell'applicazione client viene ottenuto leggendo la sezione specifica del trasporto Bluetooth della struttura [**sockaddr**](/windows/desktop/WinSock/sockaddr-2) restituita. L'uso della funzione **Accept** con Bluetooth ha il formato seguente:

-   Il parametro *addr* della funzione [**Accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) è un puntatore facoltativo a un buffer che riceve l'indirizzo dell'entità di connessione, come noto al livello di comunicazione. Viene restituito un puntatore a una struttura [**sockaddr \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) con l'indirizzo del dispositivo Bluetooth remoto.
-   Il parametro *addrlen* della funzione [**Accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) è un puntatore facoltativo a un Integer che contiene la lunghezza, in byte, di addr. Il valore integer deve essere maggiore o uguale al valore di **sizeof** ([**sockaddr \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**accettare**](/windows/desktop/api/winsock2/nf-winsock2-accept)
</dt> </dl>

 

 