---
description: L' \_ opzione EXCLUSIVEADDRUSE socket impedisce ad altri socket di essere associati forzatamente allo stesso indirizzo e alla stessa porta.
ms.assetid: ce0d8188-54be-46e8-8753-d0680f690b84
title: Opzione socket SO_EXCLUSIVEADDRUSE (Winsock2. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90d4747150f918a7e9c4ce37ec209e7261d1a00c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306899"
---
# <a name="so_exclusiveaddruse-socket-option"></a>\_Opzione socket EXCLUSIVEADDRUSE

L' \_ opzione EXCLUSIVEADDRUSE socket impedisce ad altri socket di essere associati forzatamente allo stesso indirizzo e alla stessa porta.

## <a name="syntax"></a>Sintassi

L' \_ opzione EXCLUSIVEADDRUSE impedisce ad altri socket di essere associati forzatamente allo stesso indirizzo e alla stessa porta, una pratica abilitata dall' \_ opzione socket REUSEADDR. Tale riutilizzo può essere eseguito da applicazioni dannose per compromettere l'applicazione. L' \_ opzione EXCLUSIVEADDRUSE è molto utile per i servizi di sistema che richiedono una disponibilità elevata.

Nell'esempio di codice riportato di seguito viene illustrata l'impostazione di questa opzione.


```C++
#ifndef UNICODE
#define UNICODE
#endif

#ifndef WIN32_LEAN_AND_MEAN
#define WIN32_LEAN_AND_MEAN
#endif

#include <windows.h>
#include <winsock2.h>
#include <ws2tcpip.h>
#include <stdio.h>
#include <stdlib.h>             // Needed for _wtoi

#pragma comment(lib, "Ws2_32.lib")

int __cdecl wmain(int argc, wchar_t ** argv)
{
    WSADATA wsaData;
    int iResult = 0;
    int iError = 0;

    SOCKET s = INVALID_SOCKET;
    SOCKADDR_IN saLocal;
    int iOptval = 0;

    int iFamily = AF_UNSPEC;
    int iType = 0;
    int iProtocol = 0;

    int iPort = 0;

    // Validate the parameters
    if (argc != 5) {
        wprintf(L"usage: %ws <addressfamily> <type> <protocol> <port>\n", argv[0]);
        wprintf(L"    opens a socket for the specified family, type, & protocol\n");
        wprintf(L"    sets the SO_EXCLUSIVEADDRUSE socket option on the socket\n");
        wprintf(L"    then tries to bind the port specified on the command-line\n");
        wprintf(L"%ws example usage\n", argv[0]);
        wprintf(L"   %ws 0 2 17 5150\n", argv[0]);
        wprintf(L"   where AF_UNSPEC=0 SOCK_DGRAM=2 IPPROTO_UDP=17  PORT=5150\n",
                argv[0]);
        wprintf(L"   %ws 2 1 17 5150\n", argv[0]);
        wprintf(L"   where AF_INET=2 SOCK_STREAM=1 IPPROTO_TCP=6  PORT=5150\n", argv[0]);
        wprintf(L"   See the documentation for the socket function for other values\n");
        return 1;
    }

    iFamily = _wtoi(argv[1]);
    iType = _wtoi(argv[2]);
    iProtocol = _wtoi(argv[3]);

    iPort = _wtoi(argv[4]);

    if (iFamily != AF_INET && iFamily != AF_INET6) {
        wprintf(L"Address family must be either AF_INET (2) or AF_INET6 (23)\n");
        return 1;
    }

    if (iPort <= 0 || iPort >= 65535) {
        wprintf(L"Port specified must be greater than 0 and less than 65535\n");
        return 1;
    }
    // Initialize Winsock
    iResult = WSAStartup(MAKEWORD(2, 2), &wsaData);
    if (iResult != 0) {
        wprintf(L"WSAStartup failed with error: %d\n", iResult);
        return 1;
    }
    // Create the socket
    s = socket(iFamily, iType, iProtocol);
    if (s == INVALID_SOCKET) {
        wprintf(L"socket failed with error: %ld\n", WSAGetLastError());
        WSACleanup();
        return 1;
    }
    // Set the exclusive address option
    iOptval = 1;
    iResult = setsockopt(s, SOL_SOCKET, SO_EXCLUSIVEADDRUSE,
                         (char *) &iOptval, sizeof (iOptval));
    if (iResult == SOCKET_ERROR) {
        wprintf(L"setsockopt for SO_EXCLUSIVEADDRUSE failed with error: %ld\n",
                WSAGetLastError());
    }

    saLocal.sin_family = (ADDRESS_FAMILY) iFamily;
    saLocal.sin_port = htons( (u_short) iPort);
    saLocal.sin_addr.s_addr = htonl(INADDR_ANY);

    // Bind the socket
    iResult = bind(s, (SOCKADDR *) & saLocal, sizeof (saLocal));
    if (iResult == SOCKET_ERROR) {

        // Most errors related to setting SO_EXCLUSIVEADDRUSE
        //    will occur at bind.
        iError = WSAGetLastError();
        if (iError == WSAEACCES)
            wprintf(L"bind failed with WSAEACCES (access denied)\n");
        else
            wprintf(L"bind failed with error: %ld\n", iError);

    } else {
        wprintf(L"bind on socket with SO_EXCLUSIVEADDRUSE succeeded to port: %ld\n",
                iPort);
    }

    // cleanup
    closesocket(s);
    WSACleanup();

    return 0;
}

```



Per avere un effetto, l' \_ opzione EXCLUSIVADDRUSE deve essere impostata prima di chiamare la funzione [**Bind**](/windows/desktop/api/winsock/nf-winsock-bind) (questo vale anche per l' \_ opzione REUSEADDR). Nella tabella 1 sono elencati gli effetti dell'impostazione dell' \_ opzione EXCLUSIVEADDRUSE. Il carattere jolly indica il binding all'indirizzo jolly, ad esempio 0.0.0.0 per IPv4 e:: per IPv6. Specifico indica l'associazione a un'interfaccia specifica, ad esempio l'associazione di un indirizzo IP assegnato a un adapter. Specific2 indica l'associazione a un indirizzo specifico diverso dall'indirizzo associato a nel caso specifico.

