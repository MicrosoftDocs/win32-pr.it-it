---
title: Bluetooth e accettare
description: Bluetooth usa la funzione accept per abilitare i tentativi di connessione in ingresso in un socket.
ms.assetid: 79708118-2f70-4759-b5d6-cf5cfc33c27e
keywords:
- Accettare
- Bluetooth
- Bluetooth
- Bluetooth e accettare
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c5f12a7fd9fee508354dfcd9421f830e814eed09bb207cc6024b50705cc3566
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004611"
---
# <a name="bluetooth-and-accept"></a>Bluetooth e accettare

Bluetooth usa la [**funzione accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) per abilitare i tentativi di connessione in ingresso su un socket. Il componente aggiuntivo BTH dell'applicazione client viene ottenuto leggendo Bluetooth sezione specifica del trasporto della struttura \_ [**sockaddr restituita.**](/windows/desktop/WinSock/sockaddr-2) L'uso **della funzione accept** con Bluetooth ha il formato seguente:

-   Il *parametro addr* della funzione [**accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) è un puntatore facoltativo a un buffer che riceve l'indirizzo dell'entità che si connette, noto al livello di comunicazione. Viene restituito un puntatore a una struttura [**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) con Bluetooth dispositivo remoto.
-   Il *parametro addrlen* della funzione [**accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) è un puntatore facoltativo a un integer che contiene la lunghezza, in byte, di addr. Il numero intero deve essere maggiore o uguale al valore **di sizeof** ([**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**Accettare**](/windows/desktop/api/winsock2/nf-winsock2-accept)
</dt> </dl>

 

 