---
description: Dopo che il socket è stato associato a un indirizzo IP e a una porta nel sistema, il server deve quindi restare in ascolto su tale indirizzo IP e sulla porta per le richieste di connessione in ingresso.
ms.assetid: 83c9f0e7-2e6d-449b-8d97-3d13154112cd
title: Ascolto su un socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6d6d98a13fc6e994fb5a264827b6b93047fd24e03d3e3f9953203b1fa15140f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119569781"
---
# <a name="listening-on-a-socket"></a>Ascolto su un socket

Dopo che il socket è stato associato a un indirizzo IP e a una porta nel sistema, il server deve quindi restare in ascolto su tale indirizzo IP e sulla porta per le richieste di connessione in ingresso.

## <a name="to-listen-on-a-socket"></a>Per restare in ascolto su un socket

Chiamare la [**funzione listen,**](/windows/desktop/api/Winsock2/nf-winsock2-listen) passando come parametri il socket creato e un valore per il *backlog,* la lunghezza massima della coda di connessioni in sospeso da accettare. In questo esempio il *parametro backlog* è stato impostato su **SOMAXCONN**. Questo valore è una costante speciale che indica al provider Winsock per questo socket di consentire un numero ragionevole massimo di connessioni in sospeso nella coda. Controllare il valore restituito per gli errori generali.


```C++
if ( listen( ListenSocket, SOMAXCONN ) == SOCKET_ERROR ) {
    printf( "Listen failed with error: %ld\n", WSAGetLastError() );
    closesocket(ListenSocket);
    WSACleanup();
    return 1;
}
```



Passaggio successivo: [Accettazione di una connessione](accepting-a-connection.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attività iniziali con Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Applicazione server Winsock](winsock-server-application.md)
</dt> <dt>

[Associazione di un socket](binding-a-socket.md)
</dt> </dl>

 

 