> [!Note]  
> Il caso Specific2 è applicabile solo quando viene eseguita la prima operazione di binding con un indirizzo specifico. per il caso in cui il primo socket è associato al carattere jolly, la voce per specifico copre tutti i case di indirizzi specifici.

 

Si consideri, ad esempio, un computer con due interfacce IP: 10.0.0.1 e 10.99.99.99. Se la prima operazione di binding è 10.0.0.1 e la porta 5150 con il set di opzioni \_ EXCLUSIVEADDRUSE, il secondo binding a 10.99.99.99 e la porta 5150 con un set di opzioni any o no ha esito positivo. Tuttavia, se il primo socket è associato all'indirizzo con caratteri jolly (0.0.0.0) e alla porta 5150 con \_ EXCLUSIVEADDRUSE impostato, qualsiasi associazione successiva alla stessa porta, indipendentemente dall'indirizzo IP, avrà esito negativo con WSAEADDRINUSE (10048) o WSAEACCESS (10013), a seconda delle opzioni impostate nel secondo socket di binding.

### <a name="bind-behavior-with-various-options-set"></a>Associa il comportamento con varie opzioni impostate



Seconda associazione

Prima associazione

*\_EXCLUSIVEADDRUSE*

*Nessuna opzione* o *così \_ REUSEADDR*

*Jolly*

*Specifica*

*Jolly*

*Specifica*

$ {ROWSPAN3} $*così \_ EXCLUSIVEADDRUSE*$ {Remove} $  

*Jolly*

Non riuscito (10048)

Non riuscito (10048)

Non riuscito (10048)

Non riuscito (10048)

*Specifica*

Non riuscito (10048)

Non riuscito (10048)

Non riuscito (10048)

Non riuscito (10048)

*Specific2*

n/d

Operazione riuscita

n/d

Operazione riuscita

$ {ROWSPAN3} $*Nessuna opzione*$ {Remove} $  

