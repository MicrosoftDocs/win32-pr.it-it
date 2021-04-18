---
description: Il codice di controllo acquisisce una prenotazione di runtime per un blocco di porte TCP o UDP.
ms.assetid: 1A2E3920-88D2-4109-B7EF-E66BD4AB6153
title: Codice di controllo SIO_ACQUIRE_PORT_RESERVATION
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 8eab53aeb945837b55c70560294b2fc295160a2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310429"
---
# <a name="sio_acquire_port_reservation-control-code"></a>Codice di controllo SIO_ACQUIRE_PORT_RESERVATION

## <a name="description"></a>Descrizione

Il codice di controllo della **\_ prenotazione della \_ porta \_ di acquisizione sio** acquisisce una prenotazione di runtime per un blocco di porte TCP o UDP.

Per eseguire questa operazione, chiamare la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** con i parametri seguenti.

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_ACQUIRE_PORT_RESERVATION, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to an INET_PORT_RANGE structure
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,             // pointer to an INET_PORT_RESERVATION_INSTANCE structure
  (DWORD) cbOutBuffer,   // size, in bytes, of the output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_ACQUIRE_PORT_RESERVATION, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to an INET_PORT_RANGE structure
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,             // pointer to a INET_PORT_RESERVATION_INSTANCE structure
  (DWORD) cbOutBuffer,   // size, in bytes, of the output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a>Parametri

### <a name="s"></a>s

Descrittore che identifica un socket.

### <a name="dwiocontrolcode"></a>dwIoControlCode

Codice di controllo per l'operazione.
Usare **la \_ \_ \_ prenotazione della porta di acquisizione sio**  per questa operazione.

### <a name="lpvinbuffer"></a>lpvInBuffer

Puntatore al buffer di input.
Questo parametro contiene un puntatore a una struttura di [**\_ \_ intervallo di porte inet**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_range) che specifica il numero del punto iniziale e il numero di porte da riservare.

### <a name="cbinbuffer"></a>cbInBuffer

Dimensione, in byte, del buffer di input.
Questo parametro deve corrispondere alla dimensione della struttura [**dell' \_ \_ intervallo di porte inet**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_range) .

### <a name="lpvoutbuffer"></a>lpvOutBuffer

Puntatore al buffer di output.
In caso di esito positivo, questo parametro contiene un puntatore a una struttura dell' [**\_ istanza di \_ prenotazione \_ della porta inet**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_instance) .

### <a name="cboutbuffer"></a>cbOutBuffer

Dimensione, in byte, del buffer di output.
Questo parametro deve essere pari almeno alla dimensione della struttura [**dell' \_ \_ \_ istanza di prenotazione della porta inet**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_instance) .

### <a name="lpcbbytesreturned"></a>lpcbBytesReturned

Puntatore a una variabile che riceve le dimensioni, in byte, dei dati archiviati nel buffer di output.

Se il buffer di output è troppo piccolo, la chiamata ha esito negativo, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) restituisce [**WSAEINVAL**](windows-sockets-error-codes-2.md)e il parametro *LpcbBytesReturned* punta a un valore **DWORD** pari a zero.

Se *lpOverlapped* è **null**, il valore **DWORD** a cui fa riferimento il parametro *lpcbBytesReturned* restituito per una chiamata con esito positivo non può essere zero.

Se il parametro *lpOverlapped* non è **null** per i socket sovrapposti, le operazioni che non possono essere completate immediatamente verranno avviate e il completamento verrà indicato in un secondo momento.
Il valore **DWORD** a cui fa riferimento il parametro *lpcbBytesReturned* restituito può essere zero perché non è possibile determinare la dimensione dei dati archiviati finché l'operazione sovrapposta non è stata completata.
Lo stato di completamento finale può essere recuperato quando il metodo di completamento appropriato viene segnalato al termine dell'operazione.

### <a name="lpvoverlapped"></a>lpvOverlapped

Puntatore a una struttura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .

Se il socket *s* è stato creato senza l'attributo Overlapped, il parametro *lpOverlapped* viene ignorato.

Se *s* è stato aperto con l'attributo Overlapped e il parametro *LpOverlapped* non è **null**, l'operazione viene eseguita come operazione sovrapposta (asincrona).
In questo caso, il parametro *lpOverlapped* deve puntare a una struttura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) valida.

