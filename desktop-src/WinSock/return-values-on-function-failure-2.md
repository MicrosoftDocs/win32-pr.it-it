---
description: "\\_Per verificare l'esito negativo della funzione, viene fornito l'errore di socket costante manifesto. Sebbene l'utilizzo di questa costante non sia obbligatorio, è consigliabile. Nell'esempio seguente viene illustrato l'utilizzo della costante di \\_ errore socket."
ms.assetid: b46203dc-5666-413b-90fe-8432318f3037
title: Valori restituiti sull'errore della funzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b94280d47d705833528c03c0d98a4a31232a0c6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226841"
---
# <a name="return-values-on-function-failure"></a>Valori restituiti sull'errore della funzione

Per verificare l'esito negativo della funzione, viene fornito l' **\_ errore di socket** costante manifesto. Sebbene l'utilizzo di questa costante non sia obbligatorio, è consigliabile. Nell'esempio seguente viene illustrato l'utilizzo della costante **di \_ errore socket** .

Stile BSD tipico (non funziona in Windows)


```C++
        r = recv(ClientSocket, recvbuf, recvbuflen, 0);
        if (r == -1     /* or r < 0 */
            && errno == EWOULDBLOCK) {
            printf("recv failed with error: EWOULDBLOCK\n");
        }    
```



Stile di Windows


```C++
        iResult = recv(ClientSocket, recvbuf, recvbuflen, 0);
        if (iResult == SOCKET_ERROR ) {
            iError = WSAGetLastError();
            if (iError == WSAEWOULDBLOCK)
                printf("recv failed with error: WSAEWOULDBLOCK\n");
            else
                printf("recv failed with error: %ld\n", iError);

            closesocket(ClientSocket);
            WSACleanup();
            return 1;
        }    
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Codici di errore-errno, h \_ errno e WSAGetLastError](error-codes-errno-h-errno-and-wsagetlasterror-2.md)
</dt> <dt>

[Gestione degli errori Winsock](handling-winsock-errors.md)
</dt> <dt>

[Porting delle applicazioni socket in Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[Considerazioni sulla programmazione Winsock](winsock-programming-considerations.md)
</dt> <dt>

[Codici di errore di Windows Sockets](windows-sockets-error-codes-2.md)
</dt> </dl>

 

 