*Jolly*

Non riuscito (10048)

Non riuscito (10048)

Non riuscito (10048)

Non riuscito (10048)

*Specifica*

Non riuscito (10048)

Non riuscito (10048)

Non riuscito (10048)

Non riuscito (10048)

*Specific2*

n/d

Operazione riuscita

n/d

Operazione riuscita

$ {ROWSPAN3} $*così \_ REUSEADDR*$ {Remove} $  

*Jolly*

Non riuscito (10013)

Non riuscito (10013)

Operazione completata\*

Operazione riuscita

*Specifica*

Non riuscito (10013)

Non riuscito (10013)

Operazione riuscita

Operazione completata\*

*Specific2*

n/d

Operazione riuscita

n/d

Operazione riuscita

\* Il comportamento non è definito per il socket che riceverà i pacchetti.



 

Nel caso in cui la prima operazione di binding non imposti opzioni \_ , quindi REUSEADDR e la seconda operazione di binding esegua una \_ REUSEADDR, il secondo socket avrà la porta e il comportamento che riguardano il socket che riceverà i pacchetti non è determinato. QUINDI \_ , EXCLUSIVEADDRUSE è stato introdotto per risolvere questa situazione.

\_Non è sempre possibile riutilizzare un socket con tale set EXCLUSIVEADDRUSE immediatamente dopo la chiusura del socket. Se, ad esempio, un socket di ascolto con il flag esclusivo impostato accetta una connessione dopo la quale il socket di ascolto viene chiuso, un altro socket non può essere associato alla stessa porta del primo socket di ascolto con il flag esclusivo fino a quando non è più attiva la connessione accettata.

Questa situazione può essere piuttosto complessa. anche se il socket è stato chiuso, è possibile che il trasporto sottostante non termini la connessione. Anche dopo la chiusura del socket, il sistema deve inviare tutti i dati memorizzati nel buffer, trasmettere una disconnessione normale al peer e attendere una disconnessione normale dal peer. È pertanto possibile che il trasporto sottostante non rilasci mai la connessione, ad esempio quando il peer annuncia una finestra di dimensioni pari a zero o altri attacchi di questo tipo. Nell'esempio precedente, il socket in ascolto è stato chiuso dopo l'accettazione di una connessione client. A questo punto, anche se la connessione client viene chiusa, è possibile che la porta non venga riutilizzata se la connessione client rimane in uno stato attivo a causa di dati non riconosciuti e così via.

Per evitare questa situazione, le applicazioni devono garantire un arresto normale: chiamare [**Shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) con il \_ flag di invio SD, quindi attendere il completamento di un ciclo [**ricezione**](/windows/desktop/api/winsock/nf-winsock-recv) fino a quando non vengono restituiti zero byte. In questo modo si evita il problema associato al riutilizzo delle porte, garantisce che tutti i dati siano stati ricevuti dal peer e assicura al peer che tutti i dati sono stati ricevuti correttamente.

L' \_ opzione così Linger può essere impostata su un socket per impedire che la porta si trovi in uno degli Stati di attesa attivi. Tuttavia, questa operazione è sconsigliata perché può causare effetti indesiderati, poiché può causare la reimpostazione della connessione. Se, ad esempio, i dati sono stati ricevuti ma non ancora riconosciuti dal peer e il computer locale chiude il socket con il \_ set Linger, la connessione viene reimpostata e il peer ignora i dati non riconosciuti. Inoltre, la scelta di un tempo appropriato per l'indugio è difficile. un valore troppo piccolo genera molte connessioni interrotte, mentre un timeout di grandi dimensioni può lasciare il sistema vulnerabile agli attacchi di tipo Denial of Service stabilendo molte connessioni e bloccando così numerosi thread dell'applicazione.

> [!Note]  
> Un socket che utilizza l' \_ opzione EXCLUSIVEADDRUSE deve essere arrestato correttamente prima di chiuderlo. In caso contrario, è possibile che si verifichi un attacco Denial of Service se il servizio associato deve essere riavviato.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                            |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Winsock2. h</dt> </dl> |



 

 