Per le operazioni sovrapposte, la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** restituisce immediatamente un risultato e il metodo di completamento appropriato viene segnalato al completamento dell'operazione.
In caso contrario, la funzione non restituisce alcun risultato fino a quando l'operazione non viene completata o si verifica un errore.

### <a name="lpcompletionroutine"></a>Il lpCompletionRoutine

Tipo: \_ in_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)

Puntatore alla routine di completamento chiamata quando l'operazione è stata completata (ignorata per i socket non sovrapposti).

### <a name="lpthreadid"></a>lpThreadId

Puntatore a una struttura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) che deve essere usata dal provider in una chiamata successiva a **WPUQueueApc**.
Il provider deve archiviare la struttura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) a cui si fa riferimento (non il puntatore alla stessa) finché non viene restituito il risultato della funzione **WPUQueueApc** .

**Nota**  Questo parametro è valido solo per la funzione **WSPIoctl** .

### <a name="lperrno"></a>lpErrno

Puntatore al codice di errore.

**Nota**  Questo parametro è valido solo per la funzione **WSPIoctl** .

## <a name="return-value"></a>Valore restituito

Se l'operazione viene completata correttamente, la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** restituisce zero.

Se l'operazione ha esito negativo o è in sospeso, la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** restituisce un **\_ errore socket**.
Per ottenere informazioni estese sull'errore, chiamare [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).

| Codice di errore | Significato |
|------------|---------|
|**\_io WSA \_ in sospeso** | Operazione di I/O sovrapposta in corso. Questo valore viene restituito se un'operazione sovrapposta è stata avviata correttamente e il completamento verrà indicato in un secondo momento. |
| **\_operazione WSA \_ interrotta** | L'operazione di I/O è stata interrotta a causa dell'uscita di un thread o di una richiesta dell'applicazione. Questo errore viene restituito se un'operazione sovrapposta è stata annullata a causa della chiusura del socket o dell'esecuzione del comando IOCTL di **\_ scaricamento sio** . |
| **WSAEFAULT** | Il sistema ha rilevato un indirizzo puntatore non valido durante il tentativo di usare un argomento puntatore in una chiamata. Questo errore viene restituito dal parametro *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* o *il lpCompletionRoutine* non è interamente contenuto in una parte valida dello spazio degli indirizzi utente. |
| **WSAEINPROGRESS** | È in corso un'operazione di blocco. Questo errore viene restituito se la funzione viene richiamata quando è in corso un callback. |
| **WSAEINTR** | Un'operazione di blocco è stata interrotta da una chiamata a [**WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall). Questo errore viene restituito se un'operazione di blocco è stata interrotta. |
| **WSAEINVAL** | Argomento fornito non valido. Questo errore viene restituito se il parametro *dwIoControlCode* non è un comando valido o se un parametro di input specificato non è accettabile o se il comando non è applicabile al tipo di socket specificato. |
| **WSAENETDOWN** | Rete inattiva rilevata durante l'operazione del socket. Questo errore viene restituito se il sottosistema di rete non è riuscito. |
| **WSAENOTSOCK** | Si è tentato di eseguire un'operazione su un elemento che non è un socket. Questo errore viene restituito se il descrittore *s* non è un socket. |
| **ILWSAEOPNOTSUPP** | L'operazione tentata non è supportata per il tipo di oggetto a cui si fa riferimento. Questo errore viene restituito se il comando IOCTL specificato non è supportato. Questo errore viene restituito anche se il provider di trasporto IOCTL per la **\_ prenotazione della \_ porta \_ di acquisizione sio** non è supportato. Questo errore viene restituito anche quando un tentativo di usare l'IOCTL di **\_ prenotazione della \_ porta \_ di acquisizione sio** viene eseguito su un socket diverso da UDP o TCP. |

