---
description: Dopo che il socket è stato associato a un indirizzo IP e a una porta nel sistema, il server deve quindi restare in ascolto su tale indirizzo IP e la porta per le richieste di connessione in ingresso.
ms.assetid: 83c9f0e7-2e6d-449b-8d97-3d13154112cd
title: Ascolto su un socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48c36fe1718493d1b92ca52bb3c648ebd1aa5b0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306935"
---
# <a name="listening-on-a-socket"></a>Ascolto su un socket

Dopo che il socket è stato associato a un indirizzo IP e a una porta nel sistema, il server deve quindi restare in ascolto su tale indirizzo IP e la porta per le richieste di connessione in ingresso.

## <a name="to-listen-on-a-socket"></a>Per restare in attesa su un socket

Chiamare la funzione [**Listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) , passando come parametri il socket creato e un valore per il *backlog*, la lunghezza massima della coda di connessioni in sospeso da accettare. In questo esempio il parametro *backlog* è stato impostato su **SOMAXCONN**. Questo valore è una costante speciale che indica al provider Winsock per questo socket di consentire un numero massimo ragionevole di connessioni in sospeso nella coda. Controllare il valore restituito per gli errori generali.


```C++
if ( listen( ListenSocket, SOMAXCONN ) == SOCKET_ERROR ) {
    printf( "Listen failed with error: %ld\n", WSAGetLastError() );
    closesocket(ListenSocket);
    WSACleanup();
    return 1;
}
```



Passaggio successivo: [accettazione di una connessione](accepting-a-connection.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Introduzione con Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Applicazione server Winsock](winsock-server-application.md)
</dt> <dt>

[Associazione di un socket](binding-a-socket.md)
</dt> </dl>

 

 



