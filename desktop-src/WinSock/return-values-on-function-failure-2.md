---
description: La costante manifesto SOCKET \_ ERROR viene fornita per controllare l'errore della funzione. Anche se l'uso di questa costante non è obbligatorio, è consigliabile. Nell'esempio seguente viene illustrato l'utilizzo della costante SOCKET \_ ERROR.
ms.assetid: b46203dc-5666-413b-90fe-8432318f3037
title: Valori restituiti in caso di errore della funzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b277da114c8c86c53339590eeff3e831cbaf2a4277765bf53047b3d07991b026
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117740933"
---
# <a name="return-values-on-function-failure"></a>Valori restituiti in caso di errore della funzione

La costante manifesto **SOCKET \_ ERROR viene fornita** per controllare l'errore della funzione. Anche se l'uso di questa costante non è obbligatorio, è consigliabile. Nell'esempio seguente viene illustrato l'utilizzo della **costante SOCKET \_ ERROR.**

Stile BSD tipico (non funziona in Windows)


```C++
        r = recv(ClientSocket, recvbuf, recvbuflen, 0);
        if (r == -1     /* or r < 0 */
            && errno == EWOULDBLOCK) {
            printf("recv failed with error: EWOULDBLOCK\n");
        }    
```



Windows Stile


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

[Codici di errore : errno, h \_ errno e WSAGetLastError](error-codes-errno-h-errno-and-wsagetlasterror-2.md)
</dt> <dt>

[Gestione degli errori di Winsock](handling-winsock-errors.md)
</dt> <dt>

[Porting di applicazioni socket in Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[Considerazioni sulla programmazione winsock](winsock-programming-considerations.md)
</dt> <dt>

[Windows Codici di errore dei socket](windows-sockets-error-codes-2.md)
</dt> </dl>

 

 