## <a name="remarks"></a>Commenti

Il IOCTL di **\_ prenotazione della \_ porta \_ di acquisizione sio**  è supportato in Windows Vista e nelle versioni successive del sistema operativo.

Le applicazioni e i servizi che devono riservare le porte rientrano in due categorie.
La prima categoria include i componenti che richiedono una determinata porta come parte dell'operazione.
Tali componenti preferiscono in genere specificare la porta richiesta al momento dell'installazione, ad esempio in un manifesto dell'applicazione.
La seconda categoria include i componenti che richiedono qualsiasi porta o blocco di porte disponibile in fase di esecuzione.
Queste due categorie corrispondono a richieste di prenotazione di porta specifiche e con caratteri jolly.
Richieste di prenotazione specifiche possono essere permanenti o Runtime, mentre le richieste di prenotazione di porta con caratteri jolly sono supportate solo in fase di esecuzione.

Per richiedere una prenotazione di runtime per un blocco di porte TCP o UDP, viene usato il comando di **\_ prenotazione della \_ porta \_ di acquisizione sio**  .
Per le prenotazioni di porte di runtime, il pool di porte richiede che le prenotazioni vengano utilizzate dal processo sul cui socket è stata concessa la prenotazione.
Le prenotazioni di porte di runtime durano solo fino a quando la durata del socket in cui è stata chiamata la **\_ porta di acquisizione \_ \_ sio**  è stata chiamata.
Al contrario, le prenotazioni di porte permanenti create utilizzando la funzione [**CreatePersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation) o [**CreatePersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation) possono essere utilizzate da qualsiasi processo con la possibilità di ottenere prenotazioni permanenti.

Una volta ottenuta una prenotazione della porta TCP o UDP di runtime, un'applicazione può richiedere le assegnazioni delle porte dalla prenotazione della porta aprendo un socket TCP o UDP, quindi chiamando la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) specificando il IOCTL di [**prenotazione della \_ \_ porta \_ di associazione sio**](sio-associate-port-reservation.md) e passando il token di prenotazione prima di emettere una chiamata alla funzione di binding sul socket.

Se entrambi i parametri *lpOverlapped* e *il lpCompletionRoutine* sono **null**, il socket in questa funzione verrà considerato come un socket non sovrapposto.
Per un socket non sovrapposto, i parametri *lpOverlapped* e *il lpCompletionRoutine* vengono ignorati, ad eccezione del fatto che la funzione può essere bloccata se socket *s* è in modalità di blocco.
Se il socket *s* è in modalità non di blocco, questa funzione verrà comunque bloccata poiché questo particolare IOCTL non supporta la modalità non di blocco.

Per i socket sovrapposti, le operazioni che non possono essere completate immediatamente verranno avviate e il completamento verrà indicato in un secondo momento.

Qualsiasi IOCTL può bloccarsi per un periodo illimitato, a seconda dell'implementazione del provider di servizi.
Se l'applicazione non è in grado di tollerare il blocco in una chiamata di funzione WSAIoctl o **WSPIoctl** , si consiglia di eseguire l'i/O sovrapposto per le IOCTL che sono particolarmente probabilmente bloccate.

Il codice IOCTL per la **prenotazione della porta di \_ acquisizione \_ \_ sio**  può non riuscire con l'operazione **WSAEINTR** o **WSA \_ \_ interrotta** nei casi seguenti:

* La richiesta viene annullata dal gestore di I/O.
* Il socket è chiuso.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene acquisita una prenotazione della porta di runtime, viene quindi creato un socket e viene allocata una porta dalla prenotazione della porta di runtime per il socket, quindi viene chiuso il socket e il rilascia la prenotazione della porta di Runtime.

```cpp
#ifndef UNICODE
#define UNICODE
#endif

#ifndef WIN32_LEAN_AND_MEAN
#define WIN32_LEAN_AND_MEAN
#endif

#include <Windows.h.>
#include <winsock2.h>
#include <mstcpip.h>
#include <ws2ipdef.h>
#include <stdio.h>
#include <stdlib.h>

// Need to link with Ws2_32.lib for Winsock functions
#pragma comment(lib, "ws2_32.lib")

int wmain(int argc, WCHAR ** argv)
{

    // Declare and initialize variables

    int startPort = 0;          // host byte order
    int numPorts = 0;
    USHORT startPortns = 0;     // Network byte order

    INET_PORT_RANGE portRange = { 0 };
    INET_PORT_RESERVATION_INSTANCE portRes = { 0 };

    unsigned long status = 0;

    WSADATA wsaData = { 0 };
    int iResult = 0;

    SOCKET sock = INVALID_SOCKET;
    int iFamily = AF_INET;
    int iType = 0;
    int iProtocol = 0;

    SOCKET sockRes = INVALID_SOCKET;

    DWORD bytesReturned = 0;

    // Note that the sockaddr_in struct works only with AF_INET not AF_INET6
    // An application needs to use the sockaddr_in6 for AF_INET6
    sockaddr_in service;
    sockaddr_in sockName;
    int nameLen = sizeof (sockName);

    // Validate the parameters
    if (argc != 6) {
        wprintf
            (L"usage: %s <addressfamily> <type> <protocol> <StartingPort> <NumberOfPorts>\n",
             argv[0]);
        wprintf(L"Opens a socket for the specified family, type, & protocol\n");
        wprintf
            (L"and then acquires a runtime port reservation for the protocol specified\n");
        wprintf(L"%ws example usage\n", argv[0]);
        wprintf(L"   %ws 2 2 17 5000 20\n", argv[0]);
        wprintf(L"   where AF_INET=2 SOCK_DGRAM=2 IPPROTO_UDP=17 StartPort=5000 NumPorts=20", argv[0]);

        return 1;
    }

    iFamily = _wtoi(argv[1]);
    iType = _wtoi(argv[2]);
    iProtocol = _wtoi(argv[3]);

    startPort = _wtoi(argv[4]);
    if (startPort < 0 || startPort > 65535) {
        wprintf(L"Starting point must be either 0 or between 1 and 65,535\n");
        return 1;
    }
    startPortns = htons((USHORT) startPort);

    numPorts = _wtoi(argv[5]);
    if (numPorts < 0) {
        wprintf(L"Number of ports must be a positive number\n");
        return 1;
    }

    portRange.StartPort = startPortns;
    portRange.NumberOfPorts = (USHORT) numPorts;

    // Initialize Winsock
    iResult = WSAStartup(MAKEWORD(2, 2), &wsaData);
    if (iResult != 0) {
        wprintf(L"WSAStartup failed with error = %d\n", iResult);
        return 1;
    }

    sock = socket(iFamily, iType, iProtocol);
    if (sock == INVALID_SOCKET) {
        wprintf(L"socket function failed with error = %d\n", WSAGetLastError());
        WSACleanup();
        return 1;
    } else {
        wprintf(L"socket function succeeded\n");

        iResult =
            WSAIoctl(sock, SIO_ACQUIRE_PORT_RESERVATION, (LPVOID) & portRange,
                     sizeof (INET_PORT_RANGE), (LPVOID) & portRes,
                     sizeof (INET_PORT_RESERVATION_INSTANCE), &bytesReturned, NULL, NULL);
        if (iResult != 0) {
            wprintf(L"WSAIoctl(SIO_ACQUIRE_PORT_RESERVATION) failed with error = %d\n",
                    WSAGetLastError());
            closesocket(sock);
            WSACleanup();
            return 1;
        } else {
            wprintf
                (L"WSAIoctl(SIO_ACQUIRE_PORT_RESERVATION) succeeded, bytesReturned = %u\n",
                 bytesReturned);
            wprintf(L"  Starting port=%d,  Number of Ports=%d, Token=%I64d\n",
                    htons(portRes.Reservation.StartPort),
                    portRes.Reservation.NumberOfPorts, portRes.Token);

            sockRes = socket(iFamily, iType, iProtocol);
            if (sockRes == INVALID_SOCKET) {
                wprintf(L"socket function for second socket failed with error = %d\n",
                        WSAGetLastError());
                closesocket(sock);
                WSACleanup();
                return 1;
            } else {
                wprintf(L"socket function for second socket succeeded\n");

                iResult =
                    WSAIoctl(sock, SIO_ASSOCIATE_PORT_RESERVATION,
                             (LPVOID) & portRes.Token, sizeof (ULONG64), NULL, 0,
                             &bytesReturned, NULL, NULL);
                if (iResult != 0) {
                    wprintf
                        (L"WSAIoctl(SIO_ASSOCIATE_PORT_RESERVATION) failed with error = %d\n",
                         WSAGetLastError());
                } else {
                    wprintf
                        (L"WSAIoctl(SIO_ASSOCIATE_PORT_RESERVATION) succeeded, bytesReturned = %u\n",
                         bytesReturned);

                    service.sin_family = (ADDRESS_FAMILY) iFamily;
                    service.sin_addr.s_addr = INADDR_ANY;
                    service.sin_port = 0;

                    iResult = bind(sock, (SOCKADDR *) & service, sizeof (service));
                    if (iResult == SOCKET_ERROR)
                        wprintf(L"bind failed with error = %d\n", WSAGetLastError());
                    else {
                        wprintf(L"bind succeeded\n");
                        iResult = getsockname(sock, (SOCKADDR *) & sockName, &nameLen);
                        if (iResult == SOCKET_ERROR)
                            wprintf(L"getsockname failed with error = %d\n",
                                    WSAGetLastError());
                        else {
                            wprintf(L"getsockname succeeded\n");
                            wprintf(L"Port number allocated = %u\n",
                                    ntohs(sockName.sin_port));
                        }
                    }
                }
            }

            // comment out this block of code if you don't want to delete the reservation just created
            iResult =
                WSAIoctl(sock, SIO_RELEASE_PORT_RESERVATION, (LPVOID) & portRes.Token,
                         sizeof (ULONG64), NULL, 0, &bytesReturned, NULL, NULL);
            if (iResult != 0) {
                wprintf
                    (L"WSAIoctl(SIO_RELEASE_PORT_RESERVATION) failed with error = %d\n",
                     WSAGetLastError());
            } else {
                wprintf
                    (L"WSAIoctl(SIO_RELEASE_PORT_RESERVATION) succeeded, bytesReturned = %u\n",
                     bytesReturned);
            }
        }

        if (sockRes != INVALID_SOCKET) {
            iResult = closesocket(sockRes);
            if (iResult == SOCKET_ERROR) {
                wprintf(L"closesocket for second socket failed with error = %d\n",
                        WSAGetLastError());
            }
        }
        if (sock != INVALID_SOCKET) {
            iResult = closesocket(sock);
            if (iResult == SOCKET_ERROR) {
                wprintf(L"closesocket for first socket failed with error = %d\n",
                        WSAGetLastError());
            }
        }
    }

    WSACleanup();

    return 0;
}
```

## <a name="see-also"></a>Vedi anche

[**accettare**](/windows/desktop/api/winsock2/nf-winsock2-accept)

[**associare**](/windows/desktop/api/winsock/nf-winsock-bind)

[**CreatePersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation)

[**CreatePersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation)

[**DeletePersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistenttcpportreservation)

[**DeletePersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistentudpportreservation)

[**\_intervallo di porte inet \_**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_range)

[**\_ \_ istanza prenotazione porta \_ inet**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_instance)

[**LookupPersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistenttcpportreservation)

[**LookupPersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistentudpportreservation)

[**\_ \_ prenotazione porta di associazione sio \_**](sio-associate-port-reservation.md)

[**\_ \_ prenotazione porta versione \_ sio**](sio-release-port-reservation.md)

[**presa**](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
